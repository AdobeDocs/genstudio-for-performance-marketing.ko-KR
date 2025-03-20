---
title: 텍스트 기능
description: GenStudio for Performance Marketing에 사용되는 속성 범주의 텍스트 기능에 대해 알아봅니다.
feature: Reporting and Insights, Text Attributes, Generative AI
hide: true
hidefromtoc: true
recommendations: noDisplay, noCatalog
exl-id: 7b81b0ae-0c62-468f-965c-fd8070644fb3
source-git-commit: 3448392bc3f1496dafdbed2995f40bdba9c91c31
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 1%

---

# 텍스트 기능

텍스트 기능에는 단어, 문장, 이모티콘 및 [!DNL Insights]을(를) 사용하여 분석하는 데 사용되는 의미, 감정 및 색조와 같은 특정 텍스트 요소에 대한 개수가 포함됩니다. 텍스트가 가독성 점수를 받을 수도 있습니다.

GenStudio for Performance Marketing은 Adobe의 AI 및 머신 러닝 기능을 사용하여 텍스트를 학습하고 연결된 텍스트 톤 및 마케팅 이야기를 기반으로 [!UICONTROL 미디어 특성]을 적용합니다. 이 프로세스는 입력 텍스트에 영숫자 문자가 포함되어 있는지 확인하고, 추가 공백과 인쇄할 수 없는 문자를 제거하고, 최대 허용 단어 1500개까지 텍스트를 자릅니다. 감지된 속성 태그를 적용하기 전에 AI는 유행하는 톤을 예측한다.

## 목소리 톤

톤은 언어를 통해 나타나는 일반적인 성격, 태도 또는 분위기를 나타낸다. 단어와 구두점, 문장 구조 및 스타일을 간단히 선택하면 메시지의 톤을 변경할 수 있습니다. 예를 들어 세 가지 기본 톤 레벨을 사용하여 다음 긴급 메시지를 고려하십시오.

- `Formal`

  ```
  Take advantage of this distinctive and exceptional opportunity!
  ```

- `Conversational`

  ```
  Don't miss out on this great opportunity!
  ```

- `Direct`

  ```
  Don't miss the chance!
  ```

AI는 더 미묘한 어조를 감지합니다. 이전 예제와 동일한 긴급 문을 사용하는 다음 버전에서는 기발한 `poetic` 톤을 사용합니다.

- `Poetic`

  ```
  Embrace the moment, without delay, for this occasion won't always stay.
  ```

색조에 대한 다른 보조 값은 `Enthusiastic`, `Assertive`, `Humorous/Witty`, `Inspirational`, `Empathetic`, `Sensory`, `Storytelling`, `Poetic`, `Quantitative`, `Personal`입니다.

## 이야기

이야기 속성을 통해 타겟 대상자와 공감을 주는 가치, 목적 또는 정체성을 전달하는 미디어를 식별할 수 있습니다.

| 이야기 | 설명 | 예 |
| ----------------- | ----------- | ------- |
| `Authenticity` |             |         |
| `Celebration` |             |         |
| `Community` |             |         |
| `Convenience` |             |         |
| `Empowerment` |             |         |
| `Exploration` |             |         |
| `Futuristic` |             |         |
| `Hype` |             |         |
| `Indulgence` |             |         |
| `Peace of mind` |             |         |
| `Personalization` |             |         |
| `Prestige` |             |         |
| `Timelessness` |             |         |
| `Versatility` |             |         |
| `Well-being` |             |         |

## 가독성 점수

가독성 점수는 텍스트 한 조각을 읽고 이해하는 것이 얼마나 쉬운지를 평가합니다. 이렇게 하면 콘텐츠가 타겟 대상자에게 적절한지 확인할 수 있습니다. 점수는 문장 길이, 단어 복잡성 등 다양한 요인에 기반한다.

| 점수 | 학교 수준 | 메모 |
| ----------- | ------------------ | ------------------------------------------------------------------------- |
| 100.00-90.00 | 학년 | 읽기 매우 쉽습니다. 보통 11세의 학생도 쉽게 이해할 수 있다. |
| 90.0-80.0 | 학년 | 읽기 쉽습니다. 소비자를 위한 대화식 영어. |
| 80.0-70.0 | 학년 | 읽기가 아주 쉬워 |
| 70.0-60.0 | 8학년 및 9학년 | 쉬운 영어. 13세에서 15세의 학생들이 쉽게 이해할 수 있다. |
| 60.0-50.0 | 10~12학년 | 읽기가 꽤 어려워요. |
| 50.0-30.0 | 칼리지 | 읽기 어려움. |
| 30.0-0.0 | 대학 졸업자 | 읽기가 매우 어려워요. 대학 졸업생들에 의해 가장 잘 이해된다. |

## 단어 수

TBD

다음 표에는 GenStudio for Performance Marketing AI가 인식하는 이미지 기능 카테고리가 나열되어 있습니다.

| 범주 | 설명 | 예 |
| -------------------- | ------------- | --------------------- |
| 이모티콘 수 |             |        |
| 해시 태그 수 |             |        |
| 키워드 |             |        |
| 마케팅 감정 | 감성은 마케팅 메시지에서 타겟팅되어 대상자로부터 특정 감정과 반응을 불러일으키고, 이는 브랜드와 참여 및 연결을 강화할 수 있습니다. | `Aspiration`, `Challenge`, `Curiosity`, `Exclusivity`, `Fascination`, `Gratification`, `Recognition`, `Trust`, `Urgency` |
| 설득 전략 | 소비자 행동에 영향을 주고 원하는 행동을 유도하는 데 사용되는 기법입니다. 이러한 전략은 마케팅 메시지의 효과를 높이기 위해 특정 심리적 트리거와 고객 세그먼트를 타깃팅합니다. | `Social identity`, `Social proof`, `Endorsement`, `Concreteness`, `Foot in the door`, `Overcoming reactance`, `Reciprocity`, `Comparison`, `Social impact`, `Scarcity`, `Anthropomorphism` |
| 목소리 톤 | 단어 선택, 구두점, 문장 구조 및 스타일을 통해 마케팅 메시지로 전달되는 일반적인 문자, 태도 또는 분위기. | `Enthusiastic`, `Assertive`, `Humorous/Witty`, `Inspirational`, `Empathetic`, `Sensory`, `Storytelling`, `Poetic`, `Quantitative`, `Personal` |
