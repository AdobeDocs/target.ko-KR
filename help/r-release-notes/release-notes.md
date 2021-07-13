---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여  [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 현재 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: 릴리스 정보
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: bdf8fdc0c7d92cb59270518861693ec22eb596f2
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 100%

---

# Target 릴리스 정보 (현재)

이러한 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 정보도 포함됩니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js로부터의 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 미칩니다.
>
>새로운 [!DNL Adobe Experience Platform Web SDK]의 가장 최근 , 또는 사이트에 문제가 발생할 가능성을 피하기 위해 at.js JavaScript 라이브러리로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.)

## Python SDK 1.0.0(2021년 6월 16일)

온 디바이스 결정 기능을 탑재한 새 [!DNL Adobe Target] Python SDK를 이제 이용할 수 있습니다. 이 최신 추가 기능은 서버측 SDK의 [!DNL Target] 제품군을 강화합니다. 이러한 SDK를 이용하면 [!DNL Target]과 통합할 수 있고 원하는 언어로 값까지 시간을 단축할 수 있습니다. 시장이 퍼스트파티 데이터가 귀중해지는 쿠키 없는 세상으로 전환하여 점점 더 많은 이들이 서버측 통합을 선택하고 있습니다. Target SDK는 시장에서 가장 인기 있는 프로그래밍 언어(Python, Java, JavaScript, C# / .Net)로 이용할 수 있습니다.

자세한 내용은 [Adobe Target SDKs 안내서](https://adobetarget-sdks.gitbook.io/docs/)의 [Python SDK 설명서](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/python-sdk)를 참조하십시오.

## Target Standard/Premium 21.5.1(2021년 6월 7일)

이 릴리스에는 다음 개선 사항이 포함됩니다.

| 기능 | 세부 사항 |
| --- | --- |
| ![Premium 배지](/help/assets/premium.png) [!DNL Recommendations] [!UICONTROL 카탈로그 검색] API | 검색 기준과 일치하는 항목을 식별하고 카탈로그의 관리를 단순화하려면 API를 통해 프로그래밍 방식으로 [!DNL Recommendations] 제품과 콘텐츠 카탈로그를 검색하십시오.<br>**제한과 참고 사항**:<ul><li>API를 통한 카탈로그 검색은 2,000,000개가 넘는 항목을 가진 환경에 대해서는 지원되지 않습니다.</li><li>API를 통한 카탈로그 검색 결과는 [!DNL Target] UI를 통한 카탈로그 검색 결과보다 더 빠르게 업데이트됩니다. [!DNL Target] UI의 카탈로그 검색은 최신 결과를 반영하는 데 시간이 더 걸릴 수 있습니다.</li></ul>자세한 내용은 *[!DNL Adobe Target][!DNL Recommendations] API* 안내서의 [엔티티 검색](http://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities)을 참조하십시오. |

이 릴리스 유지 보수 릴리스가 포함하는 수정 사항은 다음과 같습니다.

* [!UICONTROL Audiences] 페이지를 참조할 때 기본 작업 영역이 다른 작업 영역으로 변경되는 문제를 수정했습니다. (TGT-38871)
* 오류 메시지를 유발하는 [!UICONTROL 관리] > [!UICONTROL 구현]의 문제를 수정했습니다. 해당 오류 메시지 내용: &quot;전역 mbox가 동기화되지 않을 수 있습니다. 재저장을 해 보십시오.&quot;

## ![Adobe Experience Platform Web SDK 배지](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] 버전 2.5.0 (2021년 6월 1일)

[!DNL Platform Web SDK]의 이번 릴리스가 지원하는 것은 다음과 같습니다.

| 기능 | 세부 사항 |
| --- | --- |
| [!UICONTROL Analytics for Target] (A4T) 로 리디렉션 지원 | Platform Web SDK 가 이제 [A4T](/help/c-integrating-target-with-mac/a4t/a4t.md) 를 사용할 때 [!DNL Target] 리디렉션을 지원합니다.<br>자세한 내용은 [Analytics for [!DNL Target] 구현](/help/c-integrating-target-with-mac/a4t/a4timplementation.md)을 참조하십시오. |

## at.js 버전 2.5.0(2021년 5월 13일)

이 at.js의 릴리스에는 다음과 같은 개선 사항 및 변경 사항이 포함되어 있습니다.

* at.js에 대한 [온디바이스 의사 결정](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) 지원
* Automated Personalization 활동에 대한 [링크 미리보기](/help/c-activities/c-activity-qa/activity-qa.md) 지원

또한 이 릴리스에서는 Microsoft Internet Explorer 10, Internet Explorer 11, 그리고 그 이하 버전에 대한 지원이 제거되었습니다. Microsoft Edge는 at.js 2.5.0과 이후 버전에서 지속 지원됩니다.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
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
