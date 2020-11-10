---
keywords: Overview and Reference
description: Target과 Adobe Campaign 통합을 통해 이메일 컨텐츠를 최적화합니다.
title: Adobe Campaign과 Target 통합
feature: campaign
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 44%

---


# Adobe Campaign과 Target 통합{#integrate-target-with-adobe-campaign}

을 사용하여 이메일 [!DNL Target] 컨텐츠 [!DNL Adobe Campaign] 를 최적화할 수 있습니다.

To optimize your email content--for example, to display different offers for male and female recipients--you can create a redirect offer in [!DNL Target], then use [!DNL Adobe Campaign] to manage the email offers.

이메일이 열리면 통합이 발생합니다. When the customer opens the email, a call is made to [!DNL Target] and a dynamic version of the content appears. 컨텐츠는 모든 브라우저에서 지원되는 정적 이미지로 구성됩니다. [!DNL Target] 대상 또는 세션 수준에서 오퍼에 대한 반응을 추적하고 해당 데이터를 보고서에서 사용할 수 [!DNL Target] 있습니다.

Target은 다음과 같은 데이터를 추적할 수 있습니다.

* 사용자 에이전트
* IP 주소
* 지리적 위치
* Target에서 방문자 ID와 연관된 세그먼트(법적 승인 조건)
* Data from [!DNL Campaign] Datamart

몇 가지 제한 사항은 다음과 같습니다.

* 이미지만 사용할 수 있기 때문에 컨텐츠는 개인화할 수 없습니다.
* 추적은 통합되지 않습니다 [!DNL Adobe Campaign].
* 사용자 경험이 통합되지 않습니다.

   You must use both [!DNL Target] and [!DNL Campaign] to set up different parts of the integration:

   * The rawbox and the experience in [!DNL Target]
   >[!NOTE]
   >
   >rawbox를 사용하고 [!DNL Target]있는 경우 Target에 mbox 호출을 전송할 수 있는 호스트를 지정하는 허용 목록 [만들기 아래의 중요 보안 알림을 참조하십시오](/help/administrating-target/hosts.md#allowlist).

   * 전달 [!DNL Campaign]



## 시작하기 전에 {#section_FF19BF1BCA064260930BF6C141313B0E}

Before you use [!DNL Adobe Campaign] to set up your targeted email offers, set up the following in [!DNL Target]:

* Two or more [!DNL Target] redirect offers

   See [Create redirect offer](/help/c-experiences/c-manage-content/offer-redirect.md).
* 각 오퍼 및 원하는 [성공 지표](/help/c-activities/r-success-metrics/success-metrics.md)에 대한 경험이 포함된 Target 활동

   [URL로 리디렉션](/help/c-experiences/c-visual-experience-composer/redirect-offer.md)을 참조하십시오.

Start the activity in [!DNL Target] before setting up the [!DNL Campaign] portion of the integration.

## Adobe Campaign 이메일에 Target 오퍼 포함 {#section_B201BBE27A704E18AF0D553F35695837}

1. 이메일을 작성합니다 [!DNL Adobe Campaign].
1. 이메일 속성에서 **[!UICONTROL 포함]** > **[!UICONTROL Adobe Target에서 제공하는 동적 이미지]**&#x200B;를 클릭합니다.
1. 공유 자산에서 기본 이미지를 선택합니다.
1. 위치(rawbox)를 지정합니다.
1. 수신자의 성별 등과 같은 기타 의사결정 매개 변수를 추가합니다.
1. 각 오퍼의 수신자를 한 명 이상 선택하고(이 경우에는 여성 및 남성) 이메일을 미리 봅니다.
1. In [!DNL Campaign], define the [!DNL Target] Edge server you are using to control the activity and the name of the tenant.
1. Specify the external account used for the [!DNL Adobe Experience Cloud] so you can access the resources in the [!DNL Experience Cloud].

For more information, refer to the [!DNL Adobe Campaign] documentation.
