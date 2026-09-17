---
title: 활성화 워크플로
description: 광고 경험을 위한 활성화 워크플로에 대해 알아봅니다.
feature: Ad Activation
exl-id: 17e1bade-d52a-4953-a85c-c10d093e73d6
TQID: https://experienceleague.adobe.com/HSwFeL1qCzgFao2Ii64Hx-kaADRnd3dxaswFMzJ7nfA
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
    internal-label: GenStudio for Performance Marketing
feature_v2:
  - id: c95c94c1-727b-457a-9184-a4dda4c95ab2
    internal-label: Insights
  - id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3a
    internal-label: Create
  - id: f71bd2fc-e9ca-4cb6-8088-82e250211e32
    internal-label: Guidelines
subfeature_v2:
  - id: a98e0185-3180-4e8c-8f31-f72af4cc21a2
    internal-label: Assets
  - id: dd48f9df-f2e2-49fe-a918-332a8e240ffe
    internal-label: Channels
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: c8d964aa325aee782c175abf3fce880fb17ae6ca
workflow-type: tm+mt
source-wordcount: '1250'
ht-degree: 1%
---
# 활성화 워크플로

[!DNL Activate]이(가) 유료 광고 플랫폼에 게시된 경험을 활성화합니다. GenStudio for Performance Marketing 경험은 유료 광고 플랫폼의 특정 대상자를 위해 준비된 광고와 같은 마케팅 캠페인 구성 요소입니다. 활성화 경험에는 세 가지 주요 구성 요소가 포함되어 있습니다.

* **미디어 자산**: 광고 환경의 이미지 또는 비디오이며, 플랫폼과 형식에 따라 파일 형식과 종횡비가 다릅니다.

* **텍스트**: 헤드라인, 본문, call-to-action 요소 등 광고에 포함된 모든 형식의 복사본입니다.

* **메타데이터**: 성능 분석, 필터링 및 추적을 향상시키는 사용자 정의 특성(일반적으로 광고 대상자에게 표시되지 않음)입니다.

활성화하기 전에 [!DNL Content]에서 이러한 구성 요소를 준비하고 승인합니다. [!DNL Activate]은(는) 승인된 에셋, 헤드라인 또는 본문 복사본을 만들거나 편집하지 않습니다. 각 플랫폼에 필요한 설정만 적용한 다음 경험을 게시합니다.

단일 활성화 표에는 여러 유료 광고 플랫폼 및 광고 형식에 대한 경험이 포함될 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/3503543?captions=kor&learn=on)

## 플랫폼 계정 연결

해당 플랫폼에 경험을 활성화하려면 먼저 GenStudio 시스템 관리자 또는 편집기가 각 유료 광고 플랫폼에 대한 광고 계정을 연결해야 합니다. 이 프로세스의 단계를 보려면 [유료 미디어 계정 연결](/help/user-guide/connectors/connect-channel.md)을 참조하십시오.

## 활성화 시작

다음 두 진입점 중 하나에서 활성화를 시작합니다.

* **시작:[!DNL Content]**: 경험으로 필터링하고 게시된 경험을 한 개 이상 선택한 다음 맨 위의 작업 표시줄에서 **[!UICONTROL 활성화]**&#x200B;를 클릭합니다.

  ![콘텐츠에서 게시된 경험을 선택하고 [활성화]를 클릭하여 활성화를 시작합니다](./images/content-select-activate.png)

* [!DNL Activate]&#x200B;**에서**: [!DNL Activate] 랜딩 페이지에서 **[!UICONTROL + 새 활성화]**&#x200B;를 클릭합니다. 이렇게 하면 동일한 경험 갤러리가 열리고 활성화할 경험을 선택합니다.

두 경우 모두 경험 이름으로 검색하거나, 여러 채널로 필터링하여 원하는 경험을 찾습니다.

선택 항목에 디스플레이 형식 경험이 포함된 경우 사용할 디스플레이 플랫폼(Google Campaign Manager 360, Innovid, Amazon Ads 또는 The Trade Desk)을 지정합니다. **[!UICONTROL 활성화 시작]**&#x200B;을 클릭합니다. Meta, LinkedIn, TikTok, YouTube 및 ChatGPT와 같은 다른 형식의 경우 [!DNL Activate]은(는) 경험의 채널에서 플랫폼을 유추하고 이 단계를 건너뜁니다.

[!DNL Activate]은(는) 선택한 모든 경험을 나열하는 활성화 테이블을 생성합니다.

![새로 생성된 활성화 테이블은 Meta 및 LinkedIn 하위 테이블로 그룹화되고 모든 광고에는 해당 필드가 완료될 때까지 주의가 필요합니다.](./images/activation-table.png)

[!DNL Activate]은(는) 광고 형식 및 플랫폼(예: Meta 단일 이미지 또는 LinkedIn 단일 이미지)별로 테이블을 하위 테이블로 구성합니다. 각 행은 하나의 광고를 나타냅니다. LinkedIn, TikTok 및 디스플레이 플랫폼과 같은 대부분의 플랫폼에서 여러 종횡비의 경험이 종횡비당 하나의 행을 생성합니다. 필요하지 않은 행은 모두 삭제합니다. Meta은 예외입니다. Meta 광고는 단일 광고 내에 여러 종횡비를 포함할 수 있으므로 다중 종횡비 Meta 경험은 여전히 하나의 행만 생성합니다.

## 활성화 테이블 관리

활성화 테이블이 열리면 자동으로 초안으로 저장됩니다. 게시하기 전에 언제든지 초안을 떠났다가 다시 시작할 수 있습니다.

이미 연 활성화 테이블에 경험을 추가하려면 테이블의 오른쪽 상단에서 **[!UICONTROL 경험 추가]**&#x200B;를 클릭합니다. [!DNL Activate]이(가) 기존 표에 추가하는 추가 경험을 선택할 수 있도록 경험 갤러리가 다시 열립니다.

**[!UICONTROL 경험을 더 추가]**&#x200B;하면 같은 테이블에 있는 두 개 이상의 디스플레이 플랫폼을 활성화할 수도 있습니다. 디스플레이 형식 경험에서는 먼저 단일 디스플레이 플랫폼을 선택해야 하지만 **[!UICONTROL 경험 추가]**&#x200B;를 클릭하고 더 많은 디스플레이 형식 경험을 선택한 다음 표에 있는 것과 다른 디스플레이 플랫폼을 선택할 수 있습니다. 예를 들어 이미 Innovid 광고가 포함된 테이블에 The Trade Desk 광고를 추가할 수 있습니다.

테이블에 적합한 경험이 있으면 다음에 각 광고의 필드를 구성합니다.

## 광고 및 플랫폼 설정 세부 정보 구성

행별로 인라인으로 필드를 편집하거나 동일한 형식 테이블 내에서 여러 행을 선택하고 도구 모음에서 **[!UICONTROL 세부 정보 편집]**&#x200B;을 클릭하면 해당 필드가 한 번에 대량 편집됩니다.

![세부 정보 또는 플랫폼 설정을 일괄 편집하려면 활성화 테이블에서 여러 광고 선택](./images/bulk-edit-action-bar.png)

승인된 자산, 헤드라인 및 본문 복사본이 잠겨 있으며 [!DNL Content]에서 이미 검토 및 승인을 받았으므로 활성화 테이블에서 편집할 수 없습니다. 나머지 필드는 편집할 수 있으며 플랫폼에 따라 다릅니다. [!DNL Activate]에는 선택한 플랫폼 및 형식과 관련된 열만 표시됩니다. 아래 표를 플랫폼별로 편집할 수 있는 내용에 대한 참조로 사용하십시오.

플랫폼별 **편집 가능한 필드**

| Platform | 지원되는 형식 | 잠긴 사본 | 편집 가능한 텍스트 필드 | 편집 가능한 플랫폼 설정 필드 |
|---|---|---|---|---|
| Meta | 이미지, 비디오, 회전 메뉴 | 제목, 본문 | 설명, Call-to-action, 대상 URL, URL 매개 변수, 추적 ID | 광고 계정, Facebook 페이지, Instagram 프로필, Meta 캠페인, Meta 광고 세트 |
| LinkedIn | 단일 이미지, 단일 비디오 | 헤드라인, 소개 텍스트 | 설명, Call-to-action, 대상 URL, URL 매개 변수, 추적 ID | 광고 계정, 캠페인, 광고 세트 |
| Google Campaign Manager 360 | 정적 디스플레이, 비디오 디스플레이, HTML5 Zip 디스플레이 | 해당 없음 | 추적 ID | 광고주 |
| Amazon 광고 | 정적 디스플레이 | 해당 없음 | 추적 ID | 계정 |
| 이노비드 | 정적 디스플레이, HTML5 Zip 디스플레이 | 해당 없음 | 추적 ID | 계정, Creative 라이브러리, 개념 이름 |
| TikTok | 인피드 비디오 광고 | 기본 텍스트 | Call-to-action, 대상 URL, 추적 ID | 광고 계정, 캠페인, 광고 그룹 |
| YouTube | Google Ads Demand Gen 캠페인의 Shorts | 설명 | Call-to-action, 비즈니스 이름, 대상 URL, URL 매개 변수, 추적 ID | 계정, 캠페인, 광고 그룹, 로고 |
| ChatGPT | 채팅 카드 | 제목, 본문 | 대상 URL, 추적 ID | OpenAI 광고 계정, OpenAI 캠페인, OpenAI 광고 그룹 |
| 트레이드 데스크 | 정적 디스플레이 | 해당 없음 | 추적 ID | 계정, 캠페인 |

광고 형식 그룹에 대한 플랫폼 설정 필드를 구성하려면 **[!UICONTROL 플랫폼 설정 관리]**&#x200B;를 클릭하고 결과 대화 상자에서 필드를 편집합니다.

![Meta 광고 계정, 캠페인 및 광고 집합을 선택하는 플랫폼 설정 관리 대화 상자](./images/manage-platform-settings.png)

**[!UICONTROL 추적 ID]** 필드는 처음에 비어 있습니다. 추적 ID는 광고 플랫폼의 광고 이름 또는 크리에이티브 이름과 동일하며 광고 플랫폼에서는 이 ID를 광고의 식별 이름으로 사용합니다. 이 필드를 사용하여 보고 및 문제 해결을 위한 광고를 식별합니다. **[!UICONTROL 추적 ID]** 필드에 사용할 값을 입력하십시오.

![활성화 테이블에서 추적 ID 필드 인라인 편집](./images/tracking-id-edit.png)

**[!UICONTROL 추적 ID]** 필드 사이를 보다 빠르게 이동하려면 다음 키보드 단축키를 사용하십시오.

* 선택한 **[!UICONTROL 추적 ID]**&#x200B;에 대한 편집 필드를 열려면 **Enter**&#x200B;를 누르십시오.
* **위쪽** 또는 **아래쪽** 화살표 키를 눌러 해당 열의 이전 또는 다음 **[!UICONTROL 추적 ID]** 필드로 이동합니다.
* 편집을 저장하려면 **Enter**&#x200B;를 다시 누르십시오.

## 경험을 검토하고 해당 광고 플랫폼에 게시합니다.

모든 행에 [!UICONTROL 활성화 준비]가 표시되는지 확인합니다. [!DNL Activate] 플래그 누락되었거나 잘못된 필드, 호환되지 않는 작업 호출 및 중복 추적 ID가 [!UICONTROL 주의가 필요합니다]. 모든 행이 준비되면 **[!UICONTROL 플랫폼으로 보내기]**&#x200B;를 클릭하고 게시 대화 상자에서 확인하십시오.

![모든 행에 활성화 준비 완료, 플랫폼으로 보내기 기능이 표시되는 활성화 테이블](./images/ready-to-activate.png)

[!DNL Activate]은(는) 각 광고의 상태를 거의 실시간으로 보고합니다. [보류 중], [플랫폼으로 전송] 또는 [실패]입니다. 광고가 실패하면 해당 상태 위로 마우스를 가져가 플랫폼의 오류를 확인합니다. 각 광고를 개별적으로 다시 시도하지 않고 **[!UICONTROL 다시 시도]**&#x200B;를 클릭하여 테이블의 실패한 모든 광고를 한 번에 다시 시도할 수 있습니다. 플랫폼에 이미 전송된 행은 재제출에서 잠기고 대상 플랫폼의 기본 광고 관리자에 광고에 대한 딥링크를 포함합니다. 최종 게시 전 검토 및 광고 시작은 대상 플랫폼의 자체 광고 관리자에서 수행됩니다. [!DNL Activate]은(는) 항상 비활성 상태의 광고를 제공합니다.

![게시 후 보류 중 및 플랫폼으로 전송됨 상태의 혼합을 보여 주는 활성화 테이블](./images/activation-status-pending.png)

활성화 표가 [!DNL Activate] 랜딩 페이지에 나타납니다.

## 지원되는 플랫폼

각 유료 광고 플랫폼에는 특정 설정 필드 및 사전 요구 사항이 있습니다. 활성화 지침에 대한 유료 광고 플랫폼 선택:

* [Meta](activate-meta-ad.md)
* [LinkedIn](activate-linkedin-ad.md)
* [Google 캠페인 관리자 360](activate-cm360-ad.md)
* [Amazon 광고](activate-amazon-ad.md)
* [Innovid](activate-innovid-ad.md)
* [TikTok](activate-tiktok-ad.md)
* [YouTube](activate-youtube-ad.md)
* [ChatGPT](activate-chatgpt-ad.md)
* [무역 담당](activate-trade-desk-ad.md)
