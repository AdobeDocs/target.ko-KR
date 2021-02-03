---
keywords: Target;보고서;보고서 설정;여러 지표;지표;표시 지표;숨겨진 지표;;reports;report settings;multiple metrics;metrics;showled metrics;hidden metrics
description: Adobe Target을 사용하여 보고서에서 볼 지표를 여러 개 선택합니다.
title: 보고서에서 여러 지표 보기를 참조하십시오
feature: Reports
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 62%

---


# 보고서에서 여러 지표 보기{#view-multiple-metrics-in-a-report}

여러 지표를 선택하여 [!DNL Adobe Target] 보고서에서 볼 수 있습니다.

보고서에서 여러 지표로 작업할 때는 다음 정보를 유념하십시오.

* 여러 지표를 보는 기능은 [A/B 테스트](/help/c-activities/t-test-ab/test-ab.md), [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [자동 Target](/help/c-activities/auto-target/auto-target-to-optimize.md) 및 [경험 타깃팅](/help/c-activities/t-experience-target/experience-target.md)(XT) 활동에만 사용할 수 있습니다.
* Target](/help/c-integrating-target-with-mac/a4t/a4t.md)(A4T)에 대해 [Analytics를 사용하는 활동에 대해서는 보고서에 20개 이상의 지표를 추가할 수 없습니다. A4T를 사용하지 않는 *A1/>이(가) 아닌 활동에 대한 보고서에 활동에 있는 만큼 지표를 추가할 수 있습니다.*
* 여러 지표를 선택한 경우 보고서를 CSV로 다운로드하는 데 [](/help/c-reports/downloading-data-in-csv-file.md)다운로드 선택 사항을 사용할 수 없습니다. [!UICONTROL 다운로드] 선택 사항을 활성화하려면 하나의 지표만 선택해야 합니다.
* 2015년 7월 [!DNL Target] 릴리스(2015년 7월 30일) 전에 만든 활동에 대한 여러 지표를 볼 수 없습니다.

**보고서에 표시할 지표를 여러 개 선택하려면 다음을 수행하십시오.**

1. 보고서를 표시하려면 **[!UICONTROL 활동]**&#x200B;을 클릭하고 목록에서 원하는 활동을 클릭한 다음, **[!UICONTROL 보고서]** 탭을 클릭하십시오.
1. **[!UICONTROL 보고서 지표]** 드롭다운 목록을 클릭하여 [!UICONTROL 표시된 지표] 및 [!UICONTROL 숨겨진 지표] 목록을 표시합니다.

   ![](assets/multiple_metrics.png)

   [!UICONTROL 검색] 상자를 사용하여 사용 가능한 지표를 빠르게 찾아 [!UICONTROL 표시된 지표] 목록에 추가할 수 있습니다.

   보고서의 [!UICONTROL 표 보기]와 [!UICONTROL 그래프 보기], 이 두 모드에서 여러 지표를 선택할 수 있습니다.

1. [!UICONTROL 숨겨진 지표] 목록의 원하는 지표 위에 마우스 포인터를 놓은 다음 **[!UICONTROL 선택]**&#x200B;을 클릭하여 [!UICONTROL 표시된 지표] 목록으로 이동합니다.

   또는

   [!UICONTROL 숨겨진 지표] 목록에서 원하는 지표를 [!UICONTROL 표시된 지표] 목록으로 드래그하여 놓으십시오.

   [!UICONTROL 표시된 지표] 목록에 지표가 하나 이상 있어야 합니다.

   [!UICONTROL 표시된 지표] 목록에서 지표를 원하는 순서로 드래그하여 놓아 지표들을 다시 정렬할 수 있습니다. 선택한 순서는 [!UICONTROL 테이블 보기] 및 [!UICONTROL 그래프 보기]에 반영됩니다. [!UICONTROL 표시된 지표] 목록에서 지표를 제거하려면 지표를 마우스 포인터로 가리킨 다음, **X** 아이콘을 클릭하십시오.

1. 완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
1. (조건부) [!UICONTROL 테이블 보기]에서 보고서를 보는 동안 지표의 열 머리글에 마우스 포인터를 올려 놓아 파란색 화살표를 표시합니다. 이 화살표를 클릭하여 해당 지표에 대한 [!UICONTROL 상승도] 및 [!UICONTROL 신뢰도]를 표시하도록 표를 확장하십시오.

   ![](assets/multiple_metrics_table.png)

   한 번에 하나의 지표/열만 확장할 수 있습니다. 열을 축소하려면 화살표를 다시 클릭하십시오.

1. (조건부) 그래프 보기에서 보고서를 보는 동안 드롭다운 목록에서 표시할 개별 지표를 선택할 수 있습니다.

   ![](assets/multiple_metrics_graph.png)

