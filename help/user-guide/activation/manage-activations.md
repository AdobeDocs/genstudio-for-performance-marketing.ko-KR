---
title: 활성화 관리
description: Adobe GenStudio for Performance Marketing으로 활성화된 경험을 관리하는 방법을 알아봅니다.
feature: Ad Activation
exl-id: 7cf340d4-37ab-4906-9aad-088a26db0818
TQID: https://experienceleague.adobe.com/ird0IiW8L5Axjj2FmEjlUcD1sPaNCNfxj9XNqGfQWiI
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
    internal-label: GenStudio for Performance Marketing
feature_v2:
  - id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3a
    internal-label: Create
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: 17b2262615e10d82905ce7ebec65857e9a0b9f2a
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 1%
---
# 활성화 관리

활성화 표가 [!DNL Activate] 랜딩 페이지에 나타납니다. 각 표에는 상태와 함께 해당 광고가 나열됩니다.

| 상태 | 의미 |
|---|---|
| [!UICONTROL 주의 필요] | 활성화 테이블의 하나 이상의 광고에 호환되지 않는 call to action 또는 중복 추적 ID와 같은 누락되거나 잘못된 필드가 있습니다. |
| [!UICONTROL 활성화 준비] | 활성화 테이블의 모든 광고가 유효성 검사를 통과하고 게시할 준비가 되었습니다. |
| [!UICONTROL 보류 중] | 전체 활성화 테이블이 제출되었으며 대상 플랫폼에서 처리 중입니다. |
| [!UICONTROL 게시됨] | 전체 활성화 테이블이 게시되었습니다. |
| [!UICONTROL 실패] | 대상 플랫폼이 테이블의 광고 중 하나 이상을 거부했습니다. 플랫폼의 오류 메시지를 보려면 상태 도구 설명에 마우스를 가져다 대십시오. |

오른쪽 상단의 **[!UICONTROL 다시 시도]**&#x200B;를 클릭하여 실패한 활성화를 자동으로 다시 시도할 수 있습니다.

게시된 행은 재제출에서 잠겨 있으며 대상 플랫폼의 기본 광고 관리자에서 광고에 대한 딥링크를 포함하므로 바로 이동하여 검토하거나 시작할 수 있습니다.

## 세부 사항 보기

광고 행을 클릭하여 활성화 세부 사항에 대한 집중 보기를 엽니다. 읽기 전용 세부 사항 보기는 활성화 실패 등 활성화된 광고의 정의 세부 사항을 GenStudio for Performance Marketing 및 대상 플랫폼에서 파생된 정보로 캡처합니다.

* **게시 시간 및 날짜**: 대상 플랫폼에서 게시한 시간 및 날짜
* **광고 ID**: 대상 플랫폼에서 할당되고 추적에 사용되는 ID로, 플랫폼의 기본 광고 관리자에서 게시된 광고에 대한 딥링크가 있습니다.
* **광고 세부 정보**: 승인된 에셋, 복사본 및 광고에 사용된 메타데이터
* **플랫폼 설정**: 광고를 활성화하는 데 사용되는 계정, 캠페인 및 기타 플랫폼 설정 필드

실패한 활성화의 세부 사항 보기에는 실패 이유가 포함됩니다.
