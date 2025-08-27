---
keywords: faq;자주 묻는 질문;analytics for target;a4T;리디렉션;리디렉션 오퍼;adobe-mc-sdid;adobe_mc_ref
description: Analytics for [!DNL Target] (A4T)을(를) 사용할 때 리디렉션 오퍼 사용에 대한 질문에 대한 답변을 찾아보십시오. A4T를 사용하면  [!DNL Target] 활동에 대한 Analytics 보고를 사용할 수 있습니다.
title: A4T를 사용하는 리디렉션 오퍼에 대한 FAQ는 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
exl-id: 4706057f-bd8b-4562-94e0-be22b2e19297
source-git-commit: bb41de751246a77e71e65c11f020bc39f3105da6
workflow-type: tm+mt
source-wordcount: '1431'
ht-degree: 50%

---

# 리디렉션 오퍼 - A4T FAQ

이 주제에서는 [!DNL Adobe Analytics]을(를) [!DNL Adobe Target]의 보고 소스로 사용(A4T)할 때의 리디렉션 오퍼 사용에 대한 FAQ 답변을 제공합니다.

## Analytics for Adobe Target(A4T)에서 리디렉션 오퍼를 지원합니까? {#section_46B8B03ED4D542C6AD875F5F61176298}

+++답변
예. 구현에서 [!DNL at.js]을(를) 사용하는 경우 지원합니다. 그러나 Analytics를 보고 소스로 사용하는 활동에서 [리디렉션 오퍼](/help/main/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94)를 사용하기 위해서는 구현이 아래 나열된 최소 요구 사항을 충족해야 합니다.

+++

## ![Adobe Experience Platform Web SDK 배지](/help/main/assets/platform.png) [!DNL Adobe Experience Platform Web SDK]에서 A4T에 대한 리디렉션 오퍼를 지원합니까? {#platform}

+++답변
다음 FAQ는 [!DNL Platform Web SDK]에서 A4T 및 리디렉션 오퍼를 사용하는 방법에 대한 자세한 정보를 제공합니다.

+++

### Analytics for Target(A4T)에서 리디렉션 오퍼를 지원합니까?

+++답변
예. Platform Web SDK을 통한 A4T는 [리디렉션 오퍼](/help/main/c-experiences/c-manage-content/offer-redirect.md)를 지원합니다.

+++

### [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 및 [!UICONTROL Form-Based Experience Composer]이(가) 지원됩니까?

+++답변
예. 기본 제공 리디렉션 오퍼를 사용하는 경우 [[!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md)(VEC) 및 [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md)이(가) 지원됩니다.

+++

## A4T에 리디렉션 오퍼를 사용하기 위한 최소 요구 사항은 무엇입니까? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

+++답변
구현은 다음 최소 요구 사항을 충족해야 합니다.

* Experience Cloud 방문자 ID 서비스: [!DNL visitorAPI.js] 버전 2.3.0 이상
* Adobe Analytics: [!DNL appMeasurement.js] 버전 2.1.
* Adobe Target: [!DNL at.js] 버전 1.6.2 이상.

리디렉션 오퍼가 있는 페이지와 방문자가 리디렉션되어 도착하는 페이지 모두에 세 개의 라이브러리를 포함해야 합니다.

+++

## A4T와 Analytics 간에 때때로 데이터가 일치하지 않는 이유는 무엇입니까?

+++답변
일부 데이터 불일치가 예상됩니다. 자세한 내용은 [A4T를 사용할 때와 사용하지 않을 때 Target과 Analytics 간에 예상되는 데이터 분산](/help/main/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md)을 참조하십시오.

+++

## A4T 활동에서 리디렉션 오퍼를 사용할 때 트래픽 분배의 불일치를 최소화하려면 어떻게 해야 합니까? {#discrepancies}

+++답변
[!UICONTROL Analytics for Target]&#x200B;(A4T)으로 구성된 활동에서 리디렉션 오퍼를 사용할 때 제한된 수의 고객이 트래픽 분포에서 높은 차이를 보고했습니다.

다음 사항을 고려하십시오.

* [!DNL Target] 및 [!DNL Analytics] 호출의 순서가 잘못되어 분산 정도가 높아질 수 있습니다.

  [!DNL Target] 호출은 원본 페이지(리디렉션이 발생하는 경우) 및 대상 페이지(리디렉션이 끝나는 경우)에서 [!DNL Analytics] 호출보다 먼저 수행되어야 합니다.

* A4T 리디렉션 활동에서 리디렉션 오퍼를 사용하는지 확인합니다.
* 소스 페이지에 [!DNL Target]개의 위치 요청이 여러 개 있는 경우(리디렉션이 발생하는 경우), [!DNL Adobe]에서는 첫 번째 [!DNL Target]개의 위치 요청에서 리디렉션 활동을 실행하는 것이 좋습니다.

  첫 번째 [!DNL Target] 위치 요청에서 리디렉션 활동을 실행하면 다른 [!DNL Target] 위치 요청에서 활동 자격이 발생하고 보고서에서 카운트될 가능성이 줄어듭니다. 리디렉션된 방문자는 경험을 볼 수 없으므로 다른 활동의 보고서에서 계산되지 않아도 됩니다.

+++

## 원래 페이지의 페이지 보기 횟수와 리디렉션 페이지의 페이지 보기 횟수가 카운트되는 이유는 무엇입니까? {#section_B8F6CC2190B84CF08D945E797C5AF07B}

+++답변
at.js 버전 1.6.3 이상을 사용하는 경우 두 페이지에서 페이지 보기 수를 계산하는 것은 문제가 되지 않습니다. 이 경합 조건은 이전 버전을 사용하는 고객에게만 영향을 줍니다. Target 팀에서는 at.js의 현재 버전과 바로 전 버전, 이렇게 두 버전을 유지 관리합니다. [지원되는 버전](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}을 실행 중인지 확인하려면 at.js를 필요에 따라 업그레이드하십시오.

at.js의 지원되지 않는 이전 버전을 사용하는 경우, 리디렉션이 첫 페이지에서 실행되기 전에 Analytics 호출이 실행될 수 있는 경합 조건이 발생할 수 있습니다. 이 경우 원래 페이지 및 리디렉션 페이지의 페이지 보기가 모두 카운트될 수 있습니다. 실제로는 방문자에게 첫 번째 페이지가 &quot;표시&quot;되지 않았는데 첫 번째 페이지에 추가 페이지 보기가 발생할 수 있습니다.

페이지에서 코드가 실행되는 위치로 인해 페이지 리디렉션의 속도를 높이려면 양식 기반 작성기를 사용하여 리디렉션 활동을 빌드하는 것이 좋습니다. 또한, 리디렉션이 원래 페이지로 돌아가는 리디렉션 오퍼를 기본 경험을 포함한 모든 경험에 대해 만드는 것이 좋습니다. 각 경험에 대한 리디렉션 오퍼를 만들면 잘못된 카운트가 발생할 경우 모든 경험에서 리디렉션이 발생합니다. 보고 및 분석은 여전히 테스트에 유효합니다.

기본(제어) 경험을 포함하여 활동의 모든 경험에 대해 리디렉션 오퍼를 사용하려는 한 가지 이유는 모든 경험에 동일한 조건을 적용하기 위해서입니다. 예를 들어 기본 경험에 리디렉션 오퍼가 없지만 다른 경험에 리디렉션 오퍼가 있는 경우 리디렉션 오퍼가 없는 경험의 속도가 고유한 이점이 있습니다. 리디렉션 오퍼는 테스트와 같은 임시 시나리오에만 권장됩니다. 리디렉션 오퍼는 개인화와 같은 영구 시나리오에 권장되지 않습니다. 우승자를 결정한 후 리디렉션을 제거하여 페이지 로드 성능을 개선해야 합니다.

+++

## 시각적 경험 작성기(VEC)와 양식 기반 경험 작성기가 모두 지원됩니까? {#section_FDA26FE7909B48539DA770559E687677}

+++답변
예, 기본 제공 리디렉션 오퍼를 사용하는 한 두 작성기가 모두 지원됩니다.

리디렉션을 위한 자신만의 사용자 지정 코드를 사용하는 경우 리디렉션 URL(`adobe_mc_sdid`와 `adobe_mc_ref`)과 연결된 두 개의 새 매개 변수를 반드시 채워야 합니다.

+++

## 리디렉션 URL에 추가된 새 쿼리 문자열 매개 변수는 무엇입니까? {#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682}

+++답변
다음 쿼리 문자열 매개 변수는 리디렉션 오퍼와 연결되어 있습니다.

| 매개 변수 | 설명 |
|--- |--- |
| `adobe_mc_sdid` | `adobe_mc_sdid` 매개 변수는 SDID(Supplemental Data Id)와 Experience Cloud 조직 ID를 기본 페이지에서 새 페이지로 전달합니다. 이러한 ID를 사용하면 A4T가 기본 페이지의 Target 요청을 새 페이지의 Analytic 요청과 함께 &quot;결합&quot;(stitch)할 수 있습니다.<br>URL에서 sdid를 전달할 수 있는 예상 형식은 `ex. adobe_mc_sdid=SDID=123|MCORGID=123456789@AdobeOrg|TS=1498569322`입니다(하이브리드 앱의 경우 또는 한 앱에서 웹 사이트 또는 한 웹 사이트에서 다른 웹 사이트로) |
| `adobe_mc_ref` | `adobe_mc_ref` 매개 변수는 기본 페이지의 참조 URL을 새 페이지에 전달합니다. AppMeasurement.js 버전 2.1 이상에서 사용하는 경우 Analytics는 이 매개 변수 값을 새 페이지의 참조 URL로 사용합니다. |

이 매개 변수들은 페이지에 방문자 ID 서비스가 구현되어 있으면 VEC 및 양식 기반 경험 작성기에서 내장 리디렉션 오퍼를 사용할 때 리디렉션 URL에 자동으로 추가됩니다. VEC 또는 양식 기반 편집기에서 자신만의 사용자 지정 리디렉션 코드를 사용하는 경우 사용자 지정 코드와 함께 이 매개 변수를 전달해야 합니다.

+++

## 내 웹 서버가 내 URL에서 이러한 매개 변수를 제거하고 있습니다.어떻게 해야 합니까? {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

+++답변
IT 팀과 함께 이러한 매개 변수(`adobe_mc_sdid` 및 `adobe_mc_ref`)를 허용 목록에추가된으로 사용합니다.

+++

## 리디렉션 활동에 A4T를 사용하고 있지 않고 이러한 추가 매개 변수를 내 URL에 추가하지 않으려면 어떻게 합니까? {#section_9E608D75FF9349FE96C65FEDD7539F45}

+++답변
다음과 같은 경우 사용자 지정 코드 리디렉션을 사용합니다.

* 리디렉션 활동에 A4T를 사용하고 있지 않습니다.
* 방문자 ID 서비스를 구현했습니다
* 이러한 매개 변수를 자동으로 URL에 추가하지 않으려는 경우

그러나 레퍼러 정보를 `adobe_mc_ref`에 올바로 보고하기 위해서는 [!DNL Analytics] 매개 변수를 URL에 보관하는 것이 가장 좋습니다.

+++

## 내 구현에서 adobe_mc_ref와 adobe_mc_sdid 매개 변수가 이중 URL로 인코딩되는 이유는 무엇입니까? {#section_5EFE5F012B944C40865731EA18E7E79E}

+++답변
A4T와 리디렉션 오퍼를 사용하는 경우, Target에서는 `adobe_mc_ref`와 `adobe_mc_sdid` 매개 변수를 URL에 추가합니다. 이 값들은 이미 URL로 인코딩되어 있고, 대부분의 경우 모두 예상대로 작동합니다. 하지만, 일부 고객의 로드 밸런서나 웹 서버에서는 쿼리 문자열 매개 변수를 한 번 더 인코딩하려고 시도할 수 있습니다.

방문자 API에서 `adobe_mc_sdid` 값을 디코딩하려 할 때 이러한 이중 인코딩이 발생하면 SDID 값이 추출되지 않고 새 SDID가 생성됩니다. 이 프로세스로 인해 잘못된 SDID 값이 Target 및 Analytics로 전송되고 Analytics 보고서에 리디렉션에 대한 분할이 균일하지 않습니다.

Adobe에서는 IT 팀에 얘기해서 `adobe_mc_ref` 및 `adobe_mc_sdid`이(가) 허용 목록에추가된으로 변환되지 않도록 하는 것이 좋습니다.

+++

## 참조 URL을 새 페이지에 전달해야 하는 이유는 무엇입니까? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

+++답변
방문자가 [!DNL `www.google.com`]에서 리디렉션 활동이 라이브 상태인 홈 페이지(`www.mysite.com/index.html`)로 연결되는 링크를 클릭한 다음 새 페이지(`www.mysite.com/index2.html`)로 리디렉션된다고 가정해 보십시오.

이전에는 새 페이지에 대한 [!DNL Analytics] 요청에서 [!DNL `www.mysite.com/index.html`] 대신 [!DNL `www.google.com`]의 참조 URL을 보고했습니다. 이로 인해 참조 URL과 관련하여 [!DNL Analytics]에 정확하지 않은 보고가 발생했습니다(예를 들어 마케팅 채널 보고서에서). [!DNL `www.google.com`]에서 이 사이트에 왔다는 사실이 보고서에 없습니다.

[!DNL at.js] 버전 0.9.6 이상 및 [!DNL AppMeasurement.js] 2.1 이상을 사용하면 새 페이지에 대한 [!DNL Analytics] 요청에서 [!DNL `www.google.com`]의 참조 URL을 보고합니다.

+++

## 내가 사용자 지정/HTML 리디렉션 오퍼를 사용할 수 있습니까? {#section_E49F9A83A286488C8F1098A040203D7E}

+++답변
아니요, [!DNL Analytics]를 보고 소스로 사용(A4T)하는 활동에는 기본 제공 리디렉션 오퍼를 사용해야 합니다. [!DNL Target]의 관점에서 HTML 오퍼는 불투명합니다. [!DNL Target]은 HTML의 특정 부분이 리디렉션을 인스턴스화하는 JavaScript를 포함한다는 것을 알 수 없습니다.

+++

### [!DNL Platform Web SDK]에서 사용자 지정/HTML 리디렉션 오퍼를 사용할 수 있습니까?

+++답변
아니요, A4T를 사용하는 활동에는 내장 리디렉션 오퍼를 사용해야 합니다. [!DNL Target] 관점에서 HTML 오퍼는 불투명합니다. [!DNL Target]은(는) HTML의 특정 부분에 리디렉션을 인스턴스화하는 JavaScript이 포함되어 있음을 알 수 없습니다.

+++
