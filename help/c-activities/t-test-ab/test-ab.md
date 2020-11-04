---
keywords: AB;A/B;AB...n;compare experiences;Targeting;compare content;auto-target;auto-allocate
description: 수동 A/B 테스트 활동은 두 개 이상의 웹 사이트 컨텐츠 버전을 비교하여 사전 지정된 테스트 기간 동안 전환율을 가장 잘 개선하는 버전을 확인합니다.
title: A/B 테스트 개요
feature: ab
uuid: 154559cf-58bb-425d-bb2e-4eaf34c89451
translation-type: tm+mt
source-git-commit: e18f18e6d6e0b8fc6eb5ada845e2fe5377d6c5d0
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 38%

---


# A/B 테스트 개요

A manual [!UICONTROL A/B Test] activity compares two or more versions of your website content to see which version best improves your conversions during a pre-specified test period.

>[!NOTE]
>
>수동(기본값) [!UICONTROL A/B 테스트] 활동(이 섹션에 설명됨) 외에, 다음 두 가지 추가 [!DNL Target] 유형의 [!UICONTROL A/B 테스트] 활동을 제공합니다. [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target].
>
>자세한 내용은 [아래 A/B 테스트 활동](#types) 유형을 참조하십시오.

A manual [!UICONTROL A/B Test] activity (sometimes referred to as an A/B...N test) compares two or more versions of your Web site content to see which best lifts your conversions, sales, or other metrics you identify. A/B 테스트에서 페이지의 변경 사항을 기본 페이지 디자인과 비교하여 최상의 결과를 산출하는 경험을 확인합니다.

수동 A/B 테스트는 성공 지표 또는 대체 컨텐츠 전달을 기반으로 페이지 성과를 향상시키는 방법에 대한 명확한 가설이 있는 경우 특히 유용합니다.

수동 A/B 테스트는 새로운 레이아웃이나 완전히 다른 요소 처리가 포함될 수 있는 큰 변경에 적합합니다. If your test design does not easily break down into individual page elements, you should run an A/B test before a [multivariate test](/help/c-activities/c-multivariate-testing/multivariate-testing.md).

A/B 테스트를 설정할 때 각 경험을 보는 방문자의 비율을 확인할 수 있습니다. 예를 들어, 제어 경험과 두 번째 경험 간에 트래픽을 균등하게 분할하거나, 좀 더 위험한 신규 경험을 대상의 5%에만 공개하여 테스트해볼 수 있습니다.

>[!NOTE]
>
>A/B 테스트를 위한 최적 샘플 크기 결정에 대한 자세한 내용은 [A/B 테스트 계획](../../c-activities/t-test-ab/sample-size-determination.md)을 참조하십시오.

각기 다른 경험의 수가 5개를 초과하고 둘 이상의 위치에 걸쳐 있는 경우 A/B 테스트를 실행하기 전에 [MVT 테스트](/help/c-activities/c-multivariate-testing/multivariate-testing.md)를 실행하는 것이 좋습니다. 다변량 테스트는 페이지에서 전환율 개선 가능성이 가장 높은 영역을 보여줍니다. 마케터는 이러한 위치에 중점을 두어야 합니다. 예를 들어, MVT 테스트는 클릭 유도 문안이 목표 달성을 위한 가장 중요한 위치임을 보여줄 수 있습니다. 목표 달성에 가장 유용한 위치와 컨텐츠를 파악한 후에는 A/B 테스트를 실행하여 두 개의 특정 이미지를 서로 테스트하거나 클릭 유도 문안의 문구 또는 색상을 비교하는 등 결과를 세부적으로 조정할 수 있습니다. MVT 테스트 다음에 하나 이상의 A/B 테스트를 실행하면 원하는 결과에 대해 가능성이 가장 높은 콘텐츠를 판단할 수 있습니다.

## A/B 테스트 활동 유형 {#types}

수동 [!UICONTROL A/B 테스트] 활동(이 섹션에 설명되어 있음) 외에, 두 가지 추가 유형의 A/B 테스트 [!DNL Target] 활동을제공합니다. [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target].

| 활동 유형 | 설명 |
| --- | --- |
| [!UICONTROL 수동 A/B 테스트] | 사전 지정된 테스트 기간 동안 전환을 최고로 향상시킨 경험을 확인하기 위해 둘 이상의 경험을 비교합니다.<br>이 섹션에서는 수동 [!UICONTROL A/B 테스트] 활동을 설정하는 방법을 설명하지만 다른 유형의 [!UICONTROL A/B 테스트] 활동에 대한 단계는유사합니다. |
| [!UICONTROL 자동 할당] | 둘 이상의 경험에서 승자를 확인한 후, 트래픽을 승자로 리디렉션하여 테스트가 실행되고 학습이 진행됨에 따라 전환을 늘립니다.<br>자동 할당 활동을 사용하여 얻을 수 있는 이점에 대한 자세한 내용은 A/B 테스트 [및](/help/c-activities/t-test-ab/sample-size-determination.md#auto-allocate) 자동 할당 개요를 *실행하는* 데 [필요한](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)시간에서 자동 할당을참조하십시오. |
| ![프리미엄 배지](/help/assets/premium.png) [!UICONTROL 자동 Target] | 고급 기계 학습을 사용하여 높은 성과를 보이는, 마케터가 정의한 여러 경험을 식별한 후, 개별 고객 프로필 및 비슷한 방문자의 이전 동작을 기준으로 방문자에게 가장 잘 조정된 경험을 제공함으로써 컨텐츠를 개인화하고 전환을 유도합니다.<br>자세한 내용은 자동 [Target을 참조하십시오](/help/c-activities/auto-target/auto-target-to-optimize.md). |

이러한 [!UICONTROL A/B 테스트] 활동 중 귀하에게 적합한 활동에 대한 자세한 내용은 인터랙티브한 [Adobe Target 활동 가이드 PDF를 참조하십시오](/help/c-activities/target-activities-guide.md).

세 가지 유형의 [!UICONTROL A/B 테스트] 활동을 만드는 단계는 유사합니다. 자동 할당 [!UICONTROL 또는] 자동 Target  활동을 만들려면 먼저 A/B 테스트 활동 [을](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)만드는 것으로 시작하지만 타깃팅 페이지에 도달하면  아래에서 보듯이 원하는 트래픽 할당 방법을 선택하십시오.

* [!UICONTROL 최적의 경험에 자동 할당]
* [!UICONTROL 개인화된 경험을 위한 자동 타깃팅]

![트래픽 할당 방법 설정](/help/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method.png)

## 교육 비디오:활동 유형(9:03) ![개요 배지](/help/assets/overview.png)

다음 비디오에서는 [!DNL Target Standard/Premium]에서 사용할 수 있는 활동 유형에 대해 설명합니다.

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로우 설명

>[!VIDEO](https://video.tv.adobe.com/v/17386)
