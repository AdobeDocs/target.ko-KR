---
keywords: 대상자;성향;프로필 속성;비교하기;비교;대상자 만들기;대상자 작성
description: 두 프로필 속성을 비교할 대상을 정의하는 방법을 알아봅니다.
title: 대상에서 사용할 두 프로필 속성을 비교할 수 있습니까?
feature: Audiences
exl-id: 033e90f1-5a05-4fce-a520-68826860a908
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 49%

---

# 프로필 속성 비교 대상자 만들기

[!DNL Adobe Target]에서 대상을 정의하여 [대상 라이브러리](/help/main/c-target/c-audiences/audiences.md) 또는 [활동 전용 대상](/help/main/c-target/creating-activity-only-audience.md)의 두 프로필 특성을 비교합니다. 보다 큼, 보다 작음 또는 같음 등의 연산자를 사용하여 두 개 다른 프로필 속성 값을 동적으로 비교하는 대상자를 정의합니다.

>[!NOTE]
>
>이 기능은 [[!UICONTROL Visitor Profile]](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E) 범주에서만 사용할 수 있습니다.

## 개요 {#section_303CBC78194D49A2A004945D425441E1}

대상자는 [!DNL Target] 활동에서 포함되거나 제외되는 사용자를 결정하는 규칙으로 정의됩니다. 대상 정의에는 여러 규칙이 포함될 수 있으며 각 규칙에는 여러 매개 변수가 포함될 수 있습니다. 포함된 규칙 중 하나가 [!UICONTROL Visitor Profile] 범주를 사용하는 경우 방문자 프로필 특성의 특정 값을 기준으로 규칙을 정의하거나 해당 특성의 값을 다른 방문자 프로필 특성과 비교할 수 있습니다.

예를 들어 가구 회사에 근무하면서 두 개의 고객 성향 점수를 [!DNL Target]에 업로드했다고 가정해 보겠습니다.

* 향후 90일 이내에 부엌 가구를 구입할 가능성
* 향후 90일 이내에 거실 가구를 구입할 가능성

부엌 가구를 구입할 경향이 거실 가구를 구입할 경향보다 크다고 정의된 대상을 생성할 수 있습니다. 그런 다음 [!DNL Target]은(는) 특정 방문자의 식당 및 거실 성향 점수를 동적으로 비교하여 해당 방문자가 이 대상자에 적합한지 확인합니다.

자세한 내용은 [데이터를 Target으로 가져오는 방법](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=ko){target=_blank}을 참조하세요.

## 프로필 속성 비교 대상자 만들기 {#section_7A62FD47D5C74C3EBC3417ACDBB85013}

1. **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**&#x200B;을(를) 클릭합니다.
1. 대상자의 이름을 지정하고 선택적 설명을 추가합니다.
1. **[!UICONTROL Visitor Profile]**&#x200B;을(를) 대상 빌더 창으로 끌어서 놓습니다.
1. **[!UICONTROL Visitor Profile]** 드롭다운 목록에서 특성을 선택합니다.

   ![성향 점수 1](assets/propensity_score_1.png)

1. 평가기를 선택합니다.

   ![성향 점수 2](assets/propensity_score_2.png)

1. **[!UICONTROL Choose Comparison Type]** 드롭다운 목록에서 **[!UICONTROL Attribute]**&#x200B;을(를) 선택합니다.

   &quot;정적 값&quot; 비교 유형을 사용하면 방문자 프로필 속성을 특정 값과 비교할 수 있습니다.

   ![성향 점수 3](assets/propensity_score_3.png)

   >[!NOTE]
   >
   >기본 방문자 프로필 카테고리 중 하나(예: 새 방문자 또는 재방문자)를 사용하는 경우 정적 값 옵션만 선택할 수 있습니다. 동적 비교 옵션은 기본 카테고리에 사용할 수 없습니다. 동적 비교 옵션을 사용할 수 없는 다른 예로는 &quot;세션의 첫 페이지&quot;, &quot;다른 테스트에 없음&quot;, &quot;세션의 첫 페이지 아님&quot;, &quot;카테고리 친화성&quot;이 있습니다.

1. 초기 속성과 비교할 추가 속성을 선택합니다.

   ![propensity_score_4 이미지](assets/propensity_score_4.png)

1. **[!UICONTROL Done]** 아이콘을 클릭합니다.

## 교육 비디오 ![개요 배지](/help/main/assets/overview.png) {#section_3BB8DBF3418F4520B3E274B6F40AF8F3}

이 기능을 사용할 수 있는 시나리오 및 자세한 내용은 비디오를 참조하십시오.

>[!VIDEO](https://video.tv.adobe.com/v/23218/)
