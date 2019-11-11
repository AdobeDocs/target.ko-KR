---
keywords: 클라이언트 지원;cname;인증서 프로그램;표준 이름;쿠키;인증서;amc;adobe 관리 인증서;digicert;도메인 제어 유효성 검사;dcv
description: Adobe Target에서 CNAME(표준 이름) 지원을 구현하기 위한 Adobe Client Care 작업 정보입니다.
title: CNAME 및 Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 117e4c8712d49a284331552268cec42bb34cf013

---


# CNAME 및 Adobe Target {#cname-and-adobe-target}

Instructions about working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. 광고 차단 문제 또는 ITP 관련 쿠키 정책을 처리하기 위해 CNAME이 사용되므로 Adobe가 소유한 도메인이 아닌 고객이 소유한 도메인에 대한 호출이 수행됩니다.

## CNAME 지원 요청

Perform the following steps to request CNAME support in [!DNL Target]:

1. Adobe의 인증 기관(DigiCert)은 Adobe가 도메인 아래에 인증서를 생성할 수 있도록 인증되었는지 확인해야 합니다.

   DigiCert가 이 프로세스를 [DCV](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) (Domain Control Validation)로 호출하며, 이 프로세스가 완료될 때까지 Adobe는 도메인 아래에 인증서를 생성할 수 없습니다.

   DCV는 몇 가지 방법을 사용하며 Adobe Client Care 티켓(3단계)을 열기 전에 몇 가지 가능한 작업을 수행하여 DCV 프로세스를 가속화할 수 있습니다.

   * DigiCert는 먼저 이메일 방법을 시도하게 됩니다. 이 방법을 사용하면 미리 결정된 이메일 주소(admin, administrator, webmaster, hostmaster 및 postmaster `@[domain_name]`)뿐만 아니라 도메인의 WHOIS 정보에 있는 주소로 이메일을 보냅니다. 자세한 내용은 [DCV 메서드 설명서를](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) 참조하십시오.

      DigiCert는 DCV 이메일 프로세스를 가속화하기 위해 다음 권장 사항을 제공합니다.

      "등록업체/WHOIS 공급자가 [관련 이메일 주소를]숨기거나 제거하지 않았는지 확인하십시오. 이러한 경우 [인증 기관이] 도메인의 WHOIS 데이터에 액세스할 수 있도록 하는 방법(예: 익명 이메일 주소, 웹 양식)을 제공하는지 확인하십시오."

   * DCV 이메일 방법이 옵션이 아닌 경우 다음 방법은 DNS TXT 메서드이며, 이 방법은 해시 값으로 DNS TXT 레코드를 도메인에 추가합니다. 이 TXT 레코드는 DigitalCert에 Adobe가 인증서를 생성할 권한이 있음을 나타냅니다. 이 방법을 사용해야 하는 경우 티켓을 열 때 Adobe Client Care에 알리십시오(3단계). 이렇게 하면 DCV 프로세스를 가속화할 수 있습니다.

1. 일반 호스트 이름을 가리키는 도메인의 DNS에 CNAME 레코드를 `clientcode.tt.omtrdc.net`만듭니다. 예를 들어 클라이언트 코드가 사용자 이름이고 제안된 호스트 이름이 `target.example.com`인 경우 DNS CNAME 레코드는 다음과 같이 표시됩니다.

   ```
   target.example.com  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

1. CNAME [지원을](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C) 요청하는 Adobe Client Care 티켓을 [!DNL Target] 엽니다.

   Adobe는 DigiCert와 협력하여 Adobe의 프로덕션 서버에 인증서를 구매하고 배포합니다. DigiCert는 DCV 프로세스를 시작하고 구현 준비가 되면 Adobe Client Care에서 알려줍니다.

1. 이전 작업을 완료하고 Adobe Client Care에서 구현 준비가 되었음을 통보하면 at.js에서 새 CNAME으로 업데이트해야 `serverDomain` 합니다.

## 자주 묻는 질문

다음 정보는 에서 CNAM 지원 요청 및 구현과 관련하여 자주 묻는 질문에 대한 답변을 [!DNL Target]제공합니다.

### 나만의 인증서를 제공할 수 있습니까? 그렇다면, 어떻게 해야 합니까?

예. 자신의 인증서를 제공하여 다음을 수행할 수 있습니다.

1. 위의 1단계를 건너뛰고 2단계와 3단계를 완료합니다. Adobe Client Care 티켓(3단계)을 열었을 때, 사용자에게 자신의 인증서를 제공할 것임을 알립니다.

   Adobe에서 인증서 서명 요청(CSR)을 생성하고 발송합니다.

1. CSR을 사용하여 선택한 인증 기관(CA)을 통해 인증서를 구매합니다.

1. 새 공개 인증서를 Adobe에 보냅니다. Adobe 담당자가 프로덕션 서버에 공용 인증서를 배포합니다.

1. Adobe Client Care에서 구현 준비가 되었음을 통보하면 4단계를 완료하십시오.

### 에 대한 CNAME 구현이 이미 있습니다. [!DNL Adobe Analytics]동일한 인증서 또는 호스트 이름을 사용할 수 있습니까?

아니요. [!DNL Target] 별도의 호스트 이름과 인증서가 필요합니다.

### CNAME 구현이 트래픽을 위해 준비되었는지 어떻게 확인할 수 있습니까?

bash 및 curl 7.49+를 사용하는 MacOs 또는 Linux 명령줄 터미널에서는 다음 명령 세트를 사용합니다.

1. 먼저 이 bash 함수를 터미널에 붙여 넣습니다.

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{17,21,22,26,{28..33}}.tt.omtrdc.net; do
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
   mboxedge33.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. 새로운 DNS CNAME을 다른 curl 요청과 함께 확인할 수 있습니다. `CN=target.example.com`다음과 같습니다.

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >이 명령이 실패했지만 위의 `validateEdgeFpsslSni` 명령이 성공하면 DNS 업데이트가 완전히 전파될 때까지 기다려야 할 수 있습니다.
