---
keywords: aem;experience manager;adobe experience manager;통합;통합 기능;경험 조각;콘텐츠 조각
description: ' [!DNL Adobe Target] 활동에서 [!DNL Adobe Experience Manager] 경험 조각 및 콘텐츠 조각을 사용하는 방법에 대해 알아봅니다.'
title: ' [!DNL Adobe Experience Manager] (AEM) [!UICONTROL 경험 조각] 및 [!UICONTROL 콘텐츠 조각]을 사용하려면 어떻게 해야 합니까?'
feature: Integrations
source-git-commit: 0135831b56c48b0adca49e843c5ddd6574358aa4
workflow-type: ht
source-wordcount: '396'
ht-degree: 100%

---

# (AEM) [!UICONTROL 경험 조각] 및 [!UICONTROL 콘텐츠 조각] 개요

[!DNL Target] 활동의 [!DNL Adobe Experience Manager] (AEM)에서 생성된 [!UICONTROL 경험 조각] (XF) 및 [!UICONTROL 콘텐츠 조각] (CF)을 사용하여 최적화 또는 개인화를 지원할 수 있습니다.

>[!NOTE]
>
>[!DNL Target]에서 AEM [!UICONTROL 경험 조각] and [!UICONTROL Content Fragments]을 사용하여 작업할 때 고려할 사항:
> 
>* 이 기능을 사용하려면 [!DNL Adobe Experience Manager] (AEM) 고객이어야 합니다. 각 조각 유형에 대한 요구 사항을 충족하는지 확인: [경험 조각](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md#requirements) 또는 [콘텐츠 조각](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md#requirements).
>
>* 이 기능을 사용할 수 있는 활동 유형: [!UICONTROL A/B 테스트], [!UICONTROL 자동 할당], [!UICONTROL 자동 타겟팅], [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 경험 타겟팅] (XT). 이 기능은 [!UICONTROL 다변량 테스트] (MVT) 및 [!UICONTROL Recommendations] 활동에서 사용할 수 없습니다.
>* [시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md)(VEC) 또는 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 사용하여 [!DNL Target] 활동에서 [!UICONTROL 경험 조각]을 사용할 수 있습니다.
>
>* [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)만을 사용하여 [!UICONTROL 콘텐츠 조각]을 사용할 수 있습니다.


[!DNL Target] 활동에 [!DNL AEM]에서 만든 [!UICONTROL 경험 조각] 및 [!UICONTROL 콘텐츠 조각]을 사용하면 [!DNL AEM]의 편의성과 기능을 [!DNL Target]의 강력한 AI(인공 지능) 및 ML(기계 학습) 기능을 결합하여 경험을 다양한 규모로 테스트 및 개인화할 수 있습니다.

[!DNL AEM]에서는 모든 콘텐츠 및 에셋을 중앙 위치에 가져와서 개인화 전략을 실행합니다. [!DNL AEM]을 사용하면 코드를 작성하지 않고도 한 위치에서 데스크탑, 태블릿 및 모바일 디바이스의 콘텐츠를 쉽게 만들 수 있습니다. 모든 디바이스에 대해 페이지를 만들 필요가 없습니다. [!DNL AEM]은 콘텐츠를 사용하여 모든 디바이스에 대한 각 경험을 자동으로 조정합니다.

[!DNL Target]을 사용하면 행동 변수, 상황별 변수 및 오프라인 변수를 통합하는 규칙 기반 및 AI 중심 기계 학습 접근 방식들의 결합을 기반으로 다양한 규모의 개인화된 경험을 제공할 수 있습니다. [!DNL Target]을 사용하면 [A/B 테스트](/help/main/c-activities/t-test-ab/test-ab.md) 및 [다변량](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)(MVT) 활동을 쉽게 설정 및 실행하여 최상의 오퍼, 콘텐츠 및 경험을 결정할 수 있습니다.

[!UICONTROL 경험 조각] 및 [!UICONTROL 콘텐츠 조각]은 콘텐츠/경험 작성자 및 관리자를 [!DNL Target]을 사용하여 비즈니스 결과를 이끄는 최적화 및 개인화 전문가에게 연결하기 위한 매우 큰 단계를 나타냅니다.

## [!UICONTROL 경험 조각]과 [!UICONTROL 콘텐츠 조각]의 차이점은 무엇입니까?

[!DNL Adobe Experience Manager] [!UICONTROL 경험 조각] 및 [!UICONTROL 콘텐츠 조각]은 겉보기에 비슷해 보이나, 각 조각 유형은 다양한 사용 사례에서 중요한 역할을 합니다.

[!UICONTROL 콘텐츠 조각]과 [!UICONTROL 경험 조각]의 유사성과 차이점 및 각각의 사용 시기와 방법에 대한 자세한 내용은 [[!UICONTROL 콘텐츠 조각] 및 [!UICONTROL 경험 조각]](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/content-fragments/understand-content-fragments-and-experience-fragments.html){target="_blank"} in the [AEM Sites videos and tutorials guide](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/overview.html){target="_blank"} 이해를 참조하십시오.