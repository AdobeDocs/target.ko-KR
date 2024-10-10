---
keywords: AB;A/B;AB...n;경험 비교;타깃팅;콘텐츠 비교;자동 타겟;자동 할당
description: ' [!DNL Target] - [!UICONTROL Manual], [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target]에서 A/B 테스트 활동을 살펴봅니다.'
title: ' [!DNL Target]에서 사용할 수 있는 A/B 테스트 활동을 살펴보십시오.'
feature: A/B Tests
hide: true
hidefromtoc: true
source-git-commit: 36cc6486a95b977589aced55168a93ffd300d78f
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 21%

---

# A/B 테스트 개요

수동 [!UICONTROL A/B Test] 활동(A/B...N 테스트라고도 함)은 웹 사이트 콘텐츠의 버전을 두 개 이상 비교하여 전환, 판매 또는 식별한 다른 지표를 가장 잘 활용하는 버전을 확인합니다. A/B 테스트에서 페이지의 변경 사항을 기본 페이지 디자인과 비교하여 최상의 결과를 산출하는 경험을 확인합니다.

>[!TIP]
>
>[!DNL Target]은(는) [!UICONTROL Manual](기본값) [!UICONTROL A/B Test] 활동(이 문서에서 설명됨) 외에도 두 가지 유형의 [!UICONTROL A/B Test] 활동을 추가로 제공합니다. [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target]. 자세한 내용은 아래 [A/B 테스트 활동 유형](#types)을 참조하십시오.

수동 A/B 테스트는 성공 지표 또는 대체 콘텐츠 전달을 기반으로 페이지 성능을 개선하는 방법에 대한 명확한 가설이 있는 경우 유용합니다.

수동 A/B 테스트는 새로운 레이아웃 또는 대폭적으로 다른 요소 처리를 포함할 수 있는 큰 변화에 적합합니다. 테스트 디자인이 개별 페이지 요소로 쉽게 분류되지 않는 경우 [다변량 테스트](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)를 실행하기 전에 A/B 테스트를 실행해야 합니다.

A/B 테스트를 설정할 때 각 경험을 보는 방문자의 비율을 결정할 수 있습니다. 예를 들어, 제어와 두 번째 경험 간에 트래픽을 균등하게 분할하거나 대상의 5%에게만 표시하여 보다 위험한 새로운 경험을 테스트할 수 있습니다.

>[!NOTE]
>
>A/B 테스트를 위한 최적 샘플 크기 결정에 대한 자세한 내용은 [A/B 테스트 계획](/help/main/c-activities/t-test-ab/sample-size-determination.md)을 참조하십시오.

각기 다른 경험의 수가 5개를 초과하고 둘 이상의 위치에 걸쳐 있는 경우 A/B 테스트를 실행하기 전에 [MVT 테스트](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)를 실행하는 것이 좋습니다. 다변량 테스트는 페이지에서 전환율 개선 가능성이 가장 높은 영역을 보여줍니다. 이러한 영역은 마케터가 집중해야 하는 위치입니다. 예를 들어, MVT 테스트는 클릭 유도 문안이 목표 달성을 위한 가장 중요한 위치임을 보여줄 수 있습니다. 목표 달성에 가장 유용한 위치 및 콘텐츠를 파악한 후 A/B 테스트를 실행하여 결과를 세분화할 수 있습니다. 예를 들어 두 개의 특정 이미지를 서로 테스트하거나 클릭 유도 문안의 문구 또는 색상을 비교할 수 있습니다. MVT 테스트 다음에 하나 이상의 A/B 테스트를 실행하면 원하는 결과에 대해 가능성이 가장 높은 콘텐츠를 판단할 수 있습니다.

## A/B 테스트 활동 유형 {#types}

수동 [!UICONTROL A/B Test] 활동 외에 [!DNL Target]에서는 두 가지 유형의 [!UICONTROL A/B Testing] 활동을 추가로 제공합니다. [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target].

| 활동 유형 | 설명 |
| --- | --- |
| [!UICONTROL Manual A/B Test] | 사전 지정된 테스트 기간 동안 전환을 최고로 향상시킨 경험을 확인하기 위해 둘 이상의 경험을 비교합니다.<P>이 섹션에서는 수동 [!UICONTROL A/B Test] 활동을 설정하는 방법에 대해 설명하지만 다른 유형의 [!UICONTROL A/B Test] 활동에 대한 단계는 유사합니다. |
| [!UICONTROL Auto-Allocate] | 둘 이상의 경험에서 승자를 확인한 다음, 트래픽을 승자로 리디렉션하여 테스트가 실행되고 학습이 진행됨에 따라 전환을 늘립니다.<P>[!UICONTROL Auto-Allocate] 활동을 사용할 때의 이점에 대해 알아보려면 *A/B 테스트를 얼마 동안 실행해야 합니까* 및 [자동 할당 개요](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)의 [자동 할당](/help/main/c-activities/t-test-ab/sample-size-determination.md#auto-allocate)을 참조하십시오. |
| ![프리미엄 배지](/help/main/assets/premium.png) [!UICONTROL Auto-Target] | 고급 기계 학습을 사용하여 높은 성과를 보이는, 마케터가 정의한 여러 경험을 식별하여 콘텐츠를 개인화하고 전환을 유도합니다. 그런 다음 개별 고객 프로필 및 유사한 방문자의 이전 행동에 따라 방문자에게 가장 적합한 경험을 제공합니다.<P>자세한 내용은 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md)을 참조하세요. |

이러한 [!UICONTROL A/B Test]개의 활동 중 사용자에게 적합한 활동에 대한 자세한 내용은 대화형 [Adobe Target 활동 안내서 PDF](/help/main/c-activities/target-activities-guide.md)를 참조하십시오.

세 가지 유형의 [!UICONTROL A/B Test] 활동을 만드는 단계는 유사합니다. [!UICONTROL Auto-Allocate] 또는 [!UICONTROL Auto-Target] 활동을 만들려면:

1. [A/B 테스트 활동 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)부터 시작합니다.
1. [!UICONTROL Targeting] 페이지로 이동하면 [!UICONTROL Traffic Allocation] 컨트롤을 클릭한 다음 아래 그림과 같이 오른쪽 창에서 원하는 트래픽 할당 방법을 선택합니다.

   * [!UICONTROL Auto-Allocate to best experience]
   * [!UICONTROL Auto-Target for personalized experience]

   ![트래픽 할당 메서드 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method-new.png)

## A/B 활동 내에 권장 사항 포함

[!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] 활동(및 [!UICONTROL Experience Targeting](XT) 활동) 내에 권장 사항을 포함할 수 있습니다. 자세한 내용은 [오퍼로서의 Recommendations](/help/main/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오.

이 기능을 사용하려면 [Target Premium 라이선스](/help/main/c-intro/intro.md#premium)가 있어야 합니다.