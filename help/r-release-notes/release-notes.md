---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여  [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아보십시오 [!DNL Adobe Target].
title: 현재 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: 릴리스 정보
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 0f0dd343a39b9a57e80593c5f554e1ba576a37f9
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 62%

---

# Target 릴리스 정보 (현재)

이러한 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 사항에 대한 릴리스 노트가 해당하는 경우 포함됩니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js로부터의 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 미칩니다.
>
>새로운 [!DNL Adobe Experience Platform Web SDK]의 가장 최근 또는 사이트에 문제가 발생할 가능성을 피하기 위해 at.js JavaScript 라이브러리로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.)

## [!DNL Target] node.js SDK 2.2.0(2021년 8월 11일)

* SDK 원격 분석 데이터 수집을 추가했습니다
* 자동화된 배달 API 클라이언트 openapi 코드 겐

이 릴리스 및 이전 릴리스에 대한 자세한 내용은 Github의 [Target node.js SDK 설명서](https://github.com/adobe/target-nodejs-sdk)에서 [변경 로그](https://github.com/adobe/target-nodejs-sdk/blob/main/CHANGELOG.md)을 참조하십시오.

## [!DNL Target Standard/Premium] 21.8.1 (날짜 미정)

>[!NOTE]
>
>[!DNL Target Standard/Premium] 21.8.1 릴리스가 지연되었습니다. 2021년 8월 4일에 릴리스되지 않고 버전 21.8.1이 며칠 후에 릴리스됩니다. 사용 가능한 경우 자세한 내용을 확인하십시오.

이 유지 관리 릴리스에는 다음과 같은 고객을 위한 변경 사항을 포함하여 많은 백엔드 개선 사항이 포함되어 있습니다.

* [!UICONTROL 양식 기반 경험 작성기]에서 만들어진 [!UICONTROL 자동 개인화] 활동에 대한 보고서가 보고서에서 삭제된 오퍼를 참조하도록 하는 문제를 해결했습니다. 이 문제로 인해 &quot;이 보고서에 대한 데이터를 검색하는 데 문제가 있습니다. 문제가 계속되면 Adobe Client Care에 문의하십시오.&quot; (TGT-41028)

## [!DNL Target Delivery API] (2021년 8월 3일)

이 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

* mbox 매개 변수에 대한 제한이 100개의 매개 변수로 늘어났습니다. 이전 제한은 50개의 매개 변수입니다. (TNT-41717)
* `categoryId`에 대한 제한이 256자로 늘어났습니다. 이전 제한은 128자입니다.
* 다음 [!DNL Adobe Audience Manager](AAM) 세부 정보가 배달 API에 추가되었습니다.

   * AAM UUID: 사용자를 고유하게 식별하는 데 사용되는 내부 AAM ID입니다.
   * dataPartnerId: 데이터 파트너의 ID입니다.
   * dataPartnerUserId: 데이터 파트너가 제공한 사용자 ID입니다.

   이전에는 배달 API에 `dcsLocationHint` 및 `blob`만 포함되었습니다. (TNT-41644)

## at.js 2.6.0 (2021년 7월 27일)

* at.js settings `secureOnly`가 `true`로 설정될 때마다 쿠키에 보안 속성이 추가됩니다.
* 이제 `triggerView()`를 사용할 때 응답 토큰을 사용할 수 있습니다.
* `CONTENT_RENDERING_NO_OFFERS` 이벤트와 관련된 문제가 해결되었습니다. 이제 [!DNL Target]에서 반환되는 내용이 없을 때 이 이벤트가 정상적으로 트리거됩니다.
* `prefetch` 요청을 사용할 때 [!DNL Anlytics for Target](A4T) 클릭 메트릭 세부 사항이 정상적으로 반환됩니다.
* UUID 생성이 더 이상 `Math.random()`을 사용하지 않고 `window.crypto`를 사용합니다.
* 모든 네트워크 호출에서 `sessionId` 쿠키 만료가 정상적으로 연장됩니다.
* 이제 [!UICONTROL 단일 페이지 애플리케이션](SPA) 보기 캐시 초기화가 정상적으로 처리되며 `viewsEnable` 설정이 적용됩니다.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 노트: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Platform Web SDK의 각 버전 변경 사항에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 정보 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 정보](/help/r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 정보 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다.<br>자세한 내용은 [Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR)을 참조하십시오. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html))에 등록하십시오. |
| 향후 릴리스 정보 | 프리릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 정보 - 프리릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
