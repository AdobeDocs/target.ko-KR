---
description: Adobe "Analytics for Target"(A4T)은 Analytics 변환 지표와 대상 세그먼트를 기반으로 활동을 생성할 수 있도록 해주는 교차 솔루션 통합입니다. 이 통합에서는 Analytics 보고서를 사용하여 결과를 검사할 수 있습니다. 활동의 보고 소스로 Analytics를 사용하는 경우 해당 활동의 모든 보고 및 세그멘테이션은 Analytics 데이터 수집을 기반으로 합니다.
keywords: a4t;analytics;analytics for target;analytics 보고 소스;target용 보고 소스로서의 adobe analytics
seo-description: Adobe "Analytics for Target"(A4T)은 Analytics 변환 지표와 대상 세그먼트를 기반으로 활동을 생성할 수 있도록 해주는 교차 솔루션 통합입니다. 이 통합에서는 Analytics 보고서를 사용하여 결과를 검사할 수 있습니다. 활동의 보고 소스로 Analytics를 사용하는 경우 해당 활동의 모든 보고 및 세그멘테이션은 Analytics 데이터 수집을 기반으로 합니다.
seo-title: Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)
solution: Target
subtopic: 다변량 테스트
title: Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)
topic: Standard
uuid: 616798a6-1587-410f-9ac6-473beb39e3fc
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Adobe Target용 보고 소스로서의 Adobe Analytics(A4T){#adobe-analytics-as-the-reporting-source-for-adobe-target-a-t}

Adobe &quot;Analytics for Target&quot;(A4T)은 Analytics 변환 지표와 대상 세그먼트를 기반으로 활동을 생성할 수 있도록 해주는 교차 솔루션 통합입니다. A4T 통합에서는 Analytics 보고서를 사용하여 결과를 검사할 수 있습니다. 활동의 보고 소스로 Analytics를 사용하는 경우 해당 활동의 모든 보고 및 세그멘테이션은 Analytics 데이터 수집을 기반으로 합니다.

## A4T 개요 {#section_92B66069210C40DBA937790E8CC596CF}

Analytics와 Target 간 Analytics for Target 통합에서는 최적화 프로그램을 위한 강력한 분석 및 시간 절약 도구를 제공합니다.

Target에서 Analytics 데이터를 사용하는 세 가지 기본 이점은 다음과 같습니다.

* 마케터가 언제든지 Analytics 성공 지표 또는 보고 세그먼트를 Target 활동 보고서에 동적으로 적용할 수 있습니다. 활동을 실행하기 전에 모든 항목을 지정할 필요는 없습니다.
* 단일 데이터 소스는 두 개의 개별 시스템에서 데이터를 수집할 때 발생하는 분산을 제거합니다.
* 기존 Adobe Analytics 구현은 필요한 모든 데이터를 수집합니다. 보고서에 사용할 데이터를 수집할 목적으로 페이지에 mbox를 구현할 필요가 없습니다. 하지만, 자동화된 개인화(AP) 활동에 대해서는 여전히 주문 확인 mbox를 구현하는 것이 좋습니다.

>[!IMPORTANT]
>
>A4T를 사용하려면 먼저 계정을 통합용으로 공급하도록 요청해야 합니다. [이 양식](https://www.adobe.com/go/audiences)을 사용하여 제공을 요청합니다.
>
>Adobe Analytics를 Adobe Target(A4T)의 데이터 소스로 활성화하는 통합은 차세대 Test&amp;Target - SiteCatalyst 플러그인을 나타냅니다. 이 플러그인은 더 이상 사용되지 않지만 이미 사용 중인 경우에는 계속 지원됩니다.

활동의 보고 소스로 Analytics를 사용하는 경우 해당 활동의 모든 보고 및 세그멘테이션은 Analytics를 기반으로 합니다.

계산된 지표를 포함한 모든 Analytics 지표는 Analytics의 Target Standard/Premium 및 Target 활동 보고서에서 사용할 수 있습니다. 마찬가지로, Analytics에서 사용 가능한 모든 세그먼트를 두 솔루션 모두에 적용할 수 있습니다. 테스트를 시작한 후에 또는 테스트가 완료된 후에도 Target Standard/Premium의 보고서에 해당 지표 또는 대상을 적용할 수 있습니다.

Analytics에 기본으로 제공되는 모든 고객 지표 또는 계산된 지표를 비롯한 모든 지표가 포함됩니다.

분류 기간 후에 데이터는 웹 사이트에서 수집되고 약 1시간 후에 보고서에 표시됩니다. 보고서에 있는 모든 지표, 세그먼트, 값은 활동을 설정할 때 선택한 보고서 세트에서 가져옵니다.

A4T를 사용하려면 다음 사항을 염두에 두십시오.

* Adobe Analytics를 Adobe Target의 보고 소스로 사용하려면 본인과 회사 모두가 Adobe Analytics 및 Adobe Target에 액세스할 수 있어야 합니다. [솔루션이 필요할 경우 계정 담당자에게 문의하십시오.](../../cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB)
* 보고 소스는 각 활동에 대해 설정됩니다. Target은 보고에 사용할 데이터를 계속 수집하며 Target에서 수집된 데이터를 활동의 기준으로 활용하려는 경우 Target 데이터를 사용할 수 있습니다.
* 두 보고 소스 중 하나를 사용해야 합니다. 두 소스 모두에서 한 활동에 대한 데이터를 수집할 수 없습니다.
* A4T를 사용하는 경우 활동에 사용할 수 있는 모든 성공 지표는 Analytics 지표입니다. 그러나 목표 지표는 mbox 호출을 기반으로 할 수 있습니다. 예를 들어, Analytics 클릭 추적 코드를 구현하는 대신 A4T와 함께 Target의 즉석 클릭 추적 기능을 사용할 수 있습니다.
* Target UI에서 A4T 활동의 보고를 볼 때에는 Analytics 데이터가 보입니다. 예를 들어, Target에서 방문자 지표를 사용하는 경우 Target 방문자 지표가 아닌 Analytics 방문자(현재 참여자라고 함) 지표를 사용하는 것입니다. 이러한 차이는 기본 트래픽 지표(방문자 수, 방문 횟수, 페이지 조회 수) 및 변환 지표에 특히 중요합니다.
* 모든 기존 Target 활동은 Target 데이터 수집을 계속 사용하며 A4T 사용의 영향을 받지 않습니다.
* Analytics를 보고 소스로 사용할 때에는 하나의 mbox 기반 지표만 허용됩니다.
* Target에서 Analytics로 수행되는 서버 간 호출은 활동 및 경험 정보를 Analytics에 전송합니다. 이 통합으로 인해 Target 또는 Analytics의 추가적인 서버 호출이 발생하지 않습니다.

## 지원되는 활동 유형 {#section_F487896214BF4803AF78C552EF1669AA}

다음 표는 보고 소스(A4T)로서 Analytics를 지원하는 활동 유형을 보여줍니다.

| 활동 유형 | A4T와 호환 가능 | 해당하는 경우 메모 |
|--- |--- |--- |
| 수동 트래픽 분할을 사용하는 A/B 활동 | 예 |  |
| 자동 할당을 사용하는 A/B 활동 | 아니오 |  |
| 자동 타겟을 사용하는 A/B 활동 | 아니오 |  |
| 경험 타깃팅(XT) | 예 |  |
| 다변량 테스트(MVT) | 예 | 요소 기여도 보고서를 가져오기 위해 mbox 기반 목표 지표 목표를 필요로 합니다.  요소 기여도 보고서는 현재 Analytics 지표를 지원하지 않습니다. |
| 자동화된 개인화(AP) 활동 | 아니오 |  |
| 권장 사항 활동 | 예 |  |
| 모바일 앱 | 예 | Mobile Services SDK 버전 4.13.1 이상에서 지원됩니다.  자세한 내용은 [Mobile Services 설명서](https://marketing.adobe.com/resources/help/en_US/mobile/)를 참조하십시오. |
| 이메일 | 아니오 |  |
| 서버 측 배달 API | 예 | 자세한 내용은 [서버 측: Target 구현](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md)을 참조하십시오. |
| NodeJS SDK | 예 | 자세한 내용은 [서버 측: Target 구현](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md)을 참조하십시오. |
| AEM 6.1(또는 이하) 클라우드 서비스 통합 | 아니오 |  |
| AEM 6.2(또는 이상 버전) 클라우드 서비스 통합 | 예 | 자세한 내용은 Adobe Experience Manager 6.2 설명서에서 [Adobe Target과 통합](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html)을 참조하십시오. |
| 리디렉션 오퍼를 사용하는 모든 활동 | 예 | A4T에서 리디렉션 오퍼를 사용하기 위한 보다 엄격한 최소 요구 사항이 있습니다. 자세한 내용은 [리디렉션 오퍼 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)를 참조하십시오. |
| Node.JS | 예 |  |

일부 활동 유형은 아직 A4T를 지원하지 않으므로 &quot;orderConfirmPage&quot; mbox와 같은 중요한 전환 mbox를 유지하거나 구현하는 것이 좋습니다.

## A4T 보고서의 예 {#section_F0A43A1CB2F04E8282B909E4D7034361}

[!DNL Target]**에서 A4T 보고서를 보려면[!UICONTROL 활동]** 을 클릭하고, [!DNL Analytics]를 보고 소스로 사용하는 목록에서 원하는 활동을 클릭한 다음 **[!UICONTROL 보고서]탭을 클릭하십시오.**

>[!NOTE]
>
>[!UICONTROL 활동] 페이지의 맨 위에 있는 [!UICONTROL 보고서 소스] 드롭다운 목록을 사용하여 [!DNL Analytics]를 보고 소스로 사용하는 활동만 표시할 수 있습니다.

보고서의 오른쪽 위에서 적절한 아이콘을 클릭하여 표 보기 및 [!UICONTROL 그래프 보기] 간에 전환할 수 있습니다.

다음 그림은 사용 가능한 [!UICONTROL  목표 지표를 표시하는 ]보고서 지표[!UICONTROL  드롭다운 목록과 함께 A4T 보고서의 ]그래프 보기[!DNL Analytics]를 보여줍니다.

![](assets/a4t_report_graph1.png)

다음 그림은 사용 가능한 [!UICONTROL ] 대상을 표시하는 [!UICONTROL 대상] 드롭다운 목록과 함께 A4T 보고서의 [!DNL Analytics]그래프 보기를 보여줍니다.

![](assets/a4t_report_graph2.png)

다음 그림은 A4T 보고서의 [!UICONTROL 표 보기]를 보여줍니다.

![](assets/a4t_report_table.png)

[!DNL Analytics]이 아니라 [!DNL Target]에서 보고서를 보려면 보고서 맨 위의 **[!UICONTROL ]Analytics에서 보기** 를 클릭하십시오.

## Analytics &amp; Target: 분석 우수 사례 자습서 {#section_3438E6E77A464424B717A4FD333B84B2}

Adobe Experience League에서 제공하는 [Analytics &amp; Target: 분석 우수 사례](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) 자습서를 엽니다.

## 교육 비디오:

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### Analytics for Target(A4T)(4:32)

이 비디오에서는 Adobe Analytics를 Adobe Target에서 보고 소스로 사용하여 최적화 프로그램의 분석을 실행하는 방법에 대해 설명합니다.

* A4T가 무엇이며, 왜 사용해야 하는지에 대해 설명합니다.
* A4T의 작동 방식에 대해 설명합니다.
* A4T를 사용하기 위해 필요한 전제 조건을 이해합니다.

>[!VIDEO](https://video.tv.adobe.com/v/17384?captions=kor)

### Analytics/Target 통합(A4T)(40:33)

이 비디오는 Adobe 고객 지원 팀에서 진행한 이니셔티브인 &quot;[운영시간](../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot; 기록입니다.

* 통합이 작동하도록 설정하고 작동하는지 확인하는 방법
* 통합 작동 방식
* Analytics에서 사용할 이상적인 보고서에 대해 알아보기
* A4T와 관련된 일반적인 질문에 대한 답변

>[!VIDEO](https://video.tv.adobe.com/v/22223/?captions=kor)