---
keywords: mobile;tntVal;analytics;adobe analytics;integration;sdk;mobile sdk
description: 애드혹 세그멘테이션을 위해 Adobe Target 모바일 앱 활동 정보를 Adobe Analytics으로 전송하는 방법에 대해 알아봅니다.
title: 모바일 앱 활동 정보를 Analytics로 보낼 수 있습니까?
feature: Implement Mobile
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 29%

---


# Adobe Analytics에 활동 정보 보내기{#send-activity-information-to-adobe-analytics}

이 섹션에서는 임시 세그멘테이션을 위해 [!DNL Target] 모바일 앱 활동 정보를 Adobe [!DNL Analytics]으로 전송하는 방법에 대해 설명합니다.

**전제 조건**

* 이 통합을 사용하려면 모바일 SDK를 사용하여 [!DNL Analytics] 및 [!DNL Target]이(가) 구현되어야 합니다.
* 보고서 세트가 [!DNL Target]에서 활동 정보를 수신할 수 있도록 활성화되었는지 확인합니다.

   일반적으로 [!DNL Target] 클라이언트 코드를 [!DNL Analytics] 보고서 세트에 추가하여 수행합니다. 웹 활동에 SiteCatalyst-Test&amp;Target 통합을 사용하는 경우 이미 활성화되었을 수 있습니다. 이 단계와 관련하여 질문이 있는 경우 Adobe Client Care에 문의하십시오.

1. 활동 정보를 얻습니다.

   경험 컨텐츠에 다음과 같은 문자열을 포함할 경우 [!DNL Target]은 [!DNL Analytics]에 보낼 수 있는 활동 정보를 반환합니다.

   ```javascript
   ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}
   ```

   경험 json 코드의 텍스트를 다음 예와 같이 다른 것으로 바꾸십시오.

   ```javascript
   { 
     "tntVal": ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

   이 예에서 변수 `tntVal`을 사용하는 노드가 활동 정보를 획득하도록 추가됩니다. 적절한 제목과 메시지를 사용하는 유사한 코드를 다른 경험에 대해 추가합니다.

   이 문자열은 [!DNL Target]의 응답에 숫자(예: 115110:0:0)을 전달합니다. 이것은 활동 ID, 경험 ID 및 트래픽 유형을 나타냅니다. 다음은 [!DNL Target]의 샘플 응답입니다.

   ```javascript
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. JSON 개체를 분석합니다.

   콜백의 [!DNL Target]에서 돌아온 응답을 구문 분석합니다. `NSJSONSerialization`을 사용하여 이 응답을 분석하여 사전 또는 배열에 저장할 수 있습니다.

   자세한 내용은 [NSJSONSerialization 설명서](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error)를 참조하십시오.

1. 데이터를 [!DNL Analytics]으로 보냅니다.

    호출의 컨텍스트 데이터 개체에 구문 분석된 활동 정보(위 응답에 있는 `tntVal` 등)를 추가합니다. [!DNL Analytics] 컨텍스트 데이터를 포함하는 이 [!DNL Analytics] 호출은 즉시 실행할 수 있고 다음 [!DNL Analytics] 호출이 실행될 때까지 기다릴 수 있습니다.

   예를 들어 `targetLoadRequest` 호출의 콜백에서 이 호출을 실행할 수 있습니다.

   ```javascript
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt`는 Mobile SDK에서 예약된 이벤트 키입니다. [!DNL Analytics]에서 `tntVal` 변수의 사후 분류는 웹에서 하는 것과 동일한 방식으로 모바일 SDK에서 작동합니다(JavaScript). [!DNL Analytics]에서 정보가 처리되면 [!DNL Analytics] 인터페이스에 활동 및 경험 이름이 표시됩니다.

