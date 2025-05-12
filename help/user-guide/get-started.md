---
title: Adobe GenStudio for Performance Marketing 시작
description: GenStudio for Performance Marketing을 사용하여 새로운 브랜드 맞춤 마케팅 콘텐츠를 생성하는 방법을 알아봅니다.
level: Beginner
role: User
feature: Media Templates, Guidelines, Generative AI
exl-id: bcb03198-bbcb-45ae-af01-25c1e834b563
source-git-commit: f98a853965ce05420cd178c294b3b4d69500977b
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 2%

---

# Adobe GenStudio for Performance Marketing 시작

Adobe GenStudio for Performance Marketing은 콘텐츠 생성, 관리 및 분석을 간소화하기 위해 설계된 포괄적인 도구 모음을 제공합니다. 콘텐츠 생성 라이프사이클에 마케팅 콘텐츠가 생성, 검토, 공유 및 분석되는 방식을 전환하는 생성 AI 기능을 주입합니다.

## 콘텐츠 만들기, 공유 및 검토 시작

생성 AI 기반 도구를 처음 사용하거나 GenStudio for Performance Marketing의 핵심 원칙에 대해 궁금한 경우 [개념](concepts.md) 및 [효과적인 프롬프트 작성](effective-prompts.md)을 참조하십시오. Adobe의 온라인 학습 플랫폼인 [Adobe GenStudio Academy](https://learningmanager.adobe.com/genstudioacademy)에서 생성 AI 기술을 크리에이티브 프로세스에 사용하는 방법에 대해 확인할 수 있습니다.

## GenStudio for Performance Marketing 교육

GenStudio for Performance Marketing은 브랜드 및 시장에 대한 정보를 사용하여 브랜드 준수 콘텐츠 생성을 향상시킵니다. 교육 자료에는 예제, 고객 [personas](/help/user-guide/guidelines/personas.md) 및 [제품](/help/user-guide/guidelines/products.md)에 대한 설명, [브랜드 지침](/help/user-guide/guidelines/overview.md)이 포함됩니다.

시스템 관리자는 조직별 정보를 입력하거나 업로드하여 Adobe GenStudio for Performance Marketing을 설정합니다. 이러한 준비를 통해 콘텐츠 편집자와 공동 작업자가 생성 AI 기능을 사용하여 캠페인 에셋을 만들고 검토할 수 있습니다. Adobe 시스템 관리자가 조직의 제품 인스턴스를 프로비저닝하고 GenStudio 시스템 관리자 권한을 할당하면 GenStudio 시스템 관리자는 지침을 사용하여 제품의 기본 생성 AI 프레임워크를 준비할 수 있습니다.

### 1단계: 지침 추가

조직 브랜드 정체성의 주요 구성 요소를 설정하는 것은 콘텐츠 편집자 및 공동 작업자의 작업에 필수적인 전제 조건입니다. [지침](./guidelines/overview.md) 로고, 음색 및 색상 팔레트와 같은 브랜드 특성을 캡처합니다. [[!DNL Brands] 지침](./guidelines/brands.md) 문서를 업로드하거나 브랜드 정보를 수동으로 입력할 수 있습니다. [[!DNL Personas] 지침](./guidelines/personas.md) 및 [[!DNL Products] 지침](./guidelines/products.md)도 중요합니다. GenStudio for Performance Marketing의 기본 생성 AI 기능은 이 지침을 사용하여 콘텐츠 생성을 안내하는 가드레일을 설정합니다.

#### 지침 문서 준비

포괄적이고 집중적인 [[!DNL Brands]](./guidelines/brands.md), [[!DNL Products]](./guidelines/products.md) 및 [[!DNL Personas]](./guidelines/personas.md) 지침은 조직의 마케팅 캠페인의 핵심 측면을 정의합니다. GenStudio for Performance Marketing은 이러한 지침에서 정보를 추출하여 브랜드 구축을 시작합니다. GenStudio for Performance Marketing에 정보를 수동으로 입력할 때 지침 문서를 업로드하거나 참조할 수 있습니다. 이 정보를 업로드하거나 입력하는 방법은 [지침 추가](./guidelines/overview.md)를 참조하십시오.

#### 지침 개정

GenStudio 시스템 관리자는 조직의 특정 브랜드 요구 사항을 수동으로 입력하거나 업로드하여 제품의 기본 생성 AI 프레임워크를 준비할 수 있습니다. 조직의 브랜드 지침을 설정하는 것은 일회성 작업이지만 조직의 변동성, 성장 및 변화하는 시장 상황에 따라 이 지침을 수정하고 강화할 수 있습니다.

### 2단계: GenStudio [!DNL Brands]에 대한 Adobe Admin Console 프로젝트 설정

공동 작업자가 [!DNL Brands]을(를) 편집하거나 만들려면 시스템 관리자가 추가 설정 작업을 완료해야 합니다. Adobe 시스템 관리자는 Adobe Admin Console에서 다음 작업을 수행합니다.

* [!DNL Brands] 권한을 편집하고 만들어야 하는 모든 사용자를 포함하는 새 사용자 그룹을 만드십시오.

* Adobe Admin Console에서 새 프로젝트를 만듭니다.

[브랜드 권한 할당](configure-brand-permissions.md)을 참조하세요.

### 3단계: 템플릿 업로드

템플릿은 콘텐츠 작성 시간을 단축합니다. 템플릿에는 머리글과 바닥글과 같은 승인된 기능이 포함되어 있으며 특정 채널에 최적화되어 있습니다. 시스템 관리자는 일반적으로 조직의 템플릿을 업로드하고 관리합니다. 콘텐츠 편집자는 템플릿을 사용하여 조직 브랜드의 정해진 경계 내에서 콘텐츠 작성 프로세스를 바로 시작할 수 있습니다.

[템플릿 작업](./content/use-templates.md)을 참조하세요.

### 4단계: 승인된 에셋 업로드

[!DNL Content]의 승인된 에셋은 모든 GenStudio for Performance Marketing 편집자가 사용할 수 있습니다. [!DNL Content]을(를) 콘텐츠 편집기에서 새 경험이나 자산을 만드는 데 사용할 자산으로 채울 수 있습니다.

[승인된 에셋 업로드](./content/manage-assets.md)를 참조하십시오.

### 5단계: 메타(Facebook) 계정에 연결

GenStudio for Performance Marketing과 조직의 소셜 계정 간의 연결을 구성하여 활성 마케팅 캠페인, 에셋 및 경험에서 데이터를 받을 수 있습니다. [!DNL Insights]은(는) 채널 파생 데이터를 분석하는 도구를 제공합니다. [메타 광고에 연결](/help/user-guide/connectors/meta-ads.md)을 참조하십시오.
