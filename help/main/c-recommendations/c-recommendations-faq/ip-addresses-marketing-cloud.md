---
keywords: IP 주소, IP 주소, 허용 목록, 허용 목록, 방화벽, recs, 피드, 서버, adobe marketing cloud, 권장 사항
description: ' [!DNL Target]  Recommendations 피드 처리 서버에서 사용된 IP 주소 목록을 보고 Adobe 서버에서 시작된 IP 주소를 허용하도록 방화벽을 구성할 수 있습니다.'
title: Recommendations 피드-처리 서버에서 사용하는 IP 주소는 무엇입니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: 558de92e672c276474bc76fad19e5461ae7d4c88
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 49%

---

# 에서 사용하는 IP 주소 [!DNL Recommendations] 피드 처리 서버

에 사용된 IP 주소 목록 [!DNL Adobe Target] [!DNL Recommendations] 피드 처리 서버: IP 주소를에서 시작하도록 방화벽을 구성하는 데 도움이 됩니다. [!DNL Adobe] 서버.

>[!IMPORTANT]
>
>2023년 2월 23일: [!DNL Target] 팀에서 현재 다운로드할 NAT 게이트웨이 주소를 업데이트하고 있습니다. [!DNL Recommendations] 피드. IP 허용 목록에 추가허용 목록에 추가하다 를 구현하는 경우 다음의 새 AWS 호스트를 구현해야 합니다. 기존 호스트는 향후 폐기될 예정입니다. 이제 9개의 호스트가 모두 작동합니다.

[!DNL Target] [!UICONTROL Recommendations] 활동에서는 다음의 AWS 호스트를 사용하여 고객의 FTP 서버에 액세스합니다.

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

[!DNL Target] [!UICONTROL Recommendations] API도 동일한 AWS 호스트를 사용합니다.
