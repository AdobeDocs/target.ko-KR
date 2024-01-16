---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된  [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 78bedce2134061edc48baf7023107e1dd48da2a1
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 46%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target]릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트 날짜: 2023년 1월 16일 화요일**

>[!NOTE]
>
>릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 일자에 따라 동일하거나 다를 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## 브라우저 대상 속성에서 iPad 및 iPhone 사용 중단(2024년 4월 30일)

| 사용 중단 | 세부 사항 |
|--- |--- |
| [!DNL iPad] 및 [!DNL iPhone] 에서 더 이상 사용되지 않음 [브라우저 속성](/help/main/c-target/c-audiences/c-target-rules/browser.md) 대상자를 만들 때 사용됩니다.<p>사용 중단 날짜:<P>2024년 4월 30일 수요일 | [!DNL Adobe Target] 다음 작업을 수행할 수 있습니다. [여러 범주 속성 중 하나를 타깃팅합니다.](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), 특정 [브라우저 또는 브라우저 옵션](/help/main/c-target/c-audiences/c-target-rules/browser.md) 방문자가 페이지를 방문할 때입니다.<P><B>2024년 4월 30일부터 iPad 및 iPhone이 사용 가능한 항목에서 제거됩니다 [!UICONTROL 브라우저] 대상의 범주를 만들 때 드롭다운 목록을 입력합니다.</b><P>다음을 사용하여 iPad 또는 iPhone을 대상으로 하는 대상이 있는 경우 [!UICONTROL 브라우저] attribute가 제대로 작동하려면 2024년 4월 30일 이전에 이러한 설정을 변경해야 합니다.<P>앞으로 다음 설정을 사용해야 합니다.<ul><li>[!UICONTROL 모바일] > [!UICONTROL 태블릿임]<P>![모바일은 태블릿입니다](/help/main/r-release-notes/assets/is-tablet.png)</li><li>[!UICONTROL 모바일] > [!UICONTROL 장치 마케팅 이름] [!UICONTROL 일치] [!DNL iPad]<P>![iPad](/help/main/r-release-notes/assets/ipad.png)</li><li>[!UICONTROL 모바일] > [!UICONTROL 장치 마케팅 이름] [!UICONTROL 일치] [!DNL iPhone]<p>![iPhone](/help/main/r-release-notes/assets/iphone.png)</li></ul> |

## [!DNL Target] Standard/Premium 24.1.1(2024년 1월 22일, 23일 및 25일)

이번 릴리스는 다음 날짜로 예정되어 있습니다.

* **1월 22일**: 유럽, 중동 및 아프리카(EMEA) 지역
* **1월 23일**: 아시아 태평양(APAC) 지역
* **1월 25일**: 아메리카 지역

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 보고 날짜 간격이 제대로 작동하지 않는 문제를 해결했습니다. (TGT-47396)
* 에 잘못된 상태가 표시되는 문제를 해결했습니다. [!UICONTROL 모든 활동] 고객이 을 사용하여 활동을 활성화하거나 비활성화한 후 페이지 [!UICONTROL 추가 작업] 아이콘. (TGT-47367)
* 의 원인이 되는 문제가 해결되었습니다. [!UICONTROL 중요 속성] 한 고객에 대해 표시되지 않는 보고서입니다. (TGT-47272)
* 한 고객이 &quot;인증 필요&quot;를 활성화하려고 할 때 &quot;잘못된 페이로드&quot; 메시지가 표시되는 문제를 해결했습니다. (TGT-47195)
* 에서 현지화된 문자열을 여러 개 업데이트했습니다. [!DNL Target] UI.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 정보](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
