---
keywords: IP 주소;IP 주소;허용 목록;;허용 목록에 추가하다 방화벽;최근;피드;서버;Adobe marketing cloud;recommendations
description: Adobe Recommendations 피드 처리 서버에서 시작된 IP 주소를 허용하도록 방화벽을 구성하는 데 도움이 되는 IP 주소 목록을 봅니다.
title: Recommendations 피드 처리 서버가 사용하는 IP 주소는 무엇입니까?
feature: Recommendations
translation-type: tm+mt
source-git-commit: 55b246f5f0d660e6c4f71352c5b638347d55ac28
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 13%

---


# ![PREMIUM](/help/assets/premium.png) 권장 사항 피드 처리 서버에서 사용하는 IP 주소

Adobe 서버에서 시작된 IP 주소를 허용하도록 방화벽을 구성하는 데 도움이 되는 [!DNL Adobe Target] [!DNL Recommendations] 피드 처리 서버에 사용된 IP 주소 목록.

[!DNL Target] [!UICONTROL 권장 ] 사항 활동은 고객의 FTP 서버에 액세스할 때 다음 IP 주소를 사용합니다.

| CIDR 표기법 |
|---|
| 44.241.237.28/32 |
| 44.232.167.82/32 |
| 52.41.252.205/32 |

[!DNL Target] [!UICONTROL Recommendations] API는 다음 IP 주소를 사용합니다.

| CIDR 표기법 |
|---|
| 44.241.237.28/32 |
| 44.232.167.82/32 |
| 52.41.252.205/32 |

>[!NOTE]
>
>이러한 IP 주소는 2021년 3월 16일에 마지막으로 업데이트되었습니다. 이전에는 FTP 서버에 액세스하는 서버가 192.243.242.0/24 IP 주소 CIDR 블록에 있었습니다. Recommendations API를 호스팅하는 서버는 192.243.224.0/20 IP 주소 CIDR 블록에 있었습니다.

