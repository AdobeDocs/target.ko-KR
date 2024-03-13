---
keywords: 시간대;시작 날짜;종료 날짜;시작/종료 날짜;시간대;타깃팅 일정;주 분할;일 분할;분할
description: 시작 및 종료 날짜 및 시간을 사용하여 특정 시간대 동안 사이트를 방문하는 사용자를 타겟팅하는 방법에 대해 알아봅니다.
title: 특정 시간에 내 사이트를 방문하는 방문자를 타겟팅할 수 있습니까?
feature: Audiences
exl-id: 814d545d-baee-4f8b-a2ed-ed68fceaeb7f
source-git-commit: 0e4698935b90cc0236abe6a47a6183c7fd2a7b20
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 35%

---

# [!UICONTROL Time Frame]

시작 및 종료 날짜 및 시간을 추가할 수 있습니다. [!DNL Adobe Target] 특정 시간대 동안 사이트를 방문하는 사용자를 타겟팅할 수 있습니다. 또한 주/요일 분할 선택 사항을 설정하여 대상 타깃팅을 위한 반복 패턴을 만들 수도 있습니다.

예를 들어 [결합한 임시 대상 기능](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), 블랙 프라이데이 이전 3일 동안에 특정 콘텐츠에 돈을 덜 쓰는 대상과 블랙 프라이데이 이후에 다른 콘텐츠에 돈을 덜 쓰는 대상을 타깃팅할 수 있습니다.

1. 다음에서 [!DNL Target] 인터페이스, 클릭 **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. 대상자의 이름을 지정하고 선택적 설명을 추가합니다.
1. 드래그 앤 드롭 **[!UICONTROL Time Frame]** 대상 빌더 창으로 이동합니다.

   ![target_timeframe_dialog 이미지](assets/target_timeframe_dialog.png)

1. 다음을 지정합니다. [!UICONTROL Start] 및 [!UICONTROL End] 대상의 날짜 및 시간입니다.

   활동의 일정에 따라 타깃팅을 시작하려면 시작 날짜를 비워 두십시오. 활동의 종료 날짜 및 시간까지 계속 타깃팅하려면 종료 날짜를 비워 두십시오.

   시작 및 종료 날짜를 모두 비워 둘 수도 있습니다. 이 기능을 사용하면 활동 수준에서 시작 및 종료 날짜를 제어하면서 여러 활동에서 동일한 대상(대상 복사본을 만들지 않고)을 사용할 수 있습니다.

   >[!NOTE]
   >
   >다음 사항을 고려하십시오.
   >
   >* 시작/종료일 시간대는 GMT +/- NN:NN 형식으로 표시되며, 여기서 NN:NN은 GMT로부터의 오프셋으로서, 방문자의 시간대가 아닌 계정 수준 시간대를 반영합니다. 예를 들어, 캘리포니아 시간대는 GMT -08:00로 표시됩니다.
   >
   >* [!DNL Target] 시간 대상은 일광 절약 시간제(DST) 변경을 고려하지 않습니다. 일광 절약 시간 변경 사항을 고려하려면 대상을 수동으로 다시 저장해야 합니다.

1. (조건부) 클릭 **[!UICONTROL Set frequency]** 요일 및 시간을 포함하여 반복 패턴을 설정합니다.

   ![주/요일 분할](assets/week_and_day_parting.png)

   다음을 사용할 수 있습니다. [!UICONTROL Frequency] 예를 들어 콜센터에 근무하는 일 및 시간 동안에만 &quot;채팅 지금&quot; 옵션을 방문자에게 표시하는 옵션과 같은 옵션이 있습니다.

   요일을 하나 이상 선택한 다음, 시작 및 종료 시간을 설정하십시오. 클릭 **[!UICONTROL Add frequency]** 원하는 대로 추가 패턴을 지정합니다.

   >[!NOTE]
   >
   >의 시간대 [!UICONTROL Week and Day Parting] 는 GMT +/- NN:NN으로 표시되며, 여기서 NN:NN은 GMT로부터의 오프셋으로서, 방문자의 시간대가 아닌 계정 수준 시간대를 반영합니다. 예를 들어 태평양 일광 절약 시간제에 대한 캘리포니아 시간대는 GMT -07:00로 표시됩니다.

1. (선택 사항) 대상에 대한 추가 규칙을 설정합니다.

   원하는 경우 각 규칙에 대해 5단계를 반복할 수 있습니다.

1. **[!UICONTROL Done]** 아이콘을 클릭합니다.

## 교육 비디오: 대상자 만들기 ![개요 배지](/help/main/assets/overview.png)

다음 비디오에는 대상 카테고리 사용에 대한 정보가 포함되어 있습니다.

* 대상자 만들기
* 대상 카테고리 정의

>[!VIDEO](https://video.tv.adobe.com/v/17392)
