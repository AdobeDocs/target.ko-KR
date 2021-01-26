---
keywords: partial data;partial-data;A4T;discrepancies;analytics for target;orphaned;virtual report suite;phantom;troubleshooting;unstitched;inflated;unspecified
description: Analytics를 보고 소스로 사용할 때 부풀려진 방문 및 방문자 카운트의 효과를 최소화하는 데 도움이 되는 정보입니다.
title: A4T에서 부풀려진 방문 및 방문자 카운트 최소화
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 97%

---


# A4T에서 부풀려진 방문 및 방문자 카운트 최소화{#minimizing-inflated-visit-and-visitor-counts-in-a-t}

Analytics를 보고 소스로 사용할 때 부풀려진 방문 및 방문자 카운트의 효과를 최소화하는 데 도움이 되는 정보입니다.

>[!IMPORTANT]
>2016년 11월 14일부터 Adobe Analytics에서 타겟 분석(A4T)을 사용하는 고객에 대해 일부 데이터가 처리되는 방식이 변경되었습니다. 이러한 변경 때문에 Adobe Target 데이터가 Adobe Analytics용 데이터 모델에 더 적합해질 수 있습니다 . 이러한 변경은 A4T를 사용하는 모든 고객을 위해 롤아웃되었습니다. 이러한 변경은 특히 Target 활동이 실행 중일 때 일부 고객이 방문자 수가 부풀려졌다는 사실을 알게 되는 문제를 해결합니다.
>
>참고로 이 변경은 소급 적용되지 않습니다. 기록 보고서에 부풀려진 수가 표시되어 보고서에서 제외하고 싶은 경우, 아래 설명된 대로 가상 보고서 세트를 만들 수 있습니다.
>
>또한 부풀려진 수를 최소화하는 데 도움이 되도록 여러 JavaScript 라이브러리가 업데이트되었습니다. 다음 라이브러리 버전 이상으로 업그레이드하는 것이 좋습니다.
>
>* Experience Cloud 방문자 ID 서비스: visitorAPI.js 버전 2.3.0 이상
>* Adobe Analytics: appMeasurement.js 버전 2.1.
>* Adobe Target: at.js 버전 0.9.6 이상(A4T에서 리디렉션 오퍼를 사용하는 경우 버전 1.1.0 제외)

>
>  
mbox.js 라이브러리는 A4T를 사용하는 리디렉션 오퍼를 지원하지 않습니다. 구현에서 at.js를 사용해야 합니다.

## 변경 사항{#section_9CCF45F5D66D48EBA88F3A178B27D986}

[!DNL Adobe Analytics]를 사용하여 [!DNL Target] 활동을 측정할 때(A4T라고 함) [!DNL Analytics]에서는 페이지에 [!DNL Target] 활동이 없을 때 사용할 수 없는 추가 데이터를 수집합니다. 이것은 [!DNL Target] 활동이 페이지 맨 위에서 호출을 실행하지만 [!DNL Analytics]는 일반적으로 페이지 맨 아래에서 해당 데이터 수집 호출을 실행하기 때문입니다. 지금까지의 A4T 구현에서는 [!DNL Target] 활동이 활성 상태가 될 때마다 이 추가 데이터를 포함했습니다. 앞으로는 [!DNL Target]과 [!DNL Analytics] 태그가 모두 실행된 경우에만 이 추가 데이터를 포함하게 됩니다.

## Adobe가 이 변경 작업을 수행하는 이유는 무엇입니까? {#section_92380A4BD69E4B8886692DD27540C92A}

Adobe는 데이터 정확성 및 품질에 자부심을 갖고 있습니다. [!DNL Target] 태그가 실행되지만 [!DNL Analytics] 태그는 실행되지 않은 경우, [!DNL Analytics] 활동이 없으면 [!DNL Target]에서 캡처되지 않을 수 있는 &quot;부분 데이터&quot;(경우에 따라 &quot;연결되지 않은 히트&quot;라고도 함)가 기록됩니다. 이 부분 데이터를 [!DNL Analytics] 보고에 포함하면 추가 정보가 제공되지만, 실행 중인 [!DNL Target] 활동이 없는 기간의 기록 데이터와 불일치하게 됩니다. 이렇게 되면 시간에 따른 트렌드를 분석하는 [!DNL Analytics] 사용자의 경우 문제가 발생할 수 있습니다. [!DNL Analytics]에서 데이터 일관성을 유지하기 위해 모든 부분 데이터를 제외할 것입니다.

## 부분 데이터에 기여하는 것은 무엇입니까? {#section_C9C906BEAA7D44DAB9D3C03932A2FEB8}

[!DNL Analytics]에 있는 높은 비율의 부분 데이터가 있는 고객이 일부 확인되었습니다. 이로 인해 잘못된 구현이 진행될 수 있지만 타당한 원인도 있습니다.

부분 데이터에 대한 확인된 원인은 다음과 같습니다.

* **잘못 정렬된 보고서 세트 ID(구현):** 활동 설정 동안 지정된 보고서 세트가 테스트가 전달된 페이지의 보고서 세트와 일치하지 않습니다. 데이터가 [!DNL Analytics] 서버에서 조정될 수 없으므로 부분 데이터처럼 보입니다.
* **느린 페이지:** [!DNL Target] 호출이 페이지 위쪽에 있고 [!DNL Analytics] 호출은 일반적으로 페이지 아래쪽에 있으므로 페이지가 느리게 로드되면 [!DNL Target] 호출이 발생한 후, [!DNL Analytics] 호출 이전에 방문자가 페이지를 떠날 가능성이 높아집니다. 이러한 현상은 연결이 종종 더 느려지는 모바일 웹 사이트에서 특히 문제가 될 수 있습니다.
* **페이지 오류:** JavaScript 오류 또는 각 터치포인트가 개시되지 않는 다른 시나리오가 있는 경우(Experience Cloud ID 서비스, Target 및 Analytics) 부분 데이터가 발생합니다.
* **[!DNL Target]활동의 리디렉션 오퍼:** A4T를 사용하는 활동의 리디렉션 오퍼에 대해서는 구현이 특정 최소 요구 사항을 충족해야 합니다. 또한 사용자가 알아야 하는 중요한 정보도 있습니다. 자세한 내용은 [리디렉션 오퍼 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58)를 참조하십시오.
* **이전 버전의 라이브러리:** 작년에 Adobe는 데이터가 가능한 한, 효율적으로 전송될 수 있게 하도록 JavaScript 라이브러리([!DNL appMeasurement.js], `at.js/mbox.js` 및 `visitorAPI.js`)를 일부 개선했습니다. 구현 요구 사항에 대해 자세히 알려면 [구현하기 전에](/help/c-integrating-target-with-mac/a4t/before-implement.md#concept_046BC89C03044417A30B63CE34C22543)를 참조하십시오.

## 부분 데이터를 줄이는 우수 사례는 무엇입니까? {#section_065C38501527451C8058278054A1818D}

부분 데이터 컬렉션을 줄이려면 다음 단계를 검토하십시오.

| 단계 | 작업 |
| --- | --- |
| ![1단계](assets/step1_icon.png) | [!DNL Target]에서 선택한 보고서 세트가 활동이 표시될 페이지의 보고서 세트와 같은지 확인하십시오. |
| ![2단계](assets/step2_icon.png) | visitorAPI.js, appMeasurement.js, at.js / mbox.js 라이브러리가 A4T 호환 버전에 있는지 확인합니다. 구현 요구 사항에 대해 자세히 알려면 [구현하기 전에](/help/c-integrating-target-with-mac/a4t/before-implement.md)를 참조하십시오. |
| ![3단계](assets/step3_icon.png) | SDID가 페이지를 나가는 모든 [!DNL Target] 및 [!DNL Analytics] 호출에 대해 설정되고, 일치하는지 확인하십시오.<br/>이를 위해 네트워크 분석기 또는 디버깅 도구를 사용하여 `mboxMCSDID` 호출의 [!DNL Target] 매개 변수가 [!DNL Analytics] 호출의 SDID 매개 변수와 일치하는지 확인하면 됩니다. |
| ![4단계](assets/step4_icon.png) | 구현 라이브러리가 사이트에서 올바른 순서로 로드되는지 확인하십시오. 자세한 내용은 [Analytics for Target 구현](/help/c-integrating-target-with-mac/a4t/a4timplementation.md)의 8단계를 완료해야 합니다. |

## 보유한 부분 데이터양을 알려면 어떻게 해야 합니까? {#section_89B663E2824A4805AB934153508A0F4B}

이 정보를 [!DNL Analytics]에서 직접 사용할 수 없지만 Adobe 고객 지원 센터에 문의하여 부분 데이터 보고서를 검색할 수 있습니다. 이 보고서는 디버깅을 지원하기 위한 것입니다.

## 부분 데이터를 제외한 기록 추세를 보려면 어떻게 해야 합니까? {#section_4C9DED560FAD4428B362DDA2064897C3}

이 처리 변경 내용은 릴리스 날짜(2016년 11월 14일) 이후의 데이터에만 영향을 미치므로, 기록 지표를 일치하게 조정하려면 부분 데이터를 제외하는 세그먼트를 만드는 것이 좋습니다.

이 변경 내용과 관련된 다음 정보에는 세그먼트를 정의하고 가상 보고서 세트에 적용하여 이 세그먼트가 항상 [!DNL Analytics] 보기에 적용되도록 하는 데 도움이 되는 지침이 포함되어 있습니다.

대부분의 경우 [!DNL Target] 히트는 각 웹 페이지의 [!DNL Analytics] 히트와 연결됩니다. 이 연결은 [!DNL Target]과 [!DNL Analytics] 호출 모두에서 일관된 SDID와 [!DNL Analytics] 호출의 [!DNL Experience Cloud ID] (MCID)가 동일한 페이지에 있는 경우에 발생합니다. [!DNL Target]은 일반적으로 MCID도 포함하지만, [!DNL Target] 호출이 방문자 ID가 반환되기 전에 발생할 경우 SDID 때문에 해당 히트가 여전히 연결됩니다. 또한 [!DNL Target] 호출이 실행된 후에 [!DNL Analytics] 호출을 실행할 수 있도록 충분히 오랫동안 사용자가 페이지에 머물러야 합니다. 이것이 이상적인 시나리오입니다.

**부분 데이터 히트:** 경우에 따라 사용자가 [!DNL Analytics] 호출을 전송할 만큼 충분히 오래 페이지에 머무르지 않아도 [!DNL Target]에 적절한 MCID가 유지됩니다. 이 경우 부분 데이터 히트([!DNL Analytics] 페이지 보기가 없는 히트)가 발생합니다. 이러한 사용자가 사이트로 돌아가 [!DNL Analytics] 코드를 포함하는 페이지를 보면 재방문자로 적절히 카운트됩니다. 이것은 페이지에 [!DNL Analytics] 코드만 있었으면 손실되었을 수 있는 히트입니다. 일부 클라이언트는 특정 지표(방문)는 부풀리고 다른 지표(방문당 페이지 보기, 방문당 시간 등)는 줄이기 때문에 이러한 히트에 대한 데이터는 원하지 않습니다. 페이지 보기가 없는 방문도 표시됩니다. 그러나 이러한 데이터를 유지해야 하는 적절한 이유는 여전히 있습니다.

부분 데이터 히트를 최소화하려면 페이지를 보다 빠르게 로드하거나, 라이브러리의 최신 버전으로 업데이트하거나, 해당 히트를 제외하는 [가상 보고서 세트](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html)를 만들 수 있습니다. 단계별 지침은 *분석 구성 요소 안내서*&#x200B;의 [가상 보고서 세트 만들기](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html)를 참조하십시오.

다음 그림은 가상 보고서 세트에 대한 세그먼트 정의를 보여 줍니다.

![](assets/ts_a4t.png)

가상 보고서 세트를 만들 때 세그먼트 정의에 대해 다음 구성을 지정하십시오(위 그림 참조).

* **히트 표시:**
* Analytics for Target: 있음
* And
* 페이지 보기: 없음
* 그리고
* 사용자 지정 링크 인스턴스: 없음
* 그리고
* 다운로드 링크 인스턴스: 없음
* 그리고
* 종료 링크 인스턴스: 없음

**고립된 히트: ** 드문 경우이지만 사용자가 Analytics 호출을 위해 충분히 오래 페이지에 머무르지 않았으며 Target이 적절한 MCID를 얻지 못했습니다. 이러한 상황을 &quot;고립된&quot; 히트로 정의합니다. 이러한 히트는 거의 재방문하지 않는 고객을 나타내며, 방문 및 방문자 수를 부적절하게 부풀립니다.

이러한 &quot;고립된&quot; 히트를 최소화하기 위해 위에서 설명된 것처럼 해당 히트를 제외하는 [가상 보고서 세트](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-workflow/vrs-create.html)를 만들 수 있습니다.

## 이것은 내 [!DNL Target] 보고에 어떤 의미가 있습니까? {#section_AAD354C722BE46D4875507F0FCBA5E36}

이러한 변경이 발생하면 [!DNL Adobe]에서 들어오는 부분 데이터를 처리하지 않으므로 실시간으로 테스트할 새 방문자 및 방문 수가 줄어드는 것을 볼 수 있습니다. 다른 [!DNL Analytics] 지표에 대한 전환 및 히트는 변경되지 않습니다.
