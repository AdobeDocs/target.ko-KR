---
keywords: faq;자주 묻는 질문;analytics for target;a4T;분류;분류;분류 가져오기;post-tnt-action;이벤트 코드
description: 분류 및 [!UICONTROL Analytics for Target] (A4T)을 사용하는 것과 관련된 질문에 대한 답변을 찾으십시오.
title: A4T를 사용하여 분류에 대한 정보는 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: e81a27bc321fa83cc1b2449e5df32edfa37d5198
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 29%

---

# 분류 - A4T FAQ

이 주제에서는 분류와 [!DNL Target](A4T)의 보고 소스로 [!DNL Analytics] 를 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## [!UICONTROL 분류 가져오기]를 사용하여 분류를 다운로드한 후 post-tnt-action 값을 활동 이름과 일치시키려면 어떻게 합니까? {#section_6045DAC488B248418F430E663C38D001}

관리 도구 [분류 가져오기](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html)에서 A4T/TNT 문자열에 대한 분류를 다운로드할 수 있습니다. 변수는 내보내기 목록에서 &quot;TNT&quot;라고 합니다. 다운로드한 데이터에는 활동, 경험 등을 위한 친숙한 이름이 포함되어 있습니다.

이 조회 파일은 [!DNL Adobe]의 클릭스트림 데이터 피드를 수신하는 고객에게 유용합니다. 이 파일에는 `post_tnt` 및 `post_tnt_action` 열을 위한 친숙한 이름이 있습니다.

표준 [!UICONTROL A/B 테스트] 및 [!UICONTROL 경험 타깃팅] (XT) 활동의 경우, TNT 문자열의 형식은 다음과 같습니다.

```
activityID:experienceID:targettype|event
```

[!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동의 경우 TNT 문자열의 형식은 다음과 같습니다.

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` =  `targettype` 및 `algorithmId` 는  [!UICONTROL 자동 할당 및 ] 자동 타겟 활동에 사용되는  [!UICONTROL 내부 ] 식별자입니다.
* Event = 0은 경험 입장을 나타냅니다.
* Event = 1은 경험 방문을 나타냅니다.
* Event = 2는 활동 노출을 나타냅니다.
* Event = 3-32766 는 Analytics 성공 지표 ID를 나타냅니다.
* Event = 32767은 활동 전환을 나타냅니다.
* 이벤트 -1 또는 65535 은 사용자가 활동 또는 경험에서 제거되었음을 나타냅니다. 이러한 상황은 방문자가 전환될 때 종종 발생합니다. 방문자가 경험에서 해제되어 이제 다른 경험에 대한 자격이 제공됩니다.

[브라우저 가져오기](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) 또는 [FTP 가져오기](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en)를 사용하여 UI에서 자주 분류 파일을 가져올 수 있습니다. 엔지니어링 서비스에 참여하여 클릭스트림 데이터 피드와 함께 조회 테이블로서 이 파일을 얻을 수도 있습니다.
