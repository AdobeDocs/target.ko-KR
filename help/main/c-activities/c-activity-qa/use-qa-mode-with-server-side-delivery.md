---
keywords: qa;서버 측;서버-측;미리 보기;미리 보기 링크
description: 서버측 전달과 함께 Adobe [!DNL Target] QA URL을 사용하여, 변경되지 않는 미리 보기 링크를 통한 간편한 엔드 투 엔드 활동 QA, 선택적 대상 타기팅, 라이브 활동 데이터에서 세그멘테이션된 상태를 유지하는 QA 보고를 수행하는 방법에 대해 알아봅니다.
title: 사용 서버측 전달로 활동 QA를 수행할 수 있습니까?
feature: Activities
exl-id: eb6965be-92a6-452d-ac01-7ae1533239cc
TQID: 'https://experienceleague.adobe.com/zZJmFqpXtAigTiEWMZhRqXBJqvG3ANLussSPE3-NoDA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0a683f6e68bb7481b9e45c91a275a46b84a1ffd8
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 18%
---
# 활동 QA 및 서버측 전달 사용 {#qa-server-side}

>[!BEGINSHADEBOX]

**이 페이지에서:** `pageUrl`을(를) 사용할 수 없을 때 활동을 테스트할 수 있도록 서버측 [!DNL Adobe Target] 호출에서 활동 QA 매개 변수를 전달하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

활동 QA의 표준 구현에서는 `pageUrl` 매개 변수를 통해 `qa_mode` 매개 변수를 전달할 수 있습니다. 이 방법은 standard/ajax [!DNL Target] 호출에 편리합니다. 하지만 `pageUrl`을(를) 사용할 수 없는 모바일 SDK 구현과 같이 서버 간 호출에는 적합하지 않습니다. 이러한 경우 동일한 미리 보기 링크, 선택적 대상 타기팅 및 라이브 활동 데이터에서 세그먼트화된 QA 보고를 유지하는 요청 자체에 QA 매개 변수를 전달합니다.

다음 코드 샘플은 서버 측 호출의 활동 QA를 보여 줍니다.

```json
{
  "mbox" : "orderConfirmPage",
  "clientSideAnalyticsLogging": true,
  "clicked" : true,
  "tntId" : "12121212.17_01",
  "order" : {
    ...
  },
  "profileParameters" : {
    ...
  },
  "mboxParameters" : {
    ...
  },
  "requestLocation" : {
    ...
  },
  "qaMode" : {
    "token" : "<encrypted token string>",
    "bypassEntryAudience" : true,
    "listedActivitiesOnly" : true,
    "evaluateAsTrueAudienceIds" : [audienceId1, audienceId2...],
    "evaluateAsFalseAudienceIds" : [audienceId3, audienceId4...],
    "previewIndexes" : [
       {
         "activityIndex" : 1,
         "experienceIndex" : 1
       }
     ],
  },
  "mboxTrace" : true
}
```

다음 표에서는 서버측 요청의 매개 변수에 대해 설명합니다.

| 매개 변수 | 유형 | 기본 값 | 설명 |
|--- |--- |--- |--- |
| 토큰 | 암호화된 토큰 | 없음. 비워둘 수 없습니다. | 활동 QA에서 실행할 수 있는 활동 ID 목록을 포함하는 암호화된 엔터티입니다.<br>유효성 검사 규칙: 토큰은 [!DNL Target] 요청에 지정된 클라이언트에 속하는 암호화된 토큰이어야 합니다. 토큰에 지정된 모든 활동은 클라이언트에 속해야 합니다. |
| bypassEntryAudience | 부울 | False | QA 활동에 대한 시작 단계 대상을 일치로 평가할지 또는 일치로 간주할지 여부를 지정합니다. |
| listedActivitiesOnly | 부울 | False | QA 활동을 개별적으로 실행할지 또는 현재 환경에 대한 활성 활동으로 평가할지 여부를 지정합니다. |
| evaluateAsTrueAudienceIds | ID 목록 | 빈 목록 | [!DNL Target] 요청의 범위에서 항상 true로 평가되는 대상 ID 목록입니다. |
| evaluateAsFalseAudienceIds | ID 목록 | 빈 목록 | [!DNL Target] 요청 범위에서 항상 false로 평가되는 대상 ID 목록입니다. |
| activityIndex | 정수 | Null. 비워둘 수 없습니다. | 암호화된 토큰의 활동 색인입니다. `activityIndex`이(가) null이거나 토큰의 활동 범위를 벗어나면 무시됩니다. 인덱스는 1.<br>유효성 검사 규칙으로 시작합니다. 하나 이상의 활동 인덱스가 필요하며 토큰에 지정된 활동을 참조해야 합니다. |
| experienceIndex | 정수 | Null | 지정된 경우 활동 정의에서 색인별 경험을 선택합니다. 지정되지 않았거나 경계를 벗어나는 경우 활동의 경험 선택기 전략으로 돌아갑니다. 색인이 1.<br>유효성 검사 규칙으로 시작: 값이 null이거나 활동의 경험을 참조해야 합니다. |
