---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: 릴리스 정보
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b897829595ef1cdda28a995481fa1d2d5d1616f4
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 79%

---

# Target 릴리스 정보(프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2021년 6월 24일**

현재 릴리스에 대한 정보를 보려면, [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js에서 발송된 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 줍니다.
>
>사이트에 문제가 발생하지 않도록 하려면, 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

## [!DNL Target Standard/Premium] 21.6.1(2021년 6월 30일)

이 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

| 기능 | 세부 사항 |
| --- | --- |
| Analytics for Target (A4T) | 이제 [!DNL Analytics]를 보고 소스(A4T)로 사용하는 활동의 [!UICONTROL Reports] 페이지에서 &quot;[!UICONTROL View in Analytics]&quot; 링크를 클릭하면 [!DNL Analysis Workspace]가 열립니다. 이전에는 링크가 [!DNL Analytics] 보고를 열었습니다. (TGT-36959) |
| ![프리미엄](/help/assets/premium.png) [!DNL Recommendations] | [!DNL Recommendations] 인기 알고리즘에 적용되는 개선 사항:<ul><li>[!DNL Target]이 동작 데이터 소스일 때 모든 인기도(가장 많이 본/최상위 판매자) 알고리즘에 6시간 &quot;전환 확인 기간&quot;(데이터 범위) 옵션을 사용할 수 있습니다. (이 룩백 창은 [!DNL Adobe Analytics]가 행동적 데이터 소스일 때 *못* 사용합니다.)</li><li>선택한 경우, 다음 알고리즘은 약 3시간마다 실행되며(12시간이 아닌),<ul><li>가장 많이 본 항목</li><li>최다 구매</li><li>범주별 최고 조회수</li><li>범주별 최다 구매</li><li>알고리즘 특성별 최고 조회수(groupBy 기능 사용)</li><li>알고리즘 특성별 최다 판매(groupBy 기능 사용)</li></ul></ul>릴리스 날짜가 표시됩니다. (TOP-1086) |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
