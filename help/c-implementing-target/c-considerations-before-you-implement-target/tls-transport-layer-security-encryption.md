---
keywords: tls;tls 1.0;transport layer security;encryption;tls 1.1;tls 1.2
description: Adobe 및 Target에서 TLS(전송 계층 보안)를 사용하여 가장 높은 보안 표준을 유지 관리하고 고객 데이터의 안전을 강화하는 방법과 관련된 변경 사항에 대한 정보입니다.
title: TLS(전송 계층 보안) 암호화 변경 사항
feature: privacy and security
topic: Standard
uuid: d222b966-ee73-4254-87b7-68099583e0dd
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '1233'
ht-degree: 61%

---


# TLS(전송 계층 보안) 암호화 변경 사항{#tls-transport-layer-security-encryption-changes}

Adobe 및 Adobe Target이 TLS(전송 계층 보안)를 사용하여 최고 보안 표준을 유지하고 고객 데이터의 보안을 강화하는 방법에 대한 변경 정보입니다.

TLS(전송 계층 보안)는 네트워크를 통해 데이터를 안전하게 교환해야 하는 웹 브라우저 및 애플리케이션에서 현재 사용되는 가장 널리 배포된 보안 프로토콜입니다. Adobe는 이전 프로토콜의 서비스를 종료해야 하는 보안 준수 표준을 사용하며 최신 버전 및 보안 버전을 사용하기 위해 TLS 1.2의 사용을 권장합니다.

>[!IMPORTANT]
>
>2020년 3월 1일 이후, Adobe Target은 더 이상 VEC(Visual Experience Composer), EEC(Enhanced Experience Composer), 활동 전달, API 등에 대한 TLS 1.1 암호화를 지원하지 않습니다. 문제를 방지하려면 2020년 3월 1일 전에 TLS 1.2로 업그레이드하십시오.

이렇게 해도 고객 데이터 또는 보고에 큰 영향을 주지는 않습니다.

## EEC(향상된 경험 작성기)를 사용한 VEC(시각적 경험 작성기){#section_B374B62DEC3344C194AC7BECC2EE0AA0}

2020년 3월 1일 현재 TLS 1.2는 기본값이며 TLS 1.1은 더 이상 지원되지 않습니다.

Adobe는 단계적으로 고객을 TLS1.2.로 전환합니다. 이미 1.2 규격 도메인을 사용하는 고객은 별도로 변경할 필요 없이 TLS 1.2로 전환됩니다. 대부분의 고객 도메인은 이미 TLS 1.2를 지원합니다.그러나 도메인이 TLS 1.2를 지원하지 않는 경우 이러한 도메인은 오늘과 같은 TLS 1.1에 보관됩니다(2020년 3월까지).

이 마이그레이션 단계 중에는 문제가 발생하지 않아야 합니다. VEC가 이전에 작업하던 사이트 로드를 중지한 경우 이 마이그레이션을 가능한 원인으로 인용한 [Client Care 티켓을 여십시오](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

그러나 TLS 1.2를 지원하지 않고 TSL 1.1을 사용하는 고객 중 하나인 경우 도메인/인프라를 TLS 1.2로 이동할 계획입니다. 2020년 3월 1일까지 TLS 1.1 프로토콜을 계속 지원할 예정입니다. 2020년 3월 1일부터 Target은 향상된 경험 컴포저 기능을 통해 VEC에 사용할 TLS 1.1 프로토콜을 지원하지 않습니다.

모든 고객이 앞으로 TLS 1.2를 사용할 것을 권장하지만, TLS 1.2를 지원하지 *않는* 새로운 고객은 고객 지원에 연락하여 향상된 경험 작성기를 위해 TLS 1.1을 사용해야 한다고 알리십시오. 그러나 2020년 3월 1일 이후로도 지원되지 않으므로 TLS 1.2로 이동할 계획입니다.

## Activity delivery {#section_46CA5943E4354B259014C2BF340AECD6}

2020년 3월 1일부터 Target 서버가 더 이상 TLS 1.1을 지원하지 않습니다. 이 변경 사항으로 Target 서버는 더 이상 TLS 1.2 이상을 지원하지 않는 이전 장치 또는 웹 브라우저가 있는 방문자의 요청을 수락하지 않습니다. 따라서 TLS 1.1만 지원하거나 기본적으로 TLS 1.1을 지원하는 이전 장치 및 브라우저는 Adobe Target에서 활동 컨텐츠를 받지 않습니다. 사이트의 기본 컨텐츠가 렌더링됩니다.

영향을 받는 일부 이전 장치 및 브라우저는 다음과 같습니다.

* Google Chrome(Android용 Chrome) 버전 29 및 이전 버전
* Opera 브라우저(Opera Mobile) 버전 12.17 및 이전 버전
* Mozilla Firefox(모바일용 Firefox) 버전 26 및 이전 버전
* Android 4.3 및 이전 버전
* Windows 7 및 이전 버전의 Internet Explorer 8~10
* Windows Phone 8.0의 Internet Explorer 10
* Safari 6.0.4/OS X10.8.4 및 이전 버전

이 변경 사항에 대해 계획할 때는 다음 사항을 고려하십시오(2020년 3월 1일 마감일은 이러한 모든 항목에 영향을 줍니다).

* 기본 사이트가 호환 장치 및 브라우저를 구입할 준비가 되었는지 확인해야 합니다.
* Target 보고서의 방문자 수는 방문자 수가 잠재적으로 약간 줄어들 수 있습니다.
* TLS 1.2를 지원하지 않는 이전 디바이스 또는 브라우저를 대상으로 하기 위해 특별히 만들어진 대상을 변경해야 할 수 있습니다. 이러한 디바이스 및 브라우저로의 배달이 더 이상 작동하지 않습니다.

For more details about supported browsers and their versions, see [Supported Browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100).

## Adobe Target API {#section_88797FA5434049EC89F908853CC76903}

2020년 3월 1일부터 Target API는 더 이상 TLS 1.1 암호화를 지원하지 않습니다. API에 액세스하는 고객은 자신들에게 영향이 없는지 확인해야 합니다.

* 기본 설정으로 Java 7을 사용하는 API 클라이언트는 TLS 1.2를 지원하도록 수정해야 합니다. 자세한 내용은 Java 웹 사이트에서 &quot;[Changing default TLS protocol version for client end points: TLS 1.0 to TLS 1.2](https://www.java.com/en/configure_crypto.html)&quot;(클라이언트 종단점에 대한 기본 TLS 프로토콜 버전 변경: TLS 1.0에서 TLS 1.2로)를 참조하십시오.
* Java 8을 사용하는 API 클라이언트는 기본값 설정이 TLS 1.2이므로 영향을 받지 않아야 합니다.
* 다른 프레임워크를 사용하는 API 클라이언트의 경우 TLS 1.2 지원에 대한 자세한 내용을 알려면 해당 공급업체에 문의해야 합니다.

## Access to Experience Cloud Solutions interfaces {#section_748870ADE77B4CBEB18518DC784E64E5}

Target Standard/Premium 인터페이스에서 이미 [최신 웹 브라우저](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100)를 요구하고 있으므로 문제는 예상되지 않습니다. Target에 연결할 수 없는 경우 브라우저를 최신 버전으로 업그레이드해야 합니다.

## How to check which TLS version your browser uses {#section_44716DA2CEFF492BABD95AE32B1A3FC6}

Google Chrome을 사용하여 웹 사이트에서 TLS 버전을 확인하려면 다음을 수행하십시오.

1. Chrome에서 해당 웹 사이트를 엽니다.
1. Chrome 메뉴(세 개의 세로 줄임표)에서 추가 도구 > 개발자 도구를 클릭합니다.

   ![Chrome Developer Tools](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/chrome-developer-tools.png)

1. 보안 탭을 연 다음 연결 아래에서 TLS 버전 정보를 검사합니다.

   ![TLS 버전 세부 정보](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/chrome-tls-version.png)

>[!NOTE]
>
>이러한 지침은 게시 시점에 발표되며 변경될 수 있습니다. 빠른 인터넷 검색을 통해 이러한 지침이 변경된다면 도움이 될 것입니다.  다른 브라우저에도 유사한 단계가 있습니다.

## TLS 버전 1.2 이하를 지원하는 브라우저에서의 예상 동작 {#section_B5DA97A34EF248EB927610A5DA71EF2F}

이 섹션에서는 at.js 또는 mbox.js 구현을 사용하는 경우에만 1.2 이하에서 TLS 버전을 지원하는 브라우저에서 예상되는 내용을 설명합니다. 비교를 위해 이 섹션에서는 TLS 1.2를 지원하는 브라우저에서 예상되는 사항에 대해 설명합니다.

### 중앙 끝점

| Target JavaScript 구현 | 세부 사항 |
|--- |--- |
| at.js | TLS 1.0 또는 TLS 1.1을 사용하는 경우:<ul><li>네트워크 탭에서 브라우저 개발 도구를 사용하면 &quot;200 OK&quot;가 표시됩니다. 이는 요청이 성공했음을 의미합니다.</li><li>사용자에게 &quot;이 페이지에 안전하게 연결할 수 없음&quot; 메시지가 표시됩니다. 이 메시지는 사이트가 오래되었거나 안전하지 않은 TLS 보안 설정을 사용하기 때문에 발생했을 수 있다고 설명합니다.</li><li>콘솔 오류가 표시되지 않습니다.</li></ul>TLS 1.2 사용:<ul><li>at.js 파일이 다운로드됩니다.</li></ul> |
| mbox.js | TLS 1.0 또는 TLS 1.1을 사용하는 경우:<ul><li>네트워크 탭에서 브라우저 개발 도구를 사용하면 &quot;200 OK&quot;가 표시됩니다. 이는 요청이 성공했음을 의미합니다.</li><li>사용자에게 &quot;이 페이지에 안전하게 연결할 수 없음&quot; 메시지가 표시됩니다. 이 메시지는 사이트가 오래되었거나 안전하지 않은 TLS 보안 설정을 사용하기 때문에 발생했을 수 있다고 설명합니다.</li><li>콘솔 오류가 표시되지 않습니다.</li></ul>TLS 1.2 사용:<ul><li>mbox.js 파일이 다운로드됩니다.</li></ul> |

### 가장자리 끝점

| Target JavaScript 구현 | 세부 사항 |
|--- |--- |
| at.js | TLS 1.0 또는 TLS 1.1을 사용하는 경우:<ul><li>네트워크 탭에서 브라우저 개발 도구를 사용하면 &quot;200 OK&quot;가 표시됩니다. 이는 요청이 성공했음을 의미합니다.</li><li>사용자에게 &quot;이 페이지에 안전하게 연결할 수 없음&quot; 메시지가 표시됩니다. 이 메시지는 사이트가 오래되었거나 안전하지 않은 TLS 보안 설정을 사용하기 때문에 발생했을 수 있다고 설명합니다.</li><li>콘솔 오류가 표시되지 않습니다.</li><li>기본 컨텐츠가 제공됩니다.</li></ul>TLS 1.2 사용:<ul><li>오퍼 컨텐츠가 제공됩니다.</li></ul> |
| mbox.js | TLS 1.0 또는 TLS 1.1을 사용하는 경우:<ul><li>네트워크 탭에서 브라우저 개발 도구를 사용하면 &quot;200 OK&quot;가 표시됩니다. 이는 요청이 성공했음을 의미합니다.</li><li>사용자에게 &quot;이 페이지에 안전하게 연결할 수 없음&quot; 메시지가 표시됩니다. 이 메시지는 사이트가 오래되었거나 안전하지 않은 TLS 보안 설정을 사용하기 때문에 발생했을 수 있다고 설명합니다.</li><li>콘솔 오류가 표시되지 않습니다.</li><li>기본 컨텐츠가 제공됩니다.</li></ul>TLS 1.2 사용:<ul><li>오퍼 컨텐츠가 제공됨</li></ul> |

### 브라우저 버전 대상을 사용하는 활동(Internet Explorer, 버전 6, 7 또는 8)

>[!NOTE]
>
>Audience 작동이 중단됩니다.

| Target JavaScript 구현 | 세부 사항 |
|--- |--- |
| at.js | 버전 10 이전의 Internet Explorer 버전에서는 at.js가 지원되지 않습니다. |
| mbox.js | TLS 1.0 또는 TLS 1.1을 사용하는 경우:<ul><li>기본 컨텐츠가 제공됩니다.</li><li>Target 요청이 실행되지 않습니다.</li><li>콘솔 오류가 표시되지 않습니다.</li><li>네트워크 탭에서 브라우저 개발 도구를 사용하면 &quot;200 OK&quot;가 표시됩니다. 이는 요청이 성공했음을 의미합니다.</li></ul>TLS 1.2 사용:<ul><li>오퍼 컨텐츠가 제공됩니다.</li></ul> |