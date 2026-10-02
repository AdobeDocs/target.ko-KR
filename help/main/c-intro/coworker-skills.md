---
keywords: Adobe Target;동료;AI;스킬;실험;권장 사항
title: Adobe Target을 위한 동료 기술
description: 활동 검색, 테스트 만들기, 분석, 대상 구성 및 권장 사항 문제 해결 등 Adobe Target에서 사용할 수 있는 동료 기술에 대해 알아봅니다.
feature: Overview
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: 4b90f47050b63c7e1e6ac5019d45a7b99b3a33b8
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 2%
---

# Adobe Target을 위한 동료 기술 {#coworker-skills}

>[!BEGINSHADEBOX]

**이 페이지에서:** 활동 및 대상 탐색, 테스트 만들기 및 구성, 성능 분석, 대상 구성, 권장 사항 관리 등 Adobe Target에서 사용할 수 있는 Coworker 기술을 살펴보십시오.

>[!ENDSHADEBOX]

동료 기술은 Adobe Target 실무자가 자연어를 사용하여 테스트 및 개인화 프로그램을 탐색하고, 활동을 만들고 구성하며, 결과를 분석하고, 배달 문제를 해결하는 데 도움이 됩니다. 동료 채팅에서 수행할 작업을 설명한 다음, 작업을 수행하기 전에 반환된 권장 사항, 구성 또는 분석을 검토하십시오.

[!DNL Adobe Target] MCP 도구 및 Coworker는 별도로 문서화되어 있으며 다양한 기능을 제공합니다.

* [Target MCP](../c-integrating-target-with-mac/mcp/target-mcp-tools-reference.md) 지원되는 활동 유형, 매개 변수, 권한, 읽기 또는 쓰기 범위를 포함하여 직접 MCP 서버에 의해 노출된 개별 도구를 문서화합니다.
* [Coworker](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/use-cases/overview#target-activities-and-audiences)에서는 기능을 결합하고 추가 워크플로를 적용할 수 있는 별도의 자연어 오케스트레이션 계층을 제공합니다.

다음 표는 관련 기능을 개략적으로 비교한 것입니다.

| 기능 | Target MCP | Coworker |
| --- | --- | --- |
| 실행 중인 실험, 대상, 오퍼 또는 최근에 변경된 항목 나열 | 예 | 예 |
| Automated Personalization 활동 만들기 | 아니요 | 아니오 |
| Target 대상자 만들기 | 예 | 예 |
| Target VEC 활동, 경험 타깃팅 활동 또는 A/B 테스트 만들기 | 예 | 예 |
| Target Recommendations 활동 만들기 | 예 | 예 |
| Target에서 HTML 또는 JSON 오퍼 만들기 | 예 | 예 |
| Target 활동에서 AEM 컨텐츠 조각 사용 | 아니오 | 예 |
| 작동 중인 항목과 다음에 테스트할 항목 추천 | 일반 조언 없음 | 예 |


## Target 플러그인

**Target** 플러그인에서 다음 기술을 사용할 수 있습니다.

* **대상 찾아보기**

  활동, 대상, 오퍼 및 관련 구성을 포함하여 Target 엔터티에 대한 읽기 전용 검색, 검사 및 계산을 제공합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;내 활성 활동을 나열합니다.&quot;
* &quot;현재 실행 중인 활동은 몇 개입니까?&quot;
* &quot;이 활동에서 사용하는 대상과 오퍼를 표시합니다.&quot;

>[!ENDSHADEBOX]

* **Target 활동 평결**

  중요도 계산 및 구성 검사를 사용하여 활동을 전송할 준비가 되었는지, 더 많은 데이터를 기다려야 하는지, 중지해야 하는지 또는 수정이 필요한지 여부를 결정합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;이 테스트를 배송해야 합니까?&quot;
* &quot;이 활동을 중지할 준비가 되었습니까?&quot;
* &quot;현재 활동 구성에 문제가 있습니까?&quot;

>[!ENDSHADEBOX]

* **대상 디자인**

  활동 및 오퍼를 만들고 구성하고, QA URL을 생성하고, 오퍼 컨텐츠를 작성하거나 최적화합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;홈 페이지에 대한 A/B 테스트를 만듭니다.&quot;
* &quot;재방문자 경험에 대한 오퍼를 만듭니다.&quot;
* &quot;이 활동에 대한 QA URL을 생성합니다.&quot;

>[!ENDSHADEBOX]

* **대상 VEC**

  시각적 경험 작성기 활동 및 해당 페이지 전달 대상을 만들고 편집합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;홈 페이지에 대한 VEC A/B 테스트를 만듭니다.&quot;
* &quot;내 VEC 활동에서 영웅 헤드라인을 편집합니다.&quot;
* &quot;이 VEC 활동에 대한 페이지 전달 대상을 만듭니다.&quot;

>[!ENDSHADEBOX]

* **대상 설정**

  안내서는 사전 요구 사항, 예약, QA 및 활성화를 포함하여 A/B, 경험 타기팅 또는 시각적 경험 작성기 활동 생성을 완료합니다.

>[!BEGINSHADEBOX]

    *예제 프롬프트:*
    
    * &quot;첫 번째 테스트를 만드는 데 도움을 주세요.&quot;
    * &quot;경험 타깃팅 활동을 만들기 전에 필요한 사항은 무엇입니까?&quot;
    * &quot;이 활동을 예약, QA 및 활성화하는 방법을 살펴봅니다.&quot;

>[!ENDSHADEBOX]

* **Target 인텔리전스**

  위험, 충돌, 잘못된 구성, 위생 문제 및 빠른 승리에 대해 Target 프로그램을 감사합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;내 Target 활동 감사&quot;
* &quot;내 활동에서 충돌 또는 구성 위험을 찾습니다.&quot;
* &quot;어떤 빠른 승리로 Target 프로그램의 위생을 개선할 수 있습니까?&quot;

>[!ENDSHADEBOX]

* **Target 전략가**

  우승 패턴에 대한 이전 Target 데이터를 분석하고 향후 테스트를 권장합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;과거 결과를 기반으로 다음에 무엇을 테스트해야 합니까?&quot;
* &quot;가장 성과가 좋은 테스트에 나타나는 패턴은 무엇입니까?&quot;
* &quot;이 활동의 결과에 따라 후속 테스트를 권장합니다.&quot;

>[!ENDSHADEBOX]

* **Target 테스트 계산기**

  복수 비교를 위해 Bonferroni 수정을 사용하여 전환 및 매출 지표에 대한 A/B/n 샘플 크기, 기간 및 감지 가능한 상승도를 계획합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;어떤 샘플 크기가 필요합니까?&quot;
* &quot;5% 상승도를 감지하려면 이 A/B 테스트를 얼마 동안 실행해야 합니까?&quot;
* &quot;이 트래픽으로 어떤 상승도를 측정할 수 있습니까?&quot;

>[!ENDSHADEBOX]

* **대상 Portfolio 보고서**

  읽기 전용, 프로그램 전체 성능 롤업, 활동 트렌드 및 모멘텀 분석을 제공합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;내 최고의 테스트와 최악의 테스트는 무엇입니까?&quot;
* &quot;내 활동 전반의 성능 트렌드를 표시합니다.&quot;
* &quot;어떤 활동이 최근 추진력을 얻었거나 잃었습니까?&quot;

>[!ENDSHADEBOX]

* **대상 작성기**

  자연어 설명 또는 명시적 규칙에서 Target 네이티브 대상을 만들거나 편집합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;재방문자를 위한 대상자 만들기&quot;
* &quot;유기 검색 방문자를 포함하도록 이 대상을 편집합니다.&quot;
* &quot;가격 페이지를 본 방문자에 대한 Target 대상을 만듭니다.&quot;

>[!ENDSHADEBOX]

* **Target Recommendations**

  Target Recommendations 활동 및 구성을 관리하고 사용합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;권장 사항 활동을 만듭니다.&quot;
* &quot;내 권장 사항 활동 및 구성을 표시합니다.&quot;
* &quot;이 권장 사항 활동에 대한 설정을 업데이트합니다.&quot;

>[!ENDSHADEBOX]

* **Target 권장 사항 진단**

  Recommendations 게재, 구성, 카탈로그 및 피드 문제를 진단합니다.

>[!BEGINSHADEBOX]

*예제 프롬프트:*

* &quot;내 권장 사항이 표시되지 않는 이유는 무엇입니까?&quot;
* &quot;이 Recommendations 활동에 대한 피드 및 카탈로그 구성을 진단합니다.&quot;
* &quot;게재 또는 구성 문제가 내 권장 사항에 영향을 줍니까?&quot;

>[!ENDSHADEBOX]
