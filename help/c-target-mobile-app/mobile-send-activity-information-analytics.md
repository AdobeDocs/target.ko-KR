---
description: 이 섹션에서는 postAhoc 세그멘테이션을 위해 Target 모바일 앱 활동 정보를 Adobe Analytics에 보내는 방법을 설명합니다.
seo-description: 이 섹션에서는 postAhoc 세그멘테이션을 위해 Target 모바일 앱 활동 정보를 Adobe Analytics에 보내는 방법을 설명합니다.
seo-title: Adobe Analytics에 활동 정보 보내기
title: Adobe Analytics에 활동 정보 보내기
uuid: 2ca1ebfe-5008-4a73-a032-1ad81f062925
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Adobe Analytics에 활동 정보 보내기{#send-activity-information-to-adobe-analytics}

이 섹션에서는 postAhoc 세그멘테이션을 위해 Target 모바일 앱 활동 정보를 Adobe Analytics에 보내는 방법을 설명합니다.

**전제 조건**

* 이 통합을 사용하려면 Mobile SDK를 사용하여 Analytics와 Target을 구현해야 합니다.
* 보고서 세트가 Target에서 활동 정보를 수신하도록 설정되어 있는지 확인하십시오.

   이 작업은 일반적으로 Target 클라이언트 코드를 Analytics 보고서 세트에 추가함으로써 수행됩니다. 웹 활동에 SiteCatalyst-Test&amp;Target 통합을 사용하는 경우 이미 활성화되었을 수 있습니다. 이 단계와 관련하여 질문이 있는 경우 Adobe Client Care에 문의하십시오.

1. 활동 정보를 얻습니다.

   경험 컨텐츠에 다음과 같은 문자열을 포함하는 경우 Target에서는 Analytics에 전송할 수 있는 캠페인 정보를 반환합니다.

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

   이 예에서는 활동 정보를 얻기 위해 변수 &#39;`tntVal`&#39;을 사용하는 노드가 추가됩니다. 적절한 제목과 메시지를 사용하는 유사한 코드를 다른 경험에 대해 추가합니다.

   이 문자열은 Target의 응답에서 숫자(예: 115110:0:0)를 전달합니다. 이것은 활동 ID, 경험 ID 및 트래픽 유형을 나타냅니다. 다음은 Target의 샘플 응답입니다.

   ```
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. JSON 개체를 분석합니다.

   콜백에서 Target으로부터 돌아온 응답을 분석합니다. NSJSONSerialization을 사용하여 이 응답을 분석한 후 dict 또는 배열에 저장할 수 있습니다.

   자세한 내용은 [Nsjsonserialization 설명서를](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error) 참조하십시오.
1. 데이터를 Analytics로 보냅니다.

   Analytics 호출의 컨텍스트 데이터 개체에 구문 분석된 활동 정보(위 응답에 있는 `tntVal` 등)를 추가합니다. 컨텍스트 데이터가 포함된 이 Analytics 호출은 즉시 실행하거나 다음 Analytics 호출이 실행되기 전까지 대기할 수 있습니다.

   예를 들어 `targetLoadRequest` 호출의 콜백에서 이 호출을 실행할 수 있습니다.

   ```
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt`는 Mobile SDK에서 예약된 이벤트 키입니다. Analytics의 `tntVal` 변수에 대한 사후 분류는 웹(JavaScript)에서와 동일한 방식으로 모바일 SDK에서 작동합니다. Analytics에서 정보가 처리되면 Analytics 인터페이스에 활동 및 경험 이름이 표시됩니다.

