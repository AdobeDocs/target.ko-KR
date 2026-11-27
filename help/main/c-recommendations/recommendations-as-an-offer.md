---
keywords: 추천;오퍼
description: A/B 테스트(자동 할당 및 자동 타겟 포함) 및 경험 타깃팅(XT) 활동에서 오퍼로서 Adobe 추천를 사용하는 방법에 대해 알아봅니다.
title: 다른 활동 유형에서 추천를 제안으로 사용하는 방법은 무엇입니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: ec520555-b439-46a9-ab2d-f0981532bffb
TQID: 'https://experienceleague.adobe.com/ZMOb5RdY6bES331INSM7VF-w4be-5Xmjqon0YvfuNG4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 12%
---
# 오퍼로서의 추천 {#recommendations-as-an-offer}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!UICONTROL A/B 테스트] 및 [!UICONTROL 경험 타깃팅]&#x200B;(XT) 활동에서 오퍼로서 권장 사항을 추가, 편집 및 삭제하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

[!UICONTROL 권장 사항] 활동 외에 권장 사항은 [!UICONTROL A/B 테스트]&#x200B;([!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟] 포함) 및 [!UICONTROL 경험 타깃팅]&#x200B;(XT) 활동 내에 포함될 수 있습니다. 이렇게 하면 다음 작업을 수행할 수 있습니다.

* 동일한 활동에서 권장 사항 및 비권장 사항 콘텐츠를 테스트하고 타기팅할 수 있습니다.
* 여러 권장 사항의 순서를 포함하여 페이지의 권장 사항 배치를 테스트합니다.
* **[!UICONTROL 자동 할당]**&#x200B;을 사용하여 트래픽을 가장 성과가 가장 좋은 권장 사항 경험에 자동 푸시합니다.
* **[!UICONTROL 자동 타겟]**&#x200B;을(를) 사용하여 방문자를 프로필에 따라 맞춤 권장 사항 경험에 동적으로 지정할 수 있습니다.

## 오퍼로서 권장 사항 추가 {#add-recs-offer}

[!UICONTROL A/B 테스트] 또는 XT 활동에서 [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)를 사용하여 경험을 만드는 동안 권장 사항이 오퍼로 추가됩니다.

1. VEC의 안내가 있는 3단계 워크플로우를 시작하여 [A/B 테스트](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) 또는 [경험 타깃팅](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)(XT) 활동을 만듭니다.

   >[!NOTE]
   >
   >A/B 테스트의 경우 [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) 옵션은 트래픽을 가장 성과가 좋은 권장 사항으로 자동 푸시하고 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md) 옵션은 방문자를 해당 프로필에 따라 맞춤 권장 사항 경험에 할당합니다.

1. [경험](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)을(를) 만드는 동안 다음 방법 중 하나로 권장 사항을 오퍼로 추가하십시오.

   * 권장 사항이 추가되는 요소를 클릭하고 **[!UICONTROL 콘텐츠 바꾸기]**&#x200B;를 클릭한 다음, **[!UICONTROL 권장 사항]**&#x200B;을 선택합니다.

     ![HTML 오퍼 및 경험 조각 옵션 옆에 있는 메뉴에서 머리글이 선택되고 권장 사항 옵션이 강조 표시된 시각적 경험 작성기](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

   * **[!UICONTROL 구성 요소]** 레일에서 **[!UICONTROL 동적]** 아래의 **[!UICONTROL 권장 사항]**&#x200B;을 선택하고 페이지의 기존 요소를 마우스로 가리킨 다음 **[!UICONTROL 다음 항목 앞에 삽입]** 또는 **[!UICONTROL 다음 항목 뒤에 삽입]**&#x200B;을 클릭하여 해당 요소 앞 또는 뒤에 권장 사항을 배치합니다.

1. **[!UICONTROL 속성 표시]** 메뉴에 액세스하고 **[!UICONTROL 권장 사항 선택]**&#x200B;을 클릭합니다.

1. 원하는 [기준](/help/main/c-recommendations/c-algorithms/algorithms.md)을 선택한 후 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

1. 원하는 [디자인](/help/main/c-recommendations/c-design-overview/design-overview.md)을 선택한 후 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 옵션]** 대화 상자에서 다음을 지정합니다.

   * [컬렉션](/help/main/c-recommendations/c-products/collections.md)을 선택합니다.
   * 필요한 경우 [전면 프로모션 및 후면 프로모션](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md) 옵션을 구성합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

1. 안내가 있는 3단계 워크플로우로 [!UICONTROL A/B 테스트] 또는 XT 활동 구성을 완료합니다.

## 권장 사항 오퍼 편집 {#edit-recs-offer}

**[!UICONTROL 권장 사항]** 창에서 오퍼를 추가한 후 권장 사항 오퍼의 기준, 디자인, 컬렉션 및 프로모션을 변경할 수 있습니다.

1. 오른쪽 창 메뉴의 옵션을 편집하고 찾아보려면 오퍼를 클릭하십시오.

   ![선택한 오퍼의 기준, 디자인, 컬렉션 이름 및 프로모션 추가 단추가 있는 추천 창](assets/create_reco_7.png)

1. 다음 옵션 중 하나를 선택합니다.

   * [기준 변경](/help/main/c-recommendations/c-algorithms/algorithms.md)
   * [디자인 변경](/help/main/c-recommendations/c-design-overview/design-overview.md)
   * [컬렉션 변경](/help/main/c-recommendations/c-products/collections.md)
   * [프로모션 변경](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. 편집합니다.

## 권장 사항 오퍼 삭제 {#delete-recs-offer}

더 이상 필요하지 않은 권장 사항 오퍼는 **[!UICONTROL 권장 사항]** 창에서 삭제할 수 있습니다.

제거할 오퍼를 클릭한 다음 **[!UICONTROL 권장 사항]** 창에서 bin 아이콘(![Bin 아이콘](assets/Smock_Delete_18_N.svg) )을 클릭합니다.

![bin 아이콘이 강조 표시된 추천 창](assets/create_reco_8.png)

## 권장 사항 오퍼의 상태 보기 {#status}

권장 사항 오퍼(알고리즘)의 상태는 권장 사항 오퍼가 포함된 [!UICONTROL A/B 테스트] 및 XT 활동에 대한 **[!UICONTROL 개요]** 페이지 하단에 표시됩니다. 상태는 다음 중 하나입니다.

* **[!UICONTROL 결과 준비]**
* **[!UICONTROL 결과가 준비되지 않음]**
* **[!UICONTROL 피드 실패]**

## 교육 비디오: 오퍼로서의 추천 ![개요 배지](/help/main/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)
