---
keywords: adobe.target.알림 보내기;알림전송;알림 보내기;알림 보내기;알림;at.js;함수;함수
description: at.js에 adobe.target.sendNotifications() 를 사용하여 알림을 [!DNL Target] applyOffer를 사용하지 않고 경험을 렌더링할 때 edge. (at.js 2.1 +)
title: adobe.target.sendNotifications() 함수를 사용하려면 어떻게 해야 합니까?
feature: at.js
role: Developer
exl-id: 71b7167d-729c-4d43-8f54-f43619e14f32
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 94%

---

# adobe.target.sendNotifications(options)

이 함수는 `adobe.target.applyOffer()` 또는 `adobe.target.applyOffers()`를 사용하지 않고 경험을 렌더링할 때 Target Edge에 알림을 보냅니다.

>[!NOTE]
>
>이 함수는 at.js 2.1.0에서 처음 소개되었으며, 2.1.0 이상 버전에서 사용할 수 있습니다.

| 키 | 유형 | 필수? | 설명 |
| --- | --- | --- | --- |
| consumerId | 문자열 | 아니오 | 기본값이 제공되지 않을 경우 기본값은 클라이언트의 글로벌 mbox입니다. 이 키는 A4T 통합에 사용되는 보조 데이터 ID를 생성하는 데 사용됩니다. |
| 요청 | 개체 | 예 | 아래의 &quot;요청&quot; 표를 참조하십시오. |
| timeout | 숫자 | 아니오 | 요청 시간 제한. 지정하지 않으면 기본값 at.js 시간 제한이 사용됩니다. |

## 요청

| 필드 이름 | 유형 | 필수? | 제한 사항 | 설명 |
| --- | --- | --- | --- | --- |
| Request > notifications | 개체 배열 | 예 |  | 표시된 콘텐츠, 클릭한 선택기 및/또는 방문 보기 또는 mbox에 대한 알림입니다. |
| Request > notifications > address | 개체 | 아니오 |  |  |
| Request > notifications > address > url | 문자열 | 아니오 |  | 알림이 실행된 URL입니다. |
| Request > notifications > address > referringUrl | 문자열 | 아니오 |  | 알림이 실행된 참조 URL입니다. |
| Request > notifications > parameters | 문자열 | 아니오 | 매개 변수에는 다음 이름을 사용할 수 없습니다.<ul><li>orderId</li><li>orderTotal</li><li>productPurchasedIds</li></ul>다음 사항을 고려하십시오.<ul><li>매개 변수의 수는 최대 50개로 제한됩니다.</li><li>매개 변수 이름은 비워둘 수 없습니다.</li><li>매개 변수 이름은 최대 128자입니다.</li><li>매개 변수 이름은 &quot;profile&quot;로 시작하면 안 됩니다.</li><li>매개 변수 값의 최대 길이는 5000입니다.</li></ul> |  |
| Request > notifications > profileParameters | 문자열 | 아니오 | 매개 변수에는 다음 이름을 사용할 수 없습니다.<ul><li>orderId</li><li>orderTotal</li><li>productPurchasedIds</li></ul>다음 사항을 고려하십시오.<ul><li>매개 변수의 수는 최대 50개로 제한됩니다.</li><li>매개 변수 이름은 비워둘 수 없습니다.</li><li>매개 변수 이름은 최대 128자입니다.</li><li>매개 변수 이름은 &quot;profile&quot;로 시작하면 안 됩니다.</li><li>매개 변수 값의 최대 길이는 5000입니다.</li></ul> |  |
| Request > notifications > order | 개체 | 아니오 |  | 순서 세부 사항을 설명하는 개체입니다. |
| Request > notifications > order > id | 문자열 | 아니오 | `<=` 250자. | 주문 ID. |
| Request > notifications > order > total | 문자열 | 아니오 | `>=` 0 | 주문 총액. |
| Request > notifications > order > purchasedProductIds | 문자열의 배열 | 아니오 | <ul><li>값을 비워둘 수 없습니다.</li><li>각 제품 ID의 최대 길이는 50자입니다.</li><li>쉼표로 구분되고 연결된 제품 ID의 최대 길이가 250자를 초과하면 안 됩니다.</li></ul> | 주문 제품 ID입니다. |
| Request > notifications > product | 개체 | 아니오 |  |  |
| Request > notifications > product > id | 문자열 | 아니오 | `<=` 128자이며, 비워 둘 수 없습니다. | 제품 ID. |
| Request > notifications > product > categoryId | 문자열 | 아니오 | `<=` 128자이며, 비워 둘 수 없습니다. | 카테고리 ID입니다. |
| Request > notifications > id | 문자열 | 예 | `<=` 200자. | 알림 ID가 응답으로 반환되고, 알림이 성공적으로 처리되었음을 나타냅니다. |
| Request > notifications > impressionId | 문자열 | 아니오 | `<= 128`자. | 노출 ID는 이전 알림을 사용하여 현재 알림을 연결(링크)하거나 요청을 실행하는 데 사용됩니다. 둘 다 일치하는 경우 두 번째와 다른 후속 요청이 활동 또는 경험에 대한 새로운 노출을 생성하지 않습니다. |
| Request > notifications > type | 문자열 | 예 | click 또는 display가 지원됩니다. | 알림 유형입니다. |
| Request > notifications > timestamp | 숫자`<int64>` | 예 |  | UNIX Epoch 이후 경과된 알림의 타임스탬프(밀리초)입니다. |
| Request > notifications > tokens | 문자열의 배열 | 예 |  | 알림 유형에 따라 표시된 콘텐츠 또는 클릭한 선택기에 대한 토큰 목록입니다. |
| Request > notifications > mbox | 개체 | 아니오 |  | mbox에 대한 알림입니다. |
| Request > notifications > mbox > name | 문자열 | 아니오 | 값을 비워둘 수 없습니다.<br>허용된 문자: 이 표 다음에 나오는 참고 사항을 참조하십시오. | mbox 이름. |
| Request > notifications > mbox > state | 문자열 | 아니오 |  | mbox 상태 토큰입니다. |
| Request > notifications > view | 개체 | 아니오 |  |  |
| Request > notifications > view > id | 정수 `<int64>` | 아니오 |  | ID 보기. API 보기를 통해 보기를 만들 때 보기에 지정된 ID입니다. |
| Request > notifications > view > name | 문자열 | 아니오 | `<= 128`자. | 보기의 이름입니다. |
| Request > notifications > view > key | 문자열 | 아니오 | `<=` 512자. | 키 보기. API를 통해 보기에 설정된 키입니다. |
| Request > notifications > view > state | 문자열 | 아니오 |  | 상태 토큰 보기. |

**참고**: 다음 문자는 다음과 같습니다 *not* 허용 `Request > notifications > mbox > name`:

```
- '-, ./=`:;&!@#$%^&*()+|?~[]{}'
```

## 프리페치된 mbox 렌더링 후 sendNotifications() 호출

```javascript
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
>Adobe Analytics에서 프리페치만 사용하는 `getOffers()`와 `sendNotifications()`를 사용하는 경우 `sendNotifications()`가 실행된 후에 Analytics 요청을 실행해야 합니다. 목적은 `sendNotifications()`에서 생성한 SDID가 Analytics와 Target에 전송된 SDID와 일치하는지 확인하는 것입니다.
