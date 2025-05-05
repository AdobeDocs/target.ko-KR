---
keywords: 자동 타겟;타기팅;트래픽 할당;자주 묻는 질문;faq;문제 해결;문제해결;트래픽
description: '[!UICONTROL Auto-Target] 활동에 대한 문제 해결 주제 및 FAQ를 살펴봅니다.'
title: '[!UICONTROL Auto-Target] 활동 문제를 해결하려면 어떻게 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
source-git-commit: 3e8c2d77f300bf0e2ca83a53d30e7b9eee48894e
workflow-type: tm+mt
source-wordcount: '1850'
ht-degree: 29%

---

# [!UICONTROL Auto-Target]개의 FAQ 및 문제 해결

[!DNL Adobe Target]의 [!UICONTROL Auto-Target] 활동에 대한 문제 해결 및 자주 묻는 질문.

## [!UICONTROL Auto-Target]개의 자주 묻는 질문 {#section_5C120A2B11D14D9BAF767BBAB50FED23}

[!UICONTROL Auto-Target] 활동과 함께 작업할 때 다음 FAQ 및 답변을 참조하십시오.

### [!UICONTROL Auto-Target] 활동을 설정하는 모범 사례는 무엇입니까?

+++답변
* [!UICONTROL Revenue per Visit] (RPV) 성공 지표의 비즈니스 가치가 추가 트래픽 요구 사항의 가치가 있는지 여부를 결정합니다. RPV 사용 시에는 전환과 대조적으로 활동이 작동하려면 경험당 최소 1,000개의 전환이 필요합니다.
* 목표를 기반으로 활동을 시작하기 전에 통제와 개인화된 경험 간의 할당을 결정하십시오.
* 적절한 시간 내에 개인화 모델이 만들어지도록 [!UICONTROL Auto-Target] 활동이 실행되는 페이지에 대해 트래픽이 충분한지 판별하십시오.
* 개인화 알고리즘을 테스트하는 경우 활동이 라이브 상태인 동안에는 경험을 변경하거나 프로필 속성을 추가 또는 제거해서는 안 됩니다.
* [!UICONTROL Auto-Target] 활동에서 사용할 오퍼와 위치 간에 A/B 활동을 완료하여 위치 및 오퍼가 최적화 목표에 영향을 주는지 확인해 보십시오. A/B 활동이 상당한 차이를 보이지 않는 경우 [!UICONTROL Auto-Target]도 향상되지 않을 수 있습니다.

  A/B 테스트에 경험 간 통계적으로 중요한 차이가 없다면, 고려 중인 오퍼들이 서로 충분히 다르지 않거나, 선택한 위치가 성공 지표에 영향을 주지 않거나, 최적화 목표가 선택한 오퍼의 영향을 받기에는 전환 단계에서 너무 먼 것일 수 있습니다.

* 활동 중에 경험을 크게 변경하지 않도록 하십시오.

+++

### 모델이 빌드될 때까지 90(제어)/10(목표값) 분할로 [!UICONTROL Auto Target]을(를) 사용하는 것이 좋습니까?[!UICONTROL Adobe]

+++답변
최적의 트래픽 할당 분할은 수행할 작업에 따라 다릅니다.

가능한 많은 트래픽을 개인화하는 것이 목표라면 활동 기간 동안 90%의 목표값 할당과 10%의 제어를 유지할 수 있습니다. 개인화된 알고리즘과 컨트롤의 성능을 비교하는 실험을 실행하는 것이 목표라면 활동 기간 동안 50/50 분할이 가장 좋습니다.

가장 좋은 방법은 방문자가 목표값과 제어 경험 사이를 전환하지 않도록 활동 기간 동안 트래픽 할당 분할 유지하는 것입니다.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

+++

### 방문자가 [!UICONTROL Auto-Target] 활동을 **보지**&#x200B;하고 전환하는 경우 활동에서 전환이 카운트됩니까?

+++답변
아니요. [!UICONTROL Auto-Target] 활동에 대한 자격이 있고 이 활동을 보는 방문자만 보고에서 카운트됩니다.

+++

### 내 [!UICONTROL Auto-Target] 활동이 상승도를 생성하지 않는 이유는 무엇입니까?

+++답변
[!UICONTROL Auto-Target] 활동에서 상승도를 생성하는 데에는 네 가지 요소가 필요합니다.

* 오퍼는 방문자에게 영향을 줄 수 있을 만큼 달라야 합니다.
* 오퍼는 최적화 목표에 영향을 주는 위치에 있어야 합니다.
* 상승도를 감지하려면 테스트에 충분한 트래픽 및 통계적 &quot;검정력&quot;이 있어야 합니다.
* 개인화 알고리즘이 잘 작동해야 합니다.

가장 좋은 작업 방침은 먼저 단순하고 개인화되지 않은 A/B 테스트를 사용하여 활동 경험을 구성하는 콘텐츠와 위치가 전체 응답률에 정말로 영향을 주는지 확인하는 것입니다. 반드시 미리 샘플 크기를 계산하여, 지정된 시간에 실행을 중단하거나 변경하지 않고도 적당한 상승도를 확인하고 A/B 테스트를 실행할 수 있는 전원이 있는지 확인하십시오.

A/B 테스트 결과에 경험들 중 하나 이상에서 통계적으로 의미 있는 상승도가 나타난다면 개인화된 활동이 작동할 확률이 큽니다. 물론, 개인화는 경험의 전체 응답률에 차이가 없는 경우에도 작동할 수 있습니다. 일반적으로 이 문제는 통계적 유의성을 가지고 감지할 최적화 목표에 충분히 큰 영향을 주지 않는 오퍼 및 위치에서 비롯됩니다.

+++

### 내 [!UICONTROL Auto-Target] 활동을 언제 중지해야 합니까?

+++답변
[!UICONTROL Auto-Target]은(는) 항상 최적화되는 &quot;항시적&quot; 개인화로 사용할 수 있습니다. 특히 항상 사용되는 콘텐츠의 경우 [!UICONTROL Auto-Target] 활동을 중지할 필요가 없습니다.

[!UICONTROL Auto-Target] 활동에서 콘텐츠를 크게 변경하려면 보고서를 검토하는 다른 사용자들이 과거 결과를 다른 콘텐츠와 혼동하거나 결부 짓지 않도록 새 활동을 시작하는 것이 좋습니다.

+++

### 모델이 만들어지기까지 얼마나 기다려야 합니까? {#how-long}

+++답변
일반적으로 [!UICONTROL Auto-Target] 활동에 모델을 만드는 데 걸리는 시간은 선택한 활동 위치에 대한 트래픽 및 활동 성공 지표와 관련된 전환율에 따라 다릅니다.

[!UICONTROL Auto-Target]은(는) 해당 경험에 대해 50개 이상의 전환이 있을 때까지 해당 경험에 대한 개인화된 모델을 구축하려고 시도하지 않습니다. 더욱이, 구축된 모델의 품질이 충분하지 않다면([AUC라고 알려진 메트릭 ](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)을(를) 사용하여 홀드아웃 &quot;테스트&quot; 데이터에 대한 오프라인 평가에 의해 결정됨), 모델은 개인화된 방식으로 트래픽을 서비스하는 데 사용되지 않습니다.

[!UICONTROL Auto-Target]의 모델 구축에 대해 몇 가지 더 유의해야 할 사항은 다음과 같습니다.

* 활동이 활성 상태가 되면 [!UICONTROL Auto-Target]은(는) 모델을 만들 때 무작위로 제공된 마지막 45일의 데이터를 고려합니다. 예를 들어, 제어 트래픽과 알고리즘에 의해 유지되는 추가 무작위로 제공되는 데이터를 추가합니다.
* [!UICONTROL Revenue per Visit]이(가) 성공 메트릭인 경우 일반적으로 방문 매출에 존재하는 데이터 변량이 전환율에 비해 높기 때문에 이러한 작업을 수행하려면 일반적으로 모델을 만드는 데 더 많은 데이터가 필요합니다.
* 모델은 경험별로 구축되므로, 개인화된 모델을 재구축하기 전에 새 경험을 위해 충분한 트래픽(최소 50개의 전환)을 수집해야 한다는 의미입니다.

+++

### 내 활동에 모델 하나가 만들어져 있습니다. 해당 경험에 대한 방문이 개인화됩니까?

+++답변
아니요. 개인화를 시작하려면 활동에 만들어져 있는 모델이 두 개 이상이어야 합니다.

+++

### 내 [!UICONTROL Auto-Target] 활동의 결과는 언제 볼 수 있습니까?

+++답변
모델이 만들어져 있는 경험용으로 모델이 있는 경험을 두 개 이상 만들면(녹색 확인 표시) 그때부터 [!UICONTROL Auto-Target] 테스트 결과를 볼 수 있습니다.

+++

### 제어로 사용할 특정 환경을 지정할 수 있습니까?

+++답변
AP([Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)) 또는 AT([자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) 활동을 만드는 동안 컨트롤로 사용할 환경을 선택할 수 있습니다.

이 기능을 사용하면 활동에 구성된 트래픽 할당 비율에 따라 전체 제어 트래픽을 특정 경험으로 라우팅할 수 있습니다. 그런 다음 해당 경험의 제어 트래픽에 대해 개인화된 트래픽의 성능 보고서를 평가할 수 있습니다.

자세한 내용은 [특정 환경을 제어로 사용](/help/main/c-activities/t-automated-personalization/experience-as-control.md)을 참조하십시오.

+++

### [!UICONTROL Auto-Target] 활동 중간에 목표 지표를 변경할 수 있습니까? {#change-metric}

+++답변
Adobe은 활동 중간에 목표 지표를 변경하지 않는 것이 좋습니다. [!DNL Target] UI를 사용하는 활동 중에 목표 지표를 변경할 수 있지만 항상 새 활동을 시작해야 합니다. Adobe은 활동이 실행된 후 목표 지표를 변경하면 어떤 일이 발생하는지 보증하지 않습니다.

이 권장 사항은 [!DNL Target] 또는 [!DNL Analytics] (A4T)을 보고 소스로 사용하는 [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] 및 [!UICONTROL Automated Personalization] 활동에 적용됩니다.

+++

### [!UICONTROL Auto-Target] 활동을 실행하는 동안 [!UICONTROL Reset Report Data] 옵션을 사용할 수 있습니까?

+++답변
[!UICONTROL Auto-Target] 활동에 [!UICONTROL Reset Report Data] 옵션을 사용하는 것은 권장되지 않습니다. 이 옵션을 사용하면 표시되는 보고 데이터는 제거되지만 [!UICONTROL Auto-Target] 모델에서 모든 교육 기록이 제거되지는 않습니다. [!UICONTROL Auto-Target] 활동에 [!UICONTROL Reset Report Data] 옵션을 사용하는 대신 새 활동을 만들고 원래 활동을 비활성화하십시오.

이 지침은 [!UICONTROL Auto-Allocate] 및 [!UICONTROL Automated Personalization] 활동에도 적용됩니다.

+++

### [!UICONTROL Auto-Target] 활동에서 단일 경험을 제거하면 어떻게 됩니까?

+++답변
[!DNL Target]은(는) 경험당 하나의 모델을 구축하므로, 한 경험을 제거하면 [!DNL Target]은(는) 한 개의 모델을 더 적게 구축하며 다른 경험의 모델에는 영향을 주지 않습니다.

예를 들어 경험이 8개인 [!UICONTROL Auto-Target] 활동이 있는데 한 가지 경험의 성능이 마음에 들지 않는다고 가정합시다. 해당 경험을 제거할 수 있으며, 나머지 7개 경험의 모델에는 영향을 주지 않습니다.

+++

## 문제 해결 [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

활동은 경우에 따라 예상대로 수행되지 않을 수 있습니다. [!UICONTROL Auto-Target]과(와) 몇 가지 제안된 해결 방법을 사용하는 동안 발생할 수 있는 몇 가지 잠재적인 어려움에 대해 설명합니다.

### [!UICONTROL Auto-Target] 활동에서 모델을 만드는 데 시간이 너무 오래 걸립니다.

+++문제 해결 제안
[!UICONTROL Auto-Target] 활동에 있는 경험 수, 사이트에 대한 트래픽, 선택한 성공 지표 등 모델을 만드는 데 드는 예상 시간을 줄일 수 있는 몇 가지 활동 설정 변경 사항이 있습니다.

**해결 방법:** 활동 설정을 검토하여 모델을 만드는 속도를 개선하기 위해 변경할 사항이 있는지 확인하십시오.

* 성공 지표가 [!UICONTROL RPV] (으)로 설정된 경우 전환으로 변경할 수 있습니까? 전환 활동은 일반적으로 모델을 만드는 데 필요한 트래픽이 적습니다. 성공 지표를 RPV에서 전환으로 변경하면 활동 데이터가 손실되지 않습니다.
* 성공 지표가 활동 경험에서 판매 경로의 아래쪽에 있습니까? 활동 전환율이 낮으면 최소 전환 수가 필요하므로 모델을 만드는 데 필요한 트래픽 요구 사항이 증가합니다.
* 활동에서 삭제할 수 있는 경험이 있습니까? 활동의 경험 수를 줄이면 모델을 만드는 시간이 줄어듭니다.
* 이 활동이 더 성공할 트래픽이 더 높은 페이지가 있습니까? 활동 위치에 트래픽과 전환이 많을수록 모델이 더 빨리 구축됩니다.

+++

### 내 [!UICONTROL Auto-Target] 활동이 상승도를 생성하지 않습니다.

+++문제 해결 제안
[!UICONTROL Auto-Target] 활동에서 상승도를 생성하는 데에는 네 가지 요소가 필요합니다.

* 오퍼는 방문자에게 영향을 줄 수 있을 만큼 달라야 합니다.
* 오퍼는 최적화 목표에 영향을 주는 위치에 있어야 합니다.
* 상승도를 감지하려면 테스트에 충분한 트래픽 및 통계적 &quot;검정력&quot;이 있어야 합니다.
* 개인화 알고리즘이 잘 작동해야 합니다.

**해결 방법:** 우선, 활동이 트래픽을 개인화하는지 확인하십시오. 일부 경험에 대해 모델을 만들지 않은 경우에도 [!UICONTROL Auto-Target] 활동은 계속해서 모든 모델을 가능한 한 빨리 만들기 위해 방문 중 상당한 부분을 무작위로 제공하고 있습니다. 모델이 만들어지지 않은 경우 [!UICONTROL Auto-Target]에서 트래픽을 개인화하고 있지 않습니다.

다음으로, 간단한 개인화되지 않은 A/B 테스트를 사용하여 오퍼 및 활동 위치가 전체 응답률과 분명한 차이가 있는지 확인합니다. 반드시 미리 샘플 크기를 계산하여, 지정된 시간에 실행을 중단하거나 변경하지 않고도 적당한 상승도를 확인하고 A/B 테스트를 실행할 수 있는 전원이 있는지 확인하십시오. A/B 테스트 결과가 하나 이상의 경험에 대해 통계적으로 중요한 상승도를 보이면 개인화된 활동이 작동할 가능성이 높습니다. Personalization은 경험의 전체 응답률에 차이가 없어도 작동할 수 있습니다. 일반적으로 이 문제는 통계적 유의성을 가지고 감지할 최적화 목표에 충분히 큰 영향을 주지 않는 오퍼 및 위치에서 비롯됩니다.

+++

### 전환 지표에 종속되는 어떤 지표도 전환되지 않습니다.

+++문제 해결 제안
이는 예상되었습니다.

[!UICONTROL Auto-Target] 활동에서 전환 지표(최적화 목표든 게시 목표든)가 전환되면 사용자는 경험에서 해제되고 활동이 다시 시작됩니다.

예를 들어 전환 지표(C1)와 추가적인 지표(A1)가 있는 활동이 있습니다. A1은 C1에 따라 다릅니다. 방문자가 처음으로 활동을 시작하고 A1 및 C1을 전환하기 위한 기준이 전환되지 않은 경우 지표 A1은 성공 지표 종속성으로 인해 전환되지 않습니다. 방문자가 C1을 변환한 다음 A1을 변환하는 경우 C1이 변환되면 방문자가 해제되므로 A1은 여전히 변환되지 않습니다.

+++
