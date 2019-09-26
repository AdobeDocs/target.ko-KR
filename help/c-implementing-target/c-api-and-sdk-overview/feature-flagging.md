---
description: 현대 기술 제품 팀은 제품 출시에 대한 지속적인 제공 원칙을 채택하고 있습니다. Target을 사용하면 개발자와 제품 팀은 신속하고 효율적으로 새로운 제품 기능을 제공할 수 있습니다.
keywords: 롤아웃;롤아웃;연속 배달;제품 실행;단계별 롤아웃;롤아웃;롤아웃;롤아웃;롤아웃;연속 배달;제품 실행;단계별 롤아웃;rollment rollout;roll out;continuous delivery;product launch;단계별 롤아웃;product launch;
seo-description: 현대 기술 제품 팀은 제품 출시에 대한 지속적인 제공 원칙을 채택하고 있습니다. Adobe Target을 사용하면 개발자와 제품 팀은 단계적 출시에 새로운 제품 기능을 신속하고 효율적으로 실행할 수 있습니다.
seo-title: 현대 기술 제품 팀은 제품 출시에 대한 지속적인 제공 원칙을 채택하고 있습니다. 개발자와 제품 팀은 Adobe Target을 사용하여 신속하고 효율적으로 새로운 제품 기능을 출시할 수 있습니다.
solution: Target
title: 기능 플래그 지정
topic: Standard
translation-type: tm+mt
source-git-commit: 08debab3ec3d2f6e6bfd3c42476dc1a021185ab7

---


# 기능 플래그 지정

Contemporary technology product teams are adopting continuous delivery principles for product launches. Adobe Target을 사용하면 개발자와 제품 팀은 단계적 출시에 새로운 제품 기능을 신속하고 효율적으로 실행할 수 있습니다.

다음 링크는 지속적인 전달을 활성화하는 데 필요한 주요 개념에 대한 정보를 제공합니다.

* [A/B Test activities](/help/c-activities/t-test-ab/test-ab.md)
* [JSON 제공](/help/c-experiences/c-manage-content/create-json-offer.md)
* [Audience refinements](/help/c-target/c-audiences/creating-a-profile-attribute-comparison-audience.md)

## Continuous delivery

1. By default, turn the feature "off" on release.

   Use a server-side or in-app variable to control this.

1. Create a Target JSON Offer that sets this variable to "on."

1. Create an A/B Test activity in the Visual Experience Composer (VEC) with two experiences and use the JSON offer created in the previous step in one experience.[](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md)

   또는

   양식 기반 Experience Composer에서 [단일 경험을](/help/c-experiences/form-experience-composer.md) 사용하여 A/B 테스트 활동을 만들고 이전 단계에서 만든 JSON 오퍼를 사용합니다.

   >[!NOTE]
   >
   >The Form-based Experience Composer allows you to create an A/B Test activity with a single experience. You cannot create the activity with a single experience using the VEC.

1. 활동에 대해 원하는 트래픽 할당을 지정합니다.

   이 기능을 방문자의 5%까지 롤아웃하여 시작하려면 3부 안내 워크플로우의 타깃팅 단계에서 5를 지정하고 JSON 오퍼(경험 A)를 사용하여 적격한 방문자의 100%를 경험으로 전송합니다.

   다음 그림은 두 개의 경험이 있는 VEC를 보여줍니다.

   ![VEC의 기능 플래그 지정에 대한 트래픽 할당](/help/c-implementing-target/c-api-and-sdk-overview/assets/feature-flagging.png)

   다음 그림은 단일 경험으로 양식 기반 경험 작성기를 보여줍니다.

   ![양식 기반 Experience Composer의 기능 플래그 지정에 대한 트래픽 할당](/help/c-implementing-target/c-api-and-sdk-overview/assets/feature-flagging-form.png)

1. Target UI를 통해 또는 100% 트래픽 할당에 도달할 때까지 API를 사용하여 5%를 점차적으로 증가시켜 이 활동에 대한 트래픽 할당을 늘릴 수 있습니다.

   >[!NOTE]
   >
   >A/B 테스트 활동은 세션을 통해 방문자에게 고정됩니다. 트래픽 할당을 줄이는 경우 이 기능을 보기 시작한 방문자는 세션이 재설정될 때까지 계속 이 기능을 봅니다.

## A/B 테스트 기능

A/B/..N 테스트 기능에서는 위에 설명한 방법을 다음과 같이 개선하십시오.

* 각 기능 변형은 Target 환경을 만드는 적절한 JSON 오퍼를 사용하여 표시되어야 합니다.
* You can manage traffic allocation for this test in the manner described above.

## 매개 변수화된 롤아웃

위에 설명된 방법은 제어된 롤아웃을 관리하는 데 도움이 됩니다.

You can roll out a feature for your beta participants only and then later roll out the feature to all other customers. 이 작업은 타겟 위치(mbox) 매개 [변수](/help/c-target/c-audiences/c-target-rules/custom-parameters.md) 또는 [프로필 매개 변수를](/help/c-target/c-audiences/c-target-rules/visitor-profile.md)활용하여 쉽게 수행할 수 있습니다. These parameters can be used in conjunction with phased traffic allocation.

## Server-side vs. client-side

Feature rollouts and testing can be delivered via Target APIs (and server-side SDKs) as well as the client side SDKs (JS, Mobile SDK). [](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) Depending on how your website, mobile app, or kiosk is architected, you can leverage Target's different integration options.
