---
keywords: 구현;구현;설정;데이터 공급자
description: 데이터 공급자를 사용하여 Target에 데이터를 가져옵니다.
title: 데이터 공급자를 사용하여 데이터를 Target으로 가져오려면 어떻게 해야 합니까?
feature: 구현
role: Developer
translation-type: tm+mt
source-git-commit: e8c25685341319fea4381386cad1ce0c5b80face
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 66%

---

# 데이터 공급자

데이터 공급자는 제3자의 데이터를 [!DNL Adobe Target]으로 쉽게 전달할 수 있는 기능입니다.

참고:데이터 공급자는 at.js 1.3 이상이 필요합니다.

## 형식

`window.targetGlobalSettings.dataProviders` 설정은 데이터 공급자의 배열입니다.

각 데이터 공급자 구조에 대한 자세한 내용은 [데이터 공급자](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)를 참조하십시오.

## 활용 사례 예

날씨 서비스, DMP 또는 사용자 지정 웹 서비스와 같은 타사로부터 데이터를 수집합니다. 그런 다음, 이 데이터를 사용하여 대상, Target 콘텐츠를 작성하고 방문자 프로필을 보강할 수 있습니다.

## 방법의 이점

이 설정을 사용하여 고객은 Demandbase, BlueKai 및 사용자 지정 서비스와 같은 서드 파티 데이터 공급자로부터 데이터를 수집하고, 글로벌 mbox의 mbox 매개 변수가 요청할 때 Target으로 데이터를 전달할 수 있습니다.

비동기 및 동기 요청을 통해 여러 공급자로부터 데이터를 수집하도록 지원합니다.

이 접근 방식을 사용하면 각 공급자에 대해 독립적인 시간 제한을 포함하여 페이지 성능에 미치는 영향을 제한하면서, 기본 페이지 콘텐츠의 깜박임을 쉽게 관리할 수 있습니다

## 주의 사항

`window.targetGlobalSettings.dataProviders`에 추가된 데이터 공급자가 비동기인 경우 동시에 실행됩니다. 방문자 API 요청은 최소 대기 시간을 허용하도록 `window.targetGlobalSettings.dataProviders`에 추가된 기능과 병렬로 실행됩니다.

at.js는 데이터를 캐시하려고 하지 않습니다. 데이터 공급자는 데이터를 한 번만 가져오는 경우 데이터가 캐시되는지 확인해야 하고, 공급자 함수가 호출될 때 두 번째 호출을 위해 캐시 데이터를 제공해야 합니다.

## 코드 예제

[데이터 공급자](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)에서 몇 가지 예를 볼 수 있습니다.

## 관련 정보에 대한 링크

문서: [데이터 공급자](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)

## 교육 비디오:

* [Adobe Target에서 데이터 공급자 사용](https://helpx.adobe.com/kr/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Adobe Target에서 데이터 공급자 구현](https://helpx.adobe.com/kr/target/kt/using/dataProviders-atjs-technical-video-implement.html)