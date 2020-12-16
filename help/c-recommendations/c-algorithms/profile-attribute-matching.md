---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;profile attribute matching
description: 항목(엔티티)을 사용자 프로필의 값과 비교하여 Adobe Target Recommendations에서 동적으로 필터링합니다.
title: Adobe Target Recommendations의 동적 포함 규칙에서 프로필 속성 일치별 필터링
feature: criteria
translation-type: tm+mt
source-git-commit: 60b71c426b61bb16a23976da9a03926f8e73cf6c
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 7%

---


# ![PREMIUMProfile 속성 ](/help/assets/premium.png) 일치

항목(엔티티)을 사용자 프로필의 값과 비교하여 [!DNL Adobe Target] [!DNL Recommendations]에서 동적으로 필터링합니다.

크기 또는 즐겨찾기 브랜드와 같이 방문자의 프로필에 저장된 값과 일치하는 권장 사항을 표시하려면 [!UICONTROL 프로필 속성 일치]를 사용합니다.

>[!NOTE]
>
>기준 및 판촉 행사에 대한 포함 규칙](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)을 만들고 사용하는 [프로세스는 사용 사례 및 예와 유사합니다.

다음 시나리오에서는 [!UICONTROL 프로필 속성 일치]를 사용할 수 있는 방법을 보여줍니다.

* 안경을 판매하는 회사는 방문객이 가장 좋아하는 프레임 색상을 호두라고 저장합니다. 특정 방문자의 경우 &quot;호두&quot; 색상에 일치하는 안경 프레임만 반환하도록 권장 사항이 설정됩니다.
* 프로필 매개 변수는 회사의 웹 사이트를 탐색할 때 방문자의 옷 크기(예: 중소기업, 중간 또는 큼)에 대해 정의할 수 있습니다. 해당 프로필 매개 변수와 일치하도록 권장 사항을 설정하고 사용자가 선호하는 의류 크기만 기준으로 제품에 해당하는 제품을 반환합니다.

## 프로필 속성 일치 예 {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL 프로필 속성 ] 일치에서는 아래 예와 같이 방문자 프로필의 속성과 일치하는 항목만 권장할 수 있습니다.

### 사용자가 좋아하는 브랜드의 항목 추천

예를 들어 [!UICONTROL 프로필 속성 일치] 옵션을 사용하여 브랜드가 `profile.favoritebrand`에 저장된 값 또는 텍스트와 같은 경우에만 항목을 추천하는 규칙을 만들 수 있습니다. 이러한 규칙을 사용할 때, 방문자가 특정 브랜드의 육상용 반바지를 보고 있다면 해당 사용자가 자주 이용하는 브랜드(방문자 프로필의 `profile.favoritebrand`에 저장된 값)와 일치하는 권장 사항만 표시됩니다.

![즐겨찾기 브랜드](/help/c-recommendations/c-algorithms/assets/favorite-brand.png)

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### 구직자와 작업 일치

구직자들과 직업을 일치시키려고 한다고 가정해. 구직자와 같은 도시에 있는 일자리만 추천하고 싶으세요.

다음 예제와 같이 포함 규칙을 사용하여 Job Seeker의 위치를 방문자의 프로필에서 Job 목록에 일치시킬 수 있습니다.

![사용자 구/군/시](/help/c-recommendations/c-algorithms/assets/city.png)

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### 크기에 따라 항목 추천

프로필 속성 일치가 추천에 영향을 주는 방법에 대한 시각적 예를 보려면 전기 팬을 판매하는 웹 사이트를 고려하십시오.

방문자가 이 웹 사이트에서 팬의 다양한 이미지를 클릭하면 각 페이지는 이미지의 팬 크기가 작은지 또는 크지를 기준으로 `entity.size` 매개 변수의 값을 설정합니다.

프로필 스크립트를 만들어 `entity.size` 값이 작음 대 큼으로 설정된 횟수를 추적하고 카운트한다고 가정합니다.

그런 다음 방문자가 홈 페이지로 돌아오는 경우 더 많은 소규모 팬이나 큰 팬이 클릭되었는지 여부를 기준으로 필터링된 권장 사항을 볼 수 있습니다.

웹 사이트에서 더 많은 작은 팬을 보는 것에 기반한 Recommendations:

![소규모 팬 추천](/help/c-recommendations/c-algorithms/assets/small-fans.png)

웹 사이트에서 더 많은 팬을 보는 방법에 기반한 Recommendations:

![대형 팬 추천](/help/c-recommendations/c-algorithms/assets/large-fans.png)