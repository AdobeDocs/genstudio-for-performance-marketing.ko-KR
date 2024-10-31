---
title: 이메일 경험
description: Adobe GenStudio for Performance Marketing의 이메일 경험에 대해 알아봅니다.
feature: Experiences, Content Generation, Create, Generative AI, Variant Generation
role: User
level: Beginner
source-git-commit: cb700de090d6a2f6a6c75afcf8a4ba118ded9527
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---


# 이메일 경험

Adobe GenStudio for Performance Marketing을 사용하면 생성 AI를 사용하여 [영향력이 큰 이메일 경험 만들기](/help/user-guide/create/create-email-experience.md)를 간소화할 수 있습니다.

[!DNL Create]을(를) 사용하면 최신 마케터가 [지침](/help/user-guide/guidelines/overview.md), 이미지 에셋 및 [잘 만들어진 프롬프트](/help/user-guide/effective-prompts.md)를 사용하여 [브랜드 기반의 이메일 경험을 빠르게 만들기](/help/user-guide/create/create-email-experience.md)할 수 있습니다.

이메일 경험의 편집 가능한 섹션에는 다음이 포함됩니다.

* 사전 머리글
* 제목
* 본문
* 클릭 유도 문안(CTA)
* 이미지
* 브랜드 로고

[템플릿 요소](/help/user-guide/content/use-templates.md#template-elements)를 참조하십시오.

<!-- ## Email capabilities

Content creators and marketers can produce brand-consistent email experiences in GenStudio for Performance Marketing. -->

## 여러 섹션 이메일

이메일 경험은 여러 섹션을 포함할 수 있으므로 브랜드 및 목표에 맞게 전체 맞춤화를 구현할 수 있습니다. [각 섹션의 시각적 자산을 선택 [!DNL Products] 하고](/help/user-guide/create/create-email-experience.md#add-parameters)한 다음 [구조화된 프롬프트](/help/user-guide/effective-prompts.md#structured-prompts)를 사용하여 고유한 콘텐츠를 만듭니다. 각 섹션은 하나의 시각적 자산을 지원합니다.

다중 섹션 템플릿을 만드는 방법을 알아보려면 [전자 메일 템플릿 준비](/help/user-guide/content/email-template.md)를 참조하세요.

## 점진적 로드

콘텐츠 생성 프로세스가 시작되면 이메일 변형에서 생성된 콘텐츠의 각 섹션이 캔버스에 점진적으로 로드됩니다. 경험, 에셋, 경험 내의 필드 및 섹션은 생성될 때 캔버스에 개별적으로 표시됩니다.

**[!UICONTROL 생성]**&#x200B;을 클릭하면 캔버스 아래쪽에 로딩 표시기가 표시되어 생성 진행 상황을 업데이트합니다.

이메일 경험의 각 필드 및 섹션은 이 시퀀스에서 점진적으로 로드됩니다.

1. 변형 이름
1. 모든 변형에 대한 제목 줄
1. 사전 머리글
1. 헤드라인, 이메일 본문(단일 섹션 이메일용) 및 콜 투 액션
1. 후속 섹션의 이메일 본문(다중 섹션 이메일의 경우)
1. 브랜드 유효성 검사 프로세스가 발생하고 각 변형에 대해 [_브랜드 지침 검사_](/help/user-guide/guidelines/brand-validation.md#brand-guidelines-check)&#x200B;가 채워집니다.

## 문자 수

이메일 변형 세트를 생성하면 각 이메일 섹션에 표시되는 문자 수를 볼 수 있습니다. 생성된 섹션(예: 제목 줄이나 본문)을 마우스로 가리키거나 클릭하면 해당 섹션에 대한 섹션 이름 및 문자 수가 표시됩니다.

![문자 수](/help/assets/character-count.png){width="500" zoomable="yes"}
