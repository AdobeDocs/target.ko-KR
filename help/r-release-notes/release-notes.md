---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
title: 'Adobe Target 릴리스 노트(현재) '
feature: release notes
translation-type: tm+mt
source-git-commit: 9f69e0b58947537abb70f1acbd5400c56c594f11
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 26%

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 노트도 포함되어 있습니다(해당되는 경우).

>[!IMPORTANT]
>
>* **mbox.js 수명**&#x200B;종료:2021년 1월 18일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 1월 18일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 실행 중인 Target 활동이 있는 페이지에 영향을 줍니다. 사이트의 잠재적인 문제를 방지하려면 모든 고객이 이 날짜 전에 at.js 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 At.js 작동 [방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target 스킬 빌더를 참조하십시오.개발자 채팅에서 Adobe Target의 mbox.js를 at.js로 마이그레이션합니다](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   mbox.js는 현재 지원되지만 2017년 7월부터 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외에도 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고, 보안을 향상시키며, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe에서 기대하는 지원을 제공할 수 있습니다.
   >
   >
* **Target 공지**:Target Spuit Builder 세션, 개발자 채팅, 웨비나 및 Target Coffee Break 세션 등 예정된 이벤트에 대한 자세한 내용은 Target 공지 페이지를 참조하십시오. 자세한 내용은 [Target 공지를 참조하십시오](/help/r-release-notes/target-announcements.md).


괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## at.js 2.3.3(2020년 11월 13일)

at.js의 이 릴리스는 유지 관리 릴리스이며 다음 수정 사항이 포함되어 있습니다.

* mbox 클릭 추적 및 A4T 관련 문제를 수정했습니다.

## Target Standard/Premium 20.10.1(2020년 10월 27일)

이 릴리스에는 다음과 같은 새로운 기능이 포함됩니다.

| 기능 | 세부 사항 |
| --- | --- |
| [디바이스 내 의사 결정](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) | 디바이스 내 의사 결정 기능을 사용하면 마케터와 제품 개발자 모두 사용자의 디바이스 내에서, 모든 채널에서 거의 지연 없이 머신 러닝 기반의 개인화를 전달할 수 있습니다.<br>고객 인사이트와 사용자 만족도에 따라 업무 속도와 성능이 중요합니다.<br>장치 내 의사 결정 기능을 사용하면 A/B 테스트 및 경험 타깃팅(XT) 활동 유형의 주요 개인화 및 실험 지침을 CDN을 통해 고객 장치에 로드되는 &quot;최적화 객체:&quot; JSON 객체로 컴파일할 수 있습니다. 또한 디바이스 내 의사 결정은 기본적으로 [!DNL Adobe Experience Cloud] 제품과 연결되므로 [!DNL Target] 사용자는 신속한 분석과 빠른 경험 반복을 경험할 수 있습니다.<br>자세한 내용은 *[Adobe Target SDK 가이드에서](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning)* 장치 내 의사 결정 *소개를 참조하십시오*.<br>**지금 라이브 웨비나에 등록하십시오.** Adobe Target 제품 전문가와 함께 지연 없이 디바이스에서 실행되어야 하는 중요한 경험 최적화 의사 결정이 새로운 활용 사례를 여는 동시에 고객을 위한 사이트 성능을 향상시킬 수 있는 방법을 논의합니다.<ul><li>2020년 11월 10일</li><li>오전 10시 PT / 오후 12시 CT / 오후 1시 ET</li><li>[여기에서 등록](https://www.adobeeventsonline.com/Target/2020/OnDeviceDecisions/invite.html)</li></ul> |

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* 평균 리프트 신뢰 구간 [!UICONTROL 및] 신뢰 [!UICONTROL 가] 전체 [!DNL Auto-Target] 행 [!UICONTROL 에 대한 보고] 에 표시되지 않는 문제를해결했습니다. 모든 개별 경험에 대해 올바로 표시된 측정입니다. (TGT-37301)
* 9월 15일, 오후 2시 30분부터 [!DNL Adobe Target Premium] 사용자의 [!UICONTROL 자동 Target] 보고에 영향을 주는 문제를 수정했습니다.(PDT) - 10월 6일 오전 9시 25분(PDT). 영향을 받은 전환 지표에 대한 보고서를 볼 때(&quot;페이지를[!UICONTROL 보았습니다]&quot; 또는 &quot;mbox에서[!UICONTROL 클릭함]&quot; 옵션을 사용하여 구성됨) 전환율이 잘못 보고됩니다. 현재 알려진 배달 문제가 없습니다. 보고 재동기화 및 수정 방법에 대한 자세한 내용은 알려진 문제 및 해결된 문제 [의](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics) 자동 Target 보고 *를* 참조하십시오 **.
* [ [!UICONTROL 카탈로그 검색] 테이블] 및 [ [!UICONTROL 마지막 업데이트 위치] ] 필터 [!UICONTROL 에 선택 가능한 마지막 업데이트 위치] 열이추가되었습니다. 이 개선 사항은 마지막 업데이트 시기를 확인하기 위해 각 개별 항목을 열 필요가 없으며 항목이 마지막으로 업데이트된 날짜별로 필터링할 수 있으므로 시간과 노력을 절약할 수 있습니다.

   ![마지막 업데이트된 열 및 필터 일러스트레이션](/help/r-release-notes/assets/column-and-filter.png)

* Target UI가 [웹 컨텐츠 액세서빌러티 지침](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0 레벨 A 및 AA 성공 기준(WCAG 2.0 AA)을 준수하도록 하기 위해 업데이트가 수행되었습니다. (TGT-34384 및 TGT-24679)
* CSP(Content Security Policy)가 개선되었습니다. (TGT-37035)
* CNAME을 사용하는 고객을 위한 매개 변수로 클라이언트 코드를 지정하는 방법을 도입했습니다. (TNT-38571)
* [!DNL Adobe Experience Cloud] 설명서를 찾습니다 [!DNL Experience League]. 10월 동안 모든 릴리스 노트, 기사, 비디오 및 자습서는 현재 위치에서 로 이동하게 `docs.adobe.com` 됩니다 [!DNL Experience League]. 이렇게 하면 모든 학습, 자가 도움말, 역량 강화 및 커뮤니티 콘텐츠가 한 곳에서 제공됩니다. 이 변경 사항이 발생하면 모든 링크가 리디렉션되므로 아무 작업도 수행할 필요가 없습니다 [!DNL Experience League]. 교정이 시작되면 릴리스 노트를 업데이트할 예정입니다.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 노트 및 Experience Cloud 릴리스 노트

각 릴리스에 대한 노트 이외에 다음 리소스에서 추가 정보를 제공합니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 노트에 포함되지 않았을 수 있는 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 노트 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하세요.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 노트](/help/r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 노트 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 노트를 표시합니다.<br>자세한 내용은 [Experience Cloud 릴리스 노트를 참조하십시오](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## 사전 릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 목록 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html)에 등록하십시오. |
| 향후 릴리스 노트 | 사전 릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 노트 - 사전 릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
