---
title: 템플릿 우수 사례
description: Adobe GenStudio for Performance Marketing에서 템플릿을 사용할 때 모범 사례를 따르십시오.
level: Intermediate
role: Developer, User
feature: Media Templates, Content Generation, Brand Personalization
exl-id: 3ff24fec-e836-4202-80f8-ba165e173b75
source-git-commit: c0f45fb0ffc61d20611693498f1b12d3946ca6ca
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# 템플릿 사용 우수 사례

템플릿은 사전 구성된 레이아웃 및 디자인 요소를 포함하는 시작점을 제공하여 새 콘텐츠를 생성하는 데 필요한 시간과 노력을 크게 줄입니다.

GenStudio for Performance Marketing에서 템플릿을 사용할 때 다음 권장 사항을 사용하십시오.

1. [템플릿 요소](#know-about-template-elements)에 대해 알아보기
1. 콘텐츠의 효과적인 개인화를 위해 [채널 지침](#configure-channel-guidelines)을(를) 구성하십시오.
1. 최적의 환경을 위해 [접근성 표준](accessibility-for-templates.md)으로 디자인
1. [채널별 템플릿 지침 준수](#follow-channel-specific-template-guidelines)

>[!TIP]
>
>[템플릿 작업](use-templates.md)에서 기본 템플릿 요소 및 절차에 대해 자세히 알아보세요. 다음 캠페인에서 사용할 [템플릿 사용자 지정](customize-template.md)에 대해 자세히 알아봅니다.

## 템플릿 요소에 대해 알아보기

가장 좋은 방법은 템플릿의 부분을 숙지하는 것입니다. 각 템플릿 유형은 서로 다른 요소를 사용하여 채널별 콘텐츠 작성 구조를 만듭니다. 템플릿을 사용자 지정하려면 콘텐츠를 생성하는 데 GenStudio for Performance Marketing이 필요한 이러한 요소 대신 필드 이름을 사용하십시오.

[템플릿 요소](use-templates.md#template-elements)를 참조하십시오.

## 채널 지침 구성

명확한 채널 지침을 정의하는 것은 생성된 콘텐츠가 브랜드의 요구 사항 및 목표에 부합하는지 확인하는 데 필수적입니다. 채널 가이드라인을 사용하여 템플릿에 사용되는 톤, 길이 및 스타일과 같은 요소에 대한 규칙을 지정할 수 있습니다. 예를 들어 본문의 최대 문자 수를 설정하거나 특정 call-to-action 스타일이 필요할 수 있습니다. 이러한 지침을 미리 설정하면 각 AI 프롬프트에서 자세한 지침을 작성할 필요가 줄어들어 콘텐츠 생성 프로세스를 간소화하고 이메일 전반에서 일관성을 보장할 수 있습니다.

템플릿의 모든 키 필드에 대한 브랜드의 [채널 지침](/help/user-guide/guidelines/brands.md#channel-guidelines)을 검토하고 정의합니다. 지침을 정의하지 않으면 [기본 채널 지침](/help/user-guide/guidelines/brands.md#default-channel-guidelines)이 적용되며, 이는 브랜드 요구 사항을 완전히 반영하지 않을 수 있습니다.

![본문 사양](/help/assets/channel-email-body.png)

[브랜드, 제품 및 가상 사용자 지침](/help/user-guide/guidelines/overview.md)이 생성된 콘텐츠에 어떻게 영향을 미치며 마케팅 목표에 맞게 콘텐츠를 조정하는 방법을 알아봅니다.

## 채널별 템플릿 지침 준수

템플릿을 만들 때 의도한 채널의 특정 요구 사항을 충족하는지 확인하십시오. 각 채널의 레이아웃 및 시각적 요구 사항을 충족하는 템플릿을 빌드합니다. 다음과 같이 모든 템플릿에 적용되는 일반 지침이 있습니다.

- 깔끔하고 반응형 HTML 및 인라인 CSS 사용
- Adobe 또는 Google 글꼴 사용
- JavaScript을 사용하지 **않음**

{{note-css-effects}}

최적의 성능을 보장하기 위해 각 템플릿 유형을 사용할 때 다음과 같은 추가 팁과 제한을 참조하십시오.

- [이메일](/help/user-guide/templates/email-template.md)
- [광고 표시 및 배너](/help/user-guide/templates/display-template.md)
- [LinkedIn](/help/user-guide/templates/linkedin-template.md)
- [Meta 광고](/help/user-guide/templates/meta-template.md)
