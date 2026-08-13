---
title: LinkedIn 템플릿 지침
description: Adobe GenStudio for Performance Marketing에서 LinkedIn 템플릿을 사용할 때의 모범 사례를 따르십시오.
level: Intermediate
role: Developer, User
feature: Media Templates
exl-id: 85432185-8311-411b-b57b-f482c3d45854
TQID: https://experienceleague.adobe.com/YyG3WuMkdVAaACX03qLKzzw-fFA3WfT9K2ohjnQNPcI
product_v2:
  - id: c4f2e613-b6a1-4be6-b2fc-6021190d498d
feature_v2:
  - id: bffd9bc2-7f41-4bf6-9f08-f14cbd37afd7
  - id: cd5564d5-2a4e-4a5a-8064-57a804f6fd3a
  - id: f71bd2fc-e9ca-4cb6-8088-82e250211e32
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 242ab858144fd152fd55645143f869fddf7b6fe0
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 2%

---

# LinkedIn 템플릿 지침

LinkedIn 템플릿은 LinkedIn 캠페인에 대한 광고 크리에이티브를 만들고 사용자 지정하는 구조화된 방법을 제공합니다. 이 지침은 GenStudio for Performance Marketing의 크리에이티브 프로세스를 간소화하는 동시에 광고가 LinkedIn의 사양을 충족하도록 합니다. 이 안내서는 LinkedIn의 데스크탑 및 모바일 플랫폼 간에 일관된 브랜딩과 효과적인 성능을 준비하는 데 도움이 됩니다.

GenStudio for Performance Marketing에서 작동하도록 LinkedIn 광고 템플릿을 사용자 지정할 때 다음 디자인 모범 사례를 따르십시오.

- 정확히 하나의 이미지 필드가 필요합니다.
- 최대 이미지 크기 5MB
- 최대 헤드라인 70자
- 최대 소개 텍스트 150자
- 섹션을 하나만 사용하여 단일 템플릿 요소 세트를 생성할 수 있습니다

## 인식된 필드 이름

LinkedIn 템플릿을 사용자 지정할 때 다음 필수 필드에 콘텐츠 자리 표시자를 적용합니다.

- `image`(필수, 컨텐츠 JPEG, PNG 또는 GIF에서 선택)
- `on_image_text`(이미지 위에 표시되는 텍스트)

GenStudio for Performance Marketing은 자동으로 다음 필드를 생성합니다. 다음에 대해서는 콘텐츠 자리 표시자를 적용할 필요가 없습니다.

- `headline`
- `introductory_text`
- `cta`(Call to action)

템플릿에서 필드 이름을 사용하는 방법에 대한 자세한 내용은 [콘텐츠 자리 표시자](/help/user-guide/templates/customize-template.md#content-placeholders)를 참조하십시오.

## 지원되는 종횡비

모든 LinkedIn 템플릿 너비는 1200픽셀로 하드코딩됩니다.

| 종횡비 | Platform | 치수(픽셀) | 참고 |
|-------------------|-----------------|------------|-------------------------------------------------------------------------------------|
| 정사각형 1:1 | 데스크탑, 모바일 | 1200 x 1200 | 가장 다재다능합니다. 여러 장치와 배치에서 일관된 모습에 이상적입니다. |
| 가로 1.91:1 | 데스크탑 | 1200 x 628 | 표준 가로 형식. 스폰서 콘텐츠 및 뉴스 피드 광고에 일반적으로 사용됩니다. |
| 세로 1:1.91 | 모바일 | 1200 x 2292 | 세로 긴 형식입니다. 모바일 보기에 최적화되어 더 많은 화면을 제공합니다. |
| 세로 2:3 | 모바일 | 1200 x 1800 | 키가 1:1.91보다 약간 작습니다. 모바일 우선 캠페인에 적합합니다. |
| 세로 4:5 | 모바일 | 1200 x 1500 | 모바일에 권장. 가시성과 콘텐츠의 균형을 맞추므로 종종 더 높은 영향을 미칩니다. |

<!-- 
Potentially add an example

## Template example

+++Example: LinkedIn template

+++

-->
