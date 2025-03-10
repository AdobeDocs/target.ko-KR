---
keywords: 타깃팅;대상 필터;대상;필터
description: ' [!DNL Adobe Target] 에서 대상 필터를 사용하여 특성을 공유하는 방문자의 데이터를 보는 방법에 대해 알아봅니다.'
title: 보고에 대상 필터를 사용할 수 있습니까?
feature: Audiences
exl-id: af8dae97-4b10-4edb-a0e6-0d8daf2f0d22
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 72%

---

# 보고용 대상자 필터

[!DNL Adobe Target]의 대상 필터(또는 대상)는 특정 특성 또는 특성 집합을 공유하는 방문자 그룹입니다.

대상 필터를 사용하여 보고용으로 사용되는 대상을 지정합니다. 대상을 선택하고 성능을 전반적인 트래픽에 비교할 수 있습니다. 일반 트래픽과 비교할 때 다양한 트래픽 소스에 대한 승자가 서로 다른지 여부를 확인할 수 있습니다. 대상 필터는 다른 콘텐츠를 타겟팅할 가능성이 있는 대상을 찾는 데 도움이 됩니다. 대체로 한 우승자가 모든 트래픽에 적합하지는 않습니다.

예를 들어 특정 검색 엔진에서 페이지에 도착하는 방문자가 하나의 대상일 수 있습니다. 다른 대상은 성별, 연령, 위치, 등록 상태, 구입 내역 또는 방문자에 대해 수집할 수 있는 기타 모든 세부 사항을 기반으로 할 수 있습니다. 대상 필터를 사용하여 방문자 트래픽을 나누고 각 트래픽 세그먼트에 대한 경험 성과를 비교하십시오.

활동에 대상 필터를 사용하려는 경우 다음 지침을 고려하십시오.

* **방문자는 여러 대상에 있을 수 있습니다.** 두 개의 대상이 설정되어 있고(예: &quot;새 방문자&quot; 및 &quot;Google의 방문자&quot;) 한 사람이 두 기준을 모두 충족하는 경우 이 방문자는 두 대상에서 모두 계산되고 추적됩니다. 따라서 대상에 있는 방문자의 합계는 활동에 있는 방문자의 수와 일치하지 않습니다.
* **활동을 시작하기 전에 대상을 설정합니다.** 대상자 데이터는 소급하여 검색할 수 없습니다. 활동을 시작하기 전에 대상자 필터를 구성하지 않고 일정 기간 활동을 실행한 후 필터 사용을 결정하는 경우 이미 경과한 시간의 데이터는 수집하지 않습니다.
* **2-4개 대상자로 시작합니다.** 트래픽 소스 등의 기본 정보에 주력합니다.
* **필요한 경우 대상자 이름을 변경합니다.** 활동이 활성 상태인 경우에도 수집 중인 결과에 보다 의미 있는 대상자 이름이 되도록 데이터에 영향을 주지 않고 대상자 이름을 변경할 수 있습니다.
* **정확한 값을 입력합니다.** 대상자 필터 값은 대소문자를 구분합니다. 예를 들어 도시를 필터링하는 대상자를 사용하는 경우 &quot;OR&quot; 조건을 사용하여 &quot;Vienna&quot;, &quot;vienna&quot;, &quot;wien&quot;, &quot;Wien&quot; 등의 가능한 철자 및 대문자화 변형을 포함해야 합니다.
* [!UICONTROL Audiences] 목록에서 만든 **대상은 다시 사용할 수 있습니다.** 활동의 일부로 만들어진 대상자는 재사용할 수 없습니다.

다음 섹션에서는 대상을 설정하고 대상에 대해 보고하는 방법에 대해 자세히 설명합니다.

| 작업 | 주제 |
|--- |--- |
| 적절한 활동 또는 테스트 만들기 | [활동 및 테스트](/help/main/c-intro/target-key-concepts.md) |
| 필요한 경우 대상자 만들기 | [대상자 만들기](/help/main/c-target/c-audiences/create-audience.md) |
| 필요한 경우 여러 대상자 결합 | [여러 대상자 결합](/help/main/c-target/combining-multiple-audiences.md) |
| 활동의 목표 및 설정 페이지에서 대상자 적용 | A/B 테스트: [목표 및 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)<br>Automated Personalization: [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<br>경험 타깃팅: [목표 및 설정](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md)<br>다변량 테스트: [목표 및 설정](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md)<br>Recommendations: [Recommendations 활동 설정](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md)<br>활동 설정: [활동 설정](/help/main/c-activities/activity-settings.md) |
| 대상자 필터에 대한 정보가 있는 보고서 보기 | [보고서 설정](/help/main/c-reports/c-report-settings/report-settings.md) |
