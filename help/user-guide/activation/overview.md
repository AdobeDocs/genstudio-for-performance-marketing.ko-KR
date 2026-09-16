---
title: 활성화 개요
description: Adobe CX Enterprise 및 타사 애플리케이션을 사용하여 콘텐츠를 활성화하는 방법을 알아봅니다.
level: Beginner
feature: Ad Activation
exl-id: 365fe253-d189-467e-a723-f54cd74ff60b
TQID: https://experienceleague.adobe.com/-Nal0YqjTzKw4g2SM3IuMf0a13e87CWdTqBZPd0dBkU
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
    internal-label: GenStudio for Performance Marketing
feature_v2:
  - id: bffd9bc2-7f41-4bf6-9f08-f14cbd37afd7
    internal-label: Campaigns
  - id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3a
    internal-label: Create
subfeature_v2:
  - id: d87258a7-722c-4afd-b632-adddc447c7aa
    internal-label: Ad activation
  - id: e3878dde-4b87-4290-9e81-ed7ee6eb83fe
    internal-label: Experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
source-git-commit: 17b2262615e10d82905ce7ebec65857e9a0b9f2a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%
---
# Adobe GenStudio for Performance Marketing 활성화

GenStudio for Performance Marketing [!DNL Activate]에서 Meta 또는 LinkedIn과 같은 유료 광고 채널에 광고 경험을 준비하고 보낼 수 있습니다. _활성화_&#x200B;는 승인된 광고 경험과 해당 자산을 가져와서 특정 채널에 필요한 설정을 적용한 다음 비활성, 해제 상태의 해당 채널에 직접 전달합니다. 거기에서 광고가 라이브로 전환되기 전에 채널의 자체 광고 관리자에서 최종 검토를 수행할 수 있습니다.

[!DNL Activate]은(는) 귀하의 경험을 채널에 직접 제공하므로 파일을 내보내거나 채널의 자체 광고 관리자에 수동으로 업로드할 필요가 없습니다.

해당 채널에 광고 경험을 활성화하려면 먼저 GenStudio 시스템 관리자 또는 편집기가 각 유료 광고 채널에 대한 광고 계정을 연결해야 합니다.

## 기능 활성화

[!DNL Activate]을(를) 사용하여 대상 유료 광고 채널에 대한 광고 경험을 준비합니다. 단일 활성화 테이블에서 여러 유료 광고 채널 간에 [경험을 대량으로 활성화](create-activation.md)합니다. 그런 다음 [활성화를 관리](manage-activations.md)하여 활성화된 모든 경험의 상태와 세부 정보를 확인합니다.

>[!VIDEO](https://video.tv.adobe.com/v/3503538?learn=on)

### 콘텐츠에서 승인된 경험 활성화

[!DNL Content]에서 승인되거나 게시된 경험을 하나 이상 선택하거나 [!DNL Activate] 랜딩 페이지에서 시작하십시오. 이전 버전의 [!DNL Activate]과(와) 달리 단일 활성화 테이블에는 광고 형식 및 채널별로 구성된 여러 유료 광고 채널의 경험이 한 번에 포함될 수 있습니다.

>[!NOTE]
>
>[!DNL Content]이(가) **channel**&#x200B;에서 Meta 또는 LinkedIn 같은 대상을 호출합니다. [!DNL Activate]이(가) 동일한 대상을 **platform**&#x200B;로 호출합니다(예: **[!UICONTROL Platform 설치]**&#x200B;에서). 두 용어는 같은 것을 가리킵니다.

### 광고 및 플랫폼 설정 세부 정보 구성

활성화 테이블의 각 행은 하나의 광고를 나타냅니다. 승인된 Creative Assets, 헤드라인 및 본문 사본은 이미 검토 및 승인을 거쳤으므로 잠겨 있습니다. call-to-action 텍스트, 대상 URL 및 광고 계정, 캠페인 및 광고 세트와 같은 플랫폼 설정 세부 정보와 같은 나머지 필드를 편집할 수 있습니다. 한 번에 한 행에 대한 필드를 편집하거나, 여러 행을 선택하여 공유 필드를 일괄적으로 편집합니다.

### 경험을 검토하고 해당 광고 채널에 게시합니다.

모든 행에 [!UICONTROL 활성화 준비]가 표시되는지 확인합니다. [!DNL Activate] 플래그 누락되었거나 잘못된 필드, 호환되지 않는 작업 호출 및 중복 추적 ID가 [!UICONTROL 주의가 필요합니다]. 모든 행이 준비되면 **[!UICONTROL 플랫폼으로 보내기]**&#x200B;를 클릭하여 테이블의 모든 광고를 게시합니다. [!DNL Activate]은(는) 각 광고의 상태를 거의 실시간으로 보고하며 성공적으로 게시된 광고에는 대상 플랫폼의 기본 광고 관리자에 해당 광고에 대한 딥링크가 포함되어 있습니다. 실패한 광고는 오류 메시지를 반환하고 다시 시도할 수 있습니다.
