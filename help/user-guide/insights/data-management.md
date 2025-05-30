---
title: 데이터 관리
description: GenStudio for Performance Marketing의  [!DNL Insights] 에 대한 데이터 수집 및 저장에 대해 알아봅니다.
feature: Reporting and Insights
level: Experienced
role: Admin, Data Architect
last-substantial-update: 2025-1-7
exl-id: a5ab44d6-75c0-405b-82ad-9c65f6094bd6
source-git-commit: f98a853965ce05420cd178c294b3b4d69500977b
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---

# 데이터 관리

GenStudio for Performance Marketing은 [!DNL Insights]을(를) 지원하는 지표 및 메타데이터의 데이터 수집 및 저장을 위해 Adobe Experience Platform(AEP)를 사용합니다. AEP은 데이터 컬렉션을 저장 및 관리하기 위해 _스키마_&#x200B;를 사용하여 데이터 구조와 _데이터 세트_&#x200B;를 정의합니다.

## 데이터 연결

GenStudio for Performance Marketing은 Customer Journey Analytics(CJA)를 사용하여 하나 이상의 AEP 데이터 세트에 대한 연결을 만들어 여러 데이터 소스를 집계합니다. CJA은 이러한 데이터 연결을 사용하여 [!DNL Insights]을(를) 사용하여 지표를 분석하기 위한 데이터 보기를 만듭니다.

>[!BEGINSHADEBOX]

**데이터 연결에 대한 중요 정보**

[Adobe 시스템 관리자](/help/user-guide/user-roles.md#adobe-system-administrator-vs-genstudio-system-manager)인 경우 GenStudio for Performance Marketing을 지원하는 AEP 샌드박스 관리 및 데이터 레이크 구성 요소에 액세스할 수 있는 권한이 있을 수 있습니다.

>[!WARNING]
>
>AEP에서 프로덕션 샌드박스를 재설정하면 모든 데이터 연결이 삭제되고 [!DNL Insights]의 작동이 중지됩니다.

GenStudio for Performance Marketing이 안정적으로 작동하는 데 필요한 다음 데이터 연결을 삭제하지 말고 주의하십시오.

- `GS Insights` 접두사가 있는 AEP 데이터 세트
- `GS Insights` 접두사가 있는 AEP 스키마, 클래스 및 필드 그룹
- 사용자 지정 필드 그룹 `timestamp for metadata`
- AEP 연결: 데이터 흐름 앞에 `GS Insights`이(가) 붙습니다.
- AEP 연결: GS Insights 계정

AEP에서 데이터 구성 요소를 삭제하기 전에 _Customer Journey Analytics_ 안내서에서 [의미 삭제](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/technotes/deletion)를 참조하십시오.

>[!ENDSHADEBOX]

## 데이터 보존 정책

GenStudio for Performance Marketing은 13개월 동안 채널 데이터를 유지합니다. 이 보존 정책에는 초기 연결 중에 수집된 6개월 동안의 데이터가 포함되어 있으므로 포괄적인 내역 데이터 분석 및 보고를 보장합니다.

[유료 미디어 계정 연결](/help/user-guide/connectors/connect-channel.md)을 참조하세요.
