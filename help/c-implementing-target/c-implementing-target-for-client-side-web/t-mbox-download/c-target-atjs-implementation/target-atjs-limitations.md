---
keywords: 시각적 경험 작성기 제한 사항;브라우저 지원;통합;플러그인;비동기 고려 사항
description: Adobe Target의 기존 mbox.js 구현에 대해 알아봅니다. Adobe Experience Platform 웹 SDK(AEP 웹 SDK) 또는 최신 버전의 at.js로 마이그레이션합니다.
title: at.js와 mbox.js의 차이점은 무엇입니까?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 92%

---


# at.js 제한 사항

at.js와 mbox.js 간에 약간의 차이가 있습니다. 이 섹션에는 at.js 사용 시 성공하는 데 도움이 되도록 몇 가지 차이점과 제한 사항이 나와 있습니다.

## 알려진 시각적 경험 작성기 제한 사항 {#section_4B63C97169DE4C93B22944E880FD3DF1}

* 시각적 경험 작성기의 요소 삽입 및 다시 정렬 선택 사항은 단일 페이지 앱에서 피해야 합니다.

   DOM은 기존 웹 사이트에서 지워지듯이 단일 페이지 앱의 페이지 로드 이벤트에서 지워지지 않으므로 [요소 삽입] 및 [다시 정렬] 조작은 방문자가 SPA를 탐색하는 방식에 따라 여러 번 다시 적용할 수 있습니다.

## 통합 및 플러그인 {#section_D92E31170176406AAC7B5005F03D3425}

[!DNL mbox.js] 내의 일부 함수는 [!DNL at.js]에서 사용할 수 없습니다. 내부 [mbox.js 개체 및 메서드](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_8C78059D15D9452F95636A5640188537) (예: `mbox`, `mboxCurrent`, `mboxFactoryDefault`, `mboxFactories` 및 기타)는 더 이상 [!DNL at.js] (예: `mboxFactoryDefault`)에서 지원하지 않습니다. 이것은 [!DNL at.js] &quot;해킹&quot;을 통해 장기적으로 구현을 심각하게 손상하여 업그레이드를 불가능하게 할 수 있는 지원되지 않는 기능을 개발하지 못하도록 디자인되었습니다. 유일하게 노출되는 메서드는 이 설명서의 API 페이지에서 다룹니다. 이 때문에

* 다른 Adobe 솔루션과 이전의 페이지 기반 [통합](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39)은 작동하지 않을 수 있으므로 최신 서버 측 통합으로 업그레이드해야 합니다.
* [mbox.js용으로 개발된 사용자 지정 플러그인](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF)은 [!DNL at.js]용으로 업데이트하지 않으면 작동하지 않을 수 있습니다.

   테스트의 일부로서 어떤 [플러그인](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF)이든 반드시 포함하십시오.

## 비동기 고려 사항 {#section_B586360A3DD34E2995AE25A18E3FB953}

이제 모든 mbox는 비동기이므로 실행된 순서대로 페이지 렌더링을 차단하거나 반환되지 않습니다.

* [양식 기반 경험 작성기](/help/c-experiences/experiences.md#section_3643394BD424463C8768F2907DEBCC22)에서 글로벌 mbox를 사용하는 경우 HTML 오퍼에 `<script>`, `<style>` 및 `<link>` 태그만 포함되어 있는지 확인해야 합니다.

   전달 중에 [!DNL at.js]는 글로벌 mbox 오퍼를 적용할 때 다른 모든 HTML 태그를 필터링합니다. 글로벌 mbox 오퍼는 DIV, SPAN 등을 허용하지 않는 HTML HEAD에 적용됩니다. 예를 들면, `<div>` 태그는 HTML BODY 내부에서만 사용할 수 있으므로 `<div>test</div>`를 적용할 수 없습니다.

* 페이지 기반의 이전 [!DNL Target]-[!DNL Analytics] 통합은 작동하지 않습니다.

   이 통합을 사용하려면 [!DNL Target] 호출 전에 [!DNL Analytics] 호출을 수행해야 합니다.

* 오퍼와 페이지 간의 JavaScript 종속성에 주의하십시오.

   오퍼의 JavaScript는 mbox 아래에 있는 하드코딩된 JavaScript 전에 실행된다고 가정해서는 안 됩니다.

* 페이지에 있는 여러 오퍼 간의 JavaScript 종속성에 주의하십시오.

   더 이상 첫 번째 mbox에서 전달되는 오퍼가 두 번째 mbox에 의해 전달되는 오퍼 전에 실행된다고 가정할 수 없습니다.

* DOM 조작 및 리디렉션 오퍼는 [!DNL at.js]에서 자동 생성된 글로벌 mbox를 통해 전달되고 `<head>`에서 전달되어야 합니다.

   `<body>`의 맨 위에 있는 `mboxCreate()` 함수는 기본 컨텐츠의 플리커를 초래할 가능성이 있습니다.

