---
keywords: 보고서;보고서 다운로드;csv;성공 지표;주문 세부 사항
description: Adobe에서 데이터를 다운로드하는 방법 알아보기 [!DNL Target] 활동을 CVS 형식으로 만들어 Excel, Access 또는 기타 데이터 분석 프로그램으로 빠르게 가져올 수 있습니다.
title: 보고서 데이터를 CSV 파일로 다운로드하려면 어떻게 합니까?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
source-git-commit: fc1dcc2b6de1248c35191c1ecd7b36aeb891fd3f
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 54%

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

   ![다운로드 옵션](/help/main/c-reports/assets/download-options.png)

## [!UICONTROL 보고서를 CSV로 내보내기] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

다음 [!UICONTROL 성공 지표] 이 보고서는 성공 지표와 다음에 있는 에서 사용할 수 없는 지표에 대한 정보를 보여줍니다. [!DNL Target] UI:

* 전환까지의 평균 시간(시간 단위). 따라서 평균 방문자가 전환 지점에 도달하기까지 소요되는 시간을 확인할 수 있습니다.
* 오프라인 통계적 신뢰도 계산을 위한 매출 합계, 제곱

데이터는 활동이 끝날 때까지 저장됩니다.

>[!NOTE]
>
>CSV 보고서는 원시 데이터만 포함하며 A/B 테스트에 사용되는 방문자당 수입, 상승도 또는 신뢰도와 같이 계산된 지표는 포함하지 않습니다. 이러한 계산된 지표를 계산하려면 [!DNL Target] [완료 신뢰도 계산기](/help/main/assets/complete_confidence_calculator.xlsx) 활동의 값을 입력하거나 검토할 Excel 파일 [A/Bn 테스트의 통계 계산](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL 주문 세부 사항을 CSV로 내보내기] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

다음 [!UICONTROL 주문 세부 사항] 이 보고서는 다음 항목을 포함하여 주문에 대한 정보를 제공합니다.

* 주문 날짜 및 시간
* 주문 수량(mbox 주문하기를 삽입한 경우)

   다음 [!UICONTROL 주문 세부 사항] 보고서는 주문이 있는 경우에만 작동합니다.

* 주문 플래그(중복 또는 예외적인 주문)

   평균 주문 값에서 +/- 3 표준 편차 이상인 경우 주문이 예외로 표시됩니다. 이 계산에서는 마지막 달의 데이터를 사용합니다(계산이 수행된 시점까지). 활동이 한 시간 동안 실행되었거나 15건의 주문이 발생하면, 어느 쪽이 먼저인지 상관없이 예외적인 주문을 제외하게 됩니다. 자세한 내용은 [예외적인 주문 제외](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA)를 참조하십시오.

* 제품 ID

   쉼표와 연결된 제품 ID의 총 길이가 255자를 초과할 수 없거나 ID가 보고서에 제대로 표시되지 않습니다. 예를 들어 주문에 ID가 &quot;aa, bb&quot;인 제품이 포함되어 있으면 총 길이는 &quot;aa,bb&quot; = 5가 됩니다.

* 경험

   [!UICONTROL A/B 테스트], [!UICONTROL 경험 타깃팅] (XT) 및 [!UICONTROL 다변량 테스트] (MVT) 활동을 위 [!UICONTROL 주문 세부 사항]에서 [!UICONTROL 경험] 열에는 `localId`가 있습니다. 이것은 오퍼 토큰에 있는 `$campaign.recipe.id`의 값 출력입니다.

   [!UICONTROL 자동화된 개인화] (AP) 활동을 위한 [!UICONTROL 경험] 열은 없습니다. [!UICONTROL 의 다른 곳에 표시된 대로, 현재 ]알고리즘 이름[!DNL Target] 열은 &quot;통제&quot; 및 &quot;타깃팅된&quot; 용어로 대체되었습니다.

   [!UICONTROL 권장 사항] 활동에는 영향을 주지 않았습니다.

>[!NOTE]
>
>* 주문 보고서 데이터에는 기본 환경(호스트 그룹)의 경우는 4주, 비기본 환경의 경우는 2주 동안의 데이터가 포함됩니다.
>* &quot;&quot;로 설정된 매출 지표[!UICONTROL 증분 카운트 및 사용자를 활동에 유지]&quot;동일한 방문자가 수행한 첫 번째 주문에 대해서만 주문 세부 사항을 기록하십시오. 모든 후속 주문은 전환 카운트를 증가시키지만 RPV/AOV/매출에는 매출을 추가하지 않으며 [!UICONTROL 주문 세부 사항] 보고서.


## 우수 사례

* 주문 레코드를 기록하려면 `orderTotal` 매개 변수를 전달해야 합니다.
* `ProductPurchasedId` mbox 매개 변수를 통해 전달된 값은 주문 세부 사항 보고서에 나열됩니다.
* 모범 사례는 다음을 포함하는 것입니다. `orderID` 및 `orderTotal`. 이렇게 하면 중복 주문이 자동으로 무시됩니다.

## 주의 사항 {#section_49B9590904A645B18E694B4EFFFC1DEF}

다음 정보는 [!UICONTROL 다운로드] 옵션:

* 다음 두 보고서를 모두 다운로드할 수 있습니다. [!UICONTROL A/B 테스트], [!UICONTROL Automated Personalization], [!UICONTROL 경험 타기팅], 및 [!UICONTROL 다변량] 활동. 다음을 다운로드할 수 없습니다. [!UICONTROL 성공 지표] 다음에 대한 보고서 [!UICONTROL Recommendations] 활동.
* 다음 [!UICONTROL 다운로드] 옵션이에 사용할 수 없음 [!UICONTROL A/B 테스트] 및 [!UICONTROL 경험 타기팅] 다음 시간 이전에 생성된 활동 [!DNL Target] 버전 15.7.1(2015년 7월).
* 연결된 데이터가 없는 경험은 다운로드한 보고서에 기록되지 않습니다.
* 에 적용된 대상 [!DNL Target] 보고 UI는 다운로드 보고서로 넘겨지지 않습니다.
* 활동이 둘 이상의 지표를 사용하는 경우 .csv 파일로 다운로드하기 위해 생성된 보고서가 일관성이 없습니다. 다운로드 가능한 보고서는 보고서 설정만을 기반으로 생성되며 사용된 다른 지표에 대해 동일한 값을 고려합니다. 진실의 소스는 항상 [!DNL Target] UI에 표시되는 보고서입니다.
