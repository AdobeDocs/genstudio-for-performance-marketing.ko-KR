---
title: 텍스트 기능
description: GenStudio for Performance Marketing에 사용되는 속성 범주의 텍스트 기능에 대해 알아봅니다.
feature: Reporting and Insights, Text Attributes, Generative AI
exl-id: 7b81b0ae-0c62-468f-965c-fd8070644fb3
source-git-commit: 3ccc6313a7c559f1c0846c144d23b783da0aecfa
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 1%

---

# 텍스트 기능

텍스트 기능에는 단어, 문장, 이모티콘 및 [!DNL Insights]을(를) 사용하여 분석하는 데 사용되는 의미, 감정 및 색조와 같은 특정 텍스트 요소에 대한 개수가 포함됩니다. 텍스트가 가독성 점수를 받을 수도 있습니다.

GenStudio for Performance Marketing은 Adobe의 AI 및 머신 러닝 기능을 사용하여 텍스트를 학습하고 연결된 텍스트 톤 및 마케팅 이야기를 기반으로 [!UICONTROL 미디어 특성]을 적용합니다. 이 프로세스는 입력 텍스트에 영숫자 문자가 포함되어 있는지 확인하고, 추가 공백과 인쇄할 수 없는 문자를 제거하고, 최대 허용 단어 1500개까지 텍스트를 자릅니다. 감지된 속성 태그를 적용하기 전에 AI는 유행하는 톤을 예측한다.

## 목소리 톤

톤은 언어를 통해 나타나는 일반적인 성격, 태도 또는 분위기를 나타낸다. 단어와 구두점, 문장 구조 및 스타일을 간단히 선택하면 메시지의 톤을 변경할 수 있습니다. 예를 들어 세 가지 기본 톤 레벨을 사용하여 다음 긴급 메시지를 고려하십시오.

| 톤 | 설명 | 예 |
| -------------- | ----------------------------------- | --------------------------------------------------------- |
| 공식 | 세련되고 전문적인 언어. | `Take advantage of this distinctive and exceptional opportunity!` |
| 대화형 | 친숙하고 격식을 차리지 않는 언어. | `Don't miss out on this great opportunity!` |
| 직접 | 간단하고 요점만 말해 | `Don't miss the chance!` |

톤에 대한 다른 보조 값은 메시지의 성격과 태도를 보다 세밀하게 구분합니다. 긴급 메시지의 이전 예제를 유지하면서 GenAI는 다음과 같은 기발한 예에서 _시적인_ 톤을 감지할 수 있습니다. `Embrace the moment, without delay, for this occasion won't always stay.`

다음 표에는 GenStudio for Performance Marketing AI가 인식하는 색조 값이 나열되어 있습니다.

| 톤 | 설명 | 예 |
| -------------- | ------------------------------------------------ | --------------------------------------------------------- |
| 단호해 | 자신감 넘치고 강인한 표현력. | `You need to act now to secure this deal!` |
| 직접 | 간단하고 요점만 말해 | `Don't miss the chance!` |
| 공감 가능하 | 이해와 감수성을 나타냅니다. | `We understand your needs, and this is perfect for you.` |
| 열렬해 | 강렬하고 열정적인 즐거움, 관심 또는 승인을 보여줍니다. | `This is an amazing opportunity you can't miss!` |
| 익살스러우/재치 있음 | 명랑하고 영리해 | `Why wait? Grab this deal before it's gone!` |
| 영감을 주는 | 격려하고 기운을 북돋아 줍니다. | `Believe in yourself and seize this opportunity!` |
| 시적 | 예술적이고 표현력이 풍부합니다. | `Embrace the dawn of a new opportunity.` |
| 양적- | 숫자 데이터 기반. | `99% of users loved this offer, and you will too.` |
| 감각 | 감각을 사로잡는 거지 | `Feel the excitement with this incredible offer!` |
| 스토리텔링 | 메시지를 전달하기 위해 스토리의 내레이션. | `Once upon a time, there was an offer you couldn't refuse.` |

## 감정적 호소

마케터는 인간 감성의 힘을 활용하여 대상과 브랜드 간의 강력한 연결을 만듭니다. 마케터는 행복, 두려움, 흥분 또는 향수와 같은 감각을 활용하여 더 깊은 수준에서 울려 퍼지는 메시지를 만들어 참여를 유도하고 소비자 행동에 영향을 미칠 수 있습니다. 감성적 매력은 더 연관성 있고 기억에 남는 콘텐츠를 전달하는 데 도움이 되어 궁극적으로 브랜드 충성도를 높이고 원하는 행동을 장려합니다.

설득 전술, 마케팅 감정 및 서사 스타일이 협력하여 고객 세그먼트를 타겟팅합니다.

- 진정성, 축하와 커뮤니티 등 **서술 스타일**&#x200B;은(는) 타겟 대상자에게 공감하는 가치와 정체성을 전달하는 데 도움이 되며 보다 매력적이고 관련성 있는 메시지를 만듭니다.
- 희소성, 사회적 증거, 호혜성과 같은 **설득 전략**&#x200B;은 소비자의 감정과 선호도에 호소하여 소비자 행동에 영향을 미치도록 설계되었습니다.
- **마케팅 감정**&#x200B;은(는) 브랜드에 대한 참여도와 연결을 향상시키는 느낌을 자극하는 것을 목표로 합니다.

GenStudio for Performance Marketing AI는 정서적 신호나 음색, 서사적 스타일에 대한 텍스트를 분석하여 이러한 특성을 감지하고 구분한다. AI가 자연어 처리(NLP)와 머신러닝 알고리즘을 활용해 패턴을 파악하고 사전 정의된 정서적·설득적 속성에 따라 텍스트를 분류한다.

### 이야기 스타일

이야기 요소 또는 매력 요소 속성은 타겟 대상자와 공감을 주는 가치, 목적 또는 정체성을 전달하는 미디어를 식별하는 데 도움이 됩니다. 다음 표에는 GenStudio for Performance Marketing AI가 인식하는 서사 스타일이 나열되어 있습니다.

| 어필 요인 | 설명 | 예 |
| ----------------- | --------------------------------------------------------------------- | ------------------------------------------ |
| 신뢰성 | 진실하고 진실하며, 종종 투명성과 정직함을 강조한다. | `A behind-the-scenes look at how our products are made.` |
| 축하 | 특별한 경우나 성과를 기쁨과 축제로 표시. | `Join us in celebrating our 10th anniversary with special offers!` |
| 커뮤니티 | 집단 간의 소속감과 연대감을 기른다. | `Our brand is built on the strength of our community.` |
| 편리함 | 사용 편의성과 시간 절약형 혜택을 강조한다. | `Get what you need with just one click.` |
| 권한 부여 | 개인이 통제권을 가지고 결정을 내릴 수 있도록 장려하고 가능하게 한다. | `Empower yourself with our latest tools and resources.` |
| 탐험 | 종종 새로운 경험과 연관된 발견 및 모험을 초대합니다. | `Discover new horizons with our travel packages.` |
| 미래 지향적 | 혁신과 전향적 사고를 강조합니다. | `Experience the future of technology today.` |
| Hype | 제품 또는 이벤트에 대한 흥미와 기대감을 생성합니다. | `Don't miss out on the most anticipated event of the year!` |
| 방종 | 환상, 욕망 또는 즐거움에 호소합니다. | `Treat yourself to the finest gourmet chocolates.` |
| 마음의 평화 | 안심감 및 안정감을 제공합니다. | `Rest easy knowing your data is safe with us.` |
| 개인화 | 경험 또는 제품을 개별 환경 설정에 맞춤화합니다. | `Get a custom-fit solution just for you.` |
| 프레스티지 | 높은 지위 및 배타성과 연결. | `Join the elite with our premium membership.` |
| 무기력 | 지속적인 품질과 고전적인 매력을 강조합니다. | `Our designs are timeless and never go out of style.` |
| 다용성 | 적응성 및 여러 용도를 강조합니다. | `Our product fits seamlessly into any lifestyle.` |
| 웰빙 | 건강, 행복 및 전반적인 건강을 증진합니다. | `Enhance your well-being with our holistic approach.` |

### 설득 전술

소비자 행동에 영향을 미치고 원하는 행동을 유도하기 위해 설득 기법이 사용된다. 이러한 전략은 마케팅 메시지의 효과를 높이기 위해 특정 심리적 트리거와 고객 세그먼트를 타깃팅합니다. 다음 표에는 GenStudio for Performance Marketing AI가 인식하는 설득 전술이 나열되어 있다.

| 전술 | 설명 | 예 |
| --------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------- |
| 의인화 | 인간의 특성을 제품 또는 브랜드에 기여합니다. | `Our friendly chatbot is here to help you.` |
| 비교 | 옵션 간의 차이점을 강조 표시하여 선택에 영향을 줍니다. | `See how we compare to the competition.` |
| 구체성 | 메시지를 보다 구체적으로 만들기 위한 특정 세부 정보를 제공합니다. | `Save 20% on your next purchase.` |
| 보증 | 신뢰할 수 있는 소스 또는 영향력자의 승인 제공. | `Recommended by top industry experts.` |
| 문에 발 넣기 | 작은 요청부터 시작하여 더 큰 요청으로 합의 가능성을 높입니다. | `Try our free trial today.` |
| 리액턴스 극복 | 이의 제기 사항을 인정하고 해결하여 저항을 줄입니다. | `We understand your concerns, and here's how we address them.` |
| 상호성 | 답례품을 조장하기 위해 가치 있는 것을 제공하다. | `Get a free gift with your purchase.` |
| 희소성 | 제한된 가용성을 강조 표시하여 긴급성을 유발합니다. | `Only a few items left in stock!` |
| 소셜 ID | 소비자의 그룹 소속감을 활용합니다. | `Join our community of innovators.` |
| 소셜 임팩트 | 사회나 환경에 미치는 긍정적인 영향을 강조한다. | `Your purchase helps plant a tree.` |
| 소셜 증명 | 추천을 사용하거나 사용자가 생성한 콘텐츠를 사용하여 신뢰를 구축합니다. | `See why thousands of users love our product.` |

### 마케팅 감정

감성은 마케팅 메시지에서 타겟팅되어 대상자로부터 특정 감정과 반응을 불러일으키고, 이는 브랜드와 참여 및 연결을 강화할 수 있습니다. 다음 표에는 GenStudio for Performance Marketing AI가 인식하는 감정이 나열되어 있습니다.

| 감정 | 설명 | 예 |
| ------------- | --------------------------------------------------------------------------- | --------------------------------------------------------- |
| 흡인 | 더 큰 것을 성취하거나 성취하려는 욕망을 불러일으키다. | `Imagine the possibilities with our premium service.` |
| 과제 | 장애물을 극복하거나 새로운 과제를 수용할 수 있도록 관객을 격려한다. | `Are you ready to take the next step in your career?` |
| 큐리오시티 | 더 많은 것을 배우고 싶은 욕구와 흥미를 유발합니다. | `Discover the secrets behind our success.` |
| 배타성 | 선택한 그룹에 속해 있는 감을 만듭니다. | `Join our exclusive club for members-only benefits.` |
| 매혹 | 흥미롭고 흥미로운 콘텐츠로 관객을 사로잡습니다. | `Be amazed by our latest innovations.` |
| 만족 | 제품이나 서비스 이용으로부터 만족과 즐거움을 제공하는 것. | `Enjoy the ultimate comfort with our luxury bedding.` |
| 인식 | 청중의 성취나 지위를 인정하고 가치 있게 평가하는 것이다. | `Get the recognition you deserve with our award-winning service.` |
| 트러스트 | 브랜드에 대한 신뢰도와 신뢰성 강화. | `Trust us to deliver quality and excellence every time.` |
| 긴급도 | 시간에 민감한 기회를 강조하여 즉각적인 조치를 촉구합니다. | `Act now before this limited-time offer expires!` |

## 가독성 점수

가독성 점수는 텍스트 한 조각을 읽고 이해하는 것이 얼마나 쉬운지를 평가합니다. 이렇게 하면 콘텐츠가 타겟 대상자에게 적절한지 확인할 수 있습니다. 점수는 문장 길이, 단어 복잡성 등 다양한 요인에 기반한다. 다음 표에는 GenStudio for Performance Marketing AI가 인식하는 가독성 수준이 나열되어 있습니다.

| 가독성 수준 | 설명 | 예 |
| ------------------- | ------------------------------------------------------------------ | --------------------------------------------------------- |
| 학년 | 매우 간단한 언어, 어린 아이들에게 적합합니다. | `The cat sat on the mat.` |
| 학년 | 일반 대상자에게 적합한 간단하고 명확한 언어. | `You can find great deals on our website.` |
| 학년 | 간단한 어휘와 구조로 이해하기 쉽습니다. | `Our new product is simple to use and very effective.` |
| 8학년 및 9학년 | 청소년에게 적합한 명확하고 간결한 언어. | `This guide will help you understand the basics of our service.` |
| 10~12학년 | 보다 복잡한 언어는 10대 노인과 성인에게 적합합니다. | `The comprehensive manual provides detailed instructions for setup.` |
| 칼리지 | 고등 교육을 받은 대상자에게 적합한 고급 언어입니다. | `The study explores the multifaceted implications of the new policy.` |
| 대학 졸업자 | 전문가 및 전문가에게 적합한 고급 언어. | `The dissertation delves into the intricacies of quantum mechanics.` |

## 카운트

해시태그 수, 단어 수, 문장 수 및 정지어 비율과 같은 카운트 속성을 이해하고 활용하면 콘텐츠 전략을 크게 향상시킬 수 있습니다. 이러한 지표는 마케팅 노력의 효율성과 도달 정도에 대한 중요한 통찰력을 제공합니다. 다음 표에는 GenStudio for Performance Marketing AI가 인식하는 카운트 범주가 나열되어 있습니다.

| 범주 | 설명 | 예 |
| --------------------- | --------------------------------------------------------------------------- | --------------------- |
| 이모티콘 수 | 텍스트에 있는 이모지 수입니다. 이모티콘은 참여를 높이고 감정을 빠르게 전달할 수 있습니다. | `😊`, `🚀`, `❤️` |
| 해시 태그 수 | 텍스트에 사용된 해시태그의 수입니다. 해시태그는 콘텐츠를 분류하고 소셜 미디어에서 검색 가능성을 높이는 데 도움이 됩니다. | `#Marketing`, `#Sale` |
| 문장당 단어 수 | 텍스트의 문장당 평균 단어 수입니다. 문장이 짧을수록 읽고 이해하기가 더 쉬운 경우가 많다. | `10` |
| 단어 수 | 텍스트의 총 단어 수입니다. 단어 수가 많을수록 더 자세한 정보를 얻을 수 있지만 읽기 위한 노력이 더 많이 필요할 수도 있습니다. | `1500 words` |
| 정지어 비율 | 텍스트 내 의미 있는 단어에 대한 정지어의 비율입니다. 정지어(예: &quot;a&quot; &quot;an&quot; &quot;the&quot;)는 검색 쿼리 및 결과에서 무시되는 경우가 많습니다. 정지어 비율이 높으면 콘텐츠의 참여도가 떨어지고 읽기 어려워질 수 있습니다. | `0.375` |
| 문장 수 | 텍스트에 있는 총 문장 수입니다. 더 많은 문장은 더 자세한 내용을 나타낼 수 있지만, 지나치게 긴 텍스트는 독자의 흥미를 잃게 할 수 있다. | `75 sentences` |
