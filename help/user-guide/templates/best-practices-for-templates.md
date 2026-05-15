---
title: 템플릿 우수 사례
description: Adobe GenStudio for Performance Marketing에서 템플릿을 사용할 때 모범 사례를 따르십시오.
level: Intermediate
role: Developer, User
feature: Media Templates, Content Generation, Brand Personalization
exl-id: 3ff24fec-e836-4202-80f8-ba165e173b75
TQID: https://experienceleague.adobe.com/fiKHSZ-YFZ2gSD5iZ-aKaZtsC49Mrj1dqHpHqtbXZVM
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
feature_v2:
  - id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3a
  - id: f71bd2fc-e9ca-4cb6-8088-82e250211e32
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 3322f783cd49ddcb897942e5e91590d53b554bdd
workflow-type: tm+mt
source-wordcount: 1347
ht-degree: 0%

---

# 템플릿 사용 우수 사례

템플릿은 사전 구성된 레이아웃 및 디자인 요소를 포함하는 시작점을 제공하여 새 콘텐츠를 생성하는 데 필요한 시간과 노력을 크게 줄입니다.

GenStudio for Performance Marketing에서 템플릿을 사용할 때 다음 권장 사항을 준수하십시오.

1. [템플릿 요소](#know-about-template-elements)에 대해 알아보기
1. 콘텐츠의 효과적인 개인화를 위해 [채널 지침](#configure-channel-guidelines)을(를) 구성하십시오.
1. 최적의 환경을 위해 [접근성 표준](accessibility-for-templates.md)으로 디자인
1. [채널별 템플릿 지침 준수](#follow-channel-specific-template-guidelines)
1. [빠른 템플릿](/help/user-guide/templates/express-templates.md)을 사용하는 경우 [GenStudio으로 빠른 템플릿 모범 사례](#express-to-genstudio-template-best-practices)의 특정 팁을 고려하십시오.
&#x200B;>>
[템플릿 작업](use-templates.md)에서 템플릿 요소 및 프로시저의 기본 사항에 대해 알아봅니다. 다음 캠페인에서 사용할 특정 지침을 보려면 [템플릿 사용자 지정](customize-template.md)에 대해 자세히 알아보십시오.

## 올바른 템플릿 요소 사용

각 템플릿 유형은 서로 다른 요소를 사용하여 채널별 콘텐츠 작성 구조를 만듭니다. [템플릿의 일부를 숙지하고](use-templates.md#template-elements) 콘텐츠와 템플릿 유형에 가장 적합한 요소를 포함하십시오.

템플릿을 사용자 지정할 때 콘텐츠를 생성하기 위해 GenStudio for Performance Marketing이 필요한 이러한 요소 대신 필드 이름을 사용하십시오.

[템플릿 요소](use-templates.md#template-elements)를 참조하십시오.

## 템플릿에서 자리 표시자 텍스트 사용

자리 표시자 텍스트는 나중에 사용자가 템플릿에서 채울 콘텐츠의 구문 또는 구조를 정의하는 데 도움이 될 수 있습니다. 예를 들어 {first_name}.{last_name}@email과 같은 형식으로 전자 메일 주소를 정의하십시오. 그러나 일부 일반적인 구분 기호는 GenStudio for Performance Marketing에서 다른 의미로 이미 예약되어 있습니다.

❌ `< >` - HTML 태그에 사용 중입니다.
❌ `{{ }}` - Handlebar 식에 사용 중입니다.

기존 태그와 혼동하지 않도록 자리 표시자 텍스트를 표시하려면 단일 대괄호(직선형 또는 중괄호형)를 사용하십시오.

✅ `{first_name}` - 이름의 자리 표시자

## 채널 지침 구성

명확한 채널 지침을 정의하는 것은 생성된 콘텐츠가 브랜드의 요구 사항 및 목표에 부합하는지 확인하는 데 필수적입니다. 채널 가이드라인을 사용하여 템플릿에 사용되는 톤, 길이 및 스타일과 같은 요소에 대한 규칙을 지정할 수 있습니다. 예를 들어 본문의 최대 문자 수를 설정하거나 특정 call-to-action 스타일이 필요할 수 있습니다. 이러한 지침을 미리 설정하면 각 AI 프롬프트에서 자세한 지침을 작성할 필요가 줄어들어 콘텐츠 생성 프로세스를 간소화하고 이메일 전반에서 일관성을 보장할 수 있습니다.

템플릿의 모든 키 필드에 대한 브랜드의 [채널 지침](/help/user-guide/guidelines/brands.md#channel-guidelines)을 검토하고 정의합니다. 지침을 정의하지 않으면 [기본 채널 지침](/help/user-guide/guidelines/brands.md#default-channel-guidelines)이 적용되며, 이는 브랜드 요구 사항을 완전히 반영하지 않을 수 있습니다.

![본문 사양](/help/assets/channel-email-body.png)

[브랜드, 제품 및 가상 사용자 지침](/help/user-guide/guidelines/overview.md)이 생성된 콘텐츠에 어떻게 영향을 미치며 마케팅 목표에 맞게 콘텐츠를 조정하는 방법을 알아봅니다.

## 템플릿에 대한 이미지 업로드

템플릿에 사용되는 이미지는 컨텐츠 리포지토리에서 가져와야 하며, 이미지가 정확하게 표시되도록 하려면 올바르게 업로드해야 합니다.

템플릿에 가장자리에서 가장자리로(전체 도련) 이미지가 있으면 선택한 이미지의 크기가 전체 템플릿 크기에 맞게 자동으로 조정됩니다. 그러나 이미지가 템플릿 종횡비와 일치하지 않으면 이미지가 템플릿 크기에 맞게 잘리며 예상대로 표시되지 않을 수 있습니다.

템플릿에 포함된 이미지에 대한 &quot;자동 맞춤&quot; 기능은 없습니다.

이미지 자르기를 해결하려면 사용자는 콘텐츠 저장소에 업로드할 때 템플릿에 사용할 이미지의 종횡비를 정의해야 합니다. 승인된 템플릿을 업로드할 때:

1. [템플릿 업로드 프로세스를 계속 진행](/help/user-guide/templates/use-templates.md#add-a-template)한 다음 **[!UICONTROL 세부 정보 추가]** 페이지에 액세스합니다.

2. 템플릿에 사용할 이미지의 종횡비를 **[!UICONTROL 광고 너비(px)]** 및 **[!UICONTROL 광고 높이(px)]**&#x200B;로 정의합니다. 이렇게 하면 이미지가 표시되는 템플릿의 섹션에 대한 이미지 창이 정의됩니다.

3. **[!UICONTROL 추가 세부 정보]** 섹션에서 **[!UICONTROL 이미지 크기]** 드롭다운을 선택하고 _고정 크기로 자르기_를 선택합니다.
   ![고정 크기로 자르기](images/crop-to-fixed-size.png "고정 크기로 자르기"){width="80%"}

브라우저에서 이미지의 크기 및 종횡비를 결정하려면 다음을 수행하십시오.

1. 이미지를 검사합니다.
   - Windows/Linux의 경우:
      - F12 키를 누릅니다.
   - macOS에서:
      - Command + Option + I를 누릅니다.

1. 이미지 위로 마우스를 가져갑니다.

1. 종횡비를 확인합니다. 템플릿에서 이미지의 종횡비를 정의할 때 사용합니다.

이러한 세부 사항이 업로드 중에 적용되지 않으면 이미지는 템플릿의 전체 종횡비로 간주되며 해당 종횡비와 일치하지 않는 이미지는 잘린 것으로 표시됩니다.

![디스플레이 광고에서 자른 이미지](images/cropped-display.png "이미지 자르기"){width="60%"}

디스플레이 광고 템플릿에서 잘린 **❌이미지**

![디스플레이 광고에 표시되는 이미지](images/full-fit.png "디스플레이 광고에 표시되는 이미지"){width="60%"}

**✅이미지가 완전히 표시됨**

## 채널별 템플릿 지침 준수

템플릿을 만들 때 의도한 채널의 특정 요구 사항을 충족하는지 확인하십시오. 각 채널의 레이아웃 및 시각적 요구 사항을 충족하는 템플릿을 빌드합니다. 다음과 같이 모든 템플릿에 적용되는 일반 지침이 있습니다.

- 깔끔하고 반응형 HTML 및 인라인 CSS 사용
- Adobe 또는 Google 글꼴 사용
- JavaScript을 사용하지 **않음**

{{note-css-effects}}

최적의 성능을 보장하기 위해 각 템플릿 유형을 사용할 때 다음과 같은 추가 팁과 제한을 참조하십시오.

- [이메일](/help/user-guide/templates/email-template.md)
- [광고 표시 및 배너](/help/user-guide/templates/display-template.md)
- [LinkedIn](/help/user-guide/templates/linkedin-template.md)
- [Meta 광고](/help/user-guide/templates/meta-template.md)

## Express to GenStudio 템플릿 모범 사례

다음 팁을 통해 [!DNL Adobe Express]의 디자인을 [!DNL GenStudio for Performance Marketing]의 템플릿으로 변환할 때 신뢰할 수 있는 결과를 얻을 수 있습니다.

### 다중 변형 템플릿 사용

[!DNL Adobe Express]에서 페이지는 하나의 템플릿 파일에 여러 크기 또는 종횡비의 변화를 나타낼 수 있습니다.
[!DNL GenStudio for Performance Marketing]에서 템플릿을 선택하면 모든 변형이 캔버스에 나타납니다.

이 동작은 파일당 하나의 변형만 지원하는 HTML 템플릿에서 개선됩니다.

### 마케터가 편집할 수 있는 내용을 제어하는 필드 잠금

잠금을 사용하여 의도를 전달합니다. 예를 들어 AI가 생성되지 않도록 법적 면책조항을 잠그고 세대별로 헤드라인을 유연하게 남겨 둡니다.

잠금 동작을 설정하려면 [!DNL Adobe Express]의 요소를 마우스 오른쪽 단추로 클릭하십시오.

- **[!UICONTROL 전체 잠금]** — 요소가 정적이고 AI가 이 요소에 대한 콘텐츠를 생성하지 않습니다.
- **[!UICONTROL 잠금, 이미지 바꾸기 허용]** — 크기와 위치를 잠그지만 사용자가 이미지를 바꿀 수 있도록 합니다. 이 옵션은 로고에 적합합니다.
- **[!UICONTROL 잠금, 텍스트 바꾸기 허용]** - 크기와 위치를 잠그지만 사용자가 텍스트를 편집할 수 있도록 합니다. AI는 이에 대한 콘텐츠를 자동으로 생성하지 않습니다.
- **완전히 유연한**(잠금 해제) - 사용자는 요소를 이동하고 크기를 조정할 수 있으며 AI는 생성할 콘텐츠로 처리합니다.

### 더 나은 AI 매핑을 위해 레이어 이름 지정

디자인을 템플릿으로 변환하면 AI가 디자인을 스캔하고 헤드라인, CTA, 본문 사본과 같은 필드를 매핑합니다. AI가 매우 복잡한 레이아웃보다 간단한 템플릿을 더 자주 정확하게 매핑합니다.

**모범 사례:** 자리 표시자 복사본에 AI 맵 필드를 올바르게 만드는 데 도움이 되도록 의도한 필드 형식(예: `headline`, `sub-headline` 또는 `CTA`)을 포함하십시오. 이 방법을 사용하면 매핑 오류가 줄어들 수 있습니다.

### 템플릿으로 변환

1. [!DNL Adobe Express]에서 **[!UICONTROL 공유]** > **[!UICONTROL 템플릿으로 변환]**&#x200B;을 클릭합니다.
1. **[!UICONTROL 정보]** 탭과 **[!UICONTROL 잠금]** 탭만 [!DNL GenStudio for Performance Marketing]&#x200B;(으)로 이월됩니다.
1. 전환 시 잠금 해제 작동 방식을 선택합니다.
   - **[!UICONTROL 사용자 잠금 해제 허용]**
   - **[!UICONTROL 모든 잠금 해제 방지]**
   - **[!UICONTROL 암호 설정]** — 액세스를 영구적으로 차단하지 않고 일반적인 변경을 금지하는 중간 영역입니다.

### 원본 디자인 파일의 복사본 보관

변환하면 별도의 [!DNL Adobe Express] 템플릿 파일이 만들어지지만 원본 디자인 파일은 편집 가능합니다.

**팁:** 디자인을 수정하고, 변형을 만들고, 나중에 새 템플릿을 생성할 수 있도록 원본을 유지합니다.

### 공유를 통한 가시성 향상

변환 후 템플릿은 기본적으로 사용자에게만 표시됩니다. 개인 또는 조직 전체와 공유할 수 있습니다.

**요구 사항:** [!DNL Adobe Express] 및 [!DNL GenStudio for Performance Marketing]에서 템플릿을 동기화하려면 동일한 IMS 조직을 사용해야 합니다. 템플릿은 보통 변환 직후 [!DNL GenStudio for Performance Marketing]에 나타납니다.

### AI 필드 매핑 제어

템플릿을 선택하면 AI가 템플릿당 한 번씩 필드를 매핑하여 **[!UICONTROL 기본 미디어]**, **[!UICONTROL 생성]** 또는 **[!UICONTROL 잠김]**&#x200B;과 같은 레이블을 할당합니다. AI가 필드를 잘못 할당하면 매핑을 수동으로 조정할 수 있습니다.

필드 당 **[!UICONTROL 생성 활성화]** 토글을 사용하여 생성하기 전에 켜거나 끕니다. AI가 필드를 잘못 할당하면 매핑을 수동으로 조정할 수 있습니다. 템플릿 매핑에 대한 영구 수정은 향후 릴리스에서 계획됩니다.

### [!DNL Adobe Express]에서 디자인, [!DNL GenStudio for Performance Marketing]에서 결합

각 서비스를 최대한 활용하려면 다음 디자인 워크플로를 고려하십시오.

- [!DNL Adobe Express]에서 색상, 레이아웃 및 그래픽과 같은 디자인 작업을 완료합니다.
- [!DNL GenStudio for Performance Marketing]을(를) 사용하여 해당 템플릿에서 콘텐츠를 조합하고 생성합니다.
- 디자인 거버넌스에 [!DNL Adobe Express]개 브랜드(색상, 로고, 글꼴 및 그래픽)를 사용합니다.
- 생성 후 글꼴 색상 변경에 [!DNL GenStudio for Performance Marketing]개 브랜드를 사용합니다.

### 이메일 제한 사항

[!DNL Adobe Express] 템플릿 워크플로우의 Horizon 캔버스에서 이메일이 **지원되지 않음**&#x200B;입니다. 이메일은 기존 HTML 템플릿 프로세스를 계속 사용합니다.

### 사용자 정의 글꼴 활용

팀은 종종 [!DNL Adobe Express] 템플릿에서 사용자 지정 글꼴이 작동하는 방식을 묻습니다. 관리자는 Admin Console에서 사용자 정의 글꼴 자격 제안을 수락해야 해당 글꼴을 사용할 수 있습니다. [사용 [!DNL Adobe Express] 템플릿](express-templates.md)을 참조하세요.
