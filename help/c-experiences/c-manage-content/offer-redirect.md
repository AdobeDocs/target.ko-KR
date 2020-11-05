---
keywords: redirect offer;create redirect offer;add html offer;Pass all URL parameters in redirect;Pass mboxSessionId in redirect (only needed when the redirect is going to a different domain)
description: 브라우저가 새 페이지로 리디렉션되는 Adobe Target의 리디렉션 오퍼에 대한 정보입니다.
title: 리디렉션 오퍼 만들기
feature: offers
topic: Standard
uuid: 54336965-a26e-47c3-b3bc-079d3573502a
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 96%

---


# 리디렉션 오퍼 만들기{#create-redirect-offers}

리디렉션 오퍼가 발생하면 브라우저가 새 페이지로 리디렉션됩니다.

한 페이지 내의 컨텐츠 일부만 변경하는 대신, 완전히 다른 두 페이지를 테스트할 수 있습니다. 이 경우 A/B 테스트는 페이지 A 및 페이지 B를 비교합니다. 두 가지 경험인 기본 페이지 A를 가리키는 경험과 페이지 B로 리디렉션되는 경험을 사용하여 A/B 테스트 캠페인을 설정합니다. 오퍼는 방문자를 다른 페이지로 리디렉션하도록 구성됩니다.

>[!NOTE]
>
>ajax mbox에서 리디렉션 오퍼를 사용할 수 없습니다(`mboxUpdate`).
>
>A4T를 사용하는 활동의 리디렉션 오퍼에 대해서는 구현이 특정 최소 요구 사항을 충족해야 합니다. 또한 사용자가 알아야 하는 중요한 정보도 있습니다. 자세한 내용은 [리디렉션 오퍼 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905)를 참조하십시오.

리디렉션하는 경험을 설정하는 방법에 대한 자세한 내용은 [URL로 리디렉션](/help/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA)을 참조하십시오.

리디렉션 오퍼는 JavaScript 코드를 실행하여 브라우저를 리디렉션합니다. `window.location.replace();` 메서드를 사용하므로 방문자를 리디렉션하는 페이지는 브라우저 기록에 저장되지 않습니다. 방문자는 여전히 브라우저에서 뒤로 단추를 사용할 수 있습니다.

>[!NOTE]
>
>랜딩 페이지의 레퍼러 값을 전달하려면 리디렉션 오퍼보다는 HTML 오퍼를 사용하는 것이 좋습니다.

**리디렉션 오퍼를 만들려면:**

1. **[!UICONTROL 오퍼]**&#x200B;를 클릭한 다음, **[!UICONTROL 코드 오퍼]** 탭을 선택합니다.
1. Click **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.
1. 오퍼 이름을 입력합니다.
1. 재지정할 고유 컨텐츠 또는 대상의 URL을 입력하십시오. 절대 URL을 사용해야 합니다.

   >[!NOTE]
   >
   >리디렉션 URL에서도 사용자에게 동일한 활동의 자격을 부여하는 경우 리디렉션 오퍼는 무한 루프를 유발합니다. 사용자가 리디렉션된 후에 활동의 자격을 다시 부여받지 않도록 해야 합니다.

1. 원하는 옵션을 선택하여 리디렉션 오퍼를 사용자 지정합니다. 

* **모든 URL 매개 변수 포함:** 이전 페이지에 있는 모든 URL 매개 변수를 리디렉션된 페이지에 전파하려면 이 확인란을 선택합니다.

   예를 들어, 남성 페이지에서 남성 셔츠 카테고리 페이지로 사람들을 직접 리디렉션하려고 할 수 있습니다. 사람들이 자신의 사이트에 이메일, 배너 광고, 검색 광고를 통해 도달했는지 아니면 구조적으로 도달했는지를 추적하는 방법으로서 URL의 동적 매개 변수를 전달하고자 할 수도 있습니다. 이 확인란을 선택하면, URL 상자에 입력한 내용이 [!DNL `https://www.mycompany.com/mens.html?emailId=123`]일 때 [!DNL `https://www.mycompany.com/mensShirts.html?emailId=123`]페이지의 리디렉션 오퍼가 자동으로 [!DNL `https://www.mycompany.com/mensShirts.html`]이 됩니다.

* **mbox 세션 ID 전달(다른 도메인으로 리디렉션하는 데 필요):** `sessionId`를 리디렉션에 자동으로 포함시키려면 이 확인란을 선택하십시오. 이것은 이메일에서의 클릭이나 한 도메인에서 다른 도메인으로의 클릭을 테스트할 때에만 필요합니다. `sessionId`를 사용하여 방문자의 쿠키가 일치하는지 확인하므로, 방문자를 계속 추적할 수 있고 적절한 컨텐츠가 표시됩니다.

   자사 및 타사 쿠키 설정을 사용하는 경우에는 도메인 간에 이동할 때 mbox 세션 ID를 전달할 필요가 없습니다. 타사 쿠키에서 지속되므로 URL에는 필요하지 않습니다.

>[!NOTE]
>
>이 테스트를 실행하기 전에 담당 구현 컨설턴트에게 문의하십시오.

## 교육 비디오:컨텐츠 저장소(4:56) ![개요 배지](/help/assets/overview.png)

이 비디오에는 컨텐츠 관리에 대한 정보가 포함되어 있습니다.

* [Experience Cloud 자산 라이브러리](https://docs.adobe.com/content/help/en/core-services/interface/assets/creative-cloud.html)와 Target 컨텐츠 라이브러리 간 연결
* 사용자 지정 HTML 오퍼
* 시각적 경험 작성기의 사용자 지정 HTML 오퍼

>[!VIDEO](https://video.tv.adobe.com/v/17387)
