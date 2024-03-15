---
keywords: Recommendations;오퍼;미리 보기;시작;상태;기준;알고리즘
description: Adobe 미리보기 방법 알아보기 [!DNL Target] Recommendations 활동을 시작하여 활동을 시작하기 전에 결과를 사용할 수 있도록 합니다.
title: Recommendations 활동을 미리 보고 시작하려면 어떻게 합니까?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
source-git-commit: 0d875bfaf8c0670f657046469d2adba0647de4fb
workflow-type: tm+mt
source-wordcount: '1416'
ht-degree: 15%

---

# 권장 사항 활동 미리보기 및 시작

을(를) 만든 후 [!UICONTROL Recommendations], [!UICONTROL A/B Test], 또는 [!UICONTROL Experience Targeting] (XT) 활동 포함 [Recommendations 오퍼](/help/main/c-recommendations/recommendations-as-an-offer.md), 활동을 시작하기 전에 결과를 사용할 수 있도록 권장 사항을 미리 볼 수 있습니다. [!DNL Target Recommendations] 은 권장 사항을 미리 보는 여러 가지 방법을 제공합니다.

## Recommendations 알고리즘 상태 확인

활동을 만든 후 [!DNL Recommendations] 은 권장 사항을 생성하는 알고리즘을 실행합니다. 이 알고리즘을 실행하는 데 몇 시간이 걸릴 수 있습니다.

다음 위치에서 알고리즘 실행이 완료되었는지 확인할 수 있습니다. [!UICONTROL Activity] 개요 다이어그램. 여기서 기준 상태가 나열됩니다. 다음 그림은 의 활동 다이어그램에서 상태를 보여 줍니다. [!DNL Recommendations] 활동 [!UICONTROL Overview] 페이지:

![Recommendations 활동 개요 페이지](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

다음 그림은 의 상태를 보여 줍니다. [!UICONTROL A/B Test] 또는 XT 활동 [!UICONTROL Overview] 페이지:

![A/B 테스트 개요 페이지](/help/main/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

상태 결과에는 아래 그림과 같이 다음과 같은 항목이 포함됩니다.

* [!UICONTROL Results Ready]: 알고리즘이 결과를 반환했음을 나타냅니다
* [!UICONTROL Results Not Ready]: 알고리즘 실행이 완료되지 않았음을 나타냅니다.
* [!UICONTROL Feed Failure]: 사용자 지정 기준 피드 파일을 검색할 수 없음을 나타냅니다.

![결과 대화 상자](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## 알고리즘이 실행되는 데 얼마나 걸립니까?

기준이 포함된 활동을 저장한 후, [!DNL Target] 선택한 컬렉션, 기준, 디자인 및 프로모션을 기반으로 권장 사항을 계산합니다. 이 계산은 수행하는 데 시간이 걸리고 기간은 선택한 권장 사항 논리, 데이터 범위, 카탈로그에 있는 항목 수, 고객이 생성한 동작 데이터의 양 및 선택한 동작 데이터 소스에 따라 다릅니다.

동작 데이터 소스는 다음과 같이 처리 시간에 가장 큰 영향을 줍니다.

### mbox에 대해 Target Classic 캠페인이 실행되고 있지 않은지 확인합니다

mbox를 동작 데이터 소스로 선택한 경우, 기준이 만들어지면 즉시 실행됩니다. 사용되는 동작 데이터의 분량과 카탈로그 크기에 따라 알고리즘을 실행하는 데 최대 12시간이 걸릴 수 있습니다. 일반적으로 기준 구성을 변경하면 알고리즘이 재실행됩니다. 수행된 변경 사항에 따라 재실행이 완료될 때까지 이전에 계산된 권장 사항을 사용할 수 없거나, 더 큰 변경의 경우 재실행이 완료될 때까지 백업이나 기본 콘텐츠만 사용할 수 있습니다. 알고리즘이 수정되지 않으면 [!DNL Target]이 선택한 데이터 범위에 따라 12~48시간 간격으로 자동 재실행됩니다.

### Adobe Analytics

기준이 [!DNL Adobe Analytics]을 동작 데이터 소스로 사용하는 경우 기준 가용성의 시간은 선택한 보고서 세트 및 전환 창이 다른 모든 기준에 사용되었는지 여부에 따라 달라집니다.

* **1회성 보고서 세트 설정**: 보고서 세트가 지정된 데이터 범위 전환 확인 기간과 함께 처음 사용되는 경우, [!DNL Target Recommendations]은 2~7일 동안 [!DNL Analytics]에서 선택한 보고서 세트에 대한 동작 데이터를 완전히 다운로드할 수 있습니다. 이 기간은 [!DNL Analytics] 시스템 로드에 따라 다릅니다.
* **이미 사용 가능한 보고서 세트를 사용하는 새 기준 또는 편집된 기준**: 선택한 보고서 세트를 이미 와 함께 사용한 경우 새 기준을 만들거나 기존 기준을 편집할 때 [!DNL Target Recommendations], 데이터 범위가 선택한 데이터 범위와 같거나 그보다 적은 경우 데이터를 즉시 사용할 수 있으며 일회성 설정이 필요하지 않습니다. 이러한 경우, 또는 선택한 보고서 세트나 데이터 범위를 수정하지 않고 알고리즘 설정이 편집된 경우 알고리즘이 12시간 이내에 실행되거나 재실행됩니다.
* **지속적인 알고리즘 실행**: 데이터는 매일 [!DNL Analytics]에서 [!DNL Target Recommendations]으로 이동합니다. 예: [!UICONTROL Viewed Affinity] 권장 사항: 사용자가 제품을 볼 때 제품-보기 추적 호출이에 전달됩니다. [!DNL Analytics] 실시간에 가깝습니다. 다음 [!DNL Analytics] 데이터가 푸시됨 [!DNL Target] 다음 날 일찍 [!DNL Target] 는 12시간 이내에 알고리즘을 실행합니다.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] 오프라인 알고리즘을 실행할 필요가 없으며 결과를 즉시 사용할 수 있습니다. [!UICONTROL Top Viewed] 및 [!UICONTROL Top Sellers] mbox 데이터를 기반으로 하는 알고리즘은 일반적으로 필요한 계산이 단순하기 때문에 매우 빠르게 결과를 생성합니다. 이러한 기능은 디자인 변경을 미리 보거나 동작 데이터가 올바르게 수집되고 있는지 확인하려는 경우에 유용합니다.

## QA 링크를 사용하여 Recommendations 미리 보기

알고리즘이 결과를 준비한 후에는 다음을 사용하여 해당 결과를 미리 볼 수 있습니다. [QA 링크](/help/main/c-activities/c-activity-qa/activity-qa.md) 기능 [!DNL Adobe Target]. QA 링크는 [!UICONTROL Activity QA] 활동 개요 페이지의 섹션:

![활동 QA 링크](/help/main/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>기본적으로, [!DNL Target] 는 사용자를 QA 링크의 필수 대상자에 자동으로 추가합니다. 이 설정이 꺼져 있고 활동에 타깃팅 규칙이 있는 경우 사용자 프로필이 해당 타깃팅 규칙을 충족해야 권장 사항이 포함된 경험을 볼 수 있습니다.

QA 링크를 사용하면 페이지에서 권장 사항을 미리 볼 수 있습니다.

![추천 제품](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* Target QA 모드가 &quot;고정&quot;이며 쿠키에 저장됩니다. QA 모드를 종료하지 않으면 사이트 전체에서 QA 결과가 계속 표시됩니다. QA 모드를 종료하려면 [북마클릿](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md).
>
>* QA 모드에서는 사이트 탐색이 프로필의 [!UICONTROL Recently Viewed Items] 또는 [!UICONTROL Recently Purchased Items]. 이 동작은 의도하지 않은 생산 행동 데이터의 오염을 피하기 위해 설계에 의해 발생합니다. 의 결과를 미리 보려면 다음과 같이 하십시오. [!UICONTROL Recently Viewed Items] 또는 [!UICONTROL User-Based Recommendations] 기준은 먼저 QA 모드 외부에서 사이트를 탐색한 다음 동일한 세션을 사용하여 QA 모드 링크를 엽니다.

## CSV 다운로드를 사용하여 권장 사항 미리보기

경우에 따라 권장되는 특정 항목을 감사할 수 있습니다. 이는 다음과 같은 알고리즘을 사용할 때 특히 유용합니다. [!UICONTROL People Who Viewed This, Viewed That]: 사용자가 현재 보고 있는 항목에 따라 다른 항목 세트가 권장되며 카탈로그에 수천 또는 수백만 개의 다른 항목이 있을 수 있습니다.

다음 시간까지 결과를 다운로드할 수 없음: [!UICONTROL Results Ready] 활동의 하나 이상의 알고리즘에 대해 상태가 표시됩니다.

미리 볼 결과를 다운로드하려면 활동 개요 페이지의 오른쪽 상단에 있는 메뉴 아이콘을 클릭한 다음 를 클릭합니다 **[!UICONTROL Download data]**.

![데이터 다운로드 옵션](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

CSV 파일을 다운로드하고 있습니다. 이 폴더를 열어 추천 항목을 확인합니다.

![권장 항목 CSV 파일](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

왼쪽에서 오른쪽으로 권장 항목 목록(이 경우 가장 자주 보는 항목)이 있습니다. 권장 사항은 환경으로 구분됩니다. 이 경우 프로덕션 환경에만 권장 사항이 있습니다.

별표(*)가 행의 첫 번째 값인 경우 백업 항목을 나타냅니다. 알고리즘의 권장 항목(기준)으로 디자인의 모든 슬롯을 채울 수 없는 경우 백업 항목이 표시됩니다. 최상위 판매와 같은 인기 알고리즘의 경우 이러한 알고리즘 유형에는 &quot;키&quot;가 없으므로 CSV 파일의 각 환경에 대해 0개 또는 1개의 백업되지 않은 행만 있을 수 있습니다(예: &quot;고객이 보거나 구매할 수 있는 것에 관계없이 가장 인기 있는 제품을 고객에게 표시&quot;). 따라서 다른 키 기반 알고리즘(예: view-view)과 달리, 행의 첫 번째 값은 키가 아니라 권장 항목 목록의 첫 번째 항목입니다.

키 값을 기반으로 하는 기타 알고리즘 유형의 경우, 예: [!UICONTROL People Who Viewed This, Viewed That], 키 값(즉, &quot;This&quot; 항목)은 맨 왼쪽 열에 나열되고 권장 항목(즉, &quot;That&quot; 항목)은 Recommendation_X 열에 왼쪽에서 오른쪽으로 나열됩니다.

>[!NOTE]
>
>다음 항목이 포함된 활동에는 결과 다운로드를 사용할 수 없습니다. [!UICONTROL User-Based Recommendations] 알고리즘. 다음을 사용하는 기준에 대해서는 결과 다운로드를 사용할 수 없습니다. [!UICONTROL Recently-Viewed Items] 권장 사항 논리.

## Recommendations 활동 활성화

다음에서 [!UICONTROL Activity Overview] 탭을 클릭하고 상태 옆에 있는 드롭다운 화살표를 클릭한 다음 을 선택합니다. **[!UICONTROL Activate]**.

![활성화 옵션](/help/main/c-recommendations/t-create-recs-activity/assets/activate.png)

상태는 다음과 같이 변경됩니다 [!UICONTROL Activating]:

![활성화 중](/help/main/c-recommendations/t-create-recs-activity/assets/activating.png)

몇 초에서 몇 분 정도 지나면 상태가 로 전환됩니다. [!UICONTROL Live]:

![라이브](/help/main/c-recommendations/t-create-recs-activity/assets/live.png)

동일한 드롭다운 목록을 사용하여 활동을 비활성화하거나 보관할 수도 있습니다.

## Recommendations 설정 변경 시 중단 방지

변경 중 [!DNL Recommendations] 라이브 활동의 컬렉션, 기준, 프로모션 또는 디자인 설정으로 인해 알고리즘 결과가 잘못되고 알고리즘 상태가 로 변경될 수 있습니다. [!UICONTROL Results Not Ready].

라이브 활동이 중단되지 않도록 하려면 라이브 활동을 수정할 때 다음 접근 방식을 취하는 것이 좋습니다.

1. 원래 활동(활동 1)과 수정할 기준을 복제하여 새 활동(활동 2)을 만듭니다.
1. 복제된 활동(활동 2) 및 기준을 변경하고 알고리즘이 결과를 생성할 때까지 기다립니다.
1. 새롭고 수정된 활동(활동 2)을 미리 보고 원하는 대로 결과가 표시되는지 확인합니다.
1. 새 활동을 활성화합니다(활동 2).
1. 원래 활동(활동 1)을 비활성화합니다.

동일한 활동에서 내역 보고 결과를 유지해야 하는 경우 대체 접근 방식이 가능하며, 이로 인해 권장 사항 가용성이 일시적으로 중단될 수 있습니다.

1. 원래 활동(활동 1)과 수정할 기준을 복제하여 새 활동(활동 2)을 만듭니다.
1. 복제된 활동(활동 2) 및 기준을 변경하고 알고리즘이 결과를 생성할 때까지 기다립니다.
1. 새롭고 수정된 활동(활동 2)을 미리 보고 원하는 대로 결과가 표시되는지 확인합니다.
1. 새롭고 수정된 활동(활동 2)을 일시 중지하고 설정/기준을 원래 활동(활동 1)으로 전환합니다.
1. 원래 활동(활동 1)을 미리 보고 원하는 대로 결과가 표시되는지 확인합니다.
1. 원래 활동을 다시 활성화합니다(활동 1).
