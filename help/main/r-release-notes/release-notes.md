---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 8cdf362d9e45153b26bca5a45ed59ef557adc016
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 80%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target] Standard/Premium 22.15.1 (2023년 3월 8일, 9일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공될 예정입니다.

* **3월 8일**: 아메리카 지역
* **3월 9일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **3월 9일**: 아시아 태평양(APAC) 지역

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 기능 | 세부 사항 |
| --- | --- |
| 최적화된 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟팅]에 대한 A4T 지표 | [!DNL Target]을 사용하면 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟팅] 활동에 대한 [!UICONTROL A4T]를 사용할 때 이항 이벤트 또는 연속 이벤트를 기반으로 지표를 선택할 수 있습니다.<P>다음은 유의해야 할 지원되는 지표에서의 긴급 변경 내용입니다.<ul><li>[!DNL Target]은 2023년 9월 9일까지의 기존 활동에 대한 이전 동작을 유지했습니다. 이 날짜 이후에는 기존 활동을 새 동작으로 강제 마이그레이션하기 위해 지원되지 않는 지표를 사용하는 활동이 중단됩니다.</li></ul>자세한 내용은 *자동 할당 및 자동 타겟팅 활동에 대한 A4T 지원*&#x200B;의 [지원되는 목표 지표](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported)를 참조하십시오. |
| [!UICONTROL Analytics for Target](A4T)을 사용하는 [!UICONTROL 자동 할당] | 새 튜토리얼:<ul><li>[[!UICONTROL 자동 할당] 활동을 위해 [!DNL Analysis Workspace] 의 A4T 보고서 설정](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li></ul> |
| [!UICONTROL Analytics for Target](A4T)을 사용하는 [!UICONTROL 자동 타겟팅] | 새 튜토리얼:<ul><li>[[!UICONTROL 자동 타겟팅] 활동을 위해 [!DNL Analysis Workspace] 의 A4T 보고서 설정](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul> |

이번 릴리스에는 다음과 같은 수정 사항이 포함됩니다.

* 를 사용하여 사용자 지정 웹 구성 요소를 작성하는 업데이트 [!UICONTROL 시각적 경험 작성기] (VEC):

   * 에 대한 종속성이 없도록 작성 프로세스를 개선하여 VEC에서 섀도 DOM 요소 선택을 수정했습니다. [!DNL Target] 그림자 루트를 작성할 때의 구현 유형입니다. 이제 VEC에서 그림자 DOM 요소를 선택하면 모든 웹 사이트에 대해 작동합니다.
   * VEC에서 #Shadow DOM을 사용하여 HTML 요소를 로드할 수 없는 문제가 해결되었습니다. (TGT-35801)
   * ShadowDOM을 사용하는 SPA 웹 사이트와 관련된 VEC 문제가 해결되었습니다. (TGT-43169)
   * ShadowDOM에서 CSS 선택기를 제대로 식별하지 않은 최적화 목표: &quot;요소를 클릭함&quot; 문제를 해결했습니다.

>[!NOTE]
>
>VEC에서 작성된 변경 사항을 전달하려면 다음을 사용하는지 확인합니다. [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js) 버전 2.8보다 큼.

**알려진 문제**: 를 사용할 때 그림자 루트 요소에 대한 클릭 추적 [!DNL Adobe Experience Platform Web SDK] 이(가) 제대로 작동하지 않습니다. (TNT-47012)

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
