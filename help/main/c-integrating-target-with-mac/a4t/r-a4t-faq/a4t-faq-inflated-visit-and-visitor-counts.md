---
keywords: faq;자주 묻는 질문;analytics for target;a4T;부풀려짐;방문;방문자;부분 히트;고립됨;고아;partial-hit
description: Analytics for [!DNL Target] (A4T)을(를) 사용할 때 부풀려진 방문 및 방문자 카운트에 대한 질문에 대한 답변을 찾아보십시오. "부분 데이터"를 최소화하는 방법에 대해 알아봅니다.
title: A4T를 사용하여 부풀려진 방문 및 방문자 카운트에 대한 FAQ는 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
exl-id: e936b1f6-dc72-4ab2-9bb5-169d1710edbe
source-git-commit: 0be54d82e25eb919102f6098c1b1db76ab291675
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 69%

---

# 부풀려진 방문 및 방문자 카운트 - A4T FAQ

이 주제에서는 Analytics를 Target(A4T)의 보고 소스로 사용할 때 부풀려진 방문 및 방문자 카운트와 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## 방문 횟수에 스파이크가 표시됩니다. 이러한 방문이 부분 데이터 히트로 인해 발생하는지 어떻게 알 수 있습니까? {#section_28506672C6224ED18AC74F6A02F6F811}

+++답변
[Adobe 고객 지원](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 연락하여 부분 데이터 보고서를 검색할 수 있습니다. 이 정보는 [!DNL Analytics] UI에서 바로 이용할 수 없습니다.

+++

## 부분 데이터 히트가 발생하는 잠재적 원인은 무엇입니까? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

+++답변
부분 데이터 히트는 잘못 정렬된 보고서 세트 ID와 같은 부적절한 구현으로 인해 종종 발생합니다. 또한 느린 페이지, 페이지 오류, 활동의 리디렉션 오퍼 또는 오래된 라이브러리 버전을 포함한 타당한 원인도 있습니다.

+++

## 부분 데이터 히트를 초래할 수 있는 특정 유형의 [!DNL Target] 활동이 있습니까? {#section_69837442A9B84366BEFDA4588B31E574}

+++답변
리디렉션 오퍼에서는 즉시 사용자를 다른 페이지에 보냅니다. 이것은 [!DNL Analytics] 호출이 첫 번째 페이지에서 실행되지 않음을 의미합니다.

+++
