---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;프로모션;동적 필터링;동적;프로필 속성 일치
description: Adobe에서 동적으로 필터링하는 방법 알아보기 [!DNL Target] 항목(엔티티)을 사용자 프로필에 있는 값과 비교하여 Recommendations을 작성합니다.
title: Recommendations 활동에서 프로필 속성 일치로 필터링하려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 7%

---

# 프로필 속성 일치

에서 동적으로 필터링 [!DNL Adobe Target] [!DNL Recommendations] 항목(엔티티)을 사용자 프로필에 있는 값과 비교

사용 [!UICONTROL 프로필 속성 일치] 크기 또는 즐겨찾기 브랜드와 같이 방문자의 프로필에 저장된 값과 일치하는 권장 사항을 표시하려는 경우.

>[!NOTE]
>
>다음 [포함 규칙 만들기 및 사용 프로세스](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) 기준 및 프로모션의 경우 사용 사례 및 예제와 유사합니다.

다음 시나리오는 를 사용하는 방법을 보여 줍니다 [!UICONTROL 프로필 속성 일치]:

* 안경을 판매하는 한 회사는 방문자가 가장 좋아하는 프레임 색상을 &#39;호두&#39;로 저장한다. 특정 방문자의 경우 &quot;호두&quot;와 색상이 일치하는 안경 프레임만 반환하도록 권장 사항이 설정됩니다.
* 방문자가 회사 웹 사이트를 탐색할 때 방문자의 의류 크기(예: Small, Medium 또는 Large)에 대해 프로필 매개 변수를 정의할 수 있습니다. 해당 프로필 매개 변수와 일치하도록 권장 사항을 설정하고 사용자가 선호하는 의류 크기에만 해당하는 제품을 반환할 수 있습니다.

## 프로필 속성 일치 예 {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL 프로필 속성 일치] 에서는 아래 예제와 같이 방문자 프로필의 속성과 일치하는 항목만 추천할 수 있습니다.

### 사용자가 선호하는 브랜드의 항목 추천

예를 들어 [!UICONTROL 프로필 속성 일치] 브랜드가 저장된 값 또는 텍스트와 같은 항목만 추천하는 규칙을 만드는 옵션 `profile.favoritebrand`. 이러한 규칙을 사용할 때, 방문자가 특정 브랜드의 육상용 반바지를 보고 있다면 해당 사용자가 자주 이용하는 브랜드(방문자 프로필의 `profile.favoritebrand`에 저장된 값)와 일치하는 권장 사항만 표시됩니다.

![즐겨 찾는 브랜드](/help/main/c-recommendations/c-algorithms/assets/favorite-brand.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### 구직자에 대한 Job 대응

직업을 구직자와 일치시키려고 한다고 가정해 보자. 구직자와 같은 도시에 있는 직업만 추천하고 싶을 것이다.

다음 예제와 같이 포함 규칙을 사용하여 구직자의 방문자 프로필에서 Job 목록에 있는 위치를 일치시킬 수 있습니다.

![사용자의 도시](/help/main/c-recommendations/c-algorithms/assets/city.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### 크기에 따라 항목 추천

프로필 속성 일치가 권장 사항에 미치는 영향에 대한 시각적 예제를 보려면 선풍기를 판매하는 웹 사이트를 고려하십시오.

방문자가 이 웹 사이트에서 다양한 팬 이미지를 클릭하면 각 페이지는 의 값을 설정합니다. `entity.size` 이미지에서 팬 크기가 작은지 아니면 큰지를 기반으로 한 매개 변수입니다.

값 횟수를 추적하고 카운트하는 프로필 스크립트를 만들었다고 가정해 봅시다. `entity.size` 는 작은 크기와 큰 크기로 설정되어 있습니다.

방문자가 홈 페이지로 돌아오면 더 많은 작은 팬 또는 큰 팬을 클릭했는지 여부에 따라 필터링된 권장 사항이 표시됩니다.

Recommendations은 웹 사이트에서 더 많은 작은 팬을 보는 것을 기반으로 합니다.

![소규모 팬 추천](/help/main/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations은 웹 사이트에서 더 많은 대형 팬을 보는 것을 기반으로 합니다.

![대규모 팬 추천](/help/main/c-recommendations/c-algorithms/assets/large-fans.png)
