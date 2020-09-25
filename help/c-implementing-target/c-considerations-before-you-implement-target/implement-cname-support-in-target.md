---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Adobe Target에서 CNAME(표준 이름) 지원을 구현하기 위한 Adobe Client Care 작업 정보입니다.
title: CNAME 및 Adobe Target
feature: privacy and security
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 6922b80c88cbd2947c3bfd0cc9d8409ff5dcdcd0
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 2%

---


# CNAME 및 Adobe Target {#cname-and-adobe-target}

CNAME(표준 이름) 지원을 구현하기 위한 Adobe 클라이언트 지원 작업에 대한 지침 [!DNL Adobe Target]. 광고 차단 문제 또는 ITP 관련 쿠키 정책을 처리하기 위해 CNAME이 사용되므로 Adobe이 소유한 도메인이 아닌 고객이 소유한 도메인에 대한 호출이 수행됩니다.

## CNAME 지원 요청

Perform the following steps to request CNAME support in [!DNL Target]:

1. SSL 인증서에 필요한 호스트 이름 목록을 결정합니다(FAQ 참조).

1. 각 호스트 이름에 대해 DNS에 일반 [!DNL Target] 호스트 이름을 가리키는 CNAME 레코드를 만듭니다 `clientcode.tt.omtrdc.net`.

   예를 들어 클라이언트 코드가 &quot;사용자 이름 지정&quot;이고 제안된 호스트 이름이 `target.example.com`인 경우 DNS CNAME 레코드는 다음과 같이 표시됩니다.

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!NOTE]
   >
   >Adobe 인증 기관인 DigiCert는 이 단계가 완료될 때까지 인증서를 발급할 수 없습니다. 따라서 Adobe은 이 단계가 완료될 때까지 CNAME 구현에 대한 요청을 이행할 수 없습니다.

1. [CNAME 지원을 요청하는 Adobe 클라이언트 지원 티켓을](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/assets/FPC_Request_Form.xlsx) 열 때 이 양식을 작성하고 포함시키십시오 [](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

   * Adobe [!DNL Target] client code:
   * SSL 인증서 호스트 이름(예: `target.example.com target.example.org`):
   * SSL 인증서 구매자(Adobe 권장):Adobe/고객
   * 고객이 인증서(BYOC)를 구입하는 경우 다음과 같은 추가 정보를 작성해 주십시오.
      * 인증서 조직(예:예제 Company Inc):
      * 인증서 조직 단위(선택 사항:마케팅):
      * 인증서 국가(예:미국):
      * 인증서 상태/지역(예:캘리포니아):
      * 인증서 구/군/시(예:산호세):

1. Adobe이 인증서를 구입하는 경우 Adobe은 DigiCert와 함께 작동하여 Adobe 프로덕션 서버에 인증서를 구매하고 배포합니다.

   고객이 인증서(BYOC)를 구입하는 경우, Adobe 클라이언트 지원팀은 CSR(인증서 서명 요청)을 보내드립니다. 이 요청은 인증서 기관을 통해 인증서를 구매할 때 사용해야 합니다. 인증서가 발급되면 인증서 사본과 중간 인증서 사본을 Adobe 클라이언트 지원팀에 보내 배포해야 합니다.

   Adobe 클라이언트 지원 센터에서 구현이 준비되면 알려줍니다.

1. 이전 작업을 완료하고 Adobe 클라이언트 지원팀이 구현 준비가 되었다는 알림을 보낸 후 at.js에서 새 CNAME `serverDomain` 으로 업데이트해야 합니다.

## FAQ

다음 정보는 CNAME 지원 요청 및 구현과 관련하여 자주 묻는 질문에 대한 답변입니다 [!DNL Target].

### 직접 인증서를 제공할 수 있습니까(BYOC 또는 BYOC)?

예. 자신의 인증서를 제공할 수 있습니다.하지만 권장되지 않습니다. Adobe 구입 및 인증서 제어 시 SSL 인증서 라이프사이클의 관리가 매우 쉬워졌습니다. SSL 인증서는 매년 갱신되어야 합니다. 즉, Adobe 클라이언트 지원 팀은 Adobe에 적시에 새 인증서를 보내기 위해 매년 사용자에게 연락해야 합니다. 인증서 만료 시 브라우저 거부 때문에 [!DNL Target] 구현을 저해하는 새로운 인증서를 매년 적시에 만드는 데 어려움을 겪을 수도 있습니다.

>[!IMPORTANT]
>
>CNAME 구현 [!DNL Target] 가져오기를 요청하는 경우 매년 Adobe 클라이언트 지원팀에 갱신된 인증서를 제공할 책임이 있습니다. Adobe에서 갱신된 인증서를 배포하기 전에 CNAME 인증서가 만료되도록 허용하면 특정 구현에 대한 중단이 [!DNL Target] 발생합니다.

### 새 SSL 인증서가 만료될 때까지 얼마나 걸립니까?

2020년 9월 1일 이전에 발급된 인증서는 2년 동안 인증될 예정입니다. 2020년 9월 1일 이후에 발급되는 인증서는 1년 인증서가 됩니다. 1년 인증서로 이동하는 방법에 대한 자세한 내용을 [여기에서 확인할 수 있습니다](https://www.digicert.com/position-on-1-year-certificates).

### 어떤 호스트 이름을 선택해야 합니까? 도메인당 호스트 이름 수를 선택해야 합니까?

[!DNL Target] CNAME 구현에는 SSL 인증서 및 고객의 DNS에 도메인당 하나의 호스트 이름만 필요하므로 권장됩니다. 일부 고객은 고유한 목적(예: 스테이징에서 테스트)으로 지원되는 도메인당 추가 호스트 이름이 필요할 수 있습니다.

대부분의 고객은 호스트 이름 `target.example.com`을 선택하므로 권장하지만 선택은 궁극적으로 귀하의 것입니다. 기존 DNS 레코드의 호스트 이름을 요청하면 CNAME 요청 해결 시 충돌과 지연 시간이 발생하므로 [!DNL Target] 요청하지 마십시오.

### 에 대한 CNAME 구현이 이미 있습니다. 동일한 인증서 또 [!DNL Adobe Analytics]는 호스트 이름을 사용할 수 있습니까?

아니요. 별도의 호스트 이름과 인증서가 [!DNL Target] 필요합니다.

### 현재 구현된 Target이 ITP 2.x에 영향을 받습니까?

Safari 브라우저에서 Target JavaScript 라이브러리가 있는 웹 사이트로 이동합니다. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.x.

Analytics CNAME만 있는 Target에 대해 ITP 문제를 해결할 수 있습니다. Target이 차단된 광고 차단 시나리오의 경우에만 별도의 Target CNAME이 필요합니다.

ITP에 대한 자세한 내용은 [Apple ITP(Intelligent Tracking Prevention) 2.x를 참조하십시오](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### CNAME 구현이 배포되면 어떤 유형의 서비스 장애가 발생할 수 있습니까?

인증서를 배포(인증서 갱신 포함)할 때 서비스 중단은 발생하지 않습니다. 그러나 구현 코드(at.js [!DNL Target] 에서)의 호스트 이름을 새로운 CNAME 호스트 이름(`serverDomain` )으로 변경하면 웹 브라우저는 돌아온 방문자를 새로운 방문자로 취급하며, 브라우저 보안 모델로 인해 이전 쿠키는 이전 호스트 이름(`target.example.com``clientcode.tt.omtrdc.net`)에서 액세스할 수 없기 때문에 프로필 데이터가 유실됩니다. 이는 새로운 CNAME에 대한 초기 컷오버 시 일회성 중단입니다. 호스트 이름이 변경되지 않으므로 인증서 갱신에 동일한 효과가 없습니다.

### CNAME 구현에 어떤 키 유형 및 인증서 서명 알고리즘이 사용됩니까?

모든 인증서는 RSA SHA-256이고 키는 기본적으로 RSA 2048비트입니다. 2048비트보다 큰 키 크기는 현재 지원되지 않습니다.

### CNAME 구현이 트래픽을 위해 준비되었는지 어떻게 확인할 수 있습니까?

다음과 같은 명령 세트를 사용합니다(MacOs 또는 Linux 명령줄 터미널에서는 bash 및 curl 7.49+ 사용).

1. 먼저 이 배쉬 함수를 터미널에 붙여넣습니다.

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. 다음 단계에 이 명령을 붙여넣습니다(호스트 이름 `target.example.com` 으로 대체).

   ```
   validateEdgeFpsslSni target.example.com
   ```

   구현이 준비되면 아래와 같은 결과가 표시됩니다. 중요한 부분은 원하는 호스트 이름 `CN=target.example.com`과 일치하는 모든 라인이 표시된다는 것입니다. 이러한 항목 중 하나라도 나타나면 구현 `CN=*.tt.omtrdc.net`이 **준비되지** 않습니다.

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

1. 다음과 같이 새로운 DNS CNAME을 다른 말림 요청과 함께 확인합니다. `CN=target.example.com`

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >이 명령이 실패했지만 위의 `validateEdgeFpsslSni` 명령이 성공하면 DNS 업데이트가 완전히 전파될 때까지 기다려야 할 수 있습니다. DNS 레코드에는 해당 레코드 [의 DNS 답글에 대한 캐시 만료 시간을 지정하는 관련 TTL(](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) Time-to-Live)이 있으므로 TTL이 있을 때까지 기다려야 할 수 있습니다. 명령 또는 G Suite 도구 상자 `dig target.example.com` [](https://toolbox.googleapps.com/apps/dig/#CNAME) 를 사용하여 특정 TTL을 확인할 수 있습니다.

## 알려진 제한 사항

* CNAME과 at.js 1.x가 있는 경우 QA 모드는 타사 쿠키를 기반으로 하므로 고정되지 않습니다. 해결 방법은 탐색하는 각 URL에 미리 보기 매개 변수를 추가하는 것입니다. CNAME과 at.js 2.x가 있는 경우 QA 모드가 고정됩니다.
* 현재 이 `overrideMboxEdgeServer` 설정은 CNAME에서 제대로 작동하지 않습니다. 요청 `false` 실패를 방지하기 위해 이 값을 설정해야 합니다.
* CNAME을 사용하는 경우 Target 호출에 대한 쿠키 헤더 크기가 증가할 가능성이 커집니다. 쿠키 크기를 8KB 이하로 유지하는 것이 좋습니다.
