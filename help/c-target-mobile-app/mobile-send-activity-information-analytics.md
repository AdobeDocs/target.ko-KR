---
keywords: mobile;tntVal;analytics;adobe analytics;integration;sdk;mobile sdk;
description: 이 섹션에서는 PostHoc 세그멘테이션을 위해 Adobe Analytics으로 Adobe Target 모바일 앱 활동 정보를 전송하는 방법에 대해 설명합니다.
title: Adobe Analytics으로 Adobe Target 활동 정보 보내기
feature: mobile implementation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 30%

---


# Adobe Analytics에 활동 정보 보내기{#send-activity-information-to-adobe-analytics}

This section describes how to send [!DNL Target] mobile app activity information to Adobe [!DNL Analytics] for post hoc segmentation.

**전제 조건**

* This integration requires that [!DNL Analytics] and [!DNL Target] are implemented using the mobile SDK.
* Ensure that your report suite is enabled to receive activity information from [!DNL Target].

   This is usually done by adding the [!DNL Target] client code to the [!DNL Analytics] report suite. 웹 활동에 SiteCatalyst-Test&amp;Target 통합을 사용하는 경우 이미 활성화되었을 수 있습니다. 이 단계와 관련하여 질문이 있는 경우 Adobe Client Care에 문의하십시오.

1. 활동 정보를 얻습니다.

   If you include a string like the following in your experience content, [!DNL Target] returns the activity information that you can send to [!DNL Analytics]:

   ```
   ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}
   ```

   경험 json 코드의 텍스트를 다음 예와 같이 다른 것으로 바꾸십시오.

   ```
   { 
     "tntVal": ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

   In this example, a node with the variable `tntVal` is added to obtain the activity information. 적절한 제목과 메시지를 사용하는 유사한 코드를 다른 경험에 대해 추가합니다.

   This string delivers a number (such as 115110:0:0) in the response from [!DNL Target]. 이것은 활동 ID, 경험 ID 및 트래픽 유형을 나타냅니다. 다음은 샘플 응답입니다 [!DNL Target].

   ```
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. JSON 개체를 분석합니다.

   Parse the response that came back from [!DNL Target] in the callback. You can use `NSJSONSerialization` to parse this response and store it in a dictionary or an array.

   자세한 내용은 [NSJSONSerialization 설명서를](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error) 참조하십시오.

1. Send the data to [!DNL Analytics].

    호출의 컨텍스트 데이터 개체에 구문 분석된 활동 정보(위 응답에 있는 `tntVal` 등)를 추가합니다. [!DNL Analytics] This [!DNL Analytics] call containing the context data can be fired immediately or it can wait until the next [!DNL Analytics] call is fired.

   예를 들어 `targetLoadRequest` 호출의 콜백에서 이 호출을 실행할 수 있습니다.

   ```
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt`는 Mobile SDK에서 예약된 이벤트 키입니다. The post-classification of the `tntVal` variable in [!DNL Analytics] works in the same way in the mobile SDK as it does on the web (JavaScript). After the information is processed in [!DNL Analytics], you should see activity and experience names in the [!DNL Analytics] interface.

