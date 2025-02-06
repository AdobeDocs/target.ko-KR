---
keywords: 타깃팅;AP 보고서;자동화된 개인화 보고서;자동 타겟;auto target;자동 타겟 보고서;auto target 보고서;개인화;통찰력;자동화된 세그먼트;faq;자주 묻는 질문
description: 자동화된 세그먼트 보고서를 보고 Adobe [!DNL Target] 개인화 모델로 정의되는 서로 다른 세그먼트가 활동의 오퍼/경험에 어떻게 반응하는지 알아봅니다.
title: 자동화된 세그먼트 보고서란 무엇입니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Reports
exl-id: d21517b7-770b-4618-9899-7ac4948c2a8b
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '2066'
ht-degree: 59%

---

# [!UICONTROL Automated Segments] 보고서

[!UICONTROL Automated Personalization](AP) 및 [!UICONTROL Auto-Target](AT) 활동의 사용자가 사용할 수 있는 두 개의 전문 보고서 중 하나인 [!UICONTROL Automated Segments] 보고서에 대한 정보입니다.

>[!NOTE]
>
>[!UICONTROL Personalization Insights] 보고서를 사용할 때는 다음 사항을 고려하십시오.
>
>* AP 및 AT 활동은 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에는 포함되지 않습니다.
>
>* [!UICONTROL Personalization Insights] 보고서는 전환 최적화 목표를 사용하는 AP 및 AT 활동에만 사용할 수 있습니다. 활동이 이미 활성화된 후에 수익에서 전환하도록 최적화 목표가 변경된 활동도 지원되지 않습니다.
>
>* [!UICONTROL Personalization Insights] 보고서는 [!UICONTROL Report Metric] 드롭다운 목록에서 [!UICONTROL Primary Goal]을(를) 선택한 경우에만 사용할 수 있습니다.
>
>* [!UICONTROL Personalization Insights] 보고서는 [기본 환경](/help/main/administrating-target/hosts.md)에서만 지원됩니다.
>
>* [!UICONTROL Personalization Insights] 보고서는 [!UICONTROL Live] 상태이고 적어도 15일 동안 활성화되어 트래픽을 받는 활동에 대해서만 생성됩니다.

다른 방문자가 AP/AT 활동의 오퍼/경험에 다르게 응답합니다. 이 보고서는 Target의 개인화 모델에 정의된 다른 자동화된 세그먼트가 활동의 오퍼/경험에 응답하는 방식을 보여 줍니다.

## 자동화된 세그먼트 보고서 액세스 {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. **[!UICONTROL Activities]**&#x200B;을(를) 클릭한 다음 목록에서 원하는 [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) 또는 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md) 활동을 클릭합니다.

   많은 활동이 있는 경우 필터( ![필터 아이콘](/help/main/assets/icons/Filter.svg) ) 아이콘을 클릭하여 [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] 및 [!UICONTROL Activity Source] 드롭다운 목록에서 옵션을 선택하여 목록을 필터링합니다.

1. **[!UICONTROL Reports]** 아이콘을 클릭합니다.

   활동의 성능에 대한 정보를 제공하는 [Automated Personalization 요약](/help/main/c-reports/personalization-reports/reports-ap.md) 또는 [자동 타겟 요약](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) 보고서가 첫 번째 화면 아이콘으로 표시됩니다. 두 개의 추가 아이콘은 두 개의 [!UICONTROL Personalization Insights] 보고서를 나타냅니다. **[!UICONTROL Automated Segments]**(![자동화된 세그먼트 보고서](/help/main/assets/icons/AutomatedSegment.svg)) 및 **[!UICONTROL Important Attributes]**(![중요 특성 아이콘](/help/main/assets/icons/ViewList.svg)). 자동 타깃팅에는 [!UICONTROL Summary] 보고서의 그래픽 보기를 위한 추가 그래프 아이콘이 있습니다.

   >[!IMPORTANT]
   >
   >[!UICONTROL Automated Segments] 보고서는 활동을 활성화한 후 적어도 15일 이후에나 사용할 수 있습니다. 이 초기 기간 동안에는 이 보고서에 액세스하거나 [!UICONTROL Automated Segments] 아이콘을 클릭할 수 없습니다. 15일 이후에는 활동에 개인화된 트래픽이 충분하다고 가정하여 [!UICONTROL Automated Segments] 보고서를 사용할 수 있습니다.

1. 활동을 활성화한 후 15일이 지나면 **[!UICONTROL Automated Segments]** 아이콘을 클릭합니다.

1. 원하는 날짜 범위를 선택합니다.

   [!UICONTROL Summary] 보고서(성과 보고)와 달리 [!UICONTROL Automated Segments]을(를) 포함한 [!UICONTROL Personalization Insights]은(는) 고정 날짜 범위인 15일, 30일, 60일에 대해서만 사용할 수 있습니다. 이러한 고정 날짜 범위를 사용하면 [!UICONTROL Personalization Insights]에서 충분히 큰 데이터 범위를 사용하여 활동의 단기 패턴에서 통찰력을 얻을 가능성을 줄일 수 있습니다. 날짜 범위에 대해 가능한 두 가지 의사 결정은 &quot;종료 날짜&quot; 및 &quot;지속 시간&quot;입니다. &quot;시작&quot;이 회색으로 표시됩니다. 시작 날짜는 선택한 종료 날짜 및 지속 시간에 따라 자동으로 변경됩니다.

   [!UICONTROL Preset Date Range] 드롭다운 목록에서 사용 가능한 고정 날짜 범위에 액세스할 수 있습니다.

1. [!UICONTROL Automated Segments] 보고서 데이터를 검토하십시오.

1. (선택 사항) Excel 및 기타 도구에서 분석할 수 있도록 **[!UICONTROL Download]** ( ![다운로드 아이콘](/help/main/assets/icons/Download.svg) ) 아이콘을 클릭하여 [CSV 형식으로 보고서 다운로드](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF)합니다.

   >[!NOTE]
   >
   >개인화 통찰력 UI 보고서에는 선택 정보가 들어 있습니다. 자동화된 세그먼트의 CSV 다운로드에는 추가 세부 사항이 포함되어 있습니다. 자동화된 세그먼트 보고서 다운로드에는 UI에 포함된 최상위 세그먼트 외에 그러한 세그먼트가 오퍼 또는 경험에 대해 수행된 방식과 함께 추가 자동화 세그먼트가 포함되어 있습니다.

## 자동화된 세그먼트 보고서 해석

다음 표에는 보고서를 해석하고 해당 요소를 설명하는 방법이 나와 있습니다.

| 요소 | 세부 사항 |
|--- |--- |
| 왼쪽 패널 | 왼쪽 패널에는 이 활동에 대해 Target의 개인화 모델에서 식별한 20개의 가장 큰 &quot;자동화된 세그먼트&quot;가 나열됩니다. &quot;자동화된 세그먼트&quot;는 대상과 비슷하지만, 마케터가 아닌 Target의 개인화 모델로 정의됩니다. 자동화된 각 세그먼트는 특정 속성의 특정 값(또는 값 범위)으로 구성됩니다.<br>자동화된 세그먼트가 겹칠 수 있습니다. 자동화된 세그먼트는 1개, 2개, 3개 또는 4개의 속성으로 정의할 수 있습니다. 자세한 내용은 아래 예제를 참조하십시오.<br>Target의 개인화 모델에 대해 알려면 [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md)을 참조하십시오. Target의 개인화 모델에서 자동화된 세그먼트를 만드는 데 사용하는 속성에 대해 알려면 [Target의 개인화 알고리즘에 대한 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md)을 참조하십시오. |
| 가운데 그래프 | 가운데 그래프는 강조 표시된 자동화된 세그먼트에 대해 활동 콘텐츠가 수행된 방식을 표시합니다. 왼쪽 패널에서 다른 세그먼트를 클릭하면 가운데 그래프가 업데이트됩니다. |
| 파이 차트 | 가운데 패널의 맨 위에 있는 파이 차트는 자동화된 세그먼트의 크기뿐만 아니라, 활동에서 총 개인화 방문 횟수(예: 개인화 모델에서 제공한 이 활동에 대한 트래픽. 전체 승자 모델에서 제공한 제어 트래픽이나 트래픽은 포함되지 않음)를 보여 줍니다. 세그먼트 크기는 개인화된 방문 횟수만을 기반으로 합니다.<br>![원형 차트](/help/main/c-reports/assets/pie.png) |
| 이중 축 막대 차트 | 이중 축 막대 차트에는 자동화 특정 세그먼트에 대한 오퍼 또는 경험에 따른 방문 및 변환 정보가 포함되어 있습니다. |
| 분홍색 막대 | 분홍색 막대는 전환율을 나타내고, 그래프의 맨 아래 축을 사용합니다. 막대를 마우스로 가리키면 자세한 정보를 볼 수 있습니다. |
| 파란색 막대 | 파란색 막대는 방문 횟수를 나타내며, 그래프의 맨 위 축을 사용합니다. 막대를 마우스로 가리키면 자세한 정보를 볼 수 있습니다. |
| 회색 점선 | 회색 점선은 모든 오퍼/경험 및 자동화된 세그먼트의 활동에서 모든 개인화 방문 횟수에 대한 전환율을 나타냅니다. |

**자동화된 세그먼트 예제 1**

이 자동화 세그먼트는 한 개의 속성만 기반으로 하여 정의됩니다. 자동화된 세그먼트에 포함된 방문자가 일반적인 작업 시간이나 주말 이외의 평일에 이 AP 활동을 확인했습니다.

![자동화된 세그먼트 보고서 예제 1](/help/main/c-reports/assets/automated_segment_example_1.png)

**자동화된 세그먼트 예제 2**

이 자동화 세그먼트는 두 개의 속성을 기반으로 정의됩니다. 이 AP 활동을 본 이 자동화된 세그먼트에 포함된 방문자는 현재 방문 페이지 보기가 3개 미만이었으며, 위도 42.57과 47.29 내에 있는 위치를 기반으로 하여(대략 미국의 뉴햄프셔/오리건과 워싱턴/메인 사이에 기반을 둔 회사) 지리적으로 배치되었습니다.

![자동화된 세그먼트 보고서 예 2](/help/main/c-reports/assets/automated_segment_example_2.png)

## 자동화된 세그먼트 FAQ {#section_740910A52FA646B4AC9452F98C2F5719}

**개인화 인사이트 보고서를 아직 내 활동에 아직 사용할 수 없습니다. 이유가 무엇입니까?**

활동에 대해 [!UICONTROL Personalization Insights] 보고서를 아직 사용할 수 없는 이유는 여러 가지가 있습니다.

* 활동을 활성화한 후 15일이 지나지 않았습니다. 자동화된 세그먼트 및 중요 속성 보고서는 활동을 활성화한 후 적어도 15일 이후에나 사용할 수 있습니다. 이 초기 기간에는 보고서에 액세스하거나 자동화된 세그먼트 및 중요 속성 아이콘을 클릭할 수 없습니다.
* 사용자의 활동에 지정된 기간에 충분한 트래픽이 없습니다. 15일 이후에는 활동에 개인화 모델을 구축할 개인화된 트래픽이 충분하다고 가정하여 자동화된 세그먼트 및 중요 속성 보고서를 사용할 수 있습니다.
* 활동에는 수입 최적화 목표가 있습니다. 현재 [!UICONTROL Personalization Insights]은(는) 전환 최적화 목표 활동에만 사용할 수 있습니다. Adobe은 향후 릴리스에서 수익 최적화 목표 활동에 대한 지원을 추가할 예정입니다.

**속성이란 무엇입니까?**

속성은 트래픽을 개인화하는 방법을 학습하기 위해 개인화 알고리즘에 사용된 방문자 또는 방문자의 특정 방문에 대한 정보입니다. 예를 들어, 브라우저 유형, 위치, 방문 요일 등이 속성이 될 수 있습니다.

개인화 모델에서 [!DNL Target]이 사용하는 속성에 대한 자세한 내용은 [Target의 개인화 알고리즘에 대한 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md)을 참조하십시오. Target의 개인화 모델에 사용할 새 특성을 Target에 업로드하는 방법에 대한 자세한 내용은 [데이터를 Target에 가져오는 방법](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}을 참조하십시오.

**자동화된 세그먼트란?**

&quot;자동화된 세그먼트&quot;는 대상과 비슷하지만, 마케터가 아닌 Target의 개인화 모델로 정의됩니다.

자동화된 세그먼트는 특정 속성의 특정 값(또는 값 범위)으로 구성됩니다. 예제 자동화된 세그먼트에 대해서는 위의 5단계를 참조하십시오. 세그먼트는 겹칠 수 있습니다.

Target의 개인화 모델의 기반이 되는 Random Forest 개인화 알고리즘에 대한 자세한 내용은 [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md)을 참조하세요.

**자동화된 세그먼트의 순서를 결정하는 것은 무엇입니까?**

점수는 각 세그먼트의 크기 및 활동의 컨텐츠에 대해 세그먼트가 얼마나 다르게 수행되었는지를 기반으로 하여 각 세그먼트에 대해 계산됩니다. 이러한 입력의 조합에 따라 자동화된 세그먼트의 순서가 결정되므로, 다른 컨텐츠에 응답하는 방식에 큰 차이가 세그먼트가 많을수록 그러한 세그먼트가 목록에서 거의 맨 위에 표시됩니다.

**내 오퍼/경험 중 일부만 자동화된 세그먼트 보고서에 표시되는 이유는 무엇입니까?**

AP 및 AT 활동은 오퍼마다 한 개의 모델(AP의 경우)과 경험마다 한 개의 모델(AT의 경우)을 빌드합니다. 이러한 활동은 개인화된 트래픽을 제공하고 구축된 모델이 두 개뿐인 [!UICONTROL Personalization Insights]을(를) 만듭니다. [!UICONTROL Personalization Insights]에 일부 오퍼/경험이 표시되지 않으면 특정 오퍼/경험을 위해 만들어진 모델이 없을 수 있습니다. 활동의 [!UICONTROL Summary] 보고서를 확인하고 해당 오퍼/경험 옆에 시계 아이콘이 있는지 확인할 수 있습니다. 이 아이콘은 모델이 해당 오퍼/경험용으로 아직 빌드되지 않았음을 나타냅니다.

**전환율이 낮은 일부 오퍼/경험이 특정 자동화된 세그먼트에 대한 다른 오퍼/경험보다 큰 트래픽을 수신하는 이유는 무엇입니까?**

다음을 포함하여 자동화된 세그먼트 내에서 전환율이 낮은 오퍼 또는 경험에 대한 더 많은 방문 횟수를 볼 수 있는 몇 가지 잠재적인 이유가 있습니다.

* 특정 자동화된 세그먼트의 일부 또는 전체 오퍼/경험에 대한 보기 횟수가 적습니다.
* 특정 오퍼/경험에 모델이 빌드되지 않았거나 모델이 다른 오퍼/경험보다 일부 오퍼/경험이 빠르게 빌드된 활동의 볼륨이 작습니다.
* 방문자가 볼 수 있는 오퍼/경험을 제한하는 특정 오퍼에 대한 타깃팅 규칙입니다.

**[!UICONTROL Automated Segments] 및 [!UICONTROL Important Attributes] 보고서의 정보가 CSV 다운로드와 같습니까?**

아니요, UI 보고서에는 선택 정보가 포함되어 있습니다. CSV 다운로드에 추가 세부 사항이 포함되어 있습니다. 자동화된 세그먼트 인사이트 보고서 다운로드에는 UI에 포함된 최상위 세그먼트 외에 그러한 세그먼트가 오퍼 또는 경험에 대해 수행된 방식과 함께 추가 자동화 세그먼트가 포함되어 있습니다. 중요 속성 보고서에는 상위 100개 방문자 속성과 상대적 중요도가 포함되어 있지만, UI에는 상위 10개 방문자 속성만 포함되어 있습니다.

**사용자 지정 날짜 범위에 대한 [!UICONTROL Personalization Insights]을(를) 볼 수 있습니까?**

Personalization Insights 보고([!UICONTROL Automated Segments] 및 [!UICONTROL Important Attributes] 모두)는 고정 날짜 범위인 15일, 30일 및 60일에 대해서만 사용할 수 있습니다. 이러한 고정 날짜 범위를 사용하면 [!UICONTROL Personalization Insights]에서 충분히 큰 데이터 범위를 사용하여 활동의 단기 패턴에서 통찰력을 얻을 가능성을 줄일 수 있습니다. 종료 날짜에 대해 이러한 지속 시간을 선택할 수 있습니다(활동에 지속 시간을 충족할 충분한 데이터가 있는 경우).

**어떻게 [!UICONTROL Personalization Insights]이(가) 만들어졌습니까?**

[!UICONTROL Personalization Insights]은(는) MAGIX(Model Agnostic Globally Interpretable Explanations)라는 Adobe 특허 출원 기술을 사용하여 만들어집니다. [arXiv.org 웹 사이트](https://arxiv.org/abs/1706.07160)에 Adobe 연구 팀이 게시한 문서에서 MAGIX에 대해 자세히 알아볼 수 있습니다.

**[!UICONTROL Automated Segments] 보고서의 총 방문자 트래픽 데이터가 AP 또는 AT 요약/성과 보고서와 일치하지 않는 이유는 무엇입니까?**

[!UICONTROL Personalization Insights] 보고서에는 Target의 개인화 모델에서 선택한 콘텐츠를 본 방문자만 포함됩니다(즉, 전체 승자 모델에서 제공하는 제어 트래픽이나 트래픽을 고려하지 않음). 이 트래픽 유형을 &quot;개인화된&quot; 트래픽이라고 합니다. AP/AT의 요약 성능 보고서에는 제어와 &quot;대상&quot; 트래픽이 포함됩니다. 타깃팅된 트래픽에는 개인화된 트래픽뿐만 아니라, 전체 승자 모델을 사용하여 제공된 트래픽과 학습을 계속하는 데 사용되는 임의로 제공된 일부 트래픽이 포함되어 있습니다.

**자동화된 세그먼트가 상호 배타적입니까?**

아니요, 자동화된 세그먼트가 서로 겹칩니다.

**수익 기반 모델링 목표/기본 목표에 [!UICONTROL Personalization Insights]을(를) 사용할 수 있습니까?**

현재 [!UICONTROL Personalization Insights]은(는) 전환 최적화 목표 활동에만 사용할 수 있습니다. Adobe은 향후 릴리스에서 수익 최적화 목표 활동에 대한 지원을 추가할 예정입니다.

**개인화 인사이트의 정보를 활용할 수 있는 다른 방법에는 어떤 것이 있습니까?**

* 타깃팅할 새 대상 살펴보기: 성과가 좋은 특정 자동화된 세그먼트가 표시되면 대상을 만들어 다른 보고서에서 해당 세그먼트를 재사용할 수 있도록 고려해볼 수 있습니다.
* 어떤 유형의 방문자가 어떤 경험에 응답하는지에 대한 가설을 테스트합니다.
* 방문자에게 적용된 콘텐츠 종류에 대한 인사이트를 얻습니다. 즉, 오퍼가 방문자에 대한 리프트를 담당합니다.
* 성과가 낮은 콘텐츠를 식별합니다.
* 모델 학습 방법에 가장 중요한 속성을 파악합니다.
* 개인화 모델에서 사용되는 속성 및 그러한 속성의 중요도를 확인합니다.
* 개인화를 자세히 알릴 Target에 전달할 수 있는 추가 데이터 포인트에 대한 기회를 식별합니다.

**세그먼트 카드에 속성이 표시되는 순서에 논리가 있습니까?**

아니요, 카드 순서는 위에서 설명한 순위만 기준으로 합니다. 카드 내의 속성 순서는 논리를 기반으로 하지 않습니다.
