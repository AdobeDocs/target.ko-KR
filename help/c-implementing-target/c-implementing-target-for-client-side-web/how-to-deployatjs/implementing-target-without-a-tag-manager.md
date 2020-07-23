---
keywords: implement target;implementation;implement at.js;tag manager
description: 태그 관리자(Adobe Launch 또는 동적 태그 관리)를 사용하지 않고 Adobe Target을 구현하는 방법에 대한 정보입니다.
title: 태그 관리자 없이 Target 구현
subtopic: Getting Started
topic: Standard
uuid: 3ecc041a-42d8-40f8-90be-7856e1d3d080
translation-type: tm+mt
source-git-commit: 3edb13b196240bb1918fc66edcc653936e32d3ef
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 66%

---


# 태그 관리자 없이 Target 구현{#implement-target-without-a-tag-manager}

태그 관리자(또는)를 사용하지 [!DNL Adobe Target] 않고 구현하는[!DNL Adobe Launch] 방법에 대한 [!DNL Dynamic Tag Manager]정보입니다.

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25)는 Target 및 at.js 라이브러리를 구현하기 위해 선호되는 방법입니다. 다음 정보는 Adobe Launch를 사용하여 Target을 구현할 때 적용할 수 없습니다.

구현 [!UICONTROL 페이지에] 액세스하려면 **[!UICONTROL 관리]** > **[!UICONTROL 구현을]**&#x200B;클릭합니다.

이 페이지에서 다음 설정을 지정할 수 있습니다.

* 계정 세부 정보
* 구현 방법
* 프로필 API
* 디버거 도구
* 개인 정보 보호

>[!NOTE]
>
>Target Standard/Premium UI에서 또는 REST API를 사용하여 설정을 구성하는 대신, at.js 라이브러리에서 설정을 재정의할 수 있습니다. 자세한 내용은 [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)를 참조하십시오.

## 계정 세부 정보

다음 계정 세부 사항을 볼 수 있습니다. 이러한 설정은 변경할 수 없습니다.

| 설정 | 설명 |
| --- | --- |
| 클라이언트 코드 | 클라이언트 코드는 Target API를 사용할 때 종종 필요한 클라이언트별 문자 시퀀스입니다. |
| IMS 조직 ID | 이 ID는 구현을 [!DNL Adobe Experience Cloud] 계정에 연결합니다. |

## 구현 방법

[구현 방법] 패널에서 다음 설정을 구성할 수 있습니다.

### 전역 설정

>[!NOTE]
>
>이러한 설정은 모든 .js 라이브러리에 [!DNL Target] 적용됩니다. 구현 방법  섹션에서 변경 작업을 수행한 후 라이브러리를 다운로드하고 구현에서 업데이트해야 합니다.

|페이지 로드 활성화(전역 mbox 자동 만들기|전역 mbox 호출을 at.js 파일에 포함시켜 각 페이지 로드에서 자동으로 실행할지 여부를 선택합니다.|
|전역 mbox|전역 mbox의 이름을 선택합니다. 기본적으로 이 이름은 target-global-mbox입니다.<br>at.js를 사용하는 mbox 이름에 앰퍼샌드(&amp;)를 포함한 특수 문자를 사용할 수 있습니다.|
|Timeout (seconds)|If [!DNL Target] does not respond with content within the defined period, the server call times out and default content is displayed. 방문자 세션 동안 추가 호출이 계속 시도됩니다. 기본값은 5초입니다.<br>at.js 라이브러리는 `XMLHttpRequest`에서 시간 제한 설정을 사용합니다. 시간 제한은 요청이 시작되면 시작되고 [!DNL Target]이 서버의 응답을 받으면 중지됩니다. 자세한 내용은 Mozilla Developer Network의 [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout)을 참조하십시오.<br>응답을 받기 전에 지정된 시간 제한이 초과되면, 기본 컨텐츠가 표시되고, 모든 데이터 수집은 [!DNL Target] 에지에서 발생하므로 방문자는 활동의 참가자로 카운트될 수 있습니다. 요청이 [!DNL Target] 에지에 도달하면 방문자가 카운트됩니다.<br>시간 제한 설정을 구성할 때에는 다음 사항을 고려하십시오.<ul><li>값이 너무 낮으면, 방문자가 활동의 참가자로 카운트될 수 있음에도 불구하고 사용자에게 대부분의 시간 동안 기본 컨텐츠가 표시될 수 있습니다.</li><li>값이 너무 높으면, 확장된 기간 동안 본문 숨기기를 사용하는 경우 방문자에게 웹 페이지의 빈 영역이 표시되거나 빈 페이지가 표시될 수 있습니다.</li></ul>mbox 응답 시간을 자세히 알아보려면 브라우저의 개발자 도구에서 네트워크 탭을 살펴보십시오. 타사 웹 성과 모니터링 도구(예: Catchpoint)를 사용할 수도 있습니다.<br>**참고&#x200B;**:[visitorApiTimeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)설정은[!DNL Target]이 너무 오랫동안 방문자 API 응답을 기다리지 않도록 해줍니다. 이 설정과 여기에 설명된 at.js에 대한 시간 초과 설정은 서로 영향을 주지 않습니다.|
|프로필 라이프타임|이 설정은 방문자 프로필이 저장되는 기간을 결정합니다. 기본적으로, 프로필은 2주 동안 저장됩니다. 최대 90일까지 연장할 수 있습니다.<br>프로필 라이프타임 설정을 변경하려면[클라이언트 지원 팀에 문의하십시오](https://helpx.adobe.com/kr/contact/enterprise-support.ec.html).|

### 기본 구현 방법

>[!IMPORTANT]
>
>Target 팀은 at.js 1을 모두 지원합니다.*x*&#x200B;와 at.js 2.*x* 간의 매핑에 대해 설명합니다. 지원되는 버전을 실행하고 있는지 확인하려면 at.js의 주요 버전을 최신 버전으로 업그레이드하십시오.

원하는 at.js 버전을 다운로드하려면 해당 **[!UICONTROL 다운로드]** 단추를 클릭합니다.

at.js 설정을 편집하려면 원하는 at.js 버전 **[!UICONTROL 옆에]** 있는 편집을 클릭합니다.

>[!IMPORTANT]
>
>이러한 기본 설정을 변경하기 전에 현재 구현에 영향을 주지 않도록 [클라이언트](/help/cmp-resources-and-contact-information.md) 지원 센터에 문의하십시오.

위에 설명한 설정 외에 다음 특정 at.js 설정도 사용할 수 있습니다.

| 설정 | 설명 |
|--- |--- |
| 사용자 정의 라이브러리 헤더 | 라이브러리의 맨 위에 포함할 사용자 지정 JavaScript를 추가하십시오. |
| 사용자 정의 라이브러리 바닥글 | 라이브러리의 맨 아래에 포함할 사용자 지정 JavaScript를 추가하십시오. |

### 프로필 API

API를 통해 묶음 업데이트에 대한 인증을 활성화 또는 비활성화하고 프로필 인증 토큰을 생성합니다.

For more information, see [Profile API settings](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md).

### 디버거 도구

고급 디버깅 도구를 사용할 인증 토큰을 [!DNL Target] 생성합니다. Click **[!UICONTROL Generate New Authentication Token]**.

![새 인증 토큰 생성](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### 개인 정보 보호

이러한 설정을 통해 해당 데이터 개인 정보 보호 법 [!DNL Target] 을 준수할 수 있습니다.

방문자 IP 주소 난독화 드롭다운 목록에서 원하는 설정을 선택합니다.

* 마지막 난독화
* 전체 IP 난독화
* 없음

자세한 내용은 [개인 정보](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md)를 참조하십시오.

>[!NOTE]
>
>레거시 브라우저 지원 옵션은 at.js 버전 0.9.3 및 이전 버전에서 사용할 수 있었습니다. 이 선택 사항은 at.js 버전 0.9.4에서 제거되었습니다. at.js에서 지원하는 브라우저 목록이 필요하면 [지원되는 브라우저](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md)를 참조하십시오.<br>이전 브라우저는 CORS(Cross Origin Resource Sharing)를 완전히 지원하지는 않는 오래된 브라우저입니다. 이러한 브라우저에는 버전 11 이전의 Internet Explorer 브라우저와 Safari 버전 6 및 그 이전 버전이 포함됩니다. 기존 브라우저 지원이 비활성화된 경우, Target은 이러한 브라우저의 보고서에서 컨텐츠를 전달하거나 방문자 수를 계산하지 않았습니다. 이 옵션을 활성화한 경우, 좋은 고객 경험을 제공하기 위해 이전 브라우저에서 품질 보증을 수행하는 것이 좋습니다.

## at.js 다운로드{#concept_1E1F958F9CCC4E35AD97581EFAF659E2}를 참조하십시오 

Instructions to download the library using the [!DNL Target] interface or the Download API.

>[!NOTE]
>
>* [Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25)는 Target 및 at.js 라이브러리를 구현하기 위해 선호되는 방법입니다. 다음 정보는 Adobe Launch를 사용하여 Target을 구현할 때 적용할 수 없습니다.
   >
   >
* Target 팀은 at.js 1을 모두 지원합니다.*x*&#x200B;와 at.js 2.*x* 간의 매핑에 대해 설명합니다. 지원되는 버전을 실행하고 있는지 확인하려면 at.js의 주요 버전을 최신 버전으로 업그레이드하십시오. 각 버전에 대한 자세한 내용은 [at.js 버전 세부 사항](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)을 참조하십시오.


### Download at.js using the Target interface {#section_1F5EE401C2314338910FC57F9592894E}

[!DNL Target] 인터페이스에서 [!DNL at.js]를 다운로드하려면 다음을 수행하십시오.

1. 관리 **** > **[!UICONTROL 구현을 클릭합니다]**.
1. 구현 [!UICONTROL 방법] 섹션에서 원하는 at.js 버전 옆에 있는 **[!UICONTROL 다운로드]** 단추를 클릭합니다.

### Download at.js using the Target Download API {#section_C0D9D2A9068144708D08526BA5CA10D0}

API를 사용하여 [!DNL at.js]를 다운로드하려면 다음을 수행하십시오.

1. 클라이언트 코드를 가져옵니다.

   Your client code is available at the top of the **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** page of the [!DNL Target] interface.

1. 관리 번호를 가져옵니다.

   다음 URL을 로드하십시오.

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Replace `client code` with the client code from Step 1.

   이 URL을 로드한 결과는 다음 예와 유사해야 합니다.

   ```
   { 
     "api": "https://admin6.testandtarget.omniture.com/admin/rest/v1" 
   }
   ```

   이 예에서 &quot;6&quot;은 관리 번호입니다.

1. 다운로드 [!DNL at.js].

   이 URL을 다음 구조로 로드하십시오.

   ```
   https://admin<varname>admin number</varname>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<varname>client code</varname>&version=<version number>
   ```

   * Replace `admin number` with your admin number.
   * Replace `client code` with the client code from Step 1.
   * Replace `version number` with the desired at.js version number (for example, 2.2).

   >[!IMPORTANT]
   >
   >Target 팀에서는 [!DNL at.js]의 현재 버전과 바로 전 버전, 이렇게 두 버전만 유지 관리합니다. 지원되는 버전을 실행 중인지 확인하려면 [!DNL at.js]를 필요에 따라 업그레이드하십시오. 각 버전에 대한 자세한 내용은 [at.js 버전 세부 사항](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)을 참조하십시오.

   이 URL을 로드하면 사용자 지정된 [!DNL at.js] 파일의 다운로드가 시작됩니다.

## at.js implementation {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js는 웹 사이트에 있는 모든 페이지의 `<head>` 요소에 구현되어야 합니다.

[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25)나 [다이내믹 태그 관리](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md#concept_3A40AF6FFC0E4FD2AA81B303A79D0B96)같은 태그 관리자를 사용하지 않는 일반적인 Target 구현은 다음 모습과 같습니다.

```
<!doctype html> 
<html> 
 
<head> 
    <meta charset="utf-8"> 
    <title>Title of the Page</title> 
    <!--Preconnect and DNS-Prefetch to improve page load time--> 
    <link rel="preconnect" href="//<client code>.tt.omtrdc.net"> 
    <link rel="dns-prefetch" href="//<client code>.tt.omtrdc.net"> 
    <!--/Preconnect and DNS-Prefetch--> 
    <!--Data Layer to enable rich data collection and targeting--> 
    <script> 
        var digitalData = { 
            "page": { 
                "pageInfo": { 
                    "pageName": "Home" 
                } 
            } 
        }; 
    </script> 
    <!--/Data Layer--> 
    <!-- targetPageParams(), targetPageParamsAll(), Data Providers or targetGlobalSettings() functions to enrich the visitor profile or modify the library settings--> 
    <script> 
        targetPageParams = function() { 
            return { 
                "a": 1, 
                "b": 2, 
                "pageName": digitalData.page.pageInfo.pageName, 
                "profile": { 
                    "age": 26, 
                    "country": { 
                        "city": "San Francisco" 
                    } 
                } 
            }; 
        }; 
    </script> 
    <!--/targetPageParams()--> 
 
    <!--jQuery or other helper libraries should be implemented before at.js if you would like to use their methods in Target--> 
    <script src="jquery-3.3.1.min.js"></script> 
    <!--/jQuery--> 
    <!--Target's JavaScript SDK, at.js--> 
    <script src="at.js"></script> 
    <!--/at.js--> 
</head> 
 
<body> 
    The default content of the page 
</body> 
 
</html>
```

다음 중요 참고 사항을 고려하십시오.

* HTML5 Doctype(예: `<!doctype html>`)을 사용해야 합니다. 지원되지 않거나 이전 버전의 doctypes으로 Target이 요청을 작성할 수 없습니다.
* 사전 연결 및 미리 가져오기는 웹 페이지 로드 속도를 높일 수 있는 옵션입니다. If you use these configurations, ensure that you replace `<client code>` with your own client code, which you can obtain from the **[!UICONTROL Administration]** > **[!UICONTROL Implementation] page.
* 데이터 계층이 있는 경우 at.js가 로드되기 전에 페이지의 `<head>`에 가능한 많은 항목을 정의하는 것이 최적입니다. 이 배치는 개인화를 위해 Target에서 이 정보를 활용할 수 있는 최대 기능을 제공합니다.
* `targetPageParams()`, `targetPageParamsAll()`, Data Providers, `targetGlobalSettings()`와 같은 특수 Target 함수는 데이터 계층 뒤, at.js 로드 전에 정의해야 합니다. 또한 이러한 값은 [!UICONTROL at.js 설정 편집] 페이지의 [!UICONTROL 라이브러리 헤더] 섹션에 저장되며 at.js 라이브러리 자체의 일부로 저장될 수 있습니다. 이러한 함수에 대한 자세한 정보는 [at.js 함수](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).
* jQuery와 같은 JavaScript 헬퍼 라이브러리를 사용하는 경우 Target 경험을 작성할 때 Target 앞에 포함시키면 구문 및 메서드를 활용할 수 있습니다.
* 페이지의 `<head>`에 at.js를 포함합니다.

## Track conversions {#task_E85D2F64FEB84201A594F2288FABF053}

주문 확인 mbox는 사이트의 주문에 대한 세부 사항을 기록하고 매출 및 주문을 기준으로 보고할 수 있도록 합니다. 또한 주문 확인 mbox는 &quot;제품 x를 구입한 사람이 제품 y도 구입함&quot;과 같은 권장 사항 알고리즘을 유도할 수도 있습니다.

>[!NOTE]
>
>사용자가 웹 사이트에서 구매를 수행하는 경우, 보고 작업을 위해 A4T(Analytics for Target)를 사용하더라도 주문 확인 mbox를 구현하는 것이 좋습니다.

1. 주문 상세 정보 페이지에서 아래의 모델에 따라 mbox 스크립트를 삽입합니다.
1. WORDS IN CAPITAL LETTERS를 카탈로그의 동적 또는 정적 값과 교체합니다.

   >[!NOTE]
   >
   >여러 개의 제품 ID를 구분하려면 쉼표를 사용하십시오.

   **팁:** mbox에 주문 정보를 제공할 수도 있습니다(`orderConfirmPage`로 지칭할 필요가 없음). 주문 정보를 동일한 캠페인 내의 여러 mbox에 전달할 수도 있습니다.

   ```
   <script type="text/javascript"> 
   adobe.target.trackEvent({ 
       "mbox": "orderConfirmPage", 
       "params":{  
           "orderId": "ORDER ID FROM YOUR ORDER PAGE",  
           "orderTotal": "ORDER TOTAL FROM YOUR ORDER PAGE",  
           "productPurchasedId": "PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3"  
       } 
   }); 
   </script> 
   ```

주문 확인 mbox에서는 다음 매개 변수를 사용합니다.

| 매개 변수 | 설명 |
|--- |--- |
| orderId | 전환 계산을 위해 주문을 식별하는 고유한 값<br>`orderId`는 고유해야 합니다. 보고서에서 중복 주문은 무시됩니다. |
| orderTotal | 구매품의 통화 가치<br>통화 기호는 전달하지 마십시오. 소수점(쉼표 아님)을 사용하여 십진수 값을 표시합니다. |
| productPurchasedId(선택 사항) | 주문에서 구입한 제품 ID가 쉼표로 구분된 목록<br>이 제품 ID는 추가적인 보고 분석을 지원하기 위해 감사 보고서에 표시됩니다. |