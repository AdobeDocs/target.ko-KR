---
keywords: 콘텐츠 보안 정책;CSP;at.js;화이트리스트;플리커;사전 숨기기;사전 숨기기;사전 숨기기
description: Adobe Target을 사용할 때 추가해야 하는 콘텐츠 보안 정책(CSP) 지침에 대해 알아봅니다.
title: ' [!DNL Target] 은 콘텐츠 보안 정책(CSP)을 어떻게 처리합니까?'
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 97%

---

# 콘텐츠 보안 정책(CSP) 지침

[!DNL Adobe Target] 구현에 [콘텐츠 보안 정책](https://ko.wikipedia.org/wiki/Content_Security_Policy)(CSP)을 사용하는 경우 [at.js 2.1 이상 버전](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/)을 사용할 때 다음과 같은 CSP 지침을 추가해야 합니다.

* `*.tt.omtrdc.net` 허용 목록이 포함된 `connect-src` [!DNL Target] 에지로의 네트워크 요청을 수락하기 위해 필요합니다.
* `style-src unsafe-inline` 사전 숨기기 및 플리커 제어에 필요합니다.
* `script-src unsafe-inline`.  HTML 오퍼의 일부일 수 있는 JavaScript 실행을 허용하기 위해 필요합니다.

## 자주 묻는 질문 (FAQ)

보안 정책에 대한 다음 FAQ를 참조하십시오.

### CORS(원본 간 리소스 공유) 및 Flash 도메인 간 정책에 보안 문제가 있습니까?

CORS 정책을 구현하는 권장 방법은 신뢰할 수 있는 도메인의 허용 목록을 통해 필요한 신뢰할 수 있는 출처에만 액세스할 수 있도록 허용하는 것입니다. Flash 도메인 간 정책에 대해서도 마찬가지입니다. 일부 [!DNL Adobe Target] 고객은 [!DNL Target]의 도메인에 와일드카드 문자를 사용하는 것에 대해 우려하고 있습니다. 우려되는 것은 사용자가 애플리케이션에 로그인하여 정책에 의해 허용된 도메인을 방문하는 경우 해당 도메인에서 실행 중인 모든 악성 콘텐츠가 애플리케이션에서 민감한 콘텐츠를 검색하고 로그인한 사용자의 보안 컨텍스트에서 작업을 수행할 가능성이 있다는 것입니다. 이를 일반적으로 CSRF(크로스 사이트 요청 위조)라고 합니다.

그러나 [!DNL Adobe Target] 구현에서 이러한 정책은 보안 문제를 나타내서는 안 됩니다.

“adobe.tt.omtrdc.net”은 Adobe 소유 도메인입니다. [!DNL Adobe Target]은 테스트 및 개인화 도구이며 [!DNL Target]은 인증 없이 어디에서나 요청을 수신하고 처리할 수 있습니다. 이러한 요청에는 A/B 테스트, 권장 사항 또는 콘텐츠 개인화에 사용되는 키/값 쌍이 포함되어 있습니다.

[!DNL Adobe]은 “adobe.tt.omtrdc.net”이 가리키는 [!DNL Adobe Target] 에지 서버에 PII(개인 식별 정보) 또는 기타 민감한 정보를 저장하지 않습니다.

JavaScript 호출을 통해 모든 도메인에서 [!DNL Target]에 액세스할 수 있습니다. 이 액세스를 허용하는 유일한 방법은 와일드 카드로 “Access-Control-Allow-Origin”을 활용하는 것입니다.
