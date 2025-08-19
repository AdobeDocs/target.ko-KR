---
keywords: vec;시각적 경험 작성기; vec;iframe;확장 기능;브라우저
description: '[!UICONTROL Visual Experience Composer]​(VEC)에서 일부 웹 사이트가 안정적으로 열리지 않는 이유를 알아봅니다. VEC Helper 브라우저 확장 프로그램을 사용하면 VEC에서 웹 사이트를 안정적으로 로드할 수 있습니다.'
title: '[!UICONTROL Visual Experience Composer]​(VEC) Helper 확장 프로그램을 사용하려면 어떻게 해야 합니까?'
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: c41580bcbecf2eb2c14f13ce8e66e854c655d059
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 50%

---

# [!UICONTROL Visual Experience Composer] 도우미 확장

[!DNL Adobe Target]용 [!UICONTROL Visual Experience Composer] [!DNL Google Chrome]&#x200B;(VEC) Helper 브라우저 확장 프로그램을 사용하면 VEC에서 웹 사이트를 안정적으로 로드하여 웹 경험을 빠르게 작성 및 QA할 수 있습니다.

VEC Helper 브라우저가 [!DNL Chrome] 확장명입니다. [!DNL Mozilla Firefox]을(를) 사용할 때는 이 확장이 필요하지 않습니다.

>[!IMPORTANT]
>
>* 이 문서에 설명된 레거시 [!DNL Target] VEC Helper 확장 프로그램은 매니페스트 V2를 사용하여 만들어졌습니다. [!DNL Google]이(가) 2024년 6월부터 Manifest V2를 사용하여 만든 확장을 더 이상 허용하지 않는다고 발표했습니다. 자세한 내용은 [개발자용 Chrome](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline){target=_blank} 사이트에서 [!DNL Google]의 *Manifest V2 지원 타임라인 공지*&#x200B;를 참조하십시오.
>
>* 2024년 6월부터 [!DNL Google]은(는) Manifest V2를 사용하여 만든 확장을 비활성화하기 시작합니다. 여기에는 이 항목에 설명된 확장도 포함됩니다. [!DNL Adobe]에서는 가능한 한 빨리 고객이 최신 [Visual Editing Helper 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)(으)로 이동할 것을 권장합니다.

## 일부 웹 사이트가 VEC에서 안정적으로 열리지 않을 수 있는 이유

* 웹 사이트에 엄격한 보안 정책이 있습니다.
* 웹 사이트가 iframe으로 되어 있습니다.
* at.js 라이브러리가 아직 웹 사이트에서 구현되지 않았습니다.
* 고객의 QA 또는 스테이지 사이트는 외부에서 사용할 수 없습니다(사이트는 내부 사이트임).
* VEC를 사용하여 [서비스 작업자](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API){target=_blank}(SW)를 사용하는 웹 사이트를 열고자 하는 경우 현재 몇 가지 제한 사항이 있습니다.

SW는 웹 페이지에서 설치된 도메인에 대한 요청을 가로채는 데 사용할 수 있는 웹 기술입니다. SW는 페이지 방문 후에도 유지되며 이후 방문 시 자동으로 활성화됩니다. SW가 처리할 요청 및 이전되어 캐시에서 대신 처리될 요청을 구분합니다.

SW는 캐싱을 제어할 수 있으며 웹 페이지 자체, JS, CSS, IMG, AJAX 요청과 같은 정적 리소스, 해당 콘텐츠 및 [Target VEC Helper 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)에서 제거를 시도하는 헤더(예: X-Frame-Options: SAMEORIGIN, CSP(콘텐츠 보안 정책) 또는 쿠키 설정)를 포함하는 응답 헤더를 캐시할 수 있습니다.

웹 요청을 가로채는 Chrome 확장 API에서 SW가 가로채고 처리한 요청을 받지 못합니다. 따라서 X-Frame-Options 또는 CSP 헤더도 캐시되었으므로 웹 페이지 요청이 SW에 의해 캐시에서 제공된 경우 확장 프로그램에서 헤더와 쿠키를 수정할 수 없습니다.

잠재적인 해결 방법으로, Chrome 개발자 도구 > 애플리케이션 탭에서 서비스 작업자를 비활성화한 다음 서비스 작업자 섹션에서 &quot;네트워크 우회&quot; 확인란을 활성화할 수 있습니다.

* 향상된 SameSite 쿠키 시행 정책과 함께 Google Chrome 80+를 사용 중입니다. 자세한 내용은 [최근 발표된 Google Chrome SameSite 쿠키 시행 정책이 VEC 및 EEC에 어떤 영향을 미칩니까](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)를 참조하십시오.

Chrome용 VEC Helper 브라우저 확장 프로그램은 고객이 현재 [!DNL Target] [고급 경험 작성기](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) 또는 Requestly와 같은 서드파티 확장 프로그램에 의존하는 사이트 로드 문제를 해결합니다.

## VEC Helper 확장 프로그램 사용의 이점

* X-Frame-Options 및 Content-Security-Policy와 같은 모든 iframe 버스팅 헤더가 웹 사이트에서 암묵적으로 제거됩니다. 더 이상 복잡한 Requestly 규칙을 만들 필요가 없습니다.
* 웹 페이지에 아직 [!DNL Target] at.js JavaScript 라이브러리가 포함되어 있지 않은 경우 확장 프로그램을 사용하여 라이브러리를 주입할 수 있으므로 웹 사이트에 대한 경험을 작성할 수 있습니다. 그런 다음 활동을 만들고 미리 보기 링크를 사용하여 QA를 수행할 수 있습니다.

  EEC(고급 경험 작성기)를 사용하면 확장 기능이 at.js에 삽입되지는 않지만 SameSite 쿠키 기능은 여전히 존재합니다. 웹 페이지에서 at.js를 삽입하려면 EEC를 끕니다.

* [모바일 뷰포트](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md)은(는) [!UICONTROL Enhanced Experience Composer]&#x200B;(EEC) 없이도 지원됩니다.
* [!DNL Target]을 처음 사용하는 고객은 IT 개발자가 아직 웹 사이트에서 [!DNL Target]을 구현하지 않았더라도 확장 기능을 사용하여 [!DNL Target]을 실험해 볼 수 있습니다.
* 이제 여러 고객의 웹 사이트 및 [!DNL Target] 계정을 제공하는 파트너는 타사 도구에서 여러 규칙을 관리하는 대신 VEC 로드를 지원하는 단일 메커니즘을 보유합니다.

## VEC Helper 브라우저 확장 프로그램 받기 및 설치

1. Chrome 웹 스토어의 [Adobe Target VEC Helper 브라우저 확장 프로그램](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak)&#x200B;(으)로 이동합니다.
1. **[!UICONTROL Add to Chrome > Add Extension]** 아이콘을 클릭합니다.
1. [!DNL Target]에서 VEC를 엽니다.
1. 확장 프로그램을 사용하려면 VEC 또는 [QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md)에 있는 동안 Chrome 브라우저의 도구 모음에서 VEC Helper 브라우저 확장 프로그램 아이콘(![VEC Helper 아이콘](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png))을 클릭합니다.
1. (조건부) 웹 페이지에 아직 **[!UICONTROL Inject Target Libraries]** at.js JavaScript 라이브러리가 포함되어 있지 않은 경우 [!DNL Target] 토글을 &quot;켜짐&quot; 위치로 밉니다.

   다음 그림은 [!UICONTROL Inject Target Libraries] 설정이 활성화된 VEC Helper를 보여줍니다.

   ![VEC helper 1](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   다음 그림은 작성을 활성화하기 위해 페이지에 [!DNL Target] 라이브러리를 삽입할 것인지 여부를 묻는 VEC Helper를 보여 줍니다.

   ![VEC helper 2](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (조건부) **[!UICONTROL Cookies]** 토글을 &quot;켜짐&quot; 위치로 밀어 `SameSite=None` 특성 브라우저 수정 사항을 자동으로 추가합니다.

   ![VEC Helper 확장 프로그램에서 쿠키를 전환합니다](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   `SameSite=None` 속성 브라우저 수정 사항에 대한 자세한 내용은 “최근 발표된 Google Chrome SameSite 쿠키 시행 정책이 VEC 및 EEC에 어떤 영향을 미칩니까?”를 참조하십시오. [시각적 경험 작성기 및 고급 경험 작성기 관련 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)에서 참조하십시오.

## 참고

* 확장의 [!UICONTROL Inject Target libraries] 플래그는 기본적으로 꺼져 있습니다. [!DNL Target]용으로 아직 구현되지 않은 사이트에서 VEC를 사용하려는 경우 이 플래그를 활성화할 수 있습니다.

  이 플래그는 전역 설정입니다. VEC에서 연 모든 웹 사이트에 대해 활성화되어 있거나 비활성화되어 있습니다. 따라서, 예를 들어 이 플래그를 &quot;on&quot;으로 설정하고 at.js로 이미 구현된 웹 사이트를 여는 경우 at.js가 이미 로드되었음을 알려주는 메시지가 표시됩니다. Adobe은 대부분의 고객이 페이지에 이미 at.js를 구현하고 기본 설정인 &quot;off&quot;를 사용하고 있을 것으로 예상합니다.

* 확장 프로그램은 [!DNL Target UI]의 [!UICONTROL Administration > Implementation]에서 사용할 수 있는 최신 at.js 버전을 로드합니다.
* [QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md)에서 확장 프로그램을 사용하여 at.js를 주입하는 경우 다른 Chrome 탭이 열려 있어야 합니다. 이 Chrome 탭은 활동을 만든 조직과 동일한 [!DNL Adobe Experience Cloud] 조직으로 인증되어야 합니다.
* 다음 메시지는 사용자에게 계속 정보를 제공하는 데 도움이 됩니다.

   * 로드하지 못하는 VEC를 사용하여 웹 사이트를 로드하려고 하면 VEC Helper 브라우저 확장 프로그램 설치를 제안하는 메시지가 표시됩니다.
   * 웹 사이트에 at.js가 아직 구현되지 않은 경우 확장 프로그램 설치를 제안하는 메시지가 VEC에 표시됩니다.
   * 확장 프로그램이 활성화되어 있고 로드 기능이 켜져 있는 경우 확장 프로그램이 at.js 라이브러리를 주입(필요한 경우)하거나 VEC에서 웹 사이트를 안정적으로 열 때 메시지가 표시됩니다.
