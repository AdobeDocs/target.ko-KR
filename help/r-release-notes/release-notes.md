---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
title: 'Adobe Target 릴리스 노트(현재) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 8bd08463509e06673bedd0fedf9ee15e46472826
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 30%

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

## at.js 1.8.2 및 at.js 2.3.1 릴리스(2020년 6월 15일)

at.js 라이브러리에서 다음과 같은 개선 및 수정 사항이 [!DNL Target] 수행되었습니다.

| 기능/향상 | 설명 |
| --- | --- |
| at.js 1.8.2 | at.js의 이 릴리스는 유지 관리 릴리스이며 다음 수정 사항이 포함되어 있습니다.<ul><li>at.js 1, CNAME 및 Edge Override 사용 시 발생하는 문제를 수정했습니다.*x* 서버 도메인을 잘못 만들면 요청이 [!DNL Target] 실패할 수 있습니다. (TNT-35064)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |
| at.js 2.3.1 | at.js 유지 관리 릴리스이며, 다음과 같은 개선 기능 및 수정 사항이 포함되어 있습니다.<ul><li>targetGlobalSettings를 통해 `deviceIdLifetime` 설정이 [오버라이드되도록 했습니다](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)</li><li>at.js 2에서 CNAME 및 Edge Override를 사용할 때 발생하는 문제가 해결되었습니다.*x* 서버 도메인을 잘못 만들면 요청이 [!DNL Target] 실패할 수 있습니다. (TNT-35065)</li><li>확장 v2 및 [!DNL Target] 확장 [!DNL Launch] 을 사용할 때 [!DNL Adobe Analytics] 통화가 [!DNL Launch] 지연되는 문제가 [!DNL Target][!DNL Analytics] `sendBeacon` 수정되었습니다. (TNT-36407, TNT-35990, TNT-3600)</li></ul>For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |

## 프로필 배치 상태 API v2 변경 사항(2020년 5월 14일)

5월 20일 릴리스에서는 프로필 배치 상태가 앞으로 행 수준 실패 데이터만 반환합니다(성공 데이터는 반환되지 않음). 실패한 프로필 ID는 앞으로 API에서 반환됩니다.

이전 및 새 API 응답은 다음과 같습니다.

`ProfileBatchStatus Api
http://<<edge>>/m2/<<client>>/profile/batchStatus?batchId=<batchid>`

**현재 다음과 같은 응답을 볼 수 있습니다.**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>1514187733806-729395</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>1573612762055-214017</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

**5월 4일 이후에는 다음과 같은 응답을 하게 됩니다.**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

## Target Standard/Premium 20.4.1(2020년 5월 6일)

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* 대상의 장치 및 브라우저 유형을 잘못 검증했던 문제를 수정했습니다. (TGT-36266)
* 963픽셀 미만의 화면에서 볼 때 보고서 데이터가 표시되지 않는 문제를 해결했습니다. (TGT-36549)
* 자동 개인화 보고서가 올바르게 렌더링되지 않는 문제를 해결했습니다. (TGT-36619)
* Analytics(A4t)에 Target을 사용하는 자동 할당 및 자동 Target 활동에서 호환되지 않는 지표를 선택할 수 있도록 허용하는 문제를 수정했습니다. (TGT-36646)
* VEC(Visual Experience Composer)의 특정 옵션이 올바로 표시되지 않던 문제를 수정했습니다. (TGT-36571)
* 사용자가 단일 경험에서 컨텐츠를 교체한 후 다른 Recommendations 오퍼 미리 보기에 편집된 컨텐츠가 표시되던 Target UI의 문제를 수정했습니다. (TGT-36053 및 TGT-36894)
* 일부 사용자가 Recommendations 카탈로그에서 항목을 삭제하지 못했던 문제를 수정했습니다. (TGT-36455)
* 사용자가 여러 페이지 활동에 대한 Recommendations 기준을 저장하지 못했던 문제를 수정했습니다. (TGT-36249)
* 두 번째 연속 기준을 편집할 때 행동 데이터 소스 라디오 단추가 사라지는 문제를 수정했습니다. (TGT-36796)
* Recommendations 알고리즘이 장시간 동안 &quot;결과 가져오기&quot;를 표시하는 표시 문제를 해결했습니다. (TGT-36550 및 TGT-36551)
* 여러 언어로 번역된 많은 UI 문자열이 업데이트되었습니다.

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
