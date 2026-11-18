---
keywords: 자동화된 개인화;오퍼;보고;그룹;보고 그룹;ap
description: '[!DNL Adobe Target] [!UICONTROL Automated Personalization] 활동에서 오퍼 보고 그룹을 사용하는 방법에 대해 알아봅니다.'
title: '[!UICONTROL Automated Personalization] 활동에서 오퍼 보고 그룹을 사용할 수 있습니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
TQID: 'https://experienceleague.adobe.com/VW3zVGXb3IuQMDaRyidbkjsbUrojvwFsvwP3yRVeHp4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: e8a43148-398f-56c7-9433-6564f96999c2
    internal-label: Reports
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 3%
---
# [!UICONTROL Automated Personalization]의 오퍼 보고 그룹 {#offer-reporting-groups}

>[!BEGINSHADEBOX]

**이 페이지에서:** 오퍼 보고 그룹이 **[!UICONTROL Automated Personalization]** 활동에서 작동하는 방식, 설정하는 방법 및 보고서에서 보는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

보고 그룹을 사용하면 [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)(AP) 활동의 오퍼를 그룹으로 구성할 수 있습니다. 보고 그룹은 다음 두 가지 주요 기능을 수행합니다.

* AP 활동 보고에 그룹화된 오퍼를 볼 수 있도록 합니다.
* 이 ID는 [!DNL Target] 개인화 모델이 작동하는 방식에 중요한 역할을 합니다.

보고 그룹을 사용하는 경우 [!DNL Target]은(는) 각 보고 그룹에 대해 해당 그룹의 모든 오퍼의 데이터를 사용하여 하나의 개인화 모델을 만듭니다. 보고 그룹이 없으면 [!DNL Target]에서 AP 활동의 각 오퍼에 대한 개인화 모델을 만듭니다.

또한 활동 설정에 오퍼별 개인화 모델을 만들 수 있는 데이터가 충분하지 않은 경우 보고 그룹은 **[!UICONTROL Automated Personalization]**&#x200B;을(를) 사용하기 위한 데이터 요구 사항을 줄입니다. 이러한 콜드 스타트는 각 모델이 교육할 더 많은 데이터를 갖도록 유사한 오퍼와 함께 그룹화되는 새 오퍼의 &quot;콜드 스타트&quot; 문제를 해결하는 데 도움이 됩니다.

이 접근 방식은 방문자가 그룹의 모든 오퍼에 동일한 방식으로 응답하므로 전환율이 유사한 오퍼를 그룹화할 때 잘 작동합니다. 모든 오퍼를 단일 보고 그룹에 넣지 말고, 전환율이 다른 오퍼를 그룹화하지 마십시오. 두 옵션 모두 [!DNL Target] 개인화 모델의 효과를 낮출 수 있기 때문입니다.

>[!NOTE]
>
>보고 그룹에서 오퍼를 제거하거나 대체한 경우 해당 오퍼를 표시한 기록 트래픽도 그룹에서 삭제되므로 삭제된 오퍼는 [!DNL Target] 개인화 모델이 학습하는 데 사용하는 데이터에 기여하지 않습니다.


## 고려 사항

### 라이브 활동에 보고 그룹 사용

보고 그룹은 [!DNL Target]이(가) 모델을 만드는 방식에 영향을 줍니다. 결과적으로 [!DNL Adobe]은(는) 활동이 라이브 상태일 때 오퍼를 바꾸거나 추가할 계획인 경우에만 보고 그룹을 사용할 것을 권장합니다. 새 오퍼가 라이브 활동에 도입된 경우, 새 오퍼를 기존의 유사한 오퍼가 있는 그룹에 넣으면 [!DNL Target]은(는) 그룹의 다른 오퍼에 대해 이미 수집된 데이터를 사용하여 새 오퍼에 대해 알아볼 수 있습니다.

### 오퍼 및 위치에 대한 데이터를 기록하는 방법

AP 활동에는 위치와 오퍼의 조합(모델)이 있습니다. [!DNL Target]이(가) 보고서에 데이터를 기록할 때 이러한 조합을 고려하므로 오퍼가 발생한 이벤트(표시, 클릭 등)가 명확합니다.

예를 들어 활동에는 겹칠 수 있는 여러 위치와 오퍼가 있을 수 있습니다. 방문자가 서로 다른 위치에서 이러한 오퍼를 두 개 이상 보는 경우 [!DNL Target]은(는) 해당 오퍼에 대한 데이터만 기록합니다. 나중에 동일한 방문자가 오퍼를 클릭하면 [!DNL Target]이(가) 해당 조합에서만 이벤트를 기록합니다(모든 조합에 대해서는 기록되지 않음).

마찬가지로, 클릭이 지표에 있지만 오퍼를 표시하지 않는 다른 위치에서 온 경우 이벤트가 활동에 기록되지만 오퍼와 위치의 조합에 대해서는 기록되지 않습니다. 따라서 이 오퍼는 오퍼 보고 그룹에 표시되지 않습니다. 이 동작은 오퍼를 제공한 mbox가 아닌 다른 mbox에서 클릭할 수 있기 때문에 발생합니다. 이 경우 지표는 활동과 연결되어 있지만 오퍼와는 연결되어 있지 않습니다.

## 보고 그룹 설정

보고 그룹에 오퍼를 할당하면 [!DNL Target]이(가) 개인화 모델을 만드는 방법과 오퍼가 활동 보고서에 표시되는 방법이 결정됩니다. 활동을 빌드하는 동안 또는 나중에 라이브 활동에 새 오퍼를 추가하는 경우 그룹을 설정합니다.

1. AP 활동의 **[!UICONTROL 경험]** 페이지에서 **[!UICONTROL 콘텐츠 관리]** 아이콘(![콘텐츠 관리 아이콘](/help/main/assets/icons/Experience.svg))을 클릭합니다.

1. **[!UICONTROL 컨텐츠 관리]** 대화 상자 맨 위에 있는 **[!UICONTROL 오퍼]** 탭을 클릭합니다.

   ![구성 아이콘](../assets/ap-offers-2.png)

1. (조건부) 보고 그룹에 추가할 오퍼를 선택합니다.

   * 단일 오퍼를 추가하려면 오퍼에 대한 **[!UICONTROL 추가 작업]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmall.svg))을 클릭한 다음 **[!UICONTROL 보고 그룹]**&#x200B;을 클릭합니다.
   * 여러 개의 오퍼를 한 번에 추가하려면 오퍼에 대한 확인란을 선택한 다음 대화 상자 하단의 **[!UICONTROL 보고 그룹]**&#x200B;을 클릭합니다.

1. 선택한 오퍼를 보고 그룹에 할당합니다.

   * 기존 보고 그룹에 오퍼를 할당하려면 **[!UICONTROL 기존]**&#x200B;을 선택하고 드롭다운 목록에서 보고 그룹을 선택한 다음 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.
   * 오퍼에 대한 보고 그룹을 만들려면 **[!UICONTROL 새로 만들기]**&#x200B;를 선택하고 새 보고 그룹의 이름을 지정한 다음 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

오퍼 목록의 범위를 좁히려면 **[!UICONTROL 위치]** 목록을 사용하여 위치별로 필터링하거나 **[!UICONTROL 보고서 그룹]** 목록을 사용하여 보고 그룹별로 필터링하십시오. **[!UICONTROL 보고서 그룹]** 목록에는 아직 보고 그룹에 속하지 않은 오퍼를 표시하여 사용자에게 할당할 수 있도록 **[!UICONTROL 미할당 오퍼]** 옵션도 제공됩니다.

특정 대상에게 오퍼를 타깃팅하는 방법에 대한 자세한 내용은 [Target **[!UICONTROL Automated Personalization]** 오퍼](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#set-up-targeting-rules)를 참조하십시오.

## 보고 그룹에서 오퍼 보기

**[!UICONTROL 오퍼 수준]** 보고서는 개별 오퍼와 그룹을 비교할 수 있도록 활동의 오퍼가 보고 그룹별로 그룹화되어 수행되는 방식을 보여 줍니다.

1. **[!UICONTROL 활동]**&#x200B;을 클릭하고 목록에서 **[!UICONTROL Automated Personalization]** 활동을 클릭한 다음 **[!UICONTROL 보고서]** 탭을 클릭하여 [오퍼 수준](/help/main/c-reports/personalization-reports/reports-ap.md) 보고서를 표시합니다.

   활동이 많은 경우 **[!UICONTROL 필터 표시]**(funnel) 아이콘을 클릭한 다음 **[!UICONTROL Automated Personalization]** 확인란을 선택하여 **[!UICONTROL Automated Personalization]** 활동만 표시합니다.

1. 테이블에서 **[!UICONTROL 제어]** 또는 **[!UICONTROL 타깃팅]**&#x200B;을 클릭하여 그룹화되지 않은 오퍼와 보고 그룹 내의 오퍼를 표시합니다.

   ![오퍼 그룹: 제어 및 타깃팅](/help/main/c-reports/assets/offer-groups.png)

**[!UICONTROL Automated Personalization]** 보고서(**[!UICONTROL 오퍼 수준]** 보고서 포함) 사용에 대한 자세한 내용은 [Automated Personalization 요약 보고서](/help/main/c-reports/personalization-reports/reports-ap.md)를 참조하십시오.
