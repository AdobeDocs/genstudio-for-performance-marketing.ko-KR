---
title: LinkedIn 템플릿 지침
description: Adobe GenStudio for Performance Marketing에서 LinkedIn 템플릿을 사용할 때의 모범 사례를 따르십시오.
level: Intermediate
role: Developer, User
feature: Media Templates
source-git-commit: 35a519a8d28e260bfa6d9ed671bd5bf1cfeda931
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

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

템플릿에서 필드 이름을 사용하는 방법에 대한 자세한 내용은 [콘텐츠 자리 표시자](/help/user-guide/content/customize-template.md#content-placeholders)를 참조하십시오.

## 지원되는 종횡비

| 종횡비 | Platform | 최소 크기(픽셀) | 최대 크기(px) | 메모 |
|-------------------|-----------------|---------------|----------------|-------------------------------------------------------------------------------------|
| 정사각형 1:1 | 데스크탑, 모바일 | 360 x 360 | 4320 x 4320 | 가장 다재다능합니다. 여러 장치와 배치에서 일관된 모습에 이상적입니다. |
| 가로 1.91:1 | 데스크탑 | 640 x 360 | 7680 x 4320 | 표준 가로 형식. 스폰서 콘텐츠 및 뉴스 피드 광고에 일반적으로 사용됩니다. |
| 세로 1:1.91 | 모바일 | 360 x 640 | 2430 x 4320 | 세로 긴 형식입니다. 모바일 보기에 최적화되어 더 많은 화면을 제공합니다. |
| 세로 2:3 | 모바일 | 360 x 640 | 2430 x 4320 | 키가 1:1.91보다 약간 작습니다. 모바일 우선 캠페인에 적합합니다. |
| 세로 4:5 | 모바일 | 360 x 640 | 2430 x 4320 | 모바일에 권장. 가시성과 콘텐츠의 균형을 맞추므로 종종 더 높은 영향을 미칩니다. |

<!-- Potentially add an example

## Template example

+++Example: LinkedIn template

+++

-->
