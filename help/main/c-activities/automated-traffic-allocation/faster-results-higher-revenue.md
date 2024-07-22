---
keywords: 자동화된 트래픽 할당;타깃팅;자동 할당;자동 할당
description: ' [!DNL Adobe Target] 의 [!UICONTROL Auto Allocate] 활동이 둘 이상의 경험에서 승자를 식별하고 더 많은 트래픽을 승자에게 자동으로 재할당하는 방법에 대해 알아봅니다.'
title: '[!UICONTROL Auto-Allocate] 활동을 통해 더 빠른 결과와 더 높은 수익을 얻을 수 있습니까?'
feature: Auto-Allocate
exl-id: 104ad88f-044b-4c2f-bdaf-f023fd1787a5
source-git-commit: e9976135c46f6658030b07fce384364f0c9ff0ed
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# [!UICONTROL Auto-Allocate]은(는) 수동 테스트보다 더 빠른 테스트 결과와 더 높은 매출을 제공합니다.

수동 A/B 활동에서는 활동이 완료될 때까지 전체 대상자에게 우승 경험을 전달할 수 없기 때문에 전환율이 손실될 수 있습니다. 트래픽 분산은 일부 경험이 다른 경험보다 뛰어난 성과를 보인다는 사실을 인식하더라도 고정된 상태를 유지하며, 승자에게 조치를 취하려면 먼저 활동이 전체 과정을 실행해야 합니다.

## 트래픽 자동 할당

샘플 크기, 신뢰 수준 및 기타 통계 개념을 선택하는 설정 및 계산 비용을 동시에 제거하거나 줄이면서 활동에서 가장 성과가 좋은 경험을 더 자주 더 일찍 제공하는 옵션을 원하는 경우 [!UICONTROL Auto-Allocate]이(가) 가장 적합한 옵션입니다.

## [!UICONTROL Auto-Allocate]은(는) 어떻게 작동합니까?

[!UICONTROL Auto-Allocate]은(는) multi-armed bandit 원리를 사용합니다. 이 용어가 생소하다면, &#39;원-무장 강도&#39;는 슬롯 머신(Slot machine, Las Vegas)을 뜻하는 구어입니다. 여러 슬롯 머신(이 경우, 변형 테스트)이 있고 처음에 모든 핸들을 동일하게 가져오는 것처럼 트래픽의 자동 할당을 시각화합니다. 시간이 지남에 따라, 하나 이상의 머신 또는 테스트 변형이 다른 것보다 더 많은 비용을 지불할 수 있습니다. 이런 상황이 벌어지면 자연스럽게 승부수를 자주 끄는 도박꾼의 핸들이 늘어나기 시작한다. 트래픽 할당 조건에서 [!DNL Target]은(는) 더 많은 방문자에게 더 많은 경험을 제공하는 데 사용됩니다.

2주 A/B 활동에 대한 다음 그림을 생각해 보십시오. [!UICONTROL Auto-Allocate]을(를) 사용하면 가장 성과가 좋은 경험이 나타나면 [!UICONTROL Target]은(는) 테스트 초기에 더 많은 트래픽을 해당 승자로 전환합니다.

![자동 할당 그림](/help/main/c-activities/automated-traffic-allocation/assets/Auto-Allocate-test.png)

## [!UICONTROL Auto-Allocate]에서 더 빠른 결과를 제공하는 방법은 무엇입니까?

좋은 점은 분명합니다. 더 많은 방문자가 가장 뛰어난 성과를 보이는 변형을 보게 된다는 것입니다. 그리고 하나의 변형이 진행됨에 따라 테스트가 계속 실행되는 동안 더 많은 방문자가 우승 경험으로 전환됩니다. 이 방법은 실행 중인 A/B 활동이 휴일, 제품 출시 또는 월드 뉴스 이벤트와 같은 핵심 비즈니스 순간 중에 발생하는 경우 특히 유용합니다.

## [!UICONTROL Auto-Allocate]에서 더 높은 매출을 제공하는 방법은 무엇입니까?

[!UICONTROL Auto-Allocate]은(는) 수동 A/B 분할보다 더 빨리 승자를 찾고, 기존 또는 수동 접근 방식으로 손실되었을 수 있는 상향 매출을 즉시 포착하는 승자를 활용할 수 있습니다. [!UICONTROL Auto-Allocate]은(는) 전환율이 가장 높은 경험에 더 많은 트래픽을 보내기 때문에 활동이 실행되고 학습되는 동안 매출을 높일 수 있습니다.

다음 예에서는 [!UICONTROL Auto-Allocate]이(가) 전환율이 가장 높았던 경험 D에 더 많은 트래픽(40%)을 푸시하여 테스트 중에 더 많은 매출을 올렸습니다.

![자동 할당을 통해 더 높은 매출을 파악할 수 있음](/help/main/c-activities/automated-traffic-allocation/assets/five-experiences.png)

## 어떤 경우에 수동 트래픽 할당을 유지해야 합니까?

모든 경험이 다른 경험에 비해 상대적으로 어떻게 수행되는지 등급 순으로 정렬해야 하는 경우 수동 A/B 테스트를 가장 적용할 수 있습니다. [!UICONTROL Auto-Allocate]은(는) 상위 수행자를 찾아 활용하지만 성과가 낮은 경험 간의 차별화를 보장하지는 않습니다. 각 테스트 변형을 보는 방문자 트래픽 양을 완벽하게 제어하고 비즈니스와 관련된 통계 임계값을 사용자 지정하려면 수동 트래픽 할당을 사용합니다.

## 시작하기

첫 번째 [!UICONTROL Auto-Allocate] 활동을 시작할 준비가 되셨습니까? [방법을 알아보세요](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).
