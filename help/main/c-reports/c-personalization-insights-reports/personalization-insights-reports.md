---
keywords: 타깃팅;AP 보고서;자동화된 개인화 보고서;자동 타겟;auto target;auto target 보고서;자동 타겟 보고서;개인화;통찰력;자동화된 세그먼트;faq;자주 묻는 질문;중요 속성
description: Automated Personalization(AP) 및 AT(자동 Target) 활동인 자동화된 세그먼트와 중요 속성을 위해 전문 보고서를 사용하는 방법을 알아봅니다.
title: 개인화 인사이트 보고서를 사용하려면 어떻게 해야 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: 89295d95-f179-4277-ae63-453350e1bba8
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 45%

---

# 개인화 통찰력 보고서

두 개의 전문 보고서는 [!UICONTROL AP(자동화된 개인화)] 및 [!UICONTROL AT(Auto-Target]) 활동인 자동화된 세그먼트와 중요 속성 보고서 사용자가 사용할 수 있습니다.

>[!NOTE]
>
>개인화 통찰력 보고서를 사용할 때는 다음 사항을 고려하십시오.
>
>* AP 및 AT 활동은 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에는 포함되지 않습니다.
>
>* [!UICONTROL 개인화 인사이트 보고서는 전환 최적화 목표를 사용하는 AP 및 AT 활동에만 사용할 수 있습니다. ] 활동이 이미 활성화된 후에 수익에서 전환하도록 최적화 목표가 변경된 활동도 지원되지 않습니다.
>
>* [!UICONTROL 개인화 통찰력] 보고서는 [!UICONTROL 기본 목표] 선택 [!UICONTROL 보고서 지표] 드롭다운 목록.
>
>* 개인화 통찰력 보고서는 [기본 환경](/help/main/administrating-target/hosts.md)에서만 지원됩니다.
>
>* [!UICONTROL 개인화 통찰력] 보고서는 [!UICONTROL 라이브] 상태 및 이(가) 활성화되었으며 적어도 15일 동안 트래픽을 수신했습니다.


## 개인화 통찰력 보고 개요 {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

[!UICONTROL 개인화 인사이트] 보고서의 목표는 AP 및 AT 활동 이면의 Target 개인화 모델이 방문자 트래픽을 개인화하는 방법에 대한 자세한 정보를 제공하는 것입니다.  다음 [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) 는 [!DNL Target] 개인화 모델.

왜냐하면 [!UICONTROL 개인화 통찰력] 보고서는 [!DNL Target] 개인화 모델은 어떤 컨텐츠에 어떤 방문자를 보낼지 결정하였습니다. [!UICONTROL 개인화 통찰력] 보고서는 AP 또는 AT 활동에서 제공하는 모든 트래픽의 하위 세그먼트만 반영합니다. 특히, 두 보고서는 개인화 모델을 사용한 모든 트래픽을 반영합니다. 즉, [!UICONTROL 개인화 인사이트] 보고서는 전체 승자 모델에서 제공하는 제어 트래픽이나 트래픽을 고려하지 않습니다.

2 [!UICONTROL 개인화 통찰력] 보고서를 사용할 수 있습니다.

| 보고서 | 세부 사항 |
|--- |--- |
| [!UICONTROL 자동화된 세그먼트] | 다른 방문자가 AP/AT 활동의 오퍼/경험에 다르게 응답합니다. 이 보고서는 [!DNL Target] 개인화 모델은 활동의 오퍼/경험에 응답했습니다. |
| [!UICONTROL 중요 속성] | 다른 활동에서 다른 속성은 모델이 개인화를 결정하는 방법에 대해 더 중요하거나 덜 중요합니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다. |

## 개인화 통찰력의 속성 해석 {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

AP 또는 자동 Target 모델에 사용되는 [!UICONTROL 개인화 인사이트] 보고서에는 두 가지 유형의 속성이 표시됩니다.

* **Target에 의해 자동으로 수집된 속성:** [!DNL Target] 에서는 기본 데이터 세트를 사용하여 개인화 인사이트에 반영되는 AP 및 AT 활동에서 개인화 알고리즘을 만듭니다. 데이터 유형, 예제 속성 및 [!UICONTROL 개인화 통찰력] 이름 지정 규칙에 대해서는 [Target의 개인화 알고리즘에 대한 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md)을 참조하십시오. 이러한 속성이 고려되지만 개별 활동의 모델이 최종 모델에서 이러한 속성을 모두 사용하지 않을 수 있습니다.
* **Target에 전달된 특성:** 자세한 내용은 [Target 개인화 알고리즘을 위한 데이터 업로드](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] 에서는 추가적인 데이터를 [!DNL Target] ap 및 AT 활동에서 개인화 알고리즘을 작성하는 데 사용되는 기본 데이터 세트를 보강하려면 다음을 수행하십시오.

| 데이터 유형 | 설명 | 데이터 유형 이름 지정 규칙 |
|--- |--- |--- |
| 프로필 스크립트, 프로필 업데이트 API 및 인페이지 프로필 속성을 포함한 프로필 속성 | Target의 사용자 프로필에 포함하기로 한 모든 정보입니다.<br>이 정보는 프로필 스크립트, 프로필 업데이트 API를 사용하여 업로드된 정보 또는 &quot;profile&quot;이 접두사로 추가된 mbox 내부 프로필 매개 변수에서 제공될 수 있습니다. | `Custom - Profile - [parameter name]` |
| 페이지 매개 변수(&quot;mbox 매개 변수&quot;라고도 함) | 나중에 사용할 수 있도록 방문자 프로필에 저장되지 않은 페이지 코드를 통해 직접 전달된 이름/값 쌍입니다. | `Custom - Mbox Parameter - [parameter name]` |
| 고객 속성 | 고객 속성을 사용하면 FTP를 통해 방문자 프로필 데이터를 Experience Cloud에 업로드할 수 있습니다. 업로드했으면 Adobe Analytics 및 Adobe Target의 데이터를 활용합니다. | `Custom - Customer Attributes - [parameter name]` |
| 공유 대상(Adobe Audience Manager 또는 Adobe Analytics) | Adobe Audience Manager 또는 Adobe Analytics를 통해 생성되고 Target과 공유되는 대상입니다. | `Custom - Experience Cloud Segment - [segment name]` |
| 공유 대상(Adobe Experience Platform/실시간 CDP) | Adobe Experience Platform/실시간 CDP를 통해 만들고 대상을 통해 Target과 공유하는 대상. | `Custom - Adobe Experience Platform Segment - [segment name]` |
| 공유 속성(Adobe Experience Platform/실시간 CDP) | Adobe Experience Platform/실시간 CDP를 통해 생성되고 대상을 통해 Target과 공유되는 특성입니다. 이 기능은 현재 베타에 있습니다. | `Custom - Adobe Experience Platform Attribute - [attribute name]]` |
| 활동 보고 대상/세그먼트 | 목표 및 지표에서 설정하는 동안 AP 또는 자동 Target 활동에 정의된 대상. | `Custom - Reporting Segment - [segment name]` |

## 자주 묻는 질문

에 대한 FAQ 목록 [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 자동 Target] [!UICONTROL Insights] 보고서.

### [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 자동 타겟] 모델에 대한 데이터는 얼마나 지속됩니까?

[!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 자동 Target] 모델은 활동에 대한 최근 45일 동안의 사용자 동작(사용자 프로필, 노출 이벤트 및 전환 이벤트)에 대해 교육됩니다.

[!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 자동 Target] 모델은 사용자 행동, 트레이닝 레코드 및 모델 결정 데이터를 90일 동안 유지하여 [!UICONTROL Insights] 보고서. 90일 후 교육 기록 및 모델 결정을 삭제합니다. [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 자동 Target] 또한 모델은 보고 목적으로 집계된 경험/오퍼 수준 노출 및 전환 데이터를 2년 동안 유지합니다. 이 데이터는 집계 수준 데이터만 포함하며 개별 수준 프로필 데이터는 포함하지 않습니다.

## 교육 비디오: 개인화 통찰력 보고서 사용 ![튜토리얼 배지](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

자세한 내용은 [Adobe Target에서 개인화 통찰력 보고서 사용](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Adobe 블로그

* 1부: [AI 기반의 개인화 마법을 통한 미스터리 제거](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* 2부: [Adobe Target의 개인화를 위한 AI의 장막 뒷이야기](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* 3부: [MAGIX — AI 기반 개인화의 블랙 박스 문제 해결](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
