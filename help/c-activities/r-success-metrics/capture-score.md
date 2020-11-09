---
keywords: capture score;score
description: 캡처 점수 참여 지표는 방문자가 캠페인의 첫 번째 표시 Target 요청을 처음 본 시점부터 사이트에서 방문한 페이지에 할당된 값을 기준으로 집계된 점수를 계산합니다.
title: 캡처 점수
feature: success metrics
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 51%

---


# 캡처 점수{#capture-score}

The Capture Score engagement metric calculates an aggregated score based on the value assigned to pages visited on the site, from the point the visitor first sees the campaign&#39;s first display [!DNL Target] request.

다음 예에서는 고양이 이미지가 있는 경험과 개 이미지가 있는 경험 등 두 가지 경험을 테스트하는 캠페인에서 점수 참여가 계산되는 방식을 보여 줍니다.

![](assets/example_score.png)

이 예제에서는 첫 번째 방문자가 고양이를 경험합니다. Assume that a global [!DNL Target] request passes in a page score based on the value of the page. If the marketer has captured page count engagement on a success metric associated with `**any Target request**`, the visit score accumulates for any request seen after the display request around the cat image.

첫 번째 페이지는 점수에 1을 추가하고 두 번째 페이지는 0.25를 더하고, 세 번째 페이지는 0.10을 더하고 네 번째 페이지는 0.10을 더해 합계 1.45가 됩니다. 이 값은 통화 또는 포인트로 해석할 수 있습니다. 다른 방문에서는 방문자가 개 경험을 하며, 더 적은 페이지를 보지만 방문자가 더 귀중한 페이지를 봤기 때문에 다른 방문보다 높은 점수인 2.10을 받습니다.

다음 페이지 흐름에 설명된 대로 adbox와 리디렉터를 전달하여 획득 비용 및 제휴 링크 매출을 고려할 수 있습니다. Notice that, in this example, both [!DNL Target] requests on the article page pass a score, possibly representing a known CPM.

![](assets/example_score2.png)

**페이지 점수 할당**

페이지의 가치에 따라 사이트의 임의 페이지에 값을 할당할 수 있습니다. 예를 들어 요리 사이트는 경험 섹션보다 특집 기사 페이지의 광고를 더 비싼 값으로 판매할 수 있습니다. 따라서 특집 기사가 경험 섹션보다 더 귀중합니다. 페이지 점수를 통해 방문의 전체 &quot;값&quot;을 전개할 수 있으므로 많은 특집 기사를 읽는 사람이 경험만 찾아보는 사람보다 더 많은 &quot;포인트&quot;를 받습니다.

다음 두 가지 방법으로 페이지에 점수를 할당할 수 있습니다.

* 요청에서 [!DNL Target] 이 매개 변수를 만듭니다 `mboxPageValue`.

   예: `('global_mbox', 'mboxPageValue=10');`

   The specified value is added to the score every time the page with that [!DNL Target] request is viewed. 페이지의 여러 요청에 점수 값이 포함되는 경우 페이지의 점수는 모든 요청 값의 총계입니다. `mboxPageValue` 는 참여 점수를 캡처하기 위해 Target 요청에서 값을 전달하는 데 사용되는 예약된 매개 변수입니다. 양수 값과 음수 값을 전달할 수 있습니다. 각 방문자의 방문이 끝날 때 합계를 계산하여 해당 방문에 대한 총 점수를 계산하게 됩니다.

* 페이지의 URL에 `?mboxPageValue=n` 매개 변수를 전달합니다.

   예: `https://www.mydomain.com?mboxPageValue=5`

   Using this method, the specified value is added to the score for each [!DNL Target] request on the page. For example, if you pass the parameter `?mboxPageValue=10`and there are three [!DNL Target] requests on the page, the score for the page is 30.

>[!NOTE]
>
>활동의 첫 번째 표시 [!DNL Target] 요청 위에 있는 Target 요청은 점수에 포함되지 않습니다.

Best practice is to assign values in the [!DNL Target] request. 이렇게 하면 각 요청의 내용에 따라 측정하는 값을 정확하게 파악할 수 있습니다.

>[!NOTE]
>
>간편하게 유지 관리할 수 있도록 일부 조건부 JavaScript 논리를 사용하여 [!DNL at.js] 또는 [!DNL mbox.js] 파일에 지정된 사이트의 페이지 점수값을 구성할 수 있습니다. 이렇게 하면 페이지에 코드를 더 추가할 필요가 없습니다. 도움이 필요한 경우 계정 컨설턴트에게 문의하십시오.

두 가지 방법을 결합할 수 있지만 이 경우 예상보다 높은 점수가 발생할 수 있습니다. For example, if you assign a value of 10 to each of three [!DNL Target] requests and no score to a fourth request, then pass the URL parameter `?mboxPageValue=5`, your page score will be 50, 30 for the three requests with assigned values, and then 5 for each of the four requests on the page.

카운터는 시작 요청이 아닌 첫 번째 표시 요청으로 시작됩니다. 예를 들어 디스플레이 요청이 없는 홈 페이지의 활동을 입력한 다음 디스플레이 요청이 들어 있는 카탈로그 페이지에 연결하는 경우 카탈로그 페이지로 이동할 때 카운터가 시작됩니다.

비용이 들거나 방문자가 보지 않는 것이 좋은 특정 페이지에 대해 음수 값을 전달할 수도 있습니다. 음수 값은 전체 점수에도 영향을 줍니다. 방문자가 광고에서 도달하는 페이지에 이 기술을 사용하여 CPC 수를 확인할 수 있습니다. 또는 방문자가 전화를 걸거나 지원을 요청할 수 있는 지원 또는 연락처 페이지에 사용할 수 있습니다.
