---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된  [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 6fa553c7179cd2a6d500bdc53cc77dc01ee906e7
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 95%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target]릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트: 2023년 9월 18일**

>[!NOTE]
>
>릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 일자에 따라 동일하거나 다를 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## [!DNL Target] Standard/Premium 23.9.3(2023년 9월 18일)

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 이(가) 을(를) 개선했습니다. [!UICONTROL 시각적 경험 작성기] (VEC) - Lightning Web Components(Light DOM)를 지원합니다. (TGT-45422)
* VEC 액션이 잘못된 순서로 적용되는 문제를 수정했습니다. 일부의 경우 VEC가 일부 수정 사항을 비동기적으로 적용했으며 요소에 수정 사항을 추가로 적용하는 경우 [!UICONTROL 삽입] 작업 후 해당 요소가 표시되면 오류가 발생했습니다. 또한 앵커 링크를 클릭할 때 업데이트되는 VEC URL도 수정합니다. (TGT-45983)
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

* A4T([!UICONTROL Analytics for Target])를 보고 소스로 사용하는 [!UICONTROL 자동 할당] 작업을 위한 [!DNL Target] UI 및 [!DNL Adobe Analytics] UI에서 보고 데이터가 일관되지 않게 되는 문제를 해결했습니다. (TGT-46112)
* 시간 초과 오류를 방지하기 위해 Target Delivery API에 대한 PUT 호출 시간 초과를 15초로 늘렸습니다. (TGT-46091)
* 단일 페이지 애플리케이션(SPA) 웹 사이트를 탐색할 때 URL이 지속적으로 업데이트되지 않는 문제를 수정했습니다. (TGT-45417)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
