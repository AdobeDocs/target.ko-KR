---
keywords: A/B;활동 지표;지표;지표 설정;목표 지표;활동 설정;성공 지표;전환;매출;참여
description: A/B 활동에서 지표를 설정하여 [!UICONTROL 전환], [!UICONTROL 매출] 및 [!UICONTROL 참여]을(를) 포함하여 방문 성공을 결정하는 방법을 알아봅니다.
title: A/B 활동에서 목표 지표를 설정하려면 어떻게 합니까?
feature: A/B Tests
exl-id: 9e9e8787-c0cd-4aab-bd2d-0e9591e0a07d
TQID: https://experienceleague.adobe.com/WE27AidwrwYLn-ZlnpxKNfOG2jT07iPYztdrovRl0Qk
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 55%

---

# 지표 설정

[!DNL Adobe Target] A/B 활동의 지표를 사용하여 방문이 성공적으로 수행된 시기를 확인합니다.

성공 지표에 대한 자세한 내용은 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)를 참조하십시오.

1. **[!UICONTROL 목표 및 설정]** 페이지의 **[!UICONTROL 보고 설정]** 섹션에서 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)를 선택하십시오.

   [!UICONTROL 지표 선택] 옵션은 활동에 대해 선택할 수 있는 성공 지표를 나열합니다. 성공 지표는 다음 카테고리로 구분됩니다.

   * [!UICONTROL 전환]
   * [!UICONTROL 매출 ]
   * [!UICONTROL 참여]

   사전 빌드된 지표 중 하나를 사용하거나 사용자 지정 성공 지표를 만들 수 있습니다. 성공 지표를 기본 지표로 표시할 수도 있습니다. 기본 측정 항목(설정된 경우)을 표시하려면 Experience Cloud 카드 기본값을 보고합니다.

1. 지표에 대한 설정을 지정합니다.

   사용 가능한 설정은 사용 중인 성공 지표에 따라 다릅니다.

   사용하도록 설정하면 [!UICONTROL 전환 예상 값] 필드([!UICONTROL 페이지 점수] 지표에 사용할 수 없음)가 목표 값을 제공합니다. 이 값을 통해 [!DNL Target]이 예상 매출액 상승도를 계산할 수 있습니다. 이 필드는 선택 사항이지만, 이 필드의 값이 없으면 비매출액 지표의 증분 수익을 계산할 수 없습니다. 데이터 유형은 통화입니다. 이 필드는 사용자가 목표를 충족하기 위해 수행한 작업을 지정한 후에 점진적으로 표시됩니다. 자세한 내용은 [매출 상승도 평가](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오.

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
