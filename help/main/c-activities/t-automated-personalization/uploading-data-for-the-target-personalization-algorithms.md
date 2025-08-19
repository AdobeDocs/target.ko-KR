---
keywords: Automated Personalization;ap;데이터 업로드;오프라인 데이터;개인화 알고리즘;자동 타겟;자동 타겟;우수 사례
description: ' [!DNL Adobe Target] [!UICONTROL Automated Personalization](AP) 및 [!UICONTROL Auto-Target] 활동에서 개인화 모델을 만들 때 오프라인 데이터를 업로드하는 방법을 알아봅니다.'
title: Personalization 알고리즘을 위해 데이터를 업로드하려면 어떻게 해야 합니까?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 3f64da1c9a1146e4d2d9389d6d5ce764764d2d9c
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 10%

---

# [!DNL Target] 개인화 알고리즘에 대한 데이터 업로드

CRM 정보 또는 고객 이탈 성향 점수와 같은 오프라인 데이터는 [!DNL Adobe Target] [!UICONTROL Automated Personalization]&#x200B;(AP) 및 [!UICONTROL Auto-Target] 활동에서 개인화 모델을 작성할 때 매우 유용할 수 있습니다.

[!UICONTROL Automated Personalization]&#x200B;(AP) 및 [!UICONTROL Auto-Target] 개인화 알고리즘에서 데이터를 입력하는 방법에는 여러 가지가 있습니다. [데이터를 Target에 가져오는 메서드](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}의 메서드 외에도 [!DNL Experience Cloud]개의 공유 대상([!UICONTROL Adobe Analytics], [!DNL Audience Manager]) 및 활동 보고 대상도 [!DNL Target] 알고리즘에서 사용됩니다.

[!UICONTROL Automated Personalization] 및 [!UICONTROL Auto-Target] 개인화 알고리즘에서 자동으로 수집 및 사용되는 데이터에 대한 자세한 내용은 [Automated Personalization 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md)을 참조하십시오.

## 우수 사례 {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

다음 목록에는 [!DNL Target] 개인화 알고리즘을 위한 데이터 업로드에 대한 모범 사례가 나와 있습니다.

* [!DNL Target] 개인화 알고리즘에서 사용할 수 있는 고품질 데이터가 많을수록 [!UICONTROL Automated Personalization] 및 [!UICONTROL Auto-Target] 활동의 결과 모델 품질이 향상됩니다.
* 동일한 목적을 제공하는 여러 프로필 스크립트 또는 속성 사용을 제한합니다.
* 필요하지 않은 경우 세션 ID와 같은 고유 ID를 전달하지 마십시오.
* 중복 정보를 보내지 않도록 [!DNL Target]에서 자동으로 수집하는 데이터([Target의 Personalization 알고리즘에 대한 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md))를 검토하십시오. 예를 들어 [!DNL Target]은(는) IP 주소를 사용하여 방문자의 ZIP 코드를 결정합니다. 이 정보를 별도의 변수로 전달하지 않아도 됩니다.
* 동일한 속성 또는 변수에 여러 값을 전달하지 마십시오. 여러 변수가 연결된 경우 [!DNL Target] 개인화 알고리즘이 각 문자열을 고유한 값으로 처리하므로 개인화를 위한 정보의 값이 줄어듭니다.
* 기억에 남고 의미 있는 명명 규칙을 사용하여 [Personalization 통찰력 보고서](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767)를 보다 쉽게 이해할 수 있습니다.
