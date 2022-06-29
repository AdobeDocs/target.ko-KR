---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 49517f858b39a70df7643125e703f31bf45b7336
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 100%

---

# Target 릴리스 정보 (현재)

이러한 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target Standard/Premium] 22.6.2 (2022년 6월 24일)

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* [!UICONTROL 편집자] 역할이 있는 사용자는 더 이상 라이브 활동에서 대상을 편집할 수 없습니다. (TGT-43582)
* 고객이 대상자 이름의 첫 문자로 느낌표( ! )를 사용하여 대상자를 저장하려고 하면 경고 메시지가 표시됩니다(예: !London). (TGT-43643)
* 일부 고객의 대상 정의 세부 정보 카드에 종료된 활동이 아직 활성 상태로 나타나는 문제를 해결했습니다. (TGT-43527)

## [!DNL Target Standard/Premium] 22.6.1 (순차적 공개: 2022년 6월 7~9일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **6월 7일**: 아시아 태평양(APAC) 지역
* **6월 8일**: 아메리카 지역
* **6월 9일**: 유럽, 중동 및 아프리카(EMEA) 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 대상이 과거에 저장된 이전 데이터베이스와 백엔드에서 직접 정보를 검색하는 새 아키텍처 사이의 불일치 상태를 방지하기 위해 새 [!UICONTROL 대상] 페이지에 대한 개선 사항이 제공되었습니다. (TGT-43552)
* 대상 UI가 “빈” 컨테이너를 생성하여 일부 고객이 통합 대상을 저장하지 못하는 문제가 해결되었습니다. (TGT-43588)

## Target 플랫폼 릴리스 (2022년 5월 25일)

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* [사용자 에이전트 클라이언트 힌트](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/){target=_blank} 지원이 추가되었습니다.
* [!UICONTROL Experience Targeting] (XT) 활동에서 [!UICONTROL 오퍼 의사 결정]을 렌더링할 때 간헐적으로 시간 초과가 발생하는 문제가 해결되었습니다. (TNT-44611)

## at.js 버전 2.9.0(2022년 5월 27일)

* [사용자 에이전트 클라이언트 힌트](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/){target=_blank} 지원이 추가되었습니다.
* 동일한 페이지의 여러 mbox 요청에 서로 다른 노출 ID가 있는 버그가 수정되었습니다.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
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
