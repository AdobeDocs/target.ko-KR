---
keywords: criteria;algorithm;industry vertical;page type;recommendation key;recommendation logic;logic;data range;behavior data source;partial design;backup recommendations;inclusion rules;attribute weighting
description: 기준은 Adobe Recommendations 활동의 콘텐츠를 제어합니다. 활동에 가장 적합한 권장 사항을 표시하는 기준을 만드십시오.
title: 기준 만들기
feature: criteria
uuid: 603d4b02-cdb6-40aa-9654-0086c23b0c8e
translation-type: tm+mt
source-git-commit: 35bd6358f1deaaccbf3f272c0f3ff53ed39fb332
workflow-type: tm+mt
source-wordcount: '3609'
ht-degree: 85%

---


# ![PREMIUM](/help/assets/premium.png) 기준 만들기{#create-criteria}

기준은 [!UICONTROL 권장 사항] 활동의 컨텐츠를 제어합니다. 활동에 가장 적합한 권장 사항을 표시하는 기준을 만드십시오.

## 새 기준 만들기

다음 섹션에서는 새 기준을 만드는 방법을 설명합니다.

### 새 기준 만들기 화면에 액세스

[!UICONTROL 새 기준 만들기] 화면에 도달하는 여러 방법이 있습니다. 일부 화면 옵션은 화면에 도달하는 방법에 따라 달라집니다.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. 여기서 만드는 기준은 자동으로 모든 [!DNL Recommendations] 활동에 사용 가능해집니다.
* When you are creating a [!DNL Recommendations] activity, click **[!UICONTROL Create Criteria]** on the [!UICONTROL Select Criteria] screen. 다른 [!DNL Recommendations] 활동과 함께 사용할 새 기준을 저장하는 선택 사항이 있습니다.
* [!DNL Recommendations] 활동을 편집하는 경우 페이지에서 [!UICONTROL 권장 사항 위치] 상자를 클릭하고 **[!UICONTROL 기준 변경]**&#x200B;을 선택합니다. On the [!UICONTROL Select Criteria] screen, click **[!UICONTROL Create Criteria]**. 다른 [!DNL Recommendations] 활동과 함께 사용할 새 기준을 저장하는 선택 사항이 있습니다.

다음 단계에서는 첫 번째 방법을 사용하여 새 기준 [!UICONTROL 만들기] 화면에 액세스한다고 가정합니다.[ **[!UICONTROL Recommendations]** ] > [ **[!UICONTROL 기준]** 라이브러리] 화면

1. Recommendations **[!UICONTROL >]** 기준을 클릭합니다 ****.

1. 기준 **[!UICONTROL 만들기]** > 기준 **[!UICONTROL 만들기를 클릭합니다]**.

   ![새 기준 만들기](/help/c-recommendations/c-algorithms/assets/CreateNewCriteria_full-new.png)

### 기본 정보 섹션 채우기 {#info}

1. **[!UICONTROL 기준 이름]**&#x200B;을 입력합니다.

   기준을 설명하는 데 사용되는 &quot;내부&quot; 이름입니다. 예를 들어, &quot;최고 마진 제품&quot; 기준을 호출하려고 하지만 제목이 공개적으로 표시되는 것을 원하지 않을 수 있습니다. 공개 제목을 설정하려면 다음 단계를 참조하십시오.

   ![기본 정보 섹션](/help/c-recommendations/c-algorithms/assets/basic-information.png)

1. 이 기준을 사용하는 모든 권장 사항에 대한 페이지에 표시할 공개 **[!UICONTROL 표시 제목]**&#x200B;을 입력합니다.

   예를 들어, 이 기준을 사용하여 권장 사항을 표시할 때 &quot;특정 항목을 본 사용자&quot; 또는 &quot;유사 제품&quot;을 표시할 수 있습니다.

1. 기준에 대한 간단한 **[!UICONTROL 설명]**&#x200B;을 입력합니다.

   설명은 기준을 식별하는 데 도움이 되며 기준의 용도에 대한 정보를 포함할 수 있습니다.

1. **[!UICONTROL 업계 카테고리]**&#x200B;를 선택합니다.

   * [!UICONTROL 소매/Ecommerce]
   * [!UICONTROL 리드 생성/B2B/금융 서비스]
   * [!UICONTROL 미디어/게시]

   기타 기준 옵션은 선택한 수직 시장에 따라 달라집니다.

1. **[!UICONTROL 페이지 유형]**&#x200B;을 선택합니다.

   여러 페이지 유형을 선택할 수 있습니다.

   수직 시장 및 페이지 유형을 함께 사용하여 저장된 기준을 분류할 수 있습니다. 이렇게 하면 다른 [!DNL Recommendations] 활동에 대한 기준을 좀 더 쉽게 다시 사용할 수 있습니다.

1. **[!UICONTROL 권장 사항 키]**&#x200B;를 선택합니다.

   키를 기반으로 기준을 지정하는 방법에 대한 자세한 내용은 [권장 사항 키를 기반으로 권장 사항 만들기](#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B)를 참조하십시오.

1. **[!UICONTROL 권장 사항 논리]**&#x200B;를 선택합니다.

   권장 사항 논리 선택 사항에 대한 자세한 내용은 [기준](../../c-recommendations/c-algorithms/algorithms.md)을 참조하십시오.

   >[!NOTE]
   >
   >If you select **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]**, you will have the option to set [content similarity rules](#similarity).

### 데이터 소스 옵션 지정

1. 표시할 권장 사항을 결정할 때 사용할 사용 가능한 내역 사용자 동작 데이터의 시간 범위를 결정하려면 **[!UICONTROL 데이터 범위]**&#x200B;를 설정합니다.

   ![데이터 범위 슬라이더](/help/c-recommendations/c-algorithms/assets/data-range.png)

   사이트에 많은 트래픽이 발생하고 동작이 자주 변경되는 경우 더 짧은 데이터 기간을 선택하십시오. 더 짧은 기간을 사용하면 [!DNL Recommendations]가 시장 및 비즈니스의 변화에 보다 신속하게 대응할 수 있습니다. 예를 들어, 기간이 더 짧다는 것은 방문자가 신학기 쇼핑 또는 크리스마스와 같은 시즌 쇼핑을 시작할 때 [!DNL Recommendations]에서 방문자 동작의 변화를 감지하고 해당 쇼핑 시즌에 적합한 항목을 추천할 수 있다는 것을 의미합니다.

   데이터가 충분하지 않거나 방문자 동작이 자주 바뀌지 않을 경우에는 좀 더 긴 기간을 선택할 수 있습니다. 그러나 많은 사이트에서 기간이 더 짧을수록 더 나은 권장 사항이 제공될 수 있습니다.

   사용 가능한 날짜 범위는 다음과 같습니다.

   * 2일
   * 1주
   * 2주
   * 1개월
   * 2개월

1. (Conditional) Select the desired **[!UICONTROL Behavioral Data Source]**: [!UICONTROL mboxes] or [!UICONTROL Analytics].

   >[!NOTE]
   >
   >행동 [!UICONTROL 데이터 소스] 섹션은 구현에서 Target에 [Analytics](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T)를 사용하는 경우에만표시됩니다.

   ![행동 데이터 소스 섹션](/help/c-recommendations/c-algorithms/assets/behavioural-data-source.png)

   [!UICONTROL Analytics]를 선택한 경우 원하는 보고서 세트를 선택합니다.

   If the criteria uses [!DNL Adobe Analytics] as the behavioral data source, once created, the time for criteria availability depends on whether the selected report suite and lookback window has been used for any other criteria, as explained below:

   * **1회성 보고서 세트 설정**: 보고서 세트가 지정된 데이터 범위 전환 확인 기간과 함께 처음 사용되는 경우, [!DNL Target Recommendations]은 2~7일 동안 [!DNL Analytics]에서 선택한 보고서 세트에 대한 동작 데이터를 완전히 다운로드할 수 있습니다. This time frame is dependent on the [!DNL Analytics] system load.
   * **이미 사용 가능한 보고서 세트를 사용하는 새 기준 또는 편집된 기준**: 새 기준을 만들거나 기존 기준을 편집할 때 선택한 보고서 세트를 선택한 데이터 범위와 같거나 그보다 적은 데이터 범위를 갖는 [!DNL Target Recommendations]에서 이미 사용한 경우 데이터를 즉시 사용할 수 있으며 일회성 설정이 필요하지 않습니다. 이러한 경우, 또는 선택한 보고서 세트나 데이터 범위를 수정하지 않고 알고리즘 설정이 편집된 경우 알고리즘이 12시간 이내에 실행되거나 재실행됩니다.
   * **지속적인 알고리즘 실행**: 데이터는 매일 [!DNL Analytics]에서 [!DNL Target Recommendations]으로 이동합니다. 예를 들어 [!UICONTROL 관심도 보기] 추천의 경우, 사용자가 제품을 볼 때 제품-보기 추적 호출이 실시간에 가깝게 [!DNL Analytics]에 전달됩니다. [!DNL Analytics] 데이터가 다음 날 일찍 [!DNL Target]에 푸시되고 [!DNL Target]이 12시간 이내에 알고리즘을 실행합니다.

   자세한 내용은 Target Recommendations과 [함께 Adobe Analytics 사용을 참조하십시오](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

### 콘텐츠 설정 지정 {#content}

콘텐츠 규칙은 권장 항목 수로 디자인을 채우지 못할 경우에 발생하는 결과를 결정합니다. 권장 사항 기준에 따라 디자인이 요구하는 것보다 더 적은 수의 권장 사항이 반환될 수 있습니다. 예를 들어, 디자인에 5개의 항목에 대한 공간이 있지만 기준에 따라 3개의 항목만 권장되는 경우 나머지 공간을 비워 두거나 백업 권장 사항을 사용하여 추가 공간을 채울 수 있습니다.

![컨텐츠 섹션](/help/c-recommendations/c-algorithms/assets/content.png)

1. (선택 사항) **[!UICONTROL 부분 디자인 렌더링]** 전환 효과를 &quot;설정&quot; 위치로 밀면

   가능한 한 많은 슬롯이 채워지지만 디자인 템플릿에는 나머지 슬롯의 빈 공간이 포함될 수 있습니다.

1. (선택 사항) [백업 **[!UICONTROL 표시] Recommendations]** 전환을 &quot;켜기&quot; 위치로 밀십시오.

   사이트에서 가장 많이 본 제품을 임의 선택하여 디자인에 남아 있는 빈 슬롯을 채웁니다.

   자세한 내용은 백업 권장 [사항 사용을 참조하십시오](/help/c-recommendations/c-algorithms/backup-recs.md).

1. (조건부) 이전 단계에서 **[!UICONTROL 백업 Recommendations]** 표시를 선택한 경우 백업 권장 사항에 **[!UICONTROL 포함 규칙 적용을 활성화할 수 있습니다]**.

   포함 규칙은 권장 사항에 포함할 항목을 결정합니다. 사용 가능한 옵션은 수직 시장에 따라 다릅니다.

   자세한 내용은 [아래에서 포함 규칙을](#inclusion) 지정합니다.

1. (선택 사항) 이전에 구입한 항목 **[!UICONTROL 권장]** 사항을 &quot;설정&quot; 위치로 끕니다.

   이 설정은 `productPurchasedId`를 기준으로 합니다. 기본 동작은 이전에 구입한 항목을 추천하지 않는 것입니다. 대부분의 경우 고객이 최근에 구입한 항목을 홍보하지 않습니다. 카약처럼 일반적으로 한 번만 구매하는 항목을 판매하는 경우에 유용합니다. 샴푸나 다른 개인 품목과 같이 사람들이 다시 구입하기 위해 다시 오는 품목을 판매하면 이 옵션을 사용하도록 설정해야 합니다.

다음 매트릭스는 [!UICONTROL 부분 디자인 렌더링] 및 [!UICONTROL 백업 Recommendations] 옵션을 사용할 때 표시되는 결과를 보여줍니다.

| 부분 디자인 렌더링 | 백업 Recommendations | 결과 |
|--- |--- |--- |
| 비활성화됨 | 비활성화됨 | 디자인이 요구하는 곳보다 더 적은 수의 권장 사항이 반환되면 권장 사항 디자인은 기본 콘텐츠로 대체되고 추가 권장 사항은 표시되지 않습니다. |
| 활성화됨 | 비활성화됨 | 디자인이 렌더링되지만 디자인 요구하는 것보다 더 적은 수의 권장 사항이 반환되면 빈 공백이 포함될 수 있습니다. |
| 활성화됨 | 활성화됨 | 백업 권장 사항은 사용 가능한 디자인 &quot;슬롯&quot;을 채우고 디자인을 완전히 렌더링합니다.<br>백업 권장 사항에 포함 규칙을 적용하여 적격의 백업 권장 사항 수를 디자인을 채울 수 없는 지점까지 제한하면 디자인이 부분적으로 렌더링됩니다.<br>이 조건에 따라 어떤 권장 사항도 반환되지 않고 포함 규칙이 백업 권장 사항 수를 0으로 제한하면 디자인이 기본 콘텐츠로 바뀝니다. |
| 비활성화됨 | 활성화됨 | 백업 권장 사항은 사용 가능한 디자인 &quot;슬롯&quot;을 채우고 디자인을 완전히 렌더링합니다.<br>백업 권장 사항에 포함 규칙을 적용하여 적격의 백업 권장 사항 수를 디자인을 채울 수 없는 지점까지 제한하면 디자인이 기본 콘텐츠로 바뀌고 권장 사항은 표시되지 않습니다. |

### Specify content similarity rules {#similarity}

[!UICONTROL 콘텐츠 유사성] 규칙을 사용하여 항목 또는 미디어 속성에 따라 권장 사항을 제공합니다.

>[!NOTE]
>
>If you selected **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]** as your [recommendation logic](#info), you will have the option to set content similarity rules.

콘텐츠 유사성은 항목 속성 키워드를 비교하고 여러 항목에 공통되는 키워드의 수에 따라 권장 사항을 제공합니다. 콘텐츠 유사성을 기준으로 하는 권장 사항은 강력한 결과를 전달하기 위해 과거 데이터가 필요하지 않습니다.

콘텐츠 유사성을 사용하여 권장 사항을 생성하는 방식은 *특정 항목을 본 사용자* 및 과거 동작을 기준으로 하는 기타 논리를 사용하는 권장 사항에 표시되지 않는 새 항목에 특히 유용합니다. 또한 콘텐츠 유사성을 사용하여 과거 구입 내역 또는 기타 기록 데이터가 없는 새 방문자를 위한 유용한 권장 사항을 생성할 수도 있습니다.

**[!UICONTROL 항목]**/**[!UICONTROL 유사한 속성의 미디어]**&#x200B;를 선택하는 경우 권장 사항을 결정할 때 특정 항목 속성의 중요도를 늘리거나 줄이는 규칙을 만드는 옵션이 제공됩니다. 서적과 같은 항목의 경우 *장르*, *저자*, *시리즈*&#x200B;와 같은 속성의 중요도를 높여 비슷한 서적을 권장할 수 있습니다.

![](assets/ContentSimilarity.png)

콘텐츠 유사성은 키워드를 사용하여 항목을 비교하므로 일부 속성(예: *메시지* 또는 *설명*)이 비교에 &quot;영향&quot;을 줄 수 있습니다. 이러한 속성을 무시하는 규칙을 만들 수 있습니다.

기본적으로 모든 속성은 *기준선*&#x200B;으로 설정됩니다. 이 설정을 변경하려는 경우가 아니면, 규칙을 만들 필요가 없습니다.

>[!NOTE]
>
>컨텐츠 유사성 알고리즘은 항목 간 컴퓨팅 유사성에 임의 샘플링을 사용할 수 있습니다. 따라서 알고리즘 실행 간에 항목 간 유사성 등급이 다를 수 있습니다.

### 포함 규칙 지정 {#inclusion}

![포함 규칙](/help/c-recommendations/c-algorithms/assets/inclusion-rules.png)

여러 가지 옵션을 사용하여 권장 사항에 표시할 항목 범위를 좁힐 수 있습니다. 기준 또는 프로모션을 만들 때 포함 규칙을 사용할 수 있습니다.

포함 규칙은 선택적이지만 이러한 세부 사항을 설정하면 권장 사항에 나타나는 항목을 보다 강력하게 제어할 수 있습니다. 이후 각 세부 사항을 구성하여 표시 기준 범위를 좁힙니다.

예를 들어 재고가 50보다 많고 가격이 $25~$45 범위인 여성 신발만 표시할 것을 선택할 수 있습니다. 또한 각 속성에 가중치를 적용하여 비즈니스에 가장 중요한 항목이 가장 자주 표시되도록 할 수 있습니다.

다른 예로, 특정 도시에서만 사용자의 사이트를 방문하며 필요한 대학 학위가 있는 방문자에게만 구인 정보를 표시하도록 선택할 수 있습니다.

포함 규칙 옵션은 수직 시장에 따라 다릅니다. 기본적으로 포함 규칙은 백업 권장 사항에 적용됩니다.

>[!IMPORTANT]
>
>포함 규칙을 사용할 때는 주의해야 합니다. 이 기능은 조직에서 한 브랜드를 표시하는 동안에 다른 브랜드를 추천해선 안되는 규칙이 있는 경우 유용하지만 그러나 이 기능에는 기회비용이 있습니다. 활동 기준에 의해 정상적으로 항목이 표시될 때 일부 항목이 표시되지 않도록 제한하면 상승도 비율을 놓칠 가능성이 있습니다.

포함 규칙은 AND로 결합됩니다. 권장 사항에 항목을 포함하려면 모든 규칙을 충족해야 합니다.

앞서 언급한 것처럼 재고가 50개가 넘고 가격이 $25에서 $45 범위인 여성화만 표시하도록 단순 포함 규칙을 만들려면 다음 단계를 수행하십시오.

1. 추천할 제품에 대한 가격 범위를 설정합니다.
1. 추천할 제품에 대한 최소 재고량을 설정합니다.
1. 특정 기준을 충족할 때만 항목을 표시하도록 권장 사항을 구성합니다.

   ![](assets/Recs_InclusionRules.png)

   목록의 속성 중 하나가 충족되거나 하나 이상의 지정된 조건과 일치하지 않을 때만 항목이 포함되도록 지정할 수 있습니다.

   사용 가능한 평가기는 첫 번째 드롭다운에서 선택한 값에 따라 다릅니다. 여러 항목을 나열할 수 있습니다. 이러한 항목은 OR로 평가됩니다.

   여러 규칙은 AND로 결합됩니다.

   >[!NOTE]
   >
   >이 선택 사항은 권장 사항에 표시되는 품목을 제한하며, 권장 사항이 어느 페이지에 표시되는지에는 영향을 주지 않습니다. 권장 사항이 표시되는 위치를 제한하려면 경험 작성기에서 페이지를 선택합니다.

For more information, see [Use dynamic and static inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

### 속성 가중치 지정

컨텐츠 카탈로그에 대한 중요한 설명 또는 메타데이터를 기반으로 하는 알고리즘을 &quot;이동&quot;하는 여러 규칙을 추가하여 특정 항목이 더 잘 표시되도록 할 수 있습니다.

예를 들어, 권장 사항에 더 자주 표시되도록 세일 중인 항목에 더 높은 가중치를 적용할 수 있습니다. 판매하지 않는 항목이 완전히 제외되는 것은 아니지만 표시되는 빈도가 줄어듭니다. 여러 가중치가 적용된 속성을 동일한 알고리즘에 적용할 수 있으며 권장 사항에서 분할 트래픽에 대해 가중치가 적용된 속성을 테스트할 수 있습니다.

1. 값을 선택합니다.

   이 값은 사용 가능한 여러 기준 중 하나에 따라 표시될 가능성이 높은 항목의 유형을 결정합니다.

1. 평가자를 선택합니다.

1. 규칙 속성을 완료하기 위한 키워드를 입력합니다.

   예를 들어 전체 규칙은 &quot;카테고리에 하위 문자열 shoes가 포함되어 있습니다.&quot;일 수 있습니다.

   ![](assets/Recs_AttributeWeighting.png)

1. 규칙에 지정할 가중치를 선택합니다.

   옵션은 0 -100 사이이며 25씩 커집니다.

1. 원하는 경우 다른 규칙을 추가합니다.

완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

새 [!UICONTROL 권장 사항] 활동을 만들거나 기존 항목을 편집하는 경우 기본적으로 **[!UICONTROL 나중에 사용하기 위해 기준 저장]** 확인란이 선택됩니다. 다른 활동에서 해당 기준을 사용하지 않으려면 저장하기 전에 이 확인란을 선택 취소합니다.

## 권장 사항 키 {#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B}를 기반으로 권장 사항 만들기

키를 기반으로 하는 권장 사항은 관련 결과를 표시하는 데 방문자 행동 컨텍스트를 활용합니다.

권장 사항 유형에는 다음 두 가지가 있습니다.

* **인기도:**&#x200B;가장 많이 본 항목, 가장 많이 판매된 카테고리 및 상위 지표에 따라 항목을 표시합니다. 인기도 기준의 경우 키가 비어 있습니다.
* **키 기반:**&#x200B;기준의 나머지를 구성합니다. 권장 사항에는 키 유형과 관련된 다양한 선택 옵션이 제공됩니다. &quot;현재 항목&quot;부터 권장할 값의 키를 프로그래밍 방식으로 설정할 수 있는 &quot;프로필 매개 변수&quot;까지 다양한 옵션이 제공됩니다. 각 기준이 다른 키를 기반으로 사용하도록 하여 여러 기준을 서로에 대해 테스트할 수 있습니다.

각 기준은 자체 탭에 정의됩니다. 트래픽은 여러 기준 테스트에 고르게 분할됩니다. 즉, 두 개의 기준이 있으면 트래픽이 이러한 두 기준 간에 동일하게 분할됩니다. 두 개의 기준과 두 개의 디자인이 있는 경우 트래픽이 네 개의 조합 간에 균일하게 분할됩니다. 또한 비교를 위해 기본 콘텐츠를 보는 사이트 방문자의 비율도 지정할 수 있습니다. 그러한 경우, 지정한 비율의 방문자는 기본 콘텐츠를 보고 나머지 방문자는 기준 및 디자인 조합 간에 분할됩니다.

1. 새 권장 사항을 만들거나 기존 권장 사항을 선택하고 **[!UICONTROL 편집]**&#x200B;을 클릭합니다.
1. 권장 사항 키를 변경하려면 [!UICONTROL 권장 사항 키] 드롭다운 목록에서 새 키를 선택한 다음, **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   다른 논리가 다른 권장 사항 키에 매핑되므로 다른 권장 사항이 다른 유형의 페이지에 배치될 수 있습니다. 각 키에 대한 자세한 내용은 다음 섹션을 참조하십시오.

### 현재 항목

권장 사항은 현재 방문자가 보고 있는 항목에 의해 결정됩니다.

권장 사항에는 특정 항목에 관심이 있는 방문자의 흥미를 끌 수 있는 다른 항목이 표시됩니다.

이 옵션을 선택한 경우 디스플레이 mbox에 매개 변수로 `entity.id` 값을 전달해야 합니다.

#### 논리(기준)

* [!UICONTROL 비슷한 속성을 갖는 항목]
* [!UICONTROL 이 항목을 보고 다른 항목도 본 사람]
* [!UICONTROL 이 항목을 보고 다른 항목을 구입한 사람]
* [!UICONTROL 이 항목을 구입하고 다른 항목도 구입한 사람]
* [!UICONTROL 사이트 친화성]

#### 사이트에서 사용할 위치

제품 페이지와 같은 단일 항목 페이지입니다.

null 검색 결과 페이지는 사용하지 마십시오.

### 현재 카테고리

권장 사항은 현재 방문자가 보고 있는 제품 카테고리에 의해 결정됩니다.

권장 사항에는 지정된 제품 카테고리의 항목이 표시됩니다.

이 옵션을 선택한 경우 디스플레이 mbox에 매개 변수로 `entity.categoryId` 값을 전달해야 합니다.

#### 논리(기준)

* 최상위 판매자
* 가장 많이 본 항목

#### 사이트에서 사용할 위치

단일 카테고리 페이지입니다.

null 검색 결과 페이지는 사용하지 마십시오.

### 사용자 지정 속성 {#custom}

권장 사항은 방문자 프로필에 저장된 항목에 따라 결정되며, user.*x* 또는 profile.*x* 속성을 사용합니다.

이 옵션을 선택하는 경우 `entity.id` 값이 프로필 속성에 있어야 합니다.

#### 논리(기준)

* [!UICONTROL 이 항목을 보고 다른 항목도 본 사람]
* [!UICONTROL 이 항목을 보고 다른 항목을 구입한 사람]
* [!UICONTROL 이 항목을 구입하고 다른 항목도 구입한 사람]
* [!UICONTROL 전체 동작]
* [!UICONTROL 가장 많이 본 항목]
* [!UICONTROL 최상위 판매자]

키가 사용자 지정 프로필 속성이고 알고리즘 유형이 가장 많이 본 항목 또는 최상위 판매자인 경우, 알려진 엔티티 속성(ID, 카테고리, 마진, 값, 재고 및 환경 제외) 목록이 있는 &quot;고유값 기준 그룹화&quot;라는 새 드롭다운 목록이 표시됩니다. 이 필드는 필수입니다.

#### 사이트에서 사용할 위치

어떤 페이지에서도 사용 가능합니다.

#### 사용자 지정 권장 사항 키 사용

사용자 지정 프로필 속성값을 기준으로 하여 권장 사항을 만들 수 있습니다. 예를 들어 방문자가 가장 최근에 큐에 추가한 동영상을 기반으로 권장 동영상을 표시하려 한다고 가정합니다.

1. **[!UICONTROL 권장 사항 키]** 드롭다운 목록에서 사용자 지정 프로필 속성을 선택합니다(예를 들어 &quot;Last Show Added to Watchlist&quot;).
1. 그런 다음 **[!UICONTROL 권장 사항 논리]**&#x200B;를 선택합니다(예를 들어 &quot;People Who Viewed This, Viewed That&quot;).

   ![새 기준 만들기 대화 상자](/help/c-recommendations/c-algorithms/assets/create-new-criteria-1.png)

사용자 지정 프로필 속성이 단일 엔티티 ID와 직접 일치하지 않는 경우 엔티티에 대한 일치가 어떻게 일치하는지 [!DNL Recommendations]에 설명해야 합니다. 예를 들어 방문자가 좋아하는 브랜드에서 상위 판매 항목을 표시한다고 가정합니다.

1. **[!UICONTROL 권장 사항 키]** 드롭다운 목록에서 사용자 지정 프로필 속성을 선택합니다(예를 들어 &quot;Favorite Brand&quot;).

1. 그런 다음 이 키와 함께 사용할 **[!UICONTROL 권장 사항 논리]**&#x200B;를 선택합니다(예를 들어 &quot;Top Sellers&quot;).

   [!UICONTROL 다음의 고유한 값으로 그룹화] 옵션이 표시됩니다.

1. 선택한 키와 일치하는 엔티티 속성을 선택합니다. 이 경우 “Favorite Brand”가 `entity.brand`에 일치합니다.

   이제 [!DNL Recommendations]에서 각 브랜드에 대한 “Top Sellers” 목록을 생성하고 방문자의 Favorite Brand 프로필 속성에 저장된 값을 기반으로 적절한 “Top Sellers” 목록을 표시합니다.

   ![새 기준 만들기 대화 상자 2](/help/c-recommendations/c-algorithms/assets/create-new-criteria-2.png)

### 마지막으로 구매한 항목

고유의 각 방문자가 구매한 마지막 항목에 의해 권장 사항이 결정됩니다. 이 항목은 자동으로 캡처되므로 페이지에서 어떠한 값도 전달할 필요가 없습니다.

#### 논리(기준)

* [!UICONTROL 비슷한 속성을 갖는 항목]
* [!UICONTROL 이 항목을 보고 다른 항목도 본 사람]
* [!UICONTROL 이 항목을 보고 다른 항목을 구입한 사람]
* [!UICONTROL 이 항목을 구입하고 다른 항목도 구입한 사람]
* [!UICONTROL 사이트 친화성]

#### 사이트에서 사용할 위치

홈 페이지, 내 계정 페이지, 오프사이트 광고

제품 페이지 또는 구매와 관련된 페이지에서는 사용하지 마십시오.

### 마지막으로 본 항목

고유의 각 방문자가 본 마지막 항목에 의해 권장 사항이 결정됩니다. 이 항목은 자동으로 캡처되므로 페이지에서 어떠한 값도 전달할 필요가 없습니다.

#### 논리(기준)

* [!UICONTROL 비슷한 속성을 갖는 항목]
* [!UICONTROL 이 항목을 보고 다른 항목도 본 사람]
* [!UICONTROL 이 항목을 보고 다른 항목을 구입한 사람]
* [!UICONTROL 이 항목을 구입하고 다른 항목도 구입한 사람]
* [!UICONTROL 사이트 친화성]

#### 사이트에서 사용할 위치

홈 페이지, 내 계정 페이지, 오프사이트 광고

제품 페이지 또는 구매와 관련된 페이지에서는 사용하지 마십시오.

### 가장 많이 본 항목

즐겨찾는 카테고리에 사용된 것과 동일한 방법을 사용하여, 가장 자주 본 항목에 의해 권장 사항이 결정됩니다.

이 항목은 다음과 같이 동작하는 최신/빈도 기준에 의해 결정됩니다.

* 첫 번째 제품 보기에 대해 10포인트
* 모든 후속 보기에 대해 5포인트
* 세션 끝에서 모든 값을 2로 나누기

예를 들어 한 세션에서 surfboardA를 본 다음 surfboardB를 본 경우의 결과는 A: 10, B: 5입니다. 세션이 종료될 때 결과는 A: 5, B: 2.5입니다. 다음 세션에서 동일한 항목을 볼 경우 값은 A: 15 B: 7.5로 변경됩니다.

#### 논리(기준)

* [!UICONTROL 비슷한 속성을 갖는 항목]
* [!UICONTROL 이 항목을 보고 다른 항목도 본 사람]
* [!UICONTROL 이 항목을 보고 다른 항목을 구입한 사람]
* [!UICONTROL 이 항목을 구입하고 다른 항목도 구입한 사람]
* [!UICONTROL 사이트 친화성]

#### 사이트에서 사용할 위치

홈 페이지 또는 랜딩 페이지 및 오프사이트와 같은 일반 페이지.

### 즐겨찾는 카테고리

제품 대신 카테고리 점수가 산정되는 것만 제외하고, &quot;가장 많이 본 항목&quot;에 사용된 것과 동일한 방법을 사용하여, 가장 많은 활동을 받은 카테고리에 의해 권장 사항이 결정됩니다.

이 항목은 다음과 같이 동작하는 최신/빈도 기준에 의해 결정됩니다.

* 첫 번째 카테고리 보기에 대해 10포인트
* 모든 후속 보기에 대해 5포인트

처음으로 방문한 카테고리에는 10포인트가 부여됩니다. 같은 카테고리에 대한 후속 방문에는 5포인트가 부여됩니다. 각 방문에서 이전에 본 비현재 카테고리는 1포인트씩 감소됩니다.

예를 들어 한 세션에서 categoryA를 본 다음 categoryB를 본 경우의 결과는 A: 9, B: 10입니다. 다음 세션에서 동일한 항목을 보는 경우 값은 A: 20 B: 9로 변경됩니다.

#### 논리(기준)

* [!UICONTROL 최상위 판매자]
* [!UICONTROL 가장 많이 본 항목]

#### 사이트에서 사용할 위치

홈 페이지 또는 랜딩 페이지 및 오프사이트와 같은 일반 페이지.

### 인기도

사이트에서의 항목의 인기도에 의해 권장 사항이 결정됩니다. 인기도에는 최상위 판매자와 mbox 데이터별 가장 많이 본 항목이 포함되며 Adobe Analytics를 사용하는 경우 제품 보고서에서 사용할 수 있는 모든 지표가 포함됩니다. 항목은 선택한 권장 사항 논리에 따라 등급이 매겨집니다.

#### 논리(기준)

* [!UICONTROL 최상위 판매자]
* [!UICONTROL 가장 많이 본 항목]
* 제품 보고서 지표(Adobe Analytics를 사용하는 경우)

#### 사이트에서 사용할 위치

홈 페이지 또는 랜딩 페이지 및 오프사이트와 같은 일반 페이지.

### 최근에 본 항목 {#recently-viewed}

방문자의 기록(여러 세션)을 사용하여 디자인의 슬롯 수에 따라 방문자가 마지막으로 본 *x*&#x200B;개 항목을 표시합니다.

이제 최근에 본 항목 기준이 주어진 [환경](/help/administrating-target/hosts.md)에 따른 결과를 반환합니다. 방문자가 서로 다른 환경에 속한 두 사이트 간에 전환하는 경우 각 사이트에는 해당 사이트에서 최근에 본 항목만 표시됩니다. 방문자가 동일한 환경에 속한 두 사이트 간에 전환하는 경우 방문자에게 두 사이트에서 최근에 본 동일한 항목이 표시됩니다.

#### 사이트에서 사용할 위치

홈 페이지 또는 랜딩 페이지 및 오프사이트와 같은 일반 페이지.

>[!NOTE]
>
>최근에 본 항목은 활동에 대한 제외 전역 설정과 선택한 컬렉션 설정을 모두 준수합니다. 항목이 전역 제외에 의해 제외되거나 선택한 컬렉션에 포함되지 않은 경우 표시되지 않습니다. 따라서 최근에 본 항목 기준을 사용할 때는 일반적으로 &quot;모든 컬렉션&quot; 설정을 사용해야 합니다.

## Training video: Create criteria in Recommendations (12:33) ![Tutorial badge](/help/assets/tutorial.png)

이 비디오에는 다음 정보가 포함됩니다.

* 기준 만들기
* 기준 시퀀스 만들기
* 사용자 지정 기준 업로드

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
