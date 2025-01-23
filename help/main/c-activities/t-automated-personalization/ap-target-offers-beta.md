---
keywords: 자동화된 개인화;오퍼;타겟;대상;타깃팅 규칙;타깃팅
description: '[!UICONTROL Automated Personalization](AP) 활동을 사용하여 특정 대상에게 개별 오퍼를 타깃팅하는 방법을 알아봅니다.'
title: '[!UICONTROL Automated Personalization]개 오퍼를 타깃팅하려면 어떻게 해야 합니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Automated Personalization
solution: Target,Analytics
hide: true
hidefromtoc: true
exl-id: 2897c4d1-116d-483c-8fc0-64857b9cbdaf
source-git-commit: 2c10ec521ceed1901ef8c3f95eb11654a7182590
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 19%

---

# [!UICONTROL Automated Personalization]개 오퍼 타깃팅

[!DNL Adobe Target] [!DNL Automated Personalization](AP) 활동에서 오퍼를 특정 대상에 타깃팅할 수 있습니다.

이 기능을 사용하면 특정 방문자가 볼 수 있는 오퍼의 수가 줄어듭니다. 예를 들어, 오퍼가 세 개인 [!UICONTROL Automated Personalization] 활동을 고려해 보십시오. 오퍼 1에는 대상 A로 노출을 제한하는 타깃팅 규칙이 있습니다. 두 방문자가 이 활동을 보았습니다.

| | 방문자 1 | 방문자 2 |
|--- |--- |--- |
| 대상 자격 조건 | 대상 A | 대상 B |
| 오퍼 1 Target 개인화 모델 점수 | 90 | 90 |
| 오퍼 2 Target 개인화 모델 점수 | 50 | 70 |
| 오퍼 3 Target 개인화 모델 점수 | 80 | 60 |

이 시나리오에서 방문자 1은 해당 방문자의 가장 높은 점수인 오퍼 1(이 방문자가 대상 A의 일부로 자격이 있으므로)을 봅니다. 그러나 방문자 2는 대상 A의 일부가 아니므로 가장 높은 점수가 오퍼 1에 대한 점수임에도 불구하고 방문자 2는 오퍼 2를 봅니다. 이 예에서는 비즈니스 요구 사항을 충족하기 위해 타깃팅 규칙을 드물게 사용해야 하는 이유를 보여 줍니다. 이러한 규칙을 추가하면 [!DNL Target] 개인화 모델의 효과를 줄일 수 있습니다.

## 타깃팅 규칙 설정

1. 타깃팅하려는 오퍼가 포함된 [Automated Personalization 활동](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)을 만들거나 편집합니다.
1. [!UICONTROL Visual Experience Composer]에서 활동에 대한 오퍼를 설정한 후 **[!UICONTROL Manage Content]** 아이콘(![콘텐츠 관리 아이콘](/help/main/assets/icons/Experience.svg))을 클릭합니다.

   [!UICONTROL Manage Content] 대화 상자가 표시됩니다.

1. **[!UICONTROL Offers]** 탭을 클릭합니다.

1. 원하는 오퍼를 선택한 다음, 해당 오퍼를 볼 수 있는 대상을 선택합니다.

   단일 오퍼에 대한 타깃팅을 설정하려면 원하는 오퍼 옆에 있는 추가 정보(![추가 정보 아이콘](/help/main/assets/icons/MoreSmallList.svg) ) 아이콘을 클릭한 다음 **[!UICONTROL Target Audience]**&#x200B;을(를) 클릭하여 [!UICONTROL Add Audiences] 대화 상자를 표시합니다.

   여러 오퍼에 대한 타깃팅을 설정하려면 원하는 오퍼에 대한 확인란을 선택한 다음 목록 맨 아래에 표시되는 **[!UICONTROL Target Audience]** 링크를 클릭합니다.

1. [!UICONTROL Add Audiences] 대화 상자에서 오퍼에 대해 원하는 대상을 선택한 다음 **[!UICONTROL Assign Audience]**&#x200B;을(를) 클릭하여 [!UICONTROL Manage Content] 대화 상자로 돌아갑니다.

   >[!NOTE]
   >
   >기존 대상을 선택할 수 있을 뿐만 아니라, 새 대상을 만들지 않고 여러 대상을 결합하여 주문형 결합 대상을 만들 수도 있습니다. 자세한 내용은 [여러 대상자 결합](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)을 참조하십시오.

1. **[!UICONTROL Done]** 아이콘을 클릭합니다.

>[!NOTE]
>
>50개의 위치 및 위치당 최대 250개의 오퍼를 설정할 수 있습니다.
