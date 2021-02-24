---
keywords: 클라이언트 지원;CNAME;인증서 프로그램;표준 이름;쿠키;인증서;amc;adobe 관리 인증서;디지커드;도메인 제어 유효성 검사;dcv
description: Adobe 클라이언트 지원팀과 협력하여 Adobe Target에서 CNAME(표준 이름) 지원을 구현하여 광고 차단 문제 또는 ITP 관련 쿠키 정책을 처리합니다.
title: Target에서 CNAME을 어떻게 사용합니까?
feature: 개인 정보 및 보안
role: Developer
translation-type: tm+mt
source-git-commit: 69677b9d384d9817a39386fc1388a4aa42121713
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 2%

---


# CNAME 및 Adobe Target

[!DNL Adobe Target]에서 CNAME(Canonical Name) 지원을 구현하기 위한 클라이언트 지원 팀에 대한 지침 [!DNL Adobe] CNAME을 사용하여 광고 차단 문제 또는 ITP 관련(Intelligent Tracking Prevention) 쿠키 정책을 처리합니다. CNAME을 사용하면 [!DNL Adobe]이(가) 소유한 도메인이 아닌 고객이 소유한 도메인에 대한 호출이 수행됩니다.

## Target에서 CNAME 지원 요청

1. SSL 인증서에 필요한 호스트 이름 목록을 결정합니다(아래 FAQ 참조).

1. 각 호스트 이름에 대해 일반 [!DNL Target] 호스트 이름 `clientcode.tt.omtrdc.net`을 가리키는 DNS에 CNAME 레코드를 만듭니다.

   예를 들어 클라이언트 코드가 &quot;사용자 이름 지정&quot;이고 제안된 호스트 이름이 `target.example.com`인 경우 DNS CNAME 레코드는 다음과 비슷합니다.

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   >Adobe의 인증 기관인 DigiCert는 이 단계가 완료될 때까지 인증서를 발급할 수 없습니다. 따라서 이 단계가 완료될 때까지 [!DNL Adobe]은(는) CNAME 구현에 대한 요청을 이행할 수 없습니다.

1. [CNAME ](https://experienceleague.adobe.com/docs/core-services/assets/FPC_Request_Form.xlsx?lang=en) 지원을 요청하는 Adobe 클라이언트 지원 티켓을  [열 때 이 양식을 작성하고 포함시킵니다](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

   * Adobe [!DNL Target] 클라이언트 코드:
   * SSL 인증서 호스트 이름(예:`target.example.com target.example.org`):
   * SSL 인증서 구매자(Adobe 권장): FAQ 참조Adobe/고객
   * 고객이 &quot;BYOC(Bring Your Own Certificate)&quot;라고도 하는 인증서를 구입하는 경우 다음과 같은 추가 세부 사항을 작성합니다.
      * 인증서 조직(예:예제 Company Inc):
      * 인증서 조직 단위(선택 사항: 예:마케팅):
      * 인증서 국가(예:미국):
      * 인증서 상태/지역(예:캘리포니아):
      * 인증서 구/군/시(예:산호세):

1. [!DNL Adobe]이(가) 인증서를 구입하는 경우, [!DNL Adobe]은 DigiCert와 함께 작동하여 Adobe의 프로덕션 서버에 인증서를 구입하여 배포합니다.

   고객이 인증서(BYOC)를 구입하는 경우, [!DNL Adobe] Client Care는 사용자에게 인증서 서명 요청(CSR)을 보냅니다. 선택한 인증 기관을 통해 인증서를 구입할 때 CSR을 사용합니다. 인증서가 발급되면 인증서 사본을 [!DNL Adobe] 클라이언트 지원팀에 보내 배포하십시오.

   [!DNL Adobe] 구현이 준비되면 클라이언트 지원팀이 알려줍니다.

1. `serverDomain`을 at.js의 새 CNAME으로 업데이트합니다.

## FAQ

다음 정보는 [!DNL Target]에서 CNAME 지원 요청 및 구현과 관련하여 자주 묻는 질문에 대한 답변입니다.

### 직접 인증서를 제공할 수 있습니까(인증서 또는 BYOC 가져오기)?

직접 인증서를 제공할 수 있습니다. 그러나 [!DNL Adobe]은(는) 이 방법을 권장하지 않습니다. [!DNL Adobe] 및 [!DNL Adobe] 구매 시 SSL 인증서 라이프사이클을 모두 관리하는 것이 더 쉽습니다. SSL 인증서는 매년 갱신되어야 합니다. 따라서 [!DNL Adobe] 클라이언트 지원팀이 적절한 시기에 새 인증서를 받으려면 매년 사용자에게 연락해야 합니다. 일부 고객은 적시에 갱신된 인증서를 작성하는 데 어려움을 겪을 수 있습니다. 브라우저가 연결을 거부하므로 인증서가 만료되면 [!DNL Target] 구현이 실패합니다.

>[!IMPORTANT]
>
>[!DNL Target] BRING-your-own-certificate CNAME 구현을 요청하는 경우, 귀하는 매년 [!DNL Adobe] 클라이언트 지원팀에 갱신된 인증서를 제공해야 합니다. [!DNL Adobe]이(가) 갱신된 인증서를 배포하기 전에 CNAME 인증서가 만료되도록 허용하면 특정 [!DNL Target] 구현에 대한 중단이 발생합니다.

### 새 SSL 인증서가 만료될 때까지 얼마나 걸립니까?

2020년 9월 1일 이전에 발급된 인증서는 2년 인증서입니다. 2020년 9월 1일 이후에 발행된 인증서는 1년 인증서입니다. 1년 인증서 [여기](https://www.digicert.com/position-on-1-year-certificates)로 이동하는 방법에 대해 자세히 읽을 수 있습니다.

### 어떤 호스트 이름을 선택해야 합니까? 도메인당 호스트 이름은 몇 개입니까?

[!DNL Target] CNAME 구현에는 SSL 인증서 및 고객의 DNS에 도메인당 하나의 호스트 이름만 필요합니다. Adobe에서는 하나의 호스트 이름을 권장합니다. 일부 고객은 고유한 목적(예: 스테이징에서 테스트)으로 지원되는 도메인당 호스트 이름을 더 많이 요구합니다.

대부분의 고객은 `target.example.com` 같은 호스트 이름을 선택합니다. Adobe은 이 방법을 따를 것을 권장합니다. 그러나 선택은 궁극적으로 여러분의 것입니다. 기존 DNS 레코드의 호스트 이름을 요청하지 마십시오. 이렇게 하면 충돌이 발생하고 [!DNL Target] CNAME 요청 해결 시간이 지연됩니다.

### 이미 [!DNL Adobe Analytics]에 대한 CNAME 구현이 있습니다. 동일한 인증서 또는 호스트 이름을 사용할 수 있습니까?

아니요. [!DNL Target]에는 별도의 호스트 이름과 인증서가 필요합니다.

### 현재 구현된 Target이 ITP 2.x에 영향을 받습니까?

Safari 브라우저에서 [!DNL Target] JavaScript 라이브러리가 있는 웹 사이트로 이동합니다. `analytics.company.com` 등 CNAME 컨텍스트에서 설정된 [!DNL Target] 쿠키가 표시되는 경우 ITP 2.x의 영향을 받지 않습니다.

[!DNL Target]에 대해 [!DNL Analytics] CNAME만 사용하여 ITP 문제를 해결할 수 있습니다. [!DNL Target]이(가) 차단된 광고 차단 시나리오에서만 별도의 [!DNL Target] CNAME이 필요합니다.

ITP에 대한 자세한 내용은 [Apple ITP(Intelligent Tracking Prevention) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)을 참조하십시오.

### CNAME 구현이 배포되면 어떤 유형의 서비스 중단을 예상할 수 있습니까?

인증서를 배포(인증서 갱신 포함)할 때 서비스 중단이 발생하지 않습니다.

그러나 [!DNL Target] 구현 코드(`serverDomain` in at.js)의 호스트 이름을 새 CNAME 호스트 이름(`target.example.com`)으로 변경하면 웹 브라우저는 재방문자를 새 방문자로 처리합니다. 이전 쿠키는 이전 호스트 이름(`clientcode.tt.omtrdc.net`)에서 액세스할 수 없으므로 돌아온 방문자의 프로필 데이터가 유실됩니다. 브라우저 보안 모델로 인해 이전 쿠키에 액세스할 수 없습니다. 이러한 중단은 새 CNAME에 대한 초기 컷오버 시에만 발생합니다. 호스트 이름이 변경되지 않으므로 인증서 갱신에 동일한 효과가 없습니다.

### CNAME 구현에 어떤 키 유형 및 인증서 서명 알고리즘이 사용됩니까?

모든 인증서는 RSA SHA-256이고 키는 기본적으로 RSA 2048비트입니다. 2048비트보다 큰 키 크기는 현재 지원되지 않습니다.

### 내 CNAME 구현이 트래픽을 위해 준비되었는지 어떻게 확인할 수 있습니까?

macOS 또는 Linux 명령줄 터미널에서는 bash 및 curl 7.49+를 사용하여 다음 명령 세트를 사용합니다.

1. 이 bash 함수를 터미널에 붙여 넣습니다.

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. 이 명령을 붙여 넣습니다(호스트 이름으로 `target.example.com` 대체).

   ```
   validateEdgeFpsslSni target.example.com
   ```

   구현이 준비되면 아래와 같은 출력이 표시됩니다. 중요한 부분은 모든 줄에 원하는 호스트 이름과 일치하는 `CN=target.example.com`이 포함됩니다. 라인에 `CN=*.tt.omtrdc.net`이 포함되어 있으면 구현이 **준비되지 않음**&#x200B;입니다.

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge36.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge37.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge38.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. 새 DNS CNAME을 다른 말림 요청과 함께 확인합니다. 이 요청에는 `CN=target.example.com`도 표시됩니다.

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >이 명령이 실패했지만 위의 `validateEdgeFpsslSni` 명령이 성공하면 DNS 업데이트가 완전히 전파될 때까지 기다리십시오. DNS 레코드에는 해당 레코드의 DNS 답글에 대한 캐시 만료 시간을 지정하는 [TTL(time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records)이(가) 연결되어 있습니다. 결과적으로, TTL이 있는 한 기다려야 할 수도 있다. `dig target.example.com` 명령 또는 [G Suite 도구 상자](https://toolbox.googleapps.com/apps/dig/#CNAME)를 사용하여 특정 TTL을 찾을 수 있습니다.

## 알려진 제한 사항

* CNAME과 at.js 1.x가 있는 경우 QA 모드는 타사 쿠키를 기반으로 하므로 고정되지 않습니다. 해결 방법은 탐색하는 각 URL에 미리 보기 매개 변수를 추가하는 것입니다. CNAME 및 at.js 2.x가 있는 경우 QA 모드가 고정됩니다.
* 현재 at.js 1.8.2 및 at.js 2.3.1 이전 버전에 at.js 버전을 사용할 때 `overrideMboxEdgeServer` 설정이 CNAME에서 제대로 작동하지 않습니다. 이전 버전의 at.js를 사용 중인 경우 요청이 실패하지 않도록 이 설정을 `false`로 설정해야 합니다. 또는 [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)를 지원되는 최신 버전으로 업데이트하는 것이 좋습니다.
* CNAME을 사용할 때 [!DNL Target] 호출에 대한 쿠키 헤더의 크기가 증가할 가능성이 커집니다. [!DNL Adobe] 쿠키 크기를 8KB 이하로 유지하는 것이 좋습니다.
