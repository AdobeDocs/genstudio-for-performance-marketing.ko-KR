---
title: GenStudio용 Marketo
description: 조직에서 GenStudio for Performance Marketing의 Marketo 템플릿을 사용할 수 있도록 GenStudio Adobe Exchange 앱을 설치하고 구성합니다.
feature: Extensibility
source-git-commit: c9bfee479a433a1303a66a66917b0bbe60f24a74
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 0%

---

# GenStudio용 Marketo

동일한 [!DNL IMS] 조직에서 [!DNL Marketo Engage] 및 [!DNL GenStudio for Performance Marketing]을(를) 사용하는 조직은 [!DNL Adobe Exchange]에서 **GenStudio용 Marketo** 앱을 설치할 수 있습니다. 시스템 관리자가 앱을 승인하고 배포를 완료한 후 작성자가 [!DNL Content]에 직접 업로드된 템플릿 옆에 있는 Marketo에서 이메일 경험을 만들면서 GenStudio 템플릿을 선택할 수 있습니다.

이 항목은 앱을 설치하고, Marketo에서 자격 증명을 수집하고, Exchange에서 앱을 배포하는 **관리자**&#x200B;를 위한 항목입니다. AJO 및 Marketo 템플릿 구문이 GenStudio에서 작동하는 방법은 [AJO 및 Marketo의 템플릿](/help/user-guide/templates/use-templates.md#templates-from-ajo-and-marketo)을 참조하십시오.

## 사전 요구 사항

* 확장을 배포하는 조직에서 [!DNL Marketo Engage]을(를) 프로비저닝해야 합니다.
* 응용 프로그램을 배포하는 사용자는 **Marketo 자격 증명**&#x200B;이 필요합니다. 이러한 자격 증명을 만들고 검색하려면 **Marketo 제품 관리자** 액세스 권한이 있어야 합니다(Marketo을 열 때 **[!UICONTROL 관리자]** 영역을 사용할 수 있어야 함).

## Adobe Exchange에서 앱 설치

>[!VIDEO](https://video.tv.adobe.com/v/3483299?learn=on)

1. [Adobe Exchange](https://exchange.adobe.com)을 열고 **[!UICONTROL Experience Cloud]**(으)로 이동합니다.
1. [GenStudio용 Marketo](https://exchange.adobe.com/apps/ec/ab6p21vo8r/marketo-for-genstudio) 목록을 엽니다.
   ![Adobe Exchange에서 GenStudio용 Marketo 목록](/help/extensibility/marketo-adobe-exchange.png){width="75%"}
1. 조직에 대한 앱을 요청하려면 **[!UICONTROL 무료]**&#x200B;를 선택하세요.
1. 조직에서 요청을 **검토 및 승인**&#x200B;한 후 [Marketo 자격 증명 가져오기](#get-marketo-credentials) 및 [Exchange에서 응용 프로그램을 배포](#deploy-the-application-from-exchange)합니다.

## Marketo 자격 증명 가져오기

**Marketo** 인스턴스(Adobe Developer Console 아님)의 자격 증명을 사용합니다. Exchange에서 배포하기 전에 아래 단계를 사용하여 다음 자격 증명을 수집합니다.

>[!NOTE]
>
>Marketo 자격 증명을 생성하고 검색하려면 Marketo 제품 관리자 액세스 권한이 있어야 합니다. 그렇지 않으면 관리 탭이 Marketo에 표시되지 않습니다.

### API 전용 사용자 만들기(기존 API 사용자를 재사용하는 경우 선택 사항)

1. Marketo에서 **[!UICONTROL 관리자]**(으)로 이동합니다.
   ![Marketo 관리 탭](/help/extensibility/marketo-admin-global.png){width="80%"}
1. **[!UICONTROL 보안]**&#x200B;에서 **[!UICONTROL 사용자 및 역할]**&#x200B;을 열고 **[!UICONTROL 역할]** 탭으로 이동합니다.
1. 다음 권한을 추가하여 새 역할을 만들거나 기존 역할을 편집합니다. _API 액세스_ 및 _Design Studio 액세스_.
1. 새 API 사용자의 경우 **[!UICONTROL API 전용 사용자 만들기]**&#x200B;를 클릭합니다(각 API 사용자에 대해 고유한 이메일 사용).
1. 역할 확인란을 선택하고 만든 새 역할을 할당합니다. 사용할 API 사용자가 이미 있는 경우 [LaunchPoint 서비스 만들기 또는 선택](#create-or-select-a-launchpoint-service)으로 건너뛰십시오.

![API 전용 사용자 및 API 역할을 가진 사용자 및 역할](/help/extensibility/marketo-users-roles-api-user.png){width="80%"}

### LaunchPoint 서비스 만들기 또는 선택

1. **[!UICONTROL 관리자]**&#x200B;의 **[!UICONTROL 통합]**&#x200B;에서 **[!UICONTROL LaunchPoint]**&#x200B;를 엽니다.
1. 새 서비스를 만들거나 기존 사용자 지정 서비스를 사용하려면 **[!UICONTROL 만들기]**를 클릭하십시오.
   ![LaunchPoint 사용자 지정 서비스](/help/extensibility/marketo-launchpoint-custom-service.png){width="80%"}
1. 서비스에 대해 **[!UICONTROL 세부 정보 보기]**&#x200B;를 클릭하고 **[!UICONTROL 클라이언트 ID]** 및 **[!UICONTROL 클라이언트 암호]**&#x200B;를 복사합니다. Adobe Exchange **[!UICONTROL 구성]**&#x200B;에 입력하게 됩니다.

### Marketo REST API 기본 URL 참고

1. **[!UICONTROL 관리자]**&#x200B;의 **[!UICONTROL 통합]**&#x200B;에서 **[!UICONTROL 웹 서비스]**&#x200B;를 엽니다.
1. **[!UICONTROL REST API]** 끝점을 찾습니다. `https://###-XXX-###.mktorest.com` 형식으로 **기본 URL**(호스트)만 복사합니다. **not**&#x200B;에 `/rest` 또는 `/identity`과(와) 같은 경로 세그먼트를 포함하지 마십시오. 이 값은 Marketo 인스턴스별로 고유합니다.

![웹 서비스 REST API 끝점 기본 URL](/help/extensibility/marketo-web-services-rest-endpoint.png){width="80%"}

Exchange 배포 화면에서 요청하는 **[!UICONTROL Marketo Engage ID URL]**&#x200B;과(와) LaunchPoint의 REST 기본 URL, 클라이언트 ID 및 클라이언트 암호가 필요합니다.

## Exchange에서 애플리케이션 배포

GenStudio에서 확장을 사용할 수 있도록 하려면 Adobe Exchange에서 앱을 배포합니다.

1. [Adobe Exchange](https://exchange.adobe.com)&#x200B;(으)로 돌아갑니다.
1. **[!UICONTROL 관리]**&#x200B;를 선택하고 **GenStudio용 Marketo** 앱(예: **[!UICONTROL App Builder 응용 프로그램]** 또는 조직의 관리 앱)을 엽니다.
1. **[!UICONTROL 환경]**&#x200B;에서 드롭다운에서 기존 환경을 선택하거나 **[!UICONTROL 환경 추가]**&#x200B;를 선택하여 환경을 만듭니다.
1. 선택한 환경에 대해 **[!UICONTROL 구성]**&#x200B;을 엽니다.
1. Marketo Engage ID URL 및 Marketo Engage REST API 기본 URL 모두에 대해 [LaunchPoint](#create-or-select-a-launchpoint-service)의 **[!UICONTROL 클라이언트 ID]** 및 **[!UICONTROL 클라이언트 암호]**, **[!UICONTROL Marketo Engage ID URL]** 및 **[!UICONTROL Marketo Engage REST API 기본 URL]**([웹 서비스](#note-your-marketo-rest-api-base-url)의 기본 호스트)&#x200B;을 입력합니다.
1. **[!UICONTROL 배포]**&#x200B;를 클릭합니다. 배포가 성공하면 작업이 **[!UICONTROL 배포 취소]**(으)로 변경됩니다.

### 구성 업데이트

환경에 대한 구성 값을 변경하려면 먼저 **[!UICONTROL 배포 취소]**&#x200B;하고 필드를 업데이트한 다음 다시 **[!UICONTROL 배포]**&#x200B;하십시오.

### Workspace 구성(선택 사항)

기본 작업 영역을 사용하려면 이 단계를 건너뛸 수 있습니다. 기본적으로 **Workspace ID** 및 **템플릿 목록 페이지 크기** 필드는 미리 구성되어 있습니다.

그러나 다른 작업 영역에서 템플릿을 가져와야 하는 경우:

1. Marketo에서 **[!UICONTROL 관리]** → **[!UICONTROL 보안]** → **[!UICONTROL 작업 공간 및 파티션]**&#x200B;으로 이동합니다.
1. **Workspace ID** 열은 기본적으로 숨겨져 있습니다. 활성화하려면 머리글 행(열 이름이 표시되는 위치)을 마우스 오른쪽 단추로 클릭합니다.
1. **[!UICONTROL 열]**&#x200B;을(를) 선택하십시오.
1. 목록에서 **[!UICONTROL ID]** 사용
   ![Workspace ID 열이 활성화된 작업 공간 및 파티션](/help/extensibility/marketo-workspace-id.png){width="80%"}

표시되면 구성에 적절한 **Workspace ID**&#x200B;을(를) 사용합니다.

## GenStudio에서 Marketo 템플릿 액세스

GenStudio용 Marketo이 설치 및 구성된 후 GenStudio에서 **이메일** 경험을 만들 때 **[!UICONTROL Marketo 템플릿]** 탭이 나타납니다. 이 탭을 사용하여 Marketo Engage에서 템플릿을 검색할 수 있습니다.

>[!IMPORTANT]
>
>GenStudio for Performance Marketing의 **표준 이메일** 경험 흐름으로 이메일을 만듭니다. 이 통합은 새 이메일 편집기 경험으로 만든 이메일을 지원하지 않습니다.

![Marketo 자격 증명이 포함된 Exchange 구성](/help/extensibility/marketo-exchange-configuration.png){width="80%"}

## 문제 해결

### Marketo 템플릿 탭이 표시되지 않음

* 앱이 Exchange에서 **승인됨**&#x200B;이고 환경이 올바른 클라이언트 ID, 클라이언트 암호 및 Marketo 기본 URL을 사용하여 **배포됨**&#x200B;인지 확인하십시오.
* 자격 증명을 만들 때 **Marketo 제품 관리자** 액세스가 사용되었는지 확인하도록 관리자에게 요청하십시오.

### 템플릿이 로드되지 않음

* 페이지를 다시 로드하거나 로그아웃한 후 GenStudio으로 다시 로그인합니다.
* 브라우저 개발자 도구 **[!UICONTROL 네트워크]** 패널에서 Marketo 인스턴스에 대해 실패한 API 호출을 찾고 REST 기본 URL이 Marketo의 **[!UICONTROL 웹 서비스]**&#x200B;와(호스트 뒤에 추가 경로가 없음) 일치하는지 확인합니다.

### &quot;템플릿을 찾을 수 없음&quot; 오류

확장이 성공적으로 설치되고 Marketo 템플릿 탭이 표시되지만 &quot;템플릿을 찾을 수 없음&quot;을 표시하는 경우 템플릿을 렌더링하는 동안 애플리케이션에서 크기 제한을 초과하여 충돌이 발생할 수 있습니다.
이 문제를 해결하려면

1. Exchange에서 애플리케이션 배포를 취소합니다.
1. 템플릿 목록 페이지 크기를 줄입니다(예: 1 또는 2로 설정).
1. 응용 프로그램을 다시 배포합니다.
