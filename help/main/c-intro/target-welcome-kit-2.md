---
keywords: 시작 키트;대상 환영 키트;소개;소개;시작
description: Adobe Target을 자세히 살펴보십시오. 사용 가능한 활동, 채널, 구현, 통합 등에 대해 알아보십시오.
title: Target에 대한 높은 수준의 소개는 어디에서 찾을 수 있습니까?
feature: Overview
exl-id: 19238d4c-b7e1-418d-96e5-c46a3769f7bf
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '2478'
ht-degree: 79%

---

# 2장: Adobe [!DNL Target] 개요

[!DNL Adobe Target] 사용을 시작하기 전에 솔루션에 대한 높은 수준의 개요를 살펴보는 것이 도움이 될 수 있습니다. 이 장에서는 솔루션의 주요 기능, 이를 사용할 수 있는 브랜드 터치포인트, 구현 옵션, 중요한 사용자 인터페이스 기능 및 워크플로, 거버넌스 기능 및 전체 [!DNL Adobe Experience Cloud]에서 차지하는 역할에 대해 알아봅니다. [!DNL Adobe Target Premium] 기능으로 지정되지 않은 경우 이 장에 설명된 항목은 [!DNL Adobe Target Premium] 및 [!DNL Adobe Target Standard] 모두에서 사용할 수 있습니다. 자세한 내용은 [Target 소개](/help/main/c-intro/intro.md)를 참조하십시오.

## 기능 및 활동

테스트 및 개인화는 [!DNL Target]이(가) 제공하고 [!DNL Target]에서 &quot;활동&quot;을 만들 때 사용할 수 있는 두 가지 광범위한 기능입니다. &quot;테스트&quot;라는 용어가 &quot;최적화&quot;와 &quot;개인화&quot;라는 용어와 &quot;타기팅&quot;이라는 용어와 상호 교환하여 사용되는 것을 볼 수 있습니다.

테스트 활동에서 디지털 경험의 한 가지 변형을 하나 이상의 다른 변형과 비교하여 가장 많은 방문자가 원하는 행동을 취하도록 유도하는 변형을 발견합니다. [!DNL Target] 은 A/B 테스트, 다변량 테스트(MVT) 및 자동 할당 같은 테스트 기능을 제공합니다.

개인화 활동을 통해 특정 방문자 그룹 또는 각 개별 방문자에게 맞춤화된 디지털 경험을 제공합니다. [!DNL Target] 은 경험 타기팅, 자동 타겟, 자동 개인화 및 권장 사항 같은 개인화 기능을 제공합니다.

각 기능의 사용 시기 및 방법에 대한 자세한 내용은 [Target 활동 유형](/help/main/c-activities/target-activities-guide.md)을 참조하십시오.

| 활동 유형 | 세부 사항 |
| --- | --- |
| A/B 테스트 | 웹 사이트 또는 기타 디지털 고객 터치포인트의 두 가지 이상의 변형을 비교하여 사전 지정된 테스트 기간 동안 어떤 변형이 주요 비즈니스 조치를 가장 개선하는지 확인합니다. A/B 테스트는 새로운 웹 페이지 레이아웃, 사이트 탐색에 대한 다른 접근 방식 또는 복사, 이미지 및 콜 투 액션 버튼과 같은 디지털 경험의 개별 요소에 대한 대폭적인 다른 처리와 같은 큰 변화에 적합합니다. [자세히 알아보기](/help/main/c-activities/t-test-ab/test-ab.md) |
| 자동 할당 | 둘 이상의 경험에서 최고의 성능을 발휘하는 경험을 식별하고, 테스트가 계속 실행되고 학습하는 동안 전환을 늘리기 위해 더 많은 트래픽을 자동으로 승자에게 재할당합니다. [!DNL Adobe Sensei]으로 구동되는 인공 지능을 사용합니다. [자세히 알아보기](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) |
| 자동 타겟<br>(Premium) | [!DNL Target] 의 Adobe Sensei AI를 활용하여 각 방문자의 개별 고객 프로필과 유사한 프로필을 가진 이전 방문자의 행동을 토대로 여러 방문자의 최상의 경험을 결정하고 전달합니다. 자동 타겟을 사용하면 규모에 맞게 개인화할 수 있습니다. [자세히 알아보기](/help/main/c-activities/auto-target/auto-target-to-optimize.md) |
| Automated Personalization<br>(Premium) | [!DNL Adobe Sensei] 에서 제공하는 고급 머신 러닝 알고리즘과 자동화를 사용하여 오퍼의 다양한 이미지, 복사 및 기타 요소를 검토하고 방문자당 전환 또는 매출 증대와 같은 비즈니스 목표를 가장 잘 달성하는 각 방문자에게 최상의 조합을 제공합니다. [자세히 알아보기](/help/main/c-activities/t-automated-personalization/automated-personalization.md) |
| 경험 타기팅(XT) | 사용자가 정의한 규칙 및 기준 세트를 기준으로 특정 대상자에게 콘텐츠를 전달합니다. **[!UICONTROL Experience Targeting]**&#x200B;은(는) 대상자가 가치 있고 어떤 경험이 그들과 공감하는지 잘 알고 있을 때 특정 경험이나 콘텐츠를 특정 대상자에게 타기팅하는 데 유용합니다. [자세히 알아보기](/help/main/c-activities/t-experience-target/experience-target.md) |
| MVT(다변량 테스트) | 세 가지 다른 배경 이미지, 두 가지 변형 복사본 및 두 가지 다른 버튼 색상과 같이 페이지에 있는 요소의 변형 또는 디지털 경험의 가능한 모든 조합을 비교합니다. MVT는 어떤 조합이 특정 대상자를 위해 가장 잘 수행되고 어떤 요소가 결과에 가장 큰 영향을 미치는지 결정합니다. [자세히 알아보기](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) |
| 추천<br>(Premium) | Adobe Sensei AI를 사용하여 이전 활동과 다른 고객의 활동에 따라 관심 있는 제품 또는 콘텐츠를 자동으로 제안합니다. [자세히 알아보기](/help/main/c-recommendations/recommendations.md) |

## 채널

[!DNL Target] 을 사용하여 웹 사이트, 모바일 사이트 및 모바일 앱과 같은 전통적인 디지털 터치포인트와 키오스크, 이메일, IoT 디바이스, 게임 콘솔, Alexa 및 Cortana 같은 음성 지원 디바이스에서도 디지털 경험을 테스트하고 개인화할 수 있습니다. 많은 기업이 웹 사이트에서 [!DNL Target] 를 사용하기 시작합니다. 하지만, 최근의 연구는 더 많은 사람들이 그들의 모바일 디바이스에서 브랜드를 방문한다는 것을 보여 줍니다. 이제 모바일 채널을 최적화하는 것이 필수적입니다. 방문자의 경험을 모든 터치포인트에 연결하여 원활하고 일관된 경험을 제공하는 것이 이상적입니다.

| 채널 | 세부 사항 |
| --- | --- |
| 웹 사이트 | [!DNL Target] 은 방문자와 고객 참여를 개선하고, 전환을 증가시키며, 매출을 높이기 위해 멀티 페이지, 단일 페이지 애플리케이션(SPA) 및 모바일 웹 사이트에서 A/B 테스트, 다변량 테스트, 경험 타기팅, 자동 할당, 자동 타겟, 자동 개인화 및 권장 사항 작업을 실행하는 데 사용할 수 있습니다. |
| 모바일 웹 | [!DNL Target] 은 모바일 웹 사이트 페이지에서 웹 사이트에서 실행하는 모든 동일한 활동 유형을 실행하여 방문자 및 고객 참여를 비슷하게 개선하고 전환을 향상시키며 매출을 증대하는 데 사용할 수 있습니다. |
| 모바일 앱 | [!DNL Target] 은 사용자 동작 및 모바일 컨텍스트를 기반으로 모바일 앱 환경을 테스트하고 개인화하는 데 사용할 수 있습니다. [!DNL Target] 을 사용하면 반복적인 테스트와 경험 타기팅 및 AI 기반 개인화를 통해 상호 작용하고 전환하는 상호 작용을 제공할 수 있습니다. 모바일 앱에서 [!DNL Target] 을 사용하려면 Adobe Mobile Services SDK를 사용해야 합니다. |
| IoT/Everywhere | [!DNL Target]에서는 브라우저가 없거나 JavaScript 코드를 사용하지 않는 이메일과 터치포인트에서 기존 웹 사이트, 모바일 사이트 및 모바일 앱에서 사용하는 활동과 동일한 테스트 및 개인화 기능을 사용할 수 있도록 서버 측 구현을 제공합니다. 예를 들어 키오스크, 셋톱 박스, 게임 콘솔, 음성 지원 디바이스 및 기타 비전통적인 터치포인트를 테스트하고 개인화할 수 있습니다. |

## 구현

[!DNL Target]을(를) 사용하여 기존 웹 및 모바일 터치포인트를 비롯한 다양한 디지털 터치포인트를 테스트하고 개인화할 수 있지만 브라우저가 없거나 JavaScript 코드를 사용하지 않는 터치포인트를 사용하는 경우도 많습니다. 경우에 따라 내부 또는 외부 정책에 따라 추가적인 제어 및 보안 수준이 필요합니다. 성능 상의 이유로 백엔드 서버에서 실행해야 하는 프로세스도 있을 수 있습니다. 이러한 다양한 용도를 충족하기 위해 [!DNL Target] 을 클라이언트측, 서버측 또는 두 가지 방법의 조합으로 구현할 수 있는 기능을 제공합니다.

| 구현 유형 | 세부 사항 |
| --- | --- |
| 클라이언트측 | [!DNL Target]의 이러한 구현으로 [!DNL Target] 은 활동과 관련된 경험을 클라이언트 브라우저에 직접 전달합니다. 브라우저는 표시할 경험을 결정하고 표시합니다. 클라이언트측 구현에서는 WYSIWYG 편집기, **[!UICONTROL Visual Experience Composer]**(VEC) 또는 비시각적 인터페이스인 **[!UICONTROL Form-based Experience Composer]**&#x200B;을(를) 사용하여 테스트 및 개인화 경험을 만들 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html){target=_blank} |
| 서버측 | 이 유형의 [!DNL Target] 구현에서 클라이언트 디바이스는 서버를 통해 경험에 대한 요청을 하고, 서버는 [!DNL Target]에 요청을 보내고, [!DNL Target] 은 서버에 응답을 되돌려 보내며, 서버는 클라이언트 디바이스에 전달할 경험을 결정합니다. 경험은 음성 도우미를 통해 또는 시각적이지 않은 경험 또는 브라우저를 기반으로 하지 않는 디바이스를 통해 이메일이나 키오스크에 표시될 수 있습니다. 서버가 클라이언트와 [!DNL Target] 사이에 존재하기 때문에 제어력과 보안이 필요하거나 서버에서 실행하려는 복잡한 백엔드 프로세스가 있는 경우에 이러한 유형의 구현이 이상적입니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank} |
| 하이브리드 구현 | 이 구현에서는 주어진 사용 사례에 가장 적합한 구현 접근 방식을 선택합니다. 예를 들어 클라이언트측 구현을 사용하여 홈 페이지의 히어로 배너에서 A/B 제안을 테스트할 수 있지만, 서버측 구현을 사용하여 클라이언트 브라우저에 표시할 내부 검색 결과, 스마트 자동차 대시보드에 표시할 경험 또는 음성 지원에서 전달할 음성 응답을 결정할 수도 있습니다. |

## 활동 요소

[!DNL Target]에서는 개인화 활동, 최적화 활동 또는 개인화 접근 방식을 최적화하는 활동을 만들 수 있습니다. 각 활동에는 테스트하거나 개인화하는 경험 또는 오퍼, 경험을 제공하는 대상자 또는 개인, 활동의 영향을 측정하는 지표 및 그 영향을 시각적으로 표시하는 보고서 등 주요 요소가 있습니다.

| 요소 유형 | 세부 사항 |
| --- | --- |
| 경험 | 구매 단계 또는 다른 논리적 페이지 순서를 구성하는 페이지, 전체 웹 페이지 또는 페이지 세트에 있는 오퍼, 이미지, 텍스트, 버튼, 비디오, 이러한 여러 요소의 조합입니다. 음성 도우미, 고객 서비스 스크립트 또는 음료 자판기의 개인화된 향에 대한 답변일 수도 있습니다. [!DNL Target] 활동에서 경험을 테스트하거나 개인화합니다. [자세히 알아보기](/help/main/c-experiences/experiences.md) |
| 오퍼 | 이미지, 텍스트, HTML, 링크, 비디오, 콜 투 액션 버튼, 음성 도우미 응답 또는 기타 모든 종류의 콘텐츠를 포함할 수 있는 콘텐츠 블록입니다. 할인, 무료 배송 등을 제안할 수 있습니다. 오퍼는 웹 페이지에 표시될 수 있지만 음성 도우미나 게임 콘솔과 같은 고객 터치포인트에서도 경험할 수 있습니다. 오퍼를 테스트할 때 다른 오퍼와 비교하여 성공 여부를 측정합니다. [자세히 알아보기](/help/main/c-experiences/c-manage-content/manage-content.md) |
| 대상자 | 새 방문자, 재방문자 또는 중서부의 재방문자와 같이 동일한 특성을 가진 사람 그룹입니다. 대상자 기능을 사용하면 적절한 시간에 적절한 사람에게 적절한 메시지를 표시하여 웹 마케팅을 최적화하도록 다양한 콘텐츠 및 경험을 특정 대상자에 타기팅할 수 있습니다. 방문자가 타깃 대상자의 일부로 식별되면 [!DNL Target] 은 활동 작성 중에 정의된 기준에 따라 표시할 경험을 결정합니다. [자세히 알아보기](/help/main/c-target/target.md) |
| 성공 지표 | [!DNL Target] 활동에서 주어진 경험 또는 오퍼의 성공 여부를 확인할 수 있는 주요 비즈니스 조치입니다. 예를 들어 새 오퍼가 방문자당 매출을 늘리는지 또는 장바구니에 품목을 추가할지 여부를 결정할 수 있습니다. 성공 지표는 등록, 주문 또는 구매 흐름과 관련된 문제뿐만 아니라 방문자나 고객 참여와 관련된 문제를 발견하는 데에도 유용할 수 있습니다. [자세히 알아보기](/help/main/c-activities/r-success-metrics/success-metrics.md) |
| 보고서 | 데이터를 기반으로 결정을 내리는 데 도움이 되는 활동의 진행 상황과 결과에 대한 정보입니다. 보고서 데이터를 통해 테스트 종료 시점을 결정하고 우승자인 경험 또는 오퍼를 보여 주고 다음 작업을 결정하는 데 필요한 인사이트 또는 통찰력을 제공할 수 있습니다. [자세히 알아보기](/help/main/c-reports/reports.md) |

## 활동 생성 도구

[!DNL Target]은(는) 테스트 및 개인화 활동을 설정하는 세 가지 주요 방법인 VEC([!UICONTROL Visual Experience Composer]), [!UICONTROL Form-based Experience Composer] 및 [!UICONTROL Single Page Application (SPA) Visual Experience Composer]을(를) 제공합니다. 두 가지 모두 경험 정의, 대상자 선택 또는 정의, 활동 결과를 측정할 기본 및 보조 성공 지표 선택 등 3단계로 활동 설정 프로세스를 안내합니다.

| 도구 | 세부 사항 |
| --- | --- |
| [!UICONTROL Visual Experience Composer]&#x200B;(VEC) | 사이트 컨텍스트에서 개인화된 경험과 오퍼를 쉽게 만들고 테스트할 수 있는 WYSIWYG 사용자 인터페이스입니다. 웹 페이지(또는 오퍼) 또는 모바일 웹 페이지의 레이아웃 및 콘텐츠를 드래그 앤 드롭하고, 교체하고, 수정하여 [!DNL Target] 활동에 대한 경험과 오퍼를 만들 수 있습니다. [자세히 알아보기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) |
| [!UICONTROL Form-based Experience Composer] | 시각적 경험 작성기가 사용이 불가능하거나 실용적이지 않을 때 A/B 테스트, 경험 타깃팅, Automated Personalization 및 권장 사항 활동에 사용할 경험을 만드는 데 유용한 시각적이지 않은 경험 및 오퍼 만들기 인터페이스입니다. 예를 들어 양식 기반 작성기를 사용하여 이메일, 키오스크 및 음성 도우미에 게재할 경험과 오퍼를 만들 수 있습니다. [자세히 알아보기](/help/main/c-experiences/form-experience-composer.md) |
| [!UICONTROL Single Page Application (SPA) Visual Experience Composer] | SPA용 VEC를 사용하면 마케터가 지속적인 개발에 의존하지 않고 자체적인 방식으로 SPA에 대한 테스트를 만들고 콘텐츠를 개인화할 수 있습니다. VEC는 React 및 Angular와 같이 인기 있는 프레임워크의 A/B 테스트 및 경험 타기팅(XT) 활동을 만드는 데 사용할 수 있습니다. [자세히 알아보기](/help/main/c-experiences/spa-visual-experience-composer.md) |

## 거버넌스 및 제어

적합한 사용자에게 [!DNL Target]에 대한 올바른 역할과 관련 액세스 및 사용 권한 수준을 제공하기 위해 관리 콘솔이 있습니다. [!UICONTROL Target Premium] 사용자의 경우 보다 자세한 거버넌스 및 제어를 제공합니다.
([!UICONTROL Enterprise Permissions] 포함).

| 도구 | 세부 사항 |
| --- | --- |
| [!UICONTROL Adobe Admin Console for Enterprise] | Adobe Target에 사용자를 추가하고 Adobe Admin Console에서 사용 권한을 할당합니다. [자세히 알아보기](/help/main/administrating-target/c-user-management/c-user-management/user-management.md) |
| [!UICONTROL Enterprise Permission]s<br>(Premium) | [!DNL Target]에 대한 엔터프라이즈급 사용자 액세스를 공식적으로 관리하는 방법입니다. [!DNL Target]에 사용자를 추가하고, 역할에 따라 권한을 할당하고, 서로 다른 부서, 글로벌 위치, 채널 및 기타 논리 그룹을 기반으로 팀을 위한 작업 영역을 만듭니다. 사용자에게 관찰자, 편집자, 게시자 또는 승인자 역할을 할당할 수 있습니다. [자세히 알아보기](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) |

## 통합

[!DNL Target] 은 많은 퍼스트, 세컨드, 서드파티 시스템과 통합할 수 있습니다. 이러한 통합은 테스트 및 개인화를 위한 대상자를 만드는 데 사용할 수 있도록 이러한 시스템에서 이용 가능한 방문자 및 고객 데이터에 대한 액세스를 제공하는 데 유용할 수 있습니다. [!DNL Adobe Experience Cloud]의 일부로서 [!DNL Target] 은 [!DNL Experience Cloud] 솔루션 및 핵심 서비스와 긴밀하게 통합됩니다.

| 통합 | 세부 사항 |
| --- | --- |
| Adobe Experience Cloud | [!DNL Target] 은 다른 [!DNL Adobe Experience Cloud] 솔루션과 함께 임베드된 기능을 통해 규모에 맞게 경험을 개인화할 수 있습니다. . [!DNL Target] 의 강력한 기능을 [Adobe Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md), [Experience Cloud Audiences](/help/main/c-integrating-target-with-mac/mmp.md), [Adobe Campaign](/help/main/c-integrating-target-with-mac/campaign-and-target.md), [Adobe Audience Manager(AAM)](/help/main/c-integrating-target-with-mac/audience-manager-target-integration.md) 및 [Adobe Experience Manager(AEM)](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) 와 함께 활용하십시오. |
| Target API(Premium) | [!UICONTROL Target]은(는) Adobe Target을 퍼스트, 세컨드 및 서드파티 시스템과 통합하는 데 사용할 수 있는 API를 40개 이상 제공합니다. [자세히 알아보기](/help/main/api/api-overview.md) |

## 다음 사항에 주의하십시오.

다음 장: &quot;테스트 및 개인화 아이디어 개발&quot;로 넘어가기 전에 다음 아이디어를 생각해 보십시오.

### 최적화에 대한 모범 사례

* **좋은 전략**: 우리의 목표와 가설은 무엇입니까? 정렬되었습니까? 예를 들어 우리는 대출 신청서 제출을 늘리기를 원하므로, 신청서 양식의 필드 수를 줄이면 그렇게 될 것이라고 가정합니다.
* **절제된 방법론** 올바른 곳에서 테스트를 시작하고 있습니까? 예를 들어 트래픽이 충분하고 비즈니스에 중요한 지표에 영향을 미치는 위치가 필요합니다.
* **적절한 설정** 우리의 활동이 우리의 목적을 달성하도록 설정되었습니까? 예를 들어 대출 신청서 제출을 늘리려면 대출에 관심 있는 사람을 타겟으로 &#39;제출&#39; 버튼 클릭 수를 측정해야 한다.
* **철저한 분석**: 완료될 때까지 테스트 활동이 실행되었습니까? 결과는 어떻습니까? 95%에서 99% 사이의 통계적 신뢰가 달성될 때까지 활동을 실행하십시오. 우수성이 검증된 경험이 이겼다고 생각하는 이유를 기록하고 다른 곳에 배운 내용을 적용하십시오.
* **반복적 테스트**: 이전 활동에 대한 학습을 기반으로 하고 있습니까? 우수성이 검증된 전술을 찾았다면 이를 개선하거나 성공 지표를 더욱 향상시키기 위해 함께 작동하는 변화를 시도하십시오.

### 의견은 결과에 부정적인 영향을 미칠 수 있습니다.

* 효과에 부정적인 영향을 미칠 수있는 의견. 가장 높은 급여를 받는 사람의 의견(HIPPO), 태도, 편견. 예를 들어 CEO는 각 페이지에 더 많은 공간을 만들기 위해 검색 상자의 크기를 줄이려고 합니다. 검색 횟수가 줄어들지 않는지 확인하기 위해 테스트해야 합니다.
* 의견에 따라 행동하고 있습니까? 그 시험 방식이 마음에 들지 않아요. 고객은 이 경험을 전혀 좋아하지 않을 것입니다. 직관이 유용하기는 하지만 A/B 테스트는 항상 정확한 것은 아니라는 것을 여러 번 입증했습니다.
* 아니면 최적화 마인드를 가지고 계십니까? 어떤 경험이 승리할 수 있을지 기대됩니다. 테스트할 옵션이 충분히 있습니까?

### 가정은 또한 결과에 부정적인 영향을 미칠 수 있습니다.

* 효과에 부정적인 영향을 미칠 수있는 가정 군중 심리(이것이 우리의 경쟁자들이 하는 방식입니다). 예를 들어 우리의 모든 경쟁자들은 회전하는 이미지가 있는 영웅 배너를 사용하므로 우리도 사용해야 합니다.
* 무언가가 작동하거나 작동하지 않는 이유를 알고 있다고 가정합니다. 무언가를 테스트할 필요가 없다고 가정합니다. 예를 들어 우리는 항상 기본적으로 호텔 객실을 최고 가격에서 최저 가격 순으로 나열합니다.
* 가정에 따라 행동하고 있습니까? 테스트할 필요가 없습니다. 분석을 확인했습니다. (네, 하지만 분석 결과 드러난 것보다 더 많은 내용이 있을 수 있습니다.)
* 아니면 최적화 마인드를 가지고 계십니까? 우리는 모든 것을 테스트합니다.
