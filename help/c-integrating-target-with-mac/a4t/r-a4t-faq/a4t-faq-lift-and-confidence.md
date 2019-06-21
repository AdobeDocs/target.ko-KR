---
description: 이 주제에서는 Analytics를 Target(A4T)의 보고 소스로 사용할 때의 상승도 및 신뢰도와 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.
keywords: faq;자주 묻는 질문;analytics for target;a4T;상승도;ad hoc;report builder;신뢰도
seo-description: 이 주제에서는 Analytics를 Target(A4T)의 보고 소스로 사용할 때의 상승도 및 신뢰도와 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.
seo-title: 상승도 및 신뢰도 - A4T FAQ
solution: Target
title: 상승도 및 신뢰도 - A4T FAQ
topic: Standard
uuid: 7d0402f3-d6f2-422e-b69c-86e10120ac83
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 상승도 및 신뢰도 - A4T FAQ{#lift-and-confidence-a-t-faq}

이 주제에서는 Analytics를 Target(A4T)의 보고 소스로 사용할 때의 상승도 및 신뢰도와 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## A4T에 대해 오프라인 계산을 수행할 수 있습니까? {#section_55B5B750E17D414CAECBEECE27B15D81}

A4T에 사용할 오프라인 계산을 수행할 수 있지만 [!DNL Analytics]의 데이터 내보내기 단계가 필요합니다. 자세한 내용은 [신뢰 수준 및 신뢰 구간](../../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B)의 &quot;Analytics for Target(A4T)에 사용할 오프라인 계산 수행&quot;을 참조하십시오.

## 상승도는 어떻게 계산됩니까? {#section_8CAE788EED5646C4B1D64A0D22070734}

상승도는 제어 페이지 결과와 성공적인 테스트 변형 간의 차이를 비율로 나타낸 것입니다.

## 신뢰도는 어떻게 계산됩니까? {#section_97DB24D833E742988318CA65DA65DAD9}

신뢰도는 우연이 아닌 다른 이유로 측정된 전환율이 캠페인 페이지 전환율과 다르게 될 가능성입니다.

## 계산된 지표에서 상승도 및 신뢰도가 표시되지 않는 이유는 무엇입니까? {#section_D3E44E24782A409DBD88AE4D1595CB58}

현재 계산된 지표에는 상승도 및 신뢰도가 생성되지 않습니다. 하지만 대부분의 경우 상승도는 표준화 지표에 의해 표준화되기 때문에 문제가 되지 않습니다. 예를 들어, 주문 상승도를 선택하고 표준화 지표는 방문 횟수일 경우 상승도는 두 항목의 비율에 따라 계산되며 이것이 전환율입니다.

## A4T는 신뢰도 계산을 어떻게 처리합니까? {#section_66115EAF1BA34F7A8FCED7B08DA4F99C}

A4T는 데이터 제곱의 합과 함께 비이진 지표 계산을 사용합니다. 변화는 데이터 제곱의 합을 사용하여 계산됩니다. 비정상적인 주문은 고려되지 않습니다.

모든 Analytics 세그먼트를 보고서에 적용할 수 있습니다. 이를 통해 기타 세그먼트 옵션에서 &quot;비정상적인 주문&quot;을 가져올 수 있습니다. 또한 지표를 작성하여 방문자가 전환되는 횟수 등과 같은 사항을 제한할 수 있습니다.

## 상승도 및 신뢰도를 Ad Hoc 및 Report Builder에서 사용할 수 있습니까? 기본적으로 사용할 수 없다면 사용 설정할 수 있습니까? {#section_D8BB69AE700B4C5CB5FD28DB51F9A4E9}

향상도 및 신뢰도는 애드혹 또는 리포트 빌더에서 사용할 수 없으며 연속 변수에 자동으로 계산되지 않습니다. 하지만 이진 지표에 수동으로 계산할 수 있습니다.
