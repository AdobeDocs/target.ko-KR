---
keywords: faq;frequently asked questions;analytics for target;a4T;report;reports;view reports;reporting;counting methodology;impressions;visitors;visits;default metric;activity conversions;unspecified
description: 이 주제에서는 Analytics를 Target의 보고 소스로 사용(A4T)할 때의 보고서 보기에 대한 FAQ 답변을 제공합니다.
title: 보고서 보기 - A4T FAQ
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 7ad57c6f3814140df0826f57d8052f6db3fda301
workflow-type: tm+mt
source-wordcount: '2196'
ht-degree: 55%

---


# 보고서 보기 - A4T FAQ

This topic contains answers to questions that are frequently asked about viewing reports when using [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

## Can I view my Target activity data in Analysis Workspace? {#workspace}

활동 및 경험 [!DNL Analysis Workspace] 을 분석하는 데 사용할 수 [!DNL Target] 있습니다. Target용 [분석 패널에서는](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) 최대 3개의 성공 지표에 대한 상승도와 신뢰도를 볼 수 있습니다. 표 및 시각화를 사용하여 더 깊이 이해할 수도 있습니다.

For detailed information and examples, open the [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), provided by Adobe Experience League.

## Analysis Workspace에서 세그먼트를 적용할 수 있는 위치 {#segmentation}

세그먼트는 일반적으로 세그먼트 드롭 영역의 패널 맨 위에 적용됩니다. 세그먼트는 패널의 모든 테이블 및 시각화에 적용됩니다. 이 기술은 테스트가 사용자 하위 집합에 어떤 영향을 주는지 확인하는 데 가장 유용합니다(예: 이 테스트가 영국의 사용자에 대해 어떻게 수행되었습니까).

## 특정 Target 활동에 대해 히트 세그먼트를 적용할 때 반환되는 관련 없는 경험이 표시되는 이유는 무엇입니까? {#activity-segmentation}

[!DNL Target]에 보내진 [!DNL Analytics] 변수에는 기본 90일 만료 기간이 있습니다. (참고:필요한 경우 고객 지원 센터에서 이 만료 기간을 조정할 수 있습니다.) 방문자가 이 만료 기간 동안 사이트를 탐색하면 많은 [!DNL Target] 활동의 일부이며 이 모든 활동이 차원에서 수집됩니다.

따라서 히트에 나타낼 활동을 세그먼트화하면 해당 활동의 일부인 모든 경험과 해당 히트에 지속적인 다른 경험 *을* 얻게 됩니다.

## 방문자, 방문 또는 활동 노출 수를 표준화 지표(예: 계산 방법)로 사용해야 합니까? {#metrics}

A4T 보고에서 지표를 표준화하기 위한 몇 가지 옵션이 있습니다. 계산 방법이라고도 하는 이 지표는 리프트 계산의 분모가 됩니다. 이것은 신뢰도 계산이 적용되기 전에 데이터가 종합되는 방식에도 영향을 줍니다.

* ***고유 방문자 수***: 사용자가 처음으로 활동 자격을 확보할 때 증가합니다.
* ***방문 수***: 사용자(고유 방문자)가 활동에 참여하면 각 세션마다 증가하며, 이후 방문 시 활동이 조회되지 않더라도 마찬가지입니다.
* ***활동 노출 수***: 활동 컨텐츠가 제공될 때마다 증가합니다. (측정자 [!DNL Target]).

방문자가 활동을 포함하는 페이지를 볼 때 해당 활동의 이름을 포함하는 방문자에 대해 변수가 설정됩니다. 각 계산 방법이 비교하는 방식에 대한 내용은 아래에서 자세한 시나리오를 참조하십시오.

다음 사항을 고려하십시오.

* All of the above metrics trigger when a user qualifies for an activity and content is returned from [!DNL [!DNL Target]]. 이는 사용자가 반드시 오퍼를 보았다는 것을 의미하지는 않습니다. 활동 경험이 스크롤해야 볼 수 있는 부분에 있고 사용자가 페이지를 아래로 스크롤하지 않는 경우 [!DNL Target]에서 오퍼를 제공했지만 사용자는 볼 수 없습니다.
* 동일한 활동의 동일한 페이지에 여러 개의 mbox 호출이 있는 경우가 아니라면 [!UICONTROL 활동 노출 수]([!DNL Target]으로 측정) 및 [!UICONTROL 인스턴스 수]([!DNL Analytics]로 측정)는 동일합니다. 이로 인해 다중 [!UICONTROL 활동 노출 수]가 계산되지만, 인스턴스의 경우 단일 [!UICONTROL 인스턴스]만 계산됩니다.

## Analysis Workspace에서 보고 및 분석보다 &quot;활동 노출&quot; 및 &quot;활동 전환&quot;이 높은 이유는 무엇입니까? {#sametouch}

[!DNL Reports & Analytics] 동일한 터치 속성 모델을 &quot;활동 노출 횟수&quot; 및 &quot;활동 전환&quot;에 적용하는 반면, 차원 지속성 [!DNL Analysis Workspace] 으로 부풀려질 수 있는 원시 지표를 [!DNL Target] 표시합니다.

To evaluate accurate [!UICONTROL Activity Impressions] and [!UICONTROL Activity Conversions] metrics in [!DNL Analysis Workspace], ensure that both metrics have [!UICONTROL Same Touch] attribution models applied. 열 설정 톱니바퀴를 클릭하고, [!UICONTROL 기본값이 아닌 속성 모델]을 활성화한 다음 [!UICONTROL Same Touch]를 선택하여 모델을 적용할 수 있습니다. Analytics 도구 안내서의 [속성 IQ 개요에서](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html) 속성에 대한 *자세한 내용을 살펴보십시오*.

## 마케터가 활동을 설정할 때 Analytics 지표를 선택하는 경우 &quot;활동 전환&quot;은 무엇을 의미합니까? {#section_F3EBACF85AF846E9B366A549AAB64356}

&quot;Activity conversions&quot; will be empty if an [!DNL Analytics] metric was selected as the conversion metric for the activity.

## Analytics 보고서에서 &quot;지정되지 않음&quot;이 표시되는 이유는 무엇이며 어떤 의미입니까? {#unspecified}

기타 보고서에서 &quot;지정되지 않음&quot;은 데이터가 분류 규칙과 일치하지 않음을 의미하지만 A4T에서는 그렇지 않습니다. &quot;지정되지 않음&quot;이 표시되는 경우 분류 서비스가 아직 실행되지 않은 것입니다. 활동 데이터가 보고서에 표시되려면 일반적으로 24~72시간이 걸립니다. 이 시간까지 보고서에 활동 데이터가 표시되지 않더라도 해당 활동과 연관된 모든 방문자 데이터는 캡처되며 분류가 완료되면 표시됩니다.

분류 기간 후에 데이터는 웹 사이트에서 수집되고 약 1시간 후에 보고서에 표시됩니다. 보고서에 있는 모든 지표, 세그먼트, 값은 활동을 설정할 때 선택한 보고서 세트에서 가져옵니다.

## 활동이 비활성화된 후에도 Target 지표를 Analytics에 보내는 이유는 무엇입니까? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

[!DNL Target]에 보내진 [!DNL Analytics] 변수에는 기본 90일 만료 기간이 있습니다. 필요한 경우 고객 지원 센터에서 이 만료 기간을 조정할 수 있습니다. 이 설정값은 모든 활동에 적용되지만 하나의 사례에 맞게 조정하지 않아야 합니다.

You might see [!DNL Target] variables sent to [!DNL Analytics] after the expiration period because the expiration is 90 days, but only if that user never sees another A4T-enabled [!DNL Target] activity. 사용자가 45일 째 되는 날 사이트를 재방문하여 다른 활동을 보는 경우에는 전체 A4T eVar 값의 카운터가 90일로 재설정됩니다. 즉, 이제 첫 번째 날의 첫 번째 캠페인은 최대 45 + 90 = 135일 동안 지속할 수 있습니다. If the user keeps coming back, you might get to the point where you see metrics sent to [!DNL Analytics] in your reporting from much older activities. 사용자가 쿠키를 삭제하고 사이트로 돌아가지 않으면 해당 활동에 있는 숫자들은 삭제되지만 여전히 표시됩니다.

이것은 활동이 활성 상태인 동안 활동의 일부가 된 방문자의 경우 활동이 끝난 후 최대 90일 동안은 활동이 페이지 보기 횟수, 방문 횟수 등을 계속 얻게 됨을 의미합니다. 그러나 [!UICONTROL 활동 노출 횟수] 지표를 보는 경우 활동이 끝난 후에는 노출 횟수가 표시되지 않아야 합니다.

이것은 정상적이고 예상되는 행동입니다. A4T 변수의 값은 다른 eVar처럼 만료 기간(90일)이 될 때까지 사용자와 연결되어 있습니다. 결과적으로, 활동이 2주 동안만 활성 상태인 경우 이 값은 적어도 그 이후 90일 동안은 사용자와 여전히 연결됩니다.

활동이 라이브 상태인 기간 동안만 해당 활동에 대한 보고서를 보는 것이 좋습니다. The dates should be set correctly by default when you view the activity in [!DNL Analytics], so unless you have manually extended the date this shouldn’t be an issue from a reporting standpoint.

한 예로, A4T 변수가 90일 후에 만료되고 테스트는 1월 1일부터 1월 15일까지 활성 상태라고 가정해 보겠습니다.

1월 1일에 사용자가 사이트를 방문하여 활동 XYZ를 한 번 보고 그 뒤에 5개의 페이지 보기를 생성합니다. 다음 2주 동안 사용자는 사이트를 재방문하지 않습니다. 이 사용자에 대한 데이터는 다음과 같습니다.

| 활동 이름 | 인스턴스(노출 횟수) | 페이지 보기 횟수 | 방문 횟수 | 고유 방문자 수 |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

사용자가 2월 1일에 재방문하여 5개의 페이지를 더 보았지만, Target 활동은 더 이상 보지 않았고, 원래 활동도 더 이상 활성 상태가 아닙니다. 활동은 더 이상 활성 상태가 아니지만 eVar 지속성을 통해 여전히 사용자를 따라 가고 있습니다. 이제 데이터는 다음과 같습니다.

| 활동 이름 | 인스턴스(노출 횟수) | 페이지 보기 횟수 | 방문 횟수 | 고유 방문자 수 |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

사용자가 3월 1일에 다시 돌아와서 새 활동인 ABC를 봅니다. 사용자는 또 다섯 페이지를 봅니다. 활동 XYZ가 여전히 지속성을 통해 사용자를 따라가고 있으며 이 사용자에게 ABC 세트가 생기고 보고에 두 개의 라인 항목이 표시됩니다.

| 활동 이름 | 인스턴스(노출 횟수) | 페이지 보기 횟수 | 방문 횟수 | 고유 방문자 수 |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

그런 다음, 사용자는 4월 1일에 다시 돌아와서 다른 5개의 페이지를 보고 구매를 수행합니다. 첫 번째 eVar 값의 90일 만료가 4월 1일에 재설정되므로 보고에서 확인할 수 있습니다. 그리고 사용자에게 표시되는 모든 Target 활동이 전환 크레딧을 받지만 총 전환 수는 중복이 제거되어 계산됩니다.

| 활동 이름 | 인스턴스(노출 횟수) | 페이지 보기 횟수 | 방문 횟수 | 고유 방문자 수 | 주문 |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| 합계 | 2 | 20 | 3 | 1 | 1 |

전환 전에 두 경험을 모두 보았으므로 두 경험 모두 주문에 대한 &quot;크레딧&quot;을 받습니다. 그러나 주문은 시스템에서 하나만 발생했고 합계에 이렇게 반영됩니다. For [!DNL Target] reporting, because you aren’t putting a [!DNL Target] activity against another activity to see which is more successful, it doesn’t matter that all activities the user saw got credit. 지금은 단일 활동 내 두 항목의 결과를 비교하고 있으며, 사용자는 동일한 활동에서 서로 다른 경험을 확인할 수 없으므로 주문 크레딧의 교차 오염에 대해 걱정할 필요가 없습니다.

For more information, see [Conversion Variables (eVar](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)) in the *Analytics Admin Guide*.

## Analytics와 Analytics for Target(A4T)에서 고유 방문자 수 지표에 대해 숫자를 서로 다르게 계산하는 이유는 무엇입니까? {#section_0C3B648AB54041F9A2AA839D51791883}

학생 t 검증(t-test)(신뢰도 지표)을 사용하여 테스트 승자를 선택하는 A/B 테스트를 실행하는 경우, 여러 가지 가정 중 하나는 고정된 기간이 있는 것으로 가정합니다. 고정된 샘플 크기를 살펴보고 있는 것이 아니라면 테스트는 통계적으로 유효하지 않습니다.

The [!UICONTROL Unique Visitors] metric is different in [!DNL Analytics] and [!DNL Target] only when you are looking at a period of time that is shorter than the actual test. 샘플 크기에 도달하지 않은 경우에는 테스트를 신뢰할 수 없습니다. 자세한 내용은 [Evan Miller의 웹 사이트](https://www.evanmiller.org/index.html)에서 [How Not to Run an A/B Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html)(A/B 테스트를 실행하지 않는 방법)를 참조하십시오.

The [!UICONTROL Unique Visitors] metric displays the number of people who have been exposed to the test who have visited the site during the specified time period. 이 사람들은 여전히 테스트의 일부이므로 반드시 카운트해야 합니다. 한 주 동안 노출된 사용자 수만 보려는 경우, 활동 노출이 있는 방문자 세그먼트를 만들어 보고서에 적용할 수 있습니다.

You can shorten the amount of time the [!DNL Target] variable persists down to a session; however, that is usually problematic for tests where the conversion event isn’t as likely to happen within the same session.

## 동일한 방문자가 때로 Analytics의 여러 경험에서 카운트되는 이유는 무엇입니까? {#section_1397E972D31C4207A142E4D2D6D794A2}

The following list explains reasons why the same visitor could be counted in multiple experiences in [!DNL Analytics]:

* The [!DNL Target] profile expired but the [!DNL Analytics] cookie is still there. In this situation, [!DNL Target] re-evaluates the user but [!DNL Analytics] considers the visitor to be the same person.
* If the visitor is using the `mbox3rdPartyId`, when the anonymous visitor is merged with his or her 3rd-party ID profile, [!DNL Target] could put the visitor into a different experience to match up with the 3rd-party ID. 자세한 내용은 [mbox3rdPartyID에 대한 실시간 프로필 동기화](/help/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732)를 참조하십시오.
* [!DNL Analytics] 는 이러한 장치를 추적하는 방법과 다른 방법으로 동일한 방문자와 다른 장치를 [!DNL Target] 추적할 수 있습니다.의 타사 ID 설정 [!DNL Target] 은 Analytics와 다릅니다.

## A4T가 가상 보고서 세트를 지원합니까?

가상 보고서 세트는 보고서 세트 목록에 포함되지 *않으며*, 가상 보고서 세트의 대상은 A4T 보고에서 지원되지 않습니다.

## 활동이 활성화된 후 A4T를 사용하는 활동에서 트래픽 할당 비율을 변경할 수 있습니까?

Changing the traffic allocation percentage in an activity after activation can cause inconsistent reporting in [!DNL Analytics] because the change impacts only new visitors. 재방문자는 영향을 받지 않습니다.

활성화 이후 비율을 변경하는 대신 기존 활동을 중지한 다음 새 활동을 만드는 것이 우수 사례로 권장됩니다. 새 활동에 대한 보고는 새 방문자로 시작되며, 재방문자의 데이터로 인해 일관되지 않은 보고 문제가 발생하지는 않습니다.

## A4T를 사용하는 자동 Target 활동에서 Analytics와 전환 크레딧에서 어떻게 방문이 계산됩니까?

방문자가 자격을 얻거나, 컨텐츠를 보거나, A4T 활동을 통해 전환할 때 [!DNL Target] 이벤트 데이터를 로 보내 [!DNL Analytics]페이지에서 발생하는 전환 이벤트 및 기타 클릭 스트림 이벤트를 관련 [!DNL Analytics] [!DNL Target] 활동 및 경험으로 연결할 수 있습니다.

보고서를 볼 때 주의해야 할 몇 가지 [!DNL Analytics] 사항이 있습니다.

* 일반적으로 보고 창은 항상 활동의 시작 날짜부터 시작해야 합니다.
* 보고서 창 밖에서 전환이 발생하면 전환이 표시되지 않습니다 [!DNL Analytics].
* 자동 [!UICONTROL Target] 활동에 대한 트래픽의 &quot;타깃팅된&quot; 부분에서 방문자는 한 세션과 다른 경험을 볼 수 있습니다. 예를 들어, 방문자의 프로필 또는 컨텍스트가 변경되었으며 [!DNL Target]기계 학습 알고리즘은 새 경험에서 전환할 가능성이 더 높다고 판단합니다. 이것은 경험이 방문 간에 방문자에게 고정되는 일반적인 A/B 테스트 활동과 다릅니다.
* 방문자가 방문 간에 여러 경험을 보는 경우 모든 전환은 방문자가 마지막으로 본 경험으로 항상 귀속됩니다.하지만 방문 카운트는 방문자가 본 각 경험에 대해 증가합니다. 이렇게 하면 보고서에서 &quot;타깃팅된&quot; 차원 아래의 경험을 볼 때 경험당 전환율을 인위적으로 낮출 수 [!DNL Adobe Analytics] 있습니다.
