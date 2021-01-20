---
description: Target이 페이지의 호출을 수행하고 호출에 응답하는 방식은 사용 중인 Target 라이브러리 버전, Experience Cloud 방문자 ID 구현이 존재하는지 여부, 방문자 ID가 있는지 여부에 따라 다릅니다.
title: mbox.js 라이브러리 버전별 Target 페이지 방법
feature: at.js
translation-type: tm+mt
source-git-commit: ae44c57c7b8767915fbbce4271a4b1858dd07efd
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 92%

---


# mbox.js 라이브러리 버전별 Target 페이지 호출 방법{#target-page-methods-by-mbox-js-library-version}

Target이 페이지의 호출을 수행하고 호출에 응답하는 방식은 사용 중인 Target 라이브러리 버전, Experience Cloud 방문자 ID 구현이 존재하는지 여부, 방문자 ID가 있는지 여부에 따라 다릅니다.

>[!IMPORTANT]
>
>**mbox.js 수명 종료**:2021년 3월 31일부터 mbox.js 라이브러리는 더 이상 지원되지  [!DNL Adobe Target] 않습니다. 2021년 3월 31일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 [!DNL Target] 활동이 있는 페이지에 영향을 줍니다.
>
>사이트에서 발생할 수 있는 문제를 방지하려면 모든 고객이 이 날짜 이전에 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [개요:클라이언트측 웹](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)에 대한 Target을 구현합니다.

>[!NOTE]
>
>[!DNL at.js]를 사용하는 경우 모든 호출은 JSON을 사용하여 수행됩니다. 이 페이지에서는 [!DNL mbox.js] 라이브러리 버전에 대해 자세히 설명합니다. 아래 시나리오에 설명된 동작은 [!DNL at.js]에는 적용되지 않습니다.

이 섹션에서는 다음의 각 시나리오에서 [!DNL Target] 라이브러리의 각 버전이 어떻게 페이지의 [!DNL Target] 호출에 응답하는지에 대해 설명합니다.

구현 및 라이브러리 버전에 따라 몇 가지 유형 또는 끝점이 있습니다. 각 시나리오에서 [!DNL Target]이 호출에 응답하는 방식을 이해하려면 각 유형에 익숙해야 합니다.

| 유형/끝점 | 호출 방법 | 응답 컨텐츠 |
|--- |--- |--- |
| 글로벌 mbox를 자동으로 만들기 - 동기 | document.write을 사용하여 호출 | document.write()가 없는 JavaScript |
| 글로벌 mbox를 자동으로 만들기 - 비동기 | createElement()를 사용하여 본문에 호출 추가 | document.write()가 없는 JavaScript |
| standard | document.write을 사용하여 호출 | document.write()가 있는 JavaScript |
| ajax | createElement()를 사용하여 본문에 호출 추가 | document.write()가 없는 JavaScript |
| json | XMLHTTPrequest()를 사용하여 호출 | JSON 응답을 반환합니다. |

>[!IMPORTANT]
>
>표준을 제외한 모든 유형의 경우, 모든 사용자 지정 코드와 오퍼는 ajax 환경을 지원하도록 작성해야 합니다. 예를 들어 `document.write()`을 포함하는 JavaScript를 사용하는 경우 스크립트는 예상대로 작동하지 않습니다.

## 방문자 ID 구현이 없음 {#section_C6F7213FDE4D48E8BBCB1A9A26310FEE}

[!DNL Target Standard]를 사용하는 [!DNL Premium]나 [!DNL mbox.js]을 사용하고, 계정에 대해 [!UICONTROL 글로벌 Mbox 만들기]를 활성화한 경우, **버전에 관계없이**&#x200B;글로벌 mbox를 자동으로 만들기 - 동기[!DNL mbox.js] 유형의 호출 및 응답이 수행됩니다.

[!UICONTROL 시각적 경험 작성기] 작업을 사용하는 대신 자신만의 사용자 지정 코드를 작성하는 경우, 코드가 ajax 환경에 적합한지 확인하십시오. 예를 들어 `document.write()`을 포함하는 JavaScript를 사용하는 경우 스크립트는 예상대로 작동하지 않습니다.

>[!NOTE]
>
>mbox 이름은 동일하지만 매개 변수가 다른 여러 개의 ajax mbox 호출의 경우 동일한 페이지에서 작동하지 않습니다. 첫 번째 호출만 수행됩니다.

이전 구현에서 이전에 사용했던 페이지에서 [!DNL Target Standard]나 [!DNL Premium]을 구현하는 경우처럼, &quot;글로벌 mbox를 자동으로 만들기&quot;를 사용하지만 페이지에 `mboxCreate` 호출도 있는 경우, 글로벌 mbox 호출은 글로벌 mbox를 **자동으로 만들기 - 표준** 종단점을 사용하여 수행되고 `mboxCreate` 호출은 **표준** 종단점을 사용하여 수행됩니다. **표준** 종단점은 `document.write()`을 사용하여 호출하고 응답합니다. 이렇게 하면 모든 정보가 다운로드되기 전까지는 ajax 응답에 전달된 컨텐츠를 포함하여 페이지 로드가 차단됩니다.

[!DNL Target Classic]을 사용하여 작성된 페이지 등에서 mboxCreate만 사용하는 경우에는 페이지가 평상시처럼 작동합니다.

| 작성 방법 | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| 글로벌 mbox를 자동으로 만들기 | 글로벌 mbox를 자동으로 만들기 - 동기 | 글로벌 mbox를 자동으로 만들기 - 동기 | 글로벌 mbox를 자동으로 만들기 - 동기 | 글로벌 mbox를 자동으로 만들기 - 동기 |
| mboxCreate | standard | standard | standard | standard |

## 방문자 ID 구현이 있지만 설정된 방문자 ID가 없음 {#section_29888A119C7A4753AD287FC845AA63F4}

설정된 방문자 ID가 없는 경우 사용자에 대한 [!DNL Experience Cloud] 방문자 쿠키가 없습니다. 페이지는 방문자 ID를 얻기 위해 방문자 ID 서비스를 호출합니다. Target은 [!DNL Target]에 호출하는 ID의 응답을 기다립니다.

>[!NOTE]
>
>Target 호출이 수행되기 전에 [!DNL Mbox.js] v58을 사용하여 방문자 ID가 반환되는지 확인하는 것이 좋습니다.

이 시나리오에서는 [!DNL mbox.js] 버전 57을 사용하고 있는데, 이전 시나리오에서 설명한 대로 방문자 ID 구현이 없으면 모든 것이 원래대로 작동합니다. [!DNL mbox.js] 버전 58부터 [!DNL Experience Cloud Visitor ID] 서비스에서는 [!DNL Target] 호출을 수행하기 전에 방문자 ID를 반환하게 됩니다. 따라서 Profiles 및 Audiences 핵심 서비스를 통해 공유되는 대상 데이터를 방문자 세션의 첫 번째 [!DNL Target] 호출에 사용할 수 있게 됩니다. 테스트 컨텐츠가 반환되기 전에 기본 컨텐츠가 깜박거리는 것을 방지하기 위해 [!DNL Target]에서는 방문자 ID 서비스가 반환될 때까지 `<BODY>`를 숨깁니다. 버전 58에서는 `display:none`을 사용하여 페이지를 숨깁니다. 이렇게 하면 응답 사이트에 문제가 생기므로 버전 59부터는 `opacity:0`을 사용하여 콘텐츠를 숨깁니다.

| 작성 방법 | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| 글로벌 mbox를 자동으로 만들기 | 글로벌 mbox를 자동으로 만들기 - 동기 | 글로벌 mbox를 자동으로 만들기 - 비동기 | 글로벌 mbox를 자동으로 만들기 - 비동기 | 글로벌 mbox를 자동으로 만들기 - 비동기 |
| mboxCreate | standard | ajax | ajax | ajax |

## 방문자 ID 구현이 있고 방문자 ID도 있음  {#section_9CD4AE4C8186425D886398BC3CE6C46D}

방문자 ID 쿠키가 존재하는 경우 [!DNL Target]에서 방문자 ID 서비스에 대한 호출을 수행할 필요가 없습니다. 이 경우 컨텐츠를 표시하기 전에 방문자 ID 서비스를 기다릴 필요가 없습니다. 버전 57~59의 경우 **글로벌 mbox를 자동으로 만들기 - 비동기** 유형을 사용하므로 페이지는 계속해서 로드하기 전에 [!DNL Target]에 대한 호출이 반환되기를 기다립니다. 이렇게 하면 기본 컨텐츠가 깜박이지 않습니다. v60의 경우에는 **글로벌 mbox-비동기 유형**&#x200B;을 사용하여 [!DNL Target] 옵트아웃 서비스가 응답할 때까지 [!DNL Experience Cloud]이 기다리도록 합니다. 옵트아웃 서비스는 2016년 가을에 출시되는 Data Co-op의 일부입니다. 모든 호출은 ajax를 사용하여 반환되므로, [!DNL mbox.js] 버전 60에는 `document.write()`을 사용하면 안 됩니다.

| 작성 방법 | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| 글로벌 mbox를 자동으로 만들기 | 글로벌 mbox를 자동으로 만들기 - 동기 | 글로벌 mbox를 자동으로 만들기 - 동기 | 글로벌 mbox를 자동으로 만들기 - 동기 | 글로벌 mbox를 자동으로 만들기 - 비동기(2016년 후반에 출시되는 Data Co-op 개발을 지원합니다.) |
| mboxCreate | standard | standard | standard | ajax |