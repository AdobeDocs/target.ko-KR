---
description: mbox.js를 사용하여 구현할 때 사용할 mbox.js 함수 목록입니다.
keywords: mbox 함수
seo-description: mbox.js를 사용하여 구현할 때 사용할 mbox.js 함수 목록입니다.
seo-title: mbox.js 함수
solution: Target
title: mbox.js 함수
uuid: f503bc44-a664-4d09-82dc-80a1198ad9d0
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# mbox.js 함수{#mbox-js-functions}

mbox.js를 사용하여 구현할 때 사용할 mbox.js 함수 목록입니다.

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
| `mboxFactories.get('default').getSessionId()​.forceId("1276011116668");` |  |
| `mboxFactories.get('default').getPCId()​.forceId("1276011116668");` |  |
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
| `mboxFactoryDefault.getCookieManager()​.getCookie("name")//!= null) {` |  |
| `mboxFactoryDefault.getCookieManager()​.setCookie(_name,_value, _duration);` |  |