---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;검색 엔진 최적화;검색 엔진 최적화;seo;에지 클러스터, 중앙 클러스터;at.js;mbox.js;
description: JavaScript 라이브러리(AEP Web SDK at.js), 서버 호출 사용 전략, 사용, Adobe 데이터 센터, SEO 테스트 및 봇에 대한 정보를 포함하여  [!DNL Adobe Target] 의 작동 방식에 대해 알아봅니다.
title: ' [!DNL Target] 은 어떻게 작동합니까?'
feature: Overview
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
source-git-commit: c5cca9b4b95289626ade1654bb508ee9f0bf35f3
workflow-type: tm+mt
source-wordcount: '2214'
ht-degree: 24%

---

# [!DNL Adobe Target] 작동 방식

JavaScript 라이브러리([!DNL Adobe Target] 및 at.js)에 대한 세부 사항을 포함하여 [!DNL Adobe Experience Platform Web SDK]의 작동 방식에 대해 알아봅니다. 이 문서에서는 만들 수 있는 다양한 활동 유형, [!DNL Target] 사용 계산 전략, [!DNL Target] Edge Network, SEO 및 봇 탐지도 다룹니다.

주요 내용은 다음과 같습니다.

* **JavaScript 라이브러리**: [!DNL Target] JavaScript 라이브러리 [!DNL Adobe Experience Platform Web SDK] 및 at.js에 대한 정보를 알아봅니다.
* **서버 호출 사용 전략**: [!DNL Target]에서 끝점, 단일 mbox, 일괄 처리 mbox, 실행, 미리 가져오기 및 알림 호출을 포함하여 다양한 서버 호출을 계산하는 방법을 이해합니다.
* **Edge Network**: [!DNL Target]이(가) [!DNL Adobe Experience Platform Edge Network]과(와) 상호 작용하는 방법을 알아봅니다.
* **보호된 사용자 경험**: [!DNL Adobe]이(가) 타깃팅 인프라의 가용성과 성능을 보장하는 방법을 알아봅니다.
* **SEO 지침**: [!DNL Target] 활동을 SEO 지침에 맞추기 위한 모범 사례를 따르십시오.
* **보트 트래픽**: Target에서 비대칭 테스트 및 개인화 알고리즘을 방지하기 위해 보트 트래픽을 처리하는 방법을 알아봅니다.

## [!DNL Adobe Target] JavaScript 라이브러리 {#libraries}

Target은 [!DNL Experience Platform Web SDK] 또는 at.js를 사용하여 웹 사이트와 통합됩니다.

* **[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}**: 이 클라이언트측 JavaScript 라이브러리를 사용하면 [!DNL Adobe Experience Cloud] 고객이 [!DNL Experience Platform Edge Network]을(를) 통해 다양한 서비스와 상호 작용할 수 있습니다. [!DNL Adobe]은(는) 새 [!DNL Target] 고객이 [!DNL Experience Platform Web SDK]을(를) 구현할 것을 권장합니다.
* **[at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank}**: [!DNL Target]에 대한 이 구현 라이브러리는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 단일 페이지 애플리케이션에 대해 더 나은 옵션을 제공합니다. 새 기능으로 자주 업데이트되는 [!DNL Adobe]에서는 모든 [at.js 사용자를 최신 버전으로 업데이트할 것을 권장합니다](https://experienceleague-review.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

>[!NOTE]
>
>mbox.js 라이브러리는 [!DNL Target]에 대한 레거시 구현이며 2021년 3월 31일 이후에는 더 이상 지원되지 않습니다. [!UICONTROL Experience Platform Web SDK]&#x200B;(기본 설정) 또는 at.js 최신 버전으로 업그레이드하십시오.

사이트의 모든 페이지에서 [!UICONTROL Experience Platform Web SDK] 또는 at.js를 참조합니다. 예를 들어 이러한 라이브러리 중 하나를 글로벌 헤더에 추가합니다. 또는 [Adobe Experience Platform의 태그](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home){target=_blank}를 사용하여 [!DNL Target]을(를) 구현합니다.

다음 리소스에는 [!DNL Experience Platform Web SDK] 또는 at.js를 구현하는 데 도움이 되는 자세한 정보가 포함되어 있습니다.

* [[!DNL Adobe Experience Platform Web SDK] 확장](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html){target=_blank}
* [ [!DNL Adobe Experience Platform]을 사용하여 [!DNL Target] 구현](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch){target=_blank}

방문자가 [!DNL Target]에 최적화된 페이지를 요청할 때마다 실시간 요청이 타기팅 시스템으로 전송되어 제공할 콘텐츠를 결정합니다. 이 요청은 마케터가 관리하는 활동 및 경험에 의해 제어되며, 페이지가 로드될 때마다 만들어지고 이행됩니다. 콘텐츠는 개별 사이트 방문자를 대상으로 하며 응답률, 획득률 및 매출을 극대화합니다. 개인화된 컨텐츠는 방문자가 반응하거나, 상호 작용하거나, 구매할 수 있도록 하는 데 도움이 됩니다.

[!DNL Target]에서 페이지의 각 요소는 여러 요소를 포함할 수 있는 단일 경험의 일부입니다.

표시되는 컨텐츠는 사용자가 작성하는 활동의 유형에 따라 다릅니다.

### [!UICONTROL A/B Test]

기본 A/B 테스트에서 콘텐츠는 할당된 경험에서 임의로 선택됩니다. 각 경험에 대한 트래픽 할당 백분율을 설정할 수 있습니다. 초기에는 무작위 분할로 인해 트래픽이 불균일하게 분산될 수 있지만, 트래픽이 증가하면 균등화됩니다. 예를 들어 두 개의 경험이 있는 경우 시작 경험이 임의로 선택됩니다. 트래픽이 낮으면 방문자 비율이 한 경험으로 기울어질 수 있지만, 이러한 상황은 더 많은 트래픽과 균형을 이룹니다.

각 경험에 대한 백분율 타겟을 지정합니다. 표시할 경험을 선택하기 위해 난수가 생성됩니다. 결과 백분율이 목표와 정확히 일치하지 않을 수 있지만, 트래픽이 많으면 목표 목표에 더 가깝게 분할됩니다.

1. 고객이 브라우저에 표시되는 서버에서 페이지를 요청합니다.
1. 자사 쿠키가 고객 브라우저에 설정되어 동작을 저장합니다.
1. 페이지가 타겟팅 시스템을 호출합니다.
1. 활동 규칙에 따라 콘텐츠가 표시됩니다.

자세한 내용은 [A/B 테스트 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)를 참조하십시오.

### [!UICONTROL Auto-Allocate]

[!UICONTROL Auto-Allocate]은(는) 둘 이상의 옵션에서 우수성이 검증된 경험을 식별합니다. 그런 다음 더 많은 트래픽을 자동으로 승자에게 재할당하여 테스트가 계속 실행되고 학습됨에 따라 전환을 늘립니다.

자세한 내용은 [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)을(를) 참조하십시오.

### [!UICONTROL Auto-Target]&#x200B;(AT)

[!UICONTROL Auto-Target]은(는) 고급 머신 러닝을 활용하여 여러 가지 고성능, 마케터 정의 경험 중에서 선택합니다. [!UICONTROL Auto-Target]은(는) 개별 고객 프로필과 유사한 프로필을 가진 이전 방문자의 행동을 기반으로 각 방문자에게 가장 적합한 경험을 제공합니다. [!UICONTROL Auto-Target]을(를) 사용하여 콘텐츠를 개인화하고 전환할 수 있습니다.

자세한 내용은 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md)을 참조하십시오.

### [!UICONTROL Automated Personalization]&#x200B;(AP)

[!UICONTROL Automated Personalization]&#x200B;(AP)은(는) 오퍼 또는 메시지를 결합하고 고급 머신 러닝을 사용하여 각 방문자에게 다양한 변형을 매칭합니다. AP는 개별 고객 프로필을 기반으로 콘텐츠를 개인화하여 상승도를 높입니다.

자세한 내용은 [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)을 참조하십시오.

### [!UICONTROL Experience Targeting]&#x200B;(XT)

[!UICONTROL Experience Targeting]&#x200B;(XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상에 전달합니다. 지리 기반의 타깃팅을 포함하여, XT는 특정 경험이나 콘텐츠를 특정 대상으로 타깃팅하는 규칙을 정의할 때 유용합니다. 활동에 여러 규칙을 설정하여 다른 대상자에게 다양한 콘텐츠 변형을 전달할 수 있습니다. 방문자가 사이트를 볼 때 XT는 방문자를 평가하여 기준을 총족하는지 여부를 판단합니다. 자격이 있는 경우 활동에 입장하여 자격을 갖춘 경험을 보게 됩니다. 단일 활동 내에서 여러 대상자에 대한 경험을 만들 수 있습니다.

자세한 내용은 [Experience Targeting](/help/main/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4)을 참조하십시오.

### [!UICONTROL Multivariate Test]&#x200B;(MVT)

[!UICONTROL Multivariate Testing]&#x200B;(MVT)은 페이지 요소의 오퍼 조합을 비교하여 특정 대상에 가장 뛰어난 조합을 결정합니다. MVT는 활동의 성공에 가장 큰 영향을 미치는 요소를 식별하는 데 도움이 됩니다.

자세한 내용은 [다변량 테스트](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499)를 참조하십시오.

### [!UICONTROL Recommendations]

[!UICONTROL Recommendations] 활동은 이전 활동이나 기타 알고리즘을 기반으로 고객의 흥미를 끌 수 있는 제품이나 콘텐츠를 자동으로 표시합니다. 권장 사항은 고객이 다른 경우에는 발견하지 못할 수 있는 관련 항목을 고객에게 표시하는 데 도움이 됩니다.

자세한 내용은 [권장 사항](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0)을 참조하십시오.

<!--
## How [!DNL Target] counts server-call usage {#usage}

[!DNL Target] counts only server calls that provide value to customers. The following table shows how [!DNL Target] counts endpoints, single mbox, batch mbox calls, execute, prefetch, and notification calls.

The following information helps you understand the counting strategy used for [!DNL Target] server calls, as shown in the table below:

* **Count Once**: Counts once per API call.
* **Count the Number of mboxes**: Counts the number of mboxes under the array in the payload of a single API call.
* **Ignore**: Is not counted at all.
* **Count the Number of Views (Once)**: Counts the number of views under the array in the payload. In a typical implementation, a view notification has only one view under the notifications array, making this equivalent to counting once in most implementations.

|Endpoint|Fetch type|Options|Counting strategy|
|--- |--- |--- |-- |
|`rest//v1/mbox`|Single|[!UICONTROL execute]|Count once|
|`rest/v2/batchmbox`|Batch|[!UICONTROL execute]|Count the number of mboxes|
||Batch|[!UICONTROL prefetch]|Ignore|
||Batch|[!UICONTROL notifications]|Count the number of mboxes|
|`/ubox/[raw\|image\|page]`|Single|[!UICONTROL execute]|Count once|
|`rest/v1/delivery`<p>`/rest/v1/target-upstream`|Single|[!UICONTROL execute] > [!UICONTROL pageLoad]|Count once|
||Single|[!UICONTROL prefetch] > [!UICONTROL pageLoad]|Ignore|
||Single|[!UICONTROL prefetch] > [!UICONTROL views]|Ignore|
||Batch|[!UICONTROL execute] > [!UICONTROL mboxes]|Count the number of mboxes|
||Batch|[!UICONTROL prefetch] > [!UICONTROL mboxes]|Ignore|
||Batch|[!UICONTROL notifications] > [!UICONTROL views]|Count the number of views (once)|
||Batch|[!UICONTROL notifications] > [!UICONTROL pageLoad]|Count once|
||Batch|[!UICONTROL notifications] > type ([!UICONTROL conversions])|Count once|
||Batch|[!UICONTROL notifications] > [!UICONTROL mboxes]|Count the number of mboxes|

-->

## 에지 네트워크 {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

&#39;Edge&#39;는 지리적으로 분산된 서비스 아키텍처로, 위치에 관계없이 콘텐츠를 요청하는 방문자에게 최적의 응답 시간을 제공합니다.

응답 시간을 향상시키기 위해 [!DNL Target] Edge는 활동 논리, 캐시된 프로필 및 오퍼 정보만 호스팅합니다.

활동 및 콘텐츠 데이터베이스, [!DNL Analytics]개의 데이터, API 및 마케터 사용자 인터페이스는 [!DNL Adobe] 중앙 클러스터에 수용됩니다. 업데이트가 [!DNL Target] Edge로 전송되며 중앙 클러스터와 자동으로 동기화되어 캐시된 활동 데이터를 계속 업데이트합니다. 모든 1:1 모델링도 각 에지에 저장되므로 복잡한 요청을 로컬로 처리할 수 있습니다.

각 Edge 클러스터에는 방문자 콘텐츠 요청에 응답하고 분석 데이터를 추적하는 데 필요한 모든 정보가 포함되어 있습니다. 방문자자 요청은 가장 가까운 에지 노드로 전달됩니다.

자세한 내용은 [Adobe Target 보안 개요](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf) 백서를 참조하십시오.

[!DNL Target]은(는) 전 세계 Adobe 소유 및 Adobe 임대 데이터 센터에 호스팅됩니다.

중앙 클러스터 위치에는 데이터 수집 센터와 데이터 처리 센터가 모두 있습니다. Edge 클러스터 위치에는 데이터 수집 센터만 있습니다. 개별 보고서는 특정 데이터 처리 센터로 지정됩니다.

고객 사이트 활동 데이터는 7개의 Edge 클러스터 중 가장 가까운 곳에서 수집됩니다. 그런 다음 이 데이터는 처리를 위해 미리 결정된 중앙 클러스터 대상(오레곤, 더블린 또는 싱가포르)으로 이동합니다. 방문자 프로필 데이터는 사이트 방문자와 가장 가까운 에지 클러스터에 저장됩니다. Edge 클러스터 위치에는 중앙 클러스터 위치와 버지니아, 뭄바이, 시드니 및 도쿄가 포함됩니다.

단일 위치에서 모든 타겟팅 요청을 처리하는 대신 방문자에게 가장 가까운 Edge 클러스터에서 요청을 처리합니다. 이 접근 방식은 네트워크 및 인터넷 이동 시간의 영향을 완화합니다.

![서로 다른 유형의 Target 서버를 표시하는 맵](/help/main/c-intro/assets/target-servers.png)

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
>[!DNL Target]은(는) 현재 중국에 Edge 클러스터가 없으므로 해당 지역의 [!DNL Target] 고객에 대한 방문자 성능이 제한됩니다. 방화벽과 Edge 클러스터 부재는 사이트 경험에 영향을 주어 느린 렌더링 및 페이지 로드 시간을 초래할 수 있습니다. 또한 마케터는 [!DNL Target] 작성 UI 사용 시 지연을 경험할 수 있습니다.

원하는 경우 [!DNL Target] 에지 클러스터를 허용 목록에 추가할 수 있습니다. 자세한 내용은 [Target 에지 노드를 허용 목록에 추가](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/allowlist-edges){target=_blank}를 참조하십시오.

## 보호된 사용자 경험 {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

[!DNL Adobe]은(는) 타기팅 인프라의 가용성과 성능을 최대한 신뢰할 수 있도록 보장합니다. 그러나 방문자의 브라우저와 [!DNL Adobe] 서버 간의 통신 분류로 인해 콘텐츠 전달이 중단될 수 있습니다.

서비스 중단 및 연결 문제를 방지하기 위해 모든 위치가 기본 콘텐츠(클라이언트에 의해 정의됨)를 포함하도록 설정됩니다. 방문자의 브라우저가 [!DNL Target]에 연결할 수 없는 경우 이 기본 내용이 표시됩니다.

방문자의 브라우저가 정의된 제한 시간 내(기본값: 15초)에 연결할 수 없는 경우 페이지에 변경 사항이 적용되지 않습니다. 이 시간 초과 임계값에 도달하면 기본 위치 콘텐츠가 표시됩니다.

[!DNL Adobe]에서는 성능을 최적화 및 보호함으로써 사용자 경험을 보호합니다.

* [!DNL Adobe]은(는) [!UICONTROL Adobe Service Level Agreement]에서 보장한 업계 표준을 기반으로 성과 벤치마크를 보장합니다.
* Edge Network가 시기 적절한 데이터 전달을 보장합니다.
* [!UICONTROL Adobe]은(는) 응용 프로그램을 보호하기 위해 다층적 접근 방식을 사용하여 고객을 위한 최고 수준의 가용성과 안정성을 제공합니다.
* [!DNL Target] 컨설팅 팀에서는 구현 지원 및 지속적인 제품 지원 서비스를 제공합니다.

## SEO(검색 엔진 최적화) 친화도 테스트 {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target]은(는) 테스트를 위한 검색 엔진 지침을 따릅니다. [!DNL Google]은(는) 사용자 테스트를 권장하며 특정 지침을 따를 경우 A/B 및 [!UICONTROL Multivariate Testing]이(가) 유기 검색 엔진 랭킹에 영향을 주지 않는다고 명시합니다.

[!DNL Adobe Target]은 테스트를 위한 검색 엔진 지침을 따릅니다.

자세한 내용은 다음 Google 리소스를 참조하십시오.

* [웹 사이트 테스트 및 Google 검색](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [실험 및 클로킹](https://support.google.com/analytics/answer/12979939?hl)


지침은 [Google 웹마스터 센터 블로그](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) 게시물에 나와 있습니다. 게시 날짜가 2012년으로 거슬러 올라가지만 이 문제에 대한 [!DNL Google]의 최신 설명으로 남아 있으며 지침은 여전히 적절합니다.

* **클로킹 없음**: 클로킹 작업에는 봇을 명확히 식별하고 다른 콘텐츠를 공급함으로써 사용자에게 하나의 콘텐츠 세트와 검색 엔진 봇에 대한 다른 콘텐츠 세트가 표시됩니다.

  [!DNL Target]이(가) 검색 엔진 봇을 사용자와 동일하게 처리하도록 구성되어 있습니다. 따라서 봇을 무작위로 선택하고 테스트 변형을 &quot;참조&quot;할 경우 활동에 포함할 수 있습니다.

* **rel=&quot;canonical&quot;** 사용: 경우에 따라 A/B 테스트에는 변형에 대한 다른 URL이 필요합니다. 이 경우, 모든 변형은 원래(통제) URL을 참조하는 rel=&quot;canonical&quot; 태그를 포함해야 합니다. 예를 들어 [!DNL Adobe]이(가) 각 변형에 대해 서로 다른 URL을 사용하여 홈 페이지를 테스트하는 경우 홈 페이지에 대한 다음 표준 태그를 각 변형의 `<head>` 태그에 배치해야 합니다.

  `<link rel="canonical" href="https://www.adobe.com" />`

* **302(임시) 리디렉션 사용**: 테스트에서 변형 페이지에 별도의 URL을 사용하는 경우 [!DNL Google]에서는 302 리디렉션을 사용하여 트래픽을 테스트 변형으로 전달하는 것을 권장합니다. 302 리디렉션은 테스트가 실행되는 동안에만 리디렉션이 일시적이고 활성임을 검색 엔진에 알립니다.

  302 리디렉션은 서버측 리디렉션이지만 [!DNL Target] 및 대부분의 최적화 공급자는 클라이언트측 기능을 사용합니다. 따라서 [!DNL Target]은(는) 리디렉션에 대한 [!DNL Google]의 권장 사항을 완전히 준수하지 않습니다. 그러나 이는 극히 일부 테스트에만 영향을 미칩니다. [!DNL Target]을(를) 통해 테스트를 실행하는 표준 방법에는 단일 URL 내의 콘텐츠를 변경하여 리디렉션이 필요하지 않습니다. 테스트 변형에 여러 URL이 필요한 경우 [!DNL Target]은(는) 리디렉션이 301인지 또는 302인지를 지정하지 않는 JavaScript `window.location` 명령을 사용합니다.

  [!DNL Adobe]이(가) 검색 엔진 지침을 완전히 준수하는 솔루션을 적극적으로 찾고 있습니다. 테스트를 위해 별도의 URL이 필요한 클라이언트의 경우 [!DNL Adobe]은(는) 표준 태그를 올바르게 구현하면 관련 위험이 줄어든다고 생각합니다.

* **필요한 동안만 실험 실행**: [!DNL Adobe]은(는) 통계적 중요도에 도달하는 데 필요한 시간을 &quot;필요한 동안&quot;으로 정의합니다. [!DNL Target]은(는) 모범 사례 및 [!DNL Adobe Target] [샘플 크기 계산기](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)를 제공하여 테스트가 이 지점에 도달했는지 확인할 수 있도록 해 줍니다. [!DNL Adobe]에서는 가장 성과가 좋은 테스트의 하드코딩된 구현을 테스트 워크플로에 통합하고 적절한 리소스를 할당할 것을 권장합니다.

  [!DNL Target]을(를) 사용하여 가장 성과가 좋은 테스트를 &quot;게시&quot;하는 것은 영구적인 솔루션으로 권장되지 않습니다. 항상 사용자의 100%에 대해 가장 성과가 좋은 테스트가 게시되는 경우 가장 성과가 좋은 테스트를 하드 코딩하는 동안 이 접근 방식을 일시적으로 사용할 수 있습니다.

  테스트가 변경된 사항을 고려합니다. 단추 색상과 같은 작은 업데이트는 유기 순위에 영향을 주지 않습니다. 그러나 텍스트 변경 내용은 하드코딩해야 합니다.

  또한 테스트 중인 페이지의 접근성을 고려하십시오. 페이지가 검색 엔진에 액세스할 수 없고 유기 검색 순위에 포함될 의도가 없는 경우 이러한 고려 사항이 적용되지 않습니다. 한 가지 예는 이메일 캠페인 전용 랜딩 페이지입니다.

Google에서는 이러한 지침을 따르는 것이 &quot;테스트에서 검색 결과에 있는 여러분의 사이트에 영향을 거의 주지 않거나 전혀 주지 않는다&quot;고 명시합니다.

Google에서는 이 지침 외에도 콘텐츠 실험 도구에 대해 설명서에서 다음과 같은 지침을 하나 더 제공합니다.

* 대안 페이지는 원본 페이지의 콘텐츠와 본질적인 측면에서 동일해야 합니다. 원본 콘텐츠의 의미와 사용자가 원본 콘텐츠에서 인식하는 일반적인 개념이 대안 페이지에서 바뀌지 않는 것이 좋습니다.

Google에서는 한 예로 &quot;사이트의 원본 페이지를 로드한 키워드가 사용자에게 표시되는 조합과 관련이 없을 경우 Google은 해당 사이트를 Google 색인에서 제외할 수 있다&quot;고 명시하고 있습니다.

[!UICONTROL Adobe]은(는) 테스트 변형 내에서 원래 콘텐츠의 의미를 실수로 변경하기는 어렵다고 느끼고 있습니다. 그러나 [!UICONTROL Adobe]에서는 페이지의 키워드 테마를 인식하고 해당 테마를 유지 관리할 것을 권장합니다. 특히 관련 키워드를 추가하거나 삭제하는 등의 페이지 콘텐츠 변경은 유기 검색에서 URL에 대한 순위 변경을 초래할 수 있습니다. [!DNL Adobe]는 테스트 프로토콜의 일부로서 SEO 파트너와 협력할 것을 권장합니다.

## 보트 {#bots}

[!DNL Target]은(는) [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/) 지표 &quot;isRobot&quot;을 사용하여 요청 헤더에 전달된 사용자 에이전트 문자열을 기반으로 알려진 봇을 탐지합니다.

>[!NOTE]
>
> [!DNL Server-Side] 요청의 경우 [요청의 &quot;컨텍스트&quot; 노드](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) 에 전달된 값이 봇 탐지를 위한 사용자 에이전트 문자열보다 우선합니다.

봇 생성으로 식별된 트래픽은 여전히 콘텐츠로 제공됩니다. [!DNL Target]이(가) SEO 지침을 준수하는지 확인하기 위해 봇은 일반 사용자처럼 취급됩니다. 그러나 보트 트래픽은 일반 사용자로 취급되는 경우 A/B 테스트 또는 개인화 알고리즘을 왜곡할 수 있습니다. 따라서 [!DNL Target] 활동의 알려진 봇 트래픽은 다르게 처리됩니다. 보트 트래픽을 제거하면 사용자 활동을 보다 정확하게 측정할 수 있습니다.

알려진 봇 트래픽의 경우 [!DNL Target]은(는) 다음을 수행하지 않습니다.

* 방문자 프로필 만들기 또는 검색
* 프로필 속성 기록 또는 프로필 스크립트 실행
* [!DNL Adobe Audience Manager] (AAM) 세그먼트 조회 (해당되는 경우)
* [!UICONTROL Recommendations], [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization] 또는 [!UICONTROL Auto-Allocate] 활동에 대해 개인화된 콘텐츠를 모델링하거나 제공하는 데 봇 트래픽을 사용합니다.
* 보고를 위한 활동 방문 로그
* [!DNL Adobe Experience Cloud] 플랫폼으로 전송될 로그 데이터

알려진 봇 트래픽의 경우 [!UICONTROL Analytics for Target]&#x200B;(A4T)을 사용할 때 [!DNL Target]은(는) 다음을 수행하지 않습니다.

* [!DNL Analytics]에 이벤트 보내기

`client_side` 로깅을 사용할 때 알려진 봇 트래픽의 경우 [!DNL Target]이(가) 다음을 반환하지 않습니다.

* `tnta payload`
