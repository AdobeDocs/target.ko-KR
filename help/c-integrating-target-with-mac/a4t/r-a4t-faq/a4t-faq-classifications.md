---
description: 이 주제에서는 분류와 Analytics를 Target(A4T)의 보고 소스로 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.
keywords: faq;자주 묻는 질문;analytics for target;a4T;분류;분류;분류 가져오기;post-tnt-action
seo-description: 이 주제에서는 분류와 Analytics를 Target(A4T)의 보고 소스로 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.
seo-title: 분류 - A4T FAQ
solution: Target
title: 분류 - A4T FAQ
topic: Standard
uuid: 4b42adbc-4fa8-4b62-86c8-bb8f8bec7e54
translation-type: tm+mt
source-git-commit: 74a6f402bc0c9dae6f89cbdb632d7dbc53743593

---


# 분류 - A4T FAQ{#classifications-a-t-faq}

이 주제에서는 분류와 Analytics를 Target(A4T)의 보고 소스로 사용하는 것과 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## [분류 가져오기]를 사용하여 분류를 다운로드한 후 post-tnt-action 값을 활동 이름과 일치시키는 방법은 무엇입니까?{#section_6045DAC488B248418F430E663C38D001}

관리 도구 [분류 가져오기](https://marketing.adobe.com/resources/help/en_US/reference/c_working_with_saint.html)에서 A4T/TNT 문자열에 대한 분류를 다운로드할 수 있습니다. 변수는 내보내기 목록에서 &quot;TNT&quot;라고 합니다. 다운로드한 데이터에는 활동, 경험 등을 위한 친숙한 이름이 포함되어 있습니다.

이 조회 파일은 Adobe의 클릭스트림 데이터 피드를 받는 고객에게 유용합니다. 이 파일에는 `post_tnt` 및 `post_tnt_action` 열을 위한 친숙한 이름이 있습니다.

TNT 변수의 문자열 형식은 `activityID:experienceID:targettype|event`입니다.

* A4T의 경우 targettype은 항상 0입니다.
* Event = 0은 경험 입장을 나타냅니다.
* Event = 1은 경험 방문을 나타냅니다.
* Event = 2는 활동 노출을 나타냅니다.
* Event = 32767은 활동 전환을 나타냅니다.

[브라우저 내보내기](https://marketing.adobe.com/resources/help/en_US/reference/browser_export.html)나 [FTP 내보내기](https://marketing.adobe.com/resources/help/en_US/reference/ftp_export.html)를 사용하여 UI에서 자주 사용하는 분류 파일을 다운로드할 수 있습니다. 엔지니어링 서비스에 참여하여 클릭스트림 데이터 피드와 함께 조회 테이블로서 이 파일을 얻을 수도 있습니다.
