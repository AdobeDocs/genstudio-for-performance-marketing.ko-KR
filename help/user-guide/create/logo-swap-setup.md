---
title: 템플릿에서 로고 교체 설정
description: ' [!DNL GenStudio for Performance Marketing]에서 로고 교환을 사용하도록 템플릿에서 브랜드 로고 자리 표시자를 구성합니다.'
feature: Create Canvas
role: User
level: Intermediate
source-git-commit: 98cb7ba338878495e6d7b68f3b8c620abae10127
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 2%

---

# 템플릿에서 로고 교체 설정

이 안내서에서는 [!DNL GenStudio for Performance Marketing]에서 [로고 교체 기능](/help/user-guide/create/logo-swap.md)을 사용하도록 설정하기 위해 템플릿에서 브랜드 로고 자리 표시자를 구성하는 방법을 설명합니다. 자리 표시자가 다양한 이미지 크기와 종횡비에 올바르게 표시되도록 하려면 이 지침을 따르십시오.

## 빠른 설정

로고 이미지에 다음 기본 템플릿 코드를 사용하십시오.

```html
<img
  src="{{brand_logo}}"
  style="{{defaultLogo}}"
  class="my-logo"
>
```

필수 여부:

- `src="{{brand_logo}}"` - 로고 교체 기능을 사용합니다.
- `style="{{defaultLogo}}"` - 자리 표시자 테두리 스타일을 적용합니다.

선택 사항:

- `class="my-logo"`—크기 조정 및 스타일을 위한 사용자 지정 CSS 클래스입니다.

## 자리 표시자 테두리 이해

로고가 선택되지 않은 경우 `{{brand_logo}}`에 투명한 1×1 픽셀 이미지가 포함됩니다. `{{defaultLogo}}` 스타일은 자리 표시자가 표시되도록 윤곽선을 자동으로 적용합니다.

```css
outline: clamp(1px, 0.1em, 5px) dashed #FFF;
```

테두리 동작:

- 기본 자리 표시자가 표시되면 나타납니다.
- 로고가 교체되면 자동으로 사라집니다.
- 상위 글꼴 크기를 기준으로 배율을 조정합니다.

### 테두리 크기 조정

`clamp()` 함수는 윤곽선 두께를 템플릿 크기에 맞게 조정합니다.

| 상위 글꼴 크기 | 윤곽선 크기 |
| --- | --- |
| 10px | 1px(분) |
| 16px | 1.6px |
| 24px | 2.4px |
| 32px | 3.2px |
| 50px+ | 5px(최대) |

수식: `0.1em`은(는) 상속된 글꼴 크기의 10%와 같으며 `1px`과(와) `5px` 사이에 고정되어 있습니다.

## 자리 표시자 테두리 사용자 지정

CSS 클래스를 사용하여 기본 윤곽선을 재정의할 수 있습니다. `{{defaultLogo}}` 스타일은 기본 윤곽선을 적용하며 클래스에서는 색, 너비 및 스타일을 사용자 지정할 수 있습니다.

템플릿 HTML:

```html
<img
  src="{{brand_logo}}"
  style="{{defaultLogo}}"
  class="logo-custom-border"
>
```

템플릿 CSS:

```css
.logo-custom-border {
  outline-color: #0066CC !important;
  outline-width: 2px !important;
  outline-style: dotted !important;
}
```

>[!NOTE]
>사용자 지정 윤곽선 스타일은 자리 표시자에만 영향을 줍니다. 로고가 교체되면 모든 윤곽선 스타일이 자동으로 제거됩니다.

## 권장 로고 크기 설정

자리 표시자가 표시되고 레이아웃 이동이 발생하지 않도록 하려면 CSS 클래스에서 명시적 크기 조정을 설정하십시오.

템플릿 HTML:

```html
<img
  src="{{brand_logo}}"
  style="{{defaultLogo}}"
  class="logo-standard"
>
```

템플릿 CSS:

```css
.logo-standard {
  width: 120px;
  height: 60px;
}
```

## 로고 위치 제어

`object-fit` 및 `object-position`을(를) 사용하여 컨테이너 내에서 로고의 크기 조절 방법을 제어합니다.

### 로고 가운데 맞춤(가장 일반적)

이 로고는 가로 및 세로 가운데 150×80픽셀 이내에 맞도록 크기가 조절됩니다.

```html
<img
  src="{{brand_logo}}"
  style="{{defaultLogo}}"
  class="logo-centered"
>
```

```css
.logo-centered {
  width: 150px;
  height: 80px;
  object-fit: contain;
  object-position: center center;
}
```

### 왼쪽 로고 정렬

로고 배율은 왼쪽 가장자리에 맞게 조정되며 세로 방향으로 가운데로 맞춰집니다.

```html
<img
  src="{{brand_logo}}"
  style="{{defaultLogo}}"
  class="logo-left"
>
```

```css
.logo-left {
  width: 200px;
  height: 60px;
  object-fit: contain;
  object-position: left center;
}
```

### 오른쪽 상단의 로고

오른쪽 위 모서리에 배치된 로고 배율이 알맞습니다.

```html
<img
  src="{{brand_logo}}"
  style="{{defaultLogo}}"
  class="logo-top-right"
>
```

```css
.logo-top-right {
  width: 100px;
  height: 100px;
  object-fit: contain;
  object-position: right top;
}
```

## 전체 예

### 최소 설정

```html
<img src="{{brand_logo}}" style="{{defaultLogo}}">
```

>[!NOTE]
>이 설정은 작동하지만 투명한 1×1 픽셀 이미지가 원래 크기로 축소되므로 자리 표시자가 거의 보이지 않을 수 있습니다. 표시되는 자리 표시자에 대해 `width` 및 `height`이(가) 있는 CSS 클래스를 사용합니다.

### 권장 설정

```html
<img
  src="{{brand_logo}}"
  style="{{defaultLogo}}"
  class="brand-logo"
>
```

```css
.brand-logo {
  width: 120px;
  height: 60px;
  object-fit: contain;
  object-position: center center;
}
```

### 사용자 지정 테두리를 사용한 고급 설정

```html
<img
  src="{{brand_logo}}"
  style="{{defaultLogo}}"
  class="sponsor-logo"
>
```

```css
.sponsor-logo {
  width: 180px;
  height: 90px;
  object-fit: contain;
  object-position: left center;
  outline-color: #0066CC !important;
  outline-width: 2px !important;
  outline-style: solid !important;
}
```

### 크기 경계가 있는 유연한 설정

반응형 템플릿 또는 다양한 로고 크기에 대해 `min-*` 및 `max-*` 속성을 사용하십시오.

```html
<img
  src="{{brand_logo}}"
  style="{{defaultLogo}}"
  class="logo-flexible"
>
```

```css
.logo-flexible {
  min-width: 20px;
  min-height: 20px;
  max-width: 200px;
  max-height: 100px;
  object-fit: contain;
  object-position: center center;
}
```

작동 방식:

- `min-width` 및 `min-height`은(는) 자리 표시자를 계속 표시합니다.
- `max-width` 및 `max-height`은(는) 크기가 큰 로고가 레이아웃을 손상하지 않도록 합니다.
- 로고는 이러한 경계 내에서 비례적으로 크기가 조절됩니다.

## CSS 속성 참조

| 범주 | 속성 | 값 | 목적 |
| --- | --- | --- | --- |
| 필수(HTML) | `src` | `{{brand_logo}}` | 로고 교체 기능을 활성화합니다. |
| 필수(HTML) | `style` | `{{defaultLogo}}` | 자리 표시자 윤곽선을 적용합니다. |
| 권장(CSS 클래스) | `width` | `120px` | 최대 로고 너비를 설정합니다. |
| 권장(CSS 클래스) | `height` | `60px` | 최대 로고 높이를 설정합니다. |
| 권장(CSS 클래스) | `object-fit` | `contain` | 자르지 않고 로고 크기를 조절합니다. |
| 권장(CSS 클래스) | `object-position` | `center center` | 로고 정렬을 제어합니다. |
| 선택 사항(CSS 클래스) | `outline-color` | `#FF0000` | 윤곽선 색상을 변경합니다. |
| 선택 사항(CSS 클래스) | `outline-width` | `3px` | 윤곽선 두께를 변경합니다. |
| 선택 사항(CSS 클래스) | `outline-style` | `solid` | 윤곽선 스타일을 변경합니다. |
| 유연한 크기 조정(CSS 클래스) | `min-width` | `20px` | 자리 표시자 가시성을 보장합니다. |
| 유연한 크기 조정(CSS 클래스) | `min-height` | `20px` | 자리 표시자 가시성을 보장합니다. |
| 유연한 크기 조정(CSS 클래스) | `max-width` | `200px` | 오버플로를 방지합니다. |
| 유연한 크기 조정(CSS 클래스) | `max-height` | `100px` | 레이아웃 경계를 제어합니다. |

## 모범 사례

수행:

- 항상 `{{brand_logo}}` 및 `{{defaultLogo}}`을(를) 포함합니다.
- 자리 표시자가 표시되도록 `width` 및 `height`을(를) 정의합니다.
- 크기 조정 및 윤곽선 사용자 지정에 CSS 클래스를 사용합니다.
- 로고 종횡비를 유지하려면 `object-fit: contain`을(를) 사용하십시오.
- 크기와 종횡비가 다른 로고로 테스트합니다.

금지:

- `outline` 대신 `border`을(를) 사용합니다. 테두리는 자동으로 숨겨지지 않습니다.
- 크기 조정 속성을 인라인 스타일에 넣습니다.
- 크기 제한 생략(자리 표시자가 1×1픽셀로 렌더링됨).
- `object-fit: cover`을(를) 사용합니다(로고를 자를 수 있음).

## 문제 해결

테두리가 표시되지 않음:

- `style="{{defaultLogo}}"`이(가) 포함되어 있는지 확인하십시오.
- CSS 클래스에 `width` 및 `height`이(가) 정의되어 있는지 확인하십시오.

자리 표시자가 너무 작음(1px):

- CSS 클래스에 명시적 `width` 및 `height`을(를) 추가합니다.

교환 후 테두리가 사라지지 않음:

- `border`이(가) 아닌 CSS 클래스의 윤곽 속성을 사용합니다.

로고가 잘림:

- `cover` 대신 `object-fit: contain`을(를) 사용합니다.

로고가 너무 작거나 너무 큼:

- CSS 클래스에서 `width` 및 `height`을(를) 조정합니다.

사용자 지정 테두리가 표시되지 않음:

- `{{defaultLogo}}`이(가) `style` 특성에 있는지 확인합니다.
- CSS 클래스에 사용자 지정 `outline-*` 속성을 넣으십시오.
