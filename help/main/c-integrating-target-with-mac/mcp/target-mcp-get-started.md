---
solution: Target
product: target
title: Adobe Target MCP 서버 시작
description: 사전 요구 사항, 클라이언트 구성 및 문제 해결 등 Adobe Target MCP 서버를 AI Assistant에 연결하는 방법을 알아봅니다.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: d5d7a57ce6a3188f02e680c24849d773cb53457a
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# [!DNL Adobe Target] MCP 서버 시작 {#target-mcp-get-started}

>[!AVAILABILITY]
>
>[!DNL Adobe Target] MCP 서버는 **공개 Beta**&#x200B;의 모든 고객이 사용할 수 있습니다. 현재 **클라우드 웹**, **클라우드 데스크톱**, **클라우드 코드**, **커서** 및 **ChatGPT**&#x200B;에서 지원됩니다.

이 페이지에서는 [!DNL Adobe Target] MCP 서버를 AI 도우미에 연결하고 설정을 확인하는 데 필요한 모든 과정을 안내합니다.

>[!IMPORTANT]
>
>MCP(Model Context Protocol)는 새로운 오픈 소스 표준이며 보안 또는 신뢰성 위험을 제시할 수 있습니다. Adobe MCP 서버 통합 및 관련 설명서는 어떠한 종류의 보증도 없이 &quot;있는 그대로&quot; 제공됩니다.
>
>MCP 클라이언트 또는 서버를 Adobe 제품에 연결하는 것은 고객이 선택한 구성이며 고객은 MCP 통합의 보안 및 적합성을 평가할 책임이 있습니다. Adobe은 잘못된 구성, MCP 오용, 서드파티 구현의 취약점 또는 MCP 지원 워크플로우를 통해 수행된 의도하지 않은 작업으로 인해 발생하는 문제에 대해 책임을 지지 않습니다.
>
>위험을 줄이기 위해 Adobe에서는 생산적인 사용을 시작하기 전에 샌드박스 환경에서 통합을 테스트하고, 이를 확인하거나 의존하기 전에 모든 MCP에서 시작한 작업과 응답을 주의 깊게 검토하고 확인하는 것을 권장합니다.

## 사전 요구 사항 {#mcp-prerequisites}

[!DNL Adobe Target] MCP 서버를 MCP 클라이언트에 연결하기 전에 다음 사항을 확인하십시오.

* Adobe Experience Platform 조직에 활성 [!DNL Adobe Target] 라이선스(Adobe Experience Cloud 구독)가 있습니다.
* 지원되는 MCP 호환 응용 프로그램 (현재 Claude Web, Claude Desktop, Claude Code, Cursor 또는 ChatGPT).
* Adobe Admin Console에 [!DNL Adobe Target] 권한이 구성되어 있습니다. 공개 Beta에서 사용할 수 있는 23개의 모든 도구는 읽기 전용입니다. **관찰자** 이상의 역할만 있으면 MCP 서버를 사용할 수 있습니다.

>[!NOTE]
>
>쓰기 도구(만들기, 업데이트, 활성화, 비활성화)는 공개 Beta의 공개 MCP 카탈로그를 통해 노출되지 않습니다. 편집자 및 승인자 역할 권한은 현재 추가 도구를 잠금 해제하지 않습니다. 쓰기 액세스 권한은 향후 릴리스에서 사용할 수 있습니다.

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

1. [!DNL Adobe Target]에서 **Observer** 역할 이상이 있는지 확인하십시오([필수 구성 요소](#mcp-prerequisites) 참조).
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

## 관련 리소스 {#mcp-get-started-related}

* [개요](target-mcp.md)
* [사용 사례 및 연습](target-mcp-use-cases.md)
* [MCP 서버 도구 참조](target-mcp-tools-reference.md)
* [모델 컨텍스트 프로토콜 설명서](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] 관리 API 참조](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
