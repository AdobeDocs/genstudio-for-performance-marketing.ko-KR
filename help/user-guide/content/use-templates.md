---
title: 템플릿 작업
description: 템플릿을 효율적으로 사용하여 Adobe GenStudio for Performance Marketing에서 크리에이티브 프로세스를 간소화하는 방법에 대해 알아봅니다.
level: Intermediate
role: Developer
feature: Media Templates
exl-id: 7705bb79-19ca-4c16-8f8b-95bf8687e96d
source-git-commit: 7dfd915ebcc001b12357cfa334346e6698436d7d
workflow-type: tm+mt
source-wordcount: '1366'
ht-degree: 1%

---

# 템플릿 작업

GenStudio for Performance Marketing을 사용하면 콘텐츠 작성자가 _템플릿_&#x200B;을 사용하여 일관된 브랜드 내 마케팅 콘텐츠를 신속하게 만들 수 있습니다. 템플릿은 사전 구성된 레이아웃 및 디자인 요소를 포함하는 시작점을 제공하여 새 콘텐츠를 생성하는 데 필요한 시간과 노력을 크게 줄입니다. 시작하려면 [!DNL Content]에서 사용자 지정 템플릿을 업로드하거나 [!DNL Create]에서 시작 템플릿을 사용하십시오. [시작 템플릿](/help/user-guide/templates/starter-templates.md)은(는) 표준 디자인으로 빠르게 시작할 수 있는 방법을 제공하지만, 사용자 지정 템플릿을 사용하면 고유한 디자인과 레이아웃을 사용할 수 있습니다.

GenStudio for Performance Marketing에서는 애플리케이션 내에서 템플릿을 직접 만들 수 없지만 Adobe InDesign, Illustrator 또는 Express와 같이 인기 있는 디자인 도구를 사용하여 템플릿을 쉽게 디자인하고 준비할 수 있습니다. 디자인이 완료되면 GenStudio for Performance Marketing에서 사용하도록 조정할 수 있습니다. 다음 단계를 수행하여 템플릿 사용을 시작합니다.

1. **템플릿 디자인**: 기본 설정 디자인 도구를 사용하여 머리말, 헤드라인, 본문, CTA, 이미지, 바닥글 등의 요소가 있는 [템플릿의 시각적 레이아웃을 만듭니다](#template-elements).

2. **템플릿 코드**: 디자인을 HTML 및 인라인 CSS로 변환하여 다양한 장치에서 깔끔하고 반응하도록 합니다. 원하는 최대 대상자에 도달하도록 하려면 [접근성 지침](accessibility-for-templates.md)을 고려하십시오.

3. **GenStudio for Performance Marketing 준비**: Handlebars 템플릿 언어를 사용하여 HTML 템플릿을 조정하십시오. GenStudio for Performance Marketing에서 콘텐츠를 동적으로 생성하는 위치를 나타내는 자리 표시자를 삽입합니다. GenStudio for Performance Marketing용 [템플릿 사용자 지정](customize-template.md)하는 방법을 확인하세요.

이러한 단계를 따라 GenStudio for Performance Marketing에서 사용할 수 있는 전문적이고 효과적인 템플릿을 만들어 브랜드 내 콘텐츠를 빠르고 효율적으로 생성할 수 있습니다.

## 템플릿 요소

템플릿은 이메일, 소셜 광고를 만들거나 광고 경험을 표시하는 데 사용할 수 있는 HTML 및 인라인 CSS로 정의된 지침 세트입니다. 템플릿 요소는 콘텐츠 작성을 위한 구조를 제공합니다.

다음은 템플릿에 사용되는 요소 목록과 해당 특성에 대한 세부 정보입니다.

| **요소** | **채널** | **설명** |
|----------------------|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **사전 머리글** | 이메일 | 이메일의 기본 제목 줄을 개선하는 보조 제목 줄(일반적으로 40-50자 사이)입니다. 이메일이 열리기 전에 제목과 함께 받은 편지함에 표시됩니다. |
| **헤더** | 이메일 | 이메일을 열 때 수신자가 보는 이메일의 상단 섹션은 톤을 설정하고 포함된 콘텐츠에 대한 컨텍스트를 제공합니다. |
| **제목** | 메타 광고, 배너 및 디스플레이 광고, LinkedIn | 수신자가 보는 첫 번째 콘텐츠는 관심을 끌어야 합니다. |
| **하위 헤드라인** | 이메일, 배너 및 디스플레이 광고 | 헤드라인을 지원하는 보조 텍스트 요소입니다. 일반적으로 간결하고 주요 헤드라인을 보완하도록 설계되어 있어 독자의 관심을 콘텐츠로 더욱 끌어당깁니다. |
| **소개 텍스트** | LinkedIn | 기본 메시지는 본문 사본과 유사한 핵심 메시지를 전달합니다. 공백, 최대 4개의 이모지, 구두점 등 최대 150자를 사용할 수 있다. |
| **본문** | 이메일, 메타 광고, 배너 및 디스플레이 광고 | 광고의 주요 텍스트가 핵심 메시지를 전달합니다. 관객에게 원하는 행동을 장려하기 위해 매력적이고, 유익하며, 설득력이 있어야 한다. |
| **CTA** | 이메일, 메타 광고, 배너 및 디스플레이 광고, LinkedIn | call-to-action 버튼은 구문과 링크를 사용하여 수신자가 링크를 클릭하거나 구매하는 등의 특정 작업을 수행하도록 장려합니다. |
| **이미지** | 이메일, 메타 광고, 배너 및 디스플레이 광고, LinkedIn | 시각적 호소력을 높이고, 텍스트를 분류하고, 메시지를 지원합니다. 이미지는 고화질로 눈을 사로잡아야 합니다. |
| **바닥글** | 이메일 | 이메일의 아래 섹션에는 연락처 세부 정보, 소셜 미디어 링크, 면책조항 및 구독 취소 옵션과 같은 추가 콘텐츠가 포함되어 있습니다. |
| **텍스트 오버레이** | 메타 광고 | 헤드라인 및 본문 컨텐츠를 지원하고 개선하기 위해 이미지에 배치된 텍스트입니다. |

>[!TIP]
>
>각 채널 유형의 템플릿에 대해 GenStudio for Performance Marketing에서 지원하는 [인식된 필드 이름](customize-template.md#recognized-field-names)을(를) 참조하십시오.

## 템플릿 맞춤화

생성 AI가 콘텐츠를 삽입하는 데 사용하는 콘텐츠 자리 표시자 또는 필드를 삽입하여 GenStudio for Performance Marketing에서 사용할 [템플릿을 사용자 지정](customize-template.md)합니다. GenStudio for Performance Marketing은 `body` 필드와 같은 특정 필드를 인식하고 선택한 브랜드에 대해 구성된 채널 지침을 준수합니다.

>[!TIP]
>
>더 많은 대상자에게 도달하고 최적의 경험을 제공할 수 있도록 [접근성 지침](accessibility-for-templates.md) 및 [모범 사례](/help/user-guide/content/best-practices-for-templates.md)를 따르십시오.

## 템플릿 관리

_[!DNL Templates]_&#x200B;갤러리에는 GenStudio for Performance Marketing에서 경험을 생성하기 위해 사용자 지정된 템플릿 인벤토리가 표시됩니다.

### 템플릿 검색

각 [!DNL Content] 보기는 이상적인 자산, 경험 또는 템플릿에 대한 검색 범위를 좁히는 필터 옵션을 제공합니다. 검색 결과의 범위를 좁히기 위해 [지침](/help/user-guide/guidelines/overview.md), [키워드](asset-details.md#user-defined-metadata) 및 [특성 범주](/help/user-guide/insights/attributes.md#categories)를 기반으로 하는 필터가 있습니다.

예를 들어 사용자가 만든 특정 채널 유형 또는 종횡비의 템플릿을 찾을 수 있습니다.

- **[!UICONTROL 만든 사람]**: 사용자 또는 특정 사용자가 만든 템플릿만 표시하도록 _[!UICONTROL 템플릿]_ 목록을 제한합니다.
- **[!UICONTROL 종횡비]**: _[!UICONTROL 템플릿]_ 목록을 제한하여 특정 종횡비에 맞게 디자인된 템플릿을 표시합니다.

다음은 이메일, 디스플레이 광고, 메타 광고 및 LinkedIn 광고와 같은 채널 유형별 필터를 보여줍니다.

![콘텐츠 템플릿 목록](/help/assets/content-templates-filter.png "LinkedIn 템플릿 검색"){width="650" zoomable="yes"}

템플릿 검색 기능은 [!UICONTROL 만들기] 중에 소유 또는 유료 미디어에 대한 템플릿을 선택할 때 사용할 수 있습니다. 특정 필터 옵션이 표시되지 않으면 저장소에 해당 메타데이터 기준과 일치하는 템플릿이 없음을 나타냅니다. 이러한 필터를 통해 검색할 수 있도록 템플릿에 메타데이터가 올바르게 태그 지정되었는지 확인합니다.

### 템플릿 추가

템플릿을 업로드하기 전에 [템플릿 사용자 지정](customize-template.md)의 안내에 따라 GenStudio for Performance Marketing에서 사용할 수 있도록 완전히 준비되었는지 확인하십시오.

**템플릿을 추가하려면**:

1. _[!DNL Content]_&#x200B;에서&#x200B;**[!UICONTROL 템플릿]**&#x200B;섹션을 선택하십시오.

1. **[!UICONTROL 템플릿 추가]**&#x200B;를 클릭합니다.

1. _[!UICONTROL 승인된 템플릿 추가]_ 창에서 HTML 템플릿 파일을 검색하거나 HTML 템플릿 파일을 드롭 공간으로 드래그합니다. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

1. _[!UICONTROL 검색된 필드 확인]_ 창에서 필드를 검토합니다. 올바른 템플릿을 사용 중인지 확인하고 모든 세부 정보가 예상대로인지 확인합니다.

   이메일 템플릿에 대한 미리 보기 예:

   ![미리 보기 필드가 검색됨](/help/assets/template-detected-fields.png){width="650" zoomable="yes"}

   >[!TIP]
   >
   >템플릿이 올바르지 않으면 **[!UICONTROL 뒤로]**&#x200B;를 클릭하고 이전 단계로 돌아갑니다. 수정된 템플릿 파일을 업로드합니다. 또는 [템플릿 코드 편집기](/help/user-guide/content/code-editor.md)를 사용하여 간단하게 수정할 수 있습니다.

1. 템플릿 미리 보기에 만족하면 **[!UICONTROL 다음]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL 템플릿 세부 정보 제공 및 업로드]_&#x200B;에서 템플릿 이름을 지정하고 **[!UICONTROL 채널]** 유형을 선택하십시오.

   템플릿 이름 및 채널 유형은 필수입니다. 추가 요구 사항은 다음과 같습니다.

   - **Meta**: 종횡비가 필요합니다.
   - **배너 및 디스플레이 광고**: 차원 필요

1. 검색 및 필터링에서 템플릿 식별을 개선하기 위해 가능한 한 많은 세부 정보를 추가합니다.

1. **[!UICONTROL 완료]**&#x200B;를 클릭합니다.

### 템플릿 새로 고침

템플릿에는 아이콘 또는 로고와 같은 정적 파일이 포함될 수 있습니다. 템플릿 미리 보기를 만든 후 [정적 콘텐츠](/help/user-guide/content/customize-template.md#static-content)이(가) 저장되지 않습니다. GenStudio for Performance Marketing은 템플릿에 제공된 소스 링크를 계속 참조합니다. 새로 고침을 사용하여 이러한 에셋의 최신 버전으로 템플릿 미리 보기를 업데이트합니다.

**템플릿을 새로 고치려면**:

1. _[!DNL Content]_&#x200B;에서&#x200B;**[!UICONTROL 템플릿]**&#x200B;섹션을 선택하십시오.

1. 전체 보기 및 세부 정보 목록을 보려면 템플릿을 클릭합니다.

1. 템플릿에 사용된 모든 자산을 새로 고치려면 오른쪽 상단에서 **[!UICONTROL 새로 고침]**(순환 화살표)을 클릭합니다.

### 템플릿을 사용하여 경험 만들기

GenStudio for Performance Marketing에서 기존 템플릿을 찾아 사용하여 더 많은 경험을 만듭니다.

**템플릿을 사용하여 환경을 만들려면**:

1. _[!DNL Content]_&#x200B;에서&#x200B;**[!UICONTROL 템플릿]**&#x200B;섹션을 선택하십시오.

1. 전체 보기 및 세부 정보 목록을 보려면 템플릿을 클릭합니다.

1. 템플릿을 사용하려면 오른쪽 상단에서 **[!UICONTROL 경험 만들기]**(페인트 브러쉬)를 클릭하십시오.

1. 경험을 [만들기](/help/user-guide/create/overview.md#create-use-cases)합니다.

## AJO 및 Marketo 템플릿

Adobe Journey Optimizer(AJO) 또는 Marketo에서 만든 템플릿을 업로드할 수 있습니다. GenStudio for Performance Marketing은 애플리케이션별 패턴을 감지하고 이를 무시하며 AJO 또는 Marketo에서 계속 사용할 수 있도록 원래 양식을 보존합니다. 원래 AJO 또는 Marketo 구문을 변경할 필요가 없습니다.

인식된 애플리케이션 패턴은 다음과 같습니다.

- **AJO**: `{{profile.*}}`, `{{context.*}}`
- **Marketo**: `{{my.*}}`, `{{lead.*}}`, `{{system.*}}`

>[!BEGINSHADEBOX]

**사전 요구 사항**

- 통합을 위해 애플리케이션(AJO, Marketo)과 GenStudio for Performance Marketing이 동일한 IMS 조직에 속해 있어야 합니다
- 사용자는 &quot;공동 작업자&quot; 역할(최하위 레벨) 이상이 있어야 합니다.

>[!ENDSHADEBOX]

다음으로, GenStudio for Performance Marketing에서 콘텐츠를 생성할 위치를 나타내는 자리 표시자를 사용하여 [템플릿을 사용자 지정](/help/user-guide/content/customize-template.md)합니다. [템플릿을 [!DNL Content] 저장소에 추가](#add-a-template)하고 템플릿의 유효성을 검사하십시오. 코드 편집기를 사용하여 사소한 사항을 수정합니다.
