---
source-git-commit: c3c6aa86f4f520d020f8928612d1be6be1599652
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 3%

---
# 참조: use release sources (MCP)

## 의식 페이지 검색

| 패턴 | 예 |
|---------|---------|
| 제목 | **GenStudio** 스페이스의 `YYYY/MM Release Ceremony` |
| Jira에서 | 티켓 `description`의 Wiki 링크(기본 설정) |
| CQL 폴백 | `title ~ "2026/06 Release Ceremony" AND space = GenStudio` |

## 의식 기능 그룹

릴리스 기념식 Wiki에는 최대 **두 개**&#x200B;개의 기능 테이블이 있습니다. **storage** HTML에서 모두 구문 분석합니다.

### GA 릴리스 기능

- 섹션 제목: `GA Release Features`(`<h2>`)
- 소제목: `Feature Group:`(선택적 Floodgate 링크 포함)
- 테이블 열에는 **Type**(`GA`, `Limited`, `EA`, `Beta` 또는 비어 있음)이 포함됩니다.
- **KT 설명서** 열: `<ac:link><ri:page ri:content-title="..."/></ac:link>`

행당 추출:

| 필드 | 소스 |
|-------|--------|
| `featureDescription` | 데이터 행의 처음 `<td>` |
| `type` | 열 셀 텍스트 입력 |
| `ktPageTitle` | KT 열의 `ri:content-title` |
| `jiraKeys` | `ac:macro ac:name="jira"` → `key` 매개 변수(내부만) |
| `releaseTier` | 형식이 `GA`인 경우 `ga`; 다른 GA 테이블 값에 대해 형식 상속 |

### Beta 릴리스 기능

- 섹션 제목: `Beta Release Features`(일부 달에는 **없음**&#x200B;일 수 있음)
- 두 번째 테이블, **유형 열 없음** — 모든 행은 Beta입니다.
- GA 테이블과 동일한 KT 및 Jira 추출
- 모든 Beta 섹션 행에서 `releaseTier: beta` 및 `requiresBetaBadge: true` 설정

Beta 섹션이 누락된 경우 Beta 행을 0으로 기록하고 계속합니다.

### 스토리지 HTML 패턴

```html
<ac:link><ri:page ri:content-title="Translation on HZ Canvas" /></ac:link>
<ac:structured-macro ac:name="jira" ...><ac:parameter ac:name="key">GS-23218</ac:parameter></ac:structured-macro>
```

## MCP 도구 사용

| 단계 | 도구 | 매개변수 |
|------|------|------------|
| 티켓 | `jira_getIssue` | `issueKey`, 선택적 `expand: renderedFields` |
| 의식 | `confluence_getContent` | `contentId`, `bodyMode: storage` |
| KT 조회 | `confluence_searchContent` | `cql: title = "<KT title>" AND space = GenStudio` |
| 본문 | `confluence_getContent` | `contentId`, `bodyMode: text`, `maxBodyChars: 50000` |

**KT 링크를 구문 분석할 때 의식 페이지에 `bodyMode: text`을(를) 사용하지 마십시오**.

## KT 필드 매핑(입력 드래프팅)

생성 릴리스 정보에 매핑합니다. 공개 릴리스 정보에 축어적으로 붙여넣지 마십시오.

| 섹션 | 사용 |
|------------|-----|
| 설명 | 핵심 기능 |
| 엘리베이터 피치 | 가치 제안 |
| 기능 전달됨 | 구체적인 행동 |
| 문제 설명 | 사용자 불만(컨텍스트만) |
| 릴리스 유형 및 날짜 | GA/Beta/제한적(내부), 드라이브 배지 결정 |

## 포함 필터

명확하지 않은 경우 사용자와 범위를 확인합니다. 일반 사전 설정:

| 사전 설정 | 포함 |
|--------|----------|
| `ga_only` | Type = `GA`인 GA 테이블 행 |
| `ga_and_beta` | **향후 달에 대한 권장 기본값** — 유형 = `GA` **더하기 모두** Beta 릴리스 기능 테이블 행인 GA 행 |
| `ga_plus_empty` | GA 테이블: 유형 = `GA` 또는 빈 유형 |
| `all_except_pilot` | `Limited`을(를) 제외한 GA 테이블 행, `ga_and_beta`을(를) 사용할 때 Beta 섹션 추가 |
| `all_with_badges` | 모든 GA 테이블 행, Beta 섹션 행은 항상 Beta 배지를 받습니다 |

## Beta 배지 핸드오프

| 조건 | `requiresBetaBadge` |
|-----------|---------------------|
| **Beta 릴리스 기능** 테이블의 행 | `true` |
| 유형 = `Beta`인 GA 테이블 행 | `true` |
| 유형 = `GA`인 GA 테이블 행 | `false` |

다운스트림: [generate-release-notes 결정 규칙](../generate-release-notes/SKILL.md#decision-rules) 및 [Beta 배지 조각](../generate-release-notes/SKILL.md#beta-badge).

## 핸드오프 페이로드(비공식)

항목 목록으로 릴리즈 노트를 생성하려면 전달:

```yaml
- featureDescription: "YouTube Shorts"
  releaseTier: ga
  requiresBetaBadge: false
  ktPageTitle: "YouTube Shorts (Create + Activate)"
  # extracted KT fields: description, elevatorPitch, featuresDelivered, ...
```
