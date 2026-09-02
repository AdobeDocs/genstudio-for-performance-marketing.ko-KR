---
title: TikTok 경험
description: Adobe GenStudio for Performance Marketing에서 TikTok 인피드 비디오 광고를 만들고, 검토하고, 게시하고, 활성화하는 방법에 대해 알아봅니다.
feature: Create Canvas, Create Prompt, Generative AI, Variant Generation, Content Generation
role: User
level: Beginner
TQID: https://experienceleague.adobe.com/aK9mP2vR8xT4nW6yB1cF3hJ5kL7mN9pQ2rS4tU6vW8x
product_v2: id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
feature_v2: id: c7c3a4ab-6b96-4f2f-8931-4d2b360c3d12id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3aid: f71bd2fc-e9ca-4cb6-8088-82e250211e32
subfeature_v2: id: be495d08-ecd1-455f-951e-c22de504e667id: dd48f9df-f2e2-49fe-a918-332a8e240ffeid: dee4e9a9-78d1-4953-8179-f8da6117027did: e3878dde-4b87-4290-9e81-ed7ee6eb83feid: f54ee13b-9545-4d68-9842-a12026e60aaf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 4d6a7fafb895ad1e2429978c8ee58d750fff8970
workflow-type: tm+mt
source-wordcount: 933
ht-degree: 84%

---

# TikTok 경험

[!DNL GenStudio for Performance Marketing]을(를) 사용하여 [[!DNL Create]](/help/user-guide/create/overview.md) 워크플로우에서 유료 미디어 경험으로 TikTok 광고를 만들 수 있습니다. 최종 검토 및 실행을 위해 콘텐츠를 TikTok Ads Manager에 전달하도록 크리에이티브 변형을 생성하고, 브랜드 및 채널 검사를 실행하고, [!DNL Content]에 게시하고, [[!DNL Activate]](/help/user-guide/activation/overview.md)을(를) 통해 활성화하십시오.

[!DNL GenStudio for Performance Marketing]의 TikTok은 더 광범위한 옴니채널 워크플로에 적합합니다. 별도의 보고 도구로 전환하는 대신 다른 소셜 및 디스플레이 채널(예: Meta 및 LinkedIn)과 함께 [[!DNL Insights]](/help/user-guide/insights/overview.md#dashboard)에서 표준 [!DNL Insights] 보기—[!UICONTROL 캠페인], [!UICONTROL 광고], [!UICONTROL 미디어] 및 [!UICONTROL 특성]&#x200B;(으)로 TikTok 캠페인과 광고 성과를 분석할 수 있습니다. **[!UICONTROL Insights 2.0]** 크로스 채널 개요([Insights 개요 — Insights 2.0](/help/user-guide/insights/overview.md#insights-20))는 Meta 및 LinkedIn에만 중점을 둡니다. 현재 TikTok은 여기에 포함되어 있지 않습니다.

다음을 포함한 [!DNL Insights] 표면 지표:

* 노출 횟수
* 클릭수
* 클릭스루 비율(CTR)
* 클릭당 비용(CPC)
* 취득당 비용(CPA)
* 마일당 비용(CPM)
* 지출

결과를 보고, 창의적 효과를 비교하고, 타깃팅과 예산을 한 곳에서 개선하십시오. 매일 데이터를 업데이트하면 [!DNL GenStudio for Performance Marketing]을(를) 종료하지 않고 더 빠르게 최적화할 수 있습니다.

## 사전 요구 사항

TikTok 광고를 만들거나 활성화하기 전에 다음을 완료하십시오.

### 액세스 및 역할

GenStudio for Performance Marketing에 **편집기** 이상의 역할이 있는지 확인하십시오. [사용자 역할 및 권한](/help/user-guide/user-roles.md)을 참조하세요.

### TikTok 광고 계정 연결

1. **[!UICONTROL 설정]** > **[!UICONTROL TikTok]** > **[!UICONTROL 관리]** > **[!UICONTROL 계정 추가]**&#x200B;로 이동합니다.
1. 팝업에서 TikTok 광고 관리자에 로그인합니다.
1. 광고 계정에 대한 **운영자** 또는 **관리자** 액세스 권한이 있는지 확인하십시오.
1. TikTok을 채널로 추가하고 TikTok Ads Manager에 OAuth 로그인을 완료합니다.

### 구성 활성화

시스템 관리자가 [!DNL Activate]에서 TikTok 광고 계정을 연결했습니다.

* 하나 이상의 TikTok 광고 계정을 사용할 수 있습니다.

### 구성 만들기

* 앱이 브랜드 내 복사 및 레이아웃을 생성할 수 있도록 [브랜드, 제품 및 가상 사용자](/help/user-guide/guidelines/overview.md)이(가) 구성되어 있습니다.
* 하나 이상의 TikTok 템플릿이 업로드되었습니다. Adobe은 피드 내 배치에 최적화되어 있고 종횡비가 **9:16**&#x200B;이고 상단 및 하단 UI에 대한 안전 영역이 있는 TikTok 세로 비디오 템플릿을 권장합니다.
* 동영상이 [!DNL Content]에 업로드되었습니다.

## TikTok 인피드 광고 생성

### TikTok 경험 시작

만들기 워크플로의 ![TikTok 채널](../../assets/tiktok/create-tiktok-experience.png){width="90%"}
**TikTok 환경을 시작하려면**:

1. **[!UICONTROL 만들기]**(으)로 이동하여 **[!UICONTROL TikTok]**&#x200B;을(를) 선택하십시오.
1. TikTok 템플릿을 선택하고 **[!UICONTROL 사용]**&#x200B;을 클릭합니다.
1. 캔버스에서 **[!UICONTROL 브랜드]**, **[!UICONTROL 제품]**, **[!UICONTROL 사용자]** 및 **[!UICONTROL 언어]**&#x200B;를 선택합니다.
1. [!DNL Content]에서 비디오를 선택하십시오.
1. TikTok 헤드라인 카피에 대한 프롬프트를 입력합니다.
1. **[!UICONTROL 생성]**을 클릭합니다.
   ![Tiktok 캔버스 컨트롤 만들기](../../assets/tiktok/tiktok-prompt.png){width="40%"}

GenStudio for Performance Marketing은 4개의 광고 변형을 생성합니다.

다음과 같은 작업을 수행할 수 있습니다.

* 음색, 길이 또는 강조를 조정하려면 **[!UICONTROL 다시 생성]** 또는 **[!UICONTROL 세분화]**&#x200B;을 사용하세요.
* 캔버스에서 직접 텍스트를 편집합니다.
* [!DNL Content]에서 대체 비디오를 선택하려면 **[!UICONTROL 교체]**&#x200B;를 사용하십시오.
* **[!UICONTROL 자르기]** 또는 **[!UICONTROL 프레임]**&#x200B;을(를) 사용하여 **9:16** 프레임 내에서 비디오 레이아웃을 조정합니다.

### 브랜드 및 채널 확인 실행

검토를 위해 경험을 저장하거나 보내기 전에 컨텐츠 검사를 실행합니다.

1. **[!UICONTROL 콘텐츠 확인]**(브랜드 및 채널 확인)을 클릭합니다.
1. 다음에 대한 유효성 검사 결과 검토:
   * **브랜드 지침**—톤, 제한된 용어, 로고 사용.
   * **TikTok 채널 규칙**—종횡비, 파일 형식, 복사 길이.
1. 플래그가 지정된 문제(예: 복사 길이 또는 덴스 화면 텍스트)를 해결합니다.

콘텐츠 검사에 대한 자세한 내용은 [브랜드 유효성 검사](/help/user-guide/guidelines/brand-validation.md)를 참조하십시오.

## GenStudio for Performance Marketing에서 TikTok 광고 저장

검토, 재사용 및 활성화할 수 있도록 TikTok 경험을 [!DNL Content] 라이브러리로 이동합니다.
두 가지 상태가 있습니다.

* **초안 경험** — 진행 중인 작업 및 승인되지 않았습니다.
* **게시된 경험** — 콘텐츠를 승인했으며 활성화를 위해 [!DNL Content]에서 사용할 수 있습니다.

### 검토용으로 전송

**검토를 위해 보내려면**:

1. **[!DNL Experience]** 헤더에서 **[!UICONTROL 검토 요청]**&#x200B;을 클릭합니다.
1. 승인자를 선택합니다(예: 브랜드, 법적 또는 성과).
   * (선택 사항) **[!UICONTROL 설정]**&#x200B;에 메모를 추가합니다.
1. **[!UICONTROL 검토용으로 보내기]**&#x200B;를 클릭합니다.

승인자는 비디오 미리보기, 설명, call to action(CTA) 및 브랜드 및 채널 확인 결과를 볼 수 있습니다. 경험을 승인하거나 변경을 요청할 수 있습니다.

### [!DNL Content]에 게시

모든 필수 승인 후:

1. **[!UICONTROL 콘텐츠에 게시]**&#x200B;를 클릭합니다.
1. 메타데이터 확인:
   * 캠페인 또는 활성화 이름
   * 지역, 언어, 페르소나, funnel 스테이지
   * 채널: TikTok
1. **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

이제 TikTok 광고가 [!DNL Content]에 표시됩니다. [!DNL Channel] 또는 [!DNL Campaign]과(와) 같은 필터를 사용하여 검색할 수 있으며 [!DNL Activate]에서 선택할 준비가 되었습니다.

## TikTok 광고 활성화

TikTok 활성화에서는 Meta 및 Campaign Manager 360(CM360)과 동일한 [!DNL Activate] 모듈을 사용합니다. [!DNL Content] 워크플로 또는 [!DNL Activate] 워크플로에서 시작할 수 있습니다.

**TikTok 활성화를 시작하려면**:

1. TikTok 채널 타일을 엽니다.
1. **[!UICONTROL 활성화 만들기]**&#x200B;를 클릭합니다.
1. [!DNL Content]에서 게시된 TikTok 경험을 하나 이상 선택하십시오.

각 경험은 일반적으로 하나 이상의 비디오 변형이 있는 하나의 TikTok 광고에 매핑됩니다.

### 경험 설정 구성

선택한 각 경험에 대해 다음을 확인합니다.

* 기본 텍스트
* Call to action
* 대상 URL

### 플랫폼 설정 구성

다음과 같은 TikTok Ads Manager 세부 정보를 제공합니다.

* TikTok Ads 계정
* 캠페인
* 광고 그룹
* 광고 이름(TikTok 광고당 하나)

### 검토 및 게시

1. 모든 크리에이티브 및 플랫폼 세부 사항을 검토합니다.
1. **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

GenStudio for Performance Marketing은 일시 중지됨 또는 초안 상태에서 광고를 TikTok Ads Manager로 푸시합니다.

### 다음 단계

_게시 진행 중_ 모달이 나타나고 자동으로 닫힙니다. TikTok 활성화 테이블로 리디렉션됩니다.

![GenStudio 게시 양식](../../assets/tiktok/publishing-modal.png){width="30%"}

활성화 테이블은 처리가 완료되는 동안 **보류 중** 상태의 최신 활성화를 보여 줍니다.게시 완료 중에 다른 곳으로 이동할 수 있습니다.

![TikTok 세부 정보 페이지](../../assets/tiktok/tiktok-details-page.png){width="90%"}

완료되면 확인 팝업에 성공 또는 실패 메시지가 표시됩니다. 해당 팝업을 클릭하거나 활성화 테이블에서 TikTok 활성화를 클릭하면 **세부 정보** 페이지가 열립니다. **세부 정보** 페이지에는 전체 활성화 정보와 TikTok Ads Manager에 게시된 광고에 대한 딥링크가 포함되어 있습니다.

활성화가 실패하면 TikTok의 오류 메시지와 함께 **실패** 상태가 표시됩니다.

TikTok Ads Manager에서 미디어 팀은 다음과 같은 작업을 수행할 수 있습니다.

* 최종 검사를 수행합니다.
* 광고 또는 광고 그룹을 라이브로 전환합니다.

다른 채널과 마찬가지로 GenStudio for Performance Marketing은 비활성 상태에서 크리에이티브를 제공하므로 채널 소유자가 최종 실행 시기와 예산을 제어합니다.
