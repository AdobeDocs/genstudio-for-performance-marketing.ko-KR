---
source-git-commit: f6a305c6a4e700525b570bbe280e5d1049d06537
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 6%

---
# 참조: 릴리스 노트 작성

## 프론트메터

라이브 페이지 [help/user-guide/release-notes.md](../../help/user-guide/release-notes.md)에 최소 집합(예: `TQID`, `product_v2`, `feature_v2`, 분류 ID) 이상의 Experience League 메타데이터가 포함되어 있습니다.

**규칙:**

- 릴리스 노트 **body** 콘텐츠를 편집할 때 작업에서 메타데이터 변경을 명시적으로 요청하지 않는 한 **기존 프론트마크와 값을 유지**&#x200B;합니다.
- 더 짧은 템플릿과 일치하도록 분류 또는 제품 메타데이터를 제거하지 마십시오.
- ExL 페이지의 필수 개념에는 일반적으로 `title`, `description` 및 `role`이(가) 포함됩니다. 새 페이지의 경우 [Experience League 메타데이터 지침](https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/using-metadata)을(를) 따르십시오.

## 내부 소스(KT 및 릴리스 Wiki)

**초안을 작성하는 동안에만 사용**. 게시된 릴리스 노트는 내부 문서를 참조해서는 안 됩니다.

### KT(Knowledge Transfer) 문서

다음에서 추출:

| 필드 | 사용 |
|-------|-----|
| 설명 | 핵심 기능 설명 |
| 엘리베이터 피치 | 가치 제안 |
| 기능 전달됨 | 구체적인 행동 |
| 문제 설명 | 사용자 불만 사항 |
| 릴리스 유형 및 날짜 | 타이밍 |

### Wiki 페이지 릴리스

그룹화 기준:

| 필드 | 사용 |
|-------|-----|
| 릴리스 날짜(수정 버전) | 동일한 일자 → 동일한 릴리스 노트 배치 |
| 이니셔티브 | 컨텍스트만 해당, 공개 텍스트에서 내부적으로 링크하지 않음 |
| PM은 KT를 사용하여 기능을 제공합니다 | 더 자세한 KT 세부 정보가 존재할 수 있는 신호 |

**범위 규칙:** 릴리스 날짜(수정 버전)가 같은 항목이 같은 월별 릴리스 블록에 속합니다.

## 설명서 연결

- **가장 관련성이 높은** 구문에 대한 링크(예: 광고 형식 섹션에 &quot;지원되지 않는 이미지 및 비디오 자산&quot; 링크).
- `#anchor`개의 링크를 올바른 하위 섹션으로 선호합니다.
- 개요 페이지는 더 깊은 앵커가 존재하지 않을 때 사용할 수 있습니다.

## 공통 설명서 경로

| 영역 | 경로 접두사 |
|------|-------------|
| 만들기 | `/help/user-guide/create/` |
| 콘텐츠 | `/help/user-guide/content/` |
| 활성화 | `/help/user-guide/activation/` |
| 승인 | `/help/user-guide/approvals/` |
| Insights | `/help/user-guide/insights/` |
| 지침 | `/help/user-guide/guidelines/` |
| 템플릿 | `/help/user-guide/templates/` |
| 캠페인 | `/help/user-guide/campaigns/` |
| 확장성 | `/help/extensibility/` |
