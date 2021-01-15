---
keywords: implementation;mbox;download mbox.js;download api;mbox.js api
description: Adobe Target Standard 또는 Target Premium을 사용하려면 코드 한 줄을 추가하여 mbox.js를 호출합니다.
title: mbox.js 구현
feature: null
translation-type: tm+mt
source-git-commit: a85a5c10c31fb0d7eb00c21ff03b2012d044de45
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 32%

---


# mbox.js 구현

[!DNL Adobe Target Standard] 또는 [!DNL Target Premium]을 사용하려면 한 줄의 코드를 추가하여 mbox.js를 호출합니다.

두 라이브러리 참조 중 하나를 사용할 수 있습니다.[!DNL Adobe Experience Platform Web SDK] 또는 [!DNL at.js]. [at.js의 이점](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) 은 mbox.js와 at.js 라이브러리 간의 차이점을 설명합니다.

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리는 더 이상 지원되지  [!DNL Adobe Target] 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다. 사이트에서 발생할 수 있는 문제를 방지하려면 모든 고객이 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다.
>
>* **Adobe Experience Platform 웹 SDK**:Adobe Experience Platform  [!UICONTROL 웹 ] SDK를 사용하면 Adobe Experience Edge Network를  [!DNL Experience Cloud] (포함)에서 다양한 서비스와 상호 작용할  [!DNL Target]수 있습니다. [!DNL Adobe Experience Platform Web SDK]으로 마이그레이션하도록 선택하는 경우 *웹 SDK 안내서*&#x200B;에서 [Adobe Experience Platform 웹 SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)란?을 참조하십시오.
   >
   >
* **at.js**:at.js JavaScript 라이브러리는 mbox.js보다 많은 이점을 제공합니다. 다른 이점 중에서도 at.js는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 보안을 강화하고, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다. at.js로 마이그레이션하도록 선택하는 경우 [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target Skill Builder:개발자 채팅, Adobe Target의 mbox.js를 at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true)로 마이그레이션합니다.
>
>
mbox.js는 현재 지원되지만(2021년 3월 31일까지) 2017년 7월 이후로 이 라이브러리에 기능 업데이트를 제공하지 않았습니다. 모든 고객을 [!UICONTROL Adobe Experience Platform Web SDK] 또는 at.js로 이동하면 엔지니어 및 지원 직원이 새로운 기능을 제공하고 Adobe에서 기대하는 지원을 제공할 수 있게 됩니다.

각 페이지의 [!DNL mbox.js]에 대한 단일 참조는 모든 활동에 필요한 라이브러리를 제공합니다. [!DNL mbox.js]는 [!DNL Target] 파일을 참조하는 모든 페이지에서 [!DNL mbox.js]을 호출합니다. 이렇게 하면 [!DNL Target]에서 다음을 수행할 수 있습니다.

* Target 활동 전달
* 클릭 수 추적
* 대부분의 성공 지표 추적

>[!TIP]
>
>구현을 단순화하기 위해 글로벌 헤더에서 [!DNL mbox.js]를 참조할 수 있습니다.

파일의 다른 활동별 버전을 유지 관리할 필요는 없습니다.

1. 사이트의 각 페이지에 있는 [!DNL mbox.js] 섹션에서 `<head>`를 참조합니다.

   `<script src="/ *`directory`*/ *`scripts`*/mbox.js"></script>`

   여기서 ` *`directory`*/ *`scripts`*`는 [!DNL mbox.js] 파일을 다운로드한 후 저장한 디렉토리입니다.
기존 구현의 mbox가 페이지에 이미 있는 경우 이러한 mbox는 새 인터페이스에서 계속 사용할 수 있습니다. 업데이트된 [!DNL mbox.js] 파일은 여전히 필요하지만, 이 mbox를 활동에 대해 선택하고 [!UICONTROL 시각적 경험 작성기]를 사용하여 편집할 수 있습니다.