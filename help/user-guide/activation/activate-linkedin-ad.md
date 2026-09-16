---
title: LinkedIn 광고 활성화
description: LinkedIn 광고 경험을 활성화하는 방법을 알아봅니다.
feature: Ad Activation
exl-id: edc95319-36c3-4cbf-a5c0-865b49482b50
TQID: https://experienceleague.adobe.com/1mcxWePqYd8tYp3e1D2UTSeBHSvPj4WrqeSyiUCxD8c
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
    internal-label: GenStudio for Performance Marketing
feature_v2:
  - id: bffd9bc2-7f41-4bf6-9f08-f14cbd37afd7
    internal-label: Campaigns
  - id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3a
    internal-label: Create
subfeature_v2:
  - id: e3878dde-4b87-4290-9e81-ed7ee6eb83fe
    internal-label: Experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
source-git-commit: 17b2262615e10d82905ce7ebec65857e9a0b9f2a
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%
---
# LinkedIn 광고 활성화

Adobe GenStudio for Performance Marketing은 [LinkedIn 캠페인 관리자](https://business.linkedin.com/marketing-solutions)에 대한 LinkedIn 광고 경험의 활성화를 지원합니다.

**지원되는 형식**: 단일 이미지, 단일 비디오입니다.

GenStudio for Performance Marketing에서 [LinkedIn 경험을 만들기](/help/user-guide/create/create-linkedin.md)한 다음 활성화하도록 선택할 수 있습니다.

LinkedIn 광고를 활성화하면 다른 유료 광고 채널로의 활성화에 필요한 [동일한 일반 단계](create-activation.md)가 따릅니다. 이 페이지에서는 LinkedIn 관련 사전 요구 사항 및 설정 필드를 다룹니다. GenStudio for Performance Marketing에서 LinkedIn 경험을 활성화한 후 LinkedIn Campaign Manager를 사용하여 경험을 검토하고 광고를 시작합니다.

GenStudio 시스템 관리자 및 편집자는 광고 경험을 활성화할 수 있습니다.

## 사전 요구 사항

* 캠페인 및 광고를 관리할 수 있는 전체 권한이 있는 LinkedIn Campaign Manager 계정입니다. 이 계정에는 기존 캠페인이 포함되어야 합니다.
* 광고를 만들고 LinkedIn 페이지에 콘텐츠를 게시할 수 있는 전체 권한이 있는 LinkedIn 광고 계정입니다.

대상 LinkedIn 캠페인 및 광고 세트가 LinkedIn 캠페인 관리자에 이미 있어야 합니다. GenStudio for Performance Marketing은 캠페인이나 광고 세트를 생성하지 않습니다.

>[!NOTE]
>
>LinkedIn이 캠페인 계층 이름을 변경했습니다. 이전에 LinkedIn Campaign Manager가 **캠페인 그룹**&#x200B;이라고 불렀던 것이 이제 **campaign**&#x200B;이라고 불렸으며, 이전에 **campaign**&#x200B;이라고 불렀던 것이 이제 **광고 집합**&#x200B;이라고 했습니다. [!DNL Activate]의 **[!UICONTROL LinkedIn 캠페인]** 및 **[!UICONTROL LinkedIn 광고 집합]** 설정 필드에서 이 최신 용어를 사용합니다.

GenStudio for Performance Marketing은 현재 단일 이미지 및 단일 비디오 LinkedIn 광고를 지원하며, 각 광고는 게시물당 하나의 이미지 또는 비디오만 전달합니다. 경험에 여러 종횡비가 포함된 경우 [!DNL Activate]은(는) 활성화 테이블에서 비율별로 별도의 행을 생성하여 각 행을 고유한 광고로 실행할 수 있도록 합니다. 필요하지 않은 행은 모두 삭제하십시오.

## LinkedIn 계정 연결

조직에서 경험을 활성화하려면 먼저 GenStudio 시스템 관리자 또는 편집기가 LinkedIn 광고 계정을 GenStudio for Performance Marketing에 연결해야 합니다. 연결하려면 광고 계정과 LinkedIn 프로필 페이지에 대한 전체 관리자 액세스 권한이 있어야 합니다. **[!UICONTROL 설정]**&#x200B;에서 광고 계정을 한 번만 연결하면 됩니다. 그 후에는 해당 인스턴스에 액세스할 수 있는 모든 사용자가 사용할 수 있습니다.

이 연결을 통해 GenStudio for Performance Marketing과 LinkedIn 간에 데이터를 이동할 수 있으므로 활성화 프로세스가 활성화됩니다.

동기화가 완료되면 추가된 계정을 볼 수 있습니다. 대량의 데이터를 동기화하는 데 시간이 더 오래 걸립니다.

## LinkedIn 설정 필드

승인된 에셋, 헤드라인 및 소개 텍스트가 잠겨 있으며 [!DNL Content]에서 이미 검토 및 승인을 받았으므로 활성화 중에 편집할 수 없습니다. 다음을 편집할 수 있습니다.

* **텍스트 필드**: 설명, Call-to-action, 대상 URL, URL 매개 변수, 추적 ID(플랫폼 광고 이름으로 사용됨)
* **플랫폼 설정 필드**: LinkedIn 광고 계정, LinkedIn 캠페인, LinkedIn 광고 집합
