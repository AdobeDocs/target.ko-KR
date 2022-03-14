---
keywords: analytics for target;a4t;보고 소스로 분석;analytics
description: Analytics 사용 방법 알아보기 [!DNL Target] (A4T). A4T에서는 다음에 대한 Analytics 보고서에 액세스할 수 있습니다 [!DNL Target] analytics 지표 및 대상 세그먼트를 사용하는 활동.
title: A4T에서 보고를 사용하려면 어떻게 해야 합니까?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 29%

---

# A4T 보고

사용 [!DNL Adobe Analytics] 를 [!DNL Adobe Target] (A4T)에서 다음에 액세스할 수 있습니다 [!DNL Analytics] 보고서 [!DNL Target] 활동.

두 위치에서 활동에 대한 보고서를 볼 수 있습니다 [!DNL Analytics] 및 [!DNL Target].

를 사용하는 보고 우수 사례 [!DNL Analytics] 대상 [!DNL Target], [이 Adobe Spark Page 방문](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## 개요 {#section_035A62D65608423285D8A5A54731E2C5}

둘 다 [!DNL Analytics] 및 [!DNL Target] 보고서는 사이트 방문자가 아닌 참여자(테스트를 시작하는 사람)를 측정합니다.

방문자가 페이지에서 활동 컨텐츠를 볼 때마다, [!DNL Target] 에 직접 서버 간 호출을 수행 [!DNL Analytics]에는 방문자가 본 활동 및 경험이 포함됩니다. [!DNL Target] 또한 호출 [!DNL Analytics] 전환이 이루어지는 시점마다. [!DNL Analytics] 전환을 특정 새로운 항목으로 추가 [!DNL Analytics] 이벤트는에서 수집한 다른 데이터와 함께 추적되는 &quot;활동 변환&quot;이라고 합니다. [!DNL Analytics].

이 [!UICONTROL 선택] 작업을 사용하고 *참여자*&#x200B;를 채울 경우 선택한 기간 동안 참여자를 수신한 경험만 보고서에 표시됩니다.

>[!NOTE]
>
>지원 보고서 [!DNL Target] 지연 시간은 4분입니다. A4T에서 제공하는 활동의 경우, [!DNL Target] 및 [!DNL Analytics] 보고서, 활동을 처음 저장한 후 보고서 데이터를 경험별로 분류하려면 최대 24시간이 걸릴 수 있습니다. 처음 24시간 내에 수집된 데이터는 정확하며 올바른 경험에 지정됩니다.

## Analytics의 보고서 {#analytics}

in [!DNL Analytics]A4T 통합이 활성화되면 사용 가능한 몇 가지 차원과 지표가 있습니다.

### 차원

* [!UICONTROL Target 분석] - 통합을 통해 전달되는 상위 ID입니다. 이 차원의 형식은 다음과 같습니다 `Activity ID:Experience ID:3rd ID`. 아래 차원은 이 차원의 분류입니다.
* [!UICONTROL 타겟 활동]
* [!UICONTROL 타겟 경험]
* [!UICONTROL Target 활동] > [!UICONTROL 경험]
* [!UICONTROL 세 번째 ID] - 무시할 수 있음

### 지표

* [!UICONTROL 활동 노출 횟수] - 와 일치 [!UICONTROL 참여자] 의 숫자 [!DNL Target] 보고서 세트에 대해 설명합니다.
* [!UICONTROL 활동 전환] - 와 일치 [!UICONTROL 사용자 지정 전환] 의 숫자 [!DNL Target] 보고서 세트에 대해 설명합니다.

in [!DNL Analysis Workspace]를 사용하려면 [!UICONTROL Target 분석] 패널 분석 [!DNL Target] 향상도와 신뢰도를 갖는 활동 및 경험. 자세한 내용은 [A4T(Target 분석) 패널](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=ko-KR) 에서 *Analytics 툴 안내서*.

>[!IMPORTANT]
>
>만약 [!UICONTROL Target 활동] 보고서 위치 [!DNL Analytics] 활동을 나열하는 대신 &quot;지정되지 않음&quot;을 나열합니다. 제공된 계정에 업데이트가 필요합니다. 이 문제를 해결하려면 고객 지원팀에 문의하십시오.

자세한 내용 및 예를 보려면 [Analytics 및 Target: 분석 우수 사례](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) 자습서, Adobe Experience League에서 제공합니다.

## 의 보고서 [!DNL Target] {#section_C0D1F17F88374B6690BF904D7B83B42E}

When [!DNL Analytics] 이 보고 소스로 사용되면 [!DNL Target] 에서 수집한 데이터 표시 [!DNL Analytics]. 그 보고서는 다소 다르다 [!DNL Target] 보고서:

* 다음 [!UICONTROL 대상] 목록에는 사용 가능한 대상이 표시됩니다 [!DNL Analytics] 보고서 세트.
* 다음 [!UICONTROL 지표] 목록에는 [!DNL Analytics].

   내장된 사용자 지정 지표 또는 계산된 지표를 포함하여 모든 지표를 사용할 수 있습니다 [!DNL Analytics].

   증가를 원치 않는 경우에도 증가하는 모든 숫자가 보고서에서 양수로 표시됩니다. 예를 들어, 낮은 바운스 비율이 필요하더라도 상승도가 가장 높은 우승자로 높은 바운스 비율이 표시됩니다. 이러한 지표 및 유사 지표에 유의하여 보고서를 기준으로 수치를 높일지 또는 줄일지 결정을 내려야 합니다.

의 보고서에 지표나 대상을 적용할 수 있습니다 [!DNL Target] 활동이 시작된 후 또는 테스트가 완료된 후에도 활동을 시작할 수 있습니다. 측정할 사항을 사전에 정확히 알 필요는 없습니다.

전체 항목을 보려면 를 클릭합니다. [!DNL Analytics] 활동 보고서 페이지에서 직접 보고합니다.

## 활동 만들기 {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

활동을 만드는 중에 [!UICONTROL 설정] 페이지에서 활동의 목표를 지정해야 합니다. 이 목표는 보고서의 기본 지표가 되며 지표 선택기에서 첫 번째 옵션으로 항상 표시됩니다. 일반 Target 활동에서와 같이 보고용 세그먼트를 선택할 수는 없습니다. 테스트 대상 [!DNL Analytics] 사용 [!DNL Adobe Analytics] 세그먼트 대신 [!DNL Target] 대상.

## Analytics for Adobe Target (A4T)에 사용할 오프라인 계산 수행 {#section_33A97A691F3A45D497DAF57A844388F0}

A4T에 사용할 오프라인 계산을 수행할 수 있지만 [!DNL Analytics]의 데이터 내보내기 단계가 필요합니다. 

자세한 내용은 [Analytics for Target (A4T)에 사용할 오프라인 계산 수행](/help/main/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)을 참조하십시오.
