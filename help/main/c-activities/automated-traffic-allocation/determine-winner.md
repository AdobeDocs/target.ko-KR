---
keywords: 자동화된 트래픽 할당;타깃팅;승자;통계적 보장;신뢰도;승자 결정;상승도;신뢰도;기본값;기본 경험;자동 할당;자동 할당
description: 상승도 및 신뢰도와 같은 주요 지표를 중심으로 [!UICONTROL 자동 할당] A/B 활동 결과를 해석하는 방법을 알아봅니다.
title: '[!UICONTROL 자동 할당] 보고서를 어떻게 해석합니까?'
feature: Auto-Allocate
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
TQID: 'https://experienceleague.adobe.com/o4mFGMk-M5QUvJ57kYnfjMPvVZL8l6YegJQSJyHjAxc'
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
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 7eede3484d524e87127de9147aa786484fc87c7d
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 3%
---
# [!UICONTROL 자동 할당] 보고서 해석 {#interpret-auto-allocate-reports}

>[!BEGINSHADEBOX]

**이 페이지에서:** 통계적으로 **[!UICONTROL 자동 할당]**&#x200B;이 제공하는 **[!UICONTROL 자동 할당]** 활동의 우승 경험을 식별하는 방법과 보고서에서 상승도 및 신뢰도 수치를 읽는 방법을 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Target]의 **[!UICONTROL 자동 할당]** A/B 활동 보고서는 활동이 우승자를 발견했는지 여부와 그 결과에 대한 [!DNL Target]의 신뢰도를 보여줍니다. 승자 배지, 상승도 및 신뢰도와 같은 지표는 결과를 해석하는 데 도움이 됩니다.

많은 마케터가 결과가 명확한 승자를 표시하기 전에 가장 성과가 좋은 경험을 조급하게 선언합니다. [!DNL Target]을(를) 사용하면 우승자를 쉽게 결정할 수 있습니다. 우승자 선언에 대한 일반적인 정보는 [10가지 일반적인 A/B 테스트 위험 및 이를 피하는 방법](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md)을 참조하십시오.

## 우수성이 검증된 경험 식별 {#identify-winner}

**[!UICONTROL 자동 할당]** 기능을 사용하는 경우 [!DNL Target]은(는) 활동 페이지 맨 위에 배지를 표시합니다. 배지는 활동이 충분한 신뢰도로 최소 전환 수에 도달할 때까지 &quot;아직 우승자 없음&quot;을 나타냅니다.

![우승자 배지 없음](/help/main/c-activities/automated-traffic-allocation/assets/no-winner-new.png)

명백한 승자를 선언하면 [!DNL Target]에 &quot;우승자: 경험 *X*&quot; 배지가 표시됩니다.

![우승자 배지](/help/main/c-activities/automated-traffic-allocation/assets/winner-new.png)

우승자 배지는 **[!UICONTROL 활동]** 목록에 있는 활동의 정보 팝업에도 표시되므로 **[!UICONTROL 자동 할당]** 활동을 열지 않고도 상태를 볼 수 있습니다.

>[!NOTE]
>
>**[!UICONTROL 자동 할당]** 활동은 컨트롤과 쌍별 비교를 수행할 뿐만 아니라 모든 옵션 중에서 최상의 경험을 찾도록 설계되었습니다.

## [!UICONTROL 자동 할당]의 통계적 보장 {#statistical-guarantees}

A/B 활동이 끝날 때 **[!UICONTROL 자동 할당]**&#x200B;은(는) 결정된 우승자가 5%의 유효 긍정 오류(false-positive) 비율을 갖도록 보장합니다. 이것은 5% 동안만 결정된 승자가 활동의 모든 경험 중에서 실제로 최고의 경험이 아님을 의미합니다.

동일한 경험을 가진 [A/A 테스트](/help/main/c-activities/t-test-ab/aa-testing.md)의 경우 [!DNL Target]에서 5% 미만의 시간 동안 테스트를 완료합니다. A/A 테스트의 예상 비헤이비어는 무기한 실행되므로 우승자 배지가 나타나지 않아야 합니다.

### 신뢰도 및 p-값 {#confidence-p-values}

[!DNL Target]은(는) **[!UICONTROL 자동 할당]**&#x200B;에 p 값 기반 신뢰도를 사용하지 않습니다. **[!UICONTROL 자동 할당]** 활동의 **[!UICONTROL 신뢰도]** 열에는 경험에 1% 오차 범위 내에서 승자가 될 가능성이 표시됩니다. 알고리즘에서는 가장 좋은 전환율과 두 번째로 좋은 전환율 사이에 최소 1%의 감지 가능한 효과를 사용하며 [Bernstein 부등식](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29)을 사용하여 이 확률을 계산합니다.

일반 A/B 테스트는 p 값을 기반으로 신뢰도를 계산하며, 이 값은 주어진 경험이 통제와 다를 확률을 &quot;느슨하게&quot; 계산합니다. 이 p값은 경험이 통제 경험과 다른지 여부를 판별하는 데에만 사용할 수 있습니다. 경험이 다른 경험과 다른지(제어가 아님) 확인하는 데 사용할 수 없습니다.

>[!IMPORTANT]
>
>[!DNL Target]은(는) 사전 정의된 최소 전환 수 이후의 승자를 표시합니다. 그러나 우승자를 선택하는 최종 결정은 항상 [!DNL Adobe Target] 표본 크기 계산기의 결과를 기반으로 해야 합니다. [!DNL Target]은(는) 사이트의 기본 전환율과 활동 기간을 결정하기 위해 계산기에 제공되는 기타 중요한 측면을 고려하지 않습니다. 따라서 [!DNL Target]은(는) 최소 전환 수에 따라 보장된 것보다 우승자를 먼저 표시할 수 있습니다. 자세한 내용은 [샘플 크기 계산기](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)를 참조하십시오.

## 상승도 및 신뢰도 보고 이해 {#lift-confidence}

**[!UICONTROL 자동 할당]** 활동의 **[!UICONTROL 보고서]** 탭에는 다음 수치가 표시됩니다.

| 그림 | 설명 |
|---|---|
| **환경 제어** | 첫 번째 경험(기본적으로 경험 A라고 함)은 항상 **[!UICONTROL 보고서]** 탭에서 &quot;제어&quot; 경험으로 정의됩니다. 이 경험은 경험의 성능을 결정하는 데 사용되는 모델링에서 진정한 통계 제어로 취급되지 않지만, 보고서의 일부 수치에 대한 참조 또는 기준선으로 취급됩니다. |
| **상승도** | 각 경험의 &quot;상승도&quot; 값과 95% 한계는 항상 정의된 &quot;제어&quot; 경험을 참조하여 계산됩니다. &quot;제어&quot; 경험은 자신을 기준으로 하는 상승도를 가질 수 없으므로 이 경험에 대해 보고서에는 빈 &quot;—&quot; 값이 표시됩니다.<br>A/B 테스트와 달리 **[!UICONTROL 자동 할당]** 테스트에서는 경험이 정의된 컨트롤보다 더 나쁜 경우 음수 상승도 값이 보고되지 않습니다. 대신 &quot;—&quot;이 표시됩니다. |
| **신뢰 구간** | 표시된 **[!UICONTROL 신뢰 구간]** 막대는 경험의 평균 전환율 예상 주변의 95% 신뢰 구간을 나타냅니다. 바는 정의된 &quot;제어&quot; 경험과 관련하여 색상으로 구분됩니다.<ul><li>&quot;제어&quot; 경험의 막대는 항상 회색입니다.</li><li>&quot;제어&quot; 경험의 신뢰 구간 아래의 신뢰 구간 부분은 빨간색입니다.</li><li>&quot;제어&quot; 경험의 신뢰 구간 위의 신뢰 구간 부분은 녹색입니다.</li></ul> |
| **우승자** | 선행 경험의 95% **[!UICONTROL 신뢰 구간]**&#x200B;이(가) 다른 경험과 겹치지 않으면 우승자를 찾았습니다. 우승 경험은 경험 이름 왼쪽과 &quot;우승자&quot; 배너에 녹색 별 배지가 지정됩니다. 별이 보이지 않을 때, 배너에는 &quot;아직 우승자 없음&quot;이라고 쓰여 있고 우승자는 아직 발견되지 않았습니다. |
| **신뢰도** | 현재 선두이거나 우승한 경험 옆에도 &quot;신뢰도&quot; 수치가 보고됩니다. 이 수치는 선행 경험의 **[!UICONTROL 신뢰도]**&#x200B;가 60% 이상에 도달할 때까지만 보고됩니다.<ul><li>**[!UICONTROL 자동 할당]** 활동에 두 개의 경험이 있는 경우 숫자는 해당 경험이 다른 경험보다 더 나은 성과를 보이고 있다는 신뢰 수준을 나타냅니다.</li><li>경험이 두 개 이상 있는 경우 숫자는 정의된 &quot;제어&quot; 경험보다 경험이 더 잘 수행되고 있다는 신뢰 수준을 나타냅니다.</li><li>제어 경험이 이기는 경우 &quot;신뢰도&quot; 수치가 보고되지 않습니다.</li></ul> |

## FAQ {#faq}

자주 묻는 질문에 대해 다음 답변을 고려하십시오.

+++ 활동을 시작한 지 며칠 되었습니다. 왜 모든 신뢰 값이 여전히 0%를 표시합니까?

다음 이유 중 하나에서는 0%가 모든 경험에 대해 보고서의 **[!UICONTROL 신뢰도]** 열에 표시되는 이유를 설명합니다.

* 수동 A/B 테스트 및 **[!UICONTROL 자동 할당]**&#x200B;은(는) 다른 통계를 사용하여 **[!UICONTROL 신뢰도]** 값을 표시합니다.

  수동 A/B 테스트에서는 [Welch의 t-test](https://en.wikipedia.org/wiki/Welch%27s_t-test)를 기반으로 p값을 사용합니다. p 값은 실제로는 경험과 제어 간에 관찰된(또는 더 극단적인) 차이가 없다는 것을 감안할 때 그러한 차이를 찾을 확률입니다. 이러한 p 값은 관찰된 데이터가 주어진 경험과 일치하는지 여부와 제어가 동일한지 여부를 결정하는 데만 사용할 수 있습니다. 경험이 다른 경험과 다른지(제어가 아님) 확인하는 데 사용할 수 없습니다.

  **[!UICONTROL 자동 할당]**&#x200B;은(는) 활동의 모든 경험에서 특정 경험이 실제 승자가 될 확률을 표시합니다. 우승 경험(우승자일 가능성이 가장 높음)에만 0이 아닌 신뢰도 값이 있습니다. 다른 모든 것들은 패배자일 가능성이 가장 높고 0%를 표시합니다.

* **[!UICONTROL 자동 할당]**&#x200B;은(는) 우승 경험이 60% 신뢰도를 수집한 후에만 신뢰도를 표시하기 시작합니다. 이러한 신뢰 수준은 일반적으로 일반 A/B 테스트가 완료되는 데 걸리는 시간의 약 절반에 나타납니다(이 시간대는 보장되지 않지만). 일반 A/B 테스트가 실행되는 시간을 결정하려면 [!DNL Adobe Target] [샘플 크기 계산기](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)를 사용하십시오. &quot;기본 전환율&quot;, &quot;5%&quot;는 &quot;상승도&quot;, 95%는 &quot;신뢰도&quot;로 컨트롤의 전환율을 입력하십시오. 일반적으로 신뢰도는 각 경험이 경험당 필요한 샘플의 50% 이상을 축적한 후에 표시되기 시작합니다. 이는 신뢰가 언제부터 나타나기 시작하는지 짐작하게 한다.

* 보고서에 전체에서 0%가 표시되면 활동이 너무 이른 것 같습니다.

+++

+++ [!UICONTROL Analytics]을(를) 보고 소스로 사용(A4T)하는 [!UICONTROL 자동 할당] 활동에 대해 &quot;우승자 없음&quot;, &quot;우승자&quot; 및 &quot;별&quot; 배지를 사용할 수 있습니까?

**[!UICONTROL 활동]** 목록의 활동 정보 팝업에 &quot;아직 우승자 없음&quot; 및 &quot;우승자&quot; 배지가 나타납니다. 이러한 데이터는 [!DNL Analysis Workspace]의 **[!UICONTROL A4T]** 패널에 나타나지 않거나 [!DNL Target]에서 동일한 보고서를 볼 때 나타나지 않습니다. A4T **[!UICONTROL 자동 할당]** 활동에 대한 [!DNL Target] 보고서에 우승자 &quot;별&quot; 배지가 표시되면 무시하십시오.

이 제한 사항과 기타 제한 사항 및 메모에 대한 자세한 내용은 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟] 활동&#x200B;*에 대한* A4T 지원의 [자동 할당](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa)을 참조하십시오.

+++
