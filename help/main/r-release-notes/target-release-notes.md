---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: bc4b04ae0be1fade2456eb42ade7ee87c0f14b16
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 100%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트 날짜: 2022년 7월 20일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이들 페이지에 대한 정보는 릴리스 날짜에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target] 플랫폼 릴리스(2022년 7월 20일)

이번 릴리스에는 다음과 같은 기능, 개선 및 수정 사항이 포함되었습니다.

| 기능 | 설명 |
| --- | --- |
| IPv6 지원을 통해 대상 평가 정확도 향상 및 최종 사용자 지연 시간 감소(TNT-43364, TNT-44692) | 방문자의 지리적 위치는 이제 IPv4 주소만 사용하는 것이 아니라 IPv6 주소로 결정됩니다. 배달 API는 IPv6 입력 매개변수도 지원합니다. 필터링 및 허용 목록은 IPv4 및 IPv6 주소를 모두 지원합니다. 이 릴리스의 IPv6 지원은 방문자가 보다 정확하게 대상에 포함됨을 의미합니다(더 정확하게 활동 자격을 부여하거나 필터링 기준에 포함됨). 또한 IPv6 클라이언트가 직접 라우팅되므로 IPv6-IPv4 게이트웨이의 오버헤드가 발생하지 않으므로 데이터 지연 시간이 향상됩니다. |
| A4T 클라이언트측 페이로드 처리 문제 해결(TNT-44926) | A4T 서버측 통합을 통해 Adobe Target이 봇에서 전송된 요청을 식별하는 경우 페이로드를 Analytics로 전달하지 않으며 [!DNL Target] 로그에 mod_stats 이벤트가 기록되지 않습니다. 이 릴리스에서는 A4T 페이로드에 대한 비헤이비어가 A4T 서버측과 동일하도록 A4T 클라이언트측 로깅이 향상되었습니다. 봇으로 식별된 방문자는 [!DNL Target] 카운트/보고 대상에서 제외됩니다. (해당 문제는 클라이언트측 페이로드 처리를 사용하는 구현으로 제한되었으며 서버측에는 영향이 없었습니다. 이 릴리스에서는 서버측과 클라이언트측 모두 페이로드 처리에 대해 비헤이비어가 일관됩니다.) |


## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
