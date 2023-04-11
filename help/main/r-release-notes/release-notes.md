---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: a791fbe805735b278f650ff1f087b85898a66a07
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 100%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target] Standard/Premium 23.3.1 (2023년 3월 28~30일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공됩니다.

* **3월 28일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **3월 29일**: 아시아 태평양(APAC) 지역
* **3월 30일**: 아메리카 지역

이번 릴리스에는 다음과 같은 새로운 기능, 개선 및 수정 사항이 포함되었습니다.

| 기능 | 세부 사항 |
|--- |--- |
| 최적화된 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟팅]에 대한 A4T 지표<p>(릴리스 일자: 2023년 3월 30일) | [!DNL Target]을 사용하면 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟팅] 활동에 대한 [!UICONTROL A4T]를 사용할 때 이항 이벤트 또는 연속 이벤트를 기반으로 지표를 선택할 수 있습니다.<P>다음은 유의해야 할 지원되는 지표에서의 변경 내용입니다.<ul><li>[!DNL Target]은 2023년 9월 9일까지의 기존 활동에 대한 이전 동작을 유지했습니다. 이 날짜 이후에는 기존 활동을 새 동작으로 강제 마이그레이션하기 위해 지원되지 않는 지표를 사용하는 활동이 중단됩니다.</li></ul>자세한 내용은 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟팅] 활동을 위한](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported) [A4T 지원에서 &quot;지원되는 목표 지표&quot;를 참조하십시오.<br>이 기능과 함께 다음 튜토리얼이 업데이트되었습니다.<ul><li>[[!UICONTROL 자동 할당] 활동을 위해 [!DNL Analysis Workspace] 의 A4T 보고서 설정](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li><li>[[!UICONTROL 자동 타겟팅] 활동을 위해 [!DNL Analysis Workspace] 의 A4T 보고서 설정](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul> |

* [!DNL Adobe Experience Platform] 및 [!DNL Adobe Audience Manager]에서 생성된 항목을 [!DNL Target] UI에서 더 빠르게 사용할 수 있도록 대상자 및 활동 동기화가 개선되었습니다. (TGT-44568)
* 사용자가 [!UICONTROL 관리] > [!UICONTROL 시각적 경험 작성기] > [!UICONTROL 기본 URL]에서 [!UICONTROL 기본 URL]을 제거할 수 있도록 개선되었습니다. 이 변경을 통해 고객은 기본 URL을 빈 문자열로 다시 변경할 수 있게 되었습니다(이전에는 초기 구성 이후 변경할 수 없었음). (TGT-44577)
* 고객이 기본 제공 대상자(예약된 이름이 있는 대상자)을 편집하거나 삭제할 수 없도록 하는 제한이 제거되었습니다. (TGT-44655)
* [결합된 대상자](/help/main/c-target/combining-multiple-audiences.md)을 만들 때 회전기가 [!DNL Target] UI에 표시되는 동안 “[!UICONTROL 완료]” 옵션이 비활성화되었습니다. (TGT-44079)
* [!UICONTROL 대상자] 페이지 하단의 [!UICONTROL 언어] 링크가 “[!UICONTROL 계정 통신 환경 설정]” 페이지로 올바르게 연결되도록 수정되었습니다. (TGT-43562)
* 때때로 고객이 [!UICONTROL 관리] > [!UICONTROL 보고] > [!UICONTROL Experience Cloud 솔루션 보고]에서 [!UICONTROL Adobe Analytics] 옵션을 선택한 후 [!UICONTROL A/B Test] 테스트를 만들 수 없는 문제가 해결되었습니다. (TGT-44844)
* 고객이 [!UICONTROL 시각적 경험 작성기]&#x200B(VEC) 내에서 많은 경험이 포함된 [!UICONTROL 다변량 테스트] 활동의 마지막 경험을 볼 수 없는 문제가 해결되었습니다. 때때로 VEC 하단의 [DOM 경로](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path)로 인해 고객이 마지막 경험을 보지 못하는 경우가 있었습니다. (TGT-44578)
* 페이지에 인증이 필요하거나 페이지에서 리디렉션을 호출하는 경우 VEC의 검색 URL이 일반 브라우저 세션에 표시되는 현재 페이지를 반영하지 않는 문제가 해결되었습니다. (TGT-44350)
* 고객이 [!UICONTROL 추천] > [!UICONTROL 설정]에서 [!UICONTROL 호환되지 않는 기준 필터링] 설정을 변경하지 못하는 문제가 해결되었습니다. (TGT-44398)
* 이름에 점으로 표시된 보고서 세트와 함께 [!UICONTROL Analytics 분류]를 사용할 때 [!DNL Recommendations] 피드를 만드는 POST 요청이 실패하는 문제가 해결되었습니다. (TGT-44598)
* 새로운 [Visual Editing Helper 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)을 가리키도록 [!DNL Target] UI의 링크가 업데이트되었습니다. (TGT-44459)
* [!DNL Recommendations] 피드에서 SSRF(Server-Side Request Forgery) 시도를 방지하도록 보안이 강화되었습니다. (TGT-43769)
* [!DNL Target] UI 전반에 걸쳐 다양한 현지화 수정을 수행했습니다.

## at.js 버전 2.10.2 (2023년 3월 7일)

* `trackEvent` 함수가 항상 오류를 반환하는 문제가 해결되었습니다.

모든 at.js 릴리스에 대한 정보는 [at.js 버전 세부 정보](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}를 참조하십시오.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [설명서 변경 내용](/help/main/r-release-notes/doc-change.md) | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다. |
| [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md). | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오. |
| [Adobe Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR){target=_blank} | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [Adobe 우선순위 제품 업데이트](https://www.adobe.com/kr/subscription/priority-product-update.html){target=_blank} | [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으십시오. |
| [Target 릴리스 정보 (프리릴리스)](/help/main/r-release-notes/target-release-notes.md){target=_blank} | 프리릴리스 정보를 포함하여 현재 달의 Target 릴리스에 대한 정보입니다. |
