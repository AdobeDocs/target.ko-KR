---
keywords: 이메일;ESP;이메일 서비스 제공업체;rawbox;게재 API;다운로드 전용 템플릿;이메일 템플릿;배치;작성 시간 이메일
description: '[!DNL Target] 배달 API, rawbox 템플릿 및 다운로드 전용 템플릿을 포함하여 이메일을 Adobe [!DNL Target Recommendations]과(와) 통합하는 방법을 알아봅니다.'
title: 추천를 이메일과 통합하려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 08fcb507-2c91-444a-b8ac-26165e359f6f
TQID: 'https://experienceleague.adobe.com/ZyeOl6ysM03a0mMiNgHuicOLPfgpXnrdqXJE1gHRRvE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1741'
ht-degree: 26%
---
# [!DNL Recommendations]을(를) 이메일과 통합 {#integrate-recs-email}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Target Recommendations]을(를) ESP(이메일 서비스 공급자)와 통합하여 이메일에 포함된 권장 사항의 전송 시간 개인 맞춤화를 수행하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Adobe Target]은 이메일에 포함된 권장 사항의 전송 시간 개인 맞춤화를 지원합니다. 권장 사항의 열기 시간 개인화는 지원되지 않습니다.

[!DNL Target Recommendations]을(를) ESP와 통합하는 방법에는 세 가지가 있습니다. ESP의 기능에 따라 사용할 방법이 결정되며 계정 관리자나 컨설턴트가 최상의 옵션을 선택하는 데 도움이 될 수 있습니다.

| 방법 | 세부 사항 |
| --- | --- |
| [방법 1: [!DNL Adobe Target Delivery API]](#delivery-api) (권장) | [!DNL Adobe Target Delivery API]을(를) 사용하여 고객당, 이메일당 권장 사항에 대한 요청을 만듭니다. |
| [방법 2: [!DNL Adobe Rawbox API]](#rawbox) | [!DNL Adobe Target Rawbox API]을(를) 사용하여 고객당, 이메일당 권장 사항에 대한 요청을 만듭니다. |
| [방법 3: [!DNL Recommendations Download API]](#download-api) | [!DNL Recommendations Download API]을(를) 사용하여 제품 또는 범주 목록에 대한 권장 사항을 CSV 형식으로 일괄 요청합니다. |

방법 1과 2를 사용하려면 ESP가 고객별로, 이메일별로 외부 API를 호출하고 콘텐츠가 반환될 때까지 기다려야 합니다. 모든 ESP가 이러한 방법을 지원하는 것은 아니므로 ESP에 연락하여 이 통합 패턴과 호환되는지 확인해야 합니다.

방법 3은 ESP가 권장 사항 목록을 제품 ID 또는 범주 ID로 이메일 목록에 등록해야 합니다. 이 조인은 마지막으로 본 제품, 마지막으로 구매한 제품 또는 고객의 가장 많이 본 범주와 같은 속성을 기반으로 할 수 있습니다. 가입을 수행하려면 ESP에 고객 프로필의 이 데이터에 대한 액세스 권한이 있어야 하므로 ESP에 연락하여 이 데이터에 대한 액세스 권한이 있고 이 통합 패턴과 호환되는지 확인해야 합니다.

>[!IMPORTANT]
>
>배달 API 및 rawbox 이메일 템플릿 메서드(메서드 1 및 2)에는 다음 용량 가이드라인이 적용됩니다.
>
>* 요청의 비율은 초당 1,000개의 요청 또는 일일 최대 트래픽의 25배 중에서 낮은 것으로 제한되어야 합니다.
>* 트래픽은 분당 초당 요청 수 200개로 단계적으로 증가해야 합니다.
>
>비율 제한을 높이려면 계정 관리자에게 문의하십시오.

## 방법 1: 배달 API 사용(권장) {#delivery-api}

배달 API는 작성 시간 이메일에 작동하는 POST 요청입니다. 이 옵션은 작성 시간 이메일의 선호되는 방법입니다.

대부분의 이메일 클라이언트는 POST 요청을 허용하지 않으므로 이 API는 열기 시간 사용 사례에 권장되지 않습니다. Gmail 또는 Outlook과 같은 일부 이메일 클라이언트는 콘텐츠를 캐시하거나 이미지를 차단하며, 받는 사람이 사전에 이미지 렌더링을 허용하도록 요구할 수 있습니다.

배달 API를 사용하여 기본 콘텐츠를 반환할 수 없습니다.

다음 코드는 샘플 API 배달 요청입니다. 여기서 `clientcode`은(는) [!DNL Target] 클라이언트 코드입니다.

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

>[!NOTE]
>
>각 전자 메일 수신자(각 API 호출)에 대해 `sessionId`과(와) `tntId` 또는 `thirdPartyId` 중 하나의 고유 값을 제공합니다. 이러한 필드에 고유한 값이 없으면 단일 프로필 내에서 생성된 많은 이벤트로 인해 API 응답이 느려지거나 실패할 수 있습니다.

자세한 내용은 [배달 API 설명서](https://experienceleague.adobe.com/docs/target-dev/developer/api/delivery-api/overview.html?lang=ko){target=_blank}를 참조하세요.

## 방법 2: rawbox 이메일 템플릿 사용 {#rawbox}

rawbox는 mbox 요청과 유사하지만 ESP(이메일 서비스 공급자)와 같은 비웹 환경용입니다. [!DNL Adobe Experience Platform Web SDK] 및 [!DNL at.js]은(는) rawbox 요청에 사용할 수 없으므로 요청을 수동으로 만들어야 합니다. 다음 예에서는 이메일에서 rawbox 요청을 사용하는 방법을 설명합니다.

이 접근 방식을 사용하면 이메일에 포함된 권장 사항의 성능을 추적하고 권장 사항을 사용하여 일반적인 방법으로 테스트하고 사이트에서 추적을 계속할 수 있습니다.

>[!NOTE]
>
>rawbox 및 [!DNL Target]을 사용하는 경우, [mbox 호출을  [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist)으로 보내도록 승인된 호스트를 지정하는 허용 목록 생성 아래의 중요 보안 알림을 참조하십시오.

1. [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md) 옵션을 사용하여 [!DNL Target]에서 [!DNL Recommendations] 활동을 설정하십시오.

1. 위치에 대해 ESP에서 제공되는 rawbox 요청에 사용되는 mbox 이름을 선택합니다.

1. 이메일에 원하는 모양과 느낌을 가진 디자인을 선택합니다.

이메일 작성 시간에, ESP에서는 생성할 각 이메일의 각 rawbox에 대해 [!DNL Target] 서버를 호출합니다. ESP에는 전송 시 이메일에 반환되는 HTML을 포함할 수 있는 방법이 있어야 합니다.

이메일 시스템은 다음 시나리오를 처리할 수 있어야 합니다.

### 유효한 응답이 수신되지만 권장 사항이 없음

* 응답은 `mboxDefault` 매개 변수에 설정된 값입니다. 필수 매개변수 테이블에서 이 매개변수에 대한 설명을 참조하십시오.
* 이메일 제공업체는 이 경우에 사용할 기본 권장 사항 HTML 블록을 제공해야 합니다.

### [!DNL Target] 서버는 시간 초과되고 데이터 없이 반환됩니다

* [!DNL Target] 서버가 다음 콘텐츠를 반환합니다.

  `//ERROR: application server timeout`

* 이메일 애플리케이션은 해당 텍스트를 검색하여 오류를 처리할 수 있어야 합니다. 이메일 제공업체는 이 경우를 처리하는 여러 가지 옵션을 제공합니다.

  * 다른 서버 호출을 즉시 시도합니다(시도 카운터를 사용하는 경우 권장됨).
  * 해당 특정 이메일을 삭제하고 다음 이메일을 계속 진행합니다.
  * 해당 특정 이메일을 큐에 추가하고 초기 실행이 끝나면 실패한 이메일을 일괄로 다시 실행합니다.

### 샘플 요청 URL

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

### 필수 매개 변수 {#reqparams}

>[!NOTE]
>
>이메일에서 [!DNL Recommendations]을(를) 사용하려면 rawbox 호출은 권장 사항 기준의 유형에 따라 일반적으로 `entity.id` 또는 `entity.categoryId` 중 하나 또는 둘 다 포함해야 합니다. 위의 샘플 호출에는 둘 다 포함됩니다.

| 매개 변수 | 값 | 설명 | 유효성 검사 |
|--- |--- |--- |--- |
| `client_code` | *client_code* | [!DNL Recommendations]에서 사용되는 클라이언트 코드입니다. Adobe 컨설턴트가 이 값을 제공할 수 있습니다. |  |
| `mbox` | *mboxName* | 타기팅에 사용되는 mbox 이름입니다. | 모든 mbox 호출에 대해 동일한 유효성 검사.<br>250자 제한.<br>포함할 수 없는 문자는 다음과 같습니다. `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | 비활성화됨 | 응답이 비웹 환경에서 쿠키를 설정하지 못하도록 합니다. |  |
| `entity.id`<br>(특정 유형의 기준, 즉 보기/보기, 보기/구매, 구매/구매에 필요) | *entity_id* | 장바구니의 구매하지 않은 제품 또는 이전 구매와 같이 권장 사항의 기반이 되는 productId입니다.<br>기준에 따라 필요한 경우, rawbox 호출에 `entity.id`를 포함해야 합니다. |  |
| `entity.event.detailsOnly` | true | `entity.id`이(가) 전달된 경우 이 매개 변수를 전달하면 제품 보기 기반 알고리즘을 왜곡하지 않도록 요청에 따라 항목에 대한 누적된 페이지 보기 수를 늘릴 수 없습니다. |  |
| `entity.categoryId`<br>(특정 기준 유형, 즉 범주별로 가장 많이 본 항목 및 범주별 상위 판매자에 필요) | *category_id* | 권장 사항의 기준이 되는 범주(예: 범주의 최상위 판매자)입니다.<br>기준에 따라 필요한 경우, rawbox 호출에 `entity.categoryId`를 포함해야 합니다. |  |
| `mboxDefault` | *`https://www.default.com`* | `mboxNoRedirect` 매개 변수가 없으면, `mboxDefault` 매개 변수는 권장 사항을 사용할 수 없을 때 기본 콘텐츠를 반환하는 절대 URL이어야 합니다. 이 URL은 이미지 또는 기타 정적 콘텐츠일 수 있습니다.<br>매개 변수 `mboxNoRedirect`이(가) 있으면 `mboxDefault`은(는) 권장 사항이 없음을 나타내는 텍스트(예: `no_content`)일 수 있습니다.<br>전자 메일 공급자는 이 값이 반환되는 경우를 처리하고 기본 HTML을 전자 메일에 삽입해야 합니다.<br>표 아래의 보안 모범 사례를 참조하십시오. |  |
| `mboxHost` | *mbox_host* | 호출이 실행될 때 기본 환경(호스트 그룹)에 추가되는 도메인입니다. |  |
| `mboxPC` | Empty | (방문자 프로필을 사용하는 권장 사항에 필요합니다.)<br>제공된 &quot;thirdPartyId&quot;가 없는 경우 새 tntId가 생성되고 응답의 일부로 반환됩니다. 그렇지 않으면 값이 비어 있는 상태로 유지됩니다.<br>표 아래의 고유 값에 대한 메모를 참조하세요. | 1 &lt; 길이 &lt; 128<br>둘 이상의 &quot;.&quot; (점).<br>점은 프로필 위치 접미사에만 사용할 수 있습니다. |

### 선택적 매개 변수

| 매개 변수 | 값 | 설명 | 유효성 검사 |
|--- |--- |--- |--- |
| `mboxPC`<br>(선택 사항) | *mboxPCId* | [!DNL Target] 방문자 ID. 이 값을 사용하여 여러 방문에서 또는 사용자 프로필 매개 변수를 사용할 때 사이트로 전체 회선을 이동하는 사용자를 추적합니다.<br>이 값은 웹 사이트에서 CRM으로 내보내는 사용자의 실제 [!DNL Adobe Target] PCID여야 합니다. 이메일 공급자는 CRM 또는 데이터 웨어하우스에서 이 ID를 검색하고 이 매개 변수의 값으로 사용합니다.<br>권장 사항이 A/B 활동의 일부인 경우 `mboxPC` 값은 지표 추적을 위해 여러 방문에서 방문자 사이트 동작을 추적하는 데에도 유용합니다.<br>표 아래의 고유 값에 대한 메모를 참조하세요. | 1 &lt; 길이 &lt; 128<br>둘 이상의 &quot;.&quot; (점).<br>점은 프로필 위치 접미사에만 사용할 수 있습니다. |
| `mboxNoRedirect`<br>(선택 사항) | 1 | 기본적으로 호출자는 제공품 콘텐츠를 찾을 수 없을 때 리디렉션됩니다. 이 매개 변수를 사용하여 기본 동작을 비활성화합니다. |  |
| `mbox3rdPartyId` | *xxx* | 이 옵션을 사용하여 프로필 타깃팅에 대한 사용자 지정 방문자 ID를 지정합니다. |  |

`mboxSession` 및 `mboxPC`에 대해 각 전자 메일 수신자(각 API 호출)에 대해 고유한 값을 제공하십시오. 이러한 필드에 고유한 값이 없으면 단일 프로필 내에서 생성된 수많은 이벤트로 인해 API 응답이 느려지거나 실패할 수 있습니다.

`mboxDefault`에 대한 보안 모범 사례로 권한 있는 호스트를 사용하여 기본 리디렉션 URL 도메인을 허용 목록 하십시오. `mboxDefault` URL에 사용된 도메인이 허용 목록에추가된이 아닌 경우 오픈 리디렉션 취약점의 위험이 노출될 수 있습니다. 승인된 호스트는 리디렉터 링크 또는 `mboxDefault`을(를) 서드파티가 무단으로 사용하지 않도록 합니다. [!DNL Target]은(는) 리디렉션이 허용되는 도메인에 호스트를 사용합니다. 자세한 내용은 이 섹션의 시작 부분에 있는 보안 알림을 참조하십시오.

### 발생할 수 있는 [!DNL Target] 서버 응답

| 응답 | 설명 |
|--- |--- |
| //오류: | 콘텐츠를 반환할 수 없을 때 로드 밸런서에서 생성됩니다. |
| 성공 | `mboxNoRedirect` 매개 변수가 &#39;true&#39;로 설정되어 있고 서버가 권장 사항을 반환하지 않습니다(mbox에 대한 일치 항목이 없거나 서버 캐시가 초기화되지 않음). |
| 잘못된 요청 | `mbox` 매개 변수가 누락되었습니다.<ul><li>`mboxDefault` 또는 `mboxNoRedirect` 매개 변수가 지정되지 않았습니다.</li><li>`mboxTrace` 요청 매개 변수는 지정되었지만 `mboxNoRedirect`은(는) 지정되지 않았습니다.</li><li>mbox 이름이 `-clicked` 접미사로 끝나면 `mboxTarget` 매개 변수가 지정되지 않습니다.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | 요청에 대한 일치 항목이 없고 `mboxNoRedirect` 매개 변수가 지정되지 않은 경우 `mboxDefault`이(가) 지정되지 않습니다. |
| `Invalid mbox name:= MBOX_NAME` | `mbox` 매개 변수에 잘못된 문자가 있습니다. |
| `Mbox name [MBOX_NAME] is too long` | `mbox` 매개 변수가 250자를 초과합니다. |

## 방법 3: 권장 사항 다운로드 API 사용 {#download-api}

다른 경우처럼 권장 사항을 설정하되, 템플릿 및 mbox 조합 대신 프레젠테이션 섹션에서 **다운로드 전용** 을 선택하십시오. 그런 다음 생성된 권장 사항의 ID를 ESP에 제공합니다. ESP는 API를 통해 추천 데이터에 접근한다. 이 데이터는 특정 범주 또는 키 항목(예: 장바구니에서 포기한 항목)에 대해 권장해야 하는 항목을 보여 줍니다. ESP는 이 데이터를 저장하고, 고유의 모양과 느낌으로 연결하고, 각 항목에 대한 정보를 표시하고 이를 이메일로 전달합니다.

이 옵션을 사용하면 권장 사항 서버가 권장 사항의 성능을 직접 추적하거나 여러 알고리즘 및 템플릿 조합 간에 트래픽을 분할할 수 없습니다. 또한 권장 사항은 방문자 프로필에 연결되지 않습니다.

다운로드 API에 대한 자세한 내용은 [이전 API > 다운로드](/help/main/assets/adobe-recommendations-classic.pdf)를 참조하십시오.
