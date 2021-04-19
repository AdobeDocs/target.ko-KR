---
keywords: 구현;javascript 라이브러리;js;장치 내 의사 결정;장치 의사 결정;at.js;온-장치;on-device
description: at.js 라이브러리를 사용하여 장치 내 의사 결정을 수행하는 방법에 대해 알아봅니다.
title: 장치 내 의사 결정은 at.js JavaScript 라이브러리에서 어떻게 작동합니까?
feature: at.js
role: Developer
exl-id: 5ad6032b-9865-4c80-8800-705673657286
translation-type: tm+mt
source-git-commit: dba3044c94502ea9e25b21a3034dc581de10f431
workflow-type: tm+mt
source-wordcount: '3506'
ht-degree: 7%

---

# at.js에 대한 장치 내 의사 결정

>[!NOTE]
>
>장치 내 의사 결정은 예정된 [at.js 2.5.0 릴리스](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)와 함께 사용할 수 있습니다. 곧 발표할 날짜입니다.

버전 2.5.0부터 at.js는 장치 내 의사 결정을 제공합니다. 장치 내 의사 결정을 사용하면 [!DNL Adobe Target] 에지 네트워크에 대한 차단 네트워크 요청 없이 메모리 내 의사 결정을 수행하도록 브라우저에서 [A/B 테스트](/help/c-activities/t-test-ab/test-ab.md) 및 [경험 타깃팅](/help/c-activities/t-experience-target/experience-target.md)(XT) 활동을 캐시할 수 있습니다.

[!DNL Target] 또한 실시간 서버 호출을 통해 원하는 대로 정확하게 원하는 경험을 제공하고 머신 러닝 기반의 개인화 활동(ML 기반의)을 통해 최신 경험을 제공할 수 있습니다. 즉, 성능이 가장 중요한 경우 장치 내 의사 결정을 사용하도록 선택할 수 있습니다. 그러나 가장 관련성이 높은 최신 경험 및 ML 기반의 경험이 필요한 경우 서버 호출을 대신 수행할 수 있습니다.

## 장치 내 의사 결정의 이점은 무엇입니까?

디바이스 내 의사 결정의 이점:

* **신속한 의사 결정 및 경험 전달** 네트워크 요청을 차단하지 않도록 버켓팅 및 의사 결정이 메모리 내 및 브라우저에서 수행됩니다.
* **애플리케이션 성능 향상** 실험을 실행하고 최종 사용자 경험을 그대로 유지하면서 고객과 사용자에게 개인화를 전달할 수 있습니다.
* **Google 사이트 품질 점수를 개선합니다.** 메모리 내에서 의사 결정이 이루어지면 온라인 비즈니스의 Google 사이트 품질 점수를 높여 고객이 보다 손쉽게 찾을 수 있도록 하십시오.
* **실시간 분석을 통해 학습** Target [(A4T) 보고를 위한 ](/help/c-integrating-target-with-mac/a4t/a4t.md) Analytics를 통해 활동 성능을 실시간으로 통찰력을 얻을 수 있습니다. A4T를 사용하면 중요한 순간에 전략을 조정할 수 있습니다.

## 지원되는 기능

Adobe Target JS SDK는 고객이 결정을 위한 데이터의 최신 성능과 성능 중에서 선택할 수 있는 유연성을 제공합니다. 즉, 머신 러닝을 통해 관련성이 높고 매력적인 개인화된 콘텐츠를 전달하는 것이 가장 중요한 경우 라이브 서버를 호출해야 합니다. 그러나 성능이 더 중요한 경우 디바이스와 메모리 내 의사 결정을 내려야 합니다. 장치 내 의사 결정이 작동하려면 지원되는 기능 목록을 참조하십시오.

* 활동 유형
* 고객 타깃팅
* 할당 방법

자세한 내용은 [장치 내 의사 결정에 지원되는 기능](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md)을 참조하십시오.

## 디바이스 내 의사 결정은 어떻게 이루어집니까?

장치 내 의사 결정이 활성화된 상태에서 at.js를 배포 및 초기화하면 A/B 및 XT 활동, 대상 및 자산에 대한 장치 내 의사 결정이 포함된 [규칙 아티팩트](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md)가 방문자에게 가장 가까운 Akamai CDN에서 다운로드되고 방문자의 브라우저에 로컬로 캐시됩니다. at.js에서 경험을 검색하기 위해 요청을 할 때, 반환할 경험에 대한 결정은 캐시된 규칙 가공물에 인코딩된 메타데이터를 기반으로 메모리 내에서 수행됩니다.

## 의사 결정 방법

장치 내 의사 결정 시 [!DNL Target]에서는 [!UICONTROL 의사 결정 방법]이라는 새 설정을 소개합니다. [!UICONTROL 의사 결정 메서드] 설정은 at.js가 경험을 제공하는 방법을 나타냅니다. [!UICONTROL 의사 결정 ] 방법에는 3개의 값이 있습니다.

* [!UICONTROL 서버측 전용]
* [!UICONTROL 온디바이스 전용]
* [!UICONTROL 하이브리드]

### 서버측 전용

[!UICONTROL 서버측] 은 at.js 2.5.0+이 웹 속성에 구현되어 배포될 때 기본적으로 설정되어 있는 기본 의사 결정 방식입니다.

기본 구성으로 [!UICONTROL 서버측 전용]을 사용하는 것은 차단 서버 호출을 포함하는 [!DNL Target] 에지 네트워크에서 모든 결정을 한다는 것을 의미합니다. 이 접근 방식에서는 증분 지연을 도입할 수 있지만, [Recommendations](/help/c-recommendations/recommendations.md), [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md)(AP) 및 [자동 Target](/help/c-activities/auto-target/auto-target-to-optimize.md) 활동을 포함하는 Target의 기계 학습 기능을 적용할 수 있는 등 상당한 이점을 제공합니다.

또한 다양한 세션과 채널에서 지속되는 Target의 사용자 프로필을 사용하여 개인화된 경험을 강화하면 비즈니스에 강력한 결과를 제공할 수 있습니다.

마지막으로 [!UICONTROL 서버측 전용]을 사용하면 Adobe Experience Cloud을 사용하고 Audience Manager 및 Adobe Analytics 세그먼트를 통해 타깃팅할 수 있는 대상을 미세 조정할 수 있습니다.

다음 다이어그램은 방문자, 브라우저, at.js 2.5.0+ 및 Adobe Target Edge 네트워크 간의 상호 작용을 보여 줍니다. 이 흐름 다이어그램은 새 방문자 및 돌아온 방문자를 캡처합니다.

![서버측 전용 흐름 다이어그램](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/server-side-only.png)

다음 목록은 다이어그램의 번호에 해당합니다.

| 단계 | 설명 |
| --- | --- |
| 1 | [!DNL Experience Cloud Visitor ID]은(는) [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en)에서 검색됩니다. |
| 2 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>   at.js 라이브러리는 페이지에 구현된 선택적 사전 숨기기 조각을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 3 | at.js 라이브러리는 깜박거리는 것을 방지하기 위해 몸을 숨깁니다. |
| 4 | 페이지 로드 요청은 (ECID, 고객 ID, 사용자 지정 매개 변수, 사용자 프로필 등)과 같이 구성된 모든 매개 변수를 포함하는 것입니다. |
| 5 | 프로필 스크립트가 실행된 다음 프로필 저장소에 반영됩니다.<br>프로필 저장소는 대상 라이브러리에서 자격이 있는 대상자(예: 공유 대상  [!DNL Adobe Analytics]등) [!DNL Adobe Audience Manager]를 요청합니다.<br>고객 속성은 묶음 프로세스를 통해 프로필 저장소로 전송됩니다. |
| 6 | 프로필 스토어는 대상 자격 조건 및 버킷으로 활동을 필터링하는 데 사용됩니다. |
| 7 | 결과 컨텐츠는 라이브 [!DNL Target] 활동에서 경험이 결정된 후에 선택됩니다. |
| 8 | at.js 라이브러리는 렌더링해야 하는 경험과 연결된 페이지의 해당 요소를 숨깁니다. |
| 9 | at.js 라이브러리에는 방문자가 볼 수 있도록 페이지의 나머지 부분을 로드할 수 있도록 본문이 표시됩니다. |
| 10 | at.js 라이브러리는 Target 에지 네트워크에서 경험을 렌더링하기 위해 DOM을 조작합니다. |
| 11 | 경험은 방문자에게 렌더링됩니다. |
| 12 | 전체 웹 페이지가 로드됩니다. |
| 13 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. |
| 14 | 대상 데이터는 SDID를 통해 [!DNL Analytics] 데이터와 일치하고 [!DNL Analytics] 보고 저장소로 처리됩니다. 그런 다음 [!DNL Analytics] 데이터는 [!DNL Analytics] for [!DNL Target](A4T) 보고서를 통해 [!UICONTROL Analytics 및 ]Target 모두에서 볼 수 있게 됩니다. |

### 온디바이스 전용

[!UICONTROL 온디바이스는 ] 온디바이드 의사 결정이 웹 페이지 전체에서 사용되어야 하는 경우 at.js 2.5.0+에서 설정해야 하는 의사 결정 방식입니다.

디바이스에서 의사 결정을 내릴 수 있는 모든 활동을 포함하는 캐시된 규칙 아티팩트로 의사 결정을 내림으로써 경험 및 개인화 활동을 빠른 속도로 전달할 수 있습니다.

장치 내 의사 결정을 위한 자격이 되는 활동에 대한 자세한 내용은 [장치 내 의사 결정에서 지원되는 기능](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md)을 참조하십시오.

이 의사 결정 방법은 [!DNL Target]의 결정이 필요한 모든 페이지에서 성능이 매우 중요한 경우에만 사용해야 합니다. 또한 이 의사 결정 방법을 선택하면 장치에서 의사 결정을 할 수 없는 [!DNL Target] 활동이 전달되거나 실행되지 않습니다. at.js 라이브러리 2.5.0+은 결정을 내릴 캐시된 규칙 아티팩트만 찾도록 구성되어 있습니다.

다음 다이어그램은 방문자, 브라우저, at.js 2.5.0+ 및 Akamai CDN 간의 상호 작용을 보여 줍니다. Akamai CDN은 방문자의 첫 번째 방문에 대한 규칙 아티팩트를 캐시합니다. 새 방문자에 대한 첫 번째 페이지 방문의 경우 Akamai CDN에서 JSON 규칙 아티팩트를 다운로드하여 방문자의 브라우저에 로컬로 캐시해야 합니다. JSON 규칙 아티팩트가 다운로드된 후 네트워크 호출 차단 없이 즉시 결정이 수행됩니다. 다음 흐름 다이어그램은 새 방문자를 캡처합니다.

![장치 전용 흐름 다이어그램](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only.png)

다음 목록은 다이어그램의 번호에 해당합니다.

>[!NOTE]
>
>[!DNL Adobe Target] 관리 서버는 장치 내 의사 결정에 적합한 모든 활동을 평가하고, JSON 규칙 아티팩트를 생성하고, 이를 Akamai CDN에 전파합니다. Akamai CDN에 전파될 새 JSON 규칙 아티팩트를 출력하기 위한 업데이트를 지속적으로 활동이 모니터링됩니다.

| 단계 | 설명 |
| --- | --- |
| 1 | [!DNL Experience Cloud Visitor ID]은(는) [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html)에서 검색됩니다. |
| 2 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>at.js 라이브러리는 페이지에 구현된 선택적 사전 숨기기 조각을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 3 | at.js 라이브러리는 깜박거리는 것을 방지하기 위해 몸을 숨깁니다. |
| 4 | at.js 라이브러리는 가장 가까운 Akamai CDN에서 방문자에게 JSON 규칙 아티팩트를 검색하도록 요청합니다. |
| 5 | Akamai CDN이 JSON 규칙 아티팩트와 응답합니다. |
| 6 | JSON 규칙 아티팩트는 방문자의 브라우저에서 로컬로 캐시됩니다. |
| 7 | at.js 라이브러리는 JSON 규칙 아티팩트를 해석하고 경험 검색 결정을 실행하며 테스트된 요소를 숨깁니다. |
| 8 | at.js 라이브러리에는 방문자가 볼 수 있도록 페이지의 나머지 부분을 로드할 수 있도록 본문이 표시됩니다. |
| 9 | at.js 라이브러리는 캐시된 JSON 규칙 아티팩트에서 경험을 렌더링하기 위해 DOM을 조작합니다. |
| 10 | 경험은 방문자에게 렌더링됩니다. |
| 11 | 전체 웹 페이지가 로드됩니다. |
| 12 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. 대상 데이터는 SDID를 통해 [!DNL Analytics] 데이터와 일치하고 [!DNL Analytics] 보고 저장소로 처리됩니다. 그런 다음 [!DNL Analytics][!DNL Analytics] 데이터는 for  (A4T) 보고서를 통해 Analytics 및 Target 모두에서 볼 수 있게 됩니다.[!DNL Target] |

다음 다이어그램은 방문자의 후속 페이지 히트 또는 재방문에 대한 방문자, 브라우저, at.js 2.5.0+ 및 캐시된 JSON 규칙 가공물 간의 상호 작용을 보여 줍니다. JSON 규칙 아티팩트는 이미 캐시되어 브라우저에서 사용할 수 있으므로, 차단 네트워크 호출 없이 즉시 결정됩니다. 이 흐름 다이어그램은 후속 페이지 탐색 또는 돌아온 방문자를 캡처합니다.

![후속 페이지 탐색 및 반복 방문을 위한 장치 내 흐름 다이어그램](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only-subsequent.png)

다음 목록은 다이어그램의 번호에 해당합니다.

>[!NOTE]
>
>[!DNL Adobe Target] 관리 서버는 장치 내 의사 결정에 적합한 모든 활동을 평가하고, JSON 규칙 아티팩트를 생성하고, 이를 Akamai CDN에 전파합니다. Akamai CDN에 전파될 새 JSON 규칙 아티팩트를 출력하기 위한 업데이트를 지속적으로 활동이 모니터링됩니다.

| 단계 | 설명 |
| --- | --- |
| 3 | [!DNL Experience Cloud Visitor ID]은(는) [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html)에서 검색됩니다. |
| 2 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>at.js 라이브러리는 페이지에 구현된 선택적 사전 숨기기 조각을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 1 | at.js 라이브러리는 깜박거리는 것을 방지하기 위해 몸을 숨깁니다. |
| 4 | at.js 라이브러리는 JSON 규칙 아티팩트를 해석하고 메모리 내에서 결정을 실행하여 경험을 검색합니다. |
| 5 | 테스트된 요소는 숨겨집니다. |
| 6 | at.js 라이브러리에는 방문자가 볼 수 있도록 페이지의 나머지 부분을 로드할 수 있도록 본문이 표시됩니다. |
| 7 | at.js 라이브러리는 캐시된 JSON 규칙 아티팩트에서 경험을 렌더링하기 위해 DOM을 조작합니다. |
| 8 | 경험은 방문자에게 렌더링됩니다. |
| 9 | 전체 웹 페이지가 로드됩니다. |
| 10 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. 대상 데이터는 SDID를 통해 [!DNL Analytics] 데이터와 일치하고 [!DNL Analytics] 보고 저장소로 처리됩니다. 그런 다음 [!DNL Analytics] 데이터는 [!DNL Analytics] for [!DNL Target](A4T) 보고서를 통해 [!UICONTROL Analytics 및 ]Target 모두에서 볼 수 있게 됩니다. |

### 하이브리드

[!UICONTROL Adobe Target Edge 네트워크에 대한 네트워크 호출이 필요한 ] 장치 내 의사 결정 및 활동 모두 실행 시 at.js 2.5.0+에서 설정해야 하는 의사 결정 방법을 하이브리드합니다.

장치 내 의사 결정 활동과 서버측 활동을 모두 관리하는 경우 페이지에 [!DNL Target]을(를) 배포하고 프로비저닝하는 방법을 생각하면 다소 복잡하고 지루할 수 있습니다. 의사 결정 방법으로 하이브리드 경우 [!DNL Target]은 서버측 실행이 필요한 작업과 장치 내 의사 결정만 실행할 시기를 Adobe Target Edge 네트워크에 서버 호출을 지정해야 하는 시기를 알고 있습니다.

JSON 규칙 아티팩에는 at.js에 mbox가 실행 중인 서버측 활동 또는 장치 내 의사 결정 활동을 가지고 있는지 알리는 메타데이터가 포함되어 있습니다. 이 의사 결정 방법을 사용하면 신속하게 전달하려는 활동이 장치 내 의사 결정을 통해 이루어지며 보다 강력한 ML 기반의 개인화가 필요한 활동에 대해 이러한 활동이 Adobe Target Edge 네트워크를 통해 이루어집니다.

다음 다이어그램은 처음 페이지를 방문하는 신규 방문자를 위한 방문자, 브라우저, at.js 2.5.0+, Akamai CDN 및 Adobe Target Edge Network 간의 상호 작용을 보여줍니다. 이 다이어그램에서 테이크아웃은 JSON 규칙 아티팩트를 Adobe Target Edge 네트워크를 통해 비동기식으로 다운로드하는 것입니다.

이 방법을 사용하면 많은 활동을 포함할 수 있는 가공물의 크기가 의사 결정 지연에 부정적인 영향을 주지 않습니다. JSON 규칙 아티팩트를 동기적으로 다운로드하고 이후 결정을 내리면 지연에 부정적인 영향을 줄 수 있으며 일관되지 않을 수 있습니다. 따라서 하이브리드 의사 결정 방법은 새 방문자에 대한 의사 결정을 항상 서버측 호출로 하고 JSON 규칙 아티팩트가 동시에 캐싱될 때 권장되는 최상의 방법입니다. 이후 모든 페이지 방문 및 재방문 횟수에 대해 JSON 규칙 아티팩트를 통해 캐시 및 메모리 내 결정을 합니다.

![최초 방문자를 위한 하이브리드 흐름 다이어그램](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-first-time-visitor.png)

다음 목록은 다이어그램의 번호에 해당합니다.

>[!NOTE]
>
>[!DNL Adobe Target] 관리 서버는 장치 내 의사 결정에 적합한 모든 활동을 평가하고, JSON 규칙 아티팩트를 생성하고, 이를 Akamai CDN에 전파합니다. Akamai CDN에 전파될 새 JSON 규칙 아티팩트를 출력하기 위한 업데이트를 지속적으로 활동이 모니터링됩니다.

| 단계 | 설명 |
| --- | --- |
| 1 | [!DNL Experience Cloud Visitor ID]은(는) [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html)에서 검색됩니다. |
| 2 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>at.js 라이브러리는 페이지에 구현된 선택적 사전 숨기기 조각을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 3 | at.js 라이브러리는 깜박거리는 것을 방지하기 위해 몸을 숨깁니다. |
| 4 | 페이지 로드 요청은 Adobe Target Edge Network에 수행됩니다. 여기에는 ECID, 고객 ID, 사용자 지정 매개 변수, 사용자 프로필 등의 모든 구성 매개 변수가 포함됩니다. |
| 5 | 이와 동시에 at.js는 가장 가까운 Akamai CDN에서 방문자에게 JSON 규칙 아티팩트를 검색하도록 요청합니다. |
| 6 | (Adobe Target Edge Network) 프로필 스크립트가 실행된 다음 프로필 스토어로 피드됩니다. 프로필 저장소는 대상 라이브러리에서 자격이 있는 대상(예: [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] 등에서 공유된 대상)을 요청합니다. |
| 7 | Akamai CDN이 JSON 규칙 아티팩트와 응답합니다. |
| 8 | 프로필 스토어는 대상 자격 조건 및 버킷으로 활동을 필터링하는 데 사용됩니다. |
| 9 | 결과 컨텐츠는 라이브 [!DNL Target] 활동에서 경험이 결정된 후에 선택됩니다. |
| 10 | at.js 라이브러리는 렌더링해야 하는 경험과 연결된 페이지의 해당 요소를 숨깁니다. |
| 11 | at.js 라이브러리에는 방문자가 볼 수 있도록 페이지의 나머지 부분을 로드할 수 있도록 본문이 표시됩니다. |
| 12 | at.js 라이브러리는 Target 에지 네트워크에서 경험을 렌더링하기 위해 DOM을 조작합니다. |
| 13 | 경험은 방문자에게 렌더링됩니다. |
| 14 | 전체 웹 페이지가 로드됩니다. |
| 15 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. 대상 데이터는 SDID를 통해 [!DNL Analytics] 데이터와 일치하고 [!DNL Analytics] 보고 저장소로 처리됩니다. 그런 다음 [!DNL Analytics] 데이터는 [!DNL Analytics] for [!DNL Target](A4T) 보고서를 통해 [!UICONTROL Analytics 및 ]Target 모두에서 볼 수 있게 됩니다. |

다음 다이어그램은 후속 페이지 탐색 또는 재방문에 대한 방문자, 브라우저, at.js 2.5.0+ 및 캐시된 JSON 규칙 가공물 간의 상호 작용을 보여 줍니다. 이 다이어그램에서는 다음 페이지 탐색 또는 방문 재방문에 대해 장치에서 결정하는 사용 사례에만 초점을 둡니다. 특정 페이지에 대해 라이브되는 활동에 따라 서버측 호출을 수행하여 서버측 결정을 실행할 수 있습니다.

![후속 페이지 탐색 및 반복 방문을 위한 하이브리드 흐름 다이어그램](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-subsequent.png)

다음 목록은 다이어그램의 번호에 해당합니다.

>[!NOTE]
>
>[!DNL Adobe Target] 관리 서버는 장치 내 의사 결정에 적합한 모든 활동을 평가하고, JSON 규칙 아티팩트를 생성하고, 이를 Akamai CDN에 전파합니다. Akamai CDN에 전파될 새 JSON 규칙 아티팩트를 출력하기 위한 업데이트를 지속적으로 활동이 모니터링됩니다.

| 단계 | 설명 |
| --- | --- |
| 3 | [!DNL Experience Cloud Visitor ID]은(는) [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html)에서 검색됩니다. |
| 2 | at.js 라이브러리는 동기식으로 로드되며 문서 본문을 숨깁니다.<br>at.js 라이브러리는 페이지에 구현된 선택적 사전 숨기기 조각을 사용하여 비동기식으로 로드할 수도 있습니다. |
| 1 | at.js 라이브러리는 깜박거리는 것을 방지하기 위해 몸을 숨깁니다. |
| 4 | 경험을 검색하도록 요청합니다. |
| 5 | at.js 라이브러리는 JSON 규칙 아티팩트가 이미 캐싱되었음을 확인하고 경험을 검색하기 위해 메모리 내 결정을 실행합니다. |
| 6 | 테스트된 요소는 숨겨집니다. |
| 7 | at.js 라이브러리에는 방문자가 볼 수 있도록 페이지의 나머지 부분을 로드할 수 있도록 본문이 표시됩니다. |
| 8 | at.js 라이브러리는 캐시된 JSON 규칙 아티팩트에서 경험을 렌더링하기 위해 DOM을 조작합니다. |
| 9 | 경험은 방문자에게 렌더링됩니다. |
| 10 | 전체 웹 페이지가 로드됩니다. |
| 11 | [!DNL Analytics] 데이터가 데이터 수집 서버로 전송됩니다. 대상 데이터는 SDID를 통해 [!DNL Analytics] 데이터와 일치하고 [!DNL Analytics] 보고 저장소로 처리됩니다. 그런 다음 [!DNL Analytics] 데이터는 [!DNL Analytics] for [!DNL Target](A4T) 보고서를 통해 [!UICONTROL Analytics 및 ]Target 모두에서 볼 수 있게 됩니다. |

## 장치 내 의사 결정을 활성화하려면 어떻게 합니까?

장치 내 의사 결정은 At.js 2.5.0+을 사용하는 모든 [!DNL Target] 고객에게 제공됩니다.

장치 내 의사 결정을 활성화하려면:

>[!NOTE]
>
>장치 내 의사 결정 전환을 활성화 또는 비활성화하려면 [!UICONTROL 관리] 또는 [!UICONTROL 승인자] [사용자 역할](/help/administrating-target/c-user-management/user-management.md)이 있어야 합니다.

1. **[!UICONTROL 관리]** > **[!UICONTROL 구현]** > **[!UICONTROL 계정 세부 정보]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 계정 세부 사항]**&#x200B;에서 **[!UICONTROL 장치 내 의사 결정]**&#x200B;을 &quot;설정&quot; 위치로 끕니다.

   ![장치 내 의사 결정 전환](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-toggle.png)

   장치 내 의사 결정을 활성화하면 &quot;[!UICONTROL 가공물]&quot;에 기존의 모든 장치 내 의사 결정 자격 증명 포함 옵션이 표시됩니다.
1. (조건부) 장치 내 의사 결정을 위한 자격이 되는 모든 라이브 Target 활동을 아티팩트에 자동으로 포함하려면 토글을 &quot;켜기&quot; 위치로 밀십시오.

   이 토글을 끄면 생성된 규칙 가공물에 포함되도록 모든 장치 내 의사 결정 활동을 다시 만들고 활성화해야 합니다. 즉, [!UICONTROL 장치 내 의사 결정] 전환을 켜기 전에 라이브 상태의 모든 활동은 규칙 아티팩트에 포함되지 않습니다.

[!UICONTROL 장치 내 의사 결정] 토글을 활성화한 후 [!DNL Target]에서 클라이언트에 대해 [규칙 가공물](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md)을 생성하고 전파하기 시작합니다.

>[!IMPORTANT]
>
>Adobe Target SDK를 초기화하여 장치 내 의사 결정을 사용하려면 먼저 전환을 활성화해야 합니다. 규칙 가공물은 먼저 장치 내 의사 결정을 위해 Akamai CDN을 생성하여 전파해야 합니다. 전파에는 첫 번째 규칙 아티팩트가 생성 및 Akamai CDN에 전파되는 데 5~10분이 걸릴 수 있습니다.

## 장치 내 의사 결정을 사용하도록 at.js 2.5.0+을 구성하려면 어떻게 합니까?

1. **[!UICONTROL 관리]** > **[!UICONTROL 구현]** > **[!UICONTROL 계정 세부 정보]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 구현 메서드]** > **[!UICONTROL 기본 구현 메서드]**&#x200B;에서 at.js 버전 옆에 있는 **[!UICONTROL 편집]**&#x200B;을 클릭합니다(at.js 2.5.0 이상).

   ![기본 구현 방법 설정 편집](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/main-implementation-method.png)

   >[!IMPORTANT]
   >
   >이러한 기본 설정을 변경하기 전에 현재 구현에 영향을 미치지 않도록 클라이언트 지원 팀에 문의하십시오.

1. 원하는 의사 결정 방법을 선택합니다.

   * [!UICONTROL 서버측 전용]
   * [!UICONTROL 온디바이스 전용]
   * [!UICONTROL 하이브리드]

   ![at.js 설정 패널 편집](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/global-settings.png)

### 전역 설정

모든 [!DNL Target] 결정에 대해 기본 [!UICONTROL 의사 결정 방법]을 구성할 수 있습니다. 다양한 의사 결정 방법은 [!UICONTROL 서버측 전용], [!UICONTROL 장치 전용] 및 [!UICONTROL 하이브리드]입니다. Target UI에서 선택한 의사 결정 방법은 `decisioningMethod` 필드 아래의 `window.targetGlobalSettings`에 구성됩니다. [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)의 `decisioningMethod`에 대해 자세히 알아보십시오.

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

`window.targetGlobalSettings`에서 `decisioningMethod`을 설정했지만 사용 사례에 따라 각 Adobe Target 결정에 대해 `decisioningMethod`을(를) 재정의하려는 경우 At.js2.5.0+의 [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) 호출에 `decisioningMethod`을(를) 지정하여 이 절차를 수행할 수 있습니다.

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
>getOffers() 호출의 의사 결정 메서드로 &quot;on-device&quot; 또는 &quot;hybrid&quot;를 사용하려면 전역 설정에 `decisioningMethod`이(가) &quot;on-device&quot; 또는 &quot;hybrid&quot;인지 확인하십시오. at.js 라이브러리 2.5.0+은 페이지에 로드된 후 즉시 JSON 규칙 아티팩트를 다운로드하고 캐시할 것인지 알아야 합니다. 전역 설정에 대한 의사 결정 메서드가 &quot;서버측&quot;으로 설정되어 있고 &quot;장치에서 온-장치&quot; 또는 &quot;하이브리드&quot; 의사 결정 메서드가 getOffers() 호출로 전달되는 경우, at.js 2.5.0+에는 장치 내 결정을 실행하기 위해 캐시된 JSON 규칙 아티팩트가 없습니다.

### 가공물 캐시 TTL

[!DNL Target] 은 메타데이터, 규칙 및 조건으로 구성된 아티팩트로서 장치 내 의사 결정을 평가하는 활동을 나타냅니다. 이 가공물은 Akamai CDN에 캐시됩니다. 사용자가 처음 방문하는 동안 사용자의 브라우저가 장치 내 의사 결정 활동을 나타내는 객체를 다운로드하고 캐시합니다.

이후 사이트를 방문하면 브라우저가 해당 객체의 최신 버전을 다운로드해야 하는지 여부를 자동으로 확인합니다. 이 확인은 지연을 추가합니다. Artifact Cache TTL은 마지막으로 성공한 다운로드 이후 브라우저가 업데이트된 아티팩트를 확인할 시간을 분 단위로 정의합니다. 기간이 길수록 성능이 향상됩니다. 시간대가 짧을수록 데이터 신선도가 향상되지만 지연 시간이 더 오래 걸립니다.

## 활동이 장치 내 의사 결정 자격이 되는지 어떻게 알 수 있습니까?

장치 내 의사 결정 자격이 있는 활동을 만든 후 [!UICONTROL 장치 내 의사 결정 자격 조건]을 읽는 레이블이 활동의 [!UICONTROL 개요] 페이지에 표시됩니다.

![장치 내 의사 결정 활동의 개요 페이지에 있는 적격한 레이블.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-eligible-label.png)

이 레이블은 활동이 항상 장치 내 결정을 통해 전달된다는 것을 의미하지 않습니다. at.js 2.5.0+이 장치 내 의사 결정을 사용하도록 구성된 경우에만 이 활동이 장치에서 실행됩니다. at.js 2.5.0+이 온디바이스를 사용하도록 구성되어 있지 않은 경우, 이 활동은 at.js에서 만들어진 서버 호출을 통해 여전히 전달됩니다.

[!UICONTROL 장치 내 의사 결정 자격 조건] 필터를 통해 [!UICONTROL 활동] 페이지에 적격한 장치 내 의사 결정 관련 모든 활동을 필터링할 수 있습니다.

![활동 페이지에 대한 장치 내 의사 결정 자격 필터.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-filter.png)

>[!NOTE]
>
>장치 내 의사 결정 자격이 있는 활동을 만들고 활성화한 후에는 생성 및 Akamai CDN 프레젠테이션의 Point of Presence로 전파되는 규칙 아티팩트에 포함되기 전에 5~10분이 걸릴 수 있습니다.

## 내 장치 내 의사 결정 활동이 At.js 2.5.0을 통해 전달되도록 하는 단계 요약

1. Adobe Target UI에 액세스하고 **[!UICONTROL 관리]** > **[!UICONTROL 구현]** > **[!DNL Account Details]**&#x200B;으로 이동하여 **[!UICONTROL 장치 내 의사 결정]** 전환을 활성화합니다.
1. **&quot;[!UICONTROL 가공물]&quot;** 토글에서 검증된 모든 기존 장치 내 의사 결정 활동 포함

   첫 번째 JSON 규칙 아티팩트 생성이 최대 10분 정도 걸릴 수 있습니다.

1. 장치 내 의사 결정](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md)에서 지원하는 [활동 유형을 만들고 활성화하고 장치 내 의사 결정이 적절한지 확인합니다.
1. at.js 설정 UI를 통해 **[!UICONTROL 의사 결정 메서드]**&#x200B;를 **[!UICONTROL &quot;Hybrid&quot;]** 또는 **[!UICONTROL &quot;장치에서 On-device 전용&quot;]**&#x200B;으로 설정합니다.
1. At.js 2.5.0+을 다운로드하여 페이지에 배포합니다.
