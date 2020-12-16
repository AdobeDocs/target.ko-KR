---
keywords: Implementation;Mbox;download mbox.js;download api;mbox.js api
description: Target Standard 또는 Target Premium을 사용하려면 mbox.js를 호출할 코드 한 줄을 추가하십시오.
title: mbox.js 구현
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 55%

---


# mbox.js 구현{#mbox-js-implementation}

Target Standard 또는 Target Premium을 사용하려면 mbox.js를 호출할 코드 한 줄을 추가하십시오.

두 라이브러리 참조([!DNL mbox.js] 또는 [!DNL at.js]) 중 하나를 사용할 수 있습니다. [at.js의 이점](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits)은 두 라이브러리의 차이점을 설명합니다.

>[!NOTE]
>
>**mbox.js 수명 종료**:2021년 1월 18일부터 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 1월 18일 이후, mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 실행 중인 Target 활동이 있는 페이지에 영향을 줍니다. 모든 고객은 사이트에서 발생할 수 있는 문제를 방지하기 위해 이 날짜 이전에 at.js 라이브러리의 최신 버전으로 전환하는 것이 좋습니다. 자세한 내용은 [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)를 참조하십시오.
>
>mbox.js는 현재 지원되지만 2017년 7월부터 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 다른 이점 중에서도 at.js는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 보안을 강화하고, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
>
>모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe에서 기대하는 지원을 제공할 수 있습니다.

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