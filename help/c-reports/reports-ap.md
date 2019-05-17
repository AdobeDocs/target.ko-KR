---
description: 자동화된 개인화 사용자는 전문 보고서를 사용할 수 있습니다.
keywords: 타깃팅;AP 보고서;자동화된 개인화 보고서;활동 수준 보고서;오퍼 수준 보고서;오퍼 세부 사항 보고서
seo-description: 자동화된 개인화 사용자는 전문 보고서를 사용할 수 있습니다.
seo-title: 자동화된 개인화 요약 보고서
solution: Target
title: 자동화된 개인화 요약 보고서
title-outputclass: premium
uuid: 959b6814-9686-4741-8a79-5957e64f6209
badge: premium
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) 자동화된 개인화 요약 보고서{#automated-personalization-summary-reports}

자동화된 개인화 사용자는 전문 보고서를 사용할 수 있습니다.

>[!NOTE]
>
>자동화된 개인화는 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에는 포함되어 있지 않습니다.

1. **[!UICONTROL 활동]**을 클릭하고 목록에서 원하는 [!UICONTROL 자동화된 개인화] 활동을 클릭한 다음, **보고서[!UICONTROL 탭을 클릭합니다.]**

   많은 활동이 있는 경우 [!UICONTROL 유형] 드롭다운 목록에서 [!UICONTROL 자동화된 개인화]를 선택하여 목록을 필터링할 수 있습니다.

1. (선택 사항) 사용 가능한 모든 성공 지표로 구분된 요약 보기(예를 들어 통제 트래픽과 타깃팅된 트래픽 비교)를 다운로드하려면 [!UICONTROL 다운로드] 아이콘을 클릭하십시오.

>[!NOTE]
>
>[!UICONTROL 설정] 아이콘은 [!UICONTROL 자동화된 개인화] 보고서에 사용할 수 없습니다.

[!UICONTROL 자동화된 개인화]는 다음 보고서를 제공합니다.

## 활동 수준 보고서 {#section_6F72FC5C790B4492B3DCECBFFA971337}

[!UICONTROL 활동 수준] 보고서에서는 [!UICONTROL 자동화된 개인화] 알고리즘을 사용하는 합계 성과를 무작위로 제공된 컨텐츠(통제 컨텐츠)에 비교합니다.

![](assets/box_plot_ap.jpg)

상승도, 신뢰도, 트렌드, 지속 기간 등을 포함하여 A/B 테스트에 대한 결과 해석의 표준 규칙이 여전히 적용됩니다. 결과 해석에 대한 자세한 내용은 [전환율에 대하여](../c-reports/conversion-rate.md#concept_2D9FEDE8F94A485DAC86D611BFBDC844)를 참조하십시오.

## 오퍼 수준 보고서 {#section_CAA6409879E349C6906E2BE8156D87A1}

랜덤 포레스트 경험에 대한 [!UICONTROL 오퍼 수준] 보고서는 알고리즘이 적용된 각 오퍼의 성과를 무작위로 제공된 동일한 오퍼(통제 오퍼)에 비교합니다. 따라서 이 보기에서 오퍼는 서로 비교되지 않습니다. 아래 예에서는 오퍼 D가 무작위로 제공될 때(통제)와는 대조적으로 알고리즘 논리(랜덤 포레스트)에 따라 제공될 때 12.43% 상승도를 표시하도록 지정할 수 있습니다.

[오퍼 수준] 보고서를 보려면 경험 알고리즘(랜덤 포레스트 또는 통제)을 클릭하십시오.

![](assets/ap_OfferLevelRpt.png)

오퍼는 보고서 그룹 내에서 표시할 수 있으며 이러한 보고서 그룹은 축소하고 확장할 수 있습니다. 롤업된 정보를 오퍼별로가 아니라 그룹별로 보려면 드롭다운 목록에서 [!UICONTROL 보고 그룹]을 선택하십시오.

>[!NOTE]
>
>시계 아이콘은 알고리즘 모델이 여전히 빌드 중임을 나타냅니다. 확인 표시 아이콘은 기본 알고리즘이 설정되었음을 나타냅니다.

