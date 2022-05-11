---
keywords: 콘텐츠 보안 정책;CSP;at.js;화이트리스트;플리커;사전 숨기기;사전 숨기기;사전 숨기기
description: Adobe Target을 사용할 때 추가해야 하는 콘텐츠 보안 정책(CSP) 지침에 대해 알아봅니다.
title: ' [!DNL Target] 은 콘텐츠 보안 정책(CSP)을 어떻게 처리합니까?'
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: ht
source-wordcount: '97'
ht-degree: 100%

---

# 콘텐츠 보안 정책(CSP) 지침

[!DNL Adobe Target] 구현에 [콘텐츠 보안 정책](https://en.wikipedia.org/wiki/Content_Security_Policy)(CSP)을 사용하는 경우 [at.js 2.1 이상 버전](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)을 사용할 때 다음과 같은 CSP 지침을 추가해야 합니다.

* `*.tt.omtrdc.net` 허용 목록이 포함된 `connect-src` [!DNL Target] 에지로의 네트워크 요청을 수락하기 위해 필요합니다.
* `style-src unsafe-inline` 사전 숨기기 및 플리커 제어에 필요합니다.
* `script-src unsafe-inline`.  HTML 오퍼의 일부일 수 있는 JavaScript 실행을 허용하기 위해 필요합니다.
