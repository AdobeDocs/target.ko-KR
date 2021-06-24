---
keywords: 구현;mbox.js;dom 조작 라이브러리;target.js;시각적 경험 작성기;iframe;angular 사이트;단일 페이지 애플리케이션;단일 페이지 앱;SPA
description: Adobe Target의 이전 mbox.js 구현에 대해 알아봅니다. Adobe Experience Platform 웹 SDK(AEP 웹 SDK) 또는 최신 at.js 버전으로 마이그레이션합니다.
title: ' [!DNL Target] mbox.js 라이브러리는 무엇을 합니까?'
feature: at.js
role: Developer
exl-id: 62f0cbd2-17f0-43f4-98d3-ea39f314525e
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 78%

---

# mbox.js가 수행하는 작업

기술 담당자가 mbox.js 구현과 이 구현이 사이트에 미칠 수 있는 영향을 이해하는 데 도움이 되는 정보입니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js로부터의 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 미칩니다.
>
>이 날짜 이전에 모든 고객이 사이트에서 발생할 수 있는 문제를 방지하기 위해 새로운 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

## DOM 조작 {#section_169F8D4C077948DCB4F891ABBB03FF63}

[!DNL Target.js]는 Standard에서 사용하는 DOM 조작 라이브러리를 제어합니다. 웹 사이트의 컨텐츠를 표시하기 위해 [!DNL target.js]는 [!DNL sizzle.js] (버전1.10.8-pre)를 참조합니다. [!DNL Sizzle.js]는 HTML 요소 선택기를 활성화합니다. [!DNL sizzle.js] 이외에는 기본 JavaScript만 사용됩니다. jquery는 필요하지 않습니다.

또한 DOM을 폴링하는 데에는 다음 코드 조각이 사용됩니다.
`https://github.com/dperini/ContentLoaded`

## Target.js 및 시각적 경험 작성기 {#section_2B3FF6AC5B8D431C83D9EDCF53CB1472}

[!UICONTROL 시각적 경험 작성기]를 사용하여 활동에 대한 경험을 설정하면 웹 페이지가 iFrame으로 열립니다. iFrame이 로드되면 Standard에서는 HTML5 `postMessage` API 호출을 전송합니다. [!DNL Target.js]는 모든 `postMessage` 호출을 감지하고 웹 사이트에 다음 JavaScript 라이브러리를 포함합니다.

* 썸네일 생성용: [!DNL https://html2canvas.hertzen.com/]
* 도메인 간 쿼리용: [!DNL Admin.js], [!DNL CDQ.base.js], [!DNL CDQ.host.js], [!DNL admin.css] (여러 iFrame 간 메시지 전송에 사용됨). 이 스크립트들을 사용하면 Adobe에서 페이지 간에 데이터를 전송할 수 있습니다.

## Angular 사이트 및 단일 페이지 애플리케이션에 대한 고려 사항 {#section_16D76F16077A434FAE8CEC6FD43BE6D7}

Angular 사이트 또는 단일 페이지 애플리케이션(SPA)에서 Target을 구현하는 경우 mbox.js 대신at.js 라이브러리를 사용해야 합니다.
