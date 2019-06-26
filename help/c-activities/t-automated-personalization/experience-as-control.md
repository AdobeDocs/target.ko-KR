---
description: 자동화된 개인화 (AP) 또는 자동 타겟 활동을 만드는 동안 컨트롤로 사용할 경험을 선택합니다.
keywords: 경험; 제어; 자동화된 개인화; 자동 타깃팅
seo-description: Adobe Target에서 자동화된 개인화 (AP) 또는 자동 타겟 활동을 만드는 동안 컨트롤로 사용할 경험을 선택합니다.
seo-title: Adobe Target의 제어로 특정 경험 사용
solution: Target,Analytics
title: 특정 경험을 제어로 사용
uuid: c67901d2-19cd-47d3-b8c4-abdcb046f404
translation-type: tm+mt
source-git-commit: add895d353e7483dfcbe82f1bca55b277bc65f20

---


# ![PREMIUM](/help/assets/premium.png) 자동화된 개인화 또는 자동 타겟 활동에 대한 제어 선택

You can select a randomly served experience or a specific experience to be used as control while creating an [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT) activity.

이 기능을 사용하면 활동에 구성된 트래픽 할당 비율에 따라 관련 경험으로 트래픽을 라우팅할 수 있습니다. 그런 다음 해당 컨트롤에 대한 제어 트래픽을 기준으로 개인화된 트래픽의 성능 보고서를 평가할 수 있습니다.

AP 및 활동에서 컨트롤을 설정하는 옵션은 다른 활동 유형과 약간 다릅니다. 수동 A/B 테스트에서는 보고로 표시되는 보고를 변경할 수 있으며, 향상도는 해당 제어 경험의 전환율을 기준으로 계산됩니다. 제어가 초기에 설정되었는지에 관계없이 활동에 포함된 각 경험에 임의로 트래픽이 제공되므로 이 변경 사항을 쉽게 만들 수 있습니다. 즉, 컨트롤을 선택하는 것은 트래픽이 처리되는 방식에 영향을 주지 않습니다. AP 및 활동에서 제어로 선택할 대상에 대한 결정은 방문자 트래픽이 처리되는 방식에 영향을 줍니다. 따라서 의사 결정을 보다 신중하게 내려야 합니다.

AP 및 활동에서 제어할 수 있는 옵션은 두 가지가 있습니다. 임의로 제공되는 경험 또는 특정 경험.

* **임의로 제공**: 무작위 제어를 위해 트래픽의 제어 비율은 방문자의 프로필을 고려하지 않고 활동의 모든 경험을 임의로 제공합니다. &quot; 방문자에게 경험 (또는 오퍼) 를 임의로 제공하고 방문자의 프로필을 고려하지 않은 경우 해당 경험 (또는 오퍼) 에 대한 전환율은 얼마인지 &quot;질문에 대답하는 것으로 생각할 수 있습니다. » 컨트롤은 AI 활동 내 A/B 테스트와 같습니다. 각 경험이나 오퍼에 대해 개인화되지 않은 전환율에 대한 이러한 정보를 알고 있으면 활동 결과를 분석할 때 이해하는 데 도움이 될 수 있습니다.

* **특정 경험**: 특정 경험 컨트롤을 사용하면 Target의 개인화 모델에서 제공하는 트래픽을 특정 마케터 정의된 경험 (예: 기본 홈 페이지) 와 비교할 수 있습니다. 이 옵션을 사용하면 트래픽의 제어 비율이 해당 한 경험에만 트래픽을 임의로 제공합니다.

## 특정 경험을 제어로 지정

1. [AP 활동](/help/c-activities/t-automated-personalization/create-ap-activity.md) 또는 [활동에서](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)원하는 대로 경험을 구성합니다.
1. [!UICONTROL 타깃팅] 페이지 (3 부분으로 구성된 안내 워크플로우 중 2 단계) 에서 원하는 경험을 컨트롤로 선택합니다.
1. 제어 경험과 다른 경험에 대해 원하는 트래픽 할당을 지정합니다.

   특정 경험 컨트롤의 경우 10% ~ 30%가 권장됩니다.

1. [!UICONTROL 목표 및 설정] 페이지에서 계속합니다.

## 알려진 제한 사항 및 고려 사항

특정 경험을 제어로 사용할 때는 다음 사항을 염두에 두십시오.

* 이미 라이브 활동에서 제어 경험을 변경하는 것은 권장되지 않습니다. 선택한 최신 제어 환경은 보고에서 이름이 지정됩니다 (이전 보고서가 다른 경험을 기반으로 하는 경우에도).
* 제어 환경 삭제는 권장되지 않습니다.
* 컨트롤이 권장되지 않으므로 다양한 새 오퍼/경험을 특정 경험으로 라이브 활동에 추가할 수 있습니다.
* AP 활동에서, 해당 경험을 볼 수 없는 사람을 더 제한할 수 있는 제어 경험에 대한 타깃팅을 포함합니다.
* In AP activities, lift and confidence information is *NOT* available in the offer-level report if a specific experience is selected. 향상도 및 신뢰도 정보는 AP 활동에 대한 전반적인 &quot;타깃팅된&quot; 및 &quot;제어&quot; 트래픽 수준에서 사용할 수 있습니다. &quot; 임의 &quot;가 컨트롤로 선택되면 향상도 및 신뢰도 정보를 사용할 수 있습니다. 이러한 차이는 특정 경험의 전환율과 오퍼의 전환율이 판매량의 차이로 인한 논리적이지 않기 때문입니다. AT activity available in an same, no matter of control is selected type of control is selected.
* 모든 제어 트래픽은 제어 경험을 선택할 때 단일 경험으로 전환되므로 (무작위와 비교할 때 경험의 수 또는 활동의 오퍼에 대해 제어 트래픽 양이 분할되는 무작위와 비교) 일반적으로 트래픽에는 많은 트래픽이 필요하지 않습니다. 10%는 시작할 수 있는 좋은 장소입니다.
* 특정 경험을 제어로 사용하여 라이브 활동에 다음 중 하나를 수행하면 컨트롤은 이전에 선택한 특정 경험 대신 임의로 제공된 경험으로 자동 재설정됩니다.

   * 경험 삭제
   * 위치 또는 오퍼 제거 (AP만 해당)
   * 중복 오퍼 제거 또는 제외 그룹 (AP만 해당) 를 통해 수동으로 경험 제외

