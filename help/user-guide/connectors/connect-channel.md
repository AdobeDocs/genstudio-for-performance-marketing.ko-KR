---
title: 유료 미디어 연결
description: Adobe GenStudio for Performance Marketing을 사용하여 광고 및 미디어를 활성화하고 모니터링하려면 채널 계정을 연결하십시오.
level: Intermediate
role: Admin, Data Engineer
feature: Reporting and Insights
exl-id: e699041e-b462-45b3-8c4c-4de0d52cf0e6
source-git-commit: 2844914d25d9bc3a2be7f47d0cd7f26f7c921555
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# 유료 미디어 계정 연결

_[!DNL Data connectors]_을(를) 사용하면 GenStudio for Performance Marketing과 유료 미디어 네트워크 계정 간에 원활하게 통합할 수 있습니다. 타사 채널 계정에 연결하면 [[!DNL Insights]](/help/user-guide/insights/overview.md)에서 캠페인 성과 지표와 같은 중요한 데이터를 교환할 수 있으며 [[!DNL Activate]](/help/user-guide/activation/overview.md)에서 새로운 광고 배치를 제공할 수 있습니다. 이 통합을 통해 GenStudio for Performance Marketing은 활성 캠페인으로부터 노출, 클릭 수 및 전환 등 중요한 통찰력을 받고 미디어와 광고를 관리할 수 있습니다.

**유료 미디어 계정에 연결하려면**:

1. 줄임표 **[!UICONTROL 을(를) 클릭합니다... 왼쪽 아래 탐색에서]** 이상

1. 톱니바퀴 아이콘으로 **[!UICONTROL 설정]**&#x200B;을 선택하세요.

1. _[!UICONTROL 설정]_&#x200B;의 _[!UICONTROL Data connectors]_ 섹션에서 커넥터 유형을 선택하고 **[!UICONTROL 연결]**&#x200B;을 클릭합니다.

   선택적으로 연결된 계정이 있는 경우 _연결된 계정_&#x200B;을 클릭하여 계정 이름, 세부 정보 및 상태 목록을 볼 수 있습니다.

1. 선택한 [커넥터 유형](#connector-types)을(를) 확인하고 필수 구성 요소를 검토한 다음 연결 단계를 계속하십시오.

## 유료 미디어 연결

GenStudio for Performance Marketing은 선호하는 마케팅 플랫폼과 통합하기 위해 다양한 커넥터 유형을 지원합니다. 각 커넥터 유형에는 성공적인 연결을 위해 완료하기 위한 특정 사전 요구 사항 및 설정 단계가 있습니다.

### 메타 광고 연결

>[!BEGINSHADEBOX]

**필수 구성 요소**:

- Facebook/Meta ads 계정
- 보고서에 액세스하고 광고를 보기 위해 권한 수준이 `View performance`인 메타 광고 계정에 액세스
- 브라우저에서 팝업 차단기 제거

>[!ENDSHADEBOX]

**메타 광고 계정을 연결하려면**:

1. _Data connectors_ 섹션에서 _메타데이터_ 카드의 **[!UICONTROL 연결]**&#x200B;을 클릭합니다.

1. Facebook 계정에 로그인합니다.

   팝업 차단기를 제거한 다음 **[!UICONTROL 새로 고침]**&#x200B;을 사용하여 다시 시도할 수 있습니다.

1. Facebook 인증 지침을 따릅니다.

1. _[!UICONTROL 비즈니스용 Facebook 로그인]_ 팝업(Adobe 기호에 대한 메타)에서 다음 선택 사항을 살펴보십시오.

   - 계정 정보를 확인하고 **[!UICONTROL 다음 계정으로 계속]**&#x200B;을 클릭합니다.
   - 선택한 페이지에 대한 액세스 권한을 부여하고 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.
   - 선택한 회사에 대한 액세스 권한을 부여하고 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.
   - 하나 이상의 Instagram 계정을 선택하고 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.
   - 선택 항목을 검토하고 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. _[!UICONTROL 메타 광고]_ 보기에서 계정을 하나 이상 선택하고 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

_[!UICONTROL 메타 광고 계정]_ 보기에는 `Account name`, `Added by`, `Date added` 및 `Status`이(가) 나열됩니다. **[!UICONTROL 계정 추가]**&#x200B;를 사용하여 목록에 계정을 더 추가하십시오.

## 데이터 수집

처음에 GenStudio for Performance Marketing은 가장 최근 6개월의 내역 데이터를 가져옵니다. 이 방법을 사용하면 트렌드를 분석하고, 성과를 평가하고, 정보에 입각한 결정을 내리는 데 필요한 관련 통찰력을 즉시 확인할 수 있습니다. 수집 프로세스는 계정의 데이터 볼륨에 따라 1~5일이 걸릴 수 있습니다.

>[!BEGINSHADEBOX]

**데이터 수집 및 보존 정책**

GenStudio for Performance Marketing은 13개월 동안 채널 데이터를 유지합니다. 이 보존 정책에는 초기 연결 중에 수집된 6개월 동안의 데이터가 포함되어 있으므로 포괄적인 내역 데이터 분석 및 보고를 보장합니다.

>[!ENDSHADEBOX]
