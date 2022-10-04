---
keywords: 원격 오퍼;원격 오퍼 만들기
description: Adobe에서 JSON 오퍼를 만드는 방법을 알아봅니다 [!DNL Target] 을 참조하십시오. JSON 오퍼는 SPA 프레임워크 또는 서버측 통합에 유용합니다.
title: JSON 오퍼를 만들려면 어떻게 합니까?
feature: Experiences and Offers
exl-id: 793665a4-4cd6-458f-8225-ba23e503a115
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 38%

---

# JSON 오퍼 만들기

에서 JSON 오퍼 만들기 를 참조하십시오. [!UICONTROL 오퍼 라이브러리] in [!DNL Adobe Target] 에서 사용 [!UICONTROL 양식 기반 경험 작성기].

JSON 오퍼는 다음 위치에서 사용 사례를 가능하게 하는 양식 기반 활동에서 사용할 수 있습니다. [!DNL Target]SPA 프레임워크 또는 서버측 통합에서 소비할 JSON 형식으로 오퍼를 전송하는 데 의 의사 결정이 필요합니다.

## JSON 고려 사항

JSON 오퍼를 사용하여 작업할 때에는 다음 정보를 고려하십시오.

* JSON 오퍼는 현재 다음에만 사용할 수 있습니다 [!UICONTROL A/B 테스트] 및 [!UICONTROL 경험 타깃팅] (XT) 활동.
* JSON 오퍼는에서 사용할 수 있습니다. [양식 기반 활동](/help/main/c-experiences/form-experience-composer.md) 전용.
* JSON 오퍼는 서버측 API, Mobile SDK 또는 NodeJS SDK를 사용할 때 바로 검색할 수 있습니다.
* 브라우저에서 JSON 오퍼는 at.js 1.2.3(또는 이상)을 통해서&quot;만&quot;,  [getOffer()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/){target=_blank} 을 사용하여 작업을 필터링함으로써 `setJson` 작업.
* JSON 오퍼는 문자열이 아닌 기본 JSON 개체로 제공됩니다. 이러한 개체의 소비자는 개체를 문자열로 처리하고 JSON 개체로 변환하도록 더 이상 요구받지 않습니다.
* JSON 오퍼는 비시각적 오퍼이므로 다른 오퍼(예: HTML 오퍼)와는 대조적으로 자동으로 적용되지 않습니다. 개발자는 코드를 작성해야 [getOffer()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/){target=_blank}.

## JSON 오퍼 만들기 {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. 클릭 **[!UICONTROL 오퍼]** > **[!UICONTROL 코드 오퍼]**.

   ![오퍼 > 코드 오퍼 탭](/help/main/c-experiences/c-manage-content/assets/code-offers-tab.png)

1. **[!UICONTROL 만들기]** > **[!UICONTROL JSON 오퍼]**&#x200B;를 클릭합니다.

   ![offer-json 이미지](assets/offer-json.png)

1. 오퍼 이름을 입력합니다.
1. **[!UICONTROL 코드]** 상자에 JSON 코드를 입력하거나 붙여 넣습니다.
1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## JSON 예 {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

JSON 오퍼는 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md). 현재 JSON 오퍼를 사용할 수 있는 유일한 방법은 직접적인 API 호출을 통하는 것입니다.

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

JSON 오퍼를 추출하려면 작업을 반복하고 를 사용하여 작업을 찾습니다 `setJson` 작업을 수행한 다음 컨텐츠 배열을 반복합니다.

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

실시간 CDP 프로필 속성은 HTML 오퍼 및 JSON 오퍼에서 사용하기 위해 Target과 공유할 수 있습니다. (이 기능은 현재 베타에 있습니다.)

샘플 사용 사례: 온라인 마케터로서 Grace는 실시간 개인화를 제공하기 위해 AEP/Unified Profile이 속성 값을 Target과 공유하려고 합니다. Grace는 실시간 CDP 프로필 속성을 사용하여 토큰 대체를 사용하여 Target 오퍼에 AEP 속성 값을 표시할 수 있습니다. 예를 들어 고객이 좋아하는 색상으로 `${aep.profile.favoriteColor}`또는 토큰을 사용하여 충성도 계층 및 충성도 포인트 값을 생성합니다 `${aep.loyalty.tier}` 및 `${aep.loyalty.points}`.

![offer-json-aep-shared-attribute 이미지](assets/offer-json-aep-shared-attribute.png)

위에 표시된 예에서 기본값을 할당하는 것은 선택 사항입니다.

## JSON 오퍼 유형별로 오퍼 필터링 {#section_52533555BCE6420C8A95EB4EB8907BDE}

을(를) 필터링할 수 있습니다 [!UICONTROL 오퍼] 라이브러리 를 클릭한 다음 **[!UICONTROL 유형]** 드롭다운 목록을 클릭한 다음 **[!UICONTROL JSON]** 확인란을 선택합니다.

![offer-json-filter 이미지](assets/offer-json-filter.png)
