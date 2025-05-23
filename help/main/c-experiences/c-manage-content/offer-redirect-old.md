---
keywords: 리디렉션 오퍼;리디렉션 오퍼 만들기;html 오퍼 추가;리디렉션에서 모든 URL 매개 변수 전달;리디렉션에서 mboxSessionId 전달(리디렉션이 다른 도메인으로 진행될 경우에만 필요함)
description: ' [!DNL Target]  Adobe에서 리디렉션 오퍼를 만들어 브라우저가 새 페이지로 리디렉션하는 방법을 알아봅니다.'
title: 리디렉션 오퍼를 만들려면 어떻게 합니까?
feature: Experiences and Offers
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 45%

---

# 리디렉션 오퍼 만들기

[!DNL Adobe Target]에서 리디렉션 오퍼를 사용하면 브라우저가 새 페이지로 리디렉션됩니다.

한 페이지 내의 컨텐츠 일부만 변경하는 대신, 완전히 다른 두 페이지를 테스트할 수 있습니다. 이 경우 A/B 테스트는 페이지 A와 페이지 B를 비교합니다. 하나는 기본 페이지 A를 가리키고 다른 하나는 페이지 B로 리디렉션되는 두 가지 경험이 있는 A/B 테스트 활동을 설정합니다. 오퍼가 방문자를 다른 페이지로 리디렉션하도록 구성되었습니다.

>[!NOTE]
>
> * 리디렉션 오퍼는 [!UICONTROL Offers] > [!UICONTROL Code Offers] 페이지 또는 [Forms 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)에서 만들 수 있습니다. VEC(시각적 경험 작성기)에서는 리디렉션 오퍼를 만들거나 적용할 수 없습니다. [!DNL Target] 요청 위치에 콘텐츠가 삽입되므로 이는 전역 [!DNL Target] 요청에 적합하지 않을 수 있습니다.
>
>* ajax mbox(`mboxUpdate`)에서는 리디렉션 오퍼를 사용할 수 없습니다.
>
>* A4T를 사용하는 활동의 리디렉션 오퍼에 대해서는 구현이 특정 최소 요구 사항을 충족해야 합니다. 또한 사용자가 알아야 하는 중요한 정보도 있습니다. 자세한 내용은 [리디렉션 오퍼 - A4T FAQ](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905)를 참조하십시오.
>
>* 리디렉션하는 경험을 설정하는 방법에 대한 자세한 내용은 [URL로 리디렉션](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA)을 참조하십시오.

리디렉션 오퍼는 JavaScript 코드를 실행하여 브라우저를 리디렉션합니다. `window.location.replace();` 메서드를 사용하므로 방문자를 리디렉션하는 페이지는 브라우저 기록에 저장되지 않습니다. 방문자는 여전히 브라우저에서 뒤로 단추를 사용할 수 있습니다.

>[!NOTE]
>
>랜딩 페이지의 레퍼러 값을 전달하려면 리디렉션 오퍼보다는 HTML 오퍼를 사용하는 것이 좋습니다.

## 코드 오퍼 페이지에서 리디렉션 오퍼 만들기

1. **[!UICONTROL Offers]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Code Offers]** 탭을 선택합니다.

   ![코드 오퍼 탭](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**&#x200B;을(를) 클릭합니다.

   ![리디렉션 오퍼 만들기 대화 상자](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. 오퍼에 대해 수사적 이름을 지정합니다.

   수사적 이름을 사용하면 나와 다른 사용자가 Assets 라이브러리에서 오퍼를 빠르게 찾을 수 있습니다.

1. 재지정할 고유 컨텐츠 또는 대상의 URL을 입력하십시오. 절대 URL을 사용해야 합니다.

   >[!NOTE]
   >
   >리디렉션 URL에서도 사용자에게 동일한 활동의 자격을 부여하는 경우 리디렉션 오퍼는 무한 루프를 유발합니다. 사용자가 리디렉션된 후에 활동의 자격을 다시 부여받지 않도록 해야 합니다.

1. 원하는 옵션을 선택하여 리디렉션 오퍼를 사용자 지정합니다. 

   * **모든 URL 매개 변수 포함:** 이전 페이지에 있는 모든 URL 매개 변수를 리디렉션된 페이지에 전파하려면 토글을 밀어 이 옵션을 사용하도록 설정합니다.

     예를 들어, 남성 페이지에서 남성 셔츠 카테고리 페이지로 사람들을 직접 리디렉션하려고 할 수 있습니다. 사람들이 자신의 사이트에 이메일, 배너 광고, 검색 광고를 통해 도달했는지 아니면 구조적으로 도달했는지를 추적하는 방법으로서 URL의 동적 매개 변수를 전달하고자 할 수도 있습니다. 이 옵션을 활성화하면 URL 상자에 입력한 내용이 `https://www.mycompany.com/mensShirts.html`일 때 `https://www.mycompany.com/mens.html?emailId=123` 페이지의 리디렉션 오퍼가 자동으로 `https://www.mycompany.com/mensShirts.html?emailId=123`이(가) 됩니다.

   * **mbox 세션 ID 전달:** 다른 도메인으로 리디렉션하는 데 필요합니다. `sessionId`을(를) 리디렉션에 자동으로 포함하려면 토글을 밀어 이 옵션을 사용하도록 설정합니다. 이메일에서의 클릭이나 한 도메인에서 다른 도메인으로의 클릭을 테스트할 때만 필요합니다. `sessionId`를 사용하여 방문자의 쿠키가 일치하는지 확인하므로, 방문자를 계속 추적할 수 있고 적절한 컨텐츠가 표시됩니다.

     퍼스트 파티 및 타사 쿠키 설정을 사용하는 경우 도메인을 교차할 때 mbox 세션 ID를 전달할 필요가 없습니다. 타사 쿠키에서 지속되므로 URL에는 필요하지 않습니다.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

>[!NOTE]
>
>이 테스트를 실행하기 전에 담당 구현 컨설턴트에게 문의하십시오.

## 양식 기반 경험 작성기를 사용하여 리디렉션 오퍼 만들기

1. [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 사용하여 활동을 만드는 동안 **[!UICONTROL Content]** 섹션을 표시할 위치를 선택하십시오.

   양식 기반 경험 작성기의 ![콘텐츠 섹션](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. **[!UICONTROL Default Content]** 드롭다운 목록을 클릭한 다음 **[!UICONTROL Change Redirect Offer]**&#x200B;을(를) 클릭합니다.

   ![리디렉션 오퍼 옵션 변경](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**&#x200B;을(를) 클릭합니다.

   ![리디렉션 오퍼 만들기 대화 상자](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. 오퍼에 대해 수사적 이름을 지정합니다.

   수사적 이름을 사용하면 나와 다른 사용자가 Assets 라이브러리에서 오퍼를 빠르게 찾을 수 있습니다.

1. 재지정할 고유 컨텐츠 또는 대상의 URL을 입력하십시오. 절대 URL을 사용해야 합니다.

   >[!NOTE]
   >
   >리디렉션 URL에서도 사용자에게 동일한 활동의 자격을 부여하는 경우 리디렉션 오퍼는 무한 루프를 유발합니다. 사용자가 리디렉션된 후에 활동의 자격을 다시 부여받지 않도록 해야 합니다.

1. 원하는 옵션을 선택하여 리디렉션 오퍼를 사용자 지정합니다. 

   * **모든 URL 매개 변수 포함:** 이전 페이지에 있는 모든 URL 매개 변수를 리디렉션된 페이지에 전파하려면 토글을 밀어 이 옵션을 사용하도록 설정합니다.

     예를 들어, 남성 페이지에서 남성 셔츠 카테고리 페이지로 사람들을 직접 리디렉션하려고 할 수 있습니다. 사람들이 자신의 사이트에 이메일, 배너 광고, 검색 광고를 통해 도달했는지 아니면 구조적으로 도달했는지를 추적하는 방법으로서 URL의 동적 매개 변수를 전달하고자 할 수도 있습니다. 이 옵션을 활성화하면 URL 상자에 입력한 내용이 `https://www.mycompany.com/mensShirts.html`일 때 `https://www.mycompany.com/mens.html?emailId=123` 페이지의 리디렉션 오퍼가 자동으로 `https://www.mycompany.com/mensShirts.html?emailId=123`이(가) 됩니다.

   * **mbox 세션 ID 전달:** 다른 도메인으로 리디렉션하는 데 필요합니다. `sessionId`을(를) 리디렉션에 자동으로 포함하려면 토글을 밀어 이 옵션을 사용하도록 설정합니다. 이메일에서의 클릭이나 한 도메인에서 다른 도메인으로의 클릭을 테스트할 때만 필요합니다. `sessionId`를 사용하여 방문자의 쿠키가 일치하는지 확인하므로, 방문자를 계속 추적할 수 있고 적절한 컨텐츠가 표시됩니다.

     퍼스트 파티 및 타사 쿠키 설정을 사용하는 경우 도메인을 교차할 때 mbox 세션 ID를 전달할 필요가 없습니다. 타사 쿠키에서 지속되므로 URL에는 필요하지 않습니다.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

>[!NOTE]
>
>이 테스트를 실행하기 전에 담당 구현 컨설턴트에게 문의하십시오.

## 활동에서 리디렉션 오퍼 사용

[!UICONTROL Form-Based Experience Composer]을(를) 사용하여 리디렉션 오퍼를 적용해야 합니다. 현재 VEC를 사용하여 리디렉션 오퍼를 적용할 수 없습니다.

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer]은(는) 시각적 경험 작성기가 사용이 불가능하거나 실용적이지 않을 때 [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL Recommendations] 활동에 사용할 경험을 만드는 데 유용한 시각적이지 않은 경험 및 오퍼 만들기 인터페이스입니다. 예를 들어 [!UICONTROL Form-Based Experience Composer]을(를) 사용하여 리디렉션 오퍼를 사용하는 경험을 만들 수 있습니다.

1. [!UICONTROL Form-Based Experience Composer]에서 활동을 만들거나 편집합니다.

   자세한 단계별 지침은 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 참조하십시오.

1. 원하는 위치를 지정하고 필요에 따라 대상 세분화를 추가합니다.

1. **[!UICONTROL Content]** 섹션에서 드롭다운 목록을 클릭한 다음 **[!UICONTROL Change Redirect Offer]**&#x200B;을(를) 클릭합니다.

   ![리디렉션 오퍼 옵션 변경](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. [!UICONTROL Select Remote Offer] 대화 상자에서 원하는 리디렉션 오퍼를 선택한 다음 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

1. 활동 구성을 완료합니다.

## 교육 비디오: 양식 기반 작성기 ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오는 리디렉션 오퍼를 만드는 데 사용할 수 있는 양식 기반 작성기 데모를 제공합니다.

* 양식 기반 경험 작성기를 사용하여 활동 만들기
* 언제 양식 기반 경험 작성기를 사용하고 언제 시각적 경험 작성기를 사용할지 이해
* 개선을 통해 위치 타깃팅

>[!VIDEO](https://video.tv.adobe.com/v/17390)
