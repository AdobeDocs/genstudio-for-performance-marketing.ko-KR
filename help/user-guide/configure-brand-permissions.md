---
title: ' [!DNL Brand] 권한 할당'
description: GenStudio for Performance Marketing [!DNL Brand] 작성자 및 편집자에 대한 권한을 할당하는 방법에 대해 알아봅니다.
level: Intermediate
feature: Brand Personalization, Generative AI
exl-id: fc33ecd3-4403-4045-87af-012a0377226c
source-git-commit: adb1d34eb76d7594933fe9951c4c1885e6d6369b
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 1%

---

# [!DNL Brand] 권한 할당

기본적으로 GenStudio 시스템 관리자는 [!DNL Brands]을(를) 만들고 편집할 수 있습니다. 콘텐츠 편집기 및 공동 작업자 역할에는 편집 및 작성 권한이 있지만, 시스템 관리 권한이 필요하지 않을 수 있습니다.

콘텐츠 편집기 및 공동 작업자에게 이러한 [!DNL Brand] 관련 권한을 부여하려면 Adobe 시스템 관리자가 Adobe Admin Console에서 몇 가지 추가 구성 작업을 수행해야 합니다. [기업 및 팀 관리 가이드](https://helpx.adobe.com/kr/enterprise/using/admin-console.html#Overview)의 _Adobe Admin Console_&#x200B;을(를) 참조하십시오.

사용자 및 사용자 그룹 추가는 Admin Console을 통해 관리되는 권한이 있는 모든 Adobe 제품에 공통되는 기본 작업입니다. 사용자 관리 및 사용자 및 사용자 그룹 추가 절차에 대한 개요는 [Enterprise 및 Teams 관리 가이드](https://helpx.adobe.com/kr/enterprise/using/users.html)의 _Adobe Admin Console 사용자_&#x200B;를 참조하십시오.

이 비디오 연습을 시청하거나 아래 단계를 따르십시오.

>[!VIDEO](https://video.tv.adobe.com/v/3475004?learn=on&enablevpops&captions=kor)

## 1단계: 사용자 그룹 만들기

**사용자 그룹을 만들려면**:

1. Admin Console에 로그인하고 **[!UICONTROL 사용자]** > **[!UICONTROL 사용자 그룹]**(으)로 이동합니다.

1. **[!UICONTROL 새 사용자 그룹]**&#x200B;을 클릭합니다. _새 사용자 그룹 만들기_ 팝업이 열립니다.

1. 새 그룹의 목적을 식별하려면 **[!UICONTROL 사용자 그룹 이름]** 필드에 정보 있는 사용자 그룹 이름을 추가하십시오. 예를 들어 &quot;브랜드 관리자&quot;입니다.

1. 필요한 경우 그룹 및 해당 목적에 대한 설명을 추가합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다. Admin Console에서 새로 만든 그룹의 이름으로 _새 그룹_ 팝업이 열립니다.

[Enterprise 및 Teams 관리 가이드](https://helpx.adobe.com/kr/enterprise/using/user-groups.html)에서 _사용자 그룹 관리_&#x200B;를 참조하십시오.

## 2단계: 사용자 그룹에 GenStudio 시스템 관리자 프로필 할당

새 사용자 그룹을 만들고 사용자를 추가하면 **Adobe GenStudio 시스템 관리자** 프로필을 이 그룹에 할당할 수 있습니다. 할당된 프로필에 연결된 자격 부여를 통해 이 그룹의 모든 사용자에게 GenStudio [!DNL Brands] 권한(브랜드 만들기, 업데이트 및 삭제)을 제공합니다.

**사용자 그룹에 프로필을 할당하려면**:

1. 새로 만든 사용자 그룹으로 이동하여 _할당된 제품 프로필_ 탭을 클릭합니다.

1. _할당된 제품 프로필_ 탭에서 **[!UICONTROL 프로필 할당]**&#x200B;을 클릭합니다. _제품 및 프로필 할당_ 팝업이 열립니다.

1. `Adobe GenStudio`제품 선택&#x200B;_목록에서_&#x200B;을(를) 선택합니다.

1. **[!UICONTROL 적용]**&#x200B;을 클릭합니다. _제품 프로필 선택_ 팝업이 열리고 Adobe GenStudio과 연결된 제품 프로필이 표시됩니다.

1. `Adobe GenStudio system manager`을(를) 선택합니다.

1. **[!UICONTROL 적용]**&#x200B;을 클릭합니다. _제품 및 프로필 할당_ 팝업이 열리고 새로 만든 사용자 그룹의 제품 프로필이 표시됩니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

[엔터프라이즈 및 팀 관리 가이드](https://helpx.adobe.com/kr/enterprise/using/user-groups.html)에서 _사용자 그룹에 제품 프로필 할당_&#x200B;을 참조하세요.

## 3단계: 사용자 그룹에 사용자 추가

[!DNL Brands]을(를) 만들고 편집하고 게시할 수 있는 권한을 사용자에게 할당하려면 해당 권한을 새로 만든 사용자 그룹에 추가하십시오.

>[!NOTE]
>
>그룹을 프로젝트에 추가하기 전에 이 사용자 그룹에 사용자를 한 명 이상 추가해야 합니다.

**사용자 그룹에 사용자를 추가하려면**:

1. _Admin Console_&#x200B;에서 **[!UICONTROL 사용자]** > **[!UICONTROL 사용자 그룹]**(으)로 이동합니다.

1. 이전에 생성한 사용자 그룹의 이름을 선택합니다. _이 사용자 그룹에 사용자 추가_ 팝업이 열립니다.

1. 사용자 이름 또는 이메일 주소로 새 사용자 또는 기존 사용자를 추가합니다. 기존 사용자의 이름 또는 이메일 주소를 입력하면 이 IMS 조직에 속하는 알려진 사용자에 대해 일치하는 이름으로 이 필드가 자동으로 채워집니다. [Enterprise 및 Teams 관리 가이드](https://helpx.adobe.com/kr/enterprise/using/user-groups.html)의 _사용자 그룹 관리_&#x200B;에서 사용자 그룹 관리에 대해 알아봅니다.

사용자를 그룹에 추가하면 Adobe GenStudio 시스템 관리자의 [!DNL Brand] 만들기, 편집 및 게시 권한이 부여됩니다. 또한 사용자는 Adobe GenStudio for Performance Marketing [!DNL Brands] 프로젝트를 편집하기 위한 자동 전자 메일 초대를 받습니다.

## 4단계: [!DNL Brands] 프로젝트 만들기

_프로젝트_&#x200B;은(는) 선택한 사용자가 자산을 저장할 수 있는 저장소 위치를 제공합니다(이 경우 자산 [!DNL Brands]개).

**[!DNL Brands]저장소&#x200B;_탭에서_ 프로젝트를 만들려면**:

1. Admin Console에서 _저장소_ 탭으로 이동합니다.

1. 측면 탐색에서 **[!UICONTROL 프로젝트]**&#x200B;를 클릭합니다. _프로젝트_ 탭이 열립니다.

1. **[!UICONTROL 프로젝트 만들기]**&#x200B;를 클릭합니다. _새 프로젝트_ 팝업이 열립니다.

1. 프로젝트 이름 필드에 `Adobe GenStudio Brands`을(를) 입력하십시오. 여기에 표시된 대로 이 프로젝트 이름을 정확히 입력하십시오. 공백은 추가하지 말고 문자를 바꾸지 마십시오.

1. Click **[!UICONTROL Create]**. _프로젝트에 초대_ 팝업이 열립니다.

[Enterprise 및 Teams 관리 가이드](https://helpx.adobe.com/kr/enterprise/using/projects-in-business-storage.html)에서 _프로젝트 관리_&#x200B;를 참조하십시오.

## 5단계: 사용자 그룹을 프로젝트에 초대

이제 방금 만든 사용자 그룹을 `Adobe GenStudio [!DNL Brands]` 프로젝트에 추가할 준비가 되었습니다.

**새로 만든 프로젝트에 사용자 그룹을 초대하려면**:

1. _프로젝트에 초대_ 팝업에서 방금 만든 사용자 그룹을 이 프로젝트에 추가합니다.

1. **편집 가능** 권한 옵션을 선택합니다.

1. **[!UICONTROL 초대]**&#x200B;를 클릭합니다.
