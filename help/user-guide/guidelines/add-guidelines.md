---
title: Adobe GenStudio for Performance Marketing에 지침 추가
description: Adobe GenStudio for Performance Marketing에서 프롬프트에 대한 매개 변수로 지침을 추가하는 방법을 알아봅니다.
feature: Brand Personalization, Product Personalization, Persona Personalization, Variant Generation, Generative AI
role: User
level: Beginner
exl-id: cb893b5d-b535-42f6-8dd8-8bd779d80a4f
source-git-commit: a4df9c81339a8fe5197200d58abc8b48df59da6f
workflow-type: tm+mt
source-wordcount: '2476'
ht-degree: 0%

---

# 지침 추가

GenStudio for Performance Marketing을 사용하면 모든 AI 생성 콘텐츠를 브랜드 정체성에 맞게 사용자 정의하는 사용자 정의 지침을 설정할 수 있습니다. 이 페이지에서는 사용 가능한 각 지침을 설정하고 사용하는 지침을 제공합니다. 일반적인 설명은 [지침 개요](/help/user-guide/guidelines/overview.md)를 참조하십시오.

GenStudio for Performance Marketing에 지침을 추가하는 것은 작성 프로세스의 중요한 단계입니다. 가이드라인은 사용자 정의 프롬프트, [접근성 및 콘텐츠 검사](overview.md#compliance) 및 Adobe 생성 AI 기술과 함께 콘텐츠 만들기 프로세스를 알려 효과적인 자산을 제작합니다.

지침은 사용자 정의이거나 [기본 [!DNL Brand] 채널 지침](/help/user-guide/guidelines/brands.md#default-channel-guidelines)과 같이 기본 지침으로 존재할 수 있습니다.

미리 정의된 채널 지침([!DNL Brands], [!DNL Personas] 또는 [!DNL Products] 등)이 있는 템플릿에서 변형을 만들 때 이러한 지침은 변형에 적용됩니다. 원하는 경우 변경할 수 있습니다.

{{in-academy}}

## 브랜드 추가

[!DNL Brand]을(를) 추가하려면 지침을 선택하고 브랜드 세부 정보를 입력하여 [브랜드 가이드를 업로드](#upload-a-brand)하거나 [수동으로 브랜드 만들기](#manually-add-brand)하십시오. [향후 콘텐츠 생성에서 사용할 수 있도록  [!DNL Brand]](#publish-brand)을(를) [!DNL Content]에 게시합니다.

왼쪽 탐색 영역에서 **[!DNL Brands]**&#x200B;공유&#x200B;_목록에서_&#x200B;을(를) 클릭합니다.

GenStudio for Performance Marketing의 ![지침](/help/assets/guidelines.png){width="650" zoomable="yes"}

영어가 아닌 언어로 작성된 브랜드 지침을 업로드하거나 영어가 아닌 언어를 사용하여 브랜드를 수동으로 생성하는 경우 GenStudio for Performance Marketing은 해당 지침을 동일한 언어로 표시합니다.

>[!TIP]
>
>각 브랜드는 계층적인 관계 없이 독립적으로 운영됩니다. 상위 브랜드에서 하위 브랜드를 만들려면 만들기 프로세스 중에 상위 브랜드의 정보를 포함하십시오.

### 브랜드 업로드

최대 3개의 PDF 또는 DOC 파일 등 고유한 브랜드 가이드라인 문서를 GenStudio for Performance Marketing에 업로드하여 자동으로 브랜드를 생성할 수 있습니다.

[[!DNL Brands]](/help/user-guide/guidelines/brands.md)을(를) 참조하십시오.

**브랜드 문서를 업로드하려면**:

1. _[!DNL Brands]_&#x200B;패널에서&#x200B;**[!UICONTROL 브랜드 추가]**&#x200B;단추를 선택합니다.
1. **[!UICONTROL PDF 업로드]**&#x200B;를 선택하고 _브랜드를 추가하는 방법 선택_ 팝업에 브랜드 이름을 입력하십시오.
1. **[!UICONTROL 계속]**&#x200B;을 선택합니다.
1. 브랜드 가이드라인 문서를 검색하여 첨부하거나 드래그하여 _[!UICONTROL 브랜드 추가]_ 팝업에 추가하십시오.

   최대 5개의 PDF 파일을 최대 500MB에 첨부할 수 있습니다.

1. **[!UICONTROL 브랜드 추가]**&#x200B;를 선택합니다.

   GenStudio for Performance Marketing은 Adobe의 생성 AI 기술을 사용하여 업로드한 문서에서 정보를 추출하고 브랜드 구축을 시작합니다. 브랜드 문서의 각 지침이 조립될 때 브랜드 음성, 채널 및 이미지 지침과 같은 브랜드 정보가 채워지는 것을 볼 수 있습니다.

문서에서 추출된 브랜드 가이드라인 세부 정보를 표시하는 새 브랜드 보기가 열립니다. 팝업은 _에게 &quot;내 브랜드가 검토할 준비가 되었습니다&quot;_&#x200B;을(를) 알리는 메시지를 보내고, 추출된 콘텐츠를 검토하고 필요한 편집을 수행하도록 알려줍니다.

### 수동으로 브랜드 추가

기존 브랜드 문서를 업로드하는 대신 수동으로 브랜드 세부 정보를 추가하여 새 [브랜드](brands.md)을(를) 채울 수 있습니다.

**브랜드를 수동으로 추가하려면**:

1. **[!UICONTROL 브랜드 추가]** 단추를 선택합니다.
1. **[!UICONTROL 수동으로 업로드]**&#x200B;를 선택하고 _브랜드를 추가하는 방법 선택_ 팝업에 브랜드 이름을 입력하십시오.
1. **[!UICONTROL 브랜드 추가]**&#x200B;를 선택합니다.

   새 빈 브랜드가 생성되고 표시됩니다.

1. 다양한 브랜드 정보, 지침 및 이미지를 채워 적절한 섹션(맨 위의 탭 보기)에서 브랜드를 빌드합니다.

   새 브랜드의 홈 페이지 보기 _또는_&#x200B;에서 바로 지침을 추가할 수 있습니다. 맨 위의 개별 탭 섹션(유용한 _예제 보기_ 도구 설명 포함)에서 지침을 추가할 수 있습니다.

   ![브랜드](/help/assets/brands.png){width="600" zoomable="yes"}

   - _이 브랜드를 사용하는 시기_: **[!UICONTROL 추가]**&#x200B;를 클릭하고(또는 텍스트 필드를 클릭하여 기존 텍스트를 변경) 브랜드에 대한 개요 및 사용 정보를 입력하십시오. **[!UICONTROL 변경 내용 저장]**&#x200B;을 클릭합니다.
   - [_[!DNL Brand] 음성 지침&#x200B;_](brands.md#brand-voice-guidelines): 각 지침 필드에 적용 가능한 정보를 추가합니다.

     ![[!DNL Brand] 음성 지침 추가 &#x200B;](/help/assets/brand-voice-add.png){width="500" zoomable="yes"}

   - [_이미지 지침_](brands.md#image-guidelines): &quot;일반 미술 지침&quot; 또는 &quot;제품 사진&quot; 등의 지침 범주를 추가하려면 **[!UICONTROL 범주 추가]**&#x200B;를 클릭하십시오. 추가된 각 카테고리에 지침을 입력합니다.
   - [_채널 지침_](brands.md#channel-guidelines): 사용 가능한 각 채널을 클릭하고 적절한 지침을 추가하십시오.
   - [_로고_](brands.md#logos): 로고를 드래그 앤 드롭하거나 찾아보고 업로드하려면 **[!UICONTROL 로고 추가]**&#x200B;를 클릭하십시오.
   - [_색상_](brands.md#colors): 16진수 또는 RGB 색상 코드를 사용하거나 색상 선택기를 사용하여 개별 색상을 추가하려면 **[!UICONTROL 색상 추가]**&#x200B;를 클릭합니다.

     ![브랜드 색상](/help/assets/colors.png){width="600" zoomable="yes"}

만든 [!DNL Brands]을(를) 보려면 _[!UICONTROL 브랜드]_ 패널 상단 근처에 있는 뒤로 화살표를 클릭하여 _[!UICONTROL 브랜드]_ 홈으로 다시 이동합니다.

정보에 액세스할 수 있도록 [을(를) &#x200B;](#publish-brand)게시[!DNL Brand]하지 않아도 됩니다. 수동으로 추가된 모든 정보는 추가된 후 즉시 사용할 수 있습니다. 조직의 다른 사용자가 GenStudio for Performance Marketing의 [!DNL Brand] 정보를 사용하려면 게시해야 합니다. 만든 [!DNL Brand]은(는) 게시될 때까지 초안 양식에서 사용할 수 있습니다.

### 브랜드 썸네일 변경

[!DNL Brand]을(를) 수동으로 추가한 후 썸네일 이미지를 변경하여 [!DNL Brands] 목록 내에서 쉽게 구분할 수 있도록 할 수 있습니다.

수동으로 추가하는 대신 문서 추출을 사용하여 [!DNL Brand]을(를) 만들면 해당 문서 내에서 사용 가능한 로고가 자동으로 썸네일 이미지로 구현됩니다.

**[!DNL Brand]**&#x200B;에 대한 썸네일 이미지를 수동으로 변경합니다.

1. 작업 메뉴에서 **[!UICONTROL 썸네일 변경]**&#x200B;을 선택합니다.
1. _업로드_ 탭에서 새 이미지를 업로드합니다.
1. _[!UICONTROL 썸네일 변경]_&#x200B;에서 업로드된 이미지를 변경합니다.
1. **[!UICONTROL 업데이트]**&#x200B;를 선택하여 이미지를 [!DNL Brand] 썸네일 이미지로 저장합니다.

[!DNL Brand]에 대한 [!UICONTROL 로고] 탭 보기에서 기존 [!DNL Brand] 로고를 선택할 수 있습니다. 로고를 열려면 클릭하고 작업 메뉴에서 **[!UICONTROL 브랜드 썸네일로 사용]**&#x200B;을 선택합니다.

### 브랜드 게시

[!DNL Brand] 초안을 게시하기 전에 모든 지침 섹션을 클릭하여 채워진 모든 정보를 검토하십시오. 필요에 따라 브랜드 지침을 변경합니다.

_[!DNL Brands]_&#x200B;에서 초안 또는 게시된 [!DNL Brands]은(는) 타일로 표시됩니다. 상태 배지(_&#x200B;게시됨&#x200B;_또는_&#x200B;초안&#x200B;_)와 마지막으로 브랜드를 수정한 시간이 각 타일 하단에 표시됩니다.

>[!TIP]
>
>만든 브랜드만 보려면 **[!UICONTROL 필터(funnel 아이콘)에서]**&#x200B;사용자가 만든 [!DNL Brands]을(를) 선택하십시오.

**브랜드 초안 게시**:

1. 왼쪽 탐색 영역에서 **[!UICONTROL [!DNL Brands]]**&#x200B;을(를) 클릭합니다.
1. 기존 [!DNL Brand] 초안을 열려면 썸네일 타일을 클릭하십시오.
1. **[!UICONTROL 게시]** 단추를 클릭합니다(초안에만 사용 가능).
1. _브랜드 게시_ 팝업에서 게시된 [!DNL Brand]을(를) 보고 사용할 수 있는 액세스 권한이 있는지 확인하십시오.
1. 표시되는 _브랜드 게시_ 팝업에서 **[!UICONTROL 게시]**&#x200B;를 선택합니다.

   팝업에서 [!DNL brand]이(가) 게시되었음을 확인합니다.—&quot;{Brand}이(가) 이제 준비되었습니다.&quot;

1. 팝업을 종료하려면 **[!UICONTROL 완료]**&#x200B;를 클릭하세요.

[!DNL brand]에는 녹색 점과 이름 옆에 &quot;게시됨&quot;이 표시되며 **[!UICONTROL 게시[!DNL brand]]** 단추 대신 **&#x200B;**&#x200B;편집 단추가 나타납니다.

**게시된[!DNL brand]**&#x200B;의 게시를 취소하려면 브랜드를 클릭하여 연 다음, 작업 메뉴에서 **[!UICONTROL 게시 취소]**&#x200B;를 클릭하십시오(세 점 아이콘).

이제 게시된 브랜드를 [_[!DNL Create]_](/help/user-guide/create/overview.md) 및 [_[!DNL Content]_](/help/user-guide/content/overview.md)에서 사용할 수 있습니다.

### 브랜드 관리

_[!DNL Brands]_&#x200B;홈에서 이미 만든 브랜드를 관리하거나 게시하기 위해 클릭하여 열 수 있습니다.

**브랜드 정보를 보려면** 왼쪽 탐색 영역에서 **[!UICONTROL [!DNL Brands]]**&#x200B;을(를) 클릭하고 클릭하여 기존 브랜드를 엽니다.

**보기에서**&#x200B;브랜드를 수정하려면[!DNL Brands]:

1. **[!DNL Brands]**&#x200B;에서 을(를) 클릭하여 정의된 브랜드를 엽니다.
1. 개별 세부 정보를 보거나 지침을 수정하려면 맨 위에서 [**[!UICONTROL 브랜드 음성 지침]**](brands.md#brand-voice-guidelines), [**[!UICONTROL 이미지 지침]**](brands.md#image-guidelines), [**[!UICONTROL 채널 지침]**](brands.md#channel-guidelines), [**[!UICONTROL 로고]**](brands.md#logos) 또는 [**[!DNL Colors]**](brands.md#colors)을(를) 클릭합니다.
1. 브랜드 로고를 관리하려면 상단의 [**[!UICONTROL 로고]**](brands.md#logos)를 클릭하고 작업 메뉴(세 점)를 클릭하십시오.
   1. **[!UICONTROL 세부 정보 보기]**&#x200B;를 선택하여 [!DNL Brand]형식&#x200B;_및_&#x200B;크기&#x200B;_와 같은_&#x200B;에 대한 정보를 봅니다.
   1. 로고를 다운로드하려면 **[!UICONTROL 다운로드]**&#x200B;를 선택하십시오.
   1. 로고를 썸네일 이미지로 설정하려면 [**[!UICONTROL 브랜드 썸네일로 사용]](#change-brand-thumbnail)을(를) 선택하십시오.
   1. 로고 이름을 변경하려면 **[!UICONTROL 이름 바꾸기]**&#x200B;를 선택하십시오.
   1. 로고를 삭제하려면 **[!UICONTROL 삭제]**&#x200B;를 선택하십시오.
1. 기존 브랜드의 이름을 바꾸려면 제목을 클릭하고 새 제목을 입력합니다.
1. 기존 브랜드를 복제하려면 **[!UICONTROL 작업 메뉴에서]**&#x200B;복제&#x200B;_[!DNL Brands]_&#x200B;를 선택하십시오.
   1. _중복 브랜드_ 팝업에 브랜드 이름을 입력하고 **[!UICONTROL 중복 브랜드]**&#x200B;을 클릭합니다.

      팝업에서 브랜드가 중복됨을 확인합니다.—&quot;새 브랜드가 생성됨&quot;. 복제된 브랜드는 처음에 _게시 취소_ 모드에 있습니다.

   1. 복제된 브랜드를 사용자 지정한 다음 [게시](#publish-brand)하여 사용할 수 있도록 합니다.
1. 브랜드를 삭제하려면 **[!UICONTROL 동작 메뉴에서]**&#x200B;삭제[!DNL Brands]를 선택하십시오.

## [!DNL Personas] 추가

담당자를 추가하려면 지침을 선택하고 담당자의 세부 정보를 입력하여 [담당자를 업로드](#upload-a-persona) 또는 [담당자를 수동으로 생성](#manually-add-persona)하십시오.

왼쪽 탐색 영역에서 **[!DNL Personas]**&#x200B;공유&#x200B;_목록에서_&#x200B;을(를) 클릭합니다.

GenStudio for Performance Marketing의 ![지침](/help/assets/guidelines.png){width="650" zoomable="yes"}

GenStudio for Performance Marketing에서 [!DNL Persona]을(를) 추가하여 만든 콘텐츠를 이상적인 대상자에게 타깃팅할 수 있습니다.

[[!DNL Personas]](personas.md)을(를) 참조하십시오.

### 사용자 업로드

자신의 성향 문서를 업로드하여 새 성향을 채울 수 있습니다.

[[!DNL Personas]](/help/user-guide/guidelines/personas.md)을(를) 참조하십시오.

1. _[!DNL Personas]_&#x200B;패널에서&#x200B;**[!UICONTROL 사용자 추가]**&#x200B;단추를 선택합니다.
1. **[!UICONTROL 파일 업로드]**&#x200B;를 선택하고 _사용자 추가 방법 선택_ 팝업에 사용자 이름을 입력하십시오.
1. **[!UICONTROL 계속]**&#x200B;을 선택합니다.
1. 사용자 가이드라인 문서를 검색하여 첨부하거나 _[!UICONTROL 사용자 추가]_ 팝업에 끌어 놓으십시오.

   최대 500MB에 최대 5개의 PDF 또는 DOC 파일을 첨부할 수 있습니다.

1. **[!UICONTROL 가상 사용자 추가]**&#x200B;를 선택합니다.

   GenStudio for Performance Marketing은 Adobe의 생성 AI 기술을 사용하여 업로드한 문서에서 정보를 추출하고 사용자를 빌드하기 시작합니다. 사용자 문서의 각 지침이 조립되면 사용자 음성, 채널 및 이미지 지침과 같은 세부 정보가 채워집니다.

   문서에서 추출한 성향 가이드라인 세부 정보를 표시하는 새 성향 보기가 열립니다. 팝업은 _에게 &quot;사용자가 &quot;_&quot;을(를) 검토할 준비가 되었음을 알려주고, 추출된 콘텐츠를 검토하고 필요한 편집을 수행하도록 알려 줍니다.

### 수동으로 사용자 추가

기존 사용자 문서를 업로드하는 대신 수동으로 사용자 세부 정보를 추가하여 새 [사용자](personas.md)를 채울 수 있습니다.

**사용자를 수동으로 추가하려면**:

1. **[!UICONTROL 사용자 추가]** 단추를 선택하고 **[!UICONTROL 수동으로 추가]**&#x200B;를 선택합니다.
1. **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

   다양한 선택적 지침 및 이미지를 채워 담당자를 구축할 수 있습니다.

1. **[!UICONTROL 새 사용자 이름]**&#x200B;을(를) 클릭하고 [!DNL Persona]의 이름을 입력하십시오.
1. [!DNL Persona]설명&#x200B;_섹션에_&#x200B;에 대한 정보를 추가하십시오.

   ![[!DNL Persona]](/help/assets/personas-add.png){width="650" zoomable="yes"} 추가

1. _설명_&#x200B;을(를) 클릭하고 이 [!DNL Persona]에 대한 설명을 입력하십시오.
1. _메시징 환경 설정_&#x200B;을 클릭하고 [!DNL Persona]에 대한 메시징 세부 정보를 입력하십시오.
1. 썸네일을 편집하려면 이미지 썸네일 위로 마우스를 이동하고 작업 메뉴에서 **[!UICONTROL 썸네일 편집]**&#x200B;을 선택합니다.
   1. _갤러리_ 탭의 갤러리에서 이미지를 선택하거나 _또는_ _업로드_ 탭에서 새 이미지를 업로드하십시오.

      _업로드_ 탭에서 기존 썸네일 이미지를 삭제하거나 자를 수도 있습니다.

   1. **[!UICONTROL 이미지 사용]**&#x200B;을 클릭합니다.
1. 표지 이미지를 편집하려면 표지 위로 마우스를 가져간 다음 작업 메뉴에서 **[!UICONTROL 표지 편집]**&#x200B;을 선택합니다.
   1. _갤러리_ 탭의 갤러리에서 이미지를 선택하거나 _또는_ _업로드_ 탭에서 새 이미지를 업로드하십시오.
   1. **[!UICONTROL 이미지 사용]**&#x200B;을 클릭합니다.
   1. 표지 이미지의 위치를 변경하려면 동작 메뉴에서 **[!UICONTROL 위치 변경]**&#x200B;을 클릭하고 이미지를 원하는 위치로 드래그한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   만든 [!DNL Personas]을(를) 보려면 _성향_ 보기 상단 근처에 있는 뒤로 화살표를 클릭하여 _[!DNL Personas]_&#x200B;홈으로 다시 이동합니다.

### [!DNL Personas] 관리

_[!DNL Personas]_&#x200B;홈에서 이미 만든&#x200B;**을(를) [!DNL Persona]**&#x200B;열어 편집하거나 검토하거나&#x200B;**담당자를**&#x200B;목록에서 삭제할 수 있습니다.

- 기존 담당자를 수정하고 검토하려면 **[!UICONTROL 작업 메뉴에서]**&#x200B;열기[!DNL Personas]를 선택하십시오.
- **[!UICONTROL 동작 메뉴에서]**&#x200B;삭제[!DNL Personas]를 선택하여 담당자를 **삭제**&#x200B;합니다.
- **[!UICONTROL 동작 메뉴에서]**&#x200B;이름 바꾸기[!DNL Personas]를 선택하여 담당자로 **이름 바꾸기**&#x200B;합니다.

## [!DNL Products] 추가

제품을 추가하려면 다음 작업을 수행하십시오.

1. 왼쪽 탐색 영역에서 **[!DNL Products]**&#x200B;공유&#x200B;_목록에서_을(를) 클릭합니다.
   GenStudio for Performance Marketing의 ![지침](/help/assets/guidelines.png){width="650" zoomable="yes"}
1. _[!DNL Products]_&#x200B;패널에서&#x200B;**제품 추가**&#x200B;를 선택합니다.
1. 지침을 선택하고 제품 세부 정보를 입력하여 [제품을 업로드](#upload-a-product)하거나 [제품을 수동으로 생성](#manually-add-product)하도록 선택합니다.

![[!DNL Product]](/help/assets/products-add.png){width="650" zoomable="yes"} 추가

GenStudio for Performance Marketing에 [!DNL Product]을(를) 포함하면 특정 제품에 대해 만든 콘텐츠를 더 잘 조정할 수 있습니다.

[[!DNL Products]](products.md)을(를) 참조하십시오.

### 제품 업로드

고유한 제품 문서를 업로드하여 새 제품을 채울 수 있습니다.

[[!DNL Products]](/help/user-guide/guidelines/products.md)을(를) 참조하십시오.

1. **[!UICONTROL 제품 추가]** 단추를 선택합니다.
1. **[!UICONTROL 파일 업로드]**&#x200B;를 선택하고 _제품 추가 방법 선택_ 팝업에 제품 이름을 입력하십시오.
1. **[!UICONTROL 계속]**&#x200B;을 선택합니다.
1. 제품 지침 문서를 검색하여 첨부하거나 _[!UICONTROL 제품 추가]_ 팝업에 끌어 놓으십시오.

   최대 500MB에 최대 5개의 PDF 또는 DOC 파일을 첨부할 수 있습니다.

1. **[!UICONTROL 제품 추가]**&#x200B;를 선택합니다.

   GenStudio for Performance Marketing은 Adobe의 생성 AI 기술을 사용하여 업로드한 문서를 분석하여 제품 프로필을 구성합니다. 제품 문서의 각 지침이 처리되면 제품 설명, 값 제안 및 메시징 환경 설정과 같은 정보가 채워집니다.

   문서에서 추출한 제품 지침 세부 사항을 보여 주는 새 제품 보기가 열립니다. 팝업은 _에게 &quot;제품을 검토할 준비가 되었습니다&quot;_&#x200B;을(를) 알리는 메시지를 보내고, 추출된 콘텐츠를 검토하고 필요한 편집을 수행하도록 알려 줍니다.

### 수동으로 제품 추가

기존 제품 문서를 업로드하는 대신 수동으로 제품 세부 정보를 추가하여 새 [제품](products.md)을 채울 수 있습니다.

**제품을 수동으로 추가하려면**:

1. **[!UICONTROL 제품 추가]** 단추를 선택하고 **[!UICONTROL 수동으로 추가]**&#x200B;를 선택합니다.
1. **[!UICONTROL 계속]**&#x200B;을 클릭합니다.

   다양한 선택 정보를 채워 제품을 빌드할 수 있습니다.

1. **[!UICONTROL 새 제품 이름]**&#x200B;을 클릭하고 [!DNL product]의 이름을 입력하십시오.
1. [!DNL product]설명&#x200B;_섹션에_&#x200B;에 대한 정보를 추가하십시오.
1. _설명_&#x200B;을(를) 클릭하고 이 [!DNL Product]에 대한 설명을 입력하십시오.
1. _가치 제안_&#x200B;을(를) 클릭하고 가치 제안 세부 정보를 입력하여 [!DNL Product]을(를) 올바르게 배치하십시오.
1. _메시징 환경 설정_&#x200B;을 클릭하고 [!DNL product]에 대한 메시징 세부 정보를 입력하십시오.
1. 썸네일을 편집하려면 이미지 썸네일 위로 마우스를 이동하고 작업 메뉴에서 **[!UICONTROL 썸네일 편집]**&#x200B;을 선택합니다.
   1. _갤러리_ 탭의 갤러리에서 이미지를 선택하거나 _또는_ _업로드_ 탭에서 새 이미지를 업로드하십시오.

      _업로드_ 탭에서 기존 썸네일 이미지를 삭제하거나 자를 수도 있습니다.

   1. **[!UICONTROL 이미지 사용]**&#x200B;을 클릭합니다.
   1. 표지 이미지를 편집하려면 표지 위로 마우스를 가져간 다음 작업 메뉴에서 **[!UICONTROL 표지 편집]**&#x200B;을 선택합니다.
   1. _갤러리_ 탭의 갤러리에서 이미지를 선택하거나 _또는_ _업로드_ 탭에서 새 이미지를 업로드하십시오.
   1. **[!UICONTROL 이미지 사용]**&#x200B;을 클릭합니다.
   1. 표지 이미지의 위치를 변경하려면 동작 메뉴에서 **[!UICONTROL 위치 변경]**&#x200B;을 클릭하고 이미지를 원하는 위치로 드래그한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   만든 [!DNL Products]을(를) 보려면 _제품_ 보기 상단 근처에 있는 뒤로 화살표를 클릭하여 _[!DNL Products]_&#x200B;홈으로 다시 이동합니다.

### [!DNL Products] 관리

_[!DNL Products]_&#x200B;홈에서 이미 만든&#x200B;**을(를) [!DNL Product]**&#x200B;열어 편집하거나 검토하거나 목록에서&#x200B;**제품을 삭제**&#x200B;할 수 있습니다.

- 기존 제품을 수정하고 검토하려면 **[!UICONTROL 작업 메뉴에서]**&#x200B;열기[!DNL Products]를 선택하십시오.
- **[!UICONTROL 동작 메뉴에서]**&#x200B;삭제[!DNL Products]를 선택하여 제품을 **삭제**&#x200B;합니다.
- **[!UICONTROL 동작 메뉴에서]**&#x200B;이름 바꾸기[!DNL Products]를 선택하여 제품을 **이름 바꾸기**&#x200B;합니다.

## [!DNL Audiences] 추가

>[!NOTE]
>
>[!DNL Audiences] 기능을 사용하려면 Adobe 팀이 GenStudio에 온보딩해야 합니다. _[!DNL Audiences]_&#x200B;이(가) 템플릿 매개 변수에 나타나지 않으면 Adobe 담당자에게 문의하십시오.

[!DNL Audiences]은(는) Adobe Real-Time Customer Data Platform(RTCDP)의 타깃팅된 고객 세그먼트를 제공하여 정확한 타깃팅 데이터를 콘텐츠 생성 워크플로우로 가져옵니다. GenStudio for Performance Marketing은 대상 정의를 활용하여 특정 고객 세그먼트에 맞게 맞춤화된 마케팅 콘텐츠를 만들 수 있도록 지원합니다.

[!DNL Audiences]이(가) [_[!DNL Create]_&#x200B;워크플로](../create/overview.md#templates)의 매개 변수 창에 드롭다운으로 나타납니다._[!DNL Audiences]_&#x200B;은(는) 두 지침을 모두 사용할 때 _[!DNL Personas]_&#x200B;에 특이성을 추가할 수 있지만 독립적으로 효과적으로 사용할 수도 있습니다.

온보딩 중에 대상자 정의를 가져와 GenStudio 호환 형식으로 변환합니다. 이 프로세스는 일반적으로 완료하는 데 며칠이 걸립니다. 시작하려면 Adobe 팀에 문의하십시오.

**필수 구성 요소**:

- Adobe Real-Time Customer Data Platform에 대한 조직 액세스
- 기존 대상자가 RTCDP 샌드박스에 이미 구성됨
- _[!DNL Audience]_&#x200B;통합에는 Adobe 팀에서 수동 온보딩 프로세스를 수행해야 합니다

**대상자를 선택하려면**:

1. [_[!DNL Create]_&#x200B;워크플로](../create/overview.md#templates)에서 템플릿을 선택하고&#x200B;**[!UICONTROL 사용]**&#x200B;단추를 클릭하여 초안을 엽니다.
1. 매개 변수 목록에서 _[!UICONTROL 대상]_ 드롭다운을 클릭하여 사용 가능한 모든 대상을 봅니다.
   ![성향 매개 변수 창의 대상 드롭다운](./audience-dropdown.png){width=450}
1. 목록에서 할당할 대상자를 선택합니다. [!DNL Persona]을(를) 선택한 경우 선택한 [!DNL Persona]과(와) 일치하는 권장 대상이 표시됩니다.
1. 선택한 대상자에 대해 생성된 확장된 설명 및 메시징 환경 설정을 보려면 **[!UICONTROL 대상자 세부 정보 보기]**&#x200B;를 클릭하십시오. 대상 세부 사항은 콘텐츠 생성을 알려주며, 크리에이티브가 대상 세그먼트의 특정 특성 및 선호도에 맞게 조정되도록 합니다.
   ![대상 세부 정보 창](./audience-details.png){width=450}
