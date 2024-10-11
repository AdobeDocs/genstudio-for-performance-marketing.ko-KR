---
title: Adobe GenStudio for Performance Marketing 시작
description: 새 브랜드 정렬 마케팅 콘텐츠를 생성하도록 GenStudio for Performance Marketing을 설정하는 방법에 대해 알아봅니다.
level: Beginner
feature: Prompt, Brands Service, Personas Service, Products Service, Generative AI, Guidelines
exl-id: bcb03198-bbcb-45ae-af01-25c1e834b563
source-git-commit: 449c212ab167a6c126492e9becedf9318bfe08ee
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 1%

---

# Adobe GenStudio for Performance Marketing 시작

Adobe GenStudio for Performance Marketing은 브랜드 정체성을 반영하고 준수하는 마케팅 경험을 만들고, 평가하고, 관리하기 위한 포괄적인 플랫폼입니다.

이해 당사자의 다양한 기능에 대한 액세스는 할당된 _사용자 역할_&#x200B;에 의해 제어됩니다. 할당된 사용자 역할에 따라 GenStudio for Performance Marketing 내에서 수행할 수 있는 작업이 결정됩니다. Adobe 시스템 관리자는 Adobe Admin Console의 GenStudio for Performance Marketing 제품 프로필에 권한을 할당합니다. 시작 이메일은 할당된 역할을 식별합니다.

생성 AI 기반 도구를 처음 사용하거나 GenStudio for Performance Marketing 핵심 원칙에 대해 궁금한 경우 [개념](concepts.md) 및 [효과적인 프롬프트 작성](effective-prompts.md)을 참조하십시오.

## 사용자 역할

최신 마케팅 캠페인을 만들고 배포하려면 다양한 책임과 기술을 가진 관련자 간의 협업이 필요합니다.

세 가지 유형의 GenStudio for Performance Marketing 사용자 역할은 이러한 다양한 조직 역할을 지원합니다. 권한은 이러한 각 사용자 유형에 맞게 조정되며 마케팅 조직에서 각 사용자의 책임을 지원합니다.

**세 가지 사용자 역할 유형은**&#x200B;입니다.

* **편집자**&#x200B;는 GenStudio for Performance Marketing 생성 AI 기능을 사용하여 마케팅 캠페인 에셋을 만들고, 콘텐츠 검토 및 승인을 요청하고, 이 콘텐츠의 승인된 초안을 게시합니다. 모든 GenStudio for Performance Marketing 사용자는 자산 생성자가 콘텐츠에 저장한 후 자산에 액세스하고 사용할 수 있습니다.

* **공동 작업자**&#x200B;는 가장 광범위한 GenStudio for Performance Marketing 사용자입니다. 공동 작업자는 컨텐츠를 보고 승인할 수 있으며, 생성하는 컨텐츠가 조직의 요구 사항 및 표준과 일치하도록 하는 워크플로의 필수 부분입니다.

* **시스템 관리자**&#x200B;는 GenStudio for Performance Marketing 내에서 가장 광범위한 사용 권한을 가집니다. 시스템 관리자는 캠페인 자산 생성 및 배포를 위한 기본 가드레일을 설정하는 필수 온보딩 작업을 수행합니다. 시스템 관리자는 [브랜드 지침](/help/user-guide/guidelines/overview.md)과 같은 브랜드 및 조직별 정보를 업로드하여 이러한 보호 기능을 구현합니다. GenStudio for Performance Marketing 시스템 관리자에게는 브랜드를 만들고 게시할 수 있는 권한이 있지만, 사용자 관리 권한은 없습니다.

>[!NOTE]
>이러한 역할에 사용자를 할당하려면 먼저 Adobe Admin Console에서 Adobe 시스템 관리자를 지정하여 일회성 설정 작업을 수행해야 합니다. 이 Adobe 관리자 역할은 Adobe Admin Console 컨텍스트에서만 작동합니다. GenStudio for Performance Marketing 플랫폼 인터페이스에는 역할이 없습니다.

### GenStudio for Performance Marketing 편집기

**편집자**&#x200B;에게 GenStudio for Performance Marketing [!DNL Brands], [!DNL Campaigns] 및 [!DNL Content] 자산을 만드는 데 필요한 핵심 권한이 있습니다. 자신이 만든 에셋을 편집하고 삭제할 수도 있습니다. GenStudio for Performance Marketing은 수백 개의 컨텐츠를 빠르게 만들 수 있도록 지원합니다. 이러한 사용자는 특정 마케팅 캠페인의 요구 사항을 충족하도록 승인된 콘텐츠의 개별 조각을 오케스트레이션하는 콘텐츠 섹션 또는 전체 경험을 생성할 수 있습니다.

편집자는 _확인_&#x200B;을 통해 GenStudio for Performance Marketing 생성 AI 기술과 상호 작용합니다. 캔버스의 프롬프트 서랍에서는 특정 캠페인 지침의 컨텍스트에 프롬프트를 배치할 수 있는 도구를 제공합니다. 따라서 생성된 콘텐츠의 품질과 성공은 조직이 업로드한 브랜드 지침의 품질과 프롬프트의 특수성에 따라 부분적으로 달라집니다.

[유효한 프롬프트 쓰기](effective-prompts.md)를 참조하십시오.

다음 표에는 기본 편집기 권한이 표시됩니다.

| 기능 | 만들기 | 업데이트 | 삭제 | 보기 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Campaigns] | 예 | 예 | 예 | 예 |
| [!DNL Content] | 예 | 예 | 예 | 예 |
| [!DNL Insights] | ad 커넥터만 구성할 수 있음 |    |     | 예 |
| [!DNL Personas] | 예 | 예 | 예 | 예 |
| [!DNL Products] | 예 | 예 | 예 | 예 |
| [!DNL Reviews and approvals] | 예 | 예 | 예 | 예 |

### GenStudio for Performance Marketing 공동 작업자

**공동 작업자**&#x200B;는 GenStudio for Performance Marketing에서 자산을 볼 수 있지만 이러한 자산을 만들거나 편집하거나 삭제할 수는 없습니다. 공동 작업자에는 콘텐츠에 대한 검토 및 승인 프로세스의 성공에 필수적이지만 콘텐츠를 만들거나 직접 편집할 필요가 없는 관련자가 포함됩니다. 법률 전문가와 창작자의 관리자들은 잠재적 협력자의 사례이다. GenStudio for Performance Marketing 공동 작업자는 다른 Creative Cloud 제품에서 에셋을 만들고 볼 수 있는 권한이 있을 수 있습니다.

다음 표에는 기본 공동 작업자 권한이 표시됩니다.

| 기능 | 만들기 | 업데이트 | 삭제 | 보기 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Campaigns] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Content] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Insights] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Personas] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Products] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Reviews and approvals] | 아니요 | 아니요 | 아니요 | 예 |

### GenStudio for Performance Marketing 시스템 관리자

**GenStudio 시스템 관리자** 조직에서 GenStudio for Performance Marketing을 배포하도록 준비하는 초기 작업을 완료합니다.

다음 표에는 기본 GenStudio for Performance Marketing 시스템 관리자 권한이 표시됩니다.

| 기능 | 만들기 | 업데이트 | 삭제 | 보기 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 예 | 예 | 예 | 예 |
| [!DNL Campaigns] | 예 | 예 | 예 | 예 |
| [!DNL Content] | 예 | 예 | 예 | 예 |
| [!DNL Insights] | 예 | 예 | 예 | 예 |
| [!DNL Personas] | 예 | 예 | 예 | 예 |
| [!DNL Products] | 예 | 예 | 예 | 예 |
| [!DNL Reviews and approvals] | 예 | 예 | 예 | 예 |


## 콘텐츠를 생성할 GenStudio for Performance Marketing 준비

GenStudio for Performance Marketing 시스템 관리자는 편집자와 공동 작업자가 캠페인 에셋을 만들 수 있도록 조직의 GenStudio for Performance Marketing 환경을 준비합니다. 이러한 사전 설정 작업에는 다음이 포함됩니다.

1. [!DNL Brands], [!DNL Products] 및 [!DNL Personas]에 대해 [지침을 추가](./guidelines/overview.md)합니다. 조직 브랜드 정체성의 핵심 구성 요소를 설정하는 것은 크리에이터와 공동 작업자의 작업에 필수적인 전제 조건입니다. 브랜드 가이드라인 문서를 업로드하거나 수동으로 브랜드 정보를 입력할 수 있습니다.
   * **지침 문서를 준비하세요**. 브랜드 가이드라인을 설명적이고 포괄적일수록 출력이 향상됩니다. 브랜드에 필수라고 간주하는 기능에 대한 간단한 예를 포함하고 콘텐츠 생성에서 제외할 동작에 대한 설명을 추가합니다. GenStudio for Performance Marketing은 이러한 업로드된 문서에서 정보를 추출하고 브랜드 구축을 시작합니다. GenStudio for Performance Marketing이 업로드한 문서에서 각 지침을 어셈블하면 브랜드 음성, 채널 및 이미지 지침 등의 정보가 채워집니다.
   * **필요에 따라 브랜드 지침 필드를 편집하거나 완료합니다**. 포괄적인 브랜드 지침은 조직의 브랜드를 이해하는 GenStudio for Performance Marketing의 기반을 구성합니다. GenStudio for Performance Marketing이 브랜드 가이드라인 문서에서 필요한 정보를 추출하면 추출된 정보 필드를 수동으로 편집하거나 완료하라는 메시지가 표시됩니다. [!DNL Product]을(를) 추가하여 콘텐츠를 만들 개별 제품 포커스 영역을 지정하십시오. [!DNL Personas] 지침은 정의된 고객 세그먼트에 대한 콘텐츠 만들기를 사용자 지정하는 데 도움이 됩니다.

   조직의 브랜드 지침을 설정하는 것이 일회성 작업이 될 수 있지만 조직의 변동성, 성장 및 변화하는 시장 상황에 따라 이 지침을 수정하고 강화해야 할 수 있습니다.

1. **[템플릿 업로드](./content/use-templates.md)**. 템플릿은 바로 가기를 제공하고 컨텐츠 생성 시간을 단축합니다. 템플릿에는 머리글과 바닥글과 같은 승인된 기능이 포함되어 있으며 콘텐츠 생성을 위한 가드레일을 설정합니다. 시스템 관리자는 일반적으로 조직의 템플릿을 업로드하고 관리합니다. 크리에이터는 템플릿을 사용하여 조직 브랜드의 확립된 경계 내에서 콘텐츠 작성 프로세스를 바로 시작합니다.

1. **[승인된 에셋 업로드](./content/manage-assets.md)**. [!DNL Content]의 승인된 에셋은 모든 GenStudio for Performance Marketing 작성자가 사용할 수 있습니다. 작성자가 새 경험이나 자산을 만드는 데 사용할 수 있는 자산으로 [!DNL Content]을(를) 시드할 수 있습니다.

1. **[메타(Facebook) 계정에 연결](./insights/connect-channel.md)**. GenStudio for Performance Marketing과 조직의 소셜 계정 간의 연결을 구성하여 활성 마케팅 캠페인, 에셋 및 경험에서 데이터를 받을 수 있습니다. [[!DNL Insights]](./insights/overview.md)은(는) 채널 파생 데이터를 분석하는 도구를 제공합니다.
