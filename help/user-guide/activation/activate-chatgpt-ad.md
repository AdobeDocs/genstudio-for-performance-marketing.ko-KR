---
title: ChatGPT 광고 활성화
description: ChatGPT 광고 경험을 활성화하는 방법을 알아봅니다.
feature: Ad Activation
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
    internal-label: GenStudio for Performance Marketing
feature_v2:
  - id: bffd9bc2-7f41-4bf6-9f08-f14cbd37afd7
    internal-label: Campaigns
  - id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3a
    internal-label: Create
subfeature_v2:
  - id: d87258a7-722c-4afd-b632-adddc447c7aa
    internal-label: Ad activation
  - id: e3878dde-4b87-4290-9e81-ed7ee6eb83fe
    internal-label: Experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
source-git-commit: 17b2262615e10d82905ce7ebec65857e9a0b9f2a
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%
---
# ChatGPT 광고 활성화

Adobe GenStudio for Performance Marketing은 ChatGPT 광고 경험 활성화를 지원합니다.

**지원되는 형식**: 채팅 카드입니다.

GenStudio for Performance Marketing에서 [ChatGPT 경험을 만들기](/help/user-guide/create/create-chatgpt-ad.md)한 다음 활성화하도록 선택할 수 있습니다.

ChatGPT 광고를 활성화하면 다른 유료 광고 채널을 활성화하는 데 필요한 [동일한 일반 단계](create-activation.md)를 따릅니다. 이 페이지에서는 ChatGPT 관련 사전 요구 사항 및 설정 필드를 다룹니다. GenStudio for Performance Marketing에서 ChatGPT 경험을 활성화한 후 OpenAI Ads Manager를 사용하여 최종 검사를 실행하고 광고를 시작합니다.

GenStudio 시스템 관리자 및 편집자는 광고 경험을 활성화할 수 있습니다.

## 사전 요구 사항

* OpenAI Ads 계정 및 해당 계정의 API 키.
* 대상 ChatGPT 캠페인 및 광고 그룹이 OpenAI Ads Manager에 이미 있어야 합니다. GenStudio for Performance Marketing은 새 캠페인이나 광고 그룹을 만들지 않습니다.

## ChatGPT 계정 연결

조직에서 경험을 활성화하려면 먼저 GenStudio 시스템 관리자가 OpenAI Ads 계정을 GenStudio for Performance Marketing에 연결해야 합니다.

1. OpenAI 광고 관리자에서 **[!UICONTROL 설정]** > **[!UICONTROL API 키]** > **[!UICONTROL 새 키 만들기]**&#x200B;로 이동합니다.
1. GenStudio for Performance Marketing에서 **[!UICONTROL 자세히]** > **[!UICONTROL 설정]** > **[!UICONTROL ChatGPT]** > **[!UICONTROL 연결]** > **[!UICONTROL 계정 추가]**&#x200B;로 이동합니다.
1. OpenAI Ads 계정의 이름을 입력하고 API 키를 붙여 넣은 다음 **[!UICONTROL 계정 추가]**&#x200B;를 클릭합니다.

## ChatGPT 설정 필드

승인된 자산, 제목(제목) 및 본문 복사본이 잠겨 있으며 [!DNL Content]에서 이미 검토 및 승인을 받았으므로 활성화 중에 편집할 수 없습니다. 다음을 편집할 수 있습니다.

* **텍스트 필드**: 대상 URL, 추적 ID(플랫폼 광고 이름으로 사용됨)
* **플랫폼 설정 필드**: OpenAI 광고 계정, OpenAI 캠페인, OpenAI 광고 그룹

대상 URL은 올바른 `https://` 형식을 사용해야 합니다(예: `https://www.example.com`).
