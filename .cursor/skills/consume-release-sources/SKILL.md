---
name: consume-release-sources
description: ""
source-git-commit: c3c6aa86f4f520d020f8928612d1be6be1599652
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# 릴리스 소스 사용(Jira + Confluence MCP)

**다운스트림 초안 작성:** [generate-release-notes](../generate-release-notes/SKILL.md) → 옵션 [polish-release-notes](../polish-release-notes/SKILL.md)

**구문 분석 참조:** [reference.md](reference.md)

**대상 출력 파일(다운스트림만 해당):** [help/user-guide/release-notes.md](../../help/user-guide/release-notes.md)

## 사전 요구 사항

- **Jira MCP**(`jira_getIssue`, `jira_searchIssues`) 인증됨
- **Confluence MCP**(`confluence_getContent`, `confluence_searchContent`) 인증됨
- 지점 이름(`GS-#####`), 사용자 입력 또는 티켓 설명의 JIRA 티켓 키

## 워크플로우 체크리스트

1. [ ] **Jira 티켓 확인** — `jira_getIssue`(`issueKey` 포함). 행사 위키 링크 및 릴리스 월은 `description`을(를) 읽어 보십시오.
2. [ ] **의식 페이지 찾기** — 티켓에서 Wiki URL을 사용합니다. 대체 CQL: `title ~ "YYYY/MM Release Ceremony" AND space = GenStudio`.
3. [ ] **예식 본문 가져오기** — `bodyMode: storage`이(가) 있는 `confluence_getContent`(필수, `text`은(는) KT 링크와 테이블 구조를 잃게 됨).
4. [ ] **기능 그룹 구문 분석** — **GA 릴리스 기능** 및 **Beta 릴리스 기능**&#x200B;에서 행을 추출합니다([reference.md](reference.md#ceremony-feature-groups) 참조).
5. [ ] **포함 필터 적용** — 사용자 범위별([reference.md](reference.md#inclusion-filters) 참조); Beta 행 수 확인(0일 수 있음).
6. [ ] **KT 페이지 확인** — KT 제목당 `confluence_searchContent`; `confluence_getContent`, `bodyMode: text`.
7. [ ] **KT 필드 추출** — 설명, 엘리베이터 피치, 제공된 기능, 문제 설명, 릴리스 유형 및 날짜.
8. [ ] **Beta 플래그 설정** — `Beta` 유형의 Beta 섹션 행 또는 GA 테이블 행에 대한 `requiresBetaBadge: true`.
9. [ 구조화된 행 목록이 있는 ] **전달**&#x200B;을(를) [generate-release-notes](../generate-release-notes/SKILL.md)로 보냅니다(전송된 복사본에 wiki/Jira 참조 없음).

## Beta 레이블 지정(스킬 생성을 위한 전달)

`requiresBetaBadge: true`일 때 다운스트림 `###` 섹션은 제목 바로 아래에 을 포함해야 합니다.

```markdown
[!BADGE Beta]{type=Informative tooltip="This feature is currently in Beta, so some functionality may be limited or subject to change."}
```

Beta에 대해 기울임꼴 예약 면책조항을 추가하지 마십시오. 배지는 지원되는 패턴입니다.

## 배송된 릴리스 노트에서 금지됨

내부 ID, Wiki URL, KT 인용 및 Jira 키는 이 수집 단계에서만 유지됩니다. [generate-release-notes 금지된 콘텐츠](../generate-release-notes/SKILL.md#prohibited-content)에 따라 공개 페이지에서 사용자 대면 결과를 요약합니다.

## 대체

MCP 호출이 실패할 경우 사용자에게 세리머니와 KT 콘텐츠를 붙여 넣도록 요청한 다음 [reference.md KT 필드 매핑](../generate-release-notes/reference.md#internal-sources-kt-and-release-wikis)을 사용하여 릴리스 정보 생성을 계속합니다.

## 추가 리소스

- [reference.md](reference.md) — 식 구문 분석, CQL, 포함 필터, MCP 매개 변수
- [generate-release-notes](../generate-release-notes/SKILL.md) — 보관, 초안, 링크, 품질 검사
- [polish-release-notes](../polish-release-notes/SKILL.md) — `{#latest}` 아래 새 `###`에 대한 에디토리얼 패스
