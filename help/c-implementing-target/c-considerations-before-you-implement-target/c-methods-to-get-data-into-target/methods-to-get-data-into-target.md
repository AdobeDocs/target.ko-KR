---
keywords: 구현;구현하기;설정하기;설정;페이지 매개 변수;tomcat;url 인코딩;인페이지 프로필 속성;mbox 매개 변수;인페이지 프로필 속성;스크립트 프로필 속성;벌크 프로필 업데이트 API;단일 파일 업데이트 API;고객 속성;데이터 공급자;dataprovider;데이터공급자
description: 데이터를 Target(페이지 매개 변수, 프로필 속성, 스크립트 프로필 속성, 데이터 공급자, 단일 및 벌크 프로필 업데이트 API, 고객 속성)로 가져올 수 있습니다.
title: 데이터를 Target으로 가져오려면 어떻게 해야 합니까?
feature: 구현
role: Developer
exl-id: b42eb846-d423-4545-a8fe-0b8048ab689e
translation-type: tm+mt
source-git-commit: 70d4c5b4166081751246e867d90d43b67efa5469
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 86%

---

# 메서드 개요

데이터를 [!DNL Adobe Target]에 가져오는 데 사용할 수 있는 여러 방법에 대한 정보입니다.

사용 가능한 방법에는 다음이 포함됩니다.

| 메서드 | 세부 사항 |
| --- | --- |
| [](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/page-parameters.md)<br>페이지 매개 변수(&quot;mbox 매개 변수&quot;라고도 함) | 페이지 매개 변수는 나중에 사용할 수 있도록 방문자 프로필에 저장되지 않은 페이지 코드를 통해 직접 전달된 이름/값 쌍입니다.<br>페이지 매개 변수는 나중에 타깃팅 용도로 지정할 수 있도록 방문자의 프로필에 저장할 필요가 없는 추가적인 페이지 데이터를 Target에 전송하는 데 유용합니다. 대신 이 값은 페이지나, 특정 페이지에서 사용자가 취하는 행동을 설명하는 데 사용됩니다. |
| [](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/in-page-profile-attributes.md)<br>인페이지 프로필 속성(&quot;mbox 내 프로필 속성&quot;이라고도 함) | 인페이지 프로필 속성은 나중에 사용할 수 있도록 방문자 프로필에 저장된 페이지 코드를 통해 직접 전달된 이름/값 쌍입니다.<br>인페이지 프로필 속성을 사용하면 나중에 타깃팅 및 세그멘테이션을 수행할 수 있도록 사용자별 데이터를 Target의 프로필에 저장할 수 있습니다. |
| [스크립트 프로필 속성](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/script-profile-attributes.md) | 스크립트 프로필 속성은 Target 솔루션에 정의된 이름/값 쌍입니다. 서버 호출에 대해 Target 서버에서 JavaScript 코드 조각을 실행하여 값을 결정합니다.<br>사용자는 mbox 호출에 대해 실행되는 작은 코드 조각을 작성한 다음 대상 및 활동 멤버십에 대해 방문자를 평가합니다. |
| [데이터 공급자](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/data-providers.md) | 데이터 제공업체는 제3자의 데이터를 Target으로 쉽게 전달할 수 있는 기능입니다. |
| 벌크 프로필 업데이트 API | API를 통해 많은 방문자에 대한 방문자 프로필 업데이트를 사용하여 Target에 .csv 파일을 보냅니다. 각 방문자 프로필은 하나의 호출에서 여러 개의 인페이지 프로필 속성으로 업데이트할 수 있습니다. |
| 벌크 프로필 업데이트 API | 벌크 프로필 업데이트 API와 거의 동일하지만 한 번에 하나의 방문자 프로필이 .csv 파일이 아닌 API 호출에서 한 번에 업데이트됩니다. |
| 고객 속성 | 고객 속성을 사용하면 FTP를 통해 방문자 프로필 데이터를 Experience Cloud에 업로드할 수 있습니다. 업로드했으면 Adobe Analytics 및 Adobe Target의 데이터를 활용합니다. |







## 벌크 프로필 업데이트 API {#section_92AB4820A5624C669D9A1F1B6220D4FA}

API를 통해 많은 방문자에 대한 방문자 프로필 업데이트를 사용하여 Target에 .csv 파일을 보냅니다. 각 방문자 프로필은 하나의 호출에서 여러 개의 인페이지 프로필 속성으로 업데이트할 수 있습니다.

이 선택 사항은 다음 몇 가지 차이점을 제외하고는 고객 속성과 매우 유사합니다.

* 고객 속성은 FTP 업로드를 사용하는 반면, Target 벌크 프로필 업데이트 API는 HTTP POST API를 사용합니다.
* 고객 속성 데이터는 Analytics과 공유할 수 있고, 벌크 프로필 업데이트는 Target에서만 사용할 수 있습니다.
* 고객 속성은 Target이 아직 보지 못한 사용자에 대한 프로필 작성을 지원합니다. 벌크 프로필 업데이트 API는 기존 Target 프로필만 업데이트합니다.
* 고객 속성에는 Experience Cloud ID(ECID)를 사용해야 합니다. 벌크 프로필 업데이트 API에는 TNT ID나 `mbox3rdPartyId`를 사용해야 합니다.
* `mbox3rdPartyID`에서 더하기 기호(+)와 슬래시(/)는 보낼 수 없습니다.

### 형식

.csv 파일은 Target PCID나 mboxThirdPartyId를 통해 각 방문자를 참조해야 합니다. Experience Cloud ID(ECID)는 지원되지 않습니다. 모든 프로필 속성/값은 API를 통해 생성 및 업데이트됩니다. 형식 세부 사항은 API 설명서에 나와 있습니다.

### 사용 사례 예

CRM 또는 기타 내부 시스템은 페이지 구현에서 프로필 데이터를 노출하지 않고 Target에 지속적으로 업데이트하고자 하는 방문자에 대한 중요 데이터를 저장합니다.

### 방법 장점

프로필 속성의 개수에 대한 제한은 없습니다.

사이트를 통해 전송된 프로필 속성은 API를 통해 업데이트할 수 있으며 반대의 경우도 마찬가지입니다.

### 주의 사항

묶음 파일의 크기는 50MB 미만이어야 합니다. 또한 총 행 수는 업로드당 500,000개 행을 초과하지 않아야 합니다.

이후 묶음에서 24시간 동안 업로드할 수 있는 행 수에는 제한이 없습니다. 그러나 영업 시간 동안 처리 프로세스를 조절하여 다른 프로세스가 효율적으로 실행되도록 할 수도 있습니다.

동일한 thirdPartyIds 간에 mbox를 호출하지 않고 연속적인 [V2 배치 업데이트를 호출](https://developers.adobetarget.com/api/#updating-profiles)하면 첫 번째 배치 업데이트 호출에서 업데이트된 속성을 재정의합니다.

### 코드 예

[프로필 업데이트](https://developers.adobetarget.com/api/#updating-profiles)를 참조하십시오.

### 관련 정보 링크

[프로필 업데이트](https://developers.adobetarget.com/api/#updating-profiles)

## 벌크 프로필 업데이트 API {#section_5D7A9DD7019F40E9AEF2F66F7F345A8D}

벌크 프로필 업데이트 API와 거의 동일하지만 한 번에 하나의 방문자 프로필이 .csv 파일이 아닌 API 호출에서 한 번에 업데이트됩니다.

### 형식

방문자는 Target mboxPC 값이나 mboxThirdPartyId 값을 통해 식별해야 합니다. Experience Cloud ID(ECID)는 지원되지 않습니다. 

### 사용 사례 예

방문자가 콜 센터에 도착하거나, 대출 자금을 지원받거나, 점포에서 포인트 카드를 사용하거나, 키오스크에 액세스하는 등의 오프라인 작업을 수행하는 경우 실시간으로 Target을 업데이트할 수 있습니다.

### 방법 장점

프로필 속성의 개수에 대한 제한은 없습니다.

사이트를 통해 전송된 프로필 속성은 API를 통해 업데이트할 수 있으며 반대의 경우도 마찬가지입니다.

### 주의 사항

24시간 기간당 1,000,000개의 API 호출 수 제한(1백만)

프로필만 업데이트합니다. Target이 아직 보지 못한 잠재적 사용자에 대한 프로필을 작성할 수 없습니다.

### 코드 예

GET 및 POST가 지원됩니다. `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

### 관련 정보 링크

[프로필 업데이트](https://developers.adobetarget.com/api/#updating-profiles)

## 고객 속성{#section_C47FC7980A9A4608BD1A5F0BD900FA70}을 통해 정보를 추가할 수 있습니다 

고객 속성을 사용하면 FTP를 통해 방문자 프로필 데이터를 Experience Cloud에 업로드할 수 있습니다. 업로드했으면 Adobe Analytics 및 Adobe Target의 데이터를 활용합니다.

Target Standard 고객은 5개의 속성을 활용할 수 있으며, Target Premium 고객은 200개의 속성을 활용할 수 있습니다.

### 형식

Experience Cloud ID(ECIDs) 및 속성 이름/값 쌍이 있는 .csv 파일은 FTP를 통해 업로드되거나 Experience Cloud UI에서 수동으로 업로드됩니다.

### 사용 사례 예

CRM 또는 기타 내부 시스템은 Target 및 Analytics를 포함하여 Adobe의 Experience Cloud와 공유하려는 중요 정보를 저장합니다.

### 방법 장점

고객 데이터를 업로드하면 Target에 방문자가 아직 표시되지 않은 경우에도 Target에서 해당 방문자에 대한 프로필 항목이 만들어집니다.

동일한 데이터를 Target 및 Analytics에서 자동으로 사용할 수 있습니다.

FTP는 API보다 간단한 구현 방법일 수 있습니다.

### 주의 사항

Target Standard 고객은 5개의 속성을 활용할 수 있으며, Target Premium 고객은 200개의 속성을 활용할 수 있습니다.

페이지에서가 아니라 고객 속성을 통해서만 값을 업데이트할 수 있습니다.

Experience Cloud ID(ECID) 구현이 필요합니다.

### 코드 예

자세한 내용은 [고객 속성 소스를 만들고 데이터 파일](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html)에 업로드하십시오.

### 관련 정보 링크

[고객 속성 소스를 만들고 데이터 파일 업로드](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).
