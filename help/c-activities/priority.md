---
keywords: settings;priority
description: Adobe Target은 사용 중인 Target 인터페이스 및 활동 생성 기능(Visual Experience Composer 또는 Form Based Composer)에 따라 페이지에 다르게 전달할 활동(또는 활동)을 결정합니다.
title: Adobe Target의 우선 순위
feature: activities
topic: Standard
uuid: 114cd625-2716-4c4c-983b-a7f677717b07
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 87%

---


# 우선 순위{#priority}

Target은 사용 중인 Target 인터페이스와 활동 작성 기능(시각적 경험 작성기 또는 양식 기반 작성기)에 따라 페이지에 전달할 활동을 다르게 결정합니다.

## Target Standard/Premium Visual Experience Composer Only or Form-Based Composer Using Global Target Request Only {#section_4A0A317DFED345649B58B0CB5B410C8B}

회사에서 Target Standard/Premium 및 시각적 경험 작성기만을 사용한다면, 동일한 호출에 대해 여러 활동의 콘텐츠가 반환할 수 있습니다. 활동은 다음 결정 플로우를 사용하여 전달됩니다.

1. Target 서버 호출이 URL 관련 정보와 함께 Target으로 이동합니다.
1. Target은 해당 URL에서 실행 중인 모든 활동을 가져옵니다.
1. Target이 방문자를 활동에 대응시키려고 시도합니다.

   방문자가 A/B 테스트나 다변량 테스트에 이미 있다면 이 방문자는 전환할 때까지 해당 테스트에 속합니다. 방문자가 이전에 경험 타깃팅 활동에 있었다면 해당 활동에 다시 속해야 합니다. 대상 규칙을 충족한다면 방문자는 해당 활동 및 특정 경험에 속하게 됩니다.

1. 방문자가 대응하는 모든 활동 및 경험에 대한 콘텐츠가 페이지에 반환됩니다.
1. 각 활동의 콘텐츠가 서로 다른 [CSS 선택기](/help/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337)를 참조한다면 모든 콘텐츠가 표시됩니다.

   겹치거나 중복되는 CSS 선택기가 있는 경우 우선순위가 가장 높은 활동 콘텐츠가 표시됩니다. 페이지에서 실행되는 모든 활동의 결과는 카운트되고 보고서에 반영됩니다.

   >[!IMPORTANT]
   >
   >Target은 페이지의 모든 활동에 대한 콘텐츠를 반환하는데, 이 콘텐츠는 우선순위가 가장 낮은 콘텐츠부터 시작하여 가장 낮은 우선순위에서 가장 높은 우선순위 순서로 각 활동에 의해 덮어써집니다. 따라서 대부분의 경우 우선순위가 가장 높은 콘텐츠가 표시됩니다. 그러나 우선순위가 낮은 활동이 페이지의 DOM 구조를 변경하는 경우 우선순위가 높은 활동이 페이지 구조를 인식하지 못하게 되어 우선순위가 낮은 콘텐츠가 표시될 수 있습니다. 페이지에서 실행되는 모든 활동의 결과는 카운트되고 보고서에 반영됩니다.

1. 여러 활동의 우선순위 수준이 동일하다면 아래 기준에 따라 표시가 결정됩니다.

   * 하나의 활동에만 대상 타깃팅이 있을 경우 해당 활동이 표시됩니다.
   * 모든 활동에 타깃팅이 있거나 없으면 먼저 승인된 활동이 표시됩니다.

## Target Standard/Premium 양식 기반 작성기 및 Target Standard/Premium 시각적 경험 작성기 {#section_4620253E1CE942DD830724C7822B175F}

>[!NOTE]
>
>이 정보는 [!DNL Target Classic]에서 생성된 실행 중인 모든 캠페인에도 적용됩니다.

회사가 Target Standard/Premiumand의 양식 기반 작성기와 Target Standard/Premium 시각적 경험 작성기를 사용한다면, 여러 시각적 경험 작성기 활동의 콘텐츠를 전달할 수 있지만 양식 기반 워크플로우의 활동은 한 활동의 콘텐츠만 전달할 수 있습니다. 활동 전달은 다음 결정 플로우를 사용하여 결정됩니다.

1. Target server call comes to Target with information about the [!DNL Target] request and URL.
1. Target Classic and Standard pull every activity running in that [!DNL Target] request.
1. Target이 방문자를 활동에 대응시키려고 시도합니다.

   방문자가 A/B 테스트나 다변량 테스트에 이미 있다면 이 방문자는 전환할 때까지 해당 테스트에 속합니다. 방문자가 이전에 경험 타깃팅 활동에 있었다면 해당 활동에 다시 속해야 합니다. 대상 규칙을 충족한다면 방문자는 해당 활동 및 특정 경험에 속하게 됩니다.

1. 양식 기반 활동의 우선순위가 가장 높다면, 해당 활동 콘텐츠가 시각적 경험 작성기 활동의 모든 대응하는 활동 콘텐츠와 함께 반환됩니다.
1. 시각적 경험 작성기 활동 우선순위가 가장 높다면, 모든 대응하는 시각적 경험 작성기 활동의 콘텐츠가 반환되지만 Target Classic 또는 양식 기반 활동 콘텐츠는 반환되지 않습니다.

   페이지에서 실행되는 모든 활동의 결과는 카운트되고 보고서에 반영됩니다.

**예**

각각 검색 키워드 Nike 브랜드와 브랜드 없는 운동화 키워드를 타깃팅하는 두 개의 활동이 있는 경우 먼저 두 활동의 우선순위가 모두 확인됩니다. Nike 활동이 우선순위가 더 높은 경우 해당 콘텐츠가 표시됩니다. 운동화 활동이 우선순위가 더 높은 경우 해당 콘텐츠가 표시됩니다.

타깃팅된 두 활동의 우선순위가 서로 같다면, 가장 최근에 본 활동이 표시됩니다. 방문자가 해당 페이지를 처음 방문했다면 가장 최근에 활성화된 활동이 표시됩니다.

## Target Standard/Premium Form-Based Composer with Non-Global Target Requests {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

>[!NOTE]
>
>이 정보는 Target Classic에서 생성된 실행 중인 모든 캠페인에도 적용됩니다.

If your company uses [!DNL Target] requests other than the global [!DNL Target] request in the form-based composer, content from only one activity can be returned per call. 활동 전달은 다음 결정 플로우를 사용하여 결정됩니다.

1. The [!DNL Target] server call comes to [!DNL Target] with information about the [!DNL Target] request and URL.
1. [!DNL Target] 해당 요청에서 실행되는 모든 활동을 [!DNL Target] 가져옵니다.
1. [!DNL Target] 방문자를 가장 높은 우선 순위 활동에 일치시키려는 시도.

   방문자가 A/B 테스트나 다변량 테스트에 이미 있다면 이 방문자는 전환할 때까지 해당 테스트에 속합니다. 방문자가 이전에 경험 타깃팅 활동에 있었다면 해당 활동에 다시 속해야 합니다. 대상 규칙을 충족한다면 방문자는 해당 활동 및 특정 경험에 속하게 됩니다.

1. 여러 활동의 우선순위 수준이 동일하다면 아래 기준에 따라 표시가 결정됩니다.

   * 하나의 활동에만 대상 타깃팅이 있을 경우 해당 활동이 표시됩니다.
   * 모든 활동에 타깃팅이 있거나 없으면 먼저 승인된 활동이 표시됩니다.

## 예 {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>설정에 따라 우선순위 값은 달라집니다. 낮음, 중간 또는 높음의 레거시 설정을 사용하거나 0에서 999까지 세분화된 우선순위를 사용할 수 있습니다. 자세한 내용은 [활동 설정](/help/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02)을 참조하십시오.

**비전역 Target 요청을 사용하는 두 개의 Target 클래식 캠페인**

* 캠페인 1: homePageHero, offer1, 우선순위 높음
* 캠페인 2: homePageHero, offer2, 우선순위 낮음

응답: offer1

**두 활동이 서로 다른 선택기에 대해 시각적 경험 작성기에서 만들어진 오퍼만 사용**

* 활동 1: target-global-mbox, selector1, visualExpCompOffer1, 우선순위 낮음
* 활동 2: target-global-mbox, selector2, visualExpCompOffer2, 우선순위 높음

응답: visualExpCompOffer1, visualExpCompOffer2

**두 활동이 동일한 선택기에 대해 시각적 경험 작성기에서 만들어진 오퍼만 사용**

* 활동 1: target-global-mbox, selector1, visualExpCompOffer1, 우선순위 낮음
* 활동 2: target-global-mbox, selector1, visualExpCompOffer2, 우선순위 높음

응답: visualExpCompOffer1, visualExpCompOffer2

>[!NOTE]
>
>Target Classic이 선택기 충돌을 처리하지 않아서 위의 두 번째 사용 사례와 동일한 응답이 나왔습니다. Target Standard에서는 이러한 행동을 인식하며 선택기가 DOM에서뿐 아니라 시각적으로도 충돌(일반적으로 경험 편집기 수준이나 캠페인 시뮬레이션 모드에서)하는 기타 사용 사례도 인식합니다.

**두 활동이 시각적 경험 작성기와 두 개의 Target Classic 캠페인에서 만들어진 오퍼 사용**

* 활동 1: target-global-mbox, selector1, visualExpCompOffer1, 중간 높음
* 활동 2: target-global-mbox, selector2, visualExpCompOffer2, 우선순위 낮음
* 캠페인 1: target-global-mbox, offer1, 우선순위 높음
* 캠페인 2: target-global-mbox, offer2, 우선순위 낮음

응답: offer1, visualExpCompOffer2, visualExpCompOffer1

>[!NOTE]
>
>결합한 응답의 순서는 Classic 콘텐츠가 먼저(사용 사례 1에서는 하나의 Classic 응답만 사용됨) 온 다음, 반전된 우선순위로 순서가 지정된 시각적 경험 작성기 오퍼 응답이 옵니다.

## 교육 비디오: 활동 설정(3:02)

이 비디오에는 활동 설정에 대한 정보가 포함되어 있습니다.

* 활동의 목표 입력
* 활동의 우선순위 수준 설정
* 활동 시작 및 종료 시간 예약
* 보고서 필터를 작성하기 위해 보고 대상 추가
* 활동에 대한 메모 입력

>[!VIDEO](https://video.tv.adobe.com/v/17381)