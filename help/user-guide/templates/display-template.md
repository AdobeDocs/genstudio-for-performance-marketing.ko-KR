---
title: 광고 템플릿 지침 표시
description: Adobe GenStudio for Performance Marketing에서 디스플레이 광고 및 배너 템플릿을 사용할 때의 모범 사례를 따르십시오.
level: Intermediate
role: Developer, User
feature: Media Templates
exl-id: 076239b3-9444-48f9-bdd6-ef2b757bdf0d
source-git-commit: 4760da26d20e91489a74bb238e07f0d3b426c0a1
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---

# 광고 템플릿 지침 표시

디스플레이 템플릿은 시각적으로 매력적인 배너 및 디스플레이 광고를 만드는 데 사용되는 미리 디자인된 레이아웃입니다. 이미지, 텍스트 및 call to action을 통합할 수 있는 유연한 프레임워크를 제공하여 여러 광고 변형을 만들 때 일관성과 효율성을 보장합니다. GenStudio for Performance Marketing에서 사용할 템플릿을 준비할 때는 모든 에셋이 웹 표시에 최적화되고 필요한 파일 형식 및 크기를 충족하는지 확인하십시오.

GenStudio for Performance Marketing에서 작동하도록 배너 및 표시 광고 템플릿을 사용자 지정할 때 다음 디자인 모범 사례를 따르십시오.

- Adobe 또는 Google 글꼴 사용
- 슬림한 차원으로 잘 표시되는 에셋 준비
- 정확히 하나의 이미지 필드가 필요합니다.
- **not**(이)가 포함된 배경 이미지 또는 인코딩된 배경 이미지를 사용하지 않음
- GenStudio for Performance Marketing 콘텐츠 저장소에 업로드된 배경 이미지(`image` 필드) 사용
- JavaScript을 사용하지 **않음**
- 섹션을 하나만 사용하여 단일 템플릿 요소 세트를 생성할 수 있습니다

## 인식된 필드 이름

배너 또는 디스플레이 광고 템플릿을 사용자 지정할 때 다음 필수 필드에 콘텐츠 자리 표시자를 사용하십시오.

- `headline`
- `sub_headline`
- `body`
- `image`(필수, 컨텐츠 JPEG, PNG 또는 GIF에서 선택)

GenStudio for Performance Marketing은 자동으로 다음 필드를 생성합니다. 다음에 대해서는 콘텐츠 자리 표시자를 적용할 필요가 없습니다.

- `cta`

템플릿에서 필드 이름을 사용하는 방법에 대한 자세한 내용은 [콘텐츠 자리 표시자](/help/user-guide/content/customize-template.md#content-placeholders)를 참조하십시오.

## 지원되는 차원

너비 x 높이(픽셀)를 설정해야 합니다.

| 방향 | 치수(픽셀) | 메모 |
|--------------|-------------------------------------------------------------|------------------------------------------------------------------|
| 세로 | 300 x 600<br>160 x 600 | 초고층 건물 및 반 페이지 배너에 대 한 일반적인 |
| 가로 | 300 x 250<br>728 x 90<br>336 x 280<br>320 x 50<br>970 x 250 | 표준 순위표, 중간 사각형 및 배너 크기 |
| 사용자 정의 | 50 x 50 ~ 2000 x 2000 | 비표준 또는 고유 배치에 사용, 플랫폼 제한 확인 |

<!-- Potentially add an example

## Template example

+++Example: Display ad template

+++

-->
