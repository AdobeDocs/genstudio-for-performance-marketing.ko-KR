---
title: 템플릿에 대한 우수 사례
description: Adobe GenStudio for Performance Marketing에서 템플릿을 사용할 때 모범 사례를 따르십시오.
feature: Templates, Content
last-substantial-update: 2024-12-09T00:00:00Z
source-git-commit: 7ba2ecfbdd6853934be5210685bf447848715d28
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 템플릿 사용 우수 사례

템플릿은 사전 구성된 레이아웃 및 디자인 요소를 포함하는 시작점을 제공하여 새 콘텐츠를 생성하는 데 필요한 시간과 노력을 크게 줄입니다.

GenStudio for Performance Marketing에서 템플릿을 사용할 때 다음 권장 사항을 사용하십시오.

1. [템플릿 요소](#know-about-template-elements)에 대해 알아보기
1. 콘텐츠의 효과적인 개인화를 위해 [채널 지침](#configure-channel-guidelines)을(를) 구성하십시오.
1. 최적의 환경을 위해 [접근성 표준](accessibility-for-templates.md)으로 디자인
1. [채널별 템플릿 지침 준수](#follow-channel-specific-template-guidelines)

>[!TIP]
>
>[템플릿 작업](use-templates.md)에서 기본 템플릿 요소 및 절차에 대해 자세히 알아보세요. 다음 캠페인에서 사용할 [템플릿 사용자 지정](customize-template.md)에 대해 자세히 알아봅니다.

## 템플릿 요소에 대해 알아보기

가장 좋은 방법은 템플릿의 부분을 숙지하는 것입니다. 각 템플릿 유형은 서로 다른 요소를 사용하여 채널별 콘텐츠 작성 구조를 만듭니다. 템플릿을 사용자 지정하려면 콘텐츠를 생성하는 데 GenStudio for Performance Marketing이 필요한 이러한 요소 대신 필드 이름을 사용하십시오.

[템플릿 요소](use-templates.md#template-elements)를 참조하십시오.

## 채널 지침 구성

GenStudio for Performance Marketing에서 템플릿을 사용하기 전에 각 브랜드에 대한 채널 지침을 구성합니다. 채널 지침은 템플릿을 사용할 때 생성되는 콘텐츠 유형에 직접 영향을 줍니다. 예를 들어 전자 메일 본문에 문자 제한을 설정할 수 있습니다.

![본문 사양](/help/assets/channel-email-body.png)

[채널 지침](/help/user-guide/guidelines/brands.md#channel-guidelines)을 참조하세요.

## 채널별 템플릿 지침 준수

각 채널의 레이아웃 및 시각적 요구 사항을 충족하는 템플릿을 빌드합니다. 최적의 성능과 호환성을 위해 각 템플릿 유형을 사용할 때는 다음 팁과 제한을 고려하십시오.

>[!BEGINTABS]

>[!TAB 이메일]

GenStudio for Performance Marketing에서 작동하도록 이메일 템플릿을 사용자 지정할 때 다음 디자인 모범 사례를 따르십시오.

- Adobe 또는 Google 글꼴 사용
- 깔끔하고 반응형 HTML 및 인라인 CSS 사용
- JavaScript을 사용하지 **않음**
- **not** 본문이나 컨테이너에서 고정 너비를 사용하지 않음
- 템플릿 크기를 크게 늘릴 수 있으므로 **not**&#x200B;에서 base64 인코딩을 사용하여 이미지를 만드십시오

**제약 조건**:

- [섹션](customize-template.md#sections-or-groups) 사용:
   - 기본 템플릿(한 섹션만 해당)은 단일 템플릿 요소 집합을 생성할 수 있습니다.
   - 복합 템플릿(여러 섹션)은 최대 3개의 템플릿 요소 집합을 생성할 수 있습니다.
- 템플릿에서 허용되는 최대 필드는 20개입니다.
- 최대 HTML 파일 크기는 102KB입니다.

**인식된 필드 이름**:

전자 메일의 경우 `subject` 필드가 자동으로 포함됩니다. 다음 필드에 콘텐츠 자리 표시자를 사용합니다.

- `pre_header`
- `headline`
- `body`
- `cta`
- `image`(콘텐츠에서 선택됨)
- `brand_logo`

템플릿에서 필드 이름을 사용하는 방법에 대한 자세한 내용은 [콘텐츠 자리 표시자](customize-template.md#content-placeholders)를 참조하십시오.

>[!TAB 메타데이터]

GenStudio for Performance Marketing에서 작동하도록 메타 광고 템플릿을 사용자 정의할 때 다음 디자인 모범 사례를 따르십시오.

- 열 레이아웃에 360픽셀 너비 사용
- 이미지에 최소 1080 x 1080 픽셀 해상도 사용
- **not**(이)가 상대 글꼴 크기를 사용하지 않음
- 뷰포트를 **정의하지 않음**
- JavaScript을 사용하지 **않음**
- CSS에서 HTML 요소를 재정의하지 **마십시오**
- 배경 이미지에 대해 다음 설정을 사용합니다.

  `background-image` CSS 클래스에 `object-fit: cover` 값 추가:

  ```css
  .background-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  ```

**제약 조건**:

- [섹션](customize-template.md#sections-or-groups) 사용:
   - 섹션은 하나만 사용할 수 있으며, 템플릿 요소의 단일 세트를 생성합니다.

**지원되는 종횡비**:

- 정사각형 1:1(1080 x 1080픽셀)
- 세로 4:5(1080 x 1350픽셀)
- 스토리 9:16 (1080 x 1920픽셀)

**인식된 필드 이름**:

메타 광고의 경우 `headline`, `body` 및 `CTA` 필드가 자동으로 생성됩니다. 다음 필드에 콘텐츠 자리 표시자를 사용합니다.

- `image`(콘텐츠에서 선택됨)
- `on-image-text`
- `brand_logo`

템플릿에서 필드 이름을 사용하는 방법에 대한 자세한 내용은 [콘텐츠 자리 표시자](customize-template.md#content-placeholders)를 참조하십시오.

>[!TAB 광고 표시]

GenStudio for Performance Marketing에서 작동하도록 디스플레이 광고 템플릿을 사용자 지정할 때 다음 디자인 모범 사례를 따르십시오.

- Adobe 또는 Google 글꼴 사용
- 슬림한 차원으로 잘 표시되는 에셋 준비
- **not**(이)가 포함된 배경 이미지 또는 인코딩된 배경 이미지를 사용하지 않음
- GenStudio for Performance Marketing 콘텐츠 저장소에 업로드된 배경 이미지(`image` 필드) 사용
- JavaScript을 사용하지 **않음**

**제약 조건**:

- [섹션](customize-template.md#sections-or-groups) 사용:
   - 섹션은 하나만 사용할 수 있으며, 템플릿 요소의 단일 세트를 생성합니다.

**지원되는 차원**:

- 세로: (픽셀)
   - 300 x 600
   - 160 x 600&#x200B;
- 가로: (픽셀)
   - 300 x 250
   - 728 x 90
   - 336 x 280
   - 320 x 50
   - 970 x 250&#x200B;

**인식된 필드 이름**:

다음 필드에 콘텐츠 자리 표시자를 사용합니다.

- `headline`
- `body`
- `cta`
- `image`(콘텐츠에서 선택됨)

템플릿에서 필드 이름을 사용하는 방법에 대한 자세한 내용은 [콘텐츠 자리 표시자](customize-template.md#content-placeholders)를 참조하십시오.

>[!ENDTABS]