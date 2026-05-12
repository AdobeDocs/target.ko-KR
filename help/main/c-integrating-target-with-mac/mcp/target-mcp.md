---
solution: Target
product: target
title: Adobe Target MCP 서버 개요
description: Adobe Target MCP 서버가 무엇인지, 주요 기능 및 AI 어시스턴트에 연결하는 방법에 대해 알아봅니다.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: d5d7a57ce6a3188f02e680c24849d773cb53457a
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 0%

---

# [!DNL Adobe Target] MCP 서버 {#target-mcp}

[!DNL Adobe Target] MCP 통합을 사용하면 AI 어시스턴트에서 직접 A/B 테스트, 개인화 활동 및 권장 사항 기준을 검사하고 분석할 수 있습니다. [!DNL Target]의 실험 및 개인화 데이터를 일반 언어 워크플로우로 전환합니다. UI를 탐색하거나 API 호출을 작성하지 않고도 실험 포트폴리오를 감사하고, 성능 보고서를 검토하고, 대상자와 오퍼를 탐색합니다.

>[!AVAILABILITY]
>
>[!DNL Adobe Target] MCP 서버는 **공개 Beta**&#x200B;의 모든 고객이 사용할 수 있습니다. 현재 **클라우드 웹**, **클라우드 데스크톱**, **클라우드 코드**, **커서** 및 **ChatGPT**&#x200B;에서 지원됩니다. 추가 MCP 호환 애플리케이션에 대한 지원은 향후 릴리스에 추가될 예정입니다.


## 모델 컨텍스트 프로토콜이란 무엇입니까? {#mcp-overview}

마케팅 및 최적화 팀은 일상적인 작업을 간소화하기 위해 Anthropic Claude, OpenAI ChatGPT, Cursor, Microsoft Copilot Studio와 같은 채팅 기반 애플리케이션과 개발자 도구에 점점 더 의존하고 있습니다. 이러한 응용 프로그램은 응용 프로그램이 백엔드 도구를 대형 언어 모델(LLM)에 균일한 방식으로 노출할 수 있도록 해주는 개방형 표준인 **MCP(Model Context Protocol)**&#x200B;을 지원합니다.

[!DNL Adobe Target]은(는) 이제 MCP 호환 응용 프로그램 내에서 직접 실험, 개인화 및 권장 사항 작업을 표시하는 MCP 서버를 제공합니다. [!DNL Adobe Target]은(는) AI 도우미가 추론 및 설명을 처리하는 동안 의사 결정 및 실행 계층 역할을 하므로 팀이 여러 제품 화면을 탐색하거나 [!DNL Adobe Target] REST API에 대한 쿼리를 작성하지 않고도 최적화 인사이트에 더 빠르게 액세스할 수 있습니다.


>[!IMPORTANT]
>
>MCP(Model Context Protocol)는 새로운 오픈 소스 표준이며 보안 또는 신뢰성 위험을 제시할 수 있습니다. Adobe MCP 서버 통합 및 관련 설명서는 어떠한 종류의 보증도 없이 &quot;있는 그대로&quot; 제공됩니다.
>
>MCP 클라이언트 또는 서버를 Adobe 제품에 연결하는 것은 고객이 선택한 구성이며 고객은 MCP 통합의 보안 및 적합성을 평가할 책임이 있습니다. Adobe은 잘못된 구성, MCP 오용, 서드파티 구현의 취약점 또는 MCP 지원 워크플로우를 통해 수행된 의도하지 않은 작업으로 인해 발생하는 문제에 대해 책임을 지지 않습니다.
>
>위험을 줄이기 위해 Adobe에서는 생산적인 사용을 시작하기 전에 샌드박스 환경에서 통합을 테스트하고, 이를 확인하거나 의존하기 전에 모든 MCP에서 시작한 작업과 응답을 주의 깊게 검토하고 확인하는 것을 권장합니다.

## 주요 기능 {#mcp-capabilities}

[!DNL Adobe Target] MCP 서버는 활동, 대상, 오퍼, 권장 사항 및 구현 구성에 대한 읽기 액세스를 제공합니다. 통합을 통해 다음과 같은 작업을 수행할 수 있습니다.

* **실험 검사 및 감사** - UI를 탐색하지 않고 모든 활동에 대한 상태, 성능, 변경 내역 및 QA 미리 보기 링크를 가져옵니다.
* **결과 분석** - A/B, XT, AP 및 자동 타겟 활동에 대한 성능, 매출 및 A4T 보고서를 검색합니다.
* **활동 살펴보기** - A/B 및 XT 활동을 나열, 검사 및 분석합니다.
* **대상 및 오퍼 살펴보기** - 대상, HTML 오퍼 및 JSON 오퍼를 나열하고 검사합니다.
* **권장 사항 기준 탐색** - 기준 및 장바구니 기반 알고리즘을 나열하고 검사합니다.
* **구현 감사** - at.js 설정, 응답 토큰 및 엔터티별 개정 기록을 검토합니다.

>[!NOTE]
>
>쓰기 도구(만들기, 업데이트, 활성화, 비활성화)는 **공개 Beta**&#x200B;의 공개 MCP 카탈로그를 통해 노출되지 않습니다. 현재 사용 가능한 모든 도구는 읽기 전용입니다. 쓰기 액세스 권한은 향후 릴리스에서 사용할 수 있습니다.

[!DNL Adobe Target] MCP 서버는 활동 검사 및 보고에서 대상 탐색 및 QA 미리 보기에 이르기까지 10개의 범주에 걸쳐 23개의 읽기 전용 도구를 노출합니다. 전체 매개 변수 참조에 대해서는 [MCP 서버 도구 참조](target-mcp-tools-reference.md)를 참조하십시오.

단계별 안내 연습을 포함하여 [!DNL Adobe Target] MCP 서버로 수행할 수 있는 작업을 살펴보려면 [사용 사례 및 연습](target-mcp-use-cases.md)을 참조하세요.

필수 구성 요소, 클라이언트별 구성 및 문제 해결 등 [!DNL Adobe Target] MCP 서버를 AI Assistant에 연결하려면 [시작하기](target-mcp-get-started.md)를 참조하십시오.

## FAQ {#mcp-faq}

+++지원되는 MCP 클라이언트는 무엇입니까?

[!DNL Adobe Target] MCP 서버는 현재 **클라우드 웹**, **클라우드 데스크톱**, **클라우드 코드**, **커서** 및 **ChatGPT**&#x200B;에서 사용할 수 있습니다. 추가 MCP 호환 애플리케이션에 대한 지원은 향후 릴리스에 추가될 수 있습니다.
+++

+++MCP를 통해 액세스할 수 있는 [!DNL Adobe Target] 개체는 무엇입니까?

활동(A/B, XT, AP), 대상, 오퍼, 속성, mbox, 권장 사항 기준, 응답 토큰, at.js 구성, A4T 보고서 및 엔티티 개정 내역에 액세스할 수 있습니다. 현재 사용 가능한 23개의 모든 도구는 읽기 전용입니다.
+++

+++MCP 서버는 활동을 생성하거나 수정할 수 있습니까?

공용 Beta에서는 사용할 수 없습니다. 공개 MCP 카탈로그는 현재 23개의 읽기 전용 도구를 노출합니다. 쓰기 작업(만들기, 업데이트, 활성화, 비활성화)은 아직 공용 MCP 서버를 통해 사용할 수 없습니다. 쓰기 액세스 권한은 향후 릴리스에서 사용할 수 있습니다.
+++

+++MCP 서버를 사용하려면 개발자 액세스 권한이 필요합니까?

아니오. MCP 서버는 마케팅 및 기술 담당자 모두를 위해 설계되었습니다. 마케터는 지원되는 모든 MCP 클라이언트에서 자연어 프롬프트를 사용하여 상호 작용할 수 있으며, 개발자는 클라우드 코드 또는 커서와 같은 도구에서 사용할 수 있습니다.
+++

+++[!DNL Adobe Target] 데이터가 MCP 클라이언트 공급자로 전송되었습니까?

프롬프트를 제출하면 MCP 클라이언트는 관련 컨텍스트(MCP 서버에서 반환된 [!DNL Adobe Target] 데이터 포함)를 처리를 위해 해당 모델로 보낼 수 있습니다. 프로덕션 데이터에 연결하기 전에 MCP 클라이언트 공급자의 개인정보 보호 및 데이터 처리 정책을 검토하십시오. Adobe의 데이터 처리는 [Adobe 개인정보 처리방침](https://www.adobe.com/privacy.html) 및 [데이터 보호 약관](https://www.adobe.com/go/dpt-ww)의 적용을 받습니다.
+++

+++쓰기 작업으로 인해 라이브 활동에 의도하지 않은 변경이 발생할 수 있습니까?

공개 Beta의 공개 MCP 카탈로그를 통해서는 쓰기 도구를 사용할 수 없습니다. 현재 노출된 23개의 도구는 모두 읽기 전용입니다. 향후 릴리스에 쓰기 도구가 도입되면 명시적 사용자 확인 없이 상태 변경 작업이 실행되지 않도록 안전 주석과 확인 게이트를 포함하게 됩니다.
+++

+++[!DNL Adobe Target]에서 어떤 권한이 필요합니까?

**관찰자** 이상의 역할을 통해 Public Beta에서 사용할 수 있는 23개의 읽기 전용 도구에 대한 액세스 권한을 부여합니다. 쓰기 도구는 아직 공개 MCP 카탈로그를 통해 노출되지 않았으므로 편집자 및 승인자 역할 권한이 현재 추가 MCP 도구를 잠금 해제하지 않습니다. 현재 액세스 수준을 잘 모를 경우 [!DNL Adobe Target] 관리자에게 문의하십시오.
+++

+++여러 Target 조직 또는 속성에서 MCP 서버를 사용할 수 있습니까?

MCP 서버는 인증된 Adobe IMS 자격 증명과 연결된 조직으로 작업을 범위화합니다. 해당 조직 내의 여러 속성에 액세스할 수 있는 경우 `list_target_properties` 도구를 사용하여 속성별로 쿼리하고 그에 따라 후속 요청을 필터링할 수 있습니다.
+++

## 관련 리소스 {#mcp-related}

* [시작하기](target-mcp-get-started.md)
* [사용 사례 및 연습](target-mcp-use-cases.md)
* [MCP 서버 도구 참조](target-mcp-tools-reference.md)
* [모델 컨텍스트 프로토콜 설명서](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] 관리 API 참조](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
* [커서 설명서](https://docs.cursor.com/){target="_blank"}
