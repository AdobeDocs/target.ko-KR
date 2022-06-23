---
keywords: 클라우드 인스턴스;공용 접미어 목록;공용 접미어;쿠키;퍼스트 파티 쿠키;자사 쿠키;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: 클라우드 기반 인스턴스를 사용하여 Adobe을 테스트할 때 고객이 직면하는 문제(솔루션 관련)를 살펴보십시오 [!DNL Target] 또는 개념 입증 용도로 사용됩니다.
title: 사용할 수 있습니까 [!DNL Target] 을 클라우드 기반 인스턴스와 함께 사용해야 합니까?
feature: at.js
role: Developer
exl-id: 220371a9-ba57-4e67-b82f-8fec6f9d2833
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 64%

---

# Target에서 클라우드 기반 인스턴스 사용

클라우드 기반 인스턴스를 사용하여 [!DNL Adobe Target]을 테스트할 때 고객이 직면하는 문제에 대한 정보입니다.

 고객들이 테스트나 간단한 개념 입증 용도로 [!DNL Target]Target에 클라우드 기반 인스턴스를 사용하는 경우가 있습니다. 이러한 인스턴스에는 다음과 같은 도메인들이 포함될 수 있습니다.

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com` 또는 `firebaseapp.com`

이러한 도메인 및 기타 많은 다른 도메인이 [공용 접미사 목록](https://publicsuffix.org/list/public_suffix_list.dat)에 나와 있습니다.

**문제:** 최신 브라우저에서는 이러한 도메인을 사용하는 경우 쿠키를 저장하지 않습니다.

다음 [!DNL at.js] JavaScript 라이브러리는 쿠키를 사용하여 사용자를 추적하여 [!DNL Target] 항상 일관된 경험을 제공합니다. 만약 [!DNL Target] JavaScript 라이브러리가 쿠키를 저장할 수 없습니다. [!DNL Target] 요청이 비활성화되었습니다.

**해결 방법:**&#x200B;공용 접미어 목록에 포함된 도메인에 클라우드 기반 인스턴스를 사용하려는 경우 `cookieDomain` 설정을 사용자 지정하는 것이 좋습니다. 자세한 내용은 [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/)를 참조하십시오.
