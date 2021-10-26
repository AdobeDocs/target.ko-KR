---
keywords: 클라이언트 관리;cname;인증서 프로그램;표준 이름;쿠키;인증서;amc;adobe 관리 인증서;digicert;도메인 제어 유효성 검사;dcv
description: Adobe 클라이언트 지원팀과 협력하여 Adobe에서 CNAME(표준 이름) 지원을 구현하십시오 [!DNL Target] 광고 차단 문제를 처리하려면 다음을 수행하십시오.
title: Target에서 CNAME을 어떻게 사용합니까?
feature: Privacy & Security
role: Developer
exl-id: bf533771-6d46-48ba-964c-3ad9ce9f7352
source-git-commit: e51c7805939e8bf32d7f358036c9070931580187
workflow-type: tm+mt
source-wordcount: '1165'
ht-degree: 1%

---

# CNAME 및 Target

작업 지침 [!DNL Adobe] Client Care에서 CNAME(표준 이름) 지원을 구현하십시오. [!DNL Adobe Target]. CNAME을 사용하여 광고 차단 문제 또는 ITP 관련(Intelligent Tracking Prevention) 쿠키 정책을 처리합니다. CNAME을 사용하면 가 소유한 도메인이 아니라 고객이 소유한 도메인이 호출됩니다 [!DNL Adobe].

## Target에서 CNAME 지원 요청

1. SSL 인증서에 필요한 호스트 이름 목록을 확인합니다(아래 FAQ 참조).

1. 각 호스트 이름에 대해 일반을 가리키는 DNS에 CNAME 레코드를 만듭니다 [!DNL Target] 호스트 이름 `clientcode.tt.omtrdc.net`.

   예를 들어 클라이언트 코드가 &quot;고객&quot;이고 제안된 호스트 이름이 인 경우 `target.example.com`, DNS CNAME 레코드는 다음과 유사합니다.

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   >이 단계를 완료할 때까지 Adobe의 인증 기관인 DigiCert에서 인증서를 발급할 수 없습니다. 따라서, [!DNL Adobe] 이 단계가 완료되기 전까지는 CNAME 구현 요청을 완료할 수 없습니다.

1. [이 양식을 작성하세요](/help/assets/FPC_Request_Form.xlsx) 그리고 [CNAME 지원을 요청하는 Adobe Client Care 티켓을 엽니다.](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C):

   * Adobe [!DNL Target] 클라이언트 코드:
   * SSL 인증서 호스트 이름(예: `target.example.com target.example.org`):
   * SSL 인증서 구매자(Adobe이 적극 권장됩니다. FAQ 참조): Adobe/고객
   * 고객이 &quot;BYOC(Bring Your Own Certificate)&quot;라고도 하는 인증서를 구매하는 경우 다음 추가 정보를 채우십시오.
      * 인증서 조직(예: 예제 Company Inc):
      * 인증서 조직 단위(선택 사항, 예: 마케팅):
      * 인증서 국가(예: 미국):
      * 인증서 상태/지역(예: 캘리포니아):
      * 인증서 구/군/시(예: San Jose):

1. If [!DNL Adobe] 인증서를 구입하고 있는데 [!DNL Adobe] 는 DigiCert와 협력하여 Adobe의 프로덕션 서버에서 인증서를 구매하고 배포합니다.

   고객이 BYOC(인증서를 구매하는 경우 [!DNL Adobe] Client Care에서 CSR(인증서 서명 요청)을 보냅니다. 원하는 인증 기관을 통해 인증서를 구입할 때 CSR을 사용하십시오. 인증서가 발급되면 인증서 및 중간 인증서 사본을 로 보냅니다 [!DNL Adobe] 배포를 위한 클라이언트 지원

   [!DNL Adobe] 구현이 준비되면 Client Care에서 알려줍니다.

1. 업데이트 `serverDomain` ([설명서](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#serverDomain))를 새 CNAME 호스트 이름으로 설정하고 설정합니다. `overrideMboxEdgeServer` to `false` ([설명서](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#overridemboxedgeserver)) 내의 아무 곳에나 삽입할 수 있습니다.

## FAQ

다음 정보는에서 CNAME 지원 요청 및 구현에 대해 자주 묻는 질문과 대답(FAQ)입니다 [!DNL Target]:

### 자체 인증서를 제공할 수 있습니까(자체 인증서 또는 BYOC 가져오기)?

자체 인증서를 제공할 수 있습니다. 하지만, [!DNL Adobe] 이 방법은 권장되지 않습니다. 두 작업 모두에 SSL 인증서 수명 주기 관리가 더 쉽습니다 [!DNL Adobe] 만약 [!DNL Adobe] 인증서를 구매하고 제어합니다. SSL 인증서는 매년 갱신되어야 합니다. 따라서, [!DNL Adobe] Client Care는 적시에 새 인증서를 받으려면 매년 사용자에게 연락해야 합니다. 일부 고객은 적시에 갱신된 인증서를 생산하기 어려울 수 있습니다. 사용자 [!DNL Target] 브라우저가 연결을 거부하므로 인증서가 만료되면 구현이 위험해집니다.

>[!IMPORTANT]
>
>요청 시 [!DNL Target] 자체 인증서 CNAME 구현을 통해 갱신된 인증서를 [!DNL Adobe] 매년 고객 지원 센터. CNAME 인증서가 만료되기 전에 만료되도록 허용 [!DNL Adobe] 를 통해 갱신된 인증서를 배포하면 특정 항목에 대해 중단이 발생합니다 [!DNL Target] 구현 을 참조하십시오.

### 새 SSL 인증서가 만료될 때까지 얼마나 걸립니까?

Adobe에서 구매한 모든 인증서는 1년 동안 유효합니다. 자세한 내용은 [1년 인증서에 대한 DigiCert 문서](https://www.digicert.com/blog/position-on-1-year-certificates) 추가 정보.

### 어떤 호스트 이름을 선택해야 합니까? 도메인당 호스트 이름은 몇 개까지 선택해야 합니까?

[!DNL Target] CNAME 구현에는 SSL 인증서 및 고객의 DNS의 도메인당 하나의 호스트 이름만 필요합니다. Adobe은 도메인당 하나의 호스트 이름을 권장합니다. 일부 고객은 고유한 목적(예: 스테이징에서 테스트)을 위해 도메인당 더 많은 호스트 이름을 요구합니다.

대부분의 고객은 다음과 같은 호스트 이름을 선택합니다. `target.example.com`. Adobe은 이 방법을 권장하지만, 선택은 궁극적으로 본인의 것입니다. 기존 DNS 레코드의 호스트 이름을 요청하지 마십시오. 이렇게 하면 충돌이 발생하고 해결 시간이 지연됩니다 [!DNL Target] CNAME 요청.

### 에 대한 CNAME 구현이 이미 있습니다. [!DNL Adobe Analytics]과 같은 인증서 또는 호스트 이름을 사용할 수 있습니까?

아니요 [!DNL Target] 별도의 호스트 이름과 인증서가 필요합니다.

### 현재 구현된 [!DNL Target] ITP 2.x의 영향을 받습니까?

Apple ITP(Intelligent Tracking Prevention) 버전 2.3에는 Adobe Target CNAME 구현을 검색하고 쿠키의 만료를 7일로 줄일 수 있는 CNAME 클로킹 완화 기능이 도입되었습니다. 현재 [!DNL Target] 에는 ITP의 CNAME 클로킹 완화에 대한 해결 방법이 없습니다. ITP에 대한 자세한 내용은 [Apple ITP(Intelligent Tracking Prevention) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).


### CNAME 구현을 배포할 때 어떤 서비스 중단을 예상할 수 있습니까?

인증서가 배포될 때(인증서 갱신 포함) 서비스가 중단되지 않습니다.

그러나 호스트 이름을 변경한 후에는 [!DNL Target] 구현 코드 (`serverDomain` at.js에서 새 CNAME 호스트 이름( )에 대해`target.example.com`). 웹 브라우저는 재방문자를 새 방문자로 처리합니다. 이전 쿠키는 이전 호스트 이름(`clientcode.tt.omtrdc.net`). 브라우저 보안 모델로 인해 이전 쿠키에 액세스할 수 없습니다. 이 중단은 새 CNAME에 대한 초기 전환 시에만 발생합니다. 호스트 이름이 변경되지 않으므로 인증서 갱신에도 동일한 효과가 없습니다.

### CNAME 구현에 사용되는 키 유형 및 인증서 서명 알고리즘은 무엇입니까?

모든 인증서는 RSA SHA-256이며 키는 기본적으로 RSA 2048비트입니다. 2048비트보다 큰 키 크기는 현재 지원되지 않습니다.

### CNAME 구현이 트래픽에 대비하는 준비가 되었는지 어떻게 확인할 수 있습니까?

macOS 또는 Linux 명령줄 단말에서 bash 및 curl >=7.49를 사용하여 다음 명령 세트를 사용합니다.

1. 이 bash 함수를 복사하여 터미널에 붙여넣거나 Bash 시작 스크립트 파일(일반적으로 `~/.bash_profile` 또는 `~/.bashrc`) 따라서 이 함수를 터미널 세션 간에 사용할 수 있습니다.

   ```
   function adobeTargetCnameValidation {
     local hostname="$1"
     if [ -z "$hostname" ]; then
       echo "ERROR: no hostname specified"
       return 1
     fi
   
     local service="Adobe Target CNAME implementation"
     local edges="31 32 34 35 36 37 38"
     local edgeDomain="tt.omtrdc.net"
     local edgeFormat="mboxedge%d%s.$edgeDomain"
     local shardFormat="-alb%02d"
     local shards=5
     local shardsFoundCount=0
     local shardsFound
     local shardsFoundOutput
     local curlRegex="subject:.*CN=|expire date:|issuer:"
     local curlValidation="SSL certificate verify ok"
     local curlResponseValidation='"OK"'
     local curlEndpoint="/uptime?mboxClient=uptime3"
     local url="https://$hostname$curlEndpoint"
     local sslLabsUrl="https://ssllabs.com/ssltest/analyze.html?hideResults=on&latest&d=$hostname"
     local success="✅"
     local failure="🚫"
     local info="🔎"
     local rule="="
     local horizontalRule="$(seq ${COLUMNS:-30} | xargs printf "$rule%.0s")"
     local miniRule="$(seq 5 | xargs printf "$rule%.0s")"
     local curlVersion="$(curl --version | head -1 | cut -d' ' -f2 )"
     local curlVersionRequired=">=7.49"
     local edgeCount="$(wc -w <<< "$edges" | tr -d ' ')"
     local edge
     local shard
     local currEdgeShard
     local dnsOutput
     local cnameExists
     local endToEndTestSucceeded
     local curlResult
   
     for shard in $(seq $shards); do
       if [ "$shardsFoundCount" -eq 0 ]; then
         for edge in $edges; do
           if [ "$shard" -eq 1 ]; then
             currEdgeShard="$(printf "$edgeFormat" "$edge" "")"
           else
             currEdgeShard="$(
               printf "$edgeFormat" "$edge" "$(
                 printf -- "$shardFormat" "$shard"
               )"
             )"
           fi
           curlResult="$(curl -vsm20 --connect-to "$hostname:443:$currEdgeShard:443" "$url" 2>&1)"
           if grep -q "$curlValidation" <<< "$curlResult"; then
             shardsFound+=" $currEdgeShard"
             if grep -q "$curlResponseValidation" <<< "$curlResult"; then
               shardsFoundCount=$((shardsFoundCount+1))
               shardsFoundOutput+="\n\n$miniRule $success $hostname [edge shard: $currEdgeShard] $miniRule\n"
             else
               shardsFoundOutput+="\n\n$miniRule $failure $hostname [edge shard: $currEdgeShard] $miniRule\n"
             fi
             shardsFoundOutput+="$(grep -E "$curlRegex" <<< "$curlResult" | sort)"
             if ! grep -q "$curlResponseValidation" <<< "$curlResult"; then
               shardsFoundOutput+="\nERROR: unexpected HTTP response from this shard using $url"
             fi
           fi
         done
       fi
     done
   
     echo
     echo "$horizontalRule"
     echo
     echo "$service validation for hostname $hostname:"
     dnsOutput="$(dig -t CNAME +short "$hostname" 2>&1)"
     if grep -qFi ".$edgeDomain" <<< "$dnsOutput"; then
       echo "$success $hostname passes DNS CNAME validation"
       cnameExists=true
     else
       echo -n "$failure $hostname FAILED DNS CNAME validation -- "
       if [ -n "$dnsOutput" ]; then
         echo -e "$dnsOutput is not in the subdomain $edgeDomain"
       else
         echo "required DNS CNAME record pointing to <target-client-code>.$edgeDomain not found"
       fi
     fi
   
     curlResult="$(curl -vsm20 "$url" 2>&1)"
     if grep -q "$curlValidation" <<< "$curlResult"; then
       if grep -q "$curlResponseValidation" <<< "$curlResult"; then
         echo -en "$success $hostname passes TLS and HTTP response validation"
         if [ -n "$cnameExists" ]; then
           echo
         else
           echo " -- the DNS CNAME is not pointing to the correct subdomain for ${service}s with Adobe-managed certificates" \
             "(bring-your-own-certificate implementations don't have this requirement), but this test passes as configured"
         fi
         endToEndTestSucceeded=true
       else
         echo -n "$failure $hostname FAILED HTTP response validation --" \
           "unexpected response from $url -- "
         if [ -n "$cnameExists" ]; then
           echo "DNS is NOT pointing to the correct shard, notify Adobe Client Care"
         else
           echo "the required DNS CNAME record is missing, see above"
         fi
       fi
     else
   
       echo -n "$failure $hostname FAILED TLS validation -- "
       if [ -n "$cnameExists" ]; then
         echo "DNS is likely NOT pointing to the correct shard or there's a validation issue with the certificate or" \
           "protocols, see curl output below and optionally SSL Labs ($sslLabsUrl):"
         echo ""
         echo "$horizontalRule"
         echo "$curlResult" | sed 's/^/    /g'
         echo "$horizontalRule"
         echo ""
       else
         echo "the required DNS CNAME record is missing, see above"
       fi
     fi
   
     if [ "$shardsFoundCount" -ge "$edgeCount" ]; then
       echo -n "$success $hostname passes shard validation for the following $shardsFoundCount edge shards:"
       echo -e "$shardsFoundOutput"
       echo
   
       if [ -n "$cnameExists" ] && [ -n "$endToEndTestSucceeded" ]; then
         echo "$horizontalRule"
         echo ""
         echo "  For additional TLS/SSL validation, including detailed browser/client support,"
         echo "  see SSL Labs (click the first IP address if prompted):"
         echo ""
         echo "    $info  $sslLabsUrl"
         echo ""
         echo "  To check DNS propagation around the world, see whatsmydns.net:"
         echo ""
         echo "    $info  DNS A records:     https://whatsmydns.net/#A/$hostname"
         echo "    $info  DNS CNAME record:  https://whatsmydns.net/#CNAME/$hostname"
       fi
     else
       echo -n "$failure $hostname FAILED shard validation -- shards found: $shardsFoundCount," \
         "expected: $edgeCount"
       if bc -l <<< "$(cut -d. -f1,2 <<< "$curlVersion") $curlVersionRequired" 2>/dev/null | grep -q 0; then
         echo -n " -- insufficient curl version installed: $curlVersion, but this script requires curl version" \
           "$curlVersionRequired because it uses the curl --connect-to flag to bypass DNS and directly test" \
           "each Adobe Target edge shards' SNI confirguation for $hostname"
       fi
       if [ -n "$shardsFoundOutput" ]; then
         echo -e ":\n$shardsFoundOutput"
       fi
       echo
     fi
     echo
     echo "$horizontalRule"
     echo
   }
   ```

1. 이 명령 붙여넣기(바꾸기) `target.example.com` 호스트 이름 사용):

   ```
   adobeTargetCnameValidation target.example.com
   ```

   구현이 준비되면 다음과 같은 출력이 표시됩니다. 중요한 부분은 모든 검증 상태 라인이 `✅` 보다는 `🚫`. 각 [!DNL Target] edge CNAME 공유에는 `CN=target.example.com`: 요청된 인증서의 기본 호스트 이름과 일치하는 호스트 이름(인증서에 있는 추가 SAN 호스트 이름이 이 출력에서 인쇄되지 않음)입니다.

   ```
   $ adobeTargetCnameValidation target.example.com
   
   ==========================================================
   
   Adobe Target CNAME implementation validation for hostname target.example.com:
   ✅ target.example.com passes DNS CNAME validation
   ✅ target.example.com passes TLS and HTTP response validation
   ✅ target.example.com passes shard validation for the following 7 edge shards:
   
   ===== ✅ target.example.com [edge shard: mboxedge31-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge32-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge34-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge35-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge36-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge37-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge38-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ==========================================================
   
     For additional TLS/SSL validation, including detailed browser/client support,
     see SSL Labs (click the first IP address if prompted):
   
       🔎  https://ssllabs.com/ssltest/analyze.html?hideResults=on&latest&d=target.example.com
   
     To check DNS propagation around the world, see whatsmydns.net:
   
       🔎  DNS A records:     https://whatsmydns.net/#A/target.example.com
       🔎  DNS CNAME record:  https://whatsmydns.net/#CNAME/target.example.com
   
   ==========================================================
   ```

   >[!NOTE]
   >
   >이 유효성 검사 명령이 DNS 유효성 검사에 실패했지만 이미 필요한 DNS 변경을 수행한 경우에는 DNS 업데이트가 완전히 전파될 때까지 기다려야 할 수 있습니다. DNS 레코드에 연결된 [TTL(time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) 이는 해당 레코드의 DNS 응답에 대한 캐시 만료 시간을 지시합니다. 따라서 TTL만 있으면 대기해야 할 수 있습니다. 를 사용할 수 있습니다 `dig target.example.com` 명령 또는 [G Suite 도구 상자](https://toolbox.googleapps.com/apps/dig/#CNAME) 추가 TTL을 참조하십시오. 전 세계 DNS 전달을 확인하려면 다음을 참조하십시오 [whatsmydns.net](https://whatsmydns.net/#CNAME).

### CNAME으로 옵트아웃 링크를 사용하는 방법

CNAME을 사용하는 경우 옵트아웃 링크에 &quot;client=&quot;가 포함되어야 합니다.`clientcode` 매개 변수(예:
`https://my.cname.domain/optout?client=clientcode`.

바꾸기 `clientcode` 클라이언트 코드로 만든 다음 [옵트아웃 URL](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#reference_E7A62B7B99C94B3A806CB262D16E27FC).

## 알려진 제한 사항

* CNAME과 at.js 1.x가 있는 경우 QA 모드는 타사 쿠키를 기반으로 하므로 고정되지 않습니다. 해결 방법은 탐색하는 각 URL에 미리 보기 매개 변수를 추가하는 것입니다. CNAME과 at.js 2.x가 있는 경우 QA 모드가 고정됩니다.
* CNAME을 사용하는 경우 쿠키 헤더의 크기가 [!DNL Target] 호출이 증가합니다. [!DNL Adobe] 는 쿠키 크기를 8KB 미만으로 유지하는 것을 권장합니다.
