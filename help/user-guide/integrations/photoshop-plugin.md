---
title: Adobe GenStudio for Performance Marketing용 Photoshop 플러그인
description: GenStudio for Performance Marketing용 Photoshop 플러그인을 설치, 구성 및 사용하는 방법에 대해 알아봅니다.
feature: Generative AI
role: User
source-git-commit: bb6b8de80bdf6089e70756bea5dbf3e6a7945052
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 1%

---

# GenStudio for Performance Marketing용 Photoshop 플러그인

GenStudio for Performance Marketing Photoshop 플러그인은 Adobe Photoshop에 패널을 추가하여 브랜드 내 콘텐츠를 생성할 수 있도록 합니다.

이 페이지에서는 플러그인을 설치하고 구성하는 방법과 사용 방법에 대해 설명합니다.

이 플러그인의 기능은 다음과 같습니다.

* Adobe ID을 사용하여 GenStudio for Performance Marketing 인스턴스에 로그인합니다
* GenStudio for Performance Marketing 컨텐츠 생성 필드를 Photoshop 문서의 텍스트 레이어에 매핑
* 콘텐츠를 생성하기 위한 브랜드, 제품, 사용자 및 텍스트 프롬프트 지정
* 원할 경우 템플릿 이미지를 대체할 이미지를 추가합니다
* 생성된 온브랜드 콘텐츠 변형 미리 보기
* 생성된 콘텐츠를 현재 문서의 매핑된 레이어에 적용
* 온브랜드 콘텐츠 번역 만들기
* 생성된 [!DNL Experiences]을(를) GenStudio for Performance Marketing으로 내보내기

>[!VIDEO](https://video.tv.adobe.com/v/3478808?learn=on)

## 플러그인 설치

다음 지침에 따라 플러그인을 설치합니다.

### 사전 요구 사항

* Creative Cloud 데스크탑 애플리케이션
* Photoshop, 최소 버전 25.6.0

### 설치 단계

1. Adobe Exchange의 Creative Cloud 마켓플레이스에서 플러그인을 다운로드하고 업데이트합니다.
1. Adobe Exchange에서 **Photoshop용 GenStudio 플러그인**&#x200B;을 검색합니다.
1. 화면의 지침에 따라 플러그인을 설치합니다.

### 플러그인 제거

1. Creative Cloud 데스크탑 애플리케이션을 시작합니다.
1. **[!UICONTROL 플러그인]** 옵션을 클릭합니다.
1. 옵션을 보려면 GenStudio for Creative Cloud 카드에서 줄임표 **[!UICONTROL (...)]**&#x200B;을(를) 클릭하십시오.
1. **제거**&#x200B;를 선택하십시오.

## 템플릿 만들기

콘텐츠를 생성하려면 Photoshop 문서에서 만든 GenStudio for Performance Marketing 템플릿이 필요합니다.

GenStudio 지원 템플릿을 만들려면 다음 작업을 수행하십시오.

1. Photoshop에서 문서를 엽니다.
1. 생성된 콘텐츠에 대한 텍스트 레이어를 식별합니다.
1. 필드 이름 규칙 형식 `{<name_of_generated_field>}`을(를) 사용하여 레이어 이름을 바꾸십시오. (예: `{body}`, `{headline}`, `{cta}`)
1. 템플릿 유형[에 필요한 채널에 필요한 모든 &#x200B;](../../user-guide/templates/customize-template.md#recognized-field-names)필드의 레이어 이름을 바꾸십시오.

| 채널 | 생성을 위한 필수 필드 | 생성을 위한 선택적 필드 |
| --- | --- | --- |
| LinkedIn | `{on_image_text}`, `{image}` | `{headline}`, `{introductory_text}`, `{cta}`, `{website_url}` |
| Meta | `{on_image_text}`, `{image}` | `{body}`, `{headline}`, `{cta}`, `{website_url}`, `{display_link}` |
| 디스플레이 | `{body}`, `{image}` | `{headline}`, `{cta}`, `{website_url}` |

여러 레이어가 동일한 필드 지정을 공유할 수 있지만 각 레이어는 하나의 필드만 지정할 수 있습니다. 예를 들어 문서에 여러 대지가 있는 경우:

* 각 대지에 `{headline}` 레이어를 지정할 수 있습니다.
* 하나의 대지에 여러 `{headline}`개의 레이어를 지정할 수 있습니다.
* 단일 레이어가 `{headline}` 및 `{cta}` 필드 이름을 모두 받도록 지정할 수 없습니다.

### 템플릿 크기 요구 사항

#### Meta 템플릿

Instagram 및 Facebook 게시물의 경우:

* 너비: 1080px(고정)
* 높이: 1080px 또는 1350px

Instagram 및 Facebook 스토리:

* 너비: 1080px(고정)
* 높이: 1920px

플러그인은 템플릿의 높이를 기반으로 생성된 경험의 크롬을 결정합니다.

#### 템플릿 표시

고정 크기 요구 사항은 없습니다. 표시 템플릿은 모든 크기를 지원합니다.

#### LinkedIn 템플릿

* 너비: 1200px(고정)
* 높이: 1200px, 628px, 2292px, 1800px 또는 1500px

이제 문서를 플러그인과 함께 사용할 준비가 되었습니다.

## 새 콘텐츠 생성

1. Photoshop을 엽니다.
1. 만든 GenStudio 준비 템플릿 문서를 열거나(위의 지침 참조) GenStudio for Performance Marketing 시작 템플릿을 사용합니다. `branding-template-acrobat-handlebars.psd`.
1. **[!UICONTROL Plugins]** > **[!UICONTROL GenStudio]**&#x200B;에서 플러그인 패널을 엽니다.
1. **[!UICONTROL 로그인]** 단추를 클릭합니다. URL을 열 수 있는 권한을 묻는 메시지가 표시되면 **내 선택 사항 저장**&#x200B;을 선택한 다음 **[!UICONTROL 허용]**&#x200B;을 클릭합니다.
1. 웹 브라우저를 사용하여 GenStudio for Performance Marketing에 액세스할 수 있는 프로필로 로그인합니다.
1. 연 템플릿에 적용되는 채널(Meta, LinkedIn 또는 Display)을 선택합니다.
   ![채널 선택](./ps-select-channel.png){width="300" zoomable="yes"}
1. 콘텐츠 생성에 사용할 [!DNL Brand], [!DNL Persona] 및 [!DNL Product] 컨텍스트를 선택하십시오.
   ![브랜드, 사용자 및 제품 선택](./ps-select-box.png){width="300" zoomable="yes"}
1. 생성할 변형 수를 선택합니다.
1. **[!UICONTROL 콘텐츠 선택]** 아래의 단추를 사용하여 에셋에서 이미지를 찾아보고 선택합니다. 가장 최근에 추가된 40개의 에셋이 먼저 나타나고 다른 에셋을 검색할 수 있습니다. 선택한 이미지는 템플릿에 맞게 자동으로 크기가 조정됩니다.
1. **[!UICONTROL 텍스트 프롬프트]** 상자에 내용에 대한 텍스트 프롬프트를 입력하십시오.
1. **[!UICONTROL 생성]** 단추를 클릭합니다. 변형은 플러그인 패널의 카드에 나타납니다.

생성된 콘텐츠가 템플릿 필드에 적용된 새 문서가 Photoshop 작업 영역에 추가됩니다. 이러한 문서의 이름은 번호가 매겨진 변형 접미사를 사용하여 지정됩니다.

## 콘텐츠 번역

사용자는 복사 생성 후 콘텐츠를 지원되는 언어로 번역할 수 있습니다.

1. 플러그인으로 광고 복사본을 생성한 후 **[!UICONTROL 번역]**&#x200B;을 클릭하세요.
1. 번역할 언어를 하나 이상 선택하십시오.
1. **[!UICONTROL 번역]** 단추를 클릭합니다.

생성된 콘텐츠가 템플릿 필드에 적용된 새 문서가 Photoshop 작업 영역에 추가됩니다. 이러한 문서의 이름은 번호가 매겨진 변형 접미사를 사용하여 지정됩니다.

## GenStudio으로 경험 내보내기

사용자는 콘텐츠 생성 또는 번역 후 내보내기를 선택할 수 있습니다. 내보낸 경험이 GenStudio for Performance Marketing의 콘텐츠 섹션에 채워집니다.

![콘텐츠 섹션에 표시된 내보낸 에셋](./content-assets.png){width="90%"}

## 문제 해결

생성된 변형에서 텍스트나 이미지를 대체하지 않는 경우 이러한 모범 사례와 팁을 고려하십시오.

### 매핑된 필드

텍스트나 이미지를 바꿀 수 없는 경우 필드가 중괄호 `{}`이(가) 아닌 중괄호 `()`로 올바르게 매핑되었는지 확인하십시오.

### 글꼴을 사용할 수 있는지 확인

생성 중에 대체하려면 시스템에서 텍스트 필드의 글꼴을 사용할 수 있어야 합니다. 파일에 사용된 모든 글꼴을 컴퓨터에서 사용할 수 있는지 확인합니다. 특히 파일이 다른 사람의 컴퓨터에서 만들어진 경우 사용할 수 있습니다.

### 필드 매핑 예외

{{$include /help/_includes/field-mapping-exceptions.md}}
