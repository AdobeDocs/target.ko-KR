---
keywords: 보고서;자동 타겟;자동 타겟;AT;보고서
description: Adobe Target에서 자동 타겟 요약 보고서를 해석하는 방법을 알아봅니다. 이 보고서에서 자동화된 세그먼트 및 중요 속성 보고서로 전환할 수 있습니다.
title: 자동 타겟 요약 보고서는 어떻게 사용합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Reports
exl-id: 098fcc0e-8e17-4898-ab2f-ec74472562ff
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 52%

---

# Auto-Target 요약 보고서

[!DNL Adobe Target]의 [!UICONTROL Auto-Target Summary] 보고서를 해석하는 방법에 대한 정보입니다.

>[!NOTE]
>
>[!UICONTROL Auto-Target]은(는) [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. [Target Premium 라이선스](/help/main/c-intro/intro.md#premium)가 없는 [!DNL Target Standard]에는 포함되어 있지 않습니다.

[!UICONTROL Auto-Target Summary] 보고서를 표시하려면:

1. [!UICONTROL Activities] 페이지에서 원하는 [!UICONTROL Auto-Target] 활동을 클릭합니다.

   활동이 많은 경우 [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Property], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] 및 [!UICONTROL Activity Source] 드롭다운 목록에서 옵션을 선택하여 목록을 필터링할 수 있습니다.

1. [!UICONTROL Reports] 탭을 클릭한 다음 원하는 아이콘을 클릭합니다.

   * 표 보기
   * 그래프 보기
   * 자동화된 세그먼트
   * 중요 속성

## 표 보기

다음 그림은 [!UICONTROL Auto-Target] 활동의 보고서를 볼 때 [!UICONTROL Table View]에서 일반적인 요약 보고서가 어떻게 표시되는지 보여 줍니다.

![자동 타겟 테이블 보기 보고서](/help/main/c-reports/assets/at-table-view.png)

[!UICONTROL Auto-Target] 보고서를 해석하는 데 필요한 몇 가지 팁과 고려 사항:

* 표의 다양한 행은 활동 성능을 이해하는 데 도움이 됩니다.

   * 보고 페이지에 있는 표에서 맨 위의 두 행에는 통제군(즉, 임의로 제공된 경험)에 지정된 방문자와 개인화 알고리즘에 지정된 방문자 간의 A/B 테스트의 결과가 표시됩니다. 이 정보를 사용하여 무작위로 제공된 통제군과 비교하여 개인화 알고리즘이 어떻게 수행되었는지를 측정할 수 있습니다.
   * 나머지 행은 경험 수준의 결과를 보여줍니다. 각 경험에 대해서는, 해당 경험이 임의로 제공되는 통제 경험으로서 표시된 방문자의 평균 응답과 경험이 개인화 알고리즘을 사용하는 것으로 표시된 방문자의 평균 응답 간 비교가 있습니다.

* 보고서에서 각 경험 옆에 있는 녹색 확인 아이콘은 해당 경험에 대해 개인화된 머신 러닝 모델이 생성되었음을 나타냅니다. 시계 아이콘은 모델을 만들 수 있는 충분한 트래픽이 제공되지 않았음을 나타냅니다.

   * 모델은 경험마다 만들어지므로 녹색 확인 아이콘이 있는 경험과 시계 아이콘이 있는 다른 경험들을 위한 모델이 표시될 수 있습니다.
   * 이 경우 모든 경험을 위해 모델을 만드는 활동의 속도를 높이기 위해 아직 만들어지지 않은 모델이 있는 경험에 추가 트래픽이 전송됩니다.
   * 개인화를 시작하려면 모델이 빌드된 경험(녹색 확인 표시)이 두 개 이상 있어야 합니다.

* [!UICONTROL Auto-Target]에서 경험 A의 전환율과 경험 B의 전환율을 비교하는 것은 적절하지 않습니다. 문제는 지능적인 방식으로 제공될 때와 임의 방식(다시 말해 통제군 사용)으로 제공될 때 중 언제 경험 A가 더 나은 성과를 보이는가 하는 것입니다. 또한 개인화 알고리즘은 개별 경험이 아니라 전체 활동에 대한 성공 지표에 대해 최적화하려고 시도하므로 마케터는 개별 경험의 상승도 해석에 대해 주의해야 합니다.
* 상승도가 가장 높은 경험은 모집단 내에서 분화가 가장 큰 것으로 이해할 수 있습니다. 즉, 알고리즘이 해당 특정 경험을 가장 좋아하는 세그먼트를 찾은 것입니다.
* 테이블의 다양한 열은 방문 횟수, 전환율, 평균 상승도 및 신뢰 수준 및 신뢰도를 보여 줍니다. 자세한 내용은 [A/B 테스트의 통계 계산](/help/main/c-reports/statistical-methodology/statistical-calculations.md)을 참조하십시오.

## 그래프 보기

다음 그림은 [!UICONTROL Auto-Target] 활동의 보고서를 볼 때 [!UICONTROL Graph View]에서 일반적인 요약 보고서가 어떻게 표시되는지 보여 줍니다.

![자동 타겟 그래프 보기 보고서](/help/main/c-reports/assets/at-graph-view.png)

아래 표시된 것처럼, 두 드롭다운 목록을 사용하여 원하는 지표, 계산 방법론 등을 선택할 수 있습니다. 자세한 내용은 [보고서 설정 개요](/help/main/c-reports/c-report-settings/report-settings.md)를 참조하십시오.

![자동 타겟 그래프 보기 보고서](/help/main/c-reports/assets/at-graph-view-2.png)

## 자동화된 세그먼트

[!UICONTROL Automated Segments] 아이콘을 클릭합니다. 이 보고서는 서로 다른 방문자가 AP/AT 활동의 오퍼/경험에 어떻게 다르게 반응하는지를 보여 줍니다. 이 보고서는 Target의 개인화 모델에 정의된 다른 자동화된 세그먼트가 활동의 오퍼/경험에 응답하는 방식을 보여 줍니다.

![자동화된 세그먼트 아이콘](/help/main/c-reports/assets/icon-automated-sements.png)

자세한 내용은 [자동화된 세그먼트 보고서](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md)를 참조하십시오.

## 중요 속성

[!UICONTROL Important Attributes] 아이콘을 클릭합니다. 이 보고서는 다른 활동에서 다른 속성이 모델이 개인화를 결정하는 방법에 대해 얼마나 중요한지 (또는 덜 중요한지) 보여줍니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다.

![중요 특성 아이콘](/help/main/c-reports/assets/icon-important-attributes.png)

자세한 내용은 [중요 특성 보고서](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md)를 참조하십시오.
