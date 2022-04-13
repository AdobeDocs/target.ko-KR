---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: a03975f8f14db3cb8be0850130aab8d34c4c7fc0
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 47%

---

# Target 릴리스 정보 (현재)

이러한 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK]적용 가능한 경우 , at.js 및 기타 플랫폼 변경 사항도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## Target 플랫폼 릴리스(2022년 4월 13일)

이 릴리스에는 다음 업데이트가 포함됩니다.

* 프로필 스크립트를 사용하여 캡처할 때 IP 주소의 마지막 8진수가 제대로 난독화되도록 하는 문제가 수정되었습니다. (TNT-44076)

## [!DNL Target Standard/Premium] 22.3.1(시차 릴리스, 날짜 결정)

이 릴리스에는 다음과 같은 변경 사항 및 개선 사항이 포함되었습니다.

* 스크립트를 편집하고 활성화한 다음 비활성화한 후 프로필 스크립트 편집 내용이 편집되지 않은 원래 스크립트로 되돌리는 문제를 해결했습니다. 이제 프로필 스크립트가 편집된 상태로 유지됩니다. (TGT-43249)
* 에서 다음 오류 메시지가 표시되는 문제를 해결했습니다. [!DNL Target] 초안 상태인 활동에서 사용된 대상을 이동할 때 UI를 사용할 수 있습니다. &quot;요청을 완료할 수 없습니다. 문제가 계속되면 Adobe 고객 지원 센터에 문의하십시오.&quot; (TGT-43212)
* 이(가) [!UICONTROL 포함] 및 [!UICONTROL 제외] 활동을 편집할 때 결합된 대상에 대해 비활성화할 수 있는 옵션. (TGT-43422)
* 활동을 편집하는 동안 일부 고객이 사용 가능한 대상 목록을 볼 수 없는 문제를 해결했습니다. (TGT-43404)
* 일부 고객이 &quot;[!UICONTROL 제외할 IP [!DNL Target] 보고 데이터]&quot; 목록 [!UICONTROL 관리] > [!UICONTROL 보고]. (TGT-43384)
* 변수가 &quot;보다 큼&quot;, &quot;보다 크거나 같음&quot;, &quot;보다 작음&quot; 또는 &quot;보다 작음&quot; 또는 &quot;보다 작거나 같음&quot;인지 대상 기준에 음수가 사용되지 않는 문제를 해결했습니다. (TGT-43367)
* 고객이 를 볼 수 없는 문제를 해결했습니다 [!UICONTROL 대상 세부 사항] 결합된 대상을 만들 때 카드입니다. (TGT-43303)
* 이(가) [!DNL Target] UI 또는 신규 [!UICONTROL 대상] UI를 사용하여 일부 고객의 시간을 늦춥니다. (TGT-42590 및 TGT-43273)

## [!DNL Target] 플랫폼 릴리스(3월 30일)

이번 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

* 클릭 추적 지표에는 Analytics를 보고 소스(A4T)로 사용하고 클라이언트측에서 이벤트를 처리하는 활동에 대한 배달 API 요청에 Analytics 페이로드가 포함됩니다. (TNT-43073)

## [!DNL Target Standard] 대상 새로 고침(3월 28일)

이 릴리스에는 다음 업데이트가 포함됩니다.

* 새로운 [!UICONTROL 대상] 모든 사용자에 대해 UI가 활성화됨 [!DNL Target Standard] 고객.

## Target Standard/Premium 고객 엔지니어링 수정 사항(2022년 3월 22일)

이 유지 관리 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

* 반환할 기능이 추가되었습니다. [!DNL Analytics] 페이로드 데이터 `prefetch` 보기 및 `pageLoad` 사용할 때 지표 클릭 [!UICONTROL 배달 API] 사용 중인 활동과 [!UICONTROL 보고 소스로서의 Analytics] (A4T). (TNT-43198)
* 일본에서 일반적으로 사용되는 브라우저 유형을 허용하도록 보트 필터링 사용자 에이전트 목록을 업데이트했습니다. (TNT-43867)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko_KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

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
