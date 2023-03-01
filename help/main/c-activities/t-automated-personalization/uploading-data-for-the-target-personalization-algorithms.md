---
keywords: Automated Personalization;ap;데이터 업로드;오프라인 데이터;개인화 알고리즘;자동 타겟;자동 타겟;우수 사례
description: Adobe에서 개인화 모델을 만들 때 CRM 정보와 같은 오프라인 데이터를 업로드하는 방법을 알아봅니다 [!DNL Target] Automated Personalization (AP) 활동.
title: 개인화 알고리즘을 위해 데이터를 업로드하려면 어떻게 해야 합니까?
feature: Automated Personalization
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 7c15a0795e94b6c6317cb5b4018899be71f03a40
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 32%

---

# 다음에 대한 데이터 업로드 [!DNL Target] 개인화 알고리즘

CRM 정보 또는 고객 이탈 성향 점수와 같은 오프라인 데이터는에서 개인화 모델을 구축할 때 매우 유용할 수 있습니다. [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) 활동.

[!UICONTROL 자동화된 개인화] (AP)와 [!UICONTROL 자동 타겟] 개인화 알고리즘에서 데이터를 입력하는 방법에는 몇 가지가 있습니다. 의 메서드 외에 [데이터를 Target으로 가져오는 방법](https://experienceleague.corp.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}, Experience Cloud shared audiences (Adobe Analytics, Audience Management){target=_blank} 및 활동 보고 대상도 알고리즘에 사용됩니다.

자동화된 개인화 및 자동 타겟 개인화 알고리즘에서 자동으로 수집 및 사용되는 데이터에 대해서는 [자동화된 개인화 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md)을 참조하십시오.

## 우수 사례 {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

다음 목록은 Target의 개인화 알고리즘에 대한 데이터를 업로드하는 우수 사례입니다.

* Target의 개인화 알고리즘에 사용할 수 있는 고품질 데이터가 많을수록 AP 및 자동 Target 활동의 결과 모델 품질이 향상됩니다.
* 동일한 목적을 제공하는 여러 프로필 스크립트 또는 속성 사용을 제한합니다.
* 필요하지 않은 경우 세션 ID와 같은 고유 ID를 전달하지 마십시오.
* Target에서 자동으로 수집하는 데이터 검토( [Target의 개인화 알고리즘에 대한 데이터 수집](/help/main/c-activities/t-automated-personalization/ap-data.md))을 클릭하여 중복 정보를 전송하지 않습니다. 예를 들어, Target은 IP 주소를 사용하여 방문자의 우편 번호를 판별합니다. 이 정보를 별도의 변수로 전달하지 않아도 됩니다.
* 동일한 속성/변수에 여러 값을 전달하지 마십시오. 여러 변수가 연결된 경우 Target의 개인화 알고리즘이 각 문자열을 고유한 값으로 처리하므로 개인화를 위한 정보의 값이 줄어듭니다.
* 기억에 남고 의미 있는 명명 규칙을 사용하여 [개인화 통찰력 보고서](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) 더 이해하기 쉽습니다.
