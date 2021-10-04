---
keywords: 사용자 지정 매개 변수;타겟 사용자 지정 매개 변수;targetpageparams;타깃팅 mbox 매개 변수
description: 대상에서 사용할 [!DNL Adobe Target] 에 사용자 지정 매개 변수를 전달하는 방법을 알아봅니다.
title: 사용자 지정 매개 변수를 기준으로 방문자를 Target 할 수 있습니까?
feature: Audiences
exl-id: f0669888-6b9e-4738-9ed4-0418ea56fffa
source-git-commit: b74cccdc43c34367819ed8a908a304b567d7ecbb
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 42%

---

# 사용자 지정 매개 변수

사용자 지정 매개 변수는 [!DNL Adobe Target]의 mbox 매개 변수입니다. 임의의 mbox 매개 변수를 mbox에 전달하거나 `targetPageParams` 함수를 사용하는 경우 이러한 매개 변수는 대상자에서 사용할 수 있도록 여기에 표시됩니다.

자세한 내용은 [글로벌 mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md)에 매개 변수 전달 을 참조하십시오.

mbox 매개 변수를 기반으로 하여 사용자 지정 대상을 작성할 때 `mboxParameter`에 대해 묻는 메시지가 `mboxName`에 더 이상 표시되지 않습니다. 이제 mbox 이름은 선택 사항입니다. 따라서 여러 mbox의 매개 변수를 사용하거나 가장자리에 아직 기록되지 않은 매개 변수를 참조할 수 있습니다.

1. [!DNL Target] 인터페이스에서 **[!UICONTROL 대상자]** > **[!UICONTROL 대상자 만들기]**&#x200B;를 클릭합니다.
1. 대상자의 이름을 지정하고 선택적 설명을 추가합니다.
1. **[!UICONTROL 사용자 지정]**&#x200B;을 Audience Builder로 끌어다 놓습니다.

   원하는 매개 변수를 선택하려면 다음을 수행하십시오.

   * 대상을 만드는 동안 목록에서 매개 변수 이름을 선택하고, 원하는 매개 변수 이름의 첫 번째 문자를 입력하거나, 원하는 매개 변수 이름의 전체 이름을 입력합니다.
   * mbox 이름은 기억하지만 매개 변수 이름은 기억하지 못하는 경우 [!UICONTROL 필터 기준] 드롭다운 목록을 사용하여 원하는 매개 변수를 전달하는 알려진 mbox를 필터링하십시오.

   어느 방법을 사용하든 mbox와 매개 변수 간에 링크가 없습니다. 대상은 해당 매개 변수를 전달하는 모든 mbox의 매개 변수를 기반으로 작동합니다.

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
   * 매개 변수 값이 없습니다.
   * 매개 변수 또는 값이 없습니다.
   * Start with
   * 다음으로 끝남

   ![사용자 지정 매개 변수 대상](assets/custom.png)

1. 새 라인에 각 값을 입력합니다.
1. (선택 사항) 대상에 대한 추가 규칙을 설정합니다.
1. **[!UICONTROL 완료를 클릭합니다]**.

대상의 [정의 세부 사항 팝업 카드](/help/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780)에 규칙 섹션의 매개 변수 이름이 표시됩니다. **** 필터링에 사용된 mbox에 대한 참조가 없습니다.

>[!NOTE]
>
>[!DNL Target] 18.5.1 릴리스(2018년 5월 22일) 전에 생성된 사용자 지정 대상의 경우 mbox 이름은 대상의 정의 팝업 카드에 표시되지 않습니다. 사용자 지정 대상을 다시 저장하여 카드에 표시할 mbox 이름을 가져올 수 있습니다.

## 고려 사항 {#considerations}

* 대상 및 활동은 특정 mbox에 대해 평가됩니다. 예를 들어 글로벌 mbox가 특정 매개 변수를 전달하지만 지역 mbox가 전달하지 않으면 해당 매개 변수를 타깃팅하는 활동/대상은 지역 mbox에서 사용할 수 없습니다.
* 타깃팅은 mboxPC, mboxSession, mbox3rdPartyId, mboxMCSDID, mboxMCAVID, mboxMCGVID, mboxCount, mboxId 및 mboxVersion과 같은 내부 mbox 매개 변수에서 평가되지 않습니다.

## 교육 비디오: 대상 만들기 ![자습서 배지](/help/assets/tutorial.png)

다음 비디오에는 대상 카테고리 사용에 대한 정보가 포함되어 있습니다.

* 대상자 만들기
* 대상 카테고리 정의

>[!VIDEO](https://video.tv.adobe.com/v/17392)
