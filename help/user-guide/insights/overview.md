---
title: Insights 개요
description: 실시간 콘텐츠 성능 지표를 기반으로 광고를 최적화하는 방법을 알아봅니다.
level: Intermediate
feature: Reporting and Insights
exl-id: 26402a06-f776-42be-9d8d-fc498c0f75a8
source-git-commit: 42a211956854126798024a97fc0befc3626160b7
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Adobe GenStudio for Performance Marketing Insights

Adobe GenStudio for Performance Marketing [!DNL Insights]은(는) 데이터 기반 결정을 내리는 데 도움이 되는 콘텐츠 성능에 대한 고급 분석 및 통찰력을 제공합니다.

[!DNL Insights] 대시보드에서 다음을 수행할 수 있습니다.

- **가장 효과적인 콘텐츠 식별**: 다양한 대상자에게 가장 적합한 콘텐츠를 선택하고 트렌드 환경 설정을 위해 향후 콘텐츠나 캠페인을 사용자 지정합니다.
- **성과가 낮은 콘텐츠 최적화**: 성과가 좋지 않은 콘텐츠를 찾아 통합 생성 AI를 사용하여 즉시 변형을 만들어 처음부터 새로 시작하지 않고도 효과를 향상시킬 수 있습니다.
- **성과가 좋은 콘텐츠 활성화**: 콘텐츠를 성공적으로 가져와서 수정하여 대상자를 위한 광고를 새로 고치거나 새로운 캠페인에 사용할 영웅 콘텐츠를 조정하여 수명 주기와 성능을 확장할 수 있습니다.

## Data connectors

[!DNL Insights]을(를) 처음 열면 Adobe GenStudio for Performance Marketing과 채널 계정을 연결할 수 있도록 안내하는 배너가 표시될 수 있습니다.

이 연결을 통해 GenStudio for Performance Marketing은 활성 마케팅 캠페인, 미디어 및 광고에서 통계 데이터를 받을 수 있습니다. 처음에 GenStudio for Performance Marketing은 최근 6개월의 데이터를 수집하므로 최신 데이터를 분석하고 조치를 취할 수 있는 도구가 제공됩니다.

{{connect-insights}}

## 대시보드

[!DNL Insights] 대시보드에는 각 콘텐츠 형식에 대해 구성 가능한 테이블이 있습니다. [!UICONTROL 채널], [!UICONTROL 광고], [!UICONTROL 미디어] 및 [!UICONTROL 특성].

![[!DNL Insights] 대시보드](/help/assets/insights-dashboard.png)

각 보기에는 키워드, 필터링 및 날짜 범위별로 검색할 수 있는 해당 테이블이 표시됩니다. 표 오른쪽 위의 설정(cog) 아이콘을 클릭하여 볼 수 있는 열 유형을 전환할 수 있습니다. _[!UICONTROL 요약]_ 행은 열의 합계 또는 평균을 표시할 수 있습니다.

[!UICONTROL 광고], [!UICONTROL 미디어] 및 [!UICONTROL 특성]에는 이미지 또는 비디오 썸네일이 있는 카드를 사용하여 자산을 검색하고 정렬할 수 있는 갤러리 보기가 포함되어 있습니다. 각 카드에 세 개의 주요 지표 중 하나를 표시할 수 있는 옵션이 있습니다. `Click-through rate`, `Cost per click` 및 `Spend`.

### 채널

[[!DNL Insights] _[!UICONTROL 채널&#x200B;]_&#x200B;보기](channels.md)는 기본 보기이며 목표, 예산, 시작 날짜 및 활동과 같은 활성 캠페인 세부 정보 목록을 표시합니다. GenStudio for Performance Marketing에서 통계 데이터를 받기 시작할 수 있도록 [채널 계정을 연결](/help/user-guide/connectors/connect-channel.md)하세요.

### 광고

[[!DNL Insights] _[!UICONTROL 광고&#x200B;]_&#x200B;보기](ads.md)는 광고의 효과를 평가하는 데 중점을 둡니다. [!UICONTROL 광고] 보기를 사용하면 지정된 날짜 범위 내의 광고 배치를 기반으로 광고의 지표를 분석할 수 있습니다._[!UICONTROL &#x200B;광고 이름&#x200B;]_&#x200B;을 클릭하면 광고 성능 지표, 광고 배치별 성능 및 특성을 볼 수 있습니다.

### 미디어

[[!DNL Insights] _[!UICONTROL 미디어&#x200B;]_&#x200B;보기](media.md)는 크리에이티브 콘텐츠의 성능을 분석하는 데 도움이 되도록 설계되었습니다. 클릭이나 노출과 같이 선택한 지표를 개선하는 데 기여하는 미디어 속성을 식별할 수 있습니다.

미디어 콘텐츠를 클릭하면 다양한 광고 및 광고 배치에 대한 성능에 대한 추가 컨텍스트를 제공합니다.

![미디어 세부 정보](/help/assets/insights-media-details.png){width="600" zoomable="yes"}

미디어 세부 사항 보기의 왼쪽에 에셋의 썸네일과 속성 목록이 표시됩니다. 강조 표시된 지표가 세 개 있습니다. `Click-through rate`, `Cost per click` 및 `Spend`. 성능 강조 표시는 선택한 기간(기본값: `Last 30 days`) 동안 실제 값(실선)과 평균 값(점선)을 비교하는 방법을 보여줍니다.

### 속성

미디어 _특성_&#x200B;은(는) 색상, 색조, 컴포지션(예: 주제, 글꼴, 시각적 요소) 및 기타 주요 구성 요소와 같은 고유한 세부 사항으로 크리에이티브 콘텐츠를 식별하는 데 도움이 됩니다. 속성은 종종 가장 적게 측정되고 분석되는 콘텐츠 정보 세트입니다.

[[!DNL Insights] _[!UICONTROL 특성&#x200B;]_&#x200B;보기](attributes.md)를 통해 특정 대상, 채널, 지역에서 어떤 특성이 더 잘 작동하는지 조사하고 식별하는 데 도움이 되며, 계절별 트렌드를 강조 표시하는 데 도움이 될 수 있습니다. 이러한 통찰력을 통해 수행자 속성을 사용하여 변형을 만들거나 특정 대상을 타기팅하거나 다른 캠페인 전략으로 실험할 수 있습니다.
