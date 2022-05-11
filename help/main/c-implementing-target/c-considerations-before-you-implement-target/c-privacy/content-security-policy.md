---
keywords: 콘텐츠 보안 정책;CSP;at.js;화이트리스트;플리커;사전 숨기기;사전 숨기기;사전 숨기기
description: Adobe Target을 사용할 때 추가해야 하는 콘텐츠 보안 정책(CSP) 지침에 대해 알아봅니다.
title: ' [!DNL Target] 은 콘텐츠 보안 정책(CSP)을 어떻게 처리합니까?'
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: db632225d21c2e061e82269bec168341b410575a
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 29%

---

# 콘텐츠 보안 정책(CSP) 지침

[!DNL Adobe Target] 구현에 [콘텐츠 보안 정책](https://en.wikipedia.org/wiki/Content_Security_Policy)(CSP)을 사용하는 경우 [at.js 2.1 이상 버전](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)을 사용할 때 다음과 같은 CSP 지침을 추가해야 합니다.

* `*.tt.omtrdc.net` 허용 목록이 포함된 `connect-src` [!DNL Target] 에지로의 네트워크 요청을 수락하기 위해 필요합니다.
* `style-src unsafe-inline` 사전 숨기기 및 플리커 제어에 필요합니다.
* `script-src unsafe-inline`.  HTML 오퍼의 일부일 수 있는 JavaScript 실행을 허용하기 위해 필요합니다.

## FAQ

보안 정책에 대한 다음 FAQ를 참조하십시오.

### CORS(Cross Origin Resource Sharing) 및 Flash 도메인 간 정책이 보안 문제를 제시합니까?

CORS 정책을 구현하는 데 권장되는 방법은 신뢰할 수 있는 도메인허용 목록에 추가하다를 통해 신뢰할 수 있는 원본에만 액세스할 수 있도록 하는 것입니다. 도메인 간 Flash 정책에도 동일하게 적용될 수 있습니다. 일부 [!DNL Adobe Target] 고객은 의 도메인에 대해 와일드카드 문자를 사용하는 것에 대해 우려하고 있습니다 [!DNL Target]. 문제는 사용자가 애플리케이션에 로그인되어 정책에 의해 허용되는 도메인을 방문하는 경우, 해당 도메인에서 실행되는 모든 악성 콘텐츠는 잠재적으로 응용 프로그램에서 중요한 컨텐츠를 검색하고 로그인한 사용자의 보안 컨텍스트 내에서 작업을 수행할 수 있다는 것입니다. 일반적으로 이것을 CSRF(Cross-Site Request Forgery)라고 합니다.

에서 [!DNL Adobe Target] 그러나 이러한 정책이 보안 문제를 나타내지는 않습니다.

adobe.tt.omtrdc.net&quot;은 Adobe 소유 도메인입니다. [!DNL Adobe Target] 는 테스트 및 개인화 도구이며 [!DNL Target] 인증 없이 어디에서나 요청을 받고 처리할 수 있습니다. 이러한 요청에는 A/B 테스트, 권장 사항 또는 콘텐츠 개인화에 사용되는 키/값 쌍이 포함되어 있습니다.

[!DNL Adobe] 는 PII(개인 식별 정보) 또는 [!DNL Adobe Target] edge server. 여기서 &quot;adobe.tt.omtrdc.net&quot;은

...할 것으로 예상된다 [!DNL Target] 는 JavaScript 호출을 통해 모든 도메인에서 액세스할 수 있습니다. 이 액세스를 허용하는 유일한 방법은 와일드카드와 함께 &quot;Access-Control-Allow-Origin&quot;을 활용하는 것입니다.
