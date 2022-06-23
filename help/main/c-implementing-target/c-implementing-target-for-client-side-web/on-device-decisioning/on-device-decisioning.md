---
keywords: 구현;javascript 라이브러리;js;atjs;on-device decisioning;device decisioning;at.js;on-device;on device
description: at.js 라이브러리를 사용하여 장치 내 의사 결정을 수행하는 방법을 알아봅니다
title: On-Device Decisioning은 at.js JavaScript 라이브러리와 어떻게 작동합니까?
feature: at.js
role: Developer
exl-id: 5ad6032b-9865-4c80-8800-705673657286
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '3546'
ht-degree: 7%

---

# at.js에 대한 On-Device Decisioning

버전 2.5.0부터 at.js는 온장치 의사 결정을 제공합니다. On-Device Decisioning을 사용하여 [A/B 테스트](/help/main/c-activities/t-test-ab/test-ab.md) 및 [경험 타깃팅](/help/main/c-activities/t-experience-target/experience-target.md) (XT) 브라우저에 대한 네트워크 요청을 차단하지 않고 인메모리 의사 결정을 수행하는 활동 [!DNL Adobe Target] 에지 네트워크.

[!DNL Target] 또한 라이브 서버 호출을 통해 실험 및 기계 학습 기반(ML 기반) 개인화 활동에서 가장 연관성 있고 최신 경험을 제공할 수 있는 유연성을 제공합니다. 즉, 성능이 가장 중요한 경우 On-Device Decisioning을 사용하도록 선택할 수 있습니다. 그러나 가장 연관성이 높은 최신 및 ML 기반 경험이 필요한 경우 대신 서버 호출을 수행할 수 있습니다.

## On-Device Decisioning의 장점은 무엇입니까?

On-Device Decisioning의 장점은 다음과 같습니다.

* **매우 신속한 의사 결정 및 경험을 제공합니다.** 네트워크 요청을 차단하지 않도록 버킷과 의사 결정이 메모리 내 및 브라우저에서 수행됩니다.
* **애플리케이션 성능 향상** 최종 사용자 경험을 손상하지 않고 실험을 실행하고 고객 및 사용자에게 개인화를 전달합니다.
* **Google 사이트 품질 점수를 개선합니다.** 메모리 내에서 의사 결정을 내리면 온라인 비즈니스의 Google 사이트 품질 점수를 향상하여 소비자가 보다 검색할 수 있도록 합니다.
* **실시간 분석에서 학습합니다.** 를 통해 활동 성능을 통해 실시간으로 통찰력을 얻을 수 있습니다 [Target 분석](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) 보고. A4T를 사용하면 중요한 시점에 전략을 조정할 수 있습니다.

## 지원되는 기능

Adobe Target JS SDK를 통해 고객은 결정을 위한 데이터의 성능과 최신 기능 중에서 선택할 수 있습니다. 즉, 기계 학습을 통해 가장 연관성이 높고 매력적인 개인화된 컨텐츠를 전달하는 것이 가장 중요한 경우 라이브 서버 호출을 수행해야 합니다. 그러나 성능이 더 중요한 경우, 온디바이스 및 인메모리 결정을 내려야 합니다. 장치 내 의사 결정이 작동하려면 지원되는 기능 목록을 참조하십시오.

* 활동 유형
* 대상 타겟팅
* 할당 방법

자세한 내용은 [On-Device Decisioning에 대해 지원되는 기능](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/).

## 온장치 의사 결정은 어떻게 작동합니까?

On-Device Decisioning을 사용하여 at.js를 배포하고 초기화하면 [규칙 아티팩트](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/rule-artifact/) 여기에는 A/B 및 XT 활동, 대상 및 자산에 대한 장치 내 결정이 포함되며, 방문자에게 가장 가까운 Akamai CDN에서 다운로드되고 방문자의 브라우저에 로컬로 캐시됩니다. at.js에서 경험을 검색하도록 요청하면, 반환할 경험에 대한 결정은 캐시된 규칙 아티팩트에서 인코딩된 메타데이터를 기반으로 메모리 내 수행됩니다.

## 의사 결정 방법

On-Device Decisioning에서는 [!DNL Target] 에서는 [!UICONTROL 의사 결정 방법]. 다음 [!UICONTROL 의사 결정 방법] 를 설정하면 at.js에서 경험을 전달하는 방법이 지시됩니다. [!UICONTROL 의사 결정 방법] 에는 세 가지 값이 있습니다.

* [!UICONTROL 서버측 전용]
* [!UICONTROL 온장치만]
* [!UICONTROL 하이브리드]

### 서버측 전용

[!UICONTROL 서버측 전용] at.js 2.5.0+가 구현되고 웹 속성에 배포될 때 즉시 설정되는 기본 의사 결정 메서드입니다.

사용 [!UICONTROL 서버측 전용] 기본 구성은 모든 결정이 [!DNL Target] 서버 호출을 차단하는 에지 네트워크. 이 접근 방식에서는 증분 지연을 도입할 수 있지만 Target의 기계 학습 기능을 다음과 같은 중요한 이점을 제공합니다 [Recommendations](/help/main/c-recommendations/recommendations.md), [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) 및 [자동 Target](/help/main/c-activities/auto-target/auto-target-to-optimize.md) 활동.

또한 세션 및 채널마다 지속되는 Target의 사용자 프로필을 사용하여 개인화된 경험을 개선하면 비즈니스에 강력한 결과를 제공할 수 있습니다.

마지막으로 [!UICONTROL 서버측 전용] Adobe Experience Cloud을 사용하고 Audience Manager 및 Adobe Analytics 세그먼트를 통해 타깃팅할 수 있는 대상을 세밀하게 조정할 수 있습니다.

다음 다이어그램은 방문자, 브라우저, at.js 2.5.0+ 및 Adobe Target Edge 네트워크 간의 상호 작용을 보여줍니다. 이 흐름 다이어그램은 새 방문자와 재방문자를 캡처합니다.

![서버측 전용 흐름 다이어그램](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/server-side-only.png)

다음 목록은 다이어그램의 숫자에 해당합니다.

| 단계 | 설명 |
| --- | --- |
| 1 | 다음 [!DNL Experience Cloud Visitor ID] 는 [Adobe Experience Cloud Identity 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en). |
| 2 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>   at.js 라이브러리는 페이지에 구현된 코드 조각 사전 숨김 옵션을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 3 | at.js 라이브러리는 깜박임을 방지하기 위해 본문을 숨깁니다. |
| 4 | 페이지 로드 요청은 ECID, 고객 ID, 사용자 지정 매개 변수, 사용자 프로필 등과 같이 구성된 모든 매개 변수를 포함하는 것입니다. |
| 5 | 프로필 스크립트가 실행된 다음 프로필 저장소에 반영됩니다.<br>프로필 저장소는 대상 라이브러리의 적절한 대상(예: [!DNL Adobe Analytics], [!DNL Adobe Audience Manager]등.)<br>고객 속성은 묶음 프로세스를 통해 프로필 저장소로 전송됩니다. |
| 6 | 프로필 저장소는 대상 자격 및 버킷으로 활동을 필터링하는 데 사용됩니다. |
| 7 | 경험이 라이브 상태에서 결정된 후에는 결과 컨텐츠가 선택됩니다 [!DNL Target] 활동. |
| 8 | at.js 라이브러리는 렌더링해야 하는 경험과 연결된 페이지에서 해당 요소를 숨깁니다. |
| 9 | at.js 라이브러리에는 방문자가 볼 수 있도록 페이지의 나머지 부분을 로드할 수 있도록 본문이 표시됩니다. |
| 10 | at.js 라이브러리는 Target Edge Network에서 경험을 렌더링하도록 DOM을 조작합니다. |
| 11 | 경험이 방문자에 대해 렌더링됩니다. |
| 12 | 전체 웹 페이지가 로드됩니다. |
| 13 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. |
| 14 | 타겟팅된 데이터가 [!DNL Analytics] SDID를 통해 데이터를 하고에 처리됩니다 [!DNL Analytics] 보고 저장소. 그런 다음 [!DNL Analytics] 데이터는 [!DNL Analytics] for [!DNL Target] (A4T) 보고서를 통해 [!UICONTROL Analytics 및 ]Target 모두에서 볼 수 있게 됩니다. |

### 온장치만

[!UICONTROL 온장치만] 는 On-Device Decisioning이 웹 페이지에서만 사용되어야 하는 경우 at.js 2.5.0+에서 설정해야 하는 의사 결정 방법입니다.

On-Device Decisioning은 결정은 On-Device Decisioning에 적합한 모든 활동을 포함하는 캐시된 규칙 아티팩트로 수행되므로 매우 빠른 속도로 환경 및 개인화 활동을 제공할 수 있습니다.

장치 내 의사 결정에 적합한 활동에 대한 자세한 내용은 [On-Device Decisioning에서 지원되는 기능](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/).

이 의사 결정 방법은 결정을 필요로 하는 모든 페이지에서 성능이 매우 중요한 경우에만 사용해야 합니다 [!DNL Target]. 또한 이 의사 결정 방법을 선택하면 [!DNL Target] On-Device Decisioning에 대한 자격이 없는 활동은 전달되거나 실행되지 않습니다. at.js 라이브러리 2.5.0+는 결정을 내릴 캐시된 규칙 아티팩트를 찾도록 구성되어 있습니다.

다음 다이어그램은 방문자, 브라우저, at.js 2.5.0+ 및 Akamai CDN의 상호 작용을 보여줍니다. Akamai CDN은 방문자의 첫 번째 방문에 대한 규칙 아티팩트를 캐시합니다. 새 방문자에 대한 첫 번째 페이지 방문의 경우, 방문자의 브라우저에 로컬로 캐시하려면 Akamai CDN에서 JSON 규칙 아티팩트를 다운로드해야 합니다. JSON 규칙 아티팩트가 다운로드되면 네트워크 호출을 차단하지 않고 즉시 결정이 수행됩니다. 다음 흐름 다이어그램은 새 방문자를 캡처합니다.

![장치 내 전용 흐름 다이어그램](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only.png)

다음 목록은 다이어그램의 숫자에 해당합니다.

>[!NOTE]
>
>[!DNL Adobe Target] 관리 서버는 On-Device Decisioning에 적합한 모든 활동을 평가하고, JSON 규칙 아티팩트를 생성하고, Akamai CDN에 전파합니다. Akamai CDN에 전파할 새 JSON 규칙 아티팩트를 출력하는 업데이트를 활동이 지속적으로 모니터링됩니다.

| 단계 | 설명 |
| --- | --- |
| 1 | 다음 [!DNL Experience Cloud Visitor ID] 는 [Adobe Experience Cloud Identity 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2개 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>at.js 라이브러리는 페이지에 구현된 코드 조각 사전 숨김 옵션을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 3 | at.js 라이브러리는 깜박임을 방지하기 위해 본문을 숨깁니다. |
| 4 | at.js 라이브러리는 가장 가까운 Akamai CDN에서 방문자에게 JSON 규칙 아티팩트를 검색하도록 요청합니다. |
| 5개 | Akamai CDN이 JSON 규칙 아티팩트에 응답합니다. |
| 6 | JSON 규칙 아티팩트는 방문자의 브라우저에 로컬로 캐시됩니다. |
| 7 | at.js 라이브러리는 JSON 규칙 아티팩트를 해석하고 경험을 검색하기 위한 결정을 실행하고 테스트된 요소를 숨깁니다. |
| 8 | at.js 라이브러리에는 방문자가 볼 수 있도록 페이지의 나머지 부분을 로드할 수 있도록 본문이 표시됩니다. |
| 9 | at.js 라이브러리는 캐시된 JSON 규칙 아티팩트에서 경험을 렌더링하도록 DOM을 조작합니다. |
| 10 | 경험이 방문자에 대해 렌더링됩니다. |
| 11 | 전체 웹 페이지가 로드됩니다. |
| 12 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. 타겟팅된 데이터가 [!DNL Analytics] SDID를 통해 데이터를 하고에 처리됩니다 [!DNL Analytics] 보고 저장소. 그런 다음 [!DNL Analytics][!DNL Analytics] 데이터는 for  (A4T) 보고서를 통해 Analytics 및 Target 모두에서 볼 수 있게 됩니다.[!DNL Target] |

다음 다이어그램은 방문자의 후속 페이지 조회나 재방문에 대해 방문자, 브라우저, at.js 2.5.0+ 및 캐시된 JSON 규칙 아티팩트 간의 상호 작용을 보여줍니다. JSON 규칙 아티팩트는 이미 캐시되고 브라우저에서 사용할 수 있으므로, 네트워크 호출 차단 없이 즉시 결정됩니다. 이 흐름 다이어그램은 후속 페이지 탐색 또는 재방문자를 캡처합니다.

![이후 페이지 탐색 및 반복 방문을 위한 장치 내 흐름 다이어그램](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only-subsequent.png)

다음 목록은 다이어그램의 숫자에 해당합니다.

>[!NOTE]
>
>[!DNL Adobe Target] 관리 서버는 On-Device Decisioning에 적합한 모든 활동을 평가하고, JSON 규칙 아티팩트를 생성하고, Akamai CDN에 전파합니다. Akamai CDN에 전파할 새 JSON 규칙 아티팩트를 출력하는 업데이트를 활동이 지속적으로 모니터링됩니다.

| 단계 | 설명 |
| --- | --- |
| 1 | 다음 [!DNL Experience Cloud Visitor ID] 는 [Adobe Experience Cloud Identity 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2개 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>at.js 라이브러리는 페이지에 구현된 코드 조각 사전 숨김 옵션을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 3 | at.js 라이브러리는 깜박임을 방지하기 위해 본문을 숨깁니다. |
| 4 | at.js 라이브러리는 JSON 규칙 아티팩트를 해석하고 메모리에서 결정을 실행하여 경험을 검색합니다. |
| 5개 | 테스트한 요소는 표시되지 않습니다. |
| 6 | at.js 라이브러리에는 방문자가 볼 수 있도록 페이지의 나머지 부분을 로드할 수 있도록 본문이 표시됩니다. |
| 7 | at.js 라이브러리는 캐시된 JSON 규칙 아티팩트에서 경험을 렌더링하도록 DOM을 조작합니다. |
| 8 | 경험이 방문자에 대해 렌더링됩니다. |
| 9 | 전체 웹 페이지가 로드됩니다. |
| 10 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. 타겟팅된 데이터가 [!DNL Analytics] SDID를 통해 데이터를 하고에 처리됩니다 [!DNL Analytics] 보고 저장소. 그런 다음 [!DNL Analytics] 데이터는 [!DNL Analytics] for [!DNL Target] (A4T) 보고서를 통해 [!UICONTROL Analytics 및 ]Target 모두에서 볼 수 있게 됩니다. |

### 하이브리드

[!UICONTROL 하이브리드] 는 On-Device Decisioning과 Adobe Target Edge 네트워크에 대한 네트워크 호출이 필요한 활동을 모두 실행해야 할 때 at.js 2.5.0+에서 설정해야 하는 의사 결정 방법입니다.

On-Device Decisioning 활동과 서버측 활동을 모두 관리하는 경우 배포 및 프로비저닝 방법을 생각할 때 약간 복잡하고 번거로울 수 있습니다 [!DNL Target] 참조하십시오. 의사 결정 방법으로 하이브리드 사용, [!DNL Target] 서버측 실행이 필요한 활동과 장치 내 의사 결정만 실행해야 하는 시기를 위해 Adobe Target Edge 네트워크에 서버 호출을 해야 하는 시기를 알고 있습니다.

JSON 규칙 아티팩트에는 at.js에 mbox에 실행 중인 서버측 활동 또는 On-Device Decisioning 활동이 있는지 여부를 알리는 메타데이터가 포함되어 있습니다. 이 의사 결정 방법은 빠르게 전달하려는 활동을 On-Device Decisioning을 통해 수행하고 보다 강력한 ML 기반 개인화가 필요한 활동에 대해 이러한 활동을 Adobe Target Edge 네트워크를 통해 수행할 수 있도록 합니다.

다음 다이어그램은 처음으로 페이지를 방문하는 새 방문자에 대한 방문자, 브라우저, at.js 2.5.0+, Akamai CDN 및 Adobe Target Edge Network 간의 상호 작용을 보여줍니다. 이 다이어그램에서 가져오는 내용은 Adobe Target Edge 네트워크를 통해 결정을 내리는 동안 JSON 규칙 아티팩트가 비동기식으로 다운로드된다는 것입니다.

이 접근 방식을 사용하면 많은 활동을 포함할 수 있는 아티팩트 크기가 의사 결정의 지연에 부정적인 영향을 주지 않습니다. JSON 규칙 아티팩트를 동기식으로 다운로드하고 그런 다음 결정을 내리면 지연에 부정적인 영향을 줄 수 있으며 일관되지 않을 수 있습니다. 따라서, 하이브리드 의사 결정 방법은 새 방문자에 대한 의사 결정에 대해 항상 서버측 호출을 수행하는 우수 사례이며, JSON 규칙 아티팩트가 병렬로 캐시됩니다. 후속 페이지 방문 및 재방문에 대해 JSON 규칙 아티팩트를 통해 캐시 및 인메모리에서 결정을 합니다.

![최초 방문자를 위한 하이브리드 흐름 다이어그램](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-first-time-visitor.png)

다음 목록은 다이어그램의 숫자에 해당합니다.

>[!NOTE]
>
>[!DNL Adobe Target] 관리 서버는 On-Device Decisioning에 적합한 모든 활동을 평가하고, JSON 규칙 아티팩트를 생성하고, Akamai CDN에 전파합니다. Akamai CDN에 전파할 새 JSON 규칙 아티팩트를 출력하는 업데이트를 활동이 지속적으로 모니터링됩니다.

| 단계 | 설명 |
| --- | --- |
| 1 | 다음 [!DNL Experience Cloud Visitor ID] 는 [Adobe Experience Cloud Identity 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2개 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>at.js 라이브러리는 페이지에 구현된 코드 조각 사전 숨김 옵션을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 3 | at.js 라이브러리는 깜박임을 방지하기 위해 본문을 숨깁니다. |
| 4 | Adobe Target Edge Network에 페이지 로드 요청이 수행되며, ECID, 고객 ID, 사용자 지정 매개 변수, 사용자 프로필 등과 같은 구성된 모든 매개 변수를 포함합니다. |
| 5개 | 동시에 at.js는 가장 가까운 Akamai CDN에서 방문자에게 JSON 규칙 아티팩트를 검색하도록 요청합니다. |
| 6 | (Adobe Target Edge Network) 프로필 스크립트가 실행된 다음 프로필 저장소에 반영됩니다. 프로필 저장소는 대상 라이브러리의 적절한 대상(예: [!DNL Adobe Analytics], [!DNL Adobe Audience Manager]등.) |
| 7 | Akamai CDN이 JSON 규칙 아티팩트에 응답합니다. |
| 8 | 프로필 저장소는 대상 자격 및 버킷으로 활동을 필터링하는 데 사용됩니다. |
| 9 | 경험이 라이브 상태에서 결정된 후에는 결과 컨텐츠가 선택됩니다 [!DNL Target] 활동. |
| 10 | at.js 라이브러리는 렌더링해야 하는 경험과 연결된 페이지에서 해당 요소를 숨깁니다. |
| 11 | at.js 라이브러리에는 방문자가 볼 수 있도록 페이지의 나머지 부분을 로드할 수 있도록 본문이 표시됩니다. |
| 12 | at.js 라이브러리는 Target Edge Network에서 경험을 렌더링하도록 DOM을 조작합니다. |
| 13 | 경험이 방문자에 대해 렌더링됩니다. |
| 14 | 전체 웹 페이지가 로드됩니다. |
| 15 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. 타겟팅된 데이터가 [!DNL Analytics] SDID를 통해 데이터를 하고에 처리됩니다 [!DNL Analytics] 보고 저장소. 그런 다음 [!DNL Analytics] 데이터는 [!DNL Analytics] for [!DNL Target] (A4T) 보고서를 통해 [!UICONTROL Analytics 및 ]Target 모두에서 볼 수 있게 됩니다. |

다음 다이어그램은 방문자, 브라우저, at.js 2.5.0+ 및 후속 페이지 탐색 또는 재방문에 대해 캐시된 JSON 규칙 아티팩트 간의 상호 작용을 보여줍니다. 이 다이어그램에서는 후속 페이지 탐색 또는 재방문에 대해 장치 내에서 결정을 내리는 사용 사례에만 초점을 둡니다. 특정 페이지에 대해 라이브 상태인 활동에 따라 서버측 결정을 실행하도록 서버측 호출을 수행할 수 있습니다.

![후속 페이지 탐색 및 반복 방문을 위한 하이브리드 흐름 다이어그램](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-subsequent.png)

다음 목록은 다이어그램의 숫자에 해당합니다.

>[!NOTE]
>
>[!DNL Adobe Target] 관리 서버는 On-Device Decisioning에 적합한 모든 활동을 평가하고, JSON 규칙 아티팩트를 생성하고, Akamai CDN에 전파합니다. Akamai CDN에 전파할 새 JSON 규칙 아티팩트를 출력하는 업데이트를 활동이 지속적으로 모니터링됩니다.

| 단계 | 설명 |
| --- | --- |
| 1 | 다음 [!DNL Experience Cloud Visitor ID] 는 [Adobe Experience Cloud Identity 서비스](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2개 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>at.js 라이브러리는 페이지에 구현된 코드 조각 사전 숨김 옵션을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 3 | at.js 라이브러리는 깜박임을 방지하기 위해 본문을 숨깁니다. |
| 4 | 경험을 검색하도록 요청합니다. |
| 5개 | at.js 라이브러리는 JSON 규칙 아티팩트가 이미 캐시된 것을 확인하고 경험을 검색하기 위해 메모리에서 결정을 실행합니다. |
| 6 | 테스트한 요소는 표시되지 않습니다. |
| 7 | at.js 라이브러리에는 방문자가 볼 수 있도록 페이지의 나머지 부분을 로드할 수 있도록 본문이 표시됩니다. |
| 8 | at.js 라이브러리는 캐시된 JSON 규칙 아티팩트에서 경험을 렌더링하도록 DOM을 조작합니다. |
| 9 | 경험이 방문자에 대해 렌더링됩니다. |
| 10 | 전체 웹 페이지가 로드됩니다. |
| 11 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. 타겟팅된 데이터가 [!DNL Analytics] SDID를 통해 데이터를 하고에 처리됩니다 [!DNL Analytics] 보고 저장소. 그런 다음 [!DNL Analytics] 데이터는 [!DNL Analytics] for [!DNL Target] (A4T) 보고서를 통해 [!UICONTROL Analytics 및 ]Target 모두에서 볼 수 있게 됩니다. |

## 장치 내 의사 결정을 활성화하려면 어떻게 해야 합니까?

모든 사용자가 장치 내 의사 결정을 사용할 수 있습니다 [!DNL Target] at.js 2.5.0+를 사용하는 고객.

장치 내 의사 결정을 사용하려면

>[!NOTE]
>
>다음 항목이 있어야 합니다. [!UICONTROL 관리] 또는 [!UICONTROL 승인자] [사용자 역할](/help/main/administrating-target/c-user-management/user-management.md) On-Device Decisioning 전환을 활성화하거나 비활성화하는 중입니다.

1. 클릭 **[!UICONTROL 관리]** > **[!UICONTROL 구현]** > **[!UICONTROL 계정 세부 사항]**.
1. 아래 **[!UICONTROL 계정 세부 사항]**&#x200B;를 눌러 **[!UICONTROL On-Device Decisioning]** 켜짐 위치로 전환합니다.

   ![On-Device Decisioning 전환](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-toggle.png)

   &quot;[!UICONTROL 아티팩트에 기존의 모든 On-Device Decisioning 자격 활동 포함]장치 내 의사 결정을 활성화하는 경우 &quot;옵션이 표시됩니다.
1. (조건부) On-Device Decisioning에 대한 자격이 있는 모든 라이브 Target 활동을 아티팩트에 자동으로 포함하려면 전환을 &quot;켜기&quot; 위치로 끕니다.

   이 토글을 끄면 생성된 규칙 아티팩트에 포함할 On-Device Decisioning 활동을 다시 만들고 활성화해야 합니다. 즉, 를 켜기 전에 라이브 상태의 모든 활동 [!UICONTROL On-Device Decisioning] 토글은 규칙 아티팩트에 포함되지 않습니다.

를 활성화한 후 [!UICONTROL On-Device Decisioning] 전환, [!DNL Target] 생성 및 전파 [규칙 객체](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/rule-artifact/) 참조하십시오.

>[!IMPORTANT]
>
>Adobe Target SDK를 초기화하여 장치 내 의사 결정을 사용하도록 하려면 먼저 토글을 활성화해야 합니다. 규칙 가공물에서는 먼저 On-Device Decisioning이 작동하도록 Akamai CDN을 생성 및 전파해야 합니다. 전파는 첫 번째 규칙 아티팩트가 생성하여 Akamai CDN에 전파하는 데 5~10분이 걸릴 수 있습니다.

## On-Device Decisioning을 사용하도록 at.js 2.5.0+를 구성하려면 어떻게 합니까?

1. 클릭 **[!UICONTROL 관리]** > **[!UICONTROL 구현]** > **[!UICONTROL 계정 세부 사항]**.
1. 아래 **[!UICONTROL 구현 방법]** > **[!UICONTROL 기본 구현 방법]**&#x200B;를 클릭합니다. **[!UICONTROL 편집]** at.js 버전 옆의 at.js 2.5.0 이상을 사용해야 합니다.

   ![기본 구현 메서드 설정 편집](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/main-implementation-method.png)

   >[!IMPORTANT]
   >
   >이러한 기본 설정을 변경하기 전에 현재 구현에 영향을 주지 않도록 Client Care에 문의하십시오.

1. 원하는 의사결정 방법을 선택합니다.

   * [!UICONTROL 서버측 전용]
   * [!UICONTROL 온장치만]
   * [!UICONTROL 하이브리드]

   ![at.js 설정 패널 편집](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/global-settings.png)

### 전역 설정

기본값을 구성할 수 있습니다 [!UICONTROL 의사 결정 방법] 모든 [!DNL Target] 결정. 다양한 의사 결정 방법은 다음과 같습니다 [!UICONTROL 서버측 전용], [!UICONTROL 온장치만], 및 [!UICONTROL 하이브리드]. Target UI에서 선택한 의사 결정 방법은에서 구성됩니다. `window.targetGlobalSettings` 아래에 `decisioningMethod` 필드. 추가 정보 `decisioningMethod` in [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).

```javascript
<head> 
    <script type="text/javascript">

        window.targetGlobalSettings = { 
            clientCode: "yourClientCodeHere", 
            imsOrgId: "imsOrgId@AdobeOrg", 
            decisioningMethod: "on-device"

        }; 
    </script>

    <script type="text/javascript" src="at.js"></script> 
</head>
```

### 사용자 지정된 설정

를 설정하는 경우 `decisioningMethod` in `window.targetGlobalSettings`를 재정의하려는 경우 `decisioningMethod` 사용 사례에 따라 각 Adobe Target 결정에 대해 `decisioningMethod` at.js 2.5.0+의 [getOffers()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/) 호출.

```javascript
adobe.target.getOffers({ 

  decisioningMethod:"on-device", 
  request: { 
    execute: { 
      mboxes: [ 
        { 
          index: 0, 
          name: "homepage" 
        } 
      ] 
    } 
 } 
});
```

>[!NOTE]
>
>getOffers() 호출에서 &quot;on-device&quot; 또는 &quot;hybrid&quot;를 의사 결정 메서드로 사용하려면 전역 설정이 `decisioningMethod` 를 &quot;on-device&quot; 또는 &quot;hybrid&quot;로 설정합니다. at.js 라이브러리 2.5.0+는 페이지에 로드한 후 즉시 JSON 규칙 아티팩트를 다운로드하고 캐시할지 여부를 알고 있어야 합니다. 전역 설정에 대한 의사 결정 방법이 &quot;서버측&quot;으로 설정되고 &quot;on-device&quot; 또는 &quot;hybrid&quot; 의사 결정 메서드가 getOffers() 호출에 전달되는 경우 at.js 2.5.0+에는 장치 내 결정을 실행하기 위해 캐시된 JSON 규칙 아티팩트가 없습니다.

### 아티팩트 캐시 TTL

[!DNL Target] 메타데이터, 규칙 및 조건으로 구성된 아티팩트로 온장치 의사 결정에 적합한 활동을 나타냅니다. 이 아티팩트는 Akamai CDN에 캐시됩니다. 사용자가 처음 방문하는 동안 사용자의 브라우저는 On-Device Decisioning 활동을 나타내는 객체를 다운로드하고 캐시합니다.

이후 사이트 방문 시 브라우저는 자동으로 최신 버전의 아티팩트를 다운로드해야 하는지 여부를 확인합니다. 이 확인은 지연을 추가합니다. Artifact Cache TTL은 마지막으로 성공한 다운로드 이후 브라우저가 업데이트된 아티팩트를 확인하지 않도록 하는 시간(분)을 정의합니다. 시간이 길수록 성능이 향상됩니다. 기간이 짧을수록 데이터 신선도가 향상되지만 지연 시간이 길어집니다.

## 활동이 On-Device Decisioning이 적합한지 어떻게 알 수 있습니까?

On-Device Decisioning에 적합한 활동을 만든 후 [!UICONTROL On-Device Decisioning 적격]가 활동의 [!UICONTROL 개요] 페이지.

![활동의 개요 페이지에서 On-Device Decisioning 적격 레이블](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-eligible-label.png)

이 레이블이 활동이 항상 On-Device Decisioning을 통해 전달됨을 의미하지는 않습니다. at.js 2.5.0+가 On-Device Decisioning을 사용하도록 구성된 경우에만 이 활동이 장치에서 실행됩니다. at.js 2.5.0+가 온장치를 사용하도록 구성되지 않은 경우 이 활동은 at.js에서 수행되는 서버 호출을 통해 계속 전달됩니다.

에 자격이 있는 On-Device Decisioning의 모든 활동을 필터링할 수 있습니다 [!UICONTROL 활동] 페이지를 통해 [!UICONTROL On-Device Decisioning 적격] 필터.

![활동 페이지의 On-Device Decisioning 대상 필터.](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-filter.png)

>[!NOTE]
>
>On-Device Decisioning에 사용할 수 있는 활동을 만들고 활성화한 후에는 생성 및 Akamai CDN 프레젠테이션 지점으로 전파되는 규칙 아티팩트에 포함되려면 5~10분이 걸릴 수 있습니다.

## 내 온장치 의사 결정 활동이 At.js 2.5.0을 통해 전달되도록 하는 단계 요약+?

1. Adobe Target UI에 액세스하여 다음 위치로 이동합니다. **[!UICONTROL 관리]** > **[!UICONTROL 구현]** > **[!DNL Account Details]** 를 **[!UICONTROL On-Device Decisioning]** 토글.
1. 를 활성화합니다 **&quot;[!UICONTROL 아티팩트에 기존의 모든 On-Device Decisioning 자격 활동 포함]&quot;** 토글.

   첫 번째 JSON 규칙 아티팩트 생성이 최대 10분이 소요될 수 있습니다.

1. 만들기 및 활성화 [on-device decisioning에서 지원하는 활동 유형](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/), 그리고 온장치 의사 결정 자격이 있는지 확인합니다.
1. 설정 **[!UICONTROL 의사 결정 방법]** 다음 중 하나를 수행합니다. **[!UICONTROL &quot;하이브리드&quot;]** 또는 **[!UICONTROL &quot;온장치 전용&quot;]** at.js 설정 UI 사용.
1. 페이지에 At.js 2.5.0+를 다운로드하여 배포합니다.
