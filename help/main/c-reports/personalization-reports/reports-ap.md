---
keywords: 타깃팅;AP 보고서;자동화된 개인화 보고서;활동 수준 보고서;오퍼 수준 보고서;오퍼 세부 사항 보고서;faq
description: Adobe Target에서 Automated Personalization 요약 보고서를 해석하는 방법에 대해 알아봅니다. 이 보고서에서 자동화된 세그먼트 및 중요 속성 보고서로 전환할 수 있습니다.
title: Automated Personalization 요약 보고서는 어떻게 사용합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
feature: Reports
exl-id: 2708eba4-72d5-4e6b-b01b-d27de03463b2
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 11%

---

# Automated Personalization 요약 보고서

전문 요약 보고서는 [!DNL Adobe Target]에서 [!UICONTROL Automated Personalization] 활동의 사용자가 사용할 수 있습니다.

>[!NOTE]
>
>[!UICONTROL Automated Personalization]은(는) [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. [Target Premium 라이선스](/help/main/c-intro/intro.md#premium)가 없는 [!DNL Target Standard]에는 포함되지 않습니다.

1. **[!UICONTROL Activities]**&#x200B;을(를) 클릭하고 목록에서 원하는 [!UICONTROL Automated Personalization] 활동을 클릭한 다음 **[!UICONTROL Reports]** 탭을 클릭합니다.

   많은 활동이 있는 경우 [!UICONTROL Type] 드롭다운 목록에서 [!UICONTROL Automated Personalization]을(를) 선택하여 목록을 필터링할 수 있습니다.

1. (선택 사항) 사용 가능한 모든 성공 지표로 분류된 요약 보기(예: 제어 및 타깃팅된 트래픽 비교)를 다운로드하려면 **[!UICONTROL Download]** 아이콘을 클릭합니다.

[!UICONTROL Automated Personalization]은(는) 다음 보고서를 제공합니다.

* 활동 수준
* 오퍼 수준
* 자동화된 세그먼트
* 중요 속성

## 활동 수준 보고서 {#section_6F72FC5C790B4492B3DCECBFFA971337}

[!UICONTROL Activity Level] 보고서는 [!UICONTROL Automated Personalization] 알고리즘 사용의 집계 성과를 임의로 제공된 콘텐츠(제어)와 비교합니다.

![활동 수준 보고서](/help/main/c-reports/assets/box_plot_ap.png)

상승도, 신뢰도, 트렌드, 지속 기간 등을 포함하여 A/B 테스트에 대한 결과 해석의 표준 규칙이 여전히 적용됩니다. 결과 해석에 대한 자세한 내용은 [A/Bn 테스트의 통계 계산](/help/main/c-reports/statistical-methodology/statistical-calculations.md)을 참조하십시오.

## 오퍼 수준 보고서 {#section_CAA6409879E349C6906E2BE8156D87A1}

Random Forest 경험에 대한 [!UICONTROL Offer Level] 보고서는 각 알고리즘이 적용한 오퍼의 성능을 임의로 제공된 동일한 오퍼(제어)와 비교합니다. 따라서 이 보기에서 오퍼를 서로 비교해서는 안 됩니다.

[!UICONTROL Offer Level] 보고서를 보려면 경험 알고리즘(Random Forest 또는 컨트롤)을 클릭하십시오.

![Adobe Target의 오퍼 수준 보고서](/help/main/c-reports/assets/ap_OfferLevelRpt.png)

>[!NOTE]
>
>시계 아이콘은 알고리즘 모델이 여전히 빌드 중임을 나타냅니다. 확인 표시 아이콘은 기본 알고리즘이 설정되었음을 나타냅니다.

오퍼가 [보고 그룹](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md) 내에 표시될 수 있으며 이러한 보고 그룹을 축소 및 확장할 수 있습니다. 테이블에서 **[!UICONTROL Control]** 또는 **[!UICONTROL Targeted]**&#x200B;을(를) 클릭하여 오퍼가 아닌 보고 그룹별로 롤업된 정보를 봅니다.

## 자동화된 세그먼트

[!UICONTROL Automated Segments] 아이콘을 클릭합니다. 이 보고서는 서로 다른 방문자가 AP/AT 활동의 오퍼/경험에 어떻게 다르게 반응하는지를 보여 줍니다. 이 보고서는 Target의 개인화 모델에 정의된 다른 자동화된 세그먼트가 활동의 오퍼/경험에 응답하는 방식을 보여 줍니다.

![자동화된 세그먼트 아이콘](/help/main/c-reports/assets/icon-automated-sements-ap.png)

자세한 내용은 [자동화된 세그먼트 보고서](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md)를 참조하십시오.

## 중요 속성

[!UICONTROL Important Attributes] 아이콘을 클릭합니다. 이 보고서는 다른 활동에서 다른 속성이 모델이 개인화를 결정하는 방법에 대해 얼마나 중요한지 (또는 덜 중요한지) 보여줍니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다.

![중요 특성 아이콘](/help/main/c-reports/assets/icon-important-attributes-ap.png)

자세한 내용은 [중요 특성 보고서](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md)를 참조하십시오.

## 자주 묻는 질문

### 활동 수준 보고서와 오퍼 수준 보고서 간에 데이터에 차이가 있는 이유는 무엇입니까?

**[!UICONTROL Activity Level]보고서**: [!UICONTROL Activity Level] 보고서에 기록된 방문 횟수는 제어 경험과 &quot;대상&quot; 트래픽에 대한 방문 횟수를 캡처합니다. 타깃팅된 트래픽에는 탐색 트래픽과 개인화된 트래픽이 혼합되어 있습니다.

**오퍼 수준 보고서**: [!UICONTROL Offer Level] 보고서에 기록된 노출 횟수는 각 오퍼의 노출 횟수를 캡처합니다. 따라서 둘 이상의 위치가 있는 활동에서 모든 보고 그룹의 [!UICONTROL Offer Level] 보고서에 기록된 총 방문 수는 [!UICONTROL Activity Level] 보고서의 제어 또는 타깃팅된 트래픽에 기록된 방문 수의 배수와 활동의 총 위치 수의 곱과 같습니다. 기본 컨텐츠를 사용할 수 있는 옵션이 있었던 위치에서 발생하는 기본 컨텐츠의 노출은 &quot;기본 컨텐츠&quot; 오퍼 그룹에 기록됩니다. 보고 그룹에 할당되지 않은 오퍼의 노출 횟수는 &quot;그룹화되지 않은&quot; 오퍼 그룹에 기록됩니다.

>[!NOTE]
>
>[!UICONTROL Offer Level] 보고서에 기록된 노출 횟수는 [!UICONTROL Activity Level] 보고서에 기록된 방문 횟수의 정수가 아닐 수 있습니다. 이는 인터넷의 보고 데이터 트래픽 캡처에서 발생하는 사소한 불일치(일반적인 불일치율은 5% 미만)에 기인합니다. 따라서 활동이 활성화된 후 활동에서 사용 가능한 위치 수가 변경될 때 노출 수가 정확한 배수가 되지 않습니다.
