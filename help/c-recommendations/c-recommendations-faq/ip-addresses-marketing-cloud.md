---
keywords: IP 주소, IP 주소, 허용 목록, 허용 목록, 방화벽, recs, 피드, 서버, adobe marketing cloud, 권장 사항
description: ' [!DNL Target]  Recommendations 피드 처리 서버에서 사용된 IP 주소 목록을 보고 Adobe 서버에서 시작된 IP 주소를 허용하도록 방화벽을 구성할 수 있습니다.'
title: Recommendations 피드-처리 서버에서 사용하는 IP 주소는 무엇입니까?
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 100%

---

# ![PREMIUM](/help/assets/premium.png) 권장 사항 피드 처리 서버에서 사용하는 IP 주소

[!DNL Adobe Target] [!DNL Recommendations] 피드 처리 서버에 사용되는 IP 주소 목록으로, Adobe 서버에서 IP 주소를 생성할 수 있도록 방화벽을 구성하는 데 도움이 됩니다.

[!DNL Target] [!UICONTROL Recommendations] 활동에서는 다음의 AWS 호스트를 사용하여 고객의 FTP 서버에 액세스합니다.

| 위치 | 호스트 |
| --- | --- |
| 오레곤 | `44.241.237.28` |
| 오레곤 | `44.232.167.82` |
| 오레곤 | `52.41.252.205` |

[!DNL Target] [!UICONTROL Recommendations] API도 동일한 AWS 호스트를 사용합니다.

>[!NOTE]
>
>이 IP 주소는 2021년 3월 16일에 마지막으로 업데이트되었습니다. 이전에는 FTP 서버에 액세스하는 서버가 192.243.242.0/24 IP 주소 CIDR 블록에 있었습니다. Recommendations API를 호스트하는 서버는 192.243.224.0/20 IP 주소 CIDR 블록에 있었습니다.
