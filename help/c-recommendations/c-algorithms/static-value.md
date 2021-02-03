---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;동적 필터링;정적 필터;포함 규칙;포함 기준;권장 사항;promotion;promotion;promotions;dynamic filtering;static filter
description: Adobe Target Recommendations의 포함 규칙을 사용하여 필터링할 정적 값을 하나 이상 수동으로 입력합니다.
title: Adobe Target Recommendations의 포함 규칙에 있는 정적 값별로 필터링
feature: Recommendations
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 46%

---


# ![](/help/assets/premium.png) 자동 필터

[!DNL Adobe Target] [!DNL Recommendations]의 포함 규칙을 사용하여 필터링할 정적 값을 수동으로 하나 이상 입력합니다.

예를 들어 MPA(Motion Picture Association) 등급이 &quot;G&quot; 또는 &quot;PG&quot;인 컨텐츠만 권장합니다.

포함 규칙을 필요한 만큼 만들 수 있습니다. 포함 규칙들은 AND 연산자로 결합됩니다. 권장 사항에 항목을 포함하려면 모든 규칙을 충족해야 합니다.

>[!NOTE]
>
>Target 17.6.1 릴리스(2017년 6월) 이전에 포함 규칙이 구성되는 방식을 잘 알고 있다면, 일부 선택 사항과 연산자가 변경되었음을 알 수 있을 것입니다. 선택한 선택 사항에 적용 가능한 연산자만 표시되고, 일부 연산자의 이름은 더 일관되고 직관적이게 변경되었습니다(&quot;일치&quot;(matches)는 이제 &quot;다음과 같음&quot;(equals)임). 이 릴리스 이전에 만들어진 모든 기존 제외 규칙은 새 구조로 자동 마이그레이션됩니다. 여러분 쪽에서는 구조를 조정할 필요가 없습니다.

## G 또는 PG 등급 콘텐츠 추천

MPA 등급이 &quot;G&quot; 또는 &quot;PG&quot;인 컨텐츠만 권장하기 위해 정적 값이 포함된 포함 규칙을 만들려면(&quot;R&quot; 및 &quot;NC17&quot; 콘텐츠 제외), 아래에서 보듯이 동영상 등급 같음 &quot;g 등급&quot; 및 &quot;동영상 등급 같음 pg 등급&quot; 필터링 규칙을 만들 수 있습니다.

![동영상 등급 예](/help/c-recommendations/c-algorithms/assets/movies.png)

