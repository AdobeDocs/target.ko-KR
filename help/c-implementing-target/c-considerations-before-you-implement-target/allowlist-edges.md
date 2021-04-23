---
keywords: 구현;허용 목록;흰색 목록;허용 목록에 추가하다허용 목록;가장자리;가장자리;implementation;implementation;whitelist;white list;;edge;edges
description: Adobe [!DNL Target] 가장자리허용 목록에 추가하다를 표시하는 데 도움이 되는 호스트 목록을 봅니다(최종 사용자의 최적 응답 시간을 보장하는 지리적으로 분산된 서비스 노드).
title: '가장자리 노드허용 목록에 추가하다는 어떻게 합니까? [!DNL Target] '
feature: 개인 정보 및 보안
role: Developer
exl-id: 2d8399b9-eec8-40b0-8b35-2812f83ff4dc
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 6%

---

# 허용 목록에 추가하다 [!DNL Target] 에지 노드

[!DNL Adobe Target] 가장자리를 허용 목록에 추가하다 표시하는 데 도움이 되는 최신 호스트 목록 및 정보.

에지(edge)는 컨텐츠를 요청하는 최종 사용자가 어디에 있든지 상관없이 최적의 응답 시간을 보장하는 지리적으로 분산된 서비스 아키텍처입니다. 각 에지 노드에는 사용자의 컨텐츠 요청에 응답하고 해당 요청에 대한 분석 데이터를 추적하는 데 필요한 모든 정보가 있습니다. 사용자 요청은 가장 가까운 에지 노드로 전달됩니다. 자세한 내용은 *Adobe [!DNL Target]이(가) 작동하는 방법*&#x200B;의 [에지 네트워크](/help/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934)을 참조하십시오.

원하는 경우 [!DNL Target] 가장자리 노드를 허용 목록에 추가하다 표시할 수 있습니다.

## [!DNL Target] 가장자리의 NAT(네트워크 주소 변환) IP 주소

[!DNL Target] 가장자리의 송신 IP 주소 목록입니다. 서비스허용 목록에 추가하다에 대한 Target 도달을 계획하는 경우 이 IP를하십시오.

| 가장자리 위치 | 수신 IP 주소 |
| --- | --- |
| Edge31 (뭄바이) | 13.126.131.246<br>13.234.229.8 |
| Edge32 (도쿄) | 3.115.154.28<br>3.115.227.146 |
| Edge34(미국 동부 연안) | 34.232.149.249<br>52.21.139.93 |
| Edge35 (West Coast US) | 52.10.11.139<br>44.231.171.161 |
| Edge36 (시드니) | 13.237.227.20<br>13.210.93.142 |
| Edge37 (아일랜드) | 54.72.21.68<br>52.208.139.19 |
| Edge38(싱가포르) | 18.141.132.96<br>54.179.187.167 |

## Target Edge IP 주소

[!DNL Target] 가장자리의 IP 주소 목록입니다. 가장자리에 API를 호출하려는 경우 허용 목록에 추가하다 이 IP를 Target 가장자리에 표시합니다.

| 가장자리 위치 | 도메인 | IP 주소 |
| --- | --- | --- |
|  | `CLIENTCODE.tt.omtrdc.net`<br>(여기서 CLIENTCODE는  [!DNL Target] 클라이언트 ID) |  |
| Edge31 (뭄바이) | `mboxedge31.tt.omtrdc.net` | 15.207.157.131<br>15.206.8.201 |
| Edge32 (도쿄) | `mboxedge32.tt.omtrdc.net` | 54.199.66.101<br>54.64.93.37 |
| Edge34(미국 동부 연안) | `mboxedge34.tt.omtrdc.net` | 3.225.56.36<br>3.230.207.249<br>34.198.55.51<br>52.3.14.12<br>52.21.222.93<br>52.55.235.132<br>52.70.52.52<br>54.165.204.89 |
| Edge35 (West Coast US) | `mboxedge35.tt.omtrdc.net` | 52.10.244.20<br>52.36.232.38<br>52.88.209.29<br>54.214.180.56<br>35.162.74.35<br>34.214.12.211<br>52.42.35.202<br>54.148.71.13 |
| Edge36 (시드니) | `mboxedge36.tt.omtrdc.net` | 13.238.34.185<br>3.24.250.17<br>3.104.234.91<br>13.211.248.241 |
| Edge37 (아일랜드) | `mboxedge37.tt.omtrdc.net` | 52.212.193.208<br>52.19.133.54<br>52.51.251.137<br>34.252.156.174<br>52.213.168.74<br>34.252.166.160<br>52.18.150.20<br>18.203.205.32 |
| Edge38(싱가포르) | `mboxedge38.tt.omtrdc.net` | 52.221.145.65<br>52.220.44.99<br>13.250.75.226<br>54.151.139.123 |
