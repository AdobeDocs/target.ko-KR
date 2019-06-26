---
description: 'at. js에 대한 adobe. target. sendnotifications (options) 함수에 대한 정보입니다. '
seo-description: . js JavaScript 라이브러리의 Adobe Target에 대한 Adobe. target. sendnotifications (options) 함수에 대한 정보입니다.
seo-title: . js JavaScript 라이브러리의 Adobe Target에 대한 Adobe. target. sendnotifications (options) 함수에 대한 정보입니다.
solution: Target
subtopic: 시작하기
title: adobe. target. sendnotifications (options)
topic: Standard
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# adobe. target. sendnotifications (options)

This function sends a notification to Target edge when an experience is rendered without using `adobe.target.applyOffer()` or `adobe.target.applyOffers()`.

>[!NOTE]
>
>이 함수는. js 2.1.0에서 처음 소개되었으며 2.1.0 이상에서 사용할 수 있습니다.

| 키 | 유형 | 필수? | 설명 |
| --- | --- | --- | --- |
| consumerId | 문자열 | 아니오 | 기본값이 제공되지 않을 경우 기본값은 클라이언트의 글로벌 mbox입니다. 이 키는 A4T 통합에 사용되는 보조 데이터 ID를 생성하는 데 사용됩니다. |
| 요청 | 개체 | 예 | 아래의 &quot;요청&quot; 표를 참조하십시오. |
| timeout | 숫자 | 아니오 | 요청 시간 제한. 지정하지 않으면 기본값 at.js 시간 제한이 사용됩니다. |

## 요청

| 필드 이름 | 유형 | 필수? | 제한 사항 | 설명 |
| --- | --- | --- | --- | --- |
| 요청 &gt; 알림 | 객체 배열 | 예 |  | 표시된 컨텐츠, 클릭한 선택기 및/또는 방문 횟수 또는 mbox에 대한 알림. |
| 요청 &gt; 알림 &gt; 주소 | 개체 | 아니오 |  |  |
| 요청 &gt; 알림 &gt; 주소 &gt; URL | 문자열 | 아니오 |  | 알림이 실행된 URL. |
| 요청 &gt; 알림 &gt; 주소 &gt; 레퍼링url | 문자열 | 아니오 |  | 알림이 실행된 참조 URL. |
| 요청 &gt; 알림 &gt; 매개 변수 | 개체 | 아니오 | 매개 변수에는 다음 이름이 허용되지 않습니다.<ul><li>orderId</li><li>orderTotal</li><li>Productpurchasedids</li></ul>다음 사항을 고려하십시오.<ul><li>최대 50 개 매개 변수 제한.</li><li>매개 변수 이름은 비어 있으면 안 됩니다.</li><li>매개 변수 이름 최대 길이 128.</li><li>매개 변수 이름은 &quot;profile&quot; 로 시작하면 안 됩니다.</li><li>매개 변수 값 길이 max 5000.</li></ul> |  |
| 요청 &gt; 알림 &gt; Profileparameters | 개체 | 아니오 | 매개 변수에는 다음 이름이 허용되지 않습니다.<ul><li>orderId</li><li>orderTotal</li><li>Productpurchasedids</li></ul>다음 사항을 고려하십시오.<ul><li>최대 50 개 매개 변수 제한.</li><li>매개 변수 이름은 비어 있으면 안 됩니다.</li><li>매개 변수 이름 최대 길이 128.</li><li>매개 변수 이름은 &quot;profile&quot; 로 시작하면 안 됩니다.</li><li>매개 변수 값 길이 max 5000.</li></ul> |  |
| 요청 &gt; 알림 &gt; 주문 | 개체 | 아니오 |  | 순서 세부 사항을 설명하는 개체. |
| 요청 &gt; 알림 &gt; 주문 &gt; ID | 문자열 | 아니오 | `<=` 250자. | 주문 ID. |
| 요청 &gt; 알림 &gt; 주문 &gt; 합계 | 문자열 | 아니오 | `>=` 0 | 주문 총액. |
| 요청 &gt; 알림 &gt; 주문 &gt; Purchasedproductids | 문자열 배열 | 아니오 | <ul><li>빈 값은 허용되지 않습니다.</li><li>각 제품 ID 최대 길이 50.</li><li>제품 ID, 쉼표로 구분되고 연결된 제품 ID는 250 개를 초과할 수 없습니다.</li></ul> | 제품 ID 주문 |
| 요청 &gt; 알림 &gt; 제품 | 개체 | 아니오 |  |  |
| 요청 &gt; 알림 &gt; 제품 &gt; ID | 문자열 | 아니오 | `<=` 128 자; 비워 둘 수 없습니다. | 제품 ID. |
| 요청 &gt; 알림 &gt; 제품 &gt; Categoryid | 문자열 | 아니오 | `<=` 128 자; 비워 둘 수 없습니다. | 카테고리 ID. |
| 요청 &gt; 알림 &gt; ID | 문자열 | 예 | `<=` 200 자. | 알림 ID가 응답으로 반환되고 알림이 성공적으로 처리되었음을 나타냅니다. |
| 요청 &gt; 알림 &gt; 노출 IMPRESSIONID | 문자열 | 아니오 | `<= 128`자. | 노출 ID는 이전 알림을 사용하여 현재 알림을 stitch (링크) 하거나 요청을 실행하는 데 사용됩니다. 두 변수가 일치하는 경우 두 번째 및 기타 후속 요청은 활동 또는 경험에 새 인상을 생성하지 않습니다. |
| 요청 &gt; 알림 &gt; 유형 | 문자열 | 예 | «클릭» 또는 «디스플레이» 가 지원됩니다. | 알림 유형. |
| 요청 &gt; 알림 &gt; 타임스탬프 | 숫자`<int64>` | 예 |  | UNIX Epoch 이후 경과된 알림의 타임스탬프 (밀리초) 입니다. |
| 요청 &gt; 알림 &gt; 토큰 | 문자열 배열 | 예 |  | 알림 유형에 따라 표시된 컨텐츠 또는 클릭한 선택기의 토큰 목록입니다. |
| 요청 &gt; 알림 &gt; mbox | 개체 | 아니오 |  | mbox에 대한 알림. |
| 요청 &gt; 알림 &gt; mbox &gt; 이름 | 문자열 | 아니오 | 빈 값은 허용되지 않습니다.<br>허용되는 문자: 이 표 다음에 나오는 참고 사항을 참조하십시오. | mbox 이름. |
| 요청 &gt; 알림 &gt; mbox &gt; 상태 | 문자열 | 아니오 |  | mbox 상태 토큰입니다. |
| 요청 &gt; 알림 &gt; 보기 | 개체 | 아니오 |  |  |
| 요청 &gt; 알림 &gt; 보기 &gt; ID | 정수 `<int64>` | 아니오 |  | ID를 참조하십시오. 보기 API를 통해 보기를 만들 때 보기에 할당된 ID 입니다. |
| 요청 &gt; 알림 &gt; 보기 &gt; 이름 | 문자열 | 아니오 | `<= 128`자. | 보기 이름. |
| 요청 &gt; 알림 &gt; 보기 &gt; 키 | 문자열 | 아니오 | `<=` 512 자. | 키를 참조하십시오. API를 통해 보기에서 설정된 키. |
| 요청 &gt; 알림 &gt; 보기 &gt; 상태 | 문자열 | 아니오 |  | 상태 토큰을 봅니다. |

**** 참고: 다음 문자는 `Request > notifications > mbox > name`허용됩니다.

```
- '-, ./=`:;&!@#$%^&*()+|?~[]{}'
```

## Prefetched mbox 렌더링 후 sendnotifications () 호출

```
function createTokens(options) {
  return options.map(e => e.eventToken);
}

function createNotification(mbox, type, tokens) {
  const id = 11111; // here we should use a random ID like UUID
  const timestamp = Date.now();
  const { name, state, parameters, profileParameters, order, product } = mbox;
  const result = {
    id,
    type,
    timestamp,
    parameters,
    profileParameters,
    order,
    product
  };

  result.mbox = { name, state };
  result.tokens = tokens;

  return result;
}

adobe.target.getOffers({
  request: {
    prefetch: {
      mboxes: [
        {
          index: 0,
          name: "a1-serverside-ab"
        }
      ]
    }
  }
})
.then(response => {
  const mboxes = response.prefetch.mboxes;
  const notifications = mboxes.map(mbox => {
    const type = "display";
    const tokens = createTokens(mbox.options);

    return createNotification(mbox, type, tokens);
  });
  
  adobe.target.sendNotifications({
    request: { notifications }
  });
})
```

>[!NOTE]
>
>If you are using Adobe Analytics, `getOffers()` with prefetch only and `sendNotifications()`, the Analytics request must be fired after `sendNotifications()` is executed. The purpose of this is to ensure that the SDID generated by `sendNotifications()` will match the SDID sent to Analytics and Target.