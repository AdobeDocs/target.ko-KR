---
keywords: 추천;오퍼
description: A/B 테스트(자동 할당 및 자동 타겟 포함) 및 경험 타깃팅(XT) 활동에서 오퍼로서 Adobe 추천를 사용하는 방법에 대해 알아봅니다.
title: 다른 활동 유형에서 추천를 제안으로 사용하는 방법은 무엇입니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: f6034e83564a9a386e21e4e57279c66cc3c94537
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 42%

---

# 오퍼로서의 추천

이제 [!UICONTROL A/B 테스트]&#x200B;([!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟] 포함)와 [!UICONTROL 경험 타깃팅]&#x200B;(XT) 활동 내에 권장 사항을 포함할 수 있습니다.

이 기능은 다음과 같이 완전히 새로운 기능을 사용할 수 있도록 해 줍니다.

* 동일한 활동에서 권장 사항 및 비권장 사항 콘텐츠를 테스트하고 타기팅할 수 있습니다.
* 여러 권장 사항의 순서를 포함하여 페이지의 권장 사항 배치를 쉽게 실험할 수 있습니다.
* [!UICONTROL 자동 할당]을 사용하여 트래픽을 가장 성과가 가장 좋은 권장 사항 경험에 자동으로 푸시합니다.
* [!UICONTROL 자동 타겟]을(를) 사용하여 방문자를 프로필에 따라 맞춤 권장 사항 경험에 동적으로 지정할 수 있습니다.

시작하려면 [!UICONTROL 시각적 경험 작성기]를 사용하여 [!UICONTROL A/B 테스트] 또는 [!UICONTROL 경험 타깃팅] 활동을 만들고 [!UICONTROL 권장] 작업을 사용하여 권장 사항을 경험에 추가하십시오.

## A/B 테스트 또는 XT 활동에서 오퍼로서 권장 사항 추가

1. 시각적 경험 작성기(VEC)를 사용하여 안내가 있는 3단계 워크플로를 시작하여 [A/B 테스트](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) 또는 [경험 타깃팅](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT) 활동을 만듭니다.

   >[!NOTE]
   >
   >A/B 테스트의 경우 [자동 할당](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) 선택 사항을 선택하여 트래픽을 가장 성과가 좋은 권장 사항에 자동 푸시하거나 [자동 타겟](/help/main/c-activities/auto-target/auto-target-to-optimize.md) 선택 사항을 선택하여 방문자를 해당 프로필에 따라 맞춤 권장 사항 경험에 할당할 수 있습니다.

1. [경험](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)을 만드는 동안 권장 사항을 오퍼로 추가할 요소를 클릭하고 **[!UICONTROL 콘텐츠 바꾸기]**(![콘텐츠 바꾸기 아이콘](/help/main/assets/icons/Switch.svg))을 클릭한 다음 **[!UICONTROL 권장 사항]**&#x200B;을 선택합니다.

   ![오퍼로서 권장 사항 삽입](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

1. 오른쪽의 [!UICONTROL 권장 사항] 레일에서 **[!UICONTROL 권장 사항 선택]**&#x200B;을 클릭하여 [!UICONTROL 기준 선택] 대화 상자를 표시합니다.

1. **[!UICONTROL 기준 만들기]**&#x200B;를 클릭하거나 기존 기준을 선택하십시오.

1. (선택 사항) **[!UICONTROL 필터]** 아이콘( ![필터 아이콘](/help/main/assets/icons/Filter.svg))을 클릭하여 페이지 유형별로 인기 있는 권장 사항 기준을 보려면 다음 옵션 중에서 선택합니다.

   * 장바구니 페이지
   * 카테고리 페이지
   * 홈 페이지
   * 랜딩 페이지
   * 제품 페이지
   * 검색 결과 페이지
   * 감사 페이지
   * 기타

1. **[!UICONTROL 기준 만들기]**&#x200B;를 클릭하거나 기존 [기준](/help/main/c-recommendations/c-algorithms/algorithms.md)을 선택한 후 **[!UICONTROL 다음]**&#x200B;을 클릭하여 [!UICONTROL 디자인 선택] 대화 상자를 표시합니다.

1. **[!UICONTROL 디자인 만들기]**&#x200B;를 클릭하거나 기존 [디자인](/help/main/c-recommendations/c-design-overview/design-overview.md)을 선택한 후 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

1. [!UICONTROL 옵션] 대화 상자에서 다음을 지정합니다.

   * [컬렉션](/help/main/c-recommendations/c-products/collections.md)을 선택합니다.
   * 필요에 따라 [전면 프로모션 및 후면 프로모션](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md) 선택 사항을 구성합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
1. 안내가 있는 3가지 부분 워크플로를 사용하여 A/B 테스트 또는 XT 활동 구성을 완료합니다.

## 권장 사항 오퍼의 구성 편집

1. [!UICONTROL 권장 사항] 레일에서 [!UICONTROL 기준 이름], [!UICONTROL 디자인 이름] 또는 [!UICONTROL 컬렉션 이름] 옆에 있는 **[!UICONTROL 편집]** 아이콘(![편집 아이콘](/help/main/assets/icons/Edit.svg) )을 클릭하여 요소를 변경합니다.

## 권장 사항 오퍼 삭제

1. [!UICONTROL 권장 사항] 패널 위쪽에 있는 **[!UICONTROL 삭제]** 아이콘( ![삭제 아이콘](/help/main/assets/icons/Delete.svg))을 클릭합니다.

### 권장 사항 오퍼 상태 보기 {#status}

권장 사항 오퍼(알고리즘) 상태는 권장 사항 오퍼가 포함된 A/B 테스트 및 XT 활동에 대한 활동의 [!UICONTROL 개요] 페이지 하단에 표시됩니다.

* 결과 준비
* 결과가 준비되지 않음
* 피드 실패
