---
title: Adobe GenStudio for Performance Marketing 사용자 역할 및 권한
description: GenStudio for Performance Marketing 사용자 역할 및 권한에 대해 알아봅니다.
level: Beginner
feature: Prompt, Brands Service, Personas Service, Products Service, Generative AI, Guidelines
source-git-commit: 3e9a2a4f42ba79389691705c571bf6bbd0b990c5
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 2%

---

# 사용자 역할 및 권한

최신 마케팅 캠페인을 만들고 배포하려면 다양한 책임과 기술을 가진 관련자 간의 협업이 필요합니다. _사용자 역할_&#x200B;은(는) GenStudio for Performance Marketing의 다양한 기능에 대한 이해 당사자 액세스를 제어합니다. 할당된 사용자 역할에 따라 이 플랫폼을 사용하여 수행할 수 있는 작업이 결정됩니다. Adobe 시스템 관리자가 Adobe Admin Console에서 GenStudio 제품 프로필의 역할에 사용자를 할당합니다. 시작 이메일은 할당된 역할을 식별합니다.

>[!NOTE]
>
>이러한 역할에 사용자를 할당하려면 먼저 Adobe Admin Console에서 Adobe 시스템 관리자를 지정하여 일회성 설정 작업을 수행해야 합니다. 이 Adobe 관리자 역할은 Adobe Admin Console 컨텍스트에서만 작동합니다. GenStudio for Performance Marketing 플랫폼 인터페이스에는 역할이 없습니다. 시스템 관리자 권한이 필요한 Adobe 시스템 관리자는 Adobe Admin Console에서 GenStudio 시스템 관리자로 자신을 프로비저닝해야 합니다. [GenStudio for Performance Marketing 프로비저닝](product-provisioning.md)을 참조하십시오.

## 권한 부여

_자격_&#x200B;은(는) 특정 작업을 수행하고 보호된 리소스에 액세스할 수 있는 권한을 부여합니다. 권한은 제품 프로필 내의 사용자 역할에 정의되며 사용자는 해당 역할에 할당될 때 이러한 권한을 받습니다.

## 사용자 역할

세 가지 유형의 GenStudio for Performance Marketing 사용자 역할은 이러한 다양한 조직 역할을 지원합니다. 권한은 이러한 각 사용자 유형에 맞게 조정되며 마케팅 조직에서 각 사용자의 책임을 지원합니다. 다음 세 가지 사용자 역할 유형은 다음과 같습니다.

* **GenStudio 편집기** GenStudio for Performance Marketing의 생성 AI 기능을 사용하여 마케팅 캠페인 에셋을 만들고, 콘텐츠 검토 및 승인을 요청하고, 이 콘텐츠의 승인된 초안을 게시합니다. 편집기에서 자산을 [!DNL Content]에 저장하면 모든 GenStudio for Performance Marketing 사용자가 해당 자산에 액세스하고 사용할 수 있습니다.

* **GenStudio 공동 작업자**&#x200B;는 가장 광범위한 GenStudio for Performance Marketing 사용자입니다. 공동 작업자는 컨텐츠를 보고 승인할 수 있으며, 생성하는 컨텐츠가 조직의 요구 사항 및 표준과 일치하도록 하는 워크플로의 필수 부분입니다.

* **GenStudio 시스템 관리자**&#x200B;는 GenStudio for Performance Marketing 내에서 가장 광범위한 사용 권한 집합을 가집니다. 시스템 관리자는 캠페인 자산 생성 및 배포를 위한 기본 가드레일을 설정하는 필수 온보딩 작업을 수행합니다. 시스템 관리자는 [브랜드 지침](./guidelines/overview.md)과 같은 브랜드 및 조직별 정보를 업로드하여 이러한 보호 기능을 구현합니다. 시스템 관리자에게는 [!DNL Brands]을(를) 만들고 게시할 수 있는 권한이 있지만 사용자 관리 권한이 없습니다.

### GenStudio 편집기

_편집자_ 또는 콘텐츠 작성자는 GenStudio for Performance Marketing [!DNL Brands], [!DNL Campaigns] 및 [!DNL Content] 에셋을 만드는 데 필요한 핵심 권한이 있습니다. 자신이 만든 에셋을 편집하고 삭제할 수도 있습니다. GenStudio for Performance Marketing은 수백 개의 컨텐츠를 빠르게 만들 수 있도록 지원합니다. 이러한 사용자는 특정 마케팅 캠페인의 요구 사항을 충족하도록 승인된 콘텐츠의 개별 조각을 오케스트레이션하는 콘텐츠 조각 또는 전체 경험을 생성할 수 있습니다.

편집자는 _확인_&#x200B;을 통해 GenStudio for Performance Marketing 생성 AI 기술과 상호 작용합니다. 캔버스의 프롬프트 서랍에서는 특정 캠페인 지침의 컨텍스트에 프롬프트를 배치할 수 있는 도구를 제공합니다. 따라서 생성된 콘텐츠의 품질과 성공은 조직이 업로드한 브랜드 지침의 품질과 프롬프트의 특수성에 따라 부분적으로 달라집니다. [유효한 프롬프트 쓰기](effective-prompts.md)를 참조하십시오.

다음 표에는 기본 편집기 권한이 표시됩니다.

| 기능 | 만들기 | 업데이트 | 삭제 | 보기 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Campaigns] | 예 | 예 | 예 | 예 |
| [!DNL Content] | 예 | 예 | 예 | 예 |
| [!DNL Create] | 예 | 예 | 예 | 예 |
| [!DNL Insights] | ad 커넥터만 구성할 수 있음 |    |     | 예 |
| [!DNL Personas] | 예 | 예* | 예* | 예 |
| [!DNL Products] | 예 | 예* | 예* | 예 |
| [!DNL Reviews and approvals] | 예 | 예 | 예 | 예 |

편집자는 만든 [!DNL Personas] 및 [!DNL Products]을(를) 편집하고 삭제할 수 있습니다.

GenStudio 시스템 관리자는 편집자에게 [!DNL Brand]을(를) 편집하고 삭제할 권한을 부여할 수 있습니다.

### GenStudio 공동 작업자

_공동 작업자_&#x200B;는 GenStudio for Performance Marketing에서 자산을 볼 수 있지만 이러한 자산을 만들거나 편집하거나 삭제할 수는 없습니다. 공동 작업자에는 콘텐츠에 대한 검토 및 승인 프로세스의 성공에 필수적이지만 콘텐츠를 만들거나 직접 편집할 필요가 없는 관련자가 포함됩니다. 법률전문가와 창작 경영자는 잠재적 공동 작업자의 사례이다. GenStudio for Performance Marketing 공동 작업자는 다른 Creative Cloud 제품에서 에셋을 만들고 볼 수 있는 권한을 가질 수 있습니다.

다음 표에는 기본 공동 작업자 권한이 표시됩니다.

| 기능 | 만들기 | 업데이트 | 삭제 | 보기 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Campaigns] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Content] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Create] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Insights] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Personas] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Products] | 아니요 | 아니요 | 아니요 | 예 |
| [!DNL Reviews and approvals] | 아니요 | 아니요 | 아니요 | 예 |

### GenStudio 시스템 관리자

_GenStudio 시스템 관리자_&#x200B;에게는 GenStudio for Performance Marketing 내에서 가장 강력한 권한 집합이 있습니다. 시스템 관리자는 캠페인 자산 생성 및 배포를 위한 기본 가드레일을 설정하는 필수 온보딩 작업을 수행합니다. 시스템 관리자는 [브랜드 지침](./guidelines/overview.md)과 같은 브랜드 및 조직별 정보를 업로드하여 이러한 보호 기능을 구현합니다. 시스템 관리자에게는 [!DNL Brands]을(를) 만들고 게시할 수 있는 권한이 있지만 사용자 관리 권한이 없습니다.

다음 표에는 기본 시스템 관리자 권한이 표시됩니다.

| 기능 | 만들기 | 업데이트 | 삭제 | 보기 |
|-----------|----------------|----------------|----------------|----------------|
| [!DNL Brands] | 예 | 예 | 예 | 예 |
| [!DNL Campaigns] | 예 | 예 | 예 | 예 |
| [!DNL Content] | 예 | 예 | 예 | 예 |
| [!DNL Insights] | 예 | 예 | 예 | 예 |
| [!DNL Personas] | 예 | 예 | 예 | 예 |
| [!DNL Products] | 예 | 예 | 예 | 예 |
| [!DNL Reviews and approvals] | 예 | 예 | 예 | 예 |

사전 설정 작업에 대한 개요는 [Adobe GenStudio for Performance Marketing 시작하기](get-started.md)를 참조하십시오.