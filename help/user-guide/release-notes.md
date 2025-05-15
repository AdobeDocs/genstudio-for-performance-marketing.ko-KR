---
title: Adobe GenStudio for Performance Marketing 릴리스 노트
description: 성과 마케팅을 위한 Adobe GenStudio의 최신 기능 및 개선 사항에 대해 알아봅니다.
recommendations: noDisplay
role: User
exl-id: 32f5104e-ae15-4092-8a34-642fc641baf9
source-git-commit: c3c3ca28d31539383863cf7c8ad11a24aed0965f
workflow-type: tm+mt
source-wordcount: '2300'
ht-degree: 0%

---

# GenStudio for Performance Marketing 릴리스 노트

이 릴리스 정보는 GenStudio for Performance Marketing 애플리케이션에 대한 최신 업데이트를 자세히 설명합니다.

## 2025.05.15 {#latest}

### 수정 사항 및 개선 사항

* 개별 변형의 이미지에 [대체(alt) 텍스트를 추가](/help/user-guide/create/manage-variants.md#add-alt-text-for-images)하는 기능을 사용하도록 설정했습니다.
* [새로운 메타 종횡비](/help/user-guide/content/best-practices-for-templates.md#follow-channel-specific-template-guidelines) —가로 1.19:1(1080픽셀 너비)이 추가되었습니다.
* 이제 내보내기 또는 다운로드를 위해 두 개 이상의 경험을 선택할 수 있습니다. [경험 내보내기](/help/user-guide/content/manage-assets.md#export-experiences)를 참조하십시오.
<!-- * Added support for [publishing ad experiences](/help/user-guide/activation/activate-meta-ad.md) directly from _[!DNL Content]_ [into Google Campaign Manager 360 and Meta Ads Manager](/help/user-guide/activation/activate-cm360-ad.md). -->

## 이전 릴리스 노트

+++2025.05.15 릴리스 정보

### 수정 사항 및 개선 사항

* 템플릿에 대한 새로운 필터 옵션! 이제 [!DNL Create] 및 _[!UICONTROL 콘텐츠]_ > _[!UICONTROL 템플릿]_&#x200B;에서 _[!UICONTROL 템플릿 선택]_ 목록을 개선할 수 있습니다. [템플릿 검색](/help/user-guide/content/use-templates.md#search-templates)을 참조하세요. 이러한 필터를 통해 검색할 수 있도록 템플릿에 메타데이터가 올바르게 태그 지정되었는지 확인합니다.
* 콘텐츠 재생성이나 이미지 자르기 등 수정 시 강조할 수 있도록 경험의 [개별 레이어(편집 가능한 텍스트 필드 또는 편집 가능한 이미지)를 보고 선택하는 기능을 활성화했습니다](/help/user-guide/create/manage-variants.md#view-layers).
* 대상자의 관심을 끌고 마케팅 메시지를 강조하기 위해 경험의 추가 텍스트에 대해 [새 템플릿 필드](/help/user-guide/content/use-templates.md#template-elements), `sub-headline`을(를) 추가했습니다.
* GenStudio for Performance Marketing에서 Google Campaign Manager 360으로 [광고 경험 게시](/help/user-guide/activation/overview.md)에 대한 지원을 추가했습니다. [활성화]는 Campaign Manager 360 광고주에게 게시하기 전에 자세한 Google Campaign Manager 360 광고 미리보기를 지원합니다. [활성화]를 통해 게시된 광고는 라이브가 되면 자동으로 Insights로 가져와서 사용자가 광고 성과를 추적하고 보고할 수 있습니다.

+++2025.03.13 릴리스 정보

### 메타 광고 활성화

이제 마케터는 GenStudio for Performance Marketing에서 메타 광고 관리자로 광고 경험을 [게시](/help/user-guide/activation/overview.md)할 수 있습니다. [!DNL Activate]은(는) 배포 전에 자세한 메타데이터 미리 보기를 지원합니다. [!DNL Activate]을(를) 통해 게시된 메타 광고는 라이브 상태가 되면 자동으로 [!DNL Insights]&#x200B;(으)로 가져와서 사용자가 광고 성능을 추적하고 보고할 수 있습니다.

### LinkedIn 경험 만들기

[!BADGE Beta]{type=Informative tooltip="이 기능은 현재 Beta에 있으므로 일부 기능이 제한되거나 변경될 수 있습니다."}

[LinkedIn 경험 만들기](/help/user-guide/create/create-linkedin.md)에 대한 지원이 추가되었습니다. 채널별 지침에서 [LinkedIn 광고](/help/user-guide/content/best-practices-for-templates.md#follow-channel-specific-template-guidelines) 탭을 참조하십시오.

### 배너 경험 만들기

[!BADGE Beta]{type=Informative tooltip="이 기능은 현재 Beta에 있으므로 일부 기능이 제한되거나 변경될 수 있습니다."}

[배너 경험 만들기](/help/user-guide/create/create-banner-experience.md)에 대한 지원을 추가했습니다. 채널별 지침에서 [배너](/help/user-guide/content/best-practices-for-templates.md#follow-channel-specific-template-guidelines) 탭을 참조하십시오.

### 규정 준수

브랜드 유효성 검사 프로세스의 일부로 [콘텐츠 검사](/help/user-guide/guidelines/brand-validation.md)에 [준수 표준](/help/user-guide/guidelines/overview.md)이 도입되었습니다. 이러한 검사는 [!DNL Brand] 지침, 플랫폼 지침(예: 메타의 경우) 및 ADA 표준에 대해 경험의 각 변형을 검토합니다. 이 프로세스에서는 규정 준수 향상을 위해 개정이 필요한 지침과 표준을 포괄적으로 요약하여 제공합니다.

### 확장성

새로운 GenStudio for Performance Marketing [확장성 프레임워크](/help/extensibility/overview.md)는 추가 기능 또는 확장 가능한 응용 프로그램을 통해 조직에서 자체 클레임 규정 준수 프로토콜을 콘텐츠 만들기 워크플로 및 유효성 검사에 통합할 수 있는 도구를 제공합니다.

### 템플릿

* **템플릿 코드 편집기**—새로운 [템플릿 코드 편집기](/help/user-guide/content/code-editor.md)를 사용하면 GenStudio for Performance Marketing으로 새로운 경험을 생성할 때 최적의 사용을 위해 템플릿을 확인하고 구체화할 수 있습니다.

  ![코드 편집기 보기](/help/assets/template-detected-fields.png "검색된 필드 확인"){width="500" zoomable="yes"}

* **이미지에 있는 링크**—이미지 링크를 활성화하여 전자 메일 템플릿을 사용자 지정합니다. [템플릿 사용자 지정: 이미지에 대한 링크](/help/user-guide/content/customize-template.md#link-on-image)를 참조하십시오.
* **AJO 및 Marketo 템플릿** - Adobe Journey Optimizer(AJO) 또는 Marketo에서 만든 템플릿을 업로드합니다. [AJO 및 Marketo의 템플릿 작업](/help/user-guide/content/use-templates.md#templates-from-ajo-and-marketo)을 참조하세요.

### 수정 사항 및 개선 사항

* [[!DNL Brands]](/help/user-guide/guidelines/brands.md)을(를) 위해 [기본 채널](/help/user-guide/guidelines/brands.md#channel-guidelines), [이미지](/help/user-guide/guidelines/brands.md#image-guidelines), [로고](/help/user-guide/guidelines/brands.md#logos) 및 [색상](/help/user-guide/guidelines/brands.md#colors) 지침에 대한 기능을 활성화했습니다.
* 변형 내에서 [이미지에 링크를 추가](/help/user-guide/create/manage-variants.md#add-image-link)하는 기능이 추가되었습니다.
* 캔버스에서 공간을 최대화하고 사용자 환경을 개선하기 위해 [콘텐츠 확인](/help/user-guide/guidelines/brand-validation.md) 및 검토 및 승인 기능을 새 오른쪽 작업 표시줄로 이동했습니다.
* [브랜드를 업로드하거나 수동으로 추가](/help/user-guide/guidelines/add-guidelines.md#add-brands)하는 동안 흐름이 간소화되었습니다.
* 캔버스에서 [변형 내의 이미지 자산을 추가 또는 교체](/help/user-guide/create/manage-variants.md#swap-image)하는 기능이 도입되었습니다.
* 소유한 미디어, 유료 미디어 및 콘텐츠 섹션으로 구분하여 만들기 홈[&#128279;](/help/user-guide/create/overview.md)에서 채널 범주 의 사용자 경험과 가시성을 개선했습니다.
* [!DNL Insights] 테이블 및 갤러리 보기에서 필터링을 개선했습니다.

+++

+++2025.02.13 릴리스 정보

### [!DNL Create]의 랜딩 페이지 개선 사항

GenStudio for Performance Marketing의 [!DNL Create] 랜딩 페이지에는 사용자 경험을 개선하는 UI 개선 사항이 포함되어 있습니다. _최근 작업_ 섹션이 목록 보기를 기본 보기로 사용하여 세분화되고 구성되었습니다. 패딩 및 기타 시각적 개선 사항을 통해 [!DNL Create] 캔버스의 모양과 느낌을 간소화할 수 있습니다.

### CSV로 인사이트 내보내기

이제 [!DNL Insights] 보기에서 볼 수 있는 테이블을 CSV 파일로 다운로드할 수 있습니다. 이 기능을 사용하면 다양한 [!DNL Insights] 보기에서 데이터를 내보내고 분석할 수 있으므로 데이터 분석 및 보고 옵션을 용이하게 합니다.

+++

+++2025.01.16 릴리스 정보

### Adobe Workfront Proof와 통합

[!BADGE Beta]{type=Informative tooltip="이 기능은 현재 Beta에 있으므로 일부 기능이 제한되거나 변경될 수 있습니다."}

GenStudio for Performance Marketing 및 Adobe Workfront Proof 통합 Beta 프로그램은 이번 달에 시작됩니다. Workfront Proof은 승인 템플릿, 다단계 워크플로우 및 주석을 통해 콘텐츠 생성 및 활성화 라이프사이클을 향상시킵니다. Workfront Proof 권한이 있는 GenStudio for Performance Marketing 사용자는 GenStudio for Performance Marketing 내에 있는 Proof의 고급 기능을 사용하여 GenStudio 생성 콘텐츠를 검토하고 댓글을 달 수 있습니다.

Beta 프로그램은 제품 개발을 구체화하고 일반 가용성 준비를 결정하는 데 도움이 되는 방법을 제공합니다.

### 새 콜 투 액션 생성

이제 변형을 관리할 때 새 call-to-action(CTA) 구문을 생성할 수 있습니다. 새 _구문 변경_ 및 _링크 추가_ 옵션을 사용하여 새 구문을 생성하고 CTA 링크를 편집합니다. 이러한 새로운 CTA 기능을 사용하려면 템플릿을 올바르게 설정해야 합니다. _템플릿 사용자 지정_&#x200B;의 지침을 따르십시오. [작업 호출](/help/user-guide/content/customize-template.md#calls-to-action). 변형의 CTA 관리에 대한 지침은 [콜 투 액션 수정](/help/user-guide/create/manage-variants.md#revise-call-to-action)을 참조하십시오. <!-- GS-6676 -->

### 수정 사항 및 개선 사항

* 이제 표시 광고의 생성된 모든 필드 및 수동 필드에 문자 수가 표시됩니다. [메타 경험](/help/user-guide/create/meta-experiences.md#character-counts)에서 _문자 수_&#x200B;를 참조하십시오. <!-- GS-7732 -->

* _공동 작업자_&#x200B;가 이제 자산을 볼 수 있지만 이러한 자산을 만들거나 편집하거나 삭제할 수는 없습니다. 이전에는 [!DNL Create]에서 예상대로 Collaborator 권한이 적용되지 않았습니다. <!-- GS-7614 -->

* 이제 콘텐츠 편집기에서 에셋, 경험 및 템플릿 메타데이터를 편집할 수 있습니다. <!-- GS-4905 -->

* 이제 메타데이터 템플릿 내의 사용자 지정 이미지 크기가 지원됩니다. <!-- GS-7512 -->

* 이제 템플릿 생성 중 사용자, 브랜드 및 제품 선택이 미리 로드됩니다. <!-- GS-8069 -->

* 이메일 call-to-action 링크는 더 이상 필수 필드가 아닙니다. <!-- GS-8103 -->

* 이제 [!DNL Brand] 선택기 드롭다운 메뉴가 템플릿의 예상대로 작동합니다. 이전에는 선택기가 일부 템플릿에 대해 성공적으로 로드되지 않았습니다. <!-- GS-8908 -->

* 이제 편집자는 단일 Pod 이메일 및 메타 광고에 대해 최대 4개의 이미지를 선택할 수 있습니다. <!-- GS-2631 -->

* 승인된 경험의 `Created by` 필드에 대한 연도 값이 이제 경험의 메타데이터를 편집한 후에도 예상대로 일관되게 유지됩니다. <!-- GS-8344 -->

* 이제 콘텐츠 편집기에서 [!DNL Create]에서 템플릿을 선택할 수 있습니다. 이전에는 편집기가 템플릿을 선택할 때 애플리케이션에서 콘솔 오류가 발생했습니다.  <!-- GS-8798 -->

* 메타 광고에 대한 크기 조정 및 재생성 작업 관련 문제가 해결되었습니다. <!-- GS-8900 -->

* 이제 **[!UICONTROL 뒤로]** 단추가 예상대로 사용자를 이전 페이지 또는 [!DNL Create] 랜딩 페이지로 돌아갑니다. <!-- GS-8622 -->

+++

+++2024.12.12 릴리스 정보

### 새로운 기능

이제 편집자는 다음 메타데이터 관련 작업을 수행할 수 있습니다.

* 에셋, 경험 및 템플릿 메타데이터를 편집합니다. [자산 정보](/help/user-guide/content/asset-details.md#user-defined-metadata)를 참조하세요. <!-- GS-4905 6935-->

* 자산을 사용하는 모든 경험의 _세부 정보_ 보기에서 자산이 생성한 태그를 봅니다. [에셋 세부 정보](/help/user-guide/content/asset-details.md#generated-tags)에서 _생성된 태그_&#x200B;를 참조하십시오. <!-- GS-3705 -->

이제 편집기는 생성된 변형의 이러한 측면에 사용자 지정 값을 지정할 수 있습니다.

* 디스플레이 광고 템플릿의 웹 배너에 대한 너비 및 높이입니다. 이러한 값은 이제 템플릿 메타데이터로 저장됩니다. <!-- GS-6735 -->

* 이미지를 업로드하는 동안 디스플레이 광고 경험의 이미지에 대한 차원입니다.<!-- GS-7166 -->

* [템플릿 모범 사례](/help/user-guide/content/best-practices-for-templates.md#follow-channel-specific-template-guidelines)에서 채널별 지침을 참조하십시오.

이제 내보내기 옵션에 포함되는 사항:

* 디스플레이 광고 및 메타 광고를 HTML, JPEG 또는 PNG로 내보냅니다. [디스플레이 광고 경험 만들기](/help/user-guide/create/create-display-ad.md) 및 [메타 광고 경험 만들기](/help/user-guide/create/create-meta-ad.md)를 참조하십시오. <!-- GS-7093 6655 5152-->

새로운 추가 기능을 통해 편집자는 다음과 같은 작업을 수행할 수 있습니다.

* [!DNL Content] 템플릿 _자산 세부 정보_ 보기에서 **[!UICONTROL 새로 고침]** 단추를 사용하여 선택한 템플릿을 새로 고치십시오. <!-- GS-7102 -->

* 디스플레이 광고 및 이메일 변형 섹션을 재생성합니다. [디스플레이 광고 경험 만들기](/help/user-guide/create/create-display-ad.md#revise-generated-display-ads) 및 [이메일 경험 만들기](/help/user-guide/create/create-email-experience.md#revise-generated-emails)를 참조하십시오. <!-- GS-5080 5078-->

* 기존 브랜드를 복제합니다. [브랜드 관리](/help/user-guide/guidelines/brands.md#manage-brands)를 참조하십시오. <!-- BRANDS-548 -->

### 수정 사항 및 개선 사항

* 이제 디스플레이 광고 제목이 예상대로 [!DNL Content]에 저장됩니다. <!-- GS-7239 -->

* 편집기가 서랍 드롭다운 메뉴 외부를 클릭할 때 프롬프트 서랍이 더 이상 닫히지 않습니다. <!-- GS-7275 -->

* 썸네일 URL 서비스 오류가 발생하면 이제 [!DNL Create] [!DNL Persona]/[!DNL Product] 드롭다운 메뉴가 예상대로 로드됩니다. <!-- GS-7277 -->

* 이제 조각 오버레이가 가능한 요소가 포함된 디스플레이 광고를 편집할 수 있습니다. <!-- GS-7186 -->

* 경험에 대한 브랜드 점수가 생성되지 않으면 이제 캔버스 **[!UICONTROL 브랜드]** 단추가 비활성화됩니다. <!-- GS-6429 -->

* 이제 캔버스에 크기가 조정된 경험이 일관된 순서로 표시됩니다. <!-- GS-7123 -->

* 이제 수동 자르기는 디스플레이 광고를 편집할 때 템플릿 차원이 아닌 이미지 차원을 사용합니다. 이전에는 이미지가 디스플레이 광고 템플릿에 지정된 치수보다 작을 때 경계 상자에서 이미지 치수가 아닌 템플릿 치수를 사용했습니다. <!-- GS-7315 -->

* 이제 편집자는 디스플레이 광고를 만들 때 최대 4개의 이미지를 선택할 수 있습니다. <!-- GS-7189 -->

* 다른 브라우저에서 크기를 조정할 때 광고 및 메타 광고 초안이 예상대로 로드됩니다. <!-- GS-7204 -->

* 사용되지 않은 템플릿 필드는 생성된 콘텐츠에 더 이상 표시되지 않습니다.  <!-- GS-5670 -->

* 이제 편집자는 생성된 변형에서 예상대로 편집할 링크를 한 번 클릭할 수 있습니다. <!-- GS-7423 -->

* 이제 [!DNL Create]이(가) 공동 작업자 권한을 올바르게 준수합니다. <!-- GS-7614 -->

* 모든 크기 조정 옵션을 선택하고 렌더링한 후에는 캔버스 **[!UICONTROL 크기 조정]** 단추가 비활성화됩니다. <!-- GS-5940 -->

* 이제 보기 전용 액세스 권한이 있는 검토자는 검토 중에 변형을 확대 및 축소할 수 있습니다. <!-- GS-7371 -->

* [!DNL Create] _최근 작업_ 보기의 실행 가능한 단추에만 키보드 포커스가 추가되었습니다. <!-- GS-4060 -->

* 전자 메일 조각 저장 작업 중에 표시되는 **저장 진행 중** 메시지가 이제 저장 작업 중에만 표시됩니다. 이전에는 캔버스에 이 메시지가 무기한으로 표시되었습니다. <!-- GS-6964 -->

* 이제 편집자는 [!DNL Create] _최근 작업_ 영역에서 초안이 로드되지 않을 때 예상대로 오류 메시지를 볼 수 있습니다.  <!-- GS-8081 -->

* 이제 캔버스에 크기 조정된 메타 광고가 표시되고 올바른 순서로 광고가 표시됩니다.  <!-- GS-7375 -->

* 이제 편집자는 이메일의 필드를 한 번 클릭하고 광고를 표시할 수 있습니다. <!-- GS-6297 -->

* 이메일 및 메타 광고에 대한 조각 편집 기능이 이제 한 번의 클릭으로 예상대로 트리거됩니다. <!-- GS-8081 -->

* [!DNL Create] **[!UICONTROL 뒤로]** 단추의 성능이 향상되었습니다. <!-- GS-6767 -->

+++

+++2024.11.14 릴리스 정보

### 새로운 기능

외부 도메인에 호스팅된 정적 콘텐츠 표시에 대한 지원을 추가했습니다. GenStudio for Performance Marketing은 템플릿에 정의된 콘텐츠 소스의 유효성을 검사하고 사본을 임베드하여 템플릿 미리 보기를 생성합니다. [정적 콘텐츠](/help/user-guide/content/customize-template.md#static-content)를 참조하십시오. <!-- GS-6107 -->

### 수정 사항 및 개선 사항

* 초기 콘텐츠를 생성하는 데 사용되는 브라우저 이외의 브라우저에서 크기를 조정하면 이제 예상대로 초안이 로드됩니다. <!-- GS-7204 -->

* 이제 내보낸 HTML에 모든 문자가 올바르게 표시됩니다. <!-- GS-7246 -->

* [!DNL Content] _경험_ **[!UICONTROL 내보내기]** 팝업의 단추가 더 이상 특정 언어로 잘리지 않습니다. <!-- GS-6873 -->

* 50x50 크기의 템플릿으로 만든 디스플레이 광고를 이제 예상 이미지 크기로 내보냅니다. 이전에는 PNG 파일을 예상 차원의 두 배로 내보냈습니다. <!-- GS-7192 -->

* 디스플레이 광고 크기가 조정되었을 때 발생한 템플릿 오류가 이제 해결되었습니다. <!-- GS-7322 -->

### 로컬라이제이션

이 릴리스에는 다음을 포함하여 UI 전체의 현지화에 대한 개선 사항이 포함됩니다.

* 이제 [!DNL Content] _자산 업로드_ 팝업의 모든 문자열이 올바르게 현지화되었습니다. <!-- GS-6872 6770 -->
* [!DNL Content] _Assets_ 보기 **[!UICONTROL 검색]** 필드의 모든 도구 설명이 지역화되었습니다. <!-- GS-6879 -->
* [!DNL Create] 캔버스에서 전자 메일 변형의 기존 이미지를 바꿀 때 _콘텐츠에서 선택_ 보기가 현지화되었습니다. <!-- GS-6906 -->

+++

+++2024.11.07 릴리스 정보

### 수정 사항 및 개선 사항

* 사용자가 **[!UICONTROL 새 이미지 업로드]**&#x200B;를 클릭한 다음 업로드가 완료되기 전에 작업을 취소하면 _저장 진행 중_ 회전기가 더 이상 표시되지 않습니다. <!-- GS-6780 -->

* 이제 경험 재생성 중에 경험 제목이 올바르게 생성됩니다. <!-- GS-7006 -->

* 초안 로드 중 스크롤 막대가 깜박거리는 문제가 해결되었습니다. <!-- GS-5587 -->

* [!DNL Content] _승인된 템플릿 추가_ 팝업의 `View documentation` 링크가 이제 예상대로 작동합니다. <!-- GS-6881 -->

* 크기 조정 작업 중에 프롬프트 서랍에서 이미지를 삭제해도 더 이상 오류가 발생하지 않습니다. <!-- GS-7115 7009 -->

* [!DNL Create] 작업 메뉴(...)에서 **[!UICONTROL 삭제]**&#x200B;을(를) 선택하면 이제 예상대로 작동합니다. <!-- GS-6871 -->

* 이제 사용자는 키보드만으로 모든 메타데이터 템플릿 대화형 요소를 제어할 수 있습니다. <!-- GS-4066 -->

* 디스플레이 광고 템플릿에 템플릿 이미지 필드의 이미지 차원 추출을 추가했습니다. 이제 전체 템플릿이 아닌 실제 이미지 차원에 대해 스마트 자르기 요청이 전송됩니다. <!-- GS-6926 -->

* 생성된 이메일 및 메타 광고에서 `Zoom to fit to screen` 문자열을 지역화했습니다. <!-- GS-5063 -->

* 이제 사용자가 클릭하여 나가면 [!DNL Create] 프롬프트 창이 예상대로 닫힙니다. <!-- GS-5254 -->

* 이제 메타 광고 내보내기에 선택한 콜 투 액션 레이블이 예상대로 포함됩니다. <!-- GS-6504 -->

* 이제 브랜드 점수가 다시 생성된 경험에 대해 예상대로 업데이트되고 유지됩니다. <!-- GS-6535 -->

* 메타 광고 및 디스플레이 광고의 HTML 내보내기에 더 이상 래퍼 `div` 및 `chrome` 요소가 포함되지 않습니다. <!-- GS-7116 -->

* 이제 게시 중 이메일 초안 렌더링 문제가 해결되었습니다. <!-- GS-6394 -->

* 브랜드 점수가 생성되지 않으면 이제 캔버스 **[!UICONTROL 브랜드]** 단추가 비활성화됩니다. <!-- GS-6429 -->

* 이제 캔버스 작업 표시줄의 Facebook/Instagram 토글이 `ReadOnly` 캔버스 설정이 활성화된 경우 예상대로 경험 렌더링을 업데이트합니다. <!-- GS-7039 -->

#### 이미지 재생성

* 이제 여러 메타 광고 변형의 크기 조정이 예상대로 작동합니다. 이전에는 캔버스에 재생성된 변형이 표시되지 않았지만 비어 있었습니다. <!-- GS-7010 -->

* 이제 조각 재생성이 크기 조정된 경험에 대해 예상대로 작동합니다. <!-- GS-6836 -->

* 메타데이터 이미지를 크기 조정한 후 재생성해도 더 이상 오류가 발생하지 않습니다. 이전에는 재생성 전에 이미지 크기를 조정하면 채널 메타데이터가 `meta`에서 `facebook`(으)로 변경되었습니다. <!-- GS-7042 -->

+++

+++2024.10.31 릴리스 정보

### 새로운 기능

* 이제 **[!DNL Content]** 검색 필터가 색상 태그로 검색을 지원합니다. <!-- GS-5501 -->

* 이제 **[!DNL Create]** 캔버스에 전자 메일 조각의 문자 수가 표시됩니다. <!-- GS-5819 -->

### 수정 사항 및 개선 사항

* 누락된 화면 판독기 레이블이 모바일 및 데스크톱 `view` 요소에 추가되었습니다. <!-- GS-5624 4729 -->

* **[!DNL Create]** 캔버스 전자 메일 제목 줄 및 사전 머리글 텍스트 영역의 높이가 이제 동적입니다. <!-- GS-6258 -->

* 이메일 테두리 관련 레이아웃 문제가 해결되었습니다. <!-- GS-6631 -->

* 이제 키보드 포커스가 **[!DNL Content]** **[!UICONTROL 삭제]** 단추에서 예상대로 작동합니다. 이전에는 키보드로 이 단추에 액세스할 수 없었습니다.  <!-- GS-4065 -->

+++

+++2024.10.14 릴리스 정보

이 릴리스에서는 마케팅 캠페인의 계획, 개발 및 분석을 가속화하는 생성 AI 기반 애플리케이션인 Adobe GenStudio for Performance Marketing을 소개합니다. GenStudio for Performance Marketing은 마케팅 팀이 광고, 이메일 및 캠페인에 대한 온브랜드, 다중 채널 콘텐츠를 만들 수 있는 기능을 제공하는 동시에 콘텐츠 성능을 최적화하는 실시간 통찰력을 제공합니다.

### 기능

주요 제품 기능은 다음과 같습니다.

**[!DNL Create]**&#x200B;에서는 콘텐츠 편집기에서 콘텐츠와 변형을 빠르게 생성할 수 있도록 하는 구조화된 프롬프트 환경을 제공하는 캔버스를 소개합니다. 시스템 관리자는 조직의 브랜드 지침에 따라 제품을 교육합니다. [!DNL Create]을(를) 사용하면 모든 AI 생성 콘텐츠가 브랜드 지침(브랜딩, 고객 담당자 및 제품 설명)에 맞게 조정되고 영향력이 큰 브랜드 일관된 마케팅 콘텐츠 프로덕션을 간소화할 수 있습니다.

**[!DNL Content]**&#x200B;은(는) 조정된 브랜드 준수 승인 에셋 및 경험을 저장합니다. GenStudio for Performance Marketing 사용자는 승인된 에셋을 쉽게 찾고, 편집하고, 용도를 변경하고, 공유할 수 있으므로 모든 캠페인에 대해 콘텐츠를 처음부터 다시 만들 필요가 줄어듭니다.

**[!DNL Reviews and Approvals]**&#x200B;은(는) 이해 당사자가 **[!DNL Content]**&#x200B;에 저장하거나 내보내기 전에 생성된 변형을 검토하고 승인하도록 프레임워크를 설정합니다.

**[!DNL Campaigns]**&#x200B;에서 마케팅 캠페인을 구성하고 관리하여 실행 및 추적이 간소화됩니다. 공동 작업자는 캠페인을 시각화, 계획 및 추적하여 여러 이니셔티브를 효과적으로 관리하고 적시에 게재할 수 있습니다.

**[!DNL Insights]**&#x200B;은(는) 콘텐츠 성능에 대한 실시간 평가를 제공하여 마케터가 전략을 최적화하고 데이터 중심의 결정을 내릴 수 있도록 지원합니다.

GenStudio for Performance Marketing은 Adobe Express 및 Adobe AEM Assets을 포함한 다른 Adobe Experience Cloud 제품과 통합됩니다.

+++
