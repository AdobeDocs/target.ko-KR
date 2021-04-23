---
keywords: 개요 및 참조
description: Adobe Campaign에서 Adobe [!DNL Target] 을 사용하여 이메일 컨텐츠를 최적화하는 방법을 알아봅니다.
title: Adobe Campaign과 [!DNL Target] 을 통합하려면 어떻게 합니까?
feature: 통합
exl-id: 605b8fe4-e32f-43bc-9131-245008b655e1
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 37%

---

# Adobe Campaign과 [!DNL Target] 통합

[!DNL Adobe Campaign]과 함께 [!DNL Target]을 사용하여 이메일 컨텐츠를 최적화합니다.

이메일 컨텐츠를 최적화하려면(예: 여성 수신자와 남성 수신자에 대해 다른 오퍼를 표시하는 경우) [!DNL Target]에서 리디렉션 오퍼를 만든 다음 [!DNL Adobe Campaign]을 사용하여 이메일 오퍼를 관리할 수 있습니다.

이메일이 열리면 통합이 발생합니다. 고객이 이메일을 열면 [!DNL Target]에 대한 호출이 수행되고 동적 버전의 컨텐츠가 표시됩니다. 컨텐츠는 모든 브라우저에서 지원되는 정적 이미지로 구성됩니다. [!DNL Target] 대상 또는 세션 수준에서 오퍼에 대한 반응을 추적하고 해당 데이터를 보고서에서 사용할 수  [!DNL Target] 있습니다.

Target은 다음과 같은 데이터를 추적할 수 있습니다.

* 사용자 에이전트
* IP 주소
* 지리적 위치
* Target에서 방문자 ID와 연관된 세그먼트(법적 승인 조건)
* [!DNL Campaign] Datamart의 데이터

몇 가지 제한 사항은 다음과 같습니다.

* 이미지만 사용할 수 있기 때문에 컨텐츠는 개인화할 수 없습니다.
* 추적은 [!DNL Adobe Campaign]에 통합되지 않습니다.
* 사용자 경험이 통합되지 않습니다.

   통합의 다른 부분을 설정하려면 [!DNL Target] 및 [!DNL Campaign] 모두를 사용해야 합니다.

   * [!DNL Target]의 rawbox 및 경험
   >[!NOTE]
   >
   >rawbox 및 [!DNL Target]을 사용하는 경우 Target](/help/administrating-target/hosts.md#allowlist)에 mbox 호출을 전송할 수 있는 호스트를 지정하는 허용 목록 만들기 아래의 중요 보안 알림을 참조하십시오.[

   * [!DNL Campaign]의 배달



## 시작하기 전에 {#section_FF19BF1BCA064260930BF6C141313B0E}

[!DNL Adobe Campaign]을(를) 사용하여 타깃팅된 이메일 오퍼를 설정하기 전에 [!DNL Target]에서 다음 사항을 설정하십시오.

* 2개 이상의 [!DNL Target] 리디렉션 오퍼

   [리디렉션 오퍼 만들기](/help/c-experiences/c-manage-content/offer-redirect.md)를 참조하십시오.
* 각 오퍼 및 원하는 [성공 지표](/help/c-activities/r-success-metrics/success-metrics.md)에 대한 경험이 포함된 Target 활동

   [URL로 리디렉션](/help/c-experiences/c-visual-experience-composer/redirect-offer.md)을 참조하십시오.

통합의 [!DNL Campaign] 부분을 설정하기 전에 [!DNL Target]에서 활동을 시작합니다.

## Adobe Campaign 이메일 {#section_B201BBE27A704E18AF0D553F35695837}에 [!DNL Target] 오퍼 포함

1. [!DNL Adobe Campaign]에서 이메일을 만듭니다.
1. 이메일 속성에서 **[!UICONTROL 포함]** > **[!UICONTROL Adobe Target에서 제공하는 동적 이미지]**&#x200B;를 클릭합니다.
1. 공유 자산에서 기본 이미지를 선택합니다.
1. 위치(rawbox)를 지정합니다.
1. 수신자의 성별 등과 같은 기타 의사결정 매개 변수를 추가합니다.
1. 각 오퍼의 수신자를 한 명 이상 선택하고(이 경우에는 여성 및 남성) 이메일을 미리 봅니다.
1. [!DNL Campaign]에서 활동 및 임차인 이름을 제어하는 데 사용하는 [!DNL Target] Edge Server를 정의합니다.
1. [!DNL Experience Cloud]의 리소스에 액세스할 수 있도록 [!DNL Adobe Experience Cloud]에 사용되는 외부 계정을 지정합니다.

자세한 내용은 [!DNL Adobe Campaign] 설명서를 참조하십시오.
