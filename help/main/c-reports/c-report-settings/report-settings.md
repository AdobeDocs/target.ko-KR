---
keywords: Target;보고서;보고서 설정;사전 설정;target 사전 설정;지표;대상자;날짜 범위;설정;다운로드;테이블 보기;그래프 보기;평균 리프트;리프트;리프트 경계;신뢰 구간;신뢰도;위치 기여도;평균 실행;방법론 계산
description: 지표, 대상, 날짜 범위 등을 포함하여 Adobe Target에서 보고서 설정을 구성하는 방법에 대해 알아봅니다.
title: 보고서 설정을 구성하는 방법
feature: Reports
exl-id: 337579d1-c678-43b6-9e80-b5abe159c2d3
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '1778'
ht-degree: 48%

---

# 보고서 설정

[!DNL Adobe Target]에서 보고서에 표시할 요소를 설정하는 데 도움이 되는 정보입니다. 보고서 설정은 나중에 사용할 수 있도록 저장할 수 있습니다.

보고서를 표시하려면 다음 작업을 수행하십시오.

1. **[!UICONTROL Activities]**&#x200B;을 클릭한 다음, 목록에서 원하는 활동을 클릭합니다.
1. **[!UICONTROL Reports]** 탭을 클릭합니다.

   ![보고서 UI](/help/main/c-reports/c-report-settings/assets/report-ui-refresh.png)

## Target 사전 설정 {#section_51F67341465045BEB4F1A2FB638A8EB1}

이제 개별 활동의 보고서를 원하는 대로 구성한 후(지표, 날짜 범위, 대상, 고급 설정 등) 그러한 보고서의 여러 사전 설정을 최대 10개까지 저장할 수 있습니다. 만든 사람에 관계없이 모든 [!DNL Target] 사용자가 다양한 사전 설정을 표시, 편집 및 삭제할 수 있습니다.

개별 활동의 보고서를 원하는 대로 구성한 다음 해당 구성을 기본/즐겨 찾는 사전 설정으로 저장할 수도 있습니다. 해당 활동 보고서를 볼 때마다 표시되는 보기입니다.

### 사전 설정 또는 기본 사전 설정 만들기

1. 활동의 보고서를 원하는 대로 구성합니다.

   지표, 날짜 범위, 대상, 고급 설정 등을 포함하여 사용 가능한 설정은 아래에 설명되어 있습니다.

1. **[!UICONTROL Target Preset]** 옆에 있는 **[!UICONTROL More Options]**( ![추가 옵션 아이콘](/help/main/assets/icons/MoreSmallListVert.svg) ) 아이콘 > **[!UICONTROL Save as New]**&#x200B;을(를) 클릭합니다.

   [!UICONTROL Create Preset] 대화 상자가 표시됩니다.

   ![새 사전 설정 대화 상자](/help/main/c-reports/c-report-settings/assets/report_preset_dialog-new.png)

1. **[!UICONTROL Filters]** 섹션의 정보를 검토하여 보고서가 원하는 대로 구성되었는지 확인한 다음 **[!UICONTROL Preset Name]**(최대 50자)을 지정하십시오.
1. (조건부) 기본/즐겨 찾는 보고서 보기로 설정하려면 **[!UICONTROL Set as default preset]** 토글을 [켜짐] 위치로 밉니다.
1. **[!UICONTROL Create]** 아이콘을 클릭합니다.

### 다른 사전 설정 선택

**[!UICONTROL Target Preset]** 드롭다운 목록에서 원하는 사전 설정을 선택합니다.

### 사전 설정 편집

1. 편집할 사전 설정을 선택합니다.
1. 보고서의 구성을 원하는 대로 편집합니다(지표, 날짜 범위, 대상, 고급 설정 등).

   보고서의 구성을 편집한 후 [!UICONTROL Save]을(를) 클릭하면 사전 설정 이름 뒤에 별표(&#42;)가 표시되어 사전 설정이 변경되었음을 나타냅니다.

1. 새 사전 설정을 만들려면 **[!UICONTROL More Options]**( ![추가 옵션 아이콘](/help/main/assets/icons/MoreSmallListVert.svg) ) 아이콘 > **[!UICONTROL Save as New]**&#x200B;을(를) 클릭합니다.

### 사전 설정 삭제

1. 삭제할 사전 설정을 선택합니다.
1. **[!UICONTROL More Options]**( ![추가 옵션 아이콘](/help/main/assets/icons/MoreSmallListVert.svg) ) 아이콘 > **[!UICONTROL Delete]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Delete]**&#x200B;을(를) 다시 클릭하여 삭제를 확인합니다(삭제된 사전 설정은 복구할 수 없음).

### 사전 설정 오류 처리

보고서 내의 경고 및 메시지를 통해 사전 설정이 유효하지 않은 상태가 되는지 알 수 있습니다. 경고 또는 메시지에 올바른 사전 설정을 작성하기 위한 다른 대상, 지표, 호스트 그룹 또는 경험을 선택하라고 표시됩니다.

다음 목록은 사전 설정이 유효하지 않을 수 있는 몇 가지 상황을 설명합니다.

* 보고 대상이 활동에서 제거되었지만, 사전 설정된 정의에서 참조됩니다.
* 하나 이상의 지표가 삭제되었지만 사전 설정된 정의에서 참조됩니다. 예를 들어, 활동에서 하나 이상의 지표를 삭제한 다음 지표를 새로 추가할 수 있습니다.
* 하나 이상의 호스트 그룹(환경)이 존재하지 않지만 사전 설정된 정의에서 참조됩니다.
* 사전 설정이 작성된 후에 하나 이상의 경험이 삭제되었지만 사전 설정된 정의에서 참조됩니다.
* 참조된 엔티티가 있지만 사전 설정 정의가 의미상 변경되는 방식으로 업데이트되었으므로 사전 설정이 의미상 잘못되었습니다. 예를 들어 처음에 &quot;Revenue on Chrome&quot;이라는 사전 설정된 이름을 만들었다고 가정해 보겠습니다. 나중에 활동을 업데이트하여 수입 대신 전환 지표를 측정합니다. 활동 정의에 대한 이 업데이트는 사전 설정 정의를 의미적으로 무효화합니다.

## [!UICONTROL Report Metric] {#section_894ABD7148244806B7CE556EBBA2AD62}

**[!UICONTROL Report Metric]** 드롭다운 목록을 클릭하면 다른 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) 또는 여러 지표를 선택하여 그래프 및 차트로 표시할 수 있습니다.

기본적으로, 기본 지표는 활동을 작성할 때 성공 지표 설정에서 결정됩니다. 설정을 변경하고 활동을 다시 저장하면 보고에 대한 기본 지표가 업데이트됩니다.

보고서에서 볼 여러 지표를 선택하는 방법에 대한 자세한 내용은 [보고서에서 여러 지표 보기](/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7)를 참조하십시오.

## [!UICONTROL Audience] {#section_70926EB4618945D9AFF2B0564FF3717B}

보고서에 대해 표시된 대상을 변경하려면 **[!UICONTROL Audience]** 드롭다운 목록을 클릭하십시오.

자세한 내용은 [대상자](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522)를 참조하십시오.

## [!UICONTROL Preset Date Range]

**[!UICONTROL Preset Date Range]** 드롭다운 목록을 클릭하여 사전 설정된 날짜 범위 중에서 선택합니다.

보고서에 대한 새 **[!UICONTROL Start]** 및 **[!UICONTROL End]** 날짜를 선택하십시오. **[!UICONTROL Start of Activity]** 및 **[!UICONTROL Start of activity - End of Activity]** 범위도 사용할 수 있습니다.

사전 정의된 날짜 범위에는 최근 7일, 최근 15일 또는 최근 30일이 포함됩니다. 이러한 사전 정의된 날짜 범위는 순환 범위입니다. 시작 일자가 선택한 일 수보다 작은 경우 달력에는 시작 일자의 범위가 표시되지만 시작 일자가 활동 기간 증가에 따라 선택한 일 수보다 오래된 경우 롤온됩니다.

보고서 날짜는 다음과 같이 제한됩니다.

* 보고서의 시작 날짜는 지난 2년 이내여야 합니다.
* 오퍼 그룹 보고서는 현재 날짜로부터 99일로 제한됩니다.
* 시간별 보고서는 15일로 제한됩니다.

## 날짜 범위 {#section_A410A768403C4E01891F95CB357E63ED}

[!UICONTROL Date Range] 상자에 보고서의 현재 날짜 범위가 표시됩니다. **[!UICONTROL Calendar]**( ![달력 아이콘](/help/main/assets/icons/Calendar.svg)) 아이콘을 클릭하여 보고서의 날짜 범위를 변경할 수 있는 달력을 표시합니다.

## 설정의 지침을 완료하여 이 설정을 변경할 수 있습니다 {#section_D99CE462107D45CABE0960F820E1E972}

보고서 설정을 구성하려면:

1. **[!UICONTROL Report Settings]**( ![보고서 설정 아이콘](/help/main/assets/icons/Setting.svg) ) 아이콘을 클릭하고 원하는 대로 변경합니다(아래 설명).
1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

선택한 활동 유형에 따라 선택 사항이 달라집니다.

### 계산 방법

원하는 방법을 선택합니다.

* 방문자 수
* 방문 횟수
* 활동 노출 횟수

### 컨트롤

상승도를 계산하고 비교할 때 사용할 제어 경험을 선택하십시오.

### 환경 {#environment}

보고서에 사용할 환경(호스트 그룹)을 선택하십시오. 자세한 내용은 [호스트](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E)를 참조하십시오.

>[!NOTE]
>
>조직에서 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=ko){target=_blank}(AEP)을 사용하여 [!DNL Target]에 지표 데이터를 보내는 경우 AEP 데이터 스트림의 환경이 [!DNL Target] 보고서 설정의 환경과 일치해야 합니다.

### 보고 데이터 재설정

[!UICONTROL Reset Report Data]을(를) 클릭합니다. 이전 데이터를 제거하려면 보고 데이터를 재설정하십시오. 현재 방문자는 활동에 남아 있습니다.  이 옵션은 [!UICONTROL Approver] 권한이 있는 사용자만 사용할 수 있습니다.

>[!IMPORTANT]
>
>영구적인 작업으로서, 실행을 취소할 수 없습니다.

예외적인 값 제외

[!UICONTROL Exclude Extreme Values] 전환은 매출 및 참여 지표 유형이 있는 활동에만 적용됩니다. 자세한 내용은 [예외적인 주문 제외](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA)를 참조하십시오.

## 다운로드 {#section_77E65C50BAAF4AB79242DB3A8778ADEF}

**[!UICONTROL Download]**( ![다운로드 아이콘](/help/main/assets/icons/Download.svg)) 아이콘을 클릭하여 Excel, Access 또는 기타 데이터 분석 프로그램으로 빠르게 가져올 수 있도록 보고서 데이터를 [!DNL .csv] 형식으로 다운로드합니다.

자세한 내용은 [CSV 파일로 데이터 다운로드](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md)를 참조하십시오.

## 새로 고침 {#section_E203729F2F314DF3856D2EE67C60B370}

전체 페이지, 페이지 구성 또는 날짜 범위를 새로 고치지 않고 보고서의 테이블 및 그래프 보기를 새로 고치려면 **[!UICONTROL Refresh]** ( ![새로 고침 아이콘](/help/main/assets/icons/Refresh.svg) ) 아이콘을 클릭하십시오.

## 추가 옵션 {#section_AB1B5C695D7045A0A0AC0E2698D2E7DE}

**[!UICONTROL More Options]** 아이콘(![추가 옵션 아이콘](/help/main/assets/icons/MoreSmallListVert.svg) )을 클릭하여 [!UICONTROL Save as New] 및 [!UICONTROL Delete] 옵션에 액세스합니다.

## 옵션 보기

활동 유형에 따라 다양한 형식으로 보고서를 볼 수 있습니다. 원하는 옵션을 선택합니다.

* **테이블 보기**: 보고서를 테이블로 보려면 **[!UICONTROL Table View]**( ![테이블 보기 아이콘](/help/main/assets/icons/Table.svg)) 아이콘을 클릭하십시오.
* **그래프 보기**: 보고서를 그래프로 보려면 **[!UICONTROL Graph View]**( ![그래프 보기 아이콘](/help/main/assets/icons/GraphTrend.svg)) 아이콘을 클릭하십시오.
* **자동화된 세그먼트**:([!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL Auto-Target] (AT) 활동에만 사용 가능) **[!UICONTROL Automated Segments] ( ![자동화된 세그먼트 아이콘](/help/main/assets/icons/AutomatedSegment.svg) ) 아이콘을 클릭하여 [자동화된 세그먼트 보고서](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md)를 봅니다.
* **중요 특성**: ([!DNL Automated Personalization] (AP) 및 [!UICONTROL Auto-Target] (AT) 활동에만 사용 가능) **[!UICONTROL Important Attributes]**( ![중요 특성 아이콘](/help/main/assets/icons/ViewList.svg)) 아이콘을 클릭하여 [중요 특성 보고서](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md)를 봅니다.

## 평균 상승도, 상승도 한계 및 신뢰 구간 {#section_0D87615B1D3344B3858BA494EEBC16FB}

보고서는 활동과 연결된 상승도 한계와 신뢰 수준을 이해하는 유용한 몇 가지 데이터 포인트와 시각화 표현을 포함합니다. 이러한 항목들을 포함하는 것은 승자를 보다 정확하게 판별하는 데 도움이 됩니다.

자세한 내용은 [A/Bn 테스트의 통계 계산](/help/main/c-reports/statistical-methodology/statistical-calculations.md)을 참조하십시오.

다음 사항을 고려하십시오.

* [!UICONTROL Table View]에서 보고서를 볼 때만 사용할 수 있습니다.
* 이 기능은 [Analytics를 보고 소스로 사용(A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md)하는 활동에는 사용할 수 없습니다.

## 위치 기여도 {#section_5832F126AC114AE1ABFFF4D9B904393B}

MVT(다변량 테스트) 활동에 대한 위치별 기여도를 표시하도록 보고서를 전환하려면 [[!UICONTROL Location Contribution]](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md)( ![위치 기여도 아이콘](/help/main/assets/icons/LocationContribution.svg)) 아이콘을 클릭하십시오.

## 경험 {#section_3A450DE1FA7E43F0AAB73165EC3D1C34}

[!UICONTROL Graph View]에서 보고서를 볼 때만 사용할 수 있습니다.

차트에서 경험을 표시하거나 숨기려면 차트의 왼쪽에서 해당 경험을 선택하거나 선택 취소하십시오.

## 평균 실행 {#section_59066693158C4433B87D07402C2BC6CD}

[!UICONTROL Graph View]에서 보고서를 볼 때만 사용할 수 있습니다.

&quot;평균 실행&quot;은 누적 전환율(보고 기간 시작부터 그래프에 표시된 날짜까지)을 누적 방문자로 나눈 값을 반영합니다.

원하는 그래프 보기를 선택하십시오.

* 평균 실행
* 평균 상승도 실행
* 일별
* 일별 상승도

이 드롭다운 목록의 이름은 선택한 보기에 따라 다르지만 위에 나열된 보기 중 하나가 됩니다.

## 계산 방법 {#section_01B0ED5665C74AE1AE97259800190C3E}

[!UICONTROL Graph View]에서 보고서를 볼 때만 사용할 수 있습니다.

보고서에서 그래프에 대한 계산 방법론을 선택할 수 있습니다. [!UICONTROL Automated Personalization] (AP) 활동에는 지원되지 않습니다.

그래프 모드에서 보고서를 보는 동안 [!UICONTROL Counting Methodology] 옵션에 액세스하려면 **[!UICONTROL My Primary Goal]** 드롭다운을 클릭한 다음 계산 방법을 선택하십시오.

계산 방법론은 위에서 설명한 [!UICONTROL Settings] 대화 상자에서 선택한 방법론과 동일합니다.

기본적으로 그래프는 [!UICONTROL Daily] 모드로 표시됩니다.

[!UICONTROL Daily] 드롭다운 목록을 클릭한 다음 누적 옵션을 선택하여 모드를 변경할 수 있습니다.

>[!NOTE]
>
>이 드롭다운 목록의 이름은 선택한 모드에 따라 달라집니다.

[!UICONTROL Auto-Target] 활동에 대한 네 가지 모드, 즉 [!UICONTROL Daily Control], [!UICONTROL Daily Targeted], [!UICONTROL Cumulative Control] 및 [!UICONTROL Cumulative Targeted]가 있습니다.

그래프가 작성되는 기본 순서는 다음과 같습니다.

* **[!UICONTROL A/B Test] ([!UICONTROL Auto-Allocate] 및 [!UICONTROL Automated Personalization] 포함)**: 내림차순으로 경험 생성 순서.
* **[!UICONTROL Experience Targeting] (XT)**: 활동의 경험 순서.
* **[!UICONTROL Multivariate Test] (MVT)**: 경험 이름별 알파벳순
* **[!UICONTROL Recommendations]**: 내림차순으로 작성된 경험 순서입니다.

[!UICONTROL Counting Methodology] 옵션을 사용하여 작업할 때 다음 주의 사항을 고려하십시오.

* [[!UICONTROL Auto-Target] 활동](/help/main/c-activities/auto-target/auto-target-to-optimize.md)의 경우 계산 방법론으로 &quot;방문자&quot;를 선택할 수 있는 옵션이 없습니다. [!UICONTROL Auto-Target]은(는) 방문자별로 플롯할 수 없는 유일한 활동 유형입니다.
* [Analytics를 보고 소스로 사용(A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md)하는 활동의 경우 방문자, 방문 또는 노출을 누적하여 플롯할 수 없습니다.

## 활동에 16개 이상의 경험이 있는 그래프 작업

활동에 16개 미만의 경험이 있다면 각 경험은 그래프에서 서로 다른 색상으로 이 표시됩니다.

활동에 16개가 넘는 경험이 있다면 처음 16개의 경험에 대해서는 색상이 지정된 선이 그래프에 표시되고, 나머지 경험은 왼쪽에 있는 경험 창에 회색으로 표시되며 그래프에는 해당 그래프 선이 표시되지 않습니다. 16개 경험에 대한 선만 지정된 시간에 표시할 수 있습니다.

회색으로 처리된 경험을 마우스로 가리키면 그 경험에 해당하는 새로운 회색 그래프 선이 그래프에 임시로 표시됩니다. 회색으로 처리된 경험의 그래프 선을 어떤 색상으로 표시하기 위해서는 컬러로 표시되는 한 경험의 이름을 클릭하여 선택 취소한 다음, 회색으로 처리된 원하는 경험의 이름을 클릭하여 이 경험을 선택할 수 있습니다.

이 그래프는 처음 16개의 경험에 대한 선을 표시합니다(일부는 겹쳐져서 선이 16개 미만으로 표시됩니다.). 왼쪽에 있는 경험 패널에서 각 경험 이름 옆에 있는 색상이 지정된 점은 그 경험의 그래프 선이 해당 색상으로 표시되고 있음을 나타냅니다.

경험 창에서 아래로 스크롤하면 다음 그림과 같이 17번째부터 26번째 경험까지는 이름이 회색으로 표시됩니다.

회색으로 처리된 경험 중 하나를 마우스로 가리키면 그 경험에 해당하는 새로운 회색 그래프 선이 그래프에 임시로 표시됩니다.

경험 R에 대한 그래프 선을 표시하고 경험 P에 대한 선은 표시하지 않으려 한다고 가정하십시오. 경험 P의 이름을 클릭하여 선택을 취소한 다음, 경험 R의 이름을 클릭하여 아래와 같이 선택할 수 있습니다.
