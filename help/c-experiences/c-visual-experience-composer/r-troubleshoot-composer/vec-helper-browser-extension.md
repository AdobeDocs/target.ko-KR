---
keywords: vec;visual experience composer; vec;iframe;extension;browser
description: Adobe VEC(시각적 경험 작성기) Helper 브라우저 확장 프로그램을 사용하여 VEC에서 웹 사이트를 안정적으로 로드함으로써 경험을 빠르게 작성 및 QA하기 위한 정보입니다.
title: Adobe Target VEC(시각적 경험 작성기) Helper 확장 프로그램
feature: vec
topic: Standard
translation-type: tm+mt
source-git-commit: ee618961faa12a7352aaf9ed1d869f9e5ab39cdd
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 59%

---


# 시각적 경험 작성기 Helper 확장 프로그램

The [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) Helper browser extension for Google Chrome lets you load websites reliably within the VEC to rapidly author and QA web experiences.

일부 웹 사이트가 VEC에서 안정적으로 열리지 않을 수 있는 이유:

* 웹 사이트에 엄격한 보안 정책이 있습니다.
* 웹 사이트가 iframe으로 되어 있습니다.
* at.js 라이브러리가 아직 웹 사이트에서 구현되지 않았습니다.
* 고객의 QA 및/또는 스테이지 사이트를 외부 세계(사이트가 내부적임)에서 사용할 수 없습니다.
* 향상된 SameSite 쿠키 실행 정책과 함께 Google Chrome 80+을 사용하고 있습니다. 자세한 내용은 최근 발표된 Google [Chrome SameSite 쿠키 집행 정책이 VEC 및 EEC에 어떤 영향을 줍니까](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

The VEC Helper browser extension for Chrome solves site-loading issues for which customers now rely on the [!DNL Target] [Enhanced Experience Composer](/help/administrating-target/visual-experience-composer-set-up.md#eec) or third-party extensions, such as Requestly.

VEC Helper 확장 프로그램을 사용하는 이점:

* X-Frame-Options 및 Content-Security-Policy와 같은 모든 iframe 버스팅 헤더가 웹 사이트에서 암묵적으로 제거됩니다. 이를 수행하기 위해 더 이상 복잡한 Requestly 규칙을 만들 필요가 없습니다.
* 웹 페이지에 아직 [!DNL Target] at.js JavaScript 라이브러리가 포함되어 있지 않은 경우 확장 프로그램을 사용하여 라이브러리를 주입할 수 있으므로 웹 사이트에 대한 경험을 작성할 수 있습니다. 그런 다음 활동을 만들고 미리 보기 링크를 사용하여 QA를 수행할 수 있습니다.
* [모바일 뷰포트는](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md) EEC( [!UICONTROL Enhanced Experience Composer] )가 없어도 지원됩니다.
* [!DNL Target]을 처음 사용하는 고객은 IT 개발자가 아직 웹 사이트에서 [!DNL Target]을 구현하지 않았더라도 확장 프로그램을 사용하여 [!DNL Target]을 실험해 볼 수 있습니다.
* 이제 여러 고객의 웹 사이트 및 [!DNL Target] 계정을 제공하는 파트너는 타사 도구에서 여러 규칙을 관리하는 대신 VEC 로드를 지원하는 단일 메커니즘을 보유합니다.

## VEC Helper 브라우저 확장 프로그램 받기 및 설치

1. Navigate to the [Adobe Target VEC Helper browser extension in the Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. **[!UICONTROL Chrome에 추가 > 확장 프로그램 추가]**&#x200B;를 클릭합니다.
1. VEC를 엽니다 [!DNL Target].
1. 확장 프로그램을 사용하려면 VEC 또는 [QA 모드](/help/c-activities/c-activity-qa/activity-qa.md)에 있는 동안 Chrome 브라우저의 도구 모음에서 VEC Helper 브라우저 확장 프로그램 아이콘(![VEC Helper 아이콘](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png))을 클릭합니다.
1. (조건부) 웹 페이지에 아직 at.js JavaScript 라이브러리가 포함되어 있지 않으면 **[!UICONTROL 삽입 Target]** 라이브러리를 &quot;설정&quot; 위치로 [!DNL Target] 전환합니다.

   다음 그림은 [!UICONTROL Target 라이브러리 삽입] 설정이 활성화된 VEC Helper를 보여줍니다.

   ![VEC helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   다음 그림은 작성을 활성화하기 위해 페이지에 [!DNL Target] 라이브러리를 삽입할 것인지 여부를 묻는 VEC Helper를 보여 줍니다.

   ![VEC helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (조건부) **[!UICONTROL 쿠키]** 토글을 &quot;설정&quot; 위치로 밀어서 SameSite=None 속성 브라우저 수정 사항을 자동으로 추가한 다음 쿠키 이름과 도메인을 지정합니다.

   ![VEC 도우미 확장에서 쿠키 전환](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   다음 링크에서는 추가 정보를 제공합니다.

   * SameSite=None 속성 브라우저 수정 사항에 대한 자세한 내용은 &quot;최근에 발표된 Google Chrome SameSite 쿠키 실행 정책이 VEC 및 EEC에 어떤 영향을 줍니까?&quot;를 참조하십시오. in [Troubleshooting Issues Related to the Visual Experience Composer and Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

   * 쿠키 이름은 &quot;mbox&quot;이고 쿠키 도메인은 mbox를 제공하는 도메인의 두 번째 및 최상위 수준입니다. 회사 도메인에서 제공되기 때문에 쿠키는 자사 쿠키입니다. 예: `mycompany.com`. 자세한 내용은 [Experience Cloud 인터페이스 사용자 안내서의](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-target.html) Adobe Target 쿠키를 *참조하십시오*.

## 참고

* 구현 시 [!DNL Target]at.js 라이브러리를 사용해야 합니다. 확장 프로그램에 mbox.js 구현을 사용할 수는 없습니다.
* 확장 프로그램의 [!UICONTROL Target 라이브러리 주입] 플래그는 기본적으로 꺼져 있습니다. [!DNL Target]용으로 아직 구현되지 않은 사이트에서 VEC를 사용하려는 경우 이 플래그를 활성화할 수 있습니다.

   이 플래그는 글로벌 설정이며, VEC에서 연 모든 웹 사이트에 대해 활성화되어 있거나 비활성화되어 있습니다. 예를 들어, 이 플래그를 &quot;설정&quot;으로 설정하고 at.js로 이미 구현된 웹 사이트를 열면 at.js가 이미 로드되었음을 알리는 메시지가 표시됩니다. 대부분의 고객은 이미 at.js를 자신의 페이지에 구현했으며 기본 설정인 &quot;off&quot;를 사용할 것으로 예상됩니다.

* The extension loads the latest version of at.js that is available from the [!DNL Target UI] in [!UICONTROL Administration > Implementation].
* [QA 모드](/help/c-activities/c-activity-qa/activity-qa.md)에서 확장 프로그램을 사용하여 at.js를 주입하는 경우 다른 Chrome 탭이 열려 있어야 합니다. 이 Chrome 탭은 활동을 만든 조직과 동일한 [!DNL Adobe Experience Cloud] 조직으로 인증되어야 합니다.
* 다음 메시지는 사용자에게 계속 정보를 제공하는 데 도움이 됩니다.

   * 로드하지 못하는 VEC를 사용하여 웹 사이트를 로드하려고 하면 VEC Helper 브라우저 확장 프로그램 설치를 제안하는 메시지가 표시됩니다.
   * 웹 사이트에 at.js가 아직 구현되지 않은 경우 확장 프로그램 설치를 제안하는 메시지가 VEC에 표시됩니다.
   * 확장 프로그램이 활성화되어 있고 로드 기능이 켜져 있는 경우 확장 프로그램이 at.js 라이브러리를 주입(필요한 경우)하거나 VEC에서 웹 사이트를 안정적으로 열 때 메시지가 표시됩니다.

