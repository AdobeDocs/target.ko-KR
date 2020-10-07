---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
title: Adobe Target 프리릴리스 노트
feature: null
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 036b7e07efb0d814a9ec7e398f87371033c77eb8
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 15%

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2020년 10월 7일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시간에 따라 이러한 페이지의 정보가 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!IMPORTANT]
>
>* **Adobe, 개인화 엔진 부문 Gartner Magic Quadrant에서 리더로 선정**:Adobe은 2020년 발표된 3분기 Gartner Magic Quadrant에서 리더로 다시 선정되었습니다. Gartner Magic Quadrant의 개인화 엔진 평가 결과,비전의 완전성과 실행 능력. [Adobe 블로그에서 확인할 수 있습니다](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **mbox.js 수명**&#x200B;종료:2021년 1월 18일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 1월 18일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 실행 중인 Target 활동이 있는 페이지에 영향을 줍니다. 사이트의 잠재적인 문제를 방지하려면 모든 고객이 이 날짜 전에 at.js 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 At.js 작동 [방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target 스킬 빌더를 참조하십시오.개발자 채팅에서 Adobe Target의 mbox.js를 at.js로 마이그레이션합니다](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   mbox.js는 현재 지원되지만 2017년 7월부터 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외에도 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고, 보안을 향상시키며, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe에서 기대하는 지원을 제공할 수 있습니다.
   >
   >
* **Target 공지**:Target Spuit Builder 세션, 개발자 채팅, 웨비나 및 Target Coffee Break 세션 등 예정된 이벤트에 대한 자세한 내용은 Target 공지 페이지를 참조하십시오. 자세한 내용은 [Target 공지를 참조하십시오](/help/r-release-notes/target-announcements.md).


## Target Standard/Premium 20.10.1(2020년 10월 27일)

이 릴리스에는 다음과 같은 새로운 기능이 포함됩니다.

| 기능 | 세부 사항 |
| --- | --- |
| 장치 내 결정 | 디바이스 내 의사 결정을 통해 마케터와 제품 개발자 모두 사용자 디바이스 내에서, 모든 채널에서 거의 지연 없이 머신 러닝 기반의 개인화를 전달할 수 있습니다.<br>고객 인사이트와 사용자 만족도에 따라 업무 속도와 성능이 중요합니다. 디바이스 내 의사 결정을 통해 마케터와 이제 제품 개발자는 사용자 디바이스 내에서 바로 경험을 테스트 및 최적화하여 의사 결정 및 로드 시간을 거의 0으로 줄임으로써 컨텍스트 기반의 실시간 경험을 제공할 수 있습니다.<br>장치 내 의사 결정을 사용하면 모든 개인화 및 실험 지침을 고객 장치에 로드되는 &quot;최적화 객체&quot;에 컴파일할 수 있습니다. 지연 시간이 전혀 없는 이러한 가공물은 마케터에게 1대1 개인화, 행동 리타겟팅, 실시간 제품 및 컨텐츠 권장 사항을 제공하는 한편, 개발자와 제품 소유자는 사용자 경험 테스트, 타겟 및 단계 제품 런칭 시 코드 액세스를 직접 이용하여 실시간으로 개선합니다. 또한 On-device Decision은 기본적으로 제품과 연결되므로 [!DNL Adobe Experience Cloud] [!DNL Target] 사용자는 신속한 분석과 빠른 경험 반복을 경험할 수 있습니다. |

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
