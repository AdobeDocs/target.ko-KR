---
keywords: analytics for target;a4t;보고 소스로 분석
description: Target(A4T)에 Analytics를 사용하는 방법을 알아봅니다. A4T는 Analytics 지표 및 대상 세그먼트를 사용하는 Target 활동에 대한 Analytics 보고서에 대한 액세스 권한을 제공합니다.
title: A4T에서 보고를 사용하려면 어떻게 합니까?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 4abf975095c5e29eea42d67119a426a3922d8d79
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 30%

---


# A4T 보고{#a-t-reporting}

[!DNL Adobe Analytics]을(를) [!DNL Adobe Target](A4T)의 보고 소스로 사용하면 [!DNL Target] 활동에 대한 [!DNL Analytics] 보고서에 액세스할 수 있습니다.

[!DNL Analytics] 및 [!DNL Target] 모두에서 활동에 대한 보고서를 볼 수 있습니다.

[!DNL Target]에 대해 [!DNL Analytics]을(를) 사용하는 최상의 보고 방법을 보려면 이 Adobe Spark Page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/)을 방문하십시오.[

## 개요 {#section_035A62D65608423285D8A5A54731E2C5}

[!DNL Analytics] 및 [!DNL Target] 모두 사이트 방문자가 아닌 참여자(테스트에 참여한 사람)를 측정합니다.

방문자가 페이지에서 활동 컨텐츠를 볼 때마다 [!DNL Target]은(는) 방문자가 본 활동 및 경험을 포함하여 서버간 호출을 [!DNL Analytics]에 직접 만듭니다. [!DNL Target] 또한 전환이  [!DNL Analytics] 수행될 때마다 호출됩니다. [!DNL Analytics] 이 전환을 &quot;활동 전환&quot;이라는 이름의 특정 새  [!DNL Analytics] 이벤트로 추가하여 이 이벤트는 수집된 다른 데이터와 함께 추적됩니다 [!DNL Analytics].

[!UICONTROL Select] 작업이 사용되고 *참여자*&#x200B;를 정렬하면 선택한 기간 동안 참여자를 받은 경험만 보고서에 표시됩니다.

>[!NOTE]
>
>[!DNL Target]에서 제공하는 보고서에는 지연 시간이 4분입니다. A4T에서 제공하는 활동의 경우, [!DNL Target] 및 [!DNL Analytics] 보고서 모두에서 활동이 처음 저장된 후 24시간까지 걸릴 수 있으며, 보고서 데이터를 경험으로 분류할 수 있습니다. 처음 24시간 내에 수집된 데이터는 정확하며 올바른 경험에 지정됩니다.

## Analytics의 보고서 {#analytics}

[!DNL Analytics]에는 A4T 통합이 활성화된 후에 사용할 수 있는 차원 및 지표가 몇 개 있습니다.

### 차원

* [!UICONTROL Target]  분석 - 통합을 통해 전달된 상위 ID입니다. 이 차원의 형식은 `Activity ID:Experience ID:3rd ID`입니다. 아래 차원은 이 차원의 분류입니다.
* [!UICONTROL 타겟 활동]
* [!UICONTROL 타겟 경험]
* [!UICONTROL Target 활동] >  [!UICONTROL 경험]
* [!UICONTROL 3차 ID]  - 무시할 수 있음

### 지표

* [!UICONTROL 활동 노출 횟수]  - 보고서의   시작 횟수 수와  [!DNL Target] 일치합니다.
* [!UICONTROL 활동 전환]  - 보고서의  [!UICONTROL 사용자 지정 ] 전환 수와  [!DNL Target] 일치합니다.

[!DNL Analysis Workspace]에서 [!UICONTROL Target용 분석] 패널을 사용하여 [!DNL Target] 활동 및 경험을 향상도 및 신뢰도로 분석합니다. 자세한 내용은 *분석 도구 안내서*&#x200B;에서 [Target(A4T) 패널](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html)을 참조하십시오.

>[!IMPORTANT]
>
>[!DNL Analytics]의 [!UICONTROL Target 활동] 보고서에 활동이 나열되는 대신 &quot;지정되지 않음&quot;이 표시되는 경우 제공된 계정에 업데이트가 필요합니다. 이 문제를 해결하려면 고객 지원팀에 문의하십시오.

자세한 정보 및 예를 보려면 [분석 및 Target을 엽니다.Adobe Experience League에서 제공하는 분석](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) 자습서에 대한 우수 사례

## Target의 보고서 {#section_C0D1F17F88374B6690BF904D7B83B42E}

[!DNL Analytics]이(가) 보고 소스로 사용되면 [!DNL Target]의 보고서에 [!DNL Analytics]에서 수집된 데이터가 표시됩니다. 보고서는 다른 [!DNL Target] 보고서와 다소 다릅니다.

* [!UICONTROL 대상] 목록은 [!DNL Analytics] 보고서 세트에 사용할 수 있는 대상을 보여줍니다.
* [!UICONTROL 지표] 목록은 [!DNL Analytics]를 통해 사용할 수 있는 모든 지표를 보여줍니다.

   [!DNL Analytics]에 내장되어 있는 사용자 지정 지표나 계산된 지표를 포함하여 모든 지표를 사용할 수 있습니다.

   증가가 필요하지 않은 경우에도 증가되는 모든 숫자는 보고서에서 양수로 표시됩니다. 예를 들어, 낮은 바운스 비율이 필요하더라도 상승도가 가장 높은 우승자로 높은 바운스 비율이 표시됩니다. 이러한 지표 및 유사 지표에 유의하여 보고서를 기준으로 수치를 높일지 또는 줄일지 결정을 내려야 합니다.

활동이 시작된 후 또는 테스트가 완료된 후에도 [!DNL Target]의 보고서에 지표나 대상을 적용할 수 있습니다. 측정할 사항을 사전에 정확히 알 필요는 없습니다.

활동 보고서 페이지에서 직접 전체 [!DNL Analytics] 보고서를 보려면 을 클릭합니다.

## 활동 만들기 {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

활동을 만드는 중에 [!UICONTROL 설정] 페이지에서 활동의 목표를 지정해야 합니다. 이 목표는 보고서의 기본 지표가 되며 지표 선택기에서 첫 번째 옵션으로 항상 표시됩니다. 일반 Target 활동에서와 같이 보고용 세그먼트를 선택할 수는 없습니다. [!DNL Analytics]이(가) 있는 테스트에서는 [!DNL Target] 대상이 아닌 [!DNL Adobe Analytics] 세그먼트를 사용합니다.

## Target(A4T) {#section_33A97A691F3A45D497DAF57A844388F0} 분석에 대한 오프라인 계산 수행

A4T에 사용할 오프라인 계산을 수행할 수 있지만 [!DNL Analytics]의 데이터 내보내기 단계가 필요합니다. 

자세한 내용은 [Analytics for Target (A4T)에 사용할 오프라인 계산 수행](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)을 참조하십시오.
