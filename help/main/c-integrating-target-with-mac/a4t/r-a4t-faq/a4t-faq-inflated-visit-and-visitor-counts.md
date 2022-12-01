---
keywords: faq;자주 묻는 질문;analytics for target;a4T;부풀려짐;방문;방문자;부분 히트;고립됨;고아;partial-hit
description: Analytics를 용 [!DNL Target] (A4T). 부분 데이터를 최소화하는 방법을 알아봅니다.
title: A4T를 사용한 부풀려진 방문 및 방문자 수에 대한 FAQ는 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
exl-id: e936b1f6-dc72-4ab2-9bb5-169d1710edbe
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 49%

---

# 부풀려진 방문 및 방문자 카운트 - A4T FAQ

이 주제에서는 Analytics를 Target(A4T)의 보고 소스로 사용할 때 부풀려진 방문 및 방문자 카운트와 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## Analytics 데이터에 페이지 보기 횟수나 기타 변수 값이 없는 방문이 표시되는 이유는 무엇입니까? {#section_4D8C2C2D766842E6B12F3ECC774A64D5}

+++응답 시기 [!DNL Adobe Analytics] 측정하는 데 사용됨 [!DNL Target] 활동(A4T라고 함), [!DNL Analytics] 가 없는 경우 사용할 수 없는 데이터를 수집합니다 [!DNL Target] 활동 을 만들 수 있습니다. 이것은 [!DNL Target] 활동이 페이지 맨 위에서 호출을 실행하지만 [!DNL Analytics]는 일반적으로 페이지 맨 아래에서 해당 데이터 수집 호출을 실행하기 때문입니다. 지금까지의 A4T 구현에서 Adobe는 [!DNL Target] 활동이 활성 상태일 때마다 이 추가 데이터를 포함했습니다.

자세한 내용은 [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)를 참조하십시오.

+++

## 부분 데이터 히트가 무엇입니까? {#section_59A203E289564576BF6821F96B0B9E11}

+++답변 [!DNL Target] 페이지 맨 위에 있는 태그가 실행되지만 [!DNL Analytics] 페이지 하단의 태그는 실행되지 않습니다. 이러한 상황이 발생하는 이유는 다양합니다. 에서 [!DNL A4T] 지금까지의 구현에서 Adobe은 이러한 히트에 대한 부분 데이터를 [!DNL Target] 활동이 활성화되었습니다. 앞으로는 Adobe이 [!DNL Target] 및 [!DNL Analytics] 태그가 실행되었습니다.

자세한 내용은 [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)를 참조하십시오.

+++

## 방문 횟수에 스파이크가 표시됩니다. 이러한 방문이 부분 데이터 히트로 인해 발생하는지 어떻게 알 수 있습니까? {#section_28506672C6224ED18AC74F6A02F6F811}

+++답변 연락 가능 [고객 지원 Adobe](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) 부분 데이터 보고서를 검색하기 위해. 이 정보는 [!DNL Analytics] UI에서 바로 이용할 수 없습니다.

+++

## 부분 데이터 히트가 발생하는 잠재적 원인은 무엇입니까? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

+++부분 데이터 히트에 대한 답변은 잘못 정렬된 보고서 세트 ID와 같은 부적절한 구현의 결과인 경우가 많습니다. 또한 느린 페이지, 페이지 오류, 활동의 리디렉션 오퍼 또는 오래된 라이브러리 버전을 포함한 타당한 원인도 있습니다.

자세한 내용은 [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)의 &quot;부분 데이터에 기여하는 것은 무엇입니까?&quot;를 참조하십시오.

+++

## 부분 데이터 히트가 있습니다. 내 데이터를 정리하려면 어떤 작업을 수행합니까? {#section_CBE778A9D07A469E8FF98F68BACC7124}

+++답변 보고서에서 이전 부분 데이터를 제외하는 가상 보고서 세트를 만들 수 있습니다.

자세한 내용은 in [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)의 &quot;부분 데이터를 줄이는 우수 사례는 무엇입니까?&quot;를 참조하십시오.

+++

## 페이지에서 부분 데이터 히트가 생성되지 않게 할 방법이 있습니까? {#section_4B00E7E618444BE98A0798DE98F08B21}

+++답변 2016년 11월 14일 이후에는 Adobe이 [!DNL Target] 및 [!DNL Analytics] 태그가 실행되었습니다. 이 변경 내용은 소급 적용되지 않습니다. 내역 보고서에 부풀려진 카운트가 표시되면 가상 보고서 세트를 만들어 보고서에서 제외할 수 있습니다. 부분 데이터를 제외한 기록 추세를 보려면 어떻게 해야 합니까? 를 참조하십시오. in [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

부분 데이터 히트를 최소화하기 위해 수행할 수 있는 절차도 있습니다. 자세한 내용은 in [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)의 &quot;부분 데이터를 줄이는 우수 사례는 무엇입니까?&quot;를 참조하십시오.

+++

## 부분 데이터 히트가 보고에서 제거되면 귀중한 데이터를 유실하게 되지 않습니다 [!DNL Target] 또는 Analytics 데이터? {#section_EBC39E8A0F6A40E58F51E776936F7D9E}

+++부분 데이터를 포함하는 답변 [!DNL Analytics] 보고 기능은 추가 정보를 제공하지만, 기록 데이터가 없는 기간의 데이터와 불일치하게 됩니다 [!DNL Target] 실행 중인 활동. 부분 히트 데이터를 포함하면 다음과 같은 문제가 발생할 수 있습니다 [!DNL Analytics] 시간에 따른 트렌드를 분석하는 사용자.

부분 데이터 히트를 최소화하기 위해 수행할 수 있는 절차가 있습니다. 자세한 내용은 in [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)의 &quot;부분 데이터를 줄이는 우수 사례는 무엇입니까?&quot;를 참조하십시오.

+++

## 특별한 종류가 있나요 [!DNL Target] 부분 데이터 히트를 초래할 수 있는 활동? {#section_69837442A9B84366BEFDA4588B31E574}

+++응답 리디렉션 오퍼에서는 즉시 사용자를 다른 페이지로 보냅니다(즉, [!DNL Analytics] 첫 번째 페이지에서 호출이 실행되지 않습니다.

+++