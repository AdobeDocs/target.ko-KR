---
description: 이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
keywords: 릴리스 노트;사전 릴리스
seo-description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
seo-title: Adobe Target 릴리스 노트 (최신)
solution: Target
title: Target 릴리스 노트(현재)
topic: 권장 사항
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 2588a7c251e58193b969d57f91a7c3f640318fbf

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다.

## 공지

**2019 년 7 월 31 일**

[!UICONTROL 엔터프라이즈 권한을 통해] [!DNL Target] 고객은 단일 조직을 사용할 수 있지만 여러 팀 또는 워크플로우의 작업 영역으로 나눌 수 있습니다. [!UICONTROL 엔터프라이즈 권한] 기능을 사용하면 팀 간의 최적화 프로그램을 효율적으로 확장할 수 있습니다. 이 기능은 [!DNL Target] UI에서 사용할 수 있었지만 관리 API는 2019 [!DNL Target] 년 2 월 릴리스까지는 해당 지원을 받지 못했습니다. Adobe는 통합 계정을 사용하여 조직에서 만든 모든 작업 영역에 액세스할 수 있도록 관리 API를 업데이트했습니다. 따라서 이전에는 관리 API가 기본 작업 영역으로 제한되었지만 2019 년 2 월 업데이트에는 [!UICONTROL 승인자] 액세스 권한이 있는 모든 작업 영역에 대한 액세스가 허용되었습니다.

2019 년 9 월 출시 [!DNL Target] 이후 [!UICONTROL 엔터프라이즈 권한은] 다음과 같은 액세스 제어를 고객에게 제공합니다.

* 통합을 적용할 수 있는 작업 영역을 선택할 수 있습니다.
* Adobe I/O 통합에 역할을 적용할 수 있습니다. [!UICONTROL 승인자], [!UICONTROL 편집자][!UICONTROL 또는 관찰자.]

**조치 필요**: 현재 모든 작업 영역에서 리소스 (활동, 대상, 제안 및 보고) 에 대한 CRUD 작업을 위해 API를 활용하는 고객은 원하는 역할을 가진 모든 작업 영역에 대한 기존 Adobe I/O 통합 액세스 권한을 부여해야 합니다. 9 월 릴리스 이전에는 제품 역할 드롭다운 목록에서 선택한 역할에 관계없이 [!UICONTROL 승인자] 액세스 기능을 사용하여 모든 [!UICONTROL 통합이] 작동되었습니다. 향후 릴리스에서는 원하는 역할을 선택할 수 있습니다.

이 작업은 2019 **년 8 월 중에 수행해야 합니다.** 2019 년 9 월 [!DNL Target] 릴리스 이후 액세스 제어가 활성화되고 현재 설정된 방식으로 기본 작업 영역에 대한 액세스를 관찰할 수 있습니다. 통합 역할을 미리 설정하는 데에는 불리한 결과가 없습니다.

단계별 지침과 자세한 내용은 Adobe I/O 통합 액세스 권한 [부여 및 역할 할당을 참조하십시오](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Mobile VEC SDK iOS 2.1.0 &amp; Android 1.1.1 (2019 년 8 월 7 일)

Mobile VEC SDK의 이번 릴리스에는 다음 개선 사항 및 수정 사항이 포함되어 있습니다.

(괄호로 묶인 문제 번호는 내부 Adobe용입니다.)

* 모바일 장치에서의 시각적 활동 미리 보기에 대한 지원이 추가되었습니다. (TGT-27875)
* Apple Standard 위반이 `UIImagePickerController` 사용으로 인해 발생하는 문제를 수정했습니다.
* Android SDK에서 Gson 종속성을 제거했습니다. (TGT-31710)
* 다른 중복 Gradle 종속성 제거 (tgt -35479)
* 게재 시 배달 오퍼가 재설정되지 않는 문제를 해결했습니다. (TGT-35270)

## Target Standard/Premium 19.7.1(2019년 7월 24일) {#tgt-19-7-1}

이 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

(괄호로 묶인 문제 번호는 내부 Adobe용입니다.)

| 기능/향상 | 설명 |
| --- | --- |
| 모바일 앱 시각적 경험 작성기 | 클릭추적을 위해 설정한 요소를 표시하는 새로운 수정 패널이 모바일 앱 VEC에 표시됩니다. (TGT -31741)<br> 모바일 앱에서 클릭 추적 [설정을 참조하십시오](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md). |
| ![프리미엄 Badgeresa/B](/help/assets/premium.png)<br>테스트 및 경험 타깃팅 (XT) 활동의 사용자 지정 | Recommendations 오퍼 (알고리즘) 상태는 Recommendations 오퍼가 포함된 A/B 테스트 및 XT 활동에 대한 개요 페이지에 표시됩니다. 상태: 결과 준비, 결과 준비 안 됨 및 피드 실패. (TGT-33649)<br>See [Recommendations as an offer](/help/c-recommendations/recommendations-as-an-offer.md#status). |
| Experience Cloud ID (ECID) 라이브러리를 통해 at. js 2.0 +에 대한 도메인 간 추적 지원 | 이전에는 도메인 간 추적이. js 2에서 지원되지 않았습니다.*x*&#x200B;에는 사용할 수 없습니다. 이 릴리스를 통해 at. js 2.0 이상을 사용하는 고객은 이제 ECID 라이브러리를 통한 도메인 간 추적을 활용할 수 있습니다. 크로스 도메인 추적을 수행하려면. js 2.0 이상 버전과 함께 페이지에 ECID 라이브러리를 설치해야 합니다. [Experience Cloud ID Library 4.3.0 +](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) 를 사용해야 합니다.<br>at. js 2. x에서 [도메인 간 추적 지원을 참조하십시오](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#cross-domain). |
| Experience Cloud ID (ECID) 라이브러리 4.3를 통해 Apple의 ITP 2.1 및 ITP 2.2에 대한 Target 지원 | 현재 타깃 고객은 Adobe의 CNAME 인증 프로그램을 활용하여 Apple의 ITP 2.1 및 ITP 2.2를 완화할 수 있습니다.<br>이번 릴리스에서는 Target 이 서버측 쿠키를 활용하여 ITP 2.1 및 ITP 2.2를 완화하는 ECID Library 4.3 과의 매끄러운 통합을 도입했습니다. Target 고객은 Target의 JavaScript 라이브러리와 [함께 ECID Library 4.3 +](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) 를 배포하여 향후 ITP 릴리스를 완화하는 것이 좋습니다. ECID 라이브러리는 브라우저에서 도입된 지속적인 쿠키 정책에 강력한 솔루션을 제공하는 향상된 기능을 지속적으로 출시합니다.<br>[Apple Intelligent Tracking Prevention (ITP) 2. x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)를 참조하십시오. |

**개선 사항, 수정 및 변경 사항**

* 중복 값을 추가할 때 Recommendations 활동의 제외 값이 지워지지 않는 문제를 해결했습니다. (TGT-34996)
* 이제 타깃팅 페이지에서 추천 활동에서 디자인을 제거할 수 있습니다 (3 부분으로 구성된 안내 워크플로우 중 2 단계). 디자인을 제거하려면 두 개 이상의 디자인을 선택해야 합니다. (TGT-35118)
* 일부 고객이 타겟 UI에서 제대로 로드하거나 편집할 수 있도록 사용자 지정 기준 카드가 표시되지 않는 문제를 해결했습니다. (TGT-35170)

## at. js 버전 2.1.1 (2019 년 7 월 24 일)

at. js의 이번 릴리스는 유지 관리 릴리스이며 다음 개선 사항 및 수정 사항을 포함합니다.

(괄호로 묶인 문제 번호는 내부 Adobe용입니다.)

* Visual Experience Composer (VEC) 의 목표 및 설정 페이지에서 클릭 추적 지표를 사용할 때 여러 개의 비콘이 실행되는 문제를 해결했습니다. (TNT-32812)
* 오퍼를 두 번 이상 `triggerView()` 렌더링하지 않는 문제를 해결했습니다. (TNT-32780)
* 요청에 MCID (Marketing Cloud ID) 정보가 들어 있는지 `triggerView()` 확인하는 문제를 해결했습니다. (TNT-32776)
* 저장된 보기가 없는 경우에도 `triggerView()` 알림이 실행되지 않는 문제를 해결했습니다. (TNT-32614)
* URL에 잘못된 형식의 쿼리 문자열 매개 변수가 포함될 때 발생하는 decodeuricomponent 사용 오류로 인해 오류가 발생하던 문제를 수정했습니다. (TNT-32710)
* 이제 API를 통해 전송된 배달 요청의 컨텍스트에서 비콘 플래그가 "true" 로 `Navigator.sendBeacon()` 설정됩니다. (TNT-32683)
* 일부 고객의 웹 사이트에서 Recommendations 오퍼가 표시되지 않는 문제를 해결했습니다. 고객은 배달 API 호출에서 오퍼 컨텐츠를 볼 수 있지만 오퍼는 웹 사이트에 적용되지 않았습니다. (TNT-32680)
* 여러 경험이 걸쳐 클릭추적이 예상대로 작동되지 않는 문제를 해결했습니다. (TNT-32644)
* 첫 번째 지표 렌더링이 실패한 후 at. js에서 두 번째 지표를 적용하지 못했던 문제를 수정했습니다. (TNT-32628)
* 요청 페이로드가 쿼리 `mboxThirdPartyId` 매개 변수 또는 요청 페이로드에서 나타나지 않는 `targetPageParams` 함수를 사용하여 전달할 때의 문제를 해결했습니다. (TNT-32613)
* Chrome 기반 브라우저 (Google Chrome 포함) 에서 디스플레이 및 클릭 알림 응답이 차단되는 문제를 해결했습니다. (TNT-32290)

For information about this and previous versions of at.js, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

## 설명서 변경 내용, 이전 릴리스 노트 및 Experience Cloud 릴리스 노트 {#section_1BC5F5208DA548E9B4344A0836E4B943}

각 릴리스에 대한 노트 이외에 다음 리소스에서 추가 정보를 제공합니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 노트에 포함되지 않았을 수 있는 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 노트 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하세요.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 노트](../r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 노트 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 노트를 표시합니다.<br>자세한 내용은 [Experience Cloud 릴리스 노트를](https://marketing.adobe.com/resources/help/en_US/whatsnew/)참조하십시오. |

## 사전 릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 목록 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html)에 등록하십시오. |
| 향후 릴리스 노트 | 사전 릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 노트 - 사전 릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
