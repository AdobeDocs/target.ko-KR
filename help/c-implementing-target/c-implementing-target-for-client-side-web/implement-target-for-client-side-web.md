---
keywords: implement;implementation;at.js;adobe experience platform web sdk;aep web sdk
description: at.js를 사용하여 클라이언트측 웹용 Adobe Target 구현에 대한 정보입니다.
title: 클라이언트측 웹용 Adobe Target 구현
feature: at.js
translation-type: tm+mt
source-git-commit: bffda8c3461998767a002d66fd9340252237ae5d
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 20%

---


# 개요: 클라이언트측 웹용 Target 구현

클라이언트측 [!DNL Adobe Target]의 구현에서 [!DNL Target]은 활동과 연관된 경험을 클라이언트 브라우저에 직접 전달합니다. 브라우저는 표시할 경험을 결정하고 표시합니다. 클라이언트측 구현에서는 WYSIWYG 편집기, [시각적 경험 작성기](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) 또는 [양식 기반 경험 작성기](/help/c-experiences/form-experience-composer.md)인 비시각적 인터페이스를 사용하여 활동 및 개인화 경험을 만들 수 있습니다.

[!DNL Adobe Target] 클라이언트측을 구현하려면 다음 JavaScript 라이브러리 중 하나를 사용해야 합니다.

* [Adobe Experience Platform 웹 SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [Target at.js JavaScript 라이브러리](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리는 더 이상 지원되지  [!DNL Adobe Target] 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다. 사이트에서 발생할 수 있는 문제를 방지하려면 모든 고객이 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다.
>
>* **Adobe Experience Platform 웹 SDK**:Adobe Experience Platform  [!UICONTROL 웹 ] SDK를 사용하면 Adobe Experience Edge Network를  [!DNL Experience Cloud] (포함)에서 다양한 서비스와 상호 작용할  [!DNL Target]수 있습니다. [!DNL Adobe Experience Platform Web SDK]으로 마이그레이션하도록 선택하는 경우 *웹 SDK 안내서*&#x200B;에서 [Adobe Experience Platform 웹 SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)란?을 참조하십시오.
   >
   >
* **at.js**:at.js JavaScript 라이브러리는 mbox.js보다 많은 이점을 제공합니다. 다른 이점 중에서도 at.js는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 보안을 강화하고, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다. at.js로 마이그레이션하도록 선택하는 경우 [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target Skill Builder:개발자 채팅, Adobe Target의 mbox.js를 at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true)로 마이그레이션합니다.
>
>
mbox.js는 현재 지원되지만(2021년 3월 31일까지) 2017년 7월 이후로 이 라이브러리에 기능 업데이트를 제공하지 않았습니다. 모든 고객을 [!UICONTROL Adobe Experience Platform Web SDK] 또는 at.js로 이동하면 엔지니어 및 지원 직원이 새로운 기능을 제공하고 Adobe에서 기대하는 지원을 제공할 수 있게 됩니다.
