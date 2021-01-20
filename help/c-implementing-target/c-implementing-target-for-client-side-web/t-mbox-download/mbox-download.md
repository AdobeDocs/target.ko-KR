---
keywords: implementation;mbox;download mbox.js;download api;mbox.js api
description: Adobe Target Standard 또는 Target Premium을 사용하려면 코드 한 줄을 추가하여 mbox.js를 호출합니다.
title: mbox.js 구현
feature: null
translation-type: tm+mt
source-git-commit: ae44c57c7b8767915fbbce4271a4b1858dd07efd
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 52%

---


# mbox.js 구현

[!DNL Adobe Target Standard] 또는 [!DNL Target Premium]을 사용하려면 한 줄의 코드를 추가하여 mbox.js를 호출합니다.

두 라이브러리 참조 중 하나를 사용할 수 있습니다.[!DNL Adobe Experience Platform Web SDK] 또는 [!DNL at.js]. [at.js의 이점](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) 은 mbox.js와 at.js 라이브러리 간의 차이점을 설명합니다.

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리는 더 이상 지원되지  [!DNL Adobe Target] 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다.
>
>사이트에서 발생할 수 있는 문제를 방지하려면 모든 고객이 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [개요:클라이언트측 웹](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)에 대한 Target을 구현합니다.

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