---
title: AI Assistant 도구 참조
description: AI 도우미가 [!DNL GenStudio for Performance Marketing]과(와) 함께 사용할 수 있는 인사이트, 만들기, 계획, 활성화 및 피드백 도구에 대해 알아봅니다.
role: User
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
    internal-label: GenStudio for Performance Marketing
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 244293cf4f83acbc252f1d5f3495db403ed4a9bb
workflow-type: tm+mt
source-wordcount: '2265'
ht-degree: 13%
---

# AI 지원 도구 참조

이 참조는 연결된 AI 도우미가 [!DNL GenStudio for Performance Marketing]에서 사용할 수 있는 도구에 대해 설명합니다. 사용 가능한 도구 목록은 조직의 구성에 따라 다릅니다.

워크플로우를 시작하기 전에 액세스할 수 있는 도구를 AI 도우미에 문의하십시오.

## 기능 영역

| 영역 | 용도 | 비헤이비어 |
|---|---|---|
| Insights | 유료 미디어 및 이메일 성능을 쿼리하고 크리에이티브 추천을 검색합니다. | 읽기 전용. |
| 만들기 | 에셋을 찾고 빠른 템플릿 또는 인사이트 추천에서 초안을 조합한 다음 검토를 관리합니다. | 읽고 쓰세요. Creative Cloud에서 문서를 만듭니다. |
| 플랜 | 개요에서 캠페인 세부 사항을 추출하여 Workfront Planning에 저장합니다. | 추출은 읽기 전용입니다. 저장하면 Workfront Planning에 레코드가 생성되며 자동으로 롤백할 수 없습니다. |
| 활성화 | 게시 대상을 해결하고 승인된 경험을 플랫폼으로 전송합니다. | 쓰세요. 광고가 플랫폼으로 전송되고 꺼진 상태로 게시됩니다. 따로 켜주셔야 합니다. 이 도구를 통해 되돌릴 수 없습니다. |
| 피드백 | [!DNL GenStudio for Performance Marketing] 팀에 제품 피드백을 보냅니다. | 쓰세요. |

대부분의 Insights 도구는 `meta`, `linkedin` 및 `innovid`을(를) 포함합니다. 지표 값 도구는 `meta` 및 `linkedin`을(를) 포함합니다. 전자 메일 캠페인 보고는 Adobe Journey Optimizer(`ajo`) 및 Adobe Campaign(`acc`)에 적용됩니다.

만들기는 `meta`, `linkedin`, `display`, `tiktok` 및 `youtube`을(를) 지원합니다. 활성화는 `META`, `LINKEDIN` 및 `GOOGLECM360`을(를) 지원합니다.

## Insights 도구

### get_insights_capabilities

조직에 대해 활성화된 Insights 채널 및 보고 작업을 반환합니다. 가용성이 명확하지 않은 경우 먼저 이 도구를 사용하십시오. 지원되는 채널은 `meta`, `linkedin`, `innovid`, `ajo` 및 `acc`입니다.

이 도구는 캠페인, 광고 또는 지표 값이 아닌 기능 메타데이터를 반환합니다. 조직의 사용자 지정 지표 키를 찾으려면 `list_connected_channels_and_metrics`을(를) 사용합니다.

### list_connected_channels_and_metrics

조직의 활성 Meta, LinkedIn 및 Google Campaign Manager 360 연결, 지원되는 Insights 채널 및 작업, 구성된 사용자 지정 전환 지표를 반환합니다. `get_insights_metric_values`을(를) 호출하기 전에 지표 키를 찾는 데 사용합니다.

이 도구는 지표 값이 아닌 지표 키, 레이블 및 형식을 반환합니다. 연결은 내역 보고 데이터를 사용할 수 있음을 보장하지 않습니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. 전체 카탈로그를 반환하려면 둘 다 생략합니다. |

### get_insights_summary

선택한 날짜 범위 동안 한 채널에 대한 헤드라인 성능 지표 및 트렌드를 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `meta`, `linkedin` 또는 `innovid`. |
| `startDate` | 아니요 | `YYYY-MM-DD` 형식의 시작 날짜입니다. 기본값은 30일 전입니다. |
| `endDate` | 아니요 | 종료 날짜는 `YYYY-MM-DD` 형식입니다. 기본값은 오늘입니다. |
| `metrics` | 아니요 | 차트화할 지표: `spend`, `ctr`, `cpc`, `cpm`, `cpa`, `impressions`, `clicks`, `conversions`, `videoPlays`, `engagement`, `likes`, `comments` 또는 `shares`. 기본값은 `spend`, `ctr`, `cpc` 및 `cpm`입니다. |

### list_insights_campaigns

캠페인 성과 지표 및 합계 행의 정렬 가능한 테이블을 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `meta`, `linkedin` 또는 `innovid`. |
| `startDate`, `endDate` | 아니요 | `YYYY-MM-DD` 형식의 날짜 범위입니다. 기본값은 지난 30일입니다. |
| `search` | 아니요 | 캠페인 이름 필터. |
| `sortBy` | 아니요 | 정렬 필드: `spend`, `impressions`, `clicks`, `ctr`, `cpc`, `cpm` 또는 `name`. 기본값은 `spend`입니다. 결과는 항상 내림차순으로 정렬됩니다. |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. 기본 페이지 크기는 20입니다. |

### list_insights_email_campaigns

Adobe Journey Optimizer 및 Adobe Campaign에 대한 게재 및 참여 지표와 함께 정렬 가능한 이메일 캠페인 테이블을 반환합니다. 광고 캠페인의 경우 `list_insights_campaigns`을(를) 사용합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `ajo` 또는 `acc`. |
| `startDate`, `endDate` | 아니요 | `YYYY-MM-DD` 형식의 날짜 범위입니다. 기본값은 종료일로부터 최근 30일 전입니다. |
| `search` | 아니요 | 캠페인 이름 필터. |
| `sortBy` | 아니요 | 정렬 필드: `campaignName`, `emailsNumber`, `emailsDelivered`, `totalClicks`, `openRate`, `ctr`, `ctor`, `bounceRate`, `unsubscribeRate` 또는 `spamComplaintRate`. 기본값은 `emailsDelivered`입니다. 결과는 항상 내림차순으로 정렬됩니다. |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. |

### list_insights_ads

광고 수준 성능을 반환합니다. 정렬 가능한 테이블의 기본 찾아보기 모드나 성과가 높은 광고 및 낮은 광고의 계층 모드를 사용합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `meta`, `linkedin` 또는 `innovid`. |
| `tier` | 아니요 | `all`, `high` 또는 `low`. 기본값은 `all`입니다. |
| `mainMetric` | 아니요 | `high` 또는 `low` 계층 모드에 대한 순위 지표: `ctr`, `cpc`, `cpm`, `cpa`, `spend`, `impressions` 또는 `clicks`. 찾아보기 모드에서 무시됩니다. |
| `metrics` | 아니요 | 계층 모드의 각 광고에 대해 보고할 추가 지표입니다. |
| `campaigns` | 아니요 | 결과를 제한하는 데 사용되는 캠페인(최대 50개). 각 캠페인에는 `channel`, `accountId` 및 `campaignId`이(가) 포함됩니다. |
| `search` | 아니요 | 광고 이름 필터. |
| `sortBy` | 아니요 | 찾아보기 모드 정렬 필드: `spend`, `impressions`, `clicks`, `ctr`, `cpc`, `cpm` 또는 `name`. 기본값은 `spend`입니다. 결과는 항상 내림차순으로 정렬됩니다. |
| `spendMin`, `spendMax` | 아니요 | 각 광고에 대한 총 지출 한도. 계층 모드만 해당. |
| `includeUnsupported` | 아니요 | 크리에이티브를 렌더링할 수 없는 광고를 포함합니다. 기본값은 `false`입니다. |
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
| `ads` | 예 | 1개에서 200개 사이의 광고 설명. 각 광고에는 `channel`, `accountId`, `campaignId` 및 `adId`이(가) 포함되며 선택적으로 `adGroupId` 및 `performanceTier`(`high` 또는 `low`)이(가) 포함됩니다. 계층 모드에서 `list_insights_ads`이(가) 반환한 식별자를 사용합니다. |
| `mainMetric` | 예 | 광고 등급을 매기는 데 사용되는 지표: `ctr`, `cpc`, `cpm`, `cpa`, `spend`, `impressions` 또는 `clicks`. |
| `campaigns` | 아니요 | 비교 모집단을 정의하는 데 사용되는 캠페인(최대 50개). 각 캠페인에는 `channel`, `accountId` 및 `campaignId`이(가) 포함됩니다. |
| `spendMin`, `spendMax` | 아니요 | 비교 모집단에 대한 지출 제한입니다. |
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
| `tagSource` | 아니요 | `ad_tags` 또는 `campaign_tags`. 기본값은 `ad_tags`입니다. |
| `sortBy` | 아니요 | 정렬 필드: `adsCount`, `spend`, `impressions`, `clicks`, `conversionCount`, `ctr`, `cpc`, `cpm` 또는 `cpa`. 기본값은 `adsCount`입니다. |
| `search` | 아니요 | 태그 값 필터. |
| `startDate`, `endDate` | 아니요 | `YYYY-MM-DD` 형식의 날짜 범위입니다. |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. |

### get_insights_metric_values

Meta 및 LinkedIn에 대한 잠재 고객, 등록 또는 광고 투자 수익률과 같은 조직의 추적 지표에 대한 값과 트렌드를 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channels` | 아니요 | `meta`, `linkedin` 또는 둘 다. |
| `metrics` | 아니요 | `list_connected_channels_and_metrics`에서 최대 20개의 지표 키를 반환했습니다. 기본값은 조직의 기본 표시 집합입니다. |
| `campaigns` | 아니요 | 결과를 제한하는 데 사용되는 캠페인(최대 50개). 각 캠페인에는 `channel`, `accountId` 및 `campaignId`이(가) 포함됩니다. |
| `startDate`, `endDate` | 아니요 | `YYYY-MM-DD` 형식의 날짜 범위입니다. 기본값은 지난 30일입니다. |

### get_insights_recommendations

조직의 성과 데이터에 기반을 둔 제안된 창의적 변경 사항을 반환합니다. 선택한 범위에 적합한 광고가 포함되지 않은 경우 요청은 권장 사항을 반환하지 않을 수 있습니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channels` | 예 | 하나 이상의 `meta`, `linkedin` 또는 `innovid`. |
| `campaigns` | 아니요 | 결과를 제한하는 데 사용되는 캠페인(최대 50개). 각 캠페인에는 `channel`, `accountId` 및 `campaignId`이(가) 포함됩니다. |
| `search` | 아니요 | 캠페인 이름 필터. |
| `recommendationId` | 아니요 | 한 개의 권장 사항 중 `adUid`을(를) 자세히 검색하는 데 사용합니다. |
| `onlyWithPreview` | 아니요 | 예제 크리에이티브 미리 보기가 없는 권장 사항은 제외됩니다. 기본값은 `true`입니다. |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. |

## 도구 만들기

도구를 만들고, 에셋을 찾고, Adobe Express 템플릿에서 초안을 조합하고, 경험을 활성화하기 전에 검토를 관리합니다.

### list_express_templates

필터링 및 패싯 카운트와 함께 사용 가능한 Express 템플릿을 나열합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 아니요 | `meta`, `display`, `linkedin`, `tiktok`, `youtube` 또는 `__unspecified__`. |
| `query` | 아니요 | 템플릿 검색어. |
| `activatableMimeType`, `aspectRatios`, `externalTemplateSource`, `isHTML5Template`, `keywords`, `languages`, `mediaFormat`, `regions`, `timeframes` | 아니요 | 템플릿 Facet 필터. |
| `sortBy` | 아니요 | `modified` 또는 `created`. 기본값은 `modified`입니다. |
| `order` | 아니요 | `asc` 또는 `desc`. 기본값은 `desc`입니다. |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. |

### describe_express_template

템플릿에서 편집 가능한 텍스트 필드 및 이미지 배치를 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `templateId` | 예 | 빠른 템플릿 식별자. |

### list_cta_options

채널에 대해 허용되는 call-to-action 값을 반환합니다. Display는 자유 형식 텍스트를 허용하므로 빈 목록을 반환합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `linkedin`, `meta`, `display`, `tiktok` 또는 `youtube`. |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. 모든 옵션을 반환하려면 두 옵션을 모두 생략합니다. |

### search_assets

GenStudio 콘텐츠에서 이미지와 비디오를 검색합니다. 초안에 대한 기존 에셋을 선택하는 데 사용합니다. 파생, 외부 및 만료된 자산은 제외됩니다. 이 도구는 에셋을 업로드, 편집, 삭제 또는 생성하지 않으며, GenStudio 콘텐츠 권한이 필요합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `query` | 아니요 | 에셋 메타데이터 간의 키워드 또는 자연어 검색. |
| `mediaTypes` | 아니요 | `image`, `video` 또는 둘 다. 기본값에는 두 가지가 모두 포함됩니다. |
| `aspectRatios` | 아니요 | `1:1` 또는 `16:9` 같은 종횡비입니다. 비율을 사용할 수 없는 경우 공구는 사용 가능한 선택 항목을 반환합니다. |
| `brands`, `campaigns`, `products`, `personas`, `channels` | 아니요 | 이름별 필터. |
| `customMetadata` | 아니요 | 각각 하나 이상의 값이 있는 메타데이터 필드는 최대 5개입니다. |
| `uploadedBy` | 아니요 | `me` 또는 업로더 전자 메일 주소입니다. |
| `createdAtFrom`, `createdAtTo` | 아니요 | ISO 8601 형식의 만들기 시간 범위입니다. |
| `aiGenerated` | 아니요 | AI 세대 상태별 필터. |
| `contentCredentials` | 아니요 | Content Credentials 상태별 필터. |
| `limit`, `offset` | 아니요 | 페이지 크기 및 페이징 오프셋입니다. |

결과에는 `create_draft`에 대한 안정적인 자산 참조와 수명이 짧은 서명 URL이 포함됩니다.

### create_draft

하나 이상의 경험이 포함된 빠른 템플릿에서 편집 가능한 초안을 만듭니다. 각 호출은 새 초안을 만듭니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `templateId` | 예 | 빠른 템플릿 식별자. |
| `prompt` | 예 | Creative은 초안과 함께 저장된 지침을 간략히 설명하고 복사합니다. |
| `experiences` | 예 | 하나 이상의 경험. 다음 표를 참조하십시오. |
| `name` | 아니요 | 문서 이름. |
| `allowAssetReuse` | 아니요 | 선택한 에셋 하나를 여러 경험에서 재사용할 수 있습니다. 기본값은 `false`입니다. |

각 경험은 다음 필드를 지원합니다.

| 필드 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 예 | `linkedin`, `meta`, `display`, `tiktok` 또는 `youtube`. |
| `title` | 아니요 | 경험 제목입니다. 기본값은 &quot;개념 *n*&quot;입니다. |
| `headline` | Meta 및 LinkedIn | 기본 헤드라인. |
| `body` | Meta, LinkedIn 및 TikTok | 본문 복사. LinkedIn의 경우 소개 텍스트입니다. TikTok의 경우 기본 텍스트입니다. |
| `description` | YouTube | 광고 설명. Meta 및 LinkedIn에 선택 사항입니다. |
| `display_url` | Meta 및 LinkedIn | 광고에 표시된 URL을 표시합니다. |
| `destination_url` | 아니요 | 광고가 링크되는 URL입니다. |
| `cta` | 아니요 | `list_cta_options`의 call-to-action 텍스트입니다. |
| `templateFields` | 아니요 | `describe_express_template`에서 명명된 템플릿 요소를 재정의합니다. 각 재정의는 텍스트, 차원이 있는 이미지 URL 또는 비디오 URL을 설정합니다. |
| `assetTemplateFields` | 아니요 | 템플릿의 이미지 또는 비디오 필드에 대한 `search_assets`의 콘텐츠 자산입니다. |

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
| `emails` | 예 | 공동 작업자 이메일 주소 1~20개. |
| `role` | 예 | `editor` 또는 `viewer`. |
| `message` | 아니요 | 초대 메시지. |

### request_draft_approval

하나 이상의 사용자에게 초안을 보내어 승인합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `draftId` | 예 | 초안 자산 식별자. |
| `emails` | 예 | 검토자 이메일 주소 1~20개. |

### list_experiences

활성화하기 위해 준비된 승인되고 게시된 경험을 반환합니다. 초안은 포함되지 않습니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `channel` | 아니요 | `email`, `meta`, `meta_organic`, `display`, `ctv`, `linkedin`, `linkedin_organic`, `tiktok`, `chatgpt` 또는 `youtube`. |
| `createdByMe` | 아니요 | 현재 사용자가 만든 경험으로 결과를 제한합니다. |
| `campaignNames` | 아니요 | 최대 5개의 정확한 캠페인 이름 필터. |
| `creatorEmail` | 아니요 | 작성자 이메일 필터. |
| `createdAtFrom`, `createdAtTo` | 아니요 | 생성 날짜 범위입니다. |
| `language` | 아니요 | BCP 47 언어 태그. |
| `limit`, `cursor` | 아니요 | 페이지 크기(1-50, 기본값 20) 및 페이지 매김 커서입니다. |

## 플랜 도구

계획 도구는 캠페인 개요를 다시 볼 수 있는 캠페인 초안으로 만들고 Workfront Planning에 저장합니다.

### extract_campaign_from_brief

붙여넣은 마케팅 개요 하나에서 다시 볼 수 있는 캠페인 초안을 추출합니다. 이 도구는 레코드를 저장하지 않습니다. 누락된 사실과 날짜는 유추되지 않습니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `briefText` | 예 | 하나의 캠페인 개요에 대한 전체 일반 텍스트로서, 최대 100,000자입니다. 파일 및 링크는 지원되지 않습니다. |

그 결과에는 캠페인 초안, 지원되는 견적이 포함된 결과, 제안된 대상자 및 경고가 포함됩니다.

### create_workfront_campaign

검토 및 승인한 초안에서 연결된 제품 및 담당자로 Workfront Planning 캠페인을 생성합니다. 이 도구는 idempotent가 아니며 레코드를 자동으로 롤백할 수 없습니다. 성공했을 수 있는 쓰기를 다시 시도하기 전에 Workfront을 검사하십시오.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `campaignDraft` | 예 | 승인된 초안입니다. `name`이(가) 필요합니다. 선택적 필드는 `description`, `objective`, `keyMessaging`, `startDate`, `endDate`(`YYYY-MM-DD`), `status`, `channels`, `products` 및 `personas`입니다. |
| `channelSelections` | 아니요 | 모호한 채널 이름에 대해 승인된 선택 사항입니다. |
| `entitySelections` | 아니요 | 승인된 기존 제품 및 담당자 레코드. `null`을(를) 사용하여 새 레코드를 요청하십시오. |
| `createMissingEntities` | 아니요 | 새로 선택한 제품 및 가상 사용자를 만듭니다. 기본값은 `false`입니다. |

제품, 페르소나 채널이 애매한 경우 이 도구는 확인 옵션을 반환하고 변경하지 않습니다.

## 도구 활성화

도구 활성화 유료 미디어 타겟을 해결하고 승인된 경험을 플랫폼으로 전송합니다. 광고는 꺼짐 상태(Meta 일시 중지, LinkedIn 초안, Campaign Manager 360 비활성)로 게시되므로 게재하기 전에 별도로 켜야 합니다. 이러한 도구를 통해서는 광고를 플랫폼에 보낼 수 없습니다.

### configure_activation_target

필요한 경우 유료 미디어 계정, 캠페인, 광고 세트 및 Facebook 페이지를 확인하고 확인합니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `platform` | 예 | `META`, `LINKEDIN` 또는 `GOOGLECM360`. |
| `platformAccountId` | 아니요 | 유료 미디어 계정 식별자. 계정을 검색하려면 생략합니다. |
| `campaignId` | 아니요 | Meta 또는 LinkedIn용 Campaign 식별자. Campaign Manager 360에는 사용되지 않습니다. |
| `adsetId` | 아니요 | Meta 광고 세트 또는 LinkedIn 캠페인 식별자. Campaign Manager 360에는 사용되지 않습니다. |
| `pageId` | 아니요 | Meta용 Facebook 페이지 식별자. |

Campaign Manager 360의 경우 광고 계정만 필요합니다.

### create_activation

검증된 타겟을 사용하여 승인된 경험을 플랫폼에 광고로 전송합니다. 광고가 꺼진 상태로 게시됩니다. Meta은 각 종횡비에 대해 첫 번째 이미지가 있는 광고를 하나 만듭니다. LinkedIn 및 Campaign Manager 360은 확인된 각 이미지에 대해 하나의 광고를 만듭니다.

| 매개변수 | 필수 여부 | 설명 |
|---|---|---|
| `platform` | 예 | `META`, `LINKEDIN` 또는 `GOOGLECM360`. |
| `targetId` | 예 | `configure_activation_target`이(가) 반환한 대상을 확인했습니다. |
| `experienceId` | 예 | `list_experiences`이(가) 반환한 승인된 경험 식별자입니다. |
| `name` | 아니요 | 광고 배치 표시 이름. 기본값은 경험의 광고 제목입니다. |

결과 목록에 각 광고의 초기 상태와 [!DNL GenStudio for Performance Marketing]에 연결된 링크가 포함된 만들어지고 대기하고 건너뛴 광고의 수가 표시됩니다. `PENDING` 상태는 작업이 큐에 있음을 의미하며 광고가 게재됨을 의미하지는 않습니다.

`create_activation`을(를) 두 번 호출하면 첫 번째 광고를 업데이트하는 대신 추가 광고가 만들어집니다.

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
- **추적된 지표를 검토합니다.** `list_connected_channels_and_metrics`을(를) 호출한 다음 반환된 지표 키를 사용하여 `get_insights_metric_values`을(를) 호출합니다.
- **권장 사항을 초안으로 전환합니다.** `get_insights_recommendations`을(를) 호출한 다음 `create_draft_from_recommendation`을(를) 호출합니다.
- **템플릿에서 빌드:** `list_express_templates`, `describe_express_template` 및 `list_cta_options`을(를) 호출한 다음 `create_draft`을(를) 호출합니다.
- **기존 자산에서 빌드:** `search_assets`을(를) 호출한 다음 반환된 자산 참조를 `assetTemplateFields`의 `create_draft`에 전달합니다.
- **Workfront에 캠페인 개요를 저장합니다.** `extract_campaign_from_brief`에 전화하고 초안을 검토한 다음 `create_workfront_campaign`에 전화합니다.
- **승인된 환경을 플랫폼에 보냅니다.** `list_experiences`을(를) 호출한 다음 `configure_activation_target` 및 `create_activation`을(를) 호출합니다.

## 관련 기능

- [AI 지원 개요](overview.md)
- [AI 지원 연결](connect-ai-assistants.md)
- [AI 지원 사용](use-ai-assistants.md)
