---
keywords: 권장 사항;오퍼;미리 보기;시작;상태;기준;알고리즘
description: 활동을 시작하기 전에 결과를 사용할 수 있도록 Adobe [!DNL Target] 권장 사항 활동을 미리 보는 방법에 대해 알아봅니다.
title: 권장 사항 활동을 미리 보고 시작하려면 어떻게 합니까?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
TQID: 'https://experienceleague.adobe.com/21swhpZie0QN09m0LB7VwVO-9U6GWxQ0kbthPlnns18'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 0%
---
# 권장 사항 활동 미리보기 및 시작 {#preview-launch-recs-activity}

>[!BEGINSHADEBOX]

**이 페이지에서:** 알고리즘 상태를 확인하고, 권장 사항을 미리 보고, [!DNL Recommendations] 활동을 활성화하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

활동을 시작하기 전에 권장 사항을 미리 보면 결과를 사용할 수 있음을 확인합니다. 이는 [권장 사항 오퍼](/help/main/c-recommendations/recommendations-as-an-offer.md)를 포함하는 [!UICONTROL 권장 사항], [!UICONTROL A/B 테스트] 및 [!UICONTROL 경험 타깃팅]&#x200B;(XT) 활동에 적용됩니다. [!DNL Target Recommendations]은(는) 권장 사항을 미리 보는 여러 가지 방법을 제공합니다.

## 알고리즘 상태 확인 {#check-status}

활동이 만들어지면 [!DNL Recommendations]에서 알고리즘을 실행하여 권장 사항을 생성합니다. 이 알고리즘을 실행하는 데 몇 시간이 걸릴 수 있습니다.

알고리즘의 상태가 [!DNL Recommendations] 활동의 **[!UICONTROL 개요]** 페이지에 있는 활동 다이어그램의 조건과 함께 나열됩니다.

![권장 사항 활동 개요 페이지](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview-new.png)

상태는 다음 중 하나일 수 있습니다.

* **[!UICONTROL 결과 준비]**: 알고리즘이 결과를 반환했습니다.
* **[!UICONTROL 결과가 준비되지 않음]**: 알고리즘 실행이 완료되지 않았습니다.
* **[!UICONTROL 피드 실패]**: 사용자 지정 기준 피드 파일을 검색할 수 없습니다.

![결과 대화 상자](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## 알고리즘 실행 시간 예상 {#algorithm-run-time}

기준이 포함된 활동이 저장되면 [!DNL Target]은(는) 선택한 컬렉션, 기준, 디자인 및 프로모션을 기반으로 권장 사항을 계산합니다. 필요한 시간은 권장 사항 논리, 데이터 범위, 카탈로그에 있는 항목 수, 고객이 생성한 동작 데이터의 양 및 동작 데이터 소스에 따라 다릅니다. 동작 데이터 소스가 처리 시간에 가장 큰 영향을 미칩니다.

### mbox에 대해 Target Classic 캠페인이 실행되고 있지 않은지 확인합니다

mbox가 동작 데이터 소스인 경우 기준은 기준이 만들어진 직후에 실행됩니다. 동작 데이터의 양과 카탈로그 크기에 따라 알고리즘을 실행하는 데 최대 12시간이 걸릴 수 있습니다.

기준 구성을 변경하면 일반적으로 알고리즘이 다시 실행됩니다. 변경 내용에 따라 재실행이 완료될 때까지 이전에 계산된 권장 사항을 사용하지 못할 수 있습니다. 더 큰 변경의 경우 재실행이 완료될 때까지 백업이나 기본 콘텐츠만 사용할 수 있습니다.

수정되지 않은 알고리즘은 선택한 데이터 범위에 따라 12~48시간마다 [!DNL Target]에 의해 자동으로 다시 실행됩니다.

### [!DNL Adobe Analytics]

[!DNL Adobe Analytics]이(가) 동작 데이터 소스인 경우 기준을 사용할 수 있을 때까지의 시간은 선택한 보고서 세트 및 전환 창이 다른 기준에 이미 사용되었는지 여부에 따라 달라집니다. 보고서 세트가 지정된 전환 확인 기간과 함께 처음 사용되는 경우 [!DNL Target Recommendations]은(는) [!DNL Analytics]에서 동작 데이터를 다운로드하는 데 2~7일이 걸릴 수 있습니다.

새 기준이나 편집된 기준 및 지속적인 알고리즘 실행 시기에 대해서는 [데이터 Source](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#data-source)에서 Analytics가 데이터 소스일 때 **기준 가용성** 드롭다운을 참조하십시오.

>[!NOTE]
>
>**[!UICONTROL 최근에 본 항목]**&#x200B;은(는) 오프라인 알고리즘을 실행할 필요가 없으며 결과를 즉시 사용할 수 있습니다. mbox 데이터를 기반으로 하는 **[!UICONTROL 가장 많이 본 항목]** 및 **[!UICONTROL 최상위 판매자]** 알고리즘은 일반적으로 계산이 더 단순하기 때문에 매우 빠르게 결과를 생성합니다. 이러한 알고리즘은 동작 데이터가 올바르게 수집되고 있는지 확인하거나 디자인 변경을 미리 볼 수 있는 좋은 옵션입니다.

## QA 링크로 미리 보기 {#preview-qa-link}

알고리즘의 결과가 준비되면 [!DNL Adobe Target]의 [QA 링크](/help/main/c-activities/c-activity-qa/activity-qa.md) 기능을 사용하여 결과를 미리 볼 수 있습니다. QA 링크는 **[!UICONTROL 활동]** 개요 페이지의 **[!UICONTROL 활동 위치]** 섹션에서 사용할 수 있으며 페이지에 권장 사항을 표시합니다.

![주요 제품](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>기본적으로 [!DNL Target]은(는) QA 링크에 필요한 대상에 사용자를 자동으로 추가합니다. 이 설정이 꺼져 있고 활동에 타깃팅 규칙이 있는 경우 사용자 프로필이 해당 타깃팅 규칙을 충족해야 권장 사항이 포함된 경험을 볼 수 있습니다.

QA 모드에는 다음과 같은 동작이 있습니다.

* [!DNL Target] QA 모드가 쿠키에 저장되고 페이지 전체에서 유지됩니다. QA 모드가 종료되지 않으면 사이트 전체에 QA 결과가 계속 표시됩니다. QA 모드를 종료하려면 [북마클릿](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md)을 사용하십시오.
* QA 모드에서는 사이트 탐색이 프로필의 **[!UICONTROL 최근에 본 항목]** 또는 **[!UICONTROL 최근에 구매한 항목]**&#x200B;에 영향을 주지 않습니다. 이 동작은 의도하지 않은 생산 행동 데이터 오염을 피하기 위해 설계에 의한 것입니다. **[!UICONTROL 최근에 본 항목]** 또는 **[!UICONTROL 사용자 기반 권장 사항]** 기준의 결과를 미리 보려면 먼저 QA 모드 외부에서 사이트를 찾은 다음 동일한 세션을 사용하여 QA 모드 링크를 엽니다.

## CSV 다운로드로 미리 보기 {#preview-csv}

결과를 다운로드하면 특정 권장 항목을 감사할 수 있습니다. 이는 권장 항목이 현재 방문자가 보고 있는 항목에 따라 달라지고 카탈로그에 수천 또는 수백만 개의 다른 항목이 포함될 수 있는 **[!UICONTROL 이 항목을 본 사람, 특정 항목을 본 사람]**&#x200B;과 같은 알고리즘에 특히 유용합니다.

1. 활동에서 하나 이상의 알고리즘에 대해 **[!UICONTROL 결과 준비]** 상태가 표시될 때까지 기다리십시오. 그 전에는 결과를 다운로드할 수 없습니다.

1. **[!UICONTROL 활동]** 개요 페이지에서 오른쪽 상단의 메뉴 아이콘을 클릭한 다음 **[!UICONTROL 데이터 다운로드]**&#x200B;를 클릭합니다.

   ![데이터 다운로드 옵션](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

1. 다운로드한 CSV 파일을 열어 권장 항목을 확인합니다.

   ![권장 항목 CSV 파일](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

이 파일에는 가장 자주 보는 항목인 왼쪽에서 오른쪽으로 권장 항목이 나열됩니다. 권장 사항은 환경으로 구분됩니다. 이 예에서는 프로덕션 환경에만 권장 사항이 있습니다.

별표(*)로 시작하는 행에는 [백업 항목](/help/main/c-recommendations/c-algorithms/backup-recs.md)이 나열됩니다. 알고리즘의 권장 항목(기준)이 디자인의 모든 슬롯을 채울 수 없는 경우 백업 항목이 표시됩니다.

키 값을 기반으로 하는 알고리즘(예: **[!UICONTROL 이 항목을 본 사람, 특정 항목을 본 사람]**)의 경우 키 값(&quot;이&quot; 항목)은 맨 왼쪽 열에 있습니다. 권장 항목(&quot;해당&quot; 항목)은 Recommendation_X 열에 왼쪽에서 오른쪽으로 나열됩니다.

결과 집합이 매우 큰 활동의 경우 **[!UICONTROL 데이터 다운로드]** 옵션이 실패하고 오류 `Error while fetching recommendation data file.`이(가) 발생할 수 있습니다. 이 문제는 생성된 CSV가 사용자 인터페이스가 단일 다운로드로 반환할 수 있는 응답 크기를 초과할 때 발생합니다.

>[!NOTE]
>
>**[!UICONTROL 사용자 기반 권장 사항]** 알고리즘이 포함된 활동 또는 **[!UICONTROL 최근에 본 항목]** 권장 사항 논리를 사용하는 기준에는 결과를 다운로드할 수 없습니다.

### 인기도 기반 및 키 기반 알고리즘을 위한 CSV 다운로드 형식 {#format}

CSV 다운로드 파일은 백엔드 기준 실행 후 생성된 결과를 일관되게 반영합니다.

* **인기도 기반 알고리즘(키가 아닌 알고리즘)**: 파일에 다음이 포함됩니다.

  * 앞에 별표(*)가 붙은 백업 권장 사항 행
  * 알고리즘 설정을 기반으로 한 권장 사항을 나열하는 별도의 행

* **키 기반 알고리즘**: 파일에는 다음이 포함되어 있습니다.

  * 인기도 기반 알고리즘의 경우 백업 행
  * 키-값 형식의 여러 행. 여기서 첫 번째 항목은 키의 제품 ID이고 그 뒤에는 추천 후보를 나타내는 쉼표로 구분된 제품 ID가 옵니다.

## 활동 활성화 {#activate-activity}

활동을 활성화하면 활동이 시작되고 상태가 **[!UICONTROL Live]**(으)로 변경됩니다.

**[!UICONTROL 활동 개요]** 탭에서 **[!UICONTROL 상태]** 드롭다운 화살표를 클릭한 다음 **[!UICONTROL 활성화]**&#x200B;를 선택합니다. 활동이 현재 **[!UICONTROL 비활성]** 상태인 경우 드롭다운 목록에 **[!UICONTROL 비활성]** 레이블이 지정됩니다. 몇 초에서 몇 분 후에 상태가 **[!UICONTROL Live]**(으)로 전환됩니다.

동일한 드롭다운 목록을 사용하여 활동을 비활성화하거나 보관할 수도 있습니다.

## 설정 변경 시 중단 방지 {#avoid-disruptions}

라이브 활동에서 [!DNL Recommendations]개의 컬렉션, 기준, 프로모션 또는 디자인 설정을 변경하면 알고리즘 결과가 무효화되고 알고리즘 상태가 **[!UICONTROL 결과가 준비되지 않음]**(으)로 변경될 수 있습니다.

라이브 활동이 중단되지 않도록 하려면 활동의 사본을 수정한 다음 원본을 바꾸는 것이 좋습니다.

1. 원래 활동(활동 1)과 수정할 기준을 복제하여 새 활동(활동 2)을 만듭니다.
1. 복제된 활동(활동 2) 및 해당 기준을 변경한 다음, 알고리즘이 결과를 생성할 때까지 기다립니다.
1. 수정된 활동(활동 2)을 미리 보고 결과가 원하는 대로 표시되는지 확인합니다.
1. 새 활동을 활성화합니다(활동 2).
1. 원래 활동(활동 1)을 비활성화합니다.

기록 보고 결과를 동일한 활동에서 유지해야 하는 경우 다른 접근 방식이 가능합니다. 이 접근 방식은 권장 사항 가용성에 일시적인 중단을 초래할 수 있습니다.

1. 원래 활동(활동 1)과 수정할 기준을 복제하여 새 활동(활동 2)을 만듭니다.
1. 복제된 활동(활동 2) 및 해당 기준을 변경한 다음, 알고리즘이 결과를 생성할 때까지 기다립니다.
1. 수정된 활동(활동 2)을 미리 보고 결과가 원하는 대로 표시되는지 확인합니다.
1. 수정된 활동을 일시 중지하고(활동 2), 설정 및 기준을 원래 활동(활동 1)으로 전환합니다.
1. 원래 활동(활동 1)을 미리 보고 결과가 원하는 대로 표시되는지 확인합니다.
1. 원래 활동을 다시 활성화합니다(활동 1).
