---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;동적 필터링;동적 필터링;매개 변수 일치
description: 항목(엔터티)을 요청(API 또는 mbox)의 값과 비교하여 Adobe [!DNL Target] Recommendations에서 동적으로 필터링하는 방법을 알아보십시오.
title: Recommendations 활동에서 매개 변수 일치를 기준으로 필터링하려면 어떻게 합니까?
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 10%

---

# ![PREMIUMParameter ](/help/assets/premium.png) 일치

항목(엔티티)을 요청의 값(API 또는 mbox)과 비교하여 동적으로 필터링합니다.

예를 들어 다음 예와 같이 &quot;업계&quot; 페이지 매개 변수 또는 장치 차원이나 지리적 위치 같은 기타 매개 변수와 일치하는 컨텐츠만 권장합니다.

* 화면 너비 및 높이에 대한 mbox 매개 변수를 사용하여 모바일 방문자를 타깃팅하고 모바일 장치 및 액세서리만 권장할 수 있습니다.
* 방문자가 페이지 보기를 사용하는 모바일 장치의 화면 높이와 일치하거나 초과하는 최상위 판매 휴대 전화만 반환하는 추천 규칙을 만듭니다.
* 겨울에 도구에 대한 권장 사항을 반환하는 데 지역 위치 매개 변수를 사용할 수 있습니다. 눈이 내리지 않는 지역은 눈이 내리는 곳으로, 눈이 내리지 않는 곳에서는 눈이 내리는 곳을 추천하지 않는다.

>[!NOTE]
>
>2016년 10월 31일 이전에 활동이 만들어지면 &quot;매개 변수 일치&quot; 필터를 사용하는 경우 활동이 배달되지 않습니다. 이 문제를 해결하려면 다음을 수행하십시오.
>
>* 새 활동을 만들고 이 활동에서 기준을 추가합니다.
>* &quot;매개 변수 일치&quot; 필터가 들어 있지 않은 기준을 사용합니다.
>* 기준에서 &quot;매개 변수 일치&quot; 필터를 제거합니다.


## 매개 변수 일치 예

[!UICONTROL 매개 변수 ] 일치를 사용하면 다음 예제와 같이 페이지 매개 변수 또는 장치 차원이나 지리적 위치와 같은 방문자의 매개 변수와 일치하는 컨텐트를 권장할 수 있습니다.

[!DNL Recommendations] 호출에서 전송된 매개 변수 값과 일치시킬 수  [!DNL Target] 있습니다. 이 경우 [!DNL Target]은(는) [!DNL Target] 호출에서 전송된 화면 높이 및 너비 매개 변수를 기준으로 방문자가 모바일 장치를 사용하고 있음을 감지하고 모바일 장치인 항목만 권장합니다.

다음 Target 호출 예를 생각해 보십시오.

![Target 전화](/help/c-recommendations/c-algorithms/assets/example-target-call-2.png)

방문자가 보는 페이지에서 모바일 장치 제품이 표시됩니다.

![모바일 디바이스 제품](/help/c-recommendations/c-algorithms/assets/phones.png)
