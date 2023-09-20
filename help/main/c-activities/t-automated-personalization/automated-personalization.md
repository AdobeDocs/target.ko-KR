---
keywords: 자동화된 개인화;ap;대상;앙상블;랜덤 포레스트;multi-armed bandit;thompson 샘플링;ml;머신 러닝
description: 사용 방법 알아보기 [!UICONTROL Automated Personalization] 의 (AP) 활동 [!DNL Adobe Target] 고급 머신 러닝을 사용하여 각 방문자에게 다양한 오퍼 변형을 일치시킵니다.
title: (이)란? [!UICONTROL Automated Personalization] (AP) 활동
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 44%

---

# [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] 의 (AP) 활동 [!DNL Adobe Target] 오퍼나 메시지를 결합하고 고급 머신 러닝을 사용하여 방문자의 개별 고객 프로필을 기반으로 다양한 오퍼를 각 방문자와 비교하여 콘텐츠를 개인화하고 상승도를 유도합니다.

>[!NOTE]
>
>[!UICONTROL 자동화된 개인화]는 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에서는 사용할 수 없습니다. 이 라이센스에서 제공하는 고급 기능에 대한 자세한 내용은 [Target Premium](/help/main/c-intro/intro.md#premium)을 참조하십시오.

과 비슷하게 [!UICONTROL 자동 타기팅], [!UICONTROL Automated Personalization] 를 사용합니다. [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md)를 기본 개인화 알고리즘으로 사용하여 방문자에게 표시할 최상의 경험을 결정하는 선도적인 데이터 과학 ensemble 방법입니다. [!UICONTROL 자동화된 개인화는 테스트의 검색 단계에서 유용할 수 있습니다. ] 또한 다양한 방문자를 타깃팅할 때 기계 학습을 통해 가장 효과적인 컨텐츠를 확인하는 데도 유용합니다. 시간이 지남에 따라 이 알고리즘은 가장 효과적인 컨텐츠를 예측하는 방법을 학습하며 목표를 달성할 가능성이 가장 높은 컨텐츠를 표시합니다.

방법에 대한 자세한 내용을 보려면 [!UICONTROL Automated Personalization] 다음과 다름: [!UICONTROL 자동 타기팅], 참조 [자동 타기팅](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

마케터는 를 사용하여 컨텐츠를 가리킨 후 클릭한 다음 해당 영역에 대한 추가 컨텐츠 옵션을 시각적으로 만들고 선택할 수 있는 파일을 사이트에서 구현합니다. [!UICONTROL 시각적 경험 작성기] (VEC). 그런 후에 이 알고리즘은 시스템이 방문자에 대해 가지고 있는 모든 행동 데이터를 기준으로 각 방문자에게 전달할 컨텐츠를 자동으로 결정하며 개인화된 경험을 제공합니다. [!UICONTROL 자동화된 개인화]는 방문자 동작의 변경에 맞춰 조정될 수 있으므로 지속적인 상승도 및 개인화를 제공하기 위해 설정된 종료 날짜 없이 실행될 수 있습니다. 이 모드를 &quot;항시적&quot; 모드라고도 합니다. 마케터는 최적화를 통해 확인된 상승도를 실현하기 전에, 표준 A/B 활동의 결과를 구현하기 위한 표준 작업 순서에 해당하는 테스트 실행, 결과 분석, 승자 전달 과정을 진행할 필요가 없습니다.

다음과 같은 용어는 [!UICONTROL 자동화된 개인화]를 논의할 때 유용합니다.

| 용어 | 정의 |
|---|---|
| Multi-armed bandit | 최적화에 대한 multi-armed bandit 접근 방식은 탐색 학습과 해당 학습의 이용 간에 균형을 이룹니다. |
| Random Forest | 선도적인 머신 러닝 방식. 데이터 과학 용어에서 방문자와 방문 속성을 기반으로 많은 의사 결정 트리를 구성하여 작동하는 앙상블 분류 또는 회귀 방법이다. |
| Thompson 샘플링 | Thompson 샘플링의 목표는 해당 경험을 찾는 &quot;비용&quot;을 최소화하면서 전체적(개인화되지 않음)으로 가장 좋은 경험을 결정하는 것입니다. Thompson 샘플링에서는 두 경험 간의 통계적 차이가 없는 경우에도 항상 승자를 선택합니다. 자세한 내용은 [Thompson 샘플링](https://en.wikipedia.org/wiki/Thompson_sampling)을 참조하십시오. |

[!UICONTROL 자동화된 개인화]를 사용할 때는 다음 세부 사항을 고려하십시오.

## 자동화된 개인화는 무작위 포리스트 알고리즘을 사용하여 개인화합니다

Random Forest는 선도적인 머신 러닝 방식입니다. 데이터 과학 용어에서 방문자와 방문 속성을 기반으로 많은 의사 결정 트리를 구성하여 작동하는 앙상블 분류 또는 회귀 방법이다. 다음 범위 내 [!DNL Target], 랜덤 포레스트는 각 특정 방문자에 대해 전환 가능성이 가장 높을 것으로 예상되는 경험(또는 방문당 가장 높은 매출)을 결정하는 데 사용됩니다. 예를 들어, Chrome을 사용하고, 골드 충성도 멤버이고, 화요일에 사용자 사이트에 액세스하는 방문자는 경험 A로 전환할 가능성이 높을 수 있습니다. 뉴욕의 방문자는 경험 B로 전환할 가능성이 높을 수 있습니다. 의 Random Forest에 대한 자세한 내용 [!DNL Target], 참조 [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## 개인화 모델은 각 방문에 대해 최적화됩니다

* 알고리즘에서는 최상의 경험을 제공하기 위해 방문자의 전환 가능성(또는 전환으로 인한 예상 매출)을 예측합니다.
* 기존 세션이 종료되면 해당 방문자가 컨트롤 그룹에 속하지 않는 한 방문자는 새 경험을 사용할 수 있습니다. 방문자가 컨트롤 그룹에 있는 경우 첫 번째 방문에서 보게 되는 경험은 후속 방문에서 보게 되는 것과 동일한 경험입니다.
* 제공된 경험은 시각적 일관성을 유지하기 위해 세션 내에서 변경되지 않습니다.

## 개인화 모델은 방문자 행동 변화에 따라 조정됩니다

* Multi-arm bandit을 사용하면 모델이 항상 작은 부분의 트래픽을 &quot;소비&quot;하여 활동 기간 동안 계속 학습하고 이전에 학습한 트렌드의 과도한 사용을 방지할 수 있습니다.
* 기본 모델은 최신 방문자 행동 데이터를 사용하여 24시간마다 재구축되어 [!DNL Target] 는 항상 변화하는 방문자 환경 설정을 사용합니다.
* 이 알고리즘은 개별 방문자의 성과가 좋은 경험을 파악할 수 없는 경우 개인화된 승자를 계속 찾으면서, 전반적으로 가장 성과가 좋은 경험을 표시하는 방식으로 자동으로 전환됩니다. 최고 성과를 보이는 경험은 [Thompson 샘플링](https://en.wikipedia.org/wiki/Thompson_sampling)을 사용하여 확인되었습니다.

## 이 모델은 계속해서 단일 목표 지표를 최적화합니다

* 이 지표는 전환 기반 또는 매출 기반(좀 더 구체적으로 나타내자면 [!UICONTROL 방문자당 매출])일 수 있습니다.

## [!DNL Target] 방문자에 대한 정보를 자동으로 수집하여 개인화 모델 구축

* [!UICONTROL 자동 타겟] 및 [!UICONTROL 자동화된 개인화]에 사용되는 속성에 대한 자세한 내용은 [자동화된 개인화 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md)을 참조하십시오.

## [!DNL Target] 자동으로 모두 사용 [!DNL Adobe Experience Cloud] 개인화 모델을 구축할 공유 대상자

* 모델에 대상을 추가하기 위해 수행해야 할 특별한 작업은 없습니다. [!DNL Target]에서 [!DNL Experience Cloud Audiences] 사용에 대한 자세한 내용은 [Experience Cloud 대상](/help/main/c-integrating-target-with-mac/mmp.md)을 참조하십시오.

## 마케터는 오프라인 데이터, 성향 점수 또는 기타 사용자 지정 데이터를 업로드하여 개인화 모델을 만들 수 있습니다

CRM 정보 또는 고객 이탈 성향 점수와 같은 오프라인 데이터는 개인화 모델을 구축할 때 매우 유용할 수 있습니다. [!UICONTROL 자동화된 개인화] (AP)와 [!UICONTROL 자동 타겟] 개인화 알고리즘에서 데이터를 입력하는 방법에는 몇 가지가 있습니다.

* [mbox 매개 변수](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}
* [프로필 매개 변수](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}
* [프로필 업데이트를 위한 서버 측 API](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}

[!UICONTROL 자동화된 개인화] 및 [!UICONTROL 자동 타겟] 개인화 알고리즘에서 자동으로 수집 및 사용되는 데이터에 대해서는 [자동화된 개인화 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md)을 참조하십시오.

## 교육 비디오: 활동 유형

다음 비디오에서는 [!DNL Target]에서 사용할 수 있는 활동 유형에 대해 설명합니다. [!UICONTROL 자동화된 개인화는 5시 55분부터 논의됩니다.]

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로 설명

>[!VIDEO](https://video.tv.adobe.com/v/17386)
