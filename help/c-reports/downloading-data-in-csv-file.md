---
keywords: 보고서;보고서 다운로드;csv;성공 지표;주문 세부 사항
description: Adobe [!DNL Target] 활동에서 데이터를 CVS 형식으로 다운로드하여 Excel, Access 또는 기타 데이터 분석 프로그램으로 빠르게 가져오는 방법을 알아봅니다.
title: 보고서 데이터를 CSV 파일로 다운로드하려면 어떻게 합니까?
feature: 보고서
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 83%

---

# CSV 파일로 데이터 다운로드

데이터를 .csv 형식으로 다운로드하면 Excel, Access 또는 기타 데이터 분석 프로그램으로 빠르게 가져올 수 있습니다.

데이터를 CSV 파일로 다운로드하려면 다음을 수행하십시오.

1. **[!UICONTROL 활동]**&#x200B;을 클릭한 다음, 목록에서 원하는 활동을 클릭합니다.

   활동이 많다면 [!UICONTROL 유형], [!UICONTROL 상태], [!UICONTROL 보고 소스], [!UICONTROL 경험 작성기], [!UICONTROL 지표 유형] 및 [!UICONTROL 활동 소스] 드롭다운 목록에서 선택 사항을 선택하여 목록을 필터링할 수 있습니다.

1. **[!UICONTROL 보고서]** 탭을 클릭합니다.
1. **[!UICONTROL 다운로드]** 아이콘을 클릭한 다음, Excel 및 기타 도구에서 분석할 수 있도록 다운로드할 보고서 유형을 선택합니다.

   * [!UICONTROL 보고서를 CSV로 내보내기]
   * [!UICONTROL 주문 세부 사항을 CSV로 내보내기]

   ![다운로드 옵션](/help/c-reports/assets/download-options.png)

## 보고서를 CSV로 내보내기 {#section_38BD9743EB254453B5F4A0A6F2720CD3}

성공 지표 보고서는 Target UI에서 사용할 수 없는 다음 지표와 함께 성공 지표에 대한 정보를 보여줍니다.

* 전환까지의 평균 시간(시간 단위). 따라서 평균 방문자가 전환 지점에 도달하기까지 소요되는 시간을 확인할 수 있습니다.
* 오프라인 통계적 신뢰도 계산을 위한 매출 합계, 제곱

데이터는 활동이 끝날 때까지 저장됩니다.

>[!NOTE]
>
>CSV 보고서에는 원시 데이터만 포함되며 방문자당 매출, 리프트 또는 A/B 테스트에 사용된 신뢰도와 같은 계산된 지표는 포함되지 않습니다. 이러한 계산된 지표를 계산하려면 Target [완전한 신뢰도 계산기](/help/assets/complete_confidence_calculator.xlsx) Excel 파일을 다운로드하여 활동 값을 입력하거나 Target](/help/assets/statistical-calculations.pdf)에 사용되는 [통계 계산을 검토하십시오.

## 주문 세부 사항을 CSV로 내보내기 {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

주문 상세 정보 보고서는 다음을 포함한 주문에 대한 정보를 보여줍니다.

* 주문 날짜 및 시간
* 주문 수량(mbox 주문하기를 삽입한 경우)

   주문 세부 사항 보고서는 주문이 있는 경우에만 작동합니다.

* 주문 플래그(중복 또는 예외적인 주문)

   데이터의 마지막 월을 사용하여 평균 주문 값에서 +/- 3 이상의 표준 편차를 보이는 경우 이 주문은 극단적인 것으로 플래그가 지정됩니다(계산한 시간에 최대 포인트). 활동이 한 시간 동안 실행되었거나 15건의 주문이 발생하면, 어느 쪽이 먼저인지 상관없이 예외적인 주문을 제외하게 됩니다. 자세한 내용은 [예외적인 주문 제외](/help/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA)를 참조하십시오.

* 제품 ID

   쉼표로 연결할 제품 ID의 전체 길이는 255자를 초과하지 않아야 하며 그렇지 않을 경우 ID가 보고서에 제대로 표시되지 않습니다. 예를 들어 주문에 ID가 &quot;aa, bb&quot;인 제품이 포함되어 있으면 총 길이는 &quot;aa,bb&quot; = 5가 됩니다.

* 경험

   [!UICONTROL A/B 테스트], [!UICONTROL 경험 타깃팅] (XT) 및 [!UICONTROL 다변량 테스트] (MVT) 활동을 위 [!UICONTROL 주문 세부 사항]에서 [!UICONTROL 경험] 열에는 `localId`가 있습니다. 이것은 오퍼 토큰에 있는 `$campaign.recipe.id`의 값 출력입니다.

   [!UICONTROL 자동화된 개인화] (AP) 활동을 위한 [!UICONTROL 경험] 열은 없습니다. [!UICONTROL 의 다른 곳에 표시된 대로, 현재 ]알고리즘 이름[!DNL Target] 열은 &quot;통제&quot; 및 &quot;타깃팅된&quot; 용어로 대체되었습니다.

   [!UICONTROL 권장 사항] 활동에는 영향을 주지 않았습니다.

>[!NOTE]
>
>* 주문 보고서 데이터에는 기본 환경(호스트 그룹)의 경우는 4주, 비기본 환경의 경우는 2주 동안의 데이터가 포함됩니다.
>* &quot;증분 카운트 및 사용자를 활동에 유지&quot;로 설정된 수입 지표는 동일한 방문자가 수행한 첫 번째 주문에 대해서만 주문 세부 사항을 기록합니다. 모든 후속 주문은 전환 카운트를 증가시키지만 RPV/AOV/매출에는 매출을 추가하지 않으며 주문 세부 사항 보고서에 포함되지 않습니다.


## 우수 사례

* 주문 레코드를 기록하려면 `orderTotal` 매개 변수를 전달해야 합니다.
* `ProductPurchasedId` mbox 매개 변수를 통해 전달된 값은 주문 세부 사항 보고서에 나열됩니다.
* 가장 좋은 방법은 `orderID`와 `orderTotal`을 모두 포함하는 것입니다. 이렇게 하면 중복 주문이 자동으로 무시됩니다.

## 주의 사항 {#section_49B9590904A645B18E694B4EFFFC1DEF}

다음 정보는 다운로드 선택 사항에 적용됩니다.

* A/B 테스트, Automated Personalization, 경험 타깃팅 및 다변수 활동에 대한 보고서를 모두 다운로드할 수 있습니다.  권장 사항 활동에 대한 성공 지표 보고서는 다운로드할 수 없습니다.
* Target 버전 15.7.1(2015년 7월) 이전에 만들어진 A/B 및 경험 타깃팅 활동에는 다운로드 선택 사항을 사용할 수 없습니다.
* 연결된 데이터가 없는 경험은 다운로드한 보고서에 기록되지 않습니다.
* Target 보고 UI에 적용된 대상은 다운로드 보고서로 넘겨지지 않습니다.
