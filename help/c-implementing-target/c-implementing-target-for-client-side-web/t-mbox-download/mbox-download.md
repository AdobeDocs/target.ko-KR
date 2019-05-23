---
description: Target Standard 또는 Target Premium을 사용하려면 mbox.js를 호출할 코드 한 줄을 추가하십시오.
keywords: 구현;Mbox;mbox.js 다운로드;api 다운로드;mbox.js api
seo-description: Target Standard 또는 Target Premium을 사용하려면 mbox.js를 호출할 코드 한 줄을 추가하십시오.
seo-title: mbox.js 구현
solution: Target
subtopic: 시작하기
title: mbox.js 구현
topic: Standard
uuid: aa53dfd4-db42-4a33-b561-7e84ca7e4497
translation-type: tm+mt
source-git-commit: b45a1a141e9e1d229ed3f92b8124d3edf3bc3042

---


# mbox.js 구현{#mbox-js-implementation}

Target Standard 또는 Target Premium을 사용하려면 mbox.js를 호출할 코드 한 줄을 추가하십시오.

두 라이브러리 참조([!DNL mbox.js] 또는 [!DNL at.js]) 중 하나를 사용할 수 있습니다. [Target JavaScript 라이브러리 이해](../../../c-implementing-target/c-considerations-before-you-implement-target/target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB)에서는 두 라이브러리 간 차이점을 설명합니다.

>[!NOTE]
>
>mbox.js 라이브러리는 계속 지원되지만 기능 업데이트는 제공되지 않을 예정입니다. 모든 고객은 at.js로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [mbox.js에서 at.js로 마이그레이션](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)을 참조하십시오.

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