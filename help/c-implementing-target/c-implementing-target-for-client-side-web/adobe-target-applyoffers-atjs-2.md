---
description: 'at.js에 대한 adobe.target.applyOffers() 함수 정보입니다. '
keywords: adobe.target.applyOffers;applyOffers;applyoffers;apply offers;at.js;functions;functions
seo-description: Adobe Target at.js JavaScript 라이브러리에 대한 adobe.target.applyOffers(options) 함수 정보입니다.
seo-title: Adobe Target at.js JavaScript 라이브러리에 대한 adobe.target.applyOffers(options) 함수 정보입니다.
solution: Target
subtopic: 시작하기
title: adobe.target.applyOffers(options)
topic: Standard
translation-type: tm+mt
source-git-commit: ef2c4ac78fef5889d5a6e9e053dfd36b77919dd4

---


# adobe.target.applyOffers(options) - at.js 2.x

이 함수를 사용하면 `adobe.target.getOffers()`로 검색된 오퍼를 두 개 이상 적용할 수 있습니다.

>[!NOTE]
>
>이 함수는 at.js 2.x에서 도입되었으며, at.js 버전 1.*x*&#x200B;에는 사용할 수 없습니다.

| 키 | 유형 | 필수? | 설명 |
| --- | --- | --- | --- |
| selector | 문자열 | 아니오 | [!DNL Target]이 오퍼 컨텐츠를 배치해야 하는 HTML 요소를 식별하는 데 사용되는 HTML 요소 또는 CSS 선택기입니다. 선택기를 제공하지 않으면 [!DNL Target]에서는 사용해야 하는 HTML 요소를 HTML HEAD로 간주합니다. |
| 응답 | 개체 | 예 | `getOffers()`의 응답 개체.<br>아래의 "요청" 표를 참조하십시오. |

## 응답

| 필드 이름 | 설명 |
| --- | --- |
| response &gt; prefetch &gt; views &gt; options &gt; content | "선택 사항"의 컨텐츠가 잘 정의되어 있지 않으며 선택 사항 유형/템플릿 구조에 직접적으로 의존합니다. |
| response &gt; prefetch &gt; views &gt; options &gt; type | 선택 사항 유형. "컨텐츠" 필드의 유형을 반영합니다. 지원되는 유형은 작업입니다. |
| response &gt; prefetch &gt; views &gt; state | 보기에 대한 디스플레이 알림과 함께 전달해야 하는 불투명 보기 상태 토큰 |
| response &gt; prefetch &gt; views &gt; options &gt; responseTokens | 현재 선택 사항이 처리 중일 때 수집된 `responseTokens`의 맵을 포함합니다. |
| response &gt; prefetch &gt; views &gt; analytics &gt; payload | 보기가 적용된 후 Analytics에 전송해야 하는 클라이언트측 통합을 위한 Analytics 페이로드. |
| response &gt; prefetch &gt; views &gt; trace | 보기당 미리 가져오기 호출에 대한 모든 추적 데이터를 포함하는 개체.<br>추적 개체에는 추적용 버전도 포함됩니다.<br>추적 개체에는 현재 보기에 대한 세부 정보도 포함됩니다. |
| response &gt; prefetch &gt; views &gt; options &gt; eventToken | 이벤트 로깅은 선택 사항별로 수행됩니다. 적용된 모든 선택 사항에 대해 각각의 이벤트 토큰을 알림 토큰 목록에 추가해야 합니다. 보기는 여러 선택 사항으로 구성됩니다. 모든 선택 사항이 적용되어 표시되면 모든 `eventTokens`이 알림에 포함되어야 합니다. |
| response &gt; prefetch &gt; views &gt; name | 사람이 읽을 수 있는 보기 이름. |
| response &gt; prefetch &gt; views &gt; metrics | 감시하고 [!DNL Target]에 알려야 하는 보고 지표. 현재, 클릭 지표만 지원됩니다. 요소를 클릭하면 적절한 `eventTokens`가 수집되고 알림이 전송되어야 합니다. |
| response &gt; prefetch &gt; views &gt; key | 보기를 식별하는 키 또는 지문. |
| response &gt; prefetch &gt; views &gt; id | 보기의 ID. |
| 응답 &gt; 알림 &gt; ID | 알림 ID. |
| response &gt; notifications &gt; events &gt; type | 알림, 클릭 또는 표시의 유형. |
| response &gt; notifications &gt; events &gt; trace | 알림 이벤트에 대한 추적. |
| response &gt; notifications &gt; events &gt; token | 알림 이벤트와 함께 전송된 토큰. |
| response &gt; notifications &gt; events &gt; timestamp | 알림 이벤트와 함께 전송된 타임스탬프. |
| response &gt; notifications &gt; events &gt; errorCode | 알림이 실패한 경우 코드가 실패 이유를 나타냅니다. |
| response &gt; notifications &gt; events | 현재 알림에 대해 기록되었거나 기록되지 않은 이벤트. |
| response &gt; notifications | 기록되었거나 실패한 알림을 가리킵니다. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; trace | 개별 mbox 요청에 대한 모든 추적 데이터를 포함하는 개체. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; responseTokens | 특정 mbox 요청 실행을 위한 `responseTokens`의 맵을 포함합니다. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; option &gt; content | "선택 사항"의 컨텐츠가 잘 정의되어 있지 않으며 선택 사항 유형/템플릿 구조에 직접적으로 의존합니다. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; option &gt; type | 선택 사항 유형. "컨텐츠" 필드의 유형을 반영합니다. 지원되는 유형은 html, 리디렉션, JSON 및 다이내믹입니다. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; options | 응답 선택 사항. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; metrics &gt; eventToken | 클릭 이벤트의 토큰. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; metrics &gt; type | "click" |
| response &gt; execute &gt; mboxes &gt; mbox &gt; metrics | `clickThrough` 지표 목록을 포함합니다. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; mbox | mbox의 이름. |
| response &gt; execute &gt; mboxes &gt; mbox &gt;index | 응답이 요청에서 나온 이 색인이 있는 mbox용임을 나타냅니다. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; analytics &gt; payload | mbox가 적용된 후 Analytics에 전송해야 하는 클라이언트측 통합을 위한 Analytics 페이로드. (A4T 사용 "캠페인" 섹션을 참조하십시오.) |
| response &gt; execute &gt; mboxes | 실행된 mbox 목록. |
| response &gt; execute &gt; pageLoad &gt; options &gt; content | "선택 사항"의 컨텐츠가 잘 정의되어 있지 않으며 선택 사항 유형/템플릿 구조에 직접적으로 의존합니다. |
| response &gt; execute &gt; pageLoad &gt; options &gt; type | 선택 사항 유형. "컨텐츠" 필드의 유형을 반영합니다. 지원되는 유형은 html, 리디렉션, JSON, 다이내믹 및 작업입니다. |
| response &gt; execute &gt; pageLoad &gt; options | 보기를 기준으로 그룹화되지 않은 선택 사항(target-global-mbox + 보기를 기준으로 그룹화되지 않은 보기를 사용하는 활동의 선택 사항). |
| response &gt; execute &gt; pageLoad &gt; metrics | 특정 보기에 속하도록 설정되지 않은 클릭 지표. |
| response &gt; execute &gt; pageLoad &gt; trace | pageLoad 요청에 대한 모든 추적 데이터를 포함하는 개체. |
| response &gt; execute &gt; pageLoad &gt; analytics &gt; payload | 페이지 로드 컨텐츠가 적용된 후 Analytics에 전송해야 하는 클라이언트측 통합을 위한 Analytics 페이로드. (A4T 사용 "캠페인" 섹션을 참조하십시오.) |

## applyOffers() 호출 예

```
adobe.target.applyOffers({response:{
  "execute": {
    "pageLoad": {
      "options": [{
        "type": "html",
        "content": "page-load"
      },
      {
        "type": "actions",
        "content": [{
          "type": "setHtml",
          "content": "<h1>Container 1</h1>",
          "selector": "#container1",
          "cssSelector": "#container1"
        },
        {
          "type": "setHtml",
          "content": "<h3>Container 3</h3>",
          "selector": "#container3",
          "cssSelector": "#container3"
        }]
      }],
 
 
      "metrics": [{
        "type": "click",
        "selector": "#container1",
        "eventToken": "page-load-click-metric" 
      }]
    }
  }
}});
```

## `getOffers()` 및 `applyOffers()`가 Promise 기반이므로 이 함수를 사용하는 Promise 체인 호출 예

```
adobe.target.getOffers({...})
.then(response => adobe.target.applyOffers({ response: response }))
.then(() => console.log("Success"))
.catch(error => console.log("Error", error));
```
