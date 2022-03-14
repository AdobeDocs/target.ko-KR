---
keywords: 보고서;IP 주소 차단;IP 주소에서 방문자 차단;보고서 다운로드;csv;보고
description: Adobe에서 보고 기능을 사용하는 방법을 알아봅니다 [!DNL Target] 활동의 성과를 검사합니다. 데이터를 기반으로 보다 나은 의사 결정을 하여 ROI를 높일 수 있습니다.
title: 보고서를 보려면 어떻게 해야 합니까?
feature: Reports
exl-id: c5710eb3-0c72-47f8-870d-df50453ecf08
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 62%

---

# 보고서

보고서에는 [!DNL Adobe Target] 데이터를 기반으로 결정을 내리는 데 도움이 되는 활동. 보고서 데이터를 통해 활동을 종료할 시기를 결정하고, 우승자인 오퍼 경험을 보여주고, 다음 작업을 결정하는 데 필요한 인사이트 또는 통찰력을 제공할 수 있습니다.

## 보고서 표시 {#section_C4591A32F6D04C95A1AD5A377C27C28B}

1. **[!UICONTROL 활동]**&#x200B;을 클릭한 다음, 목록에서 원하는 활동을 클릭합니다.

   활동이 많다면 [!UICONTROL 유형], [!UICONTROL 상태], [!UICONTROL 보고 소스], [!UICONTROL 경험 작성기], [!UICONTROL 지표 유형] 및 [!UICONTROL 활동 소스] 드롭다운 목록에서 선택 사항을 선택하여 목록을 필터링할 수 있습니다.

   예를 들어, [!UICONTROL 유형] 드롭다운 목록에서 [!UICONTROL A/B 테스트]와 [!UICONTROL 경험 타깃팅]을 선택하고 [!UICONTROL 상태] 드롭다운 목록에서 [!UICONTROL 라이브]를 선택하여 활성 상태에 있는 A/B 테스트 및 경험 타깃팅 활동만 표시할 수도 있습니다.

   다음 그림은 두 가지 유형이 선택된 [!UICONTROL 유형] 드롭다운 목록을 보여줍니다. [!UICONTROL A/B 테스트] 및 [!UICONTROL 경험 타깃팅]. A/B 테스트의 세 가지 유형(수동, [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)및 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md))이 기본적으로 선택됩니다. 필요에 따라 하나 이상의 유형을 선택 취소할 수 있습니다.

   ![유형별 보고서 필터링](/help/main/c-reports/assets/report_filters-new.png)

1. **[!UICONTROL 보고서]** 탭을 클릭합니다.

   각 보고서에는 보고서를 이해하는 데 도움이 되는 범례가 포함되어 있습니다.

   ![보고서 범례](/help/main/c-reports/assets/report_menu_bar-new.png)

   범례에는 다음과 같은 정보가 표시됩니다.

   * 활동이 실행된 날짜 범위를 포함한 활동 상태.
   * 다음 [예상 우승 경험](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) (가능한 경우)

   >[!NOTE]
   >
   >경험 결과는 적어도 한 명 이상의 참여자가 경험을 본 후에야 표시됩니다.

1. (선택 사항) 원하는 대로 [보고서를 구성합니다](/help/main/c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA).
1. (선택 사항) Excel 및 기타 도구에서 분석할 [보고서를 CSV 형식으로 다운로드](/help/main/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75)합니다.

   다음 옵션을 사용할 수 있습니다.

   * [!UICONTROL 보고서를 CSV로 내보내기]
   * [!UICONTROL 주문 세부 사항을 CSV로 내보내기]

1. (선택 사항) 보고 형식 간에 전환하려면 **[!UICONTROL 표 보기]** 및 **[!UICONTROL 그래프 보기]** 아이콘을 클릭하십시오.

   ![표 및 그래프 보기 아이콘](/help/main/c-reports/assets/table-and-graph-icons.png)

   선택한 보고서 유형에 따라 다른 보기 및 보고서를 사용할 수 있습니다.

   | 보고서 유형 | 보기 |
   | --- | --- |
   | [자동 타기팅](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | 을(를) 클릭합니다. **[!UICONTROL 자동화된 세그먼트]** 또는 **[!UICONTROL 중요 속성]** 아이콘.<ul><li>다음 [자동화된 세그먼트 보고서](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) 는 서로 다른 방문자가 AP/AT 활동의 오퍼/경험에 다르게 응답하는 방식을 표시합니다. 이 보고서는 Target의 개인화 모델에 정의된 다른 자동화된 세그먼트가 활동의 오퍼/경험에 응답하는 방식을 보여 줍니다.</li><li>다음 [중요 속성 보고서](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) 다른 활동에서 모델이 개인화를 결정하는 방법에 대해 다른 속성이 더 중요하거나 덜 중요한 방법을 보여줍니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다.</li></ul> |
   | [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) | 추가 [Automated Personalization 요약 보고서](/help/main/c-reports/reports-ap.md)를 클릭하고 **[!UICONTROL 자동화된 세그먼트]** 또는 **[!UICONTROL 중요 속성]** 아이콘.<ul><li>다음 [자동화된 세그먼트 보고서](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) 는 서로 다른 방문자가 AP/AT 활동의 오퍼/경험에 다르게 응답하는 방식을 표시합니다. 이 보고서는 Target의 개인화 모델에 정의된 다른 자동화된 세그먼트가 활동의 오퍼/경험에 응답하는 방식을 보여 줍니다.</li><li>다음 [중요 속성 보고서](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) 다른 활동에서 다른 속성이 모델이 개인화를 결정하는 방법에 대해 더 중요하거나 덜 중요한 방법을 보여줍니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다.</li></ul> |
   | [다변량 테스트](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) | 추가 [경험 성과 보고서](/help/main/c-reports/experience-performance-report.md)를 클릭하고 [위치 기여도](/help/main/c-reports/location-contribution-report.md) 위치별 기여도를 표시하도록 보고서를 전환하기 위한 아이콘입니다. |

## 특정 활동 유형에 대한 추가 보고 정보 {#section_DFE037B9E1C345D3B3BDFCB3AC0359CA}

이 항목 및 하위 항목의 일반 보고 정보 외에도 개별 활동 유형에만 해당되는 추가 정보가 이 안내서의 다른 곳에 나와 있습니다.

| 활동 유형 | 세부 사항 |
|--- |--- |
| [A/B 테스트](/help/main/c-activities/t-test-ab/test-ab.md) | [!DNL Target]에 사용된 상승도 및 신뢰도와 통계적 접근 방식을 이해하려면 [A/B 테스트 계획](/help/main/c-activities/t-test-ab/sample-size-determination.md)을 참조하십시오. |
| [자동 할당 보고서 해석](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) | 결과의 해석 [!UICONTROL 자동 할당] 상승도 및 신뢰도를 포함한 중요한 지표를 검사하여 A/B 활동 [!DNL Target] UI. |
| [자동 Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) | AT 활동과 관련된 [!UICONTROL 요약] 보고서에 대한 정보입니다. 자세한 내용은 [자동 타겟 요약 보고서](/help/main/c-reports/auto-target-summary-report.md)를 참조하십시오.<br>AT 및 AP 활동에 대한 두 개의 [!UICONTROL 개인화 통찰력 보고서]인 [!UICONTROL 자동화된 세그먼트] 보고서와 [!UICONTROL 중요 속성] 보고서에 대한 정보입니다. 자세한 내용은 [개인화 통찰력 보고서](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md)를 참조하십시오. |
| [](/help/main/c-activities/t-automated-personalization/automated-personalization.md)자동화된 개인화(AP) | AP 활동의 두 개의 [!UICONTROL 자동화된 개인화 요약] 보고서인 [!UICONTROL 활동 수준] 보고서 및 [!UICONTROL 오퍼 수준] 보고서에 대한 정보. 자세한 내용은 [자동화된 개인화 요약 보고서](/help/main/c-reports/reports-ap.md)를 참조하십시오.<br>AT 및 AP 활동에 대한 두 개의 [!UICONTROL 개인화 통찰력 보고서]인 [!UICONTROL 자동화된 세그먼트] 보고서와 [!UICONTROL 중요 속성] 보고서에 대한 정보입니다. 자세한 내용은 [개인화 통찰력 보고서](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md)를 참조하십시오. |
| [](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)다변량 테스트(MVT) | MVT 활동에 대한 두 개 보고서인 [!UICONTROL 경험 성과] 보고서와 및 [!UICONTROL 위치 기여도] 보고서에 대한 정보입니다. 자세한 내용은 [경험 성과 보고서](/help/main/c-reports/experience-performance-report.md) (MVT)와 [위치 기여도 보고서](/help/main/c-reports/location-contribution-report.md) (MVT)를 참조하십시오. |
| [Adobe Target용 보고 소스로서의 Adobe Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) | [!DNL Adobe Analytics]를 [!DNL Target]을 위한 보고 소스로 사용하는 것에 대한 정보입니다. A4T를 통해 [!DNL Target] 활동에 대한 [!DNL Analytics] 보고서에 액세스할 수 있습니다. 자세한 내용은 [Analytics for Target(A4T) 보고](/help/main/c-reports/analytics-for-target-a4t-reporting.md)를 참조하십시오. |

## 지정된 IP 주소에서 보고 데이터 차단

지정된 IP 주소의 방문자가 보고서에서 계산되지 않도록 차단할 수 있습니다. 예를 들어 내부 방문자의 보고 데이터를 차단하는 데 유용합니다.

[Client Care에 문의하여 IP 필터를 설정하십시오. ](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) 이 필터링은 [Target 분석](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) (A4T)를 보고 소스로 사용할 때에는 적용되지 않습니다.
