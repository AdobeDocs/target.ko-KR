---
keywords: vec;시각적 경험 작성기; vec;iframe;확장 프로그램;브라우저
description: 일부 웹 사이트가 [!UICONTROL 시각적 경험 작성기] (VEC). 다음 [!UICONTROL 시각적 편집 도우미] 브라우저 확장을 사용하면 VEC에서 웹 사이트를 안정적으로 로드할 수 있습니다.
title: 사용 방법 [!UICONTROL 시각적 편집 도우미] 확장이요?
feature: Visual Experience Composer (VEC)
source-git-commit: 0c6d2df47a9115bcbd3c0d8a5ea7d401df29d6c8
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 27%

---

# [!UICONTROL 시각적 편집 도우미] 확장

다음 [!DNL Adobe Experience Cloud] [!UICONTROL 시각적 편집 도우미] Google Chrome용 브라우저 확장을 사용하면 웹 사이트에서 웹 사이트를 안정적으로 로드할 수 있습니다 [!UICONTROL Adobe Target] [!UICONTROL 시각적 경험 작성기] (VEC) 를 사용하여 웹 경험을 빠르게 작성 및 QA할 수 있습니다.

>[!IMPORTANT]
>
>이 새 확장은 이전 확장을 대체합니다 [Target VEC Helper 브라우저 확장 프로그램](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

## 일부 웹 사이트가 VEC에서 안정적으로 열리지 않을 수 있는 이유

* 웹 사이트에 엄격한 보안 정책이 있습니다.
* 웹 사이트가 iframe으로 되어 있습니다.
* 고객의 QA 또는 스테이지 사이트를 외부 세계(사이트가 내부적임)에서 사용할 수 없습니다.

다음 [!DNL Adobe Experience Cloud] [!UICONTROL 시각적 편집 도우미] chrome용 브라우저 확장은 고객이 현재 의존하고 있는 사이트 로딩 문제를 해결합니다. [!DNL Target] [향상된 경험 작성기](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) 또는 Requestly와 같은 타사 확장.

## 을 사용하면 얻을 수 있는 이점 [!UICONTROL 시각적 편집 도우미] 확장

* 과 같은 모든 iframe 버스팅 헤더 `X-Frame-Options` 및 `Content-Security-Policy`는 웹 사이트에서 암묵적으로 제거됩니다. 복잡한 Requestly 규칙을 만들 필요가 없습니다.
* 웹 페이지에 아직 [!DNL Target] at.js 라이브러리가 포함되어 있지 않은 경우 확장 프로그램을 사용하여 라이브러리를 주입할 수 있으므로 웹 사이트에 대한 경험을 작성할 수 있습니다. 그런 다음 활동을 만들고 미리 보기 링크를 사용하여 QA를 수행할 수 있습니다.

를 사용하여 [향상된 경험 작성기](/help/main/administrating-target/visual-experience-composer-set-up.md#eec)를 채울 때는 확장이 at.js를 주입하지 않지만 SameSite 쿠키 기능이 여전히 있습니다. 웹 페이지에서 at.js를 주입하려면 EEC를 끕니다.

* [모바일 뷰포트](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) 이 [!UICONTROL 향상된 경험 작성기] (EEC).
* [!DNL Target]을 처음 사용하는 고객은 IT 개발자가 아직 웹 사이트에서 [!DNL Target]을 구현하지 않았더라도 확장 프로그램을 사용하여 [!DNL Target]을 실험해 볼 수 있습니다.
* 이제 여러 고객의 웹 사이트 및 [!DNL Target] 계정을 제공하는 파트너는 타사 도구에서 여러 규칙을 관리하는 대신 VEC 로드를 지원하는 단일 메커니즘을 보유합니다.

## 을(를) 가져와 설치합니다. [!UICONTROL 시각적 편집 도우미] 브라우저 확장

1. 로 이동합니다 [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] chrome 웹 스토어의 브라우저 확장 프로그램](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. 클릭 **[!UICONTROL Chrome에 추가]** > **[!UICONTROL 확장 추가]**.
1. 에서 VEC 열기 [!DNL Target].
1. 확장을 사용하려면 [!UICONTROL 시각적 편집 도우미] 브라우저 확장 아이콘( ![시각적 편집 확장 아이콘](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) 내의 아무 곳에나 삽입할 수 있습니다.

   다음 [!UICONTROL 시각적 편집 도우미] 는 웹 사이트가 [!UICONTROL Target] VEC를 통해 문서 작성 가능. 확장에는 조건부 설정이 없습니다. 확장은 SameSite 쿠키 설정을 포함하여 모든 설정을 자동으로 처리합니다.

   에 대한 자세한 내용은 `SameSite=None` 속성 브라우저 수정 사항: &quot;최근에 발표된 Google Chrome SameSite 쿠키 적용 정책이 VEC 및 EEC에 어떻게 영향을 줍니까?&quot;를 참조하십시오. [시각적 경험 작성기 및 고급 경험 작성기 관련 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)에서 참조하십시오.

## 참고

* 대상 [!DNL Target]를 로드하는 경우 확장 프로그램은 [!DNL Target] 의 UI [!UICONTROL 관리] > [!UICONTROL 구현] 및 at.js는 작성 라이브러리를 다운로드합니다.
* [QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md)에서 확장 프로그램을 사용하여 at.js를 주입하는 경우 다른 Chrome 탭이 열려 있어야 합니다. 이 Chrome 탭은 동일하게 인증되어야 합니다 [!DNL Adobe Experience Cloud] 활동을 만든 조직입니다.
* 다음 메시지는 사용자에게 계속 정보를 제공하는 데 도움이 됩니다.

   * 로드하지 못하는 VEC를 사용하여 웹 사이트를 로드하려고 하면 설치를 제안하는 메시지가 표시됩니다 [!UICONTROL 시각적 편집 도우미] 브라우저 확장.
   * 웹 사이트에 at.js 또는 alloy.js가 아직 구현되지 않은 경우 확장 프로그램 설치를 제안하는 메시지가 VEC에 표시됩니다.



