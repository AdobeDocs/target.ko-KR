---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;dynamic;profile attribute matching
description: 사용자 프로필의 값과 항목(엔티티)을 비교하여 Adobe Target Recommendations에서 동적으로 필터링합니다.
title: Adobe Target Recommendations의 동적 포함 규칙에서 프로필 속성별 필터링
feature: criteria
translation-type: tm+mt
source-git-commit: c814215476ef6e40f4f175fe3f9dbb2c26b966eb
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 5%

---


# ![PREMIUM](/help/assets/premium.png) 프로필 속성 일치

항목(엔티티)과 사용자 프로필 [!DNL Adobe Target] [!DNL Recommendations] 의 값을 비교하여 동적으로 필터링합니다.

크기 또는 [!UICONTROL 즐겨찾기] 브랜드와 같이 방문자의 프로필에 저장된 값과 일치하는 권장 사항을 표시하려면 프로필 속성 일치를 사용합니다.

>[!NOTE]
>
>The [process for creating and using inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) for criteria and promotions is similar, as are the use cases and examples.

다음 시나리오에서는 프로필 속성 일치를 사용할 수 [!UICONTROL 있는 방법을 보여줍니다].

* 안경을 판매하는 회사는 방문객이 가장 좋아하는 프레임 색상을 호두라고 저장합니다. 특정 방문자의 경우 &quot;호두&quot; 색상에 일치하는 안경 프레임만 반환하도록 권장 사항이 설정됩니다.
* 프로필 매개 변수는 방문자가 회사의 웹 사이트를 탐색할 때 방문자의 옷 크기(예: 작은, 보통 또는 큰)에 대해 정의할 수 있습니다. 해당 프로필 매개 변수와 일치하도록 권장 사항을 설정하고 사용자가 선호하는 옷 크기에만 해당하는 제품을 반환합니다.

## 프로필 속성 일치 예 {#section_9873E2F22E094E479569D05AD5BB1D40}

[!UICONTROL 프로필 속성 일치를] 사용하면 아래 예와 같이 방문자 프로필의 속성과 일치하는 항목만 권장할 수 있습니다.

### 사용자가 좋아하는 브랜드의 항목 추천

For example, you can use the [!UICONTROL Profile Attribute Matching] option to create a rule that recommends items only where the brand equals the value or text stored in `profile.favoritebrand`. 이러한 규칙을 사용할 때, 방문자가 특정 브랜드의 육상용 반바지를 보고 있다면 해당 사용자가 자주 이용하는 브랜드(방문자 프로필의 `profile.favoritebrand`에 저장된 값)와 일치하는 권장 사항만 표시됩니다.

```
Profile Attribute Matching
brand - equals - the value/text stored in - profile.favoritebrand
```

### 구직자와 직장 일치

구직자들과 일자리를 맞추기 위해 노력한다고 가정합시다. 구직자와 같은 도시에 있는 일자리만 추천하고 싶은 것이다.

다음 예와 같이 포함 규칙을 사용하여 구직 방문자의 프로필에서 직무 목록까지의 위치를 일치시킬 수 있습니다.

```
Profile Attribute Matching
jobCity - equals - the value/text stored in - profile.usersCity
```

### 방문자의 크기와 일치하는 옷 추천

예를 들어 방문자 프로필에 설정된 옷 크기와 일치하는 옷을 추천합니다.

제품 페이지는 mbox 호출 `entity.size` 을 전송합니다(아래 그림에서 빨간색 화살표).

방문자가 방문한 마지막 페이지에서 [프로필](/help/c-target/c-visitor-profile/profile-parameters.md) 속성과 값을 캡처하는 프로필 스크립트를 만들 수 있습니다.

예:

```
if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'small')) { return 'small';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'medium')) { return 'medium';
}

else if ((mbox.name=="target-global-mbox") &&(mbox.param('entity.size') == 'large')) { return 'large';
}
```

프로필 스크립트는 이름이 지정된 mbox의 `entity.size` 값을 캡처하고 이 값 `target-global-mbox` 을 프로필 속성 `user.size` (아래 그림에서 파란색 화살표)으로 반환합니다.

![mbox 호출 크기](/help/c-recommendations/c-algorithms/assets/size.png)

권장 사항 기준을 만들 때 필터링 규칙 **[!UICONTROL 추가를]**&#x200B;클릭한 다음 **[!UICONTROL 프로필 속성 일치를 선택합니다]**.

![프로필 속성 일치 일러스트레이션](/help/c-recommendations/c-algorithms/assets/profile-attribute-matching.png)

프로필을 불러온 `user.size` 경우 mbox 호출( [!DNL Target])에서 프로필 스크립트 이름(`size``user.size`)에 전달된 값과 일치하도록 규칙을 설정할 때 일치하는 항목을 찾기 위해 드롭다운에 표시됩니다.

그런 다음 프로필 속성 일치에 대해 &quot;user.size&quot;에 저장된 값/텍스트를 &quot;size&quot; &quot;equals&quot;를 선택할 수 있습니다.

![크기 예](/help/c-recommendations/c-algorithms/assets/example-size.png)

프로필 속성 규칙이 빌드되면 방문자의 저장된 프로필 속성과 일치하지 않는 속성이 있는 모든 권장 사항을 필터링합니다.

### 크기에 따라 항목 추천

프로필 속성 일치가 권장 사항에 영향을 주는 방법에 대한 시각적 예를 보려면 전기 팬을 판매하는 웹 사이트를 생각해 보십시오.

방문자가 이 웹 사이트에서 팬의 다양한 이미지를 클릭하면 각 페이지는 이미지의 팬 크기가 작은지 또는 큼인지에 따라 `entity.size` 매개 변수의 값을 설정합니다.

프로필 스크립트를 만들어 값 `entity.size` 이 작음 대 큼으로 설정된 횟수를 추적하고 카운트한다고 가정합니다.

이후 방문자가 홈 페이지로 돌아가는 경우 더 많은 소규모 팬 또는 큰 팬을 클릭했는지에 따라 필터링된 권장 사항이 표시됩니다.

Recommendations은 웹사이트에서 더 많은 작은 팬을 보는 것을 기준으로 합니다.

![소규모 팬 추천](/help/c-recommendations/c-algorithms/assets/small-fans.png)

Recommendations은 웹사이트에서 더 많은 대규모 팬을 보는 것을 기준으로 합니다.

![대형 팬 추천](/help/c-recommendations/c-algorithms/assets/large-fans.png)