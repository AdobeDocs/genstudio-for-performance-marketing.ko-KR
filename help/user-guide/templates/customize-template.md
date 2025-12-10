---
title: 템플릿 사용자 정의
description: Adobe GenStudio for Performance Marketing 생성 AI에서 인식하는 콘텐츠 자리 표시자를 사용하여 HTML 템플릿을 사용자 지정하는 방법을 알아봅니다.
level: Intermediate
role: Developer
feature: Media Templates, Content Generation, Generative AI
exl-id: 292c1689-1b12-405d-951e-14ee6aebc75a
source-git-commit: 8fb4a0e3acaf1a45d8f0f00f975247fc8fb746e3
workflow-type: tm+mt
source-wordcount: '1612'
ht-degree: 0%

---

# 템플릿 사용자 정의

생성 AI가 콘텐츠를 삽입하는 데 사용하는 콘텐츠 자리 표시자 또는 필드를 삽입하여 GenStudio for Performance Marketing에서 사용할 템플릿을 사용자 지정할 수 있습니다.

다음 몇 섹션에서는 _[!DNL Handlebars]_템플릿 언어를 사용하여 GenStudio for Performance Marketing에 대한 HTML 템플릿을 적용하는 방법에 대해 설명합니다. [!DNL Handlebars] 구문은 중괄호가 있는 일반 텍스트를 콘텐츠 자리 표시자로 사용합니다. 템플릿을 준비하는 방법은 [Handlebars 언어 안내서 [!DNL Handlebars]의 ](https://handlebarsjs.com/guide/#what-is-handlebars)기능__을 참조하세요.

템플릿이 준비되면 [GenStudio for Performance Marketing에 업로드](use-templates.md#upload-a-template)하고 사용자 지정 템플릿을 기반으로 개인화된 이메일을 생성할 수 있습니다.

더 많은 대상자에게 도달하고 최적의 경험을 제공할 수 있도록 [접근성 지침](accessibility-for-templates.md) 및 [모범 사례](/help/user-guide/templates/best-practices-for-templates.md)를 따르십시오.

## 콘텐츠 자리 표시자

>[!TIP]
>
>콘텐츠 자리 표시자가 **not**(이)와 나중에 사용자가 채워야 하는 콘텐츠의 자리 표시자 텍스트가 동일합니다. [템플릿에서 자리 표시자 텍스트 사용](/help/user-guide/templates/best-practices-for-templates.md#using-placeholder-text-in-templates)에 대해 자세히 알아보세요.

GenStudio for Performance Marketing은 템플릿 내의 특정 유형의 콘텐츠 또는 [요소](use-templates.md#template-elements)를 인식하지만, [인식된 필드 이름](#recognized-field-names)으로 식별하는 경우에만 인식합니다.

HTML 템플릿의 헤드 또는 본문 내에서 [!DNL Handlebars] 구문을 사용하여 GenStudio for Performance Marketing에서 템플릿을 실제 콘텐츠로 채워야 하는 콘텐츠 자리 표시자를 삽입할 수 있습니다. GenStudio for Performance Marketing은 [인식된 _필드_ 이름](#recognized-field-names)을(를) 기반으로 이러한 자리 표시자를 인식하고 해석합니다. 각 필드 이름은 콘텐츠가 생성되고 템플릿에 삽입되는 방법을 결정하는 특정 규칙 및 동작과 연결되어 있습니다.

예를 들어 `{{headline}}` 구문과 함께 [!DNL Handlebars]을(를) 사용하여 전자 메일의 제목을 배치할 위치를 나타낼 수 있습니다. GenStudio은 이 필드를 인식하고 지침 및 프롬프트 기준에 따라 관련 헤드라인을 생성한 다음 이 위치에 헤드라인을 삽입합니다.

```handlebars
<div>{{headline}}</div>
```

### 인식된 필드 이름

다음 표에는 템플릿에 자리 표시자를 추가하기 위해 GenStudio for Performance Marketing에서 인식하는 필드 이름이 나열되어 있습니다. 각 필드는 특정 채널 지침, LLM 지침 및 역할 기반 규칙을 따릅니다. 특정 유형의 콘텐츠를 생성하기 위해 GenStudio for Performance Marketing이 필요한 템플릿에 [!DNL Handlebars] 구문을 사용하여 이러한 필드 이름을 추가합니다.

| 필드 | 역할 | 채널 템플릿 |
| ----------------------- | ------------------------- | ------------------------------------------------ |
| `{{pre_header}}` | 사전 머리글 | 이메일 |
| `{{headline}}` | 제목 | 이메일 <br>Meta 광고 <br>배너 및 디스플레이 광고 <br>LinkedIn 광고 |
| `{{sub_headline}}` | 하위 헤드라인 | 이메일<br>배너 및 디스플레이 광고 |
| `{{introductory_text}}` | 소개 텍스트 | LinkedIn 광고 |
| `{{body}}` | 본문 복사 | 이메일 <br>Meta 광고 <br>배너 및 디스플레이 광고 |
| `{{cta}}` | Call to action<br>[콜 투 액션](#calls-to-action) 보기 | 이메일 <br>Meta 광고 <br>배너 및 디스플레이 광고 <br>LinkedIn 광고 |
| `{{image}}` | 이미지—[!DNL Content]에서 선택 | 이메일 <br>Meta 광고 <br>배너 및 디스플레이 광고 <br>LinkedIn 광고 |
| `{{on_image_text}}` | 이미지 텍스트에서<br>[이미지 텍스트에서](#on-image-text)을(를) 참조하십시오. | Meta 광고 <br>LinkedIn 광고 |
| `{{link}}` | 이미지의 call to action<br>이미지의 [링크](#link-on-image)를 참조하십시오. | 이메일 |

<!-- | `{{brand_logo}}`        | Logo of selected brand<br>See [Brand logo field name](#brand-logo-field-name). | email<br>Meta ad <br>LinkedIn ad | -->

GenStudio for Performance Marketing은 다음 템플릿에서 특정 필드를 자동으로 생성합니다.

- **전자 메일 템플릿**&#x200B;에서는 `subject` 필드를 식별할 필요가 없습니다.
- **Meta 광고 템플릿**&#x200B;에서는 `headline`, `body` 및 `CTA` 필드를 식별할 필요가 없습니다.
- **배너 및 디스플레이 광고 템플릿**&#x200B;에서는 `CTA` 필드를 식별할 필요가 없습니다.
- **LinkedIn 광고 템플릿**&#x200B;에서는 `headline`, `introductory_text` 및 `CTA` 필드를 식별할 필요가 없습니다.

>[!WARNING]
>
>Instagram 광고의 경우 생성된 헤드라인이 최종 경험에 표시되지 않습니다.

GenStudio for Performance Marketing에 템플릿을 업로드할 때에는 20개의 필드 제한이 있습니다. `subject` 필드는 전자 메일에서 자동으로 생성되므로 하나의 필드로 계산됩니다. 즉, 이메일 템플릿에는 19개의 필드가 허용됩니다.

>[!TIP]
>
>GenStudio for Performance Marketing에서 [템플릿 미리 보기](#template-preview)를 사용하여 템플릿을 확인할 수 있습니다.

### 콜 투 액션

call to action(CTA)에는 구문 및 링크가 포함되어 있습니다. 변형 생성 프로세스 중에 _[!UICONTROL 구문 변경]_ 및 _[!UICONTROL 링크 추가]_ 기능이 제대로 작동하려면 템플릿에 링크 및 구문에 대한 자리 표시자를 포함해야 합니다.

CTA 자리 표시자를 설정하려면 다음 지침을 따르십시오.

- CTA 구문을 사용하고 링크를 편집할 수 있습니다.

  ```html
  <a class="button" href="{{pod1_link}}" >{{cta}}</a>
  ```

- CTA 구문을 다시 사용할 수 있지만 템플릿에 실제 링크가 제공되므로 링크를 **편집할 수 없음**

  ```html
  <a align="center" href="https://link">{{cta}}</a>
  ```

- CTA 링크를 편집할 수 있지만 구문이 템플릿에 제공되었으므로 **사용할 수 없음**

  ```html
  <a class="button" href="{{pod1_link}}" >Register now</a>
  ```

GenStudio for Performance Marketing은 변형 콜 투 액션 구문도 제공할 수 있습니다. [Call to action 개정](/help/user-guide/create/manage-variants.md#revise-call-to-action)을 참조하세요.

### 이미지에 연결

크리에이티브가 이미지에 링크를 추가하도록 이메일 템플릿을 사용자 정의할 수 있습니다. CTA 링크와 유사하게 다음 지침을 사용하여 이미지 태그에 `link` 자리 표시자를 적용합니다.

```html
<a href="{{link}}"><img src="image-source.jpg" alt="{{imageDescription}}"></a>
```

이 예에서

- `{{link}}`은(는) 실제 URL의 자리 표시자입니다.
- `src="image-source.jpg"`은(는) 실제 이미지 원본 URL로 대체해야 합니다.
- `{{imageDescription}}`은(는) 이미지의 대체 텍스트에 대한 자리 표시자를 제공하는 사용자 정의 필드 이름으로, 접근성 및 SEO에 유용합니다.

### 대체 텍스트

사용자 정의 필드 이름을 자리 표시자로 사용하여 이미지에 대한 대체 텍스트(HTML `alt="text"` 특성) 설명을 생성합니다. 다음 `{{imageDescription}}` 자리 표시자가 동일한 `{{image}}` 태그 내의 `<img>` 필드와 함께 사용되므로 이미지와 설명 간의 관계가 유지됩니다.

```html
<img src="{{image}}" alt="{{imageDescription}}">
```

이 예에서

- `{{image}}`은(는) 이미지 소스 URL의 자리 표시자입니다.
- `{{imageDescription}}`은(는) 접근성 및 SEO 목적을 위해 이미지에 대한 설명을 제공하는 대체 텍스트의 자리 표시자입니다.

### 접근성 레이블

`aria-label` 특성은 표시 레이블이 없는 요소의 액세스 가능한 이름을 정의하는 데 사용됩니다. 이 속성은 CTA 버튼과 같은 대화형 요소에 대한 컨텍스트를 제공하는 것이 중요한 템플릿에서 특히 유용합니다.

```html
<a class="button" href="{{link}}" aria-label="{{CTAAriaLabel}}">{{cta}}</a>
```

### 이미지 텍스트에서

`{{on_image_text}}` 자리 표시자는 경험의 이미지에 직접 배치된 짧은 영향력 있는 메시지의 텍스트 오버레이를 지정하는 데 사용됩니다.

```html
<div class="image-text">{{on_image_text}}</div>
```

<!-- this field does not work in Create canvas 2025/03

### Brand logo field name

At this time, you cannot select the brand logo for the template upload. The following examples demonstrate two methods that conditionally render the brand logo. Each method verifies the source, provides a default or alternative image in case the brand logo is not available, and applies a style:

**Example 1**: Using [!DNL Handlebars] Built-in Helpers condition directly in the HTML `img src` attribute:

```html
<img src="{{#if brand_logo}}{{brand_logo}}{{else}}<default-image>{{/if}}" alt="img alt text" style="max-width: 88px; margin: 10px auto; display: block;">
```

**Example 2**: Using [!DNL Handlebars] Built-in condition statement to wrap the HTML `img` tag:

```html
{{#if brand_logo}}
    <img src="{{brand_logo}}" alt="img alt text" style="width: 120px; height: 45px; margin: 10px auto; display: block;">
    {{else}}
    <img src="data:image/png;base64,iVBORw0KGgo..." alt="img alt text" style="width: 120px; height: 45px; margin: 10px auto; display: block;">
{{/if}}
```

-->

### 수동 필드 이름

다른 모든 필드 이름은 사용자가 정의하고 수동으로 채워진 필드로 처리됩니다. 예를 들어, 바닥글 콘텐츠에 대한 섹션을 예약할 수 있습니다.

편집 가능한 섹션을 만들려면 섹션 이름 주위에 이중 대괄호를 추가합니다.

```html
<tbody>
    <tr>
        <td>
            <p><span class="footer-text">{{footerLegal}}</span></p>
        </td>
    </tr>
</tbody>
```

### 리치 텍스트 편집

서식 있는 텍스트 편집으로 [!DNL Create] 프로세스 동안 크리에이티브 콘텐츠를 향상시킬 수 있습니다. 캔버스는 콘텐츠 자리 표시자의 위치에 따라 서식 있는 텍스트 기능을 결정합니다. 리치 텍스트 기능은 콘텐츠 자리 표시자를 독립 실행형 요소로 사용하거나 블록 수준 HTML 태그(예: `<p>`, `<div>` 또는 `<span>`) 내에서 사용하는 경우에만 사용할 수 있습니다.

단락의 독립 실행형 컨텐츠에 대해 리치 텍스트 편집을 사용할 수 있습니다.

```html
<p>{{body}}</p>
```

HTML 특성(예: `alt`, `href` 또는 `src`) 내에서 콘텐츠 자리 표시자를 사용하는 경우 해당 필드에 대해 서식 있는 텍스트 편집이 지원되지 않습니다.

**콘텐츠에 대해 서식 있는 텍스트 편집을**&#x200B;사용할 수 없음`alt`:

```html
<img src="image.jpg" alt="{{image_description}}">
```

필드가 두 번 이상 표시되면 인스턴스에서 HTML 속성으로 사용되는지 여부에 따라 서식 있는 텍스트 기능이 결정됩니다. 예를 들어 헤드라인을 머리글로 사용하고 이미지의 대체 텍스트로 사용하는 경우 `alt` 태그가 우선합니다.

서식 있는 텍스트 편집은 **콘텐츠로 사용되므로**&#x200B;에서 사용할 수 `headline`없음`alt`입니다.

```html
<h1>{{headline}}</h1>
<img src="image.jpg" alt="{{headline}}">
```

소셜 채널(Meta, LinkedIn)의 `on_image_text`과 같은 특정 채널 내의 특정 필드에 대해 서식 있는 텍스트 편집을 사용할 수 있습니다.

## 섹션 또는 그룹

이메일 템플릿에 여러 오퍼 또는 스토리와 같은 여러 콘텐츠 영역이 필요한 경우 섹션 또는 그룹을 사용하여 구성할 수 있습니다. _섹션_&#x200B;은(는) 이 섹션의 필드에 높은 수준의 일관성이 필요하다는 것을 GenStudio for Performance Marketing에 알립니다. 이러한 관계를 구축하면 AI가 섹션의 크리에이티브 요소와 일치하는 콘텐츠를 생성할 수 있습니다.

선택한 그룹 이름을 접두사로 사용하여 필드가 섹션 또는 그룹의 일부임을 나타냅니다. 밑줄(`headline`) 뒤에 필드 이름(예: `body`, `image`, `cta` 또는 `_`)을 사용하십시오.

구문: `groupname_fieldname`

- _수정_(👍): `pod1_body`
- _잘못됨_(❌): `pod1body`

각 섹션은 각 필드 유형 중 하나만 사용할 수 있습니다.이 규칙 때문에 섹션은 중첩될 수 없습니다.

예를 들어 다음 필드는 `pod1` 섹션에 속합니다.

- `pod1_headline`
- `pod1_body`
- `pod1_image`
- `pod1_cta`

GenStudio for Performance Marketing은 `pod1_headline`이(가) `pod1_body`보다 `pod2_body`과(와) 더 밀접하게 관련되어 있음을 이해합니다.

이메일 또는 Meta 광고와 같은 각 템플릿 유형에는 섹션 사용에 대한 채널별 제한 사항이 있습니다. [템플릿 사용 모범 사례](/help/user-guide/templates/best-practices-for-templates.md) 항목에서 _채널별 지침_&#x200B;을 참조하세요.

>[!TIP]
>
>여러 섹션 전자 메일의 각 섹션에 대해 다양한 콘텐츠를 생성하는 프롬프트를 만드는 방법을 알아보려면 [구조화된 프롬프트](/help/user-guide/effective-prompts.md#structured-prompts)를 참조하십시오.

## 템플릿 미리 보기

[템플릿을 업로드](use-templates.md#upload-a-template)하면 GenStudio for Performance Marketing에서 HTML 파일에서 인식된 필드가 검색됩니다. 미리 보기를 사용하여 [템플릿 요소](use-templates.md#template-elements)를 검토하고 [인식된 필드 이름](#recognized-field-names)으로 해당 요소를 올바르게 식별했는지 확인하십시오.

이메일 템플릿에 대한 미리 보기 예:

![미리 보기 필드가 검색됨](/help/assets/template-detected-fields.png "검색된 필드 확인"){zoomable="yes"}

[템플릿 코드 편집기](/help/user-guide/templates/code-editor.md)를 참조하세요.

### 컨트롤 미리 보기

기본 제공 도우미(특정 작업을 수행하는 [!DNL Handlebars] 템플릿 언어의 특수 표현식)를 사용하여 특수 콘텐츠의 가시성을 제어할 수 있습니다. 예를 들어 미리 보기 링크를 깔끔하게 유지하면서 내보낸 템플릿의 링크에 추적 매개 변수를 추가하는 조건문을 추가할 수 있습니다.

템플릿을 렌더링할 때는 `_genStudio.canvas` 값이 설정되고, 템플릿을 내보낼 때는 `genStudio.export` 값이 설정됩니다. 조건부 래퍼를 사용하여 이메일 상단에 특정 콘텐츠를 포함하도록 결정할 수 있습니다. 예를 들어 템플릿을 내보내기에 사용하는 경우 다음과 같습니다.

```handlebars
{{#if _genStudio.export}}
<%@ include view='emailParent' %>
{{/if}}
```

또 다른 예는 GenStudio for Performance Marketing에서 템플릿을 미리 볼 때 추적 코드를 사용하지 못하도록 하는 것일 수 있다. 다음 예제는 미리 보기 링크를 깔끔하게 유지하면서 내보낸 템플릿의 링크에 추적 매개 변수를 추가하는 방법을 보여 줍니다.

```html
<a class="button" {{#if _genStudio.canvas }}
   href="{{link}}"{{/if}}{{#if _genStudio.export }}
   href="{{link}}?trackingid=<%=getTrackingId()%>&mv=email"{{/if}}
   target="_blank">{{cta}}</a>
```

## 정적 콘텐츠

이메일 및 Meta 템플릿은 종종 다른 도메인에서 호스팅된 이미지 및 CSS 파일에 연결됩니다. GenStudio for Performance Marketing은 템플릿 미리 보기 또는 템플릿에서 파생된 경험에 대한 썸네일을 생성할 때 컨텐츠 소스의 유효성을 확인하고 미리 보기 목적으로 사본을 임베드합니다.

외부 파일은 템플릿 미리 보기를 만들기 위한 목적으로만 임시로 포함되므로 미리 보기가 생성 시 표시되는 내용을 정확하게 반영할 수 있습니다. 이러한 외부 파일은 GenStudio for Performance Marketing에 영구적으로 저장되지 **않습니다**. 템플릿 미리 보기가 만들어지면 GenStudio for Performance Marketing에서 템플릿에 제공된 원본 소스 링크를 계속 참조합니다.

### 콘텐츠 새로 고침

초기 미리 보기를 만든 후 소스가 변경되면 [새로 고침](/help/user-guide/templates/use-templates.md#refresh-template) 함수를 사용하여 외부 소스의 최신 콘텐츠 버전으로 템플릿 미리 보기를 업데이트합니다.
