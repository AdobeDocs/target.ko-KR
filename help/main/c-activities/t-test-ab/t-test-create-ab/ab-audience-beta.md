---
keywords: 대상자;대상자 선택;대상자 선택;선택기
description: 대상 기준에 따라 Adobe [!DNL Target] 활동에 참여하는 사이트 방문자를 정의합니다.
title: A [!DNL Target] A/B 활동에서 대상을 선택하려면 어떻게 해야 합니까?
feature: A/B Tests
hide: true
hidefromtoc: true
source-git-commit: cc823f84fb93cbe2e55d394d0f6f4fe48bbd5293
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 12%

---

# 대상자 선택

대상은 자격 있는 방문자가 [!DNL Adobe Target] 활동에 입력되는지 확인합니다.

[활동을 만들 때](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab-beta.md)의 세 부분으로 구성된 안내 워크플로의 [!UICONTROL Targeting] 단계에는 대상 및 해당 트래픽 비율을 할당하고, 트래픽 할당 방법을 선택하고, 활동의 각 경험에 대해 트래픽 할당을 지정하는 단계를 안내하는 흐름 다이어그램이 표시됩니다.

![A/B 테스트 타깃팅 단계](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

흐름 다이어그램의 모든 옵션에 대한 자세한 내용은 [A/B 테스트 활동 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab-beta.md)를 참조하십시오.

## 활동에 대한 대상 선택

1. **[!UICONTROL All Visitors]** 컨트롤을 클릭하여 활동에 대한 다른 대상을 선택합니다.

   [!UICONTROL All Visitors] 대상이 기본값으로 설정됩니다. 다른 대상을 선택하면 해당 이름이 가장 왼쪽 컨트롤에 표시됩니다.

   특정 대상 타깃팅이 없는 A/B 테스트의 경우 기본값 [!UICONTROL All Visitors]을(를) 선택하십시오.

   오른쪽 프레임이 표시되어 대상을 추가 또는 삭제하고 활동에 대한 방문자 비율을 할당할 수 있습니다.

1. 대상을 변경하려면 오른쪽 프레임에서 **[!UICONTROL Replace]아이콘**(![바꾸기 아이콘](/help/main/assets/icons/Retweet.svg))을 클릭합니다.

1. [!UICONTROL Add Audience] 대화 상자에서 [원하는 대상을 선택](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md)한 다음 **[!UICONTROL Assign Audience]**&#x200B;을(를) 클릭합니다.

   기본적으로 모든 방문자는 대상입니다. 그러나 대상을 변경할 수 있습니다. 대상자가 [!UICONTROL Audience Library]에서 선택되었거나 활동 전용 대상자를 만들 수 있습니다. [!UICONTROL Audience Library]에는 [!DNL Target]의 일부로 미리 만들어진 공통 대상을 포함하여 이전에 정의된 대상이 포함되어 있습니다.

1. (조건부) **대상 결합**&#x200B;에서 [여러 대상을 결합하는 대상 만들기](/help/main/c-target/combining-multiple-audiences.md)를 클릭합니다.

1. (조건부) [!UICONTROL Audience Library]에 없는 새 대상을 만들려면 **대상 만들기**&#x200B;를 클릭합니다. [대상자 만들기 워크플로](/help/main/c-target/c-audiences/audiences.md)에서 다음 옵션 중 선택할 수 있습니다.

   * [!UICONTROL Audience Library]에 저장되어 다른 활동에서 다시 사용할 수 있는 온디맨드 대상을 만듭니다.
   * [!UICONTROL Audience Library]에 저장되지 않고 현재 활동에서만 사용할 수 있는 [활동별 대상](/help/main/c-target/creating-activity-only-audience.md)을 만드십시오.

1. 오른쪽 창에서 **[!UICONTROL Visitor Percentage]**&#x200B;을(를) 클릭한 다음 활동에 포함할 자격 있는 방문자의 비율을 지정합니다.

1. 대상자가 만족스러우면 **[!UICONTROL Next]**&#x200B;을(를) 클릭하여 안내가 있는 3단계 워크플로의 세 번째 단계로 이동합니다.

>[!NOTE]
>
>대상자 목록을 연 상태에서 가져온 대상자가 10분 이상되면 배경에서 자동으로 대상자를 가져옵니다.

## 대상자 정보 보기

1. [!UICONTROL Add Audiences] 대화 상자에서 대상 옆에 있는 **[!UICONTROL Information]** 아이콘(![정보 아이콘](/help/main/assets/icons/InfoOutline.svg) )을 클릭하여 원본 및 특성을 포함하여 해당 대상에 대한 세부 정보를 봅니다.

1. 대상자에 대한 추가 세부 정보를 보려면 **[!UICONTROL View Full Details]**&#x200B;을(를) 클릭하십시오. 세부 정보에는 대상자의 속성, 대상자의 설명, 작업 공간, 유형 및 소스, 이 대상자를 참조하는 활동 목록이 포함됩니다. 활동 이름, 상태, 작업 공간 및 대상자를 마지막으로 수정한 시기와 대상자를 포함하여 각 대상자에 대한 정보를 볼 수 있습니다.

## 대상자 편집 또는 복사

[!UICONTROL Add Audience] 대화 상자에서 원하는 대상 옆에 있는 [!UICONTROL More Actions] 아이콘(![추가 작업 아이콘](/help/main/assets/icons/More.svg))을 클릭한 다음 [!UICONTROL Edit] 또는 [!UICONTROL Copy]을(를) 클릭하여 대상을 편집하거나 복사할 수 있습니다.

기존 대상과 유사한 대상을 만들려는 경우 대상을 복사하면 유용합니다. 대상을 복사하고 편집을 한 다음 새 대상으로 저장할 수 있습니다.

