---
keywords: 주문 확인;orderConfirmPage
description: Adobe Target의 기존 mbox.js 구현에 대해 알아봅니다. Adobe Experience Platform 웹 SDK(AEP 웹 SDK) 또는 최신 버전의 at.js로 마이그레이션합니다.
title: mbox.js를 사용하여 주문 확인 mbox를 만들려면 어떻게 합니까?
feature: at.js
role: Developer
exl-id: 952c2d1b-1ee8-4e9b-bce3-1c439127bb9b
translation-type: tm+mt
source-git-commit: 0a685427a047bfc0a2f5e81525b32df70af6d69f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 59%

---

# 주문 확인 mbox 만들기 - mbox.js

주문 확인 mbox는 사이트의 주문에 대한 세부 사항을 기록하고 매출 및 주문을 기준으로 보고할 수 있도록 합니다. 또한 주문 확인 mbox는 &quot;제품 x를 구입한 사람이 제품 y도 구입함&quot;과 같은 권장 사항 알고리즘을 유도할 수도 있습니다.

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리를 더 이상  [!DNL Adobe Target] 지원하지 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다.
>
>사이트에서 발생할 수 있는 문제를 방지하려면 모든 고객이 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [개요:클라이언트측 웹](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)에 대한 Target을 구현합니다.

>[!NOTE]
>
>* 사용자가 웹 사이트에서 구매를 수행하는 경우, 보고 작업을 위해 A4T(Analytics for Target)를 사용하더라도 주문 확인 mbox를 구현하는 것이 좋습니다.
   >
   >
* at.js 1에 대한 주문 확인 mbox를 만들 수도 있습니다.*동일한 방법* 사용;그러나 이  [!DNL at.js] 방법이 더 좋습니다. 자세한 내용은 [전환 추적](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)을 참조하십시오.
   >
   >
* at.js 2를 사용하는 경우&#x200B;*x*,  `mboxCreate` 더 이상 지원되지 않습니다. at.js 2를 사용하여 주문 확인을 위해.*x*, 다음 추적 관련 API를 사용하십시오. [trackEvent() ](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) 및  [sendNotifications()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md).


1. 주문 상세 정보 페이지에서 아래의 모델에 따라 mbox 스크립트를 삽입합니다.
1. WORDS IN CAPITAL LETTERS를 카탈로그의 동적 또는 정적 값과 교체합니다.

   >[!NOTE]
   >
   >여러 개의 제품 ID를 구분하려면 쉼표를 사용하십시오.

   **팁:** mbox에 주문 정보를 제공할 수도 있습니다(`orderConfirmPage`로 지칭할 필요가 없음). 주문 정보를 동일한 캠페인 내의 여러 mbox에 전달할 수도 있습니다.

   ```
   <div class="mboxDefault"> 
      <!-- CONTENT TO SHOW IF NO OFFERS AVAILABLE. --> 
   </div> 
   <script type="text/javascript">    
      mboxCreate('orderConfirmPage', 
      'productPurchasedId=PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3', 
      'orderTotal=ORDER TOTAL FROM YOUR ORDER PAGE', 
      'orderId=ORDER ID FROM YOUR ORDER PAGE'); 
   </script> 
   ```

주문 확인 mbox에서는 다음 매개 변수를 사용합니다.

| 매개 변수 | 설명 |
|--- |--- |
| `orderId` | 전환 계산을 위해 주문을 식별하는 고유한 값<br>`orderId`는 고유해야 합니다. 보고서에서 중복 주문은 무시됩니다. |
| `orderTotal` | 구매품의 통화 가치<br>통화 기호는 전달하지 마십시오. 소수점(쉼표 아님)을 사용하여 십진수 값을 표시합니다. |
| `productPurchasedId` (선택 사항) | 주문에서 구입한 제품 ID가 쉼표로 구분된 목록<br>이 제품 ID는 추가적인 보고 분석을 지원하기 위해 감사 보고서에 표시됩니다. |
