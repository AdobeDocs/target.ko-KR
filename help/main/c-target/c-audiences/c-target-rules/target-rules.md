---
keywords: 타깃팅;타겟 카테고리;타겟 조건;audience manager;사용자 지정 프로필 매개 변수;방문자 프로필;사용자 지정 사용자 매개 변수;타겟 규칙
description: '카테고리(예: 브라우저, 지역, 네트워크, 운영 체제, 방문자 프로필)를 사용하여 콘텐츠를 타깃팅하는 방법에 대해 알아봅니다.'
title: 대상의 카테고리는 무엇입니까?
feature: Audiences
exl-id: 37d6435d-4139-47c5-a871-6595e089d052
TQID: https://experienceleague.adobe.com/gdwPSImsbXfvaX2Z4bL9-hGyLwo0b0q-At0fokUfYN8
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 385
ht-degree: 50%

---

# 대상자의 카테고리

[!DNL Adobe Target]을(를) 사용하여 여러 범주 특성을 타깃팅할 수 있습니다. 각 속성에 대한 타겟팅 규칙(또는 그룹)을 만들려면 원하는 속성을 대상 빌더 창으로 끌어다 놓습니다.

![대상자에 대한 특성](/help/main/c-target/c-audiences/assets/attributes.png)

특정 카테고리가 선택된 경우 하나 이상의 타깃팅 조건을 적용할 수 있습니다. 예를 들어 지역 카테고리에서는 도시=샌프란시스코와 같은 규칙을 정의합니다. 값을 여러 개 추가하면 OR 조건이 만들어집니다. 방문자는 타깃팅 조건을 충족하기 위해 값 중 하나만 일치하면 됩니다. 동일한 매개 변수에 대한 AND 조건의 경우 사용자 지정 표현식 타겟을 만듭니다.

규칙을 만든 후 **[!UICONTROL 완료]**&#x200B;를 클릭하십시오. 타깃팅 중인 수준에 대한 타깃팅 링크 옆에 규칙의 요약이 표시됩니다.

조건을 추가하거나 다른 카테고리에 추가 규칙을 만들어 규칙을 더욱 구체화할 수 있습니다. 예를 들어 Google에서 사이트에 액세스하는 San Francisco의 Firefox 사용자만 타겟팅할 수 있습니다. [!UICONTROL Geo] 범주를 설정하여 San Francisco의 사용자를 타겟팅하고, [!UICONTROL Browser] 범주를 설정하여 Firefox를 사용하는 사용자를 타겟팅하고, [!UICONTROL 트래픽 소스] 범주를 설정하여 [!UICONTROL From Google]의 사용자를 타겟팅하십시오. 여러 카테고리에 걸쳐 만들어진 규칙은 AND 연산자와 결합됩니다.

범주의 OR 작업을 포함하는 복잡한 타겟팅 규칙을 만들려면 표현식 타겟을 만듭니다.

사용자 지정 프로필 매개 변수와 `user.` 매개 변수를 타깃팅할 수도 있습니다. 대상을 추가할 때 **[!UICONTROL 방문자 프로필]**&#x200B;을(를) 끌어다 놓은 다음 활동을 타깃팅하는 데 사용할 매개 변수를 선택하십시오. 원하는 매개 변수가 표시되지 않으면 mbox에서 매개 변수를 실행하지 않은 것입니다.

검색 상자를 사용하여 [!UICONTROL 대상] 목록을 검색하십시오. 대상 이름의 일부를 검색하거나 특정 문자열을 따옴표로 묶을 수 있습니다.

대상 이름이나 마지막으로 수정한 날짜별로 [!UICONTROL 대상] 목록을 정렬할 수 있습니다. 이름이나 날짜별로 정렬하려면 열 헤더를 클릭한 다음, 대상자를 오름차순이나 내림차순으로 표시하도록 선택하십시오.

## 교육 비디오: 대상자 ![튜토리얼 배지](/help/main/assets/tutorial.png) 만들기

다음 비디오에는 대상 카테고리 사용에 대한 정보가 포함되어 있습니다.

* 대상자 만들기
* 대상 카테고리 정의

>[!VIDEO](https://video.tv.adobe.com/v/17392)
