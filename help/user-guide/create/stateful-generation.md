---
title: 상태 저장 생성으로 콘텐츠 생성 및 세분화
description: '[!DNL GenStudio for Performance Marketing]에서 음성 인쇄 및 시각적 큐를 포함하는 대화를 통해 브랜드 내 콘텐츠를 생성하고 차례대로 구체화하는 방법에 대해 알아봅니다.'
feature: Create Prompt, Generative AI, Content Generation
role: User
level: Beginner
source-git-commit: 22db02c07a9f33cb1c70df9286ad6eb143dafd38
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%
---
# 상태 저장 생성으로 콘텐츠 생성 및 세분화

[!DNL GenStudio for Performance Marketing]은(는) Stateful Generation을 사용하여 매번 새 프롬프트로 다시 시작하지 않고 브랜드의 콘텐츠를 만든 다음 대화를 통해 차례로 세분화합니다. 세분화할 때 생성은 이전 지침과 유지한 변형을 기억한 다음 요청한 변경 사항만 적용합니다.

Stateful Generation은 세대에 세 가지 종류의 컨텍스트를 추가합니다. voiceprinting은 브랜드 음성으로 사본을 유지하고 이미지 또는 비디오에서 시각적 큐 그라운드 복사를 사용하며, 웹 페이지 URL은 선택한 페이지에서 참조 컨텍스트를 추가합니다.

## 콘텐츠 생성 및 세분화

1. [!DNL GenStudio for Performance Marketing]에서 채널 및 형식에 대한 생성을 시작합니다. 각 채널에 대한 생성을 시작하려면 [[!DNL Create] 개요](/help/user-guide/create/overview.md)를 참조하세요.
1. _선택 사항_: 복사한 내용을 자체 Creative로 지정하려면 **[!UICONTROL 콘텐츠에서 선택]**&#x200B;을 선택한 다음 [시각적 큐](#ground-content-in-an-image-or-video)로 사용할 이미지 또는 비디오를 선택하십시오.
1. **[!UICONTROL 생성]**&#x200B;을 선택하십시오. [!DNL GenStudio for Performance Marketing]은(는) 변형 집합을 만들고 지원되는 채널에서 [브랜드 음성](#keep-copy-in-your-brand-voice)을(를) 자동으로 적용합니다.
1. 프롬프트 서랍에서 결과를 세분화합니다. `shorten the headline`, `make variant 2 punchier` 또는 `change the headline` 등 원하는 변경 내용을 입력하십시오. 세대는 해당 변경 사항만 적용하고 이전 지침을 유지합니다.
1. 계속 세분화하는 동안 변형을 유지하려면 프롬프트 창에 `keep variant 2`과(와) 같은 지침을 입력하십시오.
1. 콘텐츠가 준비되면 내보내거나 검토를 위해 보냅니다.

## 이미지 또는 비디오의 그라운드 콘텐츠

시각적 큐를 통해 사용자는 첨부한 이미지나 비디오를 읽은 다음 해당 창의성을 반영하는 사본을 작성할 수 있습니다. **[!UICONTROL Creative 옵션]** 토글 컨트롤은 시각적 큐를 제어하며 기본적으로 켜져 있습니다.

시각적 큐를 사용하려면 **[!UICONTROL 콘텐츠에서 선택]**&#x200B;을 선택하고 생성하기 전에 이미지 또는 비디오를 선택하십시오. 시각적 큐 없이 생성하려면 **[!UICONTROL Creative 옵션]**&#x200B;을 끕니다.

>[!NOTE]
>다중 프레임 디스플레이 광고 또는 회전식 광고에는 시각적 큐를 사용할 수 없습니다.

## 브랜드 보이스로 카피 보관

음성 인쇄는 브랜드의 학습된 음성을 생성된 사본에 적용하여 별도의 프롬프트 없이 브랜드에서 들리게 합니다. LinkedIn 및 Meta과 같이 [Insights](/help/user-guide/insights/overview.md)가 있는 채널의 경우 기본적으로 설정되어 있습니다.

## 웹 페이지를 컨텍스트로 사용

웹 페이지에서 생성을 지정하고 해당 콘텐츠를 컨텍스트로 사용할 수 있습니다. 프롬프트 창에 `Use this URL to generate an ad for this channel: https://www.example.com`과(와) 같이 URL이 포함된 지침을 입력합니다.

>[!NOTE]
>프롬프트에 URL을 입력합니다. _매개 변수_&#x200B;를 통해 추가하지 마십시오.

## 관련 기능

- [변형 관리](/help/user-guide/create/manage-variants.md): 캔버스에서 생성된 변형을 직접 편집하고 미세 조정합니다.
- [유효한 프롬프트를 작성하십시오](/help/user-guide/effective-prompts.md): 더 나은 결과를 생성하는 메시지를 작성하십시오.
