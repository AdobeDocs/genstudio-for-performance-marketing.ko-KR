---
title: AI Assistant 도구 참조
description: AI 도우미가 [!DNL GenStudio for Performance Marketing]과(와) 함께 사용할 수 있는 인사이트, 만들기, 활성화 및 피드백 도구에 대해 알아봅니다.
role: User
source-git-commit: 6fb7ddb7549ea6bcd66b6139fbde9ebe12ddaa22
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 15%
---

# AI 지원 도구 참조

이 참조는 연결된 AI 도우미가 [!DNL GenStudio for Performance Marketing]에서 사용할 수 있는 도구에 대해 설명합니다. 사용 가능한 도구 목록은 조직의 구성에 따라 다릅니다.

워크플로우를 시작하기 전에 액세스할 수 있는 도구를 AI 도우미에 문의하십시오.

## 기능 영역

| 영역 | 용도 | 비헤이비어 |
|---|---|---|
| Insights | 유료 미디어 성능을 쿼리하고 크리에이티브 권장 사항을 검색합니다. | 읽기 전용. |
| 만들기 | Express 템플릿 또는 Insights 권장 사항에서 초안을 조합한 다음 검토를 관리합니다. | 읽고 쓰세요. Creative Cloud에서 문서를 만듭니다. |
| 활성화 | 게시 대상을 해결하고 승인된 경험을 게시합니다. | 쓰기 및 삭제 라이브 광고를 게시하여 광고 비용을 발생시킬 수 있습니다. |
| 피드백 | [!DNL GenStudio for Performance Marketing] 팀에 제품 피드백을 보냅니다. | 쓰세요. |

대부분의 Insights 도구는 `meta`, `linkedin` 및 `innovid`을(를) 포함합니다. 전환 지표 도구는 `meta` 및 `linkedin`을(를) 포함합니다.

만들기는 `meta`, `linkedin`, `display`, `tiktok` 및 `youtube`을(를) 지원합니다. 활성화는 `META`, `LINKEDIN` 및 `GOOGLECM360`을(를) 지원합니다.

## Insights 도구

### get_insights_capabilities

조직에 대해 활성화된 Insights 채널, 작업 및 사용자 지정 전환 지표를 반환합니다. 가용성이 명확하지 않은 경우 먼저 이 도구를 사용하십시오.

이 도구는 캠페인, 광고 또는 지표 값이 아닌 기능 메타데이터를 반환합니다.

### get_insights_summary

선택한 날짜 범위 동안 한 채널에 대한 헤드라인 성능 지표 및 트렌드를 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `meta`, `linkedin` 또는 `innovid`. |
| `startDate` | 아니요 | `YYYY-MM-DD` 형식의 시작 날짜입니다. 기본값은 30일 전입니다. |
| `endDate` | 아니요 | 종료 날짜는 `YYYY-MM-DD` 형식입니다. 기본값은 오늘입니다. |
| `metrics` | 아니요 | `spend`, `ctr`, `cpc`, `cpm`, `impressions`, `clicks` 또는 `conversions`과(와) 같이 차트로 작성할 지표입니다. |

### list_insights_campaigns

캠페인 성과 지표 및 합계 행의 정렬 가능한 테이블을 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `meta`, `linkedin` 또는 `innovid`. |
| `startDate`, `endDate` | 아니요 | `YYYY-MM-DD` 형식의 날짜 범위입니다. 기본값은 지난 30일입니다. |
| `search` | 아니요 | 캠페인 이름 필터. |
| `sortBy` | 아니요 | 정렬 필드(예: `spend`, `impressions`, `clicks`, `ctr`, `cpc`, `cpm` 또는 `name`). |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. |

### list_insights_ads

광고 수준 성능을 반환합니다. 정렬 가능한 테이블의 기본 찾아보기 모드나 성과가 높은 광고 및 낮은 광고의 계층 모드를 사용합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `meta`, `linkedin` 또는 `innovid`. |
| `tier` | 아니요 | `all`, `high` 또는 `low`. 기본값은 `all`입니다. |
| `mainMetric` | 조건부 | `high` 또는 `low` 계층 모드에 필요한 순위 지표입니다. |
| `campaigns` | 아니요 | 결과를 제한하는 데 사용되는 캠페인 식별자. |
| `search` | 아니요 | 광고 이름 필터. |
| `startDate`, `endDate` | 아니요 | `YYYY-MM-DD` 형식의 날짜 범위입니다. |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. |

계층 모드는 `get_insights_ad_attributes`에 필요한 광고 식별자를 반환합니다.

### get_insights_ad_details

복사, call to action, 에셋 및 배치를 포함한 하나의 광고에 대한 크리에이티브 메타데이터를 반환합니다. 성능 지표는 반환하지 않습니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `meta`, `linkedin` 또는 `innovid`. |
| `accountId` | 예 | 유료 미디어 계정 식별자. |
| `campaignId` | 예 | 캠페인 식별자. |
| `adId` | 예 | 광고 식별자. |
| `adgroupId` | 아니요 | 채널이 광고 그룹을 사용하는 경우 광고 그룹 식별자. |

### get_insights_ad_attributes

선택한 광고의 크리에이티브 트레이트를 채널 평균과 비교합니다. `list_insights_ads`이(가) 성과가 높은 광고 또는 성과가 낮은 광고를 식별한 후에 사용합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `ads` | 예 | `list_insights_ads`에서 반환된 식별자를 포함하여 설명할 광고입니다. |
| `mainMetric` | 예 | 광고 등급을 매기는 데 사용되는 지표. |
| `campaigns` | 아니요 | 비교 모집단을 정의하는 데 사용되는 캠페인 식별자. |
| `startDate`, `endDate` | 아니요 | `YYYY-MM-DD` 형식의 날짜 범위입니다. |

### get_insights_tag_categories

요청한 기간 동안 조직에서 사용할 수 있는 태그 범주를 반환합니다. 성능 지표가 아닌 카테고리 이름을 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channels` | 예 | 하나 이상의 지원되는 채널. |
| `startDate`, `endDate` | 아니요 | `YYYY-MM-DD` 형식의 날짜 범위입니다. |

### get_insights_ad_tags

제품, 지역 또는 크리에이티브 테마와 같은 한 범주 내에서 태그 값별로 성능을 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `meta`, `linkedin` 또는 `innovid`. |
| `tagCategory` | 예 | `get_insights_tag_categories`이(가) 반환한 범주 |
| `tagSource` | 아니요 | `ad_tags` 또는 `campaign_tags`. |
| `sortBy` | 아니요 | 결과 정렬에 사용되는 지표. |
| `search` | 아니요 | 태그 값 필터. |
| `startDate`, `endDate` | 아니요 | `YYYY-MM-DD` 형식의 날짜 범위입니다. |

### get_insights_custom_metrics

조직에 대해 구성된 사용자 지정 전환 지표를 반환합니다. `get_insights_conversion_metrics` 전에 사용하세요.

이 도구는 지표 값이 아닌 지표 식별자를 반환합니다.

### get_insights_conversion_metrics

Meta 및 LinkedIn에 대해 구성된 전환 지표 값 및 트렌드를 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channels` | 아니요 | 지원되는 전환 채널입니다. 기본값은 `meta`입니다. |
| `metrics` | 아니요 | `get_insights_custom_metrics`이(가) 반환한 지표 식별자입니다. |
| `campaigns` | 아니요 | 결과를 제한하는 데 사용되는 캠페인 식별자. |
| `startDate`, `endDate` | 아니요 | `YYYY-MM-DD` 형식의 날짜 범위입니다. |

### get_insights_recommendations

조직의 성과 데이터에 기반을 둔 제안된 창의적 변경 사항을 반환합니다. 선택한 범위에 적합한 광고가 포함되지 않은 경우 요청은 권장 사항을 반환하지 않을 수 있습니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channels` | 예 | 하나 이상의 지원되는 채널. |
| `campaigns` | 아니요 | 결과를 제한하는 데 사용되는 캠페인 식별자. |
| `search` | 아니요 | 캠페인 이름 필터. |
| `recommendationId` | 아니요 | 한 개의 추천을 자세히 검색하는 데 사용되는 식별자. |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. |

## 도구 만들기

도구를 만들면 Adobe Express 템플릿에서 초안을 조합하고 경험을 활성화하기 전에 검토를 관리할 수 있습니다.

### list_express_templates

필터링 및 패싯 카운트와 함께 사용 가능한 Express 템플릿을 나열합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 아니요 | `meta`, `display`, `linkedin`, `tiktok`, `youtube` 또는 `__unspecified__`. |
| `query` | 아니요 | 템플릿 검색어. |
| `aspectRatios`, `keywords`, `languages`, `mediaFormat`, `regions`, `timeframes` | 아니요 | 템플릿 Facet 필터. |
| `sortBy`, `order` | 아니요 | 필드 및 순서를 정렬합니다. |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. |

### describe_express_template

템플릿에서 편집 가능한 텍스트 필드 및 이미지 배치를 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `templateId` | 예 | 빠른 템플릿 식별자. |

### list_cta_options

채널에 대해 허용되는 call-to-action 값을 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `linkedin`, `meta`, `display`, `tiktok` 또는 `youtube`. |

### create_draft

하나 이상의 경험이 포함된 빠른 템플릿에서 편집 가능한 초안을 만듭니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `templateId` | 예 | 빠른 템플릿 식별자. |
| `prompt` | 예 | Creative은 초안과 함께 저장된 지침을 간략히 설명하고 복사합니다. |
| `experiences` | 예 | 각 경험에 대한 채널, 콘텐츠 필드 및 선택적 템플릿 필드 재정의. |
| `name` | 아니요 | 문서 이름. |

고정 call-to-action 값이 있는 채널의 초안을 만들기 전에 `list_cta_options`을(를) 사용하십시오.

### create_draft_from_recommendation

특정 Insights 권장 사항에서 편집 가능한 초안을 만듭니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `meta` 또는 `linkedin`. |
| `adUid` | 예 | `get_insights_recommendations`이(가) 반환한 권장 사항 식별자. |
| `prompt` | 예 | 권장 사항을 기반으로 한 Creative 개요. |
| `name` | 아니요 | 문서 이름. |

### list_recent_draft

최근 Express 템플릿 초안을 상태 및 링크와 함께 나열합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. |

### get_draft_metadata

초안의 이름, 채널, 승인 상태, 검토자 결과 및 공동 작업자 액세스를 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `draftId` | 예 | 초안 자산 식별자. |

### share_draft

공동 작업자에게 승인 요청 없이 초안에 대한 보기 또는 편집 액세스 권한을 부여합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `draftId` | 예 | 초안 자산 식별자. |
| `emails` | 예 | 하나 이상의 공동 작업자 이메일 주소. |
| `role` | 예 | `editor` 또는 `viewer`. |
| `message` | 아니요 | 초대 메시지. |

### request_draft_approval

하나 이상의 사용자에게 초안을 보내어 승인합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `draftId` | 예 | 초안 자산 식별자. |
| `emails` | 예 | 하나 이상의 검토자 이메일 주소. |

### list_experiences

활성화하기 위해 준비된 승인되고 게시된 경험을 반환합니다. 초안은 포함되지 않습니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 아니요 | 경험 채널 필터. |
| `createdByMe` | 아니요 | 현재 사용자가 만든 경험으로 결과를 제한합니다. |
| `campaignNames` | 아니요 | 정확한 캠페인 이름 필터. |
| `creatorEmail` | 아니요 | 작성자 이메일 필터. |
| `createdAtFrom`, `createdAtTo` | 아니요 | 생성 날짜 범위입니다. |
| `language` | 아니요 | BCP 47 언어 태그. |
| `limit`, `cursor` | 아니요 | 페이지 크기 및 페이지 매김 커서입니다. |

## 도구 활성화

도구 활성화 유료 미디어 타겟을 해결하고 승인된 경험을 게시합니다. 게시는 이러한 도구를 통해 되돌릴 수 없으며 광고 비용이 발생할 수 있습니다.

### configure_activation_target

필요한 경우 유료 미디어 계정, 캠페인, 광고 세트 및 Facebook 페이지를 확인하고 확인합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `platform` | 예 | `META`, `LINKEDIN` 또는 `GOOGLECM360`. |
| `platformAccountId` | 아니요 | 유료 미디어 계정 식별자. 계정을 검색하려면 생략합니다. |
| `campaignId` | 아니요 | Meta 또는 LinkedIn용 Campaign 식별자. |
| `adsetId` | 아니요 | Meta 광고 세트 또는 LinkedIn 캠페인 식별자. |
| `pageId` | 아니요 | Meta용 Facebook 페이지 식별자. |

### create_activation

승인된 경험과 검증된 타겟의 라이브 단일 이미지 광고를 게시합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `platform` | 예 | `META`, `LINKEDIN` 또는 `GOOGLECM360`. |
| `targetId` | 예 | `configure_activation_target`이(가) 반환한 대상을 확인했습니다. |
| `experienceId` | 예 | `list_experiences`이(가) 반환한 승인된 경험 식별자입니다. |
| `assetId` | 아니요 | 여러 적격한 변형이 있는 경험에 대한 변형 식별자. |
| `name` | 아니요 | 광고 배치 표시 이름. |

`create_activation`을(를) 두 번 호출하면 첫 번째 광고를 업데이트하는 대신 두 개의 별도 광고가 만들어집니다.

## 피드백 도구

### submit_mcp_feedback

[!DNL GenStudio for Performance Marketing] 팀에 도구 또는 워크플로에 대한 피드백을 보냅니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `category` | 예 | `bug`, `feature_request` 또는 `workflow_friction`. |
| `comment` | 예 | 피드백에 대한 간결한 설명. |
| `tags` | 아니요 | 피드백을 분류하는 데 사용되는 태그. |
| `tool_name` | 아니요 | 피드백과 연계된 도구. |

## 일반 워크플로우

한 도구가 다른 도구에 대해 식별자나 구성을 제공할 때 다음 시퀀스를 사용합니다.

- **광고 진단:** `high` 또는 `low` 계층 모드에서 `list_insights_ads`을(를) 호출한 다음 같은 순위 지표로 `get_insights_ad_attributes`을(를) 호출합니다.
- **태그별 분석:** `get_insights_tag_categories`을(를) 호출한 다음 반환된 범주로 `get_insights_ad_tags`을(를) 호출합니다.
- **전환 지표를 검토합니다.** `get_insights_custom_metrics`을(를) 호출한 다음 반환된 지표 식별자를 사용하여 `get_insights_conversion_metrics`을(를) 호출합니다.
- **권장 사항을 초안으로 전환합니다.** `get_insights_recommendations`을(를) 호출한 다음 `create_draft_from_recommendation`을(를) 호출합니다.
- **템플릿에서 빌드:** `list_express_templates`, `describe_express_template` 및 `list_cta_options`을(를) 호출한 다음 `create_draft`을(를) 호출합니다.
- **승인된 환경을 게시합니다.** `list_experiences`을(를) 호출한 다음 `configure_activation_target` 및 `create_activation`을(를) 호출합니다.

## 관련 기능

- [AI 지원 개요](overview.md)
- [AI 지원 연결](connect-ai-assistants.md)
- [AI 지원 사용](use-ai-assistants.md)
