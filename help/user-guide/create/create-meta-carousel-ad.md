---
title: Meta 광고 경험 만들기 - 광고 회전
description: '[!DNL GenStudio for Performance Marketing]에서 다중 카드 Meta 캐러셀 광고 경험을 만들고, 카드를 관리하고, 브랜드 내 개념을 생성하는 방법을 알아봅니다.'
role: User
source-git-commit: 1b407c1c66a2426b21cbbf423774ebdff16a7dec
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 1%
---

# Meta 캐러셀 광고 경험 만들기

Meta 캐러셀 광고는 각각 고유한 이미지 또는 비디오, 헤드라인 및 링크가 있는 2~10개의 유연한 카드를 보여주는 유료 광고 형식입니다.

이 페이지에서는 캐러셀 광고와 관련된 단계를 다룹니다. 템플릿 선택, 매개 변수 추가, 변형 수정 및 게시와 같이 이 페이지가 반복하지 않는 공유 단계는 [Meta 광고 경험 만들기](/help/user-guide/create/create-meta-ad.md)를 참조하십시오.

## 사전 요구 사항

회전식 광고를 만들기 전에 모든 페이지가 1:1 또는 4:5의 한 종횡비를 공유하는 템플릿이 있는지 확인하십시오. 각 템플릿 페이지는 하나의 카드가 됩니다. 자세한 내용은 [Meta 광고 템플릿 지침](/help/user-guide/templates/meta-template.md)을 참조하세요.

## 회전 메뉴 형식 선택

템플릿을 선택하고 캔버스를 연 후 프롬프트 서랍에서 슬라이드 형식을 선택합니다.

1. _[!DNL Create your ads]_&#x200B;패널에서&#x200B;_[!UICONTROL &#x200B;매개 변수&#x200B;]_&#x200B;를 확장합니다.
1. **[!UICONTROL 형식]** 드롭다운 메뉴에서 **[!UICONTROL 광고 회전]**&#x200B;을(를) 선택합니다.

   ![형식 드롭다운이 회전 광고 및 카드 목록으로 설정된 광고 패널 만들기](./carousel-format-cards.png){width="70%" zoomable="yes"}

단일 페이지 템플릿에서 시작하는 경우 [!DNL GenStudio for Performance Marketing]에서 페이지를 복제하여 최소 두 장의 카드를 충족합니다. 템플릿 페이지가 모두 하나의 종횡비를 공유하지 않는 경우 일관된 종횡비의 템플릿을 사용할 때까지 형식 스위치가 차단됩니다.

## 카드 관리

생성하기 전에 프롬프트 서랍에 카드 세트를 작성하십시오. 카드를 더 추가하려면 기존 카드를 복제하십시오.

* **카드를 복제하려면** 카드 옵션에서 **[!UICONTROL 복제]**&#x200B;를 선택하십시오.
* **카드를 다시 정렬하려면** 핸들을 사용하여 카드를 새 위치로 끕니다.
* **카드를 삭제하려면** 카드 옵션에서 **[!UICONTROL 삭제]**&#x200B;를 선택하십시오. 캐러셀에 카드가 두 개 이상 필요하므로 마지막 두 카드는 삭제할 수 없습니다.

각 카드에 대해 하나의 이미지를 선택하고 필요한 경우 상위 제품을 오버라이드하는 카드별 제품을 설정합니다. 카드당 하나의 이미지를 개별적으로 선택합니다. 카드별 대상 URL은 나중에 [!DNL Activate]에서 설정됩니다. 자세한 내용은 [Meta 광고 활성화](/help/user-guide/activation/activate-meta-ad.md)를 참조하십시오.

## 회전 메뉴 작성

프롬프트에서 회전 메뉴의 의도를 나타내므로 카드가 서로 어떻게 관련되는지 설명하십시오. 회전식 복사는 다음 두 가지 방법 중 하나를 따를 수 있습니다.

* **모듈:** 각 카드는 자체 포함된 광고이며 카드 간에 복사본이 흐르지 않습니다. 여러 제품과 같이 관련성이 있지만 독립적인 메시지 세트에 대해 이 접근 방식을 사용합니다.
* **순차적:** 복사본은 여러 카드를 연결하여 스토리, 단계별 시퀀스 또는 사용 방법을 알려줍니다. 카드가 서로 쌓일 때 이 방법을 사용하십시오.

캐러셀에 단일 제품 또는 여러 제품 포함 여부와 카드별 세부 사항을 설명할 수도 있습니다.

예를 들어 이 프롬프트는 여러 제품을 사용하는 모듈식 회전판에 대해 설명합니다.

```properties
Create a multi-product carousel for our end-of-summer skincare sale. For each card, lead with the product's core benefit and emphasize the sale value.
```

이 프롬프트는 5개의 카드에 걸쳐 스토리를 제공하는 순차적 캐러셀에 대해 설명합니다.

```properties
Create a narrative carousel for our compliance alert-management platform. Start with shared intro text about the cost of alert fatigue. Across five cards, build the story: rising review costs, too many low-value alerts, false positives as the hidden cost driver, a solution that cuts false positives by more than 50%, and a closing learn-more call to action.
```

프롬프트 기본 사항에 대해서는 [유효한 프롬프트 작성](/help/user-guide/effective-prompts.md)을 참조하십시오.

## 개념 생성 및 검토

카드와 프롬프트를 설정한 후 슬라이드를 생성하고 결과를 검토합니다.

1. **[!UICONTROL 생성]**&#x200B;을 선택하십시오.

   [!DNL GenStudio for Performance Marketing]은(는) 네 가지 캐러셀 개념을 생성합니다. 각 콘셉트는 자체 브랜드 점수가 있는 완전한 멀티 카드 캐러셀입니다.

   ![브랜드 점수와 편집 단추가 있는 4개의 생성된 회전 메뉴 개념](./carousel-concepts.png){width="80%" zoomable="yes"}

1. 개념을 선택한 다음 **[!UICONTROL 편집]**&#x200B;을 선택하여 편집할 수 있도록 엽니다.
1. 화살표를 사용하여 카드 간에 이동한 다음 텍스트를 편집하거나 **[!UICONTROL 교체]**&#x200B;를 선택하여 카드 이미지를 변경합니다. 편집에 대한 자세한 내용은 [변형 관리](/help/user-guide/create/manage-variants.md)를 참조하십시오.

카드를 생성하기 전에 순서를 변경하면 캔버스가 즉시 업데이트됩니다. 카드를 생성한 후 프롬프트 서랍에서 카드 순서를 변경하는 경우 변경 사항은 다시 생성한 후에만 적용되며 재생성 경고가 나타납니다.

## 카드별 및 공유 필드 이해

일부 캐러셀 필드는 각 카드에 개별적으로 적용되고 다른 필드는 전체 광고에 적용됩니다. 다음 표에서는 Meta 캐러셀 광고에 대해 각 필드가 작동하는 방식을 설명합니다.

| 필드 | 범위 |
|---|---|
| 제목 | 카드당 |
| 설명 | 카드당, 선택 사항, [!DNL Activate]에 설정됨 |
| Call to action | 광고에서 공유됨 |
| 기본 텍스트 | 광고에서 공유됨 |
| 미디어 | 카드당(이미지, 비디오 또는 혼합) |
| 이미지 내 텍스트 | 카드당 |
| 대상 URL | 카드당, [!DNL Activate]에 설정됨 |

## 게시, 내보내기 및 활성화

캐러셀이 준비되면 다른 Meta 광고와 동일한 방식으로 게시하고 내보냅니다. 회전판은 하나의 개념에 해당하는 단일 경험으로 저장됩니다. 내보내기는 CSV 파일과 카드 미디어를 제공합니다. 게시된 경험이 저장되는 방법은 [[!DNL Content]](/help/user-guide/content/overview.md)을(를) 참조하십시오. 캐러셀을 Meta으로 활성화하려면 [Meta 광고 활성화](/help/user-guide/activation/activate-meta-ad.md)를 참조하십시오.
