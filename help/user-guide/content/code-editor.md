---
title: 템플릿 코드 편집기
description: GenStudio for Performance Marketing에서 템플릿 코드 편집기를 사용하는 방법에 대해 알아봅니다.
level: Intermediate
role: Developer
feature: Media Templates, Content Generation
exl-id: b46fc7a9-88c1-474a-9d7b-1df7740d8f5a
source-git-commit: 3739a218ce67749d0038059e3504ab9a4df8f065
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# 템플릿 코드 편집기

템플릿 코드 편집기는 GenStudio for Performance Marketing을 사용하여 새로운 경험을 생성할 때 최적의 사용을 위해 템플릿을 확인하고 구체화하는 데 도움이 되도록 설계되었습니다. 편집기는 템플릿 내의 자리 표시자를 사용하여 GenStudio for Performance Marketing에서 자동으로 콘텐츠를 생성하는 위치를 나타내는 Handlebars 구문을 지원합니다.

>[!TIP]
>
>[!DNL Content] _템플릿_ 보기에서 템플릿 HTML 코드를 업로드하기 전에 [템플릿 사용자 지정](customize-template.md) 지침에 정의된 콘텐츠 자리 표시자를 삽입하여 템플릿을 준비합니다.

## 검색된 필드 확인

_[!UICONTROL 검색된 필드 확인]_ 창에는 GenStudio for Performance Marketing이 템플릿에서 인식하는 필드 목록이 표시됩니다. 목록을 검토하면 HTML 코드를 스크롤하여 템플릿 구성을 살펴볼 수 있습니다.

![코드 편집기 보기](/help/assets/template-detected-fields.png "검색된 필드 확인"){width="600" zoomable="yes"}

목록에서 필드가 누락된 것을 확인한 경우 템플릿 코드를 검색하고 누락된 필드의 위치를 찾습니다. Handlebars 구문과 [인식된 필드 이름](/help/user-guide/content/customize-template.md#recognized-field-names)을 사용하여 올바른 자리 표시자를 삽입합니다. 코드 편집기 하단에 나타나는 찾기 및 바꾸기 양식을 사용하여 코드의 특정 문자열을 검색합니다. (Windows `CTRL`+`F` 또는 macOS `CMD`+`F`)

### 수정하기

템플릿에 오류가 있으면 문제에 대한 간단한 설명이 포함된 `Template is invalid` 메시지가 표시될 수 있습니다. 다음 예제에서는 `_image` 필드가 다중 Pod 템플릿에 설정된 필드 명명 규칙을 준수하지 않음을 나타냅니다. 이 메시지는 필드 이름을 올바른 접두사로 업데이트해야 한다는 것을 추가로 알려 줍니다. 템플릿 코드 편집기에서 `_image` 필드를 찾은 다음 필요에 따라 이름을 업데이트합니다.

![잘못된 템플릿 수정](/help/assets/animation/template-code-editor.gif){width="600" zoomable="yes"}

_[!UICONTROL 검색된 필드 확인]_ 창이 업데이트되어 변경 내용을 반영합니다. 필드가 올바르고 완료되면 **[!UICONTROL 다음]**&#x200B;을 클릭하여 [템플릿 업로드](/help/user-guide/content/use-templates.md#add-a-template)를 계속하십시오.

## 일반적인 템플릿 문제 및 솔루션

| **오류** | **설명** | **솔루션** |
|-----------------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 구문 분석 실패 | 템플릿 콘텐츠를 유효한 Handlebars로 구문 분석할 수 없습니다. | 템플릿에 HTML 및 Handlebars 구문 오류가 있는지 확인하고 수정하여 [콘텐츠 자리 표시자](/help/user-guide/content/customize-template.md#content-placeholders)의 형식이 유효한지 확인하십시오. |
| 그룹이 할당되지 않음 | 다중 그룹 이메일 템플릿의 이미지 필드가 그룹에 할당되지 않았습니다. | 섹션 접두어의 일관된 사용을 확인합니다. 각 [섹션](/help/user-guide/content/customize-template.md#sections-or-groups)은(는) 각 필드 형식(`headline`, `body`, `image` `cta`) 중 하나만 사용할 수 있습니다. `image` 필드를 템플릿의 올바른 그룹에 할당하십시오. |
| 이미지 누락 | 필수 이미지 필드가 누락되었습니다. | 메타, 디스플레이 또는 배너 광고와 같은 특정 템플릿 유형에는 정확히 하나의 `image` 필드가 필요합니다. 필요한 `image` 필드를 템플릿에 추가합니다. |
| 잘못된 단일 그룹 | 이메일 템플릿에 잘못된 그룹이 하나만 있습니다. | 기본 전자 메일 템플릿에 [섹션 또는 그룹](/help/user-guide/content/customize-template.md#sections-or-groups)에 정의된 그룹 명명 규칙이 필요하지 않은 단일 템플릿 요소 집합이 포함되어 있습니다. 그룹 이름 지정 구문을 제거하여 템플릿이 0개의 섹션을 갖도록 조정합니다. |
| 필드 없음 | 템플릿에 필드가 없습니다. | Handlebars 구문을 사용하여 [인식된 필드 이름](/help/user-guide/content/customize-template.md#recognized-field-names)을(를) 템플릿에 추가하십시오. 여기서 특정 유형의 콘텐츠를 생성하려면 GenStudio for Performance Marketing이 필요합니다. |
| 필수 속성 누락 | 일부 필수 메타데이터 속성이 누락되었습니다. | 각 템플릿 유형에는 채널 지침을 기반으로 하는 요구 사항과 제한 사항이 있습니다. 예를 들어 메타에는 종횡비가 필요하고 디스플레이 광고에는 치수가 필요합니다. [채널별 템플릿 지침을 따르세요](/help/user-guide/content/best-practices-for-templates.md#follow-channel-specific-template-guidelines). |
| 예약된 이름이 사용됨 | 금지되거나 예약된 필드 이름이 사용되고 있습니다. | `subject` 또는 `introductory_text`과(와) 같은 특정 [필드 이름](/help/user-guide/content/customize-template.md#recognized-field-names)은(는) 예약되어 있습니다. 예약되거나 금지된 이름을 사용하는 필드의 이름을 변경합니다. |
| 필드가 너무 많음 | 필드 수가 전역 제한인 20개를 초과합니다. | 합계가 20을 초과하지 않도록 불필요한 필드를 제거하십시오. |
| 그룹이 너무 많음 | 그룹 수가 채널의 허용 최대값을 초과합니다. | Meta, display 및 LinkedIn 템플릿은 여러 섹션을 허용하지 않습니다. 이메일을 사용하려면 두 개 또는 세 개의 섹션을 정의할 때 그룹 이름을 지정해야 합니다. [채널의 요구 사항](/help/user-guide/content/best-practices-for-templates.md#follow-channel-specific-template-guidelines)을 충족하도록 템플릿의 그룹 수를 줄이십시오. |
| 지원되지 않는 필드 | 템플릿에서 채널이 지원하지 않는 필드를 사용하고 있습니다. | [인식된 필드 이름](/help/user-guide/content/customize-template.md#recognized-field-names)에 따라 지원되지 않는 필드를 바꾸거나 제거합니다. |
