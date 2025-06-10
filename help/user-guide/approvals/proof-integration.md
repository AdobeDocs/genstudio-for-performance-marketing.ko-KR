---
title: 검토 및 승인과 Workfront Proof 통합
description: Adobe GenStudio for Performance Marketing과 Workfront Proof 통합.
feature: Content Review, Content Management
source-git-commit: f8508ee9440714137141e933cfe0f5761a510c7a
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# GenStudio for Performance Marketing과 Workfront Proof 통합

Workfront Proof과 통합하면 승인 템플릿, 다단계 워크플로, [증명 버전 비교](https://experienceleague.adobe.com/en/docs/workfront/using/workfront-proof/work-with-proofs-in-wf-proof/review-proofs-web-proofing-viewer/compare-proofs)를 비롯한 고급 기능을 통해 GenStudio for Performance Marketing 검토 및 승인 수명 주기가 향상됩니다. 이러한 구조화된 버전 관리는 컨텐츠 검토 수명주기 전반에 걸쳐 투명성, 신뢰성 및 능률적인 협업을 보장합니다.

>[!BEGINSHADEBOX]

**필수 구성 요소**:

[Adobe Workfront 웹 뷰어 확장 설치](https://experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/proofing/review-proofs-in-workfront/review-a-proof/review-proof-in-web-viewer-extension)

>[!ENDSHADEBOX]

Workfront Proof [!DNL Proofing Viewer]은(는) 증명을 보고, 댓글을 달고, 비교할 수 있는 풍부한 작업 영역입니다. [!DNL Proofing Viewer]에서 다음을 수행할 수 있습니다.

* 콘텐츠의 다른 버전 비교
* 증명에 주석 및 그리기 마크업 추가
* 증명 승인

승인 요청 전자 메일 또는 제품 내 알림에서 증명 URL을 클릭하면 [!DNL Proofing Viewer]이(가) 로드됩니다. [!DNL Proofing Viewer] _내 새 승인_ 보기가 열립니다. 이 보기에서 핵심 [!DNL Proofing Viewer] 주석 도구를 사용하여 콘텐츠를 검토하고 주석을 제공할 수 있습니다.

[!DNL Proofing Viewer]을(를) 종료하려면 **[!UICONTROL GenStudio으로 돌아가기]**&#x200B;를 클릭하세요.

## Genstudio for Performance Marketing 및 Workfront Proof: 기능 비교

아래 표는 표준 GenStudio for Performance Marketing 검토 및 승인 기능을 Workfront Proof 통합을 통해 사용할 수 있는 고급 기능과 비교합니다.

| 기능        | GenStudio for Performance Marketing                                                                 | Workfront Proof                                                                 |
|-------------------------------|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| **초안/증명 수명 주기**        | 초안 콘텐츠는 게시 후 만료됩니다. | 타임스탬프가 지정된 영구 로그가 있는 다단계의 역할 기반 승인 체인입니다.<br> 모든 버전이 무기한으로 유지됩니다. |
| **댓글**                | 주석은 초안 ID에 연결되어 있으며 게시 후 삭제됩니다.                                           | 지속적인 주석 및 주석은 감사 및 규정 준수를 위해 유지됩니다.     |
| **버전**           | 초안은 고유한 인스턴스로 처리됩니다.<br>병렬 비교가 없습니다.                                      | 병렬 및 오버레이 비교 도구를 사용하여 전체 버전을 제어할 수 있습니다.        |
| **프로젝트 관리** | 기본 캠페인 관리. | 사용자 정의, 템플릿, 보고 및 상세 감사를 포함한 전체 캠페인 라이프사이클 관리. |

### 라이선스 및 사용자 역할

라이센스는 제품 내에서 사용자 권한 집합을 식별합니다. Workfront Proof은 GenStudio for Performance Marketing보다 더 많은 라이선스 유형 또는 사용자 역할을 제공합니다. [증명 역할 개요](https://experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/proofing/proofing-overview/proof-roles)에서 Workfront Proof 검토 및 승인 워크플로와 연결된 사용자 역할을 소개합니다.

| GenStudio for Performance Marketing 라이선스       | Workfront 라이선스                 | 설명                                                                                                                                                      |
|---------------------------------------------------|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GenStudio 시스템 관리자                          | Workfront 관리자/고급 사용자 | 브랜드, 사용자 및 제품 관리와 같은 GenStudio Performance Marketing 기능에 대한 전체 액세스 권한. 워크플로우 및 설정을 관리합니다. 승인 템플릿을 만듭니다. |
| 콘텐츠 작성자 및 편집기(Power 사용자 라이센스)   | 증명 작성자(표준 라이선스)  | 콘텐츠 초안을 생성하여 제출합니다. 증명 뷰어에서 에셋을 업로드하고 증명을 시작합니다. Workfront Proof 라이선스가 필요합니다.                              |
| 검토자/승인자(공동 작업자 라이선스)        | 검토자/승인자                 | 다단계 검토에 참여하고, 주석을 추가하고, 콘텐츠를 승인하거나 거부합니다.                                                                             |

Adobe 시스템 관리자는 Adobe Admin Console에서 두 제품에 대한 사용자 프로비저닝 및 권한을 관리합니다.

>[!NOTE]
>
> Workfront Proof은 [추가 사용자 역할](https://experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/proofing/proofing-overview/proof-roles)을 제공합니다. 일부 역할이 성과 마케팅 내부에 표시되는 것은 아닙니다. 그러나 시스템은 Workfront Proof 템플릿 내에 설정된 모든 역할을 수행합니다.

### 초안 및 증명

Workfront [!DNL Proofing Viewer]은(는) 보다 구조화된 검토 및 승인 기능으로 GenStudio for Performance Marketing의 기본 검토 및 승인 프로세스를 확장합니다. 이 통합에서 검토되는 증명은 GenStudio for Performance Marketing에서 지원하는 형식으로 제한됩니다.

### 버전 제어

GenStudio for Performance Marketing은 승인 템플릿을 지원하지 않지만, Workfront Proof은 지원합니다. Proof의 버전 관리 기능은 GenStudio의 콘텐츠 검토 및 승인 프로세스를 크게 향상시킵니다. 증명 워크플로의 각 제출은 콘텐츠 초안 또는 _증명_&#x200B;의 개별 버전으로 처리됩니다. 증명이 자동으로 저장되고 이전 반복과 나란히 비교될 수 있습니다. 이해 당사자는 변경 사항을 추적하고, 정확한 피드백을 제공하고, 검토 주기 전반에 걸쳐 정렬을 유지할 수 있습니다. Proof는 모든 의견, 의사 결정 및 버전에 대한 완전한 기록을 보존하여 감사 준비 및 규정 준수 요구 사항을 지원합니다. 각 버전은 승인, 거부 또는 댓글과 같은 모든 작업에 대해 명확한 로그 및 타임스탬프가 지정된 다단계 역할 기반 승인 워크플로우도 지원합니다.

### 승인 템플릿

Workfront Proof 승인 템플릿은 증명 승인 워크플로를 간소화할 수 있는 사전 형식의 단계를 제공합니다. 이러한 템플릿에는 선택한 검토자와 승인자, 증명 역할 및 마감일이 포함되어 일관성과 효율성을 보장합니다. 검토를 시작하는 콘텐츠 작성자는 단일 단계 및 다중 단계 승인 워크플로 모두에 대해 사전 정의된 템플릿 세트에서 선택할 수 있습니다.

워크플로 템플릿의 각 단계는 할당된 검토자를 식별합니다. Workfront Proof 워크플로의 모든 상태 업데이트 및 의견이 증명 뷰어 내에 표시되므로 투명성과 공동 작업이 향상됩니다.

승인 템플릿은 다양한 이해 관계자 그룹의 검토 조정을 지원하는 다단계 승인을 지원합니다.

### 댓글

검토자는 증명의 특정 영역을 직접 클릭하여 정확하고 상황에 맞는 설명을 남길 수 있습니다. 모든 댓글은 타임스탬프가 지정되며 증명 버전 내역의 일부로 저장됩니다. GenStudio for Performance Marketing에서는 댓글 기록을 사용할 수 없습니다.

[두 버전의 증명을 비교](https://experienceleague.adobe.com/en/docs/workfront/using/workfront-proof/work-with-proofs-in-wf-proof/review-proofs-web-proofing-viewer/compare-proofs)하여 리뷰 댓글과 내용을 평가할 수 있습니다.

## 알림 및 미리 알림

검토에 새 증명을 사용할 수 있거나 진행 중인 검토 상태가 변경된 경우 검토자와 승인자가 이메일 알림을 받습니다.
[증명 알림 및 미리 알림](https://experienceleague.adobe.com/en/docs/workfront/using/workfront-proof/proof-notifications-and-reminders/proof-notifications-and-reminders/proof-notifications-and-reminders)에는 증명에 대한 개인 맞춤화된 링크, 승인 프로세스를 통한 증명 및 진행 상황에 대한 세부 정보 및 버전 관리 정보가 포함되어 있습니다.
