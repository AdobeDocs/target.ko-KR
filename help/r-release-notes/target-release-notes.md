---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;사전 릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: 릴리스 정보
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 7bb1f896dd92b41d04eb0dfd39116ff1c132fe50
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 54%

---

# Target 릴리스 정보(사전 릴리스)

이 문서에는 사전 릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2021년 6월 1일**

현재 릴리스에 대한 정보를 보려면, [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js에서 발송된 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 줍니다.
>
>사이트에 문제가 발생하지 않도록 하려면, 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

## [!DNL Target Standard/Premium] 21.5.1(2021년 6월 8일)

| 기능 | 세부 사항 |
| --- | --- |
| ![Premium ](/help/assets/premium.png) [!DNL Recommendations] [!UICONTROL 배지 카탈로그 ] SearchAPI | API를 통해 프로그래밍 방식으로 [!DNL Recommendations] 제품 및 컨텐츠 카탈로그를 검색하여 검색 기준과 일치하는 항목을 식별하고 카탈로그 관리를 간소화합니다.<br>**제한 사항 및 참고**:<ul><li>API를 통한 카탈로그 검색은 2,000,000개 이상의 항목이 있는 환경에서는 지원되지 않습니다.</li><li>API를 통한 카탈로그 검색 결과는 [!DNL Target] UI를 통해 카탈로그 검색 결과보다 더 빠르게 업데이트됩니다. [!DNL Target] UI의 카탈로그 검색은 최신 결과를 반영하는 데 시간이 더 걸릴 수 있습니다.</li></ul>자세한 내용은 *[!DNL Adobe Target][!DNL Recommendations] API* 안내서에서 [엔티티 검색](http://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities)을 참조하십시오. |

## [!DNL Target Standard/Premium] 21.5.2(확정일)

이 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

| 기능 | 세부 사항 |
| --- | --- |
| ![Premium](/help/assets/premium.png) [!DNL Recommendations] | 다음 개선 사항은 [!DNL Recommendations] 인기도 알고리즘에 적용됩니다.<ul><li>[!DNL Target]이 동작 데이터 소스일 때 모든 인기도(가장 많이 본/최상위 판매자) 알고리즘에 6시간 &quot;전환 확인 기간&quot;(데이터 범위) 옵션을 사용할 수 있습니다. (이 전환 확인 기간은 *동작 데이터 소스인 경우*&#x200B;을 사용할 수 없습니다.)[!DNL Adobe Analytics]</li><li>이 옵션을 선택하면 약 3시간마다 다음 알고리즘이 실행됩니다(12시간이 아니라).<ul><li>가장 많이 본 항목</li><li>가장 많이 구입한 항목</li><li>카테고리별로 가장 많이 본 항목</li><li>가장 많이 구매된 카테고리</li><li>사용자 지정 속성으로 가장 많이 본 항목(groupBy 기능 사용)</li><li>사용자 지정 속성(groupBy 기능 사용)으로 가장 많이 구매됨</li></ul></ul>(TOP-1086) |

이 릴리스에는 다음과 같은 수정 사항이 포함됩니다.

* 릴리스 날짜가 가까워지면 콘텐츠가 추가됩니다.

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
