---
keywords: document.write;target;구현;target 구현;dtm;at.js;adobe experience platform web sdk;aep 웹 sdk;웹 sdk
description: 웹 페이지에서 Adobe [!DNL Target] by referencing the [!DNL Target] JavaScript 라이브러리를 구현합니다.
title: ' [!DNL Target]  JavaScript 라이브러리 이해 '
feature: 구현
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 19%

---


# [!DNL Target] JavaScript 라이브러리 이해 

웹 페이지에서 [!DNL Adobe Target] 라이브러리(Adobe Experience Platform Web SDK 또는 at.js)를 참조하여 [!DNL Adobe Target]을 구현합니다.

>[!NOTE]
>
>mbox.js 라이브러리는 더 이상 개발되지 않습니다. 모든 고객은 2021년 3월 31일 이전에 at.js 또는 [!UICONTROL Adobe Experience Platform Web SDK]로 마이그레이션해야 합니다.

## [!DNL Target] JavaScript 라이브러리 간 차이점 {#section_40117C78C2F84FECAC4F1BA40CC4F171}

다음 표에서는 [!DNL Target] JavaScript 라이브러리의 차이점을 설명합니다.

| 라이브러리 참조 | 설명 |
|--- |--- |
| Adobe Experience Platform 웹 SDK | [!UICONTROL Adobe Experience Platform Web SDK]를 사용하면 Adobe Experience Edge 네트워크를 통해 [!DNL Experience Cloud]([!DNL Target] 포함)의 다양한 서비스와 상호 작용할 수 있습니다. [!DNL Adobe Experience Platform Web SDK]으로 마이그레이션하도록 선택하는 경우 *웹 SDK 안내서*&#x200B;에서 [Adobe Experience Platform 웹 SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)란?을 참조하십시오. |
| at.js | at.js는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 보안을 강화하고, Google Chrome의 document.write 경고를 방지하며, 단일 페이지 애플리케이션에 대해 더 나은 구현 옵션을 제공합니다. |

## 페이지 로드 시간에 대한 at.js의 영향 {#section_16630CD0FF0A498EB596A51381366A5A}

많은 고객과 컨설턴트는 특히 새 사용자와 재방문 사용자의 컨텍스트에서 비교하여 페이지 로드 시간에 대한 [!DNL at.js]의 영향을 알고 싶어 합니다. 안타깝게도, [!DNL at.js]이 각 고객의 구현으로 인해 페이지 로드 시간에 어떤 영향을 주는지에 대한 구체적 수치를 측정하고 제공하기는 어렵습니다.

그러나 방문자 API가 페이지에 있다면 [!DNL Target]이 어떻게 [!DNL at.js]이 페이지 로드 시간에 영향을 주는지를 더 잘 이해할 수 있습니다.

>[!NOTE]
>
>방문자 API 및 [!DNL at.js]은 글로벌 mbox를 사용하는 경우에만 페이지 로드 시간에 영향을 미칩니다(본문 숨기기 기법으로 인해). 지역 mbox는 방문자 API 통합의 영향을 받지 않습니다.

다음 섹션에서는 새 방문자와 재방문자에 대한 작업 시퀀스를 설명합니다.

### 새 방문자 수

1. 방문자 API가 로드, 구문 분석 및 실행됩니다.
1. at.js가 로드, 구문 분석 및 실행됩니다.
1. 글로벌 mbox 자동 만들기가 활성화되어 있으면 [!DNL Target] JavaScript 라이브러리는 다음과 같습니다.

   * 방문자 개체를 인스턴스화합니다.
   * [!DNL Target] 라이브러리는 [!UICONTROL Experience Cloud 방문자 ID] 데이터를 검색하려고 합니다.
   * 새 방문자의 경우 방문자 API가 `demdex.net`에 대한 도메인 간 요청을 실행합니다.
   * [!UICONTROL Experience Cloud 방문자 ID] 데이터가 검색되면 Target 요청이 실행됩니다.

### 재방문자

1. 방문자 API가 로드, 구문 분석 및 실행됩니다.
1. at.js가 로드, 구문 분석 및 실행됩니다.
1. 글로벌 mbox 자동 만들기가 활성화되어 있으면 [!DNL Target] JavaScript 라이브러리는 다음과 같습니다.

   * 방문자 개체를 인스턴스화합니다.
   * [!DNL Target] 라이브러리는 [!UICONTROL Experience Cloud 방문자 ID] 데이터를 검색하려고 합니다.
   * 방문자 API는 쿠키의 데이터를 검색합니다.
   * [!UICONTROL Experience Cloud 방문자 ID] 데이터가 검색되면 [!DNL Target]에 대한 요청이 실행됩니다.

>[!NOTE]
>
>새 방문자의 경우 방문자 API가 있으면 [!DNL Target]이 배선을 여러 번 통해 [!DNL Target] 요청에 Experience Cloud 방문자 ID] 데이터가 포함되어 있는지 확인합니다. [!UICONTROL  재방문자의 경우 [!DNL Target]은(는) [!DNL Target]에만 연결하여 개인화된 콘텐츠를 검색합니다.
