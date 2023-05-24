---
keywords: 개요 및 참조
description: Adobe 사용 방법 알아보기 [!DNL Target] 이메일 콘텐츠를 최적화하기 위해 Adobe Campaign을 사용합니다.
title: 통합 방법 [!DNL Target] Adobe Campaign과 함께?
feature: Integrations
exl-id: 605b8fe4-e32f-43bc-9131-245008b655e1
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 35%

---

# 통합 [!DNL Target] Adobe Campaign 사용

사용 [!DNL Target] 포함 [!DNL Adobe Campaign] 이메일 콘텐츠를 최적화합니다.

이메일 콘텐츠를 최적화하려면에서 리디렉션 오퍼를 만들면 됩니다. [!DNL Target], 그런 다음 사용 [!DNL Adobe Campaign] 이메일 오퍼를 관리합니다. 예를 들어, 남성 수신자와 여성 수신자에 대해 서로 다른 오퍼를 표시할 수 있습니다.

이메일이 열리면 통합이 발생합니다. 고객이 이메일을 열면 [!DNL Target] 그리고 콘텐츠의 동적 버전이 나타납니다. 컨텐츠는 모든 브라우저에서 지원되는 정적 이미지로 구성됩니다. [!DNL Target] 대상자 또는 세션 수준에서 오퍼에 대한 반응을 추적하며 해당 데이터는에서 사용할 수 있습니다. [!DNL Target] 보고서.

[!DNL Target] 은 다음 데이터를 추적할 수 있습니다.

* 사용자 에이전트
* IP 주소
* 지리적 위치
* 에서 방문자의 ID와 연결된 세그먼트 [!DNL Target] (법적 승인 대상)
* 데이터 출처: [!DNL Campaign] 데이터마트

몇 가지 제한 사항은 다음과 같습니다.

* 이미지만 사용할 수 있기 때문에 컨텐츠는 개인화할 수 없습니다.
* 추적이 통합되지 않음 [!DNL Adobe Campaign].
* 사용자 경험이 통합되지 않습니다.

둘 다 사용 [!DNL Target] 및 [!DNL Campaign] 통합의 여러 부분을 설정하려면 다음을 수행하십시오.

* 원시 상자 및 의 경험 [!DNL Target]

>[!NOTE]
>
>rawbox 및 [!DNL Target]을 사용하는 경우 [Target으로 mbox 호출을 보내도록 승인된 호스트를 지정하는 허용 목록 생성](/help/main/administrating-target/hosts.md#allowlist) 아래의 중요 보안 알림을 참조하십시오.

* 의 게재 [!DNL Campaign]

## 시작하기 전에 {#section_FF19BF1BCA064260930BF6C141313B0E}

사용하기 전에 [!DNL Adobe Campaign] 타겟팅된 이메일 오퍼를 설정하려면 다음에서 다음을 설정하십시오. [!DNL Target]:

* 2개 이상 [!DNL Target] 리디렉션 오퍼

   다음을 참조하십시오 [리디렉션 오퍼 만들기](/help/main/c-experiences/c-manage-content/offer-redirect.md).

* A [!DNL Target] 각 오퍼 및 원하는 오퍼에 대한 경험이 포함된 활동 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md).

   [URL로 리디렉션](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md)을 참조하십시오.

에서 활동 시작 [!DNL Target] 을(를) 설정하기 전에 [!DNL Campaign] 부분 통합을 참조하십시오.

## 포함 [!DNL Target] 의 오퍼 [!DNL Adobe Campaign] 이메일 {#section_B201BBE27A704E18AF0D553F35695837}

1. 에서 이메일 만들기 [!DNL Adobe Campaign].
1. 이메일 속성에서 **[!UICONTROL 포함]** > **[!UICONTROL Adobe Target에서 제공하는 동적 이미지]**&#x200B;를 클릭합니다.
1. 공유 자산에서 기본 이미지를 선택합니다.
1. 위치(rawbox)를 지정합니다.
1. 수신자의 성별 등과 같은 기타 의사결정 매개 변수를 추가합니다.
1. 각 오퍼의 수신자를 한 명 이상 선택하고(이 경우에는 여성 및 남성) 이메일을 미리 봅니다.
1. 위치 [!DNL Campaign], 다음을 정의합니다. [!DNL Target] 활동 및 테넌트의 이름을 제어하는 데 사용하는 에지 서버입니다.
1. 에 사용되는 외부 계정 지정 [!DNL Adobe Experience Cloud] 의 리소스에 액세스할 수 있습니다. [!DNL Experience Cloud].

자세한 내용은 [!DNL Adobe Campaign] 설명서를 참조하십시오.

## 비디오: 통합 [!DNL Target] 포함 [!DNL Campaign]

>[!VIDEO](https://video.tv.adobe.com/v/35149)
