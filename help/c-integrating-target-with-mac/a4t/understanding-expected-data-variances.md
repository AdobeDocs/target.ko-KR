---
keywords: data variances;analytics;differences;variance;a4t;analytics for target;analytics as the reporting source;discrepancies;discrepancy
description: Analytics를 보고 소스(A4T)로 사용하지 않아 데이터 분산이 모두 삭제될 때 Target과 Adobe Analytics 간의 예상 데이터 분산에 관해 설명합니다.
title: A4T를 사용하지 않을 때 예상되는 데이터 분산
feature: a4t troubleshooting
topic: Advanced
uuid: 61bef460-8613-4251-b1b2-b6226ec86d9b
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 100%

---


# A4T를 사용할 때와 사용하지 않을 때 Target과 Analytics 간에 예상되는 데이터 분산{#expected-data-variances-when-not-using-a-t}

Analytics를 보고 소스(A4T)로 *사용*&#x200B;할 때와 *사용하지 않을* 때 [!DNL Target]와 Adobe [!DNL Analytics] 간에 예상되는 데이터 차이에 대한 정보입니다. A4T가 데이터 분산을 크게 줄임.

## A4T를 사용할 때 예상되는 데이터 차이 {#expected-using-a4t}

A4T를 사용하면 활동에 대한 Analytics 및 Target 보고는 모두 Analytics 데이터만 사용하므로 Target 활동 보고서의 솔루션 간에 차이가 거의 없습니다. 그러나 일부 경우에는 고객이 Target 데이터를 A4T 통합의 범위를 벗어난 Analytics 데이터와 비교하므로 아래에 설명된 분산 문제가 발생할 수 있습니다.

다음은 예상 데이터 차이가 발생할 수 있는 몇 가지 시나리오입니다.

* A4T에서는 Target 히트(페이지 상단)가 발생하지만 Analytics 히트(페이지 하단)는 발생하지 않을 수 있습니다. 이 방법의 예로는 사용자가 페이지를 로드하지만 Analytics 호출이 트리거되기 전에 브라우저를 닫는 경우입니다. 이 경우 A4T는 데이터에서 Target 히트를 제외합니다. 이렇게 하는 이유는 실제 Analytics 호출이 없을 때 Analytics 히트로 카운트하도록 Target 히트(즉, 페이지 상단)를 허용하면 Analytics의 데이터 세트와 일치하지 않기 때문입니다(방문자 부풀림 등).

   트래픽을 50/50(또는 25/25/25/25 등)으로 분할하도록 리디렉션 테스트가 Target에 설정된 경우 사용자 행동이 균일하게 나누어지지 않을 수 있습니다. 불규칙한 분할이 표시되는 경우, 한 사용자 그룹이 랜딩 페이지에서 다른 그룹이 했던 것보다 Analytics 호출을 더 많이 실행하지 못했음을 의미합니다. 한 그룹에 대한 Analytics 호출을 실행하지 못하면 해당 사용자에 대한 Target 히트가 제외되어 불일치가 생성됩니다.

   향후 Adobe Experience Platform에서 A4T를 사용할 때 해결되기를 바라는 문제입니다. Adobe 팀은 페이지에서 서로 다른 시간에 발생하는 이러한 여러 이벤트를 처리할 최선의 방법을 모색하고 있습니다.

   >[!NOTE]
   >
   >A4T에서 리디렉션을 사용하는 제한된 고객 수가 연결되지 않은 적중률 비율이 높아지는 알려진 문제가 해결되었습니다. [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md#redirect)를 참조하십시오.

* 모든 방문자에게 특정 페이지를 공개하는 자동 할당 활동을 만든다고 가정합니다. 자동 할당 활동은 A4T를 지원하지 않으므로 모든 활동 데이터를 [!DNL Target]에서 수집합니다. [!DNL Target] 보고의 활동 방문자가 동일한 기간에 대한 [!DNL Analytics] 보고에서 해당 페이지 방문자와 일치해야 한다고 예상할 수도 있습니다. 이 시나리오에서는 아래에 설명된 분산이 예상됩니다.

   A4T를 지원하는 전체 활동 유형 목록에 대해서는 [지원되는 활동 유형](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA)을 참조하십시오.

## A4T를 *사용하지 않을* 때 예상되는 데이터 분산 {#expected-not-using-a4t}

비슷한 데이터 집합에서도 15-20% 차이는 일반적입니다. 다르게 카운트되는 시스템은 35-50%만큼 높은 데이터 차이를 발생시킬 수 있습니다. 차이가 훨씬 더 큰 경우도 있습니다.

실제 데이터는 상당히 다를 수 있지만 일반적으로 추세는 일관됩니다. 차이와 우세가 일관되기만 하면 데이터도 귀중하고 유용한 상태로 유지됩니다. 차이와 추세가 일관되지 않은 경우 잘못 설정된 항목이 있음을 의미할 수 있습니다. 이 경우 지원을 받으려면 계정 담당자에게 문의하십시오.

[!DNL Analytics]는 방문 및 트랜잭션을 기준으로 시스템을 사용하지만 [!DNL Target]은 방문자 기반 지표를 사용합니다. 즉, 방문자가 페이지를 열 때마다 [!DNL Analytics]에서는 방문으로 계산되지만 [!DNL Target]에서는 활동에 설정된 조건이 충족될 때까지 방문으로 계산되지 않습니다.

[!DNL Target]의 보고서에는 활동을 정의할 때 선택된 전환 mbox를 기준으로 한 성과가 표시되지만, 이 전환 mbox 데이터는 [!DNL Analytics] 태깅 구현에서 정의한 대로 자체 전환 변수가 있는 [!DNL Analytics]로 전송되지 않습니다. 동일한 데이터를 예상할 수 있는 경우(예: 소매점의 주문 확인 페이지에 전환 mbox와 [!DNL Analytics] 구입 이벤트가 모두 포함된 경우) 이러한 태그의 배치 때문에 데이터가 다를 수 있습니다. 일반적으로 두 가지 제품의 보고서에서 트렌드는 비슷해야 합니다.

예상 데이터 차이는 기술 및 비즈니스 차이로 인해 발생할 수 있습니다.

### 기술적 차이의 예 {#section_C3B50ED2E2F9416FAC91437CF1A87369}

다음 사항으로 인해 기술적 차이에 따라 데이터 차이가 발생할 수 있습니다.

* [!DNL Target] 방문자는 쿠키와 JavaScript를 허용해야 합니다.
* 자사 쿠키와 타사 쿠키가 다르게 처리되므로 이러한 쿠키 유형의 데이터는 일치하지 않습니다.
* 페이지에서 태그의 상대 위치와 페이지가 완전히 로드되기 전에 페이지를 종료하는 방문자로 인한 &quot;누수&quot;
* 시간대 고려 사항
* 장치가 카운트될 수 있는 차이

### 비즈니스 차이의 예 {#section_2E1EB5E15BB64A1A80E4CDB1A5062AEE}

다음 사항으로 인해 비즈니스 차이에 따라 데이터 차이가 발생할 수 있습니다.

* 방문자와 방문 지표 간의 차이
* 활동에 대해 타깃팅하면 일부 방문자가 제외됩니다.
* 단일 mbox가 여러 페이지에 위치하고 각 페이지에서 방문자가 카운트될 수 있습니다.
* 캠페인 우선순위에 페이지의 일부 방문자는 포함되고 다른 방문자는 제외될 수 있습니다.
* 한 번 전환된 방문자가 캠페인에 다시 진입하면 다시 계산됩니다.
* [!DNL Analytics]는 모든 방문과 방문자에 대한 전환을 모두 계산하지만 [!DNL Target]은 활동에 포함된 방문과 방문자에 대한 전환만 계산합니다.