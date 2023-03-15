---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;프로모션;동적 필터링;동적;매개 변수 일치
description: Adobe에서 동적으로 필터링하는 방법 알아보기 [!DNL Target] Recommendations에서 항목(엔티티)을 요청(API 또는 mbox)에 있는 값과 비교하여 확인합니다.
title: Recommendations 활동에서 매개 변수 일치로 필터링하려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 9ec161b9-1b37-4475-b508-af676126c817
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 10%

---

# 매개 변수 일치

항목(엔티티)을 요청(API 또는 mbox)에 있는 값과 비교하여 동적으로 필터링합니다.

예를 들어 다음 예와 같이, &quot;업계&quot; 페이지 매개 변수 또는 장치 차원이나 지리적 위치와 같은 기타 매개 변수와 일치하는 컨텐츠만 추천합니다.

* 화면 너비와 높이에 대한 mbox 매개 변수는 모바일 방문자를 타깃팅하고 모바일 장치 및 액세서리만 추천하는 데 사용할 수 있습니다.
* 방문자가 페이지 보기를 사용하는 모바일 장치의 화면 높이와 일치하거나 초과하는 최상위 판매 휴대폰만 반환하는 권장 사항 규칙을 만듭니다.
* 지역 위치 매개 변수를 사용하여 겨울 동안 도구에 대한 권장 사항을 반환할 수 있습니다. 눈이 내리지 않는 지역은 눈이 내리지 않고 눈이 내리는 곳으로 손님을 안내한다.

>[!NOTE]
>
>활동이 2016년 10월 31일 이전에 만들어진 경우 &quot;매개 변수 일치&quot; 필터를 사용하면 전달이 실패합니다. 이 문제를 해결하려면 다음을 수행하십시오.
>
>* 새 활동을 만들고 이 활동에서 기준을 추가합니다.
>* &quot;매개 변수 일치&quot; 필터가 들어 있지 않은 기준을 사용합니다.
>* 기준에서 &quot;매개 변수 일치&quot; 필터를 제거합니다.


## 매개 변수 일치 예

[!UICONTROL 매개 변수 일치] 다음 예와 같이 페이지 매개 변수 또는 장치 차원이나 지리적 위치와 같은 방문자의 매개 변수와 일치하는 컨텐츠를 추천할 수 있습니다.

[!DNL Recommendations] 에서 전송된 매개 변수 값과 일치시킬 수 있습니다. [!DNL Target] 호출. 이 경우 [!DNL Target] 에서는 방문자가 [!DNL Target] 및 은 를 호출하고 모바일 장치인 항목만 추천합니다.

다음 Target 호출 예를 생각해 보십시오.

![Target 호출](/help/main/c-recommendations/c-algorithms/assets/example-target-call-2.png)

방문자가 보고 있는 페이지에는 모바일 장치 제품이 표시됩니다.

![모바일 장치 제품](/help/main/c-recommendations/c-algorithms/assets/phones.png)
