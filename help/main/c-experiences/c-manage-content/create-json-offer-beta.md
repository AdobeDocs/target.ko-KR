---
keywords: json 오퍼;json 오퍼 만들기
description: '[!UICONTROL Form-Based Experience Composer]에서 사용할 JSON 오퍼를 만드는 방법을 알아봅니다.'
title: JSON 오퍼를 작성하는 방법
feature: Experiences and Offers
hide: true
hidefromtoc: true
exl-id: e022c2d1-3326-405b-aead-5bb4ffa309b3
source-git-commit: 4b57712b838906611702db521b51af84077501e6
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 25%

---

# JSON 오퍼 만들기

[!UICONTROL Form-Based Experience Composer]에서 사용할 JSON 오퍼를 [!DNL Adobe Target]의 [!UICONTROL Offer Library]에 만듭니다.

JSON 오퍼는 양식 기반 활동에서 SPA 프레임워크 또는 서버측 통합에서 사용할 JSON 형식의 오퍼를 보내는 데 [!DNL Target] 의사 결정이 필요한 사용 사례를 사용하도록 설정할 수 있습니다.

## JSON 고려 사항

JSON 오퍼를 사용하여 작업할 때에는 다음 정보를 고려하십시오.

* JSON 오퍼는 현재 [!UICONTROL A/B Test], [!UICONTROL Automated Personalization](AP) 및 [!UICONTROL Experience Targeting](XT) 활동에만 사용할 수 있습니다.
* JSON 오퍼는 [양식 기반 활동](/help/main/c-experiences/form-experience-composer.md)에서만 사용할 수 있습니다.
* JSON 오퍼는 [Server Side API 및 Mobile Node.js, Java, .NET 및 Python SDK](https://experienceleague.adobe.com/en/docs/target-dev/developer/server-side/server-side-overview){target=_blank}를 사용할 때 바로 검색할 수 있습니다.
* 브라우저에서 at.js 1.2.3(또는 이상)을 통해서만, `setJson` 작업을 사용하여 작업을 필터링함으로써 [getOffer()](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer){target=_blank}을(를) 사용하여 JSON 오퍼를 검색할 수 있습니다.
* JSON 오퍼는 문자열이 아닌 기본 JSON 개체로 제공됩니다. 이러한 개체의 소비자는 개체를 문자열로 처리하고 JSON 개체로 변환하도록 더 이상 요구받지 않습니다.
* JSON 오퍼는 비시각적 오퍼이므로 다른 오퍼(예: HTML 오퍼)와는 대조적으로 자동으로 적용되지 않습니다. 개발자는 [getOffer()](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffer){target=_blank}을(를) 사용하여 오퍼를 명시적으로 가져오기 위한 코드를 작성해야 합니다.

## JSON 오퍼 만들기 {#section_BB9C72D59DEA4EFB97A906AE7569AD7A}

1. **[!UICONTROL Offers]** > **[!UICONTROL Code Offers]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Create Offer]** > **[!UICONTROL JSON Offer]**&#x200B;을(를) 클릭합니다.
1. 오퍼 이름을 입력합니다.
1. (조건부) [[!DNL Target] Premium 계정](/help/main/c-intro/intro.md#premium)이 있는 경우 원하는 [작업 공간](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#workspace)을 선택하세요.
1. (조건부) 원하는 프로필 속성을 선택합니다.
1. **[!UICONTROL Code]** 상자에 JSON 코드를 입력하거나 붙여 넣습니다.
1. **[!UICONTROL Create]** 아이콘을 클릭합니다.

## JSON 예 {#section_A54F7BB2B55D4B7ABCD5002E0C72D8C9}

JSON 오퍼는 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 사용하여 만든 활동에서만 지원됩니다. 현재 JSON 오퍼를 사용할 수 있는 유일한 방법은 직접 API/SDK 호출을 통해서입니다.

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

성공 콜백에 전달된 작업은 개체의 배열입니다. 단일 JSON 오퍼가 있다고 가정할 때 해당 오퍼에는 다음 내용이 포함됩니다.

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

JSON 오퍼를 추출하려면 작업을 반복하고 `setJson` 작업을 통해 해당 작업을 찾은 다음, 컨텐츠 배열을 반복합니다.

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
      "excepteur"
    ], 
    "friends": [ 
      { 
        "id": 0, 
        "name": "Carla Lyons" 
      }, 
      { 
        "id": 1, 
        "name": "Ollie Mooney" 
      } 
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

Real-Time CDP 프로필 특성을 [!DNL Target]과(와) 공유하여 HTML 및 JSON 오퍼에 사용할 수 있습니다.

자세한 내용은 [실시간 CDP 프로필 특성을 공유할 때 [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes)를 참조하십시오.

## JSON 오퍼 유형별 오퍼 필터링 {#section_52533555BCE6420C8A95EB4EB8907BDE}

**[!UICONTROL Show filters]** 아이콘(![필터 표시 아이콘](/help/main/assets/icons/Filter.svg))을 클릭한 다음 **[!UICONTROL JSON Offers]** 확인란을 선택하여 [!UICONTROL Offers] 라이브러리를 JSON 오퍼 유형별로 필터링할 수 있습니다.
