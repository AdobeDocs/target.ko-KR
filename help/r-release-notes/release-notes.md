---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5a5b39db9b9b4ffd95573d643dcff52fe562c0c2
workflow-type: ht
source-wordcount: '727'
ht-degree: 100%

---

# Target 릴리스 정보 (현재)

이러한 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 Target API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 사항에 대한 릴리스 정보도 포함됩니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js로부터의 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 미칩니다.
>
>새로운 [!DNL Adobe Experience Platform Web SDK] 의 가장 최근 또는 사이트에 문제가 발생할 가능성을 피하기 위해 at.js JavaScript 라이브러리로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.)

## [!DNL Target Standard/Premium] 21.9.1(2021년 9월 14일)

이 유지 보수 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함되어 있습니다.

* 일부 웹 브라우저의 서드파티 쿠키에 대한 새 보안 정책으로 인해 고객이 [!UICONTROL 시각적 경험 작성기] (VEC)에 로그인할 수 없는 문제가 해결되었습니다. [시각적 경험 작성기 및 고급 경험 작성기 관련 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)의 “Google Chrome 버전 80 이상을 사용할 때 시각적 경험 작성기(VEC) 또는 향상된 경험 작성기(EEC) 페이지가 로드되지 않음”에서 이 문제를 논의합니다.
* VEC의 오퍼 이름에 오퍼의 친숙한 이름 대신 오퍼의 패스가 표시되는 문제가 해결되었습니다. (TGT-41300)
* 경험 이름이 A4T 활동(TGT-38674)에 대한 [!DNL Analysis Workspace] 에 반영됩니다.
* 복제된 활동의 프로모션 엔티티 ID 변경 내용이 원래 활동에 잘못 적용되는 [!DNL Recommendations] 의 문제가 해결되었습니다. (TGT-41482)
* VEC의 [!DNL Recommendations] 활동에 대한 [!UICONTROL 경험] 페이지에서 “기준 편집” 버튼을 제대로 표시할 수 없는 문제가 해결되었습니다. (TGT-39512)
* 테스트 작업 영역에 복제 및 복사하는 경우 활동을 동기화할 수 없는 문제가 해결되었습니다. (TGT-40686)
* VEC에서 “[!UICONTROL 다음 항목 뒤에 삽입]”을 사용하는 경우 [경험 조각](/help/c-experiences/c-manage-content/aem-experience-fragments.md) 으로 선택기를 수정할 수 없는 문제가 해결되었습니다. (TGT-41802)
* 오퍼의 빈 JSON 콘텐츠를 백엔드로 전송할 수 없는 문제가 해결되었습니다. 비어있더라도 [!DNL Target] 에서 JSON 오브젝트를 보냅니다. (TGT-41555)
* 보고서를 보면서 고객이 “[!UICONTROL 분석에서 보기]”를 클릭한 경우 [!DNL Analysis Workspace] 대신 레거시 [!DNL Analytics] 보고서가 열리는 문제가 해결되었습니다. (TGT-41867)
* 고객이 [!UICONTROL Automated Personalization] 활동에 대한 보고 소스 (A4T)로 [!DNL Analytics] 선택을 시도하는 경우 표시된 UI 메시지에 추가 설명이 추가되었습니다. 메시지를 살펴보면 “[!DNL Target] 은 [!UICONTROL Automated Personalization] 활동”을 지원하는 유일한 소스입니다. (TGT-41954)
* 고객이 쉼표 대신 “새 줄”로 호스트 구분을 시도하는 경우 오류 메시지에 추가 설명이 추가되었습니다. (TGT-40671)
* 일부 활동의 “[!UICONTROL 마지막 데이트 날짜]”가 스페인어 및 일본어 고객용 영어 UI와 다를 경우 발생하는 문제가 해결되었습니다(스페인어 및 일본어로 UI를 조회하는 경우). (TGT-38980)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko_KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
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
| Adobe 우선순위 제품 업데이트 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html))에 등록하십시오. |
| 향후 릴리스 정보 | 프리릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 정보 - 프리릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
