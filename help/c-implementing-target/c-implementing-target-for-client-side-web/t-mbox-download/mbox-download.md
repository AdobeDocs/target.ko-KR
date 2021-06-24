---
keywords: 구현;mbox;mbox.js 다운로드;api 다운로드;mbox.js api
description: Adobe Target의 이전 mbox.js 구현에 대해 알아봅니다. Adobe Experience Platform 웹 SDK(AEP 웹 SDK) 또는 최신 at.js 버전으로 마이그레이션합니다.
title: mbox.js를 사용하여 [!DNL Target] 을 구현하려면 어떻게 합니까?
feature: at.js
role: Developer
exl-id: 105095d7-8e29-413b-a7f4-e46e2e30e91f
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 65%

---

# mbox.js 구현

[!DNL Adobe Target Standard] 또는 [!DNL Target Premium]을 사용하려면 mbox.js를 호출할 코드 한 줄을 추가하십시오.

다음 두 라이브러리 참조 중 하나를 사용할 수 있습니다.[!DNL Adobe Experience Platform Web SDK] 또는 [!DNL at.js]

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js로부터의 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 미칩니다.
>
>이 날짜 이전에 모든 고객이 사이트에서 발생할 수 있는 문제를 방지하기 위해 새로운 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

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
