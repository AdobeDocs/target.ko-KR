---
keywords: 타깃팅;성공;전환 지표;페이지 점수 지표;페이지 보기 지표;매출 지표;사이트에서 보낸 시간 지표;예상값;고급 설정;성공 지표;고급 설정;종속성;종속;증분 카운트 및 사용자를 활동에 유지;증분 카운트, 사용자 해제 및 재입력 허용;증분 카운트, 사용자 해제 및 재입력에서 막대
description: 활동의 성공을 결정하는 데 도움이 되는 Adobe [!DNL Target] 의 성공 지표에 대해 알아봅니다. 성공 지표에는 전환, 매출, 페이지 보기 수, 사용자 지정 점수 및 사이트에서 보낸 시간이 포함됩니다.
title: 성공 지표란 무엇입니까?
feature: Success Metrics
exl-id: 38d5314d-4950-4106-a058-0d221faf5a24
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 41%

---

# 성공 지표

[!DNL Adobe Target]에서 성공 지표는 활동의 성공을 측정하는 데 사용되는 매개 변수입니다. 성공 지표에는 [!DNL Target] 활동에서 주어진 경험 또는 오퍼의 성공을 결정할 수 있는 주요 비즈니스 조치가 포함되어 있습니다.

예를 들어 새 오퍼가 방문자당 매출을 늘리는지 또는 장바구니에 품목을 추가할지 여부를 결정할 수 있습니다. 성공 지표는 등록, 주문 또는 구매 흐름과 관련된 문제뿐만 아니라 방문자나 고객 참여와 관련된 문제를 발견하는 데에도 유용할 수 있습니다.

## 개요

[!DNL Target]에서 성공 지표는 보고 및 추적 목적을 위해 최적의 옵션으로 미리 구성되어 있습니다.

기본적으로 전환 이벤트는 &quot;[!UICONTROL Increment count & keep user in activity]&quot;(으)로 설정됩니다. 전환은 한 번만 카운트되고 반복 전환은 카운트되지 않으며, 방문자에게는 항상 활동 콘텐츠가 표시됩니다.

&quot;[!UICONTROL Increment count & keep user in activity]&quot;(으)로 설정된 매출 지표는 동일한 방문자가 수행한 첫 번째 주문에 대해서만 주문 세부 정보를 기록합니다. 모든 후속 주문은 전환 수를 증가시키지만 RPV/AOV/매출에는 매출을 추가하지 않으며 [!UICONTROL Order Details] 보고서에 포함되지 않습니다.

>[!NOTE]
>
>[Analytics를 보고 소스로 사용](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)하는 활동의 경우 목표 지표는 항상 &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; 및 &quot;[!UICONTROL On Every Impression]&quot; 설정을 사용합니다. 구성 가능한 *not*&#x200B;입니다.

다음과 같은 성공 지표를 사용할 수 있습니다.

| 성공 지표 | 측정 방법 | 정의 |
|--- |--- |--- |
| 전환 | 전환 기반 | 전환은 방문자가 사용자가 정의한 사이트에서 작업을 수행할 때입니다. 예를 들면 다음과 같습니다 <ul><li>단추를 클릭함</li><li>페이지 확인함</li><li>설문 조사 완료됨</li><li>구매함</li></ul>전환은 방문자당 한 번 또는 방문자가 전환을 완료할 때마다 계산됩니다. |
| 수입 | 전환 기반 | 방문에서 생성된 수익입니다. 다음 매출 지표 중에서 선택할 수 있습니다.<ul><li>RPV(방문자당 매출)</li><li>AOV(평균 주문 가격)</li><li>총 판매 수</li><li>주문</li></ul> |
| 페이지 보기 횟수 | 참여 기반 | 각 고유한 방문은 전환으로 간주됩니다. |
| 사용자 지정 점수 지정 | 참여 기반 | 방문자가 활동의 첫 디스플레이 [!DNL Target] 요청을 처음 본 시점부터 시작하여 사이트에서 방문한 페이지에 할당된 값에 따라 집계된 점수입니다. |
| 사이트에서 보낸 시간 | 참여 기반 | 방문자가 활동의 첫 디스플레이 [!DNL Target] 요청을 본 시점부터 세션의 요청이 있는 최종 페이지 로드까지 방문에서 보낸 시간(초)입니다. |

참여 기반 지표는 전환 기반 및 수입 기반 지표와 달리, 방문자가 해당 세션에 대한 수를 늘리기 위해 각 방문 활동의 대상 사용자여야 합니다. 연관된 지표는 적격 재확인 이후 증가하기 시작하고, 각 방문자의 세션 종료 시 중지됩니다. 세션은 활동이 없는 경우 30분 후에 종료됩니다. 따라서 테스트 중에는 결과가 즉시 표시되지 않지만 해당 세션의 모든 결과는 세션이 종료된 후 몇 분 내에 사용할 수 있습니다.

## 사용자 정의 성공 지표

사용자 지정 성공 지표를 만들 수도 있습니다.

성공 지표를 선택한 후에 방문자가 목표를 달성하기 위해 수행한 작업을 선택합니다. 예를 들어, [!UICONTROL Conversion] 지표를 선택하고, 방문자당 한 번씩 계산되도록 설정한 다음, 방문자가 특정 페이지(또는 페이지 세트)를 보거나, 특정 [!DNL Target] 요청을 보거나, 특정 링크를 클릭할 때 성공 여부를 설정합니다.

사용하도록 설정하면 [!UICONTROL Estimated Value of one conversion] 필드([!UICONTROL Page Score] 지표에 사용할 수 없음)가 목표 값을 제공하지만 다른 지표에 대해서는 값을 제공하지 않습니다. 이 값을 통해 [!DNL Target]이 예상 매출액 상승도를 계산할 수 있습니다. 이 필드는 선택 사항이지만, 이 필드의 값이 없으면 비매출액 지표의 증분 수익을 계산할 수 없습니다. 모든 매출 지표([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] 및 [!UICONTROL Orders])에 대해 예상 값은 [!UICONTROL Revenue per Visitor]을(를) 사용합니다. 데이터 유형은 통화입니다. 자세한 내용은 [매출 상승도 평가](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오.

활동에 대해 선택한 성공 지표는 활동에 대한 보고서를 볼 때 보고서 설정에서 사용할 수 있습니다.

[!UICONTROL Custom Scoring] 및 [!UICONTROL Revenue Per Visitor]과(와) 같은 일부 지표에는 주문 합계 및 주문 ID와 같은 정보를 전달하는 사용자 지정 구현이 필요합니다.

## 고급 설정 {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

고급 설정을 사용하여 성공을 측정하는 방법을 관리할 수 있습니다. 옵션에는 종속성 추가, 활동에 사용자를 유지할지 또는 제거할지 선택, 참가자 당 한 번 또는 노출 시마다 지표를 계산할지 여부가 포함됩니다.

[!UICONTROL Advanced Settings] 옵션에 액세스하려면 **[!UICONTROL More Actions]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmallListVert.svg))을 클릭한 다음 **[!UICONTROL Advanced Settings]**&#x200B;을(를) 클릭합니다.

![고급 설정 메뉴](/help/main/c-activities/r-success-metrics/assets/advanced-settings-refresh.png)

>[!NOTE]
>
>[!DNL Adobe Analytics]를 보고 소스로 사용하는 경우 설정은 [!DNL Analytics] 서버에서 관리됩니다. [!UICONTROL Advanced Settings] 옵션을 사용할 수 없습니다. 자세한 내용은 [Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md)을 참조하십시오.

### 종속성 추가

고급 설정을 사용하여 종속적 성공 지표를 만들고, 방문자가 먼저 다른 지표에 도달하는 경우에만 지표를 1씩 증분할 수 있습니다.

예를 들어, 방문자가 전환하기 전에 해당 오퍼를 클릭하거나 특정 페이지에 도달한 경우에만 테스트 전환이 유효할 수 있습니다.

종속성 기능은 다음에 대해 *지원되지 않습니다*.

* [!UICONTROL Recommendations]개 활동. 이 기능은 다른 모든 활동 유형에 대해 지원됩니다.
* [Analytics를 보고 소스로 사용](/help/main/c-integrating-target-with-mac/a4t/a4t.md)하는 경우(A4T).
* 페이지 확인함 지표 유형.
* VEC(시각적 경험 작성기) 활동에 대한 &quot;요소를 클릭함&quot; 지표 유형입니다.

종속적 성공 지표는 다음과 같은 경우에 전환되지 않습니다.

* metric1이 metric2에 종속되고 metric2가 metric1에 종속되는 순환 종속성을 만드는 경우 두 지표 모두 전환될 수 없습니다.
* [!UICONTROL Automated Personalization] 활동은 사용자를 해제하고 전환 지표에 도달하면 활동을 다시 시작하므로 전환 지표에 종속된 지표는 전환되지 않습니다.

### 사용자가 이 목표 지표에 도달한 후에 어떤 상황이 진행됩니까?

고급 설정을 사용하여 사용자가 목표 지표에 도달한 후에 발생하는 결과를 결정합니다. 다음 표에는 사용 가능한 옵션이 나와 있습니다.

| 사용자가 이 목표 지표에 접한 이후 | 옵션 |
|--- |--- |
| [!UICONTROL Increment Count & Keep User in Activity] | 카운트가 증분되는 방식 지정:<ul><li>응모자마다 한 번(기본값)</li><li>노출 시마다, 페이지 새로 고침 제외</li><li>노출 시마다</li></ul> |
| [!UICONTROL Increment Count, Release user, & Allow Reentry] | 방문자가 활동을 다시 입력하는 경우 방문자에게 표시되는 경험을 선택합니다.<ul><li>동일 경험(기본값)</li><li>임의 경험</li><li>확인되지 않은 경험</li></ul> |
| [!UICONTROL Increment Count, Release User, & Bar from Reentry] | 활동 콘텐츠 대신 사용자에게 표시되는 콘텐츠를 결정합니다.<ul><li>동일 경험, 추적 없음(기본값)</li><li>기본 콘텐츠 또는 기타 활동 콘텐츠</li></ul> |

>[!NOTE]
>
>지표를 [!UICONTROL Increment Count] 옵션 중 하나로 구성하는 경우(위에서 언급), 지표 수는 방문자 수준에서만 참여자당 한 번씩 올바르게 증가합니다. 지표 수는 방문 수준에서 모든 새 세션에 대해 방문당 한 번씩 증가합니다.

### 카운트는 어떻게 증분됩니까?

원하는 비헤이비어를 선택합니다.

* 응모자마다 한 번
* 노출 시마다(페이지 새로 고침 제외)
* 노출 시마다

## 알려진 문제

* 고급 옵션 &quot;카운트는 어떻게 증분됩니까?&quot;가 &quot;모든 노출&quot; 또는 &quot;모든 노출(새로 고침 제외)&quot;로 설정된 성공 지표는 다른 지표가 종속되는 성공 지표로 사용할 수 없습니다.

성공 지표가 노출 시마다 증가하도록 설정되어 있으면 [!DNL Target]은(는) 방문자가 이 성공 지표를 방문할 때마다 방문자를 다시 계산합니다. 그런 다음 [!DNL Target]은(는) 성공 지표 &quot;멤버십&quot;을 0으로 재설정하여 다음 노출 시 다시 카운트될 수 있도록 합니다. 따라서 이 지표를 먼저 확인해야 하는 다른 지표가 있으면 [!DNL Target]은(는) 사용자가 첫 번째 지표를 보았음을 인식하지 못합니다.

## 교육 비디오: 활동 지표

이 비디오는 활동 지표를 사용하는 방법을 보여 줍니다.

* &quot;목표&quot; 지표 이해
* 변환, 수입 및 참여 지표 이해 및 빌드
* 클릭 추적 지표 빌드

>[!VIDEO](https://video.tv.adobe.com/v/17380)
