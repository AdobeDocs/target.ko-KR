---
keywords: vec;시각적 경험 작성기; vec;iframe;확장 프로그램;브라우저
description: 일부 웹 사이트가 VEC(시각적 경험 작성기)에서 안정적으로 열리지 않을 수 있는 이유를 알아봅니다. VEC Helper 브라우저 확장 프로그램을 사용하면 VEC에서 웹 사이트를 안정적으로 로드할 수 있습니다.
title: VEC(시각적 경험 작성기) Helper 확장을 사용하려면 어떻게 합니까?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: d3e6ec7fc65bde2c82f830111d40622cd8bc8a4d
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 55%

---

# 시각적 경험 작성기 Helper 확장 프로그램

다음 [!DNL Adobe Target] [!UICONTROL 시각적 경험 작성기] (VEC) Google Chrome용 Helper 브라우저 확장 프로그램을 사용하면 VEC에서 웹 사이트를 안정적으로 로드하여 웹 경험을 빠르게 작성 및 QA할 수 있습니다.

VEC Helper 브라우저는 Chrome 확장입니다. Mozilla Firefox를 사용할 때에는 이 확장이 필요하지 않습니다.

>[!IMPORTANT]
>
>2023년 1월부터 현재 [!DNL Target] Google에서 Manifest V2를 사용하여 확장을 허용하지 않으므로 VEC Helper 확장은 Google Chrome에서 작동하지 않습니다. 에서 웹 사이트를 시각적으로 작성하려면 새 확장을 다운로드하십시오 [!DNL Target] 새해부터 자세한 내용은 [시각적 편집 도우미 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension).

## 일부 웹 사이트가 VEC에서 안정적으로 열리지 않을 수 있는 이유

* 웹 사이트에 엄격한 보안 정책이 있습니다.
* 웹 사이트가 iframe으로 되어 있습니다.
* at.js 라이브러리가 아직 웹 사이트에서 구현되지 않았습니다.
* 고객의 QA 및/또는 스테이지 사이트를 외부 세계(사이트가 내부적임)에서 사용할 수 없습니다.
* VEC를 사용하여 [서비스 작업자](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API){target=_blank}(SW)를 사용하는 웹 사이트를 열고자 하는 경우 현재 몇 가지 제한 사항이 있습니다.

SW는 웹 페이지에서 설치된 도메인에 대한 요청을 가로채는 데 사용할 수 있는 웹 기술입니다. SW는 페이지 방문 후에도 유지되며 이후 방문 시 자동으로 활성화됩니다. SW가 처리할 요청 및 이전되어 캐시에서 대신 처리될 요청을 구분합니다.

SW는 캐싱을 제어할 수 있으며 웹 페이지 자체, JS, CSS, IMG, AJAX 요청과 같은 정적 리소스, 해당 콘텐츠 및 [Target VEC Helper 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)에서 제거를 시도하는 헤더(예: X-Frame-Options: SAMEORIGIN, CSP(콘텐츠 보안 정책) 또는 쿠키 설정)를 포함하는 응답 헤더를 캐시할 수 있습니다.

안타깝게도 웹 요청을 가로채는 Chrome 확장 API는 SW에서 가로채서 처리한 요청을 받지 못합니다. 따라서 X-Frame-Options 또는 CSP 헤더도 캐시되어 있으므로 웹 페이지가 VEC 내에서 로드되지 않으므로 SW에서 웹 페이지 요청이 캐시에서 제공되는 경우 확장에서 헤더와 쿠키를 수정할 수 없습니다.

잠재적인 해결 방법으로 Chrome 개발자 도구 > 애플리케이션 탭에서 서비스 작업자를 비활성화한 다음 서비스 작업자 섹션에서 “네트워크 우회” 확인란을 활성화할 수 있습니다.

* 향상된 SameSite 쿠키 적용 정책에 Google Chrome 80+를 사용하고 있습니다. 자세한 내용은 [최근에 발표된 Google Chrome SameSite 쿠키 적용 정책은 VEC 및 EEC에 어떻게 영향을 줍니까](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

Chrome용 VEC Helper 브라우저 확장 프로그램은 고객이 현재 [!DNL Target] [향상된 경험 작성기](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) 또는 Requestly와 같은 타사 확장.

## VEC Helper 확장 프로그램을 사용하는 이점

* X-Frame-Options 및 Content-Security-Policy와 같은 모든 iframe 버스팅 헤더가 웹 사이트에서 암묵적으로 제거됩니다. 더 이상 복잡한 Requestly 규칙을 만들 필요가 없습니다.
* 웹 페이지에 아직 [!DNL Target] at.js JavaScript 라이브러리가 포함되어 있지 않은 경우 확장 프로그램을 사용하여 라이브러리를 주입할 수 있으므로 웹 사이트에 대한 경험을 작성할 수 있습니다. 그런 다음 활동을 만들고 미리 보기 링크를 사용하여 QA를 수행할 수 있습니다.

   EEC(향상된 경험 작성기)를 사용하면 확장 프로그램이 at.js를 주입하지 않지만 SameSite 쿠키 기능이 여전히 있습니다. 웹 페이지에서 at.js를 주입하려면 EEC를 끕니다.

* [모바일 뷰포트](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) 이 [!UICONTROL 향상된 경험 작성기] (EEC).
* [!DNL Target]을 처음 사용하는 고객은 IT 개발자가 아직 웹 사이트에서 [!DNL Target]을 구현하지 않았더라도 확장 프로그램을 사용하여 [!DNL Target]을 실험해 볼 수 있습니다.
* 이제 여러 고객의 웹 사이트 및 [!DNL Target] 계정을 제공하는 파트너는 타사 도구에서 여러 규칙을 관리하는 대신 VEC 로드를 지원하는 단일 메커니즘을 보유합니다.

## VEC Helper 브라우저 확장 프로그램 받기 및 설치

1. 로 이동합니다 [Chrome 웹 스토어의 Adobe Target VEC Helper 브라우저 확장 프로그램](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. **[!UICONTROL Chrome에 추가 > 확장 프로그램 추가]**&#x200B;를 클릭합니다.
1. 에서 VEC 열기 [!DNL Target].
1. 확장 프로그램을 사용하려면 VEC 또는 [QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md)에 있는 동안 Chrome 브라우저의 도구 모음에서 VEC Helper 브라우저 확장 프로그램 아이콘(![VEC Helper 아이콘](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png))을 클릭합니다.
1. (조건부) **[!UICONTROL Target 라이브러리 삽입]** 웹 페이지에 아직 이 포함되어 있지 않은 경우 &quot;켜기&quot; 위치로 전환합니다. [!DNL Target] at.js JavaScript 라이브러리.

   다음 그림은 [!UICONTROL Target 라이브러리 삽입] 설정이 활성화된 VEC Helper를 보여줍니다.

   ![VEC helper 1](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   다음 그림은 작성을 활성화하기 위해 페이지에 [!DNL Target] 라이브러리를 삽입할 것인지 여부를 묻는 VEC Helper를 보여 줍니다.

   ![VEC helper 2](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (조건부) **[!UICONTROL 쿠키]** &quot;on&quot; 위치로 전환하여 자동으로 추가 `SameSite=None` 속성 브라우저 수정.

   ![쿠키는 VEC helper 확장에서 토글합니다](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   에 대한 자세한 내용은 `SameSite=None` 속성 브라우저 수정 사항: &quot;최근에 발표된 Google Chrome SameSite 쿠키 적용 정책이 VEC 및 EEC에 어떻게 영향을 줍니까?&quot;를 참조하십시오. [시각적 경험 작성기 및 고급 경험 작성기 관련 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)에서 참조하십시오.

## 참고

* 확장 프로그램의 [!UICONTROL Target 라이브러리 주입] 플래그는 기본적으로 꺼져 있습니다. [!DNL Target]용으로 아직 구현되지 않은 사이트에서 VEC를 사용하려는 경우 이 플래그를 활성화할 수 있습니다.

   이 플래그는 글로벌 설정입니다. VEC에서 연 모든 웹 사이트에 대해 활성화되어 있거나 비활성화되어 있습니다. 따라서, 예를 들어, 이 플래그를 &quot;켜짐&quot;으로 설정하고 at.js로 이미 구현된 웹 사이트를 여는 경우 at.js가 이미 로드되었음을 알려주는 메시지가 표시됩니다. Adobe은 대부분의 고객이 이미 페이지에 at.js를 구현하고 기본 설정인 &quot;off&quot;를 사용할 것으로 예측합니다.

* 확장 프로그램은 [!DNL Target UI] in [!UICONTROL 관리 > 구현].
* [QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md)에서 확장 프로그램을 사용하여 at.js를 주입하는 경우 다른 Chrome 탭이 열려 있어야 합니다. 이 Chrome 탭은 활동을 만든 조직과 동일한 [!DNL Adobe Experience Cloud] 조직으로 인증되어야 합니다.
* 다음 메시지는 사용자에게 계속 정보를 제공하는 데 도움이 됩니다.

   * 로드하지 못하는 VEC를 사용하여 웹 사이트를 로드하려고 하면 VEC Helper 브라우저 확장 프로그램 설치를 제안하는 메시지가 표시됩니다.
   * 웹 사이트에 at.js가 아직 구현되지 않은 경우 확장 프로그램 설치를 제안하는 메시지가 VEC에 표시됩니다.
   * 확장 프로그램이 활성화되어 있고 로드 기능이 켜져 있는 경우 확장 프로그램이 at.js 라이브러리를 주입(필요한 경우)하거나 VEC에서 웹 사이트를 안정적으로 열 때 메시지가 표시됩니다.
