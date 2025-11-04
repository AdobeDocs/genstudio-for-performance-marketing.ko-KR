---
title: 템플릿 우수 사례
description: Adobe GenStudio for Performance Marketing에서 템플릿을 사용할 때 모범 사례를 따르십시오.
level: Intermediate
role: Developer, User
feature: Media Templates, Content Generation, Brand Personalization
exl-id: 3ff24fec-e836-4202-80f8-ba165e173b75
source-git-commit: 3fe6e235b774cf5a99627d981230f96d5e51ac02
workflow-type: tm+mt
source-wordcount: '678'
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

## 템플릿에 대한 이미지 업로드

템플릿에 사용되는 이미지는 컨텐츠 리포지토리에서 가져와야 하며, 이미지가 정확하게 표시되도록 하려면 올바르게 업로드해야 합니다.

템플릿에 가장자리에서 가장자리로(전체 도련) 이미지가 있으면 선택한 이미지의 크기가 전체 템플릿 크기에 맞게 자동으로 조정됩니다. 그러나 이미지가 템플릿 종횡비와 일치하지 않으면 이미지가 템플릿 크기에 맞게 잘리며 예상대로 표시되지 않을 수 있습니다.

템플릿에 포함된 이미지에 대한 &quot;자동 맞춤&quot; 기능은 없습니다.

이미지 자르기를 해결하려면 사용자는 콘텐츠 저장소에 업로드할 때 템플릿에 사용할 이미지의 종횡비를 정의해야 합니다. 승인된 템플릿을 업로드할 때:

1. [템플릿 업로드 프로세스를 계속 진행](/help/user-guide/content/use-templates.md#add-a-template)한 다음 **[!UICONTROL 세부 정보 추가]** 페이지에 액세스합니다.

2. 템플릿에 사용할 이미지의 종횡비를 **[!UICONTROL 광고 너비(px)]** 및 **[!UICONTROL 광고 높이(px)]**&#x200B;로 정의합니다. 이렇게 하면 이미지가 표시되는 템플릿의 섹션에 대한 이미지 창이 정의됩니다.

3. **[!UICONTROL 추가 세부 정보]** 섹션에서 **[!UICONTROL 이미지 크기]** 드롭다운을 선택하고 _고정 크기로 자르기_를 선택합니다.
   ![고정 크기로 자르기](./images/crop-to-fixed-size.png "고정 크기로 자르기"){width="80%"}

브라우저에서 이미지의 크기 및 종횡비를 결정하려면 다음을 수행하십시오.

1. 이미지를 검사합니다.
   - Windows/Linux:
      - F12 키를 누릅니다.
   - macOS:
      - Command + Option + I를 누릅니다.

1. 이미지 위로 마우스를 가져갑니다.

1. 종횡비를 확인합니다. 템플릿에서 이미지의 종횡비를 정의할 때 사용합니다.

이러한 세부 사항이 업로드 중에 적용되지 않으면 이미지는 템플릿의 전체 종횡비로 간주되며 해당 종횡비와 일치하지 않는 이미지는 잘린 것으로 표시됩니다.

![디스플레이 광고에서 자른 이미지](./images/cropped-display.png "이미지 자르기"){width="60%"}

디스플레이 광고 템플릿에서 잘린 **❌이미지**

![디스플레이 광고에 표시되는 이미지](./images/full-fit.png "디스플레이 광고에 표시되는 이미지"){width="60%"}

**✅이미지가 완전히 표시됨**

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
