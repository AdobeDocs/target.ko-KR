---
keywords: qa;서버 측;서버-측;미리 보기;미리 보기 링크
description: Adobe 사용 방법 알아보기 [!DNL Target] 서버 측 전달을 통한 QA URL을 통해, 변경되지 않는 미리 보기 링크를 통한 간편한 엔드 투 엔드 활동 QA, 선택적 대상 타깃팅, 라이브 활동 데이터에서 세그멘테이션된 상태를 유지하는 QA 보고를 수행할 수 있습니다.
title: 서버측 전달을 통해 활동 QA를 수행할 수 있습니까?
feature: Activities
exl-id: eb6965be-92a6-452d-ac01-7ae1533239cc
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 70%

---

# 활동 QA 및 서버측 전달 사용

에서 QA URL과 서버 측 전달 사용 [!DNL Adobe Target] 변경되지 않는 미리 보기 링크를 통한 간편한 엔드 투 엔드 활동 QA, 선택적 대상 타깃팅, 라이브 활동 데이터에서 세그멘테이션된 상태를 유지하는 QA 보고를 수행할 수 있습니다.

활동 QA의 표준 구현에서 `pageUrl` 매개 변수를 통해 `qa_mode` 매개 변수 전달을 지원합니다. 이 방법은 표준/ajax에서 편리하게 사용할 수 있습니다 [!DNL Target] 호출. 그러나 서버 간 호출의 경우 `pageUrl`을 사용할 수 없는 모바일 SDK 사례에는 적합한 방법이 아닙니다.

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

다음 표는 서버 측 요청의 세부 사항을 설명합니다.

| 매개 변수 | 유형 | 기본값 | 설명 |
|--- |--- |--- |--- |
| 토큰 | 암호화된 토큰 | 없음.<br>비워둘 수 없습니다. | 활동 QA에서 실행할 수 있는 활동 ID 목록이 들어 있는 암호화된 엔티티입니다.<br>[!DNL Target]검증 규칙:  요청에 지정된 클라이언트에 속하는 암호화된 토큰이어야 합니다. 토큰에 지정된 모든 활동은 클라이언트에 속해야 합니다. |
| bypassEntryAudience | 부울 | False | QA 활동에 대한 입력 단계 Target을 평가해야 하는지, 또는 일치한 것으로 간주해야 하는지 여부를 지정합니다. |
| listedActivitiesOnly | 부울 | False | QA 활동이 분리되어야 하는지, 또는 현재 환경에 대한 활성 활동으로 평가되어야 하는지 여부를 지정합니다. |
| evaluateAsTrueAudienceIds | ID 목록 | 목록이 비어 있습니다. | 의 범위에서 항상 true로 평가해야 하는 대상 ID 목록 [!DNL Target] 요청. |
| evaluateAsFalseAudienceIds | ID 목록 | 목록이 비어 있습니다. | 의 범위에서 항상 false로 평가해야 하는 대상 ID 목록입니다 [!DNL Target] 요청. |
| activityIndex | 정수 | Null.<br>비워둘 수 없습니다. | 암호화된 토큰의 활동 색인입니다. activityIndex가 토큰의 활동 범위를 벗어나거나 Null인 경우 무시됩니다. 색인은 1로 시작합니다.<br>검증 규칙: 한 개 이상의 활동 색인이어야 하며 토큰에 지정된 활동을 참조해야 합니다. |
| experienceIndex | 정수 | Null입니다. | 지정된 경우 활동 정의에서 색인별 경험을 선택합니다. 지정하지 않거나 범위를 벗어나면 활동의 경험 선택기 전략으로 되돌아갑니다. 색인은 1로 시작합니다.  검증 규칙: Null이거나 활동의 경험을 참조해야 합니다. |