---
keywords: Recommendations;소개;소개;웨비나;데모
description: 이전 사용자 활동 또는 기타 알고리즘을 기반으로 고객의 흥미를 끌 수 있는 콘텐츠를 자동으로 표시하는 Adobe  [!DNL Target] 의 권장 사항 활동에 대해 알아보십시오.
title: Recommendations 활동이란 무엇입니까?
feature: Recommendations
exl-id: bc4d9a46-ea21-4687-b8a0-7f2e1dc33ebf
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '2114'
ht-degree: 98%

---

# ![PREMIUM](/help/main/assets/premium.png) 추천 소개

이 문서의 텍스트는 *추천 소개* 웨비나에서 제공되며, 아래에서 전체 내용을 볼 수 있습니다.

*권장 사항 소개* 웨비나에서는 [!DNL Adobe Target Recommendations] 값을 활용하는 방법에 대한 심층적인 설명을 포함합니다. 이 [!DNL Target] 활동에서는 이전 방문 횟수에 따라 실시간 제안을 최적화하여 고객의 흥미를 끌 수 있는 제품 또는 콘텐츠를 자동으로 표시하는 방법을 알아봅니다. 또한 [!DNL Target] UI에서 [!DNL Recommendations] 활동을 구축하는 방법에 관한 단계별 개요를 살펴보십시오.

## 소개

Adobe는 소매점에서 사용하는 모든 종류의 추천에 대해 알고 있습니다. 점차 많은 고객이 이러한 종류의 추천을 기대하고 이를 사용 가능한 다른 옵션을 탐색하기 위한 시작점으로 활용합니다. 쇼핑 행동에 대해 생각해 보면 이러한 추천이 어떤 효과를 발휘하는지 알 수 있습니다. 우리 대부분은 매장이나 디지털 에셋 등 어디에서나 추천에서 처음 본 제품을 구입합니다.

다음 그림은 충전 스테이션, 케이스, 헤드폰 등과 같이 새 휴대폰과 함께 일반적으로 구입하는 액세서리 추천을 보여 줍니다.

![다른 사람이 새 휴대폰과 함께 구입한 액세서리를 보여 주는 추천.](/help/main/c-recommendations/assets/intro-1.png)

그러나 우리는 디지털 중심의 브랜드 기업이 어떻게 고객 기대치를 높이는 지에 대해 망각하곤 합니다. 미디어와 콘텐츠를 소비하는 방법은 점차 개인화된 추천에 의해 좌우되고 있습니다. Netflix, Spotify 또는 YouTube를 열 때 가장 먼저 보게 되는 것을 생각해 보십시오. 이러한 브랜드는 추천과 함께 고객 경험을 시작합니다. 그 어느 때보다 많은 대안이 제공되는 세상에서는 상호 작용 시점에서 고객과 가장 관련성이 높은 콘텐츠를 식별할 수 있어야 합니다.

![디지털 중심 브랜드를 보여 주는 추천](/help/main/c-recommendations/assets/intro-2.png)

마케팅 담당자는 [!DNL Adobe Target] 을 활용하여 다양한 업계, 고객 유형 및 채널에서 개인화된 경험을 제공합니다.

[!DNL Adobe Target] 은 어디에서나 개인화된 콘텐츠를 제공합니다.

![Target 이 다양한 위치에서 추천을 제공하는 방법을 보여 주는 그림](/help/main/c-recommendations/assets/intro-3.png)

* **게시**: 웹 게시자는 [!DNL Target Recommendations] 를 사용하여 사이트 방문자에게 문서를 추천하고 참여를 유도합니다.
* **비디오 튜토리얼**: [!DNL Adobe Creative Cloud] 은 [!DNL Target] 을 사용하여 Photoshop 애플리케이션에서 Photoshop 사용자에게 비디오 튜토리얼을 추천합니다.
* **게임**: 게임 업체는 콘솔 내의 사용자에게 게임과 콘텐츠를 추천하기 위해 [!DNL Target] 을 사용합니다.
* **B2B 판매**: [B2B 업체는 Target를 사용하여 B2B 잠재 고객에게 비디오, 백서 및 블로그 게시물을 추천하고 다운로드를 제공하며 기존 고객을 지원합니다](https://theblog.adobe.com/testing-shifts-high-gear-intel).

* **여행**: [독일 여행 예약자는 Target을 사용하여 호텔 등을 여행객에게 추천합니다](https://2017.summit.adobe.com/na/sessions/summit-online/online-2017/#17608).

* **소매**: [선도적인 BB 소매업체는 Target를 사용하여 브라우저와 모바일에서 방문자가 재방문할 수 있는 상위 범주와 제품을 추천합니다](https://theblog.adobe.com/optimization-personalization-b2b-powerhouse-grainger/)2.

다음은 고객이 Target을 사용하여 개인화된 추천을 제공하는 방법 중 일부입니다.

어떻게 우수한 추천을 할 수 있습니까?

![우수한 추천을 만드는 세 가지 요소를 보여 주는 일러스트레이션](/help/main/c-recommendations/assets/intro-4.png)

우수한 추천은 연관성이 있고 개인화되어야 합니다. 즉, 연관성과 개인화를 위해서는 3가지가 필요합니다.

* **마케팅 담당자의 제어**: 추천 항목의 연관성을 높임. 마케팅 담당자는 중요한 컨텍스트를 표로 가져와 제품 또는 콘텐츠의 어떤 속성이 추천 모델과 관련이 있는지 알고 있습니다. 비디오 사이트를 운영하는 경우 사용자가 동일한 감독의 영화를 보는 데 관심이 있을 수 있지만 동일한 스튜디오에서 제작한 영화를 보는 것에는 관심이 없을 수도 있습니다. [!DNL Target] 은 이 도메인 지식을 사용하여 알고리즘을 개선할 수 있는 제어 기능을 제공합니다.
* **정교한 모델**: 카탈로그 및 상호 작용 이벤트에서 수백만 개의 항목을 파악. [!DNL Target] 은 10년 이상의 경험을 바탕으로 한 정교한 머신 러닝 기능을 갖추고 있으며 매년 수십 억 건의 추천을 처리합니다.
* **사용자 컨텍스트**: 추천이 적시에 적절한 사용자에게 제공되도록 함. 누군가 방금 본 비디오나 누군가가 방금 장바구니에 추가한 셔츠를 추천하고 싶지 않을 것입니다. Target의 풍부한 사용자 프로필을 추천에 사용하여 개인화를 보장할 수 있습니다.

## [!DNL Target] 추천 구현

전략과 함께 시작하십시오.

![추천 전략을 보여 주는 그림](/help/main/c-recommendations/assets/intro-5.png)

* **어떤 항목을 추천하시겠습니까?** 먼저 추천할 항목을 생각해 보십시오. 제품, 비디오 또는 콘텐츠일 수 있습니다.
* **어디에서 추천하시겠습니까?** 이제 추천을 하려는 위치에 대해 생각해 보십시오. 웹, 모바일, 매장, 키오스크 등 광범위한 채널이 될 수 있습니다. 고객 여정의 어떤 부분에서 추천이 제공됩니까? 사이트의 어떤 페이지에 추천이 제공됩니까?
* **추천의 성공 여부를 어떻게 결정합니까?** 추천을 받지 않은 경험, 추천을 받은 경험 또는 두 개의 경험을 모두 갖고 있다고 가정해 봅시다. 고객에게 어떤 경험이 더 나은 경험인지 어떻게 알 수 있습니까? 일부 지표는 다른 지표보다 측정하기 더 어려울 수 있습니다. 예를 들어 추천이 고객 생애 가치에 미치는 영향은 직접적으로 측정하기 어렵습니다. 따라서 방문당 매출, 평균 주문 가격, 클릭 수 등과 같이 보다 구체적이고 덜 추상적인 지표를 측정하는 것이 더 쉬울 수 있습니다. 경우에 따라 지원 호출 수와 같은 지표를 최소화하려고 할 수도 있습니다.

전략을 구상하면 [!DNL Target Recommendations]의 구현을 시작할 준비가 된 것입니다.

추천 구현을 만드는 데에는 다음과 같은 세 가지 단계가 관련되어 있습니다.

![추천 구현을 만드는 단계를 보여 주는 그림](/help/main/c-recommendations/assets/intro-6.png)

1. [!DNL Target] 에 컨텍스트 또는 제품에 대해 교육합니다.
1. 사용자 행동을 파악합니다.
1. 상황에 맞는 추천을 받습니다.

### [!DNL Target] 에 컨텍스트 또는 제품에 대해 교육

[!DNL Recommendations]을 시작할 때 추천할 모든 항목에 대한 정보를 전달합니다. [!DNL Target] 은 카탈로그를 만들기 위한 몇 가지 통합 옵션을 제공합니다.

![컨텍스트 또는 제품에 대해 Target 교육 방법을 보여 주는 일러스트레이션](/help/main/c-recommendations/assets/intro-7.png)

가장 간편하고 자주 사용하는 방법은 제품 정보 관리 시스템 또는 콘텐츠 관리 시스템에서 매일 또는 매주 CSV 파일을 전송하는 것입니다. 그러나 [!DNL Adobe Target] Javascript 라이브러리를 사용하여 페이지에서 데이터 레이어에 대한 정보를 전달하거나, Adobe API를 사용하여 소스 시스템에서 직접 정보를 전달하거나, 이미 카탈로그 데이터를 [!DNL Analytics]에 전달한 경우 [!DNL Adobe Analytics] 통합을 사용할 수 있습니다.

예를 들어 경우에 따라 CSV 파일을 통해 대부분의 데이터를 매일 전달하고 API를 통해 보다 자주 인벤토리 업데이트를 전달하는 등 여러 옵션을 함께 사용할 수 있습니다.

IT 부서에서 일반적으로 이 단계 설정을 지원합니다.

어떤 방법을 선택하든 다음 세 가지 범주의 각 항목에 대한 메타데이터를 포함해야 합니다.

![카탈로그에 대한 메타데이터 정보를 보여 주는 일러스트레이션](/help/main/c-recommendations/assets/intro-8.png)

* 추천을 받는 사용자에게 표시하려는 데이터. 영화 이름, 썸네일 이미지 URL 등이 이에 해당합니다.
* 마케팅 및 판매 계획 관리에 유용한 데이터. 예를 들어 NC-17 영화를 추천하지 않도록 영화 등급을 지정합니다.
* 항목과 다른 항목의 유사성을 결정하는 데 유용한 데이터. 예를 들어 영화 장르나 영화 속 배우가 여기에 포함됩니다.

### 사용자 행동 파악

그런 다음 태그를 추가하거나 기존 [!DNL Analytics] 구현을 활용하여 [!DNL Target] 알고리즘을 구동하는 전환 이벤트(예: 보기 및 구매)를 추적해야 합니다.

![사용자 행동을 파악하는 방법을 보여 주는 일러스트레이션](/help/main/c-recommendations/assets/intro-9.png)

[!DNL Target] 은 사용자가 보고 구매하는 항목이 무엇인지 확인해야 합니다. 구매가 컨텍스트와 관련이 없는 경우 PDF 다운로드, 설문 조사 완료, 뉴스레터 가입, 비디오 보기 등과 같은 다른 유형의 전환 이벤트를 추적할 수 있습니다.

사이트에서 A/B 테스트 활동을 실행하는 데 이미 [!DNL Target] 을 사용 중인 경우 이 단계를 이미 완료했을 수 있습니다. 또는 사이트 방문 횟수 및 전환 동작에 대해 보고하기 위해 [!DNL Adobe Analytics] 을 사용하는 경우 [!DNL Analytics] 을 동작 데이터 소스로 사용할 수 있습니다. 그렇지 않은 경우, 의 태그와 같은 태그 관리자를 사용하여 설정하는 것이 더 쉽습니다 [[!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/). 또한 실시간 API를 통해 오프라인 또는 인앱 인터랙션을 [!DNL Target] 에 보낼 수도 있습니다.

### 상황에 맞는 추천 받기

상호 작용 시점에 사용자 및 컨텍스트에 대한 정보를 [!DNL Target] 에 전달하여 연관성 있고 개인화된 추천을 반환합니다.

![상황에 맞는 추천을 받는 방법을 보여 주는 그림](/help/main/c-recommendations/assets/intro-10.png)

집계에서 사용자 동작 외에 추천이 표시되는 특정 컨텍스트에 [!DNL Target] 을 전달해야 합니다. 여기에는 페이지 정보 및 사용자 프로필 정보가 포함됩니다. [!DNL Target] 은 이 정보를 사용하여 개인화된 추천을 제공합니다. 예를 들어 소매 웹 사이트에서는 방문자가 현재 보고 있는 제품 및 제품 범주를 알고 싶을 수 있습니다. 해당 사용자에 대한 정보(즐겨찾는 브랜드, 즐겨찾는 제품 범주, 로열티 계층 등)도 알고 싶을 수 있습니다. 이 정보는 [!DNL Target] 이 항목을 필터링하고 추천의 개인화를 개선할 수 있기 때문에 중요합니다.

## 첫 번째 추천 활동 만들기

[!DNL Recommendations] 활동이란 무엇입니까?

![우수한 추천을 만드는 요소를 보여 주는 그림](/help/main/c-recommendations/assets/intro-11.png)

[!DNL Recommendations] 활동은 다음과 같은 구성 요소로 구성됩니다.

* **대상**: 이러한 추천은 누가 보게 됩니까?
* **기준**: 어떤 항목을 추천해야 합니까?
* **디자인**: 추천 항목은 어떻게 표시됩니까?

![추천 활동을 구성하는 요소(대상, 기준 및 디자인)를 보여 주는 일러스트레이션](/help/main/c-recommendations/assets/intro-12.png)

기본적으로 [!DNL Target] 에는 14개의 내장된 대상, 42개의 내장된 기준 및 10개의 내장된 디자인 템플릿이 포함되어 있습니다. 이러한 각 항목을 사용자 정의하거나 직접 추가할 수 있습니다. Adobe는 이전에 [!DNL Target]에서 [대상 구축에 대한 웨비나](https://landing.adobe.com/acs/2018/na/adobe-target/registration.html) 를 개최했습니다. 이 섹션에서는 어떤 항목을 추천할 지에 대한 기준을 정의하는 데 중점을 둡니다.

Target는 기준 카드의 개념을 사용합니다. 기준 카드는 개인화를 위한 메뉴와 같습니다.

![기준 카드 일러스트레이션](/help/main/c-recommendations/assets/intro-13.png)

원하는 개인화 결과를 얻으려면 적절한 기준을 선택하거나 만들어야 합니다. 기준은 전체 카탈로그에서 최종 추천으로 안내하는 단계와 같습니다.

![단계 일러스트레이션](/help/main/c-recommendations/assets/intro-14.png)

다음 섹션에서는 이 단계의 다양한 부분과 [!DNL Target]에서 작동 방식을 설명합니다.

### 정적 필터(컬렉션 및 제외)

정적 필터는 자주 변경되지 않을 것으로 예상되는 카탈로그 속성과 관련하여 광범위하게 적용 가능한 규칙입니다.

![컬렉션 및 제외 일러스트레이션](/help/main/c-recommendations/assets/intro-16.png)

예를 들어 콘텐츠 컨텍스트에서 추천에 모든 영화를 포함하고 NC-17 등급의 영화는 제외할 수 있습니다. 소매 환경에서는 전 세계 다른 지역의 여러 브랜드를 사용할 수 있지만 미국에서 구할 수 있는 제품만 추천할 수 있습니다. 지역 개인 레이블의 제품을 제외시킬 수도 있습니다.

이는 여러 추천에 사용할 수 있고 자주 변경되지 않을 것으로 예상되며 광범위하게 적용 가능한 모든 카탈로그 속성입니다.

### 알고리즘(추천 키 및 논리)

다음 단계는 추천 키와 논리를 선택하는 것입니다. 여기에서 추천의 기반이 무엇인지 결정합니다.

![알고리즘 일러스트레이션](/help/main/c-recommendations/assets/intro-17.png)

가장 먼저 추천 키를 선택해야 합니다. 추천 키는 추천을 선택하기 위해 &#39;찾아보는&#39; 것입니다. 이는 사용자의 추천을 기반으로 하는 것입니다.

추천은 다음을 기반으로 할 수 있습니다.

* 방문자가 현재 보고 있는 항목
* 방문자가 현재 보고 있는 범주
* 방문자가 최근에 구매했거나 장바구니에 추가한 항목
* 방문자 또는 항목과 관련된 사용자 지정 속성

이러한 키를 기반으로 원하는 추천 논리를 선택합니다.

* 비슷한 속성을 갖는 항목
* 특정 범주에서 가장 많이 본 항목
* 이 항목을 구매한 고객이 구매한 다른 항목
* 사용자 지정 속성

기본적으로 [!DNL Target] 에는 알고리즘 포트폴리오가 포함되어 있습니다.

![알고리즘 포트폴리오 일러스트레이션](/help/main/c-recommendations/assets/intro-15.png)

* **인기도 기반 알고리즘** 에는 가장 많이 본 항목과 최상위 판매자가 포함됩니다.
* **콘텐츠 기반 알고리즘** 에는 콘텐츠 유사성이 포함됩니다.
* **항목 기반 협업 필터링 알고리즘** 에는 조회/조회, 조회/구매, 구매/구매가 포함됩니다. 구매는 모든 전환이 될 수 있습니다.
* **개인화된 알고리즘** 에는 최근에 본 항목, 사이트 친화성 및 프로필 향상 협업 필터링이 포함됩니다.
* **사용자 고유 알고리즘** 을 사용하여 사용자 지정 알고리즘을 사용할 수 있습니다.

### 온라인 비즈니스 규칙

마지막 단계는 온라인 비즈니스 규칙을 적용하는 것입니다. 이 단계에서 방문자가 디지털 에셋에 대해 수행하는 작업을 기반으로 도메인 지식과 현재 컨텍스트를 통해 알고리즘을 강화할 수 있습니다.

![온라인 비즈니스 규칙 일러스트레이션](/help/main/c-recommendations/assets/intro-18.png)

예를 들어 콘텐츠 컨텍스트에서 방문자가 이전에 시청한 영화를 제외시키거나 같은 감독의 영화를 추천하거나 동일한 장르의 영화를 더 많이 추가할 수 있습니다. 소매 환경에서는 재고 부족 제품을 제외하거나, $5~500 범위의 가격대에 있는 항목을 표시하거나, 동일한 브랜드의 항목을 늘릴 수 있습니다.

## 데모

위에서 설명한 추천 단계에 표시된 작업을 완료하면 최종 추천이 표시됩니다. [!DNL Target]에서 제품 내 데모를 시청하려면 아래 링크를 클릭하십시오. *Adobe Target 기본 사항 웨비나*&#x200B;에서 9시에 시작됩니다.

## Adobe [!DNL Target] 기본 사항 웨비나: Recommendations 소개 {#intro-to-recs}

[Recommendations 소개](https://adobecustomersuccess.adobeconnect.com/p8gt31drhs3e/?OWASP_CSRFTOKEN=4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)