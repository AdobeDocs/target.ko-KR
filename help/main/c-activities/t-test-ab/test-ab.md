---
keywords: AB;A/B;AB...n;경험 비교;타깃팅;콘텐츠 비교;자동 타겟;자동 할당
description: Adobe의 다양한 A/B 테스트 활동 유형에 대해 알아봅니다. [!DNL Target] - 수동, 자동 할당 및 자동 타겟 당신에게 맞는 것을 고르세요.
title: Target에서 사용할 수 있는 A/B 활동 유형은 무엇입니까?
feature: A/B Tests
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
source-git-commit: b5da2f5d41739af39d97e0ce9761006794c04d2b
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 25%

---

# A/B 테스트 개요

설명서 [!UICONTROL A/B 테스트] 활동은 웹 사이트 콘텐츠의 버전을 두 개 이상 비교하여 사전 지정된 테스트 기간 동안 전환율이 가장 많이 향상된 버전을 확인합니다.

>[!NOTE]
>
>수동 (기본값) 외에도 [!UICONTROL A/B 테스트] 활동(이 섹션에서 설명됨), [!DNL Target] 에서는 두 가지 추가 유형을 제공합니다. [!UICONTROL A/B 테스트] 활동: [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타기팅]. 다음을 참조하십시오 [A/B 테스트 활동 유형](#types) 자세한 내용은 아래를 참조하십시오.

설명서 [!UICONTROL A/B 테스트] 활동(A/B...N 테스트라고도 함)은 웹 사이트 콘텐츠의 버전을 두 개 이상 비교하여 사용자가 식별한 전환, 판매 또는 기타 지표를 가장 잘 상승시키는 버전을 확인합니다. A/B 테스트에서 페이지의 변경 사항을 기본 페이지 디자인과 비교하여 최상의 결과를 산출하는 경험을 확인합니다.

수동 A/B 테스트는 성공 지표 또는 대체 콘텐츠 전달을 기반으로 페이지 성능을 개선하는 방법에 대한 명확한 가설이 있는 경우 유용합니다.

수동 A/B 테스트는 새로운 레이아웃 또는 대폭적으로 다른 요소 처리를 포함할 수 있는 큰 변화에 적합합니다. 테스트 디자인이 개별 페이지 요소로 쉽게 분류되지 않는 경우 [다변량 테스트](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md).

A/B 테스트를 설정할 때 각 경험을 보는 방문자의 비율을 결정할 수 있습니다. 예를 들어, 제어 경험과 두 번째 경험 간에 트래픽을 균등하게 분할하거나, 좀 더 위험한 신규 경험을 대상의 5%에만 공개하여 테스트해볼 수 있습니다.

>[!NOTE]
>
>A/B 테스트를 위한 최적 샘플 크기 결정에 대한 자세한 내용은 [A/B 테스트 계획](/help/main/c-activities/t-test-ab/sample-size-determination.md)을 참조하십시오.

서로 다른 경험의 수가 5개를 초과하고 둘 이상의 위치에 걸쳐 있는 경우 다음을 고려하는 것이 좋습니다. [MVT 테스트](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) A/B 테스트를 실행하기 전에 다변량 테스트는 페이지에서 전환율 개선 가능성이 가장 높은 영역을 보여줍니다. 이러한 영역은 마케터가 집중해야 하는 위치입니다. 예를 들어, MVT 테스트는 클릭 유도 문안이 목표 달성을 위한 가장 중요한 위치임을 보여줄 수 있습니다. 목표 달성에 가장 유용한 위치 및 콘텐츠를 파악한 후 A/B 테스트를 실행하여 결과를 세분화할 수 있습니다. 예를 들어 두 개의 특정 이미지를 서로 테스트하거나 클릭 유도 문안의 문구 또는 색상을 비교할 수 있습니다. MVT 테스트 다음에 하나 이상의 A/B 테스트를 실행하면 원하는 결과에 대해 가능성이 가장 높은 콘텐츠를 판단할 수 있습니다.

## A/B 테스트 활동 유형 {#types}

설명서 외에 [!UICONTROL A/B 테스트] 활동(이 섹션에서 설명됨), [!DNL Target] 에서는 두 가지 추가 A/B 테스트 활동 유형을 제공합니다. [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타기팅].

| 활동 유형 | 설명 |
| --- | --- |
| [!UICONTROL 수동 A/B 테스트] | 사전 지정된 테스트 기간 동안 전환을 향상시킨 최고의 경험을 확인하기 위해 둘 이상의 경험을 비교합니다.<P>이 섹션에서는 설명서 설정 방법에 대해 설명합니다 [!UICONTROL A/B 테스트] 활동(다른 유형의 경우) [!UICONTROL A/B 테스트] 활동은 유사합니다. |
| [!UICONTROL 자동 할당] | 둘 이상의 경험에서 승자를 확인한 다음, 트래픽을 승자로 리디렉션하여 테스트가 실행되고 학습이 진행됨에 따라 전환을 늘립니다.<P>을(를) 사용하여 얻을 수 있는 이점에 대해 알아보려면 [!UICONTROL 자동 할당] 활동, 참조 [자동 할당](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) 위치: *A/B 테스트를 얼마 동안 실행해야 합니까?* 및 [자동 할당 개요](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![Premium 배지](/help/main/assets/premium.png) [!UICONTROL 자동 타기팅] | 고급 기계 학습을 사용하여 높은 성과를 보이는, 마케터가 정의한 여러 경험을 식별하여 콘텐츠를 개인화하고 전환을 유도합니다. 그런 다음 개별 고객 프로필 및 유사한 방문자의 이전 행동에 따라 방문자에게 가장 적합한 경험을 제공합니다.<P>자세한 내용은 [자동 타기팅](/help/main/c-activities/auto-target/auto-target-to-optimize.md). |

이들 중 어느 것에 대한 자세한 내용은 [!UICONTROL A/B 테스트] 활동이 적합합니다. 대화식 을 참조하십시오. [Adobe Target 활동 안내서 PDF](/help/main/c-activities/target-activities-guide.md).

다음 세 가지 유형의 [!UICONTROL A/B 테스트] 활동은 유사합니다. 을(를) 만들려면 [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 타기팅] 활동, 시작 기준 [A/B 테스트 활동 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md), 하지만 다음 위치에 도달하면 [!UICONTROL 타겟팅] 아래에서 보듯이 원하는 트래픽 할당 방법을 선택합니다.

* [!UICONTROL 최고 경험에 자동 할당]
* [!UICONTROL 개인화된 경험에 대한 자동 타겟]

![트래픽 할당 방법 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## A/B 활동 내에 권장 사항 포함

내에 권장 사항을 포함할 수 있습니다. [!UICONTROL A/B 테스트], [!UICONTROL 자동 할당], 및 [!UICONTROL 자동 타기팅] 활동(및) [!UICONTROL 경험 타기팅] (XT) 활동). 자세한 내용은 [오퍼로서의 Recommendations](/help/main/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오.

이 기능을 사용하려면 [Target Premium 라이선스](/help/main/c-intro/intro.md#premium)가 있어야 합니다

## 교육 비디오: 활동 유형(9:03) ![개요 배지](/help/main/assets/overview.png)

다음 비디오에서는 [!DNL Target Standard/Premium]에서 사용할 수 있는 활동 유형에 대해 설명합니다.

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로 설명

>[!VIDEO](https://video.tv.adobe.com/v/17386)
