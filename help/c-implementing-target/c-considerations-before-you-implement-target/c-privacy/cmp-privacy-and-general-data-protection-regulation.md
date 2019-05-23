---
description: 유럽 연합의 일반 데이터 보호 규정(GDPR)에 대한 정보 및 해당 규정이 조직 및 Adobe Target에 어떻게 영향을 미치는지에 대한 자주 묻는 질문 목록입니다.
keywords: gdpr;eu;유럽 연합;개인 정보;faq;자주 묻는 질문
seo-description: 유럽 연합의 일반 데이터 보호 규정(GDPR)에 대한 정보 및 해당 규정이 조직 및 Adobe Target에 어떻게 영향을 미치는지에 대한 자주 묻는 질문 목록입니다.
seo-title: 개인 정보 및 GDPR(일반 데이터 보호 규정)
solution: Target
title: 개인 정보 및 GDPR(일반 데이터 보호 규정)
topic: Standard
uuid: 5e67adcf-464c-495f-9ba5-15152d9a6a41
translation-type: tm+mt
source-git-commit: 6c1b4f26f635eab661ec426f9241b26247e880c3

---


# 개인 정보 및 GDPR(일반 데이터 보호 규정){#privacy-and-general-data-protection-regulation-gdpr}

유럽 연합의 일반 데이터 보호 규정(GDPR)에 대한 정보 및 해당 규정이 조직 및 Adobe Target에 어떻게 영향을 미치는지에 대한 자주 묻는 질문 목록입니다.

## 개인 정보 보호 및 일반 데이터 보호 규정(GDPR) 개요 {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Adobe가 귀하와 함께 유럽 연합의 GDPR(일반 데이터 보호 규정)을 준비하는 방법에 관한 정보입니다.

## GDPR 개요 {#section_8C99434A431B4494998B01B869E7EA5D}

2018년 5월 25일 자로 유럽 연합의 GDPR이 발효됩니다. GDPR의 발효가 귀하에게 미치는 영향에 관한 자세한 내용은 [GDPR 및 비즈니스](https://www.adobe.com/privacy/general-data-protection-regulation.html)를 참조하십시오.

Adobe가 기업에 소프트웨어 및 서비스를 제공할 때 Adobe는 이러한 서비스를 제공하는 과정에서 처리하고 저장하는 개인 데이터에 대한 데이터 처리자 역할을 합니다. Adobe는 데이터 처리자로서 귀사의 허가 및 지침(예: Adobe와의 계약에 명시된 내용)에 따라 개인 데이터를 처리합니다.

귀하는 데이터 관리자로서 Adobe가 귀하를 대신하여 처리하고 저장하는 개인 데이터를 결정합니다. 귀하가 Adobe Experience Cloud 솔루션을 사용하는 경우, Adobe는 귀하가 사용하는 솔루션 및 귀하의 Adobe Experience Cloud 계정에 전송하기로 선택한 정보에 따라 귀하를 위해 개인 데이터를 호스팅할 수 있습니다. 상세한 예제 목록은 [Adobe Experience Cloud 개인 정보](https://www.adobe.com/privacy/marketing-cloud.html#collect)를 참조하십시오.

Adobe Experience Cloud는 GDPR 규정 발효일 이전에 데이터 관리자가 다음 작업을 완료할 수 있도록 GDPR 지원 API를 제공할 예정입니다.

* Target 내에 저장된 데이터 주체 정보에 액세스
* Target 내에 저장된 데이터 주체 정보 삭제

## Adobe 일반 데이터 보호 규정 API 웹 사이트 {#section_51B8FA3CBE234E9592BDA7083B5CE4CD}

자세한 내용은 다음 문서를 참조하십시오.

* [Adobe 일반 데이터 보호 규정 API 웹 사이트](https://www.adobe.io/apis/cloudplatform/gdpr.html)
* [GDPR 설명서](https://www.adobe.io/apis/cloudplatform/gdpr/docs.html)

## Adobe Target 및 Adobe Launch 선택 {#section_6F7B53F5E40C4425934627B653E831B0}

Target은 Adobe Launch를 통해 동의 관리 전략을 지원하는 데 도움이 되는 선택 기능 지원을 제공합니다. 선택 기능을 통해 고객이 Target 태그를 실행하는 방법과 시기를 제어할 수 있습니다. Adobe Launch를 통해서 Target 태그를 사전 승인할 수 있는 옵션이 있습니다. Target at.js에서 옵트인을 사용하는 기능을 활성화하려면 `targetGlobalSettings`를 사용하고 `optinEnabled=true` 설정을 추가해야 합니다. Launch에서는 Target Launch Extension 설치 보기의 GDPR 옵트인 드롭다운 목록에서 &quot;활성화&quot;를 선택해야 합니다. 자세한 내용은 [Launch 설명서](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)를 참조하십시오.

다음 코드 조각은 `optinEnabled=true` 설정을 활성화하는 방법을 보여 줍니다.

```
window.targetGlobalSettings = {
  optinEnabled: true
};
```

>[!NOTE]
>
>옵트인 기능은 at.js 버전 1.7.0에서 지원되지만 현재 at.js 버전 2.0.0 에서는 지원되지 않습니다.
>
>Adobe Launch를 사용하여 선택 기능을 관리하는 것이 좋습니다. Adobe Launch에는 동의 전략의 일부로 활용할 수 있는 Target 실행 전에 페이지에서 선택한 요소를 숨기기 위한 세부적인 제어 기능이 추가로 있습니다.

선택 기능을 사용할 때 고려해야 할 세 가지 시나리오가 있습니다.

1. **Adobe Launch를 통해 사전 승인된 Target 태그(또는 이전에 승인된 Target의 데이터 주체):** Target 태그는 예상대로 동의 및 기능을 위해 유지되지 않습니다.
1. **Target 태그가 사전 승인되지 않으며`bodyHidingEnabled`가 FALSE:** Target 태그는 고객으로부터 동의가 수집된 후에만 실행됩니다. 동의하기 전에는 기본 컨텐츠만 사용할 수 있습니다. 동의를 받은 후 Target을 호출하여 데이터 주체(방문자)에 대해 개인화된 컨텐츠를 사용할 수 있습니다. 동의 전에는 기본 컨텐츠만 사용할 수 있으므로 페이지의 모든 부분을 포함하는 스플래시 페이지나 개인화된 컨텐츠와 같은 적절한 전략을 활용하는 것이 중요합니다. 이를 통해 데이터 주체(방문자)에 대해 일관성을 유지할 수 있습니다.
1. **Target 태그가 사전 승인되지 않으며`bodyHidingEnabled`가 TRUE:** Target 태그는 고객으로부터 동의가 수집된 후에만 실행됩니다. 동의하기 전에는 기본 컨텐츠만 사용할 수 있습니다. 그러나 `bodyHidingEnabled`가 true로 설정되어 있으므로 `bodyHiddenStyle`은 Target 태그가 실행될 때까지 페이지에 어떤 컨텐츠가 숨겨져 있는지 나타냅니다(또는 데이터 주체에서 선택 기능을 거부하며, 이 경우 기본 컨텐츠가 표시됨). 기본적으로 `bodyHiddenStyle`이 `body { opacity:0;`으로 설정되어 HTML 본문 태그를 숨깁니다. 권장되는 페이지 구성은 아래에 제시되어 있습니다. 따라서 동의 관리자 대화 상자를 제외한 페이지의 전체 본문을 숨기며, 이는 페이지의 컨텐츠를 한 개의 컨테이너에 넣고 동의 관리자 대화 상자를 별도의 컨테이너에 넣어 실행됩니다. 이 설정은 페이지 컨텐츠 컨테이너만 숨기도록 Target을 구성합니다. 이러한 설정을 구성하는 방법에 대한 자세한 내용은 [Adobe Launch 설명서](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html)를 참조하십시오.

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

## 일반 데이터 보호 규정 FAQ {#concept_41F88DE95D2943178BEC382736B5C038}

Adobe Target과 관련된 GDPR(일반 데이터 보호 규정)에 대해 자주 묻는 질문입니다.

### GDPR(일반 데이터 보호 규정)에 대한 Adobe의 정책은 무엇입니까?{#section_A6849628D6524C80A6E16946DC5D25A9}

Adobe는 데이터 처리자로서의 의무를 이미 충족하거나 구현하고 있습니다. Adobe는 인증된 보안 및 개인 정보 컨트롤에 대한 강력한 기반을 계획적으로 구축했으며, 2018년 5월 마감일 전까지 계속해서 제품을 개선할 예정입니다. 기업 고객은 이러한 개선 사항을 구현하고 필요한 정책과 절차를 모두 업데이트할 책임이 있습니다.

### 데이터 관리자 회사에서 사용 중인 Adobe Experience Cloud 솔루션 각각에 대한 GDPR 요청을 제출해야 합니까? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

아니요, Adobe는 데이터 관리자가 GDPR 요구 사항을 충족하는 데 도움이 되는 중심적인 방법을 제공합니다. 데이터 관리자는 각 솔루션에 직접 관여하지 않아도 됩니다.

Target을 비롯한 Experience Cloud 솔루션 전반에 대한 모든 GDPR 요청은 현재 GDPR API라고 하는 중앙의 Adobe API를 통해 이루어집니다. 그러면 API가 데이터 관리자의 Experience Cloud 솔루션 세트에 대한 요청을 완료합니다.

### Adobe는 데이터 주체/사용자 요청에 대응하여 고객이 어떤 정보를 삭제할 수 있도록 허용할 계획입니까? {#section_4B51D00924EC4166B2442218B69214F0}

Target 내의 개별 방문자와 관련된 정보는 Target 방문자 프로필 내에 포함되어 있습니다. Adobe Target을 사용하면 고객이 본인의 방문자 프로필에서 ID와 연결된 모든 데이터를 삭제할 수 있습니다. Adobe Target이 저장하는 프로필 데이터의 예는 [방문자 프로필](../../../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

특정 개인을 식별하지 않는 집계 또는 익명화 데이터(예: 보고 데이터) 또는 특정 개인과 관련이 없는 데이터(예: 컨텐츠 데이터)는 사용자 삭제 요청 범위를 벗어납니다.

90일 동안 비활성 상태인 Target 방문자 프로필은 별도의 조치 없이도 기본적으로 삭제됩니다.

### 고객이 Target에 대한 GDPR 액세스 및 삭제 요청을 완료할 수 있도록 지원되는 ID는 무엇입니까? {#section_F7D0EE4E6A28490FB20056A0D26118BC}

Target은 고객 프로필을 찾기 위한 다음 ID 유형을 지원합니다.

| 사용자 ID | 네임스페이스 ID 유형 | 네임스페이스 ID | 정의 |
|--- |--- |--- |--- |
| ECID(Experience Cloud ID) | Standard | 4 | 이전에는 방문자 ID 또는 Marketing Cloud ID로 알려진 Adobe Experience Cloud ID입니다. 이 ID는 JavaScript API를 사용하여 찾을 수 있습니다(아래 세부 사항 참조). |
| TnT ID/쿠키 ID(TNTID) | Standard | 9 | 방문자의 브라우저에 쿠키로 설정된 Target 식별자입니다. 이 ID는 JavaScript API를 사용하여 찾을 수 있습니다(아래 세부 사항 참조). |
| 타사 ID/CRM ID (THIRDPARTYID) | Target 관련 | 해당 없음 | Target에 고객에 대한 CRM 또는 기타 고유 식별자 정보를 제공하는 경우입니다. |

>[!NOTE]
>
>Adobe Target은 퍼스트 파티 및 타사 상호 도메인 쿠키를 모두 지원하지만, GDPR에는 퍼스트 파티 Adobe Target 쿠키만 권장됩니다.

### Adobe Target은 동의 관리를 어떻게 처리합니까? {#section_C86BF5EE4FAA47039659850E7594A6BA}

GDPR로 인해 변경되는 것은 동의를 받아야 하는 시점이 아닌 동의를 받는 방법입니다. 각 고객의 동의 전략은 자체적인 데이터 수집 및 사용 약관과 개인정보 보호정책에 따라 다릅니다. 동의 관리는 지원되지 않으며 GDPR용 Target을 통해 수행해서는 안 됩니다.

현재 Adobe는 동의 관리 솔루션을 제공하지 않지만, 새로운 요구 사항의 일부를 해결하기 위해 시장에서 여러 가지 도구가 개발되고 있습니다. 동의 관리자를 비롯한 일반적인 개인 정보 도구에 대한 자세한 내용은 iaap(International Association of Privacy Professionals) 웹 사이트의 [2017 Privacy Tech Vendor Report(2017년 개인 정보 기술 공급업체 보고서)](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf)를 참조하십시오.

Adobe Target은 Adobe Launch를 통해 동의 관리 전략을 지원하는 데 도움이 되는 선택 기능 지원을 제공합니다. 선택 기능을 통해 고객이 Adobe Target 태그를 실행하는 방법과 시기를 제어할 수 있습니다. Adobe Launch를 통해서 Adobe Target 태그를 사전 승인할 수 있는 옵션이 있습니다. Adobe Launch를 사용하여 선택 기능을 관리하는 것이 좋습니다. Adobe Launch에는 동의 전략의 일부로 활용할 수 있는 Adobe Target 실행 전에 페이지에서 선택한 요소를 숨기기 위한 세부적인 제어 기능이 추가로 있습니다.

GDPR 및 Adobe Launch에 대한 자세한 내용은 [Adobe Privacy JavaScript Library 및 GDPR](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html)을 참조하십시오. 또한 위의 &quot;Adobe Target 및 Adobe Launch 선택&quot; 섹션도 참조하십시오.

### AdobePrivacy.js가 GDPR API에 정보를 제출합니까? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js]는 API에 이 정보를 제출하지 *않습니다*. 정보 제출은 고객이 직접 해야 합니다. 이 라이브러리는 브라우저에 저장된 해당 방문자에 대한 ID만 제공합니다.

### removeIdentities가 제거하는 것은 무엇입니까? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL removeIdentities]*는 브라우저에서 이러한 ID만을* 제거하며 Adobe 솔루션이 이를 구현했는지 여부에 따라 다릅니다.

예를 들어 Target은 해당 ID를 저장하는 쿠키를 삭제하지만, AAM(Adobe Audience Manager)은 타사 쿠키에 저장된 Demdex ID를 삭제하지 않습니다.

### Target GDPR 요청에 포함해야 하는 정보는 무엇입니까? {#section_D29A4744AE6344E68AD7710B185FD6D0}

중앙 개인정보 서비스의 요구 사항 외에 Target에 유효한 GDPR 메시지는 다음과 같습니다.

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
| 처리 중 | 처리 중 | Target이 GDPR 요청을 받아서 처리 중입니다. |
| 완료 | 적용할 수 없음 - 회사 컨텍스트를 적용할 수 없음 | GDPR 요청의 IMS ID가 Target 클라이언트에 매핑되지 않습니다.<br>일부 회사에는 여러 IMS ID가 있습니다. Target이 프로비저닝된 IMS ID를 제출해야 합니다. |
| 완료 | 적용할 수 없음 - 사용자 컨텍스트를 찾을 수 없음 | 특정 방문자 또는 데이터 주제에 대한 GDPR 요청에 제공된 ID가 Target 프로필 저장소에 없습니다.<br>이 결과는 Target에서 지원하지 않는 네임스페이스 ID 유형을 제출하려고 시도하는 경우에도 반환됩니다(지원되는 ID에 대해서는 위 참조). |
| 오류 | 오류 메시지(세부 사항은 오류 유형에 따라 다름) | 요청한 데이터 주제 프로필을 가져오거나 삭제하는 중에 오류가 발생했습니다.<br>액세스 요청을 위해 Azure에 업로드하는 동안 오류가 발생했습니다. |

### Target은 액세스 요청에 대해 GDPR API로 어떤 응답을 보냅니까? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

데이터 액세스 요청에 대한 응답에는 해당 방문자에 대한 Target 프로필의 요약이 포함되어 있습니다. 이렇게 반환된 내용이 Experience Cloud GDPR^API로^전송되고^데이터 관리자에게 응답이 전송됩니다.

다음은 샘플 Target 액세스 API 응답입니다.

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
| jobId | 중앙 GDPR API의 GDPR 작업 ID를 나타냅니다. |
| imsOrgID | 회사에 대한 고유 식별자를 제공합니다. |
| namespace | 데이터 소스라고도 합니다. 이 주제에서 &quot;고객이 Target에 대한 GDPR 액세스 및 삭제 요청을 완료할 수 있도록 지원되는 ID는 무엇입니까?&quot;를 참조하십시오. |
| 유형 | GDPR 데이터 액세스를 요청한 ID의 유형입니다. Target은 여러 가지 ID 유형을 지원하는데, 이 중 일부는 표준 ID 유형이며 일부는 Target에 고유한 ID 유형입니다. 이 주제에서 &quot;고객이 Target에 대한 GDPR 액세스 및 삭제 요청을 완료할 수 있도록 지원되는 ID는 무엇입니까?&quot;를 참조하십시오. |
| value | 네임스페이스/데이터 소스의 ID입니다. 이 주제에서 &quot;고객이 Target에 대한 GDPR 액세스 및 삭제 요청을 완료할 수 있도록 지원되는 ID는 무엇입니까?&quot;를 참조하십시오. |
| 통합 코드 | 통합 코드는 데이터 소스의 친숙한 이름이며, 데이터 소스 ID를 사용하는 것보다 쉽게 데이터 소스를 추적하는 데 도움이 됩니다. |

프로필을 식별하기 위해 여러 값이 제공된 경우 유효한 식별자마다 하나의 프로필 파일을 갖습니다. 프로필 파일은 GDPR 중앙 API를 통해 Target 프로필 JSON 응답 형식으로 중앙 GDPR Azure Blob에 전송됩니다.

샘플 Target 프로필 JSON 형식은 다음 예제와 비슷합니다.

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
| Sample_Parameter | Target 프로필의 정보 중 다수는 데이터 관리자가 업로드하거나 직접 제공합니다. 이 예에서는 프로필 업데이트 API를 사용하여 Target 프로필에 매개 변수가 업로드되었습니다. 자세한 내용은 [데이터를 Target에 가져오는 방법](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md)을 참조하십시오. |
| user.ReturnTimeOfDay | 이 표준 필드에는 사용자가 최근 재방문한 시간이 포함되어 있습니다. |
| firstSessionStart | 이 표준 필드에는 사용자의 첫 번째 세션이 시작된 시간이 포함되어 있습니다. |
| user.sessionCountScript | Target 프로필의 정보 중 다수는 데이터 관리자가 업로드하거나 직접 제공합니다. 이 예제에서 프로필 스크립트는 이 방문자가 데이터 관리자의 사이트에서 수행한 세션 수를 증가시킵니다. 자세한 내용은 [프로필 스크립트 속성](/help/c-target/c-visitor-profile/profile-parameters.md)의 프로필 스크립트 정보 카드 보기 섹션을 참조하십시오. |

>[!NOTE]
>
>이는 설명을 위해 짧게 만든 버전의 Target 프로필 JSON입니다. Target 프로필의 여러 필드는 표준이 아닙니다. 반환되는 내용은 해당 방문자 프로필에 포함된 정보에 따라 다릅니다.

## Target이 IP 난독화를 지원합니까? {#section_428907B0CD9842D9B245B38C66A53C6A}

Target은 사용자가 IP 난독화를 GDPR 구현 전략의 일부로 사용하도록 선택하는 경우 Target에서 지원합니다. 자세한 내용은 [개인 정보 보호](../../../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#concept_639482A343DB4963A6144378E1D8D7F0).
