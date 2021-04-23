---
keywords: AB;A/B;AB...n;비교 경험;타깃팅;비교 내용;자동 대상;자동 할당
description: Adobe [!DNL Target] - 수동, 자동 할당 및 자동 Target에서 다양한 유형의 A/B 테스트 활동에 대해 알아보십시오. 귀하에게 딱 맞는 제품을 선택하십시오.
title: Target에서 사용할 수 있는 A/B 활동 유형은 무엇입니까?
feature: A/B 테스트
exl-id: e8ff8994-a0a9-4fc7-8fcb-e3a1b7697604
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 38%

---

# A/B 테스트 개요

수동 [!UICONTROL A/B 테스트] 활동은 두 개 이상의 웹 사이트 컨텐츠 버전을 비교하여 사전 지정된 테스트 기간 동안 전환을 가장 잘 개선하는 버전을 확인합니다.

>[!NOTE]
>
>수동(기본값) [!UICONTROL A/B 테스트] 활동(이 섹션에 설명됨) 외에 [!DNL Target]는 두 가지 추가 유형의 [!UICONTROL A/B 테스트] 활동을 제공합니다.[!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target].
>
>자세한 내용은 아래 [A/B 테스트 활동 유형](#types)을 참조하십시오.

수동 [!UICONTROL A/B 테스트] 활동(A/B...N 테스트라고도 함)은 둘 이상의 웹 사이트 컨텐츠 버전을 비교하여 전환, 판매 또는 식별한 기타 지표를 가장 잘 높여주는 버전을 확인합니다. A/B 테스트에서 페이지의 변경 사항을 기본 페이지 디자인과 비교하여 최상의 결과를 산출하는 경험을 확인합니다.

수동 A/B 테스트는 성공 지표나 대체 컨텐츠 전달을 기반으로 페이지 성능을 향상시키는 방법에 대한 명확한 가설이 있는 경우 특히 유용합니다.

수동 A/B 테스트는 새로운 레이아웃이나 완전히 다른 요소 처리가 포함될 수 있는 큰 변경에 적합합니다. 테스트 디자인이 개별 페이지 요소로 쉽게 구분되지 않을 경우 [다변수 테스트](/help/c-activities/c-multivariate-testing/multivariate-testing.md) 전에 A/B 테스트를 실행해야 합니다.

A/B 테스트를 설정할 때 각 경험을 보는 방문자의 비율을 결정할 수 있습니다. 예를 들어, 제어 경험과 두 번째 경험 간에 트래픽을 균등하게 분할하거나, 좀 더 위험한 신규 경험을 대상의 5%에만 공개하여 테스트해볼 수 있습니다.

>[!NOTE]
>
>A/B 테스트를 위한 최적 샘플 크기 결정에 대한 자세한 내용은 [A/B 테스트 계획](/help/c-activities/t-test-ab/sample-size-determination.md)을 참조하십시오.

각기 다른 경험의 수가 5개를 초과하고 둘 이상의 위치에 걸쳐 있는 경우 A/B 테스트를 실행하기 전에 [MVT 테스트](/help/c-activities/c-multivariate-testing/multivariate-testing.md)를 실행하는 것이 좋습니다. 다변량 테스트는 페이지에서 전환율 개선 가능성이 가장 높은 영역을 보여줍니다. 마케터는 이러한 위치에 중점을 두어야 합니다. 예를 들어, MVT 테스트는 클릭 유도 문안이 목표 달성을 위한 가장 중요한 위치임을 보여줄 수 있습니다. 목표 달성에 가장 유용한 위치와 컨텐츠를 파악한 후에는 A/B 테스트를 실행하여 2개의 특정 이미지를 서로 테스트하거나 클릭유도문안의 문구 또는 색상을 비교하는 등 결과를 세분화할 수 있습니다. MVT 테스트 다음에 하나 이상의 A/B 테스트를 실행하면 원하는 결과에 대해 가능성이 가장 높은 콘텐츠를 판단할 수 있습니다.

## A/B 테스트 활동 유형 {#types}

수동 [!UICONTROL A/B 테스트] 활동(이 섹션에 설명됨) 이외에도 [!DNL Target]는 두 가지 추가 유형의 A/B 테스트 활동을 제공합니다.[!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target].

| 활동 유형 | 설명 |
| --- | --- |
| [!UICONTROL 수동 A/B 테스트] | 사전 지정된 테스트 기간 동안 전환을 최고로 향상시킨 경험을 확인하기 위해 둘 이상의 경험을 비교합니다.<br>이 섹션에서는 수동  [!UICONTROL A/B 테스트 활동] 을 설정하는 방법을 설명하지만 다른 유형의  [!UICONTROL A/B 테스트 활동] 에 대한 단계는 유사합니다. |
| [!UICONTROL 자동 할당] | 둘 이상의 경험에서 승자를 확인한 후, 트래픽을 승자로 리디렉션하여 테스트가 실행되고 학습이 진행됨에 따라 전환을 늘립니다.<br>자동 할당 활동을 사용하여 얻을 수 있는 이점에 대한 자세한 내용은  [자동 할당](/help/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) 을 참조하십시오. A/B Testand  *자동 할당 개요를* 실행하는 데  [걸리는 시간을 참조하십시오](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| ![프리미엄 ](/help/assets/premium.png) [!UICONTROL 배지자동 Target] | 고급 기계 학습을 사용하여 높은 성과를 보이는, 마케터가 정의한 여러 경험을 식별한 후, 개별 고객 프로필 및 비슷한 방문자의 이전 동작을 기준으로 방문자에게 가장 잘 조정된 경험을 제공함으로써 컨텐츠를 개인화하고 전환을 유도합니다.<br>자세한 내용은 자동 Target [을 참조하십시오](/help/c-activities/auto-target/auto-target-to-optimize.md). |

이러한 [!UICONTROL A/B 테스트] 활동 중 귀하에게 적합한 활동에 대한 자세한 내용은 대화형 [Adobe Target 활동 안내서 PDF](/help/c-activities/target-activities-guide.md)를 참조하십시오.

세 가지 유형의 [!UICONTROL A/B 테스트] 활동을 만드는 단계는 서로 유사합니다. [!UICONTROL 자동 할당] 또는 [!UICONTROL 자동 Target] 활동을 만들려면 [A/B 테스트 활동](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)을 만들기 시작합니다. 하지만 [!UICONTROL 타깃팅] 페이지에 도달하면 아래에서 보듯이 원하는 트래픽 할당 방법을 선택합니다.

* [!UICONTROL 최적의 경험에 자동 할당]
* [!UICONTROL 개인화된 경험을 위한 자동 타깃팅]

![트래픽 할당 방법 설정](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## 교육 비디오:활동 유형(9:03) ![개요 배지](/help/assets/overview.png)

다음 비디오에서는 [!DNL Target Standard/Premium]에서 사용할 수 있는 활동 유형에 대해 설명합니다.

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로우 설명

>[!VIDEO](https://video.tv.adobe.com/v/17386)
