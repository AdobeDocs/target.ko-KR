---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 99152f66217f66174e8b6a5a7319f11b22c74b8e
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 96%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트: 2024년 1월 22일 화요일**

>[!NOTE]
>
>릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 일자에 따라 동일하거나 다를 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## 브라우저 대상자 속성에서 iPad 및 iPhone 사용 중단(2024년 4월 30일)

| 사용 중단 | 세부 사항 |
|--- |--- |
| 대상자를 만들 때 사용되는 [브라우저 속성](/help/main/c-target/c-audiences/c-target-rules/browser.md)에서 [!DNL iPad] 및 [!DNL iPhone]이 사용 중단됩니다.<p>사용 중단 일자:<P>2024년 4월 30일 | [!DNL Adobe Target]에서는 페이지를 방문할 때 특정 [브라우저 또는 브라우저 옵션](/help/main/c-target/c-audiences/c-target-rules/browser.md)을 사용하는 사용자 등 [여러 카테고리 속성을 타겟팅](/help/main/c-target/c-audiences/c-target-rules/target-rules.md)할 수 있습니다.<P><B>2024년 4월 30일부터 대상자 카테고리를 만들 때 사용 가능한 [!UICONTROL 브라우저] 유형 드롭다운 목록에서 iPad 및 iPhone이 제거됩니다.</b><P>[!UICONTROL 브라우저] 속성을 사용하여 iPad 또는 iPhone을 타겟팅하는 대상자가 있는 경우, 이러한 대상자가 예상대로 계속 작동하도록 하려면 2024년 4월 30일 이전에 이러한 설정을 변경해야 합니다.<p>대체 설정의 예는 를 참조하십시오. [브라우저 대상 속성에서 iPad 및 iPhone 사용 중단(2024년 4월 30일)](/help/main/c-target/c-audiences/c-target-rules/browser.md#deprecation). |

## [!DNL Target] Standard/Premium 24.1.1 (2024년 1월 22일, 23일 및 25일)

이번 릴리스는 다음 날짜로 예정되어 있습니다.

* **1월 22일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **1월 23일**: 아시아 태평양(APAC) 지역
* **1월 25일**: 아메리카 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 수익 목표 지표가 포함된 [!UICONTROL Analytics for Target] (A4T) 활동에 “매출”이 열 이름으로 표시되지 않았고 매출 지표가 보고에서 ($) 형식으로 표시되지 않았습니다. 이는 이미 해결된 표시용 문제였습니다. (TGT-46995)
* 보고 일자 간격이 올바르게 작동하지 않는 문제를 수정했습니다. (TGT-47396)
* 고객이 [!UICONTROL 추가 작업] 아이콘을 사용하여 활동을 활성화하거나 비활성화한 후 [!UICONTROL 모든 활동] 페이지에 잘못된 상태가 표시되는 문제를 수정했습니다. (TGT-47367)
* [!UICONTROL 중요 속성] 보고서가 단일 고객에 대해 표시되지 않는 문제를 수정했습니다. (TGT-47272)
* 단일 고객이 “인증 요구”를 활성화하려고 하면 “잘못된 페이로드” 메시지가 표시되는 문제를 수정했습니다. (TGT-47195)
* [!DNL Target] UI에서 여러 현지화된 문자열을 업데이트했습니다.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 정보](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=ko-KR){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
