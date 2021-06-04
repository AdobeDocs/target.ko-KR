---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 최신 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 현재 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: 릴리스 정보
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: c0c38ef739de71df314a1bdeae17c521280fb910
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 86%

---

# Target 릴리스 정보 (현재)

이러한 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 정보도 포함됩니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js로부터의 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 미칩니다.
>
>사이트에서 발생할 수 있는 문제를 방지하기 위해 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하십시오. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.)

## ![Adobe Experience Platform 웹 SDK ](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] 버전 2.6.0(2021년 6월 1일)

이 [!DNL Platform Web SDK] 릴리스에는 다음에 대한 지원이 포함되어 있습니다.

| 기능 | 세부 사항 |
| --- | --- |
| [!UICONTROL Analytics for Target](A4T)로 리디렉션 지원 | 이제 Platform Web SDK는 [A4T](/help/c-integrating-target-with-mac/a4t/a4t.md)를 사용할 때 [!DNL Target] 리디렉션을 지원합니다.<br>자세한 내용은  [Analytics 구현  [!DNL Target] 을 참조하십시오](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |

## at.js 버전 2.5.0(2021년 5월 13일)

이 at.js의 릴리스에는 다음과 같은 개선 사항 및 변경 사항이 포함되어 있습니다.

* at.js에 대한 [온디바이스 의사 결정](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) 지원
* 자동화된 개인화 활동에 대한 [링크 미리보기](/help/c-activities/c-activity-qa/activity-qa.md) 지원

또한 Microsoft Internet Explorer 10, Internet Explorer 11 및 모든 이전 버전에 대한 지원도 제거됩니다. Microsoft Edge는 at.js 2.5.0 이상에서 계속 지원됩니다.

## Target Standard/Premium 21.4.1(2021년 4월 19일)

이 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

| 기능 | 세부 사항 |
| --- | --- |
| at.js<br>(발표될 날짜)에 대한 온디바이스 의사 결정 | 마케터와 개발자는 온디바이스 의사 결정을 통해 거의 0에 가까운 지연 시간에 사용자 브라우저에 대한 실험 및 개인화를 제공할 수 있습니다.<br>자세한 내용은 [at.js에 대한 온디바이스 의사 결정](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md)을 참조하십시오. |
| ![Premium](/help/assets/premium.png) 법인 필터링 규칙에 대한 목록 기반 연산자 | [!DNL Target Recommendations]는 법인 필터링 규칙에 대한 새로운 목록 기반 연산자. (TGT-39234)<br>새로 추가된 연산자는 다음과 같습니다.<br><ul><li>Is Contained In List</li><li>Is Not Contained In List</li><li>List Contains An Item In</li><li>List Does Not Contain An Item In</li><li>List Contains All Items In</li><li>List Does Not Contain All Items In</li></ul>자세한 내용은 [동적 및 정적 포함 규칙 사용](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators)의 &quot;사용 가능한 연산자&quot;를 참조하십시오. |

이 릴리스에는 다음과 같은 수정 사항이 포함됩니다.

* 고객을 [!UICONTROL 모든 방문자] 로 변경한 후에 활동을 동기화할 수 없는 문제를 해결했습니다. (TGT-40259)
* [!UICONTROL 복제 허용] 활동이 활성화되기는 했지만, [!UICONTROL 자동화된 개인화] 활동의 여러 위치에서 사용하는 경우에 제안을 복제할 수 없는 문제를 해결했습니다. (TGT-39567)
* [!UICONTROL 관리] > [!UICONTROL Scene7 구성] 페이지를 제대로 업로드할 수 없는 문제를 해결했습니다. (TGT-39918)
* 속성을 잘못된 작업 영역으로 매핑하는 문제를 해결했습니다. (TGT-39869)
* 권장 사항 제외를 생성하는 동안 환경을 변경한 후에 요청이 실패하는 경우, 무한 로딩을 유발하는 문제를 해결했습니다. (TGT-39948)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 노트 이외에 다음 리소스에서 추가 정보를 제공합니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 정보 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 정보](/help/r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 정보 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다.<br>자세한 내용은 [Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR)을 참조하십시오. |

## 사전 릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html))에 등록하십시오. |
| 향후 릴리스 정보 | 사전 릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 정보 - 사전 릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
