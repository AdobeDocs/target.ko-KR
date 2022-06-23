---
keywords: target 구현;구현;at.js 구현;태그 관리자;온장치 의사 결정;Device Decisioning
description: 설정(계정 세부 사항, 구현 방법 등)을 지정하는 방법을 알아봅니다. Adobe 구현 [!DNL Target] 태그 관리자를 사용하지 않고 at.js 라이브러리를 설정합니다.
title: 구현할 수 있습니까? [!DNL Target] 태그 관리자 없이
feature: Implement Server-side
role: Developer
exl-id: cb57f6b8-43cb-485d-a7ea-12db8170013f
source-git-commit: 3c64945eb1898457a9d6a3e7bbfa64420bf1250a
workflow-type: tm+mt
source-wordcount: '1824'
ht-degree: 48%

---

# 구현 [!DNL Target] 태그 관리자 없이

구현에 대한 정보입니다 [!DNL Adobe Target] 태그 관리자 또는 태그를 사용하지 않고 [!DNL Adobe Experience Platform].

>[!NOTE]
>
>의 태그 [Adobe Experience Platform](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/) 는 을 구현하기 위해 선호되는 방법입니다 [!DNL Target] 및 at.js 라이브러리. 다음 정보는에서 태그를 사용할 때에는 적용할 수 없습니다 [!DNL Adobe Experience Platform] 를 구현합니다 [!DNL Target].

에 액세스하려면 [!UICONTROL 구현] 페이지를 클릭한 다음 **[!UICONTROL 관리]** > **[!UICONTROL 구현]**.

이 페이지에서 다음 설정을 지정할 수 있습니다.

* 계정 세부 사항
* 구현 방법
* 프로필 API
* 디버거 도구
* 개인정보 보호

>[!NOTE]
>
>[!DNL Target Standard/Premium] UI에서 또는 REST API를 사용하여 설정을 구성하는 대신, at.js 라이브러리에서 설정을 재정의할 수 있습니다. 자세한 내용은 [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/)를 참조하십시오.

## 계정 세부 사항

다음 계정 세부 사항을 볼 수 있습니다. 이러한 설정은 변경할 수 없습니다.

| 설정 | 설명 |
| --- | --- |
| [!UICONTROL 클라이언트 코드] | 클라이언트 코드는 [!DNL Target] API를 사용할 때 종종 필요한 클라이언트별 문자 시퀀스입니다. |
| [!UICONTROL IMS 조직 ID] | 이 ID는 구현을 [!DNL Adobe Experience Cloud] 계정에 연결합니다. |
| [!UICONTROL On-Device Decisioning] | On-Device Decisioning을 사용하려면 토글을 &quot;On&quot; 위치로 슬라이딩합니다.<br>On-Device Decisioning을 사용하여 A/B 및 [!UICONTROL 경험 타깃팅] (XT) 캠페인이 서버에 있고 거의 0개 이상의 지연에서 메모리 내 의사 결정을 수행합니다. 자세한 내용은 [On-Device Decisioning 소개](https://developer.adobe.com/target/implement/server-side/sdk-guides/on-device-decisioning/) 에서 *[!DNL Adobe Target]SDK* 안내서. |
| [!UICONTROL 아티팩트에 기존의 모든 장치 내 의사 결정 자격이 있는 활동을 포함합니다.] | (조건부) On-Device Decisioning을 활성화하면 이 옵션이 표시됩니다.<br>On-Device Decisioning에 대한 자격이 있는 모든 라이브 Target 활동을 아티팩트에 자동으로 포함하려면 전환을 &quot;켜기&quot; 위치로 끕니다.<br>이 토글을 끄면 생성된 규칙 아티팩트에 포함되려면 모든 On-Device Decisioning 활동을 다시 만들고 활성화해야 합니다. |

## 구현 방법

구현 메서드 패널에서 다음 설정을 구성할 수 있습니다.

### 전역 설정

>[!NOTE]
>
>이러한 설정은 모두 적용됩니다 [!DNL Target] .js 라이브러리. 구현 방법 섹션에서 변경을 수행한 후 라이브러리를 다운로드하고 구현에서 업데이트해야 합니다.

| 설정 | 설명 |
| --- | --- |
| 페이지 로드 활성화(글로벌 mbox 자동 만들기) | 각 페이지 로드 시 자동으로 실행할 at.js 파일에 글로벌 mbox 호출을 포함할지 여부를 선택하십시오. |
| 글로벌 mbox | 글로벌 mbox의 이름을 선택하십시오. 기본적으로 이 이름은 target-global-mbox입니다.<br>at.js를 사용하는 mbox 이름에 앰퍼샌드(&amp;)를 포함한 특수 문자를 사용할 수 있습니다. |
| 시간 초과(초) | 정의된 기간 내에 [!DNL Target]이 컨텐츠에 응답하지 않으면 서버 호출 제한 시간이 초과되어 기본 컨텐츠가 표시됩니다. 방문자 세션 동안 추가 호출이 계속 시도됩니다. 기본값은 5초입니다.<br>at.js 라이브러리는 `XMLHttpRequest`에서 시간 제한 설정을 사용합니다. 시간 제한은 요청이 시작되면 시작되고 [!DNL Target]이 서버의 응답을 받으면 중지됩니다. 자세한 내용은 Mozilla Developer Network의 [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout)을 참조하십시오.<br>응답을 받기 전에 지정된 시간 제한이 초과되면, 기본 컨텐츠가 표시되고, 모든 데이터 수집은 [!DNL Target] 에지에서 발생하므로 방문자는 활동의 참가자로 카운트될 수 있습니다. 요청이 [!DNL Target] 에지에 도달하면 방문자가 카운트됩니다.<br>시간 제한 설정을 구성할 때에는 다음 사항을 고려하십시오.<ul><li>값이 너무 낮으면, 방문자가 활동의 참가자로 카운트될 수 있음에도 불구하고 사용자에게 대부분의 시간 동안 기본 컨텐츠가 표시될 수 있습니다.</li><li>값이 너무 높으면, 확장된 기간 동안 본문 숨기기를 사용하는 경우 방문자에게 웹 페이지의 빈 영역이 표시되거나 빈 페이지가 표시될 수 있습니다.</li></ul>mbox 응답 시간을 자세히 알아보려면 브라우저의 개발자 도구에서 네트워크 탭을 살펴보십시오. 타사 웹 성과 모니터링 도구(예: Catchpoint)를 사용할 수도 있습니다.<br>**참고**: [visitorApiTimeout](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/) 설정은 [!DNL Target]이 너무 오랫동안 방문자 API 응답을 기다리지 않도록 해줍니다. 이 설정과 여기에 설명된 at.js에 대한 시간 초과 설정은 서로 영향을 주지 않습니다. |
| 프로필 라이프타임 | 이 설정은 방문자 프로필이 저장되어 있는 기간을 결정합니다. 기본적으로, 프로필은 2주 동안 저장됩니다. 이 설정은 최대 90일까지 늘릴 수 있습니다.<br>프로필 라이프타임 설정을 변경하려면 [고객 지원팀](https://helpx.adobe.com/kr/contact/enterprise-support.ec.html)에 문의하십시오. |

### 기본 구현 방법

>[!IMPORTANT]
>
>Target 팀은 at.js 1.*x*&#x200B;와 at.js 2.*x* 간의 매핑에 대해 설명합니다. 지원되는 버전을 실행 중인지 확인하려면 at.js의 주요 버전을 최신 업데이트로 업그레이드하십시오.

원하는 at.js 버전을 다운로드하려면 적절한 를 클릭합니다 **[!UICONTROL 다운로드]** 버튼을 클릭합니다.

at.js 설정을 편집하려면 **[!UICONTROL 편집]** 원하는 at.js 버전 옆의 를 클릭합니다.

>[!IMPORTANT]
>
>이러한 기본 설정을 변경하기 전에 [고객 지원 센터](/help/main/cmp-resources-and-contact-information.md) 따라서 현재 구현에는 영향을 주지 않습니다.

위에 설명된 설정 외에도 다음과 같은 특정 at.js 설정을 사용할 수도 있습니다.

| 설정 | 설명 |
|--- |--- |
| 사용자 지정 라이브러리 헤더 | 라이브러리의 맨 위에 포함할 사용자 지정 JavaScript를 추가하십시오. |
| 사용자 지정 라이브러리 바닥글 | 라이브러리의 맨 아래에 포함할 사용자 지정 JavaScript를 추가하십시오. |

### On-Device Decisioning을 사용한 구현 방법

버전 2.5.0부터 at.js는 온장치 의사 결정을 제공합니다. On-Device Decisioning을 사용하여 [A/B 테스트](/help/main/c-activities/t-test-ab/test-ab.md) 및 [경험 타깃팅](/help/main/c-activities/t-experience-target/experience-target.md) (XT) 브라우저에 대한 네트워크 요청을 차단하지 않고 인메모리 의사 결정을 수행하는 활동 [!DNL Adobe Target] 에지 네트워크.

자세한 내용은 다음 주제를 참조하십시오.

* [클라이언트측을 위한 On-Device Decisioning](https://developer.adobe.com/target/implement/client-side/){target=_blank}
* [서버측을 위한 On-Device Decisioning](https://developer.adobe.com/target/implement/server-side/sdk-guides/on-device-decisioning/){target=_blank}

### 프로필 API

API를 통해 묶음 업데이트에 대한 인증을 활성화 또는 비활성화하고 프로필 인증 토큰을 생성합니다.

자세한 내용은 [프로필 API 설정](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/profile-api-settings/).

### 디버거 도구

고급 기능을 사용할 인증 토큰 생성 [!DNL Target] 디버깅 도구. 클릭 **[!UICONTROL 새 인증 토큰 생성]**.

![새 인증 토큰 생성](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### 개인정보 보호

이러한 설정을 사용하면 다음 작업을 수행할 수 있습니다 [!DNL Target] 해당 데이터 개인 정보 보호 법률에 따라

방문자 IP 주소 난독화 드롭다운 목록에서 원하는 설정을 선택합니다.

* 마지막 8진수 난독화
* 전체 IP 난독화
* 없음

자세한 내용은 [개인 정보](https://developer.adobe.com/target/before-implement/privacy/privacy/)를 참조하십시오.

>[!NOTE]
>
>at.js 버전 0.9.3 및 이전 버전에서 레거시 브라우저 지원 옵션을 사용할 수 있었습니다. 이 선택 사항은 at.js 버전 0.9.4에서 제거되었습니다. at.js에서 지원하는 브라우저 목록이 필요하면 [지원되는 브라우저](https://developer.adobe.com/target/before-implement/supported-browsers/)를 참조하십시오.<br>이전 브라우저는 CORS(Cross Origin Resource Sharing)를 완전히 지원하지는 않는 오래된 브라우저입니다. 이러한 브라우저에는 버전 11 이전의 Internet Explorer 브라우저와 Safari 버전 6 및 그 이전 버전이 포함됩니다. 이전 브라우저 지원이 비활성화되어 있으면, 이러한 브라우저에서는 Target이 보고서에서 컨텐츠를 전달하거나 방문자 수를 카운트하지 않았습니다. 이 옵션을 활성화한 경우 좋은 고객 경험을 위해 이전 브라우저에서 품질 보증을 수행하는 것이 좋습니다.

## at.js 다운로드 {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

를 사용하여 라이브러리를 다운로드하는 지침 [!DNL Target] 인터페이스 또는 Download API를 참조하십시오.

>[!NOTE]
>
>* [[!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/) 는 을 구현하기 위해 선호되는 방법입니다 [!DNL Target] 및 at.js 라이브러리. 다음 정보는에서 태그를 사용할 때에는 적용할 수 없습니다 [!DNL Adobe Experience Platform] 를 구현합니다 [!DNL Target].
>
>* 다음 [!DNL Target] 팀은 at.js 1.*x*&#x200B;와 at.js 2.*x* 간의 매핑에 대해 설명합니다. 지원되는 버전을 실행 중인지 확인하려면 at.js의 주요 버전을 최신 업데이트로 업그레이드하십시오. 각 버전에 대한 자세한 내용은 [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/)을 참조하십시오.


### 를 사용하여 at.js 다운로드 [!DNL Target] 인터페이스 {#section_1F5EE401C2314338910FC57F9592894E}

[!DNL Target] 인터페이스에서 [!DNL at.js]를 다운로드하려면 다음을 수행하십시오.

1. **[!UICONTROL 관리]** > **[!UICONTROL 구현]**&#x200B;을 클릭합니다.
1. 에서 [!UICONTROL 구현 방법] 섹션에서 **[!UICONTROL 다운로드]** 원하는 at.js 버전 옆의 버튼을 클릭합니다.

### 를 사용하여 at.js 다운로드 [!DNL Target] API 다운로드 {#section_C0D9D2A9068144708D08526BA5CA10D0}

API를 사용하여 [!DNL at.js]를 다운로드하려면 다음을 수행하십시오.

1. 클라이언트 코드를 가져옵니다.

   클라이언트 코드는 **[!UICONTROL 관리]** > **[!UICONTROL 구현]** 페이지의 [!DNL Target] 인터페이스.

1. 관리 번호를 가져옵니다.

   다음 URL을 로드하십시오.

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   바꾸기 `client code` ( 1단계의 클라이언트 코드 사용)

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

   * 바꾸기 `admin number` 관리자 번호 사용.
   * 바꾸기 `client code` ( 1단계의 클라이언트 코드 사용)
   * 바꾸기 `version number` 원하는 at.js 버전 번호(예: 2.2)를 사용하여 at.js에 매핑해야 합니다.

   >[!IMPORTANT]
   >
   >Target 팀에서는 [!DNL at.js]의 현재 버전과 바로 전 버전, 이렇게 두 버전만 유지 관리합니다. 지원되는 버전을 실행 중인지 확인하려면 [!DNL at.js]를 필요에 따라 업그레이드하십시오. 각 버전에 대한 자세한 내용은 [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/)을 참조하십시오.

   이 URL을 로드하면 사용자 지정된 [!DNL at.js] 파일의 다운로드가 시작됩니다.

## at.js 구현 {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js는 웹 사이트에 있는 모든 페이지의 `<head>` 요소에 구현되어야 합니다.

의 태그와 같이 태그 관리자를 사용하지 않는 일반적인 Target 구현 [[!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/) 의 모습은 다음과 같습니다.

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

* HTML5 Doctype(예: `<!doctype html>`) 를 사용해야 합니다. 지원되지 않거나 이전 버전의 doctypes으로 Target이 요청을 작성할 수 없습니다.
* 사전 연결 및 미리 가져오기는 웹 페이지 로드 속도를 높일 수 있는 옵션입니다. 이러한 구성을 사용하는 경우 `<client code>` 를 사용하여 at.js 또는 mbox.js 참조 위에서 **[!UICONTROL 관리]** > **[!UICONTROL 구현] 페이지.
* 데이터 계층이 있는 경우 at.js가 로드되기 전에 페이지의 `<head>`에 가능한 많은 항목을 정의하는 것이 최적입니다. 이 배치는 개인화를 위해 Target에서 이 정보를 사용할 수 있는 최대 기능을 제공합니다.
* `targetPageParams()`, `targetPageParamsAll()`, Data Providers, `targetGlobalSettings()`와 같은 특수 Target 함수는 데이터 계층 뒤, at.js 로드 전에 정의해야 합니다. 또는 이러한 함수를 [!UICONTROL 라이브러리 헤더] 섹션 [!UICONTROL at.js 설정 편집] 페이지 및 at.js 라이브러리 자체의 일부로 저장되었습니다. 이러한 함수에 대한 자세한 내용은 [at.js 함수](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/).
* jQuery와 같은 JavaScript 헬퍼 라이브러리를 사용하는 경우 Target 경험을 작성할 때 Target 앞에 포함시키면 구문 및 메서드를 사용할 수 있습니다.
* 페이지의 `<head>`에 at.js를 포함합니다.

## 전환 추적 {#task_E85D2F64FEB84201A594F2288FABF053}

주문 확인 mbox는 사이트의 주문에 대한 세부 사항을 기록하고 매출 및 주문을 기준으로 보고할 수 있도록 합니다. 또한 주문 확인 mbox는 &quot;제품 x를 구입한 사람이 제품 y도 구입함&quot;과 같은 권장 사항 알고리즘을 유도할 수도 있습니다.

>[!NOTE]
>
>사용자가 웹 사이트에서 구매를 수행하는 경우, 보고 작업을 위해 Analytics for Target(A4T)를 사용하는 경우에도 주문 확인 mbox를 구현하는 것이 좋습니다.

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