---
keywords: vec;시각적 경험 작성기; vec;iframe;확장 프로그램;브라우저;faq
description: '[!UICONTROL 시각적 경험 작성기] (VEC)에서 일부 웹 사이트가 안정적으로 열리지 않는 이유를 알아보십시오. [!UICONTROL Visual Editing Helper] 브라우저 확장 기능을 사용하면 VEC에서 웹 사이트를 안정적으로 로드할 수 있습니다.'
title: '[!UICONTROL Visual Editing Helper] 확장 기능을 사용하려면 어떻게 해야 합니까?'
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
TQID: 'https://experienceleague.adobe.com/wUWUT-FvVIAo52PDaBMfmT7vxv8VOR71hSGhxFvylus'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
    internal-label: Web experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 4%
---
# [!UICONTROL 시각적 편집 도우미] 확장 {#visual-editing-helper}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL Visual Editing Helper]** 브라우저 확장 기능이 **[!UICONTROL 시각적 경험 작성기]**(VEC)에서 웹 사이트를 안정적으로 로드하는 방법과 웹 사이트를 설치하고 사용하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

[!DNL Google Chrome]용 [!DNL Adobe Experience Cloud] **[!UICONTROL Visual Editing Helper]** 브라우저 확장 기능은 [!DNL Adobe Target] **[!UICONTROL 시각적 경험 작성기]**(VEC)에서 웹 사이트를 안정적으로 로드하므로 웹 경험을 더 빨리 작성하고 확인할 수 있습니다.

>[!IMPORTANT]
>
>이 확장 프로그램은 해당 문서 상단의 중요 참고 사항에 설명된 대로 이전 [Target VEC Helper 브라우저 확장 프로그램](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)을 대체합니다. Manifest V3에서는 보안 기능이 향상되었으므로 [!DNL Adobe]에서 웹 사이트를 시각적으로 계속 작성하려면 이 새 확장을 다운로드해야 합니다.[!DNL Target]

## 일부 웹 사이트가 VEC에서 안정적으로 열리지 않는 이유

다음과 같은 이유로 VEC에서 웹 사이트가 안정적으로 열리지 않을 수 있습니다.

* 웹 사이트에 엄격한 보안 정책이 있습니다.
* 웹 사이트가 iframe으로 되어 있습니다.
* 고객의 QA 또는 스테이징 사이트는 내부에 있으며 네트워크 외부에서 사용할 수 없습니다.

확장은 고객이 [향상된 경험 작성기](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) 또는 Requestly와 같은 타사 확장에 의존하는 이러한 사이트 로드 문제를 해결합니다.

## 확장의 이점

* **Iframe 버스팅 헤더가 제거됨:** 확장에서 `X-Frame-Options` 및 `Content-Security-Policy`과(와) 같은 헤더를 웹 사이트에서 묵시적으로 제거하므로 복잡한 Requestly 규칙이 필요하지 않습니다.
* **at.js 삽입:** 웹 페이지에 아직 [!DNL Target] at.js 라이브러리가 포함되지 않은 경우 확장 프로그램에서 삽입할 수 있습니다. 그런 다음 웹 사이트에 대한 경험을 작성할 수 있으며 활동을 만들고 미리보기 링크로 확인할 수 있습니다. EEC([고급 경험 작성기](/help/main/administrating-target/visual-experience-composer-set-up.md#eec))를 사용하면 확장 기능이 at.js에 삽입되지는 않지만 SameSite 쿠키 기능은 유지됩니다. 웹 페이지에서 at.js를 삽입하려면 EEC를 끕니다.
* **모바일 뷰포트:** [모바일 뷰포트](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md)은(는) EEC(**[!UICONTROL 고급 경험 작성기]**) 없이도 지원됩니다.
* **새 [!DNL Target] 고객:** 확장을 사용하면 IT 개발자가 아직 웹 사이트에 [!DNL Target]을(를) 구현하지 않은 경우에도 [!DNL Target]을(를) 실험할 수 있습니다.
* **파트너:** 웹 사이트와 여러 고객의 [!DNL Target] 계정을 서비스하는 파트너는 서드파티 도구의 여러 규칙 대신 VEC 로드를 지원하는 단일 메커니즘을 사용할 수 있습니다.

## 확장 얻기 및 설치

[!DNL Chrome]에 확장을 설치하면 iframe을 차단하거나 아직 at.js가 구현되지 않은 웹 사이트를 포함하여 VEC에서 웹 사이트를 안정적으로 로드할 수 있습니다.

1. Chrome 웹 스토어의 [[!DNL Adobe Experience Cloud] **[!UICONTROL Visual Editing Helper &#x200B;]**&#x200B;브라우저 확장 기능으로 이동](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. **[!UICONTROL Chrome에 추가]** > **[!UICONTROL 확장 추가]**&#x200B;를 클릭합니다.
1. [!DNL Target]에서 VEC를 엽니다.
1. VEC 또는 QA 모드에서 [!DNL Chrome]의 도구 모음에서 **[!UICONTROL Visual Editing Helper]** 브라우저 확장 기능 아이콘(![Visual Editing Helper 아이콘](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png))을 클릭합니다.

   작성 기능을 향상시키기 위해 [!DNL Target] VEC에서 웹 사이트를 열면 확장이 자동으로 활성화됩니다. 여기에는 조건부 설정이 없으며 SameSite 쿠키 설정을 포함한 모든 설정을 자동으로 처리합니다. `SameSite=None` 특성 브라우저 수정 사항에 대한 자세한 내용은 [Google Chrome SameSite 쿠키 정책](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)을 참조하십시오.

## 사용 정보

* 확장 프로그램은 **[!UICONTROL 관리]** > **[!UICONTROL 구현]** 아래의 [!DNL Target] UI에서 사용할 수 있는 최신 at.js 버전을 로드하고 at.js에서 작성 라이브러리를 다운로드합니다.
* 확장 프로그램을 사용하여 [QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md)에서 at.js를 삽입하려면 다른 Chrome 탭이 열려 있어야 합니다. 이 탭은 활동을 만든 것과 동일한 [!DNL Adobe Experience Cloud] 조직에 대해 인증되어야 합니다.
* 다음과 같은 경우 VEC에 확장 설치를 제안하는 메시지가 표시됩니다.

  * 웹 사이트가 VEC에서 로드되지 않습니다.
  * at.js 또는 alloy.js는 아직 웹 사이트에서 구현되지 않았습니다.

* 새 확장을 시도하고 [이전 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)을(를) 다시 사용하지만 [!DNL Target]이(가) 웹 사이트를 로드하지 못한다면 브라우저 데이터를 모두 지우고 새 확장을 사용하지 않도록 설정하십시오.

## 확장 최종 변경 사항(2026년 1월 17일)

확장 프로그램은 VEC Helper에 시작 쿠키 정리 실험 기능을 추가합니다. 이 기능은 작성을 시작할 때, 지속적이 아니라 탭당 한 번씩 파티션되지 않은 쿠키를 정리하여 성능과 안정성을 개선합니다. 각 탭의 내역을 추적하여 중복 정리를 방지하고 탭을 닫으면 해당 내역을 지우므로 탭을 다시 열면 정리가 올바르게 작동합니다. 단위 테스트는 일관된 동작을 보장합니다.

![쿠키 처리 모드, 고급 로깅 옵션 및 실험 기능을 포함한 VEC Helper 확장 기능의 옵션 웹 페이지 로드, 쿠키 정리 및 시작 쿠키 정리 지연](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper.png)

## FAQ

+++ 확장 프로그램이 [!DNL Adobe Target] 또는 [!UICONTROL Adobe Journey Optimizer]&#x200B;(AJO) 외부에서 사용될 때 수행되는 작업이 있습니까?

확장 기능은 웹 사이트가 [!DNL Adobe] 제품([!DNL Target], [!DNL AJO])의 iFrame 내부에 로드된 경우에만 활성화됩니다. 이 흐름을 벗어나면 확장 기능은 헤더를 추가, 제거 또는 수정하지 않으며, 웹 사이트 내부에 코드를 삽입하지 않습니다.

+++

+++ 확장 기능이 [!DNL Adobe Target] VEC에서 활성화되면 어떤 작업을 합니까?

웹 사이트가 [!DNL Adobe] 제품([!DNL Target], [!DNL AJO])의 iFrame 내부에 로드되면 확장 기능이 확장 기능과 함께 번들로 제공되는 코드를 웹 사이트에 삽입하고 [!DNL Adobe] CDN에서 Helper 파일을 다운로드하여 시각적 저작을 가능하게 합니다.

+++
