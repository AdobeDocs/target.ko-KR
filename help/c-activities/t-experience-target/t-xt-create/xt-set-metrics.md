---
keywords: 경험 타깃팅;xt;지표;지표 설정;목표 지표;활동 설정;성공 지표;전환;매출;참여
description: Adobe Target Experience Targeting 활동에서 지표를 지정하여 전환, 매출 및 참여와 같은 성공적인 방문 시기를 결정하는 방법에 대해 학습합니다.
title: 경험 타깃팅 활동에서 목표 지표를 설정하려면 어떻게 합니까?
feature: Experience Targeting
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 80%

---


# 경험 타깃팅(XT) 활동에서 지표 설정

[!DNL Adobe Target] [!UICONTROL 경험 타깃팅](XT) 활동에서 지표를 사용하여 방문이 성공했는지 여부를 결정할 수 있습니다.

성공 지표에 대한 자세한 내용은 [성공 지표](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)를 참조하십시오.

1. 활동의 목표를 지정합니다.
1. [성공 지표](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)를 선택합니다.

   ![성공 지표 선택](/help/c-activities/t-experience-target/t-xt-create/assets/ab_metrics-new.png)

   [!UICONTROL 지표 선택] 페이지에는 활동에 대해 선택할 수 있는 성공 지표가 표시됩니다. 성공 지표는 다음 카테고리로 구분됩니다.

   * 변환
   * 수입
   * 참여

   사전 빌드된 지표 중 하나를 사용하거나 사용자 지정 성공 지표를 만들 수 있습니다. 성공 지표를 기본 지표로 표시할 수도 있습니다. 기본 측정 항목(설정된 경우)을 표시하려면 Experience Cloud 카드 기본값을 보고합니다.
1. 지표에 대한 설정을 지정합니다.

   사용 가능한 설정은 사용 중인 성공 지표에 따라 다릅니다.

   [!UICONTROL 전환 예상값] 필드가 활성화되어 있으면(페이지 점수 지표에는 사용할 수 없음) 목표값이 표시됩니다. 이 값을 통해 Target이 예상 매출액 상승도를 계산할 수 있습니다. 이 필드는 선택 사항이지만, 이 필드의 값이 없으면 비매출액 지표의 증분 수익을 계산할 수 없습니다. 데이터 유형은 통화입니다. 이 필드는 사용자가 목표를 충족하기 위해 수행한 작업을 지정한 후에 점진적으로 표시됩니다. 자세한 내용은 [매출 상승도 평가](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오.

   예상한 데이터를 가져오기 위해서는 성공 지표를 올바르게 구성해야 합니다.

   자세한 내용은 [성공 지표](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)를 참조하십시오.
1. (선택 사항) 추가 지표를 추가합니다.
1. 지표 설정이 끝나면 **[!UICONTROL 계속]**을 클릭합니다.
이름을 지정하거나 지표의 이름을 바꾸는 경우 다음 문자가 허용되지 않습니다.

   | 문자 | 설명 |
   |--- |--- |
   | `/` | 슬래시 |
   | `?` | 물음표 |
   | `#` | 숫자 기호 |
   | `:` | 콜론 |
   | `=` | 다음과 같음 |
   | `+` | 플러스 |
   | `-` | 빼기 |
   | `@` | 로그인 |

## 교육 비디오: 활동 지표(7:43)  ![자습서 배지](/help/assets/tutorial.png)


이 비디오에는 성공 지표 사용에 대한 정보가 포함되어 있습니다.

* &quot;목표&quot; 지표 이해
* 변환, 수입 및 참여 지표 이해 및 빌드
* 클릭 추적 지표 빌드

>[!VIDEO](https://video.tv.adobe.com/v/17380)
