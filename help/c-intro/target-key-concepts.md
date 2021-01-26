---
keywords: Overview and Reference;act
description: Adobe Target의 기능 및 성능을 이해하는 데 도움이 되는 주요 개념에 대한 정보입니다.
title: Target 주요 개념
feature: Overview
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 98%

---


# Target 주요 개념{#target-key-concepts}

Adobe Target의 기능 및 성능을 이해하는 데 도움이 되는 주요 개념에 대한 정보입니다.

## 활동 및 테스트 {#section_BEA0A0C51A8847579B566060206DE7E8}

활동은 사이트 방문자가 접할 수 있는 경험을 결정합니다.

예를 들어 여성의 여름 신발에 대한 정보를 강조 표시하는 페이지와 보다 일반적인 여성 의류를 강조 표시하는 페이지 등 두 개의 다른 랜딩 페이지를 테스트하는 활동을 디자인할 수 있습니다. 활동은 이러한 각 랜딩 페이지가 표시되는 시기를 제어하는 조건과 보다 성공적인 페이지를 확인하는 지표를 결정합니다. 특정 날짜 사이 등의 특정 조건이 충족될 때 시작되고 종료되거나 활동이 승인될 때 시작되고 비활성화될 때 종료되도록 활동이 구성됩니다.

활동을 디자인할 때는 신중하게 계획해야 합니다. 활동이 시작되는 시기와 지속되는 기간을 결정하십시오. 그런 후에 오퍼를 표시하고 각 오퍼에 대상을 할당합니다.

Target에는 여러 가지 활동 유형이 포함됩니다. 다음 표는 자세한 내용을 알 수 있는 링크와 함께 각 활동 유형에 대한 개요를 제공합니다. 목적에 가장 적합한 활동 유형을 선택하는 데 도움이 되도록 [Adobe Target 활동 안내서](/help/c-activities/target-activities-guide.md)를 만들었습니다.

| 활동 유형 | 설명 |
|--- |--- |
| [A/B 테스트](/help/c-activities/t-test-ab/test-ab.md) | A/B 테스트에서는 웹 사이트 콘텐츠의 버전을 두 개 이상 비교하여 사전 지정된 테스트 기간에 전환율이 가장 많이 향상된 버전을 확인합니다.<br>**참고:** 이제 [A/B 테스트 활동 내에 권장 사항](/help/c-recommendations/recommendations-as-an-offer.md)을 포함할 수 있습니다. 이 기능을 사용하려면 [Target Premium 라이센스](/help/c-intro/intro.md#premium)가 있어야 합니다. |
| [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 자동 할당은 둘 이상의 경험에서 승자를 식별하고, 테스트가 계속 실행되고 학습되는 동안 변환을 늘리기 위해 더 많은 트래픽을 승자에게 자동으로 재할당합니다.<br>**참고:** 이제 [자동 지정 활동 내에 권장 사항](/help/c-recommendations/recommendations-as-an-offer.md)을 포함할 수 있습니다. 이 기능을 사용하려면 [Target Premium 라이센스](/help/c-intro/intro.md#premium)가 있어야 합니다. |
| [자동 타겟](/help/c-activities/auto-target/auto-target-to-optimize.md)<br>![Target Premium](/help/assets/premium.png) | 자동 타겟은 콘텐츠를 개인화하고 전환을 유도하기 위해 고급 기계 학습을 사용하여 성과가 좋은 마케터가 정의한 여러 경험 중에서 식별하고, 개별 고객 프로필과, 이 프로필과 유사한 프로필을 가진 이전 방문자의 행동을 기반으로 각 방문자에게 가장 잘 맞춤 설정된 경험을 제공합니다.<br>**참고:** 이제 [자동 타겟 활동 내에 권장 사항](/help/c-recommendations/recommendations-as-an-offer.md)을 포함할 수 있습니다. 이 기능을 사용하려면 [Target Premium 라이센스](/help/c-intro/intro.md#premium)가 있어야 합니다. |
| [Analytics 데이터 사용](/help/c-activities/t-test-ab/t-test-create-ab/create-a4t.md)(A4T) | [!DNL Adobe Analytics]를 보고 소스로 사용하도록 활동을 구성할 수 있습니다. 이 활동 유형을 사용하려면 [!DNL Adobe Experience Cloud] 계정을 [!DNL Analytics]와 [!DNL Target] 모두에 연결해야 합니다. |
| [다변량 테스트](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | 다변량 테스트(MVT)는 페이지의 요소에 있는 오퍼 조합을 비교하여 특정 대상에 대해 성과가 가장 좋은 조합을 판별하고 활동의 성공에 영향을 가장 많이 주는 요소를 식별합니다. |
| [경험 타깃팅](/help/c-activities/t-experience-target/experience-target.md) | 경험 타깃팅(XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상에 전달합니다.<br>**참고:** 이제 [경험 타깃팅 활동 내에 권장 사항](/help/c-recommendations/recommendations-as-an-offer.md)을 포함할 수 있습니다. 이 기능을 사용하려면 [Target Premium 라이센스](/help/c-intro/intro.md#premium)가 있어야 합니다. |
| [자동화된 개인화](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>![Target Premium](/help/assets/premium.png) | 자동화된 개인화(AP)는 콘텐츠를 개인화하고 전환을 유도하기 위해, 오퍼나 메시지를 결합하고 고급 기계 학습을 사용하여 방문자의 개별 고객 프로필을 기반으로 다양한 변형을 각 방문자와 연결합니다. |
| [Recommendations](/help/c-recommendations/recommendations.md)<br>![Target Premium](/help/assets/premium.png) | 권장 사항은 사이트에서의 사용자 활동에 따라 웹 사이트 사용자에게 제품을 제안하는 방법을 결정합니다.<br>예를 들어, 배낭을 구입하는 사람이 하이킹 신발과 등산용 스틱까지 구입하도록 하려는 경우, &quot;이 항목을 구입하고 다른 항목도 구입한 사람&quot; 알고리즘을 사용하여 종종 함께 구입하는 항목을 보여주는 권장 사항을 생성할 수 있습니다. 또는 &quot;이 항목을 보고 다른 항목도 본 사람&quot; 알고리즘을 사용하여 방문자에게 보고 있는 것과 유사한 비디오를 추천하여 미디어 사이트에서 더 많은 시간을 소비하도록 할 수도 있습니다.<br>**참고:** 이제 A/B 테스트(자동 할당 및 자동 타겟 포함)와 경험 타깃팅(XT) 활동 내에 권장 사항을 포함할 수 있습니다. [오퍼로서의 Recommendations](/help/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오. |

## 위치 {#section_F18FBF1ED23340ED9F39C51971A4E874}

위치는 주로 웹 사이트의 페이지입니다. 모바일 앱이나 이메일의 한 위치 또는 최적화를 실행하는 기타 위치를 의미할 수도 있습니다.

위치는 활동 및 경험에 필수적입니다. 여러분은 위치에서 다음 작업 중 하나를 수행할지, 둘 다 수행할지 또는 다 수행하지 않을지 결정합니다.

* 방문자에 대한 콘텐츠를 표시하고 바꾸기
* 방문자 행동 기록

[!DNL Target Standard]에서 위치는 추적하려는 각 페이지의 `<head>` 섹션에서 [!DNL Target]을 활성화하는 단일 코드 행을 페이지가 포함하는 한 페이지의 모든 요소가 될 수 있습니다. 이 코드 행은 정보를 수집하고 방문자에게 타깃팅된 경험을 전달하는 데 필요한 JavaScript 라이브러리를 호출합니다.

위치는 대상과 결합하여 고객에게 타깃팅 정보에 대한 선택 사항을 거의 무제한으로 제공합니다. 예를 들어, 방문자가 이전에 사이트를 방문한 적이 없는 경우 신규 고객용 할인 쿠폰을 표시할 수 있습니다. 마찬가지로, 페이지가 재방문 고객에게 더 최적화된 오퍼를 표시하도록 변경될 수도 있습니다.

또한 위치를 사용하여 방문자의 웹 사이트 진행 상황을 추적하거나 방문자가 장바구니에 항목 추가, 구입 완료 등의 특정 성공 지표를 완료하는지 여부를 추적할 수도 있습니다.

## 경험 및 페이지 디자인 {#section_B806FB752EC1470784755C1EB3D4AC70}

레서피라고도 하는 경험은 페이지에 표시되는 콘텐츠를 정의하며, 뿐만 아니라 링크와 같은 기타 페이지 요소도 정의합니다.

경험은 특정 타깃팅 조건이 충족되면 특정 위치에 어떤 오퍼가 표시될지 결정합니다. 예를 들어 경험은 재방문자가 사이트를 방문할 경우 페이지 맨 위에 2일 배송 오퍼가 표시되는 것을 결정하기도 하고, 처음 온 방문자가 페이지를 볼 때 동일한 위치에 10% 할인이 나타나는 것을 결정하기도 합니다.

경험은 방문자를 여러분이 원하는 결과로 유도하는 데 도움이 되도록 페이지에 표시되는 오퍼, 이미지 자산 또는 기타 HTML 요소(예: 링크)로 구성됩니다. [!DNL Target]은 위치, 오퍼 및 경험을 결합하여 특정 테스트 동안 사이트에 표시되는 콘텐츠를 결정합니다.

경험은 다른 페이지 디자인일 수도 있습니다. 예를 들어, 한 경험에서는 페이지의 맨 위에 하나의 링크 세트를 배치할 수 있으며, 반면에 다른 경험에서는 다른 링크가 배치되거나 다른 순서로 배열된 동일한 링크들이 배치될 수 있습니다. 한 이미지가 다른 이미지보다 더 많은 상승도를 제공하는지 테스트하거나, 광고를 페이지 상단에서 클릭할 가능성이 더 큰지 아니면 다른 위치에서 클릭할 가능성이 더 큰지 테스트할 수 있습니다.

[!DNL Target]은 디지털 터치포인트에서 각 방문자에 대한 경험을 최적화하고, 서로 다른 경험을 테스트하여 가장 성공적인 경험을 결정합니다. 신중하게 계획된 경험 타깃팅을 통해 사이트 방문자에게 가장 적합한 오퍼가 페이지에서 적절한 위치에 표시되도록 하여 성공적인 방문 가능성을 높일 수 있습니다.

## 오퍼 {#section_973D4CC4CEB44711BBB9A21BF74B89E9}

오퍼는 캠페인이나 활동 중 웹 페이지에 표시되는 콘텐츠입니다.

웹 페이지를 테스트할 때에는 위치에 있는 다양한 오퍼를 통해 각 경험의 성공을 측정합니다.

오퍼는 다음 항목을 포함하여 다양한 유형의 콘텐츠를 포함할 수 있습니다.

* 이미지
* 텍스트
* HTML
* 링크
* 단추

예를 들어, 웹 페이지는 방문자가 전에 사이트에 왔었는지 여부에 따라 두 오퍼 중 하나를 표시할 수 있습니다.

*경험*&#x200B;은 특정 조건이 충족될 경우 표시되는 콘텐츠를 결정합니다.

## 대상자{#section_3F32DA46BDF947878DD79DBB97040D01}

특정 기준을 충족하는 활동 참여자에게 타깃팅된 콘텐츠를 최적화하십시오.

대상은 활동에 대한 타겟을 정의하며 타깃팅을 사용할 수 있는 모든 곳에서 사용됩니다.

[!DNL Target] 대상은 정의된 방문자 기준 세트입니다. 오퍼를 특정 대상(또는 세그먼트)에 타깃팅할 수 있습니다. 해당 대상에 속하는 방문자에게만 이들을 타깃팅하는 경험이 표시됩니다.

예를 들어, 활동을 특정 브라우저나 운영 체제를 사용하는 방문자로 구성된 대상에 타깃팅할 수 있습니다.

또는 활동을 한 지역의 방문자나 특정 검색 엔진에서 페이지에 액세스하는 사람들에 타깃팅할 수 있습니다.

여러 활동에서 재사용할 수 있도록 대상을 저장하거나, 특정 활동용으로 대상을 만들 수 있습니다.

| 대상 유형 | 설명 |
|--- |--- |
| 재사용 가능한 대상 | 재사용 가능한 대상은 활동용으로 선택할 수 있습니다. 이러한 대상 중 하나를 변경하면 이 대상을 사용하는 모든 활동에 대해 대상이 변경됩니다. |
| 사용자 지정 세그먼트 | 사용자 지정 세그먼트(캠페인별 세그먼트라고도 함)는 Target Classic에서 캠페인에 따라 다릅니다. 캠페인의 일부로 생성되며 다른 캠페인에서 다시 사용할 수 없습니다. |
| 공유 대상 | 대상은 [!DNL Adobe Experience Cloud] 솔루션에서 공유할 수 있습니다. 예를 보려면 [대상](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)을 참조하십시오. |

방문자 프로필에서 어떻게 사이트 방문자에 대한 정보를 추적하는지에 대해서는 [방문자 프로필](/help/c-target/c-visitor-profile/visitor-profile.md#concept_5E53D1A6DF224D7BAE76F4AE390B9DA1)을 참조하십시오.

## 교육 비디오:

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### 활동 유형(9:03)  ![개요 배지](/help/assets/overview.png)

다음 비디오에서는 [!DNL Target Standard/Premium]에서 사용할 수 있는 활동 유형에 대해 설명합니다.

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로우 설명

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Adobe Target에서 대상 사용(6:21) ![개요 배지](/help/assets/overview.png)

다음 비디오에서는 [!DNL Target Standard/Premium]에서 대상을 사용하는 방법을 설명합니다.

* 용어 &quot;대상&quot; 설명
* 최적화에 대상을 사용하는 두 가지 방법 설명
* 대상자 목록에서 대상자 찾기
* 활동을 대상에 타깃팅
* 활동에서 수동 보고에 대상 사용

>[!VIDEO](https://video.tv.adobe.com/v/17398)
