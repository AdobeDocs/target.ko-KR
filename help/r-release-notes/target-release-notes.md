---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
title: Adobe Target 프리릴리스 노트
feature: null
translation-type: tm+mt
source-git-commit: f4091506538cd4719302227b88fa11e9d4ae93a6
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 10%

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2020년 10월 27일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시기에 따라 이러한 페이지의 정보가 같을 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!IMPORTANT]
>
>* **Gartner Magic Quadrant에서 개인화 엔진** 부문 리더로 Adobe 재선정:Adobe은 2020년 발표된 3분기 Gartner Magic Quadrant에서 리더로 다시 선정되었습니다. Gartner Magic Quadrant의 개인화 엔진 조사 결과 15개 부문에서 벤더를 평가했으며, 그 기준은 2개였습니다.비전의 완전성과 실행의 능력. [Adobe 블로그에서 이 정보를 참조하십시오](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **mbox.js 수명 종료**:2021년 1월 18일부터 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 1월 18일 이후, mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 실행 중인 Target 활동이 있는 페이지에 영향을 줍니다. 모든 고객은 사이트에서 발생할 수 있는 문제를 방지하기 위해 이 날짜 이전에 at.js 라이브러리의 최신 버전으로 전환하는 것이 좋습니다. 자세한 내용은 [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target Skill Builder:개발자 채팅, Adobe Target의 mbox.js를 at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true)로 마이그레이션합니다.
   >
   >   
   mbox.js는 현재 지원되지만 2017년 7월부터 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 다른 이점 중에서도 at.js는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 보안을 강화하고, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe에서 기대하는 지원을 제공할 수 있습니다.
   >
   >
* **Target 공지**:Target 스킬 빌더 세션, 개발자 채팅, 웨비나 및 Target Coffee Break 세션을 비롯한 예정된 이벤트에 대한 자세한 내용은 Target 공지 페이지를 참조하십시오. 자세한 내용은 [Target 공지](/help/r-release-notes/target-announcements.md)를 참조하십시오.


## Target Standard/Premium 20.10.1(2020년 10월 27일)

이 릴리스에는 다음과 같은 새로운 기능이 포함됩니다.

| 기능 | 세부 사항 |
| --- | --- |
| [디바이스에서 의사 결정](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) | 디바이스 내 의사 결정을 통해 마케터와 제품 개발자 모두 디바이스 내에서 거의 지연 없이 모든 채널에서 실험을 바탕으로 머신 러닝 기반의 개인화를 전달할 수 있습니다.<br>고객 인사이트와 사용자 만족도에서 속도와 성능이 중요합니다.<br>장치 내 의사 결정을 사용하면 A/B 테스트 및 경험 타깃팅(XT) 활동 유형의 주요 개인화 및 실험 지침을 CDN을 통해 고객 장치에 로드되는 &quot;최적화 객체:&quot; JSON 객체로 컴파일할 수 있습니다. 또한 디바이스에서 의사 결정은 기본적으로 [!DNL Adobe Experience Cloud] 제품과 연결되므로 [!DNL Target] 사용자는 신속한 분석과 빠른 경험 반복을 경험할 수 있습니다.<br>자세한 내용은 *장치 [내 의사 결정을 참조하십시오](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md). |

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* [!UICONTROL Total] 행에 대해 [!DNL Auto-Target]보고 시 [!UICONTROL 평균 리프트 신뢰 구간] 및 [!UICONTROL 신뢰]이 표시되지 않는 문제를 해결했습니다. 모든 개별 경험에 대해 올바로 표시되는 측정입니다. (TGT-37301)
* 9월 15일, 오후 2:30부터 [!DNL Adobe Target Premium] 사용자의 [!UICONTROL 자동 Target] 보고에 영향을 주는 문제를 수정했습니다.(PDT) - 10월 6일 오전 9시 25분(PDT). 영향을 받은 전환 지표에 대한 보고서를 볼 때(&quot;[!UICONTROL 페이지] 보기&quot; 또는 &quot;[!UICONTROL mbox]&quot; 옵션을 클릭함) 전환율이 잘못 보고됩니다. 현재 알려진 배달 문제가 없습니다. 보고를 다시 동기화하고 수정하는 방법에 대한 자세한 내용은 *알려진 문제 및 해결된 문제*&#x200B;의 *해결된 문제*&#x200B;에서 [자동 Target 보고](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics)를 참조하십시오.
* [!UICONTROL 카탈로그 검색] 테이블 및 [!UICONTROL 마지막 업데이트 위치] 필터에 선택 가능한 [!UICONTROL 마지막 업데이트 위치&lt;a1/> 열이 추가되었습니다. ] 이 개선 사항은 각 개별 항목이 마지막으로 업데이트된 시기를 확인하기 위해 열 필요가 없고 항목이 마지막으로 업데이트된 날짜별로 필터링할 수 있으므로 시간과 노력을 절약할 수 있습니다.

   ![마지막 업데이트된 열 및 필터 일러스트레이션](/help/r-release-notes/assets/column-and-filter.png)

* Target UI가 [웹 컨텐츠 접근성 지침](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0 레벨 A 및 AA 성공 기준(WCAG 2.0 AA)을 준수하도록 하기 위해 업데이트가 수행되었습니다. (TGT-34384 및 TGT-24679)
* CSP(Content Security Policy)가 개선되었습니다. (TGT-37035)
* CNAME을 사용하는 고객을 위한 매개 변수로 클라이언트 코드를 지정하는 방법을 도입했습니다. (TNT-38571)
* [!DNL Adobe Experience Cloud] 설명서는 다음으로  [!DNL Experience League]이동합니다. 10월 중에 모든 릴리스 노트, 기사, 비디오 및 자습서가 현재 위치 `docs.adobe.com`에서 [!DNL Experience League]로 이동합니다. 이렇게 하면 모든 학습, 자가 도움말, 지원 및 커뮤니티 콘텐츠를 한 곳에서 제공할 수 있습니다. 이 변경 사항이 발생하면 모든 링크가 [!DNL Experience League]으로 리디렉션되므로 필요한 작업이 없습니다. 컷오버가 시작되면 릴리스 노트를 업데이트합니다.

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
