---
keywords: faq;자주 묻는 질문;analytics for target;a4T;부풀려짐;방문;방문자;부분 히트;고립됨;고아;partial-hit
description: Analytics for Target(A4T)를 사용할 때 부풀려진 방문 및 방문자 수에 대한 질문에 대한 답변을 찾습니다. "부분 데이터"를 최소화하는 방법을 알아봅니다.
title: A4T를 사용하여 부풀려진 방문 및 방문자 수에 대한 Faq는 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: e45f0d2d2370f9c7aba2c2bd26afdd4c0e401db8
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 63%

---


# 부풀려진 방문 및 방문자 카운트 - A4T FAQ{#inflated-visit-and-visitor-counts-a-t-faq}

이 주제에서는 Analytics를 Target(A4T)의 보고 소스로 사용할 때 부풀려진 방문 및 방문자 카운트와 관련하여 자주 묻는 질문에 대한 답변을 제공합니다.

## Analytics 데이터에 페이지 보기 횟수나 기타 변수 값이 없는 방문이 표시되는 이유는 무엇입니까? {#section_4D8C2C2D766842E6B12F3ECC774A64D5}

[!DNL Adobe Analytics]을(를) 사용하여 [!DNL Target] 활동(A4T라고 함)을 측정하는 경우 [!DNL Analytics]는 페이지에 [!DNL Target] 활동이 없을 때 사용할 수 없는 데이터를 수집합니다. 이것은 [!DNL Target] 활동이 페이지 맨 위에서 호출을 실행하지만 [!DNL Analytics]는 일반적으로 페이지 맨 아래에서 해당 데이터 수집 호출을 실행하기 때문입니다. A4T 구현에서 현재까지 Adobe은 [!DNL Target] 활동이 활성 상태일 때마다 이 추가 데이터를 포함합니다.

자세한 내용은 [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)를 참조하십시오.

## 부분 데이터 히트가 무엇입니까? {#section_59A203E289564576BF6821F96B0B9E11}

페이지 맨 위에 있는 [!DNL Target] 태그가 실행되었지만 페이지 맨 아래에 있는 [!DNL Analytics] 태그가 실행되지 않는 경우 부분 데이터 히트가 발생합니다. 이러한 상황이 일어나는 데에는 여러 가지 이유가 있다. [!DNL A4T] 구현에서 현재까지 Adobe은 [!DNL Target] 활동이 활성 상태일 때마다 이러한 히트에 대한 부분 데이터를 포함합니다. 앞으로 Adobe은 [!DNL Target] 및 [!DNL Analytics] 태그가 모두 실행되었을 때만 이 추가 데이터를 포함합니다.

자세한 내용은 [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)를 참조하십시오.

## 방문 횟수에 스파이크가 표시됩니다. 이러한 방문이 부분 데이터 히트로 인해 발생하는지 어떻게 알 수 있습니까?{#section_28506672C6224ED18AC74F6A02F6F811}

[Adobe 고객 지원](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 연락하여 부분 데이터 보고서를 검색할 수 있습니다. 이 정보는 [!DNL Analytics] UI에서 바로 이용할 수 없습니다.

## 부분 데이터 히트가 발생하는 잠재적 원인은 무엇입니까? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

부분 데이터 히트는 잘못 정렬된 보고서 세트 ID와 같은 부적절한 구현으로 인해 종종 발생합니다. 또한 느린 페이지, 페이지 오류, 활동의 리디렉션 오퍼 또는 오래된 라이브러리 버전을 포함한 타당한 원인도 있습니다.

자세한 내용은 [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)의 &quot;부분 데이터에 기여하는 것은 무엇입니까?&quot;를 참조하십시오.

## 부분 데이터 히트가 있습니다. 내 데이터를 정리하려면 어떤 작업을 수행합니까? {#section_CBE778A9D07A469E8FF98F68BACC7124}

보고서에서 이전 부분 데이터를 제외하도록 가상 보고서 세트를 작성할 수 있습니다.

자세한 내용은 in [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)의 &quot;부분 데이터를 제외한 기록 추세를 보려면 어떻게 해야 합니까?&quot;를 참조하십시오.

## 페이지에서 부분 데이터 히트가 생성되지 않게 할 방법이 있습니까? {#section_4B00E7E618444BE98A0798DE98F08B21}

2016년 11월 14일 이후, Adobe은 [!DNL Target] 및 [!DNL Analytics] 태그가 모두 실행된 경우에만 데이터를 포함합니다. 이 변경은 소급 적용되지 않습니다. 내역 보고서에 부풀려진 카운트가 표시되는 경우 가상 보고서 세트를 만들어 보고서에서 제외시킬 수 있습니다. 자세한 내용은 &quot;일부 데이터 없이 내역 트렌드를 보려면 어떻게 해야 합니까?&quot;를 참조하십시오. in [A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)에서 부풀려진 방문 및 방문자 카운트 최소화

부분 데이터 히트를 최소화하기 위해 수행할 수 있는 절차도 있습니다. 자세한 내용은 in [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)의 &quot;부분 데이터를 줄이는 우수 사례는 무엇입니까?&quot;를 참조하십시오.

## 부분 데이터 히트 데이터가 보고에서 제거되면 중요한 Target 또는 분석 데이터가 손실되지 않습니까?{#section_EBC39E8A0F6A40E58F51E776936F7D9E}

[!DNL Analytics] 보고에서 부분 데이터를 포함하면 추가 정보가 제공되지만 실행 중인 [!DNL Target] 활동이 없는 기간의 내역 데이터와 불일치가 생성됩니다. 부분 히트 데이터를 포함하면 시간에 따른 트렌드를 분석하는 [!DNL Analytics] 사용자에게 문제가 발생할 수 있습니다.

부분 데이터 히트를 최소화하기 위해 수행할 수 있는 절차가 있습니다. 자세한 내용은 in [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)의 &quot;부분 데이터를 줄이는 우수 사례는 무엇입니까?&quot;를 참조하십시오.

## 부분 데이터 히트를 초래할 수 있는 특정 유형의 Target 활동이 있습니까? {#section_69837442A9B84366BEFDA4588B31E574}

리디렉션 오퍼에서는 즉시 사용자를 다른 페이지에 보냅니다. 이것은 [!DNL Analytics] 호출이 첫 번째 페이지에서 실행되지 않음을 의미합니다.
