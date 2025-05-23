---
keywords: 수입 상승도;수입;수입의 상승도 예상;상승도 계산;예상 값
description: 모든 방문자에게 우승 경험이 표시되면, 테스트 도중과 마찬가지로 트렌드가 지속되면 달성할 수 있는 상승도를 예측합니다.
title: 매출 상승도를 어떻게 추정합니까?
feature: Administration & Configuration
role: Admin
exl-id: a3c5e20e-f5d5-4b6f-b169-59d5916584ab
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 85%

---

# 매출 상승도 평가

[!DNL Adobe Target]을(를) 사용하여 모든 사용자가 우승을 경험하는 경우 이루게 되는 매출 상승도를 예측합니다.

>[!NOTE]
>
>현재 [!UICONTROL Experience Targeting] (XT) 활동에는 예상 상승도를 사용할 수 없습니다.

예상 상승도 기능은 기본적으로 꺼져 있으며, 계정 환경 설정에서 활성화할 수 있습니다. Experience Cloud 관리자 사용자만 이 기능을 활성화하거나 비활성화할 수 있습니다. 예상되는 상승도가 비활성화되면 해당 필드가 인터페이스에 표시되지 않습니다. 이 기능을 비활성화해도 예상치에 사용되는 데이터를 비롯한 어떤 데이터도 손실되지 않습니다. 예상치는 기능의 활성화 여부와 관계없이 수집되는 데이터를 기준으로 합니다.

>[!IMPORTANT]
>
>예상 상승도는 추정값일 뿐입니다. 정확도는 현재 트렌드가 계속될 경우에 예측되는 수치를 비롯한 여러 요인에 따라 좌우됩니다. 이러한 값은 이전 성능을 기반으로 하는 예측값이며 재무 지침으로는 사용하지 않아야 합니다. 수치 결과는 다를 수 있습니다.

이러한 예측은 가장 성과가 좋은 경험에 의해 얻는 상승도와 활동 수명 동안 총 방문자 수를 계산하고, 테스트 중에 나타나는 트렌드가 계속된다고 가정할 경우 모든 방문자가 가장 성과가 좋은 경험을 보게 될 때 달성할 수 있는 상승도를 표시합니다.

수입의 예상 상승도는 기본 목표 지표에서 얻은 방문당 매출액(RPV)을 기반으로 계산됩니다.

예상 상승도는 공식 (&lt;우승 경험 RPV> - &lt;제어 경험 RPV>)&#42;&lt;활동의 총 방문자 수>를 사용하여 계산됩니다.

결과는 압축 양식에서 소수 앞에 한자릿수만 있으면 최대 소수 첫째 자리로 반올림됩니다. 예를 들어, $1.6M, $60K, $900, $8.5K, $205K와 같습니다.

예를 들어 가장 성과가 좋은 경험에서 $0.59의 증가를 보이고 통제 경험에서 $0.15의 증가를 보이는 경우 예상에서는 방문자당 $0.44의 증가가 계산됩니다. 방문자가 75,000명인 경우, 모든 방문자가 가장 성과가 좋은 경험을 보고 현재 트렌드가 계속된다면 발생하는 수입 증가는 $33,000가 될 것입니다.

마찬가지로, 가장 성과가 좋은 경험이 통제 경험에 비해 $0.17의 증가를 보이고 테스트 수명 동안 192,000명의 방문자가 있었다면, 현재 트렌드가 계속되는 경우, $32,640의 수입 증가를 예상할 수 있습니다.

다음 상황에서는 수입의 예상 상승도 필드가 &quot;---&quot;으로 표시됩니다.

* 합리적인 예상을 계산할 만큼 방문자가 충분하지 않은 경우
* 지표의 예상 값이 지표 설정 페이지에 제공되지 않은 경우
* 성과가 가장 좋은 경험이 통제 경험인 경우

활동의 목표를 설정할 때에는 예상 값 필드에는 목표 값을 제공합니다. 이 값을 통해 Target이 예상 수입 상승도를 계산할 수 있습니다. 이 필드는 선택 사항이지만, 이 필드의 값이 없으면 비매출액 지표의 증분 수익을 계산할 수 없습니다. 데이터 유형은 통화입니다. 이 필드는 사용자가 목표를 충족하기 위해 수행한 작업을 지정한 후에 점진적으로 표시됩니다.

방문자 100%가 가장 성과가 좋은 경험을 보는 경우 예상 수입은 Target 보고서의 맨 위에 나타납니다.
