---
keywords: 자동화된 트래픽 할당;타깃팅;자동 할당;자동 할당
description: '[!DNL Adobe Target]의 [!UICONTROL 자동 할당] 활동이 둘 이상의 경험에서 승자를 식별하고 더 많은 트래픽을 승자에게 자동으로 재할당하는 방법에 대해 알아봅니다.'
title: '[!UICONTROL 자동 할당] 활동이 더 빠른 결과와 더 높은 매출을 얻을 수 있습니까?'
feature: Auto-Allocate
exl-id: 104ad88f-044b-4c2f-bdaf-f023fd1787a5
TQID: 'https://experienceleague.adobe.com/aSxZ0Zp3cm0x-fVBXHWW4OiXd3Riz-tuhBiw0f8m4lk'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f2d0aafb-18af-41a0-a32e-2788eafacc2b
    internal-label: Auto-allocate
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 878df20c7fb08c893239135c20f358b5606d0c6f
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%
---
# [!UICONTROL 자동 할당]이 수동 테스트를 능가하는 방법 {#faster-results-higher-revenue}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL 자동 할당]** 활동이 수동 A/B 테스트보다 더 빠른 결과와 더 높은 매출을 제공할 수 있는 이유, 작동 방법, 수동 트래픽 할당이 더 나은 선택으로 남아 있는 경우 알아봅니다.

>[!ENDSHADEBOX]

수동 A/B 활동의 경우, 활동이 완료될 때까지 전체 대상자에게 우승 경험을 전달할 수 없기 때문에 전환을 잃게 될 수 있습니다. 트래픽 분산은 일부 경험이 다른 경험보다 뛰어난 성과를 보인다는 사실을 인식하더라도 고정된 상태를 유지하며, 승자에게 조치를 취하려면 먼저 활동이 전체 과정을 실행해야 합니다.

## 트래픽 자동 할당 {#auto-allocating-traffic}

**[!UICONTROL 자동 할당]**&#x200B;은(는) 샘플 크기, 신뢰 수준 및 기타 통계 개념을 선택하는 설정 및 계산 비용을 제거하거나 줄이면서 활동에서 가장 성과가 좋은 경험을 더 자주 더 일찍 제공하려는 경우 가장 적합한 옵션입니다.

## [!UICONTROL 자동 할당]은(는) 어떻게 작동합니까? {#how-it-works}

**[!UICONTROL 자동 할당]**&#x200B;은(는) multi-armed bandit 원리를 사용합니다. &#39;일방 도적&#39;은 슬롯머신을 뜻하는 구어다. 트래픽의 자동 할당을 슬롯 머신 세트(이 경우 테스트 변형)로 생각해 보십시오. 이 변형의 핸들은 처음에 동일하게 당겨집니다. 시간이 지남에 따라, 하나 이상의 머신 또는 테스트 변형이 다른 것보다 더 많은 비용을 지불할 수 있습니다. 이런 상황이 벌어지면 도박꾼은 자연스레 더 많이 이긴 기계의 손잡이를 당기기 시작한다. 트래픽 할당 조건에서 [!DNL Target]은(는) 더 많은 방문자에게 더 많은 경험을 제공하는 데 사용됩니다.

다음 그림은 2주간의 A/B 활동을 보여줍니다. **[!UICONTROL 자동 할당]**&#x200B;을 사용하면 우승 경험이 나타나면 [!DNL Target]은(는) 테스트 초기에 더 많은 트래픽을 해당 승자로 전환합니다.

![자동 할당 그림](/help/main/c-activities/automated-traffic-allocation/assets/Auto-Allocate-test.png)

## [!UICONTROL 자동 할당]은(는) 어떻게 더 빠른 결과를 제공합니까? {#faster-results}

더 많은 방문자가 가장 성과가 좋은 변형을 봅니다. 하나의 변형이 진행되면 테스트가 여전히 실행되는 동안 더 많은 방문자가 우승 경험으로 전환됩니다. 이 방법은 A/B 활동이 휴일, 제품 출시 또는 월드 뉴스 이벤트와 같은 핵심 비즈니스 순간 동안 실행되는 경우에 특히 유용합니다.

## [!UICONTROL 자동 할당]을 통해 더 높은 매출을 얻을 수 있습니까? {#higher-revenue}

**[!UICONTROL 자동 할당]**&#x200B;은(는) 수동 A/B 분할보다 더 빨리 승자를 찾아 해당 승자를 즉시 활용할 수 있도록 하여 기존 또는 수동 접근 방식으로 손실되었을 수 있는 상향 매출을 포착합니다. **[!UICONTROL 자동 할당]**&#x200B;은(는) 전환율이 가장 높은 경험에 더 많은 트래픽을 할당하므로 활동이 실행되고 학습하는 동안 매출을 높일 수 있습니다.

다음 예제에서는 **[!UICONTROL 자동 할당]**&#x200B;이(가) 전환율이 가장 높았던 경험 D에 더 많은 트래픽(40%)을 푸시하여 테스트 중에 더 많은 매출을 올렸습니다.

![자동 할당을 통해 더 높은 매출을 파악할 수 있음](/help/main/c-activities/automated-traffic-allocation/assets/five-experiences.png)

## 어떤 경우에 수동 트래픽 할당을 유지해야 합니까? {#manual-allocation}

수동 A/B 테스트는 모든 경험이 다른 경험에 비해 상대적으로 어떻게 수행되는지 등급-순서를 지정해야 하는 경우 가장 적용 가능한 옵션입니다. **[!UICONTROL 자동 할당]**&#x200B;은(는) 상위 수행자를 찾아 활용하지만 성과가 낮은 경험 간의 차별화를 보장하지는 않습니다. 각 테스트 변형을 보는 방문자 트래픽 양을 완벽하게 제어하고 비즈니스와 관련된 통계 임계값을 사용자 지정하려면 수동 트래픽 할당을 사용합니다.

## 시작하기 {#get-started}

첫 번째 **[!UICONTROL 자동 할당]** 활동을 시작할 준비가 되셨습니까? [자동 할당 활동 만들기](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) 및 [자동 할당 개요](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)를 참조하십시오.
