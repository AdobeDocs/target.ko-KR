---
keywords: aem;experience manager;adobe experience manager;통합;통합 기능;경험 조각;콘텐츠 조각
description: ' [!DNL Adobe Target] 활동에서 [!DNL Adobe Experience Manager] 경험 조각 및 콘텐츠 조각을 사용하는 방법에 대해 알아봅니다.'
title: ' [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments]을(를) 사용하는 방법'
feature: Integrations
exl-id: 6f1a02da-8f59-4a8b-8e97-c20444ef53c8
source-git-commit: f39ec80d9804fff2c65fce98ca2be5400d99aad0
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 40%

---

# AEM [!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments] 개요

최적화 및 개인화를 지원하기 위해 [!UICONTROL Experience Fragments] 활동의 [!UICONTROL Content Fragments]&#x200B;(AEM)에서 만든 [!DNL Adobe Experience Manager]&#x200B;(XF) 및 [!DNL Target]&#x200B;(CF)를 사용합니다.

[!UICONTROL Experience Fragments] 활동의 [!UICONTROL Content Fragments]에서 만든 [!DNL AEM] 및 [!DNL Target]을(를) 사용하면 [!DNL AEM]의 편의성과 기능을 [!DNL Target]의 강력한 AI(인공 지능) 및 ML(기계 학습) 기능과 결합하여 경험을 다양한 규모로 테스트 및 개인화할 수 있습니다.

[!DNL AEM]에서는 모든 콘텐츠 및 에셋을 중앙 위치에 가져와서 개인화 전략을 실행합니다. [!DNL AEM]을 사용하면 코드를 작성하지 않고도 한 위치에서 데스크탑, 태블릿 및 모바일 디바이스의 콘텐츠를 쉽게 만들 수 있습니다. 모든 디바이스에 대해 페이지를 만들 필요가 없습니다. [!DNL AEM]은 콘텐츠를 사용하여 모든 디바이스에 대한 각 경험을 자동으로 조정합니다.

[!DNL Target]을 사용하면 행동 변수, 상황별 변수 및 오프라인 변수를 통합하는 규칙 기반 및 AI 중심 머신 러닝 접근 방식들의 결합을 기반으로 다양한 규모의 개인화된 경험을 제공할 수 있습니다.

[!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments]은(는) [!DNL Target]을(를) 사용하여 비즈니스 결과를 이끄는 최적화 및 개인화 전문가에게 콘텐츠/경험 작성자 및 관리자를 연결하기 위한 매우 큰 단계를 나타냅니다.

## 고려 사항

[!UICONTROL Experience Fragments]에서 AEM [!UICONTROL Content Fragments] 및 [!DNL Target]을(를) 사용하여 작업할 때 다음 사항을 고려하십시오.
* 이 기능을 사용하려면 [!DNL Adobe Experience Manager] (AEM) 고객이어야 합니다. 각 조각 유형에 대한 요구 사항을 충족하는지 확인: [경험 조각](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md#requirements) 또는 [콘텐츠 조각](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md#requirements).
* [!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments]은(는) 다음 활동 유형에 사용할 수 있습니다.

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization]&#x200B;(AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting]&#x200B;(XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] 및 [!UICONTROL Content Fragments]은(는) 다음 활동 유형에 사용할 수 없습니다.

   * [[!UICONTROL Multivariate Test]&#x200B;(MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* [!UICONTROL Experience Fragments]시각적 경험 작성기[!DNL Target]&#x200B;(VEC) 및 [양식 기반 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md)를 사용하여 [ 활동에서 ](/help/main/c-experiences/form-experience-composer.md)을(를) 사용할 수 있습니다.
* [!UICONTROL Content Fragments]양식 기반 경험 작성기[!DNL Target]만 사용하여 [ 활동에서 ](/help/main/c-experiences/form-experience-composer.md)을(를) 사용할 수 있습니다.

## [!UICONTROL Experience Fragments]과(와) [!UICONTROL Content Fragments]의 차이점은 무엇입니까?

[!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments]과(와) [!UICONTROL Content Fragments]은(는) 겉보기에는 비슷해 보일 수 있지만 각 조각 유형이 다른 사용 사례에서 주요 역할을 합니다.

[!UICONTROL Experience Fragments]과(와) [!UICONTROL Content Fragments]의 유사성, 차이성, 사용 시기 및 방법에 대한 자세한 내용은 [AEM Sites 비디오 및 튜토리얼 가이드[!UICONTROL Content Fragments]에서 [!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/content-fragments/understand-content-fragments-and-experience-fragments.html){target=_blank} 및 [](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/overview.html){target=_blank} 이해 를 참조하십시오.
