---
keywords: 원격 오퍼;원격 오퍼 만들기
description: Adobe에서 JSON 오퍼를 만드는 방법을 알아봅니다 [!DNL Target] 양식 기반 경험 작성기에 사용됩니다.
title: JSON 오퍼를 작성하는 방법
feature: Experiences and Offers
exl-id: 793665a4-4cd6-458f-8225-ba23e503a115
source-git-commit: 7c15a0795e94b6c6317cb5b4018899be71f03a40
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 28%

---

# JSON 오퍼 만들기

에서 JSON 오퍼 만들기 [!UICONTROL 오퍼 라이브러리] 위치: [!DNL Adobe Target] 에서 사용 [!UICONTROL 양식 기반 경험 작성기].

JSON 오퍼는 다음과 같은 사용 사례를 가능하게 하는 양식 기반 활동에서 사용할 수 있습니다. [!DNL Target] SPA 프레임워크 또는 서버측 통합에서 사용할 오퍼를 JSON 형식으로 전송하는 데 의사 결정이 필요합니다.

## JSON 고려 사항

JSON 오퍼를 사용하여 작업할 때에는 다음 정보를 고려하십시오.

* JSON 오퍼는 현재 에만 사용할 수 있습니다. [!UICONTROL A/B 테스트], Automated Personalization (AP) 및 [!UICONTROL 경험 타기팅] (XT) 활동.
* JSON 오퍼는에서 사용할 수 있습니다. [양식 기반 활동](/help/main/c-experiences/form-experience-composer.md) 만 해당.
* JSON 오퍼는 를 사용할 때 직접 검색할 수 있습니다. [서버 측 API 및 Mobile Node.js, Java, .NET 및 Python SDK](https://experienceleague.corp.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}.
* 브라우저에서 JSON 오퍼는 at.js 1.2.3 이상 버전을 통해서만 검색할 수 있고 [getOffer()](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer.html){target=_blank} 를 사용하여 작업을 필터링함으로써 `setJson` 작업.
* JSON 오퍼는 문자열이 아닌 기본 JSON 개체로 제공됩니다. 이러한 개체의 소비자는 개체를 문자열로 처리하고 JSON 개체로 변환하도록 더 이상 요구받지 않습니다.
* JSON 오퍼는 비시각적 오퍼이므로 다른 오퍼(예: HTML 오퍼)와는 대조적으로 자동으로 적용되지 않습니다. 개발자는 코드를 작성해야 [getOffer()](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer.html){target=_blank}.

## JSON 오퍼 만들기 {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. 클릭 **[!UICONTROL 오퍼]** > **[!UICONTROL 코드 오퍼]**.

   ![오퍼 > 코드 오퍼 탭](/help/main/c-experiences/c-manage-content/assets/code-offers-tab.png)

1. **[!UICONTROL 만들기]** > **[!UICONTROL JSON 오퍼]**&#x200B;를 클릭합니다.

   ![offer-json 이미지](assets/offer-json.png)

1. 오퍼 이름을 입력합니다.
1. **[!UICONTROL 코드]** 상자에 JSON 코드를 입력하거나 붙여 넣습니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## JSON 예 {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

JSON 오퍼는 를 사용하여 만든 활동에서만 지원됩니다. [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md). 현재 JSON 오퍼를 사용할 수 있는 유일한 방법은 직접 API/SDK 호출을 통해서입니다.

다음은 한 예입니다.

```json
adobe.target.getOffer({ 
  mbox: "some-mbox", 
  success: function(actions) { 
    console.log('Success', actions); 
  }, 
  error: function(status, error) { 
    console.log('Error', status, error); 
  } 
});
```

성공 콜백에 전달된 작업은 개체의 배열입니다. 다음 컨텐츠가 있는 단일 JSON 오퍼가 있다고 가정하면,

```json
{ 
  "demo": {"a": 1, "b": 2} 
}
```

작업 배열의 구조는 다음과 같습니다.

```json
[ 
 { 
   action: "setJson", 
   content: [{ 
     "demo": {"a": 1, "b": 2} 
   }] 
 }  
]
```

JSON 오퍼를 추출하려면 작업을 반복하고 를 사용하여 작업을 찾습니다. `setJson` 작업을 수행한 다음 컨텐츠 배열을 반복합니다.

## 사용 사례 {#section_85B07907B51A43239C8E3498EF58B1E5}

다음 JSON 오퍼가 웹 페이지에 전달된다고 가정하겠습니다.

```json
{ 
    "_id": "5a65d24d8fafc966921e9169", 
    "index": 0, 
    "guid": "7c006504-c6f7-468d-a46f-f72531ea454c", 
    "isActive": true, 
    "balance": "$2,075.06", 
    "picture": "https://placehold.it/32x32", 
    "tags": [ 
      "esse", 
      "commodo", 
      "excepteur", 
    ], 
    "friends": [ 
      { 
        "id": 0, 
        "name": "Carla Lyons" 
      }, 
      { 
        "id": 1, 
        "name": "Ollie Mooney" 
      }, 
    ], 
    "greeting": "Hello, Stephenson Fernandez! You have 4 unread messages.", 
    "favoriteFruit": "strawberry" 
} 
  
```

다음 코드는 &quot;인사말&quot; 속성에 액세스하는 방법을 보여줍니다.

```json
adobe.target.getOffer({   
  "mbox": "name_of_mbox", 
  "params": {}, 
  "success": function(offer) {           
        console.log(offer[0].content[0].greeting); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

## 실시간 CDP 프로필 속성을 사용하는 JSON 오퍼 예

Real-Time CDP 프로필 속성을 [!DNL Target] HTML 오퍼 및 JSON 오퍼에서 사용할 수 있습니다. (이 기능은 현재 베타 버전입니다.)

샘플 사용 사례: 온라인 마케터로서 Grace는 AEP/통합 프로필이 속성 값을 와 공유하기를 원합니다. [!DNL Target] 실시간 개인화를 제공하기 위해 Real-time CDP 프로필 속성을 사용하여 Grace는 AEP 속성의 값을 [!DNL Target] 토큰 바꾸기를 사용하는 오퍼입니다. 예를 들어, 사용자는 을 사용하여 고객이 선호하는 색상에 따라 개인화할 수 있습니다. `${aep.profile.favoriteColor}`또는 토큰을 사용한 충성도 계층 및 충성도 포인트 값 `${aep.loyalty.tier}` 및 `${aep.loyalty.points}`.

![offer-json-aep-shared-attribute 이미지](assets/offer-json-aep-shared-attribute.png)

기본값 할당은 선택 사항입니다.

## JSON 오퍼 유형별 오퍼 필터링 {#section_52533555BCE6420C8A95EB4EB8907BDE}

다음을 필터링할 수 있습니다. [!UICONTROL 오퍼] 다음을 클릭하여 JSON 오퍼 유형별 라이브러리 **[!UICONTROL 유형]** 드롭다운 목록을 클릭한 다음 **[!UICONTROL JSON]** 확인란.

![offer-json-filter 이미지](assets/offer-json-filter.png)
