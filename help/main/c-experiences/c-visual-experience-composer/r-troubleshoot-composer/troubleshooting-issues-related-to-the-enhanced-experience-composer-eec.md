---
keywords: 타깃팅;eec;시각적 경험 작성기;EEC 문제 해결;문제점 해결
description: 특정 조건에서 [!DNL Adobe Target] [!UICONTROL 고급 경험 작성기] (EEC)에서 발생하는 문제를 해결하는 방법에 대해 알아봅니다.
title: '[!UICONTROL 향상된 경험 작성기]와 관련된 문제를 해결하려면 어떻게 합니까?'
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
TQID: 'https://experienceleague.adobe.com/Yan2cKWjs-u9JHQzT-PiRAFdxUJa1JSHS-fT68yxIjg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 5%
---
# [!UICONTROL 향상된 경험 작성기]와 관련된 문제 해결 {#eec-issues}

>[!BEGINSHADEBOX]

**이 페이지에서:** EEC 프록시의 IP 주소가 차단되어 로드되지 않는 페이지와 같이 EEC(Enhanced Experience Composer **)에만 영향을 주는 문제를 해결하는 방법을 알아봅니다.**

>[!ENDSHADEBOX]

특정 조건에서 [!DNL Adobe Target] **[!UICONTROL 고급 경험 작성기]**(EEC)에 문제가 발생하는 경우가 있습니다. 다음 항목에서는 EEC에만 영향을 주는 문제와 해결 방법을 설명합니다.

## EEC 프록시 허용 목록 {#eec-ip-addresses}

EEC가 공용 IP 주소에서 액세스할 수 없는 내부 QA URL을 로드하지 않습니다. 허용 목록에 추가 EEC 프록시에 사용되는 [!DNL Adobe] 서버의 IP 주소를 사용하면 이 문제가 해결됩니다. 이러한 IP 주소는 활동 편집에만 필요하며 사이트 방문자는 허용 목록에추가된으로 필요하지 않습니다. IT 팀에 다음 IP 주소를 요청하십시오.

### 미국(va7)

```
40.70.154.136/29
52.254.106.240/28
52.254.106.160/28
52.254.107.16/28
20.186.185.181
20.22.83.112
20.186.185.227
52.254.106.192/28
52.254.106.0/28
52.254.107.128/28
52.254.107.80/28
52.254.106.176/28
52.254.107.32/28
52.254.105.192/28
52.254.107.64/28
52.254.106.208/28
52.254.107.0/28
52.254.106.224/28
20.14.241.153
20.186.185.239
4.152.211.251
52.254.107.144/28
52.254.106.144/28
```

### EMEA(nld2)

```
51.138.17.16/28
51.138.17.48/28
51.138.16.128/28
51.138.17.32/28
51.138.16.240/28
51.138.17.112/28
51.138.16.160/28
51.138.16.208/28
51.138.17.80/28
51.138.17.0/28
51.138.17.96/28
51.138.16.144/28
20.31.145.248
20.126.189.248
51.138.16.224/28
51.138.16.192/28
51.138.12.94
51.138.12.11
51.138.16.176/28
51.138.12.100
51.138.17.64/28
51.138.12.160/28
```

### APAC(호주)

```
20.43.104.160/28
20.227.35.177
20.40.188.227
20.43.104.112/28
20.43.104.128/28
20.43.104.144/28
20.40.188.166
20.53.206.128
20.43.104.80/28
20.43.104.16/28
20.43.105.48/28
20.43.104.96/28
20.43.104.48/28
20.40.188.194
20.43.104.32/28
20.40.191.224/28
20.43.105.16/28
20.40.191.96/28
20.43.104.176/28
20.40.191.240/28
20.43.104.64/28
20.43.105.32/28
20.43.104.192/28
20.43.105.0/28
20.43.104.0/28
```

### 기존 IP 주소

다음 레거시 IP 주소는 추후 공지가 있을 때까지 계속 허용 목록에추가된으로 제공되어야 합니다.

```
34.254.77.200
54.73.207.147
54.229.152.123
3.224.194.242
54.90.51.39
34.228.136.112
54.150.116.11
18.178.142.8
54.199.107.77
99.80.139.221
54.78.56.224
54.247.179.246
54.80.219.243
34.201.235.54
54.196.224.236
35.75.212.45
52.199.184.130
18.180.161.176
```

+++ EEC는 웹 사이트 도메인이 차단한다는 오류 메시지를 표시합니다

다음 오류 메시지가 [!DNL Target]에 표시될 수 있습니다.

`Error: Your website domain (ISP) is blocking the Enhanced Experience Composer. You can allowlist the Enhanced Experience Composer's IP addresses or turn off Enhanced Experience Composer in Configure > Page Delivery menu.`

![경험 작성기에서 웹 사이트 도메인(ISP)이 향상된 경험 작성기를 차단하고 있다는 오류 메시지와 함께 [페이지 전달 구성] 메뉴에서 IP 주소 허용 목록 또는 작성기 끄기 제안 메시지가 표시됩니다](assets/EEC_error.png)

이 오류 메시지의 원인은 두 가지입니다.

* 웹 사이트 도메인(ISP)은 EEC를 차단합니다. 문제를 해결하려면 [EEC 프록시의 IP 주소 허용 목록](#eec-ip-addresses)에 나열된 IP 주소를 테스트합니다.
* IP 주소는 허용 목록에추가된으로 제공되지만 웹 사이트에서 TLS 1.2를 지원하지 않습니다. 문제를 해결하려면 다음 항목을 참조하십시오.

+++

+++ EEC가 TLS 1.0을 사용하는 사이트의 보안 페이지에 로드되지 않습니다

IP 주소가 허용 목록에추가된이지만 웹 사이트에서 TLS 1.2를 지원하지 않는 경우에는 이전 항목에 설명된 오류 메시지가 표시될 수 있습니다. [!DNL Target]은(는) 현재 버전 1.2를 기본 구성으로 사용합니다. [!DNL Target] 18.4.1(2018년 4월 25일) 이전에 기본 구성이 TLS 1.0을 지원했습니다. 자세한 내용은 [TLS(Transport Layer Security) 암호화 변경](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}을 참조하십시오.

Firefox에서 웹 사이트의 TLS 버전을 확인하려면(다른 브라우저도 유사한 단계를 수행함) 다음을 수행하십시오.

1. Firefox에서 해당 웹 사이트를 엽니다.
1. 브라우저의 주소 표시줄에 **[!UICONTROL 사이트 정보 표시]** 아이콘을 클릭합니다.

   ![URL 왼쪽에 사이트 정보 표시 아이콘이 강조 표시된 Firefox 주소 표시줄](assets/firefox_more_info.png)

1. **[!UICONTROL 연결 세부 사항 표시]** > **[!UICONTROL 추가 정보]**&#x200B;를 클릭하십시오.

   ![보안 연결 옆에 연결 정보 표시 화살표가 강조 표시된 Firefox 사이트 정보 패널](assets/firefox_more_info_2.png)

1. **[!UICONTROL 기술 세부 정보]**&#x200B;에서 TLS 버전 정보를 검사합니다.

   ![Firefox 페이지 정보 창, 보안 탭(기술 세부 정보 아래에 TLS 버전이 강조 표시됨)에서 다음을 수행합니다](assets/firefox_more_info_3.png)

1. 웹 사이트에서 TLS 1.0이 표시되는 경우 [!DNL Target]의 TLS 지원 정책에 대한 자세한 내용은 [TLS(전송 계층 보안) 암호화 변경 사항](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}을 참조하십시오. 현재(2018년 9월 12일까지 유효) 상황을 해결하기 위해 TLS 버전 및 도메인을 구성하려면 [고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오.

+++

+++ 프록시가 활성화된 사이트가 로드될 때 시간 초과 또는 &quot;액세스 거부&quot; 오류가 표시됩니다.

프록시 IP 주소가 환경에서 차단되지 않았는지 확인하십시오. [EEC 프록시의 IP 주소 목록](#eec-ip-addresses)에 주소가 나열되어 있습니다.

+++
