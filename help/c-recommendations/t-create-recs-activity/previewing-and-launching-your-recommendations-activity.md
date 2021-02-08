---
keywords: Recommendations;오퍼;미리 보기;시작;상태;기준;알고리즘
description: '활동을 시작하기 전에 결과를 사용할 수 있도록 Adobe Target Recommendations 활동을 미리 보는 방법을 알아봅니다. '
title: Recommendations 활동을 미리 보고 시작하려면 어떻게 합니까?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 17%

---


# Recommendations 활동 미리 보기 및 실행

[!UICONTROL Recommendations], [!UICONTROL A/B 테스트] 또는 [!UICONTROL Recommendations 오퍼](/help/c-recommendations/recommendations-as-an-offer.md)를 포함하는 경험 타깃팅](XT) 활동을 만든 후 활동을 시작하기 전에 결과를 사용할 수 있도록 권장 사항을 미리 볼 수 있습니다. [ [!DNL Target Recommendations] 권장 사항을 미리 보는 여러 가지 방법을 제공합니다.

## Recommendations 알고리즘 상태 확인

활동을 만든 후 [!DNL Recommendations]은(는) 권장 사항을 생성하는 알고리즘을 실행합니다. 이 알고리즘을 실행하는 데 몇 시간이 걸릴 수 있습니다.

기준 상태가 나열되는 [!UICONTROL 활동] 개요 다이어그램에서 알고리즘이 실행을 완료했는지 여부를 확인할 수 있습니다. 다음 그림은 [!DNL Recommendations] 활동의 [!UICONTROL 개요] 페이지의 활동 다이어그램의 상태를 보여줍니다.

![Recommendations 활동 개요 페이지](/help/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

다음 그림은 [!UICONTROL A/B 테스트] 또는 XT 활동의 [!UICONTROL 개요] 페이지의 상태를 보여 줍니다.

![A/B 테스트 개요 페이지](/help/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

상태 결과는 아래와 같이 다음과 같습니다.

* [!UICONTROL 준비 결과]:알고리즘에서 결과를 반환했음을 나타냅니다.
* [!UICONTROL 결과가 준비되지 않음]:알고리즘 실행이 완료되지 않았음을 나타냅니다.
* [!UICONTROL 피드 오류]:사용자 지정 기준 피드 파일을 검색할 수 없음을 나타냅니다.

![결과 대화 상자](/help/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## 알고리즘을 실행하는 데 얼마나 걸립니까?

기준을 포함하는 활동을 저장한 후 [!DNL Target]은 선택한 수집, 기준, 디자인 및 프로모션을 기준으로 권장 사항을 계산합니다. 이 계산은 수행하는 데 어느 정도의 시간이 걸리고, 선택한 권장 사항 논리, 데이터 범위, 카탈로그에 있는 항목 수, 고객이 생성한 행동 데이터 양 및 선택한 행동 데이터 소스에 따라 시간 프레임이 다릅니다.

동작 데이터 소스는 다음과 같이 처리 시간에 가장 큰 영향을 줍니다.

### mbox에 대해 Target Classic 캠페인이 실행되고 있지 않은지 확인합니다

mbox를 동작 데이터 소스로 선택한 경우, 기준이 만들어지면 즉시 실행됩니다. 사용되는 동작 데이터의 분량과 카탈로그 크기에 따라 알고리즘을 실행하는 데 최대 12시간이 걸릴 수 있습니다. 일반적으로 기준 구성을 변경하면 알고리즘이 재실행됩니다. 수행된 변경 내용에 따라, 재실행이 완료될 때까지 이전에 계산된 권장 사항을 사용할 수 없거나, 큰 변경 사항의 경우 재실행이 완료될 때까지 백업 또는 기본 컨텐츠만 사용할 수 있습니다. 알고리즘이 수정되지 않으면 [!DNL Target]이 선택한 데이터 범위에 따라 12~48시간 간격으로 자동 재실행됩니다.

### Adobe Analytics

기준이 [!DNL Adobe Analytics]을 동작 데이터 소스로 사용하는 경우 기준 가용성의 시간은 선택한 보고서 세트 및 전환 창이 다른 모든 기준에 사용되었는지 여부에 따라 달라집니다.

* **1회성 보고서 세트 설정**: 보고서 세트가 지정된 데이터 범위 전환 확인 기간과 함께 처음 사용되는 경우, [!DNL Target Recommendations]은 2~7일 동안 [!DNL Analytics]에서 선택한 보고서 세트에 대한 동작 데이터를 완전히 다운로드할 수 있습니다. 이 기간은 [!DNL Analytics] 시스템 로드에 따라 다릅니다.
* **이미 사용 가능한 보고서 세트를 사용하여 새 기준 또는 편집한 기준**:새 기준을 만들거나 기존 기준을 편집할 때, 선택한 보고서 세트가 이미 선택한 데이터 범위와 같거나 그보다 작은 데이터 범위 [!DNL Target Recommendations]와 함께 사용된 경우, 데이터를 즉시 사용할 수 있으며 일회성 설정이 필요하지 않습니다. 이러한 경우, 또는 선택한 보고서 세트나 데이터 범위를 수정하지 않고 알고리즘 설정이 편집된 경우 알고리즘이 12시간 이내에 실행되거나 재실행됩니다.
* **지속적인 알고리즘 실행**: 데이터는 매일 [!DNL Analytics]에서 [!DNL Target Recommendations]으로 이동합니다. 예를 들어 [!UICONTROL 관심도 보기] 추천의 경우, 사용자가 제품을 볼 때 제품-보기 추적 호출이 실시간에 가깝게 [!DNL Analytics]에 전달됩니다. [!DNL Analytics] 데이터는 다음 날 일찍 [!DNL Target]로 푸시되고 [!DNL Target]는 12시간 이내에 알고리즘을 실행합니다.

>[!NOTE]
>
>[!UICONTROL 최근에 본 항목] 은 오프라인 알고리즘을 실행하지 않아도 되며 결과를 즉시 사용할 수 있습니다. [!UICONTROL mbox ] 데이터를 기반으로 하는  [!UICONTROL 상위 보기 및 ] 상위선택기 알고리즘은 일반적으로 단순한 계산 필요 때문에 매우 빠르게 결과를 생성합니다. 이러한 옵션은 디자인 변경 사항을 미리 보거나 행동 데이터가 올바르게 수집되고 있는지 확인할 때 좋은 옵션이 될 수 있습니다.

## QA 링크를 사용하여 Recommendations 미리 보기

알고리즘에 결과가 준비되면 [!DNL Adobe Target]의 [QA 링크](/help/c-activities/c-activity-qa/activity-qa.md) 기능을 사용하여 결과를 미리 볼 수 있습니다. QA 링크는 활동 개요 페이지의 [!UICONTROL 활동 QA] 섹션에서 사용할 수 있습니다.

![활동 QA 링크](/help/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>기본적으로 [!DNL Target]은(는) QA 링크에 필요한 대상에 사용자를 자동으로 추가합니다. 이 설정이 해제되어 있고 활동에 타깃팅 규칙이 있는 경우 사용자 프로필은 권장 사항이 포함된 경험을 보려면 해당 타깃팅 규칙을 충족해야 합니다.

QA 링크를 사용하면 페이지에서 권장 사항을 미리 볼 수 있습니다.

![주요 제품](/help/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* Target QA 모드는 &quot;고정&quot;이며 쿠키에 저장됩니다. QA 모드를 종료하지 않으면 사이트 전체에서 QA 결과가 계속 표시됩니다. QA 모드를 종료하려면 [북마클릿](/help/c-activities/c-activity-qa/activity-qa-bookmark.md)을 사용합니다.
   >
   >
* QA 모드에 있는 동안 사이트를 검색해도 프로필의 [!UICONTROL 최근에 본 항목] 또는 [!UICONTROL 최근 구매한 항목]&quot;에 영향을 주지 않습니다. 이러한 행위는 생산 행동 데이터의 의도하지 않은 오염을 방지하기 위해 디자인에 의해 발생합니다. [!UICONTROL 최근에 본 항목] 또는 [!UICONTROL 사용자 기반 Recommendations] 기준의 결과를 미리 보려면 먼저 QA 모드 외부에서 사이트를 찾은 다음 동일한 세션을 사용하여 QA 모드 링크를 엽니다.


## CSV 다운로드를 사용하여 권장 사항 미리 보기

경우에 따라 권장되는 특정 항목을 감사할 수 있습니다. 이 기능은 특히 사용자가 현재 보고 있는 항목에 따라 다른 항목 세트를 추천하는 [!UICONTROL 이(가) 본 사람]과 같은 알고리즘을 사용할 때 도움이 되며, 카탈로그에 수천 또는 수백만 개의 다른 항목이 있을 수 있습니다.

활동의 하나 이상의 알고리즘에 대해 [!UICONTROL 결과 준비] 상태가 표시될 때까지 결과를 다운로드할 수 없습니다.

미리 보기용 결과를 다운로드하려면 활동 개요 페이지의 오른쪽 상단에 있는 메뉴 아이콘을 클릭한 다음 **[!UICONTROL 데이터 다운로드]**&#x200B;를 클릭합니다.

![데이터 다운로드 옵션](/help/c-recommendations/t-create-recs-activity/assets/download-data.png)

CSV 파일을 다운로드합니다. 권장 항목을 보려면 엽니다.

![권장 항목 CSV 파일](/help/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

왼쪽에서 오른쪽에는 권장 항목 목록이 있습니다. 이 경우 가장 자주 보는 항목 목록입니다. 권장 사항은 환경으로 구분됩니다. 이 경우 프로덕션 환경에만 권장 사항이 있습니다. 이 알고리즘의 경우, 키 값을 기준으로 제한을 적용하지 않았으므로 별표(*)가 표시된 행에 전체 권장 사항 세트가 포함됩니다. [!UICONTROL 본 사람, 본 사람 등 키 값을 기반으로 하는 다른 알고리즘 유형의 경우, 키 값(즉, &quot;이&quot; 항목)이 맨 왼쪽 열에 나열되고 권장 항목(즉, &quot;해당&quot; 항목)이 Recommendation_X 열에 왼쪽에서 오른쪽으로 나열됩니다.]

>[!NOTE]
>
>결과 다운로드는 [!UICONTROL 사용자 기반 Recommendations] 알고리즘을 포함하는 활동에는 사용할 수 없습니다. 결과 다운로드는 [!UICONTROL 최근에 본 항목] 권장 사항 논리를 사용하여 기준에 사용할 수 없습니다.

## Recommendations 활동 활성화

[!UICONTROL 활동 개요] 탭에서 상태 옆에 있는 드롭다운 화살표를 클릭한 다음 **[!UICONTROL 활성화]**&#x200B;를 선택합니다.

![활성화 옵션](/help/c-recommendations/t-create-recs-activity/assets/activate.png)

상태는 [!UICONTROL Activating]이 됩니다.

![활성화](/help/c-recommendations/t-create-recs-activity/assets/activating.png)

몇 초~몇 분 후 상태는 [!UICONTROL Live]로 전환됩니다.

![라이브](/help/c-recommendations/t-create-recs-activity/assets/live.png)

동일한 드롭다운 목록을 사용하여 활동을 비활성화하거나 보관할 수도 있습니다.

## Recommendations 설정을 변경할 때 중단 방지

라이브 활동에서 [!DNL Recommendations] 컬렉션, 기준, 프로모션 또는 디자인 설정을 변경하면 알고리즘 결과가 잘못되고 알고리즘의 상태가 [!UICONTROL 준비가 안 됨]으로 변경될 수 있습니다.

라이브 활동을 중단하지 않으려면 라이브 활동을 수정할 때 다음 방법을 사용하는 것이 좋습니다.

1. 수정할 활동 및 기준을 복제합니다.
1. 복제된 활동 및 기준을 변경하고 알고리즘이 결과를 생성할 때까지 기다립니다.
1. 수정된 새 활동을 미리 보고 원하는 대로 결과가 나타나는지 확인합니다.
1. 새 활동을 활성화합니다.
1. 이전 활동을 비활성화합니다.

동일한 활동에서 내역 보고 결과를 유지해야 하는 경우 대체 방법을 사용할 수 있으며, 이렇게 하면 추천 가용성에 대한 일시적인 중단을 초래할 수 있습니다.

1. 수정할 활동 및 기준을 복제합니다.
1. 복제된 활동 및 기준을 변경하고 알고리즘이 결과를 생성할 때까지 기다립니다.
1. 수정된 새 활동을 미리 보고 원하는 대로 결과가 나타나는지 확인합니다.
1. 기존 활동을 일시 중지하고 설정/기준을 새 기준으로 바꿉니다.
1. 기존 활동을 미리 보고 결과가 원하는 대로 표시되는지 확인합니다.
1. 활동을 다시 활성화합니다.
