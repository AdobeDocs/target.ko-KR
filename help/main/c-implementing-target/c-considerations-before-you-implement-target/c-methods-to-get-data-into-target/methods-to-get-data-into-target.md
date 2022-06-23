---
keywords: 구현;구현하기;설정하기;설정;페이지 매개 변수;tomcat;url 인코딩;인페이지 프로필 속성;mbox 매개 변수;인페이지 프로필 속성;스크립트 프로필 속성;벌크 프로필 업데이트 API;단일 파일 업데이트 API;고객 속성;데이터 공급자;dataprovider;데이터공급자
description: 로 데이터 가져오기 [!DNL Target] (페이지 매개 변수, 프로필 속성, 스크립트 프로필 속성, 데이터 공급자, 단일 및 벌크 프로필 업데이트 API, 고객 속성).
title: 데이터를 Target으로 가져오려면 어떻게 해야 합니까?
feature: Implementation
role: Developer
exl-id: b42eb846-d423-4545-a8fe-0b8048ab689e
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 56%

---

# 메서드 개요

로 데이터를 가져오는 데 사용할 수 있는 다양한 방법에 대한 정보입니다 [!DNL Adobe Target].

사용 가능한 메서드는 다음과 같습니다.

| 방법 | 세부 사항 |
| --- | --- |
| [페이지 매개 변수](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/page-parameters/)<br>(mbox 매개 변수라고도 함) | 페이지 매개 변수는 나중에 사용할 수 있도록 방문자 프로필에 저장되지 않은 페이지 코드를 통해 직접 전달된 이름/값 쌍입니다.<br>페이지 매개 변수는 향후 타깃팅을 사용하기 위해 방문자의 프로필과 함께 저장할 필요가 없는 Target으로 페이지 데이터를 전송하는 데 유용합니다. 대신 이 값은 페이지나, 특정 페이지에서 사용자가 취하는 행동을 설명하는 데 사용됩니다. |
| [인페이지 프로필 속성](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/in-page-profile-attributes/)<br>(mbox 내 프로필 속성이라고도 함) | 인페이지 프로필 속성은 나중에 사용할 수 있도록 방문자 프로필에 저장된 페이지 코드를 통해 직접 전달된 이름/값 쌍입니다.<br>인페이지 프로필 속성을 사용하면 나중에 타깃팅 및 세그멘테이션을 수행할 수 있도록 사용자별 데이터를 Target의 프로필에 저장할 수 있습니다. |
| [스크립트 프로필 속성](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/script-profile-attributes/) | 스크립트 프로필 속성은 Target 솔루션에 정의된 이름/값 쌍입니다. 서버 호출에 대해 Target 서버에서 JavaScript 코드 조각을 실행하여 값을 결정합니다.<br>사용자는 mbox 호출에 대해 실행되는 작은 코드 조각을 작성한 다음 대상 및 활동 멤버십에 대해 방문자를 평가합니다. |
| [데이터 공급자](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/data-providers/) | 데이터 공급자를 사용하면 타사의 데이터를 Target에 쉽게 전달할 수 있습니다. |
| [벌크 프로필 업데이트 API](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/bulk-profile-update-api/) | API를 통해 많은 방문자에 대한 방문자 프로필 업데이트를 사용하여 Target에 .csv 파일을 보냅니다. 각 방문자 프로필은 하나의 호출에서 여러 개의 인페이지 프로필 속성으로 업데이트할 수 있습니다. |
| [싱글 프로필 업데이트 API](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/single-profile-update-api/) | 벌크 프로필 업데이트 API와 거의 동일하지만 하나의 방문자 프로필은 .csv 파일이 아닌 API 호출의 한 번에 업데이트됩니다. |
| [고객 속성](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/customer-attributes/) | 고객 속성을 사용하면 FTP를 통해 방문자 프로필 데이터를 Experience Cloud에 업로드할 수 있습니다. 업로드했으면 Adobe Analytics 및 Adobe Target에서 데이터를 사용하십시오. |












