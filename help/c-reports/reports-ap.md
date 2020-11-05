---
keywords: Targeting;AP reports;automated personalization reports;activity level report;offer level report;offer detail report
description: Adobe Target의 Automated Personalization 활동 사용자는 전문 보고서를 이용할 수 있습니다.
title: 자동화된 개인화 요약 보고서
feature: reports
uuid: 959b6814-9686-4741-8a79-5957e64f6209
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 71%

---


# ![PREMIUM](/help/assets/premium.png) 자동화된 개인화 요약 보고서{#automated-personalization-summary-reports}

Specialized reports are available to users of [!UICONTROL Automated Personalization] activities in [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL 자동화된 개인화]는 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. [!DNL Target Standard]Target Premium 라이센스가 없는 [에는 포함되어 있지 않습니다](/help/c-intro/intro.md#premium).

1. **[!UICONTROL 활동]**&#x200B;을 클릭하고 목록에서 원하는 [!UICONTROL 자동화된 개인화] 활동을 클릭한 다음, **[!UICONTROL 보고서 탭을 클릭합니다.]**

   많은 활동이 있는 경우 [!UICONTROL 유형] 드롭다운 목록에서 [!UICONTROL 자동화된 개인화]를 선택하여 목록을 필터링할 수 있습니다.

1. (선택 사항) 사용 가능한 모든 성공 지표로 구분된 요약 보기(예를 들어 통제 트래픽과 타깃팅된 트래픽 비교)를 다운로드하려면 [!UICONTROL 다운로드] 아이콘을 클릭하십시오.

[!UICONTROL 자동화된 개인화]는 다음 보고서를 제공합니다.

## Activity Level report {#section_6F72FC5C790B4492B3DCECBFFA971337}

[!UICONTROL 활동 수준] 보고서에서는 [!UICONTROL 자동화된 개인화] 알고리즘을 사용하는 합계 성과를 무작위로 제공된 컨텐츠(통제 컨텐츠)에 비교합니다.

![활동 수준 보고서](/help/c-reports/assets/box_plot_ap.png)

상승도, 신뢰도, 트렌드, 지속 기간 등을 포함하여 A/B 테스트에 대한 결과 해석의 표준 규칙이 여전히 적용됩니다. 결과 해석에 대한 자세한 내용은 [전환율에 대하여](/help/c-reports/conversion-rate.md#concept_2D9FEDE8F94A485DAC86D611BFBDC844)를 참조하십시오.

## Offer Level report {#section_CAA6409879E349C6906E2BE8156D87A1}

랜덤 포레스트 경험에 대한 [!UICONTROL 오퍼 수준] 보고서는 알고리즘이 적용된 각 오퍼의 성과를 무작위로 제공된 동일한 오퍼(통제 오퍼)에 비교합니다. 따라서 이 보기에서 오퍼는 서로 비교되지 않습니다.

Click the experience algorithm (Random Forest or control) to view the [!UICONTROL Offer Level] report.

![](assets/ap_OfferLevelRpt.png)

오퍼는 보고서 그룹 내에서 표시할 수 있으며 이러한 보고서 그룹은 축소하고 확장할 수 있습니다. 롤업된 정보를 오퍼별로가 아니라 그룹별로 보려면 드롭다운 목록에서 [!UICONTROL 보고 그룹]을 선택하십시오.

>[!NOTE]
>
>시계 아이콘은 알고리즘 모델이 여전히 빌드 중임을 나타냅니다. 확인 표시 아이콘은 기본 알고리즘이 설정되었음을 나타냅니다.

## 자동화된 세그먼트

자동화된 세그먼트 [!UICONTROL 아이콘을] 클릭합니다. 이 보고서는 서로 다른 방문자가 AP/AT 활동의 오퍼/경험에 어떻게 다르게 반응하는지를 보여줍니다. 이 보고서는 Target의 개인화 모델에 정의된 다른 자동화된 세그먼트가 활동의 오퍼/경험에 응답하는 방식을 보여 줍니다.

![자동화된 세그먼트 아이콘](/help/c-reports/assets/icon-automated-sements-ap.png)

자세한 내용은 [자동화된 세그먼트 보고서를 참조하십시오](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## 중요 속성

중요 속성 [!UICONTROL 아이콘을] 클릭합니다. 이 보고서는 다양한 활동에서 모델이 개인화하는 방식에 대해 서로 다른 속성이 더 중요하거나 덜 중요한 방법을 보여줍니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다.

![중요 속성 아이콘](/help/c-reports/assets/icon-important-attributes-ap.png)

자세한 내용은 [중요 속성 보고서를 참조하십시오](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md).