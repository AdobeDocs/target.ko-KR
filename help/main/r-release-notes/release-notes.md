---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 2c4f5666b65bfc36885aad3907639a309e8c69f2
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 69%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target] Standard/Premium 22.15.1 (2023년 3월 8일, 9일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **3월 8일**: 아메리카 지역
* **3월 9일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **3월 9일**: 아시아 태평양(APAC) 지역

>[!NOTE]
>
>이후에 해결된 문제로 인해 &quot;A4T에 최적화된 지표&quot;가 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target]3월 8~9일에 릴리스된 &quot;기능이 일시적으로 제거되었습니다. 추가적인 내부 테스트 후 몇 주 후에 기능이 다시 릴리스됩니다.

이번 릴리스에는 다음과 같은 수정 사항이 포함됩니다.

* 을 사용하여 작성한 사용자 지정 웹 구성 요소에 대한 업데이트 [!UICONTROL 시각적 경험 작성기] (VEC):

   * 에 대한 종속성이 없도록 작성 프로세스를 개선하여 VEC에서 그림자 DOM 요소 선택을 수정했습니다 [!DNL Target] 그림자 루트를 작성할 때의 구현 유형입니다. 이제 VEC에서 그림자 DOM 요소 선택이 모든 웹 사이트에 대해 작동해야 합니다.
   * VEC에서 #Shadow DOM을 사용하여 HTML 요소를 로드할 수 없는 문제를 수정했습니다. (TGT-35801)
   * ShadowDOM을 사용하는 SPA 웹 사이트의 VEC 문제가 수정되었습니다. (TGT-43169)
   * 최적화 목표 관련 문제를 수정했습니다. ShadowDOM에서 CSS 선택기를 제대로 식별하지 않는 &quot;요소를 클릭함&quot;입니다.

>[!NOTE]
>
>VEC에서 작성된 변경 사항을 전달하려면 다음을 사용 중인지 확인하십시오 [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js))를 사용할 수 없습니다.

**알려진 문제**: 사용 시 섀도 루트 요소에 대한 클릭 추적 [!DNL Adobe Experience Platform Web SDK] 가 제대로 작동하지 않습니다. (TNT-47012)

## at.js 버전 2.10.2 (2023년 3월 7일)

* `trackEvent` 함수가 항상 오류를 반환하는 문제가 해결되었습니다.

모든 at.js 릴리스에 대한 정보는 [at.js 버전 세부 정보](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}를 참조하십시오.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 정보 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 정보 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다.<br>자세한 내용은 [Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR)을 참조하십시오. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html))에 등록하십시오. |
| 향후 릴리스 정보 | 프리릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 정보 - 프리릴리스](/help/main/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
