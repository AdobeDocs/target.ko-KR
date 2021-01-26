---
keywords: welcome kit;target welcome kit;intro;introduction;getting started
description: Adobe Target 시작 키트 - 2장 - Target 개요
title: Adobe Target 시작 키트 - 2장 - Target 개요
feature: Overview
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '2504'
ht-degree: 16%

---


# 2장:Adobe Target 개요

[!DNL Adobe Target]을(를) 사용하기 전에 솔루션에 대한 높은 수준의 개요를 얻는 데 도움이 될 수 있습니다. 이 장에서는 솔루션의 주요 기능, 사용할 수 있는 브랜드 접점, 구현 옵션, 중요한 사용자 인터페이스 기능 및 워크플로우, 거버넌스 기능 및 전체 [!DNL Adobe Experience Cloud]에서의 해당 역할에 대해 알아봅니다. [!DNL Adobe Target Premium] 기능으로 표시되지 않는 한 이 장에 설명된 항목은 [!DNL Adobe Target Premium] 및 [!DNL Adobe Target Standard]에서 모두 사용할 수 있습니다. 자세한 내용은 [Target 소개](/help/c-intro/intro.md)를 참조하십시오.

## 기능 및 활동

테스트 및 개인화는 [!DNL Target]이 제공하는 2가지 광범위한 기능과 [!DNL Target]에서 &quot;활동&quot;을 만들 때 사용할 수 있는 기능입니다. &quot;테스트&quot;라는 용어는 &quot;최적화&quot; 및 &quot;개인화&quot;와 함께 &quot;타깃팅&quot;과 혼용적으로 사용되는 경우를 볼 수 있습니다.

테스트 활동에서는 디지털 경험의 한 변형과 하나 이상의 다른 변형을 비교하여 가장 많은 방문자가 원하는 작업을 수행하도록 하는 변형을 발견했습니다. [!DNL Target] 에서는 다음 테스트 기능을 제공합니다.A/B 테스트, MVT(다변량 테스트) 및 자동 할당.

개인화 활동을 통해 특정 방문자 그룹 또는 각 개별 방문자에 맞게 맞춤화된 디지털 경험을 제공할 수 있습니다. [!DNL Target] 다음과 같은 개인화 기능을 제공합니다.경험 타깃팅, 자동 Target, Automated Personalization 및 Recommendations

각 기능의 사용 시기 및 방법에 대한 자세한 내용은 [Target 활동 유형](/help/c-activities/target-activities-guide.md)을 참조하십시오.

| 활동 유형 | 세부 사항 |
| --- | --- |
| A/B 테스트 | 웹 사이트 또는 기타 디지털 고객 접점에서 두 가지 이상의 경험 또는 오퍼의 변형을 비교하여 사전 지정된 테스트 기간 동안 주요 비즈니스 측정이 가장 향상되는 변형을 확인합니다. A/B 테스트는 새로운 웹 페이지 레이아웃, 다양한 사이트 탐색 방법 또는 복사, 이미지 및 클릭유도문안 버튼과 같은 디지털 경험의 개별 요소에 대한 완전히 다른 처리와 같은 큰 변경에 적합합니다. [추가 정보](/help/c-activities/t-test-ab/test-ab.md). |
| 자동 할당 | 두 개 이상의 경험 중에서 가장 성과가 좋은 경험을 식별하고 우승자에게 더 많은 트래픽을 자동으로 다시 할당하여 테스트를 계속 실행하고 학습하면서 전환율을 높일 수 있습니다. [!DNL Adobe Sensei]에서 제공하는 인공 지능을 사용합니다. [추가 정보](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| 자동 Target<br>(Premium) | Adobe Sensei AI를 [!DNL Target]에서 활용하여 개인 고객 프로필과 비슷한 프로파일을 가진 이전 방문자의 행동을 기반으로 각 방문자에게 최상의 경험을 확인하고 전달할 수 있습니다. 자동 Target을 통해 규모에 맞게 개인화할 수 있습니다. [추가 정보](/help/c-activities/auto-target/auto-target-to-optimize.md). |
| Automated Personalization<br>(Premium) | 고급 기계 학습 알고리즘 및 [!DNL Adobe Sensei]에서 제공하는 자동화를 사용하여 오퍼에 있는 다양한 이미지, 복사 및 기타 요소의 조합을 검토하고 방문자당 전환율 증가 또는 매출과 같은 비즈니스 목표를 달성하는 데 가장 적합한 조합을 각 방문자에게 제공할 수 있습니다. [추가 정보](/help/c-activities/t-automated-personalization/automated-personalization.md). |
| 경험 타깃팅(XT) | 사용자 정의 규칙 및 기준을 기반으로 특정 사용자에게 컨텐츠를 전달할 수 있습니다. **[!UICONTROL 경험]** 타게팅은 특정 대상을 특정 대상자로 타깃팅하는 데 있어 대상이 가치 있고 경험이 자신에게 미치는 영향을 잘 알고 있다는 점을 이해하는 경우에 유용합니다. [추가 정보](/help/c-activities/t-experience-target/experience-target.md). |
| MVT(다변량 테스트) | 페이지 또는 디지털 경험에서 요소의 가능한 모든 조합을 비교할 수 있습니다. 예를 들어 서로 다른 3개의 배경 이미지, 2개의 사본 변형 및 2개의 서로 다른 단추 색상이 있습니다. MVT는 특정 대상에 가장 적합한 조합을 결정하고 결과에 가장 큰 영향을 주는 요소를 결정합니다. [추가 정보](/help/c-activities/c-multivariate-testing/multivariate-testing.md). |
| Recommendations<br>(Premium) | Adobe Sensei AI를 사용하여 고객의 이전 활동과 다른 고객의 활동을 기반으로 고객의 흥미를 끌 수 있는 제품 또는 컨텐츠를 자동으로 제안할 수 있습니다. [추가 정보](/help/c-recommendations/recommendations.md). |

## 채널

[!DNL Target]을(를) 사용하여 웹 사이트, 모바일 사이트 및 모바일 앱과 같은 기존 디지털 접점을 비롯하여 키오스크, 이메일, IoT 디바이스, 게임 콘솔, Alexa 및 Cortana와 같은 음성 보조자와 같은 접점을 통해 디지털 경험을 테스트하고 개인화할 수 있습니다. 많은 회사가 웹 사이트에서 [!DNL Target]을(를) 사용하기 시작합니다. 그러나 최근 설문 조사에 따르면 모바일 디바이스에서 브랜드를 방문하는 사람들이 증가하고 있습니다. 이제 모바일 채널을 최적화하는 것이 중요합니다. 가장 좋은 방법은 모든 접점에서 방문자의 경험을 연결하여 매끄럽고 일관된 경험을 제공하는 것입니다.

| 채널 | 세부 사항 |
| --- | --- |
| 웹 사이트 | [!DNL Target] 다중 페이지, 단일 페이지 애플리케이션(SPA) 및 모바일 웹 사이트의 페이지에서 A/B 테스트, Multivariate Testing, 경험 타깃팅, 자동 할당, 자동 Target, Automated Personalization 및 Recommendations 활동을 실행하여 방문자 및 고객 참여를 향상시키고 전환율을 높이며 매출을 높일 수 있습니다. |
| 모바일 웹 | [!DNL Target] 모바일 웹 사이트 페이지에서 웹 사이트에서 실행하는 모든 동일한 활동 유형을 실행하는 데 사용할 수 있으므로 방문자와 고객 참여를 비슷하게 개선하고 전환을 증가시키며 매출을 높일 수 있습니다. |
| 모바일 앱 | [!DNL Target] 사용자 행동과 모바일 컨텍스트에 따라 모바일 앱 경험을 테스트하고 개인화하는 데 사용할 수 있습니다. [!DNL Target] 경험 타깃팅 및 AI 기반의 개인화는 물론 반복적인 테스트를 통해 고객의 참여를 유도하고 전환율을 높일 수 있습니다. 모바일 앱에서 [!DNL Target]을(를) 사용하려면 Adobe Mobile Services SDK를 사용해야 합니다. |
| 어디에서나 IoT/Everywhere | [!DNL Target] 브라우저가 없거나 JavaScript 코드를 사용하지 않는 접점의 이메일 및 모바일 앱에서 기존의 웹 사이트, 모바일 사이트 및 모바일 앱에서 사용하는 활동에 동일한 테스트 및 개인화 기능을 사용할 수 있도록 서버측 구현을 제공합니다. 예를 들어 키오스크, 셋톱 박스, 게임 콘솔, 음성 도우미 및 기타 비전통적인 접점을 테스트 및 개인화할 수 있습니다. |

## 구현

많은 사용자가 [!DNL Target]을(를) 사용하여 기존의 웹 및 모바일 접점을 비롯한 다양한 디지털 접점을 테스트하고 개인화할 수 있지만 브라우저가 없거나 JavaScript 코드를 사용하지 않는 접점도 선택할 수 있습니다. 경우에 따라 내부 또는 외부 정책을 사용하려면 추가 수준의 제어 및 보안이 필요합니다. 성능상의 이유로 백엔드 서버에서 실행해야 하는 프로세스가 있을 수도 있습니다. 이러한 다양한 사용을 충족하기 위해 다음과 같은 다양한 방법으로 [!DNL Target]을(를) 구현할 수 있습니다.클라이언트측, 서버측 또는 두 항목의 조합입니다.

| 구현 유형 | 세부 사항 |
| --- | --- |
| 고객측 | [!DNL Target]이 구현되면 [!DNL Target]은 활동과 연관된 경험을 클라이언트 브라우저에 직접 전달합니다. 브라우저는 표시할 경험을 결정하고 표시합니다. 클라이언트측은 WYSIWYG 편집기, **[!UICONTROL Visual Experience Composer]**(VEC) 또는 비시각적 인터페이스인 **[!UICONTROL 양식 기반 Experience Composer]**&#x200B;을 사용하여 테스트 및 개인화 경험을 만들 수 있습니다. [추가 정보](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). |
| 서버측 | 이러한 유형의 [!DNL Target] 구현에서 클라이언트 장치는 서버를 통해 경험을 요청하고, 사용자의 서버는 [!DNL Target]에 해당 요청을 보내고, [!DNL Target]는 서버에 응답을 보내고, 서버는 클라이언트 장치에 제공할 경험을 렌더링하기 위해 결정합니다. 경험은 음성 도우미를 통해 또는 시각적이지 않은 경험 또는 브라우저를 기반으로 하지 않는 장치를 통해 이메일이나 키오스크에 표시될 수 있습니다. 서버가 클라이언트와 [!DNL Target] 사이에 존재하기 때문에 제어력과 보안이 필요하거나 서버에서 실행하려는 복잡한 백엔드 프로세스가 있는 경우에 이러한 유형의 구현이 이상적입니다. [추가 정보](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| 하이브리드 구현 | 이 구현에서는 주어진 사용 사례에 가장 잘 작동하는 구현 방법을 선택합니다. 예를 들어 클라이언트측 구현을 사용하여 A/B 구현으로 홈 페이지의 메인 배너에서 오퍼를 테스트하고 서버측 구현을 사용하여 클라이언트 브라우저에 표시할 내부 검색 결과, 스마트 자동차 대시보드에 표시할 경험 또는 음성 도우미로부터 전달하는 음성 응답을 결정할 수 있습니다. |

## 활동 요소

[!DNL Target]에서 개인화 활동, 최적화 활동 또는 개인화 접근 방법을 최적화하는 활동을 만들 수 있습니다. 각 활동에는 테스트 또는 개인화하는 경험, 경험을 제공하는 대상 또는 개인, 활동의 영향을 측정하는 지표 및 해당 영향을 시각적으로 표시하는 보고서 등 주요 요소가 있습니다.

| 요소 유형 | 세부 사항 |
| --- | --- |
| 경험 | 구매 단계 또는 다른 논리적 페이지 순서를 구성하는 페이지, 전체 웹 페이지 또는 페이지 세트에 있는 오퍼, 이미지, 텍스트, 단추, 비디오, 이러한 여러 요소의 조합입니다. 음성 도우미, 고객 서비스 스크립트 또는 음료 자판기의 개인화된 향에 대한 답변일 수도 있습니다. [!DNL Target] 활동에서 경험을 테스트하거나 개인화합니다. [추가 정보](/help/c-experiences/experiences.md). |
| 오퍼 | 이미지, 텍스트, HTML, 링크, 비디오, 클릭유도문안, 음성 지원 응답 또는 기타 모든 유형의 컨텐츠를 포함할 수 있는 컨텐츠 블록. 할인, 무료 배송 등의 혜택을 받을 수 있습니다. 오퍼는 웹 페이지에 표시할 수 있지만 음성 지원 또는 게임 콘솔과 같은 모든 고객 접점에서 경험할 수도 있습니다. 오퍼를 테스트할 때 다른 오퍼와 비교하거나 오퍼가 없는 경우 오퍼의 성공을 측정할 수 있습니다. [추가 정보](/help/c-experiences/c-manage-content/manage-content.md). |
| 대상자 | 새 방문자, 재방문자 또는 중서부의 재방문자와 같이 동일한 특성을 가진 사람 그룹입니다. 대상 기능을 사용하면 적절한 시간에 적절한 사람에게 적절한 메시지를 표시하여 웹 마케팅을 최적화하도록 다양한 콘텐츠 및 경험을 특정 대상에 타깃팅할 수 있습니다. 방문자가 타겟 대상의 일부로 식별되는 경우, [!DNL Target]은 활동 생성 중에 정의된 기준을 기반으로 표시할 경험을 결정합니다. [추가 정보](/help/c-target/target.md). |
| 성공 지표 | [!DNL Target] 활동에서 주어진 경험 또는 오퍼의 성공을 결정할 수 있는 주요 비즈니스 측정값입니다. 예를 들어 새 오퍼가 방문자당 매출을 늘리는지 또는 장바구니에 품목을 추가할지 여부를 결정할 수 있습니다. 성공 지표는 등록, 주문 또는 구매 흐름과 관련된 문제뿐만 아니라 방문자나 고객 참여와 관련된 문제를 발견하는 데에도 유용할 수 있습니다. [추가 정보](/help/c-activities/r-success-metrics/success-metrics.md). |
| 보고서 | 데이터를 기반으로 의사 결정을 내리는 데 도움이 되는 활동의 진행 상황과 결과에 대한 정보입니다. 보고서 데이터를 통해 테스트 종료 시점을 결정하고 우승자인 경험 또는 오퍼를 보여주고 다음 작업을 결정하는 데 필요한 인사이트 또는 통찰력을 제공할 수 있습니다. [추가 정보](/help/c-reports/reports.md). |

## 활동 제작 툴

[!DNL Target] 테스트 및 개인화 활동을 설정하는 3가지 주요 방법,  [!UICONTROL VEC] ( [!UICONTROL Visual Experience Composer]),  [!UICONTROL 양식 기반 Experience Composer] 및단일 페이지 애플리케이션(SPA) Visual Experience Composer를 제공합니다. 두 단계 모두 경험 정의, 대상 선택 또는 정의, 활동 결과를 측정할 기본 및 보조 성공 지표 선택 등 3단계로 활동 설정 프로세스를 안내합니다.

| 도구 | 세부 사항 |
| --- | --- |
| VEC(시각적 경험 작성기) | 사이트 컨텍스트에서 개인화된 경험과 오퍼를 쉽게 만들고 테스트할 수 있는 WYSIWYG 사용자 인터페이스입니다. 웹 페이지(또는 오퍼) 또는 모바일 웹 페이지의 레이아웃과 컨텐츠를 드래그 앤 드롭하고 교체하고 수정하여 [!DNL Target] 활동에 대한 경험과 오퍼를 만들 수 있습니다. [추가 정보](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md). |
| [!UICONTROL 양식 기반 경험 작성기] | Visual Experience Composer를 사용할 수 없거나 사용할 수 없을 때 A/B 테스트, 경험 타깃팅, Automated Personalization 및 Recommendations 활동에 사용할 환경을 만드는 데 유용한 비시각적 경험과 오퍼 만들기 인터페이스입니다. 예를 들어 양식 기반 작성기를 사용하여 이메일, 키오스크 및 음성 도우미에 게재할 경험과 오퍼를 만들 수 있습니다. [추가 정보](/help/c-experiences/form-experience-composer.md). |
| [!UICONTROL SPA(단일 페이지 애플리케이션) Visual Experience Composer] | SPA용 VEC를 사용하면 마케터가 지속적인 개발에 의존하지 않고 자체적인 방식으로 SPA에 대한 테스트를 만들고 콘텐츠를 개인화할 수 있습니다. VEC는 React 및 Angular와 같이 인기 있는 프레임워크의 A/B 테스트 및 경험 타깃팅(XT) 활동을 만드는 데 사용할 수 있습니다. [추가 정보](/help/c-experiences/spa-visual-experience-composer.md). |

## 거버넌스 및 제어

올바른 사용자에게 올바른 역할 및 [!DNL Target]에 대한 액세스 및 권한 수준을 제공하기 위해 관리 콘솔이 있습니다. [!UICONTROL Target Premium] 사용자의 경우 보다 자세한 관리 및 제어 기능을 제공합니다.
를 사용할 수 있습니다.

| 도구 | 세부 사항 |
| --- | --- |
| [!UICONTROL Enterprise용 Adobe Admin Console] | Adobe Target에 사용자를 추가하고 Adobe Admin Console에서 권한을 할당합니다. [추가 정보](/help/administrating-target/c-user-management/c-user-management/user-management.md). |
| [!UICONTROL 엔터프라이즈 ]권한<br>(Premium) | [!DNL Target]에 대한 기업 전체 사용자 액세스를 공식적으로 관리하는 방법입니다. 사용자를 [!DNL Target]에 추가하고, 역할에 따라 권한을 할당하고, 여러 부서, 글로벌 위치, 채널 및 기타 논리 그룹을 기반으로 팀을 위한 작업 영역을 만듭니다. 옵저버, 편집자, 게시자 또는 승인자의 역할을 사용자에게 할당할 수 있습니다. [추가 정보](/help/administrating-target/c-user-management/property-channel/property-channel.md). |

## 통합

[!DNL Target] 많은 자사 시스템, 제2자 및 제3자 시스템과 통합할 수 있습니다. These
통합은 테스트 및 개인화를 위한 대상을 만드는 데 사용할 이러한 시스템에서 사용할 수 있는 방문자 및 고객 데이터에 액세스할 수 있도록 하는 데 유용합니다. [!DNL Adobe Experience Cloud]의 일부로, [!DNL Target]은 [!DNL Experience Cloud] 솔루션 및 핵심 서비스와 긴밀하게 통합됩니다.

| 통합 | 세부 사항 |
| --- | --- |
| Adobe Experience Cloud | [!DNL Target] 경험을 규모에 맞게 개인화할 수  [!DNL Adobe Experience Cloud] 있는 다른 솔루션과 기능을 제공합니다. [!DNL Target]의 강력한 기능과 [Adobe Analytics](/help/c-integrating-target-with-mac/a4t/a4t.md), [Experience Cloud 대상](/help/c-integrating-target-with-mac/mmp.md), [Adobe Campaign](/help/c-integrating-target-with-mac/campaign-and-target.md), [Adobe Audience Manager](/help/c-integrating-target-with-mac/audience-manager-target-integration.md)(AAM) 및 [Adobe Experience Manager](/help/c-experiences/c-manage-content/aem-experience-fragments.md)(AEM)을 함께 활용할 수 있습니다. |
| Target API(Premium) | [!UICONTROL Target] 은 Adobe Target을 퍼스트, 세컨드 및 타사 시스템과 통합하는 데 사용할 수 있는 40개 이상의 API를 제공합니다. [추가 정보](/help/api/api-overview.md). |

## 주의 사항

다음 장으로 이동하기 전에 다음 아이디어를 고려하십시오.&quot;테스트 및 개인화 아이디어를 개발하십시오.&quot;

### 최적화를 위한 모범 사례

* **전략**:우리의 목적과 가설은 무엇인가? 정렬되어 있습니까? 예를 들어 대출 신청 제출 수를 늘리려고 합니다. 따라서 신청 양식의 필드 수를 줄이면 그렇게 할 수 있다고 가정해 보겠습니다.
* **엄격한** 방법론우리는 적절한 장소에서 테스트를 시작합니까? 예를 들어 트래픽이 충분하고 중요한 지표에 영향을 주는 위치가 필요합니다.    를 참조하십시오.
* **적절한** 설정목적을 달성하기 위해 활동이 설정되어 있습니까? 예를 들어 대출 신청 제출 수를 늘리고자 하는 경우 대출 대상자를 타깃팅하여 &quot;제출&quot; 버튼을 클릭해야 합니다.
* **철저한 분석**:테스트 활동이 완료되었습니까? 결과가 어떻게 나오나요? 95%에서 99% 사이의 통계적 신뢰도를 얻을 때까지 활동을 실행합니다. 우승 경험이 승리했다고 생각하고 다른 곳에서 학습을 적용하는 이유를 문서화합니다.
* **반복적인 테스트**:우리는 이전 활동의 교훈을 토대로 짓고 있습니까? 성공 전략을 찾은 경우 성공 지표를 더 개선하기 위해 해당 전략을 개선하거나 해당 오퍼에 적용되는 변경 작업을 수행하면 됩니다.

### 의견은 결과에 부정적인 영향을 줄 수 있습니다

* 효과에 부정적인 영향을 줄 수 있는 의견. 가장 높은 봉급 사람의 의견(HIPPO), 태도, 편견들. 예를 들어 CEO는 각 페이지에 더 많은 공간을 제공하기 위해 검색 상자의 크기를 줄이려고 합니다. 검색 횟수가 줄어들지 않도록 테스트해야 합니다.
* 당신은 의견에 따라 행동하고 있습니까? 나는 그 시험이 그렇게 보이는 것이 싫다. 고객은 이 경험을 전혀 좋아하지 않을 것입니다. 직관력은 유용하지만 A/B 테스트는 항상 능가하는 것은 아니라는 것을 증명했습니다.
* 최적화 마인드를 갖고 계십니까? 어떤 경험이 이길지 알게 되어 기쁩니다. 테스트할 수 있는 옵션이 충분합니까?

### 가정은 결과에 부정적인 영향을 줄 수도 있습니다.

* 효과에 부정적인 영향을 줄 수 있는 가정. 군중심리 (이것이 우리의 경쟁자들이 그것을 하는 방법이다). 예를 들어 모든 경쟁사는 회전 이미지가 있는 영웅 배너를 사용하므로 우리도 해야 합니다.
* 어떤 것이 효과가 있는지 또는 효과가 없는 이유를 알고 있다고 가정하고 어떤 것을 테스트할 필요가 없다고 가정할 때 예를 들어, 우리는 항상 가장 높은 가격에서 가장 낮은 가격의 호텔 룸을 기본값으로 나열합니다.
* 가정으로 행동하고 있습니까? 테스트하지 않아도 됩니다. 분석을 확인했습니다. (예. 하지만 분석에서 보여주는 것보다 더 많은 것이 있을 수 있습니다.)
* 최적화 마인드를 갖고 계십니까? 모든 것을 테스트합니다.