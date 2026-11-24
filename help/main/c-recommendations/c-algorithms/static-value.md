---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;프로모션;동적 필터링;정적;정적 필터
description: Adobe [!DNL Target] 권장 사항에서 포함 규칙을 사용하여 필터링할 하나 이상의 정적 값을 수동으로 입력하는 방법을 알아봅니다.
title: 정적 필터
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 217e19bf-521f-4913-9b41-099c9af8b393
TQID: 'https://experienceleague.adobe.com/-HTJO4YFi0-isyA-5LbVUaEPu7YX1WFgPy-OexMSXFY'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%
---
# 정적 필터 {#static-filter}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Adobe Target Recommendations]의 포함 규칙에 하나 이상의 정적 값을 수동으로 입력하여 권장 사항을 필터링하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

**[!UICONTROL 정적 필터]**&#x200B;은(는) 권장 사항의 항목을 수동으로 입력한 정적 값과 일치하는 항목으로 제한합니다. 원하는 수만큼 포함 규칙을 만들 수 있습니다. 포함 규칙은 AND 연산자로 결합되므로 항목이 권장 사항에 포함되려면 모든 규칙이 충족되어야 합니다. 포함 규칙에 대한 일반적인 정보는 [동적 및 정적 포함 규칙 사용](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)을 참조하십시오.

## G 또는 PG 등급의 콘텐츠 추천

MPA(영화 협회) 등급이 &quot;G&quot; 또는 &quot;PG&quot;인 콘텐츠만 추천하려면(&quot;R&quot; 및 &quot;NC17&quot; 콘텐츠 제외), &quot;movie-rating equals any of&quot; 연산자로 필터링 규칙 하나를 만들고, &quot;g-rated&quot; 및 &quot;pg-rated&quot; 값을 입력합니다.
