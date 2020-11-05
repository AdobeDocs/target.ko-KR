---
keywords: Overview and Reference;SEO;search engine optimization;edge clusters, central clusters
description: Adobe Target은 JavaScript 라이브러리 at.js 또는 mbox.js 중 하나를 통해 웹 사이트와 통합
title: Adobe Target 작동 방식
feature: intro
subtopic: Getting Started
topic: Standard
uuid: 01c0072d-f77d-4f14-935b-8633f220db7b
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '2403'
ht-degree: 82%

---


# Adobe Target 작동 방식

Target JavaScript 라이브러리(at.js 및 mbox.js)와 Target에 포함된 다양한 활동 유형에 대한 정보를 포함하여 Adobe Target 작동 방식에 대한 정보입니다.

## Target JavaScript 라이브러리 {#libraries}

Adobe Target은 JavaScript 라이브러리 at.js 또는 mbox.js 중 하나를 통해 웹 사이트와 통합됩니다

* **at.js:** [at.js 라이브러리](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17)는 Target의 새 구현 라이브러리입니다. at.js 라이브러리는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 단일 페이지 애플리케이션에 대해 더 나은 구현 옵션을 제공합니다. at.js는 권장되는 구현 라이브러리이며 새 기능으로 자주 업데이트됩니다. 모든 고객이 구현하거나 [at.js 최신 버전으로 마이그레이션](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)하는 것이 좋습니다.
* **mbox.js:** mbox.js 라이브러리는 Target의 새 구현 라이브러리입니다. mbox.js 라이브러리는 계속 지원되지만 기능 업데이트는 제공되지 않을 예정입니다.

>[!IMPORTANT]
>
>모든 고객은 at.js로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [mbox.js에서 at.js로 마이그레이션](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)을 참조하십시오

사이트의 모든 페이지에서 Target JavaScript 라이브러리 파일을 참조해야 합니다. 예를 들어, 글로벌 헤더에 추가할 수 있습니다. 또는 [Adobe Launch 태그 관리자](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)를 사용하는 것이 좋습니다.

방문자가 Target에 대해 최적화된 페이지를 요청할 때마다, 방문자에게 서비스로 제공할 콘텐츠를 결정하기 위해 타깃팅 시스템으로 요청이 전송됩니다. 이 프로세스는 실시간으로 발생하며, 페이지가 로드될 때마다 콘텐츠 요청이 이루어지고 각 시스템에 의해 이행됩니다. 콘텐츠는 마케터가 관리하는 활동 및 경험의 규칙이 적용되며, 개별 사이트 방문자를 타깃팅합니다. 또한 각 사이트 방문자가 응답하고, 상호 작용하고, 궁극적으로 가장 구매할 것 같은 콘텐츠를 제공하여 응답률, 획득률 및 매출을 최적화합니다.

Target에서 페이지의 각 요소는 전체 페이지를 위한 단일 경험의 일부입니다. 각 경험은 페이지에 여러 요소를 포함할 수 있습니다.

방문자에게 표시되는 콘텐츠는 사용자가 작성하는 활동의 유형에 따라 다릅니다.

### A/B 테스트

자세한 내용은 [A/B 테스트 만들기](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)를 참조하십시오.

기본 A/B 테스트에 표시되는 콘텐츠는 각 경험에 대해 선택하는 백분율에 따라 활동에 지정하는 자산으로부터 무작위로 선택됩니다. 이러한 트래픽 무작위 분할의 결과, 초기 트래픽을 많이 사용한 후에야 비율이 안정됩니다. 예를 들어 두 개의 경험을 만드는 경우 시작 경험이 무작위로 선택됩니다. 트래픽이 거의 없다면 방문자 비율이 하나의 경험으로 기울어질 수 있습니다. 트래픽이 증가함에 따라 이러한 비율은 더 비슷해지게 됩니다.

각 경험에 대해 비율 타겟을 지정할 수 있습니다. 이런 경우, 무작위 숫자가 생성되고 이 숫자를 사용하여 표시할 경험이 선택됩니다. 결과로 얻은 비율은 지정한 타겟과 정확하게 일치하지 않을 수도 있지만 더 많은 트래픽이 일어나면 경험이 타겟 목표에 더 가깝게 분할되어야 한다는 것을 의미합니다.

1. 고객이 서버에서 페이지를 요청하고 브라우저에 표시합니다.
2. 자사 쿠키가 고객 브라우저에 설정되어 고객 동작을 저장합니다.
3. 페이지가 타깃팅 시스템을 호출합니다.
4. 활동의 규칙에 따라 콘텐츠가 표시됩니다.

### 자동 할당

자세한 내용은 [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)을 참조하십시오.

자동 할당은 둘 이상의 경험에서 승자를 식별하고, 테스트가 계속 실행되고 학습되는 동안 변환을 늘리기 위해 더 많은 트래픽을 승자에게 자동으로 재할당합니다.

### AT(자동 Target)

자세한 내용은 [자동 타겟](/help/c-activities/auto-target/auto-target-to-optimize.md)을 참조하십시오.

자동 타겟은 콘텐츠를 개인화하고 변환을 유도하기 위해 고급 기계 학습을 사용하여 성과가 좋은 마케터가 정의한 여러 경험 중에서 선택하고, 개별 고객 프로필과 이 프로필과 유사한 프로필을 가진 이전 방문자의 행동을 기반으로 각 방문자에게 가장 잘 맞춤 설정된 경험을 제공합니다.

### AP(자동화된 개인화)

자세한 내용은 [자동화된 개인화](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)를 참조하십시오.

자동화된 개인화(AP)는 콘텐츠를 개인화하고 상승도를 유도하기 위해, 오퍼나 메시지를 결합하고 고급 기계 학습을 사용하여 방문자의 개별 고객 프로필을 기반으로 다양한 오퍼를 각 방문자와 연결합니다.

### 경험 타깃팅(XT)

[경험 타깃팅](/help/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4)

경험 타깃팅(XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상에 전달합니다.

지리 기반의 타깃팅을 포함한 경험 타깃팅은 특정 경험이나 콘텐츠를 특정 대상으로 타깃팅하는 규칙을 정의할 때 유용합니다. 활동에서 여러 규칙을 정의하여 다른 대상에 다양한 콘텐츠 변형을 전달할 수 있습니다. 방문자가 사이트를 볼 때 XT(경험 타깃팅)는 방문자를 평가하여 설정된 기준을 총족하는지 여부를 판단합니다. 기준을 충족하면 적격 대상을 위해 디자인된 활동 및 경험을 시작하게 됩니다. 단일 활동 내에서 여러 대상에 대한 경험을 만들 수 있습니다.

### 다변량 테스트(MVT)

자세한 내용은 [다변량 테스트](/help/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499)를 참조하십시오.

다변량 테스트(MVT)는 페이지의 요소에 있는 오퍼 조합을 비교하여 특정 대상에 대해 성과가 가장 좋은 조합을 판별하고 활동의 성공에 영향을 가장 많이 주는 요소를 식별합니다.

### 권장 사항

자세한 내용은 [권장 사항](/help/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0)을 참조하십시오.

권장 사항 활동은 이전 사용자 활동이나 기타 알고리즘을 기반으로 고객의 흥미를 끌 수 있는 제품이나 콘텐츠를 자동으로 표시합니다. 권장 사항은 고객이 모를 수 있는 관련 항목을 고객에게 표시하는 데 도움이 됩니다.

## The edge network {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

&quot;에지(Edge)&quot;는 컨텐츠를 요청하는 최종 사용자가 전세계 위치에 관계없이 최적의 응답 시간을 보장하는 지리적으로 분산된 서비스 아키텍처입니다.

응답 시간을 개선하기 위해 Target Edges는 활동 논리, 캐시된 프로필 및 오퍼 정보만 호스팅합니다.

Activity and content databases, [!DNL Analytics] data, APIs, and marketer user interfaces are housed in Adobe’s Central Clusters. 그런 다음 업데이트가 Target 가장자리에 전송됩니다. Central Clusters 및 Edge Clusters는 캐시된 활동 데이터를 지속적으로 업데이트하기 위해 자동으로 동기화됩니다. 모든 1:1 모델링은 각 가장자리에도 저장되므로 이러한 더 복잡한 요청도 가장자리에서 처리할 수 있습니다.

각 에지 클러스터에는 사용자의 컨텐츠 요청에 응답하고 해당 요청에 대한 분석 데이터를 추적하는 데 필요한 모든 정보가 있습니다. 사용자 요청은 가장 가까운 에지 클러스터로 라우팅됩니다.

자세한 내용은 [Adobe Target Security Overview](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf) 백서를 참조하십시오.

The [!DNL Adobe Target] solution is hosted on Adobe-owned and Adobe-leased data centers around the globe.

중앙 클러스터 위치에는 데이터 수집 센터와 데이터 처리 센터가 모두 포함됩니다. Edge Cluster 위치에는 데이터 수집 센터만 포함됩니다. 개별 보고서는 특정 데이터 처리 센터로 지정됩니다.

고객 사이트 활동 데이터는 7개의 Edge Clusters에서 가장 가까운 위치에 의해 수집되며 고객의 사전 결정된 Central Cluster 대상(3개 위치 중 하나)으로 전달됩니다.Oregon, Dublin, Singapore)을 참조하십시오. 방문자 프로필 데이터는 사이트 방문자와 가장 가까운 에지 클러스터에 저장됩니다(위치에는 중앙 클러스터 위치 및 버지니아, 암스테르담, 시드니, 도쿄 및 홍콩 포함).

단일 위치에서 모든 타깃팅 요청에 응답하는 대신 요청은 방문자와 가장 가까운 에지 클러스터에 의해 처리되므로 네트워크/인터넷 여행 시간의 영향을 완화합니다.

![Target 서버 맵 유형](/help/c-intro/assets/target-servers.png)

Amazon 웹 서비스(AWS)에서 호스팅되는 Target 중앙 클러스터는 다음 위치에 있습니다.

* 오리건, 미국
* 더블린, 아일랜드
* 싱가포르

AWS에서 호스팅되는 Target 에지 클러스터는 다음 위치에 있습니다.

* 인도 뭄바이
* 도쿄, 일본
* 버지니아, 미국
* 오리건, 미국
* 오스트레일리아 시드니
* 더블린, 아일랜드
* 싱가포르

이 [!DNL Target Recommendations] 서비스는 오리건주의 [!DNL Adobe] 데이터 센터에서 호스팅됩니다.

>[!IMPORTANT]
>
>[!DNL Adobe Target] 현재 중국에는 Edge Cluster가 없으며 중국 고객의 경우 최종 사용자 성능이 계속 제한됩니다. [!DNL Target] Because of the firewall and the lack of Edge Clusters within the country, the experiences of sites with [!DNL Target] deployed will be slow to render and page loads will be affected. Also, marketers might experience latency when using the [!DNL Target] authoring UI.

원하는 경우 Target 에지 클러스터를허용 목록에 추가하다 지정할 수 있습니다. 자세한 내용은 [Target 가장자리 노드허용 목록에 추가하다를 참조하십시오](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md).

## Protected user experience {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

Adobe에서는 타깃팅 인프라의 가용성 및 성능을 가능한 한 신뢰할 수 있도록 만들고 있습니다. 하지만 최종 사용자의 브라우저와 Adobe의 서버 간 통신 실패로 인해 콘텐츠 전달이 중단될 수 있습니다.

서비스 중단 및 연결 문제가 생기지 않도록 보호하려면, 모든 위치가 사용자의 브라우저가 [!DNL Target]에 연결할 수 없을 경우 나타나는 기본 콘텐츠(클라이언트가 정의함)를 포함하도록 설정하십시오.

사용자의 브라우저가 정의된 제한 시간 내(기본적으로 15초)에 연결할 수 없는 경우 페이지에 변경 사항이 적용되지 않습니다. 이 시간 초과 임계값에 도달하면 기본 위치 콘텐츠가 표시됩니다.

Adobe에서는 성능을 최적화 및 보호함으로써 사용자 경험을 보호합니다.

* Adobe는 Adobe 서비스 수준 계약(Service Level Agreement)으로 보장된 업계 표준을 기반으로 성과 벤치마크를 보장합니다.
* 에지 네트워크가 시기 적절한 데이터 전달을 보장합니다.
* Adobe는 애플리케이션 보호에 대한 다층적 접근 방식을 사용하여 고객을 위한 최고 수준의 가용성 및 안정성을 제공합니다.
* [!DNL Target] 컨설팅 팀에서는 구현 지원 및 지속적인 제품 지원 서비스를 제공합니다.

## SEO(검색 엔진 최적화) 친화도 테스트 {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target]은 테스트를 위한 검색 엔진 지침을 따릅니다.

Google에서는 사용자 테스트를 권장하고 있으며 A/B 및 다변량 테스트가 몇 가지 간단한 지침을 따르는 한 자연 검색 엔진 순위를 손상시키지 않을 것이라고 해당 설명서에 기술했습니다.

자세한 내용은 다음 Google 리소스를 참조하십시오.

* [웹 사이트 테스트 및 Google 검색](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [실험 및 클로킹](https://support.google.com/analytics/answer/2576845?hl=en&amp;ref_topic=1745207)

지침은 [Google 웹마스터 센터 블로그](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) 게시물에 나와 있습니다. 게시 날짜가 2012년까지 거슬러 올라가지만, 이 문제에 대한 Google의 최신 성명서이며 지침도 아직 적절합니다.

* **클로킹 없음** - 클로킹(Cloaking)은 사용자와 검색 엔진 봇을 명확히 구별하여 양측에 의도적으로 서로 다른 콘텐츠를 공급함으로써 사용자에게 표시하는 콘텐츠 세트와 검색 엔진 봇에게 표시하는 콘텐츠 세트를 달리하는 것입니다.

   플랫폼인 Target은 검색 엔진 봇을 사용자와 동일하게 처리하도록 구성되었습니다. 이것은 봇이 임의로 선택되는 경우 실행 중인 테스트에 포함될 수 있으며, 테스트 변형을 &quot;볼&quot; 수 있음을 의미합니다.

* **rel=&quot;canonical&quot; 사용** - 때로 다양한 변형에 대한 다양한 URL을 사용하여 A/B 테스트를 설정해야 합니다. 이러한 경우, 모든 변형은 원래(통제) URL을 참조하는 `rel="canonical"` 태그를 포함해야 합니다. 예를 들어, Adobe가 각 변형에 대해 서로 다른 URL을 사용하여 홈 페이지를 테스트하는 경우 홈 페이지에 대한 다음 대표(canonical) 태그는 각 변형에 대해 `<head>` 태그 안으로 들어갈 것입니다.

   `<link rel="canonical" href="https://www.adobe.com" />`

* **302(임시) 리디렉션 사용** - 테스트에서 변형 페이지에 개별 URL이 사용되는 경우, Google에서는 302 리디렉션을 사용하여 트래픽을 테스트 변형으로 전달하는 것을 권장합니다. 검색 엔진은 이를 통해 리디렉션이 일시적인 것이며 테스트가 실행 중인 동안에만 실행될 것이라는 것을 알게 됩니다.

   302 리디렉션은 서버 측 리디렉션이며 대부분의 최적화 제공자와 함께 Target은 클라이언트측 기능을 사용합니다. 따라서 이것은 Target이 Google의 권장 사항을 완전히 준수하지 않는 영역입니다. 그러나 매우 일부 테스트에는 영향을 줍니다. Target을 통해 테스트를 실행하는 이 표준 접근 방식은 단일 URL 내 콘텐츠 변경을 필요로 하므로 리디렉션이 필요하지 않습니다. 클라이언트가 여러 URL을 사용하여 테스트 변형을 표현해야 하는 경우가 있습니다. 이러한 경우 Target에서는 리디렉션이 301인지 또는 302인지를 명시적으로 나타내지 않는 JavaScript `window.location` 명령을 사용하여 사용자에게 테스트 변형을 표시합니다.

   Adobe는 검색 엔진 지침에 완전히 부합하는 실행 가능한 해결 방법을 계속 찾겠지만, 테스트를 위해 별도의 URL을 사용해야 하는 클라이언트를 위해, 위에 언급된 대표(canonical ) 태그를 적절히 구현하면 이러한 접근 방식과 연관된 위험이 완화된다고 확신하고 있습니다.

* **필요한 동안만 실험 실행** - Adobe에서는 &quot;필요한 동안&quot;을 통계적 중요도에 도달하는 데 걸리는 시간 동안으로 생각합니다. Target에서는 테스트가 이 시점에 도달했을 때를 판별하는 [우수 사례를 제공합니다](https://docs.adobe.com/content/target-microsite/testcalculator.html). 가장 성과가 좋은 테스트의 하드코딩된 구현을 테스트 워크플로우에 통합하고 적절한 리소스를 할당하는 것이 좋습니다.

   Target 플랫폼을 사용하여 가장 성과가 좋은 테스트를 &quot;게시&quot;하는 것은 영구적인 해결 방법으로 권장되지 않지만, 가장 성과가 좋은 테스트를 테스트 내내 100%의 사용자에 대해 게시하는 한 가장 성과가 좋은 테스트를 하드코딩하는 프로세스가 완료된 동안 이 접근 방식을 사용할 수 있습니다.

   테스트가 변경한 사항을 고려하는 것도 중요합니다. 페이지에 있는 단추나 기타 부수적인 비텍스트 기반 항목의 색상을 단순히 업데이트하는 것은 자연 순위에는 영향을 주지 않습니다. 하지만, 텍스트 변경 사항은 하드코딩해야 합니다.

   또한 테스트 중인 페이지의 액세서빌러티를 고려하는 것도 중요합니다. 이메일 캠페인 전용 랜딩 페이지와 같은 페이지가 검색 엔진에 액세스할 수 없고 자연 검색에서 1위를 하도록 설계되지 않은 경우에는 위의 고려 사항이 적용되지 않습니다.

Google에서는 이러한 지침을 따르는 것이 &quot;테스트에서 검색 결과에 있는 여러분의 사이트에 영향을 거의 주지 않거나 전혀 주지 않는다&quot;고 명시합니다.

Google에서는 이 지침 외에도 콘텐츠 실험 도구에 대해 설명서에서 다음과 같은 지침을 하나 더 제공합니다.

* 대안 페이지는 원본 페이지의 콘텐츠와 본질적인 측면에서 동일해야 합니다. 원본 콘텐츠의 의미와 사용자가 원본 콘텐츠에서 인식하는 일반적인 개념이 대안 페이지에서 바뀌지 않는 것이 좋습니다.

Google에서는 한 예로 &quot;사이트의 원본 페이지를 로드한 키워드가 사용자에게 표시되는 조합과 관련이 없을 경우 Google은 해당 사이트를 Google 색인에서 제외할 수 있다&quot;고 명시하고 있습니다.

테스트 변형 내 원래 콘텐츠의 의미를 실수로 변경하기는 어려울 것으로 생각되지만, 페이지의 키워드 테마에 유의하고 해당 테마를 유지하는 것이 좋습니다. 특히 관련 키워드를 추가하거나 삭제하는 등의 페이지 콘텐츠 변경은 자연 검색에서 URL에 대한 순위 변경을 초래할 수 있습니다. 테스트 프로토콜의 일부로서 SEO 파트너를 이용하는 것이 좋습니다.

## 보트 {#bots}

Adobe Target uses [DeviceAtlas](https://deviceatlas.com/) to detect known bots. 보트에 의해 생성된 것으로 식별된 트래픽은 SEO 가이드라인과 일치하도록 일반 사용자와 같은 콘텐츠를 계속 제공합니다. 보트 트래픽을 사용하면 일반 사용자로 취급되는 경우 A/B 테스트 또는 개인화 알고리즘을 왜곡할 수 있습니다. 따라서 알려진 보트가 Target 활동에서 감지되면 트래픽은 다소 다르게 처리됩니다. 보트 트래픽을 제거하면 사용자 활동을 보다 정확하게 측정할 수 있습니다.

특히 알려진 보트 트래픽 Target의 경우 다음이 불가능합니다.

* 방문자 프로필 만들기 또는 검색
* 모든 프로필 속성 로깅 또는 프로필 스크립트 실행
* Adobe Audience Manager(AAM) 세그먼트 조회(해당하는 경우)
* 추천, 자동 Target, 자동 개인화 또는 자동 할당 활동에 대해 개인화된 콘텐츠를 모델링하고 제공하는 데 보트 트래픽을 사용합니다.
* 보고를 위한 활동 방문 로그
* Adobe Experience Cloud 플랫폼으로 전송될 로그 데이터
