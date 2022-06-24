---
keywords: 구현;구현;설정;데이터 공급자
description: 로 데이터 가져오기 [!DNL Target] 데이터 공급자 사용.
title: 로 데이터를 가져오려면 어떻게 해야 합니까? [!DNL Target] 데이터 공급자를 사용하십니까?
feature: Implementation
role: Developer
exl-id: 05fe9190-4d36-43e2-9fc7-c354a6821bfb
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 55%

---

# 데이터 공급자

데이터 공급자는 타사의 데이터를 [!DNL Adobe Target].

참고: 데이터 공급자는 at.js 1.3 이상이 필요합니다.

## 형식

`window.targetGlobalSettings.dataProviders` 설정은 데이터 공급자의 배열입니다.

각 데이터 공급자의 구조에 대한 자세한 내용은 [데이터 공급자](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}.

## 사용 사례 예

날씨 서비스, DMP 또는 사용자 지정 웹 서비스와 같은 타사로부터 데이터를 수집합니다. 그런 다음, 이 데이터를 사용하여 대상, Target 콘텐츠를 작성하고 방문자 프로필을 보강할 수 있습니다.

## 방법의 이점

이 설정을 사용하여 고객은 Demandbase, BlueKai 및 사용자 지정 서비스와 같은 서드 파티 데이터 공급자로부터 데이터를 수집하고, 글로벌 mbox의 mbox 매개 변수가 요청할 때 Target으로 데이터를 전달할 수 있습니다.

비동기 및 동기 요청을 통해 여러 공급자로부터 데이터를 수집하도록 지원합니다.

이 접근 방식을 사용하면 각 공급자에 대해 독립적인 시간 제한을 포함하여 페이지 성능에 미치는 영향을 제한하면서, 기본 페이지 콘텐츠의 깜박임을 쉽게 관리할 수 있습니다

## 주의 사항

데이터 공급자가 `window.targetGlobalSettings.dataProviders` 비동기 상태인 경우 동시에 실행됩니다. 방문자 API 요청은 에 추가된 함수와 함께 실행됩니다 `window.targetGlobalSettings.dataProviders` 최소 대기 시간을 허용합니다.

at.js는 데이터를 캐시하려고 하지 않습니다. 데이터 공급자는 데이터를 한 번만 가져오는 경우 데이터가 캐시되는지 확인해야 하고, 공급자 함수가 호출될 때 두 번째 호출을 위해 캐시 데이터를 제공해야 합니다.

## 코드 예

몇 가지 예는 다음과 같습니다 [데이터 공급자](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}.

## 관련 정보에 대한 링크

문서: [데이터 공급자](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/)

## 교육 비디오:

* [Adobe Target에서 데이터 공급자 사용](https://helpx.adobe.com/kr/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Adobe Target에서 데이터 공급자 구현](https://helpx.adobe.com/kr/target/kt/using/dataProviders-atjs-technical-video-implement.html)