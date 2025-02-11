---
title: 속성 범주
description: GenStudio for Performance Marketing에 사용되는 속성 카테고리에 대해 알아봅니다.
feature: Insights, Attributes, Generative AI
recommendations: noDisplay
last-substantial-update: 2024-11-11T00:00:00Z
exl-id: c3b51ef2-56ac-4dd8-98b7-79185b5998d0
source-git-commit: 976358742e598b55b1f0c4ca4664d2bcd8f1e9b9
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 1%

---

# 속성 범주

속성 카테고리는 공통적인 특성을 공유하는 관련 속성을 구성하는 분류 그룹입니다. 이러한 범주는 컨텍스트를 확대하고 애플리케이션 및 사용을 촉진하여 특정 속성을 보다 효율적으로 검색, 식별 및 이해하는 데 도움이 됩니다.

GenStudio for Performance Marketing은 Adobe의 AI 및 머신 러닝 기능을 사용하여 이미지, 비디오 및 텍스트를 학습하고 정확도 확률에 따라 [!UICONTROL 자산 속성]을 적용합니다. 에셋의 속성 목록은 완전하지 않습니다. 풍부한 기능 세트를 포함하는 Assets은 AI가 식별하는 가장 지배적인 3가지 기능으로 제한될 수 있습니다.

## 이미지 기능

이미지 기능은 [!DNL Insights](으)로 분석에 사용되는 이미지 내의 고유한 정보 요소 또는 패턴을 나타냅니다. 다음 표에는 GenStudio for Performance Marketing AI가 인식하는 이미지 기능 카테고리가 나열되어 있습니다.

<!-- For the writer: turn off word wrap to work with these tables. Option + Z -->

| 범주 | 설명 | 예 |
| ----------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 카메라 각도 | 피사체에 대한 카메라의 위치 및 각도입니다. |                                                                                                                                                                                |
| 피사체 거리 | 카메라와 이미지 피사체 사이의 거리입니다. | `close up`, `mid shot`, `long shot` |
| 카메라 설정 | 이미지를 생성하기 위한 카메라 컨트롤의 구성입니다. |                                                                                                                                                                                |
| 색상 및 톤 | 이미지 요소에 사용되는 색상을 평가합니다. 다음 이미지 레이어에서 미리 결정된 40개 색상 세트에서 1~3개 색상을 식별합니다.<br>**[!UICONTROL 전경색&#x200B;]**- 이미지의 앞 레이어에 있는 요소<br>**[!UICONTROL 배경색]** - 이미지의 뒤 레이어에 있는 요소 | 색상 값: `Red`, `Dark_Red`, `Green`, `Bright_Green`, `Dark_Green`, `Light_Green`, `Mud_Green`, `Blue`, `Dark_Blue`, `Light_Blue`, `Royal_Blue`, `Black`, `White`, `Off_White`, `Gray`, `Dark_Gray`, `Silver`, `Cream`, `Magenta`, `Cyan`, `Yellow`, `Mustard`, `Khaki`, `Brown`, `Dark_Brown`, `Violet`, `Pink`, `Dark_Pink`, `Maroon`, `Tan`, `Purple`, `Lavender`, `Turquoise`, `Plum`, `Gold`, `Emerald` `Orange`, `Beige`, `Lilac`, `Olive` |
| 색상 온도 | 이미지의 색상에 대한 일반적인 온기 또는 시원함을 설명합니다. | 색조 또는 온도 값: `warm`, `cool`, `neutral`<br>![색상 및 멋진 색조](../../assets/category/image-color-temp.png){width="200" zoomable="yes"} |
| 이미지 스타일 | 이미지의 시각적 처리. |                                                                                                                                                                                |
| 조명 상태 | 이미지의 조명 유형입니다. |                                                                                                                                                                                |
| 오브젝트 | 이미지를 구성하는 하나 이상의 항목, 엔티티 및 요소를 식별합니다. | ![해바라기, 평면, 꽃 개체](../../assets/category/image-objects.png){width="200" zoomable="yes"} |
| 방향 | 종횡비에 상대적인 이미지 위치입니다. | `landscape`, `portrait`, `square` |
| 사람 | 적어도 한 사람이 존재하는 경우, 하나 이상의 속성은 이미지 내의 사람 또는 사람을 설명할 수 있다. | ![여자 개인 춤](../../assets/category/image-people.png){width="200" zoomable="yes"} |
| 사진 장르 | `abstract` 또는 `landscape`과(와) 같이(가로 방향과 같지 않음) 이미지를 캡처하는 데 사용되는 제목 및 기술을 검색합니다. |           |
| 장면 | 이미지에 표시된 설정 또는 환경을 검색합니다. |                                             |
| 태그 | 특정 분류에 해당하지 않는 오브젝트, 요소 및 기타 이미지 특성을 탐지합니다. |                                      |

<!-- Not yet approved by legal
| Attention distribution  | The level of viewer attention spread across an image.                                                 | `high`, `medium`, `low`                                                                                                                                                                                                    |
| Content density         | The amount of information or detail in an image.                                                      | `high`, `medium`, `low`                                                                                                                                                                                                    |
-->

## 비디오 기능

이미지 기능은 [!DNL Insights]을(를) 사용하여 분석할 비디오 내의 개별적이고 유용한 요소, 소리 또는 패턴을 나타냅니다. 다음 표에는 GenStudio for Performance Marketing AI가 인식하는 비디오 기능 카테고리가 나열되어 있습니다.

| 범주 | 설명 | 예 |
| ------------------- | ------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| 오디오 장르 | 음악이 존재하는 경우, 비디오는 음악 스타일의 하나의 분류(예: `electronic` 또는 `classical`)를 수신할 수 있다. |          |
| 오디오 장르 범주 | 음악이 있는 경우, 비디오는 음악 장르의 하나의 광범위한 분류(예: `acoustic` 또는 `traditional`)를 수신할 수 있습니다. |          |
| 오디오 무드 | `relaxing` 또는 `energetic`과(와) 같은 오디오의 일반 분위기 또는 색조에 대해 설명합니다. |          |
| 오디오 유형 | 오디오가 있으면 비디오가 `music` 또는 `speech`과 같은 하나 이상의 오디오 유형에 대한 태그를 수신할 수 있습니다. |          |
| 오브젝트 | 비디오 전체에 나타나는 하나 이상의 항목, 엔티티 및 요소를 식별합니다. | 비디오의 개체 ![개](../../assets/category/video-objects.png){width="200" zoomable="yes"} |
| 방향 | 프레임의 종횡비에 상대적인 비디오 위치입니다. | `landscape`, `portrait`, `square` |
| 사람 | 적어도 하나의 사람이 존재하는 경우, 하나 이상의 속성은 그 사람 또는 비디오 내의 사람을 기술할 수 있다. |        |
| 장면 | 비디오에 표시된 설정 또는 환경입니다. |        |
| 스타일 | `matte` 또는 `neon`과(와) 같이 비디오의 요소에 적용된 시각적 처리를 검색합니다. |        |
| 태그 | 특정 분류에 해당하지 않는 오브젝트, 요소 및 기타 비디오 특성을 탐지합니다. |        |

## 텍스트 기능

텍스트 기능에는 단어, 문장, 이모티콘 및 [!DNL Insights]을(를) 사용하여 분석하는 데 사용되는 의미, 감정 및 색조와 같은 특정 텍스트 요소에 대한 개수가 포함됩니다. 텍스트가 가독성 점수를 받을 수도 있습니다. 곧 출시 예정

<!-- Not yet approved by legal

The following table lists the image feature categories recognized by the GenStudio for Performance Marketing AI.

| Category             | Description | Example |
|----------------------|-------------|--------|
| Emojis Count         |             |        |
| HashTags Count       |             |        |
| Keywords             |             |        |
| Marketing Emotions   |             |        |
| Narratives           | Text that represents an overarching situation, theme, or a story. Narratives can communicate values, purpose, or identity that resonates with consumers on many levels.   |        |
| Persuasion Strategies|             |        |
| Readability          |             |        |
| Tone of voice        | | |
-->
