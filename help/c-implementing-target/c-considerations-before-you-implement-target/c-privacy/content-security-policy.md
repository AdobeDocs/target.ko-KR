---
keywords: content security policy;csp;at.js;whitelist;allowlist;flicker;pre-hide;pre-hiding;prehiding
description: Adobe Target at.js 2.1 이상 버전을 사용할 때 추가해야 하는 CSP(Content Security Policy) 지시문에 대한 정보입니다.
title: CSP(컨텐츠 보안 정책)
feature: privacy and security
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# CSP(Content Security Policy) 지시문

Target 구현에 CSP( [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) )를 사용하는 경우 [at.js 2.1 이상 버전을 사용할 때 다음 CSP 지시문](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)을 추가해야 합니다.

* `connect-src` Adobe `*.tt.omtrdc.net` 와 허용 목록에추가된 함께. 네트워크 요청을 [!DNL Target] 에지 대상으로 허용해야 합니다.
* `style-src unsafe-inline` 구문을 사용하는 키-값 쌍으로 전달됩니다. 미리 숨김 및 깜박임 컨트롤에 필요합니다.
* `script-src unsafe-inline`.  HTML 오퍼의 일부일 수 있는 JavaScript 실행을 허용해야 합니다.
