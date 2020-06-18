---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
title: 'Adobe Target 릴리스 노트(현재) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: a55aeb18e86a4428187faa5ecba6c66d11feda6d
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 28%

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 노트도 포함되어 있습니다(해당되는 경우).

>[!NOTE]
>
>* **mbox.js 사용 중단**: 2020년 8월 30일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2020년 8월 30일 이후 mbox.js에서 수행된 모든 호출이 실패하고 Target 활동이 실행 중인 페이지에 영향을 줍니다. 사이트의 잠재적인 문제를 방지하려면 모든 고객이 이 날짜 전에 at.js 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 At.js 작동 [방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target 스킬 빌더: 개발자 채팅에서 Adobe Target mbox.js를 at.js로 마이그레이션합니다](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   mbox.js는 현재 지원되지만 2017년 7월부터 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외에도 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고, 보안을 향상시키며, 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe로부터 기대하는 지원을 제공할 수 있습니다.
   >
   >
* **Target 공지**: Target Spuit Builder 세션, 개발자 채팅, 웨비나 및 Target Coffee Break 세션 등 예정된 이벤트에 대한 자세한 내용은 Target 공지 페이지를 참조하십시오. 자세한 내용은 [Target 공지를 참조하십시오](/help/r-release-notes/target-announcements.md).


괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## Target Standard/Premium 20.5.1(2020년 6월 17일)

| 기능/향상 | 설명 |
| --- | --- |
| Analytics for Target (A4T) 자동 할당 [!UICONTROL 활동] 지원 | [!UICONTROL 이제 자동 할당] 활동이 Target에 대한 [Analytics을 지원합니다](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>이 통합을 사용하면 [!UICONTROL Adobe Analytics] 목표 지표 및/또는 [!UICONTROL Adobe Analytics] 보고 및 분석 기능을 사용하는 동시에, 여러 무장 강도 [!UICONTROL 데이터 자동 할당 기능을 사용하여 트래픽이 우승한 경험으로 유도할 수 있습니다] .<br>A/B 테스트 및 경험 [타깃팅 활동에 사용하기 위해 A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) 를 이미 구현한 경우 모두 설정됩니다.<br>자세한 내용은 [활동 생성](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) **&#x200B;시 자동 할당 활동에 대한 Target(A4T) 지원을 위한 Analytics을 참조하십시오. |
| 자동 Target 및 자동화된 개인화 활동을 위한 트래픽 할당 방법에 대한 응답 토큰 | 두 개의 [응답 토큰](/help/administrating-target/response-tokens.md) 이 [!UICONTROL 자동 Target] 및 [!UICONTROL 자동화된 개인화] 활동에 추가되어 방문자가 &quot;제어&quot;나 &quot;타깃팅된&quot; 트래픽에 지정된 결과로 특정 경험을 수신했는지 여부를 결정할 수 있습니다.<ul><li>`experience.trafficAllocationId` 방문자가 &quot;제어&quot; 트래픽에 있는 경험을 수신하면 0을 반환하고 방문자가 &quot;타깃팅된&quot; 트래픽 배포로부터 경험을 받은 경우 1을 반환합니다.</li><li>`experience.trafficAllocationType` 는 &quot;control&quot; 또는 &quot;targeted&quot;를 반환합니다.</li></ul>제어권 및 타깃팅된 트래픽에 대한 자세한 내용은 자동화된 개인화 또는 자동 Target [활동에 대한 컨트롤 선택을 참조하십시오](/help/c-activities/t-automated-personalization/experience-as-control.md). |
| [!UICONTROL 게시자] 역할 | 이 새 역할은 현재 [!UICONTROL 옵저버] 역할과 비슷합니다(활동은 볼 수 있지만 만들거나 편집할 수는 없습니다). 그러나 게시자  역할에는 활동을 활성화할 수 있는 추가 권한이 있습니다.<br>자세한 내용은 다음 문서를 참조하십시오. <ul><li>**Target Standard 사용자**: [사용자](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) 에서 역할 및 권한을 *지정합니다*.</li><li>**Target Premium 사용자**: [6단계: 엔터프라이즈 권한](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) 구성에서 역할 및 권한 *을 지정합니다*.</li></ul> |
| 2020년 6 [!DNL Analysis Workspace]<br>월 25일에 A4T 지원 | [!UICONTROL 이제 Target] (A4T)에 대한 분석이 지원됩니다 [!DNL Analysis Workspace]. Target(A4T)용 [!UICONTROL Analytics 패널을] 사용하면 [!DNL Adobe Target] 활동 및 경험을 분석할 수 [!DNL Analysis Workspace]있습니다.<br>자세한 내용은 [Analytics 도구 안내서의 A4T 보고](/help/c-integrating-target-with-mac/a4t/reporting.md) 의 Analytics에 있는 보고서 *와* Target에 대한 [Analytics(A4T) 패널](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) 에 있는 보고서 *를*&#x200B;참조하십시오. |

### 개선 사항, 수정 사항 및 변경 사항

* &quot;방문자 수&quot; 지표가 &quot;고유 방문자 수&quot; 대신 활동의 정의에 저장되는 문제를 해결했습니다. (TGT-37098)
* 대상 [!DNL Target] 페이지 [!UICONTROL 에서 세로 스크롤 막대가 제대로 작동하지 않는 UI의 문제를] 수정했습니다. (TGT-36968)

## at.js 1.8.2 및 at.js 2.3.1 릴리스(2020년 6월 15일)

at.js 라이브러리에서 다음과 같은 개선 및 수정 사항이 [!DNL Target] 수행되었습니다.

| 기능/향상 | 설명 |
| --- | --- |
| at.js 1.8.2 | at.js의 이 릴리스는 유지 관리 릴리스이며 다음 수정 사항이 포함되어 있습니다.<ul><li>at.js 1, CNAME 및 Edge Override 사용 시 발생하는 문제를 수정했습니다.*x* 서버 도메인을 잘못 만들면 요청이 [!DNL Target] 실패할 수 있습니다. (TNT-35064)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |
| at.js 2.3.1 | at.js 유지 관리 릴리스이며, 다음과 같은 개선 기능 및 수정 사항이 포함되어 있습니다.<ul><li>targetGlobalSettings를 통해 `deviceIdLifetime` 설정이 [오버라이드되도록 했습니다](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)</li><li>at.js 2에서 CNAME 및 Edge Override를 사용할 때 발생하는 문제가 해결되었습니다.*x* 서버 도메인을 잘못 만들면 요청이 [!DNL Target] 실패할 수 있습니다. (TNT-35065)</li><li>확장 v2 및 [!DNL Target] 확장 [!DNL Launch] 을 사용할 때 [!DNL Adobe Analytics] 통화가 [!DNL Launch] 지연되는 문제가 [!DNL Target][!DNL Analytics] `sendBeacon` 수정되었습니다. (TNT-36407, TNT-35990, TNT-3600)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보 - Target 서버측 API](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Adobe Target 서버측 API와 관련된 릴리스 노트입니다. |
| [릴리스 노트 - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Adobe Target Node.js SDK와 관련된 릴리스 노트입니다. |
| [릴리스 노트 - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Adobe Target Java SDK와 관련된 릴리스 노트입니다. |
| [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | at.js JavaScript 라이브러리의 각 Adobe Target 버전에 대한 변경 사항에 대한 세부 정보 |
| [mbox.js 버전 세부 정보](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | 이 페이지에는 각 mbox.js 버전에 대한 변경 사항이 표시됩니다.<br>mbox.js 라이브러리가 더 이상 개발되지 않습니다. 모든 고객은 mbox.js에서 at.js로 마이그레이션해야 합니다. |

## 설명서 변경 내용, 이전 릴리스 노트 및 Experience Cloud 릴리스 노트 {#section_1BC5F5208DA548E9B4344A0836E4B943}

각 릴리스에 대한 노트 이외에 다음 리소스에서 추가 정보를 제공합니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 노트에 포함되지 않았을 수 있는 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 노트 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하세요.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 노트](../r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 노트 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 노트를 표시합니다.<br>자세한 내용은 [Experience Cloud 릴리스 노트를 참조하십시오](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## 사전 릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 목록 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html)에 등록하십시오. |
| 향후 릴리스 노트 | 사전 릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 노트 - 사전 릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
