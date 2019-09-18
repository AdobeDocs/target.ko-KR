---
description: Experience Cloud ID(ECID) 라이브러리 4.3을 통해 Apple의 ITP 2.1 및 ITP 2.2에 대한 Target 지원에 대한 정보입니다.
keywords: apple;ITP;지능적인 추적 방지
seo-description: Experience Cloud ID(ECID) 라이브러리 4.3을 통해 Apple의 ITP 2.1 및 ITP 2.2에 대한 Adobe Target 지원에 대한 정보입니다.
seo-title: Adobe Target 및 Apple ITP 지원
solution: Target
subtopic: 시작하기
title: Apple ITP 2.x
topic: Standard
translation-type: tm+mt
source-git-commit: 8dc94ca1ed48366e6b3ac7a75b03c214f1db71d9

---


# Apple Intelligent Tracking Prevention (ITP) 2.x

ITP(Intelligent Tracking Prevention)는 Apple의 이니셔티브로 Safari 사용자의 개인 정보를 보호합니다. 2017년에 있었던 ITP의 첫 번째 릴리스는 타사 쿠키 사용을 타깃팅했습니다. 실제로, Apple은 타사 쿠키 전체를 차단하여, 결국 타사 쿠키는 일반적으로 방문자 추적 및 방문자 데이터 수집에 사용되기 때문에 광고 기술 및 마어 기술 회사에는 심각한 골칫거리가 되었습니다. 이제 Apple은 Safari 내에서 퍼스트 파티 쿠키가 사용되는 방법에 대한 제한 및 제한을 시행하려고 합니다.

이러한 버전의 ITP에는 다음 제한 사항이 포함됩니다.

| 버전 | 세부 사항 |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | API를 사용하여 브라우저에 삽입된 `document.cookie` 제한적 클라이언트측 쿠키를 7일 만료에 연결합니다.<br>2019년 2월 21일 릴리스. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | 7일 만기 한도를 하루로 대폭 줄였다.<br>2019년 4월 24일 릴리스. |

## Adobe Target 고객으로서 저에게 미치는 영향은 무엇입니까?

[!DNL Target] 방문자에게 실시간 개인화를 제공할 [!DNL Target] 수 있도록 페이지에 배포할 수 있는 JavaScript 라이브러리를 제공합니다. 세 개의 Target JavaScript 라이브러리([at.js 1)가 있습니다.*x*&#x200B;및 at.js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)및 [mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md))를 사용하여 API를 통해 방문자의 브라우저에 클라이언트측 [!DNL Target] 쿠키를 `document.cookie` 배치합니다. 결과적으로, [!DNL Target] 쿠키는 Apple의 ITP 2.1 및 2.2에 의해 영향을 받고 7일(ITP 2.1 포함) 후 및 1일(ITP 2.2 포함) 후에 만료됩니다.

Apple ITP 2.1 및 2.1은 다음 [!DNL Target] 영역에 영향을 줍니다.

| 영향 | 세부 사항 |
| --- | --- |
| 고유 방문자 수의 잠재적인 증가 | 만료 기간이 7일(ITP 2.1 사용) 및 1일(ITP 2.2 사용)로 설정되었기 때문에 Safari 브라우저에서 고유 방문자 수가 증가할 수 있습니다. 방문자가 7일(ITP 2.1) 또는 1일(ITP 2.2) 후 도메인을 다시 방문하면 만료된 쿠키 대신 새 [!DNL Target] [!DNL Target] 쿠키를 도메인에 배치해야 합니다. 사용자가 동일하더라도 새 [!DNL Target] 쿠키는 새로운 고유 방문자로 변환됩니다. |
| 활동 확인 기간 [!DNL Target] 감소 | 활동에 대한 방문자 프로필의 [!DNL Target] 확인 기간이 줄어들 수 있습니다. [!DNL Target] 쿠키를 사용하여 방문자를 식별하고 개인화를 위해 사용자 프로필 속성을 저장합니다. 7일(ITP 2.1) 또는 1일(ITP 2.2)이 지나면 Safari에서 [!DNL Target] 쿠키가 만료될 수 있으므로 삭제된 [!DNL Target] 쿠키에 연결된 사용자 프로필 데이터를 의사 결정에 사용할 수 없습니다. |

## 현재 구현이 [!DNL Target] 영향을 받습니까?

Safari 브라우저에서 JavaScript 라이브러리가 있는 웹 사이트로 [!DNL Target] 이동합니다. CNAME의 컨텍스트에서 설정된 [!DNL Target] 쿠키(예: `analytics.company.com`예:)가 표시되면 ITP 2.1 또는 2.2의 영향을 받지 않습니다.

Target JavaScript 라이브러리 외에 Experience Cloud ID(ECID) 라이브러리를 사용하는 경우, 구현에 다음 문서의 나열된 방식으로 영향을 받습니다.Safari [ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customer](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## ITP 2.1, ITP 2.2 및 향후 ITP 릴리스의 효과를 어떻게 완화시킬 수 [!DNL Target]있습니까?

ITP 2.1, ITP 2.2 및 향후 ITP 릴리스의 영향을 완화하려면 [!DNL Target]다음 작업을 완료하십시오.

1. Experience Cloud ID(ECID) 라이브러리를 페이지에 배포합니다.

   ECID 라이브러리를 사용하면 Experience Cloud 코어 솔루션에 대한 사용자 식별 프레임워크를 사용할 수 있습니다. ECID 라이브러리를 사용하면 영구적이고 고유한 식별자를 할당하여 다른 Experience Cloud 솔루션에서 동일한 사이트 방문자와 해당 데이터를 식별할 수 있습니다. ECID 라이브러리는 구현에 영향을 주는 ITP 관련 변경 사항을 완화하도록 자주 업데이트됩니다.

   ITP 2.1 및 ITP 2.2의 경우 [ECID 라이브러리 4.3.0+](https://docs.adobe.com/content/help/en/id-service/using/release-notes/release-notes.html) 를 활용하여 완화할 수 있어야 합니다.

1. Adobe의 CNAME을 사용하고 Adobe Analytics의 관리 인증서 프로그램에 등록합니다.

   ECID 라이브러리 4.3.0+를 설치한 후 Adobe Analytics의 CNAME 및 관리 인증서 프로그램을 활용할 수 있습니다. 이 프로그램을 사용하면 자사 쿠키에 대한 퍼스트 파티 인증서를 무료로 구현할 수 있습니다. CNAME을 활용하면 [!DNL Target] 고객이 ITP 2.1 및 ITP 2.2의 영향을 완화할 수 있습니다.

   CNAME을 활용하지 않는 경우 계정 담당자에게 알리고 Adobe Managed Certificate Program에 등록하여 프로세스를 시작할 [수 있습니다](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program).

ECID 라이브러리 v4.3.0+와 함께 Target JavaScript 라이브러리를 배포하고 Adobe Managed Certificate Program에 등록하여 CNAME을 활용하면 ITP 관련 변경 사항에 대한 장기적이고 강력한 완화 계획을 갖게 됩니다.

As the industry makes strides to create a more secure web for consumers, [!DNL Adobe Target] is absolutely committed to delivering personalized experiences while meeting and exceeding the privacy expectations of visitors. [!DNL Adobe Target] 이미 Apple의 ITP [2.1 및 ITP](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) 2.2에 대한 지원 외에 Google의 SameSite Chrome 정책에 대한 지원을 발표했습니다.

고객 보호를 위한 정책이 지속적으로 발전함에 따라 [!DNL Adobe] 고객은 [!DNL Target]동급 최강의 개인화된 경험을 제공하면서 이러한 이니셔티브를 지속적으로 지원할 것입니다.
