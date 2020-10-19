---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;parameter matching
description: 항목(엔티티)을 요청의 값(API 또는 mbox)과 비교하여 Adobe Target Recommendations에서 동적으로 필터링합니다.
title: Adobe Target Recommendations의 동적 포함 규칙의 매개 변수 일치별 필터링
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 27%

---


# ![PREMIUM](/help/assets/premium.png) 매개 변수 일치

요청(API 또는 mbox)의 값과 항목(엔티티)을 비교하여 동적으로 필터링합니다.

예를 들어 다음 예와 같이 &quot;업계&quot; 페이지 매개 변수 또는 장치 차원이나 지리적 위치 같은 기타 매개 변수와 일치하는 컨텐츠만 권장합니다.

* 화면 너비 및 높이에 대한 Mbox 매개 변수를 사용하여 모바일 방문자를 타깃팅하고 모바일 장치 및 액세서리만을 권장할 수 있습니다.
* 지역 위치 매개 변수를 사용하여 겨울 동안 도구에 대한 권장 사항을 반환할 수 있습니다. 눈이 내리지 않는 지역은 눈이 내리는 곳으로 안내하는 눈이 내리는 사람을 미리 안내하는 것도 좋다.

>[!NOTE]
>
>2016년 10월 31일 이전에 활동이 생성된 경우 &quot;매개 변수 일치&quot; 필터를 사용하는 경우 활동이 배달되지 않습니다. 이 문제를 해결하려면 다음을 수행하십시오.
>
>* 새 활동을 만들고 이 활동에서 기준을 추가합니다.
>* &quot;매개 변수 일치&quot; 필터가 들어 있지 않은 기준을 사용합니다.
>* 기준에서 &quot;매개 변수 일치&quot; 필터를 제거합니다.


사용 가능한 연산자:

* equals
* 다음과 같지 않음
* 다음 포함
* 다음을 포함하지 않음
* 다음으로 시작
* 다음으로 끝남
* 다음보다 크거나 같음
* 다음보다 작거나 같음
* 다음 사이