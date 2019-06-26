---
description: Analytics를 Target(A4T)의 보고 소스로 사용하면 Target 활동에 대한 Analytics 보고서에 액세스할 수 있습니다.
keywords: analytics for target;a4t;보고 소스로 분석
seo-description: Analytics를 Target(A4T)의 보고 소스로 사용하면 Target 활동에 대한 Analytics 보고서에 액세스할 수 있습니다.
seo-title: A4T 보고
solution: Target
subtopic: 다변량 테스트
title: A4T 보고
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# A4T 보고{#a-t-reporting}

Analytics를 Target(A4T)의 보고 소스로 사용하면 Target 활동에 대한 Analytics 보고서에 액세스할 수 있습니다.

Analytics와 Target Standard/Premium 둘 다에서 활동의 보고서를 볼 수 있습니다.

Analytics for Target을 사용하는 보고 우수 사례를 확인하려면 [Adobe Spark 페이지](https://spark.adobe.com/page/Lo3Spm4oBOvwF/)를 방문하십시오.

## 개요 {#section_035A62D65608423285D8A5A54731E2C5}

Analytics 및 Target 보고서는 사이트의 방문자 수가 아닌 참여자 수(테스트에 참여한 사람)를 측정합니다.

방문자가 페이지에서 활동 컨텐츠를 볼 때마다 Target은 방문자가 본 활동 및 경험을 포함하여 서버 간 호출을 Analytics로 유도합니다. 또한 Target은 전환이 발생할 때마다 Analytics를 호출합니다. Analytics는 이 전환을 &quot;활동 전환&quot;이라는 이름의 새로운 특정 Analytics 이벤트로 추가하며 이 전환은 Analytics에서 수집한 기타 데이터와 함께 추적됩니다.

선택 작업을 사용하여 *참여자*를 정렬하면 선택된 기간 중에 참여자를 수신한 경험만 보고서에 표시됩니다.

>[!NOTE]
>
>Target에서 제공하는 보고서에는 지연 시간 4분이 적용됩니다. A4T에서 Target 보고서와 Analytics 보고서에 제공하는 활동의 경우, 활동이 처음에 저장된 후 24시간이 지나야 보고서 데이터를 경험별로 분류할 수 있습니다. 처음 24시간 내에 수집된 데이터는 정확하며 올바른 경험에 지정됩니다.

## Analytics의 보고서 {#section_F6884872DC864AE7913587FAED4CD11C}

Analytics의 왼쪽 메뉴에서 **[!UICONTROL Target]** &gt; **[!UICONTROL Target 활동]** 을 클릭합니다. Target에서 활동의 보고서에 Analytics 데이터, 지표, 세그먼트가 자동으로 표시됩니다. 데이터는 사이트에서 수집된 후 약 1시간 후에 이러한 보고서에 표시됩니다. 보고서에 있는 모든 지표, 대상, 값은 활동을 설정할 때 선택한 보고서 세트에서 가져옵니다.

Analytics에서 Target 활동의 결과를 살펴보려면 Target 활동 보고서를 사용하십시오. 이 보고서에는 이전 Test&amp;Target 플러그인 스타일 페이지 통합에 관한 정보가 포함되며 Analytics for Target 데이터는 포함되지 않습니다. Activities 보고서에서 Target 경험에 대한 정보를 봅니다. **[!UICONTROL 지표]** 를 클릭하고 **Target[!UICONTROL 지표 유형을 선택합니다.]** 보고서에서 두 개의 지표를 사용할 수 있습니다.

* **활동 시작:** Target 보고서에서 참여자 수와 일치합니다.
* **활동 전환:** Target 보고서에서 사용자 지정 전환 수와 일치합니다.

>[!NOTE]
>
>Target 향상도 및 신뢰도 세부 정보도 Analytics에서 사용할 수 있습니다. 자세한 내용은 Adobe Analytics 제품 설명서에서 [Target 상승도 및 신뢰도 보고서 유형](https://marketing.adobe.com/resources/help/en_US/reference/report_target_lift_confidence.html)을 참조하십시오.

>[!IMPORTANT]
>
>Analytics에서 Target 활동 보고서에 활동이 나열되지 않고 &quot;지정되지 않음&quot;이 나열되면 제공된 계정을 업데이트해야 합니다. 이 문제를 해결하려면 고객 지원팀에 문의하십시오.

## Target의 보고서 {#section_C0D1F17F88374B6690BF904D7B83B42E}

Analytics를 보고 소스로 사용하면 Target Standard의 보고서는 Analytics에서 생성된 데이터를 보여줍니다. 이 보고서는 기타 Target Standard 보고서와 약간 다릅니다.

* 대상 목록은 Analytics 보고서 세트에 사용할 수 있는 대상을 보여줍니다.
* 지표 목록은 Analytics를 통해 사용할 수 있는 모든 지표를 보여줍니다.

   Analytics에 기본 제공되는 모든 사용자 지정 또는 계산된 지표를 비롯한 모든 지표를 사용할 수 있습니다.

   수치 증가가 실제로 불필요하더라도 증가되는 모든 숫자는 보고서에서 양수로 표시됩니다. 예를 들어, 낮은 바운스 비율이 필요하더라도 상승도가 가장 높은 우승자로 높은 바운스 비율이 표시됩니다. 이러한 지표 및 유사 지표에 유의하여 보고서를 기준으로 수치를 높일지 또는 줄일지 결정을 내려야 합니다.

테스트를 시작한 후에 또는 테스트가 완료된 후에도 Target의 보고서에 해당 지표 또는 대상을 적용할 수 있습니다. 측정할 사항을 사전에 정확히 알 필요는 없습니다.

활동 보고서 페이지에서 직접 전체 Analytics 보고서를 보려면 클릭하십시오.

## Analysis Workspace의 보고서 {#reports-in-analysis-workspace}

[!DNL Adobe Analysis Workspace]를 사용하여 데이터를 보다 깊이 있게 분석하고 그 이면에 대한 통찰력을 얻을 수 있습니다.

For detailed information and examples, open the [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), provided by Adobe Experience League.

## 활동 만들기 {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

활동을 만드는 중에 [!UICONTROL 설정] 페이지에서 활동의 목표를 지정해야 합니다. 이 목표는 보고서의 기본 지표가 되며 지표 선택기에서 첫 번째 옵션으로 항상 표시됩니다. 일반 Target 활동에서와 같이 보고용 세그먼트를 선택할 수는 없습니다. Analytics를 통한 테스트에서는 Target Standard 대상이 아닌 Adobe Analytics 세그먼트를 사용합니다.

## Analytics for Target (A4T)에 사용할 오프라인 계산 수행{#section_33A97A691F3A45D497DAF57A844388F0}

A4T에 사용할 오프라인 계산을 수행할 수 있지만 [!DNL Analytics]의 데이터 내보내기 단계가 필요합니다. 

자세한 내용은 [Analytics for Target (A4T)에 사용할 오프라인 계산 수행](../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)을 참조하십시오.
