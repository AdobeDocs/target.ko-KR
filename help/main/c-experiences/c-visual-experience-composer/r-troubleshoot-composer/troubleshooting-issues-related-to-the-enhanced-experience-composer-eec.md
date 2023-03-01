---
keywords: 타깃팅;eec;시각적 경험 작성기;EEC 문제 해결;문제점 해결
description: Adobe에서 가끔 발생하는 문제를 해결하는 방법 알아보기 [!DNL Target] 특정 조건에서 EEC(고급 경험 작성기)를 참조하십시오.
title: 고급 경험 작성기 관련 문제를 해결하려면 어떻게 합니까?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: 3ac61272ee1ccd72a8670966f181e7798cbe9f76
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 41%

---

#  [!UICONTROL Enhanced Experience Composer] 관련 문제 해결

때때로 다음과 같은 경우에 표시 문제가 발생합니다. [!DNL Adobe Target] [!UICONTROL 향상된 경험 작성기] (EEC) 특정 조건에서

## EEC가 공용 IP에서 액세스할 수 없는 내부 QA URL을 로드하지 않습니다. {#section_D29E96911D5C401889B5EACE267F13CF}

이 문제는 다음 IP 주소를 허용 목록에 추가 하여 해결할 수 있습니다. 이러한 IP 주소는 EEC 프록시에 사용되는 Adobe 서버용입니다. 활동 편집에만 필요합니다. 사이트 방문자는 이러한 IP 주소를 허용 목록에추가된으로 사용할 필요가 없습니다.

허용 목록에 추가하다 IT 팀에 다음 IP 주소를 요청하십시오.

* 34.253.100.20
* 34.248.100.23
* 52.49.228.246
* 54.205.42.123
* 107.22.177.39
* 52.201.5.105
* 52.193.211.177
* 18.180.24.249
* 52.194.154.154

에 다음 오류 메시지가 표시될 수 있습니다 [!DNL Target]:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![EEC_error 이미지](assets/EEC_error.png)

다음은 이 오류 메시지와 상황을 수정할 조치를 볼 수 있는 이유입니다.

* **문제:**[!UICONTROL 웹 사이트 도메인(ISP)에서 고급 경험 작성기를 차단하고 있습니다].

   **해결 방법:** 허용 목록에 추가하다 위에 나열된 IP 주소입니다.

* **문제:** IP 주소는 허용 목록에추가된이지만 웹 사이트에서 TLS 버전 1.2를 지원하지 않습니다. [!DNL Target] 는 현재 1.2의 기본 구성을 사용합니다. 다음 이전 [!DNL Target] 18.4.1(2018년 4월 25일), 기본 구성은 TLS 1.0을 지원합니다. 자세한 내용은 [TLS(전송 계층 보안) 암호화 변경 사항](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/){target=_blank}.

   **해결 방법:**[!UICONTROL (고급 시각적 경험 작성기가 TLS 1.2를 사용하는 사이트의 보안 페이지에 로드되지 않습니다.) 질문을 참조하십시오.]

## EEC가 TLS 1.0를 사용하는 사이트의 보안 페이지에 로드되지 않습니다. (EEC만 해당) {#section_C5B31E3D32A844F68E5A8153BD17551F}

위에서 설명한 &quot;The [!UICONTROL 향상된 시각적 경험 작성기] 내 사이트의 보안 페이지에 로드되지 않습니다.&quot; 위의 IP 주소가 허용 목록에추가된이지만 웹 사이트에서 TLS 버전 1.2를 지원하지 않는 경우입니다. [!DNL Target] 는 현재 1.2의 기본 구성을 사용합니다. 다음 이전 [!DNL Target] 18.4.1(2018년 4월 25일), 기본 구성은 TLS 1.0을 지원합니다. 자세한 내용은 [TLS(전송 계층 보안) 암호화 변경 사항](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/){target=_blank}.

Firefox를 사용하여 웹 사이트에서 TLS 버전을 확인하려면 다음을 수행하십시오(다른 브라우저에도 유사한 단계가 있음).

1. Firefox에서 해당 웹 사이트를 엽니다.
1. 브라우저의 주소 표시줄에 **[!UICONTROL 사이트 정보 표시]** 아이콘을 클릭합니다.

   ![firefox_more_info 이미지](assets/firefox_more_info.png)

1. **[!UICONTROL 연결 세부 사항 표시]** > **[!UICONTROL 추가 정보]**&#x200B;를 클릭하십시오.

   ![firefox_more_info_2 이미지](assets/firefox_more_info_2.png)

1. 기술 세부 사항 아래의 TLS 버전 정보를 검토하십시오.

   ![firefox_more_info_3 이미지](assets/firefox_more_info_3.png)

1. 웹 사이트에서 TLS 1.0이 표시되는 경우 다음을 참조하십시오. [TLS(전송 계층 보안) 암호화 변경 사항](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/){target=_blank} for information about Target's TLS support policy. To remedy the situation for now (valid until September 12, 2018){target=_blank}, 다음으로 연결 [고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) TLS 버전 및 도메인을 사용하여 구성합니다.

## 프록시가 활성화된 로드할 때 시간 초과 또는 &quot;액세스 거부&quot; 오류가 표시됩니다. (EEC만 해당) {#section_60CBB9022DC449F593606C0E6252302D}

프록시 IP가 사용자 환경에서 차단되지 않았는지 확인하십시오.
