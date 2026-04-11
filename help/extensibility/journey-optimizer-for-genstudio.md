---
title: GenStudio용 Journey Optimizer
description: 조직에서 GenStudio for Performance Marketing의 Journey Optimizer 템플릿을 사용할 수 있도록 GenStudio Adobe Exchange 앱을 설치하고 구성합니다.
feature: Extensibility
source-git-commit: fbec4567d960a6e3607c5e5e43057e2f22e9f6ea
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 0%

---

# GenStudio용 Journey Optimizer

동일한 [!DNL IMS] 조직에서 [!DNL Adobe Journey Optimizer]&#x200B;(AJO) 및 [!DNL GenStudio for Performance Marketing]을(를) 사용하는 조직은 [!DNL Adobe Exchange]에서 **GenStudio용 Journey Optimizer** 앱을 설치할 수 있습니다. 시스템 관리자가 앱을 승인하고 배포를 완료한 후 작성자는 AJO에서 [!DNL Content]에 직접 업로드된 템플릿 옆에 있는 전자 메일 환경을 만드는 동안 GenStudio 콘텐츠 템플릿을 선택할 수 있습니다.

이 항목은 앱을 설치하고, [!DNL Adobe Developer Console]에서 OAuth 자격 증명을 만들고, [!DNL Adobe Experience Platform]에서 기술 계정 권한을 매핑하는 **관리자 및 개발자**&#x200B;를 위한 항목입니다. AJO 및 Marketo 템플릿 구문이 GenStudio에서 작동하는 방법은 [AJO 및 Marketo의 템플릿](/help/user-guide/templates/use-templates.md#templates-from-ajo-and-marketo)을 참조하십시오.

## 사전 요구 사항

* AJO은 확장을 배포하는 조직에서 프로비저닝되어야 합니다.
* AJO에서 템플릿을 작성하는 사용자는 조직에서 정의한 대로 Journey Optimizer에서 **콘텐츠 템플릿을 만들고 편집**&#x200B;할 수 있는 권한이 필요합니다.
* AJO의 이메일 템플릿에는 생성된 콘텐츠가 표시되어야 하는 필드 자리 표시자(핸들바)가 포함되어야 합니다. 이러한 필드 없이 템플릿을 선택할 수 있지만, 자리 표시자 [!DNL GenStudio for Performance Marketing]에서 예상하는 필드가 없으면 **경험 생성에 실패**&#x200B;합니다. [템플릿 사용자 지정](/help/user-guide/templates/customize-template.md) 및 [인식된 필드 이름](/help/user-guide/templates/customize-template.md#recognized-field-names)을 참조하세요.

## Adobe Exchange에서 앱 설치

>[!VIDEO](https://video.tv.adobe.com/v/3483306?captions=kor&learn=on)

1. [Adobe Exchange](https://exchange.adobe.com)을 열고 **[!UICONTROL Experience Cloud]**(으)로 이동합니다.
1. [GenStudio용 Journey Optimizer](https://exchange.adobe.com/apps/ec/abpopqqr1q/journey-optimizer-for-genstudio) 목록을 엽니다.
   ![요구 사항 및 무료 설치를 포함한 Adobe Exchange의 GenStudio용 Journey Optimizer 목록](/help/extensibility/ajo-adobe-exchange.png){width="75%"}
1. 조직에 대한 앱을 요청하려면 **[!UICONTROL 무료]**&#x200B;를 선택하세요.
1. 조직에서 요청을 **검토 및 승인**&#x200B;한 후 [Adobe Developer Console에서 OAuth 자격 증명 만들기](#create-oauth-credentials-in-adobe-developer-console) 및 [Exchange에서 응용 프로그램을 배포](#deploy-the-application-from-exchange)합니다.

## Adobe Developer Console에서 OAuth 자격 증명 만들기

Journey Optimizer API에 대한 OAuth 자격 증명을 제공하는 [Adobe Developer Console](https://developer.adobe.com/console/)에 **프로젝트**&#x200B;을(를) 만듭니다. Exchange에서 앱을 구성할 때는 **클라이언트 ID**, **클라이언트 암호**, **조직 ID**, **범위** 등의 값이 필요합니다.

1. Adobe Developer Console에 로그인하고 **새 프로젝트**&#x200B;를 만듭니다.
1. **[!UICONTROL API 추가]**&#x200B;를 클릭하고 **[!DNL Experience Cloud]** 제품 API 목록에서 **[!UICONTROL Adobe Journey Optimizer]**&#x200B;을(를) 선택하여 **Adobe Journey Optimizer(AJO) API**&#x200B;을(를) 프로젝트에 추가합니다.
1. 프로젝트 작업 영역에서 자격 증명을 생성하고 **클라이언트 ID**, **클라이언트 암호**, **조직 ID**, **범위** 및 배포 플로우에서 요청하는 기타 모든 값을 복사합니다. 다음 섹션에서 안전하게 저장하십시오.

>[!NOTE]
>
>Exchange에서 설치할 때 OAuth 클라이언트 ID와 기술 계정 ID가 모두 표시되면 **OAuth 클라이언트 ID**&#x200B;를 사용하십시오.

## Exchange에서 애플리케이션 배포

### 관리에서 앱을 열고 환경 추가

1. [Adobe Exchange](https://exchange.adobe.com)&#x200B;(으)로 돌아갑니다.
1. **[!UICONTROL 관리]**&#x200B;를 선택하고 **[!UICONTROL App Builder 응용 프로그램]**(또는 조직의 관리 앱 경로)을 엽니다.
1. **GenStudio용 Journey Optimizer**&#x200B;을(를) 선택하고 앱이 **승인됨**&#x200B;인지 확인하십시오.
1. **[!UICONTROL 환경]**&#x200B;에서 **환경:** 드롭다운에서 기존 환경을 선택하거나 **[!UICONTROL 환경 추가]**&#x200B;를 선택하여 환경을 만듭니다.
   ![승인 상태의 응용 프로그램 세부 정보 및 환경 추가](/help/extensibility/ajo-config-002.png){width="50%"}
1. 선택한 환경에서 **[!UICONTROL 구성]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL 구성]** 탭에서 **[!UICONTROL AJO 자격 증명]**&#x200B;을 찾으십시오.
   ![배포 전 AJO 자격 증명을 사용한 구성(초안)](/help/extensibility/ajo-config-004.png){width="80%"}
1. Journey Optimizer API가 추가된 Developer Console 프로젝트의 자격 증명을 입력하십시오(예: **[!UICONTROL AJO 클라이언트 ID]**, **[!UICONTROL AJO 클라이언트 암호]**, **[!UICONTROL AJO 토큰 끝점]** 및 기타 필수 필드).
1. **샌드박스 이름을 모두 소문자로 입력**(예: `prod`).
1. **[!UICONTROL 배포]**&#x200B;를 클릭합니다. 배포가 완료되면 상태가 배포됨으로 표시됩니다. 단추 텍스트가 **[!UICONTROL 배포 취소]**(으)로 변경됩니다.
   ![배포된 앱 및 배포 취소를 App Builder 응용 프로그램 보기에서 사용할 수 있음](/help/extensibility/ajo-config-005.png){width="80%"}

배포 후 Adobe Developer Console에는 AJO 및 Adobe Runtime API와 함께 GenStudio &lt;Your_Environment_Name>**용**&#x200B;Journey Optimizer라는 새 자동 생성 프로젝트가 포함됩니다. 이 프로젝트는 읽기 전용이므로 편집하거나 삭제할 수 없습니다.
![배포 후 읽기 전용 Developer Console 프로젝트 자동 생성](/help/extensibility/ajo-auto-project.png){width="100%"}

### 구성 업데이트

환경에 대한 구성 변수를 변경하려면 먼저 **[!UICONTROL 배포 취소]**&#x200B;하고 값을 업데이트한 다음 다시 **[!UICONTROL 배포]**&#x200B;하여 변경 내용을 적용하세요.

Exchange에서 **여러 환경**&#x200B;을 만들 수 있습니다(예: 샌드박스당 환경 하나). 조직에서 여러 샌드박스를 사용할 때 각 배포가 GenStudio에서 별도의 경험으로 표시될 수 있습니다.

## 기술 계정에 대한 권한 매핑

사용자는 전체 [!DNL Adobe Experience Platform] 액세스 권한 없이 GenStudio에서 AJO 확장을 볼 수 있습니다. API 호출(예: 템플릿 로드)의 경우 **[!DNL Adobe Experience Platform]** > **[!UICONTROL 권한]**&#x200B;에서 OAuth 자격 증명에 연결된 기술 계정에 Journey Optimizer 권한을 부여해야 합니다. 정확한 역할 이름과 권한 집합은 조직에 따라 다릅니다.

AJO **[!UICONTROL 권한]** > **[!UICONTROL 여정]**&#x200B;의 **[!UICONTROL 역할 관리자]** 아래에서 확장을 보고 Exchange에서 배포할 때 사용한 자격 증명과 동일한 자격 증명인 Developer Console 프로젝트의 **API 자격 증명**&#x200B;을(를) 추가합니다.

![Adobe Experience Platform 권한의 AJO Architect 역할에 할당된 API 자격 증명](/help/extensibility/ajo-map-permissions.png){width="80%"}

**참고 항목**(Journey Optimizer 액세스 제어):

* [액세스 제어](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/access-control/access-control-landing-page)
* [Journey Optimizer의 권한](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/access-control/permissions)
* [시스템 관리자용 시작하기](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/get-started/quick-start/administrator)

## GenStudio에서 AJO 템플릿 액세스

배포 및 권한 매핑 후:
1. GenStudio for Performance Marketing에서 **[!UICONTROL 만들기]**&#x200B;를 열고 **전자 메일** 환경을 시작합니다.
1. **[!UICONTROL 템플릿 선택]**&#x200B;에서 **[!UICONTROL 업로드된 템플릿]** 옆의 **[!UICONTROL AJO 템플릿]** 탭을 열어 Journey Optimizer에서 템플릿을 찾아보십시오.

![AJO 템플릿 탭과 템플릿 갤러리로 템플릿 선택](/help/extensibility/ajo-template-tab.png){width="80%"}

## 문제 해결

### AJO 템플릿 탭이 표시되지 않음

* **클라이언트 ID**, **클라이언트 암호**, **범위**, **샌드박스**&#x200B;를 포함하여 Exchange **[!UICONTROL 구성]**&#x200B;에 입력한 값이 올바른지 확인하십시오.
* **샌드박스 이름이 소문자인지**(예: `prod`)를 확인하십시오.
* Exchange에서 설치할 때 [OAuth 자격 증명 만들기](#create-oauth-credentials-in-adobe-developer-console)에 설명된 대로 **클라이언트 ID**&#x200B;을(를) 사용하십시오.

### AJO 템플릿 탭이 표시되지만 템플릿이 표시되지 않음

* 페이지를 다시 로드하거나 **[!UICONTROL AJO 템플릿]** 탭을 다시 여십시오.
* 브라우저 **[!UICONTROL 네트워크]** 도구에서 **`get-templates`** 요청을 검사하십시오. **403 금지됨**&#x200B;을 반환하는 경우 기술 계정이 필요한 Journey Optimizer 권한이 있는 역할 또는 그룹에 할당되지 않습니다. 조직에 필요한 대로 [!DNL Adobe Experience Platform] **[!UICONTROL 권한]** 및 AJO **[!UICONTROL 권한]**&#x200B;에서 매핑을 업데이트하십시오.
