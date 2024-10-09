---
title: 이메일 경험 만들기
description: 성능 마케팅을 위해 Adobe GenStudio에서 이메일 경험을 만드는 방법을 알아봅니다.
feature: Content, Brands Service, Guidelines, Content Generation, Create, Experiences, Variant Generation
role: User
level: Beginner
type: Tutorial
recommendations: noDisplay
exl-id: 34446202-da98-45ff-869a-b43496a477f8
source-git-commit: 30cd73ba1beb582ea4ac73eca7e17715f9aafc66
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 0%

---

# 이메일 경험 만들기

이 튜토리얼에서는 GenStudio for Performance Marketing [[!DNL Create]](/help/user-guide/create/overview.md)(왼쪽 탐색 영역에 있는 페인트 브러시 아이콘)을 사용하여 브랜드 [이메일 경험](/help/user-guide/create/email-experiences.md)을(를) 생성하는 방법을 보여 줍니다.

효과적인 이메일 경험을 만들려면 시작하기 전에 [성능 마케팅을 위해 GenStudio에 지침을 추가](/help/user-guide/guidelines/add-guidelines.md)하고 [프롬프트 작성의 기본 사항](/help/user-guide/effective-prompts.md)을 살펴보는 것이 좋습니다.

## 템플릿 선택

새 이메일 경험을 만들려면 사용 가능한 템플릿을 사용하여 콘텐츠의 프레임워크를 제공하십시오.

**전자 메일 서식 파일을 선택하려면**:

1. _[!DNL Create]_에서_&#x200B;의 **[!UICONTROL 전자 메일]**&#x200B;을(를) 클릭합니다._섹션.
1. 특정 전자 메일 서식 파일을 찾으려면 _필터_ 옆의 검색 옵션을 사용하십시오.
1. 전자 메일 서식 파일을 클릭하여 선택하고 **[!UICONTROL 사용]**&#x200B;을 클릭합니다.

   콘텐츠 생성의 중심인 캔버스(Canvas)가 나타납니다.

## 매개 변수 추가

프롬프트 영역에서 [지침](/help/user-guide/guidelines/overview.md) 및 _매개 변수_&#x200B;의 자산을 추가하면 콘텐츠 생성 프로세스가 대체되며 이메일 경험을 생성하기 위한 필수 준비 단계입니다.

**매개 변수 및 자산을 추가하려면**:

1. _매개 변수_ 아이콘을 클릭하여 프롬프트 영역을 확장합니다.
1. _매개 변수_ 섹션에서 콘텐츠 생성을 알리는 지침—[!DNL Brands], [!DNL Personas] 및 [!DNL Products]을(를) 선택하십시오.

   이 메뉴에서 사용할 수 있는 브랜드, 가상 사용자 또는 제품이 없는 경우 [성능 마케팅을 위해 GenStudio에 지침을 추가](/help/user-guide/guidelines/add-guidelines.md)하십시오.

1. 콘텐츠 생성에 영향을 미치려면 **[!UICONTROL 콘텐츠 선택]**&#x200B;을 클릭하여 *및* 경험에 사용할 콘텐츠를 추가합니다.
   * [!DNL Content] 저장소에서 자산(이미지)을 선택하려면 **[!UICONTROL 콘텐츠에서 선택]**&#x200B;을 클릭합니다. 하나 이상의 이미지를 필터링하고 선택합니다.

     연결된 [!DNL AEM Assets Content Hub] 저장소의 자산을 사용하려면 _위치_ 드롭다운 메뉴에서 저장소를 선택하십시오. 하나 이상의 이미지를 필터링하고 선택합니다.

   * 하나 이상의 새 자산을 업로드하려면 **[!UICONTROL 업로드]**&#x200B;를 클릭하고 파일을 찾은 다음 사용할 자산을 선택하십시오. 장치 탐색과 함께 Microsoft OneDrive 또는 Dropbox에서 가져올 수 있습니다. 을(를) 클릭하여 원하는 이미지를 선택합니다.
   * 자산을 _콘텐츠_ 섹션으로 끌어다 놓습니다.
1. **[!UICONTROL 사용]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>전자 메일 템플릿에 여러 개의 섹션이 있는 경우 _여러 섹션 전자 메일_&#x200B;의 각 전자 메일 섹션에 대해 [!DNL Products] 및 콘텐츠(시각적 자산)를 선택하십시오. 여러 섹션 이메일은 섹션당 하나의 시각적 자산을 지원합니다.

매개 변수를 모두 추가했으면 _매개 변수_ 아이콘을 다시 클릭하여 프롬프트 영역을 축소할 수 있습니다.

## 프롬프트 입력

지침을 선택한 후 자연어를 사용하여 프롬프트를 만들고 새 이메일 경험을 위한 콘텐츠를 생성합니다. 세부 프롬프트는 모호하거나 설명하지 않는 프롬프트에 비해 높은 품질의 출력을 제공합니다.

프롬프트 작성에 대한 자세한 내용은 [유효한 프롬프트 작성](/help/user-guide/effective-prompts.md)을 참조하십시오.

**프롬프트를 입력하려면**:

1. _&quot;생성할 경험 설명&quot;_ 프롬프트 상자에 프롬프트를 입력하십시오.
1. **[!UICONTROL 생성]**&#x200B;을 클릭합니다.

기본적으로 네 가지 변형(모두 추가한 프롬프트, 지침 및 콘텐츠에 의해 유도됨)이 생성되어 캔버스에 표시됩니다.

생성된 콘텐츠는 점진적으로 로드됩니다. 이메일 경험의 각 섹션이 생성되면 캔버스에 표시됩니다. 변경 내용이 캔버스에 로드되는 방법을 알아보려면 [전자 메일 환경](/help/user-guide/create/meta-experiences.md#progressive-loading)을 참조하세요.

## 생성된 이메일 수정

[!DNL Content]에 게시하거나 승인을 위해 보낼 항목을 선택하기 전에 전자 메일 섹션을 편집하거나 생성된 전자 메일 집합에서 변형을 삭제할 수 있습니다.

**생성된 변형을 수정하려면**:

* **전자 메일 초안 이름을 [편집](/help/user-guide/create/manage-variants.md#change-draft-name)**&#x200B;하려면 캔버스 상단의 _제목 없는 초안_ 제목을 클릭하고 새 제목을 입력하십시오.
* **전자 메일을 수동으로 편집하려면](/help/user-guide/create/manage-variants.md#manually-edit-text)**, 편집 가능한 텍스트 필드(제목 줄, 머리글 또는 본문 복사본 등)를 두 번 클릭하고 필요에 따라 편집합니다[
<!-- * **To [regenerate a section of a variant](/help/user-guide/create/manage-variants.md#re-generate-sections)**, click an editable text field and use the _[!UICONTROL Suggested edits]_ options or enter a new prompt and click **[!UICONTROL Generate]**. -->
* **변형에 이미지를 추가하거나 교체](/help/user-guide/create/manage-variants.md#swap-image)**&#x200B;하려면 이미지 에셋(또는 현재 이미지가 없는 경우 이미지 에셋 영역)을 클릭하고 **[!UICONTROL 콘텐츠에서 선택/교체]** 또는 **[!UICONTROL 새 이미지 업로드]**&#x200B;를 클릭하여 개별 변형에서 이미지를 추가하거나 교체하십시오.[
* **전자 메일을 [삭제](/help/user-guide/create/manage-variants.md#delete-variant)**&#x200B;하려면 전자 메일 제목(예: &quot;전자 메일 1/4&quot;)을 클릭하여 선택하고 **[!UICONTROL 변형 삭제]**&#x200B;를 클릭합니다.

## 생성 피드백 제출

생성 출력의 품질에 대한 [피드백을 제출](/help/user-guide/create/manage-variants.md#generation-feedback)하려면 옵션 아이콘(세 점)을 클릭하고 **[!UICONTROL 양호한 출력]** 또는 **[!UICONTROL 저조한 출력]**&#x200B;을 선택하십시오.

## 장치 미리 보기

이메일 경험을 수정하고 준비할 때, 데스크톱 보기와 모바일 보기 간에 [전환](/help/user-guide/create/manage-variants.md#preview-for-device)하여 초안 변형의 일관성과 시각적 효과를 확인할 수 있습니다.

## 브랜드 정렬 확인

생성된 이메일을 최적화하고 브랜드 정체성을 엄격히 준수하려면 [_브랜드 지침 검사_](/help/user-guide/guidelines/brand-validation.md#brand-guidelines-check)&#x200B;의 기능(변형에 대한 브랜드 정렬 요약 제공)과 [_브랜드 유효성 검사_ 패널](/help/user-guide/guidelines/brand-validation.md#brand-validation-panel)을 활용하여 포괄적인 브랜드 유효성 검사 세부 정보를 표시하고 개선 영역을 강조하십시오.

**브랜드 정렬을 확인하려면**:

1. 변형에 대한 [**[!UICONTROL [!DNL Brand] 지침 확인]**](/help/user-guide/guidelines/brand-validation.md#brand-guidelines-check) 아이콘을 클릭하고 브랜드에 대해 확인할 때 해당 변형이 수행되는 방식에 대한 요약을 확인합니다.
1. 개선이 필요한 섹션 및 지침에 대한 세부 정보를 보려면 **[!UICONTROL 검토]** _또는_&#x200B;를 클릭하고 상단 메뉴 막대에서 브랜드 유효성 검사 아이콘을 클릭하여 [_브랜드 유효성 검사 패널_](/help/user-guide/guidelines/brand-validation.md#brand-validation-panel)&#x200B;을 엽니다.

1. 각 이메일을 전환하여 생성된 콘텐츠를 보다 브랜드 맞춤형으로 개선하는 방법을 살펴보십시오.
1. [전자 메일을 수동으로 수정](#revise-generated-emails)하여 전자 메일이 브랜드와 긴밀하게 정렬되도록 합니다.

[브랜드 유효성 검사](/help/user-guide/guidelines/brand-validation.md)를 참조하십시오.

## 검토 및 승인 받기

캔버스의 상단 메뉴 표시줄에 액세스할 수 있는 승인 패널을 사용하여 검토를 얻고 검토 설명을 추적하고 관련자로부터 승인을 받습니다.

**검토 및 승인을 얻으려면**:

1. [승인 요청을 시작](/help/user-guide/approvals/request-review.md)하여 [초안 전자 메일 경험의 승인](/help/user-guide/approvals/approve-content.md)을 요청하세요.
1. 검토 프로세스 중에 [검토자를 제거하거나 추가](/help/user-guide/approvals/review-and-edit.md#manage-approvals)합니다.
1. [검토할 콘텐츠에 액세스](/help/user-guide/approvals/review-and-edit.md#access-content-for-review)하고 수정 요청을 봅니다.
1. 리뷰 댓글별로 초안을 편집하고 [전자 메일 환경을 게시합니다](#publish-and-export-experience).

자세한 내용은 [검토 및 승인](/help/user-guide/approvals/overview.md)을 참조하세요.

## Publish 및 내보내기 경험

생성된 이메일을 현재 및 향후에 사용할 수 있도록 하려면 [!UICONTROL 콘텐츠]에 게시하고 마케팅 캠페인에서 사용하도록 내보내십시오.

1. **새 전자 메일 환경을 게시하려면**&#x200B;맨 위 도구 모음에서 **[!UICONTROL Publish]**&#x200B;을 클릭하세요.
1. **새 전자 메일 환경을 내보내려면**&#x200B;맨 위 도구 모음에서 **[!UICONTROL 내보내기]**&#x200B;를 클릭하세요.
   1. CSV 및 이미지 또는 HTML 전용 형식을 선택하고 **[!UICONTROL 내보내기]**&#x200B;를 클릭합니다.

자세한 내용은 [[!DNL Content]](/help/user-guide/content/overview.md#search-and-find-approved-content)을(를) 참조하십시오.
