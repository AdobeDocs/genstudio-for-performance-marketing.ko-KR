---
title: Adobe GenStudio for Performance Marketing 개념
description: Adobe GenStudio for Performance Marketing 개념 및 용어를 알아봅니다.
feature: Workflow, Generative AI
role: User
exl-id: 7dd00b4c-f429-499b-851d-3606c82c09dc
source-git-commit: 8a5d15df7a347c4ee7767610fc9bb23fc7b71db4
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# 개념

GenStudio for Performance Marketing은 Adobe의 콘텐츠 공급망을 구현하여 마케팅 캠페인을 간소화하는 독립 실행형 엔터프라이즈 제품입니다. 규모에 맞게 개인화되고 브랜드 승인을 받은 콘텐츠를 구축하고, 효과를 모니터링하며, 끊임없이 변화하는 시장에 신속하게 적응하는 것은 어려운 일입니다. GenStudio for Performance Marketing은 엔터프라이즈 마케팅 팀의 성능 승수로 생성 AI를 활용하는 하나의 애플리케이션에 Creative Cloud과 Experience Cloud을 통합합니다.

GenStudio for Performance Marketing을 사용하여 다음과 같은 작업을 수행할 수 있습니다.

* 유료 미디어, 이메일 및 디스플레이 광고와 같은 최우선 디지털 채널에 대한 자연어 프롬프트를 사용하여 온브랜드 콘텐츠를 만듭니다

* 관련자와 협력하여 생성된 콘텐츠 검토 및 승인
* 생성 및 승인된 콘텐츠를 저장하여 향후 마케팅 캠페인에 액세스
* 자산 성과를 분석하고 최고의 성능을 자랑하는 컨텐츠의 주요 속성을 파악하여 컨텐츠 효과 평가

## 생성 AI 기술

GenStudio for Performance Marketing은 생성 AI의 기능을 활용하여 콘텐츠 생성 프로세스를 가속화하고 고품질의 콘텐츠 생성을 보장합니다. 크리에이티브 에셋의 라이프사이클이 반복되면 타겟 대상자에게 반향을 불러일으키는 정확도와 브랜드 중심 콘텐츠가 점점 더 많아집니다.

강력한 브랜드 가이드라인 기능을 통해 조직의 브랜딩, 고객 담당자 및 제품 설명을 섭취하는 것부터 시작하십시오. 이러한 지침을 준비하고 업로드하는 방법에 대해 알아보려면 [지침 개요](../user-guide/guidelines/overview.md)를 참조하세요.

{{in-academy}}

## 큰 언어 모델

GenStudio for Performance Marketing은 기본 AI와 머신 러닝(ML) 서비스를 제공하는 Adobe의 생성 AI 플랫폼을 활용합니다. 이 플랫폼은 대형 언어 모델(LLM) 사용을 단순화하여 Adobe의 GenAI 기능을 강화하여 매력적인 경험을 만듭니다.

GenStudio for Performance Marketing은 Azure OpenAI를 통해 타사 LLM의 GPT 시리즈를 사용합니다.<!-- Claude, and Gemini models. -->

## [!DNL Generative Actions]

[Adobe GenStudio for Performance Marketing 제품 설명](https://helpx.adobe.com/legal/product-descriptions/adobe-genstudio-for-performance-marketing---product-description.html)에 정의된 _[!DNL Generative Actions]_은(는) GenStudio for Performance Marketing에서 생성 AI 기능의 사용을 정량화하는 단위입니다.

<!-- Add example about usage mode?
Where users check how many generative actions they have left
How they re-up their genactions
If genactions roll over month to month or not -->

### 비율

[GenStudio for Performance Marketing 제품 설명](https://helpx.adobe.com/legal/product-descriptions/adobe-genstudio-for-performance-marketing---product-description.html)에 설명된 대로 기본 [!DNL Generative Actions] 할당을 받습니다.

>[!NOTE]
>
>사용률은 다를 수 있습니다. 계획은 변경될 수 있습니다. 업데이트된 요금 정보는 [Adobe GenStudio for Performance Marketing 제품 설명](https://helpx.adobe.com/legal/product-descriptions/adobe-genstudio-for-performance-marketing---product-description.html)을 참조하세요.

다음 함수는 지정된 비율로 [!DNL Generative Actions]을(를) 사용합니다.

| 함수 | 생성 작용률 |
| -----------------------  | ------------------ |
| 이메일 만들기 | 세대당 5개 |
| 유료 미디어 광고 만들기 | 세대당 5개 |
| 디스플레이 광고 만들기 | 세대당 5개 |
| 단면 재생성 | 세대당 1개 |

<!-- | Generate on-brand images | 1 per prompt  |
| Translation              | 1 per prompt  |
| Video: ADLS              | 1 per prompt  |
| Video: TTS + Avatar      | 1 per prompt  | -->

다음 경우에 [!DNL Generative Actions] _은(는) 사용되지 않습니다_:

* 변형 생성 중 [브랜드 유효성 검사](/help/user-guide/guidelines/brand-validation.md) 사용
* [업로드된 지침](/help/user-guide/guidelines/add-guidelines.md)에서 정보 추출
* 수동으로 [변형을 다시 확인](/help/user-guide/guidelines/brand-validation.md#improve-brand-alignment)
* 디지털 자산에 특성([[!DNL Insights]](/help/user-guide/insights/overview.md))이 자동으로 태그 지정됩니다.

>[!TIP]
>
>[!DNL Generative Actions]의 사용 권한을 초과하는 경우 계정 담당자에게 직접 더 많은 항목을 구입할 수 있습니다.

## 데이터 거버넌스

AI와 함께 콘텐츠를 생성하는 경우 모든 사용자에게 출력이 안전하고 포괄적인지 확인하는 것이 중요합니다. 이를 위해서는 잠재적인 유해한 편견, 혐오 발언, 불쾌한 소재 또는 비속어에 대한 내용 평가가 필요하다. Adobe은 콘텐츠 생성 기술을 다양한 관점에서 철저히 테스트하고, 종합적인 윤리 검토를 수행하며, 유해한 콘텐츠가 출력에 등장하지 않도록 효과적인 완화 방안을 시행한다.

이 접근 방식은 사회적 책임을 강화하고 평판 위험을 최소화하며 [Adobe의 신뢰 및 안전 및 윤리 정책](https://www.adobe.com/content/dam/cc/en/ai-ethics/pdfs/Adobe-AI-Ethics-Principles.pdf)을 준수하도록 합니다.

GenStudio for Performance Marketing은 Adobe 데이터 거버넌스 표준 및 정책에 따라 식별된 유해하거나 편향된 콘텐츠를 사용하지 않도록 완화 계획을 통합합니다. 이러한 콘텐츠가 감지되면 에셋 생성이 &quot;생성할 수 없음&quot; 메시지로 차단됨을 알립니다.

이 메시지가 나타나면 프롬프트를 편집하고 다시 _하거나_ 플래그를 사용하여 GenStudio for Performance Marketing에서 검토할 수 있습니다. 검토용으로 플래그가 지정된 콘텐츠에 대한 프롬프트 데이터는 내부 검토 목적으로 수집됩니다.

## 콘텐츠 라이프사이클

더 빠른 속도로 여러 채널에서 고품질 경험을 구축하려는 수요가 높습니다. GenStudio for Performance Marketing은 콘텐츠 공급망을 마케터를 위해 잘 구성된 워크플로우로 간소화합니다. GenStudio for Performance Marketing은 라이프사이클의 각 단계에서 Adobe 기술을 활용합니다.

<table style="table-layout:auto">

<tr style="border: 0;">

    <td>

       <p><strong>워크플로 및 계획</strong></p>

    </td>

    <td>

        <p>아이디어를 브레인스토밍하고, 지침을 정의하고, 콘텐츠를 중심으로 전략을 구축하여 대상자를 참여시킵니다.</p>

    </td>

</tr>

<tr style="border: 0;">

    <td>

        <p><strong>제작 및 프로덕션</strong></p>

    </td>

    <td>

        <p>플랜을 기반으로 콘텐츠를 생성합니다. 실시간으로 공동 작업하고, 피드백을 받고, 편집하고, 콘텐츠를 승인합니다.</p>

    </td>

</tr>

<tr style="border: 0;">

    <td>

        <p><strong>콘텐츠 관리</strong></p>

    </td>

    <td>

        <p>중앙 집중식 저장소에서 크리에이티브 자산을 저장, 공유 및 찾습니다. 성능을 기반으로 콘텐츠를 재사용하고 활성화할 수 있습니다.</p>

    </td>

</tr>

<tr style="border: 0;">

    <td>

        <p><strong>게재 및 활성화</strong></p>

    </td>

    <td>

        <p>콘텐츠를 활성화하고 여러 마케팅 채널에 게시할 수 있습니다.</P>

    </td>

</tr>

<tr style="border: 0;">

    <td>

        <p><strong>보고 및 통찰력</strong></p>

    </td>

    <td>

        <p>자산 성능 최적화를 위한 데이터를 수집하고 통찰력을 도출합니다.</p>

    </td>

</tr>

</table>
