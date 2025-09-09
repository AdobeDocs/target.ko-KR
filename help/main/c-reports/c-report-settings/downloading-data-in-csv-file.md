---
keywords: 보고서;보고서 다운로드;csv;성공 지표;주문 세부 사항
description: Excel, Access 또는 기타 데이터 분석 프로그램으로 빠르게 가져올 수 있도록 CVS 형식으로 Adobe [!DNL Target] 활동에서 데이터를 다운로드하는 방법에 대해 알아봅니다.
title: 보고서 데이터를 CSV 파일로 다운로드하려면 어떻게 합니까?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
source-git-commit: e42398b8774fff57c00658636a52bd0038ad94b4
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 30%

---

# CSV 파일로 데이터 다운로드

데이터를 .csv 형식으로 다운로드하면 [!DNL Excel], [!DNL Access] 또는 기타 데이터 분석 프로그램으로 빠르게 가져올 수 있습니다.

데이터를 CSV 파일로 다운로드하려면 다음을 수행하십시오.

1. **[!UICONTROL Activities]**&#x200B;을 클릭한 다음, 목록에서 원하는 활동을 클릭합니다.

   많은 활동이 있는 경우 필터( ![필터 아이콘](/help/main/assets/icons/Filter.svg) ) 아이콘을 클릭하여 [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] 및 [!UICONTROL Activity Source] 드롭다운 목록에서 옵션을 선택하여 목록을 필터링합니다.

1. **[!UICONTROL Reports]** 탭을 클릭합니다.
1. **[!UICONTROL Download]**( ![다운로드 아이콘](/help/main/assets/icons/Download.svg)) 아이콘을 클릭한 다음 Excel 및 기타 도구에서 분석할 수 있도록 다운로드할 보고서 유형을 선택하십시오.

   * [!UICONTROL Export Reports to CSV]
   * [!UICONTROL Export Order Details to CSV]

## 인기도 및 키 기반 알고리즘에 대한 CSV 다운로드 형식 {#format}

CSV 다운로드 파일은 백엔드 기준 실행 후 생성된 결과를 일관되게 반영합니다.

**인기도 알고리즘(키가 아닌 기반)의 경우 파일에 다음이 포함됩니다.**

* 앞에 *가 붙은 백업 권장 사항 행
* 알고리즘 설정을 기반으로 한 권장 사항을 나열하는 별도의 행

**키 기반 알고리즘의 경우 파일에 다음이 포함됩니다.**

* 인기도 알고리즘과 유사한 백업 행
* 첫 번째 항목이 키의 제품 ID이고 그 뒤에 추천 후보를 나타내는 쉼표로 구분된 제품 ID가 오는 키-값 형식의 여러 행

## [!UICONTROL Export Report to CSV] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

[!UICONTROL Success Metrics] 보고서는 [!DNL Target] UI에서 사용할 수 없는 성공 지표와 다음 지표에 대한 정보를 보여줍니다.

* 전환까지의 평균 시간(시간 단위). 따라서 평균 방문자가 전환 지점에 도달하기까지 소요되는 시간을 확인할 수 있습니다.
* 오프라인 통계적 신뢰도 계산을 위한 매출 합계, 제곱

데이터는 활동이 끝날 때까지 저장됩니다.

>[!NOTE]
>
>CSV 보고서는 원시 데이터만 포함하며 A/B 테스트에 사용되는 방문자당 수입, 상승도 또는 신뢰도와 같이 계산된 지표는 포함하지 않습니다. 이러한 계산된 지표를 계산하려면 [!DNL Target] [Complete Confidence Calculator](/help/main/assets/complete_confidence_calculator.xlsx) Excel 파일을 다운로드하여 활동의 값을 입력하거나, [A/Bn 테스트의 통계 계산](/help/main/c-reports/statistical-methodology/statistical-calculations.md)을 검토하십시오.

## [!UICONTROL Export Order Details to CSV] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

[!UICONTROL Order Details] 보고서는 다음 항목을 포함하여 주문에 대한 정보를 표시합니다.

* 주문 날짜 및 시간
* 주문 수량(mbox 주문하기를 삽입한 경우)

  [!UICONTROL Order Details] 보고서는 주문이 있는 경우에만 작동합니다.

* 주문 플래그(중복 또는 예외적인 주문)

  평균 주문 값에서 +/- 3 표준 편차 이상인 경우 주문이 예외로 표시됩니다. 이 계산에서는 마지막 달의 데이터를 사용합니다(계산이 수행된 시점까지). 활동이 한 시간 동안 실행되었거나 15건의 주문이 발생하면, 어느 쪽이 먼저인지 상관없이 예외적인 주문을 제외하게 됩니다. 자세한 내용은 [예외적인 주문 제외](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA)를 참조하십시오.

* 제품 ID

  쉼표와 연결된 제품 ID의 총 길이가 255자를 초과할 수 없거나 ID가 보고서에 제대로 표시되지 않습니다. 예를 들어 주문에 ID가 &quot;aa, bb&quot;인 제품이 포함되어 있으면 총 길이는 &quot;aa,bb&quot; = 5가 됩니다.

* 경험

  [!UICONTROL Order Details], [!UICONTROL A/B Test]&#x200B;(XT) 및 [!UICONTROL Experience Targeting]&#x200B;(MVT) 활동에 대한 [!UICONTROL Multivariate Test] 보고서에서 [!UICONTROL Experience] 열에는 `localId` 경험이 포함되어 있습니다. 이것은 오퍼 토큰에 있는 `$campaign.recipe.id`의 값 출력입니다.

  [!UICONTROL Experience]&#x200B;(AP) 활동에 대한 [!UICONTROL Automated Personalization] 열이 없습니다. [!UICONTROL Algorithm Name]의 다른 곳에 표시된 대로 현재 [!DNL Target] 열이 &quot;컨트롤&quot; 및 &quot;타깃팅된&quot; 용어로 대체되었습니다.

  [!UICONTROL Recommendations] 활동에 영향을 주지 않았습니다.

>[!NOTE]
>
>* 주문 보고서 데이터에는 기본 환경(호스트 그룹)의 경우는 4주, 비기본 환경의 경우는 2주 동안의 데이터가 포함됩니다.
>* &quot;[!UICONTROL Increment count and keep the user in the activity]&quot;(으)로 설정된 매출 지표는 동일한 방문자가 수행한 첫 번째 주문에 대해서만 주문 세부 정보를 기록합니다. 모든 후속 주문은 전환 수를 증가시키지만 RPV/AOV/매출에는 매출을 추가하지 않으며 [!UICONTROL Order Details] 보고서에 포함되지 않습니다.

## 우수 사례

* 주문 레코드를 기록하려면 `orderTotal` 매개 변수를 전달해야 합니다.
* `ProductPurchasedId` mbox 매개 변수를 통해 전달된 값은 [!UICONTROL Order Details] 보고서에 나열됩니다.
* 가장 좋은 방법은 `orderID` 및 `orderTotal`을(를) 포함하는 것입니다. 이렇게 하면 중복 주문이 자동으로 무시됩니다.

## 주의 사항 {#section_49B9590904A645B18E694B4EFFFC1DEF}

다음 정보는 [!UICONTROL Download] 옵션에 적용됩니다.

* [!UICONTROL A/B Test], [!UICONTROL Automated Personalization], [!UICONTROL Experience Targeting] 및 [!UICONTROL Multivariate] 활동에 대한 보고서를 모두 다운로드할 수 있습니다. [!UICONTROL Success Metrics] 활동에 대한 [!UICONTROL Recommendations] 보고서를 다운로드할 수 없습니다.
* [!UICONTROL Download] 버전 15.7.1(2015년 7월) 이전에 만든 [!UICONTROL A/B Test] 및 [!UICONTROL Experience Targeting] 활동에는 [!DNL Target] 옵션을 사용할 수 없습니다.
* 연결된 데이터가 없는 경험은 다운로드한 보고서에 기록되지 않습니다.
* [!DNL Target] 보고 UI에 적용된 대상은 다운로드 보고서로 넘겨지지 않습니다.
* 활동이 둘 이상의 지표를 사용하는 경우 .csv 파일로 다운로드하기 위해 생성된 보고서가 일관성이 없습니다. 다운로드 가능한 보고서는 보고서 설정만 기반으로 생성되며 사용된 다른 지표에 대해 동일한 값을 고려합니다. 진실의 소스는 항상 [!DNL Target] UI에 표시되는 보고서입니다.
