---
title: 복잡한 대상 규칙
description: 벌크 값 제한 및 여러 조건에 규칙을 분할하는 방법을 포함하여 플래그의 큰 대상 규칙 세트 또는 복잡한 대상 규칙 세트로 작업하는 방법을 알아봅니다.
hide: true
exl-id: 37e037b6-45eb-4261-b580-30d94d8e55da
source-git-commit: eeba7af62ab101e687852ce993a001832ce4a83b
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---

# 복잡한 대상 규칙 {#complex-rules}

## 복잡한 규칙에 중첩 논리 사용 {#nested-logic}

중첩 논리를 사용하면 여러 대상 조건을 정확한 AND/OR 컨트롤과 결합할 수 있습니다. 활성화하려면:

1. 필요한 대상 조건을 추가합니다.
2. 대상 규칙 섹션에서 **중첩 논리**&#x200B;을(를) 사용하도록 설정합니다.
3. 각 조건에는 숫자가 지정됩니다. 이러한 숫자를 참조하는 논리 표현식을 입력합니다(예: ).
   * `1 and (2 or 3)`
   * `(1 and 2) or 3`
   * `(1 and 2) or (3 and 4)`

## 참조: {#see-also}

* [기능 플래그 및 기능 그룹의 대상자](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
