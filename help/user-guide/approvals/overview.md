---
title: Adobe GenStudio for Performance Marketing 검토 및 승인
description: GenStudio for Performance Marketing 검토 및 승인 프로세스에 대해 알아봅니다.
feature: Approval
exl-id: c83f47c0-e8ae-4c54-84b3-c50f67d6b3c2
source-git-commit: ce08231cb723bec3d80a732837b72a435d3b552d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Adobe GenStudio for Performance Marketing 검토 및 승인

검토 및 승인 작업 과정을 통해 크리에이티브 팀에서 법률 전문가에 이르기까지 모든 이해 당사자가 생성 AI가 제작한 브랜드 에셋을 비롯한 캠페인 에셋 및 경험을 효율적으로 검토하고 승인할 수 있습니다.

## [!DNL Review and Approval]개의 워크플로우 이점

* **강력한 반복 생성 AI 콘텐츠 만들기 지원**. 조직에서 브랜드 중심 콘텐츠를 만들고 배포하는 것은 매우 반복적인 프로세스입니다. GenStudio for Performance Marketing 생성 AI 기능은 수백 개의 자산 변형을 신속하게 만들 수 있도록 지원합니다. 각 검토자는 자산 초안을 승인하기 전에 여러 번 변경을 요청할 수 있습니다. 검토자가 많을수록 모든 관련자가 최종 변형에 동의하기 전에 잠재적 반복 횟수가 증가합니다.

* **창의적 무결성 지원**. 승인은 콘텐츠 크리에이터가 승인 프로세스에 참여하도록 하여 브랜드 자산의 창의적 무결성을 보호합니다. 검토 및 승인 프로세스에 크리에이티브 관련자(예: 콘텐츠 크리에이터 및 크리에이티브 디렉터)를 참여시킴으로써 최종 출력이 비전 및 브랜드 정체성에 부합하도록 합니다.

* **캠페인 목표 및 법적 요구 사항 준수**. 승인 프로세스는 콘텐츠가 캠페인 목표를 지원하는지 확인하는 데 도움이 됩니다. 모든 마케팅 자료가 법률 및 규제 표준을 준수하도록 하여 위험과 잠재적인 법적 문제를 최소화합니다.

## 검토 및 승인 주기

검토 및 승인 워크플로의 주요 단계는 다음과 같습니다.

* [만든 콘텐츠에 대한 검토 및 승인 요청](./request-review.md)
* [콘텐츠 검토 및 편집](./review-and-edit.md)
* [콘텐츠 승인](./approve-content.md)
* [콘텐츠 게시](./publish-content.md)

## 검토를 요청하거나 콘텐츠를 승인할 수 있는 사람은 누구입니까?

에셋 또는 경험을 만든 경우 조직의 승인 체인에 있는 다른 사용자에게 공식적으로 작업을 검토하고 주석을 달도록 요청할 수 있습니다. GenStudio for Performance Marketing 조직 구성원은 초안을 검토할 수 있지만, 지정된 승인자만 초안에 대해 댓글을 달거나 승인할 수 있습니다.

## [!DNL Content]개 초안 정보

_초안_&#x200B;은(는) 검토 및 승인 프로세스를 거치지 않은 자산 또는 경험의 예비 버전입니다. 초안 상태는 검토 및 승인 프로세스에서 초안이 어디에 있는지 식별합니다. 고유한 초안 ID는 각 초안을 식별합니다. 초안을 승인하고 [!DNL Content]에 게시하기 전까지 ID가 유효합니다. 초안에 대한 검토 주석 및 승인이 이 개별 초안 ID와 연결됩니다.

초안이 검토 및 승인 프로세스를 완료하고 [!DNL Content]에 게시되면 초안 ID가 만료되고 GenStudio for Performance Marketing에서 관련 주석 및 승인 상태를 저장하지 않습니다. 초안 URL이 더 이상 유효하지 않습니다.

초안 상태는 검토 및 승인 프로세스를 진행할 때 컨텐츠 초안의 상태를 캡처합니다. 검토 중인 에셋을 만든 GenStudio for Performance Marketing 콘텐츠 편집기는 초안 또는 승인에 대해 요청된 변경 사항에 대한 알림을 받습니다. 승인자는 초안 상태를 변경하여 초안에 추가 개정이 필요한지 또는 승인할 수 있는지 여부를 나타냅니다. 모든 지정된 승인자는 에셋 또는 경험을 게시하기 전에 승인해야 합니다.

사용 가능한 초안 상태:

**알림**: 콘텐츠 편집기가 승인자에게 초안을 검토할 준비가 되었음을 알려 검토 및 승인 프로세스를 시작했습니다.
**작업 필요**: 하나 이상의 승인자가 콘텐츠 초안에 대한 변경을 요청했음을 나타냅니다. 이 상태의 콘텐츠를 [!DNL Content]에 저장할 수 없습니다.
**승인됨**: 모든 지정 승인자가 자산 또는 경험을 승인했습니다. 이제 콘텐츠 편집기에서 에셋 또는 경험에 메타데이터를 추가하고 [!DNL Content]에 저장할 수 있습니다.

## 알림

GenStudio for Performance Marketing 제품 내 알림은 자산 상태 변경 및 `@mention`개의 댓글을 실시간으로 승인자 및 콘텐츠 편집자를 업데이트합니다. 알림은 여러 검토, 편집 및 승인 주기를 통해 신속한 반복을 지원합니다.

콘텐츠 편집자 및 승인자는 Slack에서 이러한 알림을 수신하기 위해 등록할 수 있습니다. [Experience Cloud에서 서비스 구독](https://experienceleague.adobe.com/en/docs/core-services/interface/features/account-preferences#slack)을 참조하세요.

승인 참가자가 취한 작업은 자동 제품 내 알림 및 이메일 알림을 트리거합니다. 승인 프로세스를 시작하면 지정된 승인자가 이메일과 제품 내 알림을 모두 받습니다. 승인자가 `@mention`개의 댓글을 추가하거나 결정을 내릴 때마다 제품 내 및 이메일 알림이 반복됩니다. 알림에는 콘텐츠 초안에 대한 링크가 포함되어 있습니다.

콘텐츠에 대한 검토 및 승인 프로세스를 시작한 경우 모든 승인 및 검토 의견에 대한 공지가 표시됩니다. 그러나 승인자에게는 `@mention`이(가) 포함된 댓글만 표시됩니다.