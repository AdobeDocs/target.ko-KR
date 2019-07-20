---
description: Target과 Adobe Campaign 통합을 통해 이메일 컨텐츠를 최적화합니다.
keywords: 개요 및 참조
seo-description: Target과 Adobe Campaign 통합을 통해 이메일 컨텐츠를 최적화합니다.
seo-title: Adobe Campaign과 Target 통합
solution: Target
title: Adobe Campaign과 Target 통합
topic: Standard
uuid: 1a5b70e6-d501-4b52-bec8-4ae2c419d331
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Adobe Campaign과 Target 통합{#integrate-target-with-adobe-campaign}

Target과 Adobe Campaign 통합을 통해 이메일 컨텐츠를 최적화합니다.

이메일 컨텐츠를 최적화하려면(예: 여성 수신자와 남성 수신자에게 각각 다른 오퍼 표시) Target에서 리디렉션 오퍼를 만든 다음 Adobe Campaign을 사용하여 이메일 오퍼를 관리할 수 있습니다.

이메일이 열리면 통합이 발생합니다. 고객이 이메일을 열면 Target에 호출이 수행되고 동적 버전의 컨텐츠가 나타납니다. 컨텐츠는 모든 브라우저에서 지원되는 정적 이미지로 구성됩니다. Target은 대상 또는 세션 수준에서 오퍼에 대한 반응을 추적하며 해당 데이터는 Target 보고서에서 사용할 수 있습니다.

Target은 다음과 같은 데이터를 추적할 수 있습니다.

* 사용자 에이전트
* IP 주소
* 지리적 위치
* Target에서 방문자 ID와 연관된 세그먼트(법적 승인 조건)
* Campaign Datamart의 데이터

몇 가지 제한 사항은 다음과 같습니다.

* 이미지만 사용할 수 있기 때문에 컨텐츠는 개인화할 수 없습니다.
* Adobe Campaign에서는 추적이 통합되지 않습니다.
* 사용자 경험이 통합되지 않습니다.

   Target 및 Campaign 둘 다 사용하여 통합의 여러 부분을 설정해야 합니다.

   * Target의 rawbox 및 경험
   * Campaign에서의 전달

## 시작하기 전에 {#section_FF19BF1BCA064260930BF6C141313B0E}

Adobe Campaign을 사용하여 타깃팅된 이메일 오퍼를 설정하기 전에 Target에서 다음 사항을 설정하십시오.

* 둘 이상의 Target 리디렉션 오퍼

   [리디렉션 오퍼 만들기](https://marketing.adobe.com/resources/help/en_US/target/target/t_offer_redirect.html)를 참조하십시오.
* 각 오퍼 및 원하는 [성공 지표](https://marketing.adobe.com/resources/help/en_US/target/target/r_success_metrics.html)에 대한 경험이 포함된 Target 활동

   [URL로 리디렉션](https://marketing.adobe.com/resources/help/en_US/target/target/t_redirect_offer.html)을 참조하십시오.

통합에서 Campaign 부분을 설정하기 전에 Target에서 활동을 시작합니다.

## Adobe Campaign 이메일에 Target 오퍼 포함 {#section_B201BBE27A704E18AF0D553F35695837}

1. Adobe Campaign에서 이메일을 작성합니다.
1. 이메일 속성에서 **[!UICONTROL 포함]** &gt; **[!UICONTROL Adobe Target에서 제공하는 동적 이미지]**&#x200B;를 클릭합니다.
1. 공유 자산에서 기본 이미지를 선택합니다.
1. 위치(rawbox)를 지정합니다.
1. 수신자의 성별 등과 같은 기타 의사결정 매개 변수를 추가합니다.
1. 각 오퍼의 수신자를 한 명 이상 선택하고(이 경우에는 여성 및 남성) 이메일을 미리 봅니다.
1. Campaign에서 활동 및 임차인 이름을 제어하기 위해 사용할 Target Edge 서버를 정의합니다.
1. Experience Cloud의 리소스에 액세스할 수 있도록 Experience Cloud에 사용되는 외부 계정을 지정합니다.

자세한 내용은 Adobe Campaign 문서를 참조하십시오.
