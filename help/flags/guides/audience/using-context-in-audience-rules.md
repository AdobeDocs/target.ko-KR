---
title: 대상 규칙에서 컨텍스트 사용
description: 플래그의 기능 플래그 및 기능 그룹에 대한 대상 규칙의 컨텍스트 속성을 사용하는 방법을 알아봅니다.
badge: label="Beta" type="Informative"
hide: true
exl-id: 0367f475-9209-4d53-86b4-a739a73a23a7
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---

# 대상 규칙에서 컨텍스트 사용 {#context-in-audience-rules}

컨텍스트 속성은 런타임 시 클라이언트 응용 프로그램에서 제공하는 값입니다. 이를 통해 사용자의 활성 언어, 장치 유형 또는 애플리케이션 상태와 같은 동적 세션 수준 정보를 기반으로 사용자를 타깃팅할 수 있습니다.

컨텍스트 속성은 웹 및 모바일 클라이언트와 관련이 있습니다.

## 컨텍스트 속성 작동 방식 {#how-context-attributes-work}

응용 프로그램에서 기능 플래그를 평가할 때 컨텍스트 속성을 플래그로 전달합니다. 콘솔에서 이러한 값을 확인하는 규칙을 정의하고, 플랫폼은 평가 시 이를 사용하여 사용자가 적격 상태인지 여부를 확인합니다.

## 컨텍스트 속성 추가 {#adding-context-attribute}

대상 규칙에 컨텍스트 속성을 추가하려면 다음 작업을 수행하십시오.

1. 콘솔에서 기능 플래그 또는 기능 그룹을 엽니다.
2. **대상자** 탭으로 이동합니다.
3. **Context**&#x200B;에서 새 조건을 추가합니다.
4. 컨텍스트 속성, 연산자 및 값을 선택합니다.

필요한 컨텍스트 특성이 목록에 없으면 새 특성을 만들 수 있습니다. [컨텍스트 특성 만들기](creating-your-context-attributes.md)를 참조하십시오.

## 참조: {#see-also}

* [기능 플래그 및 기능 그룹의 대상자](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
