---
title: Meta 광고 활성화
description: Meta 광고 경험을 활성화하는 방법을 알아봅니다.
feature: Ad Activation
exl-id: 157df612-a774-422c-bca3-2fde9e9d1c88
TQID: https://experienceleague.adobe.com/hDR0ngNiGnCXCCOgNhVG8gX4kHGrNvfybPbuMLwYk7U
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
    internal-label: GenStudio for Performance Marketing
feature_v2:
  - id: bffd9bc2-7f41-4bf6-9f08-f14cbd37afd7
    internal-label: Campaigns
  - id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3a
    internal-label: Create
  - id: f71bd2fc-e9ca-4cb6-8088-82e250211e32
    internal-label: Guidelines
subfeature_v2:
  - id: d87258a7-722c-4afd-b632-adddc447c7aa
    internal-label: Ad activation
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
source-wordcount: '382'
ht-degree: 0%
---
# Meta 광고 활성화

Adobe GenStudio for Performance Marketing은 Instagram 및 Facebook에 대한 Meta 광고 경험 활성화를 지원합니다.

**지원되는 형식**: 이미지, 비디오, 회전 메뉴.

GenStudio for Performance Marketing에서 [Meta 경험을 만들기](/help/user-guide/create/create-meta-ad.md)한 다음 활성화하도록 선택하십시오.

Meta 광고를 활성화하면 다른 유료 광고 채널로의 활성화에 필요한 [동일한 일반 단계](create-activation.md)를 따릅니다. 이 페이지에서는 Meta 관련 사전 요구 사항 및 설정 필드를 다룹니다. GenStudio for Performance Marketing에서 Meta 환경을 활성화한 후 [Meta Ads Manager](https://adsmanager.facebook.com/)를 사용하여 환경을 검토하고 광고를 시작합니다.

일부 다른 채널과 달리 Meta 광고는 단일 광고 내에 여러 종횡비를 포함할 수 있습니다. 경험에 종횡비가 여러 개인 경우 [!DNL Activate]은(는) 종횡비에 한 행이 아닌 한 행만 생성합니다.

GenStudio 시스템 관리자 및 편집자는 광고 경험을 활성화할 수 있습니다.

## 사전 요구 사항

연결된 Meta 광고 계정에 Meta 광고 플랫폼의 이러한 구성 요소에서 광고를 관리할 수 있는 모든 권한이 있는지 확인합니다.

* Meta 광고 계정
* Facebook 페이지
* Meta campaign
* Meta 광고 세트
* Instagram 프로필(선택 사항)

대상 Meta 캠페인 및 광고 세트는 Meta Ads Manager에 이미 있어야 합니다. GenStudio for Performance Marketing은 현재 캠페인이나 광고 세트를 생성하지 않습니다.

## Meta 계정 연결

조직에서 경험을 활성화하려면 먼저 GenStudio 시스템 관리자가 Meta 계정을 GenStudio for Performance Marketing에 연결해야 합니다. 이 연결을 통해 GenStudio for Performance Marketing과 Meta 간에 데이터를 전송하여 활성화 프로세스를 사용할 수 있습니다. [Meta 광고에 연결](/help/user-guide/connectors/meta-ads.md)을 참조하세요.

Instagram 계정을 선택하려면 Meta Business Manager에서 사용할 Instagram 계정이 온보딩 중에 선택한 [동일한 광고 계정](/help/user-guide/connectors/meta-ads.md#connect-an-instagram-account)에 연결되어 있는지 확인하십시오. 이 연결이 누락된 경우 활성화 중에 Instagram 계정이 **[!UICONTROL Instagram 프로필]** 드롭다운 메뉴에 나타나지 않을 수 있습니다.

동기화가 완료되면 추가된 계정을 볼 수 있습니다. 대량의 데이터를 동기화하는 데 시간이 더 오래 걸립니다.

## Meta 설정 필드

승인된 자산, 헤드라인 및 본문 복사본이 잠겨 있으며 [!DNL Content]에서 이미 검토 및 승인을 받았으므로 활성화 중에 편집할 수 없습니다. 다음을 편집할 수 있습니다.

* **텍스트 필드**: 설명, Call-to-action, 대상 URL, URL 매개 변수, 추적 ID(Meta 광고 이름으로 사용됨)
* **플랫폼 설정 필드**: 광고 계정, Facebook 페이지, Instagram 프로필, Meta 캠페인, Meta 광고 집합
