---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: a5d2c07105b1d0fac6115fe507537be6a36799e9
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 31%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트 날짜: 2022년 7월 19일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## [!DNL Target Standard/Premium] 22.7.1(2022년 7월 20일)

이 릴리스에는 다음과 같은 기능, 개선 사항 및 수정 사항이 포함되어 있습니다.

| 기능 | 설명 |
| --- | --- |
| IPv6 지원을 통해 대상 평가 정확도 및 최종 사용자 지연 개선 | 이제 방문자의 지리적 위치는 IPv4 주소만 사용하는 것이 아니라 가능한 경우 IPv6 주소로 결정됩니다. 배달 API는 IPv6 입력 매개 변수도 지원합니다. 필터링 및 허용 목록은 IPv4 및 IPv6 주소를 모두 지원합니다. 이 릴리스의 IPv6 지원은 방문자가 대상에 더 정확하게 포함됨을 의미합니다(활동에 대한 보다 정확한 자격이 있거나 필터링 기준에 포함될 수 있음). 또한 IPv6 클라이언트가 직접 라우팅되므로 데이터 지연을 개선하여 IPv6-to-IPv4 게이트웨이의 오버헤드가 발생하지 않습니다. |
| A4T 클라이언트측 페이로드 처리 개선 | A4T 서버측 통합을 사용할 때 Adobe Target이 봇에서 온 것으로 요청을 식별하는 경우 페이로드를 Analytics에 전달하지 않으며 에 기록된 mod_stats 이벤트가 없습니다 [!DNL Target] 로그. 이 릴리스 전에 A4T 클라이언트측 통합에서 페이로드를 [!DNL Analytics]로 식별된 경우에도 보트 트래픽으로 식별됩니다. 서버측과 클라이언트측 간에 불일치가 발생하면, 후자에 대한 A4T 보고서에 보트 트래픽이 포함되므로 불일치가 발생합니다. 또한 보트 트래픽이 반드시 식별되거나 플래그가 지정되지는 않았습니다. 즉, 나머지 트래픽에서 보트 트래픽을 명확히 표현하거나 제거할 수 없었습니다. 그리고 고객이 직접 보트 트래픽을 처리했다고 해도 반드시 다음 트래픽 세트와 일치하지 않을 수도 있습니다 [!DNL Target] 보트 트래픽으로 식별되고 제외되므로 불일치나 다른 문제가 발생합니다. 이 릴리스에서는 A4T 페이로드에 대한 동작이 A4T 서버측과 동일하도록 A4T 클라이언트측 로깅이 향상되었습니다. 보트로 식별되는 방문자는 다음에서 제외됩니다 [!DNL Target] 서버측 및 클라이언트측 구현 둘 다에 대해 카운트/보고. |


## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
