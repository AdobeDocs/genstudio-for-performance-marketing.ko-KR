---
title: 메타 광고 템플릿 지침
description: Adobe GenStudio for Performance Marketing에서 메타 광고 템플릿을 사용할 때의 모범 사례를 따르십시오.
level: Intermediate
role: Developer, User
feature: Media Templates
exl-id: e69039b0-272d-4f39-b0e4-916be710fd5f
source-git-commit: d9d774f727b69b18af6114965fdb8ffb450f797b
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 1%

---

# 메타 광고 템플릿 지침

메타 광고 템플릿을 사용하면 메타 플랫폼 간에 시각적으로 일관되고 효과적인 광고를 만들 수 있습니다. 권장되는 디자인 사례를 따르고 지원되는 필드를 사용하면 템플릿이 GenStudio for Performance Marketing에 최적화되어 있는지 확인할 수 있습니다. 이 안내서에서는 원활한 통합 및 영향력이 큰 결과를 위해 메타 광고 템플릿을 구성하고, 사용자 정의하고, 준비하는 방법을 설명합니다.

GenStudio for Performance Marketing에서 작동하도록 메타 광고 템플릿을 사용자 정의할 때 다음 디자인 모범 사례를 따르십시오.

- 열 레이아웃에 360픽셀 너비 사용
- 이미지에 최소 1080 x 1080 픽셀 해상도 사용
- 정확히 하나의 이미지 필드가 필요합니다.
- **not**(이)가 상대 글꼴 크기를 사용하지 않음
- 뷰포트를 **정의 안 함**
- JavaScript을 사용하지 **않음**
- CSS에서 HTML 요소를 재정의하지 **마십시오**
- `background-image` 대신 `<img>` 태그 사용
- 배경 이미지에 대한 텍스트 가독성을 향상시키려면 마스킹을 사용하십시오
- 섹션을 하나만 사용하여 단일 템플릿 요소 세트를 생성할 수 있습니다

## 인식된 필드 이름

메타 광고 템플릿을 사용자 정의할 때 다음 필수 필드에 콘텐츠 자리 표시자를 적용합니다.

- `image`(필수, 컨텐츠 JPEG, PNG 또는 GIF에서 선택)
- `on_image_text`(이미지 위에 표시되는 텍스트)

GenStudio for Performance Marketing은 자동으로 다음 필드를 생성합니다. 다음에 대해서는 콘텐츠 자리 표시자를 적용할 필요가 없습니다.

- `headline`
- `body`
- `cta`

템플릿에서 필드 이름을 사용하는 방법에 대한 자세한 내용은 [콘텐츠 자리 표시자](/help/user-guide/content/customize-template.md#content-placeholders)를 참조하십시오.

## 지원되는 종횡비

| 종횡비 | 치수(픽셀) | 메모 |
|------------------|----------------------------|-----------------------------------------------------------------------|
| 정사각형 1:1 | 1080 x 1080 | 대부분의 메타 배치에 대한 표준, 광범위한 호환성에 권장됩니다. |
| 세로 4:5 | 1080 x 1350 | 모바일 피드에 최적화되었습니다. 더 많은 수직 공간을 제공합니다. |
| 스토리 9:16 | 1080 x 1920 | 스토리 및 릴에 이상적입니다. 전체 모바일 화면을 채웁니다. |
| 가로 1.91:1 | 1080 x 566 | 링크 광고 및 뉴스 피드 배치, 넓은 형식에 가장 적합합니다. |
| 사용자 정의 | 최소 50 x 50(폭) | 필요한 경우에만 사용하십시오. 자르거나 비율을 조정할 수 있습니다. |

광고가 이러한 종횡비 중 하나로 디자인되지 않은 경우, GenStudio for Performance Marketing은 이미지를 적절한 크기로 자동으로 자릅니다.

## 템플릿 예제

+++예: 메타 광고 템플릿

<!-- Does this need to be a precise size? -->

다음은 메타 광고 템플릿의 기본 예입니다. 헤드에는 스타일링을 위한 인라인 CSS가 포함되어 있습니다. 본문에서는 `image` 및 `on_image_text`과(와) 같은 [콘텐츠 자리 표시자](#content-placeholders)를 사용하여 GenStudio for Performance Marketing에서 콘텐츠를 생성할 수 있는 위치를 나타냅니다.

```html {line-numbers="true" highlight="33"}
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Adobe</title>
        <style>
            .ad-container {
            font-family: Helvetica, sans-serif;
            position: relative;
            text-align: center;
            height: 100%;
            }
            .ad-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            }
            .ad-text {
            position: absolute;
            top: 0;
            left: 0;
            margin: 1em;
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            padding: 1em;
            font-size: 75px;
            }
        </style>
    </head>
    <body>
        <div class="ad-container">
            <img src="{{image}}" alt="Ad Image" class="ad-image" />
            <div class="ad-text">{{on_image_text}}</div>
        </div>
    </body>
</html>
```

+++
