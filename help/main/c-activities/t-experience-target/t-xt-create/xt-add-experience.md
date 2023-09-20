---
keywords: 경험 만들기;경험 생성;우선순위;대상;경험;시각적 경험 작성기
description: 사용 방법 알아보기 [!DNL Adobe Target] [!UICONTROL 시각적 경험 작성기] (VEC) 를 클릭하여 페이지에서 경험을 만들고 편집할 수 있습니다 [!UICONTROL 경험 타기팅] (XT) 활동.
title: 에서 경험을 만드는 방법 [!UICONTROL 경험 타기팅] 활동?
feature: Experience Targeting
exl-id: ec3fcd93-5557-4f69-8f9c-4d00569188ad
source-git-commit: 0dfdd995c00961ed2aed91ec03406e8493292af7
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 39%

---

# 에서 경험 만들기 [!UICONTROL 경험 타기팅] (XT) 활동

다음 [!UICONTROL 시각적 경험 작성기] (VEC) 위치 [!DNL Adobe Target] 에서는 페이지에서 경험을 편집할 수 있는 시각적 인터페이스를 제공합니다. [!UICONTROL 경험 타기팅] (XT) 활동.

1. 변경할 요소를 선택하고 원하는 대로 변경합니다.

   While [만들기 [!UICONTROL 경험 타기팅] 활동](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), 안내가 있는 3부분 워크플로우 중 1단계([!UICONTROL 경험])에 기본값이 표시됩니다 [!UICONTROL 경험 A] 다음 포함 [!UICONTROL 모든 방문자] 대상입니다.

   ![모든 방문자 대상](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   이제 적용되는 모든 변경 사항 [!UICONTROL 경험 A]. 아래 단계에서 다음을 클릭합니다. **[!UICONTROL 경험 타깃팅 추가]** 추가 경험을 만들려면

   페이지의 요소 위로 마우스를 가져가면 요소가 강조 표시됩니다. 강조 표시된 요소는 VEC를 사용하여 변경할 수 있습니다. 요소에서 수행하여 경험을 변경할 수 있는 작업 목록은 [시각적 경험 작성기 선택 사항](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)을 참조하십시오.

   >[!NOTE]
   >
   >기본적으로, VEC에서는 회전 배너 등과 같은 JavaScript가 포함된 요소를 변경할 수 없습니다. JavaScript를 비활성화하여 VEC를 사용하여 이러한 요소를 변경할 수 있습니다.

1. 추가 경험을 만들려면 **[!UICONTROL 경험 타깃팅 추가]**&#x200B;를 클릭합니다.

   ![경험 타깃팅 추가 링크](/help/main/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   다음 [!UICONTROL 대상 추가] 대화 상자가 표시됩니다. 경험을 대상으로 타깃팅하려면 경험을 추가하기 전에 대상을 선택하십시오.

   대상 라이브러리에는 [!DNL Target]의 일부로 사전에 만들어진 공통 대상을 포함하여 이전에 정의한 대상들이 포함되어 있습니다. 라이브러리에서 대상을 선택하거나, [새 대상을 만듭니다](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   기존 대상을 선택할 수 있을 뿐만 아니라, 새 대상을 만들지 않고 여러 대상을 결합하여 임시로 결합한 대상을 만들 수도 있습니다. 자세한 내용은 [여러 대상 결합](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)을 참조하십시오.

   대상을 만들 때 위치를 선택하고 해당 위치에 대한 매개 변수를 지정할 수 있습니다. 아래 [!UICONTROL 사용자 정의] ([!UICONTROL 대상자 만들기] > [!UICONTROL 사용자 정의]) 위치를 선택한 다음 원하는 매개 변수를 지정합니다.

   >[!NOTE]
   >
   >대상 목록을 연 상태에서 가져온 대상이 10분 이상 오래되면 배경에서 자동으로 대상을 가져옵니다.

1. 경험을 타깃팅할 대상을 한 명 이상 선택하고 **[!UICONTROL 완료]**&#x200B;를 클릭합니다.

   ![경험 B](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   경험 B는 이제 이전 일러스트레이션에 표시되며 이 경험은 미국 방문자를 대상으로 합니다.

1. 이 경험에 대해 변경할 요소를 선택하고 위의 1단계에서 설명한 대로 원하는 대로 변경합니다.

1. 필요에 따라 이전 단계를 반복하여 타깃팅된 추가 경험을 만듭니다.

1. 경험 디자인을 마치면 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   활동 다이어그램이 표시됩니다.

   ![XT 타깃팅 다이어그램](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >기본 페이지 이외의 소스에서 가져온 이미지(예:에 호스팅된 이미지)를 전달할 수 있습니다 `akamai.net` 게재일 `adobe.com`). 다른 곳에서 호스팅된 이미지는 흐름 다이어그램에 표시된 페이지의 썸네일에 표시되지 않습니다.

1. (조건부) 만들거나 편집할 때 대상 및 경험 쌍을 드래그 앤 드롭합니다 [!UICONTROL 경험 타기팅] 원하는 순서로 쌍을 정렬하는 활동입니다.

   방문자는 하향식으로 경험에 대해 평가됩니다.

   ![경험 이동](/help/main/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL 경험 타깃팅에서는 순서를 중요한 것으로 간주합니다. ] 방문자가 첫 번째 대상 및 경험 쌍에 속하면 첫 번째 경험이 전달됩니다.

   예를 들어 를 만드는 동안 순서가 중요하다는 것을 알지 못했다고 가정해 봅시다. [!UICONTROL 경험 타기팅] 활동. 경험 B 또는 C에 적격이라고 생각했던 방문자가 경험 A에 적격이라는 사실을 테스트 중에 알게 될 수 있습니다. 이것은 대상이 상호 배타적이지 않으며 적절한 순서로 정렬되지 않았기 때문일 수 있습니다(예: 경험 A = 미국, 경험 B = 샌프란시스코, 경험 C = 캘리포니아). 이 시나리오에서는 샌프란시스코나 캘리포니아에 있는 다른 곳에 있더라도 미국에서 온 모든 사용자가 경험 A에 대한 자격이 있습니다. 전체 활동을 다시 생성하지 않고, 가장 제한적이었던 대상 및 경험 쌍을 가장 덜 제한적인 것에서 가장 덜 제한적인 것으로(샌프란시스코 > 캘리포니아 > 미국) 재정렬할 수 있습니다.

   [!UICONTROL 모든 방문자] 대상이 있는 경우 다이어그램에서 첫 번째 대상이 아닌지 확인합니다. &quot; 을(를) 타깃팅한 경험[!UICONTROL 모든 방문자]&quot;는 의 마지막 경험으로 사용할 수 있습니다. [!UICONTROL 경험 타기팅] 다른 경험에 속한 적이 없는 모든 방문자를 &quot;찾기 위한&quot; 활동입니다.

## 경험 이름 변경 또는 편집

다음을 클릭할 수 있습니다 [!UICONTROL 편집] 의 경험에 대한 아이콘(수직 줄임표) [!UICONTROL 경험 타기팅] 필요한 경우 활동 및 다음 옵션 중에서 선택합니다.

* [!UICONTROL 이름 변경]
* [!UICONTROL 편집]

![이름 변경 및 편집 선택 사항](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## 경험 삭제

다음에서 **[!UICONTROL 경험]** 페이지(3단계 안내식 워크플로우의 첫 번째 단계)에서 세로 줄임표 > **[!UICONTROL 삭제]**.

![경험 삭제](/help/main/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## 경험 복제

에서 경험을 복사할 수 있습니다. [!UICONTROL 경험 타기팅] 활동을 활성화하면 전체 경험을 다시 작성하지 않고도 간단한 변경을 수행할 수 있습니다.

다음에서 **[!UICONTROL 경험]** 페이지(3단계 안내식 워크플로우의 첫 번째 단계)에서 세로 줄임표 > **[!UICONTROL 복제]**.

![중복된 경험](/help/main/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## 교육 비디오:

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### A/B 테스트에서으로 [!UICONTROL 경험 타기팅]

이 비디오에서는 을(를) 사용하여 A/B 테스트를 다음 수준으로 이끄는 방법에 대해 설명합니다. [!UICONTROL 경험 타기팅] (XT).

* 을 구성하는 3단계 안내가 있는 워크플로 설명 [!UICONTROL 경험 타기팅] 활동
* 지리적 영역에 있는 대상자에게 위치 특정 콘텐츠를 전달하는 방법을 설명합니다.
* 올바른 콘텐츠가 올바른 대상에게 전달되도록 하기 위해 경험을 재정렬하는 방법을 설명합니다.

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### 활동 유형(9:03)

다음 비디오에서는 [!DNL Target]에서 사용할 수 있는 활동 유형에 대해 설명합니다. [!UICONTROL 경험 타깃팅은 5:15에서 시작하는 것에 대해 논의합니다.]

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로 설명

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### 사용 [!UICONTROL 시각적 경험 작성기]

이 비디오에서는 사용 방법에 대한 정보를 제공합니다 [!UICONTROL 경험 타기팅] (VEC) 옵션.

* 페이지 콘텐츠 변경
* 페이지 레이아웃 변경

>[!VIDEO](https://video.tv.adobe.com/v/17399)
