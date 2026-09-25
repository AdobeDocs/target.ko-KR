---
keywords: Target Standard;추천;Target Premium;자동 개인화;자동-타겟;자동 타겟;권한;adobe target이란;
description: Adobe [!DNL Target] Standard 및 Adobe [!DNL Target] Premium의 기본 사항에 대해 알아봅니다. [!DNL Target] Premium에는 표준 제품에서 사용할 수 없는 고급 기능이 포함되어 있습니다.
landing-page-description: 고객의 경험을 개인화하여 웹 및 모바일 사이트, 앱, 소셜 미디어 및 기타 디지털 채널에서 매출을 극대화할 수 있습니다.
short-description: 고객의 경험을 개인화하여 웹 및 모바일 사이트, 앱, 소셜 미디어 및 기타 디지털 채널에서 매출을 극대화할 수 있습니다.
title: Target은 무슨 프로그램입니까?
feature: Overview
exl-id: 0e729c71-618b-4ab8-93a3-d37e73ec2740
TQID: https://experienceleague.adobe.com/Mr8fwY1FNfJShSezC50YX1QeBagmuovUySsQUO8jPqo
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
source-git-commit: 2cecb1f8ae52fd6c47e543710bb14e00503c06ef
workflow-type: tm+mt
source-wordcount: '1644'
ht-degree: 70%
---
# [!DNL Target] 소개


>[!CONTEXTUALHELP]
>id="target_sample_size_ab_daily_traffic"
>title="일별 트래픽"
>abstract="매일 얼마나 많은 사용자가 실험으로 입장하는지입니다. 일별 트래픽을 모르는 경우 위의 \&quot;트래픽 볼륨\&quot;을 선택하면 계산기가 다른 입력 값을 사용하여 일별 트래픽을 계산합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_setup"
>title="테스트 설정"
>abstract="이 필드는 A/B 테스트, 예상 결과, 결과에 필요한 신뢰 수준을 정의합니다. 위에서 선택한 항목과 연결된 필드는 자동으로 계산됩니다. 나머지 필드는 예상 값으로 채우십시오."

>[!CONTEXTUALHELP]
>id="target_sample_size_number_experiences"
>title="경험 수"
>abstract="통제를 포함하여, 실험의 변형 수입니다. A/B 테스트에는 2개의 군이 있습니다. 변형 5개에 통제군 1개를 더하면 6개가 됩니다. 실험군이 늘어날수록 통계적 검정력을 유지하기 위해 비례적으로 더 많은 트래픽이 필요합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_duration"
>title="A/B 테스트 기간"
>abstract="실험이 실행될 기간(일)입니다. 기간이 길수록 실험에서 데이터를 수집하는 시간이 더 많아지므로 더 작은 효과를 안정적으로 감지할 수 있습니다. 기간이 짧을수록 신뢰할 수 있는 결과에 도달하기 위해 더 큰 효과나 더 많은 일별 트래픽이 필요합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_minimum_detectable_effect"
>title="최소 감지 효과"
>abstract="감지가 필요한 가장 작은 개선 단위로, 조치하고자 하는 지표의 최소 변화 단위입니다. 백분율 포인트 단위의 상승폭을 나타내며 기준선 대비 백분율 변화를 의미하지 않습니다. 예를 들어 기준선이 5%이고 1% 포인트 상승폭이 중요한 경우 1을 입력합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_expected_improvement"
>title="예상되는 개선도"
>abstract="실험을 통해 달성할 수 있을 것으로 예상하는 개선도입니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_variance"
>title="분산"
>abstract="지표 값의 분산 정도를 나타내며 지표의 평균값을 의미하지 않습니다. 클릭률(대개 0초 및 1초)과 같은 지표는 분산이 낮지만, 사용자당 매출(소수의 고액 지출자와 다수의 저액 지출자)과 같은 지표는 분산이 훨씬 더 높을 수 있습니다. 확실하지 않은 경우 기본값인 1을 그대로 두십시오."

>[!CONTEXTUALHELP]
>id="target_sample_size_confidence_level"
>title="신뢰 수준"
>abstract="특정 결과가 단순히 우연히 발생한 것이 아니라 실제로 도출된 결과라고 확신하는 데 필요한 신뢰 수준을 나타내며 통계적 유의성의 임계값을 의미합니다. 95% 신뢰 수준은 긍정 오류(false positive)가 발생할 가능성이 최대 5%임을 의미합니다. 값이 높을수록 긍정 오류(false positive)는 감소하지만 더 많은 데이터가 필요합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_statistical_power"
>title="통계적 검증력"
>abstract="효과가 실제로 존재할 경우 이를 감지할 확률로, 실험의 민감도를 의미합니다. 80% 검정력은 실제 효과를 감지할 확률이 80%임을 의미합니다. 검정력이 높을수록 부정 오류(false negative)는 감소하지만 더 많은 트래픽 또는 더 긴 실행 시간이 필요합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_traffic_mode"
>title="트래픽 모드"
>abstract="사용자가 실험에 입장하는 방식입니다. 연속: 사용자가 실험 기간 동안 매일 입장합니다. 결과가 도출될 때 더 나은 성과를 내는 변형으로 트래픽이 자동으로 이동합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_metric_type"
>title="지표 유형"
>abstract="측정 중인 지표 유형입니다. 백분율: 각 사용자가 특정 작업을 수행하거나 수행하지 않는, 클릭이나 전환과 같은 이진 결과에 사용합니다. 숫자: 사용자마다 값이 크게 다를 수 있는, 매출이나 페이지 조회수와 같은 지표에 사용합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_auto_daily_traffic"
>title="일별 트래픽"
>abstract="매일 얼마나 많은 사용자가 실험으로 입장하는지입니다. 여러 날에 걸쳐 실행되는 연속 실험에 사용되며 결과가 도출될 때 더 나은 성과를 내는 변형으로 트래픽이 자동으로 이동합니다."

>[!CONTEXTUALHELP]
>id="target_sample_size_baseline_metric_rate"
>title="기준선 지표 비율"
>abstract="실험이 시작되기 전의 현재 성과를 나타내며 통제군의 평균값을 의미합니다. 항상 필요합니다. 백분율 지표의 경우 백분율로 입력하십시오. 방문자의 5%가 &#39;지금 구매&#39;를 클릭하는 경우 5를 입력합니다. 수 지표의 경우 원시 십진 값을 입력하십시오."

>[!CONTEXTUALHELP]
>id="target_ai_insights_primary_metric"
>title="기본 지표"
>abstract="기본 지표는 보고 설정에서 자동으로 가져옵니다. 변경하려면 목표 및 설정에서 목표 지표를 수정하십시오."

>[!CONTEXTUALHELP]
>id="target_ai_insights_hypothesis"
>title="가설"
>abstract="가설은 실험의 예상 결과를 설명하기 위해 정의하는 진술입니다. 어떤 대상이 어디에서 변경되는지 설명한 후 어떤 지표가 어떻게 변경될 것으로 예상하는지 명시하십시오."

>[!CONTEXTUALHELP]
>id="target_ai_insights_insights"
>title="통찰력"
>abstract="실험 인사이트는 실험 데이터가 통계적 유의성을 충족했을 때 AI가 발견한 학습 내용입니다."

>[!CONTEXTUALHELP]
>id="target_ai_insights_opportunities"
>title="기회"
>abstract="실험 기회는 AI가 실험 스크린샷과 결과에서 발견한 패턴을 기반으로 제안한 처리 아이디어입니다."

>[!CONTEXTUALHELP]
>id="target_ai_insights_treatment_details"
>title="처리 세부 정보"
>abstract="처리 세부 정보는 사용자가 처리 자격을 얻을 때 처리가 어떤 모습인지 보여 주는 이미지를 제공합니다. 모든 실험에 대해 해당 이미지를 검토할 수 있습니다. 일부 실험에서는 이미지를 확인하거나 필요한 경우 교체하도록 요청할 수 있습니다."

[!DNL Adobe Experience Cloud]의 일부인 [!DNL Adobe Target]은(는) 웹, 모바일 사이트, 앱, 소셜 미디어 및 기타 디지털 채널에서 고객 경험을 개인화할 수 있는 포괄적인 도구를 제공합니다.

[!DNL Target]은(는) 매출을 극대화하는 데 도움이 되며 [!DNL Target Standard] 또는 [!DNL Target Premium]&#x200B;(으)로 라이선스가 부여될 수 있습니다.

## [!UICONTROL Target Standard] {#section_ACD5EFF17AAB4E979CBEFA0145CCD905}

[!DNL Target Standard]은(는) A/B 테스트 및 규칙 기반 타깃팅 활동을 시각적으로 만들고 관리할 수 있도록 하는 [!DNL Adobe Target]의 프런트 엔드입니다. [!DNL Target]은(는) [[!UICONTROL VEC(시각적 경험 작성기]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md)) 워크플로 내외부에서 사용자 지정 코드 삽입을 지원합니다. [!DNL Target Standard]은(는) 사이트와 [!DNL Target] 간의 모든 통신을 관리하는 각 페이지의 단일 코드 행으로 디지털 속성에 대한 간단한 구현 전략을 제공합니다.

업계 모범 사례는 [!DNL Target Standard]에 통합되어 있어 새로운 사용자와 숙련된 사용자 모두에게 적합합니다. [!DNL Adobe Experience Cloud]을(를) 사용하여 데이터, 결과를 쉽게 공유하고 팀 구성원과 공동 작업할 수 있습니다.

## [!DNL Target Premium] {#premium}

[!BADGE Premium]{type=Positive}

[!DNL Target Premium]은(는) [!DNL Target Standard]에 프리미엄 기능을 추가하려면 라이선스가 필요한 고급 서비스입니다. [!DNL Target] 가이드의 모든 [!DNL Target Premium]개 문서에는 각 페이지 상단의 [!UICONTROL Premium] 배지 또는 영향을 받는 텍스트 근처의 인라인이 포함됩니다. [!UICONTROL Premium] 배지를 클릭할 수 있으며 이 섹션에 대한 링크입니다.

**[!DNL Target Premium]에 포함된 기능:**

### [!UICONTROL 자동화된 개인화]

[[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)(AP)은 고급 기계 학습 알고리즘을 사용하여 개인화된 경험을 제공하고 디지털 상호 작용에 대한 전환율을 향상시킵니다.

AP는 방문자 활동을 기록하여 유사한 방문자에게 콘텐츠를 타깃팅하기 위한 프로필을 빌드합니다. AP는 정교한 모델링을 사용하여 개별 및 모집단의 콘텐츠에 대한 응답을 추적하여 알려진 모든 사항을 기반으로 각 방문자를 자동으로 타깃팅합니다.

AP는 사람의 분석을 최소화하면서 완전히 자동화되고 지속적으로 학습됩니다. 방문자가 관심을 가질 만한 제품, 방문자 프로필의 정보 수집 및 저장을 결정하는 모델을 구축합니다. 여러 알고리즘을 통해 시스템에 가장 적합한 모델을 만들 수 있습니다.

### [!UICONTROL 자동 타깃팅]

[자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md)은(는) 고급 기계 학습을 사용하여 성과가 좋은 마케터가 정의한 경험을 식별합니다. 그런 다음 개별 고객 프로필과 유사한 프로필을 가진 이전 방문자의 행동을 기반으로 각 방문자에게 가장 적합한 경험을 제공합니다. [!UICONTROL 자동 타겟]은(는) 콘텐츠를 개인화하고 전환하는 데 도움이 됩니다.

### 권장 사항

[권장 사항](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) 활동은 이전 사용자 활동을 기반으로 고객의 흥미를 끌 수 있는 제품이나 콘텐츠를 자동으로 표시합니다. [!UICONTROL 권장 사항]은 고객이 모를 수 있는 관련 항목을 고객에게 표시하는 데 도움이 됩니다.

권장 사항은 사이트에서의 고객의 활동에 따라 고객에게 제품을 제안하는 방법을 결정합니다. 예:

* 배낭을 구입하는 사람이 하이킹 신발과 등산용 스틱까지 구입하도록 유도합니다.

  &quot;이 항목을 구입하고 다른 항목도 구입한 사람&quot; 알고리즘을 사용하여 종종 함께 구입하는 항목을 보여 주는 권장 사항을 생성합니다.

* 현재 시청 중인 내용과 유사한 비디오 콘텐츠를 추천하여 방문자가 여러분의 미디어 사이트에서 보내는 시간을 늘립니다.

  &quot;이 항목을 보고 다른 항목도 본 사람&quot; 기준을 사용하여 다른 비디오를 제안하는 권장 사항을 생성합니다.

* 또한 은행의 저축 제도에 대한 정보를 본 고객이 IRA 계좌에 대해서도 읽도록 제안합니다.

  &quot;이 항목을 보고 다른 항목도 구입한 사람&quot; 기준을 사용하여, 권장 사항에 있는 첫 번째 제품을 표시하지 않고 고객이 한 제품을 본 후에 구입한 다른 제품을 표시합니다.

### 오퍼로서의 추천

[오퍼로서의 Recommendations](/help/main/c-recommendations/recommendations-as-an-offer.md)를 사용하면 [!UICONTROL A/B 테스트], [!UICONTROL 자동 할당], [!UICONTROL 자동 타겟] 및 [!UICONTROL 경험 타깃팅]&#x200B;(XT) 활동 내에 권장 사항을 포함할 수 있습니다.

이 기능은 다음과 같이 완전히 새로운 기능을 사용할 수 있도록 해 줍니다.

* 동일한 활동에서 권장 사항 및 비권장 사항 콘텐츠를 테스트하고 타기팅할 수 있습니다.
* 권장 사항들의 순서를 포함하여 페이지에서의 권장 사항 배치를 쉽게 실험할 수 있습니다.
* [!UICONTROL 자동 할당]을 사용하여 트래픽을 가장 성과가 가장 좋은 권장 사항 경험에 자동으로 푸시합니다.
* [!UICONTROL 자동 타겟]을(를) 사용하여 방문자를 개별 프로필에 따라 맞춤 권장 사항 경험에 동적으로 지정할 수 있습니다.

### Enterprise 사용자 권한

[Enterprise 사용자 권한](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#concept_E396B16FA2024ADBA27BC056138F9838) 기능을 사용하면 [!DNL Adobe Admin Console for Enterprise]의 &quot;제품 프로필&quot;이라는 다른 프로젝트를 생성할 수 있습니다. [!UICONTROL Enterprise 사용자 권한]을(를) 사용하면 각 프로젝트에 대해 해당 사용자의 액세스 권한을 지정하는 단일 사용자에 대해 서로 다른 권한을 할당할 수 있습니다. 이렇게 서로 구별되는 프로젝트들은 [!DNL Adobe Analytics]에서 보고서 세트가 작동하는 방식에 비유할 수 있습니다. 각 프로젝트는 속성 세트에 적용되는 특정 역할이 있는 특정 사용자를 가질 수 있습니다. 그 결과 고객은 사용자에 대한 보기, 편집, 승인 및 게시 액세스를 제한할 수 있습니다. 지역, 환경(개발/단계/프로덕션), 채널 또는 기타 맞춤형 기준에 따라 사용자를 제한할 수 있습니다.

## Beta 기능 {#beta}

[!BADGE Beta]{type=Informative}

[!DNL Adobe Target] 팀은 테스트 및 피드백 목적으로 일부 고객을 위해 새로운 기능을 사용하는 경우가 많습니다. 테스트 기간이 완료되면 향후 [!DNL Target Standard/Premium] 릴리스의 모든 고객에 대해 이러한 기능이 활성화되어 릴리스 정보에 발표됩니다.

Beta 기능을 설명하는 [!DNL Target] 가이드의 문서에는 각 페이지 상단에 있는 Beta 배지 또는 영향을 받는 텍스트 근처에 있는 인라인이 포함됩니다. Beta 배지는 클릭할 수 있으며 이 섹션에 대한 링크를 포함합니다.

## 추천 Classic {#section_9554068100054D2DBDB298CBE5A0E413}

>[!IMPORTANT]
>
>[!DNL Recommendations Classic] 은 레거시 제품이며 더 이상 신규 고객에게 라이선스가 부여되지 않습니다. 최상의 [!DNL Recommendations] 경험을 위해 위에서 설명한 [!DNL Adobe Target Premium]에서 사용할 수 있는 [!DNL Recommendations] 활동으로 업그레이드하십시오.

[!DNL Recommendations Classic] 은 웹 사이트에서의 이전 사용자 활동을 기반으로 고객의 흥미를 끌 수 있는 제품 또는 콘텐츠를 자동으로 표시할 수 있습니다. 권장 사항을 사용하면 고객에게 모르는 제품을 안내하여 웹 사이트에서의 판매량을 늘릴 수 있습니다.

자세한 내용은 [권장 사항 Classic 설명서](/help/main/assets/adobe-recommendations-classic.pdf)를 참조하십시오.

## Experience League: Adobe [!DNL Target] 시작 키트 {#kit}

이 시작 키트를 사용하여 [!DNL Adobe Target] 에서 최적화 및 개인화 프로그램을 구축하십시오. 시작 키트에는 첫 번째 [!DNL Target] 활동을 준비하고 시작하는 데 도움이 되는 주요 정보, 도구 및 리소스가 포함되어 있습니다. 이 키트에는 단기적인 빠른 승리와 장기적인 최적화 전략에 대한 아이디어가 포함되어 있습니다.

[Adobe Target 시작 키트](/help/main/c-intro/target-welcome-kit.md)

## 교육 비디오: 활동 유형(9:03) ![개요 배지](/help/main/assets/overview.png)

다음 비디오에서는 [!DNL Target Standard/Premium] 에서 사용할 수 있는 활동 유형과 어떻게 [!DNL Target] 의 3단계 안내가 있는 워크플로가 여러분이 사이트 목표를 달성하는 데 도움이 될 수 있는지에 대해 설명합니다

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로 설명

>[!VIDEO](https://video.tv.adobe.com/v/30520?captions=kor)


