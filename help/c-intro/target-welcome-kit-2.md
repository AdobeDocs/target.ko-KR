---
keywords: welcome kit;target welcome kit;intro;introduction;getting started
description: Adobe Target 환영 키트 - 2장 - Target 개요
title: Adobe Target 환영 키트 - 2장 - Target 개요
feature: intro
translation-type: tm+mt
source-git-commit: e18f18e6d6e0b8fc6eb5ada845e2fe5377d6c5d0
workflow-type: tm+mt
source-wordcount: '2504'
ht-degree: 16%

---


# 2장:Adobe Target

사용을 시작하기 전에 솔루션 [!DNL Adobe Target]의 개요 수준을 높이는 데 도움이 될 수 있습니다. 이 장에서는 솔루션의 주요 기능, 사용할 수 있는 브랜드 접점, 구현 옵션, 중요한 유저 인터페이스 기능 및 워크플로우, 관리 기능 및 전반적인 해당 역할에 대해 자세히 설명합니다 [!DNL Adobe Experience Cloud]. 피쳐로 명시되지 않는 한 이 장에 설명된 항목은 [!DNL Adobe Target Premium] 및 [!DNL Adobe Target Premium] [!DNL Adobe Target Standard]함께 사용할 수 있습니다. For more information, see [Introduction to Target](/help/c-intro/intro.md).

## 기능 및 활동

테스트 및 개인화는 두 가지 다양한 유형의 기능으로서 [!DNL Target] , &quot;활동&quot;을 만들 때 사용할 수 있습니다 [!DNL Target]. &quot;테스트&quot;라는 용어는 &quot;최적화&quot; 및 &quot;개인화&quot;와 함께 &quot;타깃팅&quot;과 혼용적으로 사용되는 것을 볼 수 있습니다.

테스트 활동에서는 디지털 경험의 한 가지 변형과 하나 이상의 다른 변형을 비교하여 가장 많은 방문자가 원하는 작업을 수행하도록 하는 변형을 발견했습니다. [!DNL Target] 은 다음과 같은 테스트 기능을 제공합니다.A/B 테스트, MVT(다변량 테스트) 및 자동 할당

개인화 활동을 통해 특정 방문자 그룹 또는 각 개별 방문자에 맞는 디지털 경험을 제공할 수 있습니다. [!DNL Target] 다음과 같은 개인화 기능을 제공합니다.경험 타깃팅, 자동 Target, Automated Personalization 및 Recommendations

각 기능의 사용 시기 및 방법에 대한 자세한 내용은 [Target 활동 유형을 참조하십시오](/help/c-activities/target-activities-guide.md).

| 활동 유형 | 세부 사항 |
| --- | --- |
| A/B 테스트 | 웹 사이트 또는 기타 디지털 고객 접점의 두 개 이상의 다양한 경험 또는 오퍼를 비교하여 사전 지정된 테스트 기간 동안 주요 비즈니스 측정이 가장 개선되는 변화를 확인합니다. A/B 테스트는 새로운 웹 페이지 레이아웃, 다양한 사이트 탐색 방법, 복사, 이미지 및 클릭유도문안 버튼과 같은 디지털 경험의 개별 요소에 대한 완전히 다른 처리와 같은 큰 변경에 적합합니다. [추가 정보](/help/c-activities/t-test-ab/test-ab.md). |
| 자동 할당 | 두 개 이상의 경험 중에서 가장 성과가 좋은 경험을 식별하고 우승자에게 더 많은 트래픽을 자동으로 재할당하여 테스트를 계속 실행하고 학습하면서 전환율을 높입니다. 강력한 인공 지능(AI) [!DNL Adobe Sensei]사용 [추가 정보](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| 자동 Target<br>(Premium) | Adobe Sensei AI를 활용하여 개인 고객 프로필 [!DNL Target] 과 비슷한 프로파일을 사용한 이전 방문자의 행동을 기반으로 각 방문자에게 최상의 경험을 확인하고 전달할 수 있습니다. 자동 Target을 통해 규모에 맞게 개인화할 수 있습니다. [추가 정보](/help/c-activities/auto-target/auto-target-to-optimize.md). |
| Automated Personalization<br>(Premium) | 오퍼에서 다양한 이미지, 복사 및 기타 요소의 조합을 검토하여 방문자당 전환율 또는 매출 증가와 같은 비즈니스 목표를 달성하는 데 가장 효과적인 조합을 각 방문자에게 전달하는 데 사용되는 고급 기계 학습 알고리즘 및 자동화 기능을 사용할 수 있습니다. [!DNL Adobe Sensei] [추가 정보](/help/c-activities/t-automated-personalization/automated-personalization.md). |
| 경험 타깃팅(XT) | 사용자 정의 규칙 및 기준을 기반으로 특정 사용자에게 컨텐츠를 전달할 수 있습니다. **[!UICONTROL 경험 타깃팅은]** 고객이 가치 있고 경험의 반향을 잘 알고 있는 경우 특정 경험이나 컨텐츠를 특정 대상자에게 타깃팅하는 데 유용합니다. [추가 정보](/help/c-activities/t-experience-target/experience-target.md). |
| MVT(다변량 테스트) | 페이지 또는 디지털 경험에 있는 요소의 가능한 모든 변형 조합을 비교할 수 있습니다. 예를 들어 세 개의 다른 배경 이미지, 두 가지 사본 변형, 두 개의 서로 다른 단추 색상 등이 있습니다. MVT는 특정 대상에 가장 적합한 조합을 결정하고 결과에 가장 영향을 주는 요소를 결정합니다. [추가 정보](/help/c-activities/c-multivariate-testing/multivariate-testing.md). |
| Recommendations<br>(Premium) | Adobe Sensei AI를 사용하면 고객의 이전 활동과 다른 고객의 행동에 따라 고객의 관심을 끌 수 있는 제품 또는 컨텐츠를 자동으로 제안할 수 있습니다. [추가 정보](/help/c-recommendations/recommendations.md). |

## 채널

웹 사이트, 모바일 사이트 및 모바일 앱과 같은 기존 디지털 접점을 비롯하여 키오스크, 이메일, IoT 디바이스, 게임 콘솔, Alexa 및 Cortana와 같은 음성 보조자 등 어디에서나 디지털 경험을 테스트하고 개인화할 수 있습니다. [!DNL Target] 많은 회사가 웹 사이트 [!DNL Target] 에서 사용을 시작합니다. 그러나 최근 조사에서 더 많은 사람들이 자신의 모바일 장치에서 브랜드를 방문한다고 나타났습니다. 이제 모바일 채널을 최적화하는 것이 필수적입니다. 가장 좋은 방법은 모든 접점에서 방문자의 경험을 연결하여 매끄럽고 일관된 경험을 제공하는 것입니다.

| 채널 | 세부 사항 |
| --- | --- |
| 웹 사이트 | [!DNL Target] 다중 페이지, 단일 페이지 애플리케이션(SPA) 및 모바일 웹 사이트의 페이지에서 A/B 테스트, Multivariate Testing, 경험 타깃팅, 자동 할당, 자동 Target, Automated Personalization 및 Recommendations 활동을 실행하여 방문자 및 고객 참여도를 향상시키고 전환율을 높이며 매출을 높일 수 있습니다. |
| 모바일 웹 | [!DNL Target] 모바일 웹 사이트 페이지에서 웹 사이트에서 실행하는 모든 동일한 활동 유형을 실행하는 데 사용할 수 있으므로 방문자와 고객 참여도를 비슷하게 향상시키고 전환율을 높이며 매출을 높일 수 있습니다. |
| 모바일 앱 | [!DNL Target] 사용자 행동과 모바일 컨텍스트에 따라 모바일 앱 경험을 테스트하고 개인화할 수 있습니다. [!DNL Target] 인터랙티브한 테스트뿐만 아니라 경험 타깃팅 및 AI 기반의 개인화를 통해 고객의 참여를 유도하고 전환율을 높일 수 있습니다. 모바일 앱 [!DNL Target] 에서 사용하려면 Adobe Mobile Services SDK를 사용해야 합니다. |
| IoT/Everywhere | [!DNL Target] 브라우저가 없거나 JavaScript 코드를 사용하지 않는 접점의 기존 웹 사이트, 모바일 사이트 및 모바일 앱에서 사용하는 활동에 동일한 테스트 및 개인화 기능을 사용할 수 있도록 서버측 구현을 제공합니다. 예를 들어 키오스크, 셋톱 박스, 게임 콘솔, 음성 도우미 및 기타 비전통적인 접점을 테스트 및 개인화할 수 있습니다. |

## 구현

많은 사용자가 기존의 웹 및 모바일 접점을 비롯한 다양한 디지털 접점을 테스트하고 개인화할 [!DNL Target] 수 있을 뿐만 아니라 브라우저가 없거나 JavaScript 코드를 사용하지 않는 접점도 사용하고 싶을 수 있습니다. 경우에 따라 내부 또는 외부 정책을 사용하려면 추가 수준의 제어 및 보안이 필요합니다. 성능상의 이유로 백엔드 서버에서 실행해야 하는 프로세스가 있을 수도 있습니다. Adobe는 이러한 다양한 용도를 충족하기 위해 다양한 방식 [!DNL Target] 으로 구현할 수 있는 기능을 제공합니다.클라이언트측, 서버측 또는 두 항목의 조합입니다.

| 구현 유형 | 세부 사항 |
| --- | --- |
| 고객측 | With this implementation of [!DNL Target], [!DNL Target] delivers the experiences associated with an activity directly to the client browser. 브라우저는 표시할 경험을 결정하고 표시합니다. With client-side, you can use a WYSIWYG editor, the **[!UICONTROL Visual Experience Composer]** (VEC), or a non-visual interface, the **[!UICONTROL Form-based Experience Composer]**, to create your test and personalization experiences. [추가 정보](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). |
| 서버측 | 이러한 유형의 [!DNL Target] 구현에서 클라이언트 장치는 서버를 통해 경험을 요청하고, 사용자의 서버는 요청을 보내고, [!DNL Target]응답을 서버로 [!DNL Target] 다시 전송하며, 서버는 렌더링할 클라이언트 장치에 제공할 경험에 대해 결정합니다. 경험은 음성 도우미를 통해 또는 시각적이지 않은 경험 또는 브라우저를 기반으로 하지 않는 장치를 통해 이메일이나 키오스크에 표시될 수 있습니다. 서버가 클라이언트와 [!DNL Target] 사이에 존재하기 때문에 제어력과 보안이 필요하거나 서버에서 실행하려는 복잡한 백엔드 프로세스가 있는 경우에 이러한 유형의 구현이 이상적입니다. [추가 정보](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| 하이브리드 구현 | 이 구현에서는 주어진 사용 사례에 가장 적합한 구현 방법을 선택합니다. 예를 들어, 클라이언트측 구현을 사용하여 A/B 구현으로 홈 페이지의 영웅 배너에서 오퍼를 테스트하고, 서버측 구현을 사용하여 클라이언트 브라우저에 표시할 내부 검색 결과, 스마트 자동차 대시보드에 표시할 경험 또는 음성 도우미로부터 전달하는 음성 응답을 결정할 수 있습니다. |

## 활동 요소

또한 개인화 활동 [!DNL Target], 최적화 활동 또는 개인화 접근 방식을 최적화하는 활동을 만들 수 있습니다. 각 활동에는 테스트 또는 개인화, 경험을 제공할 대상 또는 개인, 활동의 영향을 측정하는 지표, 그리고 시각적으로 그 영향을 표시하는 보고서 등 주요 요소가 있습니다.

| 요소 유형 | 세부 사항 |
| --- | --- |
| 경험 | 구매 단계 또는 다른 논리적 페이지 순서를 구성하는 페이지, 전체 웹 페이지 또는 페이지 세트에 있는 오퍼, 이미지, 텍스트, 단추, 비디오, 이러한 여러 요소의 조합입니다. 음성 도우미, 고객 서비스 스크립트 또는 음료 자판기의 개인화된 향에 대한 답변일 수도 있습니다. [!DNL Target] 활동에서 경험을 테스트하거나 개인화합니다. [추가 정보](/help/c-experiences/experiences.md). |
| 오퍼 | 이미지, 텍스트, HTML, 링크, 비디오, 클릭유도문안, 음성 지원 응답 또는 기타 유형의 컨텐츠가 포함될 수 있는 컨텐츠 블록. 할인, 무료 배송 등의 혜택이 있을 수 있습니다. 웹 페이지에 오퍼를 표시할 수 있지만 음성 지원 또는 게임 콘솔과 같은 모든 고객 접점에서 경험할 수도 있습니다. 오퍼를 테스트하면 다른 오퍼와 비교하거나 오퍼가 없는 경우와 비교하여 성공 여부를 측정합니다. [추가 정보](/help/c-experiences/c-manage-content/manage-content.md). |
| 대상자 | 새 방문자, 재방문자 또는 중서부의 재방문자와 같이 동일한 특성을 가진 사람 그룹입니다. 대상 기능을 사용하면 적절한 시간에 적절한 사람에게 적절한 메시지를 표시하여 웹 마케팅을 최적화하도록 다양한 콘텐츠 및 경험을 특정 대상에 타깃팅할 수 있습니다. If a visitor is identified as part of a target audience, [!DNL Target] determines which experience to display, based on criteria defined during activity creation. [추가 정보](/help/c-target/target.md). |
| 성공 지표 | Key business measures that enable you to determine the success of a given experience or offer in a [!DNL Target] activity. 예를 들어 새 오퍼가 방문자당 매출을 늘리는지 또는 장바구니에 품목을 추가할지 여부를 결정할 수 있습니다. 성공 지표는 등록, 주문 또는 구매 흐름과 관련된 문제뿐만 아니라 방문자나 고객 참여와 관련된 문제를 발견하는 데에도 유용할 수 있습니다. [추가 정보](/help/c-activities/r-success-metrics/success-metrics.md). |
| 보고서 | 데이터를 기반으로 의사 결정을 내리는 데 도움이 되는 활동의 진행 상황과 결과에 대한 정보입니다. 보고서 데이터를 통해 테스트 종료 시점을 결정하고 우승자인 경험 또는 오퍼를 보여주고 다음 작업을 결정하는 데 필요한 인사이트 또는 통찰력을 제공할 수 있습니다. [추가 정보](/help/c-reports/reports.md). |

## 활동 제작 툴

[!DNL Target] 테스트 및 개인화 활동, VEC( [!UICONTROL Visual Experience Composer] ), [!UICONTROL 양식 기반 Experience Composer]및 [!UICONTROL 단일 페이지 애플리케이션(SPA) Visual Experience Composer를 설정하는 세 가지 주요 방법을 제공합니다]. 두 단계 모두 경험 정의, 대상 선택 또는 정의, 활동 결과를 측정할 1차 및 2차 성공 지표 선택 등 3단계의 활동 설정 프로세스를 안내합니다.

| 도구 | 세부 사항 |
| --- | --- |
| VEC(시각적 경험 작성기) | 사이트 컨텍스트에서 개인화된 경험과 오퍼를 손쉽게 제작하고 테스트할 수 있는 WYSIWYG 사용자 인터페이스입니다. You can create experiences and offers for [!DNL Target] activities by dragging and dropping, swapping, and modifying the layout and content of a web page (or offer) or mobile web page. [추가 정보](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md). |
| [!UICONTROL 양식 기반 경험 작성기] | Visual Experience Composer를 사용할 수 없거나 실용적이지 않을 때 A/B 테스트, 경험 타깃팅, Automated Personalization 및 Recommendations 활동에 사용할 수 있는 경험을 만드는 데 유용한 비시각적 경험 및 오퍼 만들기 인터페이스입니다. 예를 들어 양식 기반 작성기를 사용하여 이메일, 키오스크 및 음성 도우미에 게재할 경험과 오퍼를 만들 수 있습니다. [추가 정보](/help/c-experiences/form-experience-composer.md). |
| [!UICONTROL 단일 페이지 애플리케이션(SPA) Visual Experience Composer] | SPA용 VEC를 사용하면 마케터가 지속적인 개발에 의존하지 않고 자체적인 방식으로 SPA에 대한 테스트를 만들고 콘텐츠를 개인화할 수 있습니다. VEC는 React 및 Angular와 같이 인기 있는 프레임워크의 A/B 테스트 및 경험 타깃팅(XT) 활동을 만드는 데 사용할 수 있습니다. [추가 정보](/help/c-experiences/spa-visual-experience-composer.md). |

## 거버넌스 및 제어

적합한 사용자에게 올바른 역할 및 액세스 권한 수준을 제공하기 위해 관리 콘솔 [!DNL Target]이 있습니다. Adobe는 [!UICONTROL Target Premium] 사용자를 위해 [!UICONTROL 엔터프라이즈 권한]을 통해 보다 자세한 거버넌스와 제어를 제공합니다.

| 도구 | 세부 사항 |
| --- | --- |
| [!UICONTROL Enterprise용 Adobe Admin Console] | Adobe Target에 사용자를 추가하고 Adobe Admin Console에서 권한을 할당합니다. [추가 정보](/help/administrating-target/c-user-management/c-user-management/user-management.md). |
| [!UICONTROL 엔터프라이즈]권한<br>(Premium) | A means of formal administering enterprise-wide user access to [!DNL Target]. Add users to [!DNL Target], assign permissions based on their roles, and create workspaces for teams based on different departments, global locations, channel, and other logical groupings. 옵저버, 편집자, 게시자 또는 승인자의 역할을 사용자에게 할당할 수 있습니다. [추가 정보](/help/administrating-target/c-user-management/property-channel/property-channel.md). |

## 통합

[!DNL Target] 다양한 퍼스트 파티, 세컨드 파티 및 타사 시스템과 통합할 수 있습니다. 이러한 통합은 테스트 및 개인화를 위한 대상을 만드는 데 사용할 이러한 시스템에서 사용할 수 있는 방문자 및 고객 데이터에 액세스할 수 있도록 하는 데 유용합니다. 솔루션 및 핵심 서비스 [!DNL Adobe Experience Cloud]와 [!DNL Target] 긴밀하게 [!DNL Experience Cloud] 통합됩니다.

| 통합 | 세부 사항 |
| --- | --- |
| Adobe Experience Cloud | [!DNL Target] 경험을 규모에 맞게 개인화할 수 있는 다른 [!DNL Adobe Experience Cloud] 솔루션에 포함된 기능을 제공합니다. [!DNL Target] Adobe Analytics, [Experience Cloud 대상](/help/c-integrating-target-with-mac/a4t/a4t.md), [Adobe Campaign](/help/c-integrating-target-with-mac/mmp.md), [Adobe Audience Manager](/help/c-integrating-target-with-mac/campaign-and-target.md)[](/help/c-integrating-target-with-mac/audience-manager-target-integration.md) [](/help/c-experiences/c-manage-content/aem-experience-fragments.md) (AAM), Adobe Experience Manager 및(AEM)의 파워와 함께 활용할 수 있습니다. |
| Target API(Premium) | [!UICONTROL Target] 는 Adobe Target을 퍼스트 파티, 세컨드 및 서드 파티 시스템과 통합하는 데 사용할 수 있는 40개 이상의 API를 제공합니다. [추가 정보](/help/api/api-overview.md). |

## 주의 사항

다음 장으로 이동하기 전에 다음 아이디어를 고려하십시오.&quot;테스트 및 개인화 아이디어 개발&quot;

### 최적화를 위한 모범 사례

* **전략**:우리의 목적과 가설은? 정렬되어 있나요? 예를 들어 대출 신청 수를 늘리고 싶었기 때문에 신청서의 필드 수를 줄이면 그렇게 될 것이라고 가정해 보겠습니다.
* **잘 훈련된 방법론** 우리는 적절한 장소에서 테스트를 시작합니까? 예를 들어 트래픽이 충분하고 비즈니스에 중요한 지표에 영향을 주는 위치가 필요합니다.
* **적절한 설정** 우리의 활동이 목적을 달성하기 위해 설정되어 있습니까? 예를 들어 대출 신청 수를 늘리고자 하는 경우 대출 대상자를 타깃팅하여 &quot;제출&quot; 버튼을 클릭해야 합니다.
* **철저한 분석**:테스트 활동이 완료되었습니까? 결과가 어떻게 나오나요? 95%에서 99% 사이의 통계 신뢰도가 달성될 때까지 활동을 실행합니다. 우승 경험이 승리했다고 생각하고 다른 곳에서 학습을 적용하는 이유를 문서화합니다.
* **반복적인 테스트**:우리는 이전의 활동들에 대해 배우고 있는가? 성공 전략을 찾은 경우 성공 지표를 더 개선하기 위해 해당 전략을 개선하거나 해당 오퍼와 함께 작동하는 변경을 수행해 보십시오.

### 의견은 결과에 부정적인 영향을 줄 수 있습니다

* 효과에 부정적인 영향을 줄 수 있는 의견. 가장 높은 급여를 받는 사람의 의견(HIPPO), 태도, 편견입니다. 예를 들어 CEO는 각 페이지에 더 많은 공간을 제공하기 위해 검색 상자의 크기를 줄이려고 합니다. 검색 횟수가 줄어들지 않도록 테스트해야 합니다.
* 당신은 의견에 따라 행동하고 있습니까? 나는 그 시험이 마음에 들지 않는다. 고객은 이 경험을 전혀 좋아하지 않을 것입니다. 직관은 유용하지만 A/B 테스트는 항상 효과적인 것은 아니라는 것을 증명했습니다.
* 또는 최적화 마인드를 가지고 있습니까? 어떤 경험이 이길지 알게 되어 흥분됩니다. 테스트할 수 있는 옵션이 충분합니까?

### 가정은 결과에 부정적인 영향을 줄 수도 있습니다

* 효과에 부정적인 영향을 줄 수 있는 가정 군중심리(이것이 우리의 경쟁자들이 그것을 하는 방법이다). 예를 들어, 모든 경쟁업체는 회전 이미지와 함께 영웅 배너를 사용하므로 우리도 사용해야 합니다.
* 어떤 것이 효과가 있거나 없는 이유를 알고 있다고 가정할 때 테스트하지 않아도 된다고 가정하고 예를 들어, 우리는 항상 가장 높은 가격에서 가장 낮은 가격의 호텔 룸을 기본으로 나열합니다.
* 가설을 가지고 행동하고 있습니까? 우리는 그것을 테스트할 필요가 없고 분석을 확인했습니다. (예, 하지만 분석에서 보여주는 것보다 더 많은 것이 있을 수 있습니다.)
* 또는 최적화 마인드를 가지고 있습니까? 모든 것을 테스트합니다.