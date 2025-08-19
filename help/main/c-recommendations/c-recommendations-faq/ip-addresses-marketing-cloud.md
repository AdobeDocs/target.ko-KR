---
keywords: IP 주소, IP 주소, 허용 목록, 허용 목록, 방화벽, recs, 피드, 서버, adobe marketing cloud, 권장 사항
description: ' [!DNL Target]  추천 피드 처리 서버에서 사용된 IP 주소 목록을 보고 Adobe 서버에서 시작된 IP 주소를 허용하도록 방화벽을 구성할 수 있습니다.'
title: 추천 피드-처리 서버에서 사용하는 IP 주소는 무엇입니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: be5b3158c758fa08802c1dc0541c9e989a2c7740
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 35%

---

# [!DNL Recommendations] 피드 처리 서버에서 사용하는 IP 주소

[!DNL Adobe Target] 서버에서 시작된 IP 주소를 허용하도록 방화벽을 구성하는 데 도움이 되는 [!DNL Recommendations] [!DNL Adobe] 피드 처리 서버에서 사용된 IP 주소 목록입니다.

>[!IMPORTANT]
>
>[!DNL Target] 팀은 현재 [!DNL Recommendations] 피드를 다운로드하기 위해 NAT 게이트웨이 주소를 업데이트하는 중입니다. IP 허용 목록에 추가허용 목록에 추가하다 를 구현하는 경우 다음의 새 AWS 호스트를 구현해야 합니다. 기존 호스트는 2024년 6월 30일에 폐기될 예정입니다. 원활한 전환을 위해 9개의 주소를 모두 허용 목록에 추가하다합니다. 기존 주소를 제거해야 할 긴급성은 없습니다.

[!DNL Target] [!UICONTROL Recommendations] 활동에서는 고객의 FTP 서버에 액세스할 때 다음 AWS 호스트를 사용합니다.

**새 호스트**:

| 위치 | 호스트 |
| --- | --- |
| 오레곤 | `52.40.124.129` |
| 오레곤 | `54.148.219.69` |
| 오레곤 | `54.189.208.212` |
| 오레곤 | `44.230.236.35` |
| 오레곤 | `54.190.78.243` |
| 오레곤 | `52.41.73.133` |

**기존 호스트**:

| 위치 | 호스트 |
| --- | --- |
| 오레곤 | `44.241.237.28` |
| 오레곤 | `44.232.167.82` |
| 오레곤 | `52.41.252.205` |

[!DNL Target]개의 [!UICONTROL Recommendations] API도 동일한 AWS 호스트를 사용합니다.
