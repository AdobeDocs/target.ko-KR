---
keywords: faq;frequently asked questions;analytics for target;a4T;classifications;classification;classifications importer;post-tnt-action
description: 이 주제에서는 분류와 Analytics를 Target(A4T)의 보고 소스로 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.
title: 분류 - A4T FAQ
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 67%

---


# 분류 - A4T FAQ{#classifications-a-t-faq}

This topic contains answers to questions that are frequently asked about classifications and using [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

## 분류 가져오기를 사용하여 분류를 다운로드한 후 post-tnt-action 값을 활동 이름과 일치시키는 방법은 무엇입니까?{#section_6045DAC488B248418F430E663C38D001}

관리 도구 [분류 가져오기](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html)에서 A4T/TNT 문자열에 대한 분류를 다운로드할 수 있습니다. 변수는 내보내기 목록에서 &quot;TNT&quot;라고 합니다. 다운로드한 데이터에는 활동, 경험 등을 위한 친숙한 이름이 포함되어 있습니다.

이 조회 파일은 Adobe의 클릭스트림 데이터 피드를 받는 고객에게 유용합니다. 이 파일에는 `post_tnt` 및 `post_tnt_action` 열을 위한 친숙한 이름이 있습니다.

TNT 변수의 문자열 형식은 `activityID:experienceID:targettype|event`입니다.

* targettype = 0(control/random) 또는 1( [!UICONTROL 타깃팅됨)으로 자동 할당] 및 [!UICONTROL 자동 Target] 활동을수행합니다.
* Event = 0은 경험 입장을 나타냅니다.
* Event = 1은 경험 방문을 나타냅니다.
* Event = 2는 활동 노출을 나타냅니다.
* Event = 32767은 활동 전환을 나타냅니다.

You can import the classification file on a frequent basis from the UI using a [browser import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) or an [FTP import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html). 엔지니어링 서비스에 참여하여 클릭스트림 데이터 피드와 함께 조회 테이블로서 이 파일을 얻을 수도 있습니다.
