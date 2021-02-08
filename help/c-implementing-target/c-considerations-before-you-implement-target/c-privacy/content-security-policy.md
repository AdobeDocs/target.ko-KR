---
keywords: 컨텐트 보안 정책;csp;at.js;허용 목록;;깜박임;사전 숨기기;사전 숨기기;사전 숨기기;사전 숨기기;prehiding
description: Adobe Target 사용 시 추가해야 하는 CSP(Content Security Policy) 지문에 대해 알아봅니다.
title: Target은 CSP(Content Security Policy)를 어떻게 처리합니까?
feature: Privacy & Security
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# CSP(Content Security Policy) 지시문

[!DNL Adobe Target] 구현에 [컨텐트 보안 정책](https://en.wikipedia.org/wiki/Content_Security_Policy)(CSP)을 사용하는 경우 [at.js 2.1 이상](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)을 사용할 때 다음 CSP 지시문을 추가해야 합니다.

* `connect-src`  `*.tt.omtrdc.net` 허용 목록에추가된. 네트워크 요청을 [!DNL Target] 가장자리에 허용해야 합니다.
* `style-src unsafe-inline` 구문을 사용하는 키-값 쌍으로 전달됩니다. 사전 숨기기 및 깜박임 컨트롤에 필요합니다.
* `script-src unsafe-inline`.  HTML 오퍼의 일부일 수 있는 JavaScript 실행을 허용하는 데 필요합니다.
