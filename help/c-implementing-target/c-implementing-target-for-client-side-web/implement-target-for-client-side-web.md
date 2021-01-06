---
keywords: implement;implementation;at.js;adobe experience platform web sdk;aep web sdk
description: 클라이언트측 웹용 Adobe Target 구현에 대한 정보입니다.
title: 클라이언트측 웹용 Adobe Target 구현
feature: client-side
translation-type: tm+mt
source-git-commit: 1b426e0b2004e729ba75d218a9b6ccd5195449cd
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 66%

---


# 개요: 클라이언트측 웹용 Target 구현

클라이언트측 [!DNL Adobe Target]의 구현에서 [!DNL Target]은 활동과 연관된 경험을 클라이언트 브라우저에 직접 전달합니다. 브라우저는 표시할 경험을 결정하고 표시합니다. 클라이언트측 구현에서는 WYSIWYG 편집기, [시각적 경험 작성기](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) 또는 [양식 기반 경험 작성기](/help/c-experiences/form-experience-composer.md)인 비시각적 인터페이스를 사용하여 활동 및 개인화 경험을 만들 수 있습니다.

[!DNL Adobe Target] 클라이언트측을 구현하려면 [Adobe Experience Platform 웹 SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html), [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 또는 mbox.js 라이브러리를 사용해야 합니다.

>[!NOTE]
>
>mbox.js 라이브러리는 더 이상 개발되지 않습니다. 모든 고객은 [AEP 웹 SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html), [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md) 또는 [mbox.js에서 at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md)로 마이그레이션을 배포해야 합니다.
