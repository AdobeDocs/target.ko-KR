---
keywords: 대상자;대상자 선택;대상자 선택;선택기
description: 대상은 Adobe [!DNL Target] 활동에 입력된 사이트 방문자를 결정합니다.
title: A [!DNL Target] A/B 활동에서 대상을 선택하려면 어떻게 해야 합니까?
feature: A/B Tests
exl-id: 281ae227-c593-4b71-ad12-865430b332be
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 66%

---

# 대상자 선택

대상은 [!DNL Adobe Target] 활동에 입력된 사이트 방문자를 결정합니다.

>[!NOTE]
>
>기존 대상자를 선택할 수 있을 뿐만 아니라, 새 대상자를 만들지 않고 여러 대상자를 결합하여 임시로 결합한 대상자를 만들 수도 있습니다. 자세한 내용은 [여러 대상자 결합](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)을 참조하십시오.

1. [!UICONTROL Audience] 상자에서 **[!UICONTROL Edit]** 아이콘(세로 줄임표)을 클릭한 다음 **[!UICONTROL Replace Audience]**&#x200B;을(를) 클릭합니다.

   ![대상자 바꾸기 선택 사항](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/replace-audience.png)

   기본적으로 모든 방문자는 대상입니다. 그러나 대상을 변경할 수 있습니다. 대상 라이브러리에서 대상을 선택하거나 활동 전용 대상을 만들 수 있습니다. 대상 라이브러리에는 [!DNL Target]의 일부로 미리 만들어진 공통 대상을 포함하여 이전에 정의된 대상이 포함되어 있습니다.

1. 원하는 대상자를 선택하거나 만듭니다.

   * 라이브러리에서 대상자 선택
   * [여러 대상자 결합](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)
   * [새 대상자 만들기](/help/main/c-target/c-audiences/create-audience.md#task_1D507519D3AD4390B507F188BD294DC1)
   * [활동 전용 대상을 만듭니다](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483).

   특정 대상 타깃팅이 없는 A/B 테스트의 경우 기본값 [!UICONTROL All Visitors]을(를) 선택하십시오.

   아래 표시된 대로 [!UICONTROL Add Audience] 대화 상자에서 원하는 대상 위로 마우스를 가져간 후 대상을 편집하거나 복사할 수도 있습니다.

   기존 대상과 유사한 대상을 만들려는 경우 대상을 복사하면 유용합니다. 대상의 복사본을 만들어 편집한 다음, 새 대상으로 저장할 수 있습니다. 이 마우스로 가리키는 기능은 다른 활동 유형에서도 사용할 수 있습니다.

   ![대상자를 마우스로 가리키기](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audience_picker_hover-new.png)

   고객을 만들 때 위치(mbox)를 선택하고 해당 위치에 대한 매개 변수를 지정할 수 있습니다. [!UICONTROL Custom Parameters]에서 mbox를 선택한 다음 원하는 매개 변수를 지정합니다.

   >[!NOTE]
   >
   >대상자 목록을 연 상태에서 가져온 대상자가 10분 이상되면 배경에서 자동으로 대상자를 가져옵니다.

1. (조건부) 활동에 포함할 자격 있는 방문자의 비율을 지정합니다.

   예를 들어, 모든 방문자의 50%를 포함하도록 선택할 수 있습니다.

   ![대상자 비율](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Target에서 [트래픽을 자동으로 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)하도록 선택할 수도 있습니다.

## 교육 비디오

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### Adobe Target에서 대상자 사용(6:21) ![개요 배지](/help/main/assets/overview.png)

다음 비디오에서는 [!DNL Target Standard/Premium]에서 대상자를 사용하는 방법을 설명합니다.

* 용어 &quot;대상&quot; 설명
* 최적화에 대상을 사용하는 두 가지 방법 설명
* 대상자 목록에서 대상자 찾기
* 활동을 대상자에 타기팅
* 활동에서 수동 보고에 대상 사용

>[!VIDEO](https://video.tv.adobe.com/v/17398)

### 활동 워크플로 - 타깃팅(2:14) ![튜토리얼 배지](/help/main/assets/tutorial.png)

다음 비디오에는 대상 설정에 대한 정보가 포함되어 있습니다.

* 활동에 대상 지정
* 트래픽을 늘이기 또는 줄이기
* 트래픽 할당 방법 선택
* 서로 다른 경험에 트래픽 할당

>[!VIDEO](https://video.tv.adobe.com/v/17385)

자세한 내용은 [대상자](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271)를 참조하십시오.
