---
keywords: a4t;analytics;analytics for target;analytics 보고 소스;target용 보고 소스로서의 adobe analytics;at.js;adobe experience platform web sdk;platform sdk
description: 사용 [!DNL Analytics] 대상 [!DNL Target] (A4T)를 기반으로 활동을 만들 수 있습니다 [!DNL Analytics] 전환 지표 및 대상 세그먼트 와 사용 [!DNL Analytics] 결과를 검사할 보고서입니다.
title: 정의 [!DNL Analytics] 대상 [!DNL Target] (A4T)?
feature: Analytics for Target (A4T)
exl-id: 5bb80b03-8209-4932-a838-0e11c5865133
source-git-commit: 14dfc3e19333848e50324a61539ddf693e17d3ce
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 30%

---

# [!DNL Adobe Analytics] 를 [!DNL Adobe Target] (A4T)

[!DNL Adobe Analytics for Target] (A4T)는 을 기반으로 활동을 만들 수 있는 교차 솔루션 통합입니다 [!DNL Analytics] 전환 지표 및 대상 세그먼트 . A4T 통합을 사용하여 다음을 사용할 수 있습니다 [!DNL Analytics] 보고서를 사용하여 결과를 검사합니다. 만약 [!DNL Analytics] 활동의 보고 소스로 해당 활동의 모든 보고 및 세그멘테이션은 [!DNL Analytics] 데이터 수집.

## 개요 {#section_92B66069210C40DBA937790E8CC596CF}

다음 [!DNL Analytics for Target] 통합 간 [!DNL Analytics] 및 [!DNL Target] 은 최적화 프로그램을 위한 강력한 분석 및 시간 절약 도구를 제공합니다.

를 사용하면 다음과 같은 세 가지 주요 이점이 있습니다 [!DNL Analytics] 데이터 입력 [!DNL Target] 입니다.

* 마케터는 동적으로 적용할 수 있습니다 [!DNL Analytics] 성공 지표 또는 보고 세그먼트를 [!DNL Target] 활동은 언제든지 보고합니다. 활동을 실행하기 전에 모든 항목을 지정할 필요는 없습니다.
* 단일 데이터 소스는 두 개의 개별 시스템에서 데이터를 수집할 때 발생하는 분산을 제거합니다.
* 기존 [!DNL Analytics] 구현은 필요한 모든 데이터를 수집합니다. 보고서에 사용할 데이터를 수집할 목적으로 페이지에 mbox를 구현할 필요가 없습니다.

만약 [!DNL Analytics] 활동의 보고 소스로 해당 활동의 모든 보고 및 세그멘테이션은 [!DNL Analytics].

모두 [!DNL Analytics] 계산된 지표를 포함한 지표는에서 사용할 수 있습니다. [!DNL Target] 그리고 [!UICONTROL Target 활동] 보고서 위치 [!DNL Analytics]( 한 가지 예외 포함). 에 대한 계산된 지표 [!UICONTROL 상승도 및 신뢰도] 지원되지 않습니다. 마찬가지로, 에서 사용할 수 있는 모든 세그먼트도 있습니다 [!DNL Analytics] 두 솔루션에 모두 적용할 수 있습니다. 의 보고서에 지표나 대상을 적용할 수 있습니다 [!DNL Target] 활동이 시작된 후 또는 활동이 완료된 후에도 계속 활동을 진행할 수 있습니다.

내장된 사용자 지정 지표 또는 계산된 지표를 포함하여 모든 지표가 포함됩니다 [!DNL Analytics].

분류 기간 후에 데이터는 웹 사이트에서 수집되고 약 1시간 후에 보고서에 표시됩니다. 보고서에 있는 모든 지표, 세그먼트, 값은 활동을 설정할 때 선택한 보고서 세트에서 가져옵니다.

A4T를 사용하려면 다음 사항을 염두에 두십시오.

* 를 사용하려면 [!DNL Analytics] 를 [!DNL Target], 회사와 회사 모두 [!DNL Analytics] 및 [!DNL Target]. [솔루션이 필요할 경우 계정 담당자에게 문의하십시오.](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB)
* 보고 소스는 각 활동에 대해 설정됩니다. [!DNL Target] 는 보고 및 [!DNL Target] 에서 수집한 데이터에 대한 활동을 기반으로 하려는 경우에도 데이터를 계속 사용할 수 있습니다 [!DNL Target].
* 한 보고 소스 또는 다른 보고 소스를 사용합니다. 두 소스 모두에서 한 활동에 대한 데이터를 수집할 수 없습니다.
* A4T를 사용할 때 활동에 사용할 수 있는 모든 성공 지표는 다음과 같습니다 [!DNL Analytics] 지표 를 참조하십시오. 그러나 at.js를 사용하는 경우 목표 지표는 mbox 호출을 기반으로 할 수 있습니다. 예를 들어 Target을 구현할 필요 없이 A4T와 함께 기본적으로 제공되는 클릭 추적 기능을 사용할 수 있습니다 [!DNL Analytics] 클릭 추적 코드.
* 에서 A4T 활동 보고를 볼 때 [!DNL Target] UI, 보고 있습니다. [!DNL Analytics] 데이터. 예를 들어 [!UICONTROL 방문자] 의 지표 [!DNL Target]를 사용 중입니다. [!DNL Analytics] [!UICONTROL 방문자] 지표가 아니라 지표입니다 [!DNL Target] [!UICONTROL 방문자 수] 이제 라고 하는 지표 [!UICONTROL 참여자]. 이 차이는 특히 기본 트래픽 지표([!UICONTROL 방문자 수], [!UICONTROL 방문 횟수], [!UICONTROL 페이지 보기 수]) 및 전환 지표.
* 기존 [!DNL Target] 활동은 계속 사용 [!DNL Target] 데이터 수집은 A4T를 활성화해도 영향을 받지 않습니다.
* A4T를 사용할 때에는 하나의 mbox 기반 지표만 허용됩니다.
* 에서 서버 간 호출 [!DNL Target] to [!DNL Analytics] 에 활동 및 경험 정보를 보냅니다. [!DNL Analytics]. 이 통합은 다음 중 하나에 대한 추가 서버 호출을 발생시키지 않습니다 [!DNL Target] 또는 [!DNL Analytics].

   경우에 따라 분류는 [!DNL Target] to [!DNL Analytics] 실패 및 활동에 데이터가 표시되지 않음 [!DNL Analytics]. 자세한 내용은 [Analytics 및 Target 통합 문제 해결(A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). 다음을 수행할 수도 있습니다 [Client Care에 문의하십시오](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) 추가 지원

## A4T 구현

at.js 및 [!DNL Adobe Experience Platform Web SDK]를 참조하십시오. [Analytics for [!DNL Target] 구현](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## 지원되는 활동 유형 {#section_F487896214BF4803AF78C552EF1669AA}

다음 섹션에는 를 사용할 때 지원되는 활동 유형에 대한 정보가 포함되어 있습니다 [!DNL Adobe Experience Platform Web SDK] 또는 at.js:

| 활동 유형 | A4T와 호환 가능 | 해당하는 경우 메모 |
|--- |--- |--- |
| [수동 트래픽 분할을 사용하는 A/B 활동](/help/c-activities/t-test-ab/test-ab.md) | 예 |  |
| [자동 할당을 사용하는 A/B 활동](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 예 | 자세한 내용은 [A4T에서 자동 할당 및 자동 Target 활동을 지원합니다](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md) |
| [자동 타겟을 사용하는 A/B 활동](/help/c-activities/auto-target/auto-target-to-optimize.md) | 예 | 자세한 내용은 [A4T에서 자동 할당 및 자동 Target 활동을 지원합니다](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |
| [경험 타기팅 (XT)](/help/c-activities/t-experience-target/experience-target.md) | 예 |  |
| [다변량 테스트(MVT)](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | 예 | 다음을 얻기 위해 mbox 기반 목표 지표 목표를 필요로 합니다. [!UICONTROL 요소 기여도] 보고서 세트에 대해 설명합니다. 다음 [!UICONTROL 요소 기여도] 보고서가 현재 지원되지 않음 [!DNL Analytics] 지표 를 참조하십시오. |
| [자동화된 개인화(AP) 활동](/help/c-activities/t-automated-personalization/automated-personalization.md) | 아니오 |  |
| [권장 사항 활동](/help/c-recommendations/recommendations.md) | 예 |  |
| [리디렉션 오퍼를 사용하는 모든 활동](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | 예 |

모든 활동 유형은 아직 A4T를 지원하지 않으므로 와 같은 중요한 전환 mbox를 유지 또는 구현하는 것이 좋습니다. `orderConfirmPage` mbox를 참조하십시오.

## A4T 보고서의 예 {#section_F0A43A1CB2F04E8282B909E4D7034361}

에서 A4T 보고서를 보려면 [!DNL Target]를 클릭합니다. **[!UICONTROL 활동]**&#x200B;를 사용하는 목록에서 원하는 활동을 클릭합니다. [!DNL Analytics] 를 보고 소스로 설정한 다음 **[!UICONTROL 보고서]** 탭.

>[!NOTE]
>
>를 사용할 수 있습니다 [!UICONTROL 보고 소스] 맨 위에 있는 드롭다운 목록 [!UICONTROL 활동] A4T를 사용하는 활동만 표시할 수 있습니다.

간을 전환할 수 있습니다 [!UICONTROL 테이블 보기] 및 [!UICONTROL 그래프 보기] 보고서의 오른쪽 위에서 적절한 아이콘을 클릭하여 표시합니다.

다음 그림은 사용 가능한 [!UICONTROL  목표 지표를 표시하는 ]보고서 지표[!UICONTROL  드롭다운 목록과 함께 A4T 보고서의 ]그래프 보기[!DNL Analytics]를 보여줍니다.

![](assets/a4t_report_graph1.png)

다음 그림은 사용 가능한  대상을 표시하는 [!UICONTROL 대상] 드롭다운 목록과 함께 A4T 보고서의 [!DNL Analytics]그래프 보기를 보여줍니다.

![](assets/a4t_report_graph2.png)

다음 그림은 A4T 보고서의 [!UICONTROL 표 보기]를 보여줍니다.

![](assets/a4t_report_table.png)

[!DNL Analytics]이 아니라 [!DNL Target]에서 보고서를 보려면 보고서 맨 위의 **** Analytics에서 보기를 클릭하십시오.

## Analytics &amp; Target: 분석 우수 사례 자습서 {#section_3438E6E77A464424B717A4FD333B84B2}

를 엽니다. [Analytics 및 Target: 분석 우수 사례](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) 튜토리얼, 제공 [!DNL Adobe Experience League].

## 교육 비디오:

다음 비디오에는 이 항목에서 설명하는 개념에 대한 자세한 정보가 포함되어 있습니다.

### Analytics for Adobe Target (A4T) (4:32) ![개요 배지](/help/assets/overview.png)

다음 비디오에서는 을 사용하는 방법을 설명합니다 [!DNL Analytics] 를 의 보고 소스로 사용 [!DNL Target] 최적화 프로그램의 분석을 유도합니다.

* A4T가 무엇이며, 왜 사용해야 하는지에 대해 설명합니다.
* A4T의 작동 방식에 대해 설명합니다.
* A4T를 사용하기 위해 필요한 전제 조건을 이해합니다.

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics/Adobe Target 통합(A4T) (40:33) ![튜토리얼 배지](/help/assets/tutorial.png)

이 비디오는 Adobe 고객 지원 팀에서 진행한 이니셔티브인 &quot;[운영시간](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot; 기록입니다.

* 통합이 작동하도록 설정하고 작동하는지 확인하는 방법
* 통합 작동 방식
* Analytics에서 사용할 이상적인 보고서에 대해 알아보기
* A4T와 관련된 일반적인 질문에 대한 답변

[Analytics/Target 통합(A4T) 운영 시간](https://helpx.adobe.com/kr/customer-care-office-hours/target/analytics-target-A4T-integration.html)

>[!MORELIKETHIS]
>
>* [Analytics for [!DNL Target] 구현](/help/c-integrating-target-with-mac/a4t/a4timplementation.md): at.js 및 Platform Web SDK에 대한 구현 정보를 포함합니다.
>* [리디렉션 오퍼 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)를 참조하십시오
>* [Adobe Experience Platform Web SDK란?](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html): Platform Web SDK에 대한 개요 정보를 포함합니다.
>* [Target 개요](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html): 에 대한 정보를 포함합니다 [!DNL Target] 그리고 [!DNL Platform Web SDK].

