---
keywords: 경험;제어;자동화된 개인화;자동 타겟
description: ' [!DNL Adobe Target]에서 [!UICONTROL Automated Personalization](AP) 또는 [!UICONTROL Auto-Target] 활동을 만드는 동안 컨트롤로 사용할 환경을 선택하는 방법을 알아봅니다.'
title: '[!UICONTROL Automated Personalization] 활동에서 특정 경험을 제어로 사용하려면 어떻게 해야 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 42%

---

# [!UICONTROL Automated Personalization] 또는 [!UICONTROL Auto-Target] 활동에 대한 컨트롤 선택

AP([[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md)) 또는 AT([[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)) 활동을 만드는 동안 제어로 사용할 특정 경험이나 임의로 제공된 경험을 선택할 수 있습니다.

이 기능을 사용하면 활동에 구성된 트래픽 할당 비율에 따라 제어 트래픽을 관련 경험으로 라우팅할 수 있습니다. 그런 다음 해당 제어의 제어 트래픽에 대해 개인화된 트래픽의 성능 보고서를 평가할 수 있습니다.

[!UICONTROL Automated Personalization] 및 [!UICONTROL Auto-Target] 활동에서 컨트롤을 설정하는 옵션이 다른 활동 유형과 약간 다릅니다. 수동 [!UICONTROL A/B Test]에서 제어로 표시되는 보고를 변경할 수 있으며, 해당 제어 경험의 전환율을 기준으로 상승도가 계산됩니다. 트래픽은 초기에 설정되는 제어에 관계없이 활동에 포함한 각 경험에 임의로 처리되므로 이를 쉽게 변경할 수 있습니다. 즉, 컨트롤을 선택해도 트래픽 처리 방식에는 영향을 주지 않습니다. [!UICONTROL Automated Personalization] 및 [!UICONTROL Auto-Target] 활동에서 제어로 선택할 대상에 대한 결정은 방문자 트래픽이 제공되는 방식에 영향을 줍니다. 결과적으로, 여러분은 여러분의 결정에 대해 더 신중하게 생각해야 합니다.

[!UICONTROL Automated Personalization] 및 [!UICONTROL Auto-Target] 활동에서 컨트롤에 사용할 수 있는 두 가지 옵션이 있습니다.

* **임의로 제공되는 경험**: 임의 제어의 경우 트래픽 제어 비율은 해당 방문자의 프로필을 고려하지 않고 활동의 모든 경험을 임의로 제공합니다. 질문 &quot;방문자에게 경험(또는 오퍼)을 임의로 제공하고 방문자의 프로필을 고려하지 않은 경우 해당 경험(또는 오퍼)에 대한 전환율은 어떻게 됩니까?&quot;에 대한 답변으로 제어를 생각할 수 있습니다. 컨트롤은 AI 활동 내의 [!UICONTROL A/B Test]과(와) 같습니다. 각 경험이나 오퍼에 대해 개인화되지 않은 전환율에 대한 이러한 정보를 알고 있으면 활동 결과를 분석할 때 이해하는 데 도움이 될 수 있습니다.

* **특정 경험**: 특정 경험 제어를 사용하면 [!DNL Target] 개인화 모델에서 제공하는 트래픽을 특정 마케터가 정의한 경험(예: 기본 홈 페이지)과 비교할 수 있습니다. 이 옵션을 사용하면 트래픽의 제어 비율이 해당하는 한 개 경험에 대해서만 트래픽을 임의로 처리합니다.

## 특정 경험을 제어로 지정

1. [[!UICONTROL Automated Personalization] 활동](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) 또는 [[!UICONTROL Auto-Target] 활동](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)을 만들거나 편집하는 동안 필요에 따라 경험을 구성하십시오.
1. [!UICONTROL Targeting] 페이지(3단계 안내 워크플로의 2단계)에서 원하는 경험을 제어로 선택합니다.
1. 제어 경험과 다른 경험에 대해 원하는 트래픽 할당을 지정합니다.

   특정 경험 컨트롤의 경우 10%~30%가 권장됩니다.

1. [!UICONTROL Goals & Settings] 페이지로 계속합니다.

## 알려진 제한 사항 및 고려 사항

특정 경험을 제어로 사용할 때는 다음 사항을 염두에 두십시오.

* 라이브 활동에서 제어 경험을 변경하는 것은 권장되지 않습니다. 선택한 최신 제어 경험은 보고 시 이름이 지정됩니다(이전 보고서가 다른 경험을 기반으로 하는 경우에도).
* 제어 경험은 삭제하지 않는 것이 좋습니다.
* 특정 경험이 있는 라이브 활동에 제어로 많은 새 오퍼 또는 경험을 추가하는 것은 권장되지 않습니다.
* [!UICONTROL Automated Personalization] 활동에서는 해당 경험을 볼 수 있는 사람을 추가로 제한할 수 있는 제어 경험에 타깃팅을 포함하는 것은 권장되지 않습니다.
* [!UICONTROL Automated Personalization] 활동에서 특정 경험을 선택한 경우 상승도 및 신뢰도 정보는 오퍼 수준 보고서에서 *사용할 수 없음*&#x200B;입니다. 상승도 및 신뢰도 정보는 [!UICONTROL Automated Personalization] 활동에 대한 전체 &quot;타깃팅된&quot; 트래픽 수준과 &quot;제어&quot; 트래픽 수준에서 사용할 수 있습니다. 임의가 컨트롤로 선택된 경우 상승도 및 신뢰도 정보를 사용할 수 있습니다. 이러한 차이는 특정 경험의 전환율과 오퍼의 전환율을 비교하는 것은 단위의 차이로 인해 논리적이지 않기 때문입니다. 선택한 제어 유형에 관계없이 [!UICONTROL Auto-Target] 활동에서 사용할 수 있는 정보는 동일합니다.
* 모든 제어 트래픽은 제어로 경험을 선택할 때 단일 경험 또는 오퍼 세트로 전환되므로(제어 트래픽 양이 활동의 경험 또는 오퍼 수로 분할되는 임의에 비해) 일반적으로 제어로 유입되는 트래픽이 많이 필요하지 않습니다. 10%는 시작하기에 좋은 장소입니다.
* 특정 경험이 있는 라이브 활동에 다음 중 하나를 제어로 수행하면 제어가 이전에 선택한 특정 경험 대신 임의로 제공된 경험으로 자동 재설정됩니다.

   * 경험 삭제
   * 위치 또는 오퍼 제거([!UICONTROL Automated Personalization]만)
   * 중복 오퍼 제거 또는 제외 그룹([!UICONTROL Automated Personalization]만 해당)을 통해 경험을 수동으로 제외
