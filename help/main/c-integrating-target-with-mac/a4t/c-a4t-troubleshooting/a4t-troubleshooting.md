---
keywords: Analytics 추적 서버;A4T;Analytics 세그먼트;보고서 세트;잘못된 데이터;고립됨;SDID;VisitorAPI.js;mboxMCSDID;가상;지정되지 않음
description: 고객이 Analytics for [!DNL Target] (A4T)을 사용할 때 경험하는 일반적인 문제를 살펴봅니다.
title: Analytics 및 [!DNL Target] 통합 문제를 해결하는 방법(A4T)
feature: Analytics for Target (A4T)
exl-id: 7d155cbe-e799-43b5-afc2-1aea43f432ba
source-git-commit: 0be54d82e25eb919102f6098c1b1db76ab291675
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 88%

---

# Analytics 및 [!DNL Target] 통합 문제 해결(A4T)

이 주제에서는 몇 가지 [!DNL Adobe Target]용 보고 소스로서의 [!DNL Adobe Analytics] (A4T)를 사용할 때 발생하는 일반적인 문제를 다룹니다.

## 활동이 Analytics에서 데이터를 표시하지 않고, 대신 “지정되지 않음”으로 나열됩니다. {#unspecified}

데이터가 “지정되지 않음”으로 표시되는 이유는 다음과 같습니다.

* [!DNL Target]의 분류가 완전히 처리되지 않았습니다.

  일반적으로 첫 번째 저장 후 보고서를 분류하는 데 24~72시간이 소요됩니다.

* 보고서 세트에 데이터가 들어 있지 않은데 [!DNL Target]이 히트를 분류하려고 했습니다. 첫 번째 히트가 발생하기 전까지 [!DNL Target]은 데이터를 분류할 수 없습니다.

  보고서 세트에 하나 이상의 히트가 있는지 확인하십시오.

* [!DNL Target]에서 [!DNL Analytics]로의 분류 호출이 실패했습니다.

  도움이 필요한 경우 [고객 지원 센터](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오.

“지정되지 않음” 행을 “Analytics for Target” 차원으로 분류하고 이 행에 활동 ID가 없다면 이는 모든 항목이 올바르게 분류되었음을 의미합니다. 활동 ID가 나열되어 있다면 이는 분류 문제가 있음을 나타냅니다.

>[!NOTE]
>
>경우에 따라 분류가 완료되지 않은 새 활동이 추가되어 데이터가 보고서에 올바르게 표시되지만 “지정되지 않음”으로 되돌아갈 수 있습니다. 일반적으로 첫 번째 저장 후 보고서를 분류하는 데 24~72시간이 소요된다는 점을 기억하십시오.
>
>“지정되지 않음”으로 나열된 경우 데이터는 손실되지 않으며, 분류가 실행된 후 적절한 활동이나 경험에 적절하게 할당됩니다.

## A4T 활동 보고서에는 “지정되지 않음” 이벤트가 많은 행이 포함됩니다. {#added_unspecified_events}

데이터와 함께 표시하기 위해 사용하는 지표에 따라 보고서에 &quot;[!UICONTROL Unspecified]&quot; 이벤트 행이 표시될 수 있습니다.

일반적으로 이 행은 보고서에서 [!DNL Target]과(와) 관련되지 않은 일반적인 지표(예: [!UICONTROL Page Views], [!UICONTROL Visits], [!UICONTROL Unique Visitors] 등)를 선택하는 경우 표시됩니다. 이 경우 [!UICONTROL "Unspecified"] 행에는 [!DNL Target] 활동과 연결되지 않은 모든 [!UICONTROL Page Views], [!UICONTROL Visits] 및 [!UICONTROL Unique Visitors]이(가) 포함됩니다.

이 행에는 [!DNL Target] 관련 정보가 포함되지 않습니다(예: 방문자 수, 방문 횟수 또는 노출 횟수 없음). 자세한 내용은 *Analytics 기술 노트*&#x200B;에서 [보고의 “지정되지 않음”, “없음”, “기타” 및 “알 수 없음”](https://experienceleague.adobe.com/docs/analytics/technotes/unspecified.html?lang=ko)을 참조하십시오.

보고서에서 [!DNL Target]별 지표를 선택하는 경우 해당 [!UICONTROL "Unspecified"] 행이 표시되지 않습니다. 이를 보고서에 포함시키지 않는 유일한 방법은 해당 페이지에서 전송된 모든 요청에 대해 일반 또는 필수 호출이 아닌 [!DNL Target] 호출을 설정하는 것입니다.

## 매출액 지표의 예상 상승도에 올바른 데이터가 표시되지 않습니다. {#section_35D766E5E4D347C39E15D08AA883FBB0}

상승도 및 신뢰도 세부 정보는 Analytics에서 사용할 수 없습니다. 하지만 Target 보고서에서는 사용할 수 있습니다.

## Analytics 보고서에 활동이 표시되지 않습니다. {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

A4T 활동을 사용하려면 Analytics 추적 서버를 지정해야 합니다. Analytics 추적 서버가 올바르게 설정되었는지 확인하려면 [Analytics 추적 서버 사용](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)을 참조하십시오.

>[!NOTE]
>
>at.js 버전 0.9.1 이상을 사용 중이면 활동 생성 도중 추적 서버를 지정하지 않아도 됩니다. at.js 라이브러리는 [!DNL Target]에 추적 서버 값을 자동으로 전송합니다. 활동을 만드는 동안 [!UICONTROL Goals & Settings] 페이지의 [!UICONTROL Tracking Server] 필드를 비워 둘 수 있습니다.

## 내 Analytics 세그먼트가 Target에 표시되지 않습니다. {#section_DEE87F1557834F448E99381D3D02EEEF}

A4T 활동을 생성하기 전에 올바른 권한이 있는지 확인하십시오.

* Target용 보고 소스로서의 Analytics를 사용하려면 Adobe Analytics의 웹 서비스 액세스 그룹에 속해야 합니다.
* Analytics 및 Target에 대한 액세스 권한을 보유한 하나 이상의 Experience Cloud 그룹의 멤버여야 합니다.
* 왼쪽 탐색 메뉴의 마케팅 앱 섹션에 Analytics 및 Target이 표시되는지 확인하십시오.

## 보고서에서 바운스 비율, 바운스 및 퇴장 지표가 양수로 표시됩니다. {#section_B5C3D56EF0344407AE67ABEB93037F5A}

보고서에서 양수로 표시되는 이러한 지표는 알려진 문제입니다.

이러한 지표는 음수이지만, 상승도는 Target 보고서에서 양수인 것처럼 표시됩니다. 예를 들어 낮은 바운스 비율이 필요하더라도 상승도가 가장 높은 우승자로 높은 바운스 비율이 표시됩니다. 이러한 지표 및 유사 지표에 유의하여 보고서를 기준으로 수치를 높일지 또는 줄일지 결정을 내려야 합니다.

## 필요한 보고서 세트가 표시되지 않습니다. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

[!DNL Target Standard/Premium]에 표시되는 보고서 세트 목록은 [!DNL Target]용 보고 소스로서의 [!DNL Analytics] (A4T)에 구성된 보고서 세트 목록입니다. 보유 중인 보고서 세트 중 일부는 표시되지 않을 수 있습니다.

여러 보고 소스를 사용하는 경우 보고서 세트는 [!DNL Target]에 설정된 기본 보고 소스에도 있어야 합니다. 기본 보고 소스에 보고서 세트가 없는 경우 보고서 세트는 표시되지 않습니다.

찾고 있는 보고서 세트가 여전히 표시되지 않으면 [클라이언트 지원 팀](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하여 이를 활성화하십시오.

## 보고서에 예상만큼 많은 데이터가 표시되지 않습니다. {#section_75002584FA63456D8D9086172925DD8D}

특히 방문자가 경험을 사용할 자격이 있는 페이지에서 구현을 검토하고, 보조 데이터 ID가 [!DNL Target] 및 [!DNL Analytics] 호출에서 일치하는지 확인하십시오.

* **at.js 1.x**: [!DNL Target] 호출에서는 보조 ID가 `mboxMCSDID` 매개변수에 포함되어 있습니다. [!DNL Analytics] 호출에서는 보조 ID가 `sdid` 매개변수에 포함되어 있습니다.
* **at.js 2.x**: [!DNL Target] 호출에서는 보조 ID가 HTTP 헤더에 `experienceCloud.analytics.supplementalDataId`의 값으로 반환됩니다. [!DNL Analytics] 호출에서는 보조 ID가 `sdid` 매개변수에 포함되어 있습니다.

보조 ID를 검사하는 가장 간편한 방법은 Adobe Experience Platform Debugger를 사용하는 것입니다.

디버거를 설치하지 않았다면 [Adobe Experience Platform Debugger 소개](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html?lang=ko)를 참조하십시오.

![디버거](/help/main/c-integrating-target-with-mac/a4t/assets/debugger.png)

[!DNL Target] 호출에 보조 데이터 ID가 없습니다. [!DNL at.js] 전에 [!DNL VisitorAPI.js] 파일이 로드되었는지 확인하십시오. [!DNL Analytics] 호출에 보조 데이터 ID가 없다면 [!DNL Target] 호출 전에 [!DNL Analytics] 호출이 발생하는지 확인하십시오.

자세한 내용은 [Analytics for Target 구현](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A)이나 [고객 지원](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오.
