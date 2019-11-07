---
keywords: 콘텐츠 보안 정책;csp;at.js;화이트리스트;깜박임;사전 숨기기;사전 숨기기;사전 숨김;사전 숨김;사전 숨김;사전 숨김;prehiding
description: Adobe Target at.js 2.1 이상을 사용할 때 추가해야 하는 CSP(Content Security Policy) 지시문에 대한 정보입니다.
title: CSP(컨텐츠 보안 정책)
subtopic: 시작하기
topic: Standard
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# CSP(Content Security Policy) 디렉티브

Target 구현에 CSP [를](https://en.wikipedia.org/wiki/Content_Security_Policy) 사용하는 경우 [at.js 2.1 이상을](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)사용할 때 다음 CSP 지시어를 추가해야 합니다.

* `connect-src` 화이트리스트에 `*.tt.omtrdc.net` 추가되었습니다. 네트워크 요청을 [!DNL Target] 가장자리에 허용해야 합니다.
* `style-src unsafe-inline` 구문을 사용하는 키-값 쌍으로 전달됩니다. 미리 숨기기 및 깜박임 컨트롤에 필요합니다.
* `script-src unsafe-inline`.  HTML 오퍼의 일부일 수 있는 JavaScript 실행을 허용하는 데 필요합니다.
