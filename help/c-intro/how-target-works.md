---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;검색 엔진 최적화;검색 엔진 최적화;seo;에지 클러스터, 중앙 클러스터;at.js;mbox.js;
description: Adobe [!DNL Target] works, including information about the [!DNL Target] JavaScript 라이브러리(at.js 및 Experience Platform 웹 SDK), Adobe 데이터 센터 및 SEO 테스트 방법을 알아봅니다.
title: ' [!DNL Target] 은 어떻게 작동합니까?'
feature: 개요
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '2532'
ht-degree: 95%

---

# Adobe [!DNL Target] 작동 방식

[!DNL Adobe Experience Platform Web SDK] 및 JavaScript 라이브러리(at.js 및 mbox.js)에 대한 정보를 포함하여 [!DNL Adobe Target] 의 작동 방식을 알아보십시오. 본 문서에서는 [!DNL Target]을 사용하여 작성할 수 있는 다양한 활동 유형도 소개합니다. [!DNL Target] 에지 네트워크, SEO(검색 엔진 최적화) 및 [!DNL Target] 이 봇을 탐지하는 방법에 대해서도 배울 수 있습니다.

## [!DNL Target] Platform Web SDKs 및 JavaScript 라이브러리 {#libraries}

[!DNL Target] 은 [!DNL Experience Platform Web SDK] 또는 JavaScript 라이브러리를 사용하여 웹 사이트와 통합합니다.

* **Adobe Experience Platform Web SDK:**  [Experience Platform 웹 ](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) SDK는 새로운 클라이언트측 JavaScript 라이브러리입니다. Experience Platform 웹 SDK를 사용하면 [!DNL Adobe Experience Cloud] 고객이 [!DNL Experience Platform] Edge Network를 통해 [!DNL Experience Cloud]([!DNL Target] 포함)의 다양한 서비스와 상호 작용할 수 있습니다. Adobe는 모든 신규 [!DNL Target] 고객에게 [!DNL Experience Platform Web SDK]를 구현할 것을 권장합니다.
* **at.js:** at.js 라이브러리 는 [!DNL Target]의 새 구현 라이브러리입니다. at.js 라이브러리는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 단일 페이지 애플리케이션에 대해 더 나은 구현 옵션을 제공합니다. at.js는 새로운 기능으로 자주 업데이트됩니다. Adobe는 at.js를 사용하는 모든 고객에게 [at.js의 최신 버전](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)으로 구현을 업데이트할 것을 권장합니다.
* **mbox.js:** mbox.js 라이브러리 는 [!DNL Target]의 레거시 구현 라이브러리입니다. mbox.js 라이브러리는 2021년 3월 31일 이후로 더 이상 지원되지 않습니다.

사이트의 모든 페이지에서 [!DNL Experience Platform Web SDK] 또는 at.js를 참조하십시오. 예를 들어 이러한 라이브러리 중 하나를 글로벌 헤더에 추가할 수 있습니다. 또는 [Adobe Platform Launch](https://experienceleague.adobe.com/docs/launch/using/overview.html?lang=ko-KR) 를 사용하여 [!DNL Target]을 구현하는 것을 고려하시오.

다음 리소스에는 Experience Platform 웹 SDK 또는 at.js를 구현하는 데 도움이 되는 자세한 정보가 포함되어 있습니다.

* [Adobe Experience Platform Web SDK Extension](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html?lang=ko-KR#configure-the-aep-web-sdk-extension)
* [ [!DNL Target] Adobe Experience Platform Launch를 사용한 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)

방문자가 [!DNL Target]에 최적화된 페이지를 요청할 때마다 타기팅 시스템으로 요청이 전송됩니다. 요청은 방문자에게 제공할 콘텐츠를 결정하는 데 도움이 됩니다. 이 프로세스는 실시간으로 발생합니다. 페이지가 로드될 때마다 콘텐츠 요청이 이루어지고 시스템에 의해 이행됩니다. 콘텐츠는 마케터가 관리하는 활동 및 경험의 규칙이 적용되며, 개별 사이트 방문자를 타기팅합니다. 각 사이트 방문자가 응답하거나, 상호 작용하거나, 궁극적으로는 구매할 가능성이 가장 높은 콘텐츠가 제공됩니다. 개인화된 콘텐츠를 통해 응답률, 확보율 및 매출을 극대화할 수 있습니다.

[!DNL Target]에서 페이지의 각 요소는 전체 페이지를 위한 단일 경험의 일부입니다. 각 경험은 페이지에 여러 요소를 포함할 수 있습니다.

방문자에게 표시되는 콘텐츠는 사용자가 작성하는 활동의 유형에 따라 다릅니다.

### [!UICONTROL A/B 테스트]

기본 A/B 테스트에 표시되는 콘텐츠는 활동에 할당하는 경험 중에서 임의로 선택됩니다. 각 경험에 대해 트래픽 할당 백분율을 할당할 수 있습니다. 이러한 트래픽 무작위 분할의 결과, 상당한 양의 초기 트래픽을 사용한 후에야 비율이 안정됩니다. 예를 들어 두 개의 경험을 만드는 경우 시작 경험이 무작위로 선택됩니다. 트래픽이 거의 없다면 방문자 비율이 하나의 경험으로 기울어질 수 있습니다. 트래픽이 증가하면 백분율이 같아집니다.

각 경험에 대해 비율 타겟을 지정할 수 있습니다. 이런 경우, 무작위 숫자가 생성되고 이 숫자를 사용하여 표시할 경험이 선택됩니다. 결과로 얻은 비율은 지정한 타겟과 정확하게 일치하지 않을 수도 있지만 더 많은 트래픽이 일어나면 경험이 타겟 목표에 더 가깝게 분할되어야 한다는 것을 의미합니다.

1. 고객이 서버에서 페이지를 요청하고 브라우저에 표시합니다.
1. 자사 쿠키가 고객 브라우저에 설정되어 고객 동작을 저장합니다.
1. 페이지가 타기팅 시스템을 호출합니다.
1. 활동의 규칙에 따라 콘텐츠가 표시됩니다.

자세한 내용은 [A/B 테스트 만들기](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) 를 참조하십시오.

### [!UICONTROL 자동 할당]

[!UICONTROL 자동 할당]은 둘 이상의 경험 중 우수성이 검증된 경험을 식별합니다. [!UICONTROL 자동 할당]은 더 많은 트래픽을 자동으로 우수성이 검증된 경험에 재할당하여 테스트를 계속 실행하고 학습하는 동안 전환을 늘리는 데 도움이 됩니다.

자세한 내용은 [[!UICONTROL 자동 할당]](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) 을 참조하십시오.

### [!UICONTROL 자동 타겟](AT)

자동 타겟은 고급 머신 러닝을 사용하여 여러 가지 고성능 마케터 정의 경험 중에서 선택합니다. 자동 타겟은 각 방문자에게 가장 적합한 경험을 제공합니다. 경험 전달은 개별 고객 프로필 및 유사한 프로필을 가진 이전 방문자의 행동을 기반으로 합니다. 자동 타겟을 사용하면 콘텐츠를 개인화하고 전환할 수 있습니다.

자세한 내용은 [자동 타겟](/help/c-activities/auto-target/auto-target-to-optimize.md) 을 참조하십시오.

### [!UICONTROL Automated Personalization] (AP)

AP (Automated Personalization)는 오퍼 또는 메시지를 결합하고 고급 머신 러닝을 사용하여 각 방문자에게 다양한 오퍼를 매칭합니다. 경험 전달은 콘텐츠를 개인화하고 리프트를 구동하기 위한 개별 고객 프로필을 기반으로 합니다.

자세한 내용은 [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) 를 참조하십시오.

### [!UICONTROL 경험 타기팅] (XT)

경험 타기팅 (XT) 에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상에 전달합니다.

지리 기반의 타기팅을 포함한 경험 타기팅은 특정 경험이나 콘텐츠를 특정 대상으로 타기팅하는 규칙을 정의할 때 유용합니다. 활동에서 여러 규칙을 정의하여 다른 대상에 다양한 콘텐츠 변형을 전달할 수 있습니다. 방문자가 사이트를 볼 때 XT (경험 타기팅)는 방문자를 평가하여 설정된 기준을 총족하는지 여부를 판단합니다. 기준을 충족하면 적격 대상을 위해 디자인된 활동 및 경험을 시작하게 됩니다. 단일 활동 내에서 여러 대상에 대한 경험을 만들 수 있습니다.

자세한 내용은 [경험 타기팅](/help/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4) 을 참조하십시오.

### [!UICONTROL 다변량 테스트] (MVT)

다변량 테스트 (MVT) 는 페이지의 요소 간에 오퍼 조합을 비교하여 특정 대상에 가장 뛰어난 조합을 결정합니다. MVT는 활동의 성공에 가장 큰 영향을 미치는 요소를 식별하는 데 도움이 됩니다.

자세한 내용은 [다변량 테스트](/help/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499) 를 참조하십시오.

### [!UICONTROL Recommendations]

권장 사항 활동은 이전 사용자 활동이나 기타 알고리즘을 기반으로 고객의 흥미를 끌 수 있는 제품이나 콘텐츠를 자동으로 표시합니다. 권장 사항은 고객이 모를 수 있는 관련 항목을 고객에게 표시하는 데 도움이 됩니다.

자세한 내용은 [권장 사항](/help/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) 을 참조하십시오.

## 에지 네트워크 {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

&quot;에지(Edge)&quot;는 콘텐츠를 요청하는 방문자자가 세계 어디에 있든지 상관없이 최적의 응답 시간을 보장하는 지리적으로 분산된 서비스 아키텍처입니다.

응답 시간을 향상시키기 위해 [!DNL Target] Edge는 활동 논리, 캐시된 프로필 및 오퍼 정보만 호스팅합니다.

활동 및 콘텐츠 데이터베이스, [!DNL Analytics] 데이터, API 및 마케터 사용자 인터페이스는 Adobe의 중앙 데이터 환경에 수용됩니다. 그러면 업데이트가 [!DNL Target] 에지로 전송됩니다. 중앙 클러스터 및 에지 클러스터는 자동으로 동기화되어 캐시된 활동 데이터를 계속 업데이트합니다. 모든 1:1 모델링도 각 에지에 저장되므로 이러한 더 복잡한 요청도 에지에서 처리될 수 있습니다.

각 에지 노드에는 방문자의 콘텐츠 요청에 응답하고, 해당 요청에 대한 분석 데이터를 추적하는 데 필요한 모든 정보가 있습니다. 방문자자 요청은 가장 가까운 에지 노드로 전달됩니다.

자세한 내용은 [Adobe Target Security Overview](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf) 백서를 참조하십시오.

[!DNL Target] 솔루션은 전 세계 Adobe 소유 및 Adobe 임대 데이터 센터에 호스팅됩니다.

중앙 클러스터 위치에는 데이터 수집 센터와 데이터 처리 센터가 모두 있습니다. 에지 클러스터 위치에는 데이터 수집 센터만 있습니다. 개별 보고서는 특정 데이터 처리 센터로 지정됩니다.

고객 사이트 활동 데이터는 7개의 에지 클러스터 중 가장 가까운 곳에서 수집됩니다. 이 데이터는 처리를 위해 고객이 미리 결정한 중앙 클러스터 대상(다음 세 위치 중 하나: 오레곤, 더블린, 싱가포르)으로 이동합니다. 방문자 프로필 데이터는 사이트 방문자와 가장 가까운 에지 클러스터에 저장됩니다. 에지 클러스터 위치에는 중앙 클러스터 위치와 버지니아, 뭄바이, 시드니 및 도쿄가 포함됩니다.

단일 위치에서 모든 타기팅 요청에 응답하는 대신 방문자와 가장 가까운 에지 클러스터에서 요청을 처리합니다. 이 프로세스는 네트워크/인터넷 이동 시간의 영향을 완화하는 데 도움이 됩니다.

![서로 다른 유형의 Target 서버를 표시하는 맵](/help/c-intro/assets/target-servers.png)

AWS(Amazon Web Services)에서 호스팅되는 [!DNL Target] 중앙 클러스터는 다음과 같습니다.

* 오레곤, 미국
* 더블린, 아일랜드
* 싱가포르

AWS(Amazon Web Services)에서 호스팅되는 [!DNL Target] 에지 클러스터는 다음과 같습니다.

* 뭄바이, 인도
* 도쿄, 일본
* 버지니아, 미국
* 오레곤, 미국
* 시드니, 오스트레일리아
* 더블린, 아일랜드
* 싱가포르

[!DNL Target Recommendations] 서비스는 오레곤의 [!DNL Adobe] 데이터 센터에서 호스팅됩니다.

>[!IMPORTANT]
>
>[!DNL Adobe Target] 은 현재 중국에 에지 클러스터를 보유하고 있지 않으며, 방문자 실적은 중국의 [!DNL Target] 고객에 한정되어 있습니다. 국가 내에서 방화벽과 에지 클러스터 부족으로 인해 [!DNL Target] 이 배포된 사이트의 환경이 영향을 받을 수 있습니다. 경험을 렌더링하기 위해 속도가 느릴 수 있으며 페이지 로드에 영향을 미칠 수 있습니다. 또한 마케터는 [!DNL Target] 작성 UI 사용 시 지연을 경험할 수 있습니다.

원하는 경우 [!DNL Target] 에지 클러스터를 허용 목록에 추가할 수 있습니다. 자세한 내용은 [Target 에지 노드를 허용 목록에 추가](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md)를 참조하십시오.

## 보호된 사용자 경험 {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

Adobe에서는 타기팅 인프라의 가용성 및 성능을 가능한 한 신뢰할 수 있도록 만들고 있습니다. 하지만 방문자의 브라우저와 Adobe의 서버 간 통신 실패로 인해 콘텐츠 전달이 중단될 수 있습니다.

서비스 중단 및 연결 문제를 방지하기 위해 모든 위치가 기본 콘텐츠(클라이언트에 의해 정의됨)를 포함하도록 설정됩니다. 사용자의 브라우저가 [!DNL Target]에 연결할 수 없는 경우 이 기본 내용이 표시됩니다.

사용자의 브라우저가 정의된 제한 시간 내(기본적으로 15초)에 연결할 수 없는 경우 페이지에 변경 사항이 적용되지 않습니다. 이 시간 초과 임계값에 도달하면 기본 위치 콘텐츠가 표시됩니다.

Adobe에서는 성능을 최적화 및 보호함으로써 사용자 경험을 보호합니다.

* Adobe는 Adobe 서비스 수준 계약(Service Level Agreement)으로 보장된 업계 표준을 기반으로 성과 벤치마크를 보장합니다.
* 에지 네트워크가 시기 적절한 데이터 전달을 보장합니다.
* Adobe는 애플리케이션 보호에 대한 다층적 접근 방식을 사용하여 고객을 위한 최고 수준의 가용성 및 안정성을 제공합니다.
* [!DNL Target] 컨설팅 팀에서는 구현 지원 및 지속적인 제품 지원 서비스를 제공합니다.

## SEO(검색 엔진 최적화) 친화도 테스트 {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target] 은 테스트를 위한 검색 엔진 지침을 따릅니다.

Google은 사용자 테스트를 권장합니다. Google은 해당 설명서를 통해 A/B 및 다변량 테스트에서 특정 지침을 따를 경우 유기 검색 엔진 랭킹에 영향을 주지 않는다고 명시하고 있습니다.

자세한 내용은 다음 Google 리소스를 참조하십시오.

* [웹 사이트 테스트 및 Google 검색](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [실험 및 클로킹](https://support.google.com/analytics/answer/2576845?hl=en&amp;ref_topic=1745207)

지침은 [Google 웹마스터 센터 블로그](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) 게시물에 나와 있습니다. 게시 날짜가 2012년까지 거슬러 올라가지만, 이 문제에 대한 Google의 최신 성명서이며 지침도 아직 적절합니다.

* **클로킹 없음**: 클로킹은 사용자에게 하나의 콘텐츠 세트와 검색 엔진 봇에 대한 다른 콘텐츠 세트를 보여 줍니다. 클로킹은 특별히 봇을 식별하고 의도적으로 다른 콘텐츠를 공급함으로써 이루어집니다.

   플랫폼인 [!DNL Target]은 검색 엔진 봇을 사용자와 동일하게 처리하도록 구성되었습니다. 결과적으로, 봇을 무작위로 선택하고 테스트 변형을 &quot;참조&quot;할 경우 봇은 활동에 포함될 수 있습니다.

* **rel=&quot;canonical&quot; 사용**: 때로 다양한 변형에 대한 다양한 URL을 사용하여 A/B 테스트를 설정해야 합니다. 이러한 경우, 모든 변형은 원래(통제) URL을 참조하는 `rel="canonical"` 태그를 포함해야 합니다. 예를 들어 Adobe가 각 변형에 대해 서로 다른 URL을 사용하여 홈 페이지를 테스트한다고 가정합시다. 홈 페이지에 대한 다음 표준 태그는 각 변형에 대해 `<head>` 태그로 지정됩니다.

   `<link rel="canonical" href="https://www.adobe.com" />`

* **302(임시) 리디렉션 사용**: 테스트에서 변형 페이지에 개별 URL이 사용되는 경우, Google에서는 302 리디렉션을 사용하여 트래픽을 테스트 변형으로 전달하는 것을 권장합니다. 302 리디렉션은 리디렉션이 임시적이며 테스트가 실행되는 동안에만 활성 상태임을 검색 엔진에 알려 줍니다.

   302 리디렉션은 서버측 리디렉션이며 대부분의 최적화 제공자와 함께 [!DNL Target]은 클라이언트측 기능을 사용합니다. 따라서 리디렉션은 [!DNL Target] 이 Google의 권장 사항을 완전히 준수하지 않는 영역입니다. 그러나 이 방법은 매우 일부 테스트에는 영향을 줍니다. [!DNL Target] 을 통해 테스트를 실행하는 이 표준 접근 방식은 단일 URL 내 콘텐츠 변경을 필요로 하므로 리디렉션이 필요하지 않습니다. 클라이언트가 여러 URL을 사용하여 테스트 변형을 표현해야 하는 경우가 있습니다. 이러한 경우 [!DNL Target] 은 JavaScript `window.location` 명령을 사용합니다. 이 명령은 리디렉션이 301인지 302인지를 명시적으로 나타내지 않는 변형을 테스트하도록 사용자에게 지시합니다.

   Adobe는 검색 엔진 지침에 완벽하게 부합할 수 있는 실행 가능한 솔루션을 계속 찾고 있습니다. 테스트를 위해 별도의 URL을 사용해야 하는 클라이언트의 경우, Adobe는 표준 태그의 적절한 구현이 이 접근법과 관련된 위험을 완화한다고 확신합니다.

* **필요한 동안만 실험 실행**: Adobe에서는 &quot;필요한 동안&quot;을 통계적 중요도에 도달하는 데 걸리는 시간 동안으로 생각합니다. [!DNL Target] 에서는 테스트가 이 시점에 도달했을 때를 판별하는 [모범 사례](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=ko-KR) 를 제공합니다. 가장 성과가 좋은 테스트의 하드코딩된 구현을 테스트 워크플로에 통합하고 적절한 리소스를 할당하는 것이 좋습니다.

   [!DNL Target] 플랫폼을 사용하여 가장 성과가 좋은 테스트를 &quot;게시&quot;하는 것은 영구적인 솔루션으로 권장되지 않습니다. 100% 사용자 중 100%에 대해 채택 테스트가 게시되면 채택 테스트를 하드 코딩하는 프로세스가 완료되는 동안 이 방법을 사용할 수 있습니다.

   테스트가 변경한 사항을 고려하는 것도 중요합니다. 페이지에 있는 버튼이나 기타 부수적인 비텍스트 기반 항목의 색상을 단순히 업데이트하는 것은 자연 순위에는 영향을 주지 않습니다. 하지만, 텍스트 변경 사항은 하드코딩해야 합니다.

   또한 테스트 중인 페이지의 액세서빌러티를 고려하는 것도 중요합니다. 페이지가 검색 엔진에 액세스할 수 없고 처음부터 유기 검색 순위에 오르게 설계된 적이 없는 경우 위의 고려 사항은 적용되지 않습니다. 한 가지 예는 이메일 캠페인 전용 랜딩 페이지입니다.

Google에서는 이러한 지침을 따르는 것이 &quot;테스트에서 검색 결과에 있는 여러분의 사이트에 영향을 거의 주지 않거나 전혀 주지 않는다&quot;고 명시합니다.

Google에서는 이 지침 외에도 콘텐츠 실험 도구에 대해 설명서에서 다음과 같은 지침을 하나 더 제공합니다.

* 대안 페이지는 원본 페이지의 콘텐츠와 본질적인 측면에서 동일해야 합니다. 원본 콘텐츠의 의미와 사용자가 원본 콘텐츠에서 인식하는 일반적인 개념이 대안 페이지에서 바뀌지 않는 것이 좋습니다.

Google에서는 한 예로 &quot;사이트의 원본 페이지를 로드한 키워드가 사용자에게 표시되는 조합과 관련이 없을 경우 Google은 해당 사이트를 Google 색인에서 제외할 수 있다&quot;고 명시하고 있습니다.

Adobe는 테스트 변형 내에서 원래 콘텐츠의 의미를 의도하지 않게 변경하기는 어렵다고 느끼고 있습니다. 그러나 페이지의 키워드 테마를 알고 해당 테마를 유지 관리하는 것이 좋습니다. 특히 관련 키워드를 추가하거나 삭제하는 등의 페이지 콘텐츠 변경은 자연 검색에서 URL에 대한 순위 변경을 초래할 수 있습니다. 테스트 프로토콜의 일부로서 SEO 파트너를 이용하는 것이 좋습니다.

## 보트 {#bots}

Adobe [!DNL Target] 은 [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/) 지표 &quot;isRobot&quot;을 사용하여 요청 헤더에 전달된 사용자 에이전트 문자열을 기반으로 알려진 봇을 탐지합니다.

>[!NOTE]
>
> [!DNL Server-Side] 요청의 경우 [요청의 &quot;컨텍스트&quot; 노드](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) 에 전달된 값이 봇 탐지를 위한 사용자 에이전트 문자열보다 우선합니다.

봇에 의해 생성되는 것으로 식별되는 트래픽은 여전히 콘텐츠로 제공됩니다. [!DNL Target] 이 SEO 지침에 부합하는지 확인하기 위해 봇은 일반 사용자처럼 취급됩니다. 봇 트래픽을 사용하면 일반 사용자로 취급되는 경우 A/B 테스트 또는 개인화 알고리즘을 왜곡할 수 있습니다. 따라서 알려진 봇이 [!DNL Target] 활동에서 감지되면 트래픽은 다소 다르게 처리됩니다. 봇 트래픽을 제거하면 사용자 활동을 보다 정확하게 측정할 수 있습니다.

특히 알려진 봇 트래픽 [!DNL Target] 의 경우 다음이 불가능합니다.

* 방문자 프로필 만들기 또는 검색
* 모든 프로필 속성 로깅 또는 프로필 스크립트 실행
* Adobe Audience Manager (AAM) 세그먼트 조회(해당하는 경우)
* 권장 사항, 자동 타겟, Automated Personalization 또는 [!UICONTROL 자동 할당] 활동에 대해 개인화된 콘텐츠를 모델링하고 제공하는 데 봇 트래픽을 사용합니다.
* 보고를 위한 활동 방문 로그
* [!DNL Adobe Experience Cloud] 플랫폼으로 전송될 로그 데이터
