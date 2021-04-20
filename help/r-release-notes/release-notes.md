---
keywords: 릴리스 정보;새 기능;릴리스;업데이트;업데이트;릴리스;개선 사항;개선 사항;수정 사항;버그 수정;업데이트
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 최신 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 현재 릴리스에 포함된 새로운 기능은 무엇입니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
translation-type: tm+mt
source-git-commit: dba3044c94502ea9e25b21a3034dc581de10f431
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 35%

---

# Target 릴리스 노트(현재)

이 릴리스 노트에서는 각 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 노트도 포함되어 있습니다(해당되는 경우).

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리를 더 이상  [!DNL Adobe Target] 지원하지 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다.
>
>사이트에서 발생할 수 있는 문제를 방지하기 위해 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션합니다. 자세한 내용은 [개요:클라이언트측 웹](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)에 대한 Target을 구현합니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## Target Standard/Premium 21.4.1(2021년 4월 19일)

이 릴리스에는 다음과 같은 새로운 기능과 개선 사항이 포함됩니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

| 기능 | 세부 사항 |
| --- | --- |
| at.js<br>(발표할 날짜)에 대한 장치 내 의사 결정 지원 | 디바이스 내 의사 결정을 통해 마케터와 개발자는 0분 지연 시간에 사용자의 브라우저에서 실험과 개인화를 전달할 수 있습니다.<br>자세한 내용은 at.js [에 대한 장치 내 의사 결정을 참조하십시오.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) |
| ![엔티티 필터링 규칙에 대한 ](/help/assets/premium.png) PremiumList 기반 연산자 | [!DNL Target Recommendations] 엔티티 필터링 규칙에 대한 새 목록 기반 연산자를 지원합니다. (TGT-39234)<br>새로 추가된 연산자는 다음과 같습니다.<br><ul><li>목록에 포함</li><li>목록에 포함되지 않음</li><li>목록에</li><li>목록에</li><li>목록에</li><li>목록에</li></ul>자세한 내용은 [동적 및 정적 포함 규칙 사용](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators)의 &quot;사용 가능한 연산자&quot;를 참조하십시오. |

이 릴리스에는 다음 수정 사항이 포함되어 있습니다.

* 대상자를 [!UICONTROL 모든 방문자]로 변경한 후 활동이 동기화되지 않는 문제를 수정했습니다. (TGT-40259)
* [!UICONTROL 중복 허용 안 함] 옵션이 활성화되어 있음에도 불구하고 [!UICONTROL Automated Personalization] 활동의 다른 위치에 오퍼가 사용될 때 중복되지 않는 문제를 해결했습니다. (TGT-39567)
* [!UICONTROL 관리] > [!UICONTROL Scene7 구성] 페이지가 제대로 로드되지 않는 문제를 해결했습니다. (TGT-39918)
* 속성이 잘못된 작업 영역에 매핑되는 문제를 수정했습니다. (TGT-39869)
* 권장 사항 제외를 만드는 동안 환경을 변경한 후 요청이 실패하는 경우 로드가 제한적으로 로드되는 문제를 해결했습니다. (TGT-39948)

## at.js 버전 2.5.0(발표할 날짜)

at.js의 이번 릴리스에는 다음과 같은 개선 사항 및 변경 사항이 포함되어 있습니다.

* [at.js에 ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) 대한 장치 내 의사 결정 지원.
* [미리 ](/help/c-activities/c-activity-qa/activity-qa.md) 보기 링크Automated Personalization 활동에 대한 지원.

또한 이 릴리스에서는 Microsoft Internet Explorer 10 이상 버전에 대한 지원도 제거되었습니다.

## 추가 릴리스 노트 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 노트 및 Experience Cloud 릴리스 노트

각 릴리스에 대한 노트 이외에 다음 리소스에서 추가 정보를 제공합니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 노트에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 봅니다.<br>자세한 내용은 [설명서 변경 내용](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 노트 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하세요.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 노트](/help/r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 노트 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 노트를 표시합니다.<br>자세한 내용은  [Experience Cloud 릴리스 노트를 참조하십시오](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## 사전 릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선 순위 제품 업데이트 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html)에 등록하십시오. |
| 향후 릴리스 노트 | 사전 릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 노트 - 사전 릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
