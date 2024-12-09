---
title: 템플릿 사용자 정의
description: Adobe GenStudio for Performance Marketing용 템플릿을 개인화하고 최적화하는 방법을 알아봅니다.
level: Intermediate
feature: Templates, Content
exl-id: 292c1689-1b12-405d-951e-14ee6aebc75a
source-git-commit: f95848546abc2decbb5ac52491307977820ce503
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 템플릿 사용자 정의

생성 AI가 콘텐츠를 삽입하는 데 사용하는 콘텐츠 자리 표시자 또는 필드를 삽입하여 GenStudio for Performance Marketing에서 사용할 템플릿을 사용자 지정할 수 있습니다.

다음 몇 섹션에서는 _Handlebars_ 템플릿 언어를 사용하여 GenStudio for Performance Marketing에 대한 HTML 템플릿을 조정하는 방법을 설명합니다. [!DNL Handlebars] 구문은 중괄호가 있는 일반 텍스트를 콘텐츠 자리 표시자로 사용합니다. [내용 [!DNL Handlebars]을(를) 참조하십시오._Handlebars 언어 안내서_&#x200B;의 ](https://handlebarsjs.com/guide/#what-is-handlebars)에서 서식 파일을 준비하는 방법을 알아봅니다.


템플릿이 준비되면 [GenStudio for Performance Marketing에 업로드](use-templates.md#upload-a-template)하고 사용자 지정 템플릿을 기반으로 개인화된 이메일을 생성할 수 있습니다.

>[!TIP]
>
>더 많은 대상자에게 도달하고 최적의 경험을 제공할 수 있도록 [접근성 지침](accessibility-for-templates.md) 및 [모범 사례](/help/user-guide/content/best-practices-for-templates.md)를 따르십시오.

## 콘텐츠 자리 표시자

GenStudio for Performance Marketing은 템플릿 내의 특정 [요소](use-templates.md#template-elements)를 인식하지만, 인식된 필드 이름으로 식별하는 경우에만 인식합니다.

템플릿의 헤드 또는 본문 내에서 [!DNL Handlebars] 구문을 GenStudio for Performance Marketing에서 실제 콘텐츠로 템플릿을 채우도록 하는 콘텐츠 자리 표시자로 사용할 수 있습니다. GenStudio for Performance Marketing은 [인식된 _필드_ 이름](#recognized-field-names)을(를) 기반으로 콘텐츠 자리 표시자를 인식하고 해석합니다.

예를 들어 [!DNL Handlebars] 구문과 함께 `{{ headline }}`을(를) 사용하여 전자 메일의 제목을 배치할 위치를 나타낼 수 있습니다.

```handlebars
<div>{{headline}}</div>
```

### 인식된 필드 이름

다음 표에는 템플릿으로의 채우기에 대해 GenStudio for Performance Marketing에서 인식하는 필드 이름이 나열되어 있습니다. [!DNL Handlebars] 구문을 사용하여 이 필드 이름을 템플릿에 추가하십시오. 여기서 콘텐츠를 생성하는 GenStudio for Performance Marketing이 필요합니다.

| 필드 | 역할 | 채널 템플릿 |
| ------------------ | ---------------------- | -------------------------------- |
| `{{pre_header}}` | 사전 머리글 | 이메일 |
| `{{headline}}` | 제목 | 이메일 <br>메타 광고 <br>디스플레이 광고 |
| `{{body}}` | 본문 복사 | 이메일 <br>메타 광고 <br>디스플레이 광고 |
| `{{cta}}` | 클릭 유도 문안 | 이메일 <br>메타 광고 <br>디스플레이 광고 |
| `{{on_image_text}}` | 이미지 텍스트에서 | 메타 광고 |
| `{{image}}` | 이미지 - 콘텐츠에서 선택 | 이메일 <br>메타 광고 <br>디스플레이 광고 |
| `{{brand_logo}}` | 선택한 브랜드의 로고<br>권장 사용 방법은 [브랜드 로고 필드 이름](#brand-logo-field-name)을 참조하세요. | 이메일<br>메타데이터 |

GenStudio for Performance Marketing은 다음 템플릿에서 특정 필드를 자동으로 채웁니다.

- **전자 메일 템플릿**&#x200B;에서는 `subject` 필드를 식별할 필요가 없습니다.
- **메타 광고 템플릿**&#x200B;에서는 `headline`, `body` 및 `CTA` 필드를 식별할 필요가 없습니다.
- **디스플레이 광고 템플릿**&#x200B;에서는 `CTA` 필드를 식별할 필요가 없습니다.

>[!WARNING]
>
>instagram 광고의 경우 생성된 헤드라인은 최종 경험에 표시되지 않습니다.

GenStudio for Performance Marketing에 템플릿을 업로드할 때에는 20개의 필드 제한이 있습니다. `subject` 필드는 전자 메일에서 자동으로 생성되므로 하나의 필드로 계산됩니다. 즉, 이메일 템플릿에는 19개의 필드가 허용됩니다.

>[!TIP]
>
>GenStudio for Performance Marketing에서 [템플릿 미리 보기](#template-preview)를 사용하여 템플릿을 확인할 수 있습니다.

#### 브랜드 로고 필드 이름

지금은 템플릿 업로드에 대해 브랜드 로고를 선택할 수 없습니다. 다음 예에서는 브랜드 로고를 조건부로 렌더링하는 두 가지 방법을 보여 줍니다. 각 방법은 소스를 확인하고 브랜드 로고를 사용할 수 없는 경우 기본 또는 대체 이미지를 제공하며 스타일을 적용합니다.

**예 1**: HTML `img src` 특성에서 직접 [!DNL Handlebars] 기본 제공 도우미 조건 사용:

```html
<img src="{{#if brand_logo}}{{brand_logo}}{{else}}<default-image>{{/if}}" alt="img alt text" style="max-width: 88px; margin: 10px auto; display: block;">
```

**예 2**: [!DNL Handlebars] 기본 제공 조건 문을 사용하여 HTML `img` 태그를 래핑합니다.

```handlebars
{{#if brand_logo}}
    <img src="{{brand_logo}}" alt="img alt text" style="width: 120px; height: 45px; margin: 10px auto; display: block;">
    {{else}}
    <img src="data:image/png;base64,iVBORw0KGgo..." alt="img alt text" style="width: 120px; height: 45px; margin: 10px auto; display: block;">
{{/if}}
```

#### 수동 필드 이름

다른 모든 필드 이름은 수동으로 채워진 필드로 처리됩니다.

편집 가능한 섹션을 만들려면 섹션 이름 주위에 이중 대괄호를 추가합니다.

```handlebars
{{customVariable}}
```

### 섹션 또는 그룹

_섹션_&#x200B;은(는) 이 섹션의 필드에 높은 수준의 일관성이 필요하다는 것을 GenStudio for Performance Marketing에 알립니다. 이러한 관계를 구축하면 AI가 섹션의 크리에이티브 요소와 일치하는 콘텐츠를 생성할 수 있습니다.

필드 이름에 선택한 접두사를 사용하여 필드가 섹션 또는 그룹의 일부임을 나타냅니다. 밑줄(`_`) 뒤에 필드 이름(`headline`, `body`, `image` 또는 `cta`)을 사용하십시오. 예를 들어 다음 헤드라인 및 본문은 `pod1` 섹션에 속합니다.

- `pod1_headline`
- `pod1_body`

각 섹션은 각 필드 유형 중 하나만 사용할 수 있습니다. 위의 예에서 `pod1` 섹션은 하나의 `pod1_headline` 필드만 사용할 수 있습니다. 이 규칙 때문에 섹션을 중첩할 수 없습니다.

이메일 템플릿에는 최대 3개의 섹션이 포함될 수 있습니다. 예를 들어 다음 목록에는 세 개의 헤드라인 및 본문 섹션이 있습니다.

- `pre-header`
- `pod1_headline`
- `pod1_body`
- `pod2_headline`
- `pod2_body`
- `pod3_headline`
- `pod3_body`
- `cta`

GenStudio for Performance Marketing은 `pod1_headline`이(가) `pod2_body`보다 `pod1_body`과(와) 더 밀접하게 관련되어 있음을 이해합니다.

전자 메일의 각 섹션에 대해 다양한 콘텐츠를 생성하는 프롬프트를 만드는 방법을 알아보려면 [구조화된 프롬프트](/help/user-guide/effective-prompts.md#structured-prompts)를 참조하십시오.

## 템플릿 미리 보기

[템플릿을 업로드](use-templates.md#upload-a-template)하면 GenStudio for Performance Marketing에서 HTML 파일에서 인식된 필드가 검색됩니다. 미리 보기를 사용하여 [템플릿 요소](use-templates.md#template-elements)를 검토하고 [인식된 필드 이름](#recognized-field-names)으로 해당 요소를 올바르게 식별했는지 확인하십시오.

이메일 템플릿에 대한 미리 보기 예:

![미리 보기 필드가 검색됨](/help/assets/template-detected-fields.png){width="650"}

### 컨트롤 미리 보기

기본 제공 도우미(특정 작업을 수행하는 [!DNL Handlebars] 템플릿 언어의 특수 표현식)를 사용하여 특수 콘텐츠의 가시성을 제어할 수 있습니다. 예를 들어 미리 보기 링크를 깔끔하게 유지하면서 내보낸 템플릿의 링크에 추적 매개 변수를 추가하는 조건문을 추가할 수 있습니다.

템플릿을 렌더링할 때는 `_genStudio.browser` 값이 설정되고, 템플릿을 내보낼 때는 `genStudio.export` 값이 설정됩니다. 조건부 래퍼를 사용하여 이메일 상단에 특정 콘텐츠를 포함하도록 결정할 수 있습니다. 예를 들어 템플릿을 내보내기에 사용하는 경우 다음과 같습니다.

```handlebars
{{#if _genStudio.export}}
<%@ include view='emailParent' %>
{{/if}}
```

또 다른 예는 GenStudio for Performance Marketing에서 템플릿을 미리 볼 때 추적 코드를 사용하지 못하도록 하는 것일 수 있다. 다음 예제는 미리 보기 링크를 깔끔하게 유지하면서 내보낸 템플릿의 링크에 추적 매개 변수를 추가하는 방법을 보여 줍니다.

```handlebars
<a class="button" {{#if _genStudio.browser }}
   href="{{ link }}"{{/if}}{{#if _genStudio.export }}
   href="{{ link }}?trackingid=<%=getTrackingId()%>&mv=email"{{/if}}
   target="_blank">{{ cta }}</a>
```

## 정적 콘텐츠

이메일 및 메타 템플릿은 종종 GenStudio for Performance Marketing 외부에서 호스팅되는 이미지 및 CSS 파일에 연결됩니다. GenStudio for Performance Marketing은 이러한 템플릿 또는 템플릿에서 파생된 경험에 대한 썸네일을 생성할 때 올바른 CORS(원본 간 리소스 공유) 헤더가 없으면 이러한 외부 리소스를 무시할 수 있습니다.

썸네일 생성 프로세스 중에 이러한 리소스를 사용할 수 있도록 하려면 다음 두 가지 옵션을 고려하십시오.

1. **CORS 헤더 사용**: 호스트 서버는 프로덕션 환경에 대해 `Access-Control-Allow-Origin` 헤더가 `https://experience.adobe.com` 값으로 설정된 응답을 보내야 합니다. 이 방법을 사용하면 GenStudio for Performance Marketing에서 리소스에 액세스하고 리소스를 포함할 수 있습니다.

1. **데이터 URL 사용**: 데이터 URL을 사용하여 외부 리소스를 템플릿에 직접 포함합니다. 이 메서드는 CORS 제한을 무시하고 썸네일 생성 중에 리소스를 사용할 수 있도록 합니다.

## 템플릿 예

+++예: 한 개의 섹션이 있는 이메일 템플릿

다음은 하나의 섹션을 포함하는 이메일에 대한 HTML 템플릿의 기본 예입니다. 헤드에는 스타일링을 위한 간단한 인라인 CSS가 포함되어 있습니다. 본문에는 전자 메일 생성 프로세스 중에 GenStudio for Performance Marketing에서 콘텐츠를 삽입하는 데 사용할 `pre-header`, `headline` 및 `image` [자리 표시자](#content-placeholders)가 포함되어 있습니다.

```handlebars {line-numbers="true" highlight="13"}
<!DOCTYPE html>
<html>
<head>
    <title>Adobe</title>
    <style>
        .container {
            width: 100%;
            padding: 20px;
            font-family: Arial, sans-serif;
        }
    </style>
</head>
<body>{{ pre_header }}
    <div class="container">
        <h1>{{ headline }}</h1>
        <p><img alt="{{ headline }}"
                src="{{ image }}"
                width="600" height="600"
                border="0"/></p>
        <p>{{ body }}</p>
    </div>
</body>
</html>
```

+++

+++예: 여러 섹션이 있는 이메일 템플릿

다음은 위의 예제와 동일한 HTML 템플릿이지만 두 개의 섹션이 더 있습니다. 헤드에는 그룹을 스타일링할 인라인 CSS가 포함되어 있습니다. 본문에서는 접두사를 사용하여 [콘텐츠 자리 표시자](#content-placeholders)가 있는 두 개의 그룹을 사용합니다.

```handlebars {line-numbers="true" highlight="33"}
<!DOCTYPE html>
<html>
<head>
    <title>Adobe</title>
    <style>
        .container {
            width: 100%;
            padding: 20px;
            font-family: Arial, sans-serif;
        }
        .pod {
            background-color: #f8f8f8;
            margin: 10px;
            padding: 20px;
            border-radius: 5px;
        }
        .pod h2 {
            color: #333;
        }
        .pod p {
            color: #666;
        }
    </style>
</head>
<body>{{ pre_header }}
    <div class="container">
        <h1>{{ headline }}</h1>
        <p><img alt="{{ headline }}"
                src="{{ image }}"
                width="600" height="600"
                border="0"/></p>
        <p>{{ body }}</p>
    <!-- Pod1 -->
        <div class="pod">
            <h2>{{ pod1_header }}</h2>
            <p>{{ pod1_body }}</p>
        </div>
        <!-- End of Pod1 -->
    <!-- Pod2 -->
        <div class="pod">
            <h2>{{ pod2_header }}</h2>
            <p>{{ pod2_body }}</p>
        </div>
        <!-- End of Pod2 -->
    </div>
</body>
</html>
```

+++

+++예: 메타 광고 템플릿

다음은 메타 광고 템플릿의 기본 예입니다. 헤드에는 스타일링을 위한 인라인 CSS가 포함되어 있습니다. 본문에서는 접두사를 사용하여 [콘텐츠 자리 표시자](#content-placeholders)를 사용합니다.

```handlebars {line-numbers="true" highlight="33"}
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adobe</title>
    <style>
        .ad-container {
            width: 300px;
            border: 1px solid #ddd;
            padding: 16px;
            font-family: Arial, sans-serif;
        }
        .ad-image {
            width: 100%;
            height: auto;
        }
        .ad-headline {
            font-size: 18px;
            font-weight: bold;
            margin: 12px 0;
        }
        .ad-body {
            font-size: 14px;
            margin: 12px 0;
        }
        .ad-cta {
            display: inline-block;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            text-decoration: none;
            border-radius: 4px;
            text-align: center;
        }
    </style>
</head>
<body>
<div class="ad-container">
    <img src="{{ image }}" alt="Ad Image" class="ad-image">
    <div class="ad-headline">"{{ headline }}"</div>
    <div class="ad-body">"{{ body }}"</div>
    <a href="(https://example.com)" class="ad-cta">"{{ CTA }}"</a>
</div>
</body>
</html>
```

+++
