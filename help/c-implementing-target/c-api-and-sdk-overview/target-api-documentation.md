---
keywords: api;adobe i/o
description: Adobe Target Classic API에서 Adobe I/O의 새로운 API로 전환하는 방법을 알아봅니다.
title: 기존 API에서 Adobe I/O으로 어떻게 전환합니까?
feature: Implement Server-side
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 89%

---


# Target의 이전 API에서 Adobe I/O로 전환

Target의 이전 API에서 Adobe I/O의 새 API로 전환하는 데 도움이 되는 정보입니다.

Adobe Target Classic을 삭제하면 Target Classic 계정에 연결된 API도 사용할 수 없게 됩니다. 이 문서는 이전 API 기반 통합을 Adobe I/O에서 제공하는 Target API로 전환하는 데 도움이 됩니다.

Target API 문서에 대한 자세한 정보는 [Target API 및 NodeJS SDK](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md#concept_5718EC1FF2ED4436935D0BCCD7AA29A6).

## 용어 {#section_D8286EDAE3B24D208DA432AEF2E88FD9}

| 용어 | 설명 |
|--- |--- |
| 이전 API | Target Classic 계정에 연결된 API입니다. 이 API 호출은 사용자 이름 및 암호 기반 인증을 기반으로 하며 호스트 이름 `testandtarget.omniture.com`을 사용합니다. API 호출이 요청 URL에 사용자 이름과 암호를 포함하고 있는 경우, Adobe I/O API로 전환해야 합니다. |
| Adobe I/O | Adobe I/O는 Target API의 새로운 게이트웨이입니다. 이 API는 Target Standard/Premium 계정에 연결되어 있습니다. Adobe I/O의 Target API는 보안 엔터프라이즈 API의 업계 표준인 JWT 기반 인증을 사용합니다. |

## 타임라인 {#section_A478EBF637554A2DB5A31661955121ED}

이전 API는 Target Classic과 동시에 폐기됩니다.

| 날짜 | 세부 사항 |
|--- |--- |
| 2017년 10월 17일 | 쓰기 작업을 수행하는 모든 API 메서드(`saveCampaign`, `copyCampaign`, `saveHTMLOfferContent` 및 `setCampaignState`)가 폐기되었습니다.<br>모든 Target Classic 사용자 계정이 읽기 전용 상태로 설정되는 날짜와 동일한 날짜입니다. |
| 2017년 11월 14일 | 나머지 API는 삭제되었습니다. Target Classic 사용자 인터페이스가 삭제되는 날짜입니다. |

권장 사항 Classic API는 이 타임라인의 영향을 받지 않습니다.

## 동등한 메서드  {#section_DDB42CCC172545B09CB728D794CC466B}

다음 표에는 이전 API 메서드와 동등한 새 Target API 메서드가 나와 있습니다. 새 API는 이전 API에서 제공하는 XML 응답과 비교할 때 JSON을 반환합니다.

새 API 메서드는 API 설명서 사이트의 해당 섹션에 연결되어 있습니다. 여기에는 각 API 메서드에 대한 예가 제공됩니다. Adobe I/O의 모든 새로운 Adobe API 메서드에 대한 샘플 API 호출이 들어 있는 Admin Postman Collection을 사용할 수도 있습니다.

| 그룹 | 이전 API 메서드 | 새 API 메서드 | 참고 |
|--- |--- |--- |--- |
| 캠페인/활동 | 캠페인 만들기 | [AB 활동 만들기](http://developers.adobetarget.com/api/#create-ab-activity)<br>[XT 활동 만들기](http://developers.adobetarget.com/api/#create-xt-activity) | 새 API에서는 AB 및 XT용으로 별도의 만들기 메서드를 제공합니다. |
|  | 캠페인 업데이트 | [AB 활동 업데이트](http://developers.adobetarget.com/api/#update-ab-activity)<br>[XT 활동 업데이트](http://developers.adobetarget.com/api/#update-xt-activity) |  |
|  | 캠페인 복사 | 해당 없음 | 활동 만들기 API를 사용하십시오. |
|  | 캠페인 목록 | [활동 나열](http://developers.adobetarget.com/api/#list-activities) |  |
|  | 캠페인 상태 | [활동 상태 업데이트](http://developers.adobetarget.com/api/#update-activity-state) |  |
|  | 캠페인 보기 | [ID별 AB 활동 가져오기](http://developers.adobetarget.com/api/#get-ab-activity-by-id)<br>[ID별 XT 활동 가져오기](http://developers.adobetarget.com/api/#get-xt-activity-by-id) |  |
|  | 타사 캠페인 ID | 해당 없음 | thirdpartyID를 사용하는 경우 관련 활동 메서드를 사용할 수 있습니다. |
| 오퍼 | 오퍼 만들기 | [오퍼 만들기](http://developers.adobetarget.com/api/#create-offer) |  |
|  | 오퍼 가져오기 | [ID별 오퍼 가져오기](http://developers.adobetarget.com/api/#get-offer-by-id) |  |
|  | 오퍼 목록 | [오퍼 나열](http://developers.adobetarget.com/api/#list-offers) |  |
|  | 폴더 목록 | 해당 없음 | Target Standard/Premium에서는 폴더가 지원되지 않습니다. |
| 보고 | 캠페인 성과 보고서 | [AB 성과 보고서 가져오기](http://developers.adobetarget.com/api/#get-ab-performance-report)<br>[XT 성과 보고서 가져오기](http://developers.adobetarget.com/api/#get-xt-performance-report) |  |
|  | 감사 보고서 | [감사 보고서 가져오기](http://developers.adobetarget.com/api/#get-audit-report) |  |
|  | 1-1 컨텐츠 보고서 | [AP 성과 보고서 가져오기](http://developers.adobetarget.com/api/#get-ap-activity-performance-report) |  |
| 계정 설정 | 호스트 그룹 가져오기 | [환경 나열](http://developers.adobetarget.com/api/#list-environments) |  |

## 예외 {#section_09CF9A0E289149279783B4801D1B6D4C}

예외가 필요한 경우 Customer Success Manager에게 문의하십시오.

## 도움말  {#section_591F850E2B7A4342B1C233693425415C}

질문이 있거나 Adobe I/O에서 새 Target API로 전환하는 데 도움이 필요한 경우 Adobe Target 고객 지원팀(tt-support@adobe.com)에 문의하십시오.
