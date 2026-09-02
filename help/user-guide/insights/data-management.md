---
title: 데이터 관리
description: GenStudio for Performance Marketing의  [!DNL Insights] 에 대한 데이터 수집 및 저장에 대해 알아봅니다.
feature: Reporting and Insights
level: Experienced
role: Admin, Developer
last-substantial-update: 2025-1-7
exl-id: a5ab44d6-75c0-405b-82ad-9c65f6094bd6
TQID: https://experienceleague.adobe.com/HM2e0Yq2uwTpKtK-z8gHs0hDFrsJS6koQBqoNoKJK0Y
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
feature_v2:
  - id: c95c94c1-727b-457a-9184-a4dda4c95ab2
  - id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3a
  - id: e0aa398c-6185-4e77-8cf7-2561c578c181
subfeature_v2:
  - id: a98e0185-3180-4e8c-8f31-f72af4cc21a2
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 621f137c2c71c8ab6188c438f877eb3b3e457beb
workflow-type: tm+mt
source-wordcount: 249
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

AEP에서 데이터 구성 요소를 삭제하기 전에 _Customer Journey Analytics_ 안내서에서 [의미 삭제](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/deletion)를 참조하십시오.

>[!ENDSHADEBOX]

## 데이터 보존 정책

GenStudio for Performance Marketing은 13개월 동안 채널 데이터를 유지합니다. 이 보존 정책에는 초기 연결 중에 수집된 6개월 동안의 데이터가 포함되어 있으므로 포괄적인 내역 데이터 분석 및 보고를 보장합니다.

[유료 미디어 계정 연결](/help/user-guide/connectors/connect-channel.md)을 참조하세요.
