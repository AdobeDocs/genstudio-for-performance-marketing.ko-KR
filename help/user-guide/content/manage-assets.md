---
title: Assets 및 경험 관리
description: 디지털 마케팅 여정에서 사용하고 재사용하기 위해 브랜드 승인을 받은 에셋의 관리를 간소화하고 강화합니다.
feature: Content Management, Content Attributes
exl-id: e2ce8797-6d3b-46d4-b12f-f5f80e26c669
source-git-commit: 3251d81a6bfb0c1f7d2bf3c5bd319ad4e2237699
workflow-type: tm+mt
source-wordcount: '1509'
ht-degree: 1%

---

# 에셋 및 경험 관리

Adobe GenStudio for Performance Marketing [!DNL Content]은(는) 디지털 마케팅 여정에서 사용 및 재사용을 위해 브랜드 승인 에셋을 간편하게 관리하고 개선합니다.

## [!DNL Content] 갤러리

갤러리에는 선택한 보기에 따라 승인된 에셋, 경험 또는 템플릿의 인벤토리가 표시됩니다. 표의 왼쪽 위에 있는 필터(funnel) 전환은 **[!UICONTROL 필터]** 메뉴를 엽니다. 이 메뉴에서 여러 범주 중 선택하여 갤러리에 표시되는 콘텐츠를 필터링할 수 있습니다. _[!UICONTROL Assets]_ 보기에서 검색(돋보기) 아이콘을 클릭하여 키워드를 사용하여 자산을 찾습니다.

다음은 `space`Assets[!UICONTROL &#x200B; 갤러리에서 &#x200B;]이라는 용어에 대한 검색을 보여 줍니다.

![스페이스에서 검색이 있는 Assets 보기](/help/assets/content-assets-filter.png "스페이스 특성이 있는 에셋 검색")

### 콘텐츠 검색

필터 및 검색 인터페이스는 빠르고 반응적이며 생산적인 검색 우선 경험을 제공합니다. 각 [!DNL Content] 보기는 이상적인 자산, 경험 또는 템플릿에 대한 검색 범위를 좁히는 필터 옵션을 제공합니다. 에셋 및 경험의 경우 캠페인과 특정 지침(예: 특정 제품에 대해 만들어진 콘텐츠)을 선택할 수 있습니다.

검색 결과의 범위를 좁히기 위해 [지침](/help/user-guide/guidelines/overview.md), [키워드](asset-details.md#user-defined-metadata) 및 [특성 범주](/help/user-guide/insights/attributes.md#categories)를 기반으로 하는 필터가 있습니다. 예를 들어, 캠페인에 대한 새로운 경험을 구축하는 데 도움이 되는 특정 파일 유형 또는 제목의 자산을 찾을 수 있습니다. 또는 사용자 이름 또는 팀원의 이름을 기반으로 콘텐츠를 필터링할 수 있습니다.

- **[!UICONTROL 업로드한 사람]**: 사용자 또는 특정 사용자가 업로드한 자산만 표시하도록 _[!UICONTROL Assets]_ 목록을 제한합니다.
- **[!UICONTROL 만든 사람]**: 사용자 또는 특정 사용자가 만든 경험만 표시하도록 _[!UICONTROL 경험]_ 목록을 제한합니다.
- **[!UICONTROL 템플릿]**: 선택한 템플릿으로 만든 경험만 표시하도록 _[!UICONTROL 경험]_ 목록을 제한합니다.

특정 필터 옵션이 표시되지 않으면 저장소에 해당 메타데이터 기준과 일치하는 템플릿이 없음을 나타냅니다. 이러한 필터를 통해 검색할 수 있도록 템플릿에 메타데이터가 올바르게 태그 지정되었는지 확인합니다.

**재사용할 콘텐츠를 검색하려면**:

1. _[!DNL Content]_&#x200B;에서&#x200B;**[!UICONTROL Assets]**&#x200B;섹션을 선택합니다.

1. **[!UICONTROL 위치]** 목록에서 자산 리포지토리를 선택하거나 올바른 자산 리포지토리를 보고 있는지 확인하십시오. `GenStudio assets`이(가) 기본 리포지토리입니다.

   >[!IMPORTANT]
   >
   >_위치_ 목록은 [AEM 저장소에 연결](connect-aem-repo.md)하는 경우에만 사용할 수 있습니다.

1. 키워드나 설명을 입력하려면 **[!UICONTROL 검색]**(돋보기)을 클릭하십시오.

1. _[!UICONTROL 필터]_ 목록에서 범주를 선택하여 검색 범위를 좁힙니다. 예를 들어 PNG 파일을 찾으려면 **[!UICONTROL 파일 형식]**&#x200B;을 클릭하고 **PNG**&#x200B;를 선택하십시오.

   검색 범위를 좁힐수록 사용할 수 있는 필터 옵션이 줄어듭니다. 모든 필터를 제거하려면 **[!UICONTROL 모두 지우기]**&#x200B;를 클릭하십시오.

1. 전체 보기 및 세부 정보 목록을 위한 에셋을 선택합니다.

   로컬 워크스테이션에서 자산을 사용하려면 **[!UICONTROL 다운로드]**(아래쪽 화살표)를 클릭합니다.

### 위치

기본적으로 [!DNL Content] 프로세스 또는 업로드를 통해 [!DNL Create]에 추가하는 자산은 `GenStudio assets` 저장소에 저장됩니다. `GenStudio assets` 리포지토리는 GenStudio for Performance Marketing의 읽기-쓰기 리포지토리입니다. 즉, `GenStudio assets` 저장소에서 에셋을 저장, 편집 및 삭제할 수 있습니다.

오른쪽의 **[!UICONTROL Assets]** 갤러리 위에 있는 _[!UICONTROL 위치]_ 목록을 사용하면 연결된 Adobe Experience Manager(AEM) [!DNL Assets Content Hub] 리포지토리에서 선택할 수 있습니다.

![저장소의 위치 목록](/help/assets/content-location-selection.png "콘텐츠 저장소 선택"){width="350"}

AEM 저장소를 선택하면 갤러리에 해당 저장소의 자산 인벤토리가 표시되므로 이러한 저장소에서 승인된 자산을 콘텐츠 작성 입력으로 활용할 수 있습니다. 필터 옵션이 [!DNL AEM Assets Content Hub]에 구성된 범주를 반영하도록 변경됩니다.

[&#x200B; 리포지토리를 AEM에 추가하는 방법에 대한 지침은 &#x200B;](connect-aem-repo.md)GenStudio for Performance Marketing 리포지토리 연결[!DNL AEM Assets Content Hub]을 참조하십시오.

AEM 저장소는 읽기 전용입니다. 즉, 콘텐츠에 액세스할 수 있지만 초안, 새 에셋 또는 메타데이터를 AEM 저장소에 저장할 수는 없습니다. 에셋, 경험 및 템플릿에 대한 모든 초안 및 최종 업데이트는 새 `GenStudio assets`시스템 메타데이터[를 사용하여 &#x200B;](asset-details.md#system-metadata) 저장소에 저장됩니다.

{{note-aem-assets}}

AEM 저장소는 에셋 만료와 같은 특정 라이선스 요구 사항을 적용할 수 있습니다. 이러한 자산은 [!DNL Create] 워크플로우에서 사용할 수 없습니다. 프로젝트의 연속성을 유지하기 위해 만료된 에셋을 갱신하거나 교체해야 할 수 있습니다. 이러한 자산에 대한 도움이 필요하면 [!DNL AEM Assets Content Hub] 관리자에게 문의하십시오.

## Assets 관리

[!UICONTROL 콘텐츠]에서 디지털 자산을 쉽게 저장, 검색 및 관리할 수 있습니다. `GenStudio assets` 리포지토리와 AEM 리포지토리를 모두 활용하므로 다양한 마케팅 캠페인에 사용할 수 있도록 에셋을 잘 구성하고 액세스할 수 있습니다. 이 다중 저장소 접근 방식은 여러 환경에서 에셋 사용에 대한 유연성과 제어 기능을 제공하여 승인된 최신 에셋만 마케팅 활동에 사용하도록 합니다.

다음 표에는 에셋, 경험 및 템플릿에 사용할 수 있는 관리 작업이 나열되어 있습니다.

| 작업 | 자산 | 경험 | 템플릿 |
| --------------------------------------------------------- | :----: | :---------: | :-------: |
| [세부 정보 보기](/help/user-guide/content/asset-details.md) | ✓ | ✓ | ✓ |
| [경험 만들기](/help/user-guide/create/overview.md) |        |             | ✓ |
| [Adobe Express에서 편집](#edit-in-express) | ✓ |             |           |
| [경험 내보내기](#export-experiences) |        | ✓ |           |
| [새로 고침](/help/user-guide/templates/use-templates.md#refresh-template) |   |      | ✓ |
| [다운로드](#download-assets) | ✓ |             | ✓ |
| [삭제](#delete-assets) | ✓ | ✓ | ✓ |

### 자산 추가

자산을 [!DNL Content]에 추가하면 기본적으로 `GenStudio assets` 저장소에 저장됩니다. _[!UICONTROL 자산 추가]_ 단추는 _[!UICONTROL 위치]_&#x200B;이(가) `GenStudio assets` 저장소인 경우에만 사용할 수 있습니다.

![위치 필드](/help/assets/content-location.png "위치 필드"){width="350"}

**하나 이상의 자산을 추가하려면**:

1. _[!DNL Content]_&#x200B;에서&#x200B;**[!UICONTROL 자산 추가]**&#x200B;를 클릭합니다.

2. _승인된 에셋 추가_ 보기에서 드롭 공간에 파일을 드롭합니다. 필요한 경우 **[!UICONTROL 찾아보기]**&#x200B;를 사용하여 로컬 파일에서 선택하거나 Dropbox 또는 Microsoft OneDrive에서 파일을 가져올 수 있습니다.

3. _세부 정보 추가_ 섹션에서 **[!UICONTROL 캠페인 이름]**&#x200B;을 선택하거나 새 이름을 입력하십시오.

4. 검색 기능을 위해 _추가 정보_ 섹션에서 _브랜드 이름_, _가상 사용자_, _지역_ 및 **키워드**&#x200B;와 같은 선택적 세부 정보를 추가하십시오.

   자세히 제공할수록 GenStudio for Performance Marketing의 강력한 기능을 더 많이 경험하게 됩니다. 목록에서 세부 정보를 하나 이상 선택하거나, 해당하는 경우 키워드 등과 같이 새 세부 정보를 입력합니다. 추가하는 각 세부 사항은 목록 아래에 표시됩니다. 세부 정보를 제거하려면 **`x`**&#x200B;을(를) 클릭하십시오.

   추가하는 모든 세부 사항은 이 작업에 추가된 모든 자산에 적용됩니다.

   [메타데이터 세부 정보](/help/user-guide/content/asset-details.md#system-metadata)를 참조하세요.

5. **[!UICONTROL 자산 추가]**&#x200B;를 클릭합니다.

6. 에셋 업로드가 완료되면 **완료**&#x200B;를 클릭하세요.

7. 새로 업로드한 자산을 보려면 캔버스 하단의 **[!UICONTROL 사용 가능한 새 자산]** 알림에서 _새로 고침_&#x200B;을 클릭하세요.

### 자산 다운로드

**자산을 다운로드하려면**:

1. _[!DNL Content]_&#x200B;에서 에셋 또는 템플릿을 선택합니다. 에셋을 클릭하면 에셋의 중요 보기가 열립니다.

1. 에셋 보기에서 오른쪽 상단의 **[!UICONTROL 다운로드]** 아이콘(아래쪽을 가리키는 화살표)을 클릭합니다.

1. 다운로드는 기본 다운로드 위치에 에셋 사본을 배치하기 시작합니다.

### 에셋 삭제

**자산을 삭제하려면**:

1. _[!DNL Content]_&#x200B;에서 에셋, 경험 또는 템플릿을 선택합니다. 에셋을 클릭하면 에셋의 중요 보기가 열립니다.

1. 자산 보기에서 오른쪽 상단의 **[!UICONTROL 삭제]**(휴지통)을 클릭합니다.

1. _자산 삭제_ 팝업에서 자산을 확인하고 **[!UICONTROL 삭제]**&#x200B;를 클릭합니다.

## 경험 내보내기

타겟 채널과 호환되는 형식으로 다운로드할 승인된 경험을 하나 이상 선택할 수 있습니다. 다운로드한 파일의 이름은 내보내기 날짜 `2025-06-15-export.zip`을(를) 사용하여 지정합니다. 파일의 압축을 해제하면 선택한 형식으로 내보낸 에셋을 포함하는 각 채널 유형에 대한 폴더가 있습니다. 내보낸 각 에셋은 원래 에셋 이름을 파일 이름으로 유지합니다.

>[!WARNING]
>
>검색된 에셋은 삭제하지 않고 표시하는 것은 안전하지 않습니다. 모든 사용자는 입력 정리 기술을 사용하여 템플릿에서 XSS(크로스 사이트 스크립팅)를 처리해야 합니다.

**경험을 내보내거나 다운로드하려면**:

1. _[!DNL Content]_&#x200B;에서 경험을 하나 이상 선택하십시오.

   배너는 왼쪽에 선택한 경험 수와 오른쪽에 [!UICONTROL 활성화], [!UICONTROL 다운로드] 또는 [!UICONTROL 삭제]에 대한 옵션이 표시됩니다.

2. (선택 사항) 활성화하도록 선택하면 플랫폼을 선택한 다음 [!DNL Activate] 워크플로우를 계속하라는 메시지가 표시될 수 있습니다. [활성화](/help/user-guide/activation/overview.md)를 참조하세요.

3. **[!UICONTROL 다운로드]**&#x200B;를 클릭합니다.

4. _다운로드_ 팝업에서 사용 가능한 형식 중 하나를 선택합니다.

   서로 다른 채널에서 여러 경험을 선택한 경우 각 채널 유형에 대한 포맷을 선택할 수 있습니다.

   - 이메일, LinkedIn: `HTML`, `CSV`, `PDF`
   - Meta, 배너 및 디스플레이 광고: `HTML`, `JPEG`, `PNG`, `PDF`


## Express에서 편집

Adobe Express을 사용하여 GenStudio for Performance Marketing 내에서 직접 이미지 에셋(JPG 또는 PNG)을 편집할 수 있습니다. _[!UICONTROL Adobe Express 제공]_ 캔버스는 GenStudio 응용 프로그램을 종료하지 않고도 이미지를 개선할 수 있는 편리한 기능을 제공합니다. 배경을 쉽게 제거하고, 생성 채우기를 적용하고, 효과를 조정하고, 이미지를 자를 수 있습니다.

>[!BEGINSHADEBOX]

[!DNL Edit in Adobe Express] 기능을 사용하여 이미지를 개선하기 위한 기준:

- 지원되는 MIME 형식에는 `image/png` 및 `image/jpeg`이(가) 포함됩니다.
- 최소 이미지 크기는 50x50픽셀입니다
- 최대 이미지 크기는 8000x8000픽셀입니다
- 최대 크기는 40MB(40,000,000바이트)입니다.

>[!ENDSHADEBOX]

**Express로 자산을 편집하려면**:

1. _[!DNL Content]_&#x200B;에서 이미지 자산을 선택합니다. 에셋을 클릭하면 에셋의 중요 보기가 열립니다.

1. 에셋 보기에서 오른쪽 상단의 **[!UICONTROL Adobe Express에서 편집]** 아이콘을 클릭합니다.

1. _[!UICONTROL Adobe Express에서 제공하는]_ 캔버스에서 왼쪽 패널의 Express 컨트롤을 사용하여 이미지를 향상시킵니다.

1. 업데이트된 이미지가 마음에 들면 오른쪽 상단의 **[!UICONTROL 복사본 저장]**&#x200B;을 클릭하세요.

1. 파일 형식(JPG 또는 PNG)을 선택하고 **[!UICONTROL 복사본 저장]**&#x200B;을 클릭합니다.

1. _[!UICONTROL 에셋 복사본 저장]_ 팝업에서 **[!UICONTROL 에셋 이름]**&#x200B;을(를) 업데이트합니다.

   - **[!UICONTROL 원본 에셋과 동일한 세부 정보]**&#x200B;를 선택하여 에셋 세부 정보를 새 이미지로 이전합니다.

   - **[!UICONTROL 추가 정보]** 섹션을 확장하여 지침 및 기타 메타데이터를 업데이트합니다.

   >[!TIP]
   >
   >자세히 제공할수록 GenStudio for Performance Marketing의 강력한 기능을 더 많이 경험하게 됩니다. 목록에서 세부 정보를 하나 이상 선택하거나, 해당하는 경우 키워드 등과 같이 새 세부 정보를 입력합니다. 추가하는 각 세부 사항은 목록 아래에 표시됩니다. 세부 정보를 제거하려면 **`x`**&#x200B;을(를) 클릭하십시오.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
