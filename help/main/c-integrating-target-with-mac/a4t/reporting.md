---
keywords: analytics for target;a4t;보고 소스로 분석;analytics
description: Analytics for [!DNL Target] (A4T)을(를) 사용하는 방법을 알아봅니다. A4T에서는 Analytics 지표 및 대상 세그먼트를 사용하는  [!DNL Target] 활동에 대한 Analytics 보고서에 액세스할 수 있습니다.
title: A4T에서 보고를 사용하는 방법은 무엇입니까?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 6857ba1a6410d3140a83a052efc50e9dd1776fd9
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 39%

---

# A4T 보고

[!DNL Adobe Analytics]을(를) [!DNL Adobe Target]에 대한 보고 소스로 사용(A4T)하면 [!DNL Analytics] 활동에 대한 [!DNL Target] 보고서에 액세스할 수 있습니다.

[!DNL Analytics]과(와) [!DNL Target] 모두에서 활동에 대한 보고서를 볼 수 있습니다.

[!DNL Analytics]에 대해 [!DNL Target]을(를) 사용하는 보고 모범 사례를 보려면 [이 Adobe Spark 페이지를 방문](https://spark.adobe.com/page/Lo3Spm4oBOvwF/)하십시오.

## 개요 {#section_035A62D65608423285D8A5A54731E2C5}

[!DNL Analytics]과(와) [!DNL Target] 보고서는 모두 사이트 방문자가 아닌 입국자(테스트를 입력한 사람)를 측정합니다.

방문자가 페이지에서 활동 콘텐츠를 볼 때마다 [!DNL Target]은(는) 방문자가 본 활동 및 경험을 포함하여 [!DNL Analytics]에 대해 직접 서버 간 호출을 합니다. [!DNL Target]은(는) 전환이 이루어질 때마다 [!DNL Analytics]을(를) 호출합니다. [!DNL Analytics]은(는) 변환을 &quot;활동 전환&quot;이라는 이름의 특정 새 [!DNL Analytics] 이벤트로 추가하며, 이 이벤트는 [!DNL Analytics]에서 수집한 다른 데이터와 함께 추적됩니다.

[!UICONTROL Select] 작업을 사용하여 *참여자*&#x200B;를 정렬하면 선택한 기간 동안 참여자를 받은 경험만 보고서에 표시됩니다.

>[!NOTE]
>
>[!DNL Target]에서 제공하는 보고서에는 지연 시간이 4분입니다. A4T에서 제공하는 활동의 경우 [!DNL Target] 및 [!DNL Analytics] 보고서에서 모두 보고서 데이터를 경험별로 분류하기 전에 활동을 처음 저장한 후 최대 24시간이 걸릴 수 있습니다. 처음 24시간 내에 수집된 데이터는 정확하며 올바른 경험에 지정됩니다.

## Analytics의 보고서 {#analytics}

[!DNL Analytics]에는 A4T 통합이 활성화된 후 사용할 수 있는 몇 가지 차원과 지표가 있습니다.

### 차원

* [!UICONTROL Analytics for Target] - 통합을 통해 전달되는 상위 ID입니다. 이 차원의 형식은 `Activity ID:Experience ID:3rd ID`입니다. 아래 차원은 이 차원의 분류입니다.
* [!UICONTROL Target Activities]
* [!UICONTROL Target Experiences]
* [!UICONTROL Target Activity] > [!UICONTROL Experience]
* [!UICONTROL 3rd ID] - 무시할 수 있음

### 지표

* [!UICONTROL Activity Impressions] - [!UICONTROL Entrants] 보고서의 [!DNL Target] 숫자와 일치합니다.
* [!UICONTROL Activity Conversions] - [!UICONTROL Custom Conversions] 보고서의 [!DNL Target] 숫자와 일치합니다.

[!DNL Analysis Workspace]에서 [!UICONTROL Analytics for Target] 패널을 사용하여 향상도와 신뢰도로 [!DNL Target] 활동 및 경험을 분석하십시오. 자세한 내용은 [Analytics 도구 안내서](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=ko-KR)의 *Analytics for Target(A4T) 패널*&#x200B;을 참조하십시오.

>[!IMPORTANT]
>
>[!UICONTROL Target Activities]의 [!DNL Analytics] 보고서에 활동을 나열하는 대신 &quot;지정되지 않음&quot;이 나열되면 프로비저닝된 계정에 업데이트가 필요합니다. 이 문제를 해결하려면 고객 지원팀에 문의하십시오.

자세한 내용 및 예를 보려면 Adobe Experience League에서 제공한 [Analytics &amp; Target: 분석 우수 사례](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) 자습서를 여십시오.

## [!DNL Target]의 보고서 {#section_C0D1F17F88374B6690BF904D7B83B42E}

[!DNL Analytics]을(를) 보고 소스로 사용하면 [!DNL Target]의 보고서에는 [!DNL Analytics]에서 수집한 데이터가 표시됩니다. 이 보고서는 다른 [!DNL Target] 보고서와 다소 다릅니다.

* [!UICONTROL Audiences] 목록에는 [!DNL Analytics] 보고서 세트에 사용할 수 있는 대상이 표시됩니다.
* [!UICONTROL Metric] 목록에는 [!DNL Analytics]을(를) 통해 사용할 수 있는 모든 지표가 표시됩니다.

  [!DNL Analytics]에 내장된 사용자 지정 지표 또는 계산된 지표를 포함하여 모든 지표를 사용할 수 있습니다.

  증가가 원하지 않는 경우에도 증가하는 숫자는 보고서에서 양수로 표시됩니다. 예를 들어 낮은 바운스 비율이 필요하더라도 상승도가 가장 높은 우승자로 높은 바운스 비율이 표시됩니다. 이러한 지표 및 유사 지표에 유의하여 보고서를 기준으로 수치를 높일지 또는 줄일지 결정을 내려야 합니다.

활동이 시작된 후 또는 테스트가 완료된 후에도 [!DNL Target]의 보고서에 지표 또는 대상을 적용할 수 있습니다. 측정할 사항을 사전에 정확히 알 필요는 없습니다.

활동 보고서 페이지에서 바로 전체 [!DNL Analytics] 보고서를 보려면 클릭하십시오.

## 활동 만들기 {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

활동을 만드는 동안 [!UICONTROL Settings] 페이지에서 활동에 대한 목표를 지정해야 합니다. 이 목표는 보고서의 기본 지표가 되며 지표 선택기에서 첫 번째 옵션으로 항상 표시됩니다. 일반 Target 활동에서와 같이 보고용 세그먼트를 선택할 수는 없습니다. [!DNL Analytics]이(가) 있는 테스트에서는 [!DNL Adobe Analytics]개의 대상이 아닌 [!DNL Target]개의 세그먼트를 사용합니다.

## Analytics for Adobe Target (A4T)에 사용할 오프라인 계산 수행 {#section_B34BD016C8274C97AC9564F426B9607E}

[!DNL Target] [Complete Confidence Calculator](/help/main/assets/complete_confidence_calculator.xlsx) Excel 파일을 사용하여 A4T의 신뢰도 및 신뢰도 간격에 대해 오프라인 계산을 수행할 수 있지만 [!DNL Analytics]의 데이터 내보내기 단계가 필요합니다.

A4T의 경우 연속 변수(이진 지표가 아님)에 대해 [Welch의 t-test](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} 계산을 사용합니다. Analytics에서 방문자는 항상 추적되며 수행된 모든 작업이 카운트됩니다. 따라서 방문자가 여러 번 구입하거나 성공 지표를 여러 번 방문하면 해당 추가 히트가 카운트됩니다. 이 작업으로 지표는 연속 변수가 됩니다. Welch의 t-test 계산을 수행하기 위해서는 t-통계량의 분모에 사용되는 분산을 계산하기 위해 &quot;제곱합&quot;이 필요하다. [A/Bn 테스트의 통계 계산](/help/main/c-reports/statistical-methodology/statistical-calculations.md)에서는 사용된 수학 공식의 세부 정보를 설명합니다. [!DNL Analytics]에서 제곱합을 검색할 수 있습니다. 제곱합 데이터를 얻으려면, 최적화할 지표에 대한 방문자 수준 내보내기를 샘플 기간 동안 수행해야 합니다.

예를 들어 방문자당 페이지 보기 수를 최적화하는 경우 지정된 기간(약 2일) 동안 방문자당 기준으로 총 페이지 보기 수 샘플을 내보낼 수 있습니다(수천 개의 데이터 포인트만 필요한 경우). 그런 다음 각 값을 제곱하고 이 제곱들의 총합을 구합니다(여기서 연산 순서가 매우 중요합니다.). 그런 다음 이 &quot;제곱합&quot; 값은 Complete Confidence Calculator에서 사용됩니다. 이 값에 해당 스프레드시트의 &quot;수입&quot; 섹션을 사용하십시오.

**[!DNL Analytics] 데이터 내보내기 기능을 사용하여 다음을 수행하십시오.**

1. [!DNL Adobe Analytics]에 로그인합니다.
1. **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Data Warehouse Request]** 탭에서 필드를 채웁니다.

   각 필드에 대한 자세한 내용은 [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html)의 &quot;데이터 웨어하우스 설명&quot;을 참조하십시오.

   | 필드 | 지침 |
   |--- |--- |
   | 요청 이름 | 요청에 사용할 이름을 지정하십시오. |
   | 보고 날짜 | 기간 및 세부기간을 지정하십시오.<br>가장 좋은 방법은 첫 번째 요청에 대해 1시간 또는 하루 이하의 데이터를 선택하는 것입니다.  Data Warehouse 파일은 요청된 시간이 길수록 처리하는 데 걸리는 시간도 더 걸리므로, 항상 파일이 예상한 결과를 반환하도록 작은 기간 데이터를 먼저 요청하는 것이 좋습니다. 그런 다음 요청 관리자로 이동하여 요청을 복제하고 두 번째는 더 많은 데이터를 요청하십시오. 또한 세부 기간을 &quot;없음&quot; 이외의 값으로 전환하면 파일 크기가 크게 증가합니다.<br>![Data Warehouse](/help/main/c-reports/assets/datawarehouse.png) |
   | 사용 가능한 세그먼트 | 필요에 따라 세그먼트를 적용하십시오. |
   | 분류 | 원하는 차원을 선택합니다. 표준은 즉시 사용할 수 있는(OOTB) 반면, 사용자 지정에는 eVar 및 prop이 포함됩니다. Experience Cloud 방문자 ID 보다는 방문자 ID 수준 정보가 필요한 경우 &quot;방문자 ID&quot;를 사용하는 것이 좋습니다.<ul><li>방문자 ID는 Analytics에서 사용되는 최종 ID로서, AID(이전부터 있었던 고객인 경우) 또는 MID(MC 방문자 ID 서비스가 시작된 이후 신규 고객이거나 쿠키가 지워진 고객인 경우)입니다.</li><li>Experience Cloud 방문자 ID는 MC 방문자 ID 서비스가 시작된 이후 새 쿠키 또는 지워진 쿠키인 고객에 대해서만 설정됩니다.</li></ul> |
   | 지표 | 원하는 지표를 선택하십시오. 표준은 OOTB인 반면, 사용자 지정에는 사용자 지정 이벤트가 포함됩니다. |
   | 보고서 미리 보기 | 보고서를 예약하기 전에 설정을 검토하십시오.<br>![Data Warehouse 2](/help/main/c-reports/assets/datawarehouse2.png) |
   | 배달 예약 | 파일을 배달할 전자 메일 주소를 입력하고 파일 이름을 지정한 다음 [!UICONTROL Send Immediately]을(를) 선택하십시오.<br>참고: [!UICONTROL Advanced Delivery Options]<br>![배달 예약](/help/main/c-reports/assets/datawarehouse3.png)에서 FTP를 통해 파일을 배달할 수 있습니다. |

1. **[!UICONTROL Request this Report]** 아이콘을 클릭합니다.

   파일 배달은 요청된 데이터의 양에 따라 최대 72시간이 걸릴 수 있습니다. 언제든지 [!UICONTROL Tools] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager]을(를) 클릭하여 요청 진행 상황을 확인할 수 있습니다.

   과거에 요청한 데이터를 다시 요청하려면 필요에 따라 [!UICONTROL Request Manager]에서 이전 요청을 복제할 수 있습니다.

[!DNL Data Warehouse]에 대한 자세한 내용은 [!DNL Analytics] 도움말 설명서에서 다음 링크를 참조하십시오.

* [Data Warehouse 요청 만들기](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html)
* [Data Warehouse 모범 사례](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html)
