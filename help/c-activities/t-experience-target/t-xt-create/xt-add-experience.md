---
description: Visual Experience Composer (VEC) 는 XT (경험 타깃팅) 활동에서 페이지에서 경험을 편집할 수 있는 시각적 인터페이스를 제공합니다.
keywords: 경험 만들기;경험 생성;우선순위;대상;경험;시각적 경험 작성기
seo-description: Adobe Target VEC (Visual Experience Composer) 는 XT (경험 타깃팅) 활동에서 페이지에서 경험을 편집할 수 있는 시각적 인터페이스를 제공합니다.
seo-title: '경험 만들기 '
solution: Target
title: '경험 만들기 '
topic: 고급,Standard,Classic
uuid: ce559c3c-5a16-46b8-b2a7-df696626c7c0
translation-type: tm+mt
source-git-commit: 6911a91aba8505e8f91a7ab9723c54bd8e7082b7

---


# Create experience{#create-experience}

The [!UICONTROL Visual Experience Composer] (VEC) provides a visual interface for editing the experiences on your page in an [!UICONTROL Experience Targeting] (XT) activity.

1. 변경할 요소를 선택하고 원하는 대로 변경합니다.

   While [creating an XT activity](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), step one of the three-part guided workflow ([!UICONTROL Experiences]) displays the default [!UICONTROL Experience A] with an [!UICONTROL All Visitors] audience.

   ![모든 방문자 대상](/help/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Any changes you make now apply to Experience A. In a step below, you'll click **[!UICONTROL Add Experience Targeting]** to create additional experiences.

   페이지의 요소 위에 마우스를 가져가면 요소가 강조 표시됩니다. 강조 표시된 요소는 vec를 사용하여 변경할 수 있습니다. For a list of actions that can be performed on an element to change the experience, see [Visual Experience Composer Options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   If you created an mbox on the page using [!DNL Target Classic], that mbox appears as an element that shows the mbox name, and can be modified like any other element.

   >[!NOTE]
   >
   >기본적으로 vec는 회전 배너와 같이 JavaScript가 포함된 요소의 변경을 허용하지 않습니다. Javascript를 비활성화하여 vec를 사용하여 해당 요소를 변경할 수 있습니다.

1. To create additional experiences, click **[!UICONTROL Add Experience Targeting]**.

   ![경험 타깃팅 링크 추가](/help/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   The [!UICONTROL Choose Audience] dialog box displays. 경험을 추가하려면 경험을 추가하려면 먼저 대상을 선택해야 합니다.

   The audience library contains audiences that have previously been defined, including some common audiences that are pre-built as a part of [!DNL Target]. You can select an audience from the library or [create a new audience](../../../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   >[!NOTE]
   >
   >기존 대상을 선택할 수 있을 뿐만 아니라, 새 대상을 만들지 않고 여러 대상을 결합하여 임시로 결합한 대상을 만들 수도 있습니다. 자세한 내용은 [여러 대상 결합](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5)을 참조하십시오.

   고객을 만들 때 위치(mbox)를 선택하고 해당 위치에 대한 매개 변수를 지정할 수 있습니다. [!UICONTROL 사용자 지정] (대상 만들기 &gt; 규칙 추가 &gt; 사용자 지정) 아래에서 mbox를 선택한 다음 원하는 매개 변수를 지정합니다.

   >[!NOTE]
   >
   >대상 목록을 연 상태에서 가져온 대상이 10분 이상 오래되면 배경에서 자동으로 대상을 가져옵니다.

1. Select one or more audiences to target with the experience, then click **[!UICONTROL Done]**.

   ![경험 B](/help/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   경험 B는 이전 일러스트레이션에 표시되며 이 경험은 미국 방문자를 대상으로 합니다.

1. 이 경험에 대해 변경할 요소를 선택하고, 위의 1 단계에 설명된 대로 원하는 변경을 수행합니다.

1. 필요에 따라 위의 단계를 반복하여 타깃팅된 추가 경험을 만듭니다.

1. Click **[!UICONTROL Next]** when you are finished designing your experiences.

   활동 다이어그램이 표시됩니다.

   ![XT 타깃팅 다이어그램](/help/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >If you deliver an image from a source other than your main page (such as an image hosted on `akamai.net` and delivered on `adobe.com`), that image does not display in the thumbnail of the page shown in the flow diagram.

1. (조건부) XT 활동을 만들거나 편집하는 동안 대상/경험 쌍을 드래그하여 놓아 원하는 순서대로 쌍을 정렬합니다.

   방문자는 위에서 아래로, 순서대로 경험에 대해 평가됩니다.

   ![경험 이동](/help/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL 경험 타깃팅에서는 순서를 중요한 것으로 간주합니다. ] 방문자가 첫 번째 대상/경험 쌍에 속하는 경우 첫 번째 경험이 전달됩니다.

   예를 들어, XT 활동을 만드는 동안 순서가 중요하다는 것을 인식하지 못한다고 가정해보겠습니다. 경험 B 또는 C에 적격이라고 생각했던 방문자가 경험 A에 적격이라는 사실을 테스트 중에 알게 될 수 있습니다. 이것은 대상이 상호 배타적이지 않으며 적절한 순서로 정렬되지 않았기 때문일 수 있습니다(예: 경험 A = 미국, 경험 B = 샌프란시스코, 경험 C = 캘리포니아). 이 시나리오에서 미국의 모든 사용자는 샌프란시스코나 캘리포니아의 다른 지역에 있더라도 경험 A에 적격입니다. 전체 활동을 다시 만들지 않고, 가장 제한적인 것부터 덜 제한적인 순서로(샌프란시스코 &gt; 캘리포니아 &gt; 미국) 대상/경험 쌍을 재정렬할 수 있습니다.

   [!UICONTROL 모든 방문자] 대상자가 있는 경우, 다이어그램에서 첫 번째 대상이 아닌지 확인하십시오. "모든 방문자"를 대상으로 하는 경험은 다른 경험에 속한 적이 없는 모든 방문자를 "찾기 위한" 경험 타깃팅 활동의 마지막 경험으로 사용될 수 있습니다.

## 경험 이름 변경 또는 편집

You can click the [!UICONTROL Edit] icon (three vertical ellipses) on an experience in an XT activity and choose from the following options, as necessary:

* 이름 변경
* 편집

![이름 변경 및 편집 옵션](/help/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## 경험 삭제

**[!UICONTROL 경험]** 페이지 (3 단계 안내 워크플로우의 첫 번째 단계) 에서 세 개의 세로 줄임표 &gt; **[!UICONTROL 삭제를 클릭합니다]**.

![경험 삭제](/help/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## 경험 복제

경험을 처음부터 다시 만들지 않고도 내용을 약간 변경할 수 있도록 XT 활동에 경험을 복사할 수 있습니다.

**[!UICONTROL 경험]** 페이지(3단계 안내식 워크플로우의 첫 번째 단계)에서 세 개의 수직 줄임표 &gt; **[!UICONTROL 중복]**&#x200B;을 클릭하십시오.

![중복된 경험](/help/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## 교육 비디오:

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### A/B 테스트부터 경험 타깃팅까지

이 비디오는 경험 타깃팅(XT)을 통해 A/B 테스트를 다음 수준으로 가져오는 방법을 설명합니다.

* XT 활동을 구성하는 3단계 안내 워크플로우를 설명합니다.
* 지리적 영역에 있는 대상으로 위치 특정 컨텐츠를 전달하는 방법을 설명합니다.
* 올바른 컨텐츠가 올바른 대상에게 전달되도록 하기 위해 경험을 재정렬하는 방법을 설명합니다.

>[!VIDEO](https://video.tv.adobe.com/v/22418/?captions=kor)

### 활동 유형(9:03)

다음 비디오에서는 Target Standard/Premium에서 사용할 수 있는 활동 유형에 대해 설명합니다. 경험 타깃팅은 5:15에서 시작하는 것에 대해 논의합니다.

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로우 설명

>[!VIDEO](https://video.tv.adobe.com/v/17386?captions=kor)

### Visual Experience Composer 사용

이 비디오에서는 시각적 경험 작성기 선택 사항 사용에 대한 정보를 제공합니다.

* 페이지 컨텐츠 변경
* 페이지 레이아웃 변경

>[!VIDEO](https://video.tv.adobe.com/v/17399?captions=kor)