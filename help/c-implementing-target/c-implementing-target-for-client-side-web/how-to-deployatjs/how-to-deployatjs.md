---
keywords: implement;at.js;javascript library
description: 태그 관리자 없이 Adobe Launch 또는 Adobe DTM(Dynamic Tag Management)을 사용하여 Adobe Target JavaScript 라이브러리를 배포하는 방법에 대한 정보입니다.
title: at.js를 배포하는 방법
feature: Implement Server-side
translation-type: tm+mt
source-git-commit: 88f6e4c6ad168e4f9ce69aa6618d8641b466e28a
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 57%

---


# at.js를 배포하는 방법

태그 관리자 없이 Adobe Launch 또는 Adobe DTM(Dynamic Tag Management)을 사용하여 Adobe Target JavaScript 라이브러리를 배포하는 방법에 대한 정보입니다.

다음 방법을 사용하여 at.js를 배포할 수 있습니다.

* **[Adobe Launch를 사용하여 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)**: Launch는 Adobe의 차세대 태그 관리 플랫폼이며, Adobe Target을 구현하는 기본 방법입니다. Launch는 관련 고객 환경을 향상하는 데 필요한 모든 분석, 마케팅 및 광고 태그를 배포하고 관리하는 간단한 방법을 고객에게 제공합니다.
* **[태그 관리자를 사용하지 않고 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)**: 태그 관리자(Adobe Launch 또는 다이내믹 태그 관리)를 사용하지 않고 Target을 구현할 수 있습니다.
* **[다이내믹 태그 관리를 사용하여 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md)**:Adobe의 레거시 태그 관리자인 DTM(다이내믹 태그 관리)을 사용하여 Target을 구현할 수 있습니다. Adobe Launch는 Target 및 at.js 라이브러리를 구현하기 위해 선호되는 최신 방법입니다. 새로운 Target 구현의 경우, Launch를 사용하십시오.
* **타사 태그 관리자를 사용하여 Target 구현**: [Adobe ](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) 실행은 Target 구현에 선호되는 방법입니다.그러나 Tealium, Ensihten, Google Tag 등과 같은 타사 태그 관리자를 사용하여 Target을 구현할 수도 있습니다. Launch 사용에 대한 이점 목록은 [Target 시작 확장](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#section_48B3F938B6F8491DAF798E0DB54EF304)을 사용하여 at.js를 구현하는 이점을 참조하십시오.

   그러나 태그 관리자 없이 Target을 구현하는 방법을 알고 있는 경우 사이트 코드에서 at.js를 하드 코딩하는 대신 타사 태그 관리자로 쉽게 구현할 수 있습니다.

   다음은 제3자 태그 관리자를 사용하여 Target을 구현하는 데 도움이 되는 두 가지 관련 주제입니다.

   * [구현하기 전에](/help/c-implementing-target/c-considerations-before-you-implement-target/considerations-before-you-implement-target.md)
   * [태그 관리자 없이 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)

   자세한 내용은 제3자 태그 관리자의 설명서를 확인하십시오.

SPA(단일 페이지 애플리케이션)를 사용할 때 Target을 구현하려면 [단일 페이지 애플리케이션 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md)을 참조하십시오.