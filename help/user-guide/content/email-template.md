---
title: Adobe GenStudio for Performance Marketing용 이메일 템플릿 준비
description: Adobe GenStudio for Performance Marketing용 사용자 지정 이메일 템플릿을 구축하는 방법을 알아봅니다.
level: Intermediate
feature: Templates, Content
exl-id: 8b1e8d32-5a23-45ce-a2d4-ae6de3698c45
source-git-commit: 478815d74a742cdc05d3f1faebf27d5adc04d417
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Adobe GenStudio for Performance Marketing용 이메일 템플릿 준비

일반적으로 디자이너는 Adobe XD과 같은 디자인 프로그램에서 템플릿의 시각적 디자인을 만듭니다. 이메일 템플릿을 디자인하고 코딩하고 테스트한 후 GenStudio for Performance Marketing에서 업로드하고 사용할 수 있도록 준비할 수 있습니다.

[템플릿 요소](use-templates.md#template-elements)를 참조하십시오.

## 지침 추가

메타 광고 템플릿을 준비하기 전에 GenStudio for Performance Marketing에 [지침](/help/user-guide/guidelines/overview.md)을(를) 추가하고 관련 브랜드에 대한 포괄적인 정보로 채워졌는지 확인하십시오. [브랜드 지침](/help/user-guide/guidelines/brands.md)은(는) 생성된 콘텐츠에 직접 영향을 줍니다.

**예**: 전자 메일 템플릿의 본문을 500자 이하로 줄이려면 &quot;본문&quot; 필드에 대한 [채널 지침](/help/user-guide/guidelines/brands.md#channel-guidelines)에 해당 요구 사항을 추가하십시오.

GenStudio for Performance Marketing에 지침이 추가되지 않으면 기본값이 사용됩니다.

## 이메일 템플릿 코드 작성

템플릿이 디자인되면 HTML 및 인라인 CSS를 사용하여 코딩됩니다. 코드가 깨끗해야 하고 다양한 장치에 대해 반응해야 합니다.

[템플릿 예제](/help/user-guide/content/customize-template.md#template-examples)를 참조하십시오.

### 여러 섹션 이메일

콘텐츠를 생성하는 동안 [구조화된 프롬프트](/help/user-guide/effective-prompts.md#structured-prompts)를 사용하여 GenStudio for Performance Marketing에서 전자 메일의 섹션별로 다양한 콘텐츠를 생성하도록 지시할 수 있습니다.

예를 들어 전자 메일 템플릿의 섹션에 `Pod`—`Pod1` 및 `Pod2`이(가) 접두사로 추가된 경우 콘텐츠 생성을 위한 구조화된 프롬프트에 해당 전자 메일 섹션에 대한 특정 지시문이 포함될 수 있습니다. GenStudio for Performance Marketing은 프롬프트의 섹션별 지시문을 관련 이메일 섹션에 일치시키고 지시문에 정렬된 콘텐츠를 생성합니다.

[구조화된 프롬프트](/help/user-guide/effective-prompts.md#structured-prompts)를 참조하십시오.

## 이메일 템플릿 테스트

이메일 게재 또는 증명 플랫폼을 사용하여 이메일을 테스트하고 다양한 이메일 클라이언트 및 디바이스에서 제대로 렌더링되는지 확인합니다.

이메일 템플릿이 다음을 충족하는지 테스트합니다.

* 레이아웃은 CSS 미디어 쿼리를 사용하여 다양한 화면 크기에 맞게 조정됩니다
* 단추를 클릭하여 원하는 위치로 이동합니다.
* 이메일 템플릿을 모바일 디바이스에서 읽고 사용할 수 있습니다.

## 생성된 콘텐츠 영역 정의

이메일 템플릿에서 GenStudio for Performance Marketing의 콘텐츠로 동적으로 채워야 하는 영역을 정의합니다.

생성된 콘텐츠 영역을 정의하려면

* 헤드라인이나 CTA과 같이 GenStudio for Performance Marketing이 자동으로 생성해야 하는 템플릿의 텍스트 요소를 식별합니다.
* Handlebars 구문을 사용하여 자리 표시자를 삽입하여 HTML 템플릿을 조정합니다.

[콘텐츠 자리 표시자](/help/user-guide/content/customize-template.md#content-placeholders)를 참조하십시오.

## 템플릿 미리 보기

기본 제공 도우미를 통해 특정 콘텐츠 영역의 가시성을 제어합니다. 예를 들어 깔끔한 미리 보기 링크를 유지하면서 내보낸 템플릿의 링크에 대한 추적 매개 변수를 포함할 수 있습니다.

[템플릿 미리 보기](/help/user-guide/content/customize-template.md#template-preview)를 참조하세요.

## 템플릿 업로드 및 사용

템플릿을 디자인하고 코딩하고 테스트하고 미리 본 후에 GenStudio for Performance Marketing에 업로드하여 새로운 마케팅 콘텐츠를 생성하는 데 사용할 수 있습니다.

[템플릿 작업](use-templates.md)을 참조하세요.
