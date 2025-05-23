---
keywords: vec;시각적 경험 작성기; vec;iframe;확장 프로그램;브라우저;faq
description: '[!UICONTROL Visual Experience Composer] (VEC)에서 일부 웹 사이트가 안정적으로 열리지 않는 이유를 알아봅니다. [!UICONTROL Visual Editing Helper] 브라우저 확장을 사용하면 VEC에서 웹 사이트를 안정적으로 로드할 수 있습니다.'
title: '[!UICONTROL Visual Editing Helper] 확장을 사용하는 방법'
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
source-git-commit: c41580bcbecf2eb2c14f13ce8e66e854c655d059
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 64%

---

# [!UICONTROL Visual Editing Helper] 확장

[!DNL Google Chrome]에 대한 [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] 브라우저 확장을 사용하면 웹 사이트를 [!UICONTROL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC)에 안정적으로 로드하여 웹 경험을 빠르게 작성 및 QA할 수 있습니다.

>[!IMPORTANT]
>
>* 이 새 확장 기능은 이전의 [Target VEC Helper 브라우저 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)을 대체합니다. 이 문서의 맨 위에 있는 중요 참고 사항을 참조하십시오. Manifest v3의 향상된 보안 기능 때문에 [!DNL Adobe]에서 [!DNL Target]에서 웹 사이트를 계속 시각적으로 작성하려면 이 새 확장을 다운로드해야 합니다.

## 일부 웹 사이트가 VEC에서 안정적으로 열리지 않을 수 있는 이유

* 웹 사이트에 엄격한 보안 정책이 있습니다.
* 웹 사이트가 iframe으로 되어 있습니다.
* 고객의 QA 또는 스테이지 사이트는 외부에서 사용할 수 없습니다(사이트는 내부 사이트임).

용 [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] 브라우저 확장은 고객이 현재 [!DNL Target] [고급 경험 작성기](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) 또는 Requestly와 같은 타사 확장에 의존하는 사이트 로드 문제를 해결합니다.

## [!UICONTROL Visual Editing Helper] 확장을 사용할 때의 이점

* `X-Frame-Options` 및 `Content-Security-Policy`와 같은 모든 iframe 버스팅 헤더는 웹 사이트에서 묵시적으로 제거됩니다. 복잡한 Requestly 규칙을 만들 필요가 없습니다.
* 웹 페이지에 아직 [!DNL Target] at.js 라이브러리가 포함되어 있지 않은 경우 확장 기능을 사용하여 라이브러리를 삽입할 수 있으므로 웹 사이트에 대한 경험을 작성할 수 있습니다. 그런 다음 활동을 만들고 미리보기 링크를 사용하여 QA를 수행할 수 있습니다.

  [고급 경험 작성기](/help/main/administrating-target/visual-experience-composer-set-up.md#eec)를 사용하면 확장 기능이 at.js에 삽입되지는 않지만 SameSite 쿠키 기능은 여전히 존재합니다. 웹 페이지에서 at.js를 삽입하려면 EEC를 끕니다.

* [모바일 뷰포트](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md)은(는) [!UICONTROL Enhanced Experience Composer] (EEC) 없이도 지원됩니다.
* [!DNL Target]을 처음 사용하는 고객은 IT 개발자가 아직 웹 사이트에서 [!DNL Target]을 구현하지 않았더라도 확장 기능을 사용하여 [!DNL Target]을 실험해 볼 수 있습니다.
* 이제 여러 고객의 웹 사이트 및 [!DNL Target] 계정을 제공하는 파트너는 서드파티 도구에서 여러 규칙을 관리하는 대신 VEC 로드를 지원하는 단일 메커니즘을 보유합니다.

## [!UICONTROL Visual Editing Helper] 브라우저 확장 가져오기 및 설치

1. Chrome 웹 스토어의 [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] 브라우저 확장](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}(으)로 이동합니다.
1. **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**&#x200B;을(를) 클릭합니다.
1. [!DNL Target]에서 VEC를 엽니다.
1. 확장 기능을 사용하려면 VEC 또는 QA 모드에서 Chrome 브라우저의 도구 모음에서 [!UICONTROL Visual Editing Helper] 브라우저 확장 기능 아이콘(![시각적 편집 확장 기능 아이콘](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png))을 클릭합니다.

   작성 기능을 향상시키기 위해 [!UICONTROL Target] VEC에서 웹 사이트를 열면 [!UICONTROL Visual Editing Helper]이(가) 자동으로 활성화됩니다. 확장 기능에는 조건부 설정이 없습니다. 확장 기능은 SameSite 쿠키 설정을 포함한 모든 설정을 자동으로 처리합니다.

   `SameSite=None` 속성 브라우저 수정 사항에 대한 자세한 내용은 “최근 발표된 Google Chrome SameSite 쿠키 시행 정책이 VEC 및 EEC에 어떤 영향을 미칩니까?”를 참조하십시오. [시각적 경험 작성기 및 고급 경험 작성기 관련 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)에서 참조하십시오.

## 참고

* [!DNL Target]의 경우 확장 기능은 [!UICONTROL Administration] > [!UICONTROL Implementation]의 [!DNL Target] UI에서 사용할 수 있는 최신 at.js 버전을 로드하고 at.js에서 작성 라이브러리를 다운로드합니다.
* [QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md)에서 확장 기능을 사용하여 at.js를 삽입하는 경우 다른 Chrome 탭이 열려 있어야 합니다. 이 Chrome 탭은 활동을 만든 [!DNL Adobe Experience Cloud] 조직과 동일한 조직에서 인증되어야 합니다.
* 다음 메시지는 사용자에게 계속 정보를 제공하는 데 도움이 됩니다.

   * 로드에 실패한 VEC를 사용하여 웹 사이트를 로드하려고 하면 [!UICONTROL Visual Editing Helper] 브라우저 확장을 설치하라는 메시지가 표시됩니다.
   * 웹 사이트에서 at.js 또는 alloy.js가 아직 구현되지 않은 경우 VEC에 확장 기능을 설치하라는 메시지가 표시됩니다.
* 새로운 확장 기능을 사용해 보고 [이전 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)으로 돌아간 후 [!DNL Target]이 웹 사이트를 로드하지 못한다면 브라우저 데이터를 모두 지우고 새 확장 기능을 비활성화하십시오.

## 자주 묻는 질문

### 확장 기능이 활성화된 경우 [!DNL Adobe Target] 또는 [!UICONTROL Adobe Journey Optimizer] (AJO) 외부에서 사용될 때 수행되는 작업이 있습니까?

확장 기능은 해당 웹 사이트가 [!DNL Adobe] 제품([!DNL Target], [!DNL AJO])의 iFrame 내부에 로드된 경우에만 활성화됩니다. 이 흐름을 벗어나면 확장 기능은 헤더를 추가, 제거 또는 수정하지 않으며, 확장 기능은 웹 사이트 내부에 코드를 삽입하지 않습니다.

### 확장 기능이 [!DNL Adobe Target] VEC에서 활성화되면 어떤 작업을 합니까?

웹 사이트가 [!DNL Adobe] 제품([!DNL Target], [!DNL AJO])의 iFrame 내부에 로드되면 확장 기능이 웹 사이트에 코드(확장 기능과 함께 제공됨)를 삽입하고 [!DNL Adobe] CDN에서 Helper 파일을 다운로드하여 시각적 저작을 가능하게 합니다.
