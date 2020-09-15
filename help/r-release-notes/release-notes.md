---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
title: 'Adobe Target 릴리스 노트(현재) '
feature: release notes
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 92f5953a96b92175784600d1b04a23ec4d7152ec
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 24%

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 또한 Target API, SDK, JavaScript 라이브러리(at.js) 및 기타 플랫폼 변경 사항에 대한 릴리스 노트도 포함되어 있습니다(해당되는 경우).

>[!IMPORTANT]
>
>* **Adobe, 개인화 엔진 부문 Gartner Magic Quadrant에서 리더로 선정**:Adobe은 2020년 발표된 3분기 Gartner Magic Quadrant에서 리더로 다시 선정되었습니다. Gartner Magic Quadrant의 개인화 엔진 평가 결과,비전의 완전성과 실행 능력. [Adobe 블로그에서 확인할 수 있습니다](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **mbox.js 사용 중단**:2021년 1월 18일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 1월 18일 이후 mbox.js에서 수행된 모든 호출이 정상적으로 실패하며 기본 컨텐츠를 제공하여 실행 중인 Target 활동이 있는 페이지에 영향을 줍니다. 사이트의 잠재적인 문제를 방지하려면 모든 고객이 이 날짜 전에 at.js 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 At.js 작동 [방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [Adobe Target 스킬 빌더를 참조하십시오.개발자 채팅에서 Adobe Target의 mbox.js를 at.js로 마이그레이션합니다](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
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

## Target Standard/Premium 20.8.3(2020년 9월 15일)

| 기능 | 세부 사항 |
| --- | --- |
| ![자동 Target 활동에 대한 프리미엄 배지](/help/assets/premium.png) Analytics(A4T) 지원 | [!UICONTROL 이제 자동 Target] 활동이 Target에 [대한 분석을 지원합니다](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>이 통합을 통해 [!UICONTROL 자동 Target] 앙상블 머신 러닝 알고리즘을 사용하여 프로필, 동작 및 컨텍스트에 따라 각 방문자에 대해 최상의 경험을 선택할 수 있습니다.<br>A/B 테스트 및 경험 [타깃팅 활동에 사용하기 위해 A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) 를 이미 구현한 경우 모두 설정됩니다.<br>자세한 내용은 [활동 생성에서 자동 할당 및 자동 Target 활동에 대한 Target(A4T) 지원을](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) 참조하십시오 **. |

## Target Standard/Premium 20.8.2(2020년 9월 10일)

| 기능 | 세부 사항 |
| --- | --- |
| ![프리미엄 배지](/help/assets/premium.png) 기준 시퀀스 내의 추천 슬롯 제어 | 이제 기준 시퀀스를 사용하면 각 권장 사항 기준에 의해 수행되는 슬롯 수를 제어할 수 있으므로 다른 유형의 항목이나 다른 알고리즘 논리를 혼합하고 일치시킬 수 있습니다.<br>자세한 내용은 [기준 시퀀스](/help/c-recommendations/c-algorithms/create-criteria-sequence.md#sequence) 만들기를 참조하십시오. |

## Target Standard/Premium 20.8.1(2020년 9월 2일)

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* 조직을 전환한 후 새 [!UICONTROL 관리] 페이지를 로드할 때 오류가 표시되는 문제를 해결했습니다. (TGT-37730)
* 잘못된 클라이언트 코드가 [!UICONTROL 관리 > 구현] 페이지에 표시되던 표시 문제를 수정했습니다. (TGT-37849)
* 때때로 사용자가 VEC를 성공적으로 로드한 후 [!UICONTROL VEC] (Visual Experience Composer)의 편집 기능을 사용할 수 없는 문제를 수정했습니다. (TGT-37162)
* VEC 도우미 확장이 설치되어 있어도 VEC 및 EEC(Enhanced Experience Composer)에서 페이지를 로드할 수 없는 문제를 해결했습니다. 이는 Google Chrome 80+의 변경 때문입니다. 업데이트된 VEC [도우미 확장을 다운로드합니다](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md). (TGT-37893)
* 조직을 전환한 후 때때로 사용자가 [!UICONTROL 관리 > 구현] 페이지에서 at.js를 다운로드할 수 없는 문제를 해결했습니다. (TGT-37668)
* 이제 사용자가 다운로드 단추를 여러 번 클릭하는 경우 여러 요청을 전송할 수 없도록 로드 중에 at.js 다운로드 단추 [!DNL Target] 가 비활성화됩니다. (TGT-37633)
* 장시간 동안 경험이 &quot; [!UICONTROL 결과] &quot;를 표시하는 XT(경험 타깃팅) 활동의 문제를 수정했습니다. (TGT-37684)
* 키보드 전용 사용자를 위한 탐색 및 기능이 개선되었습니다. (TGT-34479 및 TGT-34473)
* 보조 기술을 사용하는 사용자에게 도움이 되는 레이블을 UI에 추가했습니다. (TGT-34480)
* 활동에 현재 사용되는 모바일 뷰포트를 삭제할 때 오류 메시지가 개선되었습니다. 이제 오류 메시지가 표시됩니다.&quot;이 뷰포트는 현재 하나 이상의 활동과 연결되어 있습니다. 삭제하기 전에 해당 활동에서 뷰포트를 제거해야 합니다.&quot; (TGT-37030)
* 페이지에서 둘 이상의 요소와 일치하는 css 선택기에서 클릭 추적을 허용하는 VEC에 지원을 추가했습니다. (TGT-37323)
* 특정 사용자가 [!UICONTROL 활동] 목록을 표시하지 못하는 문제를 해결했습니다. 다음 오류 메시지가 표시되었습니다.&quot;URL제안을 가져올 수 없습니다.&quot; Adobe 백엔드 시스템의 FirstName(FirstName/r/n)에서 캐리지 리턴을 사용하는 사용자에 대해 오류가 발생했습니다. (TGT-37330)
* 작업 공간 이름(Enterprise용 [!UICONTROL Adobe Admin Console에] 지정)에 아포스트로피가 포함되어 있는 경우 사용자가 [!UICONTROL 활동]페이지를 표시할 수 없는 문제를 해결했습니다. (TGT-37709)
* 보고서 세트가 이미 지정된 [!UICONTROL 경우에도 오류 메시지가 사용자에게 보고서 세트를 선택하라고 잘못 알렸던 최적화 및 전환 지표를 선택하는] 동안 자동 할당 활동의 문제를 수정했습니다. (TGT-37689)
* 타깃팅 페이지로 이동한 후 [!UICONTROL 돌아온 후 종종 목표 및 설정] 페이지의 지표가 [!UICONTROL 비어 있는] 문제를 해결했습니다. (TGT-37691)
* 기준에 대해 잘못된 최종 수정 값을 초래했던 문제를 [!DNL Recommendations] 수정했습니다. (TGT-37666)
* mbox 이름 대신 mbox 드롭다운 목록에 mbox ID가 표시되는 문제를 해결했습니다. (TGT-37739)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보 - Target 서버측 API](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Adobe Target의 서버측 API와 관련된 릴리스 노트입니다. |
| [릴리스 노트 - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Adobe Target의 Node.js SDK와 관련된 릴리스 노트입니다. |
| [릴리스 노트 - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Adobe Target의 Java SDK와 관련된 릴리스 노트입니다. |
| [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | at.js JavaScript 라이브러리의 각 버전 변경에 대한 세부 정보 |
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
