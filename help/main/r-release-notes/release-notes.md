---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 71190b0f6c66d4c448121a330e7c07b6255ae8be
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 100%

---

# Target 릴리스 정보 (현재)

이러한 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target Standard/Premium] 22.5.1(순차적 공개, 2022년 5월 11~13일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **5월 11일**: 아시아 태평양(APAC) 지역
* **5월 12일**: 북미(NA) 지역
* **5월 13일**: 유럽, 중동 및 아프리카(EMEA) 지역

이번 릴리스에는 다음과 같은 개선 사항 및 수정 사항이 포함되어 있습니다.

* JavaScript 오류의 원인이며 일부 고객이 특정 [!UICONTROL Automated Personalization](AP) 활동에 대한 활동 세부 정보에 액세스하지 못하도록 하는 문제가 해결되었습니다. (TGT-43526)
* 일부 고객이 AP 활동에 특정 제안을 추가(또는 편집)하지 못하도록 하는 문제가 해결되었습니다. (TGT-43503)
* 다음 오류 메시지를 표시하는 [!DNL Target] UI 문제가 해결되었습니다. “전역 mbox가 동기화되지 않을 수 있습니다. 재저장을 해 보십시오.” 이 문제는 UI 문제였으며 고객의 구현에 영향을 미치지 않았습니다. (TGT-43475)
* 새 [!UICONTROL 대상] UI가 배포되기 전에 세분화 및 대상이 생성된 경우 한 고객이 해당 활동에 대한 경험 수준 세분화 및 대상을 편집하지 못하도록 하는 문제가 해결되었습니다. (TGT-43433)
* 고객이 활동에 대한 보고 대상을 편집하는 동안 중복 [!DNL Adobe Audience Manager](AAM) 대상을 선택할 수 있는 문제가 해결되었습니다. (TGT-43430)
* 고객이 다른 작업 영역에서 중복 대상을 만들 수 없는 문제를 수정했습니다. (TGT-43423)
* 고객이 [!UICONTROL 양식 기반 경험 작성기]에서 생성된 활동에서 애드혹 오퍼가 있는 위치를 삭제할 수 없는 문제를 수정했습니다. (TGT-43315)
* 고객이 이미지 오퍼를 클릭하고 UI를 새로 고친 후 코드 오퍼에 액세스하지 못하는 문제를 수정했습니다. (TGT-43566)
* 스크립트를 편집하고 활성화하고 비활성화한 후 프로필 스크립트를 편집하면 편집되지 않은 원래 스크립트로 되돌아가는 문제가 해결되었습니다. 프로필 스크립트는 이제 편집된 상태로 유지됩니다. (TGT-43249)
* 대상을 다른 작업 영역으로 이동하려고 할 때 다음 오류가 발생하는 문제가 수정되었습니다. “요청을 완료할 수 없습니다. 문제가 지속되면 Adobe 클라이언트 지원 센터에 문의하십시오.” (TGT-43212)
* SPA(단일 페이지 앱) 페이지에 대한 사용자 지정 코드 수정을 복제할 때 오류가 발생하는 문제가 해결되었습니다. (TGT-43137)
* 경험을 복제한 다음 프로모션을 편집하면 원본 프로모션이 영향을 받던 문제가 해결되었습니다. (TGT-41775)

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
