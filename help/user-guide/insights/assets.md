---
title: Assets 개요
description: Adobe GenStudio for Performance Marketing에서 에셋 성과를 평가하는 방법을 알아봅니다.
feature: Insights, Assets
exl-id: 1e93422b-2645-4e29-a216-fc1008afbfc7
source-git-commit: 4284026bf14d58eecb547d80b4bdae6ac0422078
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 0%

---

# Assets 개요

[!DNL Insights] _[!UICONTROL Assets]_ 보기에는 선택한 채널 계정에 대한 경험 및 광고 캠페인에 사용된 자산 목록이 표시됩니다.

{{connect-insights}}

_[!UICONTROL Assets]_ 테이블은 [!UICONTROL 자산 ID]을(를) 사용하여 구성되었습니다. 뷰 목록(테이블) 아이콘과 갤러리 뷰(그리드) 아이콘을 사용하여 뷰 사이를 전환할 수 있습니다. 표 오른쪽 위의 설정(cog) 아이콘을 클릭하여 볼 수 있는 열을 전환합니다. 테이블 왼쪽 위의 필터(단계) 아이콘은 **[!UICONTROL 필터]** 메뉴를 엽니다. 이 메뉴에서 여러 목록을 선택할 수 있습니다. 모든 필터 선택 항목을 지우려면 **재설정**&#x200B;을 클릭하세요.

![Assets 필터 및 테이블](/help/assets/insights-assets-filter.png){zoomable="yes"}

{{$include /help/_includes/download-insights.md}}

_[!UICONTROL Assets]_ 갤러리 보기에는 자산 미리 보기의 콜라주와 지표(예: 클릭스루 비율)가 표시됩니다. 갤러리 오른쪽 위에 있는 설정(cog) 아이콘을 클릭하여 **[!UICONTROL 카드 설정]**&#x200B;을 열고 볼 수 있는 세 가지 지표 중 하나를 전환합니다.

- CPA(작업당 비용)
- CTR(클릭스루 비율)
- CPC(클릭당 비용)
- 지출

## 자산 세부 사항

_자산_&#x200B;은(는) 마케팅 이니셔티브에서 사용하도록 승인된 이미지, 비디오, 텍스트 또는 기타 크리에이티브 콘텐츠입니다.

에셋 세부 사항 보기에서 선택한 에셋을 사용하는 경험을 확인할 수 있습니다. 세부 정보에는 총 자산 성능, 사용자 정의 속성 및 자산과 관련된 AI가 감지한 기능이 포함됩니다.

![자산 세부 정보](/help/assets/insights-asset-details.png){zoomable="yes"}

## 자산 성과

인사이트 지표를 통해 캠페인 성공에 기여하는 에셋과 가장 효과적인 에셋 속성을 평가할 수 있습니다.

다음 표에서는 [!UICONTROL Assets] 테이블 보기의 주요 디지털 마케팅 지표에 대한 정의와 통찰력을 제공합니다. 각 지표에는 자산과 관련된 간단한 정의, 지표 계산 방법 및 자산의 중요도와 자산에 대한 영향을 이해하는 데 도움이 되는 하나 이상의 통찰력이 포함되어 있습니다.

| 지표 | 정의 | 인사이트 |
| ---------------------- | ----------------------------- | -------------------------------- |
| **[!UICONTROL 자산 ID]** | 이 자산과 연결된 이름입니다. | 주요 지표에 대한 열 머리글을 클릭하여 테이블을 정렬합니다. |
| **[!UICONTROL 노출 횟수]** | 상호 작용이나 보기에 관계없이 에셋이 채널에 로드될 때마다 카운트됩니다. | 노출 수가 높으면 넓은 가시성을 나타낼 수 있지만, 진정한 성능 통찰력을 위해서는 다른 참여 지표와 관련하여 고려하십시오. |
| **[!UICONTROL 클릭수]** | 사용자가 에셋에서 링크와 같은 클릭 가능한 요소와 상호 작용하는 횟수입니다. | 클릭 수가 높으면 콘텐츠에 대한 높은 관심과 참여를 나타내므로 효과적인 적절한 대상자에게 도달할 수 있습니다. |
| **[!UICONTROL CTR ]**<br>_클릭스루 비율_ | 경험 내에서 에셋 클릭을 일으킨 노출 횟수의 백분율(%).<br>**계산**: `clicks`을(를) `impressions`(으)로 나누기 | 클릭스루율이 높으면 콘텐츠가 관련성이 높고 대상자를 사로잡는다는 것을 나타냅니다. 이는 메시징과 디자인이 관객의 관심을 효과적으로 포착하고 행동을 유도하고 있음을 시사한다. 또한 높은 CTR은 자산이 잘 타겟팅되고 의도한 대상과 공감을 주어 전반적인 캠페인 성과가 개선됨을 의미할 수 있습니다. |
| **[!UICONTROL CPM ]**<br>_천 단위당 비용_ | 자산에 대한 1,000개 광고 노출 시마다 비용이 듭니다.<br>**계산**: 총 `spent`을(를) 도달 횟수로 나눈 다음 1000을 곱합니다. | 낮은 값은 특히 높은 클릭스루 속도와 쌍을 이룰 때 비용 효과적인 가시성을 나타낼 수 있다. |
| **[!UICONTROL CPA ]**<br>_작업당 비용_ | 구매 또는 구독과 같은 특정 고객 작업을 완료하는 데 소요되는 평균 비용입니다.<br>**계산**: 총 금액 `spent`을(를) 완료된 고객 작업 수로 나눈 값입니다. | 중요한 고객 작업을 발생시키는 에셋을 식별하는 데 도움이 됩니다. |
| **[!UICONTROL CPC ]**<br>_클릭당 비용_ | 에셋을 클릭할 때마다 연결되는 평균 비용입니다.<br>**계산**: 총 `spent`을(를) `clicks`(으)로 나눈 값 | 평균 비용이 낮아지면 특히 전환율 상승과 비교할 때 비용 효율적인 광고 지출이 나타날 수 있습니다. |
| **[!UICONTROL 지출]** | 지정된 기간 동안 개별 자산과 관련된 예산에서 지출된 금액입니다. | 단기간에 높은 지출액은 빠른 사용량을 나타낼 수 있으며, 이는 자원의 조기 고갈을 초래할 수 있다. 주요 성과 지표에 대한 지출 금액을 추적하여 전체 투자 수익률을 모니터링합니다. |
| **[!UICONTROL 경험 수]** | 이 자산을 사용하는 경험 수입니다. | |
| **[!UICONTROL 속성]** | 검색되어 이 자산에 적용되는 속성 목록입니다. | |
