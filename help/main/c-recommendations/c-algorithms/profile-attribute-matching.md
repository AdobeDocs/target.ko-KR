---
keywords: 포함 규칙;포함 기준;권장 사항;프로모션;프로모션;동적 필터링;동적;프로필 속성 일치
description: Adobe에서 동적으로 필터링하는 방법 알아보기 [!DNL Target] Recommendations에서 항목(엔티티)을 사용자 프로필에 있는 값과 비교하여 확인합니다.
title: Recommendations 활동에서 프로필 속성 일치별로 필터링하려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: d4b837af-771b-41b4-982b-f9f08e4753f2
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 7%

---

# 프로필 속성 일치

에서 동적으로 필터링 [!DNL Adobe Target] [!DNL Recommendations] 항목(엔티티)을 사용자 프로필에 있는 값과 비교하여 확인합니다.

사용 [!UICONTROL 프로필 속성 일치] 크기 또는 즐겨찾는 브랜드 같이 방문자 프로필에 저장된 값과 일치하는 권장 사항을 표시하려는 경우.

>[!NOTE]
>
>다음 [포함 규칙 만들기 및 사용 프로세스](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) 기준 및 프로모션의 경우 활용 사례 및 예와 유사합니다.

다음 시나리오는 사용 방법을 보여줍니다 [!UICONTROL 프로필 속성 일치]:

* 안경을 판매하는 한 회사는 방문객이 가장 좋아하는 프레임 색상을 호두라고 저장한다. 특정 방문자의 경우 &quot;호두&quot; 색상에 일치하는 안경테만 반환하도록 권장 사항이 설정됩니다.
* 프로필 매개 변수는 회사의 웹 사이트를 탐색할 때 방문자의 의류 크기(예: Small, Medium 또는 Large)에 대해 정의할 수 있습니다. 해당 프로필 매개 변수와 일치하도록 권장 사항을 설정하고 사용자의 선호 의류 크기만 기준으로 하는 제품을 반환할 수 있습니다.

## 프로필 속성 일치 예 {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL 프로필 속성 일치] 아래 예와 같이 방문자 프로필의 속성과 일치하는 항목만 추천할 수 있습니다.

### 사용자가 자주 사용하는 브랜드에서 항목 추천

예를 들어 [!UICONTROL 프로필 속성 일치] 브랜드가 저장된 값 또는 텍스트와 같은 항목만을 추천하는 규칙을 만드는 옵션 `profile.favoritebrand`. 이러한 규칙을 사용할 때, 방문자가 특정 브랜드의 육상용 반바지를 보고 있다면 해당 사용자가 자주 이용하는 브랜드(방문자 프로필의 `profile.favoritebrand`에 저장된 값)와 일치하는 권장 사항만 표시됩니다.

![즐겨찾는 브랜드](/help/main/c-recommendations/c-algorithms/assets/favorite-brand.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### 구직자와 일자리 일치

구직자들과 직업을 일치시키려고 한다고 가정해. 구직자와 동일한 도시에 있는 일자리만 추천하고 싶습니다.

다음 예와 같이 포함 규칙을 사용하여 방문자 프로필의 작업 위치를 작업 목록에 일치시킬 수 있습니다.

![사용자 구/군/시](/help/main/c-recommendations/c-algorithms/assets/city.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### 크기에 따라 항목 추천

프로필 속성 일치가 권장 사항에 영향을 주는 방법에 대한 시각적 예를 보려면 전기 팬을 판매하는 웹 사이트를 생각해 보십시오.

방문자가 이 웹 사이트에서 다양한 팬의 이미지를 클릭하면 각 페이지는 `entity.size` 이미지의 팬 크기가 작은지 또는 크지를 기준으로 하는 매개 변수입니다.

프로필 스크립트를 만들어 값 추적 및 계산 `entity.size` 은 작음 대 큼으로 설정되어 있습니다.

그런 다음 방문자가 홈 페이지로 돌아오면 작은 팬이나 큰 팬을 클릭했는지 여부에 따라 필터링된 권장 사항이 표시됩니다.

Recommendations은 웹 사이트에서 더 작은 팬을 보는 기반:

![작은 팬 권장 사항](/help/main/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations은 웹 사이트에서 더 많은 대형 팬을 보는 기반:

![대형 팬 권장 사항](/help/main/c-recommendations/c-algorithms/assets/large-fans.png)
