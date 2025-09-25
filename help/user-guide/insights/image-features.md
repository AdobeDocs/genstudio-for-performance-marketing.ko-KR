---
title: 이미지 기능
description: GenStudio for Performance Marketing에 사용되는 속성 범주의 이미지 기능에 대해 알아봅니다.
level: Intermediate
feature: Reporting and Insights, Image Attributes, Generative AI
exl-id: b7e3d202-4085-48a4-a6ba-c950dfd52233
source-git-commit: c0f45fb0ffc61d20611693498f1b12d3946ca6ca
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 0%

---

# 이미지 기능

이미지 기능은 [!DNL Insights]&#x200B;(으)로 분석에 사용되는 이미지 내의 고유한 정보 요소 또는 패턴을 나타냅니다. 이러한 기능은 시각적 콘텐츠를 분류하고 이해하는 데 도움이 되므로 보다 정확하고 자세한 통찰력을 얻을 수 있습니다. 스타일, 색상, 사물 등 다양한 속성을 식별함으로써 AI가 이미지를 종합적으로 분석해 더 나은 의사결정과 전략 수립에 도움을 줄 수 있다.

## 스타일 감지

_이미지 스타일_&#x200B;을(를) 확인하는 것은 다른 이미지 특성을 식별하기 위한 토대 역할을 합니다. AI가 적절한 분석 기법을 적용하고 관련 기능을 인식해 이미지에 대한 보다 포괄적인 이해를 유도할 수 있다. 각 스타일은 이미지 인식 및 분석 방법에 영향을 미치는 뚜렷한 시각적 특성을 가지고 있습니다.

이미지 스타일이 `photograph`(으)로 식별되는 경우, AI는 `camera settings`, `camera proximity` 및 `Photography genres`에 대한 추가 트레이트를 분석합니다. 이러한 트레이트는 사진에만 해당되며 이미지의 구성 및 품질에 대한 심층적인 통찰력을 제공합니다. Adobe의 [사진 학습](https://www.adobe.com/creativecloud/photography/discover/types-of-photography.html)에서 _28가지 사진 스타일 유형_&#x200B;을 확인하고 인기 있는 사진 유형 및 기본 용어에 대해 알아봅니다.

이미지 스타일이 `sketch` 또는 `digital cartoon`(으)로 식별되는 경우, 서로 다른 특성 집합이 관련될 수 있습니다. 이러한 계층적 접근 방식은 분석이 상황적으로 정확하고 검사되는 이미지의 특정 유형에 맞게 조정되도록 보장한다.

## 이미지 기능 검색

**특정 특성 범주의 이미지를 보려면**:

1. _[!DNL Insights]_&#x200B;에서&#x200B;**[!UICONTROL 특성]**&#x200B;보기를 선택하십시오.

1. **[!UICONTROL 이미지]**&#x200B;를 선택하여 테이블 보기를 변경합니다.

1. **[!UICONTROL 특성 범주]** 목록에서 `Scenes`과 같은 이미지 기능을 선택하십시오.

1. 해당 카테고리를 공유하는 이미지의 세부 보기에 대한 속성을 선택합니다.

   예를 들어 `Scenes` 범주는 `restaurant`을(를) 특성으로 가질 수 있습니다.

1. _특성 세부 정보_ 페이지에는 이 특성을 가진 모든 이미지가 나열됩니다.

다음 표에는 GenStudio for Performance Marketing AI가 인식하는 이미지 기능 카테고리가 나열되어 있습니다. 미디어 콘텐츠에 대해 검색된 특성 목록이 완전하지 않습니다. 풍부한 기능 세트를 포함하는 미디어는 AI가 식별하는 가장 지배적인 3가지 기능으로 제한될 수 있습니다.

<!-- For the writer: turn off word wrap to work with these tables. Option + Z -->

| 범주 | 설명 | 예 |
| ----------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 주의 분포 | 이미지의 다른 영역에 얼마나 많은 포커스를 받을 수 있는지를 나타내는 시청자 관심도 수준입니다. 분포가 높으면 단일한 영역이 시청자의 초점을 지배하지 않는다는 의미이고, 분포가 낮으면 한두 개의 초점이 시청자의 시선을 사로잡는다는 의미이다. | `high`, `medium`, `low`<p>왼쪽의 `low` 배포 및 오른쪽의 `high` 배포 예:<p>![낮은 보급률과 높은 보급률의 공 놀이](/help/assets/category/image-attn-lowhigh.png "낮은 보급률과 높은 보급률의 차이"){width="200" zoomable="yes"} |
| 카메라 각도 | 카메라가 피사체를 포착하는 원근은 뷰어의 이미지 지각과 해석에 영향을 미친다. 이미지 스타일이 `photograph`인 경우 이 특성이 식별됩니다. | `Low angle`, `High angle`, `Eye level`, `Neutral angle`, `Overhead view`, `Bird's eye view`<p>`Overhead view`의 예:<p>![오버헤드 보기](/help/assets/category/image-camera-angle.png "오버헤드 반바지 한 벌"){width="200" zoomable="yes"} |
| 카메라 설정 | 이미지의 최종 모양 및 품질에 영향을 주는 카메라 컨트롤의 특정 조정 및 구성입니다. 이미지 스타일이 `photograph`인 경우 이 특성이 식별됩니다. | `Fast shutter speed`, `Long exposure`, `Bokeh blur`, `Motion blur`, `Tilt-shift blur`, `Flash`, `Wide-angle`, `Black and white`, `Double-exposure`, `Macro`, `Normal mode`<p>`Fast shutter speed` 설정의 예:<p>![빠른 셔터 속도](/help/assets/category/image-camera-setting.png "파도 서핑"){width="200" zoomable="yes"} |
| 색상 및 톤 | 이미지 내의 색상 및 색조 특성입니다. 서로 다른 이미지 레이어에서 사전 정의된 40색 세트에서 최대 3개의 색상을 식별합니다.<p>**[!UICONTROL 전경색]**—이미지의 앞쪽 레이어 색<br>**[!UICONTROL 배경색&#x200B;]**—이미지의 뒤쪽 레이어 색 | 색상 값: `Red`, `Dark Red`, `Green`, `Bright Green`, `Dark Green`, `Light Green`, `Mud Green`, `Blue`, `Dark Blue`, `Light Blue`, `Royal Blue`, `Black`, `White`, `Off White`, `Gray`, `Dark Gray`, `Silver`, `Cream`, `Magenta`, `Cyan`, `Yellow`, `Mustard`, `Khaki`, `Brown`, `Dark Brown`, `Violet`, `Pink`, `Dark Pink`, `Maroon`, `Tan`, `Purple`, `Lavender`, `Turquoise`, `Plum`, `Gold`, `Emerald` `Orange`, `Beige`, `Lilac`, `Olive` |
| 색상 온도 | 이미지의 색상에 대한 일반적인 온기 또는 시원함을 설명합니다. | 색조 또는 온도 값: `warm`, `cool`, `neutral`<br>![색상 및 쿨 색조](/help/assets/category/image-color-temp.png "색상 온도와 여러 색상 개체"){width="200" zoomable="yes"} |
| 컨텐츠 밀도 | 이미지 내의 시각적 요소 및 세부 정보의 집중으로, 얼마나 많은 정보가 시각적 공간에 채워지는지를 나타냅니다.<p>시청자 초점이 이미지의 여러 영역에 어떻게 분산되는지 측정하는 주의 분산과 달리 콘텐츠 밀도는 존재하는 시각적 정보의 양에 중점을 둡니다. 콘텐츠 밀도가 높을수록 더 많은 요소가 존재함을 의미합니다. | `high`, `medium`, `low`<p>왼쪽의 `low` 밀도 및 오른쪽의 `high` 밀도의 예:<p>![낮은 밀도와 높은 밀도의 공 놀이](/help/assets/category/image-attn-lowhigh.png "낮은 밀도와 높은 밀도의 차이"){width="200" zoomable="yes"} |
| 이미지 스타일 | 사진이나 스케치와 같은 이미지의 시각적 처리. AI가 이미지 스타일을 결정하면 다른 트레이트를 식별할 수 있다. 예를 들어, 이미지가 사진이면, 카메라 설정, 카메라 근접, 및 조명 조건이 적용될 수 있다. | `Photograph`, `Photograph with text overlay`, `Sketch`, `Painting`, `Digital cartoon`, `Infographics`, `Graphic design`, `Collage`, `Software screenshot`<p>`digital cartoon` 이미지 스타일의 예![만화 이미지 스타일](/help/assets/category/image-style.png "고양이의 이미지 스타일 만화"){width="200" zoomable="yes"} |
| 조명 상태 | 이미지의 기분, 색조 및 가시성에 영향을 주는 이미지의 품질 및 특성을 설명합니다. | `Golden hour`, `Blue hour`, `Midday`, `Overcast`, `Night`, `Daylighting`, `Incandescent`, `Fluorescent`, `Colorful`, `Studio`<p>`daylighting` 조건의 예:<p>![자연 채광 상태에서 인도에 있는 사람과 개](/help/assets/category/image-lighting.png "자연 채광 상태"){width="200" zoomable="yes"} |
| 오브젝트 | 이미지를 구성하는 하나 이상의 항목, 엔티티 및 요소를 식별합니다. | 값이 너무 많지만 `backpack`, `book`, `hawk`, `glasses`, `fish`, `pencil`, `mountain bike`, `soap` 등이 있습니다.<p>`toucan` 및 `bird` 개체의 예:<p>![새, Toucan 개체](/help/assets/category/image-objects-bird.png "Toucan 새 개체의 그래픽 디자인"){width="200" zoomable="yes"} |
| 방향 | 폭 및 높이를 기준으로 한 이미지 맞춤입니다. 큰 키보다 넓은지(가로), 넓은 키보다 큰지(세로) 또는 폭과 높이가 같은지(사각형) 여부를 검색합니다. | `landscape`, `portrait`, `square`<p>`square` 방향의 예:<p>![사각형 스케치](/help/assets/category/image-orientation-square.png "사각형 방향 꽃 스케치"){width="200" zoomable="yes"} |
| 사람 | 적어도 한 사람이 존재하는 경우, 하나 이상의 속성은 이미지 내의 사람 또는 사람을 설명할 수 있다. | `person`, `woman`, `man`, `girl`, `boy`, `social group`, `kid`, `crowd`, `people`<p>사람 `woman` 및 `person` 범주의 예:<p>![카메라 있는 사용자](/help/assets/category/image-people.png "카메라 관리하는 사용자"){width="200" zoomable="yes"} |
| 사진 장르 | `Abstract` 또는 `Landscape`과(와) 같이(가로 방향과 같지 않음) 이미지를 캡처하는 데 사용되는 제목 및 기술을 검색합니다. | `Architecture`, `Astro`, `Landscape`, `Pet`, `Interior`, `Wildlife`, `Night`, `Cityscape`, `Seascape`, `Underwater`, `Storm`, `Adventure sports`, `Fashion`, `Portrait`, `Sports`, `Food`, `Street`, `Event`, `Lifestyle`, `Commercial`, `Group`, `Abstract`, `Minimalist`, `Composite`, `Surreal` <p>[사진 종류](https://www.adobe.com/creativecloud/photography/discover/types-of-photography.html)를 참조하세요.<p>`Adventure sports`의 예:<p>![카누로 서 있는 사람](/help/assets/category/image-photography-genres.png "카누로 서 있는 노 있는 사람"){width="200" zoomable="yes"} |
| 장면 | 이미지 내의 설정이나 환경을 식별하여 이미지가 캡처된 위치나 묘사된 위치 유형에 대한 컨텍스트를 제공합니다. | 값이 너무 많지만 `lake`, `underwater`, `highway`, `hill`, `log cabin`, `island`, `beach`, `lounge` 등이 있습니다.<p>헬멧에 반영된 `snow`, `sky`, `winter` 및 `mountain` 장면 예:<p>![겨울 설경](/help/assets/category/image-scenes.png "겨울, 눈, 하늘, 산 장면 반사"){width="200" zoomable="yes"} |
| 피사체 거리 | 카메라와 이미지 피사체 사이의 거리입니다. | `close up`, `mid shot`, `long shot`<p>`Long shot`의 예:<p>![산꼭대기가 길다](/help/assets/category/image-subject-distance.png "산꼭대기가 먼 사람"){width="200" zoomable="yes"} |
| 스타일 | Lightroom 또는 Photoshop에서 사용되는 것과 같은 이미지 요소에 적용되는 시각적 처리를 검색합니다. | `design`, `illustration`, `logo`, `square`, `cartoon`, `art`, `circle`, `circular`<p>`circular` 스타일의 예:<p>![산호초의 원형 게이트웨이](/help/assets/category/image-styles-circular.png "산호초의 원형 포털"){width="200" zoomable="yes"} |
| 태그 | 특정 분류에 해당하지 않는 다른 이미지 특성을 검색합니다. 태그는 이미지에 대한 추가 컨텍스트 및 메타데이터를 제공합니다. 예를 들어, AI는 이미지에서 `helmet` 및 `motorobike` 오브젝트를 감지하고, `riding`을(를) 태그로 포함할 수 있습니다. | 값이 너무 많지만 `construction`, `gothic`, `healing`, `military`, `selfie`, `football`, `typing`, `dancer`, `dancing` 등이 있습니다.<p>`dancer` 및 `dancing` 태그의 예:<p>![댄서 및 댄스용 태그](/help/assets/category/image-tags.png "댄싱 사용자"){width="200" zoomable="yes"} |
