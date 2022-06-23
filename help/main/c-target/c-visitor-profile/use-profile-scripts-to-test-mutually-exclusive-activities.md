---
keywords: 프로필 스크립트;프로필 스크립트 속성;상호 배타적인 활동
description: 프로필 속성을 사용하여 Adobe에서 테스트를 설정하는 방법을 알아봅니다 [!DNL Target] 여러 활동을 비교하지만 동일한 방문자가 각 활동에 참여하도록 하지는 않습니다.
title: 프로필 스크립트를 사용하여 함께 수행할 수 없는 활동을 테스트할 수 있습니까?
feature: Audiences
exl-id: b0b23887-3339-411e-9f5c-64f9d1ba778c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 74%

---

# 함께 수행할 수 없는 활동을 테스트하는 프로필 스크립트 사용

에서 프로필 속성을 사용할 수 있습니다 [!DNL Adobe Target] 두 개 이상의 활동을 비교하지만 동일한 방문자가 각 활동에 참여하도록 하지 않는 테스트를 설정하려면 다음을 수행하십시오.

상호 배타적인 활동 테스트에서는 한 활동의 방문자가 다른 활동에 대한 테스트 결과에 영향을 주지 않습니다. 방문자가 여러 활동에 참여하는 경우 양수 또는 음수 리프트가 방문자의 한 활동 경험에서 발생했는지 여부 또는 여러 활동 간의 상호 작용이 하나 이상의 활동 결과에 영향을 주었는지 여부를 확인하기 어려울 수 있습니다.

예를 들어 전자 상거래 시스템의 두 영역을 테스트할 수 있습니다. 장바구니에 추가 단추를 파란색이 아니라 빨간색으로 만들어 테스트하고 싶을 수 있습니다. 단계 수를 5개에서 2개로 줄이는 새로운 체크아웃 프로세스를 테스트할 수도 있습니다. 두 활동 모두에 동일한 성공 이벤트(완료된 구매)가 있는 경우 빨간색 단추가 전환을 향상하는지 또는 개선된 체크아웃 프로세스로 인해 동일한 전환도 증가했는지 여부를 판별하기 어려울 수 있습니다. 테스트를 상호 배타적인 활동으로 구분하면 각 변경을 독립적으로 테스트할 수 있습니다.

다음 프로필 스크립트 중 하나를 사용할 때 다음 정보를 유념하십시오.

* 프로필 스크립트는 활동이 시작되기 전에 실행되어야 하며 스크립트는 활동 지속 기간 동안 변경되지 않은 상태로 있어야 합니다.
* 이 기법은 활동의 트래픽 양을 줄임으로써 활동을 더 오래 실행해야 할 수 있습니다. 활동 지속 기간을 추정할 때 이 사실을 고려해야 합니다.

## 두 개의 활동 설정

방문자를 각각 다른 활동이 표시되는 그룹으로 정렬하려면 프로필 속성을 만들어야 합니다. 프로필 속성은 방문자를 둘 이상 그룹의 하나로 정렬할 수 있습니다. &quot;twogroups&quot;라는 프로필 속성을 설정하려면 다음 스크립트를 만드십시오.

```javascript
if (!user.get('twogroups')) { 
    var ran_number = Math.floor(Math.random() * 99); 
    if (ran_number <= 49) { 
        return 'GroupA'; 
    } else { 
        return 'GroupB'; 
    } 
}
```

* `if (!user.get('twogroups'))`는 *twogroups* 프로필 속성이 현재 방문자에 대해 설정되었는지 여부를 확인합니다. 설정된 경우 추가 작업이 필요 없습니다.

* `var ran_number=Math.floor(Math.random() *99)`는 ran_number라는 새 변수를 선언하고 해당 값을 0과 1 사이의 임의 소수로 설정한 다음 99를 곱하고 내림하여 100(0-99)의 범위를 만듭니다. 이 범위는 활동을 보는 방문자의 비율을 지정하는 데 유용합니다.

* `if (ran_number <= 49)`는 방문자가 속하는 그룹을 결정하는 루틴을 시작합니다. 반환된 숫자가 0-49이면 방문자가 GroupA에 할당됩니다. 숫자가 50-99이면 방문자가 GroupB에 할당됩니다. 그룹은 방문자에게 표시되는 활동을 결정합니다.

프로필 속성을 만든 후 사용자 프로필 매개 변수를 요구하여 원하는 모집단을 타겟팅하려면 첫 번째 활동을 설정하십시오 `user.twogroups` 는 GroupA에 지정된 값과 일치합니다.

>[!NOTE]
>
>페이지의 앞부분에서 mbox를 선택하십시오. 이 코드는 방문자가 활동을 경험하는지 여부를 결정합니다. 브라우저가 mbox를 처음 발견하기만 하면 이 값을 설정하는 데 사용할 수 있습니다.

사용자 프로필 매개 변수 `user.twogroups`가 GroupB에 대해 지정된 값과 일치하도록 두 번째 캠페인을 설정하십시오.

## 3개 이상의 활동 설정

3개 이상의 상호 배타적인 활동을 설정하는 과정은 두 개를 설정하는 과정과 비슷하지만 프로필 속성 JavaScript를 변경하여 각 활동에 대해 별도의 그룹을 만들고 각 활동을 보는 사람을 결정해야 합니다. 홀수 또는 짝수 그룹을 만드는지에 따라 난수 생성이 달라집니다.

예를 들어 그룹을 4개 만들려면 다음 JavaScript를 사용하십시오.

```javascript
if (!user.get('fourgroups')) { 
    var ran_number = Math.floor​(Math.random() * 99); 
    if (ran_number <= 24) { 
        return 'GroupA'; 
    } else if (ran_number <= 49) { 
        return 'GroupB'; 
    } else if (ran_number <= 74) { 
        return 'GroupC'; 
    } else { 
        return 'GroupD'; 
    } 
}
```

이 예에서 방문자를 그룹에 할당하는 난수 생성에 사용된 수학은 그룹이 2개인 경우와 동일합니다. 임의 소수가 생성된 다음 내림되어 정수를 만듭니다.

홀수 그룹이나 100이 균일하게 나누어지지 않는 임의 개수를 만드는 경우 소수를 정수로 내림하면 안 됩니다. 소수를 내림하지 않으면 정수가 아닌 범위를 지정할 수 있습니다. 이 작업을 수행하려면 다음 줄을 찾습니다.

`var ran_number=Math.floor(Math.random()*99);`

다음 동작을 수행합니다.

`var ran_number=Math.random()*99;`

예를 들어 방문자를 동일한 그룹 3개에 배치하려면 다음 코드를 사용하십시오.

```javascript
if (!user.get('threegroups')) { 
    var ran_number = Math.random() * 99; 
    if (ran_number <= 32.33) { 
        return 'GroupA'; 
    } else if (ran_number <= 65.66) { 
        return 'GroupB'; 
    } else { 
        return 'GroupC'; 
    } 
}
```