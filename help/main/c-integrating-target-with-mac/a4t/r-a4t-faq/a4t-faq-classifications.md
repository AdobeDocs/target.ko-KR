---
keywords: faq;자주 묻는 질문;analytics for target;a4T;분류;분류;분류 가져오기;post-tnt-action;이벤트 코드
description: 분류 및 [!UICONTROL Analytics for Target](A4T) 사용에 대한 질문에 대한 답변을 찾아보십시오.
title: A4T를 사용하는 분류에 대한 정보는 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 24%

---

# 분류 - A4T FAQ

이 주제에서는 분류와 [!DNL Analytics]을(를) [!DNL Target](A4T)의 보고 소스로 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## [!UICONTROL Classifications Importer]을(를) 사용하여 분류를 다운로드한 후 post-tnt-action 값을 활동 이름과 일치시키는 방법은 무엇입니까? {#section_6045DAC488B248418F430E663C38D001}

+++답변
관리 도구 [분류 가져오기](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html)에서 A4T/TNT 문자열에 대한 분류를 다운로드할 수 있습니다. 변수는 내보내기 목록에서 &quot;TNT&quot;라고 합니다. 다운로드한 데이터에는 활동, 경험 등을 위한 친숙한 이름이 포함되어 있습니다.

이 조회 파일은 [!DNL Adobe]의 클릭스트림 데이터 피드를 받는 고객에게 유용합니다. 이 파일에는 `post_tnt` 및 `post_tnt_action` 열을 위한 친숙한 이름이 있습니다.

표준 [!UICONTROL A/B Test] 및 [!UICONTROL Experience Targeting](XT) 활동의 경우 TNT 문자열 형식은 다음과 같습니다.

```
activityID:experienceID:targettype|event
```

[!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 활동의 경우 TNT 문자열 형식은 다음과 같습니다.

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` = `targettype` 및 `algorithmId`은(는) [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 활동에서 사용하는 내부 식별자입니다.
* Event = 0은 경험 입장을 나타냅니다.
* Event = 1은 경험 방문을 나타냅니다.
* Event = 2는 활동 노출을 나타냅니다.
* 이벤트 = 3-32766은 분석 성공 지표 ID를 나타냅니다.
* Event = 32767은 활동 전환을 나타냅니다.
* 이벤트 -1 또는 65535은 사용자가 활동 또는 경험에서 제거되었음을 나타냅니다. 이러한 상황은 방문자가 전환할 때 자주 발생합니다. 방문자가 경험에서 해제되어 이제 다른 경험을 사용할 수 있습니다.

[브라우저 가져오기](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) 또는 [FTP 가져오기](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en)를 사용하여 UI에서 자주 분류 파일을 가져올 수 있습니다. 엔지니어링 서비스에 참여하여 클릭스트림 데이터 피드와 함께 조회 테이블로서 이 파일을 얻을 수도 있습니다.

+++
