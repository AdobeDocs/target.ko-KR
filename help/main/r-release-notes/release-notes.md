---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 8da8daf7da0cfe3e4936cb48b4c594c464708775
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 66%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target] Standard/Premium 23.9.1(2023년 9월 6~11일)

이번 릴리스는 다음과 같은 순차적 일정에 따라 제공됩니다.

* **9월 6일**: 아메리카 지역
* **9월 7일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **9월 11일**: 아시아 태평양(APAC) 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 에서 일관되지 않은 보고 데이터를 발생시킨 문제를 수정했습니다. [!DNL Target] UI 및 [!DNL Adobe Analytics] 에 대한 UI [!UICONTROL 자동 할당] 를 사용하는 활동 [!UICONTROL Analytics for Target] (A4T) 를 보고 소스로 사용할 때에는 적용되지 않습니다. (TGT-46112)
* 시간 초과 오류를 방지하기 위해 Target 배달 API에 대한 PUT 호출의 시간 초과를 15초로 늘렸습니다. (TGT-46091)
* 간에 전환할 때 잘못된 보고서 이름이 표시되는 문제를 해결했습니다. [!UICONTROL 표 보기] 및 [!UICONTROL 자동화된 세그먼트] 및 [!UICONTROL 중요 속성] 보고서. (TGT-46040)
* 이(가) 을(를) 개선했습니다. [!UICONTROL 시각적 경험 작성기] (VEC) - Lightning DOM(웹 구성 요소)을 지원합니다. (TGT-45422)
* VEC 작업이 잘못된 순서로 적용되는 문제를 해결했습니다. 경우에 따라 VEC가 일부 수정 사항을 비동기적으로 적용했으며 요소에 추가 수정 사항을 추가하면 해당 요소가 다음에 표시되는 경우에 오류가 발생합니다. [!UICONTROL 삽입] 작업. (TGT-45983)
* VEC에서 SPA(단일 페이지 애플리케이션) 페이지를 연 다음 찾아보기 모드로 이동하면 뒤로 및 앞으로 화살표가 제대로 작동하지 않는 문제를 해결했습니다. (TGT-45956)
* SPA(단일 페이지 애플리케이션) 웹 사이트를 검색할 때 URL이 지속적으로 업데이트되지 않는 문제를 해결했습니다. (TGT-45417)

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
