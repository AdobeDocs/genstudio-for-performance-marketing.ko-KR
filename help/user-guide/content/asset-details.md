---
title: 자산 세부 사항
description: Adobe GenStudio for Performance Marketing은 검색 기능 및 성능 추적을 위해 승인된 컨텐츠를 풍부한 메타데이터와 함께 저장합니다.
feature: Attributes, Assets
exl-id: 2be5cfee-f315-4ad6-8cf0-a8d3929b9ba3
source-git-commit: edd27a6151cb81213ee27813beb4ecee835a1229
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 0%

---

# 자산 세부 사항

Adobe GenStudio for Performance Marketing은 검색 기능 및 성능 추적을 위해 승인된 컨텐츠를 풍부한 메타데이터와 함께 저장합니다.

각 자산(경험 및 템플릿 포함)에는 콘텐츠 성능을 식별, 추적, 사용 및 학습하는 데 도움이 되는 _세부 정보_(메타데이터)가 연결되었습니다.

**자산 세부 정보를 보려면**:

1. _[!DNL Content]_에서 에셋, 경험 또는 템플릿을 선택합니다. 에셋을 클릭하면 에셋의 중요 보기가 열립니다.

1. 자산 보기에서 오른쪽의 _[!UICONTROL 세부 정보]_ 섹션을 검토합니다.

   >[!TIP]
   >
   >_[!UICONTROL 세부 정보]_ 섹션이 표시되지 않으면 **[!UICONTROL 정보]**(i) 아이콘을 클릭합니다.

   에셋 세부 사항에는 생성 또는 업로드 프로세스 중에 적용된 메타데이터가 포함됩니다. 에셋 메타데이터 유형에는 [시스템 메타데이터](#system-metadata) 및 [사용자 정의 메타데이터](#user-defined-metadata)가 포함됩니다.

>[!NOTE]
>
>AEM 저장소의 Assets에 다른 메타데이터가 표시됩니다. [!DNL AEM Assets Content Hub] 자산 세부 정보를 구성하는 방법은 [자산 가시성 구성](connect-aem-repo.md#step-4-configure-asset-visibility)을 참조하세요.

## Express에서 편집

Adobe Express을 사용하여 GenStudio for Performance Marketing 내에서 직접 이미지 에셋(JPG 또는 PNG)을 편집할 수 있습니다. _[!UICONTROL Adobe Express 제공]_ 캔버스는 GenStudio 응용 프로그램을 종료하지 않고도 이미지를 개선할 수 있는 편리한 기능을 제공합니다. 배경을 쉽게 제거하고, 생성 채우기를 적용하고, 효과를 조정하고, 이미지를 자를 수 있습니다.

1. _[!DNL Content]_에서 이미지 자산을 선택합니다. 에셋을 클릭하면 에셋의 중요 보기가 열립니다.

1. 에셋 보기에서 오른쪽 상단의 **[!UICONTROL Adobe Express에서 편집]** 아이콘을 클릭합니다.

1. _[!UICONTROL Adobe Express 제공]_ 캔버스에서 왼쪽 패널의 Express 컨트롤을 사용하여 이미지를 향상시킵니다.

1. 업데이트된 이미지가 마음에 들면 오른쪽 상단의 **[!UICONTROL 복사본 저장]**&#x200B;을 클릭하세요.

1. 파일 형식(JPG 또는 PNG)을 선택하고 **[!UICONTROL 복사본 저장]**&#x200B;을 클릭합니다.

1. _[!UICONTROL 에셋 복사본 저장]_ 팝업에서 **[!UICONTROL 에셋 이름]**&#x200B;을(를) 업데이트합니다.

   - **[!UICONTROL 원본 에셋과 동일한 세부 정보]**&#x200B;를 선택하여 에셋 세부 정보를 새 이미지로 이전합니다.

   - **[!UICONTROL 추가 세부 정보]** 섹션을 확장하여 Campaign, 지침 및 기타 메타데이터를 업데이트합니다.

   >[!TIP]
   >
   >자세히 제공할수록 GenStudio for Performance Marketing의 강력한 기능을 더 많이 경험하게 됩니다. 목록에서 세부 정보를 하나 이상 선택하거나, 해당하는 경우 키워드 등과 같이 새 세부 정보를 입력합니다. 추가하는 각 세부 사항은 목록 아래에 표시됩니다. 세부 정보를 제거하려면 **`x`**&#x200B;을(를) 클릭하십시오.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 시스템 메타데이터

일부 에셋 메타데이터는 에셋이 업로드될 때 자동으로 수집됩니다. 기본 시스템 메타데이터는 편집할 수 없습니다.

에셋에 대해 저장되고 캡처되는 기본 메타데이터에는 파일 이름, 차원, 소스 등이 포함됩니다.

### 생성된 태그

승인된 에셋을 [!DNL Content]에 저장하면 GenStudio for Performance Marketing에서 Adobe의 AI 및 머신 러닝 기능을 사용하여 에셋을 학습하고 에셋 기능을 기반으로 태그를 적용합니다. 예를 들어, 고양이 그림으로 인해 `pet photography` 또는 `cat`과(와) 같은 속성 태그와 그림에서 지배적인 색상을 식별하는 색상 태그가 발생할 수 있습니다. 검색되어 자동으로 적용되는 태그는 편집할 수 없습니다.

이미지, 비디오 및 텍스트 기능에 대한 자세한 목록은 [!DNL Insights] [특성 범주](/help/user-guide/insights/attribute-category.md)를 참조하십시오.

### 생성된 컨텐츠 메타데이터

새 에셋 또는 경험을 생성하는 데 사용된 정보는 사용된 프롬프트와 같은 메타데이터가 됩니다. 컨텐츠가 승인된 후에는 프롬프트를 편집할 수 없지만, 새로운 항목을 생성하기 위한 시작 위치로 사용할 수 있습니다.

## 사용자 정의 메타데이터

사용자 정의 메타데이터는 에셋의 콘텐츠에 마케팅 컨텍스트를 추가하여 마케터가 에셋을 사용하고 참여하는 방법을 이해할 수 있도록 합니다.

[에셋을 업로드](/help/user-guide/content/manage-assets.md#add-assets)할 때 GenStudio for Performance Marketing에 메타데이터로 존재하는 선택적 에셋 세부 정보 집합을 정의할 수 있습니다. 더 많은 세부 정보를 포함하면 검색 및 필터링에서 에셋 식별을 향상시킬 수 있습니다.

### 메타데이터 세부 정보

다음 표에서는 자산을 생성할 때 정의할 수 있는 메타데이터(자산 세부 사항)에 대해 자세히 설명합니다.

| 필드 | 설명 |
| ------------- | ----------- |
| 캠페인(프로젝트 이름) | 에셋으로 캡처 및 저장된 기본 메타데이터 |
| [!DNL Brands] | [[!DNL Brands]](/help/user-guide/guidelines/brands.md)이(가) GenStudio for Performance Marketing에 추가되고 사용을 위해 게시됨 |
| [!DNL Products] | [[!DNL Products]](/help/user-guide/guidelines/products.md)이(가) 사용을 위해 GenStudio for Performance Marketing에 추가됨 |
| [!DNL Personas] | [[!DNL Personas]](/help/user-guide/guidelines/personas.md)이(가) 사용을 위해 GenStudio for Performance Marketing에 추가됨 |
| 채널 | 이메일 및 메타 광고와 같이 에셋이 사용되는 GenStudio for Performance Marketing의 콘텐츠 유형 |
| 일정 | 에셋이 사용된 기간(예: 분기, 시즌, 연도 등) 예: `Winter 2023` |
| 지역 | 자산이 사용되는 지역. 예: `North America`, `APAC`, `Italy` |
| 언어 | 에셋이 사용되는 언어입니다. 예: `Spanish` |
| 키워드 | 자산 특성 및 용도를 추가로 식별하기 위해 사용되는 키워드 |

<!-- ## History

Expand the _[!UICONTROL History]_ section to view a timeline of approvals and activity.

list other activity, show screenshot?
-->
