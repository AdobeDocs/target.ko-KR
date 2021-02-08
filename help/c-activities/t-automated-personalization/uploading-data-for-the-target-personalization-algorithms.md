---
keywords: Automated Personalization;ap;업로드 데이터;오프라인 데이터;개인화 알고리즘;자동 대상;자동 타겟;모범 사례
description: Adobe Target Automated Personalization(AP) 활동에서 개인화 모델을 작성할 때 CRM 정보와 같은 오프라인 데이터를 업로드하는 방법을 알아봅니다.
title: 개인화 알고리즘에 대한 데이터를 어떻게 업로드할 수 있습니까?
feature: Automated Personalization
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 77%

---


# Target의 개인화 알고리즘을 위한 데이터 업로드

CRM 정보 또는 고객 이탈률 점수와 같은 오프라인 데이터는 [!DNL Adobe Target] [!UICONTROL Automated Personalization](AP) 활동에서 개인화 모델을 작성할 때 매우 유용할 수 있습니다.

[!UICONTROL 자동화된 개인화] (AP)와 [!UICONTROL 자동 타겟] 개인화 알고리즘에서 데이터를 입력하는 방법에는 몇 가지가 있습니다. [데이터를 Target에 가져오는 방법](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)에 나와 있는 방법 외에도 Experience Cloud 공유 대상(Adobe Analytics, 고객 관리) 및 활동 보고 대상도 알고리즘에 사용됩니다.

자동화된 개인화 및 자동 타겟 개인화 알고리즘에서 자동으로 수집 및 사용되는 데이터에 대해서는 [자동화된 개인화 데이터 수집](/help/c-activities/t-automated-personalization/ap-data.md)을 참조하십시오.

## 우수 사례 {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

다음 목록은 Target의 개인화 알고리즘에 대한 데이터를 업로드하는 우수 사례입니다.

* Target의 개인화 알고리즘에 사용할 수 있는 데이터가 고품질일수록 AP 및 자동 Target 활동의 결과 모델 품질이 향상됩니다.
* 동일한 목적을 제공하는 여러 프로필 스크립트 또는 속성 사용을 제한합니다.
* 필요하지 않은 경우 세션 ID와 같은 고유 ID를 전달하지 마십시오.
* Target에서 자동으로 수집하는 데이터를 검토하므로( [Target의 개인화 알고리즘에 대한 데이터 수집](/help/c-activities/t-automated-personalization/ap-data.md)) 중복 정보를 전송할 필요가 없습니다. 예를 들어, Target은 IP 주소를 사용하여 방문자의 우편 번호를 판별합니다. 이 정보를 별도의 변수로 전달하지 않아도 됩니다.
* 동일한 속성/변수에 여러 값을 전달하지 마십시오. 여러 변수가 연결된 경우 Target의 개인화 알고리즘은 각 문자열을 고유 값으로 처리하여 개인화에 대한 정보의 값을 줄입니다.
* 기억하기 쉽고 의미 있는 이름 지정 규칙을 사용하여 [개인화 인사이트 보고서](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767)를 보다 쉽게 구분할 수 있도록 합니다.

