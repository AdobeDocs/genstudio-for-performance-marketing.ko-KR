---
title: 템플릿 코드 편집기
description: GenStudio for Performance Marketing에서 템플릿 코드 편집기를 사용하는 방법에 대해 알아봅니다.
level: Intermediate
feature: Templates, Content
source-git-commit: 96ed2b3e1a1d854b35bdddb5aa694fdfec727e1a
workflow-type: tm+mt
source-wordcount: '311'
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
