---
description: 주문 확인 mbox는 사이트의 주문에 대한 세부 사항을 기록하고 매출 및 주문을 기준으로 보고할 수 있도록 합니다. 또한 주문 확인 mbox는 "제품 x를 구입한 사람이 제품 y도 구입함"과 같은 권장 사항 알고리즘을 유도할 수도 있습니다.
keywords: 주문 확인;orderConfirmPage
seo-description: 주문 확인 mbox는 사이트의 주문에 대한 세부 사항을 기록하고 매출 및 주문을 기준으로 보고할 수 있도록 합니다. 또한 주문 확인 mbox는 "제품 x를 구입한 사람이 제품 y도 구입함"과 같은 권장 사항 알고리즘을 유도할 수도 있습니다.
seo-title: 주문 확인 mbox 만들기 - mbox.js
solution: Target
subtopic: 시작하기
title: 주문 확인 mbox 만들기 - mbox.js
uuid: 001da2bd-2ccf-490b-ba84-ac9b9a2a5451
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 주문 확인 mbox 만들기 - mbox.js{#create-an-order-confirmation-mbox-mbox-js}를 참조하십시오

주문 확인 mbox는 사이트의 주문에 대한 세부 사항을 기록하고 매출 및 주문을 기준으로 보고할 수 있도록 합니다. 또한 주문 확인 mbox는 &quot;제품 x를 구입한 사람이 제품 y도 구입함&quot;과 같은 권장 사항 알고리즘을 유도할 수도 있습니다.

>[!NOTE]
>
>사용자가 웹 사이트에서 구매를 수행하는 경우, 보고 작업을 위해 A4T(Analytics for Target)를 사용하더라도 주문 확인 mbox를 구현하는 것이 좋습니다.

>[!NOTE]
>
>동일한 메서드를 사용하여 에 대한 주문 확인 mbox를 만들 수도 있지만 [!DNL at.js]at.js 메서드가 선호됩니다. 자세한 내용은 [전환 추적](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)을 참조하십시오.

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