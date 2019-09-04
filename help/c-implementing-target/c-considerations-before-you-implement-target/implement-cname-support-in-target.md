---
description: Adobe Target에서 CNAME(표준 이름) 지원을 구현하기 위한 Adobe Client Care 작업 정보입니다.
keywords: 클라이언트 관리;cname;인증서 프로그램;표준 이름;쿠키;인증서; amc; Adobe 관리 인증서
seo-description: Adobe Target에서 CNAME(표준 이름) 지원을 구현하기 위한 Adobe Client Care 작업 정보입니다.
seo-title: CNAME 및 Adobe Target
solution: Target
title: CNAME 및 Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: b7a80326b0b89f6fe3bac70ccc6941be09d14ac1

---


# CNAME 및 Adobe Target {#cname-and-adobe-target}

Information about working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Target]. 광고 차단 문제 또는 ITP 관련 쿠키 정책을 가장 잘 처리하기 위해 CNAME 이 사용되어 Adobe가 소유한 도메인이 아니라 고객이 소유한 도메인에 호출됩니다.

Perform the following steps to request CNAME support in [!DNL Target]:

1. 호출에 [대한 CNAME 지원을](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) 요청하는 고객 지원 티켓을 [!DNL Target] 엽니다.

1. CNAME 레코드를 만듭니다 (아래 지침 참조).

   티켓을 받으면 FPSSL 전문가가 CNAME 레코드 쌍을 제공해야 합니다. Adobe가 귀하를 대신하여 인증서를 구입할 수 있으려면 먼저 회사의 DNS 서버에서 이러한 기록을 구성해야 합니다.

   CNAME는 다음 예와 유사합니다.

   `DNS record: metrics.example.com IN CNAME metricsexample-fpssl.tt.omtrdc.net`

1. 이러한 CNAME 이 준비되면 Adobe는 digicert와 협력하여 Adobe 프로덕션 서버에 인증서를 구매 및 설치합니다.

1. 이전 작업을 완료한 후에는 at. js에서 새 CNAME `serverDomain` 로 업데이트해야 합니다.
