---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 2c4f5666b65bfc36885aad3907639a309e8c69f2
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 59%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2023년 14월 3일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이들 페이지에 대한 정보는 릴리스 일자에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target] Standard/Premium 22.15.1(2023년 3월 8일, 9일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **3월 8일**: 아메리카 지역
* **3월 9일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **3월 9일**: 아시아 태평양(APAC) 지역

>[!NOTE]
>
>이후 수정된 문제로 인해 &quot;최적화된 A4T 지표 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target]3월 8일과 9일에 릴리스된 기능은 일시적으로 제거되었습니다. 추가 내부 테스트 후 이 기능은 몇 주 후에 다시 릴리스될 예정입니다.

이번 릴리스에는 다음과 같은 수정 사항이 포함됩니다.

* 를 사용하여 사용자 지정 웹 구성 요소를 작성하는 업데이트 [!UICONTROL 시각적 경험 작성기] (VEC):

   * 에 대한 종속성이 없도록 작성 프로세스를 개선하여 VEC에서 섀도 DOM 요소 선택을 수정했습니다. [!DNL Target] 그림자 루트를 작성할 때의 구현 유형입니다. 이제 VEC에서 그림자 DOM 요소를 선택하면 모든 웹 사이트에 대해 작동합니다.
   * VEC에서 #Shadow DOM을 사용하여 HTML 요소를 로드할 수 없는 문제가 해결되었습니다. (TGT-35801)
   * ShadowDOM을 사용하는 SPA 웹 사이트와 관련된 VEC 문제가 해결되었습니다. (TGT-43169)
   * ShadowDOM에서 CSS 선택기를 제대로 식별하지 않은 최적화 목표: &quot;요소를 클릭함&quot; 문제를 해결했습니다.

>[!NOTE]
>
>VEC에서 작성된 변경 사항을 전달하려면 다음을 사용하는지 확인합니다. [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js) 버전 2.8보다 큼.

**알려진 문제**: 를 사용할 때 그림자 루트 요소에 대한 클릭 추적 [!DNL Adobe Experience Platform Web SDK] 이(가) 제대로 작동하지 않습니다. (TNT-47012)

## at.js 버전 2.10.2 (2023년 3월 7일)

* `trackEvent` 함수가 항상 오류를 반환하는 문제가 해결되었습니다.

모든 at.js 릴리스에 대한 정보는 [at.js 버전 세부 정보](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}를 참조하십시오.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |


## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
