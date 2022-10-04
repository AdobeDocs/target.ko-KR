---
keywords: 타깃팅;AP 보고서;자동화된 개인화 보고서;활동 수준 보고서;오퍼 수준 보고서;오퍼 세부 사항 보고서;faq
description: Adobe Target에서 Automated Personalization 요약 보고서를 해석하는 방법을 알아봅니다. 이 보고서에서 자동화된 세그먼트 및 중요 속성 보고서로 전환할 수 있습니다.
title: Automated Personalization 요약 보고서를 어떻게 사용합니까?
feature: Reports
exl-id: 2708eba4-72d5-4e6b-b01b-d27de03463b2
source-git-commit: d90e541588f51e16dd9b11ead1ece77e9ca1408b
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 39%

---

# ![PREMIUM](/help/main/assets/premium.png) 자동화된 개인화 요약 보고서

전문 요약 보고서는 [!UICONTROL Automated Personalization] 활동 [!DNL Adobe Target].

>[!NOTE]
>
>[!UICONTROL 자동화된 개인화]는 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. [!DNL Target Standard]Target Premium 라이센스가 없는 [에는 포함되어 있지 않습니다](/help/main/c-intro/intro.md#premium).

1. **[!UICONTROL 활동]**&#x200B;을 클릭하고 목록에서 원하는 [!UICONTROL 자동화된 개인화] 활동을 클릭한 다음, **[!UICONTROL 보고서 탭을 클릭합니다.]**

   많은 활동이 있는 경우 [!UICONTROL 유형] 드롭다운 목록에서 [!UICONTROL 자동화된 개인화]를 선택하여 목록을 필터링할 수 있습니다.

1. (선택 사항) 사용 가능한 모든 성공 지표로 구분된 요약 보기(예를 들어 통제 트래픽과 타깃팅된 트래픽 비교)를 다운로드하려면 **[!UICONTROL 다운로드]** 아이콘을 클릭하십시오.

[!UICONTROL 자동화된 개인화]는 다음 보고서를 제공합니다.

* 활동 수준
* 오퍼 수준
* 자동화된 세그먼트
* 중요 속성

## 활동 수준 보고서 {#section_6F72FC5C790B4492B3DCECBFFA971337}

[!UICONTROL 활동 수준] 보고서에서는 [!UICONTROL 자동화된 개인화] 알고리즘을 사용하는 합계 성과를 무작위로 제공된 컨텐츠(통제 컨텐츠)에 비교합니다.

![활동 수준 보고서](/help/main/c-reports/assets/box_plot_ap.png)

상승도, 신뢰도, 트렌드, 지속 기간 등을 포함하여 A/B 테스트에 대한 결과 해석의 표준 규칙이 여전히 적용됩니다. 결과 해석에 대한 자세한 내용은 [A/B 테스트의 통계적 계산](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## 오퍼 수준 보고서 {#section_CAA6409879E349C6906E2BE8156D87A1}

랜덤 포레스트 경험에 대한 [!UICONTROL 오퍼 수준] 보고서는 알고리즘이 적용된 각 오퍼의 성과를 무작위로 제공된 동일한 오퍼(통제 오퍼)에 비교합니다. 따라서 이 보기에서 오퍼는 서로 비교되지 않습니다.

경험 알고리즘(Random Forest 또는 Control)을 클릭하여 [!UICONTROL 오퍼 수준] 보고서 세트에 대해 설명합니다.

![](/help/main/c-reports/assets/ap_OfferLevelRpt.png)

오퍼는 보고서 그룹 내에서 표시할 수 있으며 이러한 보고서 그룹은 축소하고 확장할 수 있습니다. 롤업된 정보를 오퍼별로가 아니라 그룹별로 보려면 드롭다운 목록에서 [!UICONTROL 보고 그룹]을 선택하십시오.

>[!NOTE]
>
>시계 아이콘은 알고리즘 모델이 여전히 빌드 중임을 나타냅니다. 확인 표시 아이콘은 기본 알고리즘이 설정되었음을 나타냅니다.

## 자동화된 세그먼트

을(를) 클릭합니다. [!UICONTROL 자동화된 세그먼트] 아이콘. 이 보고서는 서로 다른 방문자가 AP/AT 활동의 오퍼/경험에 다르게 응답하는 방식을 보여줍니다. 이 보고서는 Target의 개인화 모델에 정의된 다른 자동화된 세그먼트가 활동의 오퍼/경험에 응답하는 방식을 보여 줍니다.

![자동화된 세그먼트 아이콘](/help/main/c-reports/assets/icon-automated-sements-ap.png)

자세한 내용은 [자동화된 세그먼트 보고서](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md).

## 중요 속성

을(를) 클릭합니다. [!UICONTROL 중요 속성] 아이콘. 이 보고서는 다른 활동에서 모델이 개인화를 결정하는 방법에 대해 다른 속성이 더 중요하거나 덜 중요한 방법을 보여줍니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다.

![중요 속성 아이콘](/help/main/c-reports/assets/icon-important-attributes-ap.png)

자세한 내용은 [중요 속성 보고서](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md).

## FAQ

### 활동 수준 보고서와 오퍼 수준 보고서 간에 데이터에 차이가 있는 이유는 무엇입니까?

**[!UICONTROL 활동 수준] 보고서**: 에 기록된 방문 [!UICONTROL 활동 수준] 보고서는 제어 경험에 대한 방문 수와 &quot;타깃팅된&quot; 트래픽. 타깃팅된 트래픽에는 탐색 트래픽과 개인화된 트래픽이 혼합되어 포함됩니다.

**오퍼 수준 보고서**: 에 기록된 노출 횟수 [!UICONTROL 오퍼 수준] 보고서는 각 오퍼의 노출 횟수를 캡처합니다. 따라서 위치가 두 개 이상인 활동에서는 [!UICONTROL 오퍼 수준] 모든 보고 그룹의 보고서는 제어 또는 타깃팅된 트래픽에 대해 기록된 방문의 수의 배수와 같습니다 [!UICONTROL 활동 수준] 보고서 시간 활동의 총 위치 수를 설정합니다. 기본 콘텐츠가 사용 가능한 옵션인 위치에서 발생하는 기본 콘텐츠의 노출이 &quot;기본 콘텐츠&quot; 오퍼 그룹에 기록됩니다. 보고 그룹에 할당되지 않은 오퍼의 노출은 &quot;그룹화되지 않은&quot; 오퍼 그룹에 기록됩니다.

>[!NOTE]
>
>에 기록된 노출 횟수 [!UICONTROL 오퍼 수준] 보고서는 [!UICONTROL 활동 수준] 보고서 세트에 대해 설명합니다. 이것은 인터넷을 통한 보고 데이터 트래픽 캡처에서 발생하는 사소한 불일치 때문입니다(일반적인 불일치율은 5% 미만). 따라서 활동이 활성화된 후 활동에서 사용할 수 있는 위치 수가 변경된 경우 노출 수가 정확히 배수가 되지 않습니다.
