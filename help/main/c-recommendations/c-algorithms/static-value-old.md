---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;프로모션;동적 필터링;정적;정적 필터
description: Adobe [!DNL Target] 권장 사항에서 포함 규칙을 사용하여 필터링할 하나 이상의 정적 값을 수동으로 입력하는 방법을 알아봅니다.
title: 권장 사항 활동에서 정적 값을 기준으로 필터링하려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 217e19bf-521f-4913-9b41-099c9af8b393
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 45%

---

# 정적 필터

[!DNL Adobe Target] [!DNL Recommendations]에서 포함 규칙을 사용하여 필터링할 정적 값을 하나 이상 수동으로 입력하십시오.

예를 들어 MPA(영화 협회) 등급이 &quot;G&quot; 또는 &quot;PG&quot;인 컨텐츠만 추천합니다.

포함 규칙을 필요한 만큼 만들 수 있습니다. 포함 규칙들은 AND 연산자로 결합됩니다. 권장 사항에 항목을 포함하려면 모든 규칙을 충족해야 합니다.

>[!NOTE]
>
>Target 17.6.1 릴리스(2017년 6월) 이전에 포함 규칙이 구성되는 방식을 잘 알고 있다면, 일부 선택 사항과 연산자가 변경되었음을 알 수 있을 것입니다. 선택한 선택 사항에 적용 가능한 연산자만 표시되고, 일부 연산자의 이름은 더 일관되고 직관적이게 변경되었습니다(&quot;일치&quot;(matches)는 이제 &quot;다음과 같음&quot;(equals)임). 이번 릴리스 이전에 만들어진 모든 기존 제외 규칙은 새 구조로 자동 마이그레이션됩니다. 여러분 쪽에서는 구조를 조정할 필요가 없습니다.

## G 또는 PG 등급의 콘텐츠 추천

정적 값으로 포함 규칙을 만들어 MPA 등급이 &quot;G&quot; 또는 &quot;PG&quot;인 콘텐츠만 추천하도록 하려면(&quot;R&quot; 및 &quot;NC17&quot; 콘텐츠 제외), 아래와 같이 &quot;동영상 등급이 g 등급&quot;과 &quot;동영상 등급이 pg 등급&quot;인 다음 필터링 규칙을 만들 수 있습니다.

![동영상 등급 예제](/help/main/c-recommendations/c-algorithms/assets/movies.png)
