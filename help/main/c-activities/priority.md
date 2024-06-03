---
keywords: 설정;우선순위
description: 방법 알아보기 [!DNL Adobe Target] 에 따라 페이지에 전달할 활동을 다르게 결정합니다. [!DNL Target] 사용 중인 활동 만들기 기능과 인터페이스입니다.
title: 은 어떻게 합니까? [!DNL Target] 다른 활동에 우선 순위를 할당하시겠습니까?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
source-git-commit: be6e45ff301f549eb5be24a65b05c4a9c1cd6089
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 37%

---

# 우선순위

[!DNL Adobe Target] 에 따라 페이지에 전달할 활동을 다르게 결정합니다. [!DNL Target] 인터페이스 및 활동 만들기 기능([[!UICONTROL Visual Experience Composer (VEC)]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) 또는 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md))을 사용하고 있습니다.

## [!UICONTROL Visual Experience Composer] 또는 [!UICONTROL Form-Based Experience Composer] 전역 사용 [!DNL Target] 요청만 {#section_4A0A317DFED345649B58B0CB5B410C8B}

회사에서 VEC만 사용하는 경우 동일한 호출에 대해 여러 활동의 콘텐츠가 반환될 수 있습니다. 활동은 다음 결정 플로우를 사용하여 전달됩니다.

1. 다음 [!DNL Target] 서버 호출이 다음에 옵니다. [!DNL Target] (URL에 대한 정보 포함)
1. [!DNL Target] 는 해당 URL에서 실행 중인 모든 활동을 가져옵니다.
1. [!DNL Target] 는 방문자를 활동에 일치시키려고 시도합니다.

   방문자가 이미 다음에 있는 경우 [!UICONTROL A/B Test] 또는 [!UICONTROL Multivariate Test] 활동. 전환될 때까지 해당 활동과 일치합니다. 이전에 [!UICONTROL Experience Targeting] 활동. 다시 일치해야 합니다. 대상 규칙을 충족한다면 방문자는 해당 활동 및 특정 경험에 속하게 됩니다.

1. 방문자가 대응하는 모든 활동 및 경험에 대한 콘텐츠가 페이지에 반환됩니다.
1. 각 활동의 콘텐츠가 서로 다른 [CSS 선택기](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337)을 클릭하면 모든 컨텐츠가 표시됩니다.

   겹치거나 중복되는 CSS 선택기가 있는 경우 우선순위가 가장 높은 활동 콘텐츠가 표시됩니다. 페이지에서 실행되는 모든 활동의 결과는 카운트되고 보고서에 반영됩니다.

   >[!IMPORTANT]
   >
   >[!DNL Target] 은 페이지의 모든 활동에 대한 컨텐츠를 반환하며, 이 컨텐츠는 우선순위가 가장 낮은 컨텐츠부터 시작하여 가장 낮은 우선순위에서 가장 높은 우선순위 순서로 각 활동에 의해 덮어써집니다. 일반적으로 이렇게 하면 우선순위가 가장 높은 콘텐츠가 표시됩니다. 그러나 우선순위가 낮은 활동이 페이지의 DOM 구조를 변경하는 경우 우선순위가 높은 활동이 페이지 구조를 인식하지 못하여 우선순위가 낮은 콘텐츠가 표시될 수 있습니다. 페이지에서 실행되는 모든 활동의 결과는 카운트되고 보고서에 반영됩니다.

1. 여러 활동이 우선순위 수준을 공유하는 경우 두 개의 타이 브레이커가 있습니다.

   * 하나의 활동에만 대상 타깃팅이 있을 경우 해당 활동이 표시됩니다.
   * 모두 또는 없음에 타깃팅이 있는 경우 먼저 승인된 활동이 표시됩니다.

## [!UICONTROL Form-Based Experience Composer] 및 [!UICONTROL Visual Experience Composer] {#section_4620253E1CE942DD830724C7822B175F}

회사에서 를 사용하는 경우 [!UICONTROL Form-Based Experience Composer] *및* vec, 복수 콘텐츠 [!UICONTROL Form-Based Experience Composer] 및 VEC 활동은 전달할 수 있습니다. 이전에는 양식 기반 워크플로우에서 하나의 활동만 전달할 수 있었습니다. 더 이상 게재할 수 있는 양식 기반 활동 수에 제한이 없습니다.

활동 전달은 다음 결정 플로우를 사용하여 결정됩니다.

1. [!DNL Target] 서버 호출이 다음에 옵니다. [!DNL Target] 다음에 대한 정보 포함 [!DNL Target] 요청 및 URL입니다.
1. [!DNL Target] 에서 실행 중인 모든 활동을 가져옵니다. [!DNL Target] 요청.
1. [!DNL Target] 는 방문자를 활동에 일치시키려고 시도합니다.

   방문자가 이미 다음에 있는 경우 [!UICONTROL A/B Test] 또는 [!UICONTROL Multivariate Test] 활동을 수행하면 전환될 때까지 해당 테스트에 일치합니다. 이전에 [!UICONTROL Experience Targeting] 활동. 다시 일치해야 합니다. 대상 규칙을 충족한다면 방문자는 해당 활동 및 특정 경험에 속하게 됩니다.

1. 양식 기반 활동의 우선순위가 가장 높다면, 해당 활동 콘텐츠가 VEC 활동의 모든 일치하는 활동 콘텐츠와 함께 반환됩니다.
1. VEC 활동이 가장 높은 우선 순위인 경우, 일치하는 모든 VEC 활동의 콘텐츠가 반환되지만 양식 기반 활동 콘텐츠는 반환되지 않습니다.

   페이지에서 실행되는 모든 활동의 결과는 카운트되고 보고서에 반영됩니다.

**예**

브랜드 검색 키워드 &#39;Nike&#39;를 타깃팅하는 활동과 비브랜드 키워드 &#39;스니커즈&#39;를 타깃팅하는 두 개의 활동이 있는 경우 두 활동의 우선 순위를 확인합니다. Nike 활동이 우선순위가 더 높은 경우 해당 콘텐츠가 표시됩니다. 운동화 활동이 우선순위가 더 높은 경우 해당 콘텐츠가 표시됩니다.

타깃팅된 두 활동의 우선순위가 서로 같다면, 가장 최근에 본 활동이 표시됩니다. 방문자가 해당 페이지를 처음 방문했다면 가장 최근에 활성화된 활동이 표시됩니다.

## [!UICONTROL Form-Based Experience Composer] 비전역 [!DNL Target] 요청 {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

회사에서 를 사용하는 경우 [!DNL Target] 글로벌 이외의 요청 [!DNL Target] 양식 기반 작성기의 요청에서는 호출당 하나의 활동만 콘텐츠를 반환할 수 있습니다. 활동 전달은 다음 결정 플로우를 사용하여 결정됩니다.

1. 다음 [!DNL Target] 서버 호출이 다음에 옵니다. [!DNL Target] 다음에 대한 정보 포함 [!DNL Target] 요청 및 URL입니다.
1. [!DNL Target] 에서 실행 중인 모든 활동을 가져옵니다. [!DNL Target] 요청.
1. [!DNL Target] 는 방문자를 우선순위가 가장 높은 활동에 일치시키려고 시도합니다.

   방문자가 이미 다음에 있는 경우 [!UICONTROL A/B Test] 또는 [!UICONTROL Multivariate Test] 활동. 전환될 때까지 해당 활동과 일치합니다. 이전에 [!UICONTROL Experience Targeting] 활동. 다시 일치해야 합니다. 대상 규칙을 충족한다면 방문자는 해당 활동 및 특정 경험에 속하게 됩니다.

1. 여러 활동이 우선순위 수준을 공유하는 경우 두 개의 타이 브레이커가 있습니다.

   * 하나의 활동에만 대상 타깃팅이 있을 경우 해당 활동이 표시됩니다.
   * 모두 또는 없음에 타깃팅이 있는 경우 먼저 승인된 활동이 표시됩니다.

## 예 {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>설정에 따라 우선순위 값은 달라집니다. 의 이전 설정을 사용할 수 있습니다. [!UICONTROL Low], [!UICONTROL Medium], 또는 [!UICONTROL High]또는 0에서 999까지 세분화된 우선순위를 활성화할 수 있습니다. 자세한 내용은 [활동 설정](/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02).

응답: offer1

**두 활동은에서 만든 오퍼만 사용합니다. [!UICONTROL Visual Experience Composer] 다른 선택기용**

* 활동 1: target-global-mbox, selector1, visualExpCompOffer1, 우선순위 낮음
* 활동 2: target-global-mbox, selector2, visualExpCompOffer2, 우선순위 높음

응답: visualExpCompOffer1, visualExpCompOffer2

**두 활동은에서 만든 오퍼만 사용합니다. [!UICONTROL Visual Experience Composer] 동일한 선택기에 대해**

* 활동 1: target-global-mbox, selector1, visualExpCompOffer1, 우선순위 낮음
* 활동 2: target-global-mbox, selector1, visualExpCompOffer2, 우선순위 높음

응답: visualExpCompOffer1, visualExpCompOffer2

## 교육 비디오: 활동 설정(3:02)

이 비디오에는 활동 설정에 대한 정보가 포함되어 있습니다.

* 활동의 목표 입력
* 활동의 우선순위 수준 설정
* 활동 시작 및 종료 시간 예약
* 보고서 필터를 작성하기 위해 보고 대상 추가
* 활동에 대한 메모 입력

>[!VIDEO](https://video.tv.adobe.com/v/17381)
