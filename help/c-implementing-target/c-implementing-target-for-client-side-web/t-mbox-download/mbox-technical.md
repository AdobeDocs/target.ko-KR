---
keywords: implementation;mbox.js;dom manipulation library;target.js;visual experience composer;iframe;angular sites;single page applications;single page app;SPA
description: 기술 담당자가 mbox.js 구현과 이 구현이 사이트에 미칠 수 있는 영향을 이해하는 데 도움이 되는 정보입니다.
title: mbox.js가 수행하는 작업
feature: null
subtopic: Getting Started
topic: Standard
uuid: 5529d620-4a33-479c-871f-18dcd59abb07
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 100%

---


# mbox.js가 수행하는 작업{#what-mbox-js-does}

기술 담당자가 mbox.js 구현과 이 구현이 사이트에 미칠 수 있는 영향을 이해하는 데 도움이 되는 정보입니다.

Target Standard에는 [!DNL mbox.js] 버전 58 이상이 필요합니다. [!DNL mbox.js]를 다운로드하고 업데이트하는 방법에 대한 지침은 [Mbox 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420)을 참조하십시오.

Target Standard의 경우 [!DNL mbox.js]는 다른 JavaScript 파일인 [!DNL target.js]를 호출합니다. [!DNL Target.js]는 Adobe에 의해 호스팅되며 Adobe에 의해 자동으로 업데이트됩니다. [!DNL target.js]를 업데이트하기 위해 수행해야 할 작업은 없으며 클라이언트별 사용자 지정 사항도 없습니다.

[!DNL Target.js]는 페이지의 `<head>` 섹션에서 `target-global-mbox`라는 mbox를 만듭니다.

[!DNL Target.js]는 [!DNL mbox.js]의 [!UICONTROL 추가 JavaScript] 필드에 추가된 JavaScript 코드 행에 의해 [!DNL mbox.js]에서 호출됩니다. [!DNL target.js]를 비활성화하는 유일한 방법은 이 코드 행을 포함하지 않는 것으로서, 이렇게 하면 [!DNL Target]을 비활성화하게 됩니다.

[!DNL Target.js]는 [!DNL Target]에서 두 가지 기능이 있습니다.

* DOM 조작
* [!UICONTROL 시각적 경험 작성기]의 시각적 요소 활성화

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

자세한 내용은 [at.js 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17)을 참조하십시오.
