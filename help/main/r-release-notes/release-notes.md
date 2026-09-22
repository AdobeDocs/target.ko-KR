---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트;현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: '[!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: '[!DNL Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: e7d752d7b77f6c167878f1b3679d118c2b44a31f
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 36%
---
# [!DNL Target] 릴리스 정보 (현재)

[!DNL Adobe Target]의 최신 기능, 개선 사항 및 수정 사항을 살펴보십시오. 이러한 릴리스 노트는 해당되는 경우 [!DNL Target]개의 API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 구성 요소에 대한 업데이트도 다룹니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target Standard/Premium] 26.9.5(2026년 9월 21일)

**[!UICONTROL Analytics for Target]**

+++세부 정보 보기

* **A4T 보고서 링크가 [!DNL Target] UI에 생성되지 않음**. [!DNL A4T] 활동의 경우 기본 보고서 데이터가 [!DNL Target] UI와 [!DNL Adobe Analytics] UI 모두에 표시되었더라도 **[!UICONTROL 보고서]** 섹션에서 보고서 링크가 생성되지 않았습니다. (TGT-56247)

+++

## [!DNL Target Standard/Premium] 26.9.4(2026년 9월 17일)

**[!UICONTROL 시각적 경험 작성기] (VEC)**

+++세부 정보 보기

* 가장 위쪽 페이지 요소&#x200B;**에서 [!DNL Experience Fragments]에 대한**&#x200B;[!UICONTROL &#x200B;다음 항목 앞에 삽입] 컨트롤에 액세스할 수 없습니다. 시각적 경험 작성기에서 페이지에서 맨 위 요소를 선택하면 페이지가 위쪽으로 스크롤되어 **[!UICONTROL 다음 항목 앞에 삽입]** 컨트롤이 선택할 수 없는 표시된 뷰포트 위에 렌더링됩니다. (TGT-55829)

+++

## [!DNL Target Standard/Premium] 26.9.3(2026년 9월 16일)

**[!UICONTROL 보고]**

+++세부 정보 보기

* **일부 [!DNL A4T Auto-Target] 보고서에 [!UICONTROL 상승도] 및 [!UICONTROL 신뢰도] 값이 없음**. **[!UICONTROL 방문 전환율 최대화]** 최적화 목표를 사용하는 [!DNL A4T Auto-Target] 활동의 경우 기본 **[!UICONTROL 내 기본 지표]** 보고서 지표가 올바르게 확인되지 않아 **[!UICONTROL 상승도]** 및 **[!UICONTROL 신뢰도]**&#x200B;이(가) 비어 있습니다. (TGT-56137)

+++

**[!UICONTROL Analytics for Target]**

+++세부 정보 보기

* **[!UICONTROL 보고 Source] 필드는 이제 [!DNL Analytics] 액세스 권한이 없는 라이브 활동에 대해 읽기 전용입니다**. 이전에는 라이브 활동 소유자가 [!DNL Adobe Analytics]에 액세스할 수 없는 경우 **[!UICONTROL 보고 Source]** 필드 및 관련 필드를 편집할 수 있었습니다. (TGT-56089)

+++

## [!DNL Target Standard/Premium] 26.9.2(2026년 9월 8일)


**[!UICONTROL 추천]**

+++세부 정보 보기

* **[!DNL New]사용자 인터페이스가 피드 URL을 잘못 인코딩합니다**. 새 [!DNL Target] 인터페이스의 URL에서 권장 사항 피드를 만들 때 피드 URL이 잘못 인코딩되어 알 수 없는 오류로 인해 피드 만들기가 실패합니다. (TGT-56084)

+++

**[!UICONTROL 보고]**

+++세부 정보 보기

* **자동화된 세그먼트 보고서에 특성 값이 일관되게 표시되지 않습니다**. 자동화된 세그먼트 보고서는 [!DNL Automated Personalization] 및 [!DNL Auto-Target] 활동에 대해 일관되지 않게 표시된 특성 값과 범위를 보고합니다. 일부 자동화된 세그먼트에는 관련 값 또는 범위 대신 속성 이름만 표시되었습니다. (TGT-55855)

+++

## [!DNL Target Standard/Premium] 26.9.1(2026년 9월 1일)

**[!UICONTROL 대상자]**

+++세부 정보 보기

* **활동 전용 대상이 있는 활동을 복사할 수 없습니다**. A/B 활동이 활동 전용(로컬에서 범위 지정) 대상 규칙과 사용자 지정 코드 수정을 사용하는 경우 &quot;잘못된 대상 ID&quot; 오류와 함께 복사 및 복사 저장이 실패합니다. (TGT-55785)

+++

**[!DNL Adobe Target]MCP 서버 — 권장 사항 도구(공개 Beta)**

+++세부 정보 보기

[!DNL Adobe Target] MCP 서버는 이제 추천 도구를 노출하므로 기준, 컬렉션, 디자인, 프로모션 및 제외를 나열, 검사, 만들기 및 업데이트하고 AI 어시스턴트에서 직접 제품 카탈로그를 검색할 수 있습니다.

이 기능을 사용하려면 **Target Premium**&#x200B;이(가) 있는 권장 사항 사용 테넌트가 필요합니다. Premium이 아닌 계정에서는 사용할 수 없습니다.

자세한 내용은 [MCP 서버 도구 참조](../c-integrating-target-with-mac/mcp/target-mcp-tools-reference.md)를 참조하십시오.

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
