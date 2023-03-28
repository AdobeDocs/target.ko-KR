---
keywords: aem;experience manager;adobe experience manager;통합;통합;경험 구성요소;컨텐츠 조각
description: 사용 방법 알아보기 [!DNL Adobe Experience Manager] 의 경험 및 컨텐츠 조각 [!DNL Adobe Target] 활동.
title: 사용 방법 [!DNL Adobe Experience Manager] (AEM) [!UICONTROL 경험 조각] 및 [!UICONTROL 컨텐츠 조각]?
feature: Integrations
source-git-commit: 0135831b56c48b0adca49e843c5ddd6574358aa4
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# AEM [!UICONTROL 경험 조각] 및 [!UICONTROL 컨텐츠 조각] 개요

사용 [!UICONTROL 경험 조각] (XF) 및 [!UICONTROL 컨텐츠 조각] (CF를에서 생성) [!DNL Adobe Experience Manager] (AEM)에서 [!DNL Target] 최적화 또는 개인화를 지원하기 위한 활동.

>[!NOTE]
>
>AEM에서 작업할 때 다음 사항을 고려하십시오 [!UICONTROL 경험 조각] 및 [!UICONTROL 컨텐츠 조각] in [!DNL Target]:
> 
>* 이러한 기능을 사용하려면 다음을 수행해야 합니다 [!DNL Adobe Experience Manager] (AEM) 고객. 각 조각 유형에 대한 요구 사항을 충족하는지 확인합니다. [경험 조각](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md#requirements) 또는 [컨텐츠 조각](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md#requirements).
>
>* 이러한 기능은 다음 활동 유형에 사용할 수 있습니다. [!UICONTROL A/B 테스트], [!UICONTROL 자동 할당], [!UICONTROL 자동 Target], [!UICONTROL Automated Personalization] (AP) 및 [!UICONTROL 경험 타깃팅] (XT). 이 기능은 [!UICONTROL 다변량 테스트] (MVT) 및 [!UICONTROL Recommendations] 활동.
>* 소비할 수 있습니다 [!UICONTROL 경험 조각] in [!DNL Target] 를 사용하여 활동 [시각적 경험 작성기](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) 또는 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md).
>
>* 소비할 수 있습니다 [!UICONTROL 컨텐츠 조각] 에서 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md) 전용.


사용 [!UICONTROL 경험 조각] 및 [!UICONTROL 컨텐츠 조각] 에서 생성됨 [!DNL AEM] in [!DNL Target] 활동을 통해 사용 편의성과 기능을 결합할 수 있습니다 [!DNL AEM] 의 강력한 AI(인공 지능) 및 ML(기계 학습) 기능 사용 [!DNL Target] 경험을 규모에 맞게 테스트 및 개인화합니다.

[!DNL AEM] 모든 콘텐츠 및 자산을 중앙 위치에 가져와서 개인화 전략을 실행합니다. [!DNL AEM] 코드를 작성하지 않고도 한 위치에서 데스크톱, 태블릿 및 모바일 장치의 콘텐츠를 쉽게 만들 수 있습니다. 모든 장치를 위해 페이지를 만들 필요가 없습니다. [!DNL AEM] 콘텐츠를 사용하여 각 장치에 대해 각 경험을 자동으로 조정합니다.

[!DNL Target] 을 사용하면 행동, 컨텍스트 및 오프라인 변수를 통합하는 규칙 기반 기계 학습 접근 방식과 AI 기반 기계 학습 접근 방식을 조합하여 규모에 맞게 개인화된 경험을 제공할 수 있습니다. 사용 [!DNL Target], 쉽게 설정 및 실행할 수 있습니다. [A/B 테스트](/help/main/c-activities/t-test-ab/test-ab.md) 및 [다변량](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) 활동을 통해 최상의 오퍼, 콘텐츠 및 경험을 파악합니다.

[!UICONTROL 경험 조각] 및 [!UICONTROL 컨텐츠 조각] 은 컨텐츠/경험 작성자 및 관리자를 을 사용하여 비즈니스 결과를 이끄는 최적화 및 개인화 전문가에게 연결하기 위한 큰 단계를 나타냅니다. [!DNL Target].

## 그 사이의 차이점은 무엇입니까 [!UICONTROL 경험 조각] 및 [!UICONTROL 컨텐츠 조각]?

[!DNL Adobe Experience Manager] [!UICONTROL 경험 조각] 및 [!UICONTROL 컨텐츠 조각] 표면에서는 유사해 보일 수 있지만 각 조각 유형은 다른 사용 사례에서 주요 역할을 수행합니다.

방법에 대한 자세한 정보 [!UICONTROL 컨텐츠 조각] 및 [!UICONTROL 경험 조각] 는 서로 비슷하고, 서로 다르며, 각 보기를 사용하는 시기와 방법입니다 [이해 [!UICONTROL 컨텐츠 조각] 및 [!UICONTROL 경험 조각]](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/content-fragments/understand-content-fragments-and-experience-fragments.html){target=_blank} in the [AEM Sites videos and tutorials guide](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/overview.html){target=_blank}.