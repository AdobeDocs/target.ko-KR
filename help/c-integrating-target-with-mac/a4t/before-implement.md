---
description: Analytics를 Target(A4T)의 보고 소스로 설정할 때 데이터 수집 프로세스에 몇 가지 변경 사항이 발생합니다.
keywords: 권장 사항
seo-description: Analytics를 Target(A4T)의 보고 소스로 설정할 때 데이터 수집 프로세스에 몇 가지 변경 사항이 발생합니다.
seo-title: 구현하기 전에 Adobe Target용 보고 소스로서의 Adobe Analytics(A4T)
solution: Target
title: 구현하기 전에
topic: Premium
uuid: fe603a4b-bd61-49f4-b1b7-a0329aa905f5
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 구현하기 전에{#before-you-implement}

Analytics를 Target(A4T)의 보고 소스로 설정할 때 데이터 수집 프로세스에 몇 가지 변경 사항이 발생합니다.

이 통합의 사용 여부를 결정하기 전에, 다음 섹션을 검토하여 보고 프로세스에 미치는 영향을 고려하십시오.

## 구현 요구 사항 {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>A4T를 사용하려면 먼저 계정을 통합용으로 공급하도록 요청해야 합니다. [이 양식](https://www.adobe.com/go/audiences)을 사용하여 제공을 요청합니다.

이 A 4 T 통합을 사용하려면 4 T에서 리디렉션 오퍼를 사용할지 여부에 따라 다음 라이브러리 버전 이상을 구현해야 합니다.

### A 4 T에서 리디렉션 오퍼를 사용하지 *않을* 경우 필요한 요구 사항

이 통합을 사용하려면 4 T에서 리디렉션 오퍼 사용을 계획하지 않을 경우 다음 라이브러리 버전 이상을 구현해야 합니다. 나열된 순서는 작업 순서입니다.

* Experience Cloud 방문자 ID 서비스: visitorAPI.js 버전 1.8.0
* Adobe Target(구현에 따라 다름): at.js 버전 0.9.1 또는 mbox.js 버전 61
* Adobe Analytics: appMeasurement.js 버전 1.7.0

### A 4 T에서 리디렉션 오퍼를 사용하는 경우 요구 사항 필요

A 4 T에서 리디렉션 오퍼를 사용하려면 다음 라이브러리 버전 이상을 구현해야 합니다. 나열된 순서는 작업 순서입니다.

* Experience Cloud 방문자 ID 서비스: visitorAPI.js 버전 2.3.0
* Adobe Target: at. js 버전 1.6.2

   **참고:** mbox.js 라이브러리는 A4T를 사용하는 리디렉션 오퍼를 지원하지 않습니다. 구현에서 at.js를 사용해야 합니다.

* Adobe Analytics: appMeasurement.js 버전 2.1

다운로드 및 배포 지침은 [Target용 Adobe 구현](https://marketing.adobe.com/resources/help/en_US/target/a4t/c_a4timplementation.html)에 설명되어 있습니다.

## 구현하기 전에 알아야 할 사항 {#section_50D49CC52E11414089C89FB67F9B88F5}

* Analytics를 보고 소스로 사용하도록 선택하면 이 통합을 새 활동에 사용할 수 있습니다. 이 문서에 설명된 대로 구현을 변경해도 기존 활동에는 영향을 주지 않습니다.
* Analytics를 Target의 보고 소스로 설정하는 프로세스에는 몇 가지 구현 설정이 포함되며 그 뒤에 제공 단계가 이어집니다. 구현을 시작하기 전에 아래 설명된 프로세스를 자세히 읽어 보십시오. 이 단계를 모두 수행하면 Analytics가 활성화되는 즉시 보고 소스로 사용할 준비가 완료됩니다. 제공 프로세스는 업무일 기준으로 5일 정도 걸릴 수 있습니다.
* 방문자 ID 서비스는 Experience Cloud 전체에서 공유되는 방문자 ID를 만듭니다. 이 ID는 Target mboxPC ID 또는 Audience Manager UUID를 대체할 수 없지만 Analytics에서 신규 방문자를 식별하는 방법으로 사용할 수 있습니다. 이 ID를 올바르게 설정하면 방문자의 이전 Analytics ID를 통해 이전 Analytics 재방문자도 식별되므로 방문자 누락을 방지할 수 있습니다. 이와 마찬가지로, Target mboxPCid가 그대로 남아 있기 때문에 방문자 ID 서비스로 업그레이드할 때 Target 방문자 프로필 데이터가 손실되지 않습니다.
* 방문자 ID 서비스는 Analytics 및 Target 페이지 코드보다 먼저 실행해야 합니다. `VisitorAPI.js`는 기타 모든 Experience Cloud 제품의 태그 위에 표시되어야 합니다.

## 지연 {#section_9489BE6FD21641A4844E591711E3F813}

이 통합이 활성화되면 Adobe Analytics에서 5-10분 정도 추가적인 지연 시간이 발생합니다. 추가적인 지연 시간으로 인해 Analytics 및 Target의 데이터가 동일한 히트 수로 저장되므로 테스트를 페이지 및 사이트 섹션 단위로 분류할 수 있습니다.

추가적인 지연 시간은 라이브 스트림 및 실시간 보고를 비롯하여 모든 Adobe Analytics 서비스 및 도구에서 반영되며 다음과 같은 시나리오에서 적용됩니다.

* 라이브 스트림, 실시간 보고서 및 API 요청, 트래픽 변수의 현재 데이터의 경우 보충 데이터 ID가 있는 히트 수만 지연됩니다.
* 전환 지표의 현재 데이터, 완료된 데이터, 데이터 피드의 경우 모든 히트 수가 추가적으로 5-7분 지연됩니다.

이 통합을 완전히 완료하지 않았더라도 Experience Cloud 방문자 ID 서비스를 구현하면 추가적인 지연 시간이 발생하기 시작합니다.

## 보충 ID {#section_2C1F745A2B7D41FE9E30915539226E3A}

컨텐츠를 전달하거나 목표 지표를 기록하기 위해 A4T 활동에서 사용하는 모든 Target 호출에는 A4T가 제대로 작동하도록 동일한 보충 ID를 공유하는 해당 Analytics 히트가 있어야 합니다.

Analytics 및 Target의 데이터가 포함된 히트 수에는 보충 데이터 ID가 들어 있습니다. 이 ID는 [Adobe Debugger](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=debugger)에서 `sdid` 매개 변수로 표시됩니다 예: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. 이 ID는 다음 기준이 충족될 때 생성됩니다.

* 방문자 ID 서비스가 구현됨
* 이 통합을 지원하는 [!DNL mbox.js] 버전이 구현됨

문제를 해결할 때 보충 ID가 Analytics 히트 수에 있는지 확인하십시오.
