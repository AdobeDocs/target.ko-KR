---
keywords: 대상자;대상자 규칙;대상자 만들기;대상자 생성;활동 전용;활동전용;임시
description: Adobe [!DNL Target] 에서 일회용으로 활동 전용 대상을 만드는 방법을 알아봅니다.
title: 한 번만 사용할 대상을 만들 수 있습니까?
feature: Audiences
exl-id: 5fe0507a-75d1-47bc-a941-8c8eeeaf3b75
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 28%

---

# 활동 전용 대상자 만들기

활동을 만드는 동안 안내가 있는 [!DNL Adobe Target] 3단계 워크플로우에서 활동 전용 대상을 만듭니다. 이러한 애드혹 대상은 동일한 활동 내의 다른 위치에서 사용될 수 있지만 다른 활동에서 사용할 수 있도록 [!UICONTROL Audiences Library]에 저장되지는 않습니다.

활동 전용 대상자는 다음과 같은 이점을 제공합니다.

* 활동 전용 대상을 사용하여 한 번만 사용하려고 하며 [!UICONTROL Audiences Library]에 저장하지 않으려는 대상을 만들 수 있습니다. 활동 전용 대상은 다시 사용하지 않으려는 대상으로 [!UICONTROL Audiences Library]이(가) 복잡해지지 않도록 하는 데 도움이 됩니다.
* 활동 전용 대상이 [!UICONTROL Audiences Library]에 표시되지 않습니다. 이러한 대상은 라이브러리에 표시되지 않으므로 조직의 다른 사용자가 원치 않는 변경을 하지 않도록 방지됩니다.

1. [활동](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)을 만드는 동안 **[!UICONTROL Targeting]** 페이지에서 세 개의 세로 줄임표를 클릭한 다음 **[!UICONTROL Replace Audience]**&#x200B;을(를) 클릭합니다.

   ![단계 결과](assets/edit_audience.png)

1. **[!UICONTROL Create Audience]** 아이콘을 클릭합니다.

1. **[!UICONTROL This activity only]** 아이콘을 클릭합니다.

   ![활동 전용 aud 이미지](assets/activity-only-aud.png)

1. 특성을 설명하는 대상자 이름을 입력합니다.
1. 원하는 속성을 대상 빌더로 드래그하여 놓습니다.

   규칙을 사용하면 대상을 사이트 방문자의 하위 집합으로 제한할 수 있습니다. 각 규칙 유형에는 고유한 매개 변수가 있습니다. 각 대상 규칙 유형을 구성하는 방법에 대한 자세한 내용은 [대상 범주](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D)를 참조하십시오.

1. **[!UICONTROL Done]** 아이콘을 클릭합니다.

## 고려 사항

활동 전용 대상을 사용할 때는 다음 정보에 유의하십시오.

* [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 또는 [!UICONTROL Form-Based Experience Composer]에서 활동 전용 대상을 만들 수 있습니다. 이 기능은 이전 버전의 [!DNL Target]에서 세분화 규칙을 대체합니다.
* 다른 활동에서 재사용하기 위해 활동을 만들어 [!UICONTROL Audience Library]에 저장하거나 활동 전용 대상을 만들 수 있습니다. 대상을 저장한 후에는 대상 유형을 변경할 수 없습니다.
* 기존 활동에 대한 구체화 내용은 활동 전용 대상으로 마이그레이션됩니다.
* 활동 전용 대상의 상태는 [!UICONTROL Used] 또는 [!UICONTROL Unused]입니다. 사용되지 않음 활동 전용 대상은 활동을 저장할 때까지 표시됩니다. 사용되지 않음 상태로 두고 활동을 저장하려고 하면 사용되지 않음 활동 전용 대상은 삭제된다는 사실을 알리는 경고 메시지가 표시됩니다.
* 대상을 열지 않고 대상 선택기에서 액세스한 팝업 카드에서 대상 정의 세부 사항을 볼 수 있습니다.
* [여러 대상을 결합](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)하여 활동 전용 대상을 만들 수 있습니다.
* 활동 전용 대상은 제외 규칙을 지원하지 않습니다.

  다음 대체 요소를 사용하여 제외 규칙을 사용할 수 있습니다.

   * [활동 전용 대상 대신 라이브러리 대상을 만들어 사용](/help/main/c-target/c-audiences/create-audience.md)합니다.
   * [여러 ](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)(최대 20개) 라이브러리 대상을 활동 전용 대상으로 결합합니다. 대상을 조합할 때, 조합된 대상을 활동 전용 대상으로 저장하는 경우에도 개별 라이브러리 대상의 포함 및 제외 규칙을 사용할 수 있습니다.
