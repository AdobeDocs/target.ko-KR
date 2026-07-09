---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 327891a5a9112dfacfca1c049adaef54b218676e
workflow-type: tm+mt
source-wordcount: 719
ht-degree: 37%

---

# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target Standard/Premium] 26.6.8(2026년 6월 24일)

**활동**

+++세부 정보 보기

* **API 및 MCP에 대한 Source 필터에서 리소스를 만들었습니다.** [!UICONTROL Adobe Target API] 또는 [!UICONTROL Adobe Target MCP]에 의한 필터링이 활동, 대상 및 오퍼 목록 페이지에서 작동하지 않는 문제를 해결했습니다. (TGT-55236)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++세부 정보 보기

* **A4T 보고서가 표시되지 않습니다.** [!UICONTROL Analytics for Target]&#x200B;(A4T) 보고서가 표시되지 않는 문제가 해결되었습니다. (TGT-55432)

+++

**[!DNL Adobe Target]MCP 서버**

+++세부 정보 보기

* **통합 활동 도구** [!DNL Adobe Target] MCP 서버 활동 도구는 도구 선택 오버헤드를 줄이고 모든 활동 유형으로 읽기 및 보고서 범위를 확장하기 위해 통합되었습니다. 유형당 6개의 도구가 4개의 통합 도구로 대체되었습니다.

   * `get_activity`이(가) `get_ab_activity`, `get_xt_activity` 및 `get_abt_activity`을(를) 대체합니다. A/B 테스트, 경험 타깃팅, Automated Personalization, 자동 할당, 다변량 테스트(MVT) 및 권장 사항 등 모든 유형에 대한 전체 활동 세부 정보를 검색합니다. 활동 유형이 ID에서 자동으로 감지됩니다.
   * `update_activity`이(가) `update_ab_activity`, `update_xt_activity` 및 `update_abt_activity`을(를) 대체합니다. A/B 테스트, 경험 타기팅 및 Automated Personalization 활동을 지원합니다. 자동 할당, MVT 및 권장 사항 활동은 읽기 전용입니다.
   * `get_activity_performance_report`이(가) `get_ab_performance_report` 및 `get_xt_performance_report`을(를) 대체합니다. 모든 활동 유형에 대한 전환, 상승도 및 신뢰도 지표를 검색합니다.
   * `get_activity_orders_report`이(가) `get_ab_orders_report` 및 `get_xt_orders_report`을(를) 대체합니다. 모든 활동 유형에 대한 주문 및 매출 지표를 검색합니다.

  자세한 내용은 [[!DNL Adobe Target] MCP 서버 도구 참조](../c-integrating-target-with-mac/mcp/target-mcp-tools-reference.md)를 참조하십시오.

+++

## [!DNL Target Standard/Premium] 26.6.4(2026년 6월 16일)

**활동**

+++세부 정보 보기

* 업데이트된 [!DNL Target] UI에서 **[!UICONTROL 저장 및 닫기].** 업데이트된 [!DNL Target] UI에서 **[!UICONTROL 저장 및 닫기]** 옵션을 복원했습니다. (TGT-55152)

* 업데이트된 [!DNL Target] UI의 **QA URL.** 업데이트된 [!DNL Target] UI에서 QA URL이 올바르게 작동하지 않는 문제를 해결했습니다. ([TGT-55110](https://jira.corp.adobe.com/browse/TGT-55110))

+++

**로컬라이제이션**

+++세부 정보 보기

* **JSON 오퍼 만들기 모달에서 지역화되지 않은 문자열 입니다.** [!UICONTROL 이름] 및 [!UICONTROL Workspace]을(를) 포함한 [!UICONTROL JSON 오퍼 만들기] 모달의 문자열이 활동 생성 중에 현지화되지 않는 문제가 해결되었습니다. (TGT-50084)

* **지역화되지 않은 toast 메시지([!UICONTROL 권장 사항] 활동).** 양식 기반 [!UICONTROL 권장 사항] 활동에서 권장 사항을 추가할 때 지역화되지 않은 toast 메시지가 표시되는 문제를 해결했습니다. (TGT-50463)

* **[!UICONTROL 컬렉션] 및 [!UICONTROL 제외] 대화 상자에 지역화되지 않은 문자열.** [!UICONTROL 권장 사항]의 [!UICONTROL 컬렉션] 및 [!UICONTROL 제외] 대화 상자에서 &quot;항목 페이로드&quot; 문자열이 현지화되지 않는 문제를 해결했습니다. (TGT-51542)

* [!UICONTROL 대상] 탭에서 **지역화되지 않은 &quot;승인자&quot; 문자열입니다.** [!UICONTROL 대상 라이브러리] 페이지의 [!UICONTROL Workspace] 열에서 &quot;승인자&quot; 문자열이 현지화되지 않은 문제가 해결되었습니다. (TGT-51751)

+++

## 알아야 하는 시간에 민감한 업데이트 {#time-sensitive}

[!BADGE 중요]{type=Informative}

[!DNL Adobe Target] 및 구현과 관련된 시간에 민감한 업데이트의 경우 [!DNL Adobe]에서 [!UICONTROL Experience League]을(를) 통해 자세한 릴리스 정보 및 설명서를 제공합니다. 구현과 관련된 몇 가지 주요 사항은 다음과 같습니다.

### [!DNL Target] UI 버전 사용 중단 전환

자세한 내용은 [[!DNL Target] UI 업데이트 FAQ](/help/main/c-intro/updated-ui-faq.md)를 참조하십시오.

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [설명서 변경 내용](/help/main/r-release-notes/doc-change.md) | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다. |
| [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md). | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오. |
| [Adobe Experience Cloud 릴리스 노트](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR){target=_blank} | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [Adobe 우선순위 제품 업데이트](https://www.adobe.com/kr/subscription/priority-product-update.html){target=_blank} | [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으십시오. |
| [Target 릴리스 정보 (프리릴리스)](/help/main/r-release-notes/target-release-notes.md){target=_blank} | 프리릴리스 정보를 포함하여 현재 달의 Target 릴리스에 대한 정보입니다. |
