---
title: Adobe GenStudio for Performance Marketing에서의 브랜드 유효성 검사
description: GenStudio for Performance Marketing에서 기본 제공 브랜드 유효성 검사 시스템이 작동하는 방식을 알아봅니다.
feature: Brand Personalization, Variant Generation, Compliance, Content Generation, Content Review, Generative AI
exl-id: 2e777186-3b7e-46a6-9d37-7c7b7c2aa7ae
source-git-commit: 8f8d10db351f440ccd64f4ef5a54b6ace9f9db85
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# 브랜드 유효성 검사

GenStudio for Performance Marketing에서 브랜드 유효성 검사는 생성 AI 기능 및 지침([[!DNL Brands]](/help/user-guide/guidelines/brands.md), [[!DNL Products]](/help/user-guide/guidelines/products.md) 및 [[!DNL Personas]](/help/user-guide/guidelines/personas.md))과 함께 작동하는 필수 구성 요소입니다. 이렇게 하면 모든 콘텐츠가 브랜드 정체성, ADA 표준 및 개별 채널 플랫폼 지침에 맞게 조정됩니다.

GenStudio for Performance Marketing은 다음을 포함하여 다양한 측면에서 브랜드 유효성 검사 및 기타 콘텐츠 검사를 수행합니다.

* 정의된 또는 기본 [!DNL Brand] 지침
* 플랫폼 지침
<!-- * Ethical considerations related to gender, ethnicity, race, disability status, and age in AI-generated content -->
* 미국 장애인 법(ADA) 표준

## 콘텐츠 확인 요약

캔버스에서 각 변형에 대한 _콘텐츠 확인_ 요약 아이콘을 통해 생성된 각 콘텐츠 항목에 대한 브랜드 유효성 검사 및 기타 콘텐츠 확인 정보 요약에 액세스할 수 있습니다.

_콘텐츠 확인_ 요약에 다음이 표시됩니다.

* 유효성 검사를 통과한 [지침](overview.md)과(와) 테스트한 지침의 수로 계산된 [[!DNL Brand]](brands.md)에 대한 준수 비율
* 플랫폼 지침에 대한 `Pass` 또는 `Fail` 결과(예: Meta 또는 LinkedIn)
* ADA 접근성 표준에 대한 `Pass` 또는 `Fail` 결과

![콘텐츠 확인 요약](/help/assets/content-check-summary.png){width="400" zoomable="yes"}

비율을 클릭하여 변형이 얼마나 준수하는지 확인합니다. 변형 또는 기타 콘텐츠를 편집하면 점수가 자동으로 업데이트됩니다. _문제 보기 및 수정_&#x200B;을 클릭하여 더 준수하도록 할 수 있습니다.

[브랜드 정렬 개선](#improve-brand-alignment)을 참조하세요.

## 컨텐츠 확인 패널

[_콘텐츠 확인_ 요약 아이콘](#content-check-summary)에서 오른쪽 작업 표시줄 _또는_&#x200B;을(를) 클릭하면 캔버스 오른쪽에 _콘텐츠 확인_ 패널이 열립니다. 이 패널에서는 자세한 브랜드 유효성 검사, 플랫폼 지침 및 접근성 표준 정보를 제공하고 개선 기회를 설명합니다.

![콘텐츠 확인 패널](/help/assets/content-check-panel.png){width="400" zoomable="yes"}

_콘텐츠 검사_ 패널에 이미지 및 변형 섹션에 대한 유효성 검사 및 [준수 정보](/help/user-guide/guidelines/overview.md#compliance)가 표시됩니다.

* [!DNL Brand]에 대한 _콘텐츠 검사_ 요약 정보 표시, 플랫폼 지침 및 접근성 표준
* 실패한 지침의 수와 수정이 필요한 각 지침에 대한 자세한 정보를 표시하는 _검토 필요_ 섹션
* _통과_ 섹션에 전달된 지침의 수와 각 통과 지침에 대한 자세한 정보가 표시됩니다.

_콘텐츠 확인_ 패널 점수를 개선하는 방법을 알아보려면 [브랜드 정렬 개선](#improve-brand-alignment)을 참조하세요.

### 컨텐츠 유형

_콘텐츠 검사_ 패널에서 수행할 지침 및 접근성 표준 검사를 전환할 수 있습니다. 패널 상단의 _콘텐츠 형식_ 아이콘(수준 아이콘)을 클릭하여 켜거나 끕니다.

* **[!DNL Brand]** - [!DNL Brand] 지침과 관련된 검사를 수행합니다.
* **플랫폼 지침**—메타와 같은 채널별 플랫폼과 관련된 검사를 수행합니다.
* **접근성**—ADA 접근성 표준과 관련된 검사를 수행합니다.

**수행할 검사에 대해 콘텐츠 형식을 설정**&#x200B;하려면 사용 가능한 형식을 해제하거나 켜려면 클릭하고 **적용**&#x200B;을 클릭합니다.

## 브랜드 정렬 개선

생성된 콘텐츠의 효과를 극대화하고 일관된 브랜드 ID를 유지하려면 [_콘텐츠 확인_ 요약](#content-check-summary) 및 [_콘텐츠 확인_ 패널](#content-check-panel)을 사용하십시오. [[!DNL Brand] 지침](brands.md), 플랫폼 지침 검사 및 접근성 표준 검사에 맞게 특정 섹션을 수동으로 수정할 수 있습니다.

**생성된 변형에 대한 브랜드 정렬을 개선하려면**:

1. 유효성 검사 및 접근성 정보를 보려면 오른쪽 작업 표시줄의 _콘텐츠 확인_ 패널 아이콘을 클릭하십시오.

   개선이 필요한 항목을 확인하기 위해 _검토 필요_ 및 _합격_ 검사에 대한 요약을 볼 수 있습니다.

   >[!NOTE]
   >
   > _콘텐츠 확인_ 패널에 언급된 _브랜드 음성_ 지침은 개별 섹션이 아닌 전체 변형에 적용됩니다. 전체 콘텐츠 변형은 제안된 개선 사항을 위해 강조 표시됩니다.

1. 현재 준수하지 않는 지침을 수정하려면 클릭하십시오.
1. _제목_, _색상_, _브랜드 음성_ 등의 사용 가능한 섹션에서 검토해야 하는 각 검사를 확장하고 검사하려면 클릭하십시오.

   각 검사에 대해 제공된 추론을 사용하여 이미지와 변형을 수정할 수 있습니다.

1. 필요한 수정 사항을 적용한 후 **[!UICONTROL 점수 다시 확인]**&#x200B;을 클릭하여 변경 사항을 다시 확인하고 확인하여 브랜드 ID, 플랫폼 지침 및 접근성 표준에 더 잘 부합하는지 확인하십시오.

   콘텐츠 확인 프로세스가 다시 실행됩니다. 수정된 항목이 유효성 검사를 통과하면 캔버스 하단에 녹색 배너가 표시되어 점수가 업데이트되었는지 확인합니다. 재확인 후 변경 사항이 없으면 배너에서 점수에 대한 변경 사항이 없음을 확인합니다. 수정된 변형에 대한 _콘텐츠 확인_ 요약 아이콘의 백분율에도 진행 상황이 표시됩니다.

1. 섹션을 계속 수정하여 전체 변형이 유효성 검사 및 접근성 검사를 통과하도록 합니다. 캔버스에서 개별 변형 옆에 있는 화살표를 사용하여 각 변형을 탐색합니다.
