---
keywords: 컨텐츠 보안 정책;csp;at.js;허용 목록;허용 목록에 추가하다 플리커;사전 숨김;사전 숨김;사전 숨김;사전 숨김
description: Adobe Target 사용 시 추가해야 하는 CSP(Content Security Policy) 지시문에 대해 알아봅니다.
title: 방법 [!DNL Target] CSP(콘텐츠 보안 정책)를 처리합니까?
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# 콘텐츠 보안 정책(CSP) 지침

사용 중인 경우 [컨텐츠 보안 정책](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP)를 사용할 수 있습니다 [!DNL Adobe Target] 구현을 사용할 때는 다음 CSP 지시문을 추가해야 합니다 [at.js 2.1 이상](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` with `*.tt.omtrdc.net` 허용 목록에추가된. 네트워크 요청이 [!DNL Target] edge.
* `style-src unsafe-inline` 구문을 사용하는 키-값 쌍으로 전달됩니다. 사전 숨김 및 플리커(깜박임) 제어에 필요합니다.
* `script-src unsafe-inline`.  HTML 오퍼의 일부일 수 있는 JavaScript 실행을 허용하는 데 필요합니다.
