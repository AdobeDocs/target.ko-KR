---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
description: 권장 사항을 사용자 지정하려면 CSV 파일을 업로드합니다.
title: 사용자 지정 기준 업로드
feature: criteria
uuid: e0b4d320-db00-43ad-b49e-ce36c8532320
translation-type: tm+mt
source-git-commit: 66b3c42181daf582c9b3bee1f83a2229b823c5c3
workflow-type: tm+mt
source-wordcount: '1873'
ht-degree: 66%

---


# ![PREMIUM](/help/assets/premium.png) 사용자 지정 기준 업로드{#upload-custom-criteria}

권장 사항을 사용자 지정하려면 CSV 파일을 업로드합니다.

## 새 기준 만들기 화면에 액세스

[!UICONTROL 새 기준 만들기] 화면에 도달하는 여러 방법이 있습니다. 일부 화면 옵션은 화면에 도달하는 방법에 따라 달라집니다.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. 여기서 만드는 기준은 자동으로 모든 [!DNL Recommendations] 활동에 사용 가능해집니다.
* VEC( [!DNL Recommendations] Visual Experience Composer [!UICONTROL )를 사용하여] 활동을 하는 경우, 사용자는 페이지에서 요소 선택 [!UICONTROL 후 즉시] 기준 [!UICONTROL 선택]으로 선택한 후 [!UICONTROL , Click]Creating Recommendations/ Town을 클릭한 다음 , RecommendationsInsert, Town 또는 Insert After Creating Recommendations으로 이동합니다. 그런 다음 사용 가능한 기준을 선택하거나 기준 **[!UICONTROL 만들기를 클릭할 수 있습니다]**. 새 기준을 만드는 경우 다른 [!DNL Recommendations] 활동과 함께 사용할 기준을 저장할 수 있습니다. For more information, see [Create a Recommendations activity](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* [!DNL Recommendations] 활동을 편집하는 경우 페이지에서 [!UICONTROL 권장 사항 위치] 상자를 클릭하고 **[!UICONTROL 기준 변경]**&#x200B;을 선택합니다. On the [!UICONTROL Select Criteria] screen, click **[!UICONTROL Create Criteria]**. 다른 [!DNL Recommendations] 활동과 함께 사용할 새 기준을 저장하는 선택 사항이 있습니다.

다음 단계에서는 첫 번째 방법을 사용하여 새 기준 [!UICONTROL 만들기] 화면에 액세스한다고 가정합니다.[ **[!UICONTROL Recommendations]** ] > [ **[!UICONTROL 기준]** 라이브러리] 화면

1. Recommendations **[!UICONTROL >]** 기준을 클릭합니다 ****.

1. 기준 **[!UICONTROL 만들기]** > 사용자 지정 기준 **[!UICONTROL 업로드를 클릭합니다]**.

1. 다음 섹션에서 정보를 구성합니다.

## 기본 정보 {#info}

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

   키를 기반으로 기준을 지정하는 방법에 대한 자세한 내용은 [권장 사항 키를 기반으로 권장 사항 만들기](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md)를 참조하십시오.

1. **[!UICONTROL 권장 사항 논리]**&#x200B;를 선택합니다.

   권장 사항 논리 선택 사항에 대한 자세한 내용은 [기준](../../c-recommendations/c-algorithms/algorithms.md)을 참조하십시오.

   >[!NOTE]
   >
   >If you select **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]**, you will have the option to set [content similarity rules](#similarity).

## 콘텐츠 {#content}

Content rules determine what happens if the number of recommended items does not fill your [recommendations design](/help/c-recommendations/c-design-overview/design-overview.md). It is possible for [!DNL Recommendations] criteria to return fewer recommendations than your design calls for. 예를 들어 디자인에 네 개의 항목에 대한 슬롯이 있지만 기준에 따라 두 개의 항목만 권장되는 경우 나머지 슬롯을 비워 두거나 백업 권장 사항을 사용하여 추가 슬롯을 채울 수 있습니다.

![컨텐츠 섹션](/help/c-recommendations/c-algorithms/assets/content.png)

1. (선택 사항) **[!UICONTROL 부분 디자인 렌더링]** 전환 효과를 &quot;설정&quot; 위치로 밀면

   가능한 한 많은 슬롯이 채워지지만 디자인 템플릿에는 나머지 슬롯의 빈 공간이 포함될 수 있습니다. 이 옵션을 비활성화하고 사용 가능한 슬롯을 모두 채울 콘텐트가 충분하지 않으면 권장 사항이 제공되지 않고 기본 컨텐츠가 대신 표시됩니다.

   빈 슬롯에 권장 사항을 제공하려는 경우 이 옵션을 활성화합니다. 다음 단계의 설명에 따라 사이트의 유사한 컨텐츠나 인기 있는 컨텐츠가 들어 있는 빈 슬롯이 있는 사용자 기준에 따라 권장 사항 슬롯을 컨텐츠로 채우려면 백업 권장 사항을 사용합니다.

1. (선택 사항) [백업 **[!UICONTROL 표시] Recommendations]** 전환을 &quot;켜기&quot; 위치로 밀십시오.

   사이트에서 가장 많이 본 제품을 임의 선택하여 디자인에 남아 있는 빈 슬롯을 채웁니다.

   백업 권장 사항을 사용하면 권장 사항 디자인이 사용 가능한 모든 슬롯을 채우게 됩니다. 아래 그림과 같이 4 x 1 디자인을 가지고 있다고 가정합니다.

   ![4 x 1 디자인](/help/c-recommendations/c-design-overview/assets/velocity_example.png)

   기준에 따라 두 개의 항목만 권장된다고 가정합니다. [ [!UICONTROL 부분 디자인 렌더링] ] 옵션을 활성화하면 첫 번째 두 슬롯이 채워지지만 나머지 두 슬롯은 비어 있습니다. 그러나 [백업 Recommendations [!UICONTROL 표시] ] 옵션을 활성화하면 처음 두 슬롯이 지정된 기준에 따라 채워지고 나머지 두 슬롯은 백업 권장 사항에 따라 채워집니다.

   다음 매트릭스는 [!UICONTROL 부분 디자인 렌더링] 및 [!UICONTROL 백업 Recommendations] 옵션을 사용할 때 표시되는 결과를 보여줍니다.

   | 부분 디자인 렌더링 | 백업 Recommendations | 결과 |
   |--- |--- |--- |
   | 비활성화됨 | 비활성화됨 | 디자인이 요구하는 곳보다 더 적은 수의 권장 사항이 반환되면 권장 사항 디자인은 기본 콘텐츠로 대체되고 추가 권장 사항은 표시되지 않습니다. |
   | 활성화됨 | 비활성화됨 | 디자인이 렌더링되지만 디자인 요구하는 것보다 더 적은 수의 권장 사항이 반환되면 빈 공백이 포함될 수 있습니다. |
   | 활성화됨 | 활성화됨 | 백업 권장 사항은 사용 가능한 디자인 &quot;슬롯&quot;을 채우고 디자인을 완전히 렌더링합니다.<br>백업 권장 사항에 포함 규칙을 적용하여 적격의 백업 권장 사항 수를 디자인을 채울 수 없는 지점까지 제한하면 디자인이 부분적으로 렌더링됩니다.<br>이 조건에 따라 어떤 권장 사항도 반환되지 않고 포함 규칙이 백업 권장 사항 수를 0으로 제한하면 디자인이 기본 콘텐츠로 바뀝니다. |
   | 비활성화됨 | 활성화됨 | 백업 권장 사항은 사용 가능한 디자인 &quot;슬롯&quot;을 채우고 디자인을 완전히 렌더링합니다.<br>백업 권장 사항에 포함 규칙을 적용하여 적격의 백업 권장 사항 수를 디자인을 채울 수 없는 지점까지 제한하면 디자인이 기본 콘텐츠로 바뀌고 권장 사항은 표시되지 않습니다. |

   자세한 내용은 백업 권장 [사항 사용을 참조하십시오](/help/c-recommendations/c-algorithms/backup-recs.md).

1. (조건부) 이전 단계에서 **[!UICONTROL 백업 Recommendations]** 표시를 선택한 경우 백업 권장 사항에 **[!UICONTROL 포함 규칙 적용을 활성화할 수 있습니다]**.

   포함 규칙은 권장 사항에 포함되는 항목을 결정합니다. 사용 가능한 옵션은 수직 시장에 따라 다릅니다.

   자세한 내용은 [아래에서 포함 규칙을](#inclusion) 지정합니다.

1. (선택 사항) 이전에 구입한 항목 **[!UICONTROL 권장]** 사항을 &quot;설정&quot; 위치로 끕니다.

   이 설정은 `productPurchasedId`를 기준으로 합니다. 기본 동작은 이전에 구입한 항목을 추천하지 않는 것입니다. 대부분의 경우 고객이 최근에 구입한 항목을 홍보하지 않습니다. 카약처럼 일반적으로 한 번만 구매하는 항목을 판매하는 경우에 유용합니다. 샴푸나 다른 개인 품목과 같이 사람들이 다시 구입하기 위해 다시 오는 품목을 판매하면 이 옵션을 사용하도록 설정해야 합니다.

## 포함 규칙{#inclusion}을 참조하십시오 

여러 가지 옵션을 사용하여 권장 사항에 표시할 항목 범위를 좁힐 수 있습니다. 기준 또는 프로모션을 만들 때 포함 규칙을 사용할 수 있습니다.

![포함 규칙](/help/c-recommendations/c-algorithms/assets/inclusion-rules.png)

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

## CSV 업로드

1. **[!UICONTROL CSV 파일의 위치]**&#x200B;를 선택합니다.

   ![CSV 섹션 업로드](/help/c-recommendations/c-algorithms/assets/upload-csv.png)

   CSV 파일을 성공적으로 업로드하려면 형식이 올바르게 지정되어야 합니다. **[!UICONTROL CSV 템플릿 다운로드]**&#x200B;를 클릭하여 올바른 형식의 CSV 파일을 가져옵니다.

   다음 두 가지 위치 옵션이 있습니다.

   * **FTP:** FTP 서버에서 CSV 파일을 업로드하려면 **[!UICONTROL FTP]**&#x200B;를 선택한 다음, 필요한 정보를 입력합니다. SSL을 사용하기 위한 옵션이 제공됩니다. 이 옵션은 FTPS 프로토콜을 사용하여 CSV 파일을 안전하게 전송합니다.
   * **URL:** URL에서 CSV 파일을 업로드하려면 **[!UICONTROL URL을]**&#x200B;선택한 다음 피드 URL을 입력합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >사용자 지정 기준 엔티티(행)에는 최대 1,000개의 권장 항목(열)이 포함될 수 있습니다.

사용자 지정 기준 업데이트는 기본적으로 &quot;누적&quot;입니다. CSV 업로드 파일에 지정된 새 키-값 쌍이 기존 키-값 쌍을 덮어씁니다. CSV 업로드에 지정된 키가 없는 기존 키-값 쌍은 계속 제공할 수 있으며, CSV 파일의 일부로 마지막으로 업로드한 뒤 31일 후에 만료됩니다.

Client Care에 문의하여 다음 CSV 업로드에 포함되지 않은 기존 결과를 삭제하도록 설정을 활성화합니다. 이 설정을 활성화하면 사용자 지정 CSV 피드 파일에 있는 키만 전달할 수 있습니다. 이 설정은 모든 사용자 지정 기준에 적용됩니다.

사용자 지정 기준 피드는 24시간마다 한 번씩 업데이트됩니다.

권장 사항 > 기준 페이지에서 각 기준 카드의 맨 아래에 있는 사용자 지정 기준 업로드의 업로드 및 동기화 상태를 확인할 수 있습니다. 사용자 지정 기준을 편집할 때 편집 대화 상자에서 상태를 볼 수도 있습니다.

오류가 없는 업로드에 대한 흐름은 예약됨 > 피드 파일 다운로드 >가져오기 > 성공입니다.

The following are possible error messages you might receive if [!DNL Target] encounters a problem with the upload:

| 오류 메시지 | 세부 사항 |
|--- |--- |
| 알 수 없는 오류 | 내부 기술 오류를 나타냅니다. |
| 구문 분석 오류 | 피드 파일 형식에 문제가 있을 수 있습니다. 파일 형식을 수정하고 알고리즘을 다시 저장하여 파일 다운로드 프로세스를 다시 시작합니다. |
| 서버를 찾을 수 없음 | 인터넷에 표시되는 IP 또는 호스트 이름을 제공하십시오. |
| 자격 증명 오류 | 서버의 활성 계정에 대한 유효한 사용자 및 암호를 제공합니다. |
| 디렉토리를 찾을 수 없음 | 서버에 존재하는 디렉토리를 지정합니다. |
| 파일을 찾을 수 없음 | 표시된 디렉토리의 서버에 있는 파일의 이름을 제공합니다. |

## 교육 비디오: 추천에서 기준 만들기(12:33) ![자습서 배지](/help/assets/tutorial.png)

이 비디오에는 다음 정보가 포함되어 있습니다(사용자 지정 기준 업로드에 대한 세부 사항은 11:43부터 시작).

* 기준 만들기
* 기준 시퀀스 만들기
* 사용자 지정 기준 업로드

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)