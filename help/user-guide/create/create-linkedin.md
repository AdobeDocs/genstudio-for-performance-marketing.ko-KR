---
title: LinkedIn 경험 만들기
description: Adobe GenStudio for Performance Marketing을 사용하여 브랜드 호환 LinkedIn 경험을 만드는 방법을 알아봅니다.
feature: Create Canvas, Create Prompt, Generative AI, Variant Generation, Content Generation
role: User
level: Beginner
badgeBeta: label="Beta" tooltip="이 기능은 현재 Beta에 있으므로 일부 기능이 제한되거나 변경될 수 있습니다."
recommendations: noDisplay
exl-id: abe10fc8-d6d5-4cad-9273-400b622f22b7
source-git-commit: d12e00ba0d97e6795e7a416b77b120016bddf4e9
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# LinkedIn 경험 만들기

이 튜토리얼에서는 GenStudio for Performance Marketing [[!DNL Create]](/help/user-guide/create/overview.md)(왼쪽 탐색 영역에 있는 페인트 브러시 아이콘)을 사용하여 브랜드 지침을 준수하는 [LinkedIn 경험](/help/user-guide/create/meta-experiences.md)을 생성하는 방법을 보여 줍니다.

LinkedIn 광고 생성을 시작하기 전에 GenStudio for Performance Marketing에서 [지침을 추가](/help/user-guide/guidelines/add-guidelines.md)하고 [프롬프트 만들기](/help/user-guide/effective-prompts.md)의 기본 사항을 알아보는 것이 중요합니다.

## 템플릿 선택

새 LinkedIn 경험을 생성하려면 콘텐츠에 대한 프레임워크를 제공하는 템플릿이 필요합니다. 지원되는 LinkedIn 종횡비에 대한 자세한 내용은 [LinkedIn 템플릿 지침](/help/user-guide/templates/linkedin-template.md)을 참조하십시오.

**LinkedIn 템플릿을 선택하려면**:

1. _[!DNL Create]_에서&#x200B;**[!UICONTROL LinkedIn]**을(를) 클릭합니다.
1. _필터_ 옆의 검색 옵션을 사용하여 특정 템플릿을 찾습니다.
1. 템플릿을 선택하려면 클릭하고 **[!UICONTROL 사용]**&#x200B;을 클릭합니다.

   이 작업을 수행하면 콘텐츠 작성의 중앙 허브인 캔버스가 열립니다.

## 매개 변수 추가

프롬프트 창에 [지침](/help/user-guide/guidelines/overview.md) 및 _매개 변수_&#x200B;의 자산을 추가하면 콘텐츠 생성 프로세스가 향상되며 LinkedIn 경험 생성을 준비하는 데 중요한 단계입니다.

**매개 변수 및 자산을 추가하려면**:

1. 프롬프트 창을 확장하려면 _매개 변수_ 아이콘을 클릭하십시오.
1. _매개 변수_ 섹션에서 콘텐츠 생성을 알리는 지침—[!DNL Brands], [!DNL Personas] 및 [!DNL Products]을(를) 선택하십시오.

   ![사용자 선택](/help/assets/persona-select.png){width="600" zoomable="yes"}

   이 메뉴에서 사용할 수 있는 브랜드, 가상 사용자 또는 제품이 없는 경우 [GenStudio for Performance Marketing에 지침을 추가](/help/user-guide/guidelines/add-guidelines.md)하십시오.

1. 콘텐츠 생성에 영향을 미치려면 *및* 경험에서 사용할 콘텐츠를 추가하십시오.
   * [!DNL Content] 리포지토리에서 자산(이미지)을 선택하고, 필터링하고, 하나 이상의 이미지를 선택하려면 **[!UICONTROL 콘텐츠에서 선택]**&#x200B;을 클릭하십시오.

     ![시각적 콘텐츠 선택](/help/assets/content-select-meta.png){width="500" zoomable="yes"}

     연결된 [!DNL AEM Assets Content Hub] 저장소의 자산을 사용하려면 _위치_ 드롭다운 메뉴에서 저장소를 선택하십시오. 하나 이상의 이미지를 필터링하고 선택합니다.

   * 또는 자산을 **[!UICONTROL 콘텐츠에서 선택]** 섹션으로 끌어다 놓아 하나 이상의 새 자산을 업로드하십시오.
1. **[!UICONTROL 사용]**&#x200B;을 클릭합니다.

매개 변수를 모두 추가했으면 _매개 변수_ 아이콘을 다시 클릭하여 프롬프트 창을 축소할 수 있습니다.

## 프롬프트 입력

지침을 선택한 후 자연어를 사용하여 새 LinkedIn 경험에 대한 콘텐츠를 생성하기 시작하는 프롬프트를 작성하십시오. 자세한 프롬프트는 좋은 품질과 유용한 출력을 받을 수 있도록 해줍니다.

프롬프트 작성에 대한 자세한 내용은 [유효한 프롬프트 작성](/help/user-guide/effective-prompts.md)을 참조하십시오.

**프롬프트를 입력하려면**:

1. _&quot;생성할 경험 설명&quot;_ 프롬프트 상자에 프롬프트를 입력하십시오.
1. **[!UICONTROL 생성]**&#x200B;을 클릭합니다.

기본적으로 네 가지 변형(모두 추가한 프롬프트, 지침 및 콘텐츠에 의해 유도됨)이 생성되어 캔버스에 표시됩니다.

생성된 콘텐츠는 점진적으로 로드됩니다. LinkedIn 경험의 각 섹션이 생성되면 캔버스에 표시됩니다. 변경 내용이 캔버스에 로드되는 방법을 알아보려면 [LinkedIn 경험](/help/user-guide/create/linkedin-experiences.md#progressive-loading)을 참조하세요.

## 생성된 LinkedIn 광고 수정

승인 또는 게시를 위해 변형을 [!DNL Content]에 보내기 전에 LinkedIn 광고를 편집하거나 생성된 광고 집합에서 변형을 삭제할 수 있습니다.

**생성된 변형을 수정하려면**:

* **LinkedIn 광고 초안 이름을 [편집](/help/user-guide/create/manage-variants.md#change-draft-name)**&#x200B;하려면 캔버스 상단의 _제목 없는 초안_ 제목을 클릭하고 새 제목을 입력하십시오.
* **LinkedIn 광고를 수동으로 편집하려면[](/help/user-guide/create/manage-variants.md#manually-edit-text)**&#x200B;하려면 제목 줄, 머리글 또는 본문 복사와 같은 광고 섹션을 클릭하고 필요에 따라 편집하십시오.
* **콜 투 액션을 변경하거나 선택하려면** call-to-action 단추를 클릭하고 사용 가능한 단추 텍스트 옵션에서 선택하십시오. _Link_&#x200B;에서 call-to-action 텍스트의 URL을 입력하십시오.
* **변형의 섹션을 [다시 생성하려면](/help/user-guide/create/manage-variants.md#re-generate-sections)**&#x200B;편집 가능한 텍스트 필드를 클릭하고 _[!UICONTROL 권장 편집]_ 옵션을 사용하거나 _[!UICONTROL 새 텍스트 생성_ 섹션]에 새 프롬프트를 입력하고 **[!UICONTROL 생성]**&#x200B;을 클릭하십시오.
* **이미지를 [자르기 또는 위치 변경](/help/user-guide/create/manage-variants.md#crop-assets)**&#x200B;하려면 이미지 위로 마우스를 가져간 후 표시되는 자르기 아이콘을 클릭하고 이미지 크기와 배치를 조정하십시오.
* **변형의 이미지에 대한 대체 텍스트를 [추가하려면](/help/user-guide/create/manage-variants.md#add-alt-text-for-images)** 이미지 에셋을 클릭하고 _대체 텍스트_ 옵션을 사용하여 이미지당 대체 텍스트를 수동으로 추가하거나 생성하십시오.
* **LinkedIn 광고를 [삭제하려면](/help/user-guide/create/manage-variants.md#delete-variant)** 변형에 대한 옵션 메뉴를 클릭하고 **[!UICONTROL 변형 삭제]**&#x200B;를 클릭합니다.

## 생성 피드백 제출

생성 출력의 품질에 대한 [피드백을 제출](/help/user-guide/create/manage-variants.md#generation-feedback)하려면 옵션 아이콘(세 점)을 클릭하고 **[!UICONTROL 양호한 출력]** 또는 **[!UICONTROL 저조한 출력]**&#x200B;을 선택하십시오.

## 컨텐츠 확인 정렬 확인

생성된 변형을 최적화하고 브랜드 ID, 플랫폼 지침 및 접근성 표준을 엄격하게 준수하도록 하려면 [_콘텐츠 확인_ 패널](/help/user-guide/guidelines/brand-validation.md#content-check-panel)의 기능을 활용하십시오. 이 패널에는 포괄적인 콘텐츠 검사 세부 정보가 표시되고 개선 영역이 조명됩니다.

**변형에 대해 콘텐츠 검사를 수행하려면**:

1. 오른쪽 작업 표시줄의 _콘텐츠 확인_ 패널 아이콘을 클릭하여 [_콘텐츠 확인_ 패널](/help/user-guide/guidelines/brand-validation.md#content-check-panel)을 엽니다. 개선이 필요한 섹션 및 지침을 확인하기 위해 *검토 필요* 및 *합격* 검사에 대한 요약을 봅니다.

   ![_콘텐츠 확인_ 패널](/help/assets/content-check-panel.png){height="400" zoomable="yes"}

1. [변형을 수동으로 수정](#revise-generated-variants)하여 수행된 콘텐츠 검사와 변형이 일치하는지 확인합니다.

[브랜드 유효성 검사](/help/user-guide/guidelines/brand-validation.md)를 참조하십시오.

## 검토 및 승인 받기

캔버스의 상단 메뉴 표시줄에 액세스할 수 있는 승인 패널을 사용하여 검토를 얻고 검토 설명을 추적하고 관련자로부터 승인을 받습니다.

**검토 및 승인을 얻으려면**:

1. [승인 요청을 시작](/help/user-guide/approvals/request-review.md)하여 [초안 메타 광고 경험에 대한 승인](/help/user-guide/approvals/approve-content.md)을 요청하세요.

   ![검토 및 승인을 위해 초안 보내기](/help/assets/send-approval-meta.png){width="450" zoomable="yes"}

1. 검토 프로세스 중에 [검토자를 제거하거나 추가](/help/user-guide/approvals/review-and-edit.md#manage-approvals)합니다.
1. [검토할 콘텐츠에 액세스](/help/user-guide/approvals/review-and-edit.md#access-content-for-review)하고 수정 요청을 봅니다.
1. 리뷰 댓글별로 초안을 편집하고 [메타 광고 경험을 게시합니다](#publish-and-export-experience).

자세한 내용은 [검토 및 승인](/help/user-guide/approvals/overview.md)을 참조하세요.

## 경험 게시 및 내보내기

생성된 LinkedIn 광고를 현재 및 나중에 사용할 수 있도록 하려면 [!UICONTROL 콘텐츠]에 게시하고 마케팅 캠페인에서 사용하도록 내보내십시오.

1. **새 환경을 게시하려면**&#x200B;상단 도구 모음 또는 승인 흐름 내에서 **[!UICONTROL 게시]**&#x200B;를 클릭하십시오.
1. **새 환경을 내보내기**&#x200B;하려면 상단 도구 모음에서 **[!UICONTROL 내보내기]**&#x200B;를 클릭하세요.
   1. JPG, PNG 또는 GIF 형식을 선택하고 **[!UICONTROL 내보내기]**&#x200B;를 클릭합니다.

자세한 내용은 [[!DNL Content]](/help/user-guide/content/overview.md#search-and-find-approved-content)을(를) 참조하십시오.
