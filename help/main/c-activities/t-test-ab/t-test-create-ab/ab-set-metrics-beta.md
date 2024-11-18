---
keywords: A/B;활동 지표;지표;지표 설정;목표 지표;활동 설정;성공 지표;전환;매출;참여
description: '[!UICONTROL Conversion], [!UICONTROL Revenue] 및 [!UICONTROL Engagement]을(를) 포함하여 방문 성공을 결정하기 위해 A/B 활동에서 지표를 설정하는 방법에 대해 알아봅니다.'
title: A/B 활동에서 목표 지표를 설정하려면 어떻게 합니까?
feature: A/B Tests
hide: true
hidefromtoc: true
exl-id: b7955ed7-61b4-429f-80ff-8efcafc10542
source-git-commit: d5bd3b0d7cdf6eb06175a6365da6b8173f76800f
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 58%

---

# 지표 설정

[!DNL Adobe Target] A/B 활동의 지표를 사용하여 방문이 성공적으로 수행된 시기를 확인합니다.

성공 지표에 대한 자세한 내용은 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)를 참조하십시오.

1. **[!UICONTROL Goals & Settings]** 페이지의 **[!UICONTROL Reporting Settings]** 섹션에서 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)를 선택합니다.

   [!UICONTROL Select Metrics] 옵션은 활동에 대해 선택할 수 있는 성공 지표를 나열합니다. 성공 지표는 다음 카테고리로 구분됩니다.

   * [!UICONTROL Conversion]
   * [!UICONTROL Revenue]
   * [!UICONTROL Engagement]

   사전 빌드된 지표 중 하나를 사용하거나 사용자 지정 성공 지표를 만들 수 있습니다. 성공 지표를 기본 지표로 표시할 수도 있습니다. 기본 측정 항목(설정된 경우)을 표시하려면 Experience Cloud 카드 기본값을 보고합니다.

1. 지표에 대한 설정을 지정합니다.

   사용 가능한 설정은 사용 중인 성공 지표에 따라 다릅니다.

   사용하도록 설정하면 [!UICONTROL Estimated Value of the Conversion] 필드([!UICONTROL Page Score] 지표에 사용할 수 없음)에 목표 값이 제공됩니다. 이 값을 통해 [!DNL Target]이 예상 매출액 상승도를 계산할 수 있습니다. 이 필드는 선택 사항이지만, 이 필드의 값이 없으면 비매출액 지표의 증분 수익을 계산할 수 없습니다. 데이터 유형은 통화입니다. 이 필드는 사용자가 목표를 충족하기 위해 수행한 작업을 지정한 후에 점진적으로 표시됩니다. 자세한 내용은 [매출 상승도 평가](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오.

   예상한 데이터를 가져오려면 성공 지표를 올바르게 구성해야 합니다.

   자세한 내용은 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)를 참조하십시오.

1. (선택 사항) 추가 지표를 추가합니다.

지표의 이름을 지정하거나 지표의 이름을 바꾸는 경우 다음 문자가 허용되지 않습니다.

| 문자 | 설명 |
|--- |--- |
| / | 슬래시 |
| ? | 물음표 |
| # | 숫자 기호 |
| : | 콜론 |
| = | 다음과 같음 |
| + | 플러스 |
| - | 빼기 |
| @ | 로그인 |
