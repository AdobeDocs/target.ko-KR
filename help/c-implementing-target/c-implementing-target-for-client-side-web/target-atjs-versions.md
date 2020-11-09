---
keywords: at.js releases;at.js versions
description: at.js의 각 버전 변경 사항에 대한 세부 사항.
title: at.js 버전 세부 사항
feature: release notes
subtopic: Getting Started
uuid: 3586af55-db15-4e68-90a7-d552338ec5e8
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '3975'
ht-degree: 86%

---


# at.js 버전 세부 사항{#at-js-version-details}을 참조하십시오 

[!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다.

>[!IMPORTANT]
>
>Target 팀은 at.js 1을 모두 지원합니다.*x*&#x200B;와 at.js 2.*x* 간의 매핑에 대해 설명합니다. 지원되는 버전을 실행하고 있는지 확인하려면 at.js의 주요 버전을 최신 버전으로 업그레이드하십시오.
>
>[Adobe Experience Platform Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) 는 at.js로 업그레이드하는 것이 좋습니다. 익스텐션 개발자는 익스텐션에 새로운 기능을 지속적으로 추가하고 버그를 자주 수정할 수 있습니다. 이러한 업데이트는 새로운 버전의 익스텐션으로 패키지되어 카탈로그에서 업그레이드로 사용할 수 [!DNL Launch] 있습니다. 자세한 내용은 [Experience Platform Launch 사용 안내서](https://experienceleague.adobe.com/docs/launch/using/reference/manage-resources/extensions/extension-upgrade.html) 의 익스텐션 업그레이드 *를 참조하십시오*.

## at.js 2.3.2(2020년 7월 24일)

at.js의 이 릴리스는 유지 관리 릴리스이며 다음 수정 사항이 포함되어 있습니다.

* 스크립트나 코드가 창 또는 문서에 기본 속성을 추가할 때의 버그를 수정했습니다.

## at.js 1.8.2(2020년 6월 15일)

at.js의 이 릴리스는 유지 관리 릴리스이며 다음 수정 사항이 포함되어 있습니다.

* at.js 1, CNAME 및 Edge Override 사용 시 발생하는 문제를 수정했습니다.*x* 서버 도메인을 잘못 만들면 요청이 [!DNL Target] 실패할 수 있습니다. (TNT-35064)

## at.js 2.3.1 릴리스(2020년 6월 15일)

at.js 유지 관리 릴리스이며, 다음과 같은 개선 기능 및 수정 사항이 포함되어 있습니다.

* targetGlobalSettings를 통해 `deviceIdLifetime` 설정이 [오버라이드되도록 했습니다](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)
* at.js 2에서 CNAME 및 Edge Override를 사용할 때 발생하는 문제가 해결되었습니다.*x* 서버 도메인을 잘못 만들면 요청이 [!DNL Target] 실패할 수 있습니다. (TNT-35065)
* 확장 v2 및 [!DNL Target] 확장 [!DNL Launch] 을 사용할 때 [!DNL Adobe Analytics] 통화가 [!DNL Launch] 지연되는 문제가 [!DNL Target][!DNL Analytics] `sendBeacon` 수정되었습니다. (TNT-36407, TNT-35990, TNT-3600)

## at.js 버전 2.3.0(2020년 3월 25일)

at.js 유지 관리 릴리스이며, 다음과 같은 개선 기능 및 수정 사항이 포함되어 있습니다.

* 배달된 Target 오퍼을 적용할 때 DOM 페이지에 추가된 SCRIPT 및 STYLE 태그에 대한 Content Security 정책 원본을 설정할 수 있습니다. 고객은 at.js가 적용된 오퍼 `targetGlobalSettings.cspScriptNonce` 에서 해당 스크립트 및 스타일 태그 원본을 설정할 수 있도록 설정 및 `targetGlobalSettings.cspStyleNonce` 설정할 수 있습니다. See  [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) for more details.
* Google 태그 관리자 배포용 Google Closure 컴파일러를 사용하여 at.js를 컴파일할 때 발생하는 문제가 해결되었습니다.
* 고객의 구현과 충돌을 방지하기 위해 at.js 확인 쿠키 `check` 의 이름을 `at_check` 변경할 수 있습니다.

## at.js 버전 1.8.1(2020년 3월 25일)

at.js 유지 관리 릴리스이며, 다음과 같은 개선 기능 및 수정 사항이 포함되어 있습니다.

* 고객의 구현과 충돌을 방지하기 위해 at.js 확인 쿠키 `check` 의 이름을 `at_check` 변경할 수 있습니다.

## at.js 버전 2.2.0(2019년 10월 10일)

at.js의 이번 릴리스에는 다음과 같은 개선 사항 및 수정 사항이 포함되어 있습니다.

* 페이지 요소에 Adobe Analytics 코드가 없을 때 클릭 추적이 Target(A4T)용 Analytics에서 전환을 보고하지 않았던 문제를 수정했습니다.
* 웹 페이지에서 ECID(Experience Cloud ID Service) v4.4와 at.js 2.2를 모두 사용할 때의 성능이 개선되었습니다.
* 이전에는 at.js가 경험을 가져오기 전에 ECID에서 두 개의 차단 호출을 수행했습니다. 이는 단일 호출로 감소하여 성능이 크게 개선되었습니다.

   >[!NOTE]
   >
   >향상된 성능을 활용하려면 ECID Launch Extension을 v4.4로 업그레이드하십시오.

* at.js 버전 2.2에서는 `serverState` 이 설정은 Target의 하이브리드 통합이 구현될 때 페이지 성능을 최적화하는 데 사용할 수 있습니다. 하이브리드 통합이란 클라이언트측에서 at.js v2.2+를 사용하고 서버측에서 제공 API 또는 Target SDK를 모두 사용하여 경험을 전달하는 것을 의미합니다. `serverState` 는 at.js v2.2+를 제공하여 서버 측에서 가져온 컨텐츠에서 직접 경험을 적용하고 제공되는 페이지의 일부로 클라이언트로 돌아오는 기능을 제공합니다. For more information, see &quot;serverState&quot; in [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state).

## at.js 버전 1.8.0(2019년 10월 10일)

at.js의 이번 릴리스에는 다음과 같은 개선 사항 및 수정 사항이 포함되어 있습니다.

* 웹 페이지에서 ECID(Experience Cloud ID Service) v4.4와 at.js 1.8을 모두 사용할 때의 성능이 개선되었습니다.
* 이전에는 at.js가 경험을 가져오기 전에 ECID에서 두 개의 차단 호출을 수행했습니다. 이는 단일 호출로 감소하여 성능이 크게 개선되었습니다.

>[!NOTE]
>
>향상된 성능을 활용하려면 ECID Launch Extension을 v4.4로 업그레이드하십시오.

## at.js 버전 2.1.1(2019년 7월 24일)

at.js 유지 관리 릴리스이며, 다음과 같은 개선 기능 및 수정 사항이 포함되어 있습니다.

(괄호로 묶인 문제 번호는 내부 Adobe용입니다.)

* Visual Experience Composer(VEC)의 목표 및 설정 페이지에서 클릭 추적 지표를 사용할 때 여러 개의 비콘이 실행되는 문제를 해결했습니다. (TNT-32812)
* `triggerView()`이 오퍼를 두 번 이상 렌더링하지 않는 문제를 해결했습니다. (TNT-32780)
* `triggerView()`이 요청에서 MCID(Marketing Cloud ID) 정보가 포함되어 있는지 확인하는 문제를 해결했습니다. (TNT-32776)
* 저장된 보기가 없는 경우에도 `triggerView()` 알림이 실행되지 않는 문제를 해결했습니다. (TNT-32614)
* URL에 잘못된 형식의 쿼리 문자열 매개 변수가 포함되어 있을 때 decodeURIcomponent를 사용하여 오류가 발생하는 문제를 해결했습니다. (TNT-32710)
* 이제 `Navigator.sendBeacon()` API를 통해 전송된 배달 요청의 컨텍스트에서 비콘 플래그가 &#39;true&#39;로 설정됩니다. (TNT-32683)
* 일부 고객의 웹 사이트에서 추천 오퍼가 표시되지 않는 문제를 해결했습니다. 고객이 배달 API 호출에서 오퍼 콘텐츠를 볼 수 있지만 오퍼가 웹 사이트에 적용되지 않았습니다. (TNT-32680)
* 여러 경험에서 클릭 추적이 예상대로 작동되지 않는 문제를 해결했습니다. (TNT-32644)
* 첫 번째 지표 렌더링이 실패한 후 at.js에서 두 번째 지표를 적용하지 못했던 문제를 해결했습니다. (TNT-32628)
* 요청 페이로드가 쿼리 매개 변수 또는 요청 페이로드에 존재하지 않는 `targetPageParams` 함수를 사용하여 `mboxThirdPartyId`을 전달할 때 발생하는 문제를 해결했습니다. (TNT-32613)
* Chromium 기반 브라우저(Google Chrome 포함)에서 디스플레이 및 클릭 알림 응답이 차단되는 문제를 해결했습니다. (TNT-32290)

## at.js 버전 2.1.0(2019년 6월 3일)

이 릴리스에는 다음과 같은 기능 및 개선 사항이 포함되었습니다.

* **Adobe 옵트인(Opt-in) 지원**: Adobe 옵트인(Opt-in)은 동의 관리 플랫폼과 Adobe 솔루션과의 통합을 간소화하는 방법입니다. Adobe 옵트인에 대한 자세한 내용은 [개인 정보 및 GDPR(일반 데이터 보호 규정)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md)을 참조하십시오.

* **업계 표준 CSP 준수**: at.js는 더 이상 eval()을 사용하여 JavaScript를 실행하지 않습니다.

* **클라이언트 측 분석 로깅**: 클라이언트 측이든 아니면 서버측이든 간에 분석 데이터를 Adobe Analytics에 전송하는 방법을 고객이 완벽하게 제어할 수 있도록 합니다.

   자세한 내용은 *구현하기 전에*&#x200B;의 [클라이언트 측 분석 로깅](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side)을 참조하십시오.

* **알림 보내기**: 경험이 `applyOffer()` 또는 `applyOffers()` 대신 코드로 렌더링될 때 개발자가 알림을 전송할 수 있습니다.

   자세한 내용은 [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md)를 참조하십시오.

* **at.js 크기가 24%까지 줄어듦**: at.js의 크기가 24%까지 줄어듭니다. 파일 크기가 작을수록 페이지 로드 성능이 향상되고 페이지의 at.js 다운로드 시간이 줄어듭니다.

## at.js 버전 2.0.1(2019년 3월 19일)

유지 관리 릴리스이며, 다음과 같은 개선 기능 및 수정 사항이 포함되어 있습니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

* 특정 고객에 대해 JavaScript 예외가 발생한 DOM 폴링 코드의 경합 조건을 수정했습니다. (TNT-31869)
* 보기가 렌더링되었다는 알림이 클릭 추적 이벤트 핸들러에서 분리되었습니다. 처음에는 렌더링된 보기에 속하는 클릭 이벤트 핸들러를 첨부할 수 없는 경우 Target에서 알림을 보내지 않았습니다. 이제 Target에서 클릭 요소를 찾을 수 없는 경우에도 보기 알림을 보냅니다. (TNT-31969)
* request-succeeded 이벤트 리디렉션 플래그가 항상 true로 설정되는 문제가 해결되었습니다. (TNT-31907)
* 요소가 누락된 경우에도 VEC 재정렬 작업이 성공으로 기록되는 문제가 해결되었습니다. (TNT-31924)
* 특정 고객에 대한 알림에 엔터프라이즈 권한 속성 토큰이 포함되지 않는 문제가 해결되었습니다. (TNT-31999)

## at.js 버전 1.7.1(2019년 3월 19일)

유지보수 릴리스이며, 다음과 같은 수정 사항이 포함되어 있습니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

* 특정 고객에 대해 JavaScript 예외가 발생한 DOM 폴링 코드의 경합 조건을 수정했습니다. (TNT-31869)

## at.js 버전 2.0.0 {#at-js-200}

at.js 2에서는 차세대 클라이언트측 기술에 대한 개인화를 실행하도록 기업을 지원하는 다양한 기능 세트를 제공합니다. 이 새로운 버전은 단일 페이지 애플리케이션(SPA)과 조화로운 상호 작용을 하도록 at.js를 업그레이드하는 데 주력하고 있습니다.

at.js 2.x를 사용하면 이전 버전에서 사용할 수 없는 다음과 같은 몇 가지 이점이 있습니다.

* 페이지 로드 시 모든 오퍼를 캐시하여 여러 서버 호출을 하나의 서버 호출로 줄일 수 있습니다.
* 오퍼가 기존 서버 호출로 인해 초래되는 지연 없이 캐시를 통해 즉시 표시되므로 사이트에서 최종 사용자의 경험을 크게 향상시킬 수 있습니다.
* 간단한 1줄의 코드 및 일회용 개발자 설정으로 마케터가 단일 페이지 애플리케이션에서 시각적 경험 작성기(VEC)를 통해 A/B 및 경험 타깃팅(XT) 활동을 만들고 실행할 수 있도록 할 수 습니다.

at.js 2.x에서는 다음과 같은 새로운 기능을 도입했습니다.

* getOffers()
* applyOffers()
* triggerView()

다음 함수는 at.js 2.x의 도입으로 더 이상 사용되지 않습니다.

* mboxCreate()
* mboxDefine
* registerExtension()

자세한 내용은 [at.js 1.x에서 at.js 2.x로 업그레이드](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md)와 [at.js 함수](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md)를 참조하십시오.

>[!NOTE]
>
>GDPR([일반 데이터 보호 규정](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md))에 대한 Adobe 옵트인 지원이 필요한 경우 현재 at.js 1.7.0 또는 at.js 2.1.0을 사용해야 합니다.

## at.js 버전 1.7.0 {#at-js-170}

at.js 1.7.0에서는 Adobe 옵트인을 지원합니다. Adobe 옵트인(Opt-in)은 동의 관리 플랫폼과 Adobe 솔루션과의 통합을 간소화하는 방법입니다.

Adobe 옵트인에 대한 자세한 내용은 [개인 정보 보호 및 일반 데이터 보호 규정](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md)(GDPR)을 참조하십시오.

또한 이 릴리스에서는 Target이 리디렉션 URL에서 발생하는 매개 변수로 리디렉션 URL 매개 변수를 무시할 수 있는 문제를 수정합니다.

>[!NOTE]
>
>GDPR에 대한 Adobe 옵트인 지원이 필요한 경우 현재 at.js 1.7.0 또는 2.1.0을 사용해야 합니다.<br>모든 버전의 목록에 대해서는 [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)을 참조하십시오.

## at.js 버전 1.6.4 {#at-js-164}

at.js 1.6.4는 유지보수 릴리스이며 다음 문제를 해결합니다.

* Microsoft Internet Explorer 11에서 중복된 오퍼가 적용되는 경합 조건 매니페스트를 수정했습니다.

## at.js 버전 1.6.3 {#section_484A56774E004282B98FFFF851E4E670}

at.js 버전 1.6.3에는 다음의 수정 사항과 개선 사항이 포함되어 있습니다.

* 이제 선택기는 십진수, 하이픈 두 개 또는 뒤에 십진수가 있는 하이픈(예: #-123)으로 시작하는 ID 또는 CSS 클래스를 포함하는 경우 CSS가 이스케이프 처리됩니다. (TNT-31061)
* 동일한 CSS 선택기에 적용되는 서로 다른 활동의 시각적 경험 작성기(VEC) 오퍼가 활동 우선순위를 준수하지 않는 at.js 1.6.2에서 발생하는 문제를 수정했습니다. (TNT-31052)
* 약속에 대한 기본 지원이 없는 환경에서 약속 시간 제한 관련 문제를 해결했습니다. (TNT-30974)
* 이제 콘텐츠 렌더링 실패 이벤트를 통해 문제가 올바로 캡처되고 보고됩니다. 이전에는 사실이 아님에도 불구하고 JavaScript가 성공적으로 실행된 것으로 보고되었습니다. (TNT-30599)

## at.js 버전 1.6.2 {#section_88BE2F69943D4280B8170F377886B58E}

유지보수 릴리스이며 다음 문제를 해결합니다.

* 일부 고객 사이트에서 무한 &quot;비동기화&quot; 루프가 발생하는 문제를 해결했습니다.

>[!IMPORTANT]
>
>또한 at.js 버전 1.6.2에는 at.js 버전 1.6.1 및 1.6.0에 포함된 모든 개선 사항 및 수정 사항이 포함되어 있으며 이러한 버전은 더 이상 다운로드할 수 없습니다. 1.6.1 또는 1.6.0을 사용하는 경우 버전 1.6.2로 업그레이드하는 것이 좋습니다

다음은 at.js 버전 1.6.1에 포함된 개선 사항 및 수정 사항입니다.

* 권장 사항이 Microsoft Internet Explorer 11에서 복제되도록 하는 at.js 1.6.0 문제가 해결되었습니다. (TNT-30593)
* 이제 at.js는 사용자가 세션 중에 엣지를 변경하는 경우 엣지 오버라이드 로직이 엣지 클러스터 쿠키의 존재 여부를 확인하여 다른 엣지 번호가 발생하지 않도록 합니다. (TNT-30563)
* HTML 콘텐츠에 잘못된 JS 코드가 포함된 경우 at.js가 후속 조치를 실행하지 못하도록 하는 문제가 수정되었습니다. 이제 at.js는 오류를 로그하고 문제 없이 나머지 조치를 렌더링합니다. (TNT-30546)
* .리디렉션 페이지가 리디렉션 활동에 대해 다시 자격을 확보할 때 예외가 발생하도록 변경했습니다. (TNT-30532)
* getOffer() API 요청에서 올바른 요청 제한 시간이 적용되지 않는 문제가 수정되었습니다. (TNT-30498)
* 파일 프로토콜을 사용할 때 at.js 1.6.0이 쿠키를 저장하지 못하도록 하는 문제가 수정되었습니다. (TNT-30454)
* Analytics for Target(A4T)을 사용할 때 일부 경험이 리디렉션과 함께 제공되지 않는 것으로 나타나는 문제가 수정되었습니다. (TNT-30444)
* Target 호출이 성공한 후 페이지가 숨겨지는 문제가 수정되었습니다. (TNT-30358)

다음은 at.js 버전 1.6.0에 포함된 개선 사항 및 수정 사항입니다.

* 이제 리디렉션 오퍼는 Analytics for Target(A4T) 통합에서 자동으로 지원됩니다. 클라이언트 측 임시 해결책이 제거되었습니다. (TNT-30247)
* 이제 클라이언트 측 엣지 라우팅이 기본적으로 사용됩니다. (TNT-30261)
* 동작 간에 종속성이 있을 때 Visual Experience Composer(VEC) 동작 렌더링에 문제가 수정되었습니다. (TNT-30248)

## at.js 버전 1.5.0 {#section_128C6761884C4DA8AE50D6A605FF6F55}

이제 at.js 버전 1.5.0을 사용할 수 있습니다.

* `at-request-succeeded` 이벤트 세부 사항에 리디렉션 플래그가 들어 있습니다. 이 플래그는 페이지가 다른 URL로 리디렉션되는지 여부를 확인하는 데 사용할 수 있습니다. URL을 알아보려면 `at-content-rendering-redirect`에 가입합니다. (TNT-29834)
* false로 설정한 경우 런타임 예외로 인해 `window.targetGlobalSettings.enabled`에 오류가 발생하는 문제가 해결되었습니다. (TNT-29829)
* 글로벌 mbox 요청 실행에 사용자 지정 코드를 사용하고 본문 숨기기를 사용하는 경우 VEC(시각적 경험 작성기)에서 로드하는 동안 페이지에 오류가 발생하는 문제가 해결되었습니다. (TNT-29795)
* `screenOrientation`, `devicePixelRatio` 및 `webGLRenderer`에 대한 지원을 추가했습니다. 이러한 새로운 Target 요청 매개 변수는 iPhone X 및 기타 최신 장치 검색에 사용됩니다. 자세한 내용은 [모바일](/help/c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89)을 참조하십시오. (TNT-29781)
* AAM(Adobe Audience Manager) 위치 힌트가 가끔씩 전송되지 않은 문제가 해결되었습니다. (TNT-29695)
* 이를 지원하는 브라우에서 at.js 1.5.0이 선택기 폴링을 위해 MutationObserver로 전환됩니다. at.js 1.0.0 이전의 버전은 MutationObserver polyfill을 사용했으며, 이는 문제가 있는 것으로 입증되었습니다. polyfill 문제를 방지하기 위해 버전 1.5.0에서 다음 의사 코드를 사용하여 사용할 예약 메커니즘을 결정합니다.

   ```
   if MutationObserver is supported
     scheduler = MutationObserver
   else if document is visible
     scheduler = requestAnimationFrame
   else
     scheduler = setTimeout
   ```

## at.js 버전 1.3.0 {#section_24EAAE1CFA814EF8B19E61842F4D8321}

현재 at.js 버전 1.3.0을 사용할 수 있습니다.

* at.js와의 상호 작용을 추적, 디버깅 및 사용자 지정하는 데 도움이 되도록 다음과 같은 새 이벤트를 사용할 수 있습니다.

   * LIBRARY_LOADED
   * REQUEST_START
   * CONTENT_RENDERING_START
   * CONTENT_RENDERING_NO_OFFERS
   * CONTENT_RENDERING_REDIRECT

   자세한 내용은 [at.js 사용자 지정 이벤트](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md)를 참조하십시오.

* 데이터 공급자에서 가져온 추가 매개 변수로 at.js 요청을 확장할 수 있습니다. 데이터 공급자는 `dataProviders key` 아래의 `window.targetGlobalSettings`에 추가되어야 합니다.

   자세한 내용은 [데이터 공급자](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)를 참조하십시오.

* 이제 at.js 요청은 GET을 사용하지만 URL 크기가 2048자를 초과하면 POST로 전환됩니다. 필요한 경우 크기 제한을 늘릴 수 있는 `urlSizeLimit`라는 새 특성이 있습니다. 이를 통해 Target에서 동일한 기술을 사용하여 AppMeasurement에 맞게 at.js를 조정할 수 있습니다.
* 이제 Target에서는 `adobe.target.applyOffer(options)` 함수의 `mbox` 키를 사용하도록 강제할 수 있습니다. 이 키는 과거에는 필요했지만 현재 Target에서는 이 키를 적용하여 적절한 유효성 검사가 수행되는지와 고객이 함수를 올바르게 사용하고 있는지를 확인합니다.
* at.js의 이벤트 및 클릭 추적 기능이 개선되었습니다. at.js는 `navigator.sendBeacon()`을 사용하여 이벤트 추적 데이터를 전송하고, `navigator.sendBeacon()`이 지원되지 않을 때 동기 XHR로 대체됩니다. 이 대체 항목은 주로 Internet Explorer 10 및 11과 일부 Safari 버전에 영향을 줍니다. Safari는 향후 iOS 11.3 릴리스에서 `navigator.sendBeacon()`을 추가로 지원할 예정입니다.
* 이제 페이지가 백그라운드 탭에서 열릴 때도 at.js가 오퍼를 렌더링할 수 있습니다. 백그라운드 탭의 브라우저 조절 동작으로 인해 `requestAnimationFrame()`이 비활성화될 때 일부 Target 고객에서 문제가 발생합니다.
* 이번 릴리스에서는 Chrome CPU 프로필 검사 시 호출 스택 단축을 비롯하여 여러 가지 성능이 개선되었습니다.
* at.js 1.3.0은 더 이상 Microsoft Internet Explorer 9에서 콘텐츠 전달을 지원하지 않습니다. 지원되는 브라우저 목록에 대해서는 [지원되는 브라우저](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100)를 참조하십시오. 앞으로, 모든 요청은 JSONP 요청 없이 CORS가 지원되는 `XMLHttpRequest`를 통해 실행됩니다. 이 변경 사항은 보안을 크게 향상시킵니다.

## at.js 버전 1.2.3 {#section_CE4D14AF00D04F4C8A2F0513F5EA1A84}

이제 [!DNL at.js] 버전 1.2.3을 사용할 수 있습니다.

* JSON 오퍼에 대한 지원을 추가합니다. JSON은 양식 기반 경험 작성기를 사용하여 만든 활동에서만 지원됩니다. 현재 JSON을 사용하는 유일한 방법은 직접 API 호출을 통해서입니다. 자세한 내용은 [JSON 오퍼 만들기](/help/c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D)를 참조하십시오.

## at.js 버전 1.2.2 {#section_4E96D13F2DFE4F1F81A1089877D53649}

이제 [!DNL at.js] 버전 1.2.2를 사용할 수 있습니다.

* Target 라이브러리가 QUIRKS 모드를 사용하여 페이지에 로드될 때 JavaScript 오류를 반환한 문제가 수정되었습니다. (TNT-28312)
* Target 클릭 추적으로 인해 Analytics 데이터 컬렉션 호출이 중단되는 문제가 수정되었습니다. (TNT-28261)
* `targetPageParams()`가 빈 문자열을 반환하는 경우 `getOffer() params`가 실패하도록 하는 문제가 수정되었습니다. (TNT-28359)
* x-only를 사용할 때 발생하는 세션 ID 생성 관련 문제가 수정되었습니다. (TNT-28361)

## at.js 버전 1.2.1 {#section_F757C8174BBA4F68AC5524ADC3D9C5E3}

이제 [!DNL at.js] 버전 1.2.1을 사용할 수 있습니다.

* target=&quot;_blank&quot;인 링크에 대한 클릭 추적을 수행할 경우 새 탭에서 링크가 열리지 않도록 하는 문제가 수정되었습니다.

## at.js 버전 1.2.0 {#section_1C3A18C595C34B25A14A440D213F3B9C}

이제 [!DNL at.js] 버전 1.2는 대부분의 버그 수정 사항을 포함하는 유지 관리 릴리스로 사용할 수 있습니다.

* 클릭 추적 특수 사례에 대해 기본 동작이 수행되지 않도록 하는 문제가 수정되었습니다. (TNT-28089)
* `target="_blank"`인 링크에 대한 클릭 추적을 수행할 경우 새 탭에서 링크가 열리지 않도록 하는 문제가 수정되었습니다. (TNT-28072)
* IP 주소를 쿠키 도메인으로 사용할 수 있습니다. (TNT-28002)
* 글로벌 mbox 또는 기타 지역 mbox가 있는 리디렉션 오퍼에서 깜박임을 유발하던 문제가 수정되었습니다. (TNT-27978)
* 찾아보기와 작성 간을 전환할 때 VEC 내에서 경험 타깃팅 활동 설정이 실패하는 문제가 수정되었습니다. (TNT-27942)
* 클릭 추적 요소에 대한 깜박임 스타일 클래스의 잘못된 처리가 수정되었습니다. (TNT-27896)
* 전역 mbox 매개 변수가 모든 mbox 매개 변수와 혼합되도록 하는 문제가 수정되었습니다. (TNT-27846)
* Handlebars, Mustache 및 기타 클라이언트 측 템플릿 라이브러리가 [!DNL at.js]에서 제대로 처리되도록 하는 데 필요한 변경이 수행되었습니다. (TNT-27831)
* `sdidParamExpiry`가 제대로 초기화되어 방문자 API로 전달되도록 하는 데 필요한 변경이 수행되었습니다. `at.js 1.1.0`에 추가된 회귀입니다. 이전 [!DNL at.js] 버전은 영향을 받지 않습니다. 리디렉션 오퍼 및 A4T를 사용하는 클라이언트에만 영향을 줍니다. (TNT-27791)
* 사용 중인 형식 속성과 관계없이 `SCRIPT`가 실행되도록 하는 데 필요한 변경이 수행되었습니다. (TNT-27865)

## at.js 버전 1.1.0 {#section_8F494E1EA94E48A9B169F5CF9FE6DC56}

**날짜:** 2017년 8월 2일

다음 개선 사항 및 수정 사항이 [!DNL at.js] 버전 1.1에 포함되어 있습니다.

* 응답 토큰 처리가 추가되었습니다. 자세한 내용은 [응답 토큰](/help/administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4)을 참조하십시오.
* `document.currentScript polyfill`이 Angular 1.X를 방해하지 않도록 문제가 해결되었습니다.
* 클릭 추적이 가시성 속성을 방해하지 않도록 하는 데 필요한 변경이 수행되었습니다. 클릭 추적 요소가 `at-element-click-tracking` 대신 `at-element-marker` CSS 클래스로 표시됩니다.

## at.js 버전 1.0.0 {#section_37A3D23FC4AD42A68AA831B89E03E725}

**날짜:** 2017년 7월 7일

다음 개선 사항 및 수정 사항이 at.js 버전 1.0에 포함되어 있습니다.

* 더 빠른 페이지 로드를 위해 at.js의 비동기식 로드가 지원됩니다.
* at.js를 비동기식으로 로드할 때 사전 숨김 페이지 콘텐츠가 지원됩니다.
* 콘텐츠 전달을 사용하지 않도록 설정할 때 오류 메시지가 개선됩니다.
* 여러 활동을 전달할 때 성능이 향상됩니다.
* YUI Compressor가 지원됩니다.
* 활동 전달 중 사용자 지정 이벤트에 대한 버그/오류가 보고됩니다.
* Microsoft Internet Explorer 11의 성능 문제가 해결되었습니다.
* 일부 웹 사이트에 오류를 발생하는 `getOffer()` 함수가 수정되었습니다.
* Target 라이브러리를 비동기식으로 로드하십시오. 자세한 내용은 [at.js FAQ](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769)를 참조하십시오.

## at.js 버전 0.9.7 {#section_6C7B698BE21E40E495FD2850EFBF3E80}

**날짜:** 2017년 5월 22일

다음 개선 사항 및 수정 사항이 [!DNL at.js] 버전 0.9.7에 포함되어 있습니다.

* VEC(시각적 경험 작성기)에서 `insertAfter` 및`insertBefore` 작업에서 누락된 자산 키와 관련된 문제가 수정되었습니다. 이러한 문제는 시각적 오퍼에서 오퍼 템플릿으로의 마이그레이션과 관련되어 있습니다.

## at.js 버전 0.9.6 {#section_EEFA6413F2F947AD8C4A88128B90245D}

**날짜:** 2017년 4월 13일

다음 개선 사항 및 수정 사항이 [!DNL at.js] 버전 0.9.6에 포함되어 있습니다.

* A4T에 대해 리디렉션 오퍼가 지원됩니다. [!DNL at.js] 버전 0.9.6을 다운로드하여 설치한 후에는 [!DNL Adobe Analytics]를 [!DNL Target]에 대한 보고 소스로 사용하는(A4T) 활동에서 리디렉션 오퍼를 사용할 수 있습니다. [!DNL at.js] 버전 0.9.6 외에, 리디렉션 오퍼 및 A4T를 사용하기 위해 구현이 충족해야 하는 다른 최소 요구 사항도 있습니다. 자세한 내용 및 알고 있어야 하는 추가 중요한 정보는 [리디렉션 오퍼 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905)를 참조하십시오.
* 방문자 API가 페이지에 있고 [!DNL at.js] 설정이 너무 적극적이었던 `visitorApiTimeout` 0.9.6 이전에는 Target에서 [!DNL Target] 요청에 MCID 데이터를 전송하지 않는 상황이 발생할 수 있었습니다. 이로 인해 A4T를 사용할 때 [!DNL Analytics]에서 연결되지 않은 히트 발생과 같은 문제가 나타날 수 있습니다.

   이 동작은 [!DNL at.js]이 1ms로 설정되어 있더라도 Target은 SDID, 추적 서버 및 고객 ID를 수집한 후 Target 요청에 전송하려고 하므로 `visitorApiTimeout` 0.9.6에서 변경되었습니다.

* `selectorsPollingTimeout` 설정이 추가되었습니다. 자세한 내용은 [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)를 참조하십시오.
* `getOffer()`의 응답 형식이 변경되었습니다. 자세한 내용은 [adobe.target.getOffer(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md)를 참조하십시오.
* 지원되지 않는 `<!DOCTYPE>` 선언에 대한 콘솔 로깅이 추가되었습니다.
* 여러 기본 오퍼가 단일 mbox에 전달된 경우 [!DNL Target Classic] 플러그인이 올바르게 적용되지 않던 문제가 수정되었습니다. (TGT-22664)
* mbox 쿠키가 이러한 도메인(예: [!DNL test.no], [!DNL autodrives.ca] 등)에 대해 올바르게 설정되었는지 확인할 수 있게 두 글자로 된 TLD(최상위 수준 도메인)에 대한 쿠키 설정이 향상되었습니다.
* 쿠키를 저장할 때 사용해야 하는 최상위 도메인을 추출하는 알고리즘이 at.js 버전 0.9.6에서 변경되었습니다. 이러한 변경으로 인해 쿠키를 IP를 사용하는 주소에 저장할 수 없습니다. 대부분의 경우 IP 주소는 테스트 용도로 사용되지만, 해결 방법으로 DNS 항목을 사용하거나, 로컬 상자에서 호스트 파일을 조정할 수 있습니다.
* 속성이 정수 대신 문자열 값일 때 이동 및 재정렬 작업 처리 방식이 수정되었습니다.

## at.js 버전 0.9.4 {#section_A15B12F12CD94F07B3F56613A79A815F}

**날짜:** 2017년 1월 19일

* 이제 mbox 이름에는 mbox.js를 사용하는 mbox 이름에 대한 이름 지정 요구 사항과 일치하도록 하기 위해 앰퍼샌드(&amp;)를 비롯한 특수 문자가 포함될 수 있습니다.

   허용 가능한 특수 문자 목록이 필요하면 [at.js 구성](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_2FA0456607D04F82B0539C5BF5309812)을 참조하십시오.

* at.js에서 HTTPS만 사용되는지 또는 페이지 프로토콜을 기준으로 HTTP와 HTTPS 간을 전환할 수 있는지를 나타내는 `secureOnly` 설정이 추가되었습니다. 이 설정은 기본값이 False이고 `targetGlobalSettings`를 통해 대체할 수 있는 고급 설정입니다.
* at.js 버전 0.9.3 및 이전 버전에서 [!UICONTROL 레거시 브라우저 지원] 옵션을 사용할 수 있습니다. 이 옵션은 at.js 버전 0.9.4에서 제거되었습니다.

## at.js 버전 0.9.3 {#section_DF13BC1D7C994AE7A36B81937A699DF4}

**날짜:** 2016년 10월 10일

* at.js 설정에서 레거시 브라우저가 비활성화될 경우 Microsoft Internet Explorer 11에서 mbox가 실행되도록 합니다.
* 다이내믹 원격 오퍼가 실패하는 경우(예를 들어, URL이 올바르지 않고 404 오류를 반환하는 경우) 기본 콘텐츠가 렌더링되도록 합니다.
* DOM에서 VEC 클릭 추적 선택기를 찾을 수 없는 경우 요소가 빠르게 표시되도록 합니다.

## at.js 버전 0.9.2 {#section_148549CBB4F046BAA8F79C79B64EC889}

**날짜:** 2016년 9월 21일

* Device Graph 옵트아웃을 활성화하거나 비활성화하는 `optoutEnabled` 설정이 추가되었습니다. 이 설정이 `true`로 설정되고 방문자가 추적을 옵트아웃한 경우 방문자의 브라우저는 mbox 호출을 수행하지 않습니다. Device Graph는 현재 베타 버전입니다. 이 설정은 기본적으로 `false`로 설정되지만 Device Graph를 사용하는 경우에는 `true`로 설정되어야 합니다. 비슷한 옵션이 mbox.js v61에 포함되어 있습니다.
* 알림 메커니즘에 대한 `CustomEvent` 지원이 추가되었습니다. 이전에는 at.js 이벤트 알림 메커니즘을 `document.addEventListener()`()와 같은 표준 DOM API를 통해 사용할 수 없었습니다. 이제는 `document.addEventListener()`를 사용하여 요청 이벤트 및 콘텐츠 렌더링 이벤트와 같은 at.js 이벤트에 가입할 수 있습니다.
* VEC(시각적 경험 작성기)에서 만든 오퍼와 관련된 문제가 수정되었습니다. 이 릴리스 이전에 Target은 선택기를 숨기고, 모든 선택기가 선택될 때만 숨김을 해제했습니다. at.js 0.9.2 Target은 일치하는 선택기가 확인되면 바로 숨김을 해제합니다.

## at.js 버전 0.9.1 {#section_DAFB99114D604CFB8416C1BC7DEEAEEE}

**날짜:** 2016년 7월 14일

* 서비스의 자체 시간 제한 시간과는 별개인 방문자 ID 서비스에 대한 시간 제한을 at.js에 제공합니다.
* 일부 페이지에서는 at.js를 사용하고 다른 페이지에서는 mbox.js를 사용하여 구현에 영향을 미치던 0.9.0의 문제를 수정합니다.
* Adobe Analytics를 활동의 보고 소스로 사용하는 경우, mbox.js 버전 61 이상 또는 at.js 버전 0.9.1 이상을 사용하는 경우 활동 생성 중에 추적 서버를 지정할 필요가 없습니다. mbox.js 또는 at.js 라이브러리는 자동으로 추적 서버 값을 [!DNL Target]에 보냅니다. 활동을 작성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.

## at.js 버전 0.9.0 {#section_2981CC9792F245389B39BB5B69F84C4E}

**Target 릴리스:** 16.6.1

**날짜:** 2016년 6월 23일

* VEC 오퍼를 사용할 때 발생하는 흰색 화면 문제를 수정합니다. [!DNL at.js]을 사용하는 모든 사용자는 이 새 버전으로 업그레이드해야 합니다.
* 새 `registerExtension` API.

   이 새로운 API는 개발자들이 라이브러리에 대한 확장 프로그램(즉, 플러그인)을 개발하기 위해 [!DNL at.js]에서 사용되는 특정 jQuery 모듈에 액세스할 수 있도록 합니다. 이 변경으로 인해 몇 가지 결과가 나타납니다. 이러한 결과는 다음 기능을 사용하는 사용자에게만 적용됩니다.

   * `getSettings()` API가 제거되었지만 `registerExtension()`을 사용하여 동일한 기능을 사용할 수 있습니다.
   * `getTracking()` API가 제거되었지만 `registerExtension()`을 사용하여 동일한 기능을 사용할 수 있습니다.

   * 기존 확장(예: AngularJS 확장)은 `registerExtension()` 접근 방식을 사용하도록 업데이트해야 합니다.

* at.js 알림 API가 새로 추가되었습니다.

   이 알림 시스템의 목표는 페이지에서 [!DNL at.js]가 수행하는 작업과 문제가 발생하는 경우를 보다 잘 이해할 수 있도록 하는 것입니다. VEC에서 나타나는 일반적인 문제는 IT 릴리스가 페이지를 변경하고, VEC 선택기가 중단되고, 테스트가 더 이상 콘텐츠를 올바르게 배달하지 못하는 것입니다. 이 알림 시스템의 목표는 이 배달 문제를 페이지에 알려서 개발자들이 이 정보에 액세스하고, [!DNL Adobe Analytics]와 같은 시스템에 전달하고, 테스트가 중단된 비즈니스 소유자에게 경고를 보낼 수 있도록 하는 것입니다.

* 새 `targetGlobalSettings()` API 메서드.

   [!DNL Target Standard/Premium UI]에서 또는 REST API를 사용하여 설정을 구성하는 대신, at.js 라이브러리에서 설정을 재정의할 수 있습니다.

## at.js 버전 0.8.0 {#section_E1C7B08EC0494388A022C28A8B8FE807}

**날짜:** 2016년 5월 5일

이것은 [!DNL at.js] 라이브러리의 첫 번째 공식 릴리스입니다.

[!DNL at.js]는 일반적인 웹 구현과 단일 페이지 애플리케이션 둘 다에 맞게 디자인된 새로운 [!DNL Target]용 구현 라이브러리입니다.

[!DNL at.js]는 [!DNL Adobe Target]을 구현할 수 있도록 [!DNL mbox.js]를 대체합니다.

>[!NOTE]
>
>[!DNL at.js]는 [!DNL mbox.js]를 대신하지만 mbox.js는 계속 지원될 예정입니다. 대부분의 사용자에게 [!DNL at.js]는 [!DNL mbox.js]보다 나은 이점을 제공합니다. 이 기회에 [!DNL at.js]를 테스트해 보고 페이지에서 구현을 변경해 보십시오.

여러 가지 이점 중에서 [!DNL at.js]는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 보안을 강화하고, 단일 페이지 애플리케이션에 대해 더 나은 구현 옵션을 제공합니다.

[!DNL at.js]에는 [!DNL target.js]에 포함된 조각도 포함되어 있으므로 더 이상 [!DNL target.js]를 호출할 필요가 없습니다.

[!DNL at.js]를 구현할 때는 다음에 유의하십시오.

* 버전 8 이전의 Internet Explorer 버전은 지원되지 않습니다.
* 비동기식 구현은 [!DNL Test&Target]과 [!DNL SiteCatalyst] 플러그인의 통합과 같은 이전 통합이 작동되지 않을 수 있음을 의미합니다.
* [!DNL Target] 개체 및 메서드를 참조하는 [!DNL mbox.js] 플러그인은 지원되지 않습니다.
* 모든 [!DNL Target] 호출은 XMLHTTPRequest를 통해 수행되고 콘텐츠는 JSON을 통해 반환됩니다.
