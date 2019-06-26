---
description: at.js를 사용하여 자동 생성된 글로벌 mbox에 대해 전송하거나 수집한 호출 및 정보의 플로우를 표시하는 Target 시스템 다이어그램입니다.
keywords: 시스템 다이어그램;플리커;Target Standard;at.js;구현
seo-description: at.js를 사용하여 자동 생성된 글로벌 mbox에 대해 전송하거나 수집한 호출 및 정보의 플로우를 표시하는 Adobe Target 시스템 다이어그램입니다.
seo-title: Adobe Target at.js 작동 방식
solution: Target
title: at.js 작동 방식
topic: Standard
uuid: 8ed04881-3dd9-496f-9c9c-feb9c740ed80
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# at.js 작동 방식{#how-at-js-works}

[!DNL Adobe Target] 클라이언트측을 구현하려면 at.js 라이브러리를 사용해야 합니다.

클라이언트측 [!DNL Adobe Target]의 구현에서 [!DNL Target]은 활동과 연관된 경험을 클라이언트 브라우저에 직접 전달합니다. 브라우저는 표시할 경험을 결정하고 표시합니다. 클라이언트측 구현에서는 WYSIWYG 편집기, VEC([시각적 경험 작성기](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md)) 또는 [양식 기반 경험 작성기](/help/c-experiences/form-experience-composer.md)인 비-시각적 인터페이스를 사용하여 테스트 및 개인화 경험을 만들 수 있습니다.

## at.js란 무엇입니까?

[at.js 라이브러리](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17)는 Target의 새 구현 라이브러리입니다. at.js 라이브러리는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 단일 페이지 애플리케이션에 대해 더 나은 구현 옵션을 제공합니다. at.js는 권장되는 구현 라이브러리이며 새 기능으로 자주 업데이트됩니다. 모든 고객이 구현하거나 [at.js 최신 버전으로 마이그레이션](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)하는 것이 좋습니다.

자세한 내용은 [Target JavaScript 라이브러리](/help/c-intro/how-target-works.md#libraries)를 참조하십시오.

아래에 표시된 [!DNL Target] 구현에서는 [!DNL Adobe Experience Cloud] 솔루션으로서 Analytics, Target 및 Audience Management가 구현되었습니다. 또한 Experience Cloud 핵심 서비스로서 다이내믹 태그 관리(활성화), 대상 및 방문자 ID 서비스가 구현되었습니다.

## At.js 1.*x* 및 at.js 2.x 워크플로우 다이어그램의 차이점은 무엇입니까?

[at.js 1.x에서 at.js 2.x로 업그레이드](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md)에서 1.*x*와 다른 2.O에 도입된 차이점을 자세히 알 수 있습니다.

상위 수준의 보기에서 보면 두 버전 간에 두 가지 차이점이 있습니다.

* at.js 2.x에는 글로벌 mbox 요청 개념이 없지만 페이지 로드 요청은 있습니다. 페이지 로드 요청은 웹 사이트의 초기 페이지 로드 시 적용해야 하는 컨텐츠를 검색하는 요청으로 볼 수 있습니다.
* at.js 2.x는 SPA(단일 페이지 애플리케이션)에 사용되는 &quot;보기&quot; 개념을 관리합니다. at.js 1.*x*는 이 개념을 알지 못합니다.

## at.js 2.x 다이어그램

다음 다이어그램은 보기가 있는 at.js 2.x의 워크플로우를 이해하고 이를 통해 어떻게 SPA 통합이 향상되는지를 이해하는 데 도움이 됩니다. at.js 2.x에서 사용되는 개념의 도입을 보다 잘 이해하려면 [단일 페이지 애플리케이션 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md)을 참조하십시오.

![at.js 2.x에서 Target 흐름](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| 단계 | 세부 사항 |
| --- | --- |
| 1 | 사용자가 인증되면 호출에서 [!DNL Experience Cloud ID]를 반환합니다. 다른 호출은 고객 ID를 동기화합니다. |
| 2 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>at.js는 페이지에 구현된 코드 조각을 미리 숨기는 선택 사항을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 3 | 모든 구성된 매개 변수(MCID, SDID 및 고객 ID)를 포함하는 페이지 로드 요청이 이루어집니다. |
| 4 | 프로필 스크립트가 실행된 다음 프로필 저장소에 반영됩니다. 저장소는 대상 라이브러리의 적절한 대상(예: Adobe Analytics, Audience Management 등에서 공유되는 대상)을 요청합니다.<br>고객 속성은 묶음 프로세스를 통해 프로필 저장소로 전송됩니다. |
| 5 | [!DNL Target]에서는 URL 요청 매개 변수 및 프로필 데이터를 기반으로 현재 페이지 및 미래 보기를 위해 방문자에게 반환할 활동 및 경험을 결정합니다. |
| 6 | 타깃팅된 컨텐츠는 다시 페이지로 전송되며, 원할 경우 추가적인 개인화를 위한 프로필 값을 포함할 수 있습니다.<br>현재 페이지의 타깃팅된 컨텐츠는 기본 컨텐츠의 플리커 없이 가능한 한 빨리 나타납니다.<br>`triggerView()`를 통해 보기를 트리거할 때 추가적인 서버 호출 없이 즉시 적용할 수 있도록 브라우저에서 캐시된 SPA의 사용자 동작에 대한 결과로서 표시되는 보기를 위한 타깃팅된 컨텐츠입니다. |
| 7 | Analytics 데이터가 데이터 수집 서버로 전송됩니다. |
| 8 | 타깃팅된 데이터는 SDID를 통해 Analytics 데이터에 대응되며 Analytics 보고 저장소로 처리됩니다.그런 다음 <br>Analytics 데이터는 Analytics for Target (A4T) 보고서를 통해 Analytics 및 Target 모두에서 볼 수 있게 됩니다. |

이제 SPA에서 `triggerView()`가 구현될 때 그곳이 어디든, 보기 및 작업은 캐시에서 검색되고 서버 호출 없이 사용자에게 표시됩니다. `triggerView()`는 또한 노출 수를 증가시키고 기록하기 위해 [!DNL Target] 백엔드에 알림을 요청합니다. 보기가 있는 SPA용 at.js에 대한 자세한 내용은 [단일 페이지 애플리케이션 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md)을 참조하십시오.

![Target 흐름 at.js 2.x triggerView](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| 단계 | 세부 사항 |
| --- | --- |
| 1 | 보기를 렌더링하고 작업을 적용하여 시각적 요소를 수정하기 위해 SPA에서 `triggerView()`가 호출됩니다. |
| 2 | 보기용으로 타깃팅된 컨텐츠를 캐시에서 읽습니다. |
| 3 | 타깃팅된 컨텐츠는 기본 컨텐츠의 플리커 없이 가능한 한 빨리 나타납니다. |
| 4 | 활동 및 증분 지표에서 방문자를 계산하기 위해 알림 요청이 [!DNL Target] 프로필 스토어에 전송됩니다. |
| 5 | Analytics 데이터가 데이터 수집 서버로 전송됩니다. |
| 6 | Target 데이터는 SDID를 통해 Analytics 데이터에 대응되며 Analytics 보고 저장소로 처리됩니다. 그런 다음 Analytics 데이터는 A4T 보고서를 통해 Analytics 및 Target 모두에서 볼 수 있게 됩니다. |

## at.js 1.x 다이어그램

![](assets/target-flow.png)

| 단계 | 설명 | 호출 | 설명 |
|--- |--- |--- |--- |
| 1 | 사용자가 인증되면 호출에서 [!DNL Experience Cloud ID] (MCID)를 반환합니다. 다른 호출은 고객 ID를 동기화합니다. | 2 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다. |
| 3 | 모든 구성된 매개 변수, MCID, SDID 및 고객 ID(선택 사항)를 포함하는 글로벌 mbox 요청이 이루어집니다. | 4 | 프로필 스크립트가 실행된 다음 프로필 저장소에 반영됩니다. 저장소는 [!UICONTROL 대상 라이브러리]의 적절한 대상(예: [!DNL Adobe Analytics], [!DNL Audience Manager] 등에서 공유되는 대상)을 요청합니다.<br>고객 속성은 배치 프로세스를 통해 [!DNL Profile Store]로 전송됩니다. |
| 5 | [!DNL Target]에서는 URL, mbox 매개 변수 및 프로필 데이터를 기반으로 방문자에게 반환할 활동 및 경험을 결정합니다. | 6 | 타깃팅된 컨텐츠는 다시 페이지로 전송되며, 원할 경우 추가적인 개인화를 위한 프로필 값을 포함할 수 있습니다.<br>경험은 기본 컨텐츠의 플리커 없이 가능한 한 빨리 나타납니다. |
| 7 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. | 8 | [!DNL Target] 데이터는 SDID를 통해 [!DNL Analytics] 데이터에 대응되며 [!DNL Analytics] 보고 저장소로 처리됩니다.<br>그런 다음 [!DNL Analytics] 데이터는 [!DNL Analytics for Target] (A4T) 보고서를 통해 [!DNL Analytics] 및 [!DNL Target] 모두에서 볼 수 있게 됩니다. |

## 교육 비디오: at.js 2.x 아키텍처 다이어그램

at.js 2.x는 SPA에 대한 Adobe Target의 지원을 개선하고 다른 Experience Cloud 솔루션과 통합됩니다. 다음 비디오에서는 모든 것이 어떻게 합쳐지는지 설명합니다.

>[!VIDEO](https://video.tv.adobe.com/v/26250?captions=kor)

See [Understanding how at.js 2.x works](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) for more information.