---
keywords: Target;at.js;at.js로 마이그레이션;준비 상태;at.js 감사;at.js 통합
description: 일반적인 웹 구현과 SPA(단일 페이지 애플리케이션)를 위해 설계된 Adobe [!DNL Target] 용 새 구현 라이브러리인 at.js로 마이그레이션하는 방법에 대해 알아봅니다.
title: mbox.js에서 at.js로 마이그레이션하는 방법
feature: at.js
role: Developer
exl-id: d612ca74-521b-437e-aa9a-b1065e460d45
translation-type: tm+mt
source-git-commit: 824743300725bbd39077882a0971a9ccb4f753ab
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 92%

---

# mbox.js에서 at.js로 마이그레이션하는 방법

mbox.js에서 [!DNL Adobe Target]의 at.js로 마이그레이션하는 절차는 간단합니다.

다음 단계를 사용하여 [!DNL mbox.js]에서 [!DNL at.js]로 마이그레이션하고 마이그레이션을 확인하십시오.

1. 조직의 [브라우저 지원](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100) 요구 사항을 파악합니다.
1. 웹 사이트의 현재 [!DNL mbox.js] 구현이 [!DNL at.js]에서 지원하지 않는 기능을 제공하는지 확인합니다. 

   구현을 감사할 때 다음을 찾아보십시오.

   **현재 사용 중인 mbox 유형은 무엇입니까?**

   | 유형 | 세부 사항 |
   |--- |--- |
   | 자동으로 만든 글로벌 mbox | 자동으로 만든 글로벌 mbox는 사이트의 유일한 Target 코드 줄이 mbox.js 파일일 때 만들어집니다. 이 파일은 자동으로 mbox 호출을 생성합니다. |
   | 비어 있는 글로벌 mboxCreate | 자동으로 만든 글로벌 mbox로 전환하는 것이 좋습니다. |
   | mboxCreate 래핑 | `mboxCreate()` 앞에 `<div class="mboxDefault"></div>`가 오면 마이그레이션이 간단해집니다. |
   | mboxUpdate | 마이그레이션은 `mboxUpdate()`가 `mboxDefine()` 또는`mboxCreate()`과 함께 사용되면 간단해집니다. `mboxUpdate()`는 자동으로 만든 글로벌 mbox 또는 원래 `getOffer()`에 의해 만들어진 mbox는 업데이트하지 않습니다. 이러한 상황에서는 at.js로 마이그레이션할 때 `getOffer()`와 `applyOffer()`를 결합하여 `mboxUpdate()`를 대체해야 합니다. |
   | 사용자 지정 클릭 추적 mbox(mboxTrack 포함) | 코드를 `trackEvent()`. |

   >[!NOTE]
   >
   >앞의 표에 언급된 다양한 함수에 대한 자세한 내용은 [at.js 함수](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md)를 참조하십시오.

   **[!DNL mbox.js] 파일에 대한 사용자 지정 사항이 있습니까?**

   * mboxParameters()
   * mboxSupported()
   * mboxCookieDomain()
   * 추가 JavaScript
   * 기타 위치

   대부분의 [mbox.js 개체 및 메서드](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_8C78059D15D9452F95636A5640188537)(예: `mbox`, `mboxCurrent`, `mboxFactoryDefault`, `mboxFactories` 등)는 지원되지 않습니다. 다른 방법으로 원하는 작업을 수행할 수도 있습니다.

   **웹 페이지에 [!DNL mbox.js]가 있습니까?**

   동일한 웹 페이지에서 [!DNL at.js] 및 [!DNL mbox.js]를 둘 다 사용할 수는 없습니다. 그러나 동일한 웹 사이트의 두 개의 다른 페이지에서 두 개의 자바스크립트 라이브러리를 사용할 수 있습니다.

   mbox 쿠키는 Adobe가 페이지 간에 방문자를 연결하는 기본 방법입니다. QA 프로세스의 일부로, 방문자가 [!DNL at.js]가 있는 페이지와 [!DNL mbox.js]가 있는 페이지 간을 앞뒤로 이동할 때 쿠키가 보존되고 올바르게 읽히는지 확인해야 합니다. 방문자가 처음 배치되는 사이트의 섹션(`mboxPC` 또는 `mboxSession`) 및 처음에 해당 쿠키를 설정하는 섹션이 무엇인지에 관계없이, 동일한 값이 [!DNL at.js] 및 [!DNL mbox.js] 값이 mbox 호출에 전달되는지 확인하십시오. 구현에서 타사 쿠키를 사용하는 경우 사이트를 검색할 때와 동일하게 유지되는지 확인하십시오.

   **[!DNL Target]을 다른 Adobe 솔루션과 통합하려고 합니까?**

   * Analytics(A4T)
   * Analytics(레거시 통합)
   * AAM(백엔드)
   * AAM(레거시 프런트엔드)
   * AEM
   * Data Workbench

   레거시 통합 중 일부는 [!DNL at.js]에서 지원되지 않습니다. 자세한 내용은 [통합](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) 페이지를 참조하십시오.

   **[!DNL Target]을 타사 도구와 통합하려고 합니까?**

   * 기타 Analytics 도구
   * 기타 DMP
   * Demandbase
   * Click-tale
   * 기타

   [!DNL at.js]를 사용하도록 이러한 통합을 조정해야 할 수 있습니다. 자세한 내용은 [통합](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) 페이지를 참조하십시오.

   **태그 관리자를 사용합니까?**

   * Adobe Experience Platform Launch
   * Ensighten
   * Tealium
   * Signal/BrightTag

   자세한 내용은 [at.js 통합](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39)을 참조하십시오.

   >[!NOTE]
   >
   >현재, 태그 관리자를 사용하여 [!DNL Target]을 배포하고 있지 않다면 고려해볼 때가 되었습니다.
   >
   >[!DNL Platform Launch] 는 다음세대 태그 관리 플랫폼 [!DNL Adobe] 으로 구현하기 위한 기본 방법입니다 [!DNL Adobe Target]. [!DNL Platform Launch] 고객은 연관성 있는 고객 경험을 향상시키는 데 필요한 분석, 마케팅 및 광고 태그를 간단하게 배포 및 관리할 수 있습니다.
   >
   >자세한 내용은 [구현 [!DNL Target] using [!DNL Adobe Platform Launch]](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)을 참조하십시오.

1. 현재의 모든 작업 및 통합이 예상대로 작동하는지 확인하십시오.

   다음은 [!DNL at.js]가 예상대로 작동하는지 확인하기 위해 테스트하는 동안 수행할 수 있는 몇 가지 작업입니다.

   * 모든 현재 활동이 새 자바스크립트 라이브러리에서 작동하는지 확인합니다.
   * 모든 [통합](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) 및 [플러그인](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF)이 예상대로 작동하는지 확인합니다.
   * [!DNL at.js]에 사용 가능한 접근 방식으로 [디버깅](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F)할 때 문제가 없는지 확인합니다.

**at.js로 마이그레이션할 때의 발생할 수 있는 문제** at.js로의 마이그레이션을 수행한 후 일부 고객들이 다음과 같은 문제점을 신고했습니다.

* [!DNL mbox.js]가 있는 페이지에서 빌드된 일부 VEC 활동은 [!DNL at.js]에서 작동되도록 업데이트해야 할 수 있습니다.

   이러한 문제는 HTML 요소에서 많은 ID 또는 클래스 속성을 사용하지 않는 웹 사이트에서 가장 자주 발생합니다. 페이지를 로드하고 `?mboxDebug=true`를 사용하여 페이지를 로드한 후 콘솔 명령문을 검토하여 경험이 예상대로 전달되는지를 확인함으로써 이 문제가 발생하는지 알아볼 수 있습니다.

   ![](assets/mboxdebug.png)
이러한 경우 요소 선택기는 다음으로 시작될 수 있으며

   ```
   HTML > BODY > DIV:nth-of-type(2)
   ```

   [!DNL mbox.js]가 페이지 맨 위에 추가 `<div>` 요소를 추가했다는 가정하에 빌드되었습니다. [!DNL at.js]는 페이지 맨 위에 `<div>` 요소를 추가하지 않으므로 이 선택기는 더 이상 [!DNL at.js]에서 작동하지 않습니다.

   이 문제는 [!DNL at.js]를 사용하여 URL의 VEC에서 활동을 다시 만들거나 VEC에서 **[!UICONTROL &lt;/> 코드]** > **[!UICONTROL 수정]** 옵션을 사용하여 선택기를 수동으로 업데이트하여 해결할 수 있습니다.

   이 문제를 해결하려면 BODY 다음에 나오는 첫 번째 DIV 요소의 n번째 유형 번호에서 1을 뺍니다. 위의 예제에서 편집된 코드는 다음과 같습니다.

   ```
   HTML > BODY > DIV:nth-of-type(1)
   ```

   코드 편집기를 사용하여 이 작업을 수행하는 방법에 대한 자세한 내용은 [코드 편집기](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5).

* 이제 모든 mbox는 비동기이므로 실행된 순서대로 페이지 렌더링을 차단하거나 반환되지 않습니다. 자세한 내용은 [at.js 제한 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md#concept_FA99E4D6EC274552BF45E01AFB76CCAE)을 참조하십시오.
