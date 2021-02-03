---
keywords: Analytics 추적 서버;A4T;분석 세그먼트;보고서 세트;잘못된 데이터;고립됨;sdid;VisitorAPI.js;mboxMCSDID;phantom;지정되지 않음
description: 이 주제에서는 Analytics를 Target(A4T)의 보고 소스로 사용할 때 발생하는 몇 가지 일반적인 문제에 대해 설명합니다.
title: 분석 및 Target 통합 문제 해결(A4T)
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 63%

---


# Analytics 및 Target 통합 문제 해결(A4T)

이 주제에서는 Analytics를 Target(A4T)의 보고 소스로 사용할 때 발생하는 몇 가지 일반적인 문제에 대해 설명합니다.

## 활동이 Analytics에서 데이터를 표시하지 않고, 대신 &quot;지정되지 않음&quot;으로 나열됩니다.{#unspecified}

이러한 상황이 발생할 수 있는 이유에는 다음과 같이 몇 가지가 있습니다.

* [!DNL Target]의 분류가 완전히 처리되지 않았습니다.

   일반적으로 분류는 처음 저장한 후 보고서를 분류하는 데 24~72시간 정도가 소요됩니다.

* 보고서 세트에 데이터가 들어 있지 않은데 [!DNL Target]이 히트를 분류하려고 했습니다. 첫 번째 히트가 발생하기 전까지 [!DNL Target]은 데이터를 분류할 수 없습니다.

   보고서 세트에 하나 이상의 히트가 있는지 확인하십시오.

* [!DNL Target]에서 [!DNL Analytics]로의 분류 호출이 실패했습니다.

   도움이 필요하면 [고객 지원팀에 문의하십시오.](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)

&quot;Target에 대한 분석&quot; 차원으로 &quot;지정되지 않음&quot; 행을 분류하고 활동 ID로 구성되어 있지 않은 경우, 모든 것이 올바르게 분류됨을 의미합니다.  활동 ID가 여기에 나열되면 분류 문제를 나타내는 역할을 합니다.

>[!NOTE]
>
>때로 데이터가 보고서에 올바로 표시되지만, 분류를 완료하지 않은 새 활동이 추가되었기 때문에 &quot;지정되지 않음&quot;으로 다시 되돌려집니다. 일반적으로 처음 저장한 후 보고서를 분류하는 데 24~72시간 정도가 소요됩니다.
>
>&quot;지정되지 않음&quot;으로 나열된 경우 데이터는 손실되지 않으며, 분류가 실행된 후 적절한 활동이나 경험에 적절하게 지정됩니다.

## A4T 활동 보고서에는 &quot;지정되지 않음&quot; 이벤트가 많은 행이 포함됩니다.{#added_unspecified_events}

데이터를 표시하는 데 사용하는 지표에 따라 보고서에 &quot;[!UICONTROL 지정되지 않음]&quot; 이벤트 행이 표시될 수 있습니다.

일반적으로 이 행은 보고서에서 [!DNL Target] 특정 지표가 아닌 공통 지표를 선택하는 경우 표시됩니다(예: [!UICONTROL 페이지 보기 횟수], [!UICONTROL 방문 횟수], [!UICONTROL 고유 방문자 수] 등). 이 경우 [!UICONTROL &quot;지정되지 않음&quot;] 행에는 [!DNL Target] 활동과 연결되지 않은 [!UICONTROL 페이지 보기 횟수], [!UICONTROL 방문 횟수] 및 [!UICONTROL 고유 방문자]이 모두 포함됩니다.

해당 행에는 [!DNL Target] 관련 정보가 없습니다(예: 방문자, 방문 또는 노출 횟수 없음). 자세한 내용은 *Analytics 기술 노트*&#x200B;의 보고](https://experienceleague.adobe.com/docs/analytics/technotes/unspecified.html?lang=en)에서 [&quot;지정되지 않음,&quot; &quot;없음&quot;, &quot;없음&quot;, &quot;기타&quot; 및 &quot;알 수 없음&quot;을 참조하십시오.

보고서에서 [!DNL Target] 특정 지표를 선택하는 경우 [!UICONTROL &quot;지정되지 않음&quot;] 행은 표시되지 않습니다. 이 보고서를 모두 사용하지 않는 유일한 방법은 해당 페이지에서 보낸 모든 요청에 대해 [!DNL Target] 호출을 설정하는 것입니다. 이 호출은 일반적이거나 필요하지 않습니다.

## A4T를 시작한 이후 내 Analytics 데이터에 부풀려진 방문 또는 방문자 카운트가 표시됩니다. {#section_4BE374E573D44FB7918611699B74F58E}

자세한 내용은 [A4T에서 부풀려진 방문 및 방문자 카운트 최소화](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)를 참조하십시오.

## 매출액 지표의 예상 상승도에 올바른 데이터가 표시되지 않습니다. {#section_35D766E5E4D347C39E15D08AA883FBB0}

상승도 및 신뢰도 세부 정보는 Analytics에서 사용할 수 없습니다. 하지만 Target 보고서에서는 사용할 수 있습니다.

## Analytics 보고서에 활동이 표시되지 않습니다. {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

A4T 활동을 사용하려면 Analytics 추적 서버를 지정해야 합니다. Analytics 추적 서버를 올바로 설정하려면 [Analytics 추적 서버 사용](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.

>[!NOTE]
>
>Adobe Analytics를 활동의 보고 소스로 사용하는 경우, mbox.js 버전 61 이상 또는 at.js 버전 0.9.1 이상을 사용하는 경우 활동 생성 중에 추적 서버를 지정할 필요가 없습니다. mbox.js 또는 at.js 라이브러리는 자동으로 추적 서버 값을 [!DNL Target]에 보냅니다. 활동을 작성하는 동안에는 [!UICONTROL 목표 및 설정] 페이지의 [!UICONTROL 추적 서버] 필드를 비워둘 수 있습니다.

## 내 Analytics 세그먼트가 Target에 표시되지 않습니다.  {#section_DEE87F1557834F448E99381D3D02EEEF}

A4T 활동을 만들기 전에 올바른 권한이 있는지 확인하십시오.

* Analytics를 Target의 보고 소스로 사용하려면 Adobe Analytics에서 웹 서비스 액세스 그룹에 속해 있어야 합니다.
* 하나 이상의 Experience Cloud 그룹의 구성원으로서 Analytics 및 Target에 액세스할 수 있어야 합니다.
* 왼쪽 탐색 메뉴의 [마케팅 앱] 섹션에 Analytics 및 Target이 표시되는지 확인하십시오.

## 보고서에서 바운스 비율, 바운스 및 퇴장 지표가 양수로 표시됩니다.  {#section_B5C3D56EF0344407AE67ABEB93037F5A}

이는 알려진 문제입니다.

이러한 지표는 음수이지만, 상승도는 Target 보고서에서 양수인 것처럼 표시됩니다. 예를 들어, 낮은 바운스 비율이 필요하더라도 상승도가 가장 높은 우승자로 높은 바운스 비율이 표시됩니다. 이러한 지표 및 유사 지표에 유의하여 보고서를 기준으로 수치를 높일지 또는 줄일지 결정을 내려야 합니다.

## 필요한 보고서 세트가 표시되지 않습니다.{#section_BD8F956E41D6475B98B7BF0C74CC387C}

[!DNL Target Standard/Premium]에 나타나는 보고서 세트 목록은 [!DNL Analytics]에 대해 [!DNL Target](A4T)의 보고 소스로 구성된 보고서 세트 목록입니다. 따라서 사용하고 있는 일부 보고서 세트가 표시되지 않을 수 있습니다.

또한 여러 보고 소스를 사용하는 경우 보고서 세트가 [!DNL Target]의 기본 보고 소스 설정에도 있어야 합니다.그렇지 않으면 보고서 세트가 표시되지 않습니다.

여전히 찾고 있는 보고서 세트가 표시되지 않으면 [클라이언트 지원](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하여 활성화하십시오.

## 보고서에 예상한 만큼의 데이터가 표시되지 않습니다. {#section_75002584FA63456D8D9086172925DD8D}

특히 방문자가 경험을 사용할 자격이 있는 페이지에서 구현을 검토하고, 보조 데이터 ID가 [!DNL Target] 및 [!DNL Analytics] 호출에서 일치하는지 확인하십시오.

* **at.js 1.x**:호출에서  [!DNL Target] 보충 ID는 매개 변수에  `mboxMCSDID` 포함됩니다. [!DNL Analytics] 호출에서는 보조 ID가 `sdid` 매개 변수에 포함되어 있습니다.
* **at.js 2.x**:호출에서  [!DNL Target] 보충 ID는 HTTP 헤더에서 의 값으로 반환됩니다 `experienceCloud.analytics.supplementalDataId`. [!DNL Analytics] 호출에서는 보조 ID가 `sdid` 매개 변수에 포함되어 있습니다.

보충 ID를 검사하는 가장 쉬운 방법은 Adobe Experience Platform Debugger를 사용하는 것입니다.

디버거를 설치하지 않은 경우 [Adobe Experience Platform 디버거 소개](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html)를 참조하십시오.

![디버거](/help/c-integrating-target-with-mac/a4t/assets/debugger.png)

[!DNL Target] 호출에 보조 데이터 ID가 없다면 [!DNL at.js]나 [!DNL mbox.js] 전에 [!DNL VisitorAPI.js] 파일을 로드했는지 확인하십시오. [!DNL Analytics] 호출에 보조 데이터 ID가 없다면 [!DNL Target] 호출 전에 [!DNL Analytics] 호출이 발생하는지 확인하십시오.

자세한 내용은 [Analytics for Target 구현](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A)이나 [고객 지원](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오.
