---
keywords: 자동화된 개인화;오퍼;보고;그룹;보고 그룹;ap
description: Adobe에서 오퍼 보고 그룹을 사용하는 방법 알아보기 [!DNL Target] [!UICONTROL Automated Personalization] 활동.
title: Automated Personalization 활동에서 오퍼 보고 그룹을 사용할 수 있습니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 29%

---

# [!UICONTROL Automated Personalization의 오퍼 보고 그룹]

에서 보고 그룹 사용에 대한 정보 [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) 활동.

보고 그룹은 다음 두 가지 주요 기능을 수행합니다.

* 보고 그룹을 사용하면 AP 활동 보고로 그룹화된 오퍼를 볼 수 있습니다.
* 보고 그룹은 다음 방법에 대해 중요한 역할을 합니다. [!DNL Target] 개인화 모델 기능.

보고 그룹을 사용할 때 [!DNL Target] 는 해당 그룹에 있는 모든 오퍼의 데이터를 사용하여 각 보고 그룹에 대해 하나의 개인화 모델을 만듭니다. 보고 그룹이 없으면 [!DNL Target] 는 AP 활동의 각 오퍼에 대한 개인화 모델을 만듭니다.

활동 설정에 오퍼별로 개인화 모델을 작성할 충분한 데이터가 없는 경우 보고 그룹을 통해 사용할 데이터 요구 사항을 줄일 수 있습니다 [!UICONTROL Automated Personalization]. 또한 보고 그룹은 각 모델이 더 많은 데이터를 얻을 수 있도록 유사한 오퍼를 그룹화하여 새 오퍼에 대한 &quot;cold start&quot; 문제를 해결하는 데 도움을 줄 수 있습니다. 모델링 그룹은 새 오퍼가 AP 활동에 정기적으로 도입되는 활동에도 사용할 수 있습니다.

이 방법은 방문자가 그룹의 모든 오퍼에 대해 동일한 방식으로 응답하는 경우 잘 작동합니다. 우수 사례는 비슷한 방문자 그룹이 유사한 방식으로 응답하는 오퍼를 그룹화하는 것입니다. 즉, 전환율이 유사한 오퍼를 그룹화합니다. 모든 오퍼를 단일 보고 그룹에 넣어서는 안 됩니다. 모든 오퍼를 그룹화하거나 전환율이 다른 오퍼를 그룹화하면 의 효과가 떨어질 수 있습니다. [!DNL Target] 개인화 모델.

>[!NOTE]
>
>특정 모델링 그룹에서 오퍼를 제거하거나 대체한 경우 해당 특정 오퍼를 표시한 기록 트래픽도 모델링 그룹에서 삭제됩니다. 즉, 삭제된 오퍼는 의 어떤 데이터가 사용되는지에 기여하지 않습니다. [!DNL Target] 학습할 개인화 모델.

## 보고 그룹 설정

1. 다음에서 **[!UICONTROL 경험]** AP 활동의 페이지에서 **[!UICONTROL 콘텐츠 관리]** 아이콘.

   ![콘텐츠 관리 아이콘](/help/main/c-reports/assets/ap_manage_content.png)

1. **[!UICONTROL 컨텐츠 관리]** 대화 상자 맨 위에 있는 [!UICONTROL 오퍼] 탭을 클릭합니다.
1. (조건부) 원하는 오퍼 위로 마우스를 이동한 다음 **[!UICONTROL 보고 그룹]** 폴더 아이콘을 클릭하여 보고 그룹에 특정 경험을 추가합니다.

   ![보고 그룹 아이콘](/help/main/c-reports/assets/ap_manage_content_2.png)

1. (조건부) 관련 경험에 대한 확인란을 선택한 다음 을 클릭하여 배치에 보고 그룹의 경험을 포함합니다. **[!UICONTROL 보고 그룹]** 대화 상자의 오른쪽 상단 모서리에 있는 폴더 아이콘

   ![보고 그룹 아이콘](/help/main/c-reports/assets/ap_manage_content_3.png)

1. 선택한 오퍼를 기존 보고 그룹에 지정하려면 **[!UICONTROL 기존]**&#x200B;을 선택하고 드롭다운 목록에서 원하는 보고 그룹을 선택한 다음 **[!UICONTROL 적용]**&#x200B;을 클릭합니다.

   또는

   선택한 오퍼를 지정할 보고 그룹을 생성하려면 다음을 선택합니다. **[!UICONTROL 신규]**&#x200B;를 클릭하고 새 보고 그룹의 이름을 지정한 다음 **[!UICONTROL 적용]**.

   ![새 보고 그룹을 만드는 새 아이콘](/help/main/c-reports/assets/ap_reporting_groups.png)

다음을 사용할 수 있습니다. [!UICONTROL 위치] 위치별로 오퍼를 필터링할 목록입니다. [!UICONTROL 보고서 그룹] 목록을 사용하여 보고 그룹별로 오퍼를 필터링합니다. 또한 [!UICONTROL 보고 그룹] 목록을 사용하여 [!UICONTROL 지정되지 않은 오퍼]를 필터링하면 현재 보고 그룹에 지정되지 않은 오퍼에 보고 그룹을 지정할 수 있습니다.

특정 대상에게 오퍼를 타깃팅하는 방법에 대한 내용은 [AP 오퍼 Target](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

## 주의 사항

* 보고 그룹이 다음에 미치는 영향을 이해하는 것이 중요합니다 [!DNL Target] 는 모델을 빌드합니다. 그 결과, [!DNL Adobe] 은 활동이 라이브 상태인 동안 새 오퍼를 바꾸거나 추가할 계획인 경우에만 보고 그룹을 사용할 것을 권장합니다. 새 오퍼가 라이브 활동에 도입되는 경우, 새 오퍼를 기존의 유사한 오퍼와 함께 그룹에 넣으면 시스템에서 그룹의 다른 오퍼에 대해 이미 수집된 데이터를 사용하여 새 오퍼에 대해 학습할 수 있습니다. 모든 오퍼를 단일 보고 그룹에 넣어서는 안 됩니다.

* AP 활동에는 위치+오퍼(모델)의 조합이 있습니다. 날짜 [!DNL Target] 보고서에 데이터를 기록합니다. [!DNL Target] 은 오퍼가 발생한 이벤트(표시, 클릭 등)를 명확하게 알 수 있도록 이러한 조합을 고려합니다.

   예를 들어 활동에는 겹칠 수 있는 여러 위치와 오퍼가 있을 수 있습니다. 방문자가 서로 다른 위치에서 이러한 오퍼를 두 개 이상 보는 경우 [!DNL Target] 는 해당 오퍼에 대해서만 데이터를 기록합니다. 동일한 방문자가 나중에 오퍼를 클릭하면 [!DNL Target] 해당 조합에서만 이벤트를 기록합니다(모든 조합에 대해서는 기록되지 않음).

   마찬가지로, 클릭이 지표에 있지만 오퍼를 표시하지 않는 다른 위치에서 온 경우 이 이벤트는 활동에 기록되지만 오퍼+위치 조합에 대해서는 기록되지 않습니다. 따라서 이 오퍼는 오퍼 보고 그룹에 표시되지 않습니다.

   이 동작은 오퍼를 제공한 mbox가 아니라 다른 mbox에서 클릭할 수 있다는 사실 때문입니다. 이러한 이유로 지표는 활동과 연결되어 있지만 오퍼와는 연결되어 있지 않습니다.

## 보고 그룹에서 오퍼 보기

1. 클릭 **[!UICONTROL 활동]**&#x200B;을 클릭하고 원하는 을 클릭합니다 [!UICONTROL Automated Personalization] 목록에서 활동을 클릭한 다음 **[!UICONTROL 보고서]** 탭을 사용하여 다음을 표시합니다. [오퍼 수준](/help/main/c-reports/personalization-reports/reports-ap.md) 보고서.

   많은 활동이 있는 경우 [!UICONTROL 유형] 드롭다운 목록에서 [!UICONTROL 자동화된 개인화]를 선택하여 목록을 필터링할 수 있습니다.

1. 클릭 **[!UICONTROL 제어]** 또는 **[!UICONTROL 타깃팅됨]** 보고 그룹 내에 그룹화되지 않은 오퍼 및 오퍼를 표시하는 표입니다.

   ![오퍼 그룹: 제어 및 타깃팅](/help/main/c-reports/c-report-settings/assets/offer-groups.png)

사용에 대한 정보 [!UICONTROL Automated Personalization] 보고서(다음을 포함) [!UICONTROL 오퍼 수준] report), 참조 [Automated Personalization 요약 보고서](/help/main/c-reports/personalization-reports/reports-ap.md).


