---
title: 유료 미디어 연결
description: Adobe GenStudio for Performance Marketing을 사용하여 광고 및 미디어를 활성화하고 모니터링하려면 채널 계정을 연결하십시오.
level: Intermediate
role: Admin, Data Engineer
feature: Reporting and Insights
exl-id: e699041e-b462-45b3-8c4c-4de0d52cf0e6
source-git-commit: cf4be61925761c9630cb8ea5c995d017b3938a31
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# 유료 미디어 계정 연결

_[!DNL Data connectors]_&#x200B;을(를) 사용하면 GenStudio for Performance Marketing과 유료 미디어 네트워크 계정 간에 원활하게 통합할 수 있습니다. 타사 채널 계정에 연결하면 [[!DNL Insights]](/help/user-guide/insights/overview.md)에서 캠페인 성과 지표와 같은 중요한 데이터를 교환할 수 있으며 [[!DNL Activate]](/help/user-guide/activation/overview.md)에서 새로운 광고 배치를 제공할 수 있습니다. 이 통합을 통해 GenStudio for Performance Marketing은 활성 캠페인으로부터 노출, 클릭 수 및 전환 등 중요한 통찰력을 받고 미디어와 광고를 관리할 수 있습니다.

**유료 미디어 계정에 연결하려면**:

1. 줄임표 **[!UICONTROL 을(를) 클릭합니다... 왼쪽 아래 탐색에서]** 이상

1. 톱니바퀴 아이콘으로 **[!UICONTROL 설정]**&#x200B;을 선택하세요.

1. _[!UICONTROL 설정]_&#x200B;의 _[!UICONTROL Data connectors]_ 섹션에서 커넥터 유형을 선택하고 **[!UICONTROL 연결]**&#x200B;을 클릭합니다.

   선택적으로 연결된 계정이 있는 경우 _연결된 계정_&#x200B;을 클릭하여 계정 이름, 세부 정보 및 상태 목록을 볼 수 있습니다.

1. 선택한 [커넥터 유형](#connector-types)을(를) 확인하고 필수 구성 요소를 검토한 다음 연결 단계를 계속하십시오.

## 유료 미디어 연결

GenStudio for Performance Marketing은 선호하는 마케팅 플랫폼과 통합하기 위해 다양한 커넥터 유형을 지원합니다. 각 커넥터 유형에는 성공적인 연결을 위해 완료하기 위한 특정 사전 요구 사항 및 설정 단계가 있습니다.

### Google Campaign Manager 360 연결

>[!BEGINSHADEBOX]

**필수 구성 요소**:

- Google Campaign Manager 360 계정
- 브라우저에서 팝업 차단기 제거

>[!ENDSHADEBOX]

**Google Campaign Manager 360 계정에 연결하려면**:

1. _Data Connectors_ 섹션의 _Google Campaign Manager 360_ 카드에서 **[!UICONTROL 연결]**&#x200B;을 클릭합니다.

1. Google Campaign Manager 360 계정에 로그인합니다.

   팝업 차단기를 제거한 다음 **[!UICONTROL 새로 고침]**&#x200B;을 사용하여 다시 시도할 수 있습니다.

1. 사용 약관을 읽고 **[!UICONTROL 허용]**&#x200B;을 클릭하여 액세스 권한을 부여합니다.

1. _[!UICONTROL Google 캠페인 관리자 360]_ 보기에서 하나 이상의 광고주를 선택하고 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

_[!UICONTROL Google Campaign Manager 360 계정]_ 보기에는 `Account name`, `Added by`, `Date added` 및 `Status`이(가) 나열됩니다. **[!UICONTROL 계정 추가]**&#x200B;를 사용하여 목록에 계정을 더 추가하십시오.

### 메타 광고 연결

_Meta Business_ 프로필을 GenStudio for Performance Marketing에 연결하면 비즈니스 페이지, Meta Ads 계정 및 기타 Meta 에셋의 광고 데이터에 원활하게 액세스할 수 있습니다.

>[!BEGINSHADEBOX]

**필수 구성 요소**:

- Meta Ads 계정 및 Facebook 비즈니스 프로필과 같은 모든 Meta 서비스에 액세스할 수 있는 Facebook/Meta 로그인
- 보고서에 액세스하고 광고를 보기 위해 권한 수준이 `View performance`인 메타 광고 계정에 액세스하십시오. 여기에는 다음이 포함됩니다
   - [!DNL Insights]에 필요한 권한:

      - `pages_show_list`
      - `ads_read`
      - `ads_management`
      - `pages_read_engagement`

   - [!DNL Activate]에 필요한 권한:

      - `ads_management`
      - `ads_read`
      - `business_management`
      - `instagram_basic`
      - `instagram_content_publish`
      - `pages_manage_ads`
      - `pages_manage_posts`
      - `pages_show_list`

- 브라우저에서 팝업 차단기 제거

>[!ENDSHADEBOX]

**메타 광고 계정을 연결하려면**:

1. _Data connectors_ 섹션에서 _메타데이터_ 카드의 **[!UICONTROL 연결]**&#x200B;을 클릭합니다.

1. Facebook 계정에 로그인합니다.

   팝업 차단기를 제거한 다음 **[!UICONTROL 새로 고침]**&#x200B;을 사용하여 다시 시도할 수 있습니다.

1. Facebook 인증 지침을 따라 계정 정보를 확인하고 **[!UICONTROL 다음 계정으로 계속...]**&#x200B;을 클릭합니다.

1. _[!UICONTROL 비즈니스용 Facebook 로그인]_(Adobe 기호에 대한 메타)에서, 다음 선택 사항을 단계별로 진행하여 GenStudio for Performance Marketing 액세스 권한을 부여합니다.

   - 하나 이상의 메타 비즈니스 프로필을 선택하고 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.
   - 하나 이상의 메타 페이지를 선택하고 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.
   - Instagram 계정을 하나 이상 선택하고 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.
   - 선택 항목을 검토하고 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. 계정이 연결되어 있는지 확인받으면 **[!UICONTROL 가져오기]**&#x200B;를 클릭합니다.

   이 단계에서는 GenStudio for Performance Marketing이 최적의 성능을 위해 모든 광고, 메타데이터 및 지표에 액세스할 수 있도록 합니다.

1. _[!UICONTROL 메타 광고]_&#x200B;에서 [!DNL Insights]에 포함할 계정을 하나 이상 선택하고 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

1. _연결된 플랫폼_ 확인을 받으면 **[!UICONTROL 계정 보기]**&#x200B;를 클릭합니다.

   _[!UICONTROL 메타 광고 계정]_ 보기에는 `Account name`, `Added by`, `Date added` 및 `Status`이(가) 나열됩니다.

**[!UICONTROL 계정 추가]**&#x200B;를 사용하여 목록에 계정을 더 추가하십시오. 동일한 Meta Business 프로필에 연결된 계정을 추가할 때 인증 흐름이 약간 다를 수 있습니다. 연결 프로세스 중에 새 메타 광고 계정만 선택합니다.

## 데이터 수집

처음에 GenStudio for Performance Marketing은 가장 최근 6개월의 내역 데이터를 가져옵니다. 이 방법을 사용하면 트렌드를 분석하고, 성과를 평가하고, 정보에 입각한 결정을 내리는 데 필요한 관련 통찰력을 즉시 확인할 수 있습니다. 수집 프로세스는 계정의 데이터 볼륨에 따라 1~5일이 걸릴 수 있습니다.

>[!BEGINSHADEBOX]

**데이터 수집 및 보존 정책**

GenStudio for Performance Marketing은 13개월 동안 채널 데이터를 유지합니다. 이 보존 정책에는 초기 연결 중에 수집된 6개월 동안의 데이터가 포함되어 있으므로 포괄적인 내역 데이터 분석 및 보고를 보장합니다.

>[!ENDSHADEBOX]
