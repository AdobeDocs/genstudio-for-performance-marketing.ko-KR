---
title: ChatGPT 광고 경험 만들기
description: Adobe GenStudio for Performance Marketing에서 ChatGPT 유료 미디어 경험을 만들고, 검토하고, 게시하고, 활성화하는 방법을 알아봅니다.
feature: Create Canvas, Create Prompt, Generative AI, Variant Generation, Content Generation
role: User
level: Beginner
source-git-commit: 17b2262615e10d82905ce7ebec65857e9a0b9f2a
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 8%
---

# ChatGPT 광고 경험 만들기

가이드라인 및 자산부터 생성, 브랜드 및 채널 확인, 승인, [!DNL Content]에 게시 및 Meta 및 Google Campaign Manager 360과 같은 채널에 사용되는 동일한 [!DNL Activate] 흐름에서의 활성화를 통해 [!DNL GenStudio for Performance Marketing]의 [[!DNL Create]](/help/user-guide/create/overview.md)을(를) 사용하여 **ChatGPT 광고**&#x200B;를 유료 미디어 경험으로 빌드합니다.

시작하기 전에 필요한 경우 [지침을 추가](/help/user-guide/guidelines/add-guidelines.md)하고 [유효 프롬프트](/help/user-guide/effective-prompts.md)를 검토하여 헤드라인 프롬프트가 강력한 변형을 생성하도록 합니다.

## 사전 요구 사항

[!DNL GenStudio for Performance Marketing]에서 ChatGPT 광고를 만들거나 활성화하기 전에 이러한 사전 요구 사항에 따라 설정해야 합니다.

### 액세스 및 역할

* [!DNL GenStudio for Performance Marketing]에 **Editor** 역할 이상이 있습니다. [사용자 역할 및 권한](/help/user-guide/user-roles.md)을 참조하세요.
* 해당 계정의 **OpenAI 광고 계정** 및 **API 키**&#x200B;가 있습니다.
* **ChatGPT Ads** 계정이 [!DNL GenStudio for Performance Marketing]에 연결되어 있습니다.

OpenAI Ads Manager에서 API 키를 만들려면:

1. OpenAI 광고 관리자에서 **[!UICONTROL 설정]** > **[!UICONTROL API 키]** > **[!UICONTROL 새 키 만들기]**&#x200B;로 이동합니다.

[!DNL GenStudio for Performance Marketing]에서 ChatGPT 광고 계정을 연결하려면:

1. 왼쪽 아래 영역에서 **[!UICONTROL 자세히]** > **[!UICONTROL 설정]** > **[!UICONTROL ChatGPT]** > **[!UICONTROL 연결]** > **[!UICONTROL 계정 추가]**&#x200B;를 클릭합니다.
1. OpenAI 광고 계정의 이름을 입력하고 API 키를 붙여 넣은 다음 **[!UICONTROL 계정 추가]**&#x200B;를 클릭합니다.

흐름이 성공적으로 완료되면 광고 계정이 연결됩니다.

### 구성 만들기

* **[!DNL Brands]**, **[!DNL Products]** 및 **[!DNL Personas]**&#x200B;이(가) 구성되어 앱에서 브랜드 내 복사본을 생성할 수 있습니다. [지침 개요](/help/user-guide/guidelines/overview.md)를 참조하세요.
* 사용할 이미지는 [[!DNL Content]](/help/user-guide/content/overview.md)에서 사용할 수 있습니다.

## ChatGPT 광고 생성

[!DNL Create] 작업 영역에서 유료 미디어 경험으로 ChatGPT 광고를 만듭니다.

### ChatGPT 경험 시작

ChatGPT 작성을 열려면:

1. **[!UICONTROL 만들기]** > **[!UICONTROL ChatGPT]**(으)로 이동합니다. ChatGPT에 대한 템플릿은 선택하지 않습니다. 단일 광고 레이아웃이 사용됩니다.
   ![만들기 워크플로의 ChatGPT 타일](./create-chatgpt-clp.png){width="60%"}
1. _Canvas_&#x200B;에서 **[!DNL Brand]**, **[!DNL Product]**, **[!DNL Persona]** 및 **언어**&#x200B;를 선택합니다.
1. [!DNL Content]에서 이미지를 선택하십시오.
1. ChatGPT 헤드라인 카피에 대한 프롬프트를 입력합니다.
1. **[!UICONTROL 생성]**&#x200B;을 클릭합니다.

[!DNL GenStudio for Performance Marketing] **4개의** Creative 변형을 생성합니다.

다음과 같은 작업을 수행할 수 있습니다.

* 음색, 길이 또는 강조를 조정하려면 **[!UICONTROL 다시 생성]** 또는 **[!UICONTROL 세분화]**&#x200B;을 사용하세요.
* _캔버스_&#x200B;에서 직접 텍스트를 편집합니다.
* **[!UICONTROL 교체]**&#x200B;를 사용하여 [!DNL Content]에서 대체 이미지를 선택하십시오.

생성된 경험을 편집하는 자세한 방법은 [변형 관리](/help/user-guide/create/manage-variants.md)를 참조하십시오.

### 브랜드 및 채널 확인 실행

검토를 위해 경험을 저장하거나 보내기 전에 브랜드 및 채널 규칙에 따라 복사 및 레이아웃의 유효성을 검사하십시오.

컨텐츠 검사를 실행하려면

1. **[!UICONTROL 콘텐츠 확인]**(브랜드 및 채널 확인)을 클릭합니다.
1. [_콘텐츠 확인_ 패널](/help/user-guide/guidelines/brand-validation.md#content-check-panel)에서 유효성 검사 결과를 검토합니다.
1. 필요에 따라 변형을 편집하거나 다시 생성하여 플래그가 지정된 문제(예: 복사 길이 또는 덴스 화면 텍스트)를 해결합니다.

[브랜드 유효성 검사](/help/user-guide/guidelines/brand-validation.md)를 참조하십시오.

## [!DNL GenStudio for Performance Marketing]에 ChatGPT 광고 저장

저장하면 ChatGPT 광고 경험이 [!DNL Content]&#x200B;(으)로 이동되므로 검토, 재사용 및 활성화할 수 있습니다.

두 가지 상태가 있습니다.

* **초안 경험**: 작업이 진행 중이며 승인되지 않았습니다.
* **게시된 경험**: 승인되었으며 활성화를 위해 [!DNL Content]에서 사용할 수 있습니다.

### 검토용으로 전송

1. 경험 헤더에서 **[!UICONTROL 검토 요청]**&#x200B;을 클릭합니다.
1. 승인자(예: 브랜드, 법률 또는 성과 관련자)를 선택합니다.
1. 선택 사항: **[!UICONTROL 설정]**&#x200B;에 메모를 추가합니다.
1. **[!UICONTROL 검토용으로 보내기]**&#x200B;를 클릭합니다.

승인자는 ChatGPT 경험, 브랜드 및 채널 확인 결과를 보고 **[!UICONTROL 승인]**&#x200B;하거나 변경을 요청할 수 있습니다.

[검토 및 승인 요청](/help/user-guide/approvals/request-review.md) 및 [검토 및 승인](/help/user-guide/approvals/overview.md)을 참조하세요.

### 콘텐츠에 게시

필요한 모든 승인이 완료되면 [!DNL Content]에 게시하십시오.

1. **[!UICONTROL 콘텐츠에 게시]**&#x200B;를 클릭합니다.
1. 캠페인 또는 활성화 이름, 지역, 언어, 페르소나, funnel 단계 및 **채널: ChatGPT**&#x200B;과 같은 메타데이터를 확인합니다.
1. **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

ChatGPT 광고가 [!DNL Content]에 나타나며, 채널 또는 캠페인과 같은 필터로 검색할 수 있고 [!DNL Activate]에서 선택할 준비가 되었습니다.

[승인된 콘텐츠 게시](/help/user-guide/approvals/publish-content.md) 및 [[!DNL Content] 개요](/help/user-guide/content/overview.md)를 참조하십시오.

## ChatGPT 광고 활성화

ChatGPT 활성화는 다른 유료 채널과 동일한 [[!DNL Activate]](/help/user-guide/activation/overview.md) 모듈을 사용합니다. 필수 구성 요소 및 ChatGPT 관련 설정 필드는 [ChatGPT 광고 활성화](/help/user-guide/activation/activate-chatgpt-ad.md)를 참조하십시오.
