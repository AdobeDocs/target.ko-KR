---
solution: Target
product: target
title: Adobe Target MCP 서버 — 사용 사례 및 연습
description: Adobe Target MCP 서버에 대한 일반적인 사용 사례와 단계별 프롬프트 연습을 살펴봅니다.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 53dc7056ca62339a682756fe1b39e6af349f3ae6
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 1%

---

# [!DNL Adobe Target] MCP 서버 — 사용 사례 및 연습 {#target-mcp-use-cases}

>[!AVAILABILITY]
>
>[!DNL Adobe Target] MCP 서버는 **공개 Beta**&#x200B;의 모든 고객이 사용할 수 있습니다. 현재 **클라우드 웹**, **클라우드 데스크톱**, **클라우드 코드**, **커서** 및 **ChatGPT**&#x200B;에서 지원됩니다.

이 페이지에서는 빠른 조회, 여러 단계 분석 및 보고 작업에 이르기까지 자연어 프롬프트를 사용하여 [!DNL Adobe Target] MCP 서버를 통해 수행할 수 있는 작업을 보여 줍니다.

>[!IMPORTANT]
>
>MCP(Model Context Protocol)는 새로운 오픈 소스 표준이며 보안 또는 신뢰성 위험을 제시할 수 있습니다. Adobe MCP 서버 통합 및 관련 설명서는 어떠한 종류의 보증도 없이 &quot;있는 그대로&quot; 제공됩니다.
>
>MCP 클라이언트 또는 서버를 Adobe 제품에 연결하는 것은 고객이 선택한 구성이며 고객은 MCP 통합의 보안 및 적합성을 평가할 책임이 있습니다. Adobe은 잘못된 구성, MCP 오용, 서드파티 구현의 취약점 또는 MCP 지원 워크플로우를 통해 수행된 의도하지 않은 작업으로 인해 발생하는 문제에 대해 책임을 지지 않습니다.
>
>위험을 줄이기 위해 Adobe에서는 생산적인 사용을 시작하기 전에 샌드박스 환경에서 통합을 테스트하고, 이를 확인하거나 의존하기 전에 모든 MCP에서 시작한 작업과 응답을 주의 깊게 검토하고 확인하는 것을 권장합니다.

## 사용 사례 {#mcp-use-cases}

다음 예제는 자연어를 사용하여 [!DNL Adobe Target] MCP 서버와 상호 작용하는 방법을 보여 줍니다.

| 목표 | 예제 프롬프트 |
|---|---|
| **실험 상태 감사** | &quot;현재 홈페이지에서 활성화된 A/B 테스트는 무엇입니까? 상태, 트래픽 할당 및 각각 실행된 기간을 표시합니다.&quot; |
| **성능 검토** | &quot;통계적 중요도에 도달한 모든 활성 테스트를 표시합니다. 어떤 경험이 승리하고 있습니까?&quot; |
| **매출 분석** | &quot;활동 AT4821에 대한 주문 및 매출 보고서를 가져와 방문자당 가장 많은 매출을 창출하는 경험을 요약합니다.&quot; |
| **A4T 보고** | &quot;내 체크아웃 최적화 테스트를 위한 A4T 보고서를 가져오고 Analytics측 전환 데이터를 요약합니다.&quot; |
| **활동 인사이트** | &quot;내 &#39;여름 세일 배너&#39; 테스트에 대한 통찰력을 얻으십시오. 성과가 어떤 모양이며 예외 항목이 있습니까?&quot; |
| **대상자 관리** | &quot;모바일 사용자를 타겟팅하는 모든 대상을 나열하고 연결되는 활동을 보여 주십시오.&quot; |
| **QA 및 미리 보기** | &quot;활성화하기 전에 모든 변형을 검토할 수 있도록 활동 12345에 대한 QA 미리보기 URL을 생성합니다.&quot; |
<!-- | **Recommendations review** | "List all Recommendations criteria configured in this account and summarize the algorithm types in use." | -->
| **구현 감사** | &quot;구성된 at.js 버전과 현재 활성화된 응답 토큰은 무엇입니까?&quot; |
| **감사 변경** | &quot;지난 30일 동안 활동 98765에 대한 모든 변경 사항 및 변경 사항을 적용한 사용자를 표시합니다.&quot; |

## 사용 사례 연습 {#mcp-use-case-walkthroughs}

다음 연습에서는 [!DNL Adobe Target] MCP 서버에서 자연어 프롬프트를 사용하여 일반적인 작업을 완료하는 방법을 보여 줍니다.

<!--
+++Creating an A/B test

**Prompt:**
"Create an A/B test called 'Homepage Hero Image Test' with two experiences: 'Control' showing the current hero and 'Variant' showing a new summer-themed hero image. Target the homepage mbox."

The AI assistant uses the `create_ab_activity` tool to create the activity with the configuration you described. The tool returns the new activity ID and a confirmation of the created experiences.

+++
-->

+++활동 성능 확인

**프롬프트:**
&quot;지난 30일 동안의 내 &#39;체크아웃 흐름 최적화&#39; 활동에 대한 성능 지표를 보여 줍니다.&quot;

AI 도우미는 `get_ab_performance_report` 또는 `get_xt_performance_report`(활동 유형에 따라 다름)을 사용하여 지정된 기간의 전환율, 방문자 수 및 기타 지표를 검색합니다.

+++

<!--
+++Managing offers

**Prompt:**
"Create an HTML offer called 'Summer Sale Banner' with a promotional banner that says '20% off all summer items'."

The AI assistant uses the `create_target_offer` tool to create the offer with your specified HTML content and returns a confirmation with the new offer ID.

+++

+++Building an audience

**Prompt:**
"Create an audience called 'Mobile Visitors from California' that targets users on mobile devices located in California."

The AI assistant uses the `create_target_audience` tool with the appropriate targeting rules derived from your description.

+++
-->

+++QA 미리 보기 링크 생성

**프롬프트:**
&quot;각 경험을 테스트할 수 있도록 활동 12345에 대한 미리보기 URL을 생성합니다.&quot;

AI 도우미는 `preview_activity` 도구를 사용하여 대상 타깃팅을 우회하는 클릭 가능한 URL을 생성하므로 각 경험을 브라우저에서 직접 볼 수 있습니다.

+++

<!--
+++Creating an Experience Targeting activity

**Prompt:**
"Create an Experience Targeting activity called 'Geo Personalization' that shows different hero banners to visitors from different regions."

The AI assistant uses `create_xt_activity` to build the activity with audience-based experience mapping according to the regions you describe.

+++

+++Scheduling an activity

**Prompt:**
"Update the schedule for activity 12345 to start on May 1st and end on May 31st."

The AI assistant uses the `update_activity_schedule` tool to apply the new start and end dates to the activity.

+++
-->

## 관련 리소스 {#mcp-use-cases-related}

* [개요](target-mcp.md)
* [시작하기](target-mcp-get-started.md)
* [MCP 서버 도구 참조](target-mcp-tools-reference.md)
* [모델 컨텍스트 프로토콜 설명서](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] 관리 API 참조](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
