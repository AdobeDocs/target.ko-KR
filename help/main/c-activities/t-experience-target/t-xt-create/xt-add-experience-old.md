---
keywords: 경험 만들기;경험 생성;우선순위;대상자;경험;시각적 경험 작성기
description: ' [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (XT) 활동에서 [!UICONTROL Experience Targeting]​(VEC)를 사용하여 페이지에서 경험을 만들고 편집하는 방법을 알아봅니다.'
title: '[!UICONTROL Experience Targeting] 활동에서 경험을 만들려면 어떻게 해야 합니까?'
feature: Experience Targeting
exl-id: ec3fcd93-5557-4f69-8f9c-4d00569188ad
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 35%

---

# [!UICONTROL Experience Targeting]&#x200B;(XT) 활동에서 경험 만들기

[!UICONTROL Visual Experience Composer]의 [!DNL Adobe Target]&#x200B;(VEC)은 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동에서 페이지에서 경험을 편집할 수 있는 시각적 인터페이스를 제공합니다.

1. 변경할 요소를 선택하고 원하는 대로 변경합니다.

   [[!UICONTROL Experience Targeting] 활동을 만드는 동안](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) 세 부분으로 구성된 안내 워크플로우([!UICONTROL Experiences])의 1단계는 [!UICONTROL Experience A] 대상이 있는 기본 [!UICONTROL All Visitors]을(를) 표시합니다.

   ![모든 방문자 대상자](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   이제 변경 사항이 [!UICONTROL Experience A]에 적용됩니다. 아래 단계에서 **[!UICONTROL Add Experience Targeting]**&#x200B;을(를) 클릭하여 추가 경험을 만듭니다.

   페이지의 요소 위로 마우스를 가져가면 요소가 강조 표시됩니다. 강조 표시된 요소는 VEC를 사용하여 변경할 수 있습니다. 요소에서 수행하여 경험을 변경할 수 있는 작업 목록은 [시각적 경험 작성기 선택 사항](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)을 참조하십시오.

   >[!NOTE]
   >
   >기본적으로, VEC에서는 회전 배너 등과 같은 JavaScript가 포함된 요소를 변경할 수 없습니다. JavaScript을 비활성화하여 VEC를 사용하여 해당 요소를 변경할 수 있습니다.

1. 추가 경험을 만들려면 **[!UICONTROL Add Experience Targeting]**&#x200B;을(를) 클릭합니다.

   ![경험 타깃팅 추가 링크](/help/main/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   [!UICONTROL Add Audience] 대화 상자가 표시됩니다. 경험을 대상으로 타깃팅하려면 경험을 추가하기 전에 대상을 선택하십시오.

   대상자 라이브러리에는 [!DNL Target]의 일부로 사전에 만들어진 공통 대상자를 포함하여 이전에 정의한 대상자가 포함되어 있습니다. 라이브러리에서 대상자를 선택하거나, [새 대상자를 만듭니다](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   기존 대상자를 선택할 수 있을 뿐만 아니라, 새 대상자를 만들지 않고 여러 대상자를 결합하여 임시로 결합한 대상자를 만들 수도 있습니다. 자세한 내용은 [여러 대상자 결합](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)을 참조하십시오.

   대상을 만들 때 위치를 선택하고 해당 위치에 대한 매개 변수를 지정할 수 있습니다. [!UICONTROL Custom]&#x200B;([!UICONTROL Create Audience] > [!UICONTROL Custom])에서 위치를 선택한 다음 원하는 매개 변수를 지정합니다.

   >[!NOTE]
   >
   >대상 목록을 연 상태에서 가져온 대상이 10분 이상 오래되면 배경에서 자동으로 대상을 가져옵니다.

1. 경험을 타깃팅할 대상을 한 명 이상 선택하고 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

   ![경험 B](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   경험 B는 이제 이전 일러스트레이션에 표시되며 이 경험은 미국 방문자를 대상으로 합니다.

1. 이 경험에 대해 변경할 요소를 선택하고 위의 1단계에서 설명한 대로 원하는 대로 변경합니다.

1. 필요에 따라 이전 단계를 반복하여 타깃팅된 추가 경험을 만듭니다.

1. 환경 디자인을 마치면 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

   활동 다이어그램이 표시됩니다.

   ![XT 타깃팅 다이어그램](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >기본 페이지 이외의 소스에서 가져온 이미지(예: `akamai.net`에 호스팅되고 `adobe.com`에 전달된 이미지)를 전달할 수 있습니다. 다른 곳에서 호스팅된 이미지는 흐름 다이어그램에 표시된 페이지의 썸네일에 표시되지 않습니다.

1. (조건부) 대상 및 경험 쌍을 원하는 순서로 배열하기 위한 [!UICONTROL Experience Targeting] 활동을 만들거나 편집하면서 대상 및 경험 쌍을 드래그 앤 드롭합니다.

   방문자는 하향식으로 경험에 대해 평가됩니다.

   ![경험 이동](/help/main/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL Experience Targeting]은(는) 순서가 중요하다고 가정합니다. 방문자가 첫 번째 대상 및 경험 쌍에 속하면 첫 번째 경험이 전달됩니다.

   예를 들어 [!UICONTROL Experience Targeting] 활동을 만드는 동안 순서가 중요하다는 것을 알지 못했다고 가정해 봅시다. 경험 B 또는 C에 적격이라고 생각했던 방문자가 경험 A에 적격이라는 사실을 테스트 중에 알게 될 수 있습니다. 이것은 대상이 상호 배타적이지 않으며 적절한 순서로 정렬되지 않았기 때문일 수 있습니다(예: 경험 A = 미국, 경험 B = 샌프란시스코, 경험 C = 캘리포니아). 이 시나리오에서는 샌프란시스코나 캘리포니아에 있는 다른 곳에 있더라도 미국에서 온 모든 사용자가 경험 A에 대한 자격이 있습니다. 전체 활동을 다시 생성하지 않고, 가장 제한적이었던 대상 및 경험 쌍을 가장 덜 제한적인 것에서 가장 덜 제한적인 것으로(샌프란시스코 > 캘리포니아 > 미국) 재정렬할 수 있습니다.

   대상이 [!UICONTROL All Visitors]개인 경우 다이어그램에서 첫 번째 대상이 아닌지 확인하십시오. &quot;[!UICONTROL All Visitors]&quot;을(를) 대상으로 하는 경험은 다른 경험에 속한 적이 없는 모든 방문자를 &quot;찾기 위한&quot; [!UICONTROL Experience Targeting] 활동의 마지막 경험으로 사용할 수 있습니다.

## 경험 이름 변경 또는 편집

[!UICONTROL Edit] 활동의 경험에 대한 [!UICONTROL Experience Targeting] 아이콘(세로 줄임표)을 클릭하고 필요에 따라 다음 옵션 중에서 선택할 수 있습니다.

* [!UICONTROL Rename]
* [!UICONTROL Edit]

![이름 변경 및 편집 선택 사항](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## 경험 삭제

**[!UICONTROL Experiences]** 페이지(3단계 안내식 워크플로우의 첫 번째 단계)에서 세로 줄임표 > **[!UICONTROL Delete]**&#x200B;을(를) 클릭합니다.

![경험 삭제](/help/main/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## 경험 복제

[!UICONTROL Experience Targeting] 활동에서 경험을 복사할 수 있으므로 전체 경험을 다시 작성하지 않고도 약간의 콘텐츠를 변경할 수 있습니다.

**[!UICONTROL Experiences]** 페이지(3단계 안내식 워크플로우의 첫 번째 단계)에서 세로 줄임표 > **[!UICONTROL Duplicate]**&#x200B;을(를) 클릭합니다.

![중복된 경험](/help/main/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## 교육 비디오:

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### A/B 테스트에서 [!UICONTROL Experience Targeting]&#x200B;(으)로

이 비디오에서는 [!UICONTROL Experience Targeting]&#x200B;(XT)을(를) 사용하여 A/B 테스트를 한 단계 업그레이드하는 방법에 대해 설명합니다.

* [!UICONTROL Experience Targeting] 활동을 구성하는 안내가 있는 3단계 워크플로를 설명합니다.
* 지리적 영역에 있는 대상자에게 위치 특정 콘텐츠를 전달하는 방법을 설명합니다.
* 올바른 콘텐츠가 올바른 대상자에게 전달되도록 하기 위해 경험을 재정렬하는 방법을 설명합니다.

>[!VIDEO](https://video.tv.adobe.com/v/30948?captions=kor)

### 활동 유형(9:03)

다음 비디오에서는 [!DNL Target]에서 사용할 수 있는 활동 유형에 대해 설명합니다. [!UICONTROL Experience Targeting]은(는) 5:15부터 논의됩니다.

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로 설명

>[!VIDEO](https://video.tv.adobe.com/v/30520?captions=kor)

### [!UICONTROL Visual Experience Composer] 사용

이 비디오에서는 [!UICONTROL Experience Targeting]&#x200B;(VEC) 옵션 사용에 대한 정보를 제공합니다.

* 페이지 콘텐츠 변경
* 페이지 레이아웃 변경

>[!VIDEO](https://video.tv.adobe.com/v/30516?captions=kor)
