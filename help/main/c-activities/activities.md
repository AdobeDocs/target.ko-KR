---
keywords: 활동 목록;활동;활동;활동 유형;활동 편집;활동 작업;활동 속성;활동 목록 필터;활동 제한 사항;개인화;개인화
description: Adobe에서의 활동 방법 알아보기 [!DNL Target] 을 사용하면 특정 대상에게 콘텐츠를 개인화하고 페이지 설계를 테스트할 수 있습니다.
title: 을 사용하여 콘텐츠를 개인화하고 페이지 설계를 테스트하려면 어떻게 해야 합니까? [!DNL Target]?
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
source-git-commit: 4b62017fe4dca61b5b05c7778f3a02cf446c17f7
workflow-type: tm+mt
source-wordcount: '2489'
ht-degree: 44%

---

# 활동

[!DNL Adobe Target] 의 활동을 통해 특정 대상에게 콘텐츠를 개인화하고 페이지 설계를 테스트할 수 있습니다. 

예를 들어 여성의 여름 신발에 대한 정보를 강조 표시하는 페이지와 보다 일반적인 여름 의류를 강조 표시하는 랜딩 페이지 등 두 개의 다른 랜딩 페이지를 테스트하는 활동을 디자인할 수 있습니다. 활동은 이러한 각 랜딩 페이지가 표시되는 시기를 제어하는 조건과 보다 성공적인 페이지를 확인하는 지표를 결정합니다. 특정 날짜 사이 등의 특정 조건이 충족될 때 시작되고 종료되거나 활동이 승인될 때 시작되고 비활성화될 때 종료되도록 활동이 구성됩니다.

활동을 디자인할 때는 신중하게 계획해야 합니다. 활동이 시작되는 시기와 지속되는 기간을 결정합니다. 그런 후에 오퍼를 표시하고 각 오퍼에 대상을 할당합니다.

## 활동 목록 {#section_DE8E2DB30D534962A931EF8BB48240F5}

[!UICONTROL 활동] 목록은 [!DNL Target]을 열 때의 기본 보기입니다. 이 페이지에서 활동을 만들고 기존 활동을 관리할 수 있습니다.

[!DNL Target] UI 상단에 있는 [!UICONTROL 활동] 탭을 클릭하여 [!UICONTROL 활동] 목록을 표시할 수도 있습니다.

>[!NOTE]
>
>다음 그림 및 표는 현재 베타 버전인 업데이트된 활동 목록 UI의 기능을 보여주며 곧 출시될 예정입니다.


![활동 목록](/help/main/c-activities/assets/activities-list-new.png)

다음 [!UICONTROL 활동] list는 모든 활동에 대한 개요를 제공하며 다양한 작업을 수행할 수 있도록 해 줍니다.

| 요소 | 설명 |
|--- |--- |
| 왼쪽 탐색 레일 | 저장된 활동 또는 라이브 활동과 실패한 활동 간 또는 [초안 활동](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL 필터 표시] 아이콘<P>![필터 표시 아이콘](/help/main/c-activities/assets/show-filters-icon.png) | 다음을 클릭하여 필터에 액세스 **[!UICONTROL 필터 표시]** 목록 맨 위에 있는 아이콘.<P>자세한 내용은 [활동 목록에 필터 적용](#filters) 아래요. |
| 검색 상자 | 활동을 빠르게 찾거나 다음에 표시되는 활동 수를 줄이십시오. [!UICONTROL 활동] 목록을 표시합니다. 다음을 기준으로 검색할 수 있습니다. [!UICONTROL 이름], [!UICONTROL URL], 또는 [!UICONTROL ID]. |
| [!UICONTROL 활동 만들기] | 활동을 만듭니다. 다양한 활동 유형 만들기에 대한 자세한 내용은 다음을 참조하십시오. <ul><li>[A/B 테스트 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[자동 할당 활동 만들기](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[자동 타겟 활동 만들기](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[자동화된 개인화 활동 만들기](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[경험 타기팅 활동 만들기](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[다변량 테스트 만들기](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[권장 사항 활동 만들기](/help/main/c-recommendations/recommendations.md)</li></ul>각 유형에 대한 자세한 내용은 [활동 유형](#types) 아래요. |
| [!UICONTROL 모바일 미리 보기 링크 만들기]<P>![기타 작업 메뉴](/help/main/c-activities/assets/icon-create-mobile-link.png) | 사용 [모바일 미리 보기 링크](https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/target-mobile-preview.html) 모바일 앱 활동에 대한 간단한 종단 간 QA를 수행할 수 있습니다.<P>다음을 클릭합니다. **추가 옵션** 아이콘(세로 줄임표)을 클릭하고 **모바일 미리 보기 링크 만들기**&#x200B;그런 다음 모바일에서 테스트할 활동을 선택합니다. |
| 표 맞춤화<P>![표 맞춤화 아이콘](/help/main/c-activities/assets/icon-customize-table.png) | 에 표시되는 열 변경 [!UICONTROL 활동] 다음을 클릭하여 나열 **[!UICONTROL 표 맞춤화]** 아이콘 을 클릭하여 테이블의 오른쪽 상단에서 원하는 열을 선택하거나 선택 취소합니다.<P>변경 사항은 계정에 적용되며 로그아웃한 후에도 활성 상태로 유지됩니다 [!DNL Target]. |
| 대량 작업 확인란 | 모든 활동 또는 선택한 활동에 대해 일괄 작업을 수행합니다.<P>사용 가능한 작업 목록은 권한 및 활동 상태에 따라 다음을 참조하십시오. [빠른 작업 수행](#quick-actions) 아래요. |
| [!UICONTROL 유형] | 활동 유형. 다음 [!UICONTROL 유형] 열을 사용하면 유형별로 각 활동을 빠르게 식별할 수 있습니다. <ul><li>AB-M: 수동 [!UICONTROL A/B 테스트]</li><li>AB-AA: [!UICONTROL 자동 할당]</li><li>AB-AT: [!UICONTROL 자동 타기팅]</li><li>AP: [!UICONTROL Automated Personalization]</li><li>XT [!UICONTROL 경험 타기팅]</li><li>MVT: [!UICONTROL 다변량 테스트]</li><li>REC: [!UICONTROL Recommendations]</li></ul>각 유형에 대한 자세한 내용은 [활동 유형](#types) 아래요. |
| [!UICONTROL 이름] | 활동의 이름. 활동 이름을 클릭하여 해당 활동의 [!UICONTROL 개요] 페이지를 가리키도록 업데이트하는 중입니다. <P>다음을 클릭합니다. **[!UICONTROL 빠른 정보]** 아이콘을 클릭하면 팝업 카드에서 해당 활동에 대한 자세한 정보를 볼 수 있습니다.<p>다음을 클릭합니다. **[!UICONTROL 추가 작업]** 각 활동 이름 옆에 있는 아이콘(가로 줄임표)을 클릭하여 활동에 대한 빠른 작업을 수행할 수 있는 메뉴를 엽니다. 사용 권한 및 활동 상태에 따라 다음 작업을 사용할 수 있습니다. [!UICONTROL 편집], [!UICONTROL 활성화], [!UICONTROL 비활성화], [!UICONTROL 복사], [!UICONTROL 삭제], 및 [!UICONTROL 보관]. 각 작업에 대한 자세한 내용은 [빠른 작업 수행](#quick-actions) 아래요.<P>테이블 헤더를 클릭하여 목록을 이름별로 오름차순 또는 내림차순으로 정렬합니다. |
| [!UICONTROL 상태] | 활동의 상태는 다음 중 하나일 수 있습니다.<ul><li>**라이브**: 활동이 현재 실행 중입니다.</li><li>**초안**: 활동 설정이 시작되었지만 활동이 다음 위치에 있습니다. [초안 모드](/help/main/c-activities/edit-activity.md) 및 은(는) 아직 실행할 준비가 되지 않았습니다.</li><li>**예약됨**: 지정된 시작 날짜 및 시간에 도달하면 활동이 활성화되도록 준비되었습니다.</li><li>**비활성**: 활동이 일시 정지되었거나 비활성화되었습니다.</li><li>**동기화 중**[!DNL Target]: 활동이 저장되었으며 배달 네트워크에 동기화되고 있습니다.</li><li>**종료**: 활동의 지정된 종료 날짜 및 시간에 도달하여 활동이 더 이상 지원되지 않습니다.</li><li>**보관됨**: 활동이 보관되었습니다. 보관된 활동을 활성화하여 다시 사용할 수 있습니다.</li></ul>**참고**[!DNL Target]: API 방법을 사용하여 UI 외부에서의 활동 활성화와 같은 특정 작업을 수행하면 업데이트가 UI로 전파되는 데 최대 10분이 걸릴 수 있습니다.[!DNL Target] |
| [!UICONTROL 마지막 업데이트 날짜] | 활동을 마지막으로 업데이트한 날짜 및 시간과 그 사람.<P>날짜별로 목록을 오름차순 또는 내림차순으로 정렬하려면 테이블 헤더를 클릭하십시오. |
| [!UICONTROL 우선순위] | 활동의 우선 순위입니다.<P>대상이 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.<P>다음에 따라 [설정](/help/main/administrating-target/reporting.md), [!DNL Target] 의 UI 및 옵션 [!UICONTROL 우선 순위] 다양합니다. 낮음, 중간 또는 높음의 레거시 설정을 사용하거나 0에서 999까지 세분화된 우선순위를 사용할 수 있습니다. |
| [!UICONTROL 속성] | 활동에 대한 [속성](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)을 표시합니다.<P>Enterprise 사용자 권한은 [Target Premium](/help/main/c-intro/intro.md#premium) 기능. |
| [!UICONTROL 수입의 예상 상승도] | 대상의 100%에게 가장 성과가 좋은 경험이 표시되는 경우 수입의 예상되는 증가를 보여줍니다.<P>다음 공식을 사용하여 계산됩니다.<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>압축 양식에서 소수 앞에 한자릿수만 있으면 최대 소수 첫째 자리로 반올림됩니다. 예를 들어, $1.6M, $60K, $900, $8.5K, $205K와 같습니다.<P>승자를 확정하기에 충분한 데이터가 없거나 예상 비용이 없는 활동의 경우 이 열에 &quot;---&quot;이 표시됩니다.<P>자세한 내용은 [매출 상승도 평가](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오. |
| [!UICONTROL 소스] | 활동이 만들어진 위치를 표시합니다. [!DNL Adobe Target], [ADOBE TARGET API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=ko-KR), [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html), [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html), 또는 [Adobe Mobile Services](https://developer.adobe.com/client-sdks/documentation/). |
| [!UICONTROL 위치] | 활동용 URL은 활동이 표시되는 위치를 나타냅니다. 이 열은 활동을 빠르게 식별하고 특정 페이지에서 이미 활동이 실행 중인지 여부를 판별하는 데 도움이 됩니다.<P>활동이 여러 URL에서 실행되는 경우 링크에 추가로 사용된 URL의 수가 표시됩니다. 해당 활동에 대한 전체 URL 목록을 보려면 링크를 클릭하십시오.<P>URL을 기준으로 검색할 수 있습니다. 검색 상자 옆에 있는 드롭다운 목록을 사용하고 선택 [!UICONTROL URL]. |
| Author | 활동을 만든 사람의 이름입니다. |
| [!UICONTROL 의사 결정 방법] | 각 활동에 사용되는 의사 결정 방법: [서버측](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html) 또는 [클라이언트측](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html). |

## 활동 유형 {#types}

[!DNL Target] 에는 여러 활동 유형이 포함되어 있습니다. 다음 표는 자세한 내용을 알 수 있는 링크와 함께 각 활동 유형에 대한 개요를 제공합니다. 목적에 가장 적합한 활동 유형을 선택하는 데 도움이 되도록 [Adobe Target 활동 안내서](/help/main/c-activities/target-activities-guide.md)를 만들었습니다.

| 활동 유형 | 설명 |
|--- |--- |
| [A/B 테스트](/help/main/c-activities/t-test-ab/test-ab.md) | A/B 테스트에서는 웹 사이트 콘텐츠의 버전을 두 개 이상 비교하여 사전 지정된 테스트 기간 동안 전환율이 가장 많이 향상된 버전을 확인합니다. |
| [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | [!UICONTROL 자동 할당]는 A/B 테스트의 한 유형으로, 둘 이상의 경험에서 승자를 식별하고, 테스트가 계속 실행되고 학습되는 동안 변환을 늘리기 위해 더 많은 트래픽을 승자에게 자동으로 재할당합니다. |
| [자동 타겟팅](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<P>![Target Premium](/help/main/assets/premium.png) | A/B 테스트의 한 유형인 자동 타겟 은 컨텐츠를 개인화하고 전환을 유도하기 위해 고급 기계 학습을 사용하여 성과가 좋은 마케터가 정의한 여러 경험 중에서 식별하고, 개별 고객의 프로필과 이 프로필과 유사한 프로필을 가진 이전 방문자의 행동을 기반으로 각 방문자에게 가장 잘 맞춤 설정된 경험을 제공합니다. |
| [다변량 테스트](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | [!UICONTROL Multivariate Testing] (MVT)는 페이지의 요소 간에 오퍼 조합을 비교하여 특정 대상에 대해 성과가 가장 좋은 조합을 판별하고 활동의 성공에 영향을 가장 많이 주는 요소를 식별합니다. |
| [경험 타기팅](/help/main/c-activities/t-experience-target/experience-target.md) | [!UICONTROL Experience Targeting] (XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상자에게 전달합니다. |
| [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<P>![Target Premium](/help/main/assets/premium.png) | [!UICONTROL Automated Personalization] (AP)는 컨텐츠를 개인화하고 전환을 유도하기 위해, 오퍼나 메시지를 결합하고 고급 기계 학습을 사용하여 방문자의 개별 고객 프로필을 기반으로 다양한 변형을 각 방문자와 연결합니다. |
| [Recommendations](/help/main/c-recommendations/recommendations.md)<P>![Target Premium](/help/main/assets/premium.png) | 권장 사항은 사이트에서의 방문자의 활동에 따라 웹 사이트 방문자에게 제품을 제안하는 방법을 결정합니다.<P>예를 들어 배낭을 구입하는 사람이 하이킹 신발과 등산용 스틱까지 구입하도록 하려는 경우, &quot;이 항목을 구입하고 다른 항목도 구입한 사람&quot; 알고리즘을 사용하여 종종 함께 구입하는 항목을 보여 주는 권장 사항을 생성할 수 있습니다. 또는 &quot;이 동영상을 본 사용자&quot; 알고리즘을 사용하여 시청 중인 비디오와 유사한 비디오를 추천하여 방문자가 미디어 사이트에서 더 많은 시간을 보내도록 유도할 수 있습니다.<P>**참고**: 내에 권장 사항을 포함할 수도 있습니다 [!UICONTROL A/B 테스트], [!UICONTROL 자동 할당], [!UICONTROL 자동 타기팅], 및 [!UICONTROL 경험 타기팅] (XT) 활동. 자세한 내용은 [오퍼로서의 Recommendations](/help/main/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오. 이 기능을 사용하려면 [Target Premium 라이선스](/help/main/c-intro/intro.md#premium)가 있어야 합니다. |

## 활동 목록에 필터 적용 {#filters}

다음을 클릭하여 필터에 액세스 **[!UICONTROL 필터 표시]** 목록 맨 위에 있는 아이콘.

![필터 옵션](/help/main/c-activities/assets/show-filters-options.png)

메뉴를 사용하면 다음 속성으로 활동을 필터링할 수 있습니다. |속성|세부 정보| | — | — | |[!UICONTROL 유형]|필터링 기준 [활동 유형](#types).| |[!UICONTROL 상태]|활동 상태별로 필터링합니다.| |[!UICONTROL 보고 소스]|보고 소스로 필터링합니다.<ul><li>[분석](/help/main/c-integrating-target-with-mac/a4t/a4t.md): 를 사용하는 활동 표시 [!UICONTROL Analytics for Target] (A4T) 를 보고 소스로 사용할 때에는 적용되지 않습니다.</li><li>[Target](/help/main/c-reports/reports.md): 를 사용하는 활동 표시 [!DNL Target] 를 보고 소스로 사용합니다.</li></ul>| |[!UICONTROL 경험 작성기]|활동을 만드는 동안 경험 작성기가 사용된 필터:<ul><li>[비주얼](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): 를 사용하여 생성된 활동을 표시합니다. [!UICONTROL 시각적 경험 작성기] (VEC).</li><li>[양식 기반](/help/main/c-experiences/form-experience-composer.md): 를 사용하여 생성된 활동 표시 [!UICONTROL 양식 기반 경험 작성기].</li></ul>| |[!UICONTROL 지표 유형]|다음 기준 필터링 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md) 활동을 만드는 동안 이(가) 선택되었습니다.<ul><li>변환</li><li>수입</li><li>참여</li></ul>| |[!UICONTROL 의사 결정 방법]|각 활동에 사용된 의사 결정 방법으로 필터링<ul><li>[서버측](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html): 서버측 의사 결정을 사용하는 활동을 표시합니다.</li><li>[클라이언트측](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html): 클라이언트측 의사 결정을 사용하는 활동을 표시합니다.</li></ul>| |[!UICONTROL 활동 소스]|각 활동을 만드는 데 사용되는 활동 소스로 필터링합니다.<ul><li>[!DNL Adobe Target]</li><li>[ADOBE TARGET API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=ko-KR)</li><li>[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html)</li><li>[Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html)</li><li>[Adobe Mobile 서비스](https://developer.adobe.com/client-sdks/documentation/)</li></ul>| |[!UICONTROL 속성]|다음을 기준으로 필터링 [속성](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) 활동을 만든 시간.|

## 빠른 작업 수행 {#quick-actions}

다음을 클릭합니다. **[!UICONTROL 추가 작업]** 각 활동 이름 옆에 있는 아이콘(가로 줄임표)을 클릭하여 활동에 대한 빠른 작업을 수행할 수 있는 메뉴를 엽니다.

![빠른 작업 옵션](/help/main/c-activities/assets/quick-actions.png)

사용 권한 및 활동 상태에 따라 다음 작업을 사용할 수 있습니다.

| 작업 | 설명 |
| --- | --- |
| [!UICONTROL 편집] | 활동을 변경합니다. 모든 활동은 편집할 수 있습니다.<P>활동을 편집할 수 있는 다양한 방법에 대해서는 [활동 편집 또는 초안으로 저장](/help/main/c-activities/edit-activity.md)을 참조하십시오. |
| [!UICONTROL 비활성화] | 라이브 또는 예약된 활동을 중지합니다. 비활성화된 활동은 다시 활성화하거나 보관할 수 있습니다.<P>활동을 비활성화하거나 보관한 후에 다시 활성화하는 경우, 비활성화 또는 보관 이전에 활동에 있었던 방문자는 재활성화 이후에도 계속해서 해당 활동에 속하게 됩니다. 두 이벤트 사이의 시간 동안 기록된 전환 지표는 해당 활동으로 분류되지 않습니다. |
| [!UICONTROL 활성화] | 비활성 활동 또는 활성화할 준비가 된 활동을 시작합니다. |
| [!UICONTROL 보관] | 활동을 보관 파일에 보냅니다. 기본적으로 보관된 활동은 더 이상 [!UICONTROL 활동] 목록을 표시합니다. 보관된 활동을 보려면 이러한 활동을 포함하도록 활동 목록에 대한 필터를 변경하십시오. 보관된 활동을 활성화하여 다시 사용할 수 있습니다.<P>활동을 비활성화하거나 보관한 후에 다시 활성화하는 경우, 비활성화 또는 보관 이전에 활동에 있었던 방문자는 재활성화 이후에도 계속해서 해당 활동에 속하게 됩니다. 두 이벤트 사이의 시간 동안 기록된 전환 지표는 해당 활동으로 분류되지 않습니다. |
| [!UICONTROL 복사] | 활동을 복사합니다. 모든 활동은 복사할 수 있습니다. 활동을 복사하면 동일한 이름에 &quot;사본&quot;이 추가된 채 새 활동이 만들어집니다. 예를 들어, &quot;브라우저 오퍼&quot;라는 테스트는 &quot;브라우저 오퍼 사본&quot;으로 복사됩니다.<P>시각적 오퍼는 활동과 함께 복사됩니다. 원래 활동에 영향을 주지 않고 사본에서 오퍼를 안전하게 편집할 수 있습니다. 유일한 예외는 콘텐츠/자산 폴더에 있는 저장된 오퍼와 이미지입니다. |
| [!UICONTROL 삭제] | 초안이나 활동을 삭제합니다.<P>**참고**:삭제된 활동은 복구할 수 없습니다. 이 활동이 다시 필요하지 않은지 확신할 수 없는 경우 [!UICONTROL 보관] 작업. 그런 다음 필요한 경우 활동을 다시 활성화할 수 있습니다. |

## 고려 사항

에 대한 다음 세부 사항을 참고하십시오. [!UICONTROL 활동] 목록:

* 보관된 활동과 종료된 활동은 [!UICONTROL 활동] 목록에 표시되지 않습니다. 이러한 활동을 보려면 [필터 아이콘](#filters) 목록의 맨 위에 있습니다.
* 활동이에서 원래 만들어진 시기 [!DNL Target Classic] 이(가) 비활성화되거나 삭제되며,에서 삭제됩니다. [!DNL Target Standard/Premium]. 원래 [!DNL Target Classic]에서 만들어진 삭제된 작업은 [!DNL Target Standard/Premium]의 [!UICONTROL 보관] 폴더로 보내지지 않습니다. 보관된 폴더 기능은 [!DNL Target Standard/Premium]에서 만들어진 활동에만 적용됩니다.
* [!UICONTROL 자동화된 개인화] (AP), [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟] 이외의 모든 활동 유형에서는 [!DNL Target] 또는 [!DNL Adobe Analytics]를 데이터 소스로 사용하도록 선택할 수 있습니다. [!UICONTROL AP], [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟]은 *항상* [!DNL Target] 데이터를 사용합니다.
* 활동은 몇 가지 채널에서 사용할 수 있습니다.

   * 웹 및 모바일 사이트
   * 키오스크 및 ATM을 포함하는 인터넷이 연결된 스크린 및 장치
   * 이메일 및 기타 획득 채널 또는 파트너 사이트
   * 모바일 앱
   * 태그된 콘텐츠를 제공할 수 있는 그 밖의 모든 곳

## 제한 {#section_049D4684403A4E07B998067EB8E9BE56}

각 Target 활동에는 다음의 콘텐츠 제한 사항이 있습니다.

| 항목 |  제한 |
|--- |--- |
| 고유 선택기 | 300 선택기가 다른 경험에서 반복되는 경우 한 번만 카운트됩니다. 그러나 동일한 경험에서 반복되는 경우에는 다시 카운트됩니다. |
| 각 경험의 오퍼 | 350 |
| 지표에 있는 클릭 추적 선택기 | 50 |
| 지표의 mbox | 50 |
| 대상 및 위치 | 50 대상 및 위치(mbox) 조합은 50개를 초과할 수 없습니다. |

이러한 제한을 초과하는 경우 활동을 저장할 수 없습니다.

활동에서 이러한 항목의 수를 늘리면 활동을 동기화하는 데 걸리는 시간도 늘어납니다 [!DNL Target].

V의 추가 제한 사항[!UICONTROL 시각적 경험 작성기] VEC, 참조 [시각적 경험 작성기 제한 사항](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## 속성을 로 가져옴 [!DNL Target] 의 외부에서 업데이트된 활동용 [!DNL Target] {#section_802B0D174E6A44E1A96F404CA81AAE44}

다음 기간 동안 활동이 만들어짐: [!DNL Target] 의 외부에서 업데이트됩니다. [!DNL Target] (예: API를 통해) 다음 활동 속성을 다시으로 가져옵니다. [!DNL Target]: `thirdpartyId`, `startDate`, `endDate`, `status`, `priority`, 및 `marketingCloudMetadata(remoteModifiedBy)`.

이 가져오기 작업은 활동 페이지를 열 때 실행되며 최대 지연 시간은 10분입니다.

## 교육 비디오 {#section_BE80D13A2E81460C885F902010E1AD87}

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### 활동 유형(9:03)

다음 비디오에서는 [!DNL Target Standard/Premium]에서 사용할 수 있는 활동 유형에 대해 설명합니다.

* [!DNL Adobe Target]에 포함된 활동 유형 설명
* 목표를 달성하기 위한 적절한 활동 유형 선택
* 모든 활동 유형에 적용되는 3단계 안내가 있는 워크플로 설명

>[!VIDEO](https://video.tv.adobe.com/v/17386)

