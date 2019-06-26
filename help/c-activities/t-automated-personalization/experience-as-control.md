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


# ![프리미엄](/help/assets/premium.png) 특정 경험을 제어로 사용

[자동화된 개인화](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) 또는 [자동 타겟](/help/c-activities/auto-target-to-optimize.md) (AT) 활동을 만드는 동안 컨트롤로 사용할 경험을 선택할 수 있습니다.

이 기능을 사용하면 활동에 구성된 트래픽 할당 비율에 따라 전체 제어 트래픽을 특정 경험으로 라우팅할 수 있습니다. 그런 다음 해당 경험의 제어 트래픽에 대한 개인화된 트래픽의 성능 보고서를 평가할 수 있습니다.

경험을 임의로 제공하는 제어 옵션도 사용할 수 있습니다.

특정 경험을 제어로 사용함으로써 보고서가 &quot;AP/활동 실행 대신 더 나은 작업 실행&quot; 이라는 질문에 답하는 데 도움이 될 수 있습니다. AP/AT 활동의 이점은 모든 사용자에게 전달하는 것이 적합하지 않을 수 있는 더 많은 옵션을 만들 수 있지만, 올바른 사용자에게 강력할 수 있다는 것입니다. 그러나 이는 알고리즘을 무작위와 비교하는 것이 아니라 사이트에서 모든 방문자에게 모든 옵션을 실행할 수 없습니다.

## 특정 경험을 제어로 지정

1. [AP 활동](/help/c-activities/t-automated-personalization/create-ap-activity.md) 또는 [활동에서](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)원하는 대로 경험을 구성합니다.
1. [!UICONTROL 타깃팅] 페이지 (3 부분으로 구성된 안내 워크플로우 중 2 단계) 에서 원하는 경험을 컨트롤로 선택합니다.
1. 제어 경험과 다른 경험에 대해 원하는 트래픽 할당을 지정합니다.
1. [!UICONTROL 목표 및 설정] 페이지에서 계속합니다.

## 알려진 제한 사항

다음은 특정 경험을 제어로 사용하는 경우 알려진 제한 사항입니다.

* 이미 라이브 활동에서 제어 경험을 변경하는 것은 권장되지 않습니다. 선택한 최신 제어 환경은 보고에서 이름이 지정됩니다 (이전 보고서가 다른 경험을 기반으로 하는 경우에도).
* 제어 환경 삭제는 권장되지 않습니다.
* 컨트롤 경험에 대한 타깃팅을 포함한 AP 활동에서는 해당 경험을 볼 수 있는 사람을 더 이상 제한할 수 없습니다.
* In AP activities, lift and confidence information is *NOT* available in the offer-level report if a specific experience is selected. &quot; 임의 &quot;가 컨트롤로 선택되면 향상도 및 신뢰도 정보를 사용할 수 있습니다.

   Lift and confidence information *is* available at the overall &quot;targeted&quot; vs. &quot;control&quot; traffic level for the activity. 이러한 차이는 특정 경험의 전환율과 오퍼의 전환율이 판매량의 차이로 인한 논리적이지 않기 때문입니다.

## 문제 해결

문제가 발생하면 다음 문제 해결 팁을 고려하십시오.

* 모든 제어 트래픽은 제어 경험을 선택할 때 단일 경험으로 전환되므로 (무작위와 비교할 때 경험 수가 경험의 경험/오퍼 수로 분할되는 무작위와 비교) 일반적으로 트래픽에는 많은 트래픽이 필요하지 않습니다. 10%는 시작할 수 있는 좋은 장소입니다.
* 라이브 활동에 다음 중 하나를 수행하면 컨트롤은 이전에 선택한 특정 경험 대신 임의로 제공된 경험으로 자동 재설정됩니다.

   * 경험 삭제
   * 위치 또는 오퍼 제거 (AP만 해당)
   * 중복 오퍼 제거 또는 제외 그룹 (AP만 해당) 를 통해 수동으로 경험 제외
