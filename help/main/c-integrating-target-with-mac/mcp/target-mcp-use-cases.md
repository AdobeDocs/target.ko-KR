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
source-git-commit: 40e87a3a70d51ccda99f046609ba9633719ea540
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 0%

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
| **A/B 테스트 만들기** | &quot;홈 페이지 히어로 mbox를 대상으로 하는 &#39;제어&#39;와 &#39;변형&#39;의 두 가지 경험이 있는 &#39;홈 페이지 히어로 이미지 테스트&#39;라는 A/B 테스트를 만듭니다.&quot; |
| **오퍼 만들기** | &quot;&#39;여름 제품 전체 20% 할인&#39; 홍보 배너와 함께 &#39;여름 판매 배너&#39;라는 HTML 오퍼를 만듭니다.&quot; |
| **대상 작성** | &quot;CA의 모바일 사용자를 타깃팅하는 &#39;캘리포니아에서 모바일 방문자&#39;라는 대상을 만듭니다.&quot; |
| **XT 활동 만들기** | &quot;다른 지역의 방문자에게 다른 영웅 배너를 표시하는 &#39;지역 Personalization&#39;라는 경험 타깃팅 활동을 만듭니다.&quot; |
| **활동 예약** | &quot;활동 12345 일정을 6월 1일에 시작하여 6월 30일에 끝나도록 업데이트하십시오.&quot; |
| **활성화 또는 일시 중지** | &quot;활동 12345 활성화&quot; 또는 &quot;홈 페이지 히어로 테스트 일시 중지&quot; |
| **트래픽 분할 업데이트** | &quot;활동 변수에 대한 트래픽 분할12345 70% 제어 및 30% 변형 A로 변경합니다.&quot; |
| **변형 추가** | &quot;오퍼 활동을 사용하여 A/B 활동에 &#39;휴일 테마&#39;라12345 새 변형을 67890.&quot; |

## 사용 사례 연습 {#mcp-use-case-walkthroughs}

다음 연습에서는 [!DNL Adobe Target] MCP 서버에서 자연어 프롬프트를 사용하여 일반적인 작업을 완료하는 방법을 보여 줍니다.

+++A/B 테스트 만들기

**프롬프트:**
&quot;현재 영웅을 보여주는 &#39;제어&#39;와 새로운 여름 테마 영웅 이미지를 보여주는 &#39;변형&#39;의 두 가지 경험으로 &#39;홈 페이지 영웅 이미지 테스트&#39;라는 A/B 테스트를 만듭니다. 홈 페이지 mbox를 타깃팅합니다.&quot;

AI 도우미는 `create_ab_activity` 도구를 사용하여 설명한 구성으로 활동을 만듭니다. 이 도구는 새 활동 ID와 생성된 경험에 대한 확인을 반환합니다.

+++

+++활동 성능 확인

**프롬프트:**
&quot;지난 30일 동안의 내 &#39;체크아웃 흐름 최적화&#39; 활동에 대한 성능 지표를 보여 줍니다.&quot;

AI 도우미는 `get_ab_performance_report` 또는 `get_xt_performance_report`(활동 유형에 따라 다름)을 사용하여 지정된 기간의 전환율, 방문자 수 및 기타 지표를 검색합니다.

+++

+++오퍼 관리

**프롬프트:**
&quot;HTML 오퍼 &#39;여름 세일 배너&#39;를 &#39;모든 여름 상품 20% 할인&#39;이라는 홍보 배너와 함께 만듭니다.&quot;

AI 도우미는 `create_target_offer` 도구를 사용하여 지정된 HTML 콘텐츠로 오퍼를 만들고 새 오퍼 ID로 확인을 반환합니다.

+++

+++대상자 만들기

**프롬프트:**
&quot;캘리포니아에 위치한 모바일 디바이스의 사용자를 타겟팅하는 &#39;캘리포니아 출신 모바일 방문자&#39;라는 대상을 만듭니다.&quot;

AI 도우미는 설명에서 파생된 적절한 타깃팅 규칙과 함께 `create_target_audience` 도구를 사용합니다.

+++

+++QA 미리 보기 링크 생성

**프롬프트:**
&quot;각 경험을 테스트할 수 있도록 활동 12345에 대한 미리보기 URL을 생성합니다.&quot;

AI 도우미는 `preview_activity` 도구를 사용하여 대상 타깃팅을 우회하는 클릭 가능한 URL을 생성하므로 각 경험을 브라우저에서 직접 볼 수 있습니다.

+++

+++경험 타깃팅 활동 만들기

**프롬프트:**
&quot;다른 지역의 방문자에게 다른 영웅 배너를 표시하는 &#39;지역 Personalization&#39;라는 경험 타깃팅 활동을 만듭니다.&quot;

AI 도우미는 `create_xt_activity`을(를) 사용하여 설명한 지역에 따라 대상 기반 경험 매핑으로 활동을 만듭니다.

+++

+++활동 예약

**프롬프트:**
&quot;5월 1일에 시작하여 5월 31일에 끝나도록 활동 12345 일정을 업데이트합니다.&quot;

AI 도우미는 `update_activity_schedule` 도구를 사용하여 새 시작 날짜와 종료 날짜를 활동에 적용합니다.

+++

## 관련 리소스 {#mcp-use-cases-related}

* [개요](target-mcp.md)
* [시작하기](target-mcp-get-started.md)
* [MCP 서버 도구 참조](target-mcp-tools-reference.md)
* [모델 컨텍스트 프로토콜 설명서](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] 관리 API 참조](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
