---
keywords: 사용자 지정 매개 변수;타겟 사용자 지정 매개 변수;targetpageparams;타깃팅 mbox 매개 변수
description: 대상자에서 사용할 수 있도록  [!DNL Adobe Target] 에 사용자 지정 매개 변수를 전달하는 방법을 알아봅니다.
title: 사용자 지정 매개 변수를 기반으로 하여 방문자를 타깃팅할 수 있습니까?
feature: Audiences
exl-id: f0669888-6b9e-4738-9ed4-0418ea56fffa
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 38%

---

# 사용자 지정 매개 변수

사용자 지정 매개 변수는 [!DNL Adobe Target]의 mbox 매개 변수입니다. mbox 매개 변수를 mbox에 전달하거나 `targetPageParams` 함수를 사용하는 경우 해당 매개 변수가 여기에 표시되어 대상에 사용됩니다.

자세한 내용은 [글로벌 mbox에 매개 변수 전달](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/global-mbox/pass-parameters-to-global-mbox.html?lang=ko){target=_blank}을 참조하세요.

mbox 매개 변수를 기반으로 하여 사용자 지정 대상자를 작성할 때 `mboxParameter`에 대해 묻는 메시지가 `mboxName`에 더 이상 표시되지 않습니다. 이제 mbox 이름은 선택 사항입니다. 따라서 여러 mbox의 매개 변수를 사용하거나 가장자리에 아직 기록되지 않은 매개 변수를 참조할 수 있습니다.

1. [!DNL Target] 인터페이스에서 **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**&#x200B;을(를) 클릭합니다.
1. 대상자의 이름을 지정하고 선택적 설명을 추가합니다.
1. **[!UICONTROL Custom]**&#x200B;을(를) 대상 빌더로 끌어서 놓습니다.

   원하는 매개 변수를 선택하려면 다음을 수행하십시오.

   * 대상을 만드는 동안 목록에서 매개 변수 이름을 선택하고, 원하는 매개 변수 이름의 첫 번째 문자를 입력하거나, 원하는 매개 변수 이름의 전체 이름을 입력합니다.
   * mbox 이름은 기억하지만 매개 변수 이름은 기억하지 못하는 경우 [!UICONTROL Filter by] 드롭다운 목록을 사용하여 원하는 매개 변수를 전달하는 알려진 mbox를 필터링하십시오.

   어느 방법을 사용하든 mbox와 매개 변수 간에 링크가 없습니다. 대상자는 해당 매개 변수를 전달하는 모든 mbox에서 매개 변수를 기반으로 작동합니다.

   >[!NOTE]
   >
   >[!UICONTROL Filter By] 드롭다운 목록에서 선택한 mbox는 활동 생성 시 저장되지 않습니다. 이 옵션을 사용하면 선택한 mbox를 기반으로 매개변수를 필터링할 수 있습니다.

   기존 대상을 편집하는 경우 필터링 기준에는 작성 중에 제공된 mbox 이름이 함께 표시됩니다.

1. 평가자를 선택합니다:

   * 다음 포함(대/소문자 구분 안 함)
   * 다음을 포함하지 않음(대/소문자 구분 안 함)
   * 다음과 같음
   * 다음과 같지 않음
   * 다음보다 큼
   * 다음보다 크거나 같음
   * 다음보다 작음
   * 다음보다 작거나 같음
   * 매개 변수가 있음
   * 매개 변수가 없습니다.
   * 매개 변수 값이 있음
   * 매개 변수 값이 없음
   * 매개 변수 또는 값이 없음
   * Start with
   * 다음으로 끝남

   ![사용자 지정 매개 변수 대상자](assets/custom.png)

1. 새 라인에 각 값을 입력합니다.
1. (선택 사항) 대상에 대한 추가 규칙을 설정합니다.
1. **[!UICONTROL Done]** 아이콘을 클릭합니다.

대상자의 [정의 세부 정보 팝업 카드](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780)에 **[!UICONTROL Rules]** 섹션에 매개 변수 이름이 표시됩니다. 필터링에 사용된 mbox에 대한 참조가 없습니다.

>[!NOTE]
>
>[!DNL Target] 18.5.1 릴리스(2018년 5월 22일) 이전에 만들어진 사용자 지정 대상의 경우 mbox 이름이 대상의 정의 팝업 카드에 표시되지 않습니다. 사용자 지정 대상을 다시 저장하여 카드에 표시할 mbox 이름을 가져옵니다.

## 고려 사항 {#considerations}

* 대상자 및 활동은 특정 mbox에 대해 평가됩니다. 예를 들어 글로벌 mbox가 특정 매개 변수를 전달하지만 지역 mbox가 전달하지 않으면 해당 매개 변수를 타깃팅하는 활동/대상은 지역 mbox에서 사용할 수 없습니다.
* 타깃팅은 mboxPC, mboxSession, mbox3rdPartyId, mboxMCSDID, mboxMCAVID, mboxMCGVID, mboxCount, mboxId 및 mboxVersion과 같은 내부 mbox 매개 변수에서 평가되지 않습니다.

## 교육 비디오: 대상자 ![튜토리얼 배지](/help/main/assets/tutorial.png) 만들기

다음 비디오에는 대상 카테고리 사용에 대한 정보가 포함되어 있습니다.

* 대상자 만들기
* 대상 카테고리 정의

>[!VIDEO](https://video.tv.adobe.com/v/17392)
