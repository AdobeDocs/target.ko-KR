---
keywords: 이메일;ESP;이메일 서비스 제공업체;rawbox;배달 API;다운로드 전용 템플릿;이메일 템플릿;일괄처리;작성 시간 이메일
description: ' [!DNL Target Recommendations], including using the [!DNL Target]  배달 API, Rawbox 템플릿 및 다운로드 전용 템플릿을 포함하여 이메일을 Adobe Target Recommendations과 통합하는 방법에 대해 알아보십시오.'
title: Recommendations를 이메일과 통합하려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 08fcb507-2c91-444a-b8ac-26165e359f6f
source-git-commit: 2a25fdb42ce4470f9126b7e0e7f6fd9e60c350e5
workflow-type: tm+mt
source-wordcount: '1715'
ht-degree: 96%

---

# [!DNL Recommendations]를 이메일과 통합

[!DNL Adobe Target]은 이메일에 포함된 권장 사항의 전송 시간 개인 맞춤화를 지원합니다.

ESP(이메일 서비스 공급자)를 통해 [!DNL Target Recommendations]를 통합하는 방법에는 세 가지가 있습니다. ESP의 역량은 사용하는 방법에 따라 결정됩니다. 계정 관리자 또는 컨설턴트가 사용자의 가장 적합한 옵션 선택을 지원할 수 있습니다.

| 방법 | 세부 사항 |
| --- | --- |
| [방법 1: [!DNL Adobe Target Delivery API]](#delivery-api) (권장) | [!DNL Adobe Target Delivery API]를 사용하여 고객당/이메일당 권장 사항에 대한 요청을 만듭니다. |
| [방법 2: [!DNL Adobe Rawbox API]](#rawbox) | [!DNL Adobe Target Rawbox API]를 사용하여 고객/이메일 단위의 권장 사항에 대한 요청을 만듭니다. |
| [방법 3: [!DNL Recommendations Download API]](#download-api) | 권장 사항 다운로드 API를 사용하여 제품 또는 범주 목록에 대한 권장 사항을 CSV 포맷으로 일괄 요청합니다. |

방법 1 또는 방법 2를 사용하려면 ESP가 고객/이메일 단위로 외부 API를 호출하고 콘텐츠가 반환될 때까지 기다려야 합니다. 모든 ESP에서 이들 방법이 지원되는 것은 아닙니다. 귀하의 ESP에 문의하여 이 통합 패턴과 호환되는지 확인하십시오.

방법 3을 사용하려면 ESP가 권장 사항 목록을 제품 ID 또는 범주 ID로 이메일 목록에 등록해야 합니다. 이 방법은 고객의 마지막으로 본 제품, 마지막으로 구매한 제품 또는 가장 많이 본 범주와 같은 속성을 기반으로 할 수 있습니다. 단, 등록을 수행하려면 ESP에 고객 프로필에 있는 이 데이터에 대한 액세스 권한이 있어야 합니다. 귀하의 ESP에 문의하여 이 데이터에 대한 액세스 권한이 있으며 이 통합 패턴과 호환되는지 확인하십시오.

[!DNL Adobe Target]은 권장 사항의 열기 시간 개인 맞춤화를 지원하지 않습니다.

>[!IMPORTANT]
>
>아래에 기술된 배달 API 및 rawbox 이메일 템플릿 방법(방법 1 및 2)에는 다음의 용량 가이드라인이 적용됩니다.
>
>* 요청의 비율은 초당 1,000개의 요청 또는 일일 최대 트래픽의 25배 중에서 낮은 것으로 제한되어야 합니다.
>* 매 분마다 초당 요청 수 200개인 단계의 램프 트래픽.
> 
>비율 제한을 높이려면 계정 관리자에게 문의하십시오.

## 방법 1: 배달 API 사용(권장) {#delivery-api}

배달 API는 작성 시간 이메일에 작동하는 POST 요청입니다. 이 옵션은 작성 시간 이메일의 선호되는 방법입니다.

대부분의 이메일 클라이언트에서는 POST를 요청할 수 없어, 이 API가 열기 시간 사용 사례에 적합하지 않습니다. Gmail 또는 Outlook 같은 일부 이메일 클라이언트는 콘텐츠를 캐시하거나 이미지를 차단하며, 받는 사람이 사전에 이미지 렌더링을 허용하도록 요구할 수 있습니다.

배달 API를 사용하여 기본 콘텐츠를 반환할 수 없습니다.

다음 코드는 샘플 API 게재 요청입니다.

```javascript
curl -X POST \ 
  'https://clientcode.tt.omtrdc.net/rest/v1/mbox/?client=clientcode' \ 
  -H 'authorization: Bearer 3423614b-4843-4664-83c4-c6c3f6c8869b' \ 
  -H 'cache-control: no-cache' \ 
  -H 'content-type: application/json' \ 
  -d '{ 
  "mbox" : "email-mbox", 
  "tntId" : "111499796294071-449025.28_44", 
  "requestLocation" : { 
    "host" : "prod" 
  }, 
   "profileParameters" : { 
   }, 
  "mboxParameters" : { 
    "at_property": "b468a242-64a4-32a0-ca0c-890bddd78789", 
    "entity.id": "article-123", 
    "entity.event.detailsOnly" : "true" 
  } 
  "contentAsJson":  true 
}'
```

여기서 `clientcode`는 [!DNL Target] 클라이언트 코드입니다.

>[!NOTE]
>
>모든 이메일 수신자(예: API 호출)에 대해 `sessionId` 및 `tntId` 또는 `thirdPartyId` 중 하나에 고유값을 제공해야 합니다. 이러한 필드에 고유한 값을 제공하지 않으면, 단일 프로필 내에서 많은 이벤트가 생성되어 API 응답이 느려지거나 실패할 수 있습니다.

자세한 내용은 [배달 API 설명서](https://experienceleague.corp.adobe.com/docs/target-dev/developer/implementation/delivery-api/overview.html)를 참조하십시오.{target=_blank}

## 방법 2: rawbox 이메일 템플릿 사용 {#rawbox}

rawbox는 mbox 요청과 유사하지만 ESP(이메일 서비스 공급자)와 같은 비웹 환경용입니다. rawbox 요청에 사용할 [!DNL Adobe Experience Platform Web SDK] 또는 [!DNL at.js]가 없으므로 요청을 수동으로 만들어야 합니다. 아래의 예에서는 이메일에서 rawbox 요청을 사용하는 방법을 설명합니다.

>[!NOTE]
>
>rawbox 및 [!DNL Target]을 사용하는 경우, [mbox 호출을  [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist)으로 보내도록 승인된 호스트를 지정하는 허용 목록 생성 아래의 중요 보안 알림을 참조하십시오.

이 접근 방법을 사용하면 이메일에 포함된 권장 사항의 성과를 추적하고 권장 사항을 사용하여 일반적인 방법으로 테스트하고 사이트에 대한 추적을 계속할 수 있습니다.

[양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) 선택 사항을 사용하여 [!DNL Target]에서 [!DNL Recommendations] 활동을 설정하십시오. 위치에 대해 ESP에서 제공되는 rawbox 요청에서 사용하기로 선택한 mbox의 이름을 선택합니다. 원하는 이메일의 모양과 느낌을 갖는 디자인을 선택합니다. 이메일 작성 시간에, ESP에서는 생성할 각 이메일의 각 rawbox에 대해 [!DNL Target] 서버를 호출합니다. ESP는 전송 시 이메일에 반환되는 HTML을 포함할 방법을 제공해야 합니다.

다음 시나리오를 처리할 수 있는 이메일 시스템을 사용해야 합니다.

### 유효한 응답이 수신되지만 권장 사항이 없음

* 이 경우 응답은 `mboxDefault` 매개 변수 값으로 설정됩니다. 이 매개 변수에 대해서는 아래 설명을 참조하십시오.
* 이메일 제공업체는 이 경우에 사용할 기본 권장 사항 HTML 블록을 제공해야 합니다.

### [!DNL Target] 서버는 시간 초과되고 데이터 없이 반환됩니다

* 이 경우 [!DNL Target] 서버는 다음 콘텐츠를 반환합니다.

   `//ERROR: application server timeout`

* 이메일 애플리케이션은 해당 텍스트를 검색하여 오류를 처리할 수 있어야 합니다. 이메일 제공업체는 이 경우를 처리하는 여러 가지 옵션을 제공합니다.

   * 다른 서버 호출을 즉시 시도합니다(시도 카운터를 사용하는 경우 권장됨).
   * 특정 이메일을 제외하고 다음 이메일을 계속 실행합니다.
   * 해당 특정 이메일을 큐에 추가하고, 초기 실행이 끝나면 실패한 이메일을 일괄로 다시 실행합니다.

### 샘플 요청 URL

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

### 필수 매개 변수: {#reqparams}

>[!NOTE]
>
>이메일에서 [!DNL Recommendations] 를 사용하기 위해 rawbox 호출은 권장 사항 기준의 유형에 따라 `entity.id` 또는 `entity.categoryId` 중 하나 또는 둘 다 포함해야 합니다. 위의 샘플 호출에는 둘 다 포함됩니다.

| 매개 변수 | 값 | 설명 | 유효성 검사 |
|--- |--- |--- |--- |
| `client_code` | *client_code* | Recommendations에 사용되는 클라이언트의 코드입니다. Adobe 컨설턴트가 이 값을 제공할 수 있습니다. |  |
| `mbox` | *mboxName* | 타기팅에 사용되는 mbox 이름입니다. | 모든 mbox 통화에 대해 동일한 유효성 검사입니다.<br>250자로 제한됩니다.<br>포함할 수 없는 문자는 다음과 같습니다. `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | 비활성화됨 | 응답이 비웹 환경에서 쿠키를 설정하지 못하도록 합니다. |  |
| `entity.id`<br>(특정 유형의 기준, 즉 보기/보기, 보기/구매, 구매/구매에 필요) | *entity_id* | 권장 사항의 기준이 되는 productId(예: 장바구니에서 구매하지 않은 제품 또는 이전 구매)입니다.<br>기준에 따라 필요한 경우, rawbox 호출에 `entity.id`를 포함해야 합니다. |  |
| `entity.event.detailsOnly` | true | `entity.id` 가 전달된 경우 이 매개 변수도 함께 전달하여 제품 보기 기반 알고리즘을 왜곡하지 않도록, 요청에 따라 항목에 대한 누적된 페이지 보기 수를 증분 되지 않게 하는 것이 좋습니다. |  |
| `entity.categoryId`<br>(특정 기준 유형, 즉 범주별로 가장 많이 본 항목 및 범주별 상위 판매자에 필요) | *category_id* | 권장 사항의 기준이 되는 범주(예: 범주의 최상위 판매자)입니다.<br>기준에 따라 필요한 경우, rawbox 호출에 `entity.categoryId`를 포함해야 합니다. |  |
| `mboxDefault` | *`https://www.default.com`* | `mboxNoRedirect` 매개 변수가 없으면, `mboxDefault` 매개 변수는 권장 사항을 사용할 수 없을 때 기본 콘텐츠를 반환하는 절대 URL이어야 합니다. 이 URL은 이미지 또는 기타 정적 콘텐츠일 수 있습니다.<br>. `mboxNoRedirect` 매개 변수가 있으면 `mboxDefault` 는 권장 사항이 없음을 나타내는 텍스트(예: `no_content`)일 수 있습니다.<br>이메일 공급자는 이 값이 반환되는 경우를 처리하고 기본 HTML을 이메일에 삽입해야 합니다. <br> **보안 모범 사례**: `mboxDefault` URL에 사용된 도메인이 허용 목록에 추가되지 않으면, 오픈 리디렉션 취약점의 위험에 노출될 수 있습니다. 리디렉터 링크 또는 `mboxDefault` 을 서드파티가 무단으로 사용하지 않도록 하려면, &quot;승인된 호스트&quot;를 사용하여 기본 리디렉션 URL 도메인을 허용 목록에 추가하는 것이 좋습니다. Target은 호스트를 사용하여 리디렉션을 허용할 도메인을 허용 목록에 추가합니다. 자세한 내용은 호스트에서 [mbox 호출을 *호스트*&#x200B;의  [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist)로 보내도록 승인된 호스트를 지정하는 허용 목록 생성을 참조하십시오. |  |
| `mboxHost` | *mbox_host* | 호출이 실행될 때 기본 환경(호스트 그룹)에 추가되는 도메인입니다. |  |
| `mboxPC` | Empty | (방문자 프로필을 사용하는 권장 사항에 필수입니다.)<br>&quot;thirdPartyId&quot;가 제공되지 않으면 새 tntId가 생성되고 응답의 일부로 반환됩니다. 그렇지 않으면 비어 있는 상태로 유지됩니다.<br>**참고**: 각 이메일 수신자에게(즉, 각 API 호출에 대해) `mboxSession` 및 `mboxPC` 의 고유한 값을 제공해야 합니다. 이러한 필드에 고유한 값을 제공하지 않으면, 단일 프로필 내에서 생성된 수많은 이벤트로 인해 API 응답이 느려지거나 실패할 수 있습니다. | 1 &lt; 길이 &lt; 128<br>둘 이상의 &quot;.&quot; (점)을 포함할 수 없습니다.<br>점은 프로필 위치 접미사에만 사용할 수 있습니다. |

### 선택적 매개 변수

| 매개 변수 | 값 | 설명 | 유효성 검사 |
|--- |--- |--- |--- |
| `mboxPC`<br>(선택 사항) | *mboxPCId* | Target 방문자 ID입니다. 여러 방문에서 사용자가 사이트로 처음 경로로 완전히 다시 돌아오는 경우를 추적하려고 하거나 사용자 프로필 매개 변수를 사용하는 경우 이 값을 사용하십시오.<br>이 값은 웹 사이트에서 CRM으로 내보내는 사용자의 실제 [!DNL Adobe Target] PCID여야 합니다. 이메일 공급자는 CRM 또는 데이터 웨어하우스에서 이 ID를 검색하고 이 매개 변수의 값에 사용합니다.<br>. `mboxPC` 값은 권장 사항이 A/B 활동의 일부인 경우 여러 방문에서 지표 추적을 위해 방문자 사이트 동작을 추적하는 데에도 유용합니다.<br>**참고**: 각 이메일 수신자에게(즉, 각 API 호출에 대해) `mboxSession` 및 `mboxPC` 의 고유한 값을 제공해야 합니다. 이러한 필드에 고유한 값을 제공하지 않으면, 단일 프로필 내에서 생성된 수많은 이벤트로 인해 API 응답이 느려지거나 실패할 수 있습니다. | 1 &lt; 길이 &lt; 128<br>둘 이상의 &quot;.&quot; (점)을 포함할 수 없습니다.<br>점은 프로필 위치 접미사에만 사용할 수 있습니다. |
| `mboxNoRedirect`<br>(선택 사항) | 1 | 기본적으로 호출자는 제공품 콘텐츠를 찾을 수 없을 때 리디렉션됩니다. 기본 작동을 비활성화하려면 사용하십시오. |  |
| `mbox3rdPartyId` | *xxx* | 프로필 타기팅에 사용할 사용자 고유의 사용자 지정 방문자 ID가 있는 경우, 이 옵션을 사용하십시오. |  |

### 발생할 수 있는 [!DNL Target] 서버 응답

| 응답 | 설명 |
|--- |--- |
| //오류: | 콘텐츠 반환할 수 없을 때 로드 밸런서에서 생성됨 |
| 성공 | `mboxNoRedirect` 매개 변수가 &#39;true&#39;로 설정되어 있고 서버가 권장 사항을 반환하지 않습니다(즉, mbox에 대한 일치 항목이 없거나 서버 캐시가 초기화되지 않음). |
| 잘못된 요청 | `mbox` 매개 변수가 누락되었습니다.<ul><li>`mboxDefault` 또는 `mboxNoRedirect` 매개 변수가 지정되지 않았습니다.</li><li>`mboxTrace` 요청 매개 변수는 지정되었지만 `mboxNoRedirect` 은 지정되지 않았습니다.</li><li>mbox 이름이 접미사 `-clicked`로 끝나면 `mboxTarget`매개 변수가 지정되지 않습니다.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | 요청에 대한 일치 항목이 없고 `mboxDefault` 매개 변수가 지정되지 않은 경우 `mboxNoRedirect` 가 지정되지 않습니다. |
| `Invalid mbox name:= MBOX_NAME` | `mbox` 매개 변수에 부적합한 문자가 포함되어 있음을 나타냅니다. |
| `Mbox name [MBOX_NAME] is too long` | `mbox` 매개 변수가 250자를 초과함을 나타냅니다. |

## 방법 3: 권장 사항 다운로드 API 사용 {#download-api}

다른 경우처럼 권장 사항을 설정하되, 템플릿 및 mbox 조합 대신 프레젠테이션 섹션에서 **다운로드 전용** 을 선택하십시오. 그런 다음 ESP에서, 만든 권장 사항 ID가 무엇인지를 ESP에 알려 주십시오. ESP는 API를 통해 권장 사항 데이터를 평가합니다. 이 데이터는 특정 범주 또는 키 항목(예: 장바구니에서 포기한 항목)에 대해 권장해야 하는 항목을 보여 줍니다. ESP는 이 데이터를 저장하고 자체 모양과 느낌으로 연결하며 각 항목에 대한 정보를 표시한 후 해당 정보를 이메일로 전달합니다.

이 옵션을 사용할 경우 권장 사항 서버가 권장 사항의 성과를 직접 추적할 수 없거나 여러 알고리즘/템플릿 조합 간에 트래픽을 분리할 수 없습니다. 또한 권장 사항은 방문자 프로필에 연결되지 않습니다.

다운로드 API에 대한 자세한 내용은 [이전 API > 다운로드](/help/main/assets/adobe-recommendations-classic.pdf)를 참조하십시오.
