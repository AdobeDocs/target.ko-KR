---
keywords: 활동 목록;활동;활동;활동 유형;활동 편집;활동 작업;활동 속성;활동 목록 필터;활동 제한 사항;개인화;개인화
description: ' [!DNL Adobe Target] 활동을 통해 특정 대상을 위한 콘텐츠를 개인화하고 페이지 디자인을 테스트합니다.'
title: ' [!DNL Target]을(를) 사용하여 콘텐츠를 개인화하고 페이지 디자인을 테스트하려면 어떻게 해야 합니까?'
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
source-git-commit: 5012c2b849d6b415f08fcaa3be85508637e30481
workflow-type: tm+mt
source-wordcount: '2292'
ht-degree: 25%

---

# 활동 개요

[!DNL Adobe Target] 활동을 통해 특정 대상자에 대한 콘텐츠를 개인화하고 페이지 디자인을 테스트합니다.

예를 들어 여성의 여름 신발에 대한 정보를 강조 표시하는 페이지와 보다 일반적인 여름 의류를 강조 표시하는 랜딩 페이지 등 두 개의 다른 랜딩 페이지를 테스트하는 활동을 디자인할 수 있습니다. 활동은 이러한 각 랜딩 페이지를 표시할 시기를 제어하는 조건과 더 성공적인 페이지를 결정하는 지표를 결정합니다. 활동은 특정 날짜 사이와 같이 특정 조건이 충족될 때 시작되고 종료되도록 구성됩니다. 또는 활동이 승인될 때 시작하도록 선택하고 비활성화될 때 종료하도록 선택할 수 있습니다.

활동을 디자인할 때는 신중하게 계획해야 합니다. 활동이 시작되는 시기와 지속되는 기간을 결정합니다. 그런 후에 오퍼를 표시하고 각 오퍼에 대상자를 할당합니다.

## 활동 목록 {#section_DE8E2DB30D534962A931EF8BB48240F5}

[!UICONTROL Activities]을(를) 열 때 [!DNL Target] 목록이 기본 보기입니다. 이 페이지에서 활동을 만들고 기존 활동을 관리할 수 있습니다.

[!UICONTROL Activities] UI 상단의 [!UICONTROL Activities] 탭을 클릭하여 [!DNL Target] 목록을 표시할 수도 있습니다.

[!UICONTROL Activities] 목록은 [!DNL Target] 구현의 모든 활동에 대한 개요를 제공하며 다양한 작업을 수행할 수 있도록 해 줍니다.

다음 표는 [!UICONTROL Activities] UI의 [!DNL Target] 목록에 있는 다양한 요소를 이해하는 데 도움이 됩니다.

| 요소 | 설명 |
|--- |--- |
| [!UICONTROL Show filters] 아이콘<P>![필터 표시 아이콘](/help/main/assets/icons/Filter.svg) | 목록 맨 위에 있는 **[!UICONTROL Show Filters]** 아이콘을 클릭하여 필터에 액세스하여 활동을 [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], [!UICONTROL Decisioning Source], [!UICONTROL Activity Source] 및 [!UICONTROL Properties]별로 필터링합니다.<P>구성하는 필터는 현재 세션에서 영구적입니다.<P>자세한 내용은 아래의 [[!UICONTROL Activities] 목록에 필터 적용](#filters)을 참조하십시오. |
| 필드 검색 | 활동을 빠르게 찾거나 [!UICONTROL Activity] 목록에 표시되는 활동 수를 줄이십시오. 드롭다운을 사용하여 [!UICONTROL Activity Name], [!UICONTROL URL] 또는 [!UICONTROL ID]별로 검색할 수 있습니다.<P>사용자가 구성하는 검색 옵션은 현재 세션에서 지속됩니다. |
| [!UICONTROL Create Activity] | 활동을 만듭니다.<P>다양한 활동 유형 만들기에 대한 자세한 내용은 다음을 참조하십시오. <ul><li>[[!UICONTROL A/B Test] 활동 만들기](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[[!UICONTROL Auto-Allocate] 활동 만들기](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[[!UICONTROL Auto-Target] 활동 만들기](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[[!UICONTROL Automated Personalization] 활동 만들기](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[[!UICONTROL Experience Targeting] 활동 만들기](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[활동 만들기](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[[!UICONTROL Recommendations] 활동 만들기](/help/main/c-recommendations/recommendations.md)</li></ul>각 유형에 대한 자세한 내용은 아래의 [활동 유형](#types)을 참조하세요. |
| [!UICONTROL Create mobile preview link]<P>![추가 작업 메뉴](/help/main/assets/icons/MoreVertical.svg) | [모바일 미리 보기 링크](https://experienceleague.adobe.com/en/docs/target-dev/developer/mobile-apps/target-mobile-preview)를 사용하여 모바일 앱 활동에 대한 간단한 전체 QA를 수행합니다.<P>**추가 옵션** 아이콘을 클릭하고 **모바일 미리 보기 링크 만들기**&#x200B;를 선택한 다음 모바일에서 테스트할 활동을 선택하십시오. |
| 표 맞춤화<P>![표 사용자 지정 아이콘](/help/main/assets/icons/ColumnSetting.svg) | 페이지의 오른쪽 상단에 있는 [!UICONTROL Activity] 아이콘을 클릭한 다음 원하는 열을 선택하거나 선택 취소하여 **[!UICONTROL Customize Table]** 목록에 표시되는 열을 변경합니다.<P>변경 내용은 계정에 적용되며 [!DNL Target]에서 로그아웃한 후에도 활성 상태로 유지됩니다. |
| 대량 작업 확인란<P>![일괄 작업 아이콘](/help/main/assets/icons/Rectangle.svg) | 모든 활동 또는 선택한 활동에 대해 일괄 작업을 수행합니다.<P>사용 권한 및 활동 상태에 따라 사용 가능한 작업 목록을 보려면 아래의 [빠른 작업 수행](#quick-actions)을 참조하십시오. |
| [!UICONTROL Type] | 활동 유형. [!UICONTROL Type] 열을 사용하면 유형별로 각 활동을 빠르게 식별할 수 있습니다. <ul><li>**AB-M**: 수동 [!UICONTROL A/B Test]</li><li>**AB-AA**: [!UICONTROL Auto-Allocate]</li><li>**AB-AT**: [!UICONTROL Auto-Target]</li><li>**AP**: [!UICONTROL Automated Personalization]</li><li>**XT**: [!UICONTROL Experience Targeting]</li><li>**MVT**: [!UICONTROL Multivariate Test]</li><li>**REC**: [!UICONTROL Recommendations]</li></ul>각 유형에 대한 자세한 내용은 아래의 [활동 유형](#types)을 참조하세요. |
| [!UICONTROL Name] | 활동의 이름입니다. **[!UICONTROL Quick Info]**, ![, ](/help/main/assets/icons/InfoOutline.svg), [!UICONTROL Activity ID] 및 [!UICONTROL Activity Objective]을(를) 포함하여 팝업 카드에서 해당 활동에 대한 자세한 정보를 보려면 각 활동 이름 옆에 있는 [!UICONTROL Activity Location] 아이콘([!UICONTROL Goal]빠른 정보 아이콘[!UICONTROL Status])을 클릭하십시오.<P>각 활동 이름 옆의 **[!UICONTROL More actions]** 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmallList.svg) )을 클릭하여 활동에 대한 빠른 작업을 수행할 수 있는 메뉴를 엽니다. 사용 권한 및 활동 상태에 따라 [!UICONTROL Edit], [!UICONTROL Activate], [!UICONTROL Deactivate], [!UICONTROL Copy], [!UICONTROL Delete] 및 [!UICONTROL Archive] 작업을 사용할 수 있습니다.<P>각 작업에 대한 자세한 내용은 아래의 [빠른 작업 수행](#quick-actions)을 참조하십시오.<P>테이블 헤더를 클릭하여 목록을 이름별로 오름차순 또는 내림차순으로 정렬합니다. |
| [!UICONTROL Status] | 활동의 상태는 다음 중 하나일 수 있습니다.<ul><li>**[!UICONTROL Live]**: 활동이 현재 실행 중입니다.</li><li>**[!UICONTROL Scheduled]**: 지정된 시작 날짜 및 시간에 도달하면 활동이 활성화되도록 준비되었습니다.</li><li>**[!UICONTROL Inactive]**: 활동이 일시 중지되었거나 비활성화되었습니다.</li><li>**[!UICONTROL Ended]**: 활동의 지정한 종료 날짜 및 시간에 도달하여 활동이 더 이상 지원되지 않습니다.</li><li>**[!UICONTROL Archived]**: 활동이 보관되었습니다. 보관된 활동을 활성화하여 다시 사용할 수 있습니다.</li></ul>**참고**: API 방법을 사용하여 [!DNL Target] UI 외부에서의 활동 활성화와 같은 특정 작업을 수행하면 업데이트가 [!DNL Target] UI로 전파되는 데 최대 10분이 걸릴 수 있습니다. |
| [!UICONTROL Last Updated] | 활동을 마지막으로 업데이트한 날짜 및 시간과 그 사람.<P>날짜별로 목록을 오름차순 또는 내림차순으로 정렬하려면 테이블 헤더를 클릭하십시오. |
| [!UICONTROL Priority] | 활동의 우선 순위입니다.<P>대상자가 같은 동일한 위치에 여러 개의 활동이 지정되는 경우 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.<P>[설정](/help/main/administrating-target/reporting.md)에 따라 [!DNL Target]에 대한 [!UICONTROL Priority] UI 및 옵션이 달라집니다. [!UICONTROL Low], [!UICONTROL Medium] 또는 [!UICONTROL High]의 기존 설정을 사용하거나 0에서 999까지 세분화된 우선 순위를 사용할 수 있습니다.<P>우선 순위 설정에 대한 자세한 내용은 [목표 및 설정](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#section_DCBDC354261F420EBD4B43EA34947BAC)의 *활동 설정*&#x200B;에서 *우선 순위*&#x200B;를 참조하십시오. |
| [!UICONTROL Property] | 활동에 대한 [속성](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)을 표시합니다.<P>Enterprise 사용자 권한은 [Target Premium](/help/main/c-intro/intro.md#premium) 기능입니다. |
| [!UICONTROL Estimated Lift in Revenue] | 대상의 100%에게 가장 성과가 좋은 경험이 표시되는 경우 수입의 예상되는 증가를 보여줍니다.<P>다음 공식을 사용하여 계산됩니다.<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>압축 양식에서 소수 앞에 한자릿수만 있으면 최대 소수 첫째 자리로 반올림됩니다. 예를 들어, $1.6M, $60K, $900, $8.5K, $205K와 같습니다.<P>승자를 확정하기에 충분한 데이터가 없거나 예상 비용이 없는 활동의 경우 이 열에 &quot;---&quot;이 표시됩니다.<P>자세한 내용은 [매출 상승도 평가](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md)를 참조하십시오. |
| [!UICONTROL Source] | 활동이 만들어진 위치를 표시합니다. [!DNL Adobe Target], [Adobe Target API](https://experienceleague.adobe.com/en/docs/target-dev/developer/overview), [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html), [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html) 또는 [Adobe 모바일 서비스](https://developer.adobe.com/client-sdks/documentation/). |
| [!UICONTROL Author] | 활동을 만든 사람의 이름입니다. |
| [!UICONTROL Decisioning Method] | 각 활동에 사용된 의사 결정 메서드: [서버측](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=ko-KR) 또는 [클라이언트측](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html). |

<!--|[!UICONTROL Location]|The URL for the activity identifies where the activity is displayed. This column helps you quickly identify an activity and determine whether a particular page already has an activity running on it.<P>If an activity runs on multiple URLs, a link shows how many more URLs are used. Click the link to view the complete list of URLs for that activity.<P>You can search based on the URL. Use the drop-down list next to the search box and select [!UICONTROL URL].|-->

## 활동 유형 {#types}

[!DNL Target]에 여러 활동 유형이 포함되어 있습니다. 다음 테이블은 자세한 내용을 알 수 있는 링크와 함께 각 활동 유형에 대한 개요를 제공합니다. 목적에 가장 적합한 활동 유형을 선택하는 데 도움이 되도록 [Adobe Target 활동 안내서](/help/main/c-activities/target-activities-guide.md)를 사용하십시오.

| 활동 유형 | 설명 |
|--- |--- |
| [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md) | A/B 테스트에서는 웹 사이트 콘텐츠의 버전을 두 개 이상 비교하여 사전 지정된 테스트 기간 동안 전환율이 가장 많이 향상된 버전을 확인합니다. |
| [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | A/B 테스트 유형인 [!UICONTROL Auto-Allocate]은(는) 둘 이상의 경험에서 승자를 식별하고, 테스트가 계속 실행되고 학습되는 동안 변환을 늘리기 위해 더 많은 트래픽을 승자에게 자동으로 재할당합니다. |
| [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<P>![Target Premium](/help/main/assets/premium.png) | A/B 테스트의 한 유형인 자동 타겟 은 컨텐츠를 개인화하고 전환을 유도하기 위해 고급 기계 학습을 사용하여 성과가 좋은 마케터가 정의한 여러 경험 중에서 식별하고, 개별 고객의 프로필과 이 프로필과 유사한 프로필을 가진 이전 방문자의 행동을 기반으로 각 방문자에게 가장 잘 맞춤 설정된 경험을 제공합니다. |
| [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | [!UICONTROL Multivariate Testing]&#x200B;(MVT)은 페이지의 요소에 있는 오퍼 조합을 비교하여 특정 대상에 대해 성과가 가장 좋은 조합을 판별하고 활동의 성공에 영향을 가장 많이 주는 요소를 식별합니다. |
| [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) | [!UICONTROL Experience Targeting]&#x200B;(XT)에서는 마케터가 정의한 규칙 및 기준에 따라 콘텐츠를 특정 대상에 전달합니다. |
| [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<P>![Target Premium](/help/main/assets/premium.png) | [!UICONTROL Automated Personalization]&#x200B;(AP)은(는) 콘텐츠를 개인화하고 전환을 유도하기 위해 오퍼나 메시지를 결합하고 고급 기계 학습을 사용하여 방문자의 개별 고객 프로필을 기반으로 다양한 변형을 각 방문자와 연결합니다. |
| [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)<P>![Target Premium](/help/main/assets/premium.png) | 권장 사항은 사이트에서의 방문자의 활동에 따라 웹 사이트 방문자에게 제품을 제안하는 방법을 결정합니다.<P>예를 들어, 배낭을 구입하는 사람이 하이킹 신발과 등산용 스틱까지 구입하도록 하려는 경우, &quot;이 항목을 구입하고 다른 항목도 구입한 사람&quot; 알고리즘을 사용하여 종종 함께 구입하는 항목을 보여 주는 권장 사항을 생성할 수 있습니다. 또는 &quot;이 동영상을 본 사용자&quot; 알고리즘을 사용하여 시청 중인 비디오와 유사한 비디오를 추천하여 방문자가 미디어 사이트에서 더 많은 시간을 보내도록 유도할 수 있습니다.<P>**참고**: [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] 및 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동 내에 권장 사항을 포함할 수도 있습니다. 자세한 내용은 [오퍼로서의 추천](/help/main/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오. 이 기능을 사용하려면 [Target Premium 라이선스](/help/main/c-intro/intro.md#premium)가 있어야 합니다. |

## 활동 목록에 필터 적용 {#filters}

목록 맨 위에 있는 **[!UICONTROL Show Filters]** 아이콘(![필터 표시 아이콘](/help/main/assets/icons/Filter.svg))을 클릭하여 필터에 액세스합니다.

메뉴를 사용하면 다음 속성으로 활동을 필터링할 수 있습니다.

| 속성 | 세부 사항 |
| --- | --- |
| [!UICONTROL Type] | [활동 유형](#types)별로 필터링합니다. |
| [!UICONTROL Status] | 활동 상태별로 필터링합니다.<ul><li>**[!UICONTROL Live]**: 활동이 현재 실행 중입니다.</li><li>**[!UICONTROL Scheduled]**: 지정된 시작 날짜 및 시간에 도달하면 활동이 활성화되도록 준비되었습니다.</li><li>**[!UICONTROL Inactive]**: 활동이 일시 중지되었거나 비활성화되었습니다.</li><li>**[!UICONTROL Ended]**: 활동의 지정한 종료 날짜 및 시간에 도달하여 활동이 더 이상 지원되지 않습니다.</li><li>**[!UICONTROL Archived]**: 활동이 보관되었습니다. 보관된 활동을 활성화하여 다시 사용할 수 있습니다.</li></ul>더 이상 사용되지 않는 [!UICONTROL Save as Draft] 및 [!UICONTROL Syncing] 상태에 대한 자세한 내용은 이 표 아래의 메모를 참조하십시오. |
| [!UICONTROL Reporting Source] | 보고 소스로 필터링합니다.<ul><li>[[!DNL Analytics]](/help/main/c-integrating-target-with-mac/a4t/a4t.md): [!UICONTROL Analytics for Target]&#x200B;(A4T)을 보고 소스로 사용하는 활동을 표시합니다.</li><li>[[!DNL Target]](/help/main/c-reports/reports.md): [!DNL Target]을(를) 보고 소스로 사용하는 활동을 표시합니다.</li><li>[[!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md): [!DNL Adobe Customer Analytics]을(를) 보고 소스로 사용하는 활동을 표시합니다.</li></ul> |
| [!UICONTROL Experience Composer] | 활동을 만드는 동안 경험 작성기가 사용된 기준 필터링:<ul><li>[Visual](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): VEC([!UICONTROL Visual Experience Composer])를 사용하여 만든 활동을 표시합니다.</li><li>[양식 기반](/help/main/c-experiences/form-experience-composer.md): [!UICONTROL Form-Based Experience Composer]을(를) 사용하여 만든 활동을 표시합니다.</li></ul> |
| [!UICONTROL Metrics Type] | 활동을 만드는 동안 [성공 지표](/help/main/c-activities/r-success-metrics/success-metrics.md)를 선택한 기준 필터링.<ul><li>[!UICONTROL Conversion]</li><li>[!UICONTROL Revenue]</li><li>[!UICONTROL Engagement]</li><li>[!UICONTROL Use an Analytics metric]</lI></ul> |
| [!UICONTROL Decisioning Method] | 각 활동에 사용된 의사 결정 방법으로 필터링합니다.<ul><li>[서버측](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=ko-KR): 서버측 의사 결정을 사용하는 활동을 표시합니다.</li><li>[클라이언트측](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html): 클라이언트측 의사 결정을 사용하는 활동을 표시합니다.</li></ul> |
| [!UICONTROL Activity Source] | 각 활동을 만드는 데 사용되는 활동 소스로 필터링합니다.<ul><li>[!DNL Adobe Target]</li><li>[[!DNL Adobe Target] API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html)</li><li>[[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/experience-platform.html)</li><li>[[!DNL Adobe Experience Manager]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html)</li><li>[[!DNL Adobe Mobile Services]](https://developer.adobe.com/client-sdks/home/)</li></ul> |
| [!UICONTROL Property] | 활동을 만든 [속성](/help/main/administrating-target/c-user-management/property-channel/property-channel.md)(으)로 필터링합니다. |


>[!NOTE]
>
>**업데이트된 UI에서 활동 상태 업데이트**: 사용자 인터페이스에 대한 최신 업데이트를 통해 [!UICONTROL Save as Draft] 및 [!UICONTROL Syncing] 상태를 더 이상 사용할 수 없습니다. 이제 모든 활동 만들기 및 편집이 GraphQL 계층을 사용하여 백엔드 [!DNL Target] 전달 시스템 내에서 직접 수행되므로 보다 간소하고 효율적인 프로세스가 보장되기 때문입니다.
>
>이전에는 활동이 먼저 [!DNL Target] 프론트엔드에 저장된 다음 백엔드 [!DNL Target] 전달 시스템에 동기화되어 해당 중간 상태가 필요했습니다. 더 이상 해당되지 않으므로 이러한 상태는 제거되었습니다.
>
>[!DNL Adobe]은(는) 일부 고객이 [!UICONTROL Save as Draft] 기능에 관심을 표시했음을 이해합니다. 이 피드백에 감사하지만 이 기능은 현재 지원되지 않습니다.

## 빠른 작업 수행 {#quick-actions}

각 활동 이름 옆의 **[!UICONTROL More actions]** 아이콘(![추가 작업 메뉴](/help/main/assets/icons/MoreVertical.svg))을 클릭하여 활동에 대한 빠른 작업을 수행할 수 있는 메뉴를 엽니다.

사용 권한 및 활동 상태에 따라 다음 작업을 사용할 수 있습니다.

| 액션 | 설명 |
| --- | --- |
| [!UICONTROL Edit] | 활동을 변경합니다. 모든 활동은 편집할 수 있습니다.<P>활동을 편집할 수 있는 다양한 방법에 대한 자세한 내용은 [활동 편집 또는 초안으로 저장](/help/main/c-activities/edit-activity.md)을 참조하십시오. |
| [!UICONTROL Deactivate] | 라이브 또는 예약된 활동을 중지합니다. 비활성화된 활동은 다시 활성화하거나 보관할 수 있습니다.<P>활동을 비활성화하거나 보관한 후에 다시 활성화하는 경우, 비활성화 또는 보관 이전에 활동에 있었던 방문자는 재활성화 이후에도 계속해서 해당 활동에 속하게 됩니다. 두 이벤트 사이의 시간 동안 기록된 전환 지표는 해당 활동으로 분류되지 않습니다. |
| [!UICONTROL Activate] | 비활성 활동 또는 활성화할 준비가 된 활동을 시작합니다. |
| [!UICONTROL Archive] | 활동을 보관 파일에 보냅니다. 기본적으로 보관된 활동은 더 이상 [!UICONTROL Activities] 목록에 표시되지 않습니다. 보관된 활동을 포함하도록 [!UICONTROL Activities] 목록에 대한 필터를 변경하십시오. 보관된 활동을 활성화하여 다시 사용할 수 있습니다.<P>활동을 비활성화하거나 보관한 후에 다시 활성화하는 경우, 비활성화 또는 보관 이전에 활동에 있었던 방문자는 재활성화 이후에도 계속해서 해당 활동에 속하게 됩니다. 두 이벤트 사이의 시간 동안 기록된 전환 지표는 해당 활동으로 분류되지 않습니다. |
| [!UICONTROL Copy] | 활동을 복사합니다. 모든 활동은 복사할 수 있습니다. 활동을 복사하면 동일한 이름에 &quot;사본&quot;이 추가된 채 새 활동이 만들어집니다. 예를 들어, &quot;브라우저 오퍼&quot;라는 테스트는 &quot;브라우저 오퍼 사본&quot;으로 복사됩니다.<P>시각적 오퍼는 활동과 함께 복사됩니다. 원래 활동에 영향을 주지 않고 사본에서 오퍼를 안전하게 편집할 수 있습니다. 유일한 예외는 콘텐츠/자산 폴더에 있는 저장된 오퍼와 이미지입니다. |
| [!UICONTROL Delete] | 초안이나 활동을 삭제합니다.<P>**참고**: 삭제된 활동은 복구할 수 없습니다. 이 활동이 다시 필요하지 않은지 확신할 수 없는 경우 [!UICONTROL Archive] 작업을 사용하십시오. 그런 다음 필요한 경우 활동을 다시 활성화할 수 있습니다. |

## 고려 사항

[!UICONTROL Activity] 목록에 대한 다음 세부 정보를 참고하십시오.

* [!UICONTROL Archived] 및 [!UICONTROL Ended] 활동이 [!UICONTROL Activities] 목록에 표시되지 않습니다. 이러한 활동을 보려면 목록 맨 위에 있는 [필터 아이콘](#filters)(![필터 표시 아이콘](/help/main/assets/icons/Filter.svg) )을 사용하여 필터링하십시오.
* 원래 [!DNL Target Classic]에서 만들어진 활동이 비활성화되거나 삭제되면 [!DNL Target Standard/Premium]에서 삭제됩니다. 원래 [!DNL Target Classic]에서 만들어진 삭제된 활동은 [!UICONTROL Archive]의 [!DNL Target Standard/Premium] 폴더로 전송되지 않습니다. 보관된 폴더 기능은 [!DNL Target Standard/Premium]에서 만들어진 활동에만 적용됩니다.
* [!UICONTROL Automated Personalization]&#x200B;(AP), [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 이외의 모든 활동 유형에서는 [!DNL Target] 또는 [!DNL Adobe Analytics]을(를) 데이터 소스로 사용하도록 선택할 수 있습니다. [!UICONTROL Automated Personalization], [!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] *항상*&#x200B;은(는) [!DNL Target] 데이터를 사용합니다.
* 활동은 몇 가지 채널에서 사용할 수 있습니다.

   * 웹 및 모바일 사이트
   * 키오스크 및 ATM을 포함하는 인터넷이 연결된 스크린 및 장치
   * 이메일 및 기타 획득 채널 또는 파트너 사이트
   * 모바일 앱
   * 태그된 콘텐츠를 제공할 수 있는 그 밖의 모든 곳

## 제한 {#section_049D4684403A4E07B998067EB8E9BE56}

각 [!DNL Target] 활동에는 다음과 같은 콘텐츠 제한 사항이 있습니다.

| 항목 |  제한 |
|--- |--- |
| 고유 선택기 | 선택기가 다른 경험에서 반복되는 경우 300으로 한 번 계산됩니다. 그러나 동일한 경험에서 반복되는 경우에는 다시 카운트됩니다. |
| 각 경험의 오퍼 | 350 |
| 지표에 있는 클릭 추적 선택기 | 50 |
| 지표의 mbox | 50 |
| 대상 및 위치 | 50개의 대상 및 위치(mbox) 조합은 50개를 초과할 수 없습니다. |

이러한 제한을 초과하는 경우 활동을 저장할 수 없습니다.

활동에서 이러한 항목의 수를 늘리면 [!DNL Target]에서 활동을 동기화하는 데 걸리는 시간도 늘어납니다.

[!UICONTROL Visual Experience Composer]&#x200B;(VEC)의 추가 제한에 대해서는 [시각적 경험 작성기 제한 사항](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721)을 참조하십시오.

## [!DNL Target] 외부에서 업데이트된 활동을 위해 [!DNL Target]&#x200B;(으)로 가져온 특성 {#section_802B0D174E6A44E1A96F404CA81AAE44}

[!DNL Target]에서 만든 활동이 [!DNL Target] 외부에서(예를 들어 API를 통해) 업데이트된 경우 [!DNL Target], `thirdpartyId`, `startDate`, `endDate`, `status` 및 `priority` 활동 특성을 다시 `marketingCloudMetadata(remoteModifiedBy)`(으)로 가져옵니다.

이 가져오기 작업은 [!UICONTROL Activities] 목록을 열 때 실행되며 최대 지연 시간은 10분입니다.

