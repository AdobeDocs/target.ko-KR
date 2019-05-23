---
description: 두 개의 전문 보고서는 AP(자동화된 개인화)와 AT(자동 타겟) 활동인 자동화된 세그먼트와 중요 속성 보고서의 사용자가 사용할 수 있습니다.
keywords: 타깃팅;AP 보고서;자동화된 개인화 보고서;자동 타겟;auto target;auto target 보고서;자동 타겟 보고서;개인화;통찰력;자동화된 세그먼트;faq;자주 묻는 질문;중요 속성
seo-description: 두 개의 전문 보고서는 AP(자동화된 개인화)와 AT(자동 타겟) 활동인 자동화된 세그먼트와 중요 속성 보고서의 사용자가 사용할 수 있습니다.
seo-title: 개인화 통찰력 보고서
solution: Target
title: 개인화 통찰력 보고서
title-outputclass: premium
uuid: 2507a7a6-d229-412a-a992-5777b45c80e7
badge: premium
translation-type: tm+mt
source-git-commit: 6cd0179b3fc1df8ec9ae1cbecd10749f751d9cd8

---


# ![PREMIUM](/help/assets/premium.png) 개인화 통찰력 보고서{#personalization-insights-reports}

두 개의 전문 보고서는 AP(자동화된 개인화) 및 AT(Auto-Target) 활동인 자동화된 세그먼트와 중요 속성 보고서 사용자가 사용할 수 있습니다.

>[!NOTE]
>
>AP 및 AT 활동은 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에는 포함되지 않습니다.
>
>개인화 인사이트 보고서는 전환 최적화 목표를 사용하는 AP 및 AT 활동에만 사용할 수 있습니다. 활동이 이미 활성화된 후에 수익에서 전환하도록 최적화 목표가 변경된 활동도 지원되지 않습니다.
>
>개인화 통찰력 보고서는 [기본 환경](../../administrating-target/hosts.md)에서만 지원됩니다.

## 개인화 통찰력 보고 개요 {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

[!UICONTROL 개인화 인사이트] 보고서의 목표는 AP 및 AT 활동 이면의 Target 개인화 모델이 방문자 트래픽을 개인화하는 방법에 대한 자세한 정보를 제공하는 것입니다. [Random Forest 알고리즘](/help/c-activities/t-automated-personalization/algo-random-forest.md)은 Target의 개인화 모델에 대한 기준입니다.

개인화 인사이트의 목표는 Target의 개인화 모델이 어떤 컨텐츠에 어떤 방문자를 보낼지 결정하는 방법을 이해하는 것이므로, 개인화 인사이트 보고서는 AP 또는 AT 활동이 제공하는 모든 트래픽의 하위 세그먼트만 반영합니다. 특히, 두 보고서는 개인화 모델을 사용한 모든 트래픽을 반영합니다. 즉, 개인화 인사이트 보고서는 전체 승자 모델에서 제공하는 제어 트래픽이나 트래픽을 고려하지 않습니다.

사용할 수 있는 보고서로는 두 가지가 있습니다.

| 보고서 | 세부 사항 |
|--- |--- |
| 자동화된 세그먼트 | 다른 방문자가 AP/AT 활동의 오퍼/경험에 다르게 응답합니다. 이 보고서는 Target의 개인화 모델에 정의된 다른 자동화된 세그먼트가 활동의 오퍼/경험에 응답하는 방식을 보여 줍니다. |
| 중요 속성 | 다른 활동에서 다른 속성은 모델이 개인화를 결정하는 방법에 대해 더 중요하거나 덜 중요합니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다. |

## 개인화 통찰력의 속성 해석 {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

AP 또는 자동 Target 모델에 사용되는 [!UICONTROL 개인화 인사이트] 보고서에는 두 가지 유형의 속성이 표시됩니다.

* **Target에서 자동으로 수집한 속성:** Target은 기본 데이터 세트를 사용하여 개인화 인사이트에 반영된 AP 및 AT 활동에 해당 개인화 알고리즘을 작성합니다. 데이터 유형, 예제 속성 및 [!UICONTROL 개인화 통찰력] 이름 지정 규칙에 대해서는 [Target의 개인화 알고리즘에 대한 데이터 수집](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058)을 참조하십시오. 이러한 속성을 고려하지만 개별 활동 모델은 최종 모델에서 이러한 속성을 모두 사용하지 않을 수 있습니다.
* **Target에 전달된 속성:** [Target의 개인화 알고리즘을 위한 데이터 업로드](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6)를 참조하십시오.

Target은 AP 및 AT 활동에서 해당 개인화 알고리즘을 작성하는 데 사용된 기본 데이터 세트를 보강하기 위해 Target에 추가 데이터를 전달하는 여러 가지 방법을 제공합니다.

| 데이터 유형 | 설명 | 데이터 유형 이름 지정 규칙 |
|--- |--- |--- |
| 프로필 스크립트, 프로필 업데이트 API 및 인페이지 프로필 속성을 포함한 프로필 속성 | Target의 사용자 프로필에 포함하기로 한 모든 정보입니다.<br>이 정보는 프로필 스크립트, 프로필 업데이트 API를 사용하여 업로드된 정보 또는 &quot;profile&quot;이 접두사로 추가된 mbox 내부 프로필 매개 변수에서 제공될 수 있습니다. | `Custom - Profile - [parameter name]` |
| 페이지 매개 변수(&quot;mbox 매개 변수&quot;라고도 함) | 나중에 사용할 수 있도록 방문자 프로필에 저장되지 않은 페이지 코드를 통해 직접 전달된 이름/값 쌍입니다. | `Custom - Mbox Parameter - [parameter name]` |
| 고객 속성 | 고객 속성을 사용하면 FTP를 통해 방문자 프로필 데이터를 Experience Cloud에 업로드할 수 있습니다. 업로드했으면 Adobe Analytics 및 Adobe Target의 데이터를 활용합니다. | `Custom - Customer Attributes - [parameter name]` |
| 공유 대상(Adobe Audience Manager 또는 Adobe Analytics) | Adobe Audience Manager 또는 Adobe Analytics를 통해 생성되고 Target과 공유되는 대상입니다. | `Custom - Experience Cloud Segment - [segment name]` |
| 활동 보고 대상/세그먼트 | &quot;목표 및 지표&quot;에서 설정하는 동안 AP 또는 자동 Target 활동에 정의된 대상입니다. | `Custom - Reporting Segment - [segment name]` |

## 교육 비디오: 개인화 통찰력 보고서 사용

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

자세한 내용은 Adobe Target에서 개인화 인사이트 보고서 [사용을](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html)참조하십시오.
