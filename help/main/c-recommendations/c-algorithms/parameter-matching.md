---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;프로모션;동적 필터링;동적;매개 변수 일치
description: 항목(엔티티)을 요청(API 또는 mbox)에 있는 값과 비교하여 Adobe [!DNL Target] 권장 사항에서 동적으로 필터링하는 방법을 알아봅니다.
title: 매개 변수 일치
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
TQID: 'https://experienceleague.adobe.com/GTli-O1p4Gm2Fg9J-L0ukQ8dSw2t-da8OatFLP8Ks9g'
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
source-wordcount: '311'
ht-degree: 8%
---
# 매개 변수 일치 {#parameter-matching}

>[!BEGINSHADEBOX]

**이 페이지에서:** 항목(엔터티)을 요청(API 또는 mbox)에 있는 값과 비교하여 [!DNL Adobe Target Recommendations]에서 권장 사항을 동적으로 필터링하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

**[!UICONTROL 매개 변수 일치]**&#x200B;에서는 페이지 매개 변수 또는 방문자의 매개 변수(예: 장치 차원 또는 지리적 위치)와 일치하는 콘텐츠만 권장합니다. 예를 들어 &quot;업계&quot; 페이지 매개 변수와 일치하는 컨텐츠만 추천할 수 있습니다. 기준 및 프로모션에 대한 포함 규칙을 만들고 사용하는 프로세스는 사용 사례 및 예와 비슷합니다. 자세한 내용은 [동적 및 정적 포함 규칙 사용](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)을 참조하세요.

기타 예는 다음과 같습니다.

* 화면 너비 및 높이에 대한 Mbox 매개 변수는 모바일 방문자를 타깃팅하고 모바일 장치 및 액세서리만 권장하는 데 사용할 수 있습니다.
* 권장 사항 규칙은 방문자가 페이지를 보는 데 사용하는 모바일 장치의 화면 높이와 일치하거나 초과하는 최상위 판매 휴대폰만 반환할 수 있습니다.
* 지리적 위치 매개 변수는 겨울 동안 도구에 대한 권장 사항을 반환하는 데 사용할 수 있습니다. 눈이 내리는 지역에는 눈송풍기 및 기타 눈저감구를 방문자에게 추천할 수 있지만 눈이 내리지 않는 지역에는 방문자가 추천하지 않는다.

## 매개 변수 일치 예

[!DNL Recommendations]은(는) [!DNL Target] 호출 시 전송된 매개 변수 값과 일치할 수 있습니다. 다음 예에서 [!DNL Target]은(는) [!DNL Target] 호출에서 전송된 화면 높이 및 너비 매개 변수를 기반으로 방문자가 모바일 장치를 사용하고 있음을 감지하고 모바일 장치인 항목만 추천합니다.

다음 [!DNL Target] 호출 예를 생각해 보십시오.

![대상 호출](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

방문자가 보고 있는 페이지에 모바일 장치 제품이 표시됩니다.

![모바일 장치 제품](/help/main/c-recommendations/c-algorithms/assets/phones.png)
