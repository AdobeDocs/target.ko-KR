---
keywords: 타깃팅;eec;시각적 경험 작성기;EEC 문제 해결;문제점 해결
description: 특정 조건에서 Adobe [!DNL Target] EEC(Enhanced Experience Composer)에서 가끔 발생하는 문제를 해결하는 방법을 알아봅니다.
title: 향상된 경험 작성기와 관련된 문제를 해결하려면 어떻게 합니까?
feature: 시각적 경험 작성기(VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: b14c9bb4bc0363c77de084c7ae7110e73c5f2f13
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 51%

---

# [!UICONTROL 향상된 경험 작성기]와 관련된 문제 해결

특정 조건 아래의 [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer](EEC)에서 디스플레이 문제가 발생하는 경우가 있습니다.

## EEC가 공용 IP에서 액세스할 수 없는 내부 QA URL을 로드하지 않습니다. {#section_D29E96911D5C401889B5EACE267F13CF}

이 문제는 다음 IP 주소를 허용 목록에 추가로 해결할 수 있습니다. 이러한 IP 주소는 EEC 프록시에 사용되는 Adobe 서버를 위한 것입니다. 활동 편집에만 필요합니다. 사이트 방문자에게 이러한 IP 주소가 필요하지 허용 목록에추가된 않습니다.

IT 팀에 다음 IP 주소를 허용 목록에 추가하다 지정하도록 요청합니다.

* 52.55.99.45
* 52.51.238.221
* 52.193.67.35

[!DNL Target]에 다음 오류 메시지가 표시될 수 있습니다.

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![](assets/EEC_error.png)

다음은 이 오류 메시지와 상황을 수정할 조치를 볼 수 있는 이유입니다.

* **문제:**[!UICONTROL 웹 사이트 도메인(ISP)에서 고급 경험 작성기를 차단하고 있습니다].

   **해결 방법:** 위에 나열된 IP 주소를 허용 목록에 추가하다 표시합니다.

* **문제: IP 주소** 는 TLS 버전 1.2를 지원하지 허용 목록에추가된 않지만 웹 사이트는 현재 기본 구성 1.2를  [!DNL Target] 사용합니다.  [!DNL Target] 18.4.1(2018년 4월 25일) 이전에는 기본 구성이 지원되는 TLS 1.0이 이전에 지원됩니다. 자세한 내용은  [TLS(전송 레이어 보안) 암호화 변경 사항을 참조하십시오](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

   **해결 방법:**[!UICONTROL (고급 시각적 경험 작성기가 TLS 1.2를 사용하는 사이트의 보안 페이지에 로드되지 않습니다.) 질문을 참조하십시오.]

## EEC가 TLS 1.0를 사용하는 사이트의 보안 페이지에 로드되지 않습니다. (EEC만 해당) {#section_C5B31E3D32A844F68E5A8153BD17551F}

위의 &quot;The [!UICONTROL Enhanced Visual Experience Composer]이(가) 내 사이트의 보안 페이지에서 로드되지 않습니다.&quot;에 설명된 오류 메시지가 나타날 수 있습니다. 위 IP 주소가 TLS 버전 1.2를 지원하지 허용 목록에추가된 않지만 웹 사이트에서 TLS 버전 1.2를 지원하지 않는 경우 [!DNL Target]은(는) 현재 기본 구성인 1.2를 사용합니다. [!DNL Target] 18.4.1(2018년 4월 25일) 이전에는 기본 구성이 지원되는 TLS 1.0을 참조하십시오. 자세한 내용은 [TLS(전송 레이어 보안) 암호화 변경 사항](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

Firefox를 사용하여 웹 사이트에서 TLS 버전을 확인하려면 다음을 수행하십시오(다른 브라우저에도 유사한 단계가 있음).

1. Firefox에서 해당 웹 사이트를 엽니다.
1. 브라우저의 주소 표시줄에 **[!UICONTROL 사이트 정보 표시]** 아이콘을 클릭합니다.

   ![](assets/firefox_more_info.png)

1. **[!UICONTROL 연결 세부 사항 표시]** > **[!UICONTROL 추가 정보]**&#x200B;를 클릭하십시오.

   ![](assets/firefox_more_info_2.png)

1. 기술 세부 사항 아래의 TLS 버전 정보를 검토하십시오.

   ![](assets/firefox_more_info_3.png)

1. 웹 사이트에 TLS 1.0이 표시되는 경우에는 [TLS(전송 계층 보안) 암호화 변경 사항](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451)에서 Target의 TLS 지원 정책에 대한 정보를 참조하십시오. 현재(2018년 9월 12일까지 유효) 상황을 해결하기 위해 TLS 버전 및 도메인을 구성하려면 [고객 지원 센터](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오.

## 프록시가 활성화된 로드할 때 시간 초과 또는 &quot;액세스 거부&quot; 오류가 표시됩니다. (EEC만 해당) {#section_60CBB9022DC449F593606C0E6252302D}

프록시 IP가 사용자 환경에서 차단되지 않았는지 확인하십시오.
