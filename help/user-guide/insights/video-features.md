---
title: 비디오 기능
description: GenStudio for Performance Marketing에 사용되는 속성 범주의 비디오 기능에 대해 알아봅니다.
level: Intermediate
feature: Reporting and Insights, Video Attributes, Generative AI
exl-id: 0dfdd735-b365-4a15-a6fd-e981697442cb
source-git-commit: 72cd93d9d6fdd99d5a524d05cba923e9c0191960
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 1%

---

# 비디오 기능

비디오 기능은 [!DNL Insights]을(를) 사용한 분석을 위해 비디오 내의 구별되고 유용한 요소, 소리 또는 패턴을 나타냅니다. 이러한 기능은 비디오 콘텐츠를 분류하고 이해하는 데 도움이 되므로 보다 정확하고 자세한 통찰력을 얻을 수 있습니다. AI가 오디오 무드, 음악 장르, 사물 등 다양한 속성을 파악해 영상을 종합적으로 분석해 더 나은 의사결정과 전략 수립에 도움을 줄 수 있다.

## 오디오 감지

GenStudio for Performance Marketing의 오디오 감지에는 다양한 속성을 식별하기 위해 비디오의 오디오 트랙을 분석하는 작업이 포함됩니다. 이 검출 프로세스는 존재하는 오디오의 유형을 식별하고, 특정 장르나 음악 범주에 태깅하고, 음성에서 키워드를 추출함으로써 오디오의 전반적인 분위기를 결정합니다. 이러한 오디오 요소를 이해함으로써 AI가 비디오의 콘텐츠와 맥락에 대한 심층적인 통찰력을 제공하여 전반적인 분석과 분류 프로세스를 향상시킬 수 있다.

## 비디오 기능 검색

**비디오를 미리 보고 오디오 샘플을 들으려면**:

1. _[!DNL Insights]_에서&#x200B;**[!UICONTROL 특성]**보기를 선택하십시오.

1. **[!UICONTROL 비디오]**&#x200B;를 선택하여 테이블 보기를 변경합니다.

1. **[!UICONTROL 특성 범주]** 목록에서 기능을 선택하십시오. 오디오의 경우 **음악 장르**&#x200B;를 선택하십시오.

1. 해당 카테고리를 공유하는 비디오의 상세 보기에 대한 속성을 선택합니다.

   예를 들어 `Music genre` 범주는 `electronic`을(를) 특성으로 가질 수 있습니다.

1. _특성 세부 정보_ 페이지에는 이 특성을 가진 모든 비디오가 나열됩니다. 비디오 미리 보기를 시작하려면 목록의 비디오 위에 마우스 포인터를 놓습니다.

1. **음소거 해제**(비디오 미리 보기의 왼쪽 아래 모서리에 있음) 단추를 전환하고 비디오 미리 보기의 오디오를 듣습니다.

다음 표에는 GenStudio for Performance Marketing AI가 인식하는 비디오 기능 카테고리가 나열되어 있습니다. 미디어 콘텐츠에 대해 검색된 속성 목록이 완전하지 않습니다. 풍부한 기능 세트를 포함하는 미디어는 AI가 식별하는 가장 지배적인 3가지 기능으로 제한될 수 있습니다.

<!-- For the writer: turn off word wrap to work with these tables. Option + Z -->

| 범주 | 설명 | 예 |
| ------------------- | ------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| 오디오 무드 | `calm`, `upbeat` 또는 `tense`과(와) 같은 오디오 트랙의 전반적인 감정 톤 또는 분위기를 결정합니다. | `Energetic`, `Happy`, `Emotional Ambient/atmospheric`, `Relaxing`, `Dramatic`, `Expressive/characterful`, `Intense`, `Slow`, `Neutral` |
| 오디오 유형 | 하나 이상의 오디오 콘텐츠 형식(예: `music` 또는 `speech`)이 있는 비디오에 태그를 지정합니다. | `Music`, `Speech`, `Silence`, `Special effects`, `Ambience` |
| 카테고리 | 비디오를 하나 이상의 광범위한 콘텐츠 카테고리로 분류합니다. | `Entertainment`, `Sports`, `Music`, `Gaming`, `Howto tutorials`, `Fashion and style`, `Film and animation`, `Science and technology`, `Autos and vehicles`, `Pets and animals`, `People and blogs`, `News and politics`, `Social causes and activism`, `Travel and events`, `Education`, `Sales and offers` |
| 음악 카테고리 | 비디오에 음악이 있는 경우 음악 장르의 광범위한 분류. 장르는 `contemporary` 또는 `traditional` 스타일과 같은 일반적인 음악 형식을 식별하는 데 도움이 됩니다. | `Contemporary/pop music`, `Traditional/folk-based music`, `Instrumental/orchestral music`, `Rock music`, `Acoustic/unplugged music`, `Specialised/occasional music`, `Experimental/unique music` |
| 음악 장르 | 비디오에 음악이 있는 경우 음악 스타일의 특정 분류로, `electronic` 또는 `jazz`과 같이 음악에 대한 보다 자세한 식별을 제공합니다. | `electronic`, `hip-hop`, `dance`, `novelty`, `rock`, `world`, `reggae`, `pop`, `film`, `jazz`, `background`, `latin` |
| 오브젝트 | 비디오에 나타나는 하나 이상의 항목, 엔티티 및 요소를 식별합니다. | 값이 너무 많지만 `backpack`, `book`, `hawk`, `glasses`, `fish`, `pencil`, `mountain bike`, `soap` 등이 있습니다. |
| 방향 | 폭 및 높이를 기준으로 한 비디오 맞춤입니다. 큰 키보다 넓은지(가로), 넓은 키보다 큰지(세로) 또는 폭과 높이가 같은지(사각형) 여부를 검색합니다. | `landscape`, `portrait`, `square` |
| 사람 | 적어도 하나의 사람이 존재하는 경우, 하나 이상의 속성은 사람, 또는 비디오 내에 존재하는 사람을 기술할 수 있다. | `person`, `woman`, `man`, `girl`, `boy`, `social group`, `kid`, `crowd`, `people` |
| 장면 | 비디오 내의 설정이나 환경을 식별하여 비디오가 만들어진 위치나 묘사된 위치 유형에 대한 컨텍스트를 제공합니다. | 값이 너무 많지만 `lake`, `underwater`, `highway`, `hill`, `log cabin`, `island`, `beach`, `lounge` 등이 있습니다. |
| 스타일 | After Effects 또는 Lightroom에서 사용되는 시각적 처리와 같이 비디오 요소에 적용되는 시각적 처리를 검색합니다. | `design`, `illustration`, `logo`, `square`, `cartoon`, `art`, `matte`, `neon` |
| 태그 | 특정 분류에 해당하지 않는 다른 비디오 특성을 검색합니다. 태그는 비디오에 대한 추가 컨텍스트 및 메타데이터를 제공합니다. | 값이 너무 많지만 `construction`, `gothic`, `healing`, `military`, `selfie`, `football`, `typing`, `dancer`, `dancing` 등이 있습니다. |
