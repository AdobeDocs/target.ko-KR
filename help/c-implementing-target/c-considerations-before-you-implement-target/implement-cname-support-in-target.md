---
description: Adobe Target에서 CNAME(표준 이름) 지원을 구현하기 위한 Adobe Client Care 작업 정보입니다.
keywords: 클라이언트 관리;cname;인증서 프로그램;표준 이름;쿠키;인증서
seo-description: Adobe Target에서 CNAME(표준 이름) 지원을 구현하기 위한 Adobe Client Care 작업 정보입니다.
seo-title: CNAME 및 Adobe Target
solution: Target
title: CNAME 및 Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 72260f1bf82dfeab2582add69111439498ad5eb8

---


# CNAME 및 Adobe Target{#cname-and-adobe-target}

Adobe Target에서 CNAME(표준 이름) 지원을 구현하기 위한 Adobe Client Care 작업 정보입니다. 광고 차단 문제를 가장 잘 처리하기 위해 CNAME 이 사용되므로 Adobe가 소유한 도메인이 아니라 고객이 소유한 도메인에 호출됩니다.

다음 단계를 수행하여 Target에서 CNAME 지원을 요청합니다.

1. Adobe Target 호출에 대한 [CNAME 지원을 요청하는 고객 지원 센터 티켓](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)입니다.
1. [AMC(Adobe Managed Certificate) 프로그램](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html)에 등록하고 [!DNL Adobe Analytics]*자사 쿠키* 가이드에 제공된 구현 단계를 따르십시오.

   AMC 프로그램은 자사 쿠키를 구현할 때 고객이 겪게 되는 노력과 혼란을 없애는 데 도움이 됩니다. 이 프로그램에 등록하면 Adobe에서 보안 서버에 설치할 인증서를 구매하여 발급합니다.

   >[!NOTE]
   >
   >CNAME은 AMC 프로그램에 등록하기 전에 구성해야 합니다.

1. 이전 작업을 완료한 후에는 at. js에서 새 CNAME `serverDomain` 로 업데이트해야 합니다.

## 교육 비디오: 퍼스트 파티 쿠키 및 Adobe 관리 인증서 사용

This video is a recording of [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7), an initiative led by the Adobe Customer Care team. Adobe 관리 인증서 프로그램 토론은 10:21 부터 시작됩니다.

[Adobe Analytics: 퍼스트 파티 쿠키 및 Adobe 관리 인증서 사용](https://helpx.adobe.com/customer-care-office-hours/analytics/first-party-cookies-adobe-managed-certificates.html)
