---
keywords: 활동 설정;A/B 목표 및 설정;보고 설정;목표 지표;성공 지표;종속 성공 지표;고급 설정;기본 목표;추가 지표;목표;우선순위;지속 기간;보고 솔루션;목표;보고 대상자;이 지표를 늘리려면 어떤 성공 지표에 도달해야 합니까;사용자가 이 목표 지표를 접하면 어떻게 됩니까;메모
description: '[!UICONTROL 목표 및 설정] 페이지를 사용하여 A/B 활동 목표를 정의하는 방법을 알아봅니다.'
title: '[!DNL Target] A/B 활동에서 목표와 설정을 지정하는 방법'
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
TQID: 'https://experienceleague.adobe.com/X3JDvfXDHM2rAOodEY5N9TVO-tBpz4vNDUvhOpC0XZ4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: abab6b3e464bb9f294e9c3c455dca1f57bb0d458
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 24%
---
# 목표 및 설정 {#ab-goals-and-settings}

>[!BEGINSHADEBOX]

**이 페이지에서:** A/B, XT(경험 타기팅) 또는 MVT(다변량 테스트) 활동의 **[!UICONTROL 목표 및 설정]** 페이지에서 설정할 수 있는 내용(활동 설정, 보고 설정, 고급 설정 및 메모)을 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Target]의 **[!UICONTROL 목표 및 설정]** 페이지에서 활동 목표에 대한 정보를 지정합니다.

사용 가능한 설정은 Target 또는 [Analytics를 보고 소스로 사용](/help/main/c-integrating-target-with-mac/a4t/a4t.md)하는지에 따라 다릅니다.

A/B 활동에만 사용할 수 있는 [통계 방법](#section_statistical-methodology)을 제외하고 [!UICONTROL 경험 타깃팅]&#x200B;(XT) 및 [!UICONTROL 다변량 테스트]&#x200B;(MVT) 활동에도 동일한 설정이 적용됩니다.

* [활동 설정](#section_DCBDC354261F420EBD4B43EA34947BAC): 목표, 우선 순위 및 기간
* [보고 설정](#section_13119392051044FBA6387D9B3B1C43CF): 보고 소스, 목표 지표, 추가 지표 및 대상자
* [고급 설정](#section_E2FE441AFB324E498793ABB025ED9974): 종속성 및 방문자가 목표에 도달한 후 수행되는 작업
* [통계 방법](#section_statistical-methodology): 결과를 분석하는 방법
* [기타 메타데이터](#section_2E8917BEFB954480A4206B9E9E917F80): 메모

## [!UICONTROL 활동 설정] {#section_DCBDC354261F420EBD4B43EA34947BAC}

**[!UICONTROL 목표 및 설정]** 페이지의 **[!UICONTROL 활동 설정]** 섹션에서 다음 옵션을 구성할 수 있습니다.

![](../../assets/goals-ab-1.png)

### 목표 {#objective}

추가 목표를 입력합니다. 목표는 사용자와 팀 구성원이 활동을 식별하는 데 도움이 되는 모든 정보일 수 있습니다.

### 우선순위 {#priority}

대상자가 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.

설정에 따라 **[!UICONTROL 우선 순위]**&#x200B;에 대한 [!DNL Target] UI 및 옵션이 달라집니다.

* **이전 우선 순위(기본값):** 이 옵션이 **[!UICONTROL 관리]**(기본값)에서 활성화되지 않으면 **[!UICONTROL 낮음]**, **[!UICONTROL Medium]** 또는 **[!UICONTROL 높음]**&#x200B;의 우선 순위를 지정하십시오.
* **세분화된 우선 순위:** 0에서 999 사이의 값을 지정하십시오. 여기서 0 = **[!UICONTROL 낮음]** 및 999 = **[!UICONTROL 높음]**&#x200B;입니다.

  [세분화된 우선 순위](/help/main/administrating-target/reporting.md)를 사용하려면 **[!UICONTROL 관리]** > **[!UICONTROL 보고]**&#x200B;에 액세스한 다음 **[!UICONTROL 세분화된 우선 순위 사용]** 옵션을 전환하십시오.

이전 버전의 [!DNL Target]에서 만든 활동의 경우 **[!UICONTROL 낮음]** 우선순위는 0으로, **[!UICONTROL Medium]**&#x200B;은(는) 5로, **[!UICONTROL 높음]**&#x200B;은(는) 10으로 전환됩니다. 필요에 따라 이러한 값을 조정할 수 있습니다.

>[!NOTE]
>
>세분화된 우선순위를 사용한 후에 비활성화하려면 먼저 모든 우선순위를 0, 5, 10으로 다시 설정해야 합니다.

### 지속 시간 {#duration}

활동은 승인될 때 시작되거나 특정 날짜 및 시간을 설정하여 시작할 수 있습니다. 이와 마찬가지로, 활동은 비활성화될 때 종료되거나 날짜 및 시간을 설정하여 종료할 수 있습니다.

시간 선택기는 24시간 형식을 사용하며 00:00은 자정을 나타냅니다. 해당 시간대는 브라우저에 구성된 시간대로 설정됩니다. 다른 시간대를 사용하려면 브라우저를 다른 시간대로 설정하고 브라우저를 다시 시작하십시오.

## [!UICONTROL 보고 설정] {#section_13119392051044FBA6387D9B3B1C43CF}

**[!UICONTROL 목표 및 설정]** 페이지의 **[!UICONTROL 보고 설정]** 섹션에서 다음 옵션을 구성할 수 있습니다.

![](../../assets/goals-ab-2.png)

### 보고 소스 {#reporting-source}

수집할 솔루션 데이터 지정:

* [!DNL Adobe Target]

* [!DNL Adobe Analytics]

  +++ 보고 소스로서의 Analytics에 대한 자세한 정보

  보고 솔루션 간의 차이점과 각 솔루션의 이점에 대해 자세히 알아보려면 [Adobe Analytics를 Target의 보고 소스로 사용](/help/main/c-integrating-target-with-mac/a4t/a4t.md)을 참조하십시오. [!DNL Target]에 대한 보고 소스로 [!DNL Analytics]을(를) 선택할 때 [!DNL Target] 활동 데이터를 받을 [!DNL Analytics] 보고서 세트를 선택합니다.

  보고 소스를 지정하려면 먼저 사용자 계정이 연결된 [!DNL Analytics] 회사 중에서 선택한 다음 활동에 대한 보고서 세트를 선택합니다. [!DNL Adobe Target]에 연결하기 위해 제공된 보고서 세트만 선택할 수 있습니다. 예상한 보고서 세트가 표시되지 않으면 먼저 로그아웃했다가 [!DNL Adobe Experience Cloud]에 다시 로그인하여 다시 시도하십시오. 보고서 세트가 여전히 목록에서 누락된 경우 고객 지원 센터에 문의하십시오.

  [!DNL Analytics for Target]&#x200B;(A4T)에서는 결과를 올바로 보고하려면 추적 서버가 필요합니다. 기본 추적 서버가 **[!UICONTROL 추적 서버]** 필드에 표시됩니다. 추적 서버를 두 개 이상 사용하는 경우 이 필드에 올바른 추적 서버를 포함해야 합니다. 자세한 내용은 [Analytics 추적 서버 사용](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.
  +++

* [!DNL Adobe Customer Journey Analytics]

  +++ 보고 소스로서의 Customer Journey Analytics에 대한 자세한 정보

  지원되는 활동 유형, 샌드박스 및 데이터 보기 선택, 목표 지표 및 [!DNL Customer Journey Analytics]의 보고 설정에 대해서는 [[!DNL Target] 보고 위치 [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md)를 참조하십시오.
  +++

[계정 설정](/help/main/administrating-target/reporting.md)에 보고 소스가 지정되어 있으면 지정된 소스가 사용되며 이 설정은 표시되지 않습니다.

보고서 일관성을 유지하기 위해 활동이 활성 상태가 되면 보고 소스를 변경할 수 없습니다.

### 목표 지표 {#goal-metric}

>[!NOTE]
>
>보고 솔루션을 [!DNL Analytics]&#x200B;(으)로 설정하면 사용 가능한 목표 지표는 **[!UICONTROL 전환]**&#x200B;뿐입니다. [!DNL Analytics] 지표를 목표로 선택할 수 없습니다.

목표를 달성하려면 방문자가 수행한 동작을 선택합니다. 예를 들어 **[!UICONTROL 전환]** 지표를 선택한 다음 성공 시기를 결정하는 매개 변수를 설정합니다.

지표 설정에 대한 자세한 내용은 [지표 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md)을 참조하십시오.

추가 옵션을 보려면 목표 지표 옆에 있는 **[!UICONTROL 자세히]** 아이콘을 클릭한 다음 **[!UICONTROL 고급 설정]**&#x200B;을 클릭합니다. [고급 설정](#section_E2FE441AFB324E498793ABB025ED9974)을 참조하세요.

![](../../assets/goals-ab-3.png)

**[!UICONTROL 전환 예상 값]** 필드가 사용하도록 설정되어 있으면 목표 값을 제공하지만 다른 지표의 값은 제공하지 않습니다. 이 필드에는 다음 사항이 적용됩니다.

* 이 값을 사용하면 [!DNL Target]에서 예상 매출액 상승도를 계산할 수 있습니다.
* 필드는 선택 사항입니다. 하지만 비수익 지표에 대한 증분 매출은 이 필드 없이 계산할 수 없습니다.
* **[!UICONTROL 페이지 점수]** 지표에 대해 필드를 사용할 수 없습니다.
* 모든 매출 지표(**[!UICONTROL 방문자당 매출]**, **[!UICONTROL 평균 주문 가격]**, **[!UICONTROL 총 매출]** 및 **[!UICONTROL 주문 수]**)에 대해 예상 값은 **[!UICONTROL 방문자당 매출]**&#x200B;을 사용합니다. 데이터 유형은 통화입니다.

### 추가 지표 {#additional-metrics}

보고 솔루션을 [!DNL Analytics]&#x200B;(으)로 설정한 경우에는 이 설정을 사용할 수 없습니다. 이 경우 [!DNL Analytics] 보고서 세트에 대해 정의된 지표가 적용됩니다.

### 보고 대상 {#audiences-for-reporting}

![](../../assets/goals-ab-4.png)

기본적으로 보고서에는 자격을 갖춘 모든 방문자의 결과가 표시됩니다. 보고서 대상을 추가하여 특정 대상에만 대한 정보를 표시할 수 있습니다.

[!DNL Analytics]을(를) 보고 솔루션으로 선택하는 경우에는 이 설정을 사용할 수 없습니다. [!DNL Analytics] 보고서 세트에 대해 정의된 대상이 적용됩니다.

## 고급 설정 {#section_E2FE441AFB324E498793ABB025ED9974}

**[!UICONTROL 목표 및 설정]** 페이지의 **[!UICONTROL 고급 설정]** 섹션에서 고급 옵션을 구성할 수 있습니다.

고급 설정을 지정하려면 **[!UICONTROL 내 기본 목표]** 섹션에서 **[!UICONTROL 자세히]** 아이콘(![자세히 아이콘](/help/main/assets/icons/MoreSmallList.svg))을 클릭한 다음 **[!UICONTROL 고급 설정]**&#x200B;을 클릭합니다.

![](../../assets/goals-ab-3.png)

>[!NOTE]
>
>[!DNL Adobe Analytics]를 보고 소스로 사용하는 경우 설정은 [!DNL Analytics] 서버에서 관리됩니다. 고급 설정 옵션은 사용할 수 없습니다.

### 이 지표가 증가되기 위해 도달해야 할 성공 지표는 무엇입니까? {#dependencies}

다른 성공 지표에 도달한 적이 있는 경우에만 이 옵션을 사용하여 성공 지표에 도달한 것으로 카운트하십시오. 예를 들어, 방문자가 전환하기 전에 오퍼를 클릭하거나 특정 페이지에 도달한 경우에만 활동 전환이 유효할 수 있습니다.

여러 지표에 대한 종속성과 유연성을 제공하여 카운트를 늘리기 위해 지표에 도달해야 할지 또는 도달하지 않아야 할지를 선택할 수 있습니다. 두 성공 지표(또는 여러 개의 성공 지표)를 정의한 다음 두 성공 지표를 서로 종속시킵니다. **[!UICONTROL 종속성 추가]** 옵션을 사용하면 다른 성공 지표에 도달했거나 도달하지 않은 경우 성공 지표를 늘릴 수 있습니다.

종속성을 추가하려면 다음을 수행하십시오.

1. 추가 지표를 추가한 후 **[!UICONTROL 고급 설정]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 종속성 추가]** 옵션을 클릭합니다.

1. 원하는 지표를 드래그하여 놓은 다음 **[!UICONTROL 도달]**&#x200B;을 클릭하여 **[!UICONTROL 도달]**&#x200B;과(와) **[!UICONTROL 도달 못 함]** 간에 설정을 전환합니다.

종속성을 추가한 후 편집하거나 제거할 수 있습니다.

### 사용자가 이 목표 지표에 도달한 후에 어떤 상황이 진행됩니까? {#after-goal}

활동 목표에 도달한 후에는 우선순위가 높은 활동에 방문자가 적격한 경우를 제외하고 방문자에게 활동 콘텐츠가 계속 표시됩니다. 해당 방문자가 목표에 다시 도달하면 다른 전환으로 카운트됩니다. 이는 방문자가 활동을 다시 볼 경우 새 방문자로 계산되는 [!DNL Target Classic]의 기본 비헤이비어와 다릅니다.

사용자가 목표 지표에 도달한 다음에 진행되는 상황을 지정할 수 있는 세 가지 옵션이 있습니다.

* 카운트가 증가하는 방식을 지정하려면 **[!UICONTROL 카운트를 늘리고 사용자를 활동에 유지]**&#x200B;하세요.
* **[!UICONTROL 증분 카운트, 사용자 해제 및 재입력 허용]**&#x200B;을 통해 사용자가 활동을 다시 입력할 경우 표시되는 경험을 지정할 수 있습니다.
* **[!UICONTROL 활동 콘텐츠 대신 사용자에게 표시되는 콘텐츠를 지정하려면 증분 카운트, 재입력에서 사용자 및 막대 해제]**.

### 카운트는 어떻게 증분됩니까? {#count-increment}

카운트를 늘리는 방법에는 다음 세 가지가 있습니다.

* **[!UICONTROL 응모자마다 한 번]**
* **[!UICONTROL 노출 시마다(페이지 새로 고침 제외)]**
* **[!UICONTROL 노출 시마다]**

고급 설정에 대한 자세한 내용은 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md#overview)를 참조하십시오.

## 통계적 방법론 {#section_statistical-methodology}

**[!UICONTROL 목표 및 설정]** 페이지의 **[!UICONTROL 통계 방법]** 섹션에서 실험 결과를 분석하는 방법을 선택할 수 있습니다.

### 방법론 옵션 {#methodology-options}

이 선택은 이 활동의 **[!UICONTROL 전환]** 목표 지표에 사용되는 통계 프레임워크, 결과 지표 및 결정 기준을 결정합니다.

* 데이터가 도착하면 신념을 업데이트하는 확률 기반 의사 결정 **[!UICONTROL 베이지안]:** 지속적인 모니터링과 더 작은 샘플 크기를 지원합니다. 결과는 한 변형이 다른 변형보다 나을 확률로 표현됩니다(예: &quot;변형 B가 제어를 이길 확률 92%&quot;).
  * 작은 샘플 크기, 연속 모니터링, 확률을 선호하는 이해 당사자 또는 적용할 과거 테스트의 사전 지식이 있는 경우에 가장 적합합니다.
  * 엄격한 규제 또는 규정 준수 승인이 필요하거나 기존 p-value가 필요한 경우에는 적합하지 않습니다.
  * 보고서에 빈도가 높은 **[!UICONTROL 신뢰도]** 열 대신 **[!UICONTROL 제어를 이길 가능성]** 및 신뢰할 수 있는 간격이 표시됩니다.
* **[!UICONTROL Welch의 t-test(Frequentist)]:** 기존 가설-테스트 방법론입니다. p 값을 사용하며 고정된 샘플 크기가 필요합니다. 보고서에 **[!UICONTROL 신뢰도]** 백분율 및 신뢰 구간이 표시됩니다.

이 설정은 기본 목표 지표가 **[!UICONTROL 전환]**&#x200B;인 활동에만 사용할 수 있습니다. **[!UICONTROL 매출]** 또는 **[!UICONTROL 참여]** 기본 목표가 있는 활동은 항상 **[!UICONTROL Welch의 t-test]**&#x200B;를 사용합니다.

각 방법론의 계산 및 보고 방법에 대한 자세한 내용은 [A/Bn 테스트의 통계 계산](/help/main/c-reports/statistical-methodology/statistical-calculations.md)을 참조하십시오.

### 베이지안 구성 {#bayesian-configuration}

이 설정은 **[!UICONTROL 베이지안]**&#x200B;이(가) **[!UICONTROL 통계 방법]**(으)로 선택된 경우에만 표시됩니다. 다음 옵션을 구성합니다.

* **[!UICONTROL 신뢰할 수 있는 간격]**: 실제 효과가 떨어질 범위를 설정합니다.
* **[!UICONTROL 결정 임계값]**: 승자로 선언하기 전에 **[!UICONTROL 제어]**&#x200B;를 기준으로 변형이 도달해야 하는 최소 확률을 설정합니다.
* **[!UICONTROL 과거 테스트의 사전 지식을 사용하시겠습니까?]**: **[!UICONTROL 베이지안]** 계산을 알리기 위해 과거 성능에서 사전 지식을 제공하려면 이 옵션을 켜십시오.

## 기타 메타데이터 {#section_2E8917BEFB954480A4206B9E9E917F80}

**[!UICONTROL 목표 및 설정]** 페이지의 **[!UICONTROL 기타 메타데이터]** 섹션을 통해 귀하 또는 다른 팀원을 위해 유용한 활동에 대한 정보를 지정할 수 있습니다.
