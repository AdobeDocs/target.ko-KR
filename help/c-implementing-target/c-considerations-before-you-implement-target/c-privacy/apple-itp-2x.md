---
description: Experience Cloud ID (ECID) 라이브러리 4.3를 통한 Apple의 ITP 2.1 및 ITP 2.2에 대한 Target 지원에 대한 정보입니다.
keywords: Apple; ITP; 지능적인 추적 방지
seo-description: Experience Cloud ID (ECID) 라이브러리 4.3를 통한 Apple의 ITP 2.1 및 ITP 2.2에 대한 Adobe Target 지원에 대한 정보입니다.
seo-title: Adobe Target 및 Apple ITP 지원
solution: Target
subtopic: 시작하기
title: Apple ITP 2. x
topic: Standard
translation-type: tm+mt
source-git-commit: 71419ee6053eeb86ab6595cfba2f05d8506e05b3

---


# Apple Intelligent Tracking Prevention (ITP) 2. x

지능형 추적 방지 (ITP) 는 Safari 사용자의 개인 정보를 보호하는 Apple의 이니셔티브입니다. 2017 년 있었던 ITP의 첫 번째 릴리스에서는 타사 쿠키의 사용을 타깃팅했습니다. 실제로 Apple는 타사 쿠키를 완전히 차단했습니다. 타사 쿠키는 일반적으로 방문자를 추적하고 방문자 데이터를 수집하는 데 사용되기 때문에 광고 기술 및 Mar Tech 회사를 위한 심각한 골두통이 있었습니다. 이제 Apple는 Safari 내에서 퍼스트 파티 쿠키를 사용하는 방법에 대한 제한 사항과 제한 사항을 적용하려고 합니다.

이러한 ITP 버전에는 다음과 같은 제한 사항이 포함됩니다.

| 버전 | 세부 사항 |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Capped client-side cookies that are placed on the browser using the `document.cookie` API to a seven-day expiry.<br>2019 년 2 월 21 일 릴리스 |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | 7 일간의 만료 시간을 하루 크게 단축했습니다.<br>2019 년 4 월 24 일 릴리스 |

## Adobe Target 고객으로 어떤 영향을 미칩니까?

[!DNL Target] 방문자에게 실시간 개인화를 제공할 수 있도록 페이지에 [!DNL Target] 배포할 JavaScript 라이브러리를 제공합니다. There are three Target JavaScript libraries ([at.js 1.*x*&#x200B;및 at. js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)및 [mbox. js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)) [!DNL Target]`document.cookie` 를 참조하십시오. As a result, [!DNL Target] cookies are impacted by Apple’s ITP 2.1 and 2.2 and will expire after seven days (with ITP 2.1) and after one day (with ITP 2.2).

Apple ITP 2.1 and 2.1 impact [!DNL Target] in the following areas:

| 영향 | 세부 사항 |
| --- | --- |
| 고유 방문자 수 증가 수 | 만료 창이 7 일 (ITP 2.1 포함) 및 하루 (ITP 2.2 포함) 로 설정되어 있으므로 Safari 브라우저에서 오는 고유 방문자 수가 증가할 수 있습니다. If your visitors revisit your domain after seven days (ITP 2.1) or one day (ITP 2.2), [!DNL Target] is forced to place a new [!DNL Target] cookie on your domain in place of the expired cookie. The new [!DNL Target] cookie translates to a new unique visitor even though the user is the same. |
| Decreased lookback periods for [!DNL Target] activities | [!DNL Target] 활동의 방문자 프로필에는 의사 결정 기간 감소가 있을 수 있습니다. [!DNL Target] 쿠키는 방문자를 식별하고 개인화를 위해 사용자 프로필 속성을 저장하는 데 사용됩니다. Given that [!DNL Target] cookies can be expired on Safari after seven days (ITP 2.1) or one day (ITP 2.2), the user profile data that was tied to the purged [!DNL Target] cookie cannot be used for decisioning. |

## Is my current implementation of [!DNL Target] impacted?

In a Safari browser, navigate to your website on which you have a [!DNL Target] JavaScript library. If you see a [!DNL Target] cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.1 or 2.2.

If you are using the Experience Cloud ID (ECID) library in addition to the Target JavaScript library, your implementation will be impacted in the ways listed in this article: [Safari ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customers](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## How can I mitigate the impact of ITP 2.1, ITP 2.2, and future ITP releases to [!DNL Target]?

To mitigate the impact of ITP 2.1, ITP 2.2, and future ITP releases to [!DNL Target], complete the following tasks:

1. 페이지에 Experience Cloud ID (ECID) 라이브러리를 배포합니다.

   ECID 라이브러리는 Experience Cloud 핵심 솔루션에 대한 People Identification Framework를 활성화합니다. ECID 라이브러리를 사용하면 영구 및 고유 식별자를 할당하여 다른 Experience Cloud 솔루션에서 동일한 사이트 방문자 및 해당 데이터를 식별할 수 있습니다. ECID 라이브러리는 자주 업데이트되므로 구현에 영향을 주는 모든 ITP 관련 변경 사항을 완화할 수 있습니다.

   For ITP 2.1 and ITP 2.2, [ECID library 4.3.0+](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) must be utilized for mitigation.

1. Adobe CNAME를 사용하고 Adobe Analytics의 관리 인증서 프로그램에 등록합니다.

   ECID Library 4.3.0 +를 설치한 후 Adobe Analytics의 CNAME 및 관리 인증서 프로그램을 활용할 수 있습니다. 이 프로그램을 사용하면 자사 쿠키에 대한 자사 인증서를 무료로 구현할 수 있습니다. Leveraging CNAME will help [!DNL Target] customers mitigate the impact of ITP 2.1 and ITP 2.2.

   If you are not leveraging CNAME, you can start the process by talking with your account representative and enrolling in the [Adobe Managed Certificate Program](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html).

Target JavaScript 라이브러리를 ECID Library v 4.3.0 +와 함께 배포하고 Adobe Managed Certificate Program에 등록하여 CNAME를 활용하면, ITP 관련 변경에 대한 강력한 및 장기 완화 계획을 갖게 됩니다.

As the industry makes strides to create a more secure web for consumers, [!DNL Adobe Target] is absolutely committed to delivering personalized experiences while meeting and exceeding the privacy expectations of visitors. [!DNL Adobe Target] 는 Apple의 ITP 2.1 및 ITP 2.2에 대한 지원과 [더불어 Google의 Samesite Chrome 정책에](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) 대한 지원을 이미 발표했습니다.

As policies continue to evolve to protect our consumers, [!DNL Adobe] will also continue to support these initiatives in [!DNL Target], while helping our customers provide the best-in-class personalized experiences.
