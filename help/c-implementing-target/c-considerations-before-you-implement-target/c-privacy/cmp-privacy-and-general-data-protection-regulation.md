---
description: 유럽 연합의 GDPR(General Data Protection Regulation), CCPA(California Consumer Privacy Act) 및 기타 국제 개인 정보 보호 요구 사항에 대한 정보, 그리고 이러한 규정이 귀하의 조직 및 Adobe Target에 어떤 영향을 미치는지에 대한 정보입니다.
keywords: gdpr;eu;유럽 연합;개인 정보;faq;FAQ;FAQ;캘리포니아 소비자 개인 정보 보호 법;cpa;개인 정보 보호;옵트아웃;정부 규정
seo-description: 유럽 연합의 GDPR(General Data Protection Regulation), CCPA(California Consumer Privacy Act) 및 기타 국제 개인 정보 보호 요구 사항에 대한 정보, 그리고 이러한 규정이 귀하의 조직 및 Adobe Target에 어떤 영향을 미치는지에 대한 정보입니다.
seo-title: 유럽 연합의 GDPR(General Data Protection Regulation), CCPA(California Consumer Privacy Act) 및 기타 국제 개인 정보 보호 요구 사항에 대한 정보, 그리고 이러한 규정이 귀하의 조직 및 Adobe Target에 어떤 영향을 미치는지에 대한 정보입니다.
solution: Target
title: 개인 정보 보호 및 데이터 보호 규정
topic: Standard
uuid: 5e67adcf-464c-495f-9ba5-15152d9a6a41
translation-type: tm+mt
source-git-commit: d21838bdf17327b394f6e3106ea5ce4bc72605e6

---


# 개인 정보 보호 및 데이터 보호 규정 {#privacy-and-general-data-protection-regulation-gdpr}

유럽 연합의 GDPR(General Data Protection Regulation), CCPA(California Consumer Privacy Act) 및 기타 국제 개인 정보 보호 요구 사항에 대한 정보, 그리고 이러한 규정이 귀하의 조직 및 Adobe Target에 어떤 영향을 미치는지에 대한 정보입니다.

## Privacy and General Data Protection Regulation (GDPR) overview {#topic_DE567ECB6C944695AEE5073889F1AEA9}

2018년 5월 25일, 유럽 연합의 GDPR이 발효되었습니다. GDPR의 발효가 귀하에게 미치는 영향에 관한 자세한 내용은 [GDPR 및 비즈니스](https://www.adobe.com/privacy/general-data-protection-regulation.html)를 참조하십시오.

When [!DNL Adobe] is providing software and services to an enterprise, [!DNL Adobe] is acting as a Data Processor for any personal data it processes and stores as part of providing these services. As a Data Processor, [!DNL Adobe] processes personal data in accordance with your company's permission and instructions (for example, as set out in your agreement with [!DNL Adobe]).

As the Data Controller, you determine the personal data that [!DNL Adobe] processes and stores on your behalf. If you use [!DNL Adobe Experience Cloud] solutions, [!DNL Adobe] might host personal data for you, depending on the solutions you use and the information you choose to send to your [!DNL Adobe Experience Cloud] account. 상세한 예제 목록은 [Adobe Experience Cloud 개인 정보](https://www.adobe.com/privacy/marketing-cloud.html#collect)를 참조하십시오.

[!DNL Adobe Experience Cloud] 다음 작업을 완료할 수 있는 데이터 관리자를 위한 GDPR 준비 API를 제공합니다.

*  내에 저장된 데이터 주체 정보에 액세스[!DNL Target]
*  내에 저장된 데이터 주체 정보 삭제[!DNL Target]

자세한 내용은 다음 문서를 참조하십시오.

* [Adobe 일반 데이터 보호 규정 API 웹 사이트](https://www.adobe.io/apis/cloudplatform/gdpr.html)
* [GDPR 설명서](https://www.adobe.io/apis/cloudplatform/gdpr/docs.html)

## CCPA(California Consumer Privacy Act) 개요

CCPA(California Consumer Privacy Act)는 캘리포니아 소비자에게 개인 정보에 대한 새로운 권리를 제공하고 캘리포니아에서 사업을 수행하는 특정 업체에 데이터 보호 책임을 부과합니다. CPA는 2020년 1월 1일부터 시작됩니다.

높은 수준에서, 그 법은 캘리포니아 사람들에게 다음과 같은 권리를 포함해 몇 가지 중요한 권리를 제공한다.

* 요청 정보(데이터 액세스)
* 개인 정보 판매 거부(제3자와의 정보 공유를 거부할 수 있는 매우 광범위하게 정의된 권한)
* 개인 정보 삭제
* 개인 정보가 공개되거나 판매되고 있다는 것을 알려주십시오

귀하가 작년에 유럽의 개인 정보 보호 법(GDPR)을 준비하느라 바빴다면, 이러한 권리 중 일부는 친숙할 수 있고, 귀하가 수행한 대부분의 작업은 재사용될 수 있습니다.

## Adobe Target and [!DNL Experience Platform Launch] opt-in {#section_6F7B53F5E40C4425934627B653E831B0}

[!DNL Target] 동의 관리 전략을 지원하는 [!DNL Launch] 데 도움이 되는 옵트인 기능 지원을 제공합니다. Opt-in functionality lets customers control how and when the [!DNL Target] tag is fired. There is also an option via [!DNL Launch] to pre-approve the [!DNL Target] tag. To enable the ability to use Opt-In in the [!DNL Target] at.js library, you should use `targetGlobalSettings` and add the `optinEnabled=true` setting. In [!DNL Launch] you'll need to select "enable" from the [!UICONTROL GDPR Opt-In] drop-down list in the [!DNL Launch] extension installation view. 자세한 내용은 [Launch 설명서](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)를 참조하십시오.

다음 코드 조각은 `optinEnabled=true` 설정을 활성화하는 방법을 보여 줍니다.

```
window.targetGlobalSettings = {
  optinEnabled: true
};
```

>[!NOTE]
>
>옵트인 기능은 at.js 버전 1.7.0 및 at.js 2.1.0 이상에서 지원됩니다. 옵트인은 at.js 버전 2.0.0 및 2.0.1에서 지원되지 않습니다.
>
>Using [!DNL Experience Platform Launch] to manage opt-in is the recommended approach. Further granular control exists in [!DNL Launch] to hide selected elements of your page prior to [!DNL Target] firing that are helpful to leverage as part of your consent strategy.

선택 기능을 사용할 때 고려해야 할 세 가지 시나리오가 있습니다.

1. **[!DNL Target]태그는 다음을 통해 사전 승인됩니다([!DNL Launch]또는 이전에 승인된 데이터 주체[!DNL Target]**).이 [!DNL Target] 태그는 동의 및 기능을 위해 부착되지 않습니다.
1. **[!DNL Target]태그가 사전 승인되지 않으며`bodyHidingEnabled`가 FALSE:** 태그는 고객으로부터 동의가 수집된 후에만 실행됩니다. [!DNL Target] 동의하기 전에는 기본 콘텐츠만 사용할 수 있습니다. After consent is received, [!DNL Target] is called and personalized content is available to the data subject (visitor). 동의 전에는 기본 콘텐츠만 사용할 수 있으므로 페이지의 모든 부분을 포함하는 스플래시 페이지나 개인화된 콘텐츠와 같은 적절한 전략을 활용하는 것이 중요합니다. 이를 통해 데이터 주체(방문자)에 대해 일관성을 유지할 수 있습니다.
1. **[!DNL Target]태그가 사전 승인되지 않으며`bodyHidingEnabled`가 TRUE:** 태그는 고객으로부터 동의가 수집된 후에만 실행됩니다. [!DNL Target] 동의하기 전에는 기본 콘텐츠만 사용할 수 있습니다. 그러나 `bodyHidingEnabled`가 true로 설정되어 있으므로 `bodyHiddenStyle`은 태그가 실행될 때까지 페이지에 어떤 콘텐츠가 숨겨져 있는지 나타냅니다(또는 데이터 주체에서 선택 기능을 거부하며, 이 경우 기본 콘텐츠가 표시됨). [!DNL Target] 기본적으로 `bodyHiddenStyle`이 `body { opacity:0;`으로 설정되어 HTML 본문 태그를 숨깁니다. 권장되는 페이지 구성은 아래에 제시되어 있습니다. 따라서 동의 관리자 대화 상자를 제외한 페이지의 전체 본문을 숨기며, 이는 페이지의 콘텐츠를 한 개의 컨테이너에 넣고 동의 관리자 대화 상자를 별도의 컨테이너에 넣어 실행됩니다. This setup configures [!DNL Target] so that it hides the page content container only. 이러한 설정을 구성하는 방법에 대한 자세한 내용은 [ Launch 설명서](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html)를 참조하십시오.

   시나리오 3에 대한 권장 페이지 설정은 다음과 같습니다.

   ```
   <html> 
   <head> 
   //visitor, at.js 
   </head> 
   
   <body> 
   <div id = "consentManagerDialog"> 
   
   //consent manager html dialog goes here 
   </div> 
   
   <div id="pageContent"> 
   // page content goes here 
   </div> 
   
   </body> 
   </html> 
   ```

   `bodyHiddenStyle`이 다음과 같다고 가정합니다.

   ```
   #pageContent { opacity:0;}
   ```

## 개인 정보 보호 및 데이터 보호 규정 FAQ {#concept_41F88DE95D2943178BEC382736B5C038}

유럽 연합의 GDPR(General Data Protection Regulation), CCPA(California Consumer Privacy Act) 및 기타 Target 관련 국제 개인 정보 보호 요구 사항에 대한 FAQ입니다.

### 이러한 규정에 대한 Adobe의 정책은 무엇입니까? {#section_A6849628D6524C80A6E16946DC5D25A9}

[!DNL Adobe] 이미 데이터 프로세서로서의 의무를 충족하거나 구현하고 있습니다. Adobe는 철저한 보안 및 디자인 개인 정보 관리를 기반으로 2018년 5월 이전에 제품을 개선했습니다. 기업 고객은 이러한 개선 사항을 구현하고 필요한 정책과 절차를 모두 업데이트할 책임이 있습니다.

### Will my company, the Data Controller, need to submit a GDPR or CCPA request to each [!DNL Adobe Experience Cloud] solution that it uses? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

No, [!DNL Adobe] is providing a central way to help Data Controllers meet their GDPR and CCPA requirements. 데이터 관리자는 각 솔루션에 직접 관여하지 않아도 됩니다.

All GDPR and CCPA requests across [!DNL Experience Cloud] solutions, including [!DNL Target], will be made through a central Adobe API, currently called the GDPR API. The API will then complete the request across the Data Controller's [!DNL Experience Cloud] solution suite.

### What information will [!DNL Adobe] enable our customers to delete in response to a data subject/user request? {#section_4B51D00924EC4166B2442218B69214F0}

The information related to an individual visitor within [!DNL Target] is contained within the [!DNL Target] Visitor Profile. [!DNL Target] 방문자 프로필에서 ID와 관련된 모든 데이터를 삭제할 수 있습니다. 프로필 데이터 저장소의 예는 방문자 프로필을 [!DNL Target] 참조하십시오 [](../../../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

특정 개인을 식별하지 않는 집계 또는 익명화 데이터(예: 보고 데이터) 또는 특정 개인과 관련이 없는 데이터(예: 콘텐츠 데이터)는 사용자 삭제 요청 범위를 벗어납니다.

[!DNL Target]90일 동안 비활성 상태인 방문자 프로필은 별도의 조치 없이도 기본적으로 삭제됩니다.

### What IDs are supported to help customers complete a GDPR or CCPA access and deletion request for [!DNL Target]? {#section_F7D0EE4E6A28490FB20056A0D26118BC}

[!DNL Target] 고객 프로파일을 찾으려면 다음 ID 유형을 지원합니다.

| 사용자 ID | 네임스페이스 ID 유형 | 네임스페이스 ID | 정의 |
|--- |--- |--- |--- |
| ECID(Experience Cloud ID) | Standard | 4 | 이전에는 방문자 ID 또는 Marketing Cloud ID로 알려진 Adobe Experience Cloud ID입니다. 이 ID는 JavaScript API를 사용하여 찾을 수 있습니다(아래 세부 사항 참조). |
| TnT ID/쿠키 ID(TNTID) | Standard | 9 | 방문자의 브라우저에 쿠키로 설정된 Target 식별자입니다. 이 ID는 JavaScript API를 사용하여 찾을 수 있습니다(아래 세부 사항 참조). |
| 타사 ID/CRM ID (THIRDPARTYID) | Target 관련 | 해당 없음 | Target에 고객에 대한 CRM 또는 기타 고유 식별자 정보를 제공하는 경우입니다. |

>[!NOTE]
>
>퍼스트 파티 및 서드 파티 도메인 간 쿠키를 모두 [!DNL Target] 지원하지만, 퍼스트 파티 [!DNL Target] 쿠키는 GDPR 및 CCPA에만 권장됩니다.

### 동의 관리는 어떻게 [!DNL Target] 처리합니까? {#section_C86BF5EE4FAA47039659850E7594A6BA}

GDPR and CCPA do not change when you need to get consent, but how you get it. 각 고객의 동의 전략은 자체적인 데이터 수집 및 사용 약관과 개인정보 보호정책에 따라 다릅니다. Consent management isn’t supported by and shouldn’t be achieved via [!DNL Target] for GDPR and CCPA.

[!DNL Adobe] 은(는) 현재 동의 관리 솔루션을 제공하지 않지만, 새로운 요구 사항 중 일부를 해결하기 위해 시장에 개발 중인 다양한 도구가 있습니다. For more information on privacy tools in general, including consent managers, see the [2017 Privacy Tech Vendor Report](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf) on the *International Association of Privacy Professionals (iaap)* website.

[!DNL Target] 동의 관리 전략에 대한 지원을 [!DNL Launch] 제공하기 위해 는 동의 기능 지원을 제공합니다. Opt-in functionality lets customers control how and when the [!DNL Target] tag is fired. There is also an option via [!DNL Launch] to pre-approve the [!DNL Target] tag. Using [!DNL Launch] to manage opt-in is the recommended approach. Further granular control exists in [!DNL Launch] to hide select elements of your page prior to the [!DNL Target] firing that might be helpful to leverage as part of your consent strategy.

For more information on GDPR, CCPA, and [!DNL Launch], see [The Adobe Privacy JavaScript Library and GDPR](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html). Also, see the *Adobe Target and Experience Platform Launch opt-in* section above.

### AdobePrivacy.js가 GDPR API에 정보를 제출합니까? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js]는 API에 이 정보를 제출하지 *않습니다*. 정보 제출은 고객이 직접 해야 합니다. 이 라이브러리는 브라우저에 저장된 해당 방문자에 대한 ID만 제공합니다.

### removeIdentities가 제거하는 것은 무엇입니까? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL removeIdentities]*는 브라우저에서 이러한 ID만을*[!DNL Adobe] 제거하며 솔루션이 이를 구현했는지 여부에 따라 다릅니다.

For example, [!DNL Target] deletes the cookies storing its IDs, but [!DNL Adobe Audience Manager] (AAM) does not delete the demdex ID that is stored in a third-party cookie.

### What information needs to be included in a Target GDPR or CCPA request? {#section_D29A4744AE6344E68AD7710B185FD6D0}

In addition to the requirements from Central Privacy Service, a valid GDPR or CCPA message for [!DNL Target] contains:

```
{ 
    "jobId":"12345AD43E", 
    ... 
    "products":["Target",...], 
    "companyContexts":[ 
        { 
            "namespace":"imsOrgID", 
            "value":"123456789@AdobeOrg" 
        }, 
        ... 
    ], 
    "userContexts":[ 
        { 
            "namespace":"ECID", 
            "namespaceId":4, 
            "type":"standard", 
            "value":"53792210477379708453829363835595041181" 
        } 
        And/OR: 
        { 
            "namespace":"TNTID", 
            "namespaceId":9, 
            "type":"standard", 
            "value":"1234567890" 
        } 
        And/OR: 
        { 
            "namespace":"THIRDPARTYID", 
            "type":"target", 
            "value":"thirdPartyIdName" 
        }, 
        ... 
    ] 
}
```

### GDPR API를 통해 Target에서 예상할 수 있는 응답 유형은 무엇입니까? {#section_F67263D2A72B4641A47CE36729CCAE8F}

| 요청 상태 | Target 응답 메시지 | 시나리오 |
|--- |--- |--- |
| 처리 중 | 처리 중 | Target이 GDPR 또는 CCPA 요청을 수신했으며 처리 중입니다. |
| 완료 | 적용할 수 없음 - 회사 컨텍스트를 적용할 수 없음 | GDPR 또는 CPA 요청의 IMS ID가 Target 클라이언트에 매핑되지 않습니다.<br>일부 회사에는 여러 IMS ID가 있습니다. Target이 프로비저닝된 IMS ID를 제출해야 합니다. |
| 완료 | 적용할 수 없음 - 사용자 컨텍스트를 찾을 수 없음 | 특정 방문자 또는 데이터 주체의 GDPR 또는 CCPA 요청에 제공된 ID가 Target 프로필 저장소에 없습니다.<br>이 결과는 Target에서 지원하지 않는 네임스페이스 ID 유형을 제출하려고 시도하는 경우에도 반환됩니다(지원되는 ID에 대해서는 위 참조). |
| 오류 | 오류 메시지(세부 사항은 오류 유형에 따라 다름) | 요청한 데이터 주제 프로필을 가져오거나 삭제하는 중에 오류가 발생했습니다.<br>액세스 요청을 위해 Azure에 업로드하는 동안 오류가 발생했습니다. |

### Target은 액세스 요청에 대해 GDPR API로 어떤 응답을 보냅니까? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

Responses to access data requests contain a summary of the [!DNL Target] profile for the visitor in question. Note that this return is sent to the [!DNL Experience Cloud] GDPR API, which in turn sends Data Controllers a response.

A sample [!DNL Target] access API response could look like this:

```
{ 
    "jobId":"12345AD43E", 
    ... 
    "products":["Target",...], 
    "companyContexts":[ 
        { 
            "namespace":"imsOrgID", 
            "value":"123456789@AdobeOrg" 
        }, 
        ... 
    ], 
    "userContexts":[ 
        { 
            ~"namespace":"ECID", 
            "namespaceId":4, 
            "type":"standard", 
            "value":"53792210477379708453829363835595041181" 
        } 
        And/OR: 
        { 
            ~"namespace":"tntId", 
            "namespaceId":9, 
            "type":"standard", 
            "value":"1234567890" 
        } 
        And/OR: 
        { 
            "namespace":"thirdPartyId", 
            "type":"target", 
            "value":"thirdPartyIdName" 
        }, 
        ... 
    ] 
} 
```

| 필드 | 설명 |
|--- |--- |
| jobId | Indicates the GDPR or CCPA job ID from the Central GDPR API. |
| imsOrgID | 회사에 대한 고유 식별자를 제공합니다. |
| namespace | 데이터 소스라고도 합니다. See "What IDs are supported to help customers complete a GDPR or CCPA access and deletion request for Target?" 참조하십시오. |
| 유형 | The type of ID for which you requested the GDPR or CCPA data access. Target은 여러 가지 ID 유형을 지원하는데, 이 중 일부는 표준 ID 유형이며 일부는 Target에 고유한 ID 유형입니다. See "What IDs are supported to help customers complete a GDPR or CCPA access and deletion request for Target?" 참조하십시오. |
| value | 네임스페이스/데이터 소스의 ID입니다. "고객이 Target에 대한 GDPR 또는 CPA 액세스 및 삭제 요청을 완료하는 데 도움이 되는 ID는 무엇입니까?"를 참조하십시오. 참조하십시오. |
| 통합 코드 | 통합 코드는 데이터 소스의 친숙한 이름이며, 데이터 소스 ID를 사용하는 것보다 쉽게 데이터 소스를 추적하는 데 도움이 됩니다. |

프로필을 식별하기 위해 여러 값이 제공된 경우 유효한 식별자마다 하나의 프로필 파일을 갖습니다. The profile file(s) are sent to the central GDPR Azure Blob through the GDPR Central API, in the format of [!DNL Target] Profile JSON response.

A sample [!DNL Target] Profile JSON could look like the following example:

```
{"profileAttributes": 
 
"Sample_Parameter":{"value":"Gold Loyalty Status","modifiedAt":"2018-04-11T21:44:14.000-04:00"}, 
 
"user.ReturnTimeOfDay":{"value":"44.0","modifiedAt":"2018-04-11T21:44:14.000-04:00"}, 
 
"firstSessionStart":{"value":"1523497450602","modifiedAt":"2018-04-11T21:44:10.000-04:00"}, 
 
"user.sessionCountScript":{"value":"1","modifiedAt":"2018-04-11T21:44:14.000-04:00"} 
   } 
} 
```

다음 표에서는 설명용 프로필 JSON 필드를 설명합니다.

| 필드 | 설명 |
|--- |--- |
| Sample_Parameter | Many pieces of information in the [!DNL Target] profile are uploaded or directly provided by the Data Controller. In this example, a parameter was uploaded into the [!DNL Target] profile using the Profile Update API. 자세한 내용은 데이터를 Target [으로 가져오는 방법을 참조하십시오](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md). |
| user.ReturnTimeOfDay | 이 표준 필드에는 사용자가 최근 재방문한 시간이 포함되어 있습니다. |
| firstSessionStart | 이 표준 필드에는 사용자의 첫 번째 세션이 시작된 시간이 포함되어 있습니다. |
| user.sessionCountScript | Many pieces of information in the [!DNL Target] profile are uploaded or directly provided by the Data Controller. 이 예제에서 프로필 스크립트는 이 방문자가 데이터 관리자의 사이트에서 수행한 세션 수를 증가시킵니다. 자세한 내용은 [프로필 스크립트 속성](/help/c-target/c-visitor-profile/profile-parameters.md)의 프로필 스크립트 정보 카드 보기 섹션을 참조하십시오. |

>[!NOTE]
>
>This is a shortened version of a [!DNL Target] profile JSON for the purpose of illustration. Many of the fields of the [!DNL Target] profile are not standard. 반환되는 내용은 해당 방문자 프로필에 포함된 정보에 따라 다릅니다.

### Target이 IP 난독화를 지원합니까? {#section_428907B0CD9842D9B245B38C66A53C6A}

[!DNL Target] 는 GDPR 또는 CPA 구현 전략의 일부로 IP 난독화를 지원합니다. 자세한 내용은 개인 정보를 [참조하십시오](../../../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#concept_639482A343DB4963A6144378E1D8D7F0).
