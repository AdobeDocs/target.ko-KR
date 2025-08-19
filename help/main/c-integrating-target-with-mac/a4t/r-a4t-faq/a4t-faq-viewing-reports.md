---
keywords: faq;자주 묻는 질문;analytics for target;a4T;보고서;보고서;보고서 보기;보고;계산 방법론;노출 횟수;방문자 수;방문 횟수;기본 지표;활동 전환;지정되지 않음
description: Analytics for [!DNL Target] (A4T)을(를) 사용할 때 보고서를 보는 것과 관련하여 자주 묻는 질문에 대한 답변을 찾아보십시오. A4T를 사용하면  [!DNL Target] 활동에 대한 Analytics 보고를 사용할 수 있습니다.
title: A4T를 사용하여 보고서를 보는 것과 관련된 질문에 대한 답변을 찾으시나요?
feature: Analytics for Target (A4T)
exl-id: a02eeb34-3975-424b-a046-e51f10ae1823
source-git-commit: c747a8a0ed480130f254818e21b98addca16ca41
workflow-type: tm+mt
source-wordcount: '2539'
ht-degree: 26%

---

# 보고서 보기 - A4T FAQ

이 주제에서는 [!DNL Adobe Analytics]을(를) [!DNL Adobe Target]의 보고 소스로 사용(A4T)할 때의 보고서 보기에 대한 FAQ 답변을 제공합니다.

## [!DNL Target]에서 내 [!DNL Analysis Workspace] 활동 데이터를 볼 수 있습니까? {#workspace}

+++답변
[!DNL Analysis Workspace]을(를) 사용하여 [!DNL Target] 활동 및 경험을 분석할 수 있습니다. [Analytics for Target 패널](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=ko-KR)을 사용하면 최대 3개의 성공 지표에 대한 상승도 및 신뢰도를 볼 수 있습니다. 표 및 시각화를 사용하여 더 깊이 파고들 수도 있습니다.

자세한 내용과 예를 보려면 [에서 제공하는 ](https://spark.adobe.com/page/Lo3Spm4oBOvwF/)Analytics &amp; Target: 분석 모범 사례 자습서[!UICONTROL Adobe Experience League]를 여십시오.

+++

## [!DNL Analysis Workspace]에서 세그먼트를 적용할 수 있는 위치는 어디입니까? {#segmentation}

+++답변
세그먼트는 세그먼트 드롭 영역의 패널 맨 위에서 가장 일반적으로 사용됩니다. 세그먼트는 패널의 모든 테이블 및 시각화에 적용됩니다. 이 기법은 테스트가 사람들의 하위 집합에 어떤 영향을 미치는지 확인하는 데 가장 유용합니다(예: 이 테스트는 영국의 사람들에 대해 어떻게 수행되었습니까?).

세그먼트는 자유 형식 테이블 내에서 직접 계층화할 수도 있지만 A4T 패널 내에서 상승도 및 신뢰도 계산을 유지하려면 전체 테이블에 오버레이해야 합니다. 열 수준 세그먼트는 현재 패널 내에서 지원되지 않습니다.

+++

## [!DNL Analysis Workspace]에서 사용되는 Attribution IQ 모델은 무엇입니까?

+++답변
[!DNL Target]에서 [!DNL Analysis Workspace]개의 활동 노출 및 전환을 사용할 때 정확한 계산을 위해 &quot;동일한 터치&quot; Attribution IQ 모델이 지표에 적용되는 기본 모델입니다. 이 모델은 99%의 경우 효과가 좋습니다. 그러나 Attribution IQ에서 이 표준 속성을 재정의할 수 있습니다.

+++

## 특정 [!DNL Target] 활동에 대해 히트 세그먼트를 적용하면 관련 없는 경험이 반환되는 이유는 무엇입니까? {#activity-segmentation}

+++답변
[!DNL Target]에 보내진 [!DNL Analytics] 변수에는 기본 90일 만료 기간이 있습니다. (참고: 이 만료 기간은 필요한 경우 고객 지원 센터에서 조정할 수 있습니다.) 방문자가 이 만료 창 전체에서 사이트를 탐색할 때 이 방문자는 많은 [!DNL Target] 활동에 속하며 이 모든 활동은 차원에서 수집됩니다.

히트에 있는 활동을 세그먼트화할 때 해당 활동에 속하는 모든 경험 *plus*&#x200B;을(를) 해당 히트에서 지속되는 다른 경험으로 가져옵니다.

+++

## 내 [!UICONTROL Goal Metrics]을(를) 구성하는 동안 [!UICONTROL Advanced Settings]에 액세스할 수 없는 이유는 무엇입니까?

+++답변
[!DNL Analytics]을(를) 보고 소스로 사용(A4T)하는 활동의 경우 목표 지표는 &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; 및 &quot;[!UICONTROL On Every Impression]&quot; 설정을 사용합니다. 이러한 설정은 *구성할 수 없습니다*.

자세한 내용은 &quot;목표 지표를 구성하는 동안 고급 설정 옵션에 액세스할 수 없는 이유는 무엇입니까?&quot;를 참조하십시오. [지표 정의 - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md)에서.

+++

## 방문자 수, 방문 횟수 또는 활동 노출 횟수를 표준화 지표(즉, 계산 방법론)로 사용해야 합니까? {#metrics}

+++답변
A4T 보고에는 지표를 표준화하는 몇 가지 옵션이 있습니다. 계산 방법론이라고도 하는 이 지표는 상승도 계산의 분모가 됩니다. 이것은 신뢰도 계산이 적용되기 전에 데이터가 종합되는 방식에도 영향을 줍니다.

* 사용자가 처음 활동 자격을 얻으면 ***고유 방문자 수***&#x200B;가 한 번 증가합니다.
* ***방문***&#x200B;은(는) 사용자(고유 방문자)가 활동을 시작하면 해당 활동이 후속 방문에서 보이지 않더라도 각 세션에 대해 증가합니다.
* ***활동 노출 수***&#x200B;는 활동 콘텐츠가 제공될 때마다 증가합니다. ([!DNL Target]&#x200B;(으)로 측정).

방문자가 활동을 포함하는 페이지를 볼 때 해당 활동의 이름을 포함하는 방문자에 대해 변수가 설정됩니다. 각 계산 방법이 비교하는 방식에 대한 내용은 아래에서 자세한 시나리오를 참조하십시오.

다음 사항을 고려하십시오.

* 사용자가 활동 자격을 확보하고 [!DNL Target]에서 콘텐츠가 반환될 때 위의 지표를 트리거합니다. 이는 사용자가 반드시 오퍼를 보았다는 것을 의미하지는 않습니다. 활동 경험이 스크롤해야 볼 수 있는 부분에 있고 사용자가 페이지를 아래로 스크롤하지 않는 경우 [!DNL Target]에서 오퍼를 제공했지만 사용자는 볼 수 없습니다.
* 동일한 활동의 동일한 페이지에 여러 개의 mbox 호출이 있는 경우가 아니라면 [!UICONTROL Activity Impressions]&#x200B;([!DNL Target]&#x200B;(으)로 측정) 및 [!UICONTROL Instances]&#x200B;([!DNL Analytics]&#x200B;(으)로 측정)은 같습니다. 이로 인해 여러 [!UICONTROL Activity Impressions]이(가) 계산되지만 단일 [!UICONTROL Instance]만 계산됩니다.

자세한 내용은 [Adobe Target 자습서](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=ko-KR)에서 *자동 타겟 활동을 위해 Analysis Workspace에서 A4T 보고서를 설정하는 방법*&#x200B;을 참조하십시오.

+++

## [!DNL Analysis Workspace]에서 [!UICONTROL Reports & Analytics]보다 &quot;활동 노출 수&quot; 및 &quot;활동 전환 수&quot;가 더 높은 이유는 무엇입니까? {#sametouch}

+++답변
[!DNL Reports & Analytics]은(는) &quot;활동 노출 수&quot; 및 &quot;활동 전환&quot;에 동일한 터치 속성 모델을 적용하지만 [!DNL Analysis Workspace]은(는) [!DNL Target] 차원의 지속성으로 인해 부풀려진 것처럼 보일 수 있는 원시 지표를 표시합니다.

[!UICONTROL Activity Impressions]에서 정확한 [!UICONTROL Activity Conversions] 및 [!DNL Analysis Workspace] 지표를 평가하려면 두 지표 모두에 [!UICONTROL Same Touch] 속성 모델이 적용되어 있는지 확인하십시오. 열 설정 톱니바퀴를 클릭하고 [!UICONTROL Non-default attribution models]을(를) 활성화한 다음 [!UICONTROL Same Touch]을(를) 선택하여 모델을 적용할 수 있습니다. [Analytics 도구 안내서](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/attribution.html)의 *특성 IQ 개요*&#x200B;에서 특성에 대해 자세히 알아보세요.

+++

## 마케터가 활동을 설정하는 동안 [!DNL Analytics] 지표를 선택하는 경우 &quot;활동 전환&quot;은 무엇을 의미합니까? {#section_F3EBACF85AF846E9B366A549AAB64356}

+++답변
[!DNL Analytics] 지표를 활동의 전환 지표로 선택한 경우 &quot;활동 전환&quot;이 비어 있습니다.

+++

## [!DNL Analytics] 보고서에 &quot;지정되지 않음&quot;이 표시되는 이유는 무엇입니까? 어떤 의미입니까? {#unspecified}

+++답변
기타 보고서에서 &quot;지정되지 않음&quot;은 데이터가 분류 규칙과 일치하지 않음을 의미하지만 A4T에서는 그렇지 않습니다. &quot;지정되지 않음&quot;이 표시되는 경우 분류 서비스가 아직 실행되지 않은 것입니다. 활동 데이터가 보고서에 표시되려면 일반적으로 24~72시간이 걸립니다. 이 시간까지 보고서에 활동 데이터가 표시되지 않더라도 해당 활동과 연관된 모든 방문자 데이터는 캡처되어 분류가 완료되면 표시됩니다.

분류 기간 후에 데이터는 웹 사이트에서 수집되고 약 1시간 후에 보고서에 표시됩니다. 보고서에 있는 모든 지표, 세그먼트, 값은 활동을 설정할 때 선택한 보고서 세트에서 가져옵니다.

해당 활동에 대해 분류가 수행되었으며 보고서에 여전히 &quot;지정되지 않음&quot; 행이 표시되는 경우 보고서에서 데이터를 표시하는 데 [!DNL Target]이(가) 아닌 지표를 사용하고 있지 않은지 확인하십시오. 보고서가 [!DNL Target]별 지표를 사용하지 않는 한 &quot;지정되지 않음&quot; 행에 [!DNL Target]과(와) 연결되지 않은 호출에 대한 이벤트가 포함되어 있습니다. 해당 행에는 [!DNL Target] 관련 정보(예: 방문자/방문 횟수/노출 횟수)가 포함되지 않습니다.

+++

## 활동이 비활성화된 후에도 [!DNL Target] 지표를 [!DNL Analytics]&#x200B;(으)로 보내는 이유는 무엇입니까? {#section_38AA8380A4D54A18972F1EF3E73E22EF}

+++답변
[!DNL Target]에 보내진 [!DNL Analytics] 변수에는 기본 90일 만료 기간이 있습니다. 이 만료 기간은 필요한 경우 고객 지원 센터에서 조정할 수 있습니다. 이 설정은 모든 활동에 대해 전역적입니다. 하지만 한 가지 경우에는 조정해서는 안 됩니다.

만료 기간이 90일이므로 만료 기간 후에 [!DNL Target]에 전송된 [!DNL Analytics]개의 변수가 표시될 수 있지만, 해당 사용자가 다른 A4T 사용 [!DNL Target] 활동을 보지 못하는 경우에만 표시됩니다. 사용자가 45일 째 되는 날 사이트를 재방문하여 다른 활동을 보는 경우에는 전체 A4T eVar 값의 카운터가 90일로 재설정됩니다. 즉, 이제 첫 번째 날의 첫 번째 캠페인은 최대 45 + 90 = 135일 동안 지속할 수 있습니다. 사용자가 계속 돌아오면 보고 시 이전 활동에서 [!DNL Analytics]에 전송된 지표를 볼 수 있는 지점에 도달할 수 있습니다. 사용자가 쿠키를 삭제하고 사이트로 돌아가지 않으면 해당 활동의 숫자는 감소하지만 여전히 볼 수 있습니다.

즉, 활동이 활성화된 동안 활동에 일부가 된 방문자에 대해 활동이 종료된 후 최대 90일 동안 활동이 페이지 보기 수, 방문 횟수 등을 계속 가져옵니다. 그러나 [!UICONTROL Activity Impressions] 지표를 보면 활동이 끝난 후 노출이 표시되지 않습니다.

이것은 정상적이고 예상되는 행동입니다. A4T 변수의 값은 다른 eVar처럼 만료 기간(90일)이 될 때까지 사용자와 연결되어 있습니다. 그 결과 활동이 2주 동안만 활성 상태인 경우, 해당 값은 적어도 다음 90일 동안 사용자와 계속 연결됩니다.

활동이 라이브 상태인 기간 동안만 해당 활동에 대한 보고서를 보는 것이 좋습니다. [!DNL Analytics]에서 활동을 볼 때는 기본적으로 날짜가 올바르게 설정되어야 하므로 날짜를 수동으로 연장하지 않은 경우 보고 관점에서 볼 때 문제가 되지 않습니다.

예를 들어 A4T 변수가 90일 후에 만료되고 테스트가 1월 1일부터 1월 15일까지 활성 상태라고 가정해 보겠습니다.

1월 1일에 사용자가 사이트를 방문하여 활동 XYZ를 한 번 보고 그 뒤에 5개의 페이지 보기를 생성합니다. 다음 2주 동안 사용자는 사이트를 재방문하지 않습니다. 이 사용자에 대한 데이터는 다음과 같습니다.

| 활동 이름 | 인스턴스(노출 횟수) | 페이지 보기 횟수 | 방문 횟수 | 고유 방문자 수 |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 5 | 1 | 1 |

사용자는 2월 1일에 돌아가서 5개의 페이지를 더 보고 더 이상 Target 활동이 발생하지 않으며, 원래 활동이 더 이상 활성화되지 않습니다. 활동은 더 이상 활성 상태가 아니지만 eVar 지속성을 통해 여전히 사용자를 따라 가고 있습니다. 이제 데이터는 다음과 같습니다.

| 활동 이름 | 인스턴스(노출 횟수) | 페이지 보기 횟수 | 방문 횟수 | 고유 방문자 수 |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 10 | 2 | 1 |

사용자가 3월 1일에 다시 돌아와서 새 활동인 ABC를 봅니다. 사용자는 또 다섯 페이지를 봅니다. 활동 XYZ가 지속성을 통해 사용자를 계속 팔로우하고 있으며 이 사용자에게는 ABC 세트가 있으므로 보고에서 두 개의 라인 항목이 표시됩니다.

| 활동 이름 | 인스턴스(노출 횟수) | 페이지 보기 횟수 | 방문 횟수 | 고유 방문자 수 |
|--- |--- |--- |--- |--- |
| XYZ | 1 | 15 | 3 | 1 |
| ABC | 1 | 5 | 1 | 1 |

그런 다음, 사용자는 4월 1일에 다시 돌아와서 다른 5개의 페이지를 보고 구매를 수행합니다. 첫 번째 eVar 값의 90일 만료가 4월 1일에 재설정되므로 보고에서 볼 수 있습니다. 그리고 사용자에게 표시되는 모든 Target 활동이 전환 크레딧을 받지만 총 전환 수는 중복이 제거되어 계산됩니다.

| 활동 이름 | 인스턴스(노출 횟수) | 페이지 보기 횟수 | 방문 횟수 | 고유 방문자 수 | 주문 |
|--- |--- |--- |--- |--- |--- |
| XYZ | 1 | 20 | 4 | 1 | 1 |
| ABC | 1 | 10 | 2 | 1 | 1 |
| 합계 | 2 | 20 | 3 | 1 | 1 |

두 경험 모두 전환 전에 표시되었기 때문에 두 경험 모두 주문에 대한 &quot;크레딧&quot;을 받습니다. 그러나 주문은 시스템에서 하나만 발생했고 합계에 이렇게 반영됩니다. [!DNL Target] 보고의 경우 다른 활동에 대해 [!DNL Target] 활동을 적용하여 어느 활동이 더 성공적인지 확인하지 않으므로 사용자가 본 모든 활동이 크레딧을 받은 것은 문제가 되지 않습니다. 단일 활동 내에 있는 두 항목의 결과를 비교하고 있습니다. 사용자가 동일한 활동에서 다른 경험을 볼 수 없으므로 주문 크레딧의 교차 오염에 대해 걱정할 필요가 없습니다.

자세한 내용은 [Analytics 관리 안내서](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/conversion-variables/conversion-var-admin.html)의 *전환 변수(eVar*)를 참조하십시오.

+++

## 내 활동이 비활성화된 후에 계속해서 더 많은 인상을 확인하는 이유가 무엇입니까? {#deactivated}

+++답변
비활성화 후 A4T 활동의 보고서에 대한 노출 횟수의 소스는 QA 모드 트래픽일 수 있습니다. Target은 일반적으로 비활성화된 활동에 대한 이벤트를 기록하지 않지만 Analytics에서는 QA 모드에서 노출 수가 증가하고 있음을 알 수 있는 방법이 없습니다. Analytics에서 Target 활동 보고서를 검색하면 다음 노출 수가 표시됩니다. 이는 고객이 QA 모드를 사용하여 활동이 활성화되지 않은 경우에도 A4T 보고서를 확인할 수 있는 방법이 필요하기 때문에 설계된 대로 작동합니다.

+++

## [!DNL Analytics] 및 [!UICONTROL Analytics for Adobe Target]&#x200B;(A4T)에서 [!UICONTROL Unique Visitors] 지표에 대한 숫자를 다르게 계산하는 이유는 무엇입니까? {#section_0C3B648AB54041F9A2AA839D51791883}

+++답변
[Welch의 t-test](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank}(신뢰도 지표)를 사용하여 테스트 승자를 선택하는 A/B 테스트를 실행할 때 가정 중 하나는 고정된 시간대가 있다는 것입니다. 고정된 샘플 크기를 확인하지 않는 한 테스트는 통계적으로 유효하지 않습니다.

[!UICONTROL Unique Visitors] 지표는 실제 테스트보다 짧은 기간을 보는 경우에만 [!DNL Analytics]과(와) [!DNL Target]에서 다릅니다. 샘플 크기에 도달하지 않은 경우 테스트를 신뢰할 수 없습니다. 자세한 내용은 [Evan Miller의 웹 사이트](https://www.evanmiller.org/index.html)에서 [How Not to Run an A/B Test](https://www.evanmiller.org/how-not-to-run-an-ab-test.html)&#x200B;(A/B 테스트를 실행하지 않는 방법)를 참조하십시오.

[!UICONTROL Unique Visitors] 지표는 지정된 기간 동안 사이트를 방문한 테스트에 노출된 사람 수를 표시합니다. 이 사람들은 시험의 일부이므로 계산되어야 합니다. 한 주 동안 노출된 사용자 수만 보려는 경우, 활동 노출이 있는 방문자 세그먼트를 만들어 보고서에 적용할 수 있습니다.

[!DNL Target] 변수가 세션까지 지속되는 시간을 줄일 수 있지만, 전환 이벤트가 동일한 세션 내에서 발생할 가능성이 없는 테스트에는 문제가 있습니다.

+++

## [!DNL Analytics]에서 같은 방문자가 여러 경험에서 가끔 계산되는 이유는 무엇입니까? {#section_1397E972D31C4207A142E4D2D6D794A2}

+++답변
다음 목록은 [!DNL Analytics]의 여러 경험에서 동일한 방문자를 계산할 수 있는 이유를 설명합니다.

* [!DNL Target] 프로필이 만료되었지만 [!DNL Analytics] 쿠키가 남아 있습니다. 이 경우 [!DNL Target]은(는) 사용자를 다시 평가하지만 [!DNL Analytics]은(는) 방문자를 동일한 사람으로 간주합니다.
* 방문자가 `mbox3rdPartyId`을(를) 사용하는 경우 익명의 방문자가 타사 ID 프로필과 병합되면 [!DNL Target]에서 방문자를 타사 ID에 해당하는 다른 경험으로 분류할 수 있습니다. 자세한 내용은 [mbox3rdPartyID에 대한 실시간 프로필 동기화](/help/main/c-target/c-visitor-profile/3rd-party-id.md#concept_BF4113593F614987B1D3E359AE1C5732)를 참조하십시오.
* [!DNL Analytics]은(는) [!DNL Target]이(가) 장치를 추적하는 것과 다른 방식으로 다른 장치를 동일한 방문자로 추적할 수 있습니다. [!DNL Target]의 타사 ID 설정은 Analytics와 다릅니다.

+++

## A4T가 가상 보고서 세트를 지원합니까? {#virtual}

+++답변
가상 보고서 세트가 [!UICONTROL Report Suite] 목록에 포함되지 않지만 [!DNL Analytics]의 가상 보고서 세트에 연결된 보고서 세트와 공유된 모든 A4T 데이터는 해당 데이터에 액세스할 수 있습니다. 가상 보고서 세트에서 만든 대상은 다시 [!DNL Target]에 공유할 수 없습니다.

+++

## 활동이 활성화된 후 A4T를 사용하는 활동에서 트래픽 할당 비율을 변경할 수 있습니까?

+++답변
활성화 후 활동에서 트래픽 할당 비율을 변경하면 변경 사항이 새 방문자에게만 영향을 주므로 [!DNL Analytics]에서 보고가 일관되지 않을 수 있습니다. 재방문자는 영향을 받지 않습니다.

활성화 이후 비율을 변경하는 대신 기존 활동을 중지한 다음 새 활동을 만드는 것이 우수 사례로 권장됩니다. 새 활동에 대한 보고는 새 방문자로 시작되며, 재방문자의 데이터로 인해 일관되지 않은 보고가 발생하지 않습니다.

+++

## A4T를 사용하는 [!DNL Analytics] 활동에서 할당된 [!UICONTROL Auto-Target] 및 전환 크레딧에서 방문 횟수는 어떻게 계산됩니까?

+++답변
방문자가 A4T 활동에서 자격을 얻거나, 콘텐츠를 보거나, 변환할 때 [!DNL Target]이(가) 이벤트 데이터를 [!DNL Analytics]&#x200B;(으)로 보냅니다. 이 이벤트 데이터를 사용하면 [!DNL Analytics]이(가) 페이지에서 발생하는 전환 이벤트와 기타 클릭스트림 이벤트를 관련 [!DNL Target] 활동 및 경험에 연결할 수 있습니다.

[!DNL Analytics] 보고서를 볼 때 몇 가지 유의해야 할 사항은 다음과 같습니다.

* 일반적으로 보고 기간은 활동의 시작 날짜부터 시작하는 것이 좋습니다.
* 보고서 창 외부에서 변환이 발생하면 해당 변환이 [!DNL Analytics]에 표시되지 않습니다.
* [!UICONTROL Auto-Target] 활동에 대한 트래픽의 &quot;타깃팅된&quot; 부분에 있으면 방문자가 한 세션에서 다음 세션까지 다른 경험을 볼 수 있습니다. 예를 들어, 프로필이나 컨텍스트가 변경되어 [!DNL Target]의 머신 러닝 알고리즘이 새 경험에서 전환할 가능성이 높다고 판단하는 경우, 방문자가 경험에서 경험으로 이동할 때 표시되는 각 경험에 대해 방문 횟수가 증가합니다. 이는 경험이 방문 간에 방문자에게 고정된 일반적인 A/B 테스트 활동과 다릅니다.
* 방문자가 방문 간에 여러 경험을 보는 경우 전환은 항상 방문자가 본 마지막 경험으로 귀속됩니다. 언급된 바와 같이, 방문 카운트는 방문자가 본 각 경험에 대해 증가합니다. 이렇게 하면 [!UICONTROL Targeted] 보고서에서 &quot;[!DNL Adobe Analytics]&quot; 차원에서 경험을 볼 때 경험당 전환율을 인위적으로 낮출 수 있습니다.

+++

## [!DNL Analysis Workspace]&#x200B;(A4T)을(를) 사용할 때 [!UICONTROL Analytics for Target]에서 활동 노출 횟수를 추적하는 방법은 무엇입니까? {#activity-impressions}

+++답변

[!DNL Analysis Workspace]에서 활동 노출 횟수를 보려면:

1. [!DNL Target] UI에서 **[!UICONTROL View in Analytics]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Activity Impressions]** 열을 [[!DNL Analytics Workspace]](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html){target=_blank} 보고서에 추가합니다.
1. **[!UICONTROL Activity Impressions]** 열에서 [!UICONTROL Gear] 아이콘을 클릭합니다.
1. **[!UICONTROL Use non-default attribution model]** 아이콘을 클릭합니다.
1. **[!UICONTROL Same Touch Model]** > **[!UICONTROL Apply]**&#x200B;을(를) 선택합니다.

+++
