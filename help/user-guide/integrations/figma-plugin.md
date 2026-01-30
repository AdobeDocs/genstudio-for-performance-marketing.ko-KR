---
title: Adobe GenStudio for Performance Marketing용 Figma 플러그인
description: GenStudio for Performance Marketing용 Figma 플러그인을 구성하고 사용하는 방법에 대해 알아봅니다.
feature: Generative AI
role: User
source-git-commit: bb6b8de80bdf6089e70756bea5dbf3e6a7945052
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 0%

---

# GenStudio for Performance Marketing용 Figma 플러그인

GenStudio for Performance Marketing Figma 플러그인은 Figma 애플리케이션에 온-브랜드 콘텐츠를 생성할 수 있는 새 패널을 추가합니다.

이 페이지에서는 플러그인을 구성하고 사용하는 방법에 대해 설명합니다.

이 플러그인의 기능은 다음과 같습니다.

* 그림 텍스트 요소를 `headline`, `body`, `on_image_text` 등 GenStudio for Performance Marketing 필드에 매핑합니다.
* 브랜드, 사용자, 제품 및 텍스트 프롬프트를 기반으로 새 On-Brand Meta, LinkedIn 또는 Display 광고 [!DNL Experiences]을(를) 생성합니다.
* 매핑된 Figma 요소의 텍스트를 GenStudio for Performance Marketing에서 생성된 값으로 바꾸어 Figma 문서에서 직접 [!DNL Experiences]을(를) 만듭니다.
* 프롬프트에 따라 기존 콘텐츠를 다시 구문 분석, 단축, 길이 조정 또는 번역할 수 있습니다.
* 생성된 [!DNL Experiences]을(를) 여러 언어로 번역합니다.
* 생성된 [!DNL Experiences]을(를) 병합된 이미지로 로컬 원본으로 내보냅니다.
* 생성된 [!DNL Experiences]을(를) GenStudio for Performance Marketing으로 내보냅니다.
* 그림 캔버스에서 선택한 요소에 맞게 조정하는 플러그인 옵션을 사용합니다.

>[!VIDEO](https://video.tv.adobe.com/v/3478816?captions=kor&learn=on)

## 템플릿 만들기

플러그인을 사용하려면 Figma 문서의 처음 두 수준이 이 규칙을 따라야 합니다.

* **섹션** - 여러 템플릿을 포함할 수 있는 상위 프로젝트를 나타냅니다.
* **프레임** - 프로젝트 내의 템플릿을 나타냅니다. 템플릿은 텍스트, 이미지, 구성 요소 및 기타 요소로 채울 수 있습니다.

### Meta 템플릿

지원되는 템플릿 크기는 다음과 같습니다.

Instagram 또는 Facebook 게시물의 경우:

* 너비: 1080px(고정)
* 높이: 1080px 또는 1350px

Instagram 또는 Facebook 스토리:

* 너비: 1080px(고정)
* 높이: 1920px

플러그인은 템플릿의 높이를 기반으로 생성된 경험의 크롬을 결정합니다.

### 템플릿 표시

고정 크기 요구 사항은 없습니다. 표시 템플릿은 모든 크기를 지원합니다.

### LinkedIn 템플릿

* 너비: 1200px(고정)
* 높이: 1200px, 628px, 2292px, 1800px 또는 1500px

### 필드 역할 매핑

플러그인은 헤드라인, 본문 또는 이미지와 같은 템플릿의 다양한 요소를 이해해야 합니다.

요소 역할을 할당하려면

1. 템플릿에서 요소(텍스트, 이미지 등)를 선택합니다.
1. 드롭다운 메뉴를 사용하여 역할을 할당합니다.

플러그인은 생성된 콘텐츠에 사용할 이러한 매핑을 기억합니다. 필드 역할은 여러 템플릿 요소에 매핑될 수 있습니다.

![필드 역할 매핑](./field-role-mapping.png){width="600"}

### 필드 매핑 예외

{{$include /help/_includes/field-mapping-exceptions.md}}

## 새 콘텐츠 생성

GenStudio for Performance Marketing AI를 사용하여 그림 템플릿의 요소를 생성하거나 변형할 수 있습니다.

1. GenStudio 플러그인 플레이그라운드 또는 이미 준비된 템플릿을 사용하는 경우 광고 템플릿이 포함된 섹션 노드를 선택합니다. **레이어** 패널에서 수행하거나 캔버스의 섹션을 직접 클릭하여 수행할 수 있습니다.
   ![섹션 선택 또는 변형](./plugin-playground.png){width="500" zoomable="yes"}
1. 플러그인 창에서 변형의 프로젝트 이름을 입력하고 컨텐츠의 플랫폼을 선택한 다음 기타 필수 정보를 입력합니다. 그런 다음 **[!UICONTROL 설치 완료]** 단추를 클릭합니다.
   ![프로젝트 설정 창](./setup-project.png){width="300" zoomable="yes"}
1. 콘텐츠 생성에 사용할 [!DNL Brand], [!DNL Persona] 및 [!DNL Product]을(를) 선택하십시오.
1. 생성할 변형 수(최대 8개)를 선택합니다.
1. **[!UICONTROL 콘텐츠 선택]** 아래의 단추를 사용하여 에셋에서 이미지를 찾아보고 선택합니다. 가장 최근에 추가된 40개의 에셋이 먼저 나타나고 다른 에셋을 검색할 수 있습니다. 선택한 이미지는 템플릿에 맞게 자동으로 크기가 조정됩니다.
1. 텍스트 프롬프트를 입력합니다. **[!UICONTROL 필드]** 목록의 각 필드에는 새 콘텐츠에 대해 **[!UICONTROL 작업]** 옵션이 **[!UICONTROL 생성]**(으)로 설정되어 있습니다.
1. 모든 필드 역할을 매핑합니다. [필드 역할 매핑](#field-role-mapping)을 참조하세요.
1. **[!UICONTROL 생성]** 단추를 클릭합니다.

## 기존 콘텐츠에서 광고 복사 변형 번역 또는 생성

GenStudio for Performance Marketing AI를 사용하여 광고 카피 변형을 생성하거나 Figma 템플릿을 번역합니다.

1. 광고 템플릿이 포함된 섹션 노드를 선택합니다. **레이어** 패널에서 수행하거나 캔버스의 섹션을 직접 클릭하여 수행할 수 있습니다.
   ![섹션 선택 또는 변형](./plugin-playground.png){width="500" zoomable="yes"}
1. 플러그인 창에서 변형의 프로젝트 이름을 입력하고 컨텐츠의 플랫폼을 선택합니다.
1. **[!UICONTROL 의 목표는 무엇입니까?]**, **[!UICONTROL 변형 생성]** 또는 **[!UICONTROL 번역]**&#x200B;을 선택한 다음 **[!UICONTROL 설치 완료]** 단추를 클릭하십시오.
   ![프로젝트 설정 창](./setup-project.png){width="300" zoomable="yes"}
1. 콘텐츠 생성에 사용할 [!DNL Brand], [!DNL Persona] 및 [!DNL Product]을(를) 선택하십시오.
1. 생성할 변형 수를 선택합니다.
1. **[!UICONTROL 콘텐츠 선택]** 아래의 단추를 사용하여 에셋에서 이미지를 찾아보고 선택합니다. 가장 최근에 추가된 40개의 에셋이 먼저 나타나고 다른 에셋을 검색할 수 있습니다. 선택한 이미지는 템플릿에 맞게 자동으로 크기가 조정됩니다.
1. 텍스트 프롬프트를 입력합니다. **[!UICONTROL 필드]** 목록의 각 필드에는 새 콘텐츠에 대해 **[!UICONTROL 작업]** 옵션이 **[!UICONTROL 생성]**(으)로 설정되어 있습니다.
1. 모든 필드 역할을 매핑합니다. [필드 역할 매핑](#field-role-mapping)을 참조하세요.
1. 각 필드 유형을 선택하여 변형을 생성하거나 플러그인 왼쪽의 패널에서 번역한 다음 초기 콘텐츠를 각 **[!UICONTROL 초기 콘텐츠]** 상자에 붙여 넣습니다.
   ![초기 콘텐츠 상자의 샘플 텍스트](./initial-content-box.png){width="60%" zoomable="yes"}
1. **[!UICONTROL 생성]** 단추를 클릭합니다.

## 생성 후 콘텐츠 번역

1. 번역할 세대를 선택합니다.
   ![생성 선택](./select-generation.png){width="200" zoomable="yes"}
1. **[!UICONTROL 번역]**&#x200B;을 선택한 다음 **[!UICONTROL 번역]**&#x200B;을 클릭합니다.
1. 타겟 언어를 선택합니다.
1. **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

번역 결과는 다음과 같습니다.

* 번역된 콘텐츠가 있는 새 페이지가 나타납니다.
* 각 번역에는 대상 언어 또는 로케일이 표시됩니다.
* 원본 콘텐츠는 원본 페이지에서 변경되지 않은 상태로 유지됩니다.

![번역 결과](./translation-results.png){width="60%" zoomable="yes"}

## 생성 후 콘텐츠 필드에 대한 기타 작업

필드에서 기존 콘텐츠를 편집하는 경우 유용한 옵션이 플러그인 패널에 나타납니다.

![플러그 인 작업 옵션](./figma-other-actions.png){width="300" zoomable="yes"}

옵션은 다음과 같습니다.

* 텍스트를 직접 변경하려면 **[!UICONTROL 값]**&#x200B;을(를) 변경하십시오. 이 콘텐츠를 변경하면 선택한 모든 변형에 자동으로 적용됩니다.
* AI는 다음을 포함한 많은 **[!UICONTROL 작업]** 옵션을 수행할 수 있습니다.

| 액션 | 설명 |
| --- | --- |
| **[!UICONTROL 생성]** | 텍스트의 새 변형을 생성합니다. |
| **[!UICONTROL 구문 변경]** | 텍스트의 새 변형을 생성합니다. |
| **[!UICONTROL 단축]** | 텍스트의 짧은 변형을 생성합니다. |
| **[!UICONTROL 길이]** | 더 긴 텍스트 변형을 생성합니다. |

**[!UICONTROL 작업]** 옵션을 선택한 후 **[!UICONTROL 다시 생성]** 단추로 콘텐츠를 다시 생성합니다.

## 경험 내보내기

Figma에서 변형을 GenStudio for Performance Marketing [!DNL Experiences]&#x200B;(으)로 내보낼 수 있습니다.

1. 다음 중 하나를 수행하여 그림 캔버스에서 내보낼 콘텐츠를 선택합니다.
   * 캔버스에서 생성 섹션을 선택한 다음 플러그인 패널에서 **[!UICONTROL 모두 내보내기 표시]**&#x200B;를 클릭합니다.
     ![생성 섹션 선택](./select-generation-section.png){width="200" zoomable="yes"}
   * 캔버스에서 개별 세대를 선택한 다음 플러그 인 패널에서 **[!UICONTROL 내보낼 표시]**&#x200B;를 클릭합니다.
     ![개별 생성 선택](./select-generation.png){width="200" zoomable="yes"}
1. 사이드바 메뉴에서 내보내기 항목을 선택합니다.
   ![Meta 광고에 대해 [내보내기 표시] 단추가 표시됨](./mark-for-export.png){width="60%" zoomable="yes"}
1. 대상을 선택하십시오.
1. 콘텐츠를 내보내려면 **[!UICONTROL 내보내기]**&#x200B;를 클릭합니다.

플러그인 패널에서 ZIP 파일이 만들어지거나 **[!UICONTROL GenStudio에서 열기]**&#x200B;에 대한 링크가 나타납니다. ZIP 링크를 사용하여 파일을 저장할 위치를 선택하거나 **[!UICONTROL GenStudio에서 열기]**&#x200B;를 선택합니다.

## 생성 기록

플러그인은 각 필드에 대한 변경 사항 기록을 유지 관리합니다. 템플릿 페이지의 플러그 인 사이드바에서 **[!UICONTROL 생성 기록]**&#x200B;을 선택하십시오.

![Meta 광고에 대해 표시되는 생성 기록 옵션](./generation-history.png){width="80%" zoomable="yes"}

## 문제 해결

생성된 변형에서 텍스트나 이미지를 대체하지 않는 경우 이러한 모범 사례와 팁을 고려하십시오.

### 매핑된 필드

텍스트 또는 이미지가 바뀌지 않는 경우 필드가 플러그인 UI에서 GenStudio 필드 역할에 매핑되었는지 확인합니다. [필드 역할 매핑](#field-role-mapping)을 참조하세요.

### 글꼴을 사용할 수 있는지 확인

생성 중에 대체하려면 시스템에서 텍스트 필드의 글꼴을 사용할 수 있어야 합니다. 파일에 사용된 모든 글꼴을 컴퓨터에서 사용할 수 있는지 확인합니다. 특히 파일이 다른 사람의 컴퓨터에서 만들어진 경우 사용할 수 있습니다.

### 필드 역할 지원 고려

특정 채널에서는 특정 필드에서만 교체를 지원합니다. [필드 역할 매핑](#field-role-mapping)에 대한 예외를 알아 두십시오.
