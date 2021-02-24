---
keywords: Adobe Experience Platform 웹 SDK;aep 웹 sdk;aep sdk;검색 엔진 최적화;검색 엔진 최적화;seo;edge 클러스터, 중앙 클러스터;at.js;mbox.js;
description: Target JavaScript 라이브러리(at.js 및 AEP Web SDK), Adobe 데이터 센터 및 SEO 테스트에 대한 정보를 포함하여 Adobe Target이 작동하는 방식에 대해 알아봅니다.
title: Target은 어떻게 작동합니까?
feature: 개요
translation-type: tm+mt
source-git-commit: 69677b9d384d9817a39386fc1388a4aa42121713
workflow-type: tm+mt
source-wordcount: '2570'
ht-degree: 30%

---


# Adobe Target 작동 방식

[!DNL Adobe Experience Platform Web SDK] 및 JavaScript 라이브러리(at.js 및 mbox.js)에 대한 정보를 포함하여 [!DNL Adobe Target]의 작동 방식을 알아봅니다. 또한 이 문서에서는 [!DNL Target]을 사용하여 만들 수 있는 다양한 활동 유형을 소개합니다. 또한 [!DNL Target] 에지 네트워크, 검색 엔진 최적화(SEO) 및 [!DNL Target]에서 보트를 감지하는 방법에 대해 알 수 있습니다.

## Target 플랫폼 웹 SDK 및 JavaScript 라이브러리 {#libraries}

[!DNL Target] 또는 JavaScript 라이브러리를 사용하여 웹  [!DNL AEP Web SDK] 사이트와 통합합니다.

* **Adobe Experience Platform 웹 SDK:** AEP  [웹 ](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) SDK는 새로운 클라이언트측 JavaScript 라이브러리입니다. AEP 웹 SDK를 통해 [!DNL Adobe Experience Cloud] 고객이 [!DNL AEP] 에지 네트워크를 통해 [!DNL Experience Cloud]([!DNL Target] 포함)의 다양한 서비스와 상호 작용할 수 있습니다. Adobe에서는 모든 새 [!DNL Target] 고객이 [!DNL AEP Web SDK]을(를) 구현할 것을 권장합니다.
* **at.js:** at.js 라이브러리 [는 ](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) 용 구현  [!DNL Target]라이브러리입니다. at.js 라이브러리는 웹 구현에 대한 페이지 로드 시간을 향상시키고, 단일 페이지 애플리케이션에 대해 더 나은 구현 옵션을 제공합니다. at.js는 새로운 기능으로 자주 업데이트됩니다. Adobe에서는 at.js를 사용하는 모든 고객이 자신의 구현을 최신 버전의 at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)로 업데이트할 것을 권장합니다.[
* **mbox.js:** mbox.js  [라이브러리는 ](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md) 이전 구현  [!DNL Target]라이브러리입니다. mbox.js 라이브러리는 2021년 3월 31일까지 지원됩니다.그러나 기능 업데이트는 없습니다.

>[!IMPORTANT]
>
>모든 고객은 [!DNL AEP Web SDK] 또는 최신 버전의 at.js로 마이그레이션해야 합니다. 자세한 내용은 [Adobe Experience Platform 웹 SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) 또는 [mbox.js에서 at.js로 마이그레이션](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)을 참조하십시오.

사이트의 모든 페이지에서 [!DNL AEP Web SDK] 또는 at.js를 참조하십시오. 예를 들어 이러한 라이브러리 중 하나를 전역 헤더에 추가할 수 있습니다. 또는 [Adobe Platform launch](https://experienceleague.adobe.com/docs/launch/using/overview.html)을 사용하여 [!DNL Target]를 구현하십시오.

다음 리소스에는 AEP 웹 SDK 또는 at.js를 구현하는 데 도움이 되는 자세한 정보가 포함되어 있습니다.

* [Adobe Experience Platform Web SDK Extension](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html?lang=en#configure-the-aep-web-sdk-extension)
* [Adobe Launch를 사용하여 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)

방문자가 [!DNL Target]에 대해 최적화된 페이지를 요청할 때마다 요청이 타깃팅 시스템으로 전송됩니다. 이 요청은 해당 방문자에게 제공할 컨텐츠를 결정하는 데 도움이 됩니다. 이 프로세스는 실시간으로 이루어집니다. 페이지가 로드될 때마다 컨텐트에 대한 요청이 이루어지고 시스템에 의해 이행됩니다. 콘텐츠는 마케터가 관리하는 활동 및 경험의 규칙이 적용되며, 개별 사이트 방문자를 타깃팅합니다. 컨텐츠는 각 사이트 방문자가 응답하거나 상호 작용하거나 궁극적으로 구매할 가능성이 가장 큰 컨텐츠가 제공됩니다. 개인화된 컨텐츠를 통해 응답률, 취득률 및 매출을 극대화할 수 있습니다.

[!DNL Target]에서 페이지의 각 요소는 전체 페이지에 대한 단일 경험의 일부입니다. 각 경험은 페이지에 여러 요소를 포함할 수 있습니다.

방문자에게 표시되는 콘텐츠는 사용자가 작성하는 활동의 유형에 따라 다릅니다.

### A/B 테스트

기본 A/B 테스트에 표시되는 컨텐츠는 활동에 지정한 경험에서 임의로 선택됩니다. 각 경험에 대한 트래픽 할당 비율을 할당할 수 있습니다. 이러한 트래픽 무작위 분할의 결과로 비율이 계산되기 전에 초기 트래픽의 양이 상당히 증가할 수 있습니다. 예를 들어 두 개의 경험을 만드는 경우 시작 경험이 무작위로 선택됩니다. 트래픽이 거의 없다면 방문자 비율이 하나의 경험으로 기울어질 수 있습니다. 트래픽이 증가하면 비율이 균일화됩니다.

각 경험에 대해 비율 타겟을 지정할 수 있습니다. 이런 경우, 무작위 숫자가 생성되고 이 숫자를 사용하여 표시할 경험이 선택됩니다. 결과로 얻은 비율은 지정한 타겟과 정확하게 일치하지 않을 수도 있지만 더 많은 트래픽이 일어나면 경험이 타겟 목표에 더 가깝게 분할되어야 한다는 것을 의미합니다.

1. 고객이 서버에서 페이지를 요청하고 브라우저에 표시합니다.
2. 고객 브라우저에 퍼스트 파티 쿠키를 설정하여 고객 행동을 저장합니다.
3. 페이지가 타깃팅 시스템을 호출합니다.
4. 활동의 규칙에 따라 콘텐츠가 표시됩니다.

자세한 내용은 [A/B 테스트 만들기](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)를 참조하십시오.

### 자동 할당

자동 할당은 두 개 이상의 경험 중에서 우승자를 식별합니다. 자동 할당은 성공 경험에 더 많은 트래픽을 자동으로 재할당하므로 테스트가 계속 실행되고 학습하는 동안 전환을 늘리는 데 도움이 됩니다.

자세한 내용은 [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)을 참조하십시오.

### AT(자동 Target)

자동 Target은 고급 머신 러닝을 사용하여 성과가 높은 마케터가 정의한 경험 중에서 선택할 수 있습니다. 자동 Target은 각 방문자에게 가장 맞춤화된 경험을 제공합니다. 경험 배달은 개별 고객 프로파일과 비슷한 프로파일을 가진 이전 방문자의 행동을 기반으로 합니다. 자동 Target을 사용하여 컨텐츠를 개인화하고 전환을 촉진합니다.

자세한 내용은 [자동 타겟](/help/c-activities/auto-target/auto-target-to-optimize.md)을 참조하십시오.

### AP(자동화된 개인화)

Automated Personalization(AP)는 오퍼 또는 메시지를 결합하고 고급 기계 학습을 사용하여 각 방문자에게 다양한 오퍼 변형을 일치시킵니다. 경험 전달은 컨텐츠를 개인화하고 향상도를 높일 수 있는 개별 고객 프로파일을 기반으로 합니다.

자세한 내용은 [자동화된 개인화](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)를 참조하십시오.

### 경험 타깃팅(XT)

경험 타깃팅(XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상에 전달합니다.

지리 기반의 타깃팅을 포함한 경험 타깃팅은 특정 경험이나 콘텐츠를 특정 대상으로 타깃팅하는 규칙을 정의할 때 유용합니다. 활동에서 여러 규칙을 정의하여 다른 대상에 다양한 콘텐츠 변형을 전달할 수 있습니다. 방문자가 사이트를 볼 때 XT(경험 타깃팅)는 방문자를 평가하여 설정된 기준을 총족하는지 여부를 판단합니다. 기준을 충족하면 적격 대상을 위해 디자인된 활동 및 경험을 시작하게 됩니다. 단일 활동 내에서 여러 대상에 대한 경험을 만들 수 있습니다.

자세한 내용은 [경험 타깃팅](/help/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4)을 참조하십시오.

### 다변량 테스트(MVT)

Multivariate Testing(MVT)는 페이지에 있는 요소의 오퍼 조합을 비교하여 특정 대상에 가장 적합한 조합을 결정합니다. MVT는 활동의 성공에 가장 큰 영향을 미치는 요소를 식별하는 데 도움이 됩니다.

자세한 내용은 [다변량 테스트](/help/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499)를 참조하십시오.

### Recommendations

권장 사항 활동은 이전 사용자 활동이나 기타 알고리즘을 기반으로 고객의 흥미를 끌 수 있는 제품이나 콘텐츠를 자동으로 표시합니다. 권장 사항은 고객이 모를 수 있는 관련 항목을 고객에게 표시하는 데 도움이 됩니다.

자세한 내용은 [권장 사항](/help/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0)을 참조하십시오.

## 에지 네트워크 {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

&quot;에지(Edge)&quot;는 컨텐츠를 요청하는 방문자가 세계 어디에 있든지 상관없이 최적의 응답 시간을 보장하는 지리적으로 분산된 서비스 아키텍처입니다.

응답 시간을 개선하기 위해 [!DNL Target] Edges는 활동 논리, 캐시된 프로필 및 오퍼 정보만 호스팅합니다.

활동 및 컨텐츠 데이터베이스, [!DNL Analytics] 데이터, API 및 마케터 사용자 인터페이스는 Adobe의 Central 클러스터에 수용됩니다. 업데이트가 [!DNL Target] Edges로 전송됩니다. Central Clusters 및 Edge Clusters는 캐시된 활동 데이터를 지속적으로 업데이트하기 위해 자동으로 동기화됩니다. 모든 1:1 모델링은 각 가장자리에도 저장되므로 이러한 더 복잡한 요청도 가장자리에서 처리할 수 있습니다.

각 에지 클러스터에는 방문자의 컨텐츠 요청에 응답하고 해당 요청에 대한 분석 데이터를 추적하는 데 필요한 모든 정보가 있습니다. 방문자 요청은 가장 가까운 에지 클러스터로 라우팅됩니다.

자세한 내용은 [Adobe Target Security Overview](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf) 백서를 참조하십시오.

[!DNL Target] 솔루션은 전 세계 Adobe 소유 및 Adobe에서 임대한 데이터 센터에 호스팅됩니다.

중앙 클러스터 위치에는 데이터 수집 센터와 데이터 처리 센터가 모두 포함됩니다. Edge Cluster 위치에는 데이터 수집 센터만 포함됩니다. 개별 보고서는 특정 데이터 처리 센터로 지정됩니다.

고객 사이트 활동 데이터는 7개의 Edge 클러스터 중 가장 근접한 곳에서 수집됩니다. 이 데이터는 고객이 미리 지정한 중앙 클러스터 대상(다음 3개 위치 중 하나)으로 보내집니다.처리를 위한 오레곤, 더블린, 싱가포르). 방문자 프로필 데이터는 사이트 방문자와 가장 가까운 에지 클러스터에 저장됩니다. Edge 클러스터 위치에는 중앙 클러스터 위치, 버지니아, 암스테르담, 시드니, 도쿄 및 홍콩이 포함됩니다.

단일 위치의 모든 타깃팅 요청에 대응하는 대신, 요청은 방문자와 가장 가까운 에지 클러스터에 의해 처리됩니다. 이 프로세스는 네트워크/인터넷 출장에 따른 영향을 완화시켜 줍니다.

![Target 서버 맵 유형](/help/c-intro/assets/target-servers.png)

[!DNL Target] AWS(Amazon Web Services)에서 호스팅되는 Central Clusters에는 다음이 포함됩니다.

* 오리건, 미국
* 더블린, 아일랜드
* 싱가포르 공화국

[!DNL Target] AWS에서 호스팅되는 Edge Clusters에는 다음이 포함됩니다.

* 인도 뭄바이
* 도쿄, 일본
* 버지니아, 미국
* 오리건, 미국
* 오스트레일리아 시드니
* 더블린, 아일랜드
* 싱가포르 공화국

[!DNL Target Recommendations] 서비스는 오리건 주의 [!DNL Adobe] 데이터 센터에서 호스팅됩니다.

>[!IMPORTANT]
>
>[!DNL Adobe Target] 현재 중국에 Edge Cluster가 없으며 중국 고객의 경우 방문자 성능이  [!DNL Target] 제한됩니다. 방화벽과 국가 내 Edge Clusters가 없기 때문에 [!DNL Target]이(가) 배포된 사이트의 경험에 영향을 줄 수 있습니다. 경험은 렌더링 속도가 느려질 수 있고 페이지 로드에 영향을 줄 수 있습니다. 또한 마케터는 [!DNL Target] 작성 UI를 사용할 때 지연을 경험할 수 있습니다.

원하는 경우 [!DNL Target] 에지 클러스터를 허용 목록에 추가하다할 수 있습니다. 자세한 내용은 [허용 목록에 추가하다 Target 가장자리 노드](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md)를 참조하십시오.

## 보호된 사용자 경험 {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

Adobe에서는 타깃팅 인프라의 가용성 및 성능을 가능한 한 신뢰할 수 있도록 만들고 있습니다. 그러나 방문자의 브라우저와 Adobe 서버 간의 통신 분류로 인해 컨텐츠 전달이 중단될 수 있습니다.

서비스 중단 및 연결 문제를 방지하기 위해 모든 위치가 기본 컨텐츠(클라이언트가 정의함)를 포함하도록 설정됩니다. 이 기본 컨텐츠는 사용자의 브라우저가 [!DNL Target]에 연결할 수 없을 때 표시됩니다.

사용자의 브라우저가 정의된 제한 시간 내(기본적으로 15초)에 연결할 수 없는 경우 페이지에 변경 사항이 적용되지 않습니다. 이 시간 초과 임계값에 도달하면 기본 위치 콘텐츠가 표시됩니다.

Adobe에서는 성능을 최적화 및 보호함으로써 사용자 경험을 보호합니다.

* Adobe는 Adobe 서비스 수준 계약(Service Level Agreement)으로 보장된 업계 표준을 기반으로 성과 벤치마크를 보장합니다.
* 에지 네트워크가 시기 적절한 데이터 전달을 보장합니다.
* Adobe는 애플리케이션 보호에 대한 다층적 접근 방식을 사용하여 고객을 위한 최고 수준의 가용성 및 안정성을 제공합니다.
* [!DNL Target] 컨설팅 팀에서는 구현 지원 및 지속적인 제품 지원 서비스를 제공합니다.

## SEO(검색 엔진 최적화) 친화도 테스트 {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target]은 테스트를 위한 검색 엔진 지침을 따릅니다.

Google은 사용자 테스트를 권장합니다. Google은 문서에 A/B 및 Multivariate Testing이 특정 지침을 따를 경우 유기적 검색 엔진 등급을 훼손하지 않는다고 명시하고 있습니다.

자세한 내용은 다음 Google 리소스를 참조하십시오.

* [웹 사이트 테스트 및 Google 검색](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [실험 및 클로킹](https://support.google.com/analytics/answer/2576845?hl=en&amp;ref_topic=1745207)

지침은 [Google 웹마스터 센터 블로그](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html) 게시물에 나와 있습니다. 게시 날짜가 2012년까지 거슬러 올라가지만, 이 문제에 대한 Google의 최신 성명서이며 지침도 아직 적절합니다.

* **숨김 없음**:숨김에는 사용자에게 하나의 컨텐츠 세트와 검색 엔진 보트 세트의 다른 컨텐츠 세트가 표시됩니다. 클로킹은 특별히 보트를 식별하여 다른 컨텐츠를 의도적으로 제공한 방식으로 수행됩니다.

   [!DNL Target], 플랫폼으로서, 모든 사용자와 동일한 검색 엔진 보트를 처리하도록 구성되어 있습니다. 그 결과, 보트를 임의로 선택하고 테스트 변형을 &quot;보기&quot;할 경우 보트는 활동에 포함될 수 있습니다.

* **rel=&quot;canonical&quot;** 사용:경우에 따라 변형에 대해 다른 URL을 사용하여 A/B 테스트를 설정해야 합니다. 이러한 경우, 모든 변형은 원래(통제) URL을 참조하는 `rel="canonical"` 태그를 포함해야 합니다. 예를 들어 Adobe이 각 변형에 대해 서로 다른 URL을 사용하여 홈 페이지를 테스트한다고 가정해 봅니다. 홈 페이지에 대한 다음 표준 태그는 각 변형에 대해 `<head>` 태그로 이동합니다.

   `<link rel="canonical" href="https://www.adobe.com" />`

* **302(임시) 리디렉션 사용**:테스트의 변형 페이지에 별도의 URL을 사용하는 경우 Google에서는 302 리디렉션을 사용하여 트래픽을 테스트 변형으로 보내는 것이 좋습니다. 302 리디렉션은 리디렉션이 일시적이며 테스트가 실행되는 동안에만 활성화됨을 검색 엔진에 알립니다.

   302 리디렉션은 서버측 리디렉션으로, 대부분의 최적화 공급자와 함께 [!DNL Target]은 클라이언트측 기능을 사용합니다. 따라서 리디렉션은 [!DNL Target]이 Google의 권장 사항과 완전히 호환되지 않는 영역입니다. 하지만 이러한 방법은 테스트 중 극히 일부에만 영향을 줍니다. 단일 URL 내의 콘텐츠를 변경하도록 [!DNL Target] 호출을 통해 테스트를 실행하는 표준 방식이므로 리디렉션이 필요하지 않습니다. 클라이언트가 테스트 변형을 나타내기 위해 여러 URL을 사용해야 하는 경우가 있습니다. 이러한 경우 [!DNL Target]은 JavaScript `window.location` 명령을 사용합니다. 이 명령은 사용자가 변형을 테스트하도록 지시하며, 리디렉션이 301 또는 302인지 여부를 명시적으로 표시하지 않습니다.

   Adobe은 검색 엔진 지침에 맞게 실행 가능한 솔루션을 계속 찾습니다. 테스트를 위해 개별 URL을 사용해야 하는 클라이언트의 경우, Adobe은 표준 태그를 적절히 구현하면 이 접근 방식과 관련된 위험을 완화시킬 수 있다고 확신합니다.

* **필요한** 경우에만 실험을 실행합니다.Adobe은 통계적 중요성을 깨닫기 위해 시간이 걸리는 한 &quot;필요한 한&quot;이라고 생각한다. [!DNL Target] [테스트](https://docs.adobe.com/content/target-microsite/testcalculator.html) 가 이 포인트에 도달했는지 확인하는 모범 사례를 제공합니다. Adobe에서는 우승 테스트의 하드 코딩된 구현을 테스트 작업 과정에 통합하고 적절한 리소스를 할당하는 것이 좋습니다.

   [!DNL Target] 플랫폼을 사용하여 &quot;게시&quot; 수상 테스트를 영구 솔루션으로 사용하지 않는 것이 좋습니다. 우승 테스트가 100% 사용자 중 100%에 대해 게시된 경우 우승 테스트를 하드 코딩하는 프로세스가 완료되는 동안 이 방법을 사용할 수 있습니다.

   테스트가 변경한 사항을 고려하는 것도 중요합니다. 페이지에서 단추나 기타 텍스트가 아닌 항목의 색상을 업데이트하면 유기 등급에 영향을 주지 않습니다. 하지만, 텍스트 변경 사항은 하드코딩해야 합니다.

   또한 테스트 중인 페이지의 액세서빌러티를 고려하는 것도 중요합니다. 검색 엔진에서 페이지에 액세스할 수 없고 첫 번째 위치에서 유기적 검색의 등급을 지정하도록 설계되지 않은 경우 위의 고려 사항 중 어느 것도 적용되지 않습니다. 예: 이메일 캠페인에 대한 전용 랜딩 페이지입니다.

Google에서는 이러한 지침을 따르는 것이 &quot;테스트에서 검색 결과에 있는 여러분의 사이트에 영향을 거의 주지 않거나 전혀 주지 않는다&quot;고 명시합니다.

Google에서는 이 지침 외에도 콘텐츠 실험 도구에 대해 설명서에서 다음과 같은 지침을 하나 더 제공합니다.

* 대안 페이지는 원본 페이지의 콘텐츠와 본질적인 측면에서 동일해야 합니다. 원본 콘텐츠의 의미와 사용자가 원본 콘텐츠에서 인식하는 일반적인 개념이 대안 페이지에서 바뀌지 않는 것이 좋습니다.

Google에서는 한 예로 &quot;사이트의 원본 페이지를 로드한 키워드가 사용자에게 표시되는 조합과 관련이 없을 경우 Google은 해당 사이트를 Google 색인에서 제외할 수 있다&quot;고 명시하고 있습니다.

Adobe은 테스트 변형 내에서 원본 컨텐츠의 의미를 의도치 않게 변경하는 것이 어렵다고 생각합니다. 그러나 Adobe은 페이지에서 키워드 테마를 인지하고 이러한 테마를 유지 관리할 것을 권장합니다. 특히 관련 키워드를 추가하거나 삭제하는 등의 페이지 콘텐츠 변경은 자연 검색에서 URL에 대한 순위 변경을 초래할 수 있습니다. Adobe은 테스트 프로토콜의 일부로 SEO 파트너와 교류하는 것을 권장합니다.

## 보트 {#bots}

Adobe [!DNL Target]은 [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/) 지표 &quot;isRobot&quot;를 사용하여 요청 헤더에 전달된 사용자 에이전트 문자열을 기반으로 알려진 보트를 감지합니다.

>[!NOTE]
>
> [!DNL Server-Side] 요청의 경우 [요청의 &quot;Context&quot; 노드](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API)에 전달된 값이 보트 감지를 위한 사용자 에이전트 문자열보다 우선합니다.

보트가 생성하는 것으로 식별되는 트래픽은 여전히 컨텐츠를 제공합니다. 보트는 일반 사용자로 취급되어 [!DNL Target]이(가) SEO 지침과 일치하는지 확인합니다. 보트 트래픽을 사용하면 일반 사용자로 취급되는 경우 A/B 테스트 또는 개인화 알고리즘을 왜곡할 수 있습니다. 따라서 알려진 보트가 [!DNL Target] 활동에서 감지되면 트래픽은 약간 다르게 처리됩니다. 보트 트래픽을 제거하면 사용자 활동을 보다 정확하게 측정할 수 있습니다.

특히 알려진 보트 트래픽의 경우 [!DNL Target]은 다음을 수행하지 않습니다.

* 방문자 프로필 만들기 또는 검색
* 모든 프로필 속성 로깅 또는 프로필 스크립트 실행
* Adobe Audience Manager(AAM) 세그먼트 조회(해당하는 경우)
* Recommendations, 자동 Target, Automated Personalization 또는 자동 할당 활동에 대한 맞춤형 컨텐츠를 모델링 및 제공하는 데 보트 트래픽을 사용합니다.
* 보고를 위한 활동 방문 로그
* [!DNL Adobe Experience Cloud] 플랫폼으로 전송할 로그 데이터
