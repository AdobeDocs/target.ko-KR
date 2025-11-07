---
keywords: A4T;Analytics;Analytics for Target;Analytics 보고 소스;Target용 보고 소스로서의 Adobe Analytics;atjs;at.js;Adobe Experience Platform Web SDK;Platform Web SDK;Platform SDK
description: ' [!DNL Analytics] for [!DNL Target] (A4T)을 사용하여 [!DNL Analytics] 전환 지표 및 대상자 세그먼트를 기반으로 하는 활동을 생성하고 [!DNL Analytics] 보고서를 사용하여 결과를 검사할 수 있습니다.'
title: ' [!DNL Analytics] for [!DNL Target] (A4T)이란 무엇입니까?'
feature: Analytics for Target (A4T)
exl-id: 5bb80b03-8209-4932-a838-0e11c5865133
source-git-commit: e45ac15a60c83e35b8b2b2ba29a42727faf746df
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 80%

---

# [!DNL Adobe Target]용 보고 소스로서의 [!DNL Adobe Analytics] (A4T)

[!DNL Adobe Analytics for Target]&#x200B;(A4T)은 [!DNL Analytics] 전환 지표 및 대상자 세그먼트를 기반으로 하는 활동을 생성할 수 있는 솔루션 간 통합입니다. A4T 통합을 통해 [!DNL Analytics] 보고서를 사용하여 결과를 검사할 수 있습니다. 활동용 보고 소스로서의 [!DNL Analytics]를 사용하는 경우 해당 활동에 대한 모든 보고 및 세분화는 [!DNL Analytics] 데이터 수집을 기반으로 합니다.

## 개요 {#section_92B66069210C40DBA937790E8CC596CF}

[!DNL Analytics]와 [!DNL Target] 간의 [!DNL Analytics for Target] 통합은 귀하의 최적화 프로그램에 강력한 분석과 시간 절약에 유용한 도구를 제공합니다.

[!DNL Target]에서 [!DNL Analytics] 데이터를 사용하면 다음과 같은 세 가지 주요 이점이 있습니다.

* 마케터는 언제든지 [!DNL Target] 활동 보고서에 [!DNL Analytics] 성공 지표 또는 보고 세그먼트를 동적으로 적용할 수 있습니다. 활동을 실행하기 전에 모든 항목을 지정할 필요는 없습니다.
* 단일 데이터 소스는 두 개의 개별 시스템에서 데이터를 수집할 때 발생하는 분산을 제거합니다.
* 귀하의 기존 [!DNL Analytics] 구현은 필요한 모든 데이터를 수집합니다. 보고서에 사용할 데이터를 수집할 목적으로 페이지에 mbox를 구현할 필요가 없습니다.

활동용 보고 소스로서의 [!DNL Analytics]를 사용하는 경우 해당 활동에 대한 모든 보고 및 세분화는 [!DNL Analytics]를 기반으로 합니다.

계산된 지표를 포함한 모든 [!DNL Analytics] 지표는 한 가지 예외를 제외하고 [!DNL Target] 및 [!UICONTROL Target Activities]의 [!DNL Analytics] 보고서에서 사용할 수 있습니다. [!UICONTROL Lift & Confidence]에 대한 계산된 지표는 지원되지 않습니다. 마찬가지로 [!DNL Analytics]에서 사용할 수 있는 모든 세그먼트를 각 솔루션에 적용할 수 있습니다. 활동이 시작된 후 또는 활동이 완료된 후 [!DNL Target]의 보고서에 지표 또는 대상자를 적용할 수 있습니다.

[!DNL Analytics]에 기본 제공 사용자 정의 또는 계산된 지표 등 모든 지표가 포함됩니다.

분류 기간 후에 데이터는 웹 사이트에서 수집되고 약 1시간 후에 보고서에 표시됩니다. 보고서에 있는 모든 지표, 세그먼트, 값은 활동을 설정할 때 선택한 보고서 세트에서 가져옵니다.

A4T를 사용하려면 다음 사항을 염두에 두십시오.

* [!DNL Target]용 보고 소스로서의 [!DNL Analytics]를 사용하려면 귀하 및 귀사 모두 [!DNL Analytics] 및 [!DNL Target]에 대한 액세스 권한을 보유해야 합니다. [솔루션이 필요할 경우 계정 담당자에게 문의하십시오.](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB)
* 보고 소스는 각 활동에 대해 설정됩니다. [!DNL Target]은 보고에 사용할 데이터를 계속 수집하며 [!DNL Target]에서 수집된 데이터에 활동의 기반을 두고자 하는 경우 [!DNL Target] 데이터를 계속 사용할 수 있습니다.
* 하나의 보고 소스 또는 다른 보고 소스를 사용하십시오. 두 소스 모두에서 한 활동에 대한 데이터를 수집할 수 없습니다.
* A4T 사용 시 활동에 사용할 수 있는 모든 성공 지표는 [!DNL Analytics] 지표입니다. 그러나 at.js를 사용하는 경우 목표 지표는 mbox 호출을 기반으로 할 수 있습니다. 예를 들어 A4T를 통해 [!DNL Analytics] 클릭 추적 코드를 구현하지 않고도 Target의 획기적인 클릭 추적 기능을 사용할 수 있습니다.
* [!DNL Target] UI에서 A4T 활동의 보고를 보면 [!DNL Analytics] 데이터가 표시됩니다. 예를 들어 [!UICONTROL Visitor]에서 [!DNL Target] 지표를 사용하는 경우 [!DNL Analytics] [!UICONTROL Visitor] 지표가 아닌 [!DNL Target] [!UICONTROL Visitors] 지표를 사용합니다(이제 [!UICONTROL Entrants]). 이 차이는 기본 트래픽 지표([!UICONTROL Visitors], [!UICONTROL Visits], [!UICONTROL Page Views])와 전환 지표에 특히 중요합니다.
* 모든 기존 [!DNL Target] 활동은 계속 [!DNL Target] 데이터 수집을 사용하며 A4T 활성화의 영향을 받지 않습니다.
* A4T 사용 시 하나의 mbox 기반 지표만 허용됩니다.
* [!DNL Target]에서 [!DNL Analytics]로의 서버 간 호출은 [!DNL Analytics]로 활동 및 경험 정보를 전송합니다. 이 통합은 [!DNL Target] 또는 [!DNL Analytics]에 대해 추가 서버 호출을 발생시키지 않습니다.

  경우에 따라 [!DNL Target]에서 [!DNL Analytics]로의 분류가 실패하며 [!DNL Analytics]의 데이터가 활동에 표시되지 않습니다. [Analytics 및 Target 통합 문제 해결 (A4T)](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md)을 참조하십시오. 추가 지원이 필요한 경우 [클라이언트 지원 팀에 문의](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB)할 수도 있습니다.

## A4T 구현

at.js 및 [!DNL Adobe Experience Platform Web SDK]를 통한 A4T 구현에 대한 정보는 [Analytics for [!DNL Target] 구현](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md)을 참조하십시오.

## 지원되는 활동 유형 {#section_F487896214BF4803AF78C552EF1669AA}

다음 섹션에는 [!DNL Adobe Experience Platform Web SDK] 또는 at.js 사용 시 지원되는 활동 유형에 대한 정보가 포함되어 있습니다.

| 활동 유형 | A4T와 호환 가능 | 해당하는 경우 메모 |
|--- |--- |--- |
| [수동 트래픽 분할을 사용하는 A/B 활동](/help/main/c-activities/t-test-ab/test-ab.md) | 예 |  |
| [자동 할당을 사용하는 A/B 활동](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 예 | [자동 할당 및 자동 타겟팅 활동에 대한 A4T 지원](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md)을 참조하십시오. |
| [자동 타겟팅을 사용하는 A/B 활동](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | 예 | 이제 자동 타겟팅 활동에 대한 A4T 지원은 [!DNL Platform Web SDK] 및 at.js 모두에 대해 지원됩니다. |
| [경험 타겟팅(XT)](/help/main/c-activities/t-experience-target/experience-target.md) | 예 |  |
| [다변량 테스트(MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | 예 | [!UICONTROL Element Contribution] 보고서를 가져오려면 mbox 기반 목표 지표 목표가 필요합니다. [!UICONTROL Element Contribution] 보고서는 현재 [!DNL Analytics] 지표를 지원하지 않습니다. |
| [Automated Personalization(AP) 활동](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | 아니요 |  |
| [추천 활동](/help/main/c-recommendations/recommendations.md) | 예 |  |
| [리디렉션 오퍼를 사용하는 모든 활동](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | 예 |  |

일부 활동 유형은 아직 A4T를 지원하지 않으므로 `orderConfirmPage` mbox와 같이 중요한 전환 mbox를 유지하거나 구현하는 것이 좋습니다.

## A4T 보고서의 예 {#section_F0A43A1CB2F04E8282B909E4D7034361}

[!DNL Target]에서 A4T 보고서를 보려면 **[!UICONTROL Activities]**&#x200B;을(를) 클릭하고 [!DNL Analytics]을(를) 보고 소스로 사용하는 목록에서 원하는 활동을 클릭한 다음 **[!UICONTROL Reports]** 탭을 클릭하십시오.

>[!NOTE]
>
>[!UICONTROL Reporting Source] 페이지 상단의 [!UICONTROL Activities] 드롭다운 목록을 사용하여 A4T를 사용하는 활동만 표시할 수 있습니다.

보고서의 오른쪽 상단에 있는 적절한 아이콘을 클릭하여 보고서의 [!UICONTROL Table View]과(와) [!UICONTROL Graph View] 사이를 전환할 수 있습니다.

다음 그림은 사용 가능한 [!UICONTROL Graph View] 목표 지표를 표시하는 [!UICONTROL Report Metric] 드롭다운 목록과 함께 A4T 보고서의 [!DNL Analytics]을(를) 보여 줍니다.

![a4t_report_graph1 이미지](assets/a4t_report_graph1.png)

다음 그림은 사용 가능한 [!UICONTROL Graph View]개의 대상을 표시하는 [!UICONTROL Audience] 드롭다운 목록과 함께 A4T 보고서의 [!DNL Analytics]을(를) 보여 줍니다.

![a4t_report_graph2 이미지](assets/a4t_report_graph2.png)

다음 그림은 A4T 보고서의 [!UICONTROL Table View]을(를) 보여 줍니다.

![a4t_report_table 이미지](assets/a4t_report_table.png)

[!DNL Analytics]이(가) 아닌 [!DNL Target]에서 보고서를 보려면 보고서 상단의 **[!UICONTROL View in Analytics]**&#x200B;을(를) 클릭하십시오.

## Analytics &amp; Target: 분석 모범 사례 튜토리얼 {#section_3438E6E77A464424B717A4FD333B84B2}

[!DNL Adobe Experience League]에서 제공하는 [Analytics &amp; Target: 분석 모범 사례](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) 튜토리얼을 엽니다.

## 교육 비디오:

다음 비디오에는 이 주제에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### Analytics for Adobe Target(A4T) (4:32) ![개요 배지](/help/main/assets/overview.png)

이 비디오는 [!DNL Target]에서 보고 소스로서의 [!DNL Analytics]를 사용하여 최적화 프로그램의 분석을 추진하는 방법에 대해 설명합니다.

* A4T가 무엇이며, 왜 사용해야 하는지에 대해 설명합니다.
* A4T의 작동 방식에 대해 설명합니다.
* A4T를 사용하기 위해 필요한 전제 조건을 이해합니다.

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics/Adobe Target 통합(A4T) (40:33) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오는 Adobe 고객 지원 팀에서 진행한 이니셔티브인 &quot;[운영시간](/help/main/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot; 기록입니다.

* 통합이 작동하도록 설정하고 작동하는지 확인하는 방법
* 통합 작동 방식
* Analytics에서 사용할 이상적인 보고서에 대해 알아보기
* A4T와 관련된 일반적인 질문에 대한 답변

[Analytics/Target 통합(A4T) 운영 시간](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)

>[!MORELIKETHIS]
>
>* [Analytics for [!DNL Target] 구현](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md): at.js 및 Platform Web SDK에 대한 구현 정보가 포함되어 있습니다.
>* [리디렉션 오퍼 - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)
>* [Adobe Experience Platform Web SDK 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html): Platform Web SDK에 대한 개요 정보가 포함되어 있습니다.
>* [Target 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html): [!DNL Target] 및 [!DNL Platform Web SDK]와 관련된 정보가 포함되어 있습니다.
