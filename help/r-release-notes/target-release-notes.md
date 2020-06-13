---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
title: Adobe Target 프리릴리스 노트
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 25f7ce65f4f9b863ce6ebfe0a7ff8df08e561741
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 17%

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2020년 6월 12일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시간에 따라 이러한 페이지의 정보가 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!NOTE]
>
>* **mbox.js 사용 중단**: 2020년 8월 30일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2020년 8월 30일 이후 mbox.js에서 수행된 모든 호출이 실패하고 Target 활동이 실행되는 페이지에 영향을 줍니다. 사이트의 잠재적인 문제를 방지하려면 모든 고객이 이 날짜 전에 at.js 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 At.js 작동 [방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target 기술 빌더: 개발자 채팅에서 Adobe Target의 mbox.js를 at.js로 마이그레이션합니다](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   mbox.js는 현재 지원되지만 2017년 7월부터 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외에도 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고, 보안을 향상시키며, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe로부터 기대하는 지원을 제공할 수 있습니다.
   >
   >
* **타겟 공지**: Target Spuit Builder 세션, 개발자 채팅, 웨비나, Target Coffee Break 세션 등 예정된 이벤트에 대한 자세한 내용은 Target 공지 페이지를 참조하십시오. 자세한 내용은 [Target 공지를 참조하십시오](/help/r-release-notes/target-announcements.md).


## at.js 1.8.2 및 at.js 2.3.1 릴리스(2020년 6월 15일)

at.js 라이브러리에서 다음과 같은 개선 및 수정 사항이 [!DNL Target] 수행되었습니다.

### at.js 1.8.2

* at.js 1, CNAME 및 Edge Override 사용 시 발생하는 문제를 수정했습니다.*x* 서버 도메인을 잘못 만들면 요청이 [!DNL Target] 실패할 수 있습니다. (TNT-35064)

### at.js 2.3.1

* targetGlobalSettings를 통해 `deviceIdLifetime` 설정이 [오버라이드되도록 했습니다](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)
* at.js 2에서 CNAME 및 Edge Override를 사용할 때 발생하는 문제가 해결되었습니다.*x* 서버 도메인을 잘못 만들면 요청이 [!DNL Target] 실패할 수 있습니다. (TNT-35065)
* 확장 v2 및 [!DNL Target] 확장 [!DNL Launch] 을 사용할 때 [!DNL Adobe Analytics] 통화가 [!DNL Launch] 지연되는 문제가 [!DNL Target][!DNL Analytics] `sendBeacon` 수정되었습니다. (TNT-36407, TNT-35990, TNT-3600)

## Target Standard/Premium 20.5.1(2020년 6월 17일)

| 기능/향상 | 설명 |
| --- | --- |
| Analytics for Target (A4T) 자동 할당 활동 지원 | 6월 릴리스에서는 자동 할당 테스트가 [Target용 Analytics를 지원합니다](/help/c-integrating-target-with-mac/a4t/a4t.md). 이 통합을 사용하면 Adobe Analytics 목표 지표 및/또는 Adobe Analytics 보고 및 분석 기능을 사용하는 동안 자동 할당의 여러 무장 강도적 기능을 사용하여 트래픽을 이기고 탁월한 경험으로 유도할 수 있습니다. A/B 테스트 및 경험 [타깃팅 활동에 사용하기 위해 A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) 를 이미 구현한 경우 모두 설정됩니다. |
| 게시자 역할 | 이 새 역할은 현재 옵저버 역할과 비슷합니다(활동은 볼 수 있지만 만들거나 편집할 수는 없습니다). 그러나 게시자 역할에는 활동을 활성화할 수 있는 추가 권한이 있습니다. |

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
