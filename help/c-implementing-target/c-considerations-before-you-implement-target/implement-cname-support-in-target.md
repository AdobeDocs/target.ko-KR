---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Adobe Target에서 CNAME(표준 이름) 지원을 구현하기 위한 Adobe Client Care 작업 정보입니다.
title: CNAME 및 Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 113a48f2f06730d637049538cf617f386d9ba4bd

---


# CNAME 및 Adobe Target {#cname-and-adobe-target}

Adobe Client Care에서 CNAME(Canonical Name) 지원을 구현하기 위한 지침을 [!DNL Adobe Target]참조하십시오. 광고 차단 문제 또는 ITP 관련 쿠키 정책을 처리하기 위해 CNAME이 사용되므로 Adobe가 소유한 도메인이 아닌 고객이 소유한 도메인에 대한 호출이 수행됩니다.

## CNAME 지원 요청

Perform the following steps to request CNAME support in [!DNL Target]:

1. Adobe의 인증 기관(DigiCert)은 Adobe가 도메인 아래에 인증서를 생성할 수 있도록 인증되었는지 확인해야 합니다.

   DigiCert가 이 프로세스를 [DCV(Domain Control Validation)](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/)호출하며, 다음 DCV 방법 중 하나 이상에 대해 이 프로세스가 완료될 때까지 Adobe는 도메인 아래에 인증서를 생성할 수 없습니다.

   * 가장 빠른 DCV 메서드는 DNS CNAME 메서드로, DNS CNAME 레코드(토큰 포함)를 DigiCert의 DCV 호스트 이름(`dcv.digicert.com`)을 가리키는 도메인에 추가합니다. 이 CNAME 레코드는 Adobe가 인증서를 생성할 권한이 있음을 DigiCert에 표시합니다. Adobe Client Care에서 필요한 DNS 레코드와 함께 지침을 보냅니다. 예:

      ```
      3b0332e02daabf31651a5a0d81ba830a.target.example.com.  IN  CNAME  dcv.digicert.com.
      ```

      >[!NOTE]
      >
      >* 이러한 DCV 토큰은 30일 후 만료되며 Adobe Client Care에서 업데이트된 토큰을 수신하게 됩니다. CNAME 요청을 가장 빨리 해결할 수 있도록 요청을 제출하기 전에 요청된 모든 도메인에서 이러한 DNS를 변경할 수 있도록 준비하십시오.
         >
         >
      * 도메인에 DNS [CAA 레코드가](https://en.wikipedia.org/wiki/DNS_Certification_Authority_Authorization)있으면 아직 추가되지 않은 `digicert.com` 경우 추가해야 합니다. 이 DNS 레코드는 도메인에 대한 인증서를 발급하도록 인증 받은 인증 기관을 나타냅니다. 결과 DNS 레코드는 다음과 같습니다. `example.com. IN CAA 0 issue "digicert.com"`Adobe G Suite [도구 상자를](https://toolbox.googleapps.com/apps/dig/#CAA) 사용하여 루트 도메인에 기존 CAA 레코드가 있는지 확인할 수 있습니다. DigiCert가 CAA 레코드를 처리하는 방법에 대한 자세한 내용을 [여기에서](https://docs.digicert.com/manage-certificates/dns-caa-resource-record-check)확인할 수 있습니다.


   * 또한 DigiCert는 도메인의 WHOIS 정보에 있는 주소와 미리 결정된 이메일 주소(admin, administrator, webmaster, hostmaster 및 postmaster `@[domain_name]`)로 이메일 메시지를 전송하는 이메일 방법을 시도합니다. 자세한 내용은 [DCV 메서드 설명서를](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) 참조하십시오.

      DigiCert는 DCV 이메일 프로세스를 가속화하기 위해 다음 권장 사항을 제공합니다.

      &quot;등록업체/WHOIS 공급자가 [관련 이메일 주소를]숨기거나 제거하지 않았는지 확인하십시오. 이러한 경우 [인증 기관이] 도메인의 WHOIS 데이터에 액세스할 수 있도록 하는 방법(예: 익명 이메일 주소, 웹 양식)을 제공하는지 확인하십시오.&quot;

1. 일반 호스트 이름을 가리키는 도메인의 DNS에 CNAME 레코드를 `clientcode.tt.omtrdc.net`만듭니다. 예를 들어 클라이언트 코드가 사용자 이름이고 제안된 호스트 이름이 `target.example.com`인 경우 DNS CNAME 레코드는 다음과 같이 표시됩니다.

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

1. CNAME [지원을](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C) 요청하는 Adobe Client Care 티켓을 [!DNL Target] 엽니다.

   Adobe는 DigiCert와 협력하여 Adobe의 프로덕션 서버에 인증서를 구매하고 배포합니다. DigiCert는 DCV 프로세스를 시작하고 구현 준비가 되면 Adobe Client Care에서 알려줍니다.

1. 이전 작업을 완료하고 Adobe Client Care에서 구현 준비가 되었음을 통보하면 at.js에서 새 CNAME으로 업데이트해야 `serverDomain` 합니다.

## FAQ

다음 정보는 에서 CNAME 지원 요청 및 구현에 대한 FAQ를 [!DNL Target]제공합니다.

### 직접 인증서(BYOC 또는 BYOC라고도 함)를 제공할 수 있습니까? 그렇다면, 어떻게 해야 합니까?

예. 고유한 인증서를 제공할 수 있습니다.그러나 권장되지 않습니다. Adobe에서 인증서를 구매하고 제어할 때 SSL 인증서 라이프사이클의 관리가 Adobe와 사용자 모두에게 매우 쉬워졌습니다. SSL 인증서는 매년 갱신되어야 합니다. 즉, Adobe Client Care는 매년 귀하에게 연락하여 Adobe에 적시에 새로운 인증서를 보내야 합니다. 일부 고객은 인증서가 만료되면 브라우저가 연결을 거부하기 때문에 매년 적시에 갱신된 인증서를 만드는 데 어려움을 겪을 수 있습니다. [!DNL Target]

>[!IMPORTANT]
>
>CNAME [!DNL Target] 가져오기를 요청하는 경우 매년 Adobe Client Care에 갱신된 인증서를 제공할 책임이 있습니다. Adobe에서 갱신된 인증서를 배포하기 전에 CNAME 인증서가 만료되도록 허용하면 특정 [!DNL Target] 구현에 대한 중단이 발생합니다.

1. 위의 1단계를 건너뛰고 2단계와 3단계를 완료합니다. Adobe Client Care 티켓(3단계)을 열었을 때, 사용자에게 자신의 인증서를 제공할 것임을 알립니다.

   Adobe에서 인증서 서명 요청(CSR)을 생성하고 발송합니다.

1. CSR을 사용하여 선택한 인증 기관(CA)을 통해 인증서를 구매합니다.

1. 새 공개 인증서를 Adobe에 보냅니다. Adobe 담당자가 프로덕션 서버에 공용 인증서를 배포합니다.

1. Adobe Client Care에서 구현 준비가 되었음을 통보하면 4단계를 완료하십시오.

### 새 SSL 인증서가 만료될 때까지 얼마나 걸립니까?

2020년 9월 1일 이전에 발급된 인증서는 2년 인증입니다. 2020년 9월 1일 이후에 발행된 인증서는 1년 인증서가 됩니다. 1년 인증서로 전환하는 방법에 대한 자세한 내용을 [여기에서](https://www.digicert.com/position-on-1-year-certificates)확인할 수 있습니다.

### 어떤 호스트 이름을 선택해야 합니까? 도메인당 호스트 이름은 몇 개입니까?

[!DNL Target] CNAME 구현에는 SSL 인증서 및 고객의 DNS에 도메인에 대해 하나의 호스트 이름만 있으면 되므로 권장됩니다. 일부 고객은 고유한 목적(예: 스테이징에서 테스트)을 위해 도메인당 추가 호스트 이름이 필요할 수 있습니다. 이 작업은 지원됩니다.

대부분의 고객은 호스트 이름 같은 `target.example.com`것을 선택하므로 권장하지만 선택은 궁극적으로 귀하의 것입니다. 기존 DNS 레코드의 호스트 이름을 요청하면 CNAME 요청의 충돌 및 해결 시간이 지연되므로 [!DNL Target] 안 됩니다.

### 에 대한 CNAME 구현이 이미 있습니다. [!DNL Adobe Analytics]동일한 인증서 또는 호스트 이름을 사용할 수 있습니까?

아니요. [!DNL Target] 별도의 호스트 이름과 인증서가 필요합니다.

### Target의 현재 구현이 ITP 2.1 또는 2.2의 영향을 받습니까?

Safari 브라우저에서 Target JavaScript 라이브러리가 있는 웹 사이트로 이동합니다. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.1 or 2.2.

Analytics CNAME만 있는 Target에 대해 ITP 문제를 해결할 수 있습니다. Target이 차단되는 광고 차단 시나리오의 경우에만 별도의 Target CNAME이 필요합니다.

ITP에 대한 자세한 내용은 Apple Intelligent [Tracking Prevention(ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)를 참조하십시오.

### Adobe/DigiCert에서 DCV 이메일을 다른 이메일 주소로 보낼 수 `<someone>@example.com`있습니까?

아니요. DigiCert(또는 인증 기관)는 도메인의 WHOIS 정보 또는 미리 결정된 주소 목록(위 참조)에도 이메일 주소가 포함되어 있지 않은 경우 동일한 도메인 아래에 이메일 주소를 가진 사람만이 SSL 인증서를 인증하도록 허용하지 않습니다. 이렇게 하면 권한이 있는 사용자만 특정 도메인에 대해 DCV를 승인할 수 있습니다. 이 방법을 사용할 수 없는 경우 DNS CNAME DCV 메서드를 사용하는 것이 좋습니다(위 참조).

### CNAME 구현이 트래픽을 위해 준비되었는지 어떻게 확인할 수 있습니까?

bash 및 curl 7.49+를 사용하는 MacOs 또는 Linux 명령줄 터미널에서는 다음 명령 세트를 사용합니다.

1. 먼저 이 bash 함수를 터미널에 붙여 넣습니다.

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{17,21,22,26,{28..32},34,35,37,38}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. 다음 단계에 이 명령을 붙여 넣습니다(호스트 이름으로 `target.example.com` 대체).

   ```
   validateEdgeFpsslSni target.example.com
   ```

   구현이 준비되면 아래와 같이 출력물이 표시됩니다. 중요한 부분은 원하는 호스트 이름과 일치하는 모든 라인이 표시된다는 `CN=target.example.com`것입니다. 표시되는 `CN=*.tt.omtrdc.net`경우 구현이 준비되지 **않았습니다** .

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge17.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge21.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge22.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge26.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge28.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge29.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge30.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge37.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge38.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. 새로운 DNS CNAME을 다른 curl 요청과 함께 확인할 수 있습니다. `CN=target.example.com`다음과 같습니다.

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >이 명령이 실패했지만 위의 `validateEdgeFpsslSni` 명령이 성공하면 DNS 업데이트가 완전히 전파될 때까지 기다려야 할 수 있습니다. DNS 레코드에는 TTL [(time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) 이 연결되어 있으므로 해당 레코드의 DNS 답글에 대한 캐시 만료 시간이 지정되므로 TTL이 있는 한 기다려야 할 수 있습니다. 명령이나 G Suite `dig target.example.com` 도구 상자를 사용하여 [](https://toolbox.googleapps.com/apps/dig/#CNAME) 특정 TTL을 조회할 수 있습니다.
