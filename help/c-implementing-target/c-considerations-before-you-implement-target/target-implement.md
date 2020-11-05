---
keywords: document.write;target;implement;implement target;dtm;dynamic tag management;at.js;mbox.js;target.js;mbox
description: 웹 페이지에서 Target 라이브러리(at.js 또는 mbox.js)를 참조하여 Target을 구현합니다.
title: Target JavaScript 라이브러리 이해
feature: implementation general
topic: Target
uuid: c8a254c9-afc9-4a55-be01-788c11bef7cc
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 100%

---


# [!DNL Target] JavaScript 라이브러리 이해 {#understand-the-target-javascript-libraries}

웹 페이지에서 [!DNL Target] 라이브러리(at.js 또는 mbox.js)를 참조하여 [!DNL Target]을 구현합니다.

>[!NOTE]
>
>mbox.js 라이브러리는 더 이상 개발되지 않습니다. 모든 고객은 mbox.js에서 at.js로 마이그레이션해야 합니다. 자세한 내용은 [mbox.js에서 at.js로 마이그레이션](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)을 참조하십시오.

## 두 라이브러리 간의 차이점 {#section_40117C78C2F84FECAC4F1BA40CC4F171}

다음 표는 두 라이브러리의 차이점에 대해 설명합니다.

| 라이브러리 참조 | 설명 |
|--- |--- |
| at.js | at.js는 [!DNL Target] 구현을 위한 mbox.js를 대신합니다.<br>여러 가지 이점 중에서 at.js는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 보안을 강화하고, Google Chrome의 document.write 경고를 방지하며, 단일 페이지 애플리케이션에 대해 더 나은 구현 선택 사항을 제공합니다.<br>자세한 내용은 [at.js 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md)을 참조하십시오. |
| mbox.js | [!DNL Target] 16.3.1(2016년 3월) 이전 [!DNL Target]에서는 [!DNL Target]에서 활동을 전달하고, 클릭을 추적하고, 대부분의 성공 지표를 추적하는 데 필요한 글로벌 mbox를 만들 수 있도록 mbox.js를 호출해야 했습니다. 이 파일에는 모든 활동에 필요한 라이브러리가 들어 있으므로, 파일의 다른 활동별 버전을 유지 관리할 필요는 없습니다.<br>페이지에 이전 스타일의 [!DNL Target] 구현에서 비롯된 랩핑 mbox가 이미 있다면, 이 mbox를 새 인터페이스에서 계속 사용할 수 있습니다. 업데이트된 mbox.js 파일은 여전히 필요하지만, 이 mbox를 활동에 대해 선택하고 시각적 경험 작성기를 사용하여 편집할 수 있습니다.<br>[!DNL Target] Standard 및 Premium은 target.js 파일을 참조하여 mbox.js를 업데이트하고 보완합니다. target.js 파일은 Adobe로 호스팅됩니다. target.js 파일은 페이지에 사전 정의된 mbox가 없는 경우에도 시각적 경험 작성기를 사용하여 어떤 페이지에서든 콘텐츠를 편집할 수 있도록 해줍니다. 사이트의 모든 페이지에서는 이 파일을 참조해야 합니다.<br>자세한 내용은 [mbox.js 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)을 참조하십시오.<br>**중요**: mbox.js 라이브러리는 계속 지원되지만 기능 업데이트는 제공되지 않을 예정입니다. 모든 고객은 at.js로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [mbox.js에서 at.js로 마이그레이션](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md)<br>을 참조하십시오 |

## 페이지 로드 시간에 대한 at.js 및 mbox.js의 영향 {#section_16630CD0FF0A498EB596A51381366A5A}

많은 고객과 컨설턴트는 특히 새 사용자와 재방문 사용자의 컨텍스트에서 비교하여 페이지 로드 시간에 대한 [!DNL at.js]와 [!DNL mbox.js]의 영향을 알고 싶어 합니다. 안타깝게도, 제각각의 고객 구현으로 인해 [!DNL at.js]나 [!DNL mbox.js]가 어떻게 페이지 로드 시간에 영향을 주는지에 대한 구체적 수치를 측정하고 제공하기는 어렵습니다.

하지만 방문자 API가 페이지에 있다면 [!DNL at.js]와 [!DNL mbox.js]가 어떻게 페이지 로드 시간에 영향을 주는지를 더 잘 이해할 수 있습니다.

>[!NOTE]
>
>방문자 API와 [!DNL at.js] 또는 [!DNL mbox.js]는 글로벌 mbox를 사용하는 경우에만 페이지 로드 시간에 영향을 미칩니다(본문 숨기기 기법으로 인해). 지역 mbox는 방문자 API 통합의 영향을 받지 않습니다.

다음 섹션에서는 새 방문자와 재방문자에 대한 작업 시퀀스를 설명합니다.

### 새 방문자 수

1. 방문자 API가 로드, 구문 분석 및 실행됩니다.
1. at.js/mbox.js가 로드, 구문 분석 및 실행됩니다.
1. 글로벌 mbox 자동 생성 기능이 활성화되어 있을 경우, Target JavaScript 라이브러리는

   * 방문자 개체를 인스턴스화합니다.
   * Target 라이브러리가 Experience Cloud 방문자 ID 데이터 검색을 시도합니다.
   * 새 방문자이므로 방문자 API는 demdex.net에 대한 도메인 간 요청을 실행합니다.
   * Experience Cloud 방문자 ID 데이터가 검색되면 Target에 대한 요청이 실행됩니다.

### 재방문자

1. 방문자 API가 로드, 구문 분석 및 실행됩니다.
1. at.js/mbox.js가 로드, 구문 분석 및 실행됩니다.
1. 글로벌 mbox 자동 생성 기능이 활성화되어 있을 경우, Target JavaScript 라이브러리는

   * 방문자 개체를 인스턴스화합니다.
   * Target 라이브러리가 Experience Cloud 방문자 ID 데이터 검색을 시도합니다.
   * 방문자 API는 쿠키의 데이터를 검색합니다.
   * Experience Cloud 방문자 ID 데이터가 검색되면 Target에 대한 요청이 실행됩니다.

>[!NOTE]
>
>새 방문자의 경우, 방문자 API가 있으면 Target은 여러 번 연결하여 Target 요청에 Experience Cloud 방문자 ID 데이터가 포함되어 있는지 확인해야 합니다. 재방문자의 경우 Target은 Target에만 연결하여 개인화된 콘텐츠를 검색합니다.
