---
keywords: 구현;구현;설정;벌크 프로파일 업데이트
description: 벌크 프로필 업데이트 API를 사용하여 Target에 데이터를 가져옵니다.
title: 벌크 프로필 업데이트 API를 사용하여 Target에 데이터를 가져오려면 어떻게 합니까?
feature: 구현
role: Developer
translation-type: tm+mt
source-git-commit: e8c25685341319fea4381386cad1ce0c5b80face
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 82%

---

# 벌크 프로필 업데이트 API

API를 통해 많은 방문자의 방문자 프로필 업데이트가 있는 .csv 파일을 [!DNL Adobe Target]으로 보냅니다. 각 방문자 프로필은 하나의 호출에서 여러 개의 인페이지 프로필 속성으로 업데이트할 수 있습니다.

이 옵션은 몇 가지 차이점이 있는 고객 속성과 유사합니다.

* 고객 속성은 FTP 업로드를 사용하는 반면, Target 벌크 프로필 업데이트 API는 HTTP POST API를 사용합니다.
* 고객 속성 데이터는 Analytics과 공유할 수 있고, 벌크 프로필 업데이트는 Target에서만 사용할 수 있습니다.
* 고객 속성은 Target이 아직 보지 못한 사용자에 대한 프로필 작성을 지원합니다. 벌크 프로필 업데이트 API는 기존 Target 프로필만 업데이트합니다.
* 고객 속성에는 Experience Cloud ID(ECID)를 사용해야 합니다. 벌크 프로필 업데이트 API에는 TNT ID나 `mbox3rdPartyId`를 사용해야 합니다.
* `mbox3rdPartyID`에서 더하기 기호(+)와 슬래시(/)는 보낼 수 없습니다.

## 형식

.csv 파일은 Target PCID나 mboxThirdPartyId를 통해 각 방문자를 참조해야 합니다. Experience Cloud ID(ECID)는 지원되지 않습니다. 모든 프로필 속성/값은 API를 통해 생성 및 업데이트됩니다. 형식 세부 사항은 API 설명서에 나와 있습니다.

## 활용 사례 예

CRM 또는 기타 내부 시스템은 페이지 구현에서 프로필 데이터를 노출하지 않고 Target에 지속적으로 업데이트하고자 하는 방문자에 대한 중요 데이터를 저장합니다.

## 방법의 이점

프로필 속성의 개수에 대한 제한은 없습니다.

사이트를 통해 전송된 프로필 속성은 API를 통해 업데이트할 수 있으며 반대의 경우도 마찬가지입니다.

## 주의 사항

묶음 파일의 크기는 50MB 미만이어야 합니다. 또한 총 행 수는 업로드당 500,000개 행을 초과하지 않아야 합니다.

이후 묶음에서 24시간 동안 업로드할 수 있는 행 수에는 제한이 없습니다. 그러나 영업 시간 동안 처리 프로세스를 조절하여 다른 프로세스가 효율적으로 실행되도록 할 수도 있습니다.

동일한 thirdPartyIds 간에 mbox를 호출하지 않고 연속적인 [V2 배치 업데이트를 호출](https://developers.adobetarget.com/api/#updating-profiles)하면 첫 번째 배치 업데이트 호출에서 업데이트된 속성을 재정의합니다.

## 코드 예제

[프로필 업데이트](https://developers.adobetarget.com/api/#updating-profiles)를 참조하십시오.

### 관련 정보에 대한 링크

[프로필 업데이트](https://developers.adobetarget.com/api/#updating-profiles)