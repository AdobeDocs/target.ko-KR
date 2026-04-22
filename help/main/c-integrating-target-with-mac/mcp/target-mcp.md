---
solution: Target
product: target
title: MCP 클라이언트 작업
description: MCP 서버를 사용하여 Adobe Target을 MCP 클라이언트에 연결하는 방법에 대해 알아봅니다
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 6e7fa766f3da76f3e9d1f4527bfe50b9e703db4e
workflow-type: tm+mt
source-wordcount: '2376'
ht-degree: 1%

---

# MCP 클라이언트 작업 {#target-mcp}

>[!BEGINSHADEBOX]

목차:

* **[MCP 클라이언트 작업](target-mcp.md)**
* [MCP 서버 도구 참조](target-mcp-tools-reference.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>[!DNL Adobe Target] MCP 서버는 현재 **클라우드 웹**, **클라우드 데스크톱**, **클라우드 코드**, **커서** 및 **ChatGPT**&#x200B;에서 사용할 수 있습니다. 추가 MCP 호환 애플리케이션에 대한 지원은 향후 릴리스에 추가될 예정입니다.

[!DNL Adobe Target] MCP 통합을 통해 A/B 테스트, 개인화 활동 및 권장 사항 기준을 AI 도우미에서 직접 검사, 분석 및 관리할 수 있습니다. [!DNL Target]의 읽기 및 쓰기 API를 일반 언어 워크플로우로 전환합니다. 실험 포트폴리오를 감사하고, 성능 보고서를 검토하고, 대상 및 오퍼를 관리하고, UI를 탐색하거나 API 호출을 작성하지 않고도 통제된 작업을 수행할 수 있습니다. 이 페이지에서는 통합 작동 방식, 통합 기능으로 수행할 수 있는 작업 및 시작 방법을 설명합니다.

>[!IMPORTANT]
>
>MCP(Model Context Protocol)는 새로운 오픈 소스 표준이며 보안 또는 신뢰성 위험을 제시할 수 있습니다. Adobe MCP 서버 통합 및 관련 설명서는 어떠한 종류의 보증도 없이 &quot;있는 그대로&quot; 제공됩니다.
>
>MCP 클라이언트 또는 서버를 Adobe 제품에 연결하는 것은 고객이 선택한 구성이며 고객은 MCP 통합의 보안 및 적합성을 평가할 책임이 있습니다. Adobe은 잘못된 구성, MCP 오용, 서드파티 구현의 취약점 또는 MCP 지원 워크플로우를 통해 수행된 의도하지 않은 작업으로 인해 발생하는 문제에 대해 책임을 지지 않습니다.
>
>위험을 줄이기 위해 Adobe에서는 생산적인 사용을 시작하기 전에 샌드박스 환경에서 통합을 테스트하고, 이를 확인하거나 의존하기 전에 모든 MCP에서 시작한 작업과 응답을 주의 깊게 검토하고 확인하는 것을 권장합니다.

## 모델 컨텍스트 프로토콜이란 무엇입니까? {#mcp-overview}

마케팅 및 최적화 팀은 일상적인 작업을 간소화하기 위해 Anthropic Claude, OpenAI ChatGPT, Cursor, Microsoft Copilot Studio와 같은 채팅 기반 애플리케이션과 개발자 도구에 점점 더 의존하고 있습니다. 이러한 응용 프로그램은 응용 프로그램이 백엔드 도구를 대형 언어 모델(LLM)에 균일한 방식으로 노출할 수 있도록 해주는 개방형 표준인 **MCP(Model Context Protocol)**&#x200B;을 지원합니다.

[!DNL Adobe Target]은(는) 이제 MCP 호환 응용 프로그램 내에서 직접 실험, 개인화 및 권장 사항 작업을 표시하는 MCP 서버를 제공합니다. [!DNL Adobe Target]은(는) AI 도우미가 추론 및 설명을 처리하는 동안 의사 결정 및 실행 계층 역할을 하므로 팀이 여러 제품 화면을 탐색하거나 [!DNL Adobe Target] REST API에 대한 쿼리를 작성하지 않고도 최적화 인사이트에 더 빠르게 액세스할 수 있습니다.

## 주요 기능 {#mcp-capabilities}

[!DNL Adobe Target] MCP 서버는 활동, 대상, 오퍼, 권장 사항 및 구현 구성에 대한 읽기 및 쓰기 액세스를 모두 제공합니다. 통합을 통해 다음과 같은 작업을 수행할 수 있습니다.

* **실험 검사 및 감사** - UI를 탐색하지 않고 모든 활동에 대한 상태, 성능, 변경 내역 및 QA 미리 보기 링크를 가져옵니다.
* **결과 분석** - A/B, XT, AP 및 자동 타겟 활동에 대한 성능, 매출 및 A4T 보고서를 검색합니다.
* **활동 관리** - A/B 및 XT 활동을 만들고 업데이트하고 활성화합니다. 트래픽 분할, 변형, 일정 및 우선 순위를 조정합니다.
* **대상 및 오퍼 관리** - 대상, HTML 오퍼 및 JSON 오퍼를 나열, 검사 및 만듭니다.
* **권장 사항 기준 탐색** - 기준 및 장바구니 기반 알고리즘을 나열하고 검사합니다.
* **구현 감사** - at.js 설정, 응답 토큰 및 엔터티별 개정 기록을 검토합니다.

>[!NOTE]
>
>쓰기 작업(만들기, 업데이트, 활성화, 비활성화)에는 안전 주석이 포함됩니다. 명시적인 사용자 확인 없이 변경 사항이 실행되지 않습니다.

## 사용 가능한 도구 {#mcp-tools}

[!DNL Adobe Target] MCP 서버는 52개의 도구를 노출합니다. 읽기 도구는 보기 권한이 있는 연결된 모든 사용자가 사용할 수 있습니다. 쓰기 도구에는 편집자 또는 승인자 역할이 필요합니다.

### 활동 도구 - 읽기

| 도구 | 설명 |
|---|---|
| `list_target_activities` | 상태, 유형, 이름, 날짜, 우선 순위, mbox 및 작업 영역별로 서버 측 필터링이 포함된 활동 나열 |
| `list_all_target_activities` | 필터와 일치하는 모든 활동 가져오기, 결과 자동 페이지 지정 |
| `get_ab_activity` | 특정 A/B 활동에 대한 전체 세부 정보 가져오기 |
| `get_xt_activity` | 특정 경험 타기팅(XT) 활동에 대한 전체 세부 정보 가져오기 |
| `get_abt_activity` | 특정 Automated Personalization(AP) 활동에 대한 전체 세부 정보 가져오기 |

### 활동 도구 - 쓰기

| 도구 | 설명 |
|---|---|
| `create_ab_activity` | 새 A/B 테스트 활동 만들기 |
| `create_xt_activity` | 새 XT(경험 타깃팅) 활동 만들기 |
| `create_activity_from_modifications` | JavaScript 수정 사항에서 XT 활동 만들기 |
| `update_ab_activity` | 기존 A/B 활동 업데이트 |
| `update_xt_activity` | 기존 XT 활동 업데이트 |
| `update_abt_activity` | 기존 Automated Personalization 활동 업데이트 |
| `update_activity_state` | 활동 활성화, 비활성화, 일시 중지 또는 보관 |
| `update_activity_schedule` | 활동의 시작 및 종료 날짜 업데이트 |
| `update_activity_priority` | 활동의 우선 순위 업데이트 |
| `update_activity_name` | 활동 이름 바꾸기 |
| `add_activity_variant` | 활동에 새 변형(경험) 추가 |
| `update_traffic_split` | 변형 간 트래픽 할당 업데이트 |
| `update_variant_offer` | 변형에 대한 오퍼 또는 VEC 수정 사항 변경 |
| `remove_activity_variant` | 활동에서 변형 제거 |

### 오퍼 도구

| 도구 | 설명 |
|---|---|
| `list_target_offers` | 서버측 필터링 및 정렬이 포함된 오퍼 나열 |
| `list_all_target_offers` | 일치하는 모든 오퍼 가져오기, 자동 페이지 지정 |
| `get_target_offer` | 특정 오퍼에 대한 세부 정보 가져오기 |
| `create_target_offer` | 새 HTML 오퍼 만들기 |
| `create_target_json_offer` | 새 JSON 오퍼 만들기 |
| `update_target_offer` | 기존 HTML 오퍼 업데이트 |

### 대상 도구

| 도구 | 설명 |
|---|---|
| `list_target_audiences` | 서버측 필터링 및 정렬을 사용하여 대상자 나열 |
| `create_target_audience` | 선택적 타깃팅 규칙으로 대상자 만들기 |

### Mbox 및 위치 도구

| 도구 | 설명 |
|---|---|
| `list_target_mboxes` | 필터링 및 정렬이 포함된 목록 mbox |
| `list_all_target_mboxes` | 필터, 자동 페이지 지정과 일치하는 모든 mbox 가져오기 |
| `get_target_mbox` | 이름별로 특정 mbox에 대한 세부 정보 가져오기 |
| `list_target_mbox_profile_attributes` | mbox와 연결된 모든 프로필 속성 나열 |

### 속성

| 도구 | 설명 |
|---|---|
| `list_target_properties` | 모든 Target 속성 나열 |

### 보고 및 통찰력 도구

| 도구 | 설명 |
|---|---|
| `get_ab_performance_report` | A/B, 자동 할당 또는 자동 타겟 활동에 대한 성과 보고서 가져오기 |
| `get_ab_orders_report` | A/B 또는 자동 타겟 활동에 대한 주문 및 매출 보고서 가져오기 |
| `get_xt_performance_report` | XT 활동에 대한 성과 보고서 가져오기 |
| `get_xt_orders_report` | XT 활동에 대한 주문 및 매출 보고서 가져오기 |
| `get_apt_performance_report` | AP 또는 자동 타겟 활동에 대한 성과 보고서 가져오기 |
| `get_activity_insights` | 이름으로 활동을 검색하고 자세한 성능 통찰력을 얻으십시오 |
| `get_a4t_report` | 활동에 대한 A4T(Analytics for Target) 보고서 가져오기 |

### 권장 사항 도구

| 도구 | 설명 |
|---|---|
| `list_target_criteria` | 모든 권장 사항 기준 나열 |
| `get_target_criteria` | 특정 권장 사항 기준의 세부 정보 가져오기 |
| `update_target_criteria_cart` | 추천 장바구니 기반 기준 업데이트 |

### 구현 및 구성 도구

| 도구 | 설명 |
|---|---|
| `get_atjs_settings` | AT.js 설정 및 구성 가져오기 |
| `get_atjs_versions` | AT.js 버전 사용 가능 |
| `list_target_response_tokens` | Target 테넌트의 모든 응답 토큰 나열 |
| `create_target_response_token` | 새 사용자 지정 응답 토큰 만들기 |

### 감사 및 개정 도구

| 도구 | 설명 |
|---|---|
| `get_target_revisions` | 작성자로 필터링된 리소스 유형에 대한 감사 로그 가져오기 |
| `get_target_entity_revisions` | ID로 특정 엔티티의 모든 개정 버전 가져오기 |

### 유틸리티

| 도구 | 설명 |
|---|---|
| `preview_activity` | 타겟 활동에 대한 QA 미리보기 URL 생성 |
| `create_page_delivery_segment` | VEC 활동 타깃팅을 위한 페이지 전달 세그먼트 만들기 |
| `list_target_templates` | 사용 가능한 MCP 리소스 및 템플릿 나열 |
| `debug_token_info` | 현재 OAuth 토큰 범위 및 클레임 검사 |

## 사용 사례 {#mcp-use-cases}

다음 예제는 자연어를 사용하여 [!DNL Adobe Target] MCP 서버와 상호 작용하는 방법을 보여 줍니다.

| 목표 | 예제 프롬프트 |
|---|---|
| **실험 상태 감사** | &quot;현재 홈페이지에서 활성화된 A/B 테스트는 무엇입니까? 상태, 트래픽 할당 및 각각 실행된 기간을 표시합니다.&quot; |
| **성능 검토** | &quot;통계적 중요도에 도달한 모든 활성 테스트를 표시합니다. 어떤 경험이 승리하고 있습니까?&quot; |
| **매출 분석** | &quot;활동 AT4821에 대한 주문 및 매출 보고서를 가져와 방문자당 가장 많은 매출을 창출하는 경험을 요약합니다.&quot; |
| **A4T 보고** | &quot;내 체크아웃 최적화 테스트를 위한 A4T 보고서를 가져오고 Analytics측 전환 데이터를 요약합니다.&quot; |
| **활동 관리** | &quot;활동 98765을 일시 중지하고 활동 11111 우선 순위를 200으로 업데이트합니다.&quot; |
| **활동 인사이트** | &quot;내 &#39;여름 세일 배너&#39; 테스트에 대한 통찰력을 얻으십시오. 성과가 어떤 모양이며 예외 항목이 있습니까?&quot; |
| **대상자 관리** | &quot;모바일 사용자를 타겟팅하는 모든 대상을 나열하고 연결되는 활동을 보여 주십시오.&quot; |
| **QA 및 미리 보기** | &quot;활성화하기 전에 모든 변형을 검토할 수 있도록 활동 12345에 대한 QA 미리보기 URL을 생성합니다.&quot; |
| **권장 사항 검토** | &quot;이 계정에 구성된 모든 권장 사항 기준을 나열하고 사용 중인 알고리즘 유형을 요약합니다.&quot; |
| **구현 감사** | &quot;구성된 at.js 버전과 현재 활성화된 응답 토큰은 무엇입니까?&quot; |
| **감사 변경** | &quot;지난 30일 동안 활동 98765에 대한 모든 변경 사항 및 변경한 사람을 표시합니다.&quot; |

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

## 사전 요구 사항 {#mcp-prerequisites}

[!DNL Adobe Target] MCP 서버를 MCP 클라이언트에 연결하기 전에 다음 사항을 확인하십시오.

* Adobe Experience Platform 조직에 활성 [!DNL Adobe Target] 라이선스(Adobe Experience Cloud 구독)가 있습니다.
* 지원되는 MCP 호환 응용 프로그램 (현재 Claude Web, Claude Desktop, Claude Code, Cursor 또는 ChatGPT).
* Adobe Admin Console에 [!DNL Adobe Target] 권한이 구성되어 있습니다.
   * **관찰자** 역할: 읽기 전용 도구
   * **편집기** 역할: 읽기 + 도구 만들기
   * **승인자** 역할: 읽기 + 만들기 + 활성화/비활성화 도구

## [!DNL Adobe Target] MCP 서버 연결 {#mcp-connect}

>[!NOTE]
>
>[!DNL Adobe Target] MCP 서버는 인증을 위해 OAuth 2.0을 사용합니다. 처음 Target MCP 도구를 사용하면 Adobe Experience Cloud으로 리디렉션되어 로그인하고 조직을 선택한 다음 요청된 권한을 부여합니다. 정적 자격 증명이 필요하지 않습니다.

**클라우드 데스크톱 또는 클라우드 웹에서 연결하려면:**

1. MCP 클라이언트 설정을 열고 새 MCP 서버를 추가합니다.
1. 서버 URL 입력: `https://targetmcp.adobe.io/mcp`
1. 메시지가 표시되면 Adobe Experience Cloud 자격 증명으로 Adobe IMS OAuth 로그인을 완료합니다.
1. 인증되면 모든 도구를 즉시 사용할 수 있습니다. &quot;모든 활성 Target 활동 나열&quot;을 시도하여 연결을 확인하십시오.

**클라우드 코드에서 연결하려면:**

클라우드 코드 MCP 구성에 다음 내용을 추가하십시오.

```json
{
  "mcpServers": {
    "adobe-target": {
      "url": "https://targetmcp.adobe.io/mcp"
    }
  }
}
```

처음 사용할 때 메시지가 표시되면 OAuth 브라우저 플로우를 완료합니다.

**커서에서 연결하려면:**

1. **커서**&#x200B;를 열고 **설정** → **MCP** → **새 글로벌 MCP 서버 추가**&#x200B;로 이동합니다.
1. 다음 구성을 추가합니다.

```json
{
  "mcpServers": {
    "target": {
      "type": "streamable-http",
      "url": "https://targetmcp.adobe.io/mcp"
    }
  }
}
```

1. 구성을 저장합니다. [!DNL Target] MCP 서버가 사용 가능한 MCP 서버에 나타납니다.

>[!TIP]
>
>잘못된 조직의 활동이나 데이터가 나타나면 Adobe Experience Cloud에서 완전히 로그아웃한 후 MCP 서버를 다시 연결하고 재인증 중에 올바른 조직을 신중하게 선택하십시오.

## 문제 해결 {#mcp-troubleshooting}

+++OAuth 플로우가 실패하거나 잘못 리디렉션됨

1. Adobe Experience Cloud에서 완전히 로그아웃합니다.
1. adobe.com 도메인에 대한 브라우저 쿠키를 지웁니다.
1. 인증 흐름을 다시 시도하십시오.
1. 메시지가 표시되면 올바른 조직을 선택해야 합니다.
+++

+++잘못된 조직의 활동 또는 데이터가 표시됨

1. Adobe Experience Cloud에서 완전히 로그아웃합니다.
1. 클라이언트 설정에서 MCP 서버 연결을 끊고 다시 연결합니다.
1. 재인증 중에 올바른 조직을 신중하게 선택하십시오.
+++

+++도구가 오류 메시지를 반환합니다.

1. [!DNL Adobe Target]에서 작업에 필요한 권한이 있는지 확인하십시오([필수 구성 요소](#mcp-prerequisites) 참조).
1. 참조된 리소스(활동, 오퍼, 대상)가 조직에 있는지 확인합니다.
1. 활동 ID 및 기타 식별자가 올바른지 확인합니다.
+++

+++MCP 서버에 연결할 수 없습니다.

1. 인터넷 연결을 확인합니다.
1. MCP 서버 URL이 클라이언트 구성에 올바르게 입력되었는지 확인합니다.
1. MCP 클라이언트 설정에서 서버를 제거하고 다시 추가해 보십시오.
+++

## 보안 및 권한 {#mcp-security}

[!DNL Adobe Target] MCP 서버는 Adobe 사용자 계정에 보기 또는 수정 권한이 있는 데이터에만 액세스할 수 있습니다. 모든 작업은 [!DNL Target] 역할 할당 및 작업 영역 권한을 준수합니다.

서버가 요청하는 OAuth 범위는 다음과 같습니다.

* `AdobeID` — 기본 Adobe ID
* `openid` — OpenID Connect 인증
* `additional_info.projectedProductContext` — 테넌트 검색
* `read_organizations` — 조직 수준 작업
* `additional_info.roles` — 역할 기반 액세스 제어

OAuth 토큰은 각 요청에 대해 Adobe IMS에 대해 검증되며, MCP 서버에 의해 영구적으로 저장되지 않으며, 모든 통신은 HTTPS를 사용합니다.

## FAQ {#mcp-faq}

+++지원되는 MCP 클라이언트는 무엇입니까?

[!DNL Adobe Target] MCP 서버는 현재 **클라우드 웹**, **클라우드 데스크톱**, **클라우드 코드**, **커서** 및 **ChatGPT**&#x200B;에서 사용할 수 있습니다. 추가 MCP 호환 애플리케이션에 대한 지원은 향후 릴리스에 추가될 수 있습니다.
+++

+++MCP를 통해 액세스할 수 있는 [!DNL Adobe Target] 개체는 무엇입니까?

활동(A/B, XT, AP), 대상, 오퍼, 속성, mbox, 권장 사항 기준, 응답 토큰, at.js 구성, A4T 보고서 및 엔티티 개정 내역에 액세스할 수 있습니다. 읽기 및 쓰기 작업은 모두 52개의 도구에서 지원됩니다. 쓰기 작업에는 적절한 역할과 명시적 확인이 필요합니다.
+++

+++MCP 서버는 활동을 생성하거나 수정할 수 있습니까?

예. 읽기 작업 외에도 서버는 활동을 만들고, 일시 중지하며, 우선 순위를 업데이트하고, 트래픽 분할을 조정하는 등의 작업을 수행할 수 있는 쓰기 작업을 표시합니다. 쓰기 작업은 [!DNL Adobe Target] UI와 동일한 권한 모델을 따릅니다. 변경하려면 적절한 역할이 필요하며, 명시적인 사용자 확인 없이는 작업이 실행되지 않습니다.
+++

+++MCP 서버를 사용하려면 개발자 액세스 권한이 필요합니까?

아니오. MCP 서버는 마케팅 및 기술 담당자 모두를 위해 설계되었습니다. 마케터는 지원되는 모든 MCP 클라이언트에서 자연어 프롬프트를 사용하여 상호 작용할 수 있으며, 개발자는 클라우드 코드 또는 커서와 같은 도구에서 사용할 수 있습니다.
+++

+++[!DNL Adobe Target] 데이터가 MCP 클라이언트 공급자로 전송되었습니까?

프롬프트를 제출하면 MCP 클라이언트는 관련 컨텍스트(MCP 서버에서 반환된 [!DNL Adobe Target] 데이터 포함)를 처리를 위해 해당 모델로 보낼 수 있습니다. 프로덕션 데이터에 연결하기 전에 MCP 클라이언트 공급자의 개인정보 보호 및 데이터 처리 정책을 검토하십시오. Adobe의 데이터 처리는 [Adobe 개인정보 처리방침](https://www.adobe.com/kr/privacy.html) 및 [데이터 보호 약관](https://www.adobe.com/go/dpt-ww)의 적용을 받습니다.
+++

+++쓰기 작업으로 인해 라이브 활동에 의도하지 않은 변경이 발생할 수 있습니까?

쓰기 도구에는 안전 주석 및 확인 게이트가 포함됩니다. 활동 활성화, 우선 순위 변경 또는 트래픽 할당 업데이트와 같은 상태 변경 작업 전에 서버는 영향을 받는 객체, 예상되는 트래픽 영향 및 필요한 명시적 승인 단계를 표시하는 구조화된 확인을 표시합니다. 확정될 때까지 변경 사항이 없습니다.
+++

+++[!DNL Adobe Target]에서 어떤 권한이 필요합니까?

최소한 **관찰자** 역할은 모든 읽기 도구에 대한 액세스 권한을 부여합니다. **편집기** 역할을 사용하면 활동, 대상 및 오퍼를 만들 수 있습니다. 활동을 활성화, 비활성화 또는 보관하려면 **승인자** 역할이 필요합니다. 현재 액세스 수준을 잘 모를 경우 [!DNL Adobe Target] 관리자에게 문의하십시오.
+++

+++여러 Target 조직 또는 속성에서 MCP 서버를 사용할 수 있습니까?

MCP 서버는 인증된 Adobe IMS 자격 증명과 연결된 조직으로 작업을 범위화합니다. 해당 조직 내의 여러 속성에 액세스할 수 있는 경우 `list_target_properties` 도구를 사용하여 속성별로 쿼리하고 그에 따라 후속 요청을 필터링할 수 있습니다.
+++

## 관련 리소스 {#mcp-related}

* [MCP 서버 도구 참조](target-mcp-tools-reference.md)
* [모델 컨텍스트 프로토콜 설명서](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] 관리 API 참조](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
* [커서 설명서](https://docs.cursor.com/){target="_blank"}
