---
keywords: mbox 함수
description: mbox.js를 사용하여 구현할 때 사용할 mbox.js 함수 목록입니다.
title: mbox.js 함수
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 59%

---


# mbox.js 함수{#mbox-js-functions}

mbox.js를 사용하여 구현할 때 사용할 mbox.js 함수 목록입니다.

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리는 더 이상 지원되지  [!DNL Adobe Target] 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다.
>
>사이트에서 발생할 수 있는 문제를 방지하려면 모든 고객이 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [개요:클라이언트측 웹](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)에 대한 Target을 구현합니다.

>[!NOTE]
>
>[!DNL at.js]를 사용하는 경우에는 이 메서드가 적용되지 않습니다.

| 메서드 | 참고 |
|--- |--- |
| `mbox.getName()` |  |
| `mbox.getURL()` |  |
| `mbox.getDiv()` | mbox(기본 컨텐츠 또는 오퍼 포함)와 연결된 div를 반환합니다. |
| `mbox.getParameters()` | 두 개의 필드, 이름 및 값이 있는 매개 변수의 배열 |
| `mbox.setOnError()` | 예:<br>`mbox.setOnError(function() { alert(this.getName() +" had error"});` |
| `mbox.setMessage(message)` | 디버그 창에서 메시지를 볼 수 있습니다. |
| `mboxCurrent.activate()` |  |
| `mboxCurrent.cancelTimeout()` |  |
| `mboxCurrent.finalize()` |  |
| `mboxCurrent.getDefaultDiv()` |  |
| `mboxCurrent.getDiv()` | mbox(기본 컨텐츠 또는 오퍼 포함)와 연결된 div를 반환합니다. |
| `mboxCurrent.getEventTimes()` |  |
| `mboxCurrent.getFetcher()` |  |
| `mboxCurrent.getId()` |  |
| `mboxCurrent.getImportName()` |  |
| `mboxCurrent.getName()` |  |
| `mboxCurrent.getOffer()` |  |
| `mboxCurrent.getParameters()` | 두 개의 필드, 이름 및 값이 있는 매개 변수의 배열 . |
| `mboxCurrent.getURL()` |  |
| `mboxCurrent.getURLBuilder()` |  |
| `mboxCurrent.hide()` |  |
| `mboxCurrent.isActivated`() |  |
| `mboxCurrent.load()` |  |
| `mboxCurrent.loaded()` |  |
| `mboxCurrent.setEventTime()` |  |
| `mboxCurrent.setFetcher()` |  |
| `mboxCurrent.setMessage()` |  |
| `mboxCurrent.setMessage(message)` | 디버그 창에 메시지를 표시합니다. |
| `mboxCurrent.setOffer()` |  |
| `mboxCurrent.setOnError()` | 예:<br>`mboxCurrent.setOnError(function(){ alert(this.getName() +" had error"});` |
| `mboxCurrent.setOnLoad()` | 예:<br>`mboxCurrent.setOnLoad(function(){alert(this.getName()+" loaded")});` |
| `mboxCurrent.show()` |  |
| `mboxCurrent.showContent()` |  |
| `mboxFactoryDefault.addOnLoad(action)` | 페이지가 로드될 때 작업이 호출됩니다. |
| `mboxFactoryDefault.getMboxes().each()` | 예:<br>`mboxFactoryDefault.getMboxes().each(function() { alert(mbox.getName()) };` |
| `mboxFactoryDefault.getMboxes().length()` |  |
| `mboxFactoryDefault.getPageId()` |  |
| `mboxFactoryDefault.getPCId().getId()` |  |
| `mboxFactoryDefault.getSessionId().getId()` |  |
| `mboxFactories.get('default').getSessionId()&#x200B;.forceId("1276011116668");` |  |
| `mboxFactories.get('default').getPCId()&#x200B;.forceId("1276011116668");` |  |
| `mboxFactoryDefault.create()` |  |
| `mboxFactoryDefault.disable()` |  |
| `mboxFactoryDefault.enable()` |  |
| `mboxFactoryDefault.get()` |  |
| `mboxFactoryDefault.getCookieManager()` |  |
| `mboxFactoryDefault.getDisableReason()` |  |
| `mboxFactoryDefault.getEllapsedTime()` |  |
| `mboxFactoryDefault.getEllapsedTimeUntil()` |  |
| `mboxFactoryDefault.getMboxes()` | `mboxList`를 반환합니다. |
| `mboxFactoryDefault.getSignaler()` |  |
| `mboxFactoryDefault.getURLBuilder()` |  |
| `mboxFactoryDefault.isAdmin()` |  |
| `mboxFactoryDefault.isDomLoaded()` |  |
| `mboxFactoryDefault.isEnabled()` |  |
| `mboxFactoryDefault.isSupported()` |  |
| `mboxFactoryDefault.limitTraffic()` |  |
| `mboxFactoryDefault.update()` |  |
| `mboxFactoryDefault.getCookieManager()&#x200B;.getCookie("name")//!= null) {` |  |
| `mboxFactoryDefault.getCookieManager()&#x200B;.setCookie(_name,_value, _duration);` |  |