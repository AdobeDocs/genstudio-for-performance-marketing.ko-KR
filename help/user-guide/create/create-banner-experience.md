---
title: 배너 경험 만들기
description: 성과 마케팅을 위해 Adobe [!DNL GenStudio] 에서 배너 경험을 만드는 방법을 알아봅니다.
feature: Create Canvas, Create Prompt, Generative AI, Variant Generation, Content Generation
badgeBeta: label="Beta" tooltip="이 기능은 현재 Beta에 있으므로 일부 기능이 제한되거나 변경될 수 있습니다."
role: User
level: Beginner
recommendations: noDisplay
exl-id: c5d541a9-a97b-44da-a15c-61aceefd0e8c
source-git-commit: 47195c08f500e50a01db127c6badc461c10afaf9
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---

# 배너 경험 만들기

이 자습서에서는 GenStudio for Performance Marketing [(왼쪽 탐색 영역에 있는 페인트 브러시 아이콘)을 사용하여 브랜드 ](banner-experiences.md)배너 경험[[!DNL Create]](/help/user-guide/create/overview.md)을 만드는 방법을 보여줍니다.

매력적인 배너 경험을 디자인하려면 시작하기 전에 [GenStudio for Performance Marketing에 지침을 추가](/help/user-guide/guidelines/add-guidelines.md)하고 [프롬프트 작성의 기본 사항](/help/user-guide/effective-prompts.md)을 검토하는 것이 좋습니다.

## 템플릿 선택

배너 경험을 만들려면 사용 가능한 템플릿을 사용하여 콘텐츠의 프레임워크를 제공하십시오. 지원되는 배너 차원에 대한 자세한 내용은 [템플릿 모범 사례](/help/user-guide/content/best-practices-for-templates.md#follow-channel-specific-template-guidelines)를 참조하세요.

**배너 템플릿을 선택하려면**:

1. _[!DNL Create]_에서&#x200B;**[!UICONTROL 배너]**를 클릭합니다.
1. _필터_ 옆의 검색 옵션을 사용하여 특정 배너 템플릿을 찾습니다.
1. _템플릿 선택_ 보기에서 배너 템플릿을 클릭합니다.
1. **[!UICONTROL 사용]**&#x200B;을 클릭합니다.

   콘텐츠 작성의 홈 베이스인 캔버스 가 표시됩니다.

## 매개 변수 추가

프롬프트 서랍에서 [지침](/help/user-guide/guidelines/overview.md) 및 자산을 _매개 변수_&#x200B;에 통합하면 콘텐츠 생성 프로세스가 향상되며 배너 경험을 만드는 중요한 준비 단계입니다.

**매개 변수 및 자산을 추가하려면**:

1. 프롬프트 창을 확장하려면 _매개 변수_ 아이콘을 클릭하십시오.
1. _매개 변수_ 섹션에서 콘텐츠 생성을 알리는 지침—[!DNL Brands], [!DNL Personas] 및 [!DNL Products]을(를) 선택하십시오.

   이 메뉴에서 사용할 수 있는 브랜드, 가상 사용자 또는 제품이 없는 경우 [GenStudio for Performance Marketing에 지침을 추가](/help/user-guide/guidelines/add-guidelines.md)하십시오.

1. *및* 경험에서 사용할 콘텐츠를 추가하여 콘텐츠 생성에 영향을 미치려면 다음을 수행하십시오.
   * **[!UICONTROL 리포지토리에서 자산(이미지)을 선택하고, 필터링하고, 하나 이상의 이미지를 선택하려면]**&#x200B;콘텐츠에서 선택[!DNL Content]을 클릭하십시오.

     연결된 [!DNL AEM Assets Content Hub] 저장소의 자산을 사용하려면 _위치_ 드롭다운 메뉴에서 저장소를 선택하십시오. 하나 이상의 이미지를 필터링하고 선택합니다.

   * 또는 자산을 **[!UICONTROL 콘텐츠에서 선택]** 섹션으로 끌어다 놓아 하나 이상의 새 자산을 업로드하십시오.
1. **[!UICONTROL 사용]**&#x200B;을 클릭합니다.

매개 변수를 모두 추가했으면 _매개 변수_ 아이콘을 다시 클릭하여 프롬프트 서랍을 축소합니다.

## 프롬프트 입력

지침을 선택한 후에는 자연어를 사용하여 새 배너 경험을 위한 콘텐츠 생성을 시작하라는 메시지를 표시하십시오. 고품질 결과를 보장하려면 세부적이고 설명적인 프롬프트를 작성하는 것이 중요합니다.

![프롬프트 입력](/help/assets/prompt-displayad.png){width="650" zoomable="yes"}

프롬프트 작성에 대한 자세한 내용은 [유효한 프롬프트 작성](/help/user-guide/effective-prompts.md)을 참조하십시오.

**프롬프트를 입력하려면**:

1. _&quot;생성할 경험 설명&quot;_ 프롬프트 상자에 프롬프트를 입력하십시오.
1. **[!UICONTROL 생성]**&#x200B;을 클릭합니다.

기본적으로 프롬프트, 지침 및 추가한 컨텐츠에 의해 유발되는 네 가지 변형이 생성되어 캔버스에 표시됩니다.

## 생성된 배너 수정

[!DNL Content]에 게시하거나 승인을 위해 보낼 항목을 선택하기 전에 배너 섹션 및 텍스트 필드를 편집하거나 생성된 변형을 삭제할 수 있습니다.

**생성된 변형을 수정하려면**:

* **배너 초안 이름을 [편집](/help/user-guide/create/manage-variants.md#change-draft-name)**&#x200B;하려면 캔버스 상단의 _제목 없는 초안_ 제목을 클릭하고 새 제목을 입력하십시오.
* **배너를 [수동으로 편집](/help/user-guide/create/manage-variants.md#manually-edit-text)**&#x200B;하려면 배너 섹션이나 필드(예: 헤드라인이나 CTA)를 두 번 클릭하고 필요에 따라 편집하십시오.
* **변형에서 [텍스트 서식을 적용하려면](/help/user-guide/create/manage-variants.md#manually-edit-text)** 변형에 대한 온라인 이미지 텍스트나 인라인 링크를 클릭한 다음 **[!UICONTROL 텍스트 서식 지정]**&#x200B;을 클릭하십시오.
* **변형의 섹션을 [다시 생성하려면](/help/user-guide/create/manage-variants.md#re-generate-sections)**&#x200B;편집 가능한 텍스트 필드를 클릭하고 _[!UICONTROL 권장 편집]_ 옵션을 사용하거나 _[!UICONTROL 새 텍스트 생성_ 섹션]에 새 프롬프트를 입력하고 **[!UICONTROL 생성]**&#x200B;을 클릭하십시오.
* **변형에서 이미지를 [추가하거나 교체](/help/user-guide/create/manage-variants.md#swap-image)**&#x200B;하려면 이미지 에셋(또는 현재 이미지가 없는 경우 이미지 에셋 영역)을 클릭하고 **[!UICONTROL 콘텐츠에서 교체]** 아이콘을 클릭하십시오.
* **변형의 이미지에 링크를 추가하려면[이미지 자산(또는 이미지가 현재 없는 경우 이미지 자산 영역)을 클릭하고 링크 아이콘을 클릭합니다.](/help/user-guide/create/manage-variants.md#add-image-link)**
* **변형의 이미지에 대한 대체 텍스트를 [추가하려면](/help/user-guide/create/manage-variants.md#add-alt-text-for-images)** 이미지 에셋을 클릭하고 _대체 텍스트_ 옵션을 사용하여 이미지당 대체 텍스트를 수동으로 추가하거나 생성하십시오.
* **변형에 [접근성 레이블을 추가](/help/user-guide/create/manage-variants.md#add-accessibility-labels)하려면** 이미지 또는 call-to-action 링크를 클릭한 다음, 링크 또는 단추의 기능에 대해 설명하는 간단한 설명을 제공하십시오.
* **광고 크기 및 종횡비를 [변경하려면](/help/user-guide/create/manage-variants.md#change-aspect-ratio)**_[!UICONTROL 크기 조정]_ 단추(캔버스 왼쪽에 단추 아이콘이 있는 상자)를 클릭하고 모든 변형에 적용할 새 크기 및 종횡비를 선택하십시오. 변형은 복제되고 크기가 조정됩니다.
* **이미지를 [자르기 또는 위치 변경](/help/user-guide/create/manage-variants.md#crop-assets)**&#x200B;하려면 이미지를 클릭하고 **[!UICONTROL 편집]**(연필 아이콘)을 클릭한 다음 **[!UICONTROL 자르기]**&#x200B;를 클릭합니다. 이미지 크기와 배치를 조정합니다.
* **[이미지 크기를 조정하고 맞추는 [생성 확장]을 사용](/help/user-guide/create/manage-variants.md#use-generative-expand)하려면** 이미지를 클릭하고 **[!UICONTROL 편집]**(연필 모양 아이콘)을 클릭한 다음 **[!UICONTROL 확장]**&#x200B;을 클릭합니다. 필요한 종횡비와 템플릿에 맞게 이미지를 조정합니다.

<!-- # Preview for device
When revising and preparing email experiences, you can toggle between previews for desktop and mobile views to ensure coherence and visual appeal of draft variants.
**To preview variants for desktop and mobile devices** toggle the device preview option—between **desktop** and **mobile**—in the right menu bar (computer and phone icons) to preview how variants appear. -->

## 생성 피드백 제출

생성 출력의 품질에 대한 [피드백을 제출](/help/user-guide/create/manage-variants.md#generation-feedback)하려면 옵션 아이콘(세 점)을 클릭하고 **[!UICONTROL 양호한 출력]** 또는 **[!UICONTROL 저조한 출력]**&#x200B;을 선택하십시오.

## 컨텐츠 확인 정렬 확인

생성된 변형을 최적화하고 브랜드 ID, 플랫폼 지침 및 접근성 표준을 엄격하게 준수하도록 하려면 [_콘텐츠 확인_ 패널](/help/user-guide/guidelines/brand-validation.md#content-check-panel)의 기능을 활용하십시오. 이 패널에는 포괄적인 콘텐츠 검사 세부 정보가 표시되고 개선 영역이 조명됩니다.

**변형에 대해 콘텐츠 검사를 수행하려면**:

1. 오른쪽 작업 표시줄의 _콘텐츠 확인_ 패널 아이콘을 클릭하여 [_콘텐츠 확인_ 패널](/help/user-guide/guidelines/brand-validation.md#content-check-panel)을 엽니다. 개선이 필요한 섹션 및 지침을 확인하기 위해 _검토 필요_ 및 _합격_ 검사에 대한 요약을 봅니다.

   ![_콘텐츠 확인_ 패널](/help/assets/content-check-panel.png){height="400" zoomable="yes"}

1. [변형을 수동으로 수정](#revise-generated-banners)하여 수행된 콘텐츠 검사와 변형이 일치하는지 확인합니다.

[브랜드 유효성 검사](/help/user-guide/guidelines/brand-validation.md)를 참조하십시오.

## 검토 및 승인 받기

캔버스의 오른쪽 작업 표시줄에 아이콘으로 액세스할 수 있는 _승인_ 패널을 사용하여 검토를 받고, 검토 의견을 추적하고, 관련자로부터 승인을 받습니다.

**검토 및 승인을 얻으려면**:

1. [승인 요청을 시작](/help/user-guide/approvals/request-review.md)하여 [초안 배너 경험의 승인](/help/user-guide/approvals/approve-content.md)을 요청하세요.
1. 검토 프로세스 중에 [검토자를 제거하거나 추가](/help/user-guide/approvals/review-and-edit.md#manage-approvals)합니다.
1. [검토할 콘텐츠에 액세스](/help/user-guide/approvals/review-and-edit.md#access-content-for-review)하고 수정 요청을 봅니다.
1. 리뷰 댓글별로 초안을 편집하고 [배너 경험을 게시합니다](#publish-and-export-experience).

[검토 및 승인](/help/user-guide/approvals/overview.md)을 참조하세요.

## 경험 게시 및 내보내기

생성된 배너를 현재 및 나중에 사용할 수 있도록 하려면 [!UICONTROL 콘텐츠]에 게시하고 마케팅 캠페인에서 사용하도록 내보내십시오.

1. **새 배너 환경을 게시하려면**, 상단 도구 모음 또는 승인 흐름 내에서 **[!UICONTROL 게시]**&#x200B;를 클릭하십시오.
   1. _[!UICONTROL [!DNL Campaigns]]_을(를) 선택하고 필요한 경우_[!UICONTROL &#x200B;추가 세부 정보&#x200B;]_를 추가하십시오.
   1. **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

      ![배너 게시](/help/assets/publish-displayad.png){width="450" zoomable="yes"}

1. **새 배너를 내보내려면** 상단 도구 모음에서 **[!UICONTROL 내보내기]**&#x200B;를 클릭합니다.
   1. HTML 및 이미지, PNG 또는 JPG 형식을 선택하고 **[!UICONTROL 내보내기]**&#x200B;를 클릭합니다.

      내보낸 HTML은 템플릿 또는 `div` 컨테이너와 같은 미리 정의된 웹 속성 내에 배치해야 합니다. 이렇게 설정된 치수가 없으면 독립적으로 볼 때 이미지가 왜곡되어 표시될 수 있습니다.

[[!DNL Content]](/help/user-guide/content/overview.md#search-and-find-approved-content)을(를) 참조하십시오.
