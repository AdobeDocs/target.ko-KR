---
keywords: Recommendations;Recommendations criteria;recommendations algorithms;recommendations activity;criteria;recommendations targeting;recs
description: Adobe Target의 Recommendations 활동은 이전 사용자 활동 또는 기타 알고리즘을 기반으로 고객의 관심을 끌 수 있는 제품 또는 컨텐츠를 자동으로 표시합니다. 권장 사항은 고객이 모를 수 있는 관련 항목을 고객에게 표시하는 데 도움이 됩니다.
title: Adobe Target Recommendations
feature: Recommendations
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 59%

---


# ![PREMIUM](/help/assets/premium.png) 권장 사항{#recommendations}

[!DNL Adobe Target Recommendations] 활동은 이전 사용자 활동, 기본 설정 또는 기타 기준을 기반으로 방문자의 관심을 끌 수 있는 제품, 서비스 또는 컨텐츠를 자동으로 표시합니다. [!DNL Target Recommendations] 방문자가 모르는 관련 항목으로 안내하는 데 도움이 됩니다. [!DNL Recommendations] 방문자에게 적절한 시기에 적절한 컨텐츠를 제공할 수 있습니다.

>[!NOTE]
>
>[!DNL Recommendations] 작업은 [Target Premium 솔루션](/help/c-intro/intro.md#premium)의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다.
>
>[!DNL Recommendations Classic]을 사용 중이라면 [Recommendations Classic과 Target Premium의 권장 사항 활동 비교](/help/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md#concept_A80223EF66634EA380580C2823A581C5)를 참조하십시오.

[!DNL Recommendations]은 채널, 앱, 페이지, 이메일 메시지 및 기타 전달 선택 사항에 대해 실시간 제안을 최적화 및 사용자 지정하여 관리 노력을 줄이면서도 참여 및 전환을 높이는 데 유용합니다.

[!DNL Recommendations]은 다음 작업에 유용합니다.

* 권장 사항을 자동화하는 정교한 기준(규칙) 만들기
* 몇 개의 JavaScript 코드 조각을 사용하여 자동으로 권장 사항 표시
* 권장 사항을 표시하는 권장 사항 기준 및 디자인 테스트 및 최적화
* 권장 사항 활동 결과에 대한 보고서

다음 그림은 웹 페이지에 권장 사항을 보여줍니다.

![](assets/velocity_example.png)

권장 사항은 사이트에서의 방문자 활동에 따라 방문자에게 제품을 제안하는 방법을 결정합니다. 예:

| 원하는 작업 | 권장 사항 |
|--- |--- |
| 배낭을 구입하는 사람이 하이킹 신발과 등산용 스틱까지 구입하도록 유도합니다. | &quot;이 항목을 구입하고 다른 항목도 구입한 사람&quot; 알고리즘을 사용하여 종종 함께 구입하는 항목을 보여주는 권장 사항을 생성합니다. |
| 시청 중인 내용과 유사한 미디어 콘텐츠를 추천하여 방문자가 여러분의 미디어 사이트에서 보내는 시간을 늘립니다. | &quot;이 항목을 보고 다른 항목도 본 사람&quot; 기준을 사용하여 다른 비디오를 제안하는 권장 사항을 생성합니다. |
| 또한 은행의 저축 제도에 대한 정보를 본 고객이 IRA 계좌에 대해서도 읽도록 제안합니다. | &quot;이 항목을 보고 다른 항목도 구입한 사람&quot; 기준을 사용하여, 권장 사항에 있는 첫 번째 제품을 표시하지 않고 고객이 한 제품을 본 후에 구입한 다른 제품을 표시합니다. |

이러한 기준 및 기타 [!DNL Recommendations] 기준에 대한 자세한 내용은 [기준](/help/c-recommendations/c-algorithms/algorithms.md)을 참조하십시오.

## 용어

[!DNL Recommendations]을(를) 사용하기 전에 이 섹션에 사용된 용어의 일부를 알고 있으면 유용합니다. 아직 이 용어를 완전히 이해하지 못하면 [!DNL Recommendations] 활동을 설정할 때 해당 용어에 더욱 익숙해질 것입니다.

| 용어 | 정의 |
| --- | --- |
| 활동 | [!DNL Target]의 활동을 사용하면 특정 대상에 맞게 컨텐츠를 개인화하고 페이지 디자인을 테스트할 수 있습니다. [!DNL Recommendations] 은 에서 사용할 수 있는 여러 활동 유형 중 하나에 불과합니다 [!DNL Target]. 자세한 내용은 [Target 활동 유형](/help/c-activities/target-activities-guide.md)을 참조하십시오. |
| 엔티티 | 엔티티는 추천할 항목을 나타냅니다. 엔티티는 제품, 컨텐츠(기사, 슬라이드 쇼, 이미지, 동영상, tv 쇼), 취업 목록, 레스토랑 등과 같은 모든 것을 사용할 수 있습니다. 자세한 내용은 [엔티티](/help/c-recommendations/c-products/products.md)를 참조하십시오. |
| 피드 | 피드는 개체를 [!DNL Recommendations]으로 가져오는 데 사용됩니다. 엔티티는 CSV 파일, Google 제품 검색 피드 형식 및/또는 Adobe Analytics 제품 분류를 사용하여 보낼 수 있습니다. 자세한 내용은 [피드](/help/c-recommendations/c-products/feeds.md)를 참조하십시오. |
| 카탈로그 | 카탈로그는 전체 제품 세트(엔티티)를 의미합니다. 카탈로그에는 여러 컬렉션이 포함될 수 있으며 이는 제품을 논리 버킷으로 구성하는 방법입니다. |
| 컬렉션 | 컬렉션은 단일 제품 카테고리와 같이 유사하거나 관련된 항목 집합을 의미합니다. 그러나 어떤 항목이든 특정 가격 범위나 색상 또는 특정 지역에서 관심을 가질 수 있는 항목 등, 비즈니스에 의미가 있는 카테고리로 그룹화할 수 있습니다. 자세한 내용은 [컬렉션](/help/c-recommendations/c-products/collections.md)을 참조하십시오. |
| 기준 | 기준은 사전 결정된 방문자 행동 세트를 기준으로 추천할 제품을 결정하는 규칙입니다.<br>기준의 몇 가지 예는 다음과 같습니다. <ul><li>이 항목을 구입하고 다른 항목도 구입한 사람</li><li>이 항목을 보고 다른 항목도 본 사람</li><li>비슷한 속성을 갖는 항목</li><li>마지막으로 구매한 항목</li><li>즐겨찾는 카테고리</li></ul>  자세한 내용은 [기준](/help/c-recommendations/c-algorithms/algorithms.md)을 참조하십시오. |
| 디자인 | 디자인은 행, 열, 표 또는 격자와 같은 [!DNL Recommendations] 활동에서 권장 사항의 모양을 정의합니다. 이 문서의 상단에 있는 그림은 4 x 1 디자인을 보여줍니다. 자세한 내용은 [디자인 만들기](/help/c-recommendations/c-design-overview/create-design.md)를 참조하십시오. |
| 위치 | 위치는 개인화 및 최적화를 위한 활동을 실행하는 웹 페이지, 모바일 앱 또는 이메일의 특정 컨텐츠 영역을 의미합니다. |
| 대상자 | 대상은 타깃팅된 활동을 볼 비슷한 활동 참여자의 그룹입니다. 대상은 새 방문자, 재방문자 또는 중서부의 재방문자와 같이 동일한 특성을 가진 사람 그룹입니다. 대상 기능을 사용하면 적절한 시간에 적절한 사람에게 적절한 메시지를 표시하여 웹 마케팅을 최적화하도록 다양한 콘텐츠 및 경험을 특정 대상에 타깃팅할 수 있습니다. 자세한 내용은 [대상](/help/c-target/target.md)을 참조하십시오. |
| 오퍼로서의 Recommendations | A/B 테스트(자동 할당 및 자동 Target 포함) 및 경험 타깃팅(XT) 활동 내에 권장 사항을 포함할 수 있는 기능입니다. 자세한 내용은 [오퍼로서의 Recommendations](/help/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오. |

## 교육 비디오:활동 유형 ![개요 배지](/help/assets/overview.png)

다음 비디오에서는 [!DNL Target Standard/Premium]에서 사용할 수 있는 활동 유형에 대해 설명합니다. [!DNL Recommendations]은 7:20부터 설명합니다.

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로우 설명

>[!VIDEO](https://video.tv.adobe.com/v/17386)

## Adobe Target 기본 사항 웨비나: Recommendations 소개 ![자습서 배지](/help/assets/tutorial.png) {#intro-to-recs}

*권장 사항 소개* 웨비나에서는 [!DNL Adobe Target Recommendations] 값을 활용하는 방법에 대한 심층적인 설명을 포함합니다. 이 [!DNL Target] 활동에서는 이전 방문 횟수에 따라 실시간 제안을 최적화하여 고객의 흥미를 끌 수 있는 제품 또는 콘텐츠를 자동으로 표시하는 방법을 알아봅니다. 또한 [!DNL Target] UI에서 [!DNL Recommendations] 활동을 구축하는 방법에 관한 단계별 개요를 살펴보십시오.

[추천 소개](https://adobecustomersuccess.adobeconnect.com/p8gt31drhs3e/?OWASP_CSRFTOKEN=4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)