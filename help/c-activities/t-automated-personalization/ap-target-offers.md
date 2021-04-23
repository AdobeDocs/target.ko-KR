---
keywords: 자동화된 개인화;오퍼;대상;대상;타깃팅 규칙;타깃팅
description: Adobe Target에서 AP(Automated Personalization) 활동을 사용하여 특정 대상자에게 개별 오퍼를 타깃팅하는 방법을 알아봅니다.
title: 'Automated Personalization 오퍼을 어떻게 사용할 수 있습니까? [!DNL Target] '
feature: 자동화된 개인화
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 87%

---

# ![](/help/assets/premium.png) [!DNL Target] Premium자동화된 개인화 제공

[!DNL Adobe Target] [!DNL Automated Personalization] (AP) 활동에서 특정 대상에 오퍼를 타깃팅할 수 있습니다.

이 기능을 사용하면 특정 방문자가 볼 수 있는 오퍼의 수가 줄어듭니다. 예를 들면 3개의 오퍼가 있는 AP 활동을 고려합니다. 오퍼 1에는 대상 A로 노출을 제한하는 타깃팅 규칙이 있습니다. 두 방문자가 이 AP 활동을 확인했습니다.

|  | 방문자 1 | 방문자 2 |
|--- |--- |--- |
| 대상 자격 | 대상 A | 대상 B |
| 오퍼 1 Target 개인화 모델 점수 | 90 | 90 |
| 오퍼 2 Target 개인화 모델 점수 | 50 | 70 |
| 오퍼 3 Target 개인화 모델 점수 | 80 | 60 |

이 시나리오에서 방문자 1에게는 해당 방문자의 최고 점수 점수인 오퍼 1이 표시됩니다(방문자 1이 대상 A의 일부로 자격을 얻으므로). 그러나 방문자 2는 대상 A의 일부가 아니므로 최고 점수가 오퍼 1에 대한 것이더라도 오퍼 2가 표시됩니다. 이 예제에서는 비즈니스 요구에 맞게 타깃팅 규칙을 사용해야 하는 이유를 보여 줍니다. 이러한 규칙을 추가하면 Target 개인화 모델의 효율성이 줄어들 수 있습니다.

## 타깃팅 규칙 설정

1. 타깃팅하려는 오퍼가 포함된 [자동화된 개인화 활동](/help/c-activities/t-automated-personalization/create-ap-activity.md)을 만듭니다.
1. 시각적 경험 작성기에서 활동에 대한 오퍼를 설정한 후에 **[!UICONTROL 콘텐츠 관리]**&#x200B;를 클릭합니다.

   ![콘텐츠 관리](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   콘텐츠 관리 대화 상자가 열립니다.

1. 오퍼 탭을 클릭합니다.

   ![오퍼 페이지](/help/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. 원하는 오퍼를 선택하고 해당 오퍼를 볼 수 있는 대상을 선택합니다.

   단일 오퍼에 대한 타깃팅을 설정하려면 원하는 오퍼 위를 마우스로 가리킨 다음 **[!UICONTROL 타깃팅]** 아이콘을 클릭합니다.

   여러 오퍼에 대한 타깃팅을 설정하려면 원하는 오퍼에 대한 확인란을 선택한 다음 목록의 오른쪽 상단에 표시되는 **[!UICONTROL 타깃팅] 아이콘을 클릭합니다.

1. 다음 [!UICONTROL 대상자 선택] 대화 상자에서 오퍼에 대해 원하는 대상자를 선택한 다음 **[!UICONTROL 완료]**&#x200B;를 클릭하여 [!UICONTROL 콘텐츠 관리] 대화 상자로 돌아갑니다.

   >[!NOTE]
   >
   >기존 대상을 선택할 수 있을 뿐만 아니라, 새 대상을 만들지 않고 여러 대상을 결합하여 임시로 결합한 대상을 만들 수도 있습니다. 자세한 내용은 [여러 대상 결합](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)을 참조하십시오.

1. **[!UICONTROL 완료를 클릭합니다]**.

>[!NOTE]
>
>50개의 위치 및 위치당 최대 250개의 오퍼를 설정할 수 있습니다.
