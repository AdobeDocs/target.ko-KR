---
description: CRM 정보나 고객 이탈 성향 점수와 같은 오프라인 데이터는 개인화 모델을 만들 때 매우 소중합니다.
seo-description: CRM 정보나 고객 이탈 성향 점수와 같은 오프라인 데이터는 개인화 모델을 만들 때 매우 소중합니다.
seo-title: Target의 개인화 알고리즘을 위해 데이터 업로드
solution: Target
title: Target의 개인화 알고리즘을 위해 데이터 업로드
topic: Premium
uuid: eb0938b9-7f35-4bb5-ac4b-260b2144db5b
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Target의 개인화 알고리즘을 위한 데이터 업로드{#upload-data-for-target-s-personalization-algorithms}

CRM 정보나 고객 이탈 성향 점수와 같은 오프라인 데이터는 개인화 모델을 만들 때 매우 소중합니다.

자동화된 개인화(AP)와 자동 타겟 개인화 알고리즘에서 데이터를 입력하는 방법에는 몇 가지가 있습니다. 데이터를 Target로 가져오는 [메서드의 메서드 외에도](../../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17), Experience Cloud 공유 대상 (Adobe Analytics, 고객 관리) 및 활동 내 보고 대상이 알고리즘에서도 사용됩니다.

자동화된 개인화 및 자동 타겟 개인화 알고리즘에서 자동으로 수집 및 사용되는 데이터에 대해서는 [자동화된 개인화 데이터 수집](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058)을 참조하십시오.

## 우수 사례 {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

다음 목록은 Target의 개인화 알고리즘에 대한 데이터를 업로드하는 우수 사례입니다.

* Target의 개인화 알고리즘에 사용할 수 있는 데이터가 고품질일수록 AP 및 자동 Target 활동의 결과 모델 품질이 향상됩니다.
* 동일한 목적을 제공하는 여러 프로필 스크립트 또는 속성 사용을 제한합니다.
* 필요하지 않은 경우 세션 ID와 같은 고유 ID를 전달하지 마십시오.
* Target에서 자동으로 수집하는 데이터를 검토하므로( [Target의 개인화 알고리즘에 대한 데이터 수집](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058)) 중복 정보를 전송할 필요가 없습니다. 예를 들어, Target은 IP 주소를 사용하여 방문자의 우편 번호를 판별합니다. 이 정보를 별도의 변수로 전달하지 않아도 됩니다.
* 동일한 속성/변수에 여러 값을 전달하지 마십시오. 여러 변수가 연결된 경우 Target의 개인화 알고리즘은 각 문자열을 고유 값으로 처리하여 개인화에 대한 정보의 값을 줄입니다.
* 기억하기 쉽고 의미 있는 이름 지정 규칙을 사용하여 [개인화 인사이트 보고서](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767)를 보다 쉽게 구분할 수 있도록 합니다.

