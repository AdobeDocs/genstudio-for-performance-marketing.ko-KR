---
title: 이메일 경험
description: 캔버스 동작 및 승인된 라이브러리의 콘텐츠 조각 교체를 포함하여 Adobe GenStudio for Performance Marketing의 이메일 경험에 대해 알아봅니다.
feature: Create Canvas, Media Templates
role: User
level: Beginner
exl-id: e2bddd02-914e-43a8-92b6-fdcbced94a6a
TQID: https://experienceleague.adobe.com/-lwSfvc0TnVd8byNT-5OfoEsXz7yaeIifcHOJtp-n4c
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
feature_v2:
  - id: c7c3a4ab-6b96-4f2f-8931-4d2b360c3d12
  - id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3a
  - id: f71bd2fc-e9ca-4cb6-8088-82e250211e32
subfeature_v2:
  - id: a8b28c00-da6e-4d27-8667-80f790ad8972
  - id: be495d08-ecd1-455f-951e-c22de504e667
  - id: dee4e9a9-78d1-4953-8179-f8da6117027d
  - id: ee4b6e5f-5b7a-421b-9859-0f964841a866
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 3890f933a4cccae2e5dbe7ef2184e1dfd089b20b
workflow-type: tm+mt
source-wordcount: 600
ht-degree: 0%

---

# 이메일 경험

Adobe GenStudio for Performance Marketing을 사용하면 생성 AI를 사용하여 [영향력이 큰 이메일 경험 만들기](/help/user-guide/create/create-email-experience.md)를 간소화할 수 있습니다.

[!DNL Create]을(를) 사용하면 최신 마케터가 [지침](/help/user-guide/guidelines/overview.md), 이미지 에셋 및 [잘 만들어진 프롬프트](/help/user-guide/effective-prompts.md)를 사용하여 [브랜드 기반의 이메일 경험을 빠르게 만들기](/help/user-guide/create/create-email-experience.md)할 수 있습니다.

이메일 경험을 생성할 때 4개의 변형이 만들어져 캔버스에 표시됩니다.

이메일 경험의 편집 가능한 섹션에는 다음이 포함됩니다.

* 사전 머리글
* 제목
* 하위 헤드라인
* 본문
* Call to action(CTA)
* 이미지

[템플릿 요소](/help/user-guide/templates/use-templates.md#template-elements)를 참조하십시오.

<!-- 
## Email capabilities

Content creators and marketers can produce brand-consistent email experiences in GenStudio for Performance Marketing. 
-->

## 여러 섹션 이메일

이메일 경험은 여러 섹션을 포함할 수 있으므로 브랜드 및 목표에 맞게 전체 맞춤화를 구현할 수 있습니다. [각 섹션의 시각적 자산을 선택 [!DNL Products] 하고](/help/user-guide/create/create-email-experience.md#add-parameters)한 다음 [구조화된 프롬프트](/help/user-guide/effective-prompts.md#structured-prompts)를 사용하여 고유한 콘텐츠를 만듭니다. 각 섹션은 하나의 시각적 자산을 지원합니다.

다중 섹션 템플릿을 만드는 방법은 [섹션을 사용하여 템플릿 사용자 지정](/help/user-guide/templates/customize-template.md#sections-or-groups)을 참조하세요.

## 점진적 로드

콘텐츠 생성 프로세스가 시작되면 이메일 변형에서 생성된 콘텐츠의 각 섹션이 캔버스에 점진적으로 로드됩니다. 경험, 에셋, 경험 내의 필드 및 섹션은 생성될 때 캔버스에 개별적으로 표시됩니다.

**[!UICONTROL 생성]**&#x200B;을 클릭하면 캔버스 아래쪽에 로딩 표시기가 표시되어 생성 진행 상황을 업데이트합니다.

이메일 경험의 각 필드 및 섹션은 이 시퀀스에서 점진적으로 로드됩니다.

1. 변형 이름
1. 모든 변형에 대한 제목 줄
1. 사전 머리글
1. 헤드라인, 이메일 본문(단일 섹션 이메일용) 및 콜 투 액션
1. 후속 섹션의 이메일 본문(다중 섹션 이메일의 경우)
1. 브랜드 유효성 검사

   브랜드 유효성 검사 및 컨텐츠 검사 프로세스가 수행되며 각 변형에 대해 [_컨텐츠 검사_ 요약](/help/user-guide/guidelines/brand-validation.md#content-check-summary)이(가) 채워집니다.

## 문자 수

이메일 변형 세트를 생성하면 각 섹션에 표시된 문자 수를 볼 수 있습니다. 생성된 섹션(예: 제목 줄이나 본문)을 마우스로 가리키거나 클릭하면 해당 섹션에 대한 섹션 이름 및 문자 수가 표시됩니다.

![문자 수](/help/assets/character-count.png){width="500" zoomable="yes"}

## 컨텐츠 조각 교체 {#content-fragment-swap}

>[!NOTE]
>
>콘텐츠 조각 교환은 오늘 캔버스에서 **이메일** 경험에 사용할 수 있습니다. **Horizon** 채널 지원이 곧 제공됩니다.

엔터프라이즈 이메일 컨텐츠는 템플릿을 위해 구체화하는 컨텐츠와 함께 새로 생성된 사본 및 승인된 모듈식 블록(예: 면책조항, 안전 언어, 오퍼 및 규제 대상 청구)이 모두 필요한 경우가 많습니다. [!DNL Adobe Experience Manager]에 모듈식 콘텐츠를 저장하는 팀은 [!DNL GenStudio for Performance Marketing]을(를) 종료하지 않고 전자 메일 경험에서 사용할 해당 콘텐츠를 찾아서 교환할 수 있습니다. 이 기능은 다음 경우에 유용합니다.

* **규정 준수 인식 콘텐츠:** AI는 크리에이티브 슬롯을 채울 수 있으며 규정 준수 승인 조각은 주입 가능한 슬롯을 대체합니다. 내보내기를 통해 잠긴 법적 영역은 변경되지 않습니다.
* **재사용 가능한 승인된 콘텐츠 구성 요소:** 승인된 헤드라인, 지역 면책조항 또는 제품 설명은 작성자가 복사하여 붙여 넣는 해결 방법 없이 변형으로 가져오는 동안 [!DNL Adobe Experience Manager]의 기록 시스템으로 남아 있을 수 있습니다.

크리에이터는 캔버스에서 경험을 조합합니다. 브랜드 및 규정 준수 팀은 [!DNL Adobe Experience Manager]에서 승인 워크플로를 유지합니다. IT 및 통합 팀은 조직에 필요한 저장소 및 권한을 연결합니다.

![콘텐츠 조각 바꾸기](./cf-swap.png){width="500" zoomable="yes"}

조직에서 콘텐츠 조각 교체를 활성화하면 다음을 기대할 수 있습니다.

* 수동 입력 또는 AI 생성만 하는 대신 연결된 콘텐츠 라이브러리에서 콘텐츠 조각 필드를 채울 수 있습니다.
* 캠페인, 성향, 채널, 언어 및 브랜드와 같은 메타데이터를 사용하여 조각을 검색, 검색 및 필터링합니다.
* 저장소 선택기는 여러 저장소가 구성된 경우 사용할 수 있습니다.
* 필드 텍스트를 바꾸기 전에 조각을 미리 봅니다.
* 한 번의 작업으로 모든 변형에서 조각 선택을 전달합니다.

![콘텐츠 조각 UI 창](./cf-pane.png){width="500" zoomable="yes"}

조직은 사용 가능한 콘텐츠 조각 소스 및 저장소를 선택합니다. 관리자가 소스를 구성하는 방법 및 작성자가 캔버스에서 **[!UICONTROL 교체]**&#x200B;로 복사본을 교환하는 방법은 [콘텐츠 조각 확장 찾기](/help/extensibility/deploy-app.md#find-content-fragment-extension)를 참조하십시오.

HTML 캔버스에서 승인된 이메일 경험을 여러 언어로 번역할 수도 있습니다. [경험 번역 및 지역화](/help/user-guide/create/translate-experiences.md)를 참조하세요.
