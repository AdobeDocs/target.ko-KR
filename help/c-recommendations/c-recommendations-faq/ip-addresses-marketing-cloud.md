---
keywords: IP 주소;IP 주소;허용 목록;;허용 목록에 추가하다 방화벽;최근;피드;서버;Adobe marketing cloud;recommendations
description: Adobe 서버에서 시작된 IP 주소를 허용하도록 방화벽을 구성하는 데 도움이 되도록  [!DNL Target] Recommendations 피드 처리 서버에 사용된 IP 주소 목록을 봅니다.
title: Recommendations 피드 처리 서버가 사용하는 IP 주소는 무엇입니까?
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 8%

---

# ![PREMIUM](/help/assets/premium.png) 권장 사항 피드 처리 서버에서 사용하는 IP 주소

Adobe 서버에서 시작된 IP 주소를 허용하도록 방화벽을 구성하는 데 도움이 되는 [!DNL Adobe Target] [!DNL Recommendations] 피드 처리 서버에 사용된 IP 주소 목록.

[!DNL Target] [!UICONTROL 권장 ] 사항 활동은 고객의 FTP 서버에 액세스할 때 다음과 같은 AWS 호스트를 사용합니다.

| 위치 | 호스트 |
| --- | --- |
| 오리건 주 | `44.241.237.28` |
| 오리건 주 | `44.232.167.82` |
| 오리건 주 | `52.41.252.205` |

[!DNL Target] [!UICONTROL 또한 ] RecommendationsAPI는 동일한 AWS 호스트를 사용합니다.

>[!NOTE]
>
>이러한 IP 주소는 2021년 3월 16일에 마지막으로 업데이트되었습니다. 이전에는 FTP 서버에 액세스하는 서버가 192.243.242.0/24 IP 주소 CIDR 블록에 있었습니다. Recommendations API를 호스팅하는 서버는 192.243.224.0/20 IP 주소 CIDR 블록에 있었습니다.
