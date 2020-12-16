---
keywords: a4t;analytics;analytics for target;analytics reporting source;adobe analytics as the reporting source for target
description: Adobe "Analytics for Target"(A4T)은 Analytics 변환 지표와 대상 세그먼트를 기반으로 활동을 생성할 수 있도록 해주는 교차 솔루션 통합입니다. 이 통합에서는 Analytics 보고서를 사용하여 결과를 검사할 수 있습니다. 활동의 보고 소스로 Analytics를 사용하는 경우 해당 활동의 모든 보고 및 세그멘테이션은 Analytics 데이터 수집을 기반으로 합니다.
title: Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)
feature: a4t general
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1269'
ht-degree: 46%

---


# Adobe Target용 보고 소스로서의 Adobe Analytics(A4T){#adobe-analytics-as-the-reporting-source-for-adobe-target-a-t}

[!DNL Adobe Analytics for Target] (A4T)는  [!DNL Analytics] 전환 지표 및 대상 세그먼트를 기반으로 활동을 만들 수 있는 솔루션 간 통합입니다. A4T 통합을 사용하면 [!DNL Analytics] 보고서를 사용하여 결과를 검사할 수 있습니다. 활동의 보고 소스로 [!DNL Analytics]을 사용하는 경우 해당 활동에 대한 모든 보고 및 세그멘테이션은 [!DNL Analytics] 데이터 수집을 기반으로 합니다.

## A4T 개요 {#section_92B66069210C40DBA937790E8CC596CF}

[!DNL Analytics]과 [!DNL Target] 간의 [!DNL Analytics for Target] 통합은 최적화 프로그램을 위해 강력한 분석과 작업 시간을 단축시켜주는 도구를 제공합니다.

[!DNL Target]에서 [!DNL Analytics] 데이터를 사용하여 얻을 수 있는 3가지 주요 이점은 다음과 같습니다.

* 마케터는 언제든지 [!DNL Analytics] 성공 지표 또는 보고 세그먼트를 [!DNL Target] 활동 보고서에 동적으로 적용할 수 있습니다. 활동을 실행하기 전에 모든 항목을 지정할 필요는 없습니다.
* 단일 데이터 소스는 두 개의 개별 시스템에서 데이터를 수집할 때 발생하는 분산을 제거합니다.
* 기존 [!DNL Analytics] 구현은 필요한 모든 데이터를 수집합니다. 보고서에 사용할 데이터를 수집할 목적으로 페이지에 mbox를 구현할 필요가 없습니다. 그러나 [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md)(AP) 활동에 대한 주문 확인 mbox를 구현하는 것이 좋습니다.

>[!IMPORTANT]
>
>A4T를 사용하려면 먼저 계정을 통합용으로 공급하도록 요청해야 합니다. [이 양식](https://www.adobe.com/go/audiences_kr)을 사용하여 제공을 요청합니다.
>
>[!DNL Analytics]을(를) [!DNL Target](A4T)의 데이터 소스로 활성화하는 통합은 SiteCatalyst에 대한 차세대 Test&amp;Target 플러그인을 나타냅니다. 이 플러그인은 더 이상 사용되지 않지만 이미 사용 중인 경우에는 계속 지원됩니다.

활동의 보고 소스로 [!DNL Analytics]을 사용하는 경우 해당 활동에 대한 모든 보고 및 세그멘테이션은 [!DNL Analytics]을 기반으로 합니다.

계산된 지표를 비롯한 모든 [!DNL Analytics] 지표는 [!DNL Target] 및 [!DNL Analytics]의 [!UICONTROL Target 활동] 보고서에서 사용할 수 있습니다. 마찬가지로 [!DNL Analytics]에서 사용할 수 있는 모든 세그먼트는 두 솔루션 모두에 적용할 수 있습니다. 활동이 시작된 후 또는 활동이 완료된 후에도 [!DNL Target]의 보고서에 지표나 대상을 적용할 수 있습니다.

[!DNL Analytics]에 내장되어 있는 고객 또는 계산된 지표를 포함하여 모든 지표가 포함됩니다.

분류 기간 후에 데이터는 웹 사이트에서 수집되고 약 1시간 후에 보고서에 표시됩니다. 보고서에 있는 모든 지표, 세그먼트, 값은 활동을 설정할 때 선택한 보고서 세트에서 가져옵니다.

A4T를 사용하려면 다음 사항을 염두에 두십시오.

* [!DNL Analytics]을(를) [!DNL Target]의 보고 소스로 사용하려면 사용자와 회사 모두 [!DNL Analytics] 및 [!DNL Target]에 액세스할 수 있어야 합니다. [솔루션이 필요할 경우 계정 담당자에게 문의하십시오.](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB)
* 보고 소스는 각 활동에 대해 설정됩니다. [!DNL Target] 는 보고에 사용할 데이터를 계속 수집하며,  [!DNL Target] 데이터를 통해 수집된 데이터를 기반으로 하는 활동을 원하는 경우에는 데이터를 계속 사용할 수 있습니다 [!DNL Target].
* 두 보고 소스 중 하나를 사용해야 합니다. 두 소스 모두에서 한 활동에 대한 데이터를 수집할 수 없습니다.
* A4T를 사용할 때 활동에 사용할 수 있는 모든 성공 지표는 [!DNL Analytics] 지표입니다. 그러나 목표 지표는 mbox 호출을 기반으로 할 수 있습니다. 예를 들어 [!DNL Analytics] 클릭 추적 코드를 구현하지 않고도 A4T에서 Target의 기본 클릭 추적 기능을 사용할 수 있습니다.
* [!DNL Target] UI에서 A4T 활동의 보고를 볼 때 [!DNL Analytics] 데이터가 표시됩니다. 예를 들어 [!DNL Target]에서 [!UICONTROL 방문자] 지표를 사용하는 경우 [!DNL Target] [!UICONTROL  &lt;a7/>방문자] 지표가 아닌 [!DNL Analytics] [!UICONTROL 방문자] 지표를 사용합니다(현재 [!UICONTROL 참여자]). 이 차이는 기본 트래픽 지표([!UICONTROL 방문자], [!UICONTROL 방문 횟수], [!UICONTROL 페이지 보기 횟수]) 및 전환 지표에 특히 중요합니다.
* 기존 [!DNL Target] 활동은 계속 [!DNL Target] 데이터 수집을 사용하며 A4T 활성화의 영향을 받지 않습니다.
* 보고 소스로 [!DNL Analytics]을(를) 사용할 때는 mbox 기반 지표를 하나만 사용할 수 있습니다.
* [!DNL Target]에서 [!DNL Analytics]로 서버 간 호출은 활동 및 경험 정보를 [!DNL Analytics]에 전송합니다. 이 통합으로 인해 [!DNL Target] 또는 [!DNL Analytics]에 대한 추가 서버 호출이 발생하지 않습니다.

   경우에 따라 [!DNL Target]에서 [!DNL Analytics]로의 분류 호출이 실패할 수 있으며 활동이 [!DNL Analytics]에 데이터를 표시하지 않을 수 있습니다. 이러한 경우 [Analytics 및 Target 통합 문제 해결(A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md)을 참조하십시오. 추가 지원을 위해 [클라이언트 지원 센터](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB)에 문의할 수도 있습니다.

## 지원되는 활동 유형 {#section_F487896214BF4803AF78C552EF1669AA}

다음 표는 [!DNL Target](A4T)에서 보고 소스로 [!DNL Analytics]을(를) 지원하는 활동 유형을 보여줍니다.

| 활동 유형 | A4T와 호환 가능 | 해당하는 경우 메모 |
|--- |--- |--- |
| 수동 트래픽 분할을 사용하는 A/B 활동 | 예 |  |
| 자동 할당을 사용하는 A/B 활동 | 예 | 자동 할당 및 자동 Target 활동에 대한 [Target(A4T) 지원 분석](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa)을 참조하십시오. |
| 자동 타겟을 사용하는 A/B 활동 | 예 | 자동 할당 및 자동 Target 활동에 대한 [Target(A4T) 지원 분석](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa)을 참조하십시오. |
| 경험 타깃팅(XT) | 예 |  |
| 다변량 테스트(MVT) | 예 | [!UICONTROL 요소 기여도] 보고서를 가져오려면 mbox 기반 목표 지표 목표가 필요합니다.  [!UICONTROL 요소 기여도] 보고서는 현재 [!DNL Analytics] 지표를 지원하지 않습니다. |
| 자동화된 개인화(AP) 활동 | 아니오 |  |
| 권장 사항 활동 | 예 |  |
| 모바일 앱 | 예 | Mobile Services SDK 버전 4.13.1 이상에서 지원됩니다.  자세한 내용은 [Mobile Services 설명서](https://experienceleague.adobe.com/docs/mobile-services/using/home.html)를 참조하십시오. |
| 이메일 | 아니오 |  |
| 서버 측 배달 API | 예 | 자세한 내용은 [서버 측: Target 구현](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md)을 참조하십시오. |
| NodeJS SDK | 예 | 자세한 내용은 [서버 측: Target 구현](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md)을 참조하십시오. |
| AEM 6.1(또는 이하) 클라우드 서비스 통합 | 아니오 |  |
| AEM 6.2(또는 이상 버전) 클라우드 서비스 통합 | 예 | 자세한 내용은 [!DNL Adobe Experience Manager] 6.2 설명서의 [Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html)과 통합을 참조하십시오. |
| 리디렉션 오퍼를 사용하는 모든 활동 | 예 | A4T에서 리디렉션 오퍼를 사용하기 위한 보다 엄격한 최소 요구 사항이 있습니다. 자세한 내용은 [리디렉션 오퍼 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)를 참조하십시오. |
| Node.JS | 예 |  |

모든 활동 유형은 아직 A4T를 지원하지 않으므로 `orderConfirmPage` mbox와 같은 중요한 전환 mbox를 유지하거나 구현하는 것이 좋습니다.

## A4T 보고서 예 {#section_F0A43A1CB2F04E8282B909E4D7034361}

[!DNL Target]에서 A4T 보고서를 보려면 **[!UICONTROL 활동]**&#x200B;을 클릭하고 [!DNL Analytics]을 보고 소스로 사용하는 목록에서 원하는 활동을 클릭한 다음 **[!UICONTROL 보고서]** 탭을 클릭합니다.

>[!NOTE]
>
>[!UICONTROL 활동] 페이지의 맨 위에 있는 [!UICONTROL 보고서 소스] 드롭다운 목록을 사용하여 [!DNL Analytics]를 보고 소스로 사용하는 활동만 표시할 수 있습니다.

보고서 오른쪽 상단의 해당 아이콘을 클릭하여 보고서의 [!UICONTROL 테이블 보기]와 [!UICONTROL 그래프 보기] 간을 전환할 수 있습니다.

다음 그림은 사용 가능한 [!UICONTROL  목표 지표를 표시하는 ]보고서 지표[!UICONTROL  드롭다운 목록과 함께 A4T 보고서의 ]그래프 보기[!DNL Analytics]를 보여줍니다.

![](assets/a4t_report_graph1.png)

다음 그림은 사용 가능한  대상을 표시하는 [!UICONTROL 대상] 드롭다운 목록과 함께 A4T 보고서의 [!DNL Analytics]그래프 보기를 보여줍니다.

![](assets/a4t_report_graph2.png)

다음 그림은 A4T 보고서의 [!UICONTROL 표 보기]를 보여줍니다.

![](assets/a4t_report_table.png)

[!DNL Analytics]이 아니라 [!DNL Target]에서 보고서를 보려면 보고서 맨 위의 **** Analytics에서 보기를 클릭하십시오.

## Analytics &amp; Target: 분석 우수 사례 자습서 {#section_3438E6E77A464424B717A4FD333B84B2}

[분석 및 Target을 엽니다.[!DNL Adobe Experience League]에서 제공하는 분석](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) 자습서에 대한 우수 사례입니다.

## 교육 비디오:

다음 비디오에는 이 항목에서 설명하는 개념에 대한 자세한 정보가 포함되어 있습니다.

### Target 분석(A4T)(4:32) ![개요 배지](/help/assets/overview.png)

이 비디오에서는 [!DNL Target]의 보고 소스로 [!DNL Analytics]을 사용하여 최적화 프로그램의 분석을 실행하는 방법을 설명합니다.

* A4T가 무엇이며, 왜 사용해야 하는지에 대해 설명합니다.
* A4T의 작동 방식에 대해 설명합니다.
* A4T를 사용하기 위해 필요한 전제 조건을 이해합니다.

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### 분석/Target 통합(A4T)(40:33) ![자습서 배지](/help/assets/tutorial.png)

이 비디오는 Adobe 고객 지원 팀에서 진행한 이니셔티브인 &quot;[운영시간](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot; 기록입니다.

* 통합이 작동하도록 설정하고 작동하는지 확인하는 방법
* 통합 작동 방식
* Analytics에서 사용할 이상적인 보고서에 대해 알아보기
* A4T와 관련된 일반적인 질문에 대한 답변

[분석/Target 통합(A4T) 오피스 시간](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)