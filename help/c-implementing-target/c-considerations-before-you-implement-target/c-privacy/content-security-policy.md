---
description: . js 2.1 이상에서 Adobe Target를 사용할 때 추가해야 하는 CSP (Content Security Policy) 지시문에 대한 정보입니다.
keywords: 컨텐트 보안 정책; csp; at. js; 화이트 리스트; 깜박임; pre-hide; 사전 숨기기; Prehiding
seo-description: . js 2.1 이상에서 Adobe Target를 사용할 때 추가해야 하는 CSP (Content Security Policy) 지시문에 대한 정보입니다.
seo-title: CSP (Content Security Policies)
solution: Target
subtopic: 시작하기
title: CSP (Content Security Policy) 지시문
topic: Standard
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# CSP (Content Security Policy) 지시문

Target 구현에 [대한 CSP (Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) ) 를 사용하는 경우. js 2.1 이상에서 사용할 [때 다음 CSP 지침을 추가해야](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)합니다.

* `connect-src` 화이트 리스트 `*.tt.omtrdc.net` 사용 네트워크 요청을 [!DNL Target] Edge에 허용하기 위해 필요합니다.
* `style-src unsafe-inline` 구문을 사용하는 키-값 쌍으로 전달됩니다. 사전 숨기기 및 깜박임 제어에 필요합니다.
* `script-src unsafe-inline`.  HTML 오퍼에 포함될 수 있는 JavaScript 실행을 허용하는 데 필요합니다.
