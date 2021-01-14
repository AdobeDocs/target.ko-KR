---
keywords: Recommendations;offer
description: A/B 테스트(자동 할당 및 자동 타겟 포함) 및 경험 타깃팅(XT) 활동에서 오퍼로서 Adobe Recommendations
title: A/B 테스트(자동 할당 및 자동 타겟 포함) 및 경험 타깃팅(XT) 활동에서 오퍼로서 Adobe Recommendations
feature: Recommendations
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 98%

---


# ![PREMIUM](/help/assets/premium.png) 오퍼로서의 Recommendations

이제 [!UICONTROL A/B 테스트] ([!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟] 포함)와 [!UICONTROL 경험 타깃팅] (XT) 활동 내에 권장 사항을 포함할 수 있습니다.

이 기능은 다음과 같이 완전히 새로운 기능을 사용할 수 있도록 해줍니다.

* 동일한 활동에서 권장 사항 및 비권장 사항 콘텐츠를 테스트하고 타깃팅할 수 있습니다.
* 권장 사항들의 순서를 포함하여 페이지에서의 권장 사항 배치를 쉽게 실험할 수 있습니다.
* [!UICONTROL 자동 할당]을 사용하여 트래픽을 가장 성과가 가장 좋은 권장 사항 경험에 자동 푸시할 수 있습니다.
* [!UICONTROL 자동 타겟]을 사용하여 방문자를 프로필에 따라 맞춤 권장 사항 경험에 동적으로 지정할 수 있습니다.

시작하려면 [!UICONTROL 시각적 경험 작성기]를 사용하여 [!UICONTROL A/B 테스트] 또는 [!UICONTROL 경험 타깃팅] 활동을 만들고, [!UICONTROL 다음 항목 앞에 삽입], [!UICONTROL 다음 항목 뒤에 삽입] 또는 [!UICONTROL 다음으로 바꾸기] 작업을 사용하여 권장 사항을 경험에 추가하십시오.

## A/B 테스트 또는 XT 활동에서 오퍼로서 권장 사항 추가

1. 시각적 경험 작성기(VEC)를 사용하여 안내가 있는 3단계 워크플로우를 시작하여 [A/B 테스트](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) 또는 [경험 타깃팅](/help/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT) 활동을 만듭니다.

   >[!NOTE]
   >
   >A/B 테스트의 경우 [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) 선택 사항을 선택하여 트래픽을 가장 성과가 좋은 권장 사항에 자동 푸시하거나 [자동 타겟](/help/c-activities/auto-target/auto-target-to-optimize.md) 선택 사항을 선택하여 방문자를 해당 프로필에 따라 맞춤 권장 사항 경험에 할당할 수 있습니다.

1. [경험](/help/c-experiences/c-visual-experience-composer/viztarget-options.md)을 만드는 동안 권장 사항을 오퍼로 추가할 요소를 클릭하고 **[!UICONTROL 다음 항목 앞에 삽입]**, **[!UICONTROL 다음 항목 뒤에 삽입]** 또는 **[!UICONTROL 다음으로 바꾸기]** 작업을 선택한 다음, [!UICONTROL 권장 사항]을 선택합니다.

   다음 그림은 [!UICONTROL 다음 항목 뒤에 삽입 > 권장 사항] 선택 사항을 보여줍니다.

   ![오퍼로서 권장 사항 삽입](/help/c-recommendations/assets/replace-after-recommendations.png)

1. 다음 선택 사항 중에서 선택하여 페이지 유형별로 인기 있는 권장 사항 기준을 확인합니다.

   * 장바구니 페이지
   * 카테고리 페이지
   * 홈 페이지
   * 랜딩 페이지
   * 제품 페이지
   * 검색 결과 페이지
   * 감사 페이지
   * 기타

1. 원하는 [기준](/help/c-recommendations/c-algorithms/algorithms.md)을 선택하고 [!UICONTROL 다음]을 클릭합니다.
1. 원하는 [디자인](/help/c-recommendations/c-design-overview/design-overview.md)을 선택하고 [!UICONTROL 다음]을 클릭합니다.
1. [!UICONTROL 선택 사항] 대화 상자에서 다음을 지정합니다.

   * [컬렉션](/help/c-recommendations/c-products/collections.md)을 선택합니다.
   * 필요에 따라 [전면 프로모션 및 후면 프로모션](/help/c-recommendations/t-create-recs-activity/adding-promotions.md) 선택 사항을 구성합니다.

1. [!UICONTROL 저장]을 클릭합니다.
1. 안내가 있는 3가지 부분 워크플로우를 사용하여 A/B 테스트 또는 XT 활동 구성을 완료합니다.

## 권장 사항 오퍼의 구성 편집

오퍼의 구성을 편집할 수 있는 방법에는 두 가지가 있습니다.

* [!UICONTROL 편집] 메뉴 사용
* [!UICONTROL 수정 사항] 패널 사용

### 편집 메뉴를 사용하여 권장 사항 오퍼 편집

1. 편집할 오퍼를 클릭한 다음, **[!UICONTROL 편집]**&#x200B;을 클릭합니다.

   ![추천 오퍼 편집](/help/c-recommendations/assets/recs-offer-edit.png)

1. 다음 선택 사항 중 하나를 선택합니다.

   * [기준 변경](/help/c-recommendations/c-algorithms/algorithms.md)
   * [디자인 변경](/help/c-recommendations/c-design-overview/design-overview.md)
   * [컬렉션 변경](/help/c-recommendations/c-products/collections.md)
   * [프로모션 변경](/help/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. 편집합니다.

### 수정 사항 패널을 사용하여 권장 사항 오퍼 편집

1. [!UICONTROL 수정 사항] 아이콘 **(`</>`)**&#x200B;을 클릭하여 [수정 사항](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) 창을 표시합니다.
1. 원하는 작업을 마우스로 가리킨 다음, **[!UICONTROL 편집]** 아이콘을 클릭합니다.

   ![수정 사항 패널](/help/c-recommendations/assets/recs-offer-modifications.png)

1. 편집합니다.

## 권장 사항 오퍼 삭제

권장 사항 오퍼를 삭제하는 방법에는 두 가지가 있습니다.

* [!UICONTROL 편집] 메뉴 사용
* [!UICONTROL 수정 사항] 패널 사용

### 편집 메뉴를 사용하여 권장 사항 오퍼 삭제

1. 제거할 오퍼를 클릭한 다음, **[!UICONTROL 레이아웃 > 제거]**&#x200B;를 클릭합니다.

   ![제거](/help/c-recommendations/assets/recs-offer-remove.png)

### 수정 사항 패널을 사용하여 권장 사항 오퍼 삭제

1. [!UICONTROL 수정 사항] 아이콘 **( &lt;/> )**&#x200B;을 클릭하여 [수정 사항](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) 창을 표시합니다.
1. 원하는 작업을 마우스로 가리킨 다음, [!UICONTROL 삭제] 아이콘을 클릭합니다.

   ![삭제 아이콘](/help/c-recommendations/assets/recs-offer-delete.png)

### 수정 오퍼 상태 보기 {#status}

수정 오퍼의 (알고리즘) 상태는 추천 오퍼가 포함된 A/B 테스트 및 XT 활동에 대한 [!UICONTROL 개요] 페이지 하단에 표시됩니다.

* 결과 준비
* 결과가 준비되지 않음
* 피드 실패

![추천 오퍼 상태](/help/c-recommendations/assets/recs-offer-status.png)

## 교육 비디오:Recommendations을 오퍼 ![개요 배지](/help/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)