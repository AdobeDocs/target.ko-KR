---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;parameter matching
description: 항목(엔티티)을 요청의 값(API 또는 mbox)과 비교하여 Adobe Target Recommendations에서 동적으로 필터링합니다.
title: Adobe Target Recommendations의 동적 포함 규칙의 매개 변수 일치별 필터링
feature: criteria
translation-type: tm+mt
source-git-commit: c814215476ef6e40f4f175fe3f9dbb2c26b966eb
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 10%

---


# ![PREMIUM](/help/assets/premium.png) 매개 변수 일치

요청(API 또는 mbox)의 값과 항목(엔티티)을 비교하여 동적으로 필터링합니다.

예를 들어 다음 예와 같이 &quot;업계&quot; 페이지 매개 변수 또는 장치 차원이나 지리적 위치 같은 기타 매개 변수와 일치하는 컨텐츠만 권장합니다.

* 화면 너비 및 높이에 대한 Mbox 매개 변수를 사용하여 모바일 방문자를 타깃팅하고 모바일 장치 및 액세서리만을 권장할 수 있습니다.
* 방문자가 페이지 보기를 사용하는 모바일 장치의 화면 높이와 일치하거나 초과하는 최상위 판매 휴대폰만 반환하는 추천 규칙을 만듭니다.
* 지역 위치 매개 변수를 사용하여 겨울 동안 도구에 대한 권장 사항을 반환할 수 있습니다. 눈이 내리지 않는 지역은 눈이 내리는 곳으로 안내하는 눈이 내리는 사람을 미리 안내하는 것도 좋다.

>[!NOTE]
>
>2016년 10월 31일 이전에 활동이 생성된 경우 &quot;매개 변수 일치&quot; 필터를 사용하는 경우 활동이 배달되지 않습니다. 이 문제를 해결하려면 다음을 수행하십시오.
>
>* 새 활동을 만들고 이 활동에서 기준을 추가합니다.
>* &quot;매개 변수 일치&quot; 필터가 들어 있지 않은 기준을 사용합니다.
>* 기준에서 &quot;매개 변수 일치&quot; 필터를 제거합니다.


## 매개 변수 일치 예

[!UICONTROL 매개 변수 일치를] 사용하면 다음 예제와 같이 페이지 매개 변수 또는 방문자의 매개 변수(예: 장치 차원 또는 지리적 위치)와 일치하는 컨텐트를 권장할 수 있습니다.

[!DNL Recommendations] 호출에서 전송된 매개 변수 값과 일치시킬 수 [!DNL Target] 있습니다. 이 경우, 방문자가 통화 중에 전송된 화면 높이 및 너비 매개 변수를 기준으로 모바일 장치를 사용하고 있음을 [!DNL Target] 감지하고 [!DNL Target] 모바일 장치인 항목만 권장합니다.

다음 Target 호출을 고려하십시오.

![Target 전화](/help/c-recommendations/c-algorithms/assets/example-target-call-2.png)

방문자가 보는 페이지에서 모바일 장치 제품이 표시됩니다.

![모바일 디바이스 제품](/help/c-recommendations/c-algorithms/assets/phones.png)
