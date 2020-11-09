---
keywords: Targeting;success;conversion metric;page score metric;page views metric;revenue metrics;time on site metric;estimated value;advanced settings;success metrics;advanced settings;dependency;dependant;Increment Count & Keep User in Activity;Increment Count, Release user, & Allow Reentry;increment Count, Release User, & Bar from Reentry
description: Adobe Target에서 성공 지표는 활동의 성공을 측정하는 데 사용되는 매개 변수입니다. 성공 지표에는 타겟 활동에 주어진 경험 또는 오퍼의 성공을 결정할 수 있는 주요 비즈니스 정책이 포함되어 있습니다.
title: Adobe Target의 성공 지표
feature: success metrics
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 48%

---


# 성공 지표{#success-metrics}

In [!DNL Adobe Target] success metrics are parameters used to measure the success of an activity. Success metrics include key business measures that enable you to determine the success of a given experience or offer in a [!DNL Target] activity.

예를 들어 새 오퍼가 방문자당 매출을 늘리는지 또는 장바구니에 품목을 추가할지 여부를 결정할 수 있습니다. 성공 지표는 등록, 주문 또는 구매 흐름과 관련된 문제뿐만 아니라 방문자나 고객 참여와 관련된 문제를 발견하는 데에도 유용할 수 있습니다.

## 개요

즉, [!DNL Target]성공 지표는 보고 및 추적 목적을 위한 최적의 옵션을 사용하여 미리 구성됩니다.

기본적으로 전환 이벤트는 &quot;[!UICONTROL 증가 카운트 및 사용자 활동 유지&quot;로 설정됩니다]. 전환은 한 번만 계산되고, 반복 전환은 계산되지 않으며, 방문자는 항상 활동 컨텐츠를 보게 됩니다.

Revenue metrics that are set to &quot;[!UICONTROL Increment count &amp; keep user in activity]&quot; log order details only for the first order made by the same visitor. All subsequent orders increase conversion count, but will not add revenue to RPV/AOV/Sales, and will not be included in the [!UICONTROL Order Details] report.

>[!NOTE]
>
>보고 소스 [(A4T)로](/help/c-integrating-target-with-mac/a4t/a4t.md) Analytics를 사용하는 활동에 대한 기본 동작은 &quot;[!UICONTROL 참가자당]1회&quot;와 함께 &quot;사용자 활동[!UICONTROL 유지&quot;입니다].

다음과 같은 성공 지표를 사용할 수 있습니다.

| 성공 지표 | 측정 방법 | 정의 |
|--- |--- |--- |
| 변환 | 전환 기반 | 전환은 방문자가 정의된 사이트(예: <ul><li>단추 클릭</li><li>페이지 확인함</li><li>설문 조사 완료</li><li>구매</li></ul>전환은 방문자당 한 번 또는 방문자가 전환을 완료할 때마다 카운트될 수 있습니다. |
| 수입 | 전환 기반 | 방문에서 생성된 수익입니다. 다음 매출 지표 중에서 선택할 수 있습니다.<ul><li>RPV(방문자당 매출)</li><li>AOV(평균 주문 가격)</li><li>총 판매 수</li><li>주문</li></ul> |
| 페이지 보기 횟수 | 참여 기반 | 각 고유한 방문은 전환으로 간주됩니다. |
| 사용자 지정 점수 지정 | 참여 기반 | Aggregated score based on the value assigned to pages visited on the site, from the point the visitor first sees the activity&#39;s first display [!DNL Target] request. |
| 사이트에서 보낸 시간 | 참여 기반 | Time spent in the visit (in seconds) from the point the visitor sees the activity&#39;s first display [!DNL Target] request to the load of the final page with a request in the session. |

참여 기반 지표는 전환 기반 및 수입 기반 지표와 달리, 방문자가 해당 세션에 대한 수를 늘리기 위해 각 방문 활동의 대상 사용자여야 합니다. 연관된 지표는 적격 재확인 이후 증가하기 시작하고, 각 방문자의 세션 종료 시 중지됩니다. 세션은 활동이 없는 경우 30분 후에 종료됩니다. 따라서 테스트 도중 결과가 바로 표시되지 않습니다.그러나 세션 종료 후 몇 분 이내에 해당 세션의 모든 결과를 사용할 수 있습니다.

## 사용자 지정 성공 지표

사용자 지정 성공 지표를 만들 수도 있습니다.

성공 지표를 선택한 후에 방문자가 목표를 달성하기 위해 수행한 작업을 선택합니다. For example, choose a [!UICONTROL Conversion] metric, set it to be counted once per visitor, then set whether success is achieved when a visitor views a certain page (or set of pages), views a specific [!DNL Target] request, or clicks a specific link.

If enabled, the [!UICONTROL Estimated Value of one conversion] field (not available for the [!UICONTROL Page Score] metrics) provides a value for your goal, but not for other metrics. 이 값을 통해 [!DNL Target]이 예상 매출액 상승도를 계산할 수 있습니다. 이 필드는 선택 사항이지만, 이 필드의 값이 없으면 비매출액 지표의 증분 수익을 계산할 수 없습니다. For all revenue metrics ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], and [!UICONTROL Orders]), the estimate uses [!UICONTROL Revenue per Visitor]. 데이터 유형은 통화입니다. 자세한 내용은 [매출 상승도 평가](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오.

활동에 대해 선택한 성공 지표는 활동에 대한 보고서를 볼 때 보고서 설정에서 사용할 수 있습니다.

Some metrics, such as [!UICONTROL Custom Scoring] and [!UICONTROL Revenue Per Visitor], require a customized implementation that passes in information such as order totals and order IDs.

## 고급 설정 {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

고급 설정을 사용하여 성공을 측정하는 방법을 관리할 수 있습니다. 옵션에는 종속성 추가, 사용자를 활동에 유지할지 또는 제거할지 여부, 참가자당 한 번 또는 모든 노출에서 지표를 계산할지 여부 선택 등이 포함됩니다.

고급 [!UICONTROL 설정] 옵션에 액세스하려면 **[!UICONTROL 세로 줄임표]** > **[!UICONTROL 고급 설정]**&#x200B;을클릭합니다.

![고급 설정 메뉴](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

>[!NOTE]
>
>[!DNL Adobe Analytics]를 보고 소스로 사용하는 경우 설정은 [!DNL Analytics] 서버에서 관리됩니다. The [!UICONTROL Advanced Settings] option will not be available. For more information, see [Adobe Analytics as the reporting source for Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md).

### 종속성 추가

고급 설정을 사용하여 종속 성공 지표를 만들 수 있습니다. 방문자가 다른 지표에 먼저 도달한 경우에만 하나의 지표를 증가시킵니다.

![종속성 추가](/help/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

예를 들어, 방문자가 전환하기 전에 해당 오퍼를 클릭하거나 특정 페이지에 도달한 경우에만 테스트 전환이 유효할 수 있습니다.

Dependency functionality is *not* supported for the following:

* [!UICONTROL 권장 사항 활동. ] 이 기능은 다른 모든 활동 유형에 대해 지원됩니다.
* If you use [Analytics as your reporting source](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* &quot;페이지 확인함&quot; 지표 유형
* VEC(시각적 경험 작성기) 활동에 대한 &quot;요소를 클릭함&quot; 지표 유형

종속적 성공 지표는 다음과 같은 경우에 전환되지 않습니다.

* metric1이 metric2에 종속되고 metric2가 metric1에 종속되는 순환 종속성을 만드는 경우 두 지표 모두 전환될 수 없습니다.
* 자동화된 개인화 활동은 전환 지표에 도달할 때 사용자를 해제하고 활동을 다시 시작하므로, 전환 지표에 종속되는 모든 지표가 전환되지 않습니다.

### 사용자가 이 목표 지표에 도달한 후에 어떤 상황이 진행됩니까?

고급 설정을 사용하여 사용자가 목표 지표에 도달한 후에 발생하는 결과를 결정합니다. 다음 표에는 사용 가능한 옵션이 나와 있습니다:

| 사용자가 이 목표 지표에 접한 이후 | 옵션 |
|--- |--- |
| [!UICONTROL 증분 카운트 및 사용자를 활동에 유지] | 카운트가 증분되는 방식 지정:<ul><li>응모자마다 한 번(기본값)</li><li>노출 시마다, 페이지 새로 고침 제외</li><li>노출 시마다</li></ul> |
| [!UICONTROL 증분 카운트, 릴리스 사용자 및 재입력 허용] | 방문자가 활동을 다시 입력하는 경우 방문자에게 표시되는 경험을 선택합니다.<ul><li>동일 경험(기본값)</li><li>임의 경험</li><li>확인되지 않은 경험</li></ul> |
| [!UICONTROL 증분 카운트, 사용자 해제 및 재입력에서 막대] | 활동 콘텐츠 대신 사용자에게 표시되는 콘텐츠를 결정합니다.<ul><li>동일 경험, 추적 없음(기본값)</li><li>기본 콘텐츠 또는 기타 활동 콘텐츠</li></ul> |

>[!NOTE]
>
>지표를 [!UICONTROL 증가 카운트 옵션 중 하나(위에 언급된)로] 구성하는 경우, 지표 카운트는 참가자당 한 번만 올바르게 증가합니다. 지표 카운트는 방문 수준에서 모든 새 세션에 대해 방문당 한 번씩 증가합니다.

### 카운트는 어떻게 증분됩니까:

원하는 동작을 선택합니다.

* 참가자당 한 번
* 모든 노출 시(페이지 새로 고침 제외)
* 노출 시마다

## 교육 비디오: 활동 지표

이 비디오는 활동 지표를 사용하는 방법을 보여 줍니다.

* &quot;목표&quot; 지표 이해
* 변환, 수입 및 참여 지표 이해 및 빌드
* 클릭 추적 지표 빌드

>[!VIDEO](https://video.tv.adobe.com/v/17380)