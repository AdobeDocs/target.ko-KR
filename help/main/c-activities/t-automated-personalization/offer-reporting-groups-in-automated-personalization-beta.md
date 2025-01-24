---
keywords: 자동화된 개인화;오퍼;보고;그룹;보고 그룹;ap
description: ' [!DNL Adobe Target] [!UICONTROL Automated Personalization] 활동에서 오퍼 보고 그룹을 사용하는 방법을 알아봅니다.'
title: '[!UICONTROL Automated Personalization] 활동에서 오퍼 보고 그룹을 사용할 수 있습니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Reports
hide: true
hidefromtoc: true
source-git-commit: 19f70ce944e4db4aa0774da034a0d16be34a4ec8
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 15%

---

# [!UICONTROL Automated Personalization]의 오퍼 보고 그룹

[!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)(AP) 활동에서 보고 그룹을 사용하는 방법에 대한 정보입니다.

보고 그룹은 다음 두 가지 주요 기능을 수행합니다.

* 보고 그룹을 사용하면 AP 활동 보고로 그룹화된 오퍼를 볼 수 있습니다.
* 보고 그룹은 [!DNL Target] 개인화 모델이 작동하는 방식에 대해 중요한 역할을 합니다.

보고 그룹을 사용하는 경우 [!DNL Target]은(는) 해당 그룹에 있는 모든 오퍼의 데이터를 사용하여 각 보고 그룹에 대해 하나의 개인화 모델을 만듭니다. 보고 그룹이 없으면 [!DNL Target]에서 AP 활동의 각 오퍼에 대한 개인화 모델을 만듭니다.

활동 설정에 오퍼별로 개인화 모델을 만들 수 있는 데이터가 충분하지 않은 경우 보고 그룹을 사용하면 [!UICONTROL Automated Personalization]을(를) 사용하기 위한 데이터 요구 사항을 줄일 수 있습니다. 또한 보고 그룹은 각 모델이 더 많은 데이터를 얻을 수 있도록 유사한 오퍼를 그룹화하여 새 오퍼에 대한 &quot;cold start&quot; 문제를 해결하는 데 도움을 줄 수 있습니다. 모델링 그룹은 새 오퍼가 AP 활동에 정기적으로 도입되는 활동에도 사용할 수 있습니다.

이 방법은 방문자가 그룹의 모든 오퍼에 대해 동일한 방식으로 응답하는 경우 잘 작동합니다. 우수 사례는 비슷한 방문자 그룹이 유사한 방식으로 응답하는 오퍼를 그룹화하는 것입니다. 즉, 전환율이 유사한 오퍼를 그룹화합니다. 모든 오퍼를 단일 보고 그룹에 넣어서는 안 됩니다. 모든 오퍼를 그룹화하거나 전환율이 다른 오퍼를 그룹화하면 [!DNL Target] 개인화 모델의 효과가 떨어질 수 있습니다.

>[!NOTE]
>
>특정 모델링 그룹에서 오퍼를 제거하거나 대체한 경우 해당 특정 오퍼를 표시한 기록 트래픽도 모델링 그룹에서 삭제됩니다. 즉, 삭제된 오퍼는 [!DNL Target] 개인화 모델이 학습하는 데 사용되는 데이터에 기여하지 않습니다.

## 보고 그룹 설정

1. AP 활동의 **[!UICONTROL Experiences]** 페이지에서 **[!UICONTROL Manage Content]** 아이콘(![콘텐츠 관리 아이콘](/help/main/assets/icons/Experience.svg))을 클릭합니다
1. [!UICONTROL Manage Content] 대화 상자 상단의 **[!UICONTROL Offers]** 탭을 클릭합니다.
1. (조건부) 원하는 오퍼에 대해 [!UICONTROL More Actions] 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmall.svg))을 클릭한 다음 **[!UICONTROL Reporting Group]**&#x200B;을(를) 클릭하여 보고 그룹에 특정 경험을 추가합니다.

1. (조건부) 관련 경험에 대한 확인란을 선택한 다음 대화 상자 하단의 **[!UICONTROL Reporting Group]**&#x200B;을(를) 클릭하여 배치에 보고 그룹의 경험을 포함합니다.

1. 선택한 오퍼를 기존 보고 그룹에 할당하려면 **[!UICONTROL Existing]**&#x200B;을(를) 선택하고 드롭다운 목록에서 원하는 보고 그룹을 선택한 다음 **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

   또는

   선택한 오퍼를 할당할 보고 그룹을 만들려면 **[!UICONTROL New]**&#x200B;을(를) 선택하고 새 보고 그룹의 이름을 지정한 다음 **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

[!UICONTROL Location] 목록을 사용하여 위치별로 오퍼를 필터링할 수 있습니다. [!UICONTROL Report Group] 목록을 사용하여 보고 그룹별로 오퍼를 필터링합니다. [!UICONTROL Report Group] 목록을 사용하여 [!UICONTROL Unassigned Offers]을(를) 필터링할 수도 있으므로 현재 보고 그룹에 할당되지 않은 오퍼에 보고 그룹을 할당할 수 있습니다.

특정 대상에게 오퍼를 타기팅하는 방법에 대한 자세한 내용은 [오퍼 타기팅](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E)을 참조하십시오.[!UICONTROL Automated Personalization]

## 주의 사항

* 보고 그룹이 [!DNL Target]에서 해당 모델을 만드는 방식에 영향을 준다는 것을 이해하는 것이 중요합니다. 결과적으로 [!DNL Adobe]은(는) 활동이 활성 상태인 동안 새 오퍼를 바꾸거나 추가할 계획인 경우에만 보고 그룹을 사용할 것을 권장합니다. 새 오퍼가 라이브 활동에 도입되는 경우, 새 오퍼를 기존의 유사한 오퍼와 함께 그룹에 넣으면 시스템에서 그룹의 다른 오퍼에 대해 이미 수집된 데이터를 사용하여 새 오퍼에 대해 학습할 수 있습니다. 모든 오퍼를 단일 보고 그룹에 넣어서는 안 됩니다.

* AP 활동에는 위치+오퍼(모델)의 조합이 있습니다. [!DNL Target]이(가) 보고서에 데이터를 기록할 때 [!DNL Target]은(는) 이러한 조합을 고려하므로 오퍼가 발생한 이벤트(표시, 클릭 등)를 명확하게 합니다.

  예를 들어 활동에는 겹칠 수 있는 여러 위치와 오퍼가 있을 수 있습니다. 방문자가 서로 다른 위치에서 이러한 오퍼를 두 개 이상 보는 경우 [!DNL Target]은(는) 해당 오퍼에 대한 데이터만 기록합니다. 나중에 동일한 방문자가 오퍼를 클릭하면 [!DNL Target]이(가) 해당 조합에서만 이벤트를 기록합니다(모든 조합에 대해서는 기록되지 않음).

  마찬가지로, 클릭이 지표에 있지만 오퍼를 표시하지 않는 다른 위치에서 온 경우 이 이벤트는 활동에 기록되지만 오퍼+위치 조합에 대해서는 기록되지 않습니다. 따라서 이 오퍼는 오퍼 보고 그룹에 표시되지 않습니다.

  이 동작은 오퍼를 제공한 mbox가 아니라 다른 mbox에서 클릭이 수행될 수 있기 때문입니다. 이러한 이유로 지표는 활동과 연결되어 있지만 오퍼와는 연결되어 있지 않습니다.

## 보고 그룹에서 오퍼 보기

1. **[!UICONTROL Activities]**&#x200B;을(를) 클릭하고 목록에서 원하는 [!UICONTROL Automated Personalization] 활동을 클릭한 다음 **[!UICONTROL Reports]** 탭을 클릭하여 [오퍼 수준](/help/main/c-reports/personalization-reports/reports-ap.md) 보고서를 표시합니다.

   많은 활동이 있는 경우 [!UICONTROL Show Filters](단계) 아이콘을 클릭한 다음 [!UICONTROL Automated Personalization] 확인란을 선택하여 [!UICONTROL Automated Personalization]개의 활동만 표시하도록 목록을 필터링합니다.

1. 테이블의 **[!UICONTROL Control]** 또는 **[!UICONTROL Targeted]**&#x200B;을(를) 클릭하여 그룹화되지 않은 오퍼 및 오퍼를 보고 그룹 내에 표시합니다.

   ![오퍼 그룹: 제어 및 타깃팅](/help/main/c-reports/c-report-settings/assets/offer-groups.png)

[!UICONTROL Automated Personalization]개 보고서([!UICONTROL Offer Level] 보고서 포함) 사용에 대한 자세한 내용은 [Automated Personalization 요약 보고서](/help/main/c-reports/personalization-reports/reports-ap.md)를 참조하십시오.
