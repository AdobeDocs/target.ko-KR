---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: dbf9a51044f317d02a705f2331d6dc58b6549606
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 93%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target] Standard/Premium 23.9.4 (2023년 10월 4~6일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공됩니다.

* **10월 4일**: 아시아 태평양(APAC) 지역
* **10월 5일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **10월 6일**: 아메리카 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

| 기능 | 세부 사항 |
| --- | --- |
| [!UICONTROL 활동] UI 새로 고침<P>및<P>[!UICONTROL 피드] UI 새로 고침 | [!DNL Target] 사용자용 사용자 경험을 개선하기 위한 [!DNL Adobe Target] 팀의 지속적인 노력의 일환으로 이번 릴리스에서는 [!DNL Target] UI의 [!UICONTROL 활동] 및 [!DNL Recommendations] [!UICONTROL 피드] 페이지가 새롭게 업데이트되었습니다. 이번 업데이트를 통해 새로운 개선 사항이 추가되었으며 이전에 일관되지 않았던 디자인 패턴이 통합되고 표준화되었습니다.<P>자세한 내용은 [활동](/help/main/c-activities/activities.md) 및 [피드](/help/main/c-recommendations/c-products/feeds.md). |
| [!DNL Recommendations] 구현 패턴 | 다음 *at.js를 사용한 Recommendations 구현 패턴* 문서는 을 이해하고 작성하는 데 도움이 됩니다. [!DNL Adobe Target Recommendations] at.js JavaScript 라이브러리를 사용할 때의 구현입니다.<P>자세한 내용은 [at.js 개요를 사용한 Recommendations 구현 패턴](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/recs-implementation-pattern-atjs.html){target=_blank} 다음에서 *Adobe Target 개발자 안내서*. |

* 동적 프레임워크용 [!UICONTROL 시각적 경험 작성기](VEC) 개선 사항이 추가되었습니다. (TGT-44064)
* `getViewInAnalyticsId` 요청에서 선택한 날짜가 제대로 업데이트되지 않는 문제가 수정되었습니다. 이 수정 사항은 날짜 범위 및 지표 보고서 설정이 변경되는 경우 보고 시 [!DNL Analytics] 링크를 다시 계산하는 데 도움이 됩니다. (TGT-46246)

## [!DNL Target] Standard/Premium 23.9.3(2023년 9월 18일)

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* [!UICONTROL 시각적 경험 작성기](VEC)가 Lightning 웹 구성 요소(Light DOM)을 지원하도록 개선되었습니다. (TGT-45422)
* VEC 액션이 잘못된 순서로 적용되는 문제를 수정했습니다. 일부의 경우 VEC가 일부 수정 사항을 비동기적으로 적용했으며 요소에 수정 사항을 추가로 적용하는 경우 [!UICONTROL 삽입] 작업 후 해당 요소가 표시되면 오류가 발생했습니다. 또한 앵커 링크를 클릭할 때 업데이트되는 VEC URL도 수정했습니다. (TGT-45983)
* VEC [!UICONTROL 오버레이] 기능 관련 문제를 해결하여 이제 Shadow DOM의 요소를 지원합니다. (TGT-45202 및 TGT-45262)
* VEC에서 단일 페이지 애플리케이션(SPA) 페이지를 연 다음 [!UICONTROL 검색] 모드로 전환하면 뒤로 및 앞으로 화살표가 올바르게 작동하지 않는 문제를 해결했습니다. (TGT-45956)
* 일부 웹 페이지가 VEC에서 로드되지 않는 문제를 수정했습니다. (TGT-45983)

## [!DNL Target] Standard/Premium 23.9.2 (2023년 9월 12~14일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공됩니다.

* **9월 12일**: 아메리카 지역
* **9월 13일**: 아시아 태평양(APAC) 지역
* **9월 14일**: 유럽, 중동 및 아프리카(EMEA) 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* [!DNL Analytics] API가 새로운 [!DNL Analytics] API 버전 2.0으로 변경되었습니다. (TGT-45345)
* [!DNL Target] 백엔드에서 활동을 적시에 동기화하고 미리보기 링크에서 예상되는 경험을 제공하는 것을 포함하여 일부 고객의 [!UICONTROL Automated Personalization] (AP) 활동에 영향을 미치는 문제가 수정되었습니다. (TGT-46202)

## [!DNL Target] Standard/Premium 23.9.1 (2023년 9월 6~11일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공됩니다.

* **9월 6일**: 아메리카 지역
* **9월 7일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **9월 11일**: 아시아 태평양(APAC) 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* A4T( [!UICONTROL  Analytics for Target ] )를 보고 소스로 사용하는 [!UICONTROL 자동 할당]작업을 위한 [!DNL Target] UI 및 [!DNL Adobe Analytics] UI에서 보고 데이터가 일관되지 않게 되는 문제를 해결했습니다. (TGT-46112)
* 시간 초과 오류를 방지하기 위해 Target Delivery API에 대한 PUT 호출 시간 초과를 15초로 늘렸습니다. (TGT-46091)
* 단일 페이지 애플리케이션(SPA) 웹 사이트를 탐색할 때 URL이 지속적으로 업데이트되지 않는 문제를 수정했습니다. (TGT-45417)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

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
