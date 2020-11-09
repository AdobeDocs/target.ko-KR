---
keywords: implement;implementing;setting up;setup;page parameter;tomcat;url encoded;in-page profile attribute;mbox parameter;in-page profile attributes;script profile attribute;bulk profile update API;single file update API;customer attributes;data providers;dataprovider;data provider
description: 페이지 매개 변수, 인페이지 프로필 속성, 스크립트 프로필 속성, 데이터 공급자, 벌크 프로필 업데이트 API, 단일 프로필 업데이트 API 및 고객 속성을 비롯하여 데이터를 Target에 가져오는 데 사용할 수 있는 다양한 방법에 대한 정보입니다.
title: 데이터를 Target에 가져오는 방법
feature: implementation general
subtopic: Getting Started
topic: Standard
uuid: a6d64e39-6cdc-49fe-afe5-ecf7dcacf97d
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '1936'
ht-degree: 97%

---


# 데이터를 Target에 가져오는 방법{#methods-to-get-data-into-target}

페이지 매개 변수, 인페이지 프로필 속성, 스크립트 프로필 속성, 데이터 공급자, 벌크 프로필 업데이트 API, 단일 프로필 업데이트 API 및 고객 속성을 비롯하여 데이터를 Target에 가져오는 데 사용할 수 있는 다양한 방법에 대한 정보입니다.

## 페이지 매개 변수(&quot;mbox 매개 변수&quot;라고도 함){#section_5A297816173C4FE48DC4FE03860CB42B}

페이지 매개 변수는 나중에 사용할 수 있도록 방문자 프로필에 저장되지 않은 페이지 코드를 통해 직접 전달된 이름/값 쌍입니다.

페이지 매개 변수는 나중에 타깃팅 용도로 지정할 수 있도록 방문자의 프로필에 저장할 필요가 없는 추가적인 페이지 데이터를 Target에 전송하는 데 유용합니다. 대신 이 값은 페이지나, 특정 페이지에서 사용자가 취하는 행동을 설명하는 데 사용됩니다.

### 형식

페이지 매개 변수는 서버 호출을 통해 문자열 이름/값 쌍으로 Target에 전달됩니다. 매개 변수 이름과 값은 사용자 지정할 수 있습니다(특정 용도로 &quot;예약된 이름&quot;도 있음).

예:

* `page=productPage`

* `categoryId=homeLoans`

### 사용 사례 예

**제품 페이지**: 표시된 특정 제품에 대한 정보를 보냅니다(권장 사항 작동 방식).

**주문 세부 사항**: 주문 수집을 위해 주문 ID, orderTotal 등을 보냅니다.

**카테고리 친화성**: 특정 사이트 카테고리에 대한 사용자의 친화성에 대한 지식을 구축하기 위해 본 카테고리 정보를 Target에 보냅니다.

**타사 데이터**: 날씨 타깃팅 제공자, 계정 데이터(예: DemandBase), 인구 데이터(예: Experian) 등과 같은 타사 데이터 소스의 정보를 보냅니다.

### 방법 장점

데이터는 실시간으로 Target에 전송되며 이 데이터가 들어오는 동일한 서버 호출에서 사용할 수 있습니다.

### 주의 사항

* 페이지 코드 업데이트가 필요합니다(직접 또는 태그 관리 시스템 사용).
* 후속 페이지/서버 호출에서 타깃팅을 위해 데이터를 사용해야 하는 경우 프로필 스크립트로 변환해야 합니다.
* 쿼리 문자열에는 [IETF(Internet Engineering Task Force) 표준](https://www.ietf.org/rfc/rfc3986.txt)에 대한 문자만 포함될 수 있습니다 .

   IETF 사이트에서 언급된 것 외에도, Target은 쿼리 문자열에 다음과 같은 문자를 허용합니다.

   `&lt; > # % &quot; { } | \\ ^ \[\] \``

   다른 모든 문자는 URL로 인코딩해야 합니다. The standard specifies the following format ( [https://www.ietf.org/rfc/rfc1738.txt](https://www.ietf.org/rfc/rfc1738.txt) ), as illustrated below:

   ![](assets/ietf1.png)

   또는 간단하게 전체 목록을 지정합니다.

   ![](assets/ietf2.png)

### 코드 예

targetPageParamsAll(매개 변수를 페이지의 모든 mbox 호출에 추가합니다.):

`function targetPageParamsAll() { return "param1=value1&param2=value2&p3=hello%20world";`

targetPageParams(매개 변수를 페이지의 글로벌 mbox에 추가합니다.):

`function targetPageParams() { return "param1=value1&param2=value2&p3=hello%20world";`

mboxCreate 코드에 있는 매개 변수:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','param1=value1','param2=value2'); </script>`

### 관련 정보 링크

권장 사항: [페이지 유형에 따른 구현](/help/c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC)

주문 확인: [전환 추적](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)

카테고리 친화성: [카테고리 친화성](/help/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC)

## 인페이지 프로필 속성(&quot;mbox 내 프로필 속성&quot;이라고도 함) {#section_57E1C161AA7B444689B40B6F459302B6}

인페이지 프로필 속성은 나중에 사용할 수 있도록 방문자 프로필에 저장된 페이지 코드를 통해 직접 전달된 이름/값 쌍입니다.

인페이지 프로필 속성을 사용하면 나중에 타깃팅 및 세그멘테이션을 수행할 수 있도록 사용자별 데이터를 Target의 프로필에 저장할 수 있습니다.

### 형식

인페이지 프로필 속성은 서버 호출을 통해 속성 이름 앞에 접두사 &quot;profile.&quot;을 사용하는 문자열 이름/값 쌍으로 Target에 전달됩니다.

속성 이름과 값은 사용자 지정할 수 있습니다(특정 용도로 &quot;예약된 이름&quot;도 있음).

예:

* `profile.membershipLevel=silver`
* `profile.visitCount=3`

### 사용 사례 예

**로그인 정보**: 사용자의 로그인을 기준으로 비PII(개인 식별 정보) 데이터를 Target에 공유합니다. 멤버십 상태, 주문 히스토리 등이 이러한 정보일 수 있습니다.

**스토어 정보**: 이 사용자의 기본 설정 위치가 되는 스토어를 추적합니다.

**이전 상호 작용**: 향후 개인화할 때 알려주기 위해 이전에 사이트에서 수행한 작업을 추적합니다.

### 방법 장점

데이터는 실시간으로 Target에 전송되며 이 데이터가 들어오는 동일한 서버 호출에서 사용할 수 있습니다.

### 주의 사항

페이지 코드 업데이트가 필요합니다(직접 또는 태그 관리 시스템 사용).

속성 및 값은 서버 호출에 표시되므로 방문자가 값을 볼 수 있습니다. 크레딧 범위와 같은 정보나 기타 개인적일 수 있는 정보를 공유하는 경우 이 방법은 최고의 접근 방식이 아닐 수 있습니다.

### 코드 예

targetPageParamsAll(속성을 페이지의 모든 mbox 호출에 추가합니다.):

`function targetPageParamsAll() { return "profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

targetPageParams(속성을 페이지의 글로벌 mbox에 추가합니다.):

`function targetPageParams() { return profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

mboxCreate 코드에 있는 속성:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); </script>`

### 관련 정보 링크

[프로필 속성](/help/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201)

[방문자 프로필](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E)

## 스크립트 프로필 속성 {#section_3E27B58C841448C38BDDCFE943984F8D}

스크립트 프로필 속성은 Target 솔루션에 정의된 이름/값 쌍입니다. 서버 호출에 대해 Target 서버에서 JavaScript 코드 조각을 실행하여 값을 결정합니다.

사용자는 mbox 호출에 대해 실행되는 작은 코드 조각을 작성한 다음 대상 및 활동 멤버십에 대해 방문자를 평가합니다.

### 형식

스크립트 프로필 속성은 Target의 대상 섹션에서 만들어집니다. 모든 속성 이름은 유효하며, 값은 Target 사용자가 작성한 JavaScript 함수의 결과입니다. 인페이지 프로필 속성과 구분할 수 있도록 속성 이름에는 Target에서 자동으로 &quot;user. &quot;가 접두사로 지정됩니다.

코드 조각은 Rhino JS 언어로 작성되며 토큰 및 기타 값을 참조할 수 있습니다.

### 사용 사례 예

**장바구니 포기**: 방문자가 장바구니에 도달하면 프로필 스크립트를 1로 설정합니다. 방문자가 전환하면 0으로 재설정합니다. 값이 1이면 방문자의 장바구니에 항목이 있습니다.

**방문 카운트**: 모든 신규 방문에서 카운트가 1씩 증가하여 방문자가 사이트를 재방문하는 빈도를 추적합니다.

### 방법 장점

페이지 코드 업데이트가 필요하지 않습니다.

대상 및 활동 멤버십 결정 전에 실행되므로 이러한 프로필 스크립트 속성은 단일 서버 호출의 멤버십에 영향을 줄 수 있습니다.

매우 활발히 실행될 수 있습니다. 스크립트당 많은 수의 명령어를 실행할 수 있습니다.

### 주의 사항

JavaScript 지식이 필요합니다.

프로필 스크립트의 실행 순서는 보장할 수 없으므로 서로 의존할 수 없습니다.

디버깅하기가 어려울 수 있습니다.

### 코드 예

프로필 스크립트는 매우 유연합니다.

`user.purchase_recency: var dayInMillis = 3600 * 24 * 1000; if (mbox.name == 'orderThankyouPage') {  user.setLocal('lastPurchaseTime', new Date().getTime()); } var lastPurchaseTime = user.getLocal('lastPurchaseTime'); if (lastPurchaseTime) {  return ((new Date()).getTime()-lastPurchaseTime)/dayInMillis; }`

### 관련 정보 링크

[프로필 스크립트 속성](/help/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)의 프로필 스크립트 정보 카드 보기 섹션을 참조하십시오

## 데이터 공급자 {#section_14FF3BE20DAA42369E4812D8D50FBDAE}

데이터 공급자는 타사의 데이터를 Target에 쉽게 전달할 수 있는 기능입니다.

참고: 데이터 공급자는 at.js 1.3 이상이 필요합니다.

### 형식

`window.targetGlobalSettings.dataProviders` 설정은 데이터 공급자의 배열입니다.

각 데이터 공급자 구조에 대한 자세한 내용은 [데이터 공급자](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)를 참조하십시오.

### 사용 사례 예

날씨 서비스, DMP 또는 사용자 지정 웹 서비스와 같은 타사로부터 데이터를 수집합니다. 그런 다음, 이 데이터를 사용하여 대상, Target 콘텐츠를 작성하고 방문자 프로필을 보강할 수 있습니다.

### 방법 장점

이 설정을 사용하여 고객은 Demandbase, BlueKai 및 사용자 지정 서비스와 같은 서드 파티 데이터 공급자로부터 데이터를 수집하고, 글로벌 mbox의 mbox 매개 변수가 요청할 때 Target으로 데이터를 전달할 수 있습니다.

비동기 및 동기 요청을 통해 여러 공급자로부터 데이터를 수집하도록 지원합니다.

이 접근 방식을 사용하면 각 공급자에 대해 독립적인 시간 제한을 포함하여 페이지 성능에 미치는 영향을 제한하면서, 기본 페이지 콘텐츠의 깜박임을 쉽게 관리할 수 있습니다

### 주의 사항

`window.targetGlobalSettings.dataProviders`에 추가된 데이터 공급자가 비동기 상태인 경우 병렬로 실행됩니다. 방문자 API 요청은 최소 대기 시간을 허용하기 위해 `window.targetGlobalSettings.dataProviders`에 추가된 함수와 함께 실행됩니다.

at.js는 데이터를 캐시하려고 하지 않습니다. 데이터 공급자는 데이터를 한 번만 가져오는 경우 데이터가 캐시되는지 확인해야 하고, 공급자 함수가 호출될 때 두 번째 호출을 위해 캐시 데이터를 제공해야 합니다.

### 코드 예

[데이터 공급자](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)에서 몇 가지 예를 볼 수 있습니다.

### 관련 정보 링크

문서: [데이터 공급자](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)

### 교육 비디오:

* [Adobe Target에서 데이터 공급자 사용](https://helpx.adobe.com/kr/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Adobe Target에서 데이터 공급자 구현](https://helpx.adobe.com/kr/target/kt/using/dataProviders-atjs-technical-video-implement.html)

## 벌크 프로필 업데이트 API {#section_92AB4820A5624C669D9A1F1B6220D4FA}

API를 통해 많은 방문자에 대한 방문자 프로필 업데이트를 사용하여 Target에 .csv 파일을 보냅니다. 각 방문자 프로필은 하나의 호출에서 여러 개의 인페이지 프로필 속성으로 업데이트할 수 있습니다.

이 선택 사항은 다음 몇 가지 차이점을 제외하고는 고객 속성과 매우 유사합니다.

* 고객 속성은 FTP 업로드를 사용하는 반면, Target 벌크 프로필 업데이트 API는 HTTP POST API를 사용합니다.
* 고객 속성 데이터는 Analytics과 공유할 수 있고, 벌크 프로필 업데이트는 Target에서만 사용할 수 있습니다.
* 고객 속성은 Target이 아직 보지 못한 사용자에 대한 프로필 작성을 지원합니다. 벌크 프로필 업데이트 API는 기존 Target 프로필만 업데이트합니다.
* 고객 속성에는 Experience Cloud ID(ECID)를 사용해야 합니다. 벌크 프로필 업데이트 API에는 TNT ID나 `mbox3rdPartyId`를 사용해야 합니다.
* `mbox3rdPartyID`에서 더하기 기호(+)와 슬래시(/)는 보낼 수 없습니다.

### 형식

.csv 파일은 Target PCID나 mboxThirdPartyId를 통해 각 방문자를 참조해야 합니다. Experience Cloud ID(ECID)는 지원되지 않습니다. 모든 프로필 속성/값은 API를 통해 생성 및 업데이트됩니다. 형식 세부 사항은 API 설명서에 나와 있습니다.

### 사용 사례 예

CRM 또는 기타 내부 시스템은 페이지 구현에서 프로필 데이터를 노출하지 않고 Target에 지속적으로 업데이트하고자 하는 방문자에 대한 중요 데이터를 저장합니다.

### 방법 장점

프로필 속성의 개수에 대한 제한은 없습니다.

사이트를 통해 전송된 프로필 속성은 API를 통해 업데이트할 수 있으며 반대의 경우도 마찬가지입니다.

### 주의 사항

묶음 파일의 크기는 50MB 미만이어야 합니다. 또한 총 행 수는 업로드당 500,000개 행을 초과하지 않아야 합니다.

이후 묶음에서 24시간 동안 업로드할 수 있는 행 수에는 제한이 없습니다. 그러나 영업 시간 동안 처리 프로세스를 조절하여 다른 프로세스가 효율적으로 실행되도록 할 수도 있습니다.

동일한 thirdPartyIds 간에 mbox를 호출하지 않고 연속적인 [V2 배치 업데이트를 호출](https://developers.adobetarget.com/api/#updating-profiles)하면 첫 번째 배치 업데이트 호출에서 업데이트된 속성을 재정의합니다.

### 코드 예

[프로필 업데이트](https://developers.adobetarget.com/api/#updating-profiles)를 참조하십시오.

### 관련 정보 링크

[프로필 업데이트](https://developers.adobetarget.com/api/#updating-profiles)

## 벌크 프로필 업데이트 API {#section_5D7A9DD7019F40E9AEF2F66F7F345A8D}

한 방문자 프로필은 벌크 프로필 업데이트 API와 거의 동일하지만, .csv 파일을 사용하는 대신 API 호출에서 일렬로 한 번에 업데이트됩니다.

### 형식

방문자는 Target mboxPC 값이나 mboxThirdPartyId 값을 통해 식별해야 합니다. Experience Cloud ID(ECID)는 지원되지 않습니다. 

### 사용 사례 예

방문자가 콜 센터에 도착하거나, 대출 자금을 지원받거나, 점포에서 포인트 카드를 사용하거나, 키오스크에 액세스하는 등의 오프라인 작업을 수행하는 경우 실시간으로 Target을 업데이트할 수 있습니다.

### 방법 장점

프로필 속성의 개수에 대한 제한은 없습니다.

사이트를 통해 전송된 프로필 속성은 API를 통해 업데이트할 수 있으며 반대의 경우도 마찬가지입니다.

### 주의 사항

24시간 기간당 1,000,000개의 API 호출 수 제한(1백만)

프로필만 업데이트합니다. Target이 아직 보지 못한 잠재적 사용자에 대한 프로필을 작성할 수 없습니다.

### 코드 예

GET 및 POST가 지원됩니다. `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

### 관련 정보 링크

[프로필 업데이트](https://developers.adobetarget.com/api/#updating-profiles)

## 고객 속성{#section_C47FC7980A9A4608BD1A5F0BD900FA70}을 통해 정보를 추가할 수 있습니다 

고객 속성을 사용하면 FTP를 통해 방문자 프로필 데이터를 Experience Cloud에 업로드할 수 있습니다. 업로드했으면 Adobe Analytics 및 Adobe Target의 데이터를 활용합니다.

Target Standard 고객은 5개의 속성을 활용할 수 있으며, Target Premium 고객은 200개의 속성을 활용할 수 있습니다.

### 형식

Experience Cloud ID(ECIDs) 및 속성 이름/값 쌍이 있는 .csv 파일은 FTP를 통해 업로드되거나 Experience Cloud UI에서 수동으로 업로드됩니다.

### 사용 사례 예

CRM 또는 기타 내부 시스템은 Target 및 Analytics를 포함하여 Adobe의 Experience Cloud와 공유하려는 중요 정보를 저장합니다.

### 방법 장점

고객 데이터를 업로드하면 Target에 방문자가 아직 표시되지 않은 경우에도 Target에서 해당 방문자에 대한 프로필 항목이 만들어집니다.

동일한 데이터를 Target 및 Analytics에서 자동으로 사용할 수 있습니다.

FTP는 API보다 간단한 구현 방법일 수 있습니다.

### 주의 사항

Target Standard 고객은 5개의 속성을 활용할 수 있으며, Target Premium 고객은 200개의 속성을 활용할 수 있습니다.

페이지에서가 아니라 고객 속성을 통해서만 값을 업데이트할 수 있습니다.

Experience Cloud ID(ECID) 구현이 필요합니다.

### 코드 예

Details can be found in [Create a customer attribute source and upload the data file](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).

### 관련 정보 링크

[고객 속성 소스를 만들고 데이터 파일 업로드](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).