---
keywords: 구현;구현;at.js;adobe experience platform 웹 sdk;aep 웹 sdk
description: Adobe 구현 방법 알아보기 [!DNL Target] for client-side web using the Adobe Experience Platform Web SDK  (AEP Web SDK) or the [!DNL Target] at.js JavaScript 라이브러리.
title: 구현 방법 [!DNL Target] 클라이언트측 웹용
feature: at.js
role: Developer
exl-id: 34c1e39b-acae-4547-b67f-584bcd59913f
source-git-commit: bef2b493e8964f468d4f766c932a96d32e994a03
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 47%

---

# 개요: 구현 [!DNL Target] 클라이언트측 웹용

클라이언트측 [!DNL Adobe Target]의 구현에서 [!DNL Target]은 활동과 연관된 경험을 클라이언트 브라우저에 직접 전달합니다. 브라우저는 표시할 경험을 결정하고 표시합니다. 클라이언트측 구현에서는 WYSIWYG 편집기, [시각적 경험 작성기](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) 또는 [양식 기반 경험 작성기](/help/c-experiences/form-experience-composer.md)인 비시각적 인터페이스를 사용하여 활동 및 개인화 경험을 만들 수 있습니다.

구현하려면 [!DNL Adobe Target] 클라이언트측: 다음 JavaScript 라이브러리 중 하나를 사용해야 합니다.

* [Adobe Experience Platform 웹 SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [at.js JavaScript 라이브러리 Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js에서 발송된 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 줍니다. 모든 고객은 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하여 사이트에 문제가 발생하지 않도록 하는 것이 좋습니다.
>
>* **Adobe Experience Platform Web SDK**: 다음 [!UICONTROL Adobe Experience Platform Web SDK] 에서는 [!DNL Experience Cloud] (포함) [!DNL Target]) 내의 아무 곳에나 삽입할 수 있습니다. 로 마이그레이션하도록 선택하는 경우 [!DNL Adobe Experience Platform Web SDK]를 참조하십시오. [Adobe Experience Platform Web SDK란?](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) 에서 *웹 SDK 안내서*.
>
>* **at.js**: at.js JavaScript 라이브러리는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 보안을 강화하고, 단일 페이지 애플리케이션에 대해 더 나은 구현 옵션을 제공합니다. at.js로 마이그레이션하도록 선택하는 경우 다음을 참조하십시오 [At.js 작동 방식](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target Skill Builder: 개발자 채팅, Adobe Target의 mbox.js를 at.js로 마이그레이션](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).


