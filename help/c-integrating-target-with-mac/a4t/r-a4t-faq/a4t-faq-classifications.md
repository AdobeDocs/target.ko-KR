---
keywords: faq;자주 묻는 질문;analytics for target;a4T;분류;분류;분류 가져오기;post-tnt-action
description: 분류 및 [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] 활동에 대한 Analytics 사용에 대한 질문에 대한 답변을 찾습니다.
title: A4T를 사용하여 분류에 대한 정보를 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 59%

---

# 분류 - A4T FAQ

이 주제에는 분류에 대해 자주 묻는 질문과 [!DNL Analytics]을(를) [!DNL Target](A4T)의 보고 소스로 사용하는 질문에 대한 답변이 포함되어 있습니다.

## 분류 가져오기를 사용하여 분류를 다운로드한 후 post-tnt-action 값을 활동 이름과 일치시키는 방법은 무엇입니까?{#section_6045DAC488B248418F430E663C38D001}

관리 도구 [분류 가져오기](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html)에서 A4T/TNT 문자열에 대한 분류를 다운로드할 수 있습니다. 변수는 내보내기 목록에서 &quot;TNT&quot;라고 합니다. 다운로드한 데이터에는 활동, 경험 등을 위한 친숙한 이름이 포함되어 있습니다.

이 조회 파일은 Adobe의 클릭스트림 데이터 피드를 받는 고객에게 유용합니다. 이 파일에는 `post_tnt` 및 `post_tnt_action` 열을 위한 친숙한 이름이 있습니다.

TNT 변수의 문자열 형식은 `activityID:experienceID:targettype|event`입니다.

* [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동에 대한 targettype = 0(control/random) 또는 1(타깃팅됨)입니다.
* Event = 0은 경험 입장을 나타냅니다.
* Event = 1은 경험 방문을 나타냅니다.
* Event = 2는 활동 노출을 나타냅니다.
* 이벤트 = 3-32766은 분석 성공 지표 id를 나타냅니다.
* Event = 32767은 활동 전환을 나타냅니다.

[브라우저 가져오기](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) 또는 [FTP 가져오기](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html)를 사용하여 UI에서 자주 분류 파일을 가져올 수 있습니다. 엔지니어링 서비스에 참여하여 클릭스트림 데이터 피드와 함께 조회 테이블로서 이 파일을 얻을 수도 있습니다.
