---
title: 이메일 템플릿 지침
description: Adobe GenStudio for Performance Marketing에서 이메일 템플릿을 사용할 때 모범 사례를 따르십시오.
level: Intermediate
role: Developer, User
feature: Media Templates
exl-id: 8b1e8d32-5a23-45ce-a2d4-ae6de3698c45
source-git-commit: d9d774f727b69b18af6114965fdb8ffb450f797b
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# 이메일 템플릿 지침

마케팅 이메일 템플릿은 시각적으로 매력적인 반응형 이메일 캠페인을 위한 기반 역할을 합니다. 일반적으로 HTML 템플릿을 사용하면 레이아웃, 타이포그래피, 색상 및 이미지를 브랜드 지침에 맞게 제어할 수 있습니다. GenStudio for Performance Marketing에서 사용할 템플릿을 준비할 때는 스타일링에 시맨틱 HTML 및 인라인 CSS를 사용하고 스크립트나 외부 종속성을 사용하지 마십시오. 잘 구성된 HTML 템플릿은 수신자의 경험을 개선하고 전달성 및 참여율을 향상시킬 수 있습니다.

GenStudio for Performance Marketing에서 작동하도록 이메일 템플릿을 사용자 지정할 때 다음 디자인 모범 사례를 따르십시오.

- Adobe 또는 Google 글꼴 사용
- 깔끔하고 반응형 HTML 및 인라인 CSS 사용
- JavaScript을 사용하지 **않음**
- **not** 본문이나 컨테이너에서 고정 너비를 사용하지 않음
- 템플릿 크기를 크게 늘릴 수 있으므로 **not**&#x200B;에서 base64 인코딩을 사용하여 이미지를 만드십시오
- 최대 HTML 파일 크기는 102KB입니다

## 인식된 필드 이름

GenStudio for Performance Marketing은 이메일에 대한 `subject` 필드를 자동으로 생성합니다. 템플릿을 사용자 정의할 때 다음 필수 필드에 콘텐츠 자리 표시자를 사용하십시오.

- `pre_header`(서식 있는 텍스트가 활성화되지 않음)
- `headline`
- `sub_headline`
- `body`
- `cta`
- `image`(컨텐츠 JPEG, PNG 또는 GIF에서 선택됨)

템플릿에서 허용되는 최대 필드는 20개입니다. 템플릿에서 필드 이름을 사용하는 방법에 대한 자세한 내용은 [콘텐츠 자리 표시자](/help/user-guide/content/customize-template.md#content-placeholders)를 참조하십시오.

## 여러 섹션 이메일

_섹션_&#x200B;을(를) 사용하면 콘텐츠를 보다 복잡한 레이아웃을 지원하는 고유한 그룹으로 구성할 수 있습니다. Genstudio for Performance Marketing에서는 그룹 명명 규칙을 사용하여 각 섹션을 정의할 수 있습니다. [템플릿 섹션 사용자 지정](/help/user-guide/content/customize-template.md#sections-or-groups)을 참조하세요.

다중 섹션 템플릿에는 0, 2 또는 3개의 섹션이 있을 수 있습니다.

- 기본 템플릿(0개의 섹션)은 그룹 명명 규칙이 필요하지 않은 단일 템플릿 요소 집합을 생성할 수 있습니다.
- 복합 템플릿(여러 섹션)은 최대 3개의 템플릿 요소 집합을 생성할 수 있으므로 그룹 명명 규칙(`groupname_fieldname`)을 준수해야 합니다.

두 섹션의 필드 이름 예:

- `pod1_headline`, `pod1_body`, `pod1_cta`
- `pod2_headline`, `pod2_body`, `pod2_cta`

## 템플릿 예

+++예: 한 개의 섹션이 있는 이메일 템플릿

다음은 하나의 섹션을 포함하는 이메일에 대한 HTML 템플릿의 기본 예입니다. 헤드에는 스타일링을 위한 간단한 인라인 CSS가 포함되어 있습니다. 본문에는 전자 메일 생성 프로세스 중에 GenStudio for Performance Marketing에서 콘텐츠를 삽입하는 데 사용할 `pre_header`, `headline` 및 `image` [자리 표시자](#content-placeholders)가 포함되어 있습니다.

```html {line-numbers="true" highlight="13"}
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
    <body>{{pre_header}}
        <div class="container">
            <h1>{{headline}}</h1>
            <p><a href="{{link}}">
            <img alt="{{headline}}"
                    src="{{image}}"
                    width="600" height="600"
                    border="0"/></a></p>
            <p>{{body}}</p>
        </div>
    </body>
</html>
```

+++

+++예: 여러 섹션이 있는 이메일 템플릿

다음은 위의 예제와 동일한 HTML 템플릿이지만 두 개의 섹션이 더 있습니다. 헤드에는 그룹을 스타일링할 인라인 CSS가 포함되어 있습니다. 본문에서는 접두사를 사용하여 [콘텐츠 자리 표시자](#content-placeholders)가 있는 두 개의 그룹을 사용합니다.

```html
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
    <body>{{pre_header}}
        <div class="container">
            <h1>{{headline}}</h1>
            <p>{{body}}</p>
            <!-- Pod1 -->
            <div class="pod">
                <h2>{{pod1_headline}}</h2>
                <p><img alt="{{ headline }}" src="{{pod1_image}}" width="200" height="200" border="0"></p>
                <p>{{pod1_body}}</p>
            </div>
            <!-- End of Pod1 -->
            <!-- Pod2 -->
            <div class="pod">
                <h2>{{pod2_headline}}</h2>
                <p><img alt="{{headline}}" src="{{pod2_image}}" width="200" height="200" border="0"></p>
                <p>{{pod2_body}}</p>
            </div>
            <!-- End of Pod2 -->
        </div>
    </body>
</html>
```

+++
