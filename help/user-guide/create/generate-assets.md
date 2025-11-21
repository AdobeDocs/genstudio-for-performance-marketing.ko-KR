---
title: 이미지 생성
description: 성능 마케팅을 위해 Adobe [!DNL GenStudio] 에서 참조 이미지의 스타일과 일치하는 이미지를 만듭니다.
feature: Create Canvas, Create Prompt, Generative AI, Variant Generation, Content Generation
badgeBeta: label="Beta" tooltip="이 기능은 현재 Beta에 있으므로 일부 기능이 제한되거나 변경될 수 있습니다."
role: User
level: Beginner
recommendations: noDisplay
exl-id: c1118ada-7fee-43cd-aff4-eab69539afb4
source-git-commit: 3251d81a6bfb0c1f7d2bf3c5bd319ad4e2237699
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# 이미지 생성

GenStudio for Performance Marketing [[!DNL Create]](/help/user-guide/create/overview.md)(페인트 브러쉬 아이콘)을 사용하면 선택한 이미지에서 영감을 얻어 시각적 효과와 전반적인 미적 효과를 캡처하는 _[!DNL On-brand images]_&#x200B;을(를) 생성할 수 있습니다.<!-- [two types of images](#image-types) using GenStudio for Performance Marketing [[!DNL Create]](/help/user-guide/create/overview.md) (paintbrush icon)—_[!DNL On-brand images]_ and _[!DNL Similar images]_. -->

눈길을 끄는 효과적인 이미지를 디자인하려면 [GenStudio for Performance Marketing에 지침을 추가](/help/user-guide/guidelines/add-guidelines.md)하고 [프롬프트 작성의 기본 사항](/help/user-guide/effective-prompts.md)을 검토하는 것이 좋습니다.

## 이미지 유형

_[!DNL On-brand images]_&#x200B;은(는) 선택한 이미지에서 영감을 얻어 생성되는 에셋으로 시각적 효과와 전반적인 미적 효과를 캡처합니다. 이러한 이미지는 [!DNL Content]에서 이미 사용할 수 있는 이미지와 디자인을 안내하는 정교하게 만들어진 프롬프트를 사용하여 만들어집니다. 생성 프로세스 중에 선택한 브랜드 지침과 매개 변수를 모두 엄격히 따릅니다.

_[!DNL On-brand images]_<!-- and _[!DNL Similar images]_ -->은(는) 집합 지침, 매개 변수 및 [신중하게 만들어진 프롬프트](/help/user-guide/effective-prompts.md)를 통합하여 눈길을 끄는 이미지 에셋을 제공합니다.

<!-- * _[!DNL Similar images]_—Image assets created with strong similarity to an existing selected image available in [!DNL Content]. When generating similar images, GenStudio for Performance Marketing redesigns the selected image, giving slight variations on the content to provide variety and nuance. -->

## 브랜드 이미지 생성

정의된 지침, 매개 변수 및 선택한 참조 이미지를 사용하여 [!DNL On-brand images]을(를) 생성할 수 있습니다. 이러한 요소는 프롬프트와 함께 일관된 [!DNL On-brand image] 변형을 만드는 데 도움이 됩니다.

### 참조 이미지 선택

_[!DNL On-brand images]_&#x200B;을(를) 만들려면 [!DNL Content]에 저장된 기존 이미지를 선택하십시오. 지원되는 [&#x200B; 차원에 대한 자세한 내용은 &#x200B;](/help/user-guide/templates/best-practices-for-templates.md#follow-channel-specific-template-guidelines)템플릿 모범 사례[!DNL on-brand image]를 참조하세요.

**참조 이미지를 선택하려면**:

1. _[!DNL Create]_&#x200B;에서&#x200B;**[!UICONTROL 브랜드 이미지 사용]**&#x200B;을 클릭하세요.
1. _필터_ 옆의 검색 옵션을 사용하여 특정 이미지를 찾습니다.

   ![참조 이미지 선택](/help/assets/select-img.png){width="400" zoomable="yes"}

   연결된 [!DNL AEM Assets Content Hub] 리포지토리의 자산을 사용하려면 _위치_ 드롭다운 메뉴에서 리포지토리를 선택하십시오. 이미지 하나를 필터링하고 선택합니다.

1. _이미지 선택_ 보기에서 이미지를 클릭합니다.

   선택한 이미지의 크기는 최대 10mb입니다.

1. **[!UICONTROL 사용]**&#x200B;을 클릭합니다.

   콘텐츠 작성의 중앙 허브 역할을 하는 캔버스가 표시됩니다.

### 매개 변수 추가

[지침](/help/user-guide/guidelines/overview.md)과 매개 변수를 통합하면 콘텐츠 생성 프로세스가 향상되며 [!DNL on-brand image]을(를) 만드는 중요한 준비 단계입니다.

**지침 및 매개 변수를 추가하려면**:

1. _기본_ 탭에서 [!DNL Brand]을(를) 선택하여 콘텐츠 생성을 알립니다.

   이 메뉴에서 사용할 수 있는 브랜드가 없는 경우 [GenStudio for Performance Marketing에 지침을 추가](/help/user-guide/guidelines/add-guidelines.md)하십시오.

1. _[!UICONTROL 이미지 범주]_&#x200B;에서 원하는 결과에 가장 적합한 이미지 범주를 선택하십시오.

   [!DNL Brand]을(를) 선택한 경우 이미지 범주를 사용할 수 있습니다. 옵션은 선택한 [!DNL Brand]에 의해 결정됩니다.

<!-- 1. _(Optional)_ Select a custom model from _[!UICONTROL Model]_.

   Models are available if you access to [custom models in Firefly](https://adobedx.slack.com/archives/CMF1JGMLY/p1743534402774569). The _Models_ list will be blank if you do not have access. -->

1. _[!UICONTROL 종횡비]_&#x200B;에서 원하는 종횡비를 선택하십시오.
1. 참조 이미지를 추가하려면 **[!UICONTROL 스타일 참조]**&#x200B;에서 _[!UICONTROL 콘텐츠에서 선택]_&#x200B;을 클릭하세요. 선택한 이미지는 사용자가 생성하는 이미지의 시각적 심미성과 깊이에 영향을 줍니다.

   연결된 [!DNL AEM Assets Content Hub] 리포지토리의 자산을 사용하려면 _위치_ 드롭다운 메뉴에서 리포지토리를 선택하십시오. 이미지 하나를 필터링하고 선택합니다.

1. _고급_ 탭에서 _콘텐츠 형식_&#x200B;을(를) 선택합니다.

   선택한 [!DNL Brand]—_Art_ 또는 _사진_&#x200B;에 대한 이미지 범주에 따라 미리 선택되었으며 편집할 수 없습니다.

1. _[!UICONTROL 시각적 강도]_&#x200B;에서 이미지의 기존 시각적 특성의 전체 강도를 조정합니다.

### 프롬프트 입력

매개 변수를 선택한 후 자연어를 사용하여 브랜드 이미지를 생성하기 시작한다는 메시지를 작성하십시오.

[유효한 프롬프트 쓰기](/help/user-guide/effective-prompts.md)를 참조하십시오.

**프롬프트를 입력하려면**:

1. 프롬프트 상자에 프롬프트를 입력합니다.
1. **[!UICONTROL 생성]**&#x200B;을 클릭합니다.

기본적으로 프롬프트, 매개변수 및 추가한 컨텐트에 의해 연료화되는 네 가지 변형이 생성되어 캔버스에 표시됩니다.

### Adobe Express에서 편집

이미지 변형을 생성한 후 Adobe Express을 사용하여 Adobe GenStudio for Performance Marketing에서 직접 편집할 수 있습니다.

**Adobe Express을 사용하여 개별 이미지를 편집하려면**:

1. 생성된 이미지 변형 위로 마우스를 가져간 후 _[!UICONTROL Adobe Express에서 편집]_&#x200B;을 클릭합니다.

   _Powered by Adobe Express_ 창이 나타납니다.

1. [이미지 자르기](https://helpx.adobe.com/express/create-and-edit-images/edit-images/crop-images.html), [개체 제거](https://helpx.adobe.com/express/create-and-edit-images/create-and-modify-with-generative-ai/remove-objects-generative-fill.html), 효과 적용 등의 이미지 편집을 수행합니다.

   Adobe Express을 사용하여 GenStudio for Performance Marketing에서 이미지를 수정하는 방법에 대해 알아보려면 [Adobe Express 설명서](https://helpx.adobe.com/express/user-guide.html)를 참조하십시오.

1. _[!UICONTROL 변경 내용 적용]_&#x200B;을 클릭하여 편집 내용을 저장합니다.
1. 원하는 대로 개별 이미지 변형을 계속 편집하고 변경 사항을 적용하여 진행률을 저장합니다.

### 컨텐츠 확인 정렬 확인

생성된 변형을 최적화하고 브랜드 ID, 플랫폼 지침 및 접근성 표준을 엄격하게 준수하도록 하려면 [_콘텐츠 확인_ 패널](/help/user-guide/guidelines/brand-validation.md#content-check-panel)의 기능을 활용하십시오. 이 패널에는 포괄적인 콘텐츠 검사 세부 정보가 표시되고 개선 영역이 조명됩니다.

**콘텐츠 검사를 수행하려면**:

1. 오른쪽 작업 표시줄의 _콘텐츠 확인_ 패널 아이콘을 클릭하여 [_콘텐츠 확인_ 패널](/help/user-guide/guidelines/brand-validation.md#content-check-panel)을 엽니다. 개선이 필요한 섹션 및 지침을 확인하기 위해 *검토 필요* 및 *합격* 검사에 대한 요약을 봅니다.

   ![_콘텐츠 확인_ 패널](/help/assets/content-check-img.png){width="500" zoomable="yes"}

1. 이미지 변형을 수정하여 변형이 수행된 콘텐츠 확인과 밀접하게 정렬되도록 합니다.

[브랜드 유효성 검사](/help/user-guide/guidelines/brand-validation.md)를 참조하십시오.

<!-- ## Generate Similar images

You can quickly generate images similar to a selected image within [!DNL Content] from the [!DNL Create] home.

**To create _[!DNL Similar images]_**:

1. In _[!DNL Create]_, click **[!UICONTROL Similar images]**.
1. Use the search option, adjacent to _Filter_, to find a specific image.

   To use assets from a connected [!DNL AEM Assets Content Hub] repository, choose a repository from the _Location_ drop-down menu. Filter and select one image.

1. In the _Select image_ view, click on an image.
1. Click **[!UICONTROL Use]**.

   The Canvas, which serves as the central hub for content creation, is displayed. Four image variations similar to the original selected image appear.

   ![Generate similar images](/help/assets/generate-similar.png){width="400" zoomable="yes"} -->

## 이미지 게시 및 내보내기

생성된 이미지 초안은 _홈의_&#x200B;최근 항목[!DNL Create] 섹션에 표시됩니다.

생성된 이미지를 현재 및 나중에 사용할 수 있도록 하려면 이미지를 [!UICONTROL 콘텐츠]에 게시하고 마케팅 캠페인에서 사용하도록 내보내십시오.

1. **새 이미지를 게시하려면** 맨 위 도구 모음에서 **[!UICONTROL 게시]**&#x200B;를 클릭합니다.
   1. 원하는 경우 _[!UICONTROL 세부 정보 추가]_(예: _[!UICONTROL 캠페인]_ 또는 _[!UICONTROL 채널]_).
   1. **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

1. **새 이미지를 내보내려면** 맨 위 도구 모음에서 **[!UICONTROL 내보내기]**&#x200B;를 클릭합니다.
   1. JPG 또는 PNG 형식을 선택하고 **[!UICONTROL 내보내기]**&#x200B;를 클릭합니다.

[[!DNL Content]](/help/user-guide/content/overview.md#search-and-find-approved-content)을(를) 참조하십시오.
