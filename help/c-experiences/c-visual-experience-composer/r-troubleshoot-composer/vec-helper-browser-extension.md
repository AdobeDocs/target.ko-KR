---
description: VEC(시각적 경험 작성기) Helper 브라우저 확장 프로그램을 사용하여 VEC에서 웹 사이트를 안정적으로 로드함으로써 경험을 빠르게 작성 및 QA하기 위한 정보입니다.
keywords: vec;시각적 경험 작성기; vec;iframe;확장 프로그램;브라우저
seo-description: Adobe VEC(시각적 경험 작성기) Helper 브라우저 확장 프로그램을 사용하여 VEC에서 웹 사이트를 안정적으로 로드함으로써 경험을 빠르게 작성 및 QA하기 위한 정보입니다.
seo-title: Adobe Target VEC(시각적 경험 작성기) Helper 확장 프로그램
solution: Target
title: 시각적 경험 작성기 Helper 확장 프로그램
topic: Standard
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 시각적 경험 작성기 Helper 확장 프로그램

Google Chrome용 [!DNL Adobe Target] VEC(시각적 경험 작성기) Helper 브라우저 확장 프로그램을 사용하면 VEC에서 웹 사이트를 안정적으로 로드하여 웹 경험을 빠르게 작성 및 QA할 수 있습니다.

일부 웹 사이트가 VEC에서 안정적으로 열리지 않을 수 있는 이유:

* 웹 사이트에 엄격한 보안 정책이 있습니다.
* 웹 사이트가 iframe으로 되어 있습니다.
* at.js 라이브러리가 아직 웹 사이트에서 구현되지 않았습니다.
* 고객의 QA 및/또는 스테이지 사이트를 외부 세계(사이트가 내부적임)에서 사용할 수 없습니다.

Chrome용 VEC Helper 브라우저 확장 프로그램은 고객이 현재 [!DNL Target][!UICONTROL 고급 경험 작성기]나, Requestly와 같은 확장 프로그램에 의존하고 있는 사이트 로딩 문제를 해결합니다.

VEC Helper 확장 프로그램을 사용하는 이점:

* X-Frame-Options 및 Content-Security-Policy와 같은 모든 iframe 버스팅 헤더가 웹 사이트에서 암묵적으로 제거됩니다. 이를 수행하기 위해 더 이상 복잡한 Requestly 규칙을 만들 필요가 없습니다.
* 웹 페이지에 아직 [!DNL Target] at.js JavaScript 라이브러리가 포함되어 있지 않은 경우 확장 프로그램을 사용하여 라이브러리를 주입할 수 있으므로 웹 사이트에 대한 경험을 작성할 수 있습니다. 그런 다음 활동을 만들고 미리 보기 링크를 사용하여 QA를 수행할 수 있습니다.
* 모바일 뷰포트는 [!UICONTROL 고급 경험 작성기] (EEC) 없이도 지원됩니다.
* [!DNL Target]을 처음 사용하는 고객은 IT 개발자가 아직 웹 사이트에서 [!DNL Target]을 구현하지 않았더라도 확장 프로그램을 사용하여 [!DNL Target]을 실험해 볼 수 있습니다.
* 이제 여러 고객의 웹 사이트 및 [!DNL Target] 계정을 제공하는 파트너는 타사 도구에서 여러 규칙을 관리하는 대신 VEC 로드를 지원하는 단일 메커니즘을 보유합니다.

## VEC Helper 브라우저 확장 프로그램 받기 및 설치

1. Chrome 웹 저장소에서 [Adobe Target VEC Helper Browser Extension로 이동합니다](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. [!UICONTROL Chrome에 추가 &gt; 확장 프로그램 추가]를 클릭합니다.
1. 확장 프로그램을 사용하려면 VEC 또는 [QA 모드](/help/c-activities/c-activity-qa/activity-qa.md)에 있는 동안 Chrome 브라우저의 도구 모음에서 VEC Helper 브라우저 확장 프로그램 아이콘(![VEC Helper 아이콘](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png))을 클릭합니다.

다음 그림은 타겟 라이브러리 [!UICONTROL 주입] 설정이 활성화된 VEC 헬퍼를 보여 줍니다.

![VEC Helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

다음 그림에서는 작성을 활성화하기 위해 페이지에서 라이브러리를 주입할 [!DNL Target] 것인지 여부를 묻는 VEC 헬퍼를 보여 줍니다.

![VEC Helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

## 참고

* 구현 시 [!DNL Target]at.js 라이브러리를 사용해야 합니다. 확장 프로그램에 mbox.js 구현을 사용할 수는 없습니다.
* 확장 프로그램의 [!UICONTROL Target 라이브러리 주입] 플래그는 기본적으로 꺼져 있습니다. [!DNL Target]용으로 아직 구현되지 않은 사이트에서 VEC를 사용하려는 경우 이 플래그를 활성화할 수 있습니다.

   이 플래그는 글로벌 설정이며, VEC에서 연 모든 웹 사이트에 대해 활성화되어 있거나 비활성화되어 있습니다. 따라서, 예를 들어, 이 플래그를 [켜짐]으로 설정하고 at.js로 이미 구현된 웹 사이트를 여는 경우 at.js가 이미 로드되었음을 알려주는 메시지가 표시됩니다. 대부분의 고객은 페이지에 이미 at.js를 구현하고 기본 설정인 [꺼짐]을 사용할 것으로 예상됩니다.

* 확장 프로그램은 [!UICONTROL 설정 &gt; 구현]을 통해 [!DNL Target UI]에서 사용할 수 있는 최신 at.js 버전을 로드합니다.
* [QA 모드](/help/c-activities/c-activity-qa/activity-qa.md)에서 확장 프로그램을 사용하여 at.js를 주입하는 경우 다른 Chrome 탭이 열려 있어야 합니다. 이 Chrome 탭은 활동을 만든 조직과 동일한 [!DNL Adobe Experience Cloud] 조직으로 인증되어야 합니다.
* 다음 메시지는 사용자에게 계속 정보를 제공하는 데 도움이 됩니다.

   * 로드하지 못하는 VEC를 사용하여 웹 사이트를 로드하려고 하면 VEC Helper 브라우저 확장 프로그램 설치를 제안하는 메시지가 표시됩니다.
   * 웹 사이트에 at.js가 아직 구현되지 않은 경우 확장 프로그램 설치를 제안하는 메시지가 VEC에 표시됩니다.
   * 확장 프로그램이 활성화되어 있고 로드 기능이 켜져 있는 경우 확장 프로그램이 at.js 라이브러리를 주입(필요한 경우)하거나 VEC에서 웹 사이트를 안정적으로 열 때 메시지가 표시됩니다.
