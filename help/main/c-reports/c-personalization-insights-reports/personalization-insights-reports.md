---
keywords: 타깃팅;AP 보고서;자동화된 개인화 보고서;자동 타겟;auto target;auto target 보고서;자동 타겟 보고서;개인화;통찰력;자동화된 세그먼트;faq;자주 묻는 질문;중요 속성
description: Automated Personalization(AP) 및 자동 타겟(AT) 활동용 전문 보고서 - 자동화된 세그먼트와 중요 속성을 사용하는 방법에 대해 알아봅니다.
title: 개인화 통찰력 보고서를 사용하려면 어떻게 해야 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
feature: Reports
exl-id: 89295d95-f179-4277-ae63-453350e1bba8
source-git-commit: 6c8f042acb257fc908349c679bf745e477f94af4
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 28%

---

# [!UICONTROL Personalization Insights] 보고서

다음의 사용자는 두 개의 전문 보고서를 사용할 수 있습니다. [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL Auto-Target] (AT) 활동: [!UICONTROL Automated Segments] 및 [!UICONTROL Important Attributes] 보고서.

## 고려 사항

을 사용할 때는 다음 사항을 고려하십시오 [!UICONTROL Personalization Insights] 보고서:

* AP 및 AT 활동은 의 일부로 사용할 수 있습니다 [[!DNL Target Premium] 솔루션](/help/main/c-intro/intro.md#premium). [!DNL Target Premium] 라이센스가 없는 [!DNL Target Standard]에는 포함되지 않습니다.

* [!UICONTROL Personalization Insights] 보고서는 다음과 같이 구성된 AP 및 AT 활동에만 사용할 수 있습니다.

   * [!DNL Target] 보고 > [!UICONTROL Conversion]

     예:

     ![Target 보고 > 전환](/help/main/c-reports/assets/conversion.png)

   * [!DNL Analytics] 보고 > [!DNL Conversion]

     예:

     ![분석 보고 > 전환](/help/main/c-reports/assets/analytics-reporting-conversion.png)

   * [!DNL Analytics] 보고 > [!UICONTROL Use an Analytics metric] > [!UICONTROL Maximize Visit Conversion Rate]

     예:

     ![Analytics 지표 > 방문 전환율 최대화 사용](/help/main/c-reports/assets/maximize-visit-conversion-rate.png)

* 활동이 이미 활성화된 후에 수익에서 전환하도록 최적화 목표가 변경된 활동도 지원되지 않습니다.

* [!UICONTROL Personalization Insights] 보고서는 다음 경우에만 사용할 수 있습니다 [!UICONTROL Primary Goal] 에서 선택됨 [!UICONTROL Report Metric] 드롭다운 목록입니다.

* [!UICONTROL Personalization Insights] 보고서는에서 지원됩니다. [기본 환경](/help/main/administrating-target/hosts.md) 만 해당.

* [!UICONTROL Personalization Insights] 보고서는에 있는 활동에 대해서만 생성됩니다. [!UICONTROL Live] 최소 15일 동안 및 가 활성화되고 트래픽을 수신하고 있습니다.

## 개인화 통찰력 보고 개요 {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

의 목표 [!UICONTROL Personalization Insights] 보고서는 다음과 같은 방법에 대한 자세한 정보를 [!UICONTROL Target] ap 및 AT 활동 이면의 개인화 모델은 방문자 트래픽을 개인화합니다. 다음 [Random Forest 알고리즘](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) 은(는) 의 기초입니다. [!DNL Target] 개인화 모델.

왜냐하면 [!UICONTROL Personalization Insights] 보고서는 이(가) [!DNL Target] 개인화 모델이 어떤 콘텐츠를 [!UICONTROL Personalization Insights] 보고서는 AP 또는 AT 활동이 제공하는 모든 트래픽의 하위 세그먼트만 반영합니다. 특히, 두 보고서는 개인화 모델을 사용한 모든 트래픽을 반영합니다. 다른 말로 하자면 [!UICONTROL Personalization Insights] 보고서는 전체 승자 모델에서 제공하는 제어 트래픽 또는 트래픽을 고려하지 않습니다.

2 [!UICONTROL Personalization Insights] 보고서를 사용할 수 있습니다.

| 보고서 | 세부 사항 |
|--- |--- |
| [!UICONTROL Automated Segments] | 다른 방문자가 AP/AT 활동의 오퍼/경험에 다르게 응답합니다. 이 보고서는 [!DNL Target] 개인화 모델은 활동의 오퍼/경험에 응답했습니다. |
| [!UICONTROL Important Attributes] | 다른 활동에서 다른 속성은 모델이 개인화를 결정하는 방법에 대해 더 중요하거나 덜 중요합니다. 이 보고서는 모델 및 모델의 상대적 중요도에 영향을 미친 주요 속성을 보여 줍니다. |

## 개인화 통찰력의 속성 해석 {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

에는 두 가지 유형의 속성이 표시됩니다. [!UICONTROL Personalization Insights] AP 또는 자동 타겟 모델에 사용되는 보고서:

* **Target에서 자동으로 수집한 속성:** [!DNL Target] 은 기본 데이터 세트를 사용하여 개인화 인사이트에 반영되는 AP 및 AT 활동에서 개인화 알고리즘을 구축합니다. 다음을 참조하십시오 [Target의 개인화 알고리즘에 대한 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md) 데이터 유형, 예제 속성 및 해당 [!UICONTROL Personalization Insights] 명명 규칙. 이러한 속성이 고려되지만 개별 활동의 모델은 최종 모델에서 이러한 모든 속성을 사용하지 않을 수 있습니다.
* **Target에 전달된 속성:** 다음을 참조하십시오 [Target의 개인화 알고리즘을 위한 데이터 업로드](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] 는 추가 데이터를에 전달하는 다양한 방법을 제공합니다. [!DNL Target] ap 및 AT 활동에서 개인화 알고리즘을 작성하는 데 사용되는 기본 데이터 세트를 보강하려면 다음을 수행하십시오.

| 데이터 유형 | 설명 | 데이터 유형 이름 지정 규칙 |
|--- |--- |--- |
| 프로필 스크립트, 프로필 업데이트 API 및 인페이지 프로필 속성을 포함한 프로필 속성 | Target의 사용자 프로필에 포함하기로 한 모든 정보입니다.<br>이 정보는 프로필 스크립트, 프로필 업데이트 API를 사용하여 업로드된 정보 또는 &quot;profile&quot;이 접두사로 추가된 mbox 내부 프로필 매개 변수에서 제공될 수 있습니다. | `Custom - Profile - [parameter name]` |
| 페이지 매개 변수(&quot;mbox 매개 변수&quot;라고도 함) | 나중에 사용할 수 있도록 방문자 프로필에 저장되지 않은 페이지 코드를 통해 직접 전달된 이름/값 쌍입니다. | `Custom - Mbox Parameter - [parameter name]` |
| 고객 속성 | 고객 속성을 사용하면 FTP를 통해 방문자 프로필 데이터를 Experience Cloud에 업로드할 수 있습니다. 업로드했으면 Adobe Analytics 및 Adobe Target의 데이터를 활용합니다. | `Custom - Customer Attributes - [parameter name]` |
| 공유 대상(Adobe Audience Manager 또는 Adobe Analytics) | Adobe Audience Manager 또는 Adobe Analytics를 통해 생성되고 Target과 공유되는 대상입니다. | `Custom - Experience Cloud Segment - [segment name]` |
| 공유 대상(Adobe Experience Platform/Real-time CDP) | Adobe Experience Platform/Real-Time CDP를 통해 만들어지고 대상을 통해 Target과 공유되는 대상입니다. | `Custom - Adobe Experience Platform Segment - [segment name]` |
| 공유 속성(Adobe Experience Platform/Real-time CDP) | Adobe Experience Platform/Real-Time CDP를 통해 생성되고 대상을 통해 Target과 공유되는 속성입니다. 이 기능은 현재 Beta 버전입니다. | `Custom - Adobe Experience Platform Attribute - [attribute name]]` |
| 활동 보고 대상/세그먼트 | &quot;목표 및 지표&quot;에서 설정하는 동안 AP 또는 자동 타겟 활동에 정의된 대상입니다. | `Custom - Reporting Segment - [segment name]` |

## 자주 묻는 질문

다음에 대한 FAQ 목록 [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL Auto-Target] [!UICONTROL Insights] 보고서.

### 데이터 체류 기간 [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL Auto-Target] 모델이 지속됩니까?

[!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL Auto-Target] 모델은 활동에 대한 지난 45일 사용자 비헤이비어(사용자 프로필, 노출 이벤트 및 전환 이벤트)에 대해 교육됩니다.

[!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL Auto-Target] 모델은 90일 동안 사용자 비헤이비어, 교육 레코드 및 모델 결정 데이터를 유지하여 [!UICONTROL Insights] 보고서. 90일 이후에는 교육 기록 및 모델 결정을 삭제합니다. [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL Auto-Target] 또한 모델은 2년 동안 보고 목적으로 집계된 경험/오퍼 수준 노출 및 전환 데이터를 유지합니다. 이 데이터는 집계 수준 데이터이며 개별 수준 프로필 데이터를 포함하지 않습니다.

## 교육 비디오: 개인화 통찰력 보고서 사용 ![튜토리얼 배지](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

자세한 내용은 [Adobe Target에서 개인화 통찰력 보고서 사용](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Adobe 블로그

* 1부: [AI 기반 개인화의 마법에서 미스터리 제거](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* 2부: [Adobe Target의 개인화를 위한 AI의 장막 뒤에서 엿보기](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* 3부: [MAGIX — AI 기반 개인화의 블랙박스 문제에 대한 솔루션](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
