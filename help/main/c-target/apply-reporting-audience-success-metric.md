---
keywords: 타깃팅;대상;보고;성공 지표
description: 에서 성공 지표를 선택하는 방법을 알아봅니다 [!DNL Adobe Target] 사용자를 보고 대상이 될 수 있도록 합니다.
title: 성공 지표에 보고 대상을 적용할 수 있습니까?
feature: Success Metrics
exl-id: 6b2f6669-6178-4da4-850d-8b1ce796a50d
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 54%

---

# 성공 지표에 보고 대상 적용

사용자를 보고 대상이 될 수 있도록 하는 성공 지표를 선택하십시오 [!DNL Adobe Target].

[!UICONTROL 적용 대상] 드롭다운 목록을 사용하면 모든 활동에서 대상을 성공 지표에 적용하여 성공 지표에 도달한 후 및 그 이후의 작업에서 보고된 수치를 확인할 수 있습니다.

![](assets/success_metric.png)

예를 들어, 홈 페이지에서 들어가서 전환 페이지에 도달하는 모든 방문자를 위한 활동을 만들었지만, 전환하기 전에 50달러 이상을 장바구니에 추가한 방문자를 더 자세히 드릴다운하고 싶은 경우를 가정할 수 있습니다.

다음 [!UICONTROL 적용 위치] 드롭다운 목록은 다음 세 가지 카테고리를 잠재적으로 제공합니다. 활동의 모든 방문자, 활동의 특정 단계에 도달하는 방문자만 또는 전환에 도달한 방문자만 또는 다른 식으로 구문을 지정하기 위해서는 방문자가 활동의 시작 페이지에 있는 mbox나, 활동 중간에 있는 어떤 시점을 정의하는 mbox 또는 활동의 끝에 있는 전환 mbox에 도달했어야 한다고 지정할 수 있습니다.

[성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)는 활동에 대해 구성한 경우에만 사용할 수 있습니다. 성공 지표를 정의하지 않은 경우 드롭다운 목록에 다음 두 가지 옵션만 표시됩니다. [!UICONTROL 캠페인 시작] 및 [!UICONTROL 전환].

보고 대상을 성공 지표에 적용할 때에는 다음 정보를 고려하십시오.

* 적용된 성공 지표를 사용한 작업 전 작업의 경우, [!DNL Target] 세그먼트화된 대상은 적용하지 않습니다.
* 적용된 성공 지표 이후의 작업의 경우, [!DNL Target] 세그먼트화된 대상을 적용합니다.

보고에서 세그멘테이션을 보려면 [!UICONTROL Audience] 활동의 보고서에 있는 드롭다운 목록입니다.

![](assets/reporting_audience_dropdown.png)
