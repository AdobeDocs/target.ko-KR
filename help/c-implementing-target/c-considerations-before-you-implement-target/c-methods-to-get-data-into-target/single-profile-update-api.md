---
keywords: 구현;구현;설정;단일 프로파일 업데이트
description: 단일 프로필 업데이트 API를 사용하여 Target에 데이터를 가져옵니다.
title: 단일 프로필 업데이트 API를 사용하여 Target에 데이터를 가져오려면 어떻게 합니까?
feature: Implementation
role: Developer
exl-id: 8331866c-0b84-4d08-83b4-f7f82c67cd21
translation-type: tm+mt
source-git-commit: 20daf4510e754d77cd16be64770105932178fec5
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 45%

---

# 벌크 프로필 업데이트 API

벌크 프로필 업데이트 API와 거의 동일하지만 한 번에 하나의 방문자 프로필이 .csv 파일이 아닌 API 호출에서 한 번에 업데이트됩니다.

## 형식

방문자는 Target mboxPC 값이나 mboxThirdPartyId 값을 통해 식별해야 합니다. Experience Cloud ID(ECID)는 지원되지 않습니다. 

## 사용 사례 예

방문자가 일부 오프라인 작업을 수행할 때 실시간으로 Target을 업데이트하려는 경우 조치에는 콜 센터 도달, 대출 지원, 매장 내 충성도 카드 사용, 키오스크 액세스 등이 포함됩니다.

## 방법의 이점

프로필 속성의 개수에 대한 제한은 없습니다.

사이트를 통해 전송된 프로필 속성은 API를 통해 업데이트할 수 있으며 반대의 경우도 마찬가지입니다.

## 주의 사항

24시간 기간당 1,000,000개의 API 호출 수 제한(1백만)

프로필만 업데이트합니다. Target이 아직 보지 못한 잠재적 사용자에 대한 프로필을 작성할 수 없습니다.

## 코드 예제

GET 및 POST가 지원됩니다. `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

## 관련 정보에 대한 링크

[프로필 업데이트](https://developers.adobetarget.com/api/#updating-profiles)
