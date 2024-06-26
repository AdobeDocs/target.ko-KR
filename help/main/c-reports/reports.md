---
keywords: 보고서;IP 주소 차단;IP 주소에서 방문자 차단;보고서 다운로드;csv;보고
description: Adobe에서 보고 기능을 사용하는 방법을 알아봅니다. [!DNL Target] 을 클릭하여 활동의 성과를 검사합니다. 데이터를 기반으로 더 나은 결정을 내려 ROI를 높일 수 있습니다.
title: 보고서를 보려면 어떻게 해야 합니까?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
source-git-commit: a7a03cba466fbe7abfc8eb1f80292e1a2de7fe2d
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 41%

---

# 보고서

보고서는 의 진행 상황과 결과에 대한 정보를 제공합니다. [!DNL Adobe Target] 데이터를 기반으로 결정을 내리는 데 도움이 되는 활동. 보고서 데이터를 통해 활동 종료 시점을 결정하고 우승자인 경험 또는 오퍼를 보여주고 다음 작업을 결정하는 데 필요한 인사이트 또는 통찰력을 제공할 수 있습니다.

## 보고서 표시 {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. **[!UICONTROL Activities]**&#x200B;을 클릭한 다음, 목록에서 원하는 활동을 클릭합니다.

   활동이 많다면 목록에서 옵션을 선택하여 목록을 필터링할 수 있습니다. [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], 및 [!UICONTROL Activity Source] 드롭다운 목록입니다.

   예를 들어 다음을 선택할 수 있습니다 [!UICONTROL A/B Test] 및 [!UICONTROL Experience Targeting] 다음에서 [!UICONTROL Type] 드롭다운 목록 및 [!UICONTROL Live] 다음에서 [!UICONTROL Status] 활성 상태인 A/B 테스트 및 경험 타깃팅 활동만 표시하는 드롭다운 목록입니다.

   다음 그림은 를 보여줍니다. [!UICONTROL Type] 두 가지 유형이 선택된 드롭다운 목록: [!UICONTROL A/B Test] 및 [!UICONTROL Experience Targeting]. A/B 테스트의 세 가지 유형(수동, [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)및 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md))이 기본적으로 선택됩니다. 필요에 따라 하나 이상의 유형을 선택 취소할 수 있습니다.

   ![유형별 보고서 필터링](/help/main/c-reports/assets/report_filters-new.png)

1. 다음을 클릭합니다. **[!UICONTROL Reports]** 탭.

   각 보고서에는 보고서를 이해하는 데 도움이 되는 범례가 포함되어 있습니다.

   ![보고서 범례](/help/main/c-reports/assets/report_menu_bar-new.png)

   범례에는 다음과 같은 정보가 표시됩니다.

   * 활동이 실행된 날짜 범위를 포함한 활동 상태.
   * 다음 [예상 우승 경험](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) (가능한 경우).

   >[!NOTE]
   >
   >경험 결과는 적어도 한 명 이상의 참여자가 경험을 본 후에야 표시됩니다.

1. (선택 사항) 원하는 대로 [보고서를 구성합니다](/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA).
1. (선택 사항) Excel 및 기타 도구에서 분석할 [보고서를 CSV 형식으로 다운로드](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md)합니다.

   다음 옵션을 사용할 수 있습니다.

   * [!UICONTROL Export Report to CSV]
   * [!UICONTROL Export Order Details to CSV]

1. (선택 사항) **[!UICONTROL Table View]** 및 **[!UICONTROL Graph View]** 보고 형식 간에 전환하는 아이콘입니다.

   ![표 및 그래프 보기 아이콘](/help/main/c-reports/assets/table-and-graph-icons.png)

   선택한 보고서 유형에 따라 다른 보기 및 보고서를 사용할 수 있습니다.

   | 보고서 유형 | 보기 |
   | --- | --- |
   | [자동 타겟팅](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | 다음을 클릭합니다. **[!UICONTROL Automated Segments]** 또는 **[!UICONTROL Important Attributes]** 아이콘.<ul><li>다음 [자동화된 세그먼트 보고서](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) 은 서로 다른 방문자가 AP/AT 활동의 오퍼/경험에 어떻게 다르게 반응하는지를 보여 줍니다. 이 보고서는 Target의 개인화 모델에 정의된 다른 자동화된 세그먼트가 활동의 오퍼/경험에 응답하는 방식을 보여 줍니다.</li><li>다음 [중요 속성 보고서](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) 모델이 개인화를 결정하는 방법에 대해 다른 활동에서 다른 속성이 더(또는 덜) 중요한 방법을 보여 줍니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다.</li></ul> |
   | [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | 이외에도 [Automated Personalization 요약 보고서](/help/main/c-reports/personalization-reports/reports-ap.md)를 클릭하고 **[!UICONTROL Automated Segments]** 또는 **[!UICONTROL Important Attributes]** 아이콘.<ul><li>다음 [자동화된 세그먼트 보고서](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) 은 서로 다른 방문자가 AP/AT 활동의 오퍼/경험에 어떻게 다르게 반응하는지를 보여 줍니다. 이 보고서는 Target의 개인화 모델에 정의된 다른 자동화된 세그먼트가 활동의 오퍼/경험에 응답하는 방식을 보여 줍니다.</li><li>다음 [중요 속성 보고서](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) 다른 활동에서 다른 속성이 모델이 개인화를 결정하는 방법에 대해 더(또는 덜) 중요한 방법을 보여 줍니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다.</li></ul> |
   | [다변량 테스트](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | 이외에도 [경험 성과 보고서](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md)를 클릭하고 [위치 기여도](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) 위치별 기여도를 표시하도록 보고서를 전환하는 아이콘입니다. |

## 특정 활동 유형에 대한 추가 보고 정보 {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

이 항목 및 하위 항목의 일반 보고 정보 외에도 개별 활동 유형에만 해당되는 추가 정보가 이 안내서의 다른 곳에 나와 있습니다.

| 활동 유형 | 세부 사항 |
|--- |--- |
| [A/B 테스트](/help/main/c-activities/t-test-ab/test-ab.md) | [!DNL Target]에 사용된 상승도 및 신뢰도와 통계적 접근 방식을 이해하려면 [A/B 테스트 계획](/help/main/c-activities/t-test-ab/sample-size-determination.md)을 참조하십시오. |
| [자동 할당 보고서 해석](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | 의 결과 해석 [!UICONTROL Auto-Allocate] 에서 상승도 및 신뢰도를 포함한 중요한 지표를 검사하여 A/B 활동 [!DNL Target] UI. |
| [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) | 에 대한 정보 [!UICONTROL Summary] at 활동에 대해 보고합니다. 자세한 내용은 [자동 타겟 요약 보고서](/help/main/c-reports/personalization-reports/auto-target-summary-report.md)를 참조하십시오.<br>에 대한 정보 [!UICONTROL Personalization Insights] at 및 AP 활동에 대한 보고서: [!UICONTROL Automated Segments] 보고 및 [!UICONTROL Important Attributes] 보고서. 자세한 내용은 [개인화 통찰력 보고서](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md)를 참조하십시오. |
| [](/help/main/c-activities/t-automated-personalization/automated-personalization.md)자동화된 개인화(AP) | 에 대한 정보 [!UICONTROL Automated Personalization Summary] ap 활동에 대한 보고서: [!UICONTROL Activity Level] 보고 및 [!UICONTROL Offer Level] 보고서. 자세한 내용은 [자동화된 개인화 요약 보고서](/help/main/c-reports/personalization-reports/reports-ap.md)를 참조하십시오.<br>에 대한 정보 [!UICONTROL Personalization Insights] at 및 AP 활동에 대한 보고서: [!UICONTROL Automated Segments] 보고 및 [!UICONTROL Important Attributes] 보고서. 자세한 내용은 [개인화 통찰력 보고서](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md)를 참조하십시오. |
| [](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)다변량 테스트(MVT) | MVT 활동에 대한 두 보고서에 대한 정보: [!UICONTROL Experience Performance] 보고 및 [!UICONTROL Location Contribution] 보고서. 자세한 내용은 [경험 성과 보고서](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) (MVT)와 [위치 기여도 보고서](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) (MVT)를 참조하십시오. |
| [Adobe Target용 보고 소스로서의 Adobe Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | [!DNL Adobe Analytics]를 [!DNL Target]을 위한 보고 소스로 사용하는 것에 대한 정보입니다. A4T를 통해 [!DNL Target] 활동에 대한 [!DNL Analytics] 보고서에 액세스할 수 있습니다. 자세한 내용은 [Analytics for Target(A4T) 보고](/help/main/c-reports/analytics-for-target-a4t-reporting.md)를 참조하십시오. |
| [[!DNL Target] 보고 위치 [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) | 간의 통합에 대한 정보 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} 및 [!DNL Target] 최적화 프로그램에 강력한 분석 및 시간 절약 도구를 제공합니다. |

## 지정된 IP 주소에서 보고 데이터 차단

지정된 IP 주소의 방문자가 보고서에서 계산되지 않도록 차단할 수 있습니다. 예를 들어 내부 방문자의 보고 데이터를 차단하는 데 유용합니다.

[고객 지원 문의](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) IP 필터를 설정합니다. 을 사용하는 경우에는 이 필터링이 적용되지 않습니다 [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T)를 보고 소스로 사용할 때에는 적용되지 않습니다.
