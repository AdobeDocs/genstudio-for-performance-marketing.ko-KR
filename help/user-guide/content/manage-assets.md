---
title: 에셋 및 경험 관리
description: 디지털 마케팅 여정에서 사용하고 재사용하기 위해 브랜드 승인을 받은 에셋의 관리를 간소화하고 강화합니다.
feature: Content, Assets, Experiences
exl-id: e2ce8797-6d3b-46d4-b12f-f5f80e26c669
source-git-commit: 82ac164cb852305fce206845d15f04c4b4395387
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---

# 에셋 및 경험 관리

Adobe GenStudio for Performance Marketing [!DNL Content]은(는) 디지털 마케팅 여정에서 사용 및 재사용을 위해 브랜드 승인 에셋을 간편하게 관리하고 개선합니다.

## Assets 갤러리

[!UICONTROL Assets] 갤러리에 승인된 자산의 인벤토리가 표시됩니다. 테이블 왼쪽 위의 필터(단계) 아이콘은 **[!UICONTROL 필터]** 메뉴를 엽니다. 이 메뉴에서 여러 범주 중 선택하여 갤러리에 표시된 에셋을 필터링할 수 있습니다. 검색(돋보기) 아이콘을 클릭하여 키워드를 사용하여 에셋을 찾습니다.

다음은 [!UICONTROL Assets] 갤러리에서 `dog`이라는 용어에 대한 검색을 보여 줍니다.

![dog에서 검색이 포함된 Assets 보기](../../assets/content-assets.png)

### Assets 위치

기본적으로 [!DNL Create] 프로세스 또는 업로드를 통해 [!DNL Content]에 추가하는 자산은 `GenStudio assets` 저장소에 저장됩니다. `GenStudio assets` 리포지토리는 GenStudio for Performance Marketing의 읽기-쓰기 리포지토리입니다. 즉, `GenStudio assets` 저장소에서 에셋을 저장, 편집 및 삭제할 수 있습니다.

오른쪽의 갤러리 위에 있는 **[!UICONTROL 위치]** 목록을 사용하면 연결된 Adobe Experience Manager(AEM) [!DNL Assets Content Hub] 리포지토리에서 선택할 수 있습니다. AEM 저장소를 선택하면 갤러리에 해당 저장소의 자산 인벤토리가 표시되므로 이러한 저장소에서 승인된 자산을 콘텐츠 작성 입력으로 활용할 수 있습니다. 필터 옵션이 [!DNL AEM Assets Content Hub]에 구성된 범주를 반영하도록 변경됩니다.

[!DNL AEM Assets Content Hub] 리포지토리를 GenStudio for Performance Marketing에 추가하는 방법에 대한 지침은 [AEM 리포지토리 연결](connect-aem-repo.md)을 참조하십시오.

AEM 저장소는 읽기 전용입니다. 즉, 초안, 새 에셋 또는 메타데이터를 AEM 저장소에 저장할 수 없습니다. 에셋, 경험 및 템플릿에 대한 모든 초안 및 최종 업데이트는 새 [시스템 메타데이터](asset-details.md#system-metadata)를 사용하여 `GenStudio assets` 저장소에 저장됩니다.

{{note-aem-assets}}

## Assets 관리

[!UICONTROL 콘텐츠]에서 성능 마케터는 디지털 자산을 쉽게 저장, 검색 및 관리할 수 있습니다. `GenStudio assets` 리포지토리와 AEM 리포지토리를 모두 활용함으로써 사용자는 다양한 마케팅 캠페인에 맞게 에셋을 잘 구성하고 액세스할 수 있습니다. 이 다중 저장소 접근 방식은 여러 환경에서 에셋 사용에 대한 유연성과 제어 기능을 제공하여 승인된 최신 에셋만 마케팅 활동에 사용하도록 합니다.

### 에셋 추가

자산을 [!DNL Content]에 추가하면 기본적으로 `GenStudio assets` 저장소에 저장됩니다. _[!UICONTROL 자산 추가]_ 단추는 _[!UICONTROL 위치]_&#x200B;이(가) `GenStudio assets` 저장소인 경우에만 사용할 수 있습니다.

![위치 필드](../../assets/content-location.png){width="350" align="center"}

**하나 이상의 자산을 추가하려면**:

1. _[!DNL Content]_에서&#x200B;**[!UICONTROL 자산 추가]**를 클릭합니다.

1. _승인된 에셋 추가_ 보기에서 드롭 공간에 파일을 드롭합니다. 필요한 경우 **[!UICONTROL 찾아보기]**&#x200B;를 사용하여 로컬 파일에서 선택하거나 Dropbox 또는 Microsoft OneDrive에서 파일을 가져올 수 있습니다.

1. _세부 정보 추가_ 섹션에서 **[!UICONTROL 캠페인 이름]**&#x200B;을 선택하거나 새 이름을 입력하십시오.

1. 검색 기능을 향상시키려면 **추가 정보** 섹션에서 _브랜드 이름_, _가상 사용자_, _지역_ 및 _키워드_&#x200B;와 같은 선택적 세부 정보를 추가하십시오.

   자세히 제공할수록 GenStudio for Performance Marketing의 강력한 기능을 더 많이 경험하게 됩니다. 목록에서 세부 정보를 하나 이상 선택하거나, 해당하는 경우 키워드 등과 같이 새 세부 정보를 입력합니다. 추가하는 각 세부 사항은 목록 아래에 표시됩니다. 세부 정보를 제거하려면 **`x`**&#x200B;을(를) 클릭하십시오.

   추가하는 모든 세부 사항은 이 작업에 추가된 모든 자산에 적용됩니다.

   [메타데이터 세부 정보](/help/user-guide/content/asset-details.md#system-metadata)를 참조하세요.

1. **[!UICONTROL 자산 추가]**&#x200B;를 클릭합니다.

1. 에셋 업로드가 완료되면 **완료**&#x200B;를 클릭하세요.

1. 새로 업로드한 자산을 보려면 캔버스 하단의 _사용 가능한 새 자산_ 알림에서 **[!UICONTROL 새로 고침]**&#x200B;을 클릭하세요.

<!-- 
In the future, need guidance on template upload errors. For now, the UI just says error.
-->

### 콘텐츠 검색

필터 및 검색 인터페이스는 빠르고 반응적이며 생산적인 검색 우선 경험을 제공합니다. 각 [!DNL Content] 보기는 이상적인 자산, 경험 또는 템플릿에 대한 검색 범위를 좁히는 필터 옵션을 제공합니다. 에셋 및 경험의 경우 캠페인과 특정 지침(예: 특정 제품에 대해 만들어진 콘텐츠)을 선택할 수 있습니다.

검색 결과 범위를 좁히기 위해 [키워드](asset-details.md#user-defined-metadata) 및 [특성](/help/user-guide/insights/attributes.md)을 기반으로 하는 필터가 있습니다. 예를 들어, 캠페인에 대한 새로운 경험을 구축하는 데 도움이 되는 특정 파일 유형 또는 제목의 자산을 찾을 수 있습니다.

_경험_&#x200B;을(를) 검색할 때 **[!UICONTROL 작성자]** 필터를 사용하여 사용자 또는 특정 사용자가 만든 경험만 표시하도록 목록을 제한할 수 있습니다.

**재사용할 콘텐츠를 검색하려면**:

1. _[!DNL Content]_에서&#x200B;**[!UICONTROL Assets]**섹션을 선택합니다.

1. **[!UICONTROL 위치]** 목록에서 자산 리포지토리를 선택하거나 올바른 자산 리포지토리를 보고 있는지 확인하십시오. `GenStudio assets`이(가) 기본 리포지토리입니다.

   >[!IMPORTANT]
   >
   >_위치_ 목록은 [AEM 저장소에 연결](connect-aem-repo.md)하는 경우에만 사용할 수 있습니다.

1. 키워드나 설명을 입력하려면 **[!UICONTROL 검색]**(돋보기)을 클릭하십시오.

1. _[!UICONTROL 필터]_ 목록에서 범주를 선택하여 검색 범위를 좁힙니다. 예를 들어 PNG 파일을 찾으려면 **[!UICONTROL 파일 형식]**&#x200B;을 클릭하고 **PNG**&#x200B;를 선택하십시오.

   검색 범위를 좁힐수록 사용할 수 있는 필터 옵션이 줄어듭니다. 모든 필터를 제거하려면 **[!UICONTROL 모두 지우기]**&#x200B;를 클릭하십시오.

1. 전체 보기 및 세부 정보 목록을 위한 에셋을 선택합니다.

   로컬 워크스테이션에서 자산을 사용하려면 **[!UICONTROL 다운로드]**(아래쪽 화살표)를 클릭합니다.
