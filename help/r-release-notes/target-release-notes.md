---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: 릴리스 정보
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 42d9d7ed422bd5334a7f5e6467b0257f7ff4ab50
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 59%

---

# Target 릴리스 정보(프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**최근 업데이트: 2021년 8월 3일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js에서 발송된 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 줍니다.
>
>사이트에 문제가 발생하지 않도록 하려면 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

## [!DNL Target Standard/Premium] 21.8.1 (날짜 미정)

이 유지 관리 릴리스에는 다음과 같은 고객을 위한 변경 사항을 포함하여 많은 백엔드 개선 사항이 포함되어 있습니다.

* [!UICONTROL 양식 기반 경험 작성기]에서 만들어진 [!UICONTROL 자동 개인화] 활동에 대한 보고서가 보고서에서 삭제된 오퍼를 참조하도록 하는 문제를 해결했습니다. 이 문제로 인해 &quot;이 보고서에 대한 데이터를 검색하는 데 문제가 있습니다. 문제가 계속되면 Adobe Client Care에 문의하십시오.&quot; (TGT-41028)

## Target 배달 API(2021년 8월 3일)

이 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

* mbox 매개 변수에 대한 제한이 100개의 매개 변수로 늘어났습니다. 이전 제한은 50개의 매개 변수입니다. (TNT-41717)
* `categoryId`에 대한 제한이 256자로 늘어났습니다. 이전 제한은 128자입니다.
* 다음 [!DNL Adobe Audience Manager](AAM) 세부 정보가 배달 API에 추가되었습니다.

   * AAM UUID: 사용자를 고유하게 식별하는 데 사용되는 내부 AAM ID입니다.
   * dataPartnerId: 데이터 파트너의 ID입니다.
   * dataPartnerUserId: 데이터 파트너가 제공한 사용자 ID입니다.

   이전에는 배달 API에 `dcsLocationHint` 및 `blob`만 포함되었습니다. (TNT-41644)

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
