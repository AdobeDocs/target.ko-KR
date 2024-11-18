---
keywords: 활동 url;url;다른 url
description: 테스트 페이지를 정의하고 정확한 테스트 디자인을 보장하기 위해 [!UICONTROL Activity URL]을(를) 설정하는 방법에 대해 알아봅니다.
title: A/B 활동의 활동 URL이란 무엇입니까?
feature: A/B Tests
hide: true
hidefromtoc: true
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
source-git-commit: d5bd3b0d7cdf6eb06175a6365da6b8173f76800f
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 40%

---

# 활동 URL

활동 URL은 테스트에 사용되는 페이지를 결정하며 [!DNL Adobe Target]을(를) 사용하여 테스트를 디자인할 때 열립니다.

활동을 만들 때 메시지가 표시되면 활동 URL을 지정하십시오. 전체 URL(`https://` 포함)을 입력한 다음 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>[!DNL Target]은 URL 프로토콜([!DNL https]와 [!DNL http])을 구분하지 않습니다. 따라서 [!DNL `http://www.adobe.com`] 및 [!DNL `https://www.adobe.com`]이(가) 모두 일치합니다.

## 다른 URL 지정

기본적으로 [!UICONTROL Visual Experience Composer]은(는) [시각적 경험 작성기 설정](/help/main/administrating-target/visual-experience-composer-set-up.md)에 지정된 페이지를 엽니다. 활동을 만들 때 다른 페이지를 지정할 수 있습니다.

1. (조건부) [!UICONTROL Visual Experience Composer]이(가) 열린 후에 다른 페이지를 표시하려면 **[!UICONTROL Experiences]** 페이지에서 페이지 상단의 **[!UICONTROL Configure]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Page Delivery]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL URL]** 필드에 URL을 지정하십시오.

1. (조건부) 활동에 페이지 또는 섹션을 추가하려면 **[!UICONTROL Add Rule]**&#x200B;을(를) 클릭합니다.

   추가 규칙은 다음 중 하나를 기반으로 할 수 있습니다.

   * URL
   * 도메인
   * 경로
   * 해시(#) 조각
   * 쿼리
   * mbox 매개 변수
   * 사용자 정의

   추가 규칙은 AND 또는 OR로 활동 URL에 조인할 수 있습니다. 추가하는 모든 규칙은 AND를 사용하여 서로 평가됩니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

<!-- If you entered a URL for a site that does not include the [!DNL Target]s JavaScript code, you cannot select page elements.

By default, the [!UICONTROL Visual Experience Composer] does not allow changes to elements containing JavaScript, such as rotating banners. You can toggle off **[!UICONTROL Render using JavaScript]** if you want to be able to alter those elements using the [!UICONTROL Visual Experience Composer].-->

>[!NOTE]
>
>페이지를 변경한 후에 하나 이상의 경험에 대해 이 URL을 변경하면 해당 경험은 새 페이지를 사용하여 재설정되고 수행한 변경 사항은 손실됩니다.
