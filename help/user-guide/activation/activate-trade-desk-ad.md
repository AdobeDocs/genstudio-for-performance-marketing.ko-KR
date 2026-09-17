---
title: 트레이드 데스크에 대한 광고 활성화
description: The Trade Desk에 정적 디스플레이 광고 경험을 활성화하는 방법을 알아봅니다.
feature: Ad Activation
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
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
source-git-commit: 17b2262615e10d82905ce7ebec65857e9a0b9f2a
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%
---
# Trade Desk 광고 활성화

Adobe GenStudio for Performance Marketing은 The Trade Desk에 대한 광고 경험 활성화를 지원합니다.

**지원되는 형식**: 정적 표시(단일 자산만 해당).

The Trade Desk에 대한 광고를 활성화하면 다른 유료 광고 채널에 대해 활성화하는데 필요한 [동일한 일반 단계](create-activation.md)를 따르며 한 가지 차이점이 있습니다. 트레이드 데스크는 셀프서비스 광고 플랫폼이 아닌 매니지드 엔터프라이즈 서비스이기 때문에 계정 액세스가 다른 채널과 다르게 작동합니다. 이 페이지에서는 Trade Desk와 관련된 사전 요구 사항 및 설정 필드와 함께 이러한 차이점을 다룹니다.

GenStudio 시스템 관리자 및 편집자는 광고 경험을 활성화할 수 있습니다.

## 사전 요구 사항

* 기존의 라이브 The Trade Desk 계정입니다. GenStudio for Performance Marketing에 연결하기 전에 트레이드 데스크를 통해 직접 설정합니다.
* Trade Desk 계정 팀에서 활성화한 API 액세스입니다. 트레이드 데스크의 경우 계정 팀이 다른 유료 광고 채널에서 사용하는 OAuth 로그인이 아닌 API 토큰을 사용하여 이 액세스를 대신 활성화합니다.
* GenStudio for Performance Marketing 통합을 위해 The Trade Desk가 활성화한 올바른 광고주, 시트 및 권한.
* 광고 크리에이티브를 타겟 광고주 계정에 게시할 수 있는 권한이 있는 Trade Desk 계정 팀의 API 토큰 또는 자격 증명입니다.
* 무역 부서에 이미 존재하는 대상 캠페인입니다. GenStudio for Performance Marketing은 해당 기존 캠페인에 광고를 활성화합니다.

## 트레이드 데스크 계정 연결

조직에서 경험을 활성화하기 전에 Trade Desk 계정 팀과 협력하여 API 액세스를 활성화한 다음 GenStudio 시스템 관리자가 계정을 GenStudio for Performance Marketing에 연결합니다.

1. Trade Desk 계정 팀에 문의하여 GenStudio for Performance Marketing의 크리에이티브를 Trade Desk 계정에 게시하기 위한 액세스 권한을 요청하십시오. 활성화에 사용할 광고주 ID, 시트 또는 파트너 세부 사항을 확인합니다.
1. The Trade Desk 계정 팀으로부터 API 토큰 또는 자격 증명을 획득하고 토큰이 타겟 광고주 계정에 대한 크리에이티브 게시 권한을 지원하는지 확인합니다.
1. GenStudio for Performance Marketing에서 **[!UICONTROL 설정]** > **[!UICONTROL 채널]**(으)로 이동한 다음 **[!UICONTROL 트레이드 데스크]** 타일에서 **[!UICONTROL 연결]**&#x200B;을 클릭합니다. 계정 이름, 광고주 ID, API 토큰 또는 자격 증명을 입력한 다음 연결을 저장합니다.

연결에 실패하는 경우 Trade Desk 계정 팀에 API 액세스가 활성화되었고 토큰에 올바른 광고주 및 시트 권한이 있는지 확인하십시오.

## 트레이드 데스크 설정 필드

승인된 자산은 [!DNL Content]에서 이미 검토 및 승인을 거쳤으므로 활성화 중에 잠겨서 편집할 수 없습니다. 다음을 편집할 수 있습니다.

* **텍스트 필드**: 추적 ID(Platform Creative 이름으로 사용됨)
* **플랫폼 설정 필드**: 계정, 캠페인

현재 Trade Desk에 대한 활성화는 단일 에셋 정적 디스플레이 광고만 지원합니다.
