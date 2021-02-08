---
keywords: apple;ITP;지능적 추적 방지;experience cloud id;ecid
description: Safari 사용자의 개인 정보를 보호하려는 Adobe Target과 Apple Intelligent Tracking Prevention(ITP) 이니셔티브의 영향에 대해 알아봅니다.
title: Target은 Apple ITP 지원을 어떻게 처리합니까?
feature: Privacy & Security
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 51%

---


# Apple ITP(Intelligent Tracking Prevention) 2.x

ECID(Experience Cloud ID) 라이브러리 4.3을 통해 Apple의 ITP 2.x에 대한 [!DNL Adobe Target] 지원에 대한 정보입니다.

ITP(Intelligent Tracking Prevention)는 Safari 사용자의 개인 정보를 보호하는 Apple의 이니셔티브입니다. 2017년에 있었던 ITP의 첫 번째 릴리스에서는 타사 쿠키의 사용을 타깃팅했습니다. 실제로 Apple은 타사 쿠키를 완전히 차단했습니다. 타사 쿠키는 일반적으로 방문자를 추적하고 방문자 데이터를 수집하는 데 사용되기 때문에 광고 기술 및 마테크(martech) 기업의 심각한 문제 요소였습니다. 이제 Apple은 Safari 내에서 타사 쿠키가 사용되는 방법에 대해 제한 사항을 적용하려고 합니다.

이러한 ITP 버전에는 다음과 같은 제한 사항이 포함됩니다.

| 버전 | 세부 사항 |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | `document.cookie` API를 사용하여 브라우저에 배치된 클라이언트측 쿠키가 7일 만료로 설정됩니다.<br>2019년 2월 21일 릴리스 |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | 7일 만료 시간을 1일로 크게 단축했습니다.<br>2019년 4월 24일 릴리스 |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-2-3/) | localStorage를 채택하거나 JavaScript `Document.referrer property` 사용과 같은 여러 해결 방법을 제거했습니다.<br>2019년 9월 23일 릴리스. |

## Adobe Target 고객에게 어떤 영향을 미칩니까? {#impact}

[!DNL Target]은 [!DNL Target]이 방문자에게 실시간 개인화를 제공할 수 있도록 페이지에 배포할 JavaScript 라이브러리를 제공합니다. 3개의 target JavaScript 라이브러리([at. js 1.`document.cookie` API를 통해 방문자의 브라우저에 클라이언트측 [!DNL Target] 쿠키를 배치하는 x, at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) 및 [mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)). 그 결과, [!DNL Target] 쿠키는 Apple의 ITP 2.x의 영향을 받으며, 7일(ITP 2.1의 경우) 후(ITP 2.2 및 ITP 2.3의 경우) 후에 만료됩니다.

Apple ITP 2.x는 다음 영역에서 [!DNL Target]에 영향을 줍니다.

| 영향 | 세부 사항 |
| --- | --- |
| 고유 방문자 수의 잠재적 증가 | 만료 기간이 7일(ITP 2.1 포함) 및 하루(ITP 2.2 및 ITP 2.3 포함)로 설정되었기 때문에 Safari 브라우저에서 고유 방문자 수가 증가하는 것을 볼 수 있습니다. 방문자가 7일(ITP 2.1) 또는 1일(ITP 2.2 및 ITP 2.3) 후에 도메인을 다시 방문하면 [!DNL Target]은 만료된 쿠키 대신 도메인에 새로운 [!DNL Target] 쿠키를 배치해야 합니다. 사용자가 동일하지만 새 [!DNL Target] 쿠키는 새 고유 방문자로 해석됩니다. |
| [!DNL Target] 활동에 대한 전환 기간 감소 | [!DNL Target] 활동의 방문자 프로필에는 의사 결정에 대해 전환 기간이 감소될 수 있습니다. [!DNL Target] 쿠키는 방문자를 식별하고 개인화를 위해 사용자 프로필 속성을 저장하는 데 사용됩니다. [!DNL Target] 쿠키는 7일(ITP 2.1) 또는 1일(ITP 2.2 및 2.3) 이후에 Safari에서 만료될 수 있으므로 삭제된 [!DNL Target] 쿠키에 연결된 사용자 프로필 데이터를 의사 결정에 사용할 수 없습니다. |
| 3rdPartyID를 기반으로 하는 프로필 스크립트 | 만료 기간이 7일(ITP 2.1 포함) 및 하루(ITP 2.2 및 ITP 2.3 포함)로 설정되므로 3rdPartyID 쿠키를 기반으로 하는 [프로필 스크립트](/help/c-target/c-visitor-profile/profile-parameters.md)가 만료 시 작동하지 않습니다. |
| iOS 장치의 QA/미리 보기 URL | 만료 기간이 7일(ITP 2.1 포함) 및 1일(ITP 2.2 및 ITP 2.3 포함)로 설정되기 때문에 URL이 3rdPartyID 쿠키를 기반으로 하므로 [QA/미리 보기 URL](/help/c-activities/c-activity-qa/activity-qa.md)이 만료 시 작동하지 않습니다. |

## 현재 [!DNL Target] 구현이 영향을 받습니까?

Safari 브라우저에서 [!DNL Target] JavaScript 라이브러리가 있는 웹 사이트로 이동합니다. `analytics.company.com` 등 CNAME 컨텍스트에서 설정된 [!DNL Target] 쿠키가 표시되는 경우 ITP 2.x의 영향을 받지 않습니다.

Target JavaScript 라이브러리 외에 ECID(Experience Cloud ID) 라이브러리를 사용하는 경우, 구현은 [Safari ITP 2.1이 Adobe Experience Cloud 및 Experience Platform 고객에게 미치는 영향](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac)에 나열된 방식으로 영향을 받게 됩니다.

## 향후 ITP 2.x 릴리스가 Target에 미치는 영향을 어떻게 해결할 수 있습니까?

향후 ITP 2.x 릴리스가 Target에 미치는 영향을 완화하려면 다음 작업을 완료하십시오.

1. 페이지에 ECID(Experience Cloud ID) 라이브러리를 배포합니다.

   ECID 라이브러리는 Experience Cloud 핵심 솔루션에 대한 개인 식별 프레임워크를 활성화합니다. ECID 라이브러리를 사용하면 영구 및 고유 식별자를 할당하여 다른 Experience Cloud 솔루션에서 동일한 사이트 방문자와 해당 데이터를 식별할 수 있습니다. ECID 라이브러리는 자주 업데이트되므로 구현에 영향을 주는 모든 ITP 관련 변경 사항을 완화할 수 있습니다.

   ITP 2.x의 경우 완화를 위해 [ECID 라이브러리 4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html)을 사용해야 합니다.

1. Adobe의 CNAME을 사용하고 Adobe Analytics의 관리 인증서 프로그램에 등록합니다.

   ECID Library 4.3.0+를 설치한 후 Adobe Analytics의 CNAME 및 관리 인증서 프로그램을 활용할 수 있습니다. 이 프로그램을 사용하면 자사 쿠키에 대한 자사 인증서를 무료로 구현할 수 있습니다. CNAME을 활용하면 [!DNL Target] 고객이 ITP 2.x의 영향을 완화할 수 있습니다.

   CNAME을 활용하지 않는 경우 계정 담당자에게 알리고 [Adobe 관리 인증서 프로그램](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program)에 등록하여 프로세스를 시작할 수 있습니다.

CNAME을 활용하기 위해 Target JavaScript 라이브러리를 ECID Library v4.3.0+와 함께 배포하고 Adobe 관리 인증서 프로그램에 등록하면, ITP 관련 변경에 대한 강력하고 장기적인 완화 계획을 갖게 됩니다.

업계에서 소비자를 위해 보다 안전한 웹을 만들기 위해 노력함에 따라 [!DNL Adobe Target]은 방문자의 개인 정보 보호 기대치를 충족시키는 동시에 개인화된 경험을 제공하기 위해 노력을 아끼지 않고 있습니다. [!DNL Adobe Target] 이미 Apple의 ITP 2.x 지원 외에  [Google의 SameSite Chrome ](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) Policy에 대한 지원을 발표했습니다.

고객을 보호하기 위한 정책이 지속적으로 발전함에 따라 [!DNL Adobe]는 [!DNL Target]에서 이러한 이니셔티브를 지속적으로 지원하고 고객이 최상의 개인화된 경험을 제공할 수 있도록 지원할 것입니다.
