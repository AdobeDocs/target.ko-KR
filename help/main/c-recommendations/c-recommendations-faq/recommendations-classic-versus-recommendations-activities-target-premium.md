---
keywords: 권장 사항, 권장 사항 알고리즘, 권장 사항 활동, recommendations classic
description: 정보를 검토하면 [!DNL Target] Premium의 기존 Recommendations Classic과 Recommendations 활동의 차이점을 이해하는 데 도움이 됩니다.
title: '[!DNL Target] Premium에서 Recommendations Classic과 Recommendations 간의 차이점은 무엇입니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 07548155-9548-4870-b886-6cb4ff37a0bd
TQID: 'https://experienceleague.adobe.com/EoTkyY0kOwRKT52WIwOuTCoUziIJOnNtTo6llsTNpsM'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 19%
---
# 권장 사항 Classic과 [!DNL Target] Premium의 권장 사항 활동 비교 {#classic-versus-activities}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Recommendations Classic]이(가) [!DNL Target Premium]의 [!DNL Recommendations] 활동과 어떻게 다른지 알아보고 둘 중 하나를 선택하세요.

>[!ENDSHADEBOX]

>[!NOTE]
>
>[!DNL Recommendations] 활동은 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Standard] 라이선스가 없는 [!DNL Target Premium] 에서는 사용할 수 없습니다.

클래식 [!DNL Recommendations] 제품에서, 권장 사항은 페이지에 데이터 컬렉션 mbox를 만든 다음 특정 페이지 위치에 디스플레이 mbox를 추가하여 표시했습니다. [!DNL Target Premium]의 [!DNL Recommendations] 활동은 제품 또는 콘텐츠를 권장하는 각 위치에 대해 mbox 없이 페이지의 어디에서든 방문자 정보를 수집하고 권장 사항을 만듭니다. 페이지 헤더의 JavaScript 참조는 페이지의 어디에서나 권장 사항을 사용할 수 있습니다. 이 참조는 `entity.id` 및 `entity.categoryId` 키와 같은 키를 전역 [!DNL Target] mbox에 전달합니다.

[!DNL Recommendations Classic] 은 [!DNL Experience Cloud] UI에서 자체 카드로 표시됩니다. [!DNL Recommendations] 활동은 [!DNL Target Premium] 워크플로에서 사용할 수 있습니다.

[!DNL Recommendations Classic] 사용자는 [!DNL Target Recommendations]에서 [!DNL Recommendations] mbox를 계속 사용할 수 있습니다. mbox를 유지하고 헤더에서 JavaScript 코드를 사용하여 페이지의 다른 요소에 대해 [!DNL Recommendations] 기능을 활성화하여 클래식 및 [!DNL Target] 접근 방식을 결합할 수도 있습니다. 그러나 전체 [!DNL Target] 기능을 사용하려면 [!DNL Recommendations Classic] 사용자가 이전 mbox를 삭제하고 [!DNL Target Recommendations]에만 의존하는 것이 좋을 수 있습니다.

[!DNL Target]의 [!DNL Recommendations] 활동이 다음 기본 영역의 [!DNL Recommendations Classic]에서 개선됩니다.

## 오퍼로서의 추천 {#recs-as-offer}

권장 사항은 [!UICONTROL A/B 테스트]&#x200B;([!UICONTROL 자동 할당] 및 [!UICONTROL 자동 타겟] 포함)와 [!UICONTROL 경험 타깃팅]&#x200B;(XT) 활동 내에 포함될 수 있습니다. 이를 통해 여러 기능 중에서 동일한 활동 내에서 권장 사항 및 비권장 사항 콘텐츠를 테스트하고 타깃팅할 수 있습니다. 자세한 내용은 [오퍼로서의 추천](/help/main/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오.

## 기준 {#criteria-comparison}

[!DNL Target Recommendations]에는 사전 패키징된 규칙 및 구성 집합이 있는 기준 라이브러리가 포함되어 있습니다. [!DNL Recommendations Classic]에서 각 권장 사항은 양식에 입력하고 큰 규칙 목록에서 선택하여 수동으로 빌드되었습니다. [!DNL Recommendations] 활동이 만들어지면 미리 구성된 기준 집합이 선택됩니다. 사용자 지정 권장 사항을 만들 수는 있지만 기준 라이브러리에는 프로세스를 단순화하고 사람들이 이해하는 언어를 사용하도록 사전 빌드된 가장 일반적인 구성이 많이 포함되어 있습니다. 미리 패키지된 기준은 있는 그대로 사용하거나 특정 요구 사항에 맞게 복사 및 편집할 수 있습니다.

![사람들이 이해하는 언어, 규칙 및 논리, 구성 레이블이 지정된 기준 카드, 상향 판매를 보여주는 슬라이드](assets/overview_criteria.png)

기준은 업계 카테고리, 페이지 유형 및 구현 별로 사전 구성 및 정렬됩니다. 예를 들어, 소매 범주에 적용되는 기준은 제품 페이지에서 사용할 수 있도록 찾을 수 있으며, 특정 범주(`entity.categoryID` 매개 변수로 정의되는 범주) 내의 제품을 표시합니다.

기준 사용 및 작성에 대한 자세한 내용은 [기준](/help/main/c-recommendations/c-algorithms/algorithms.md)을 참조하십시오.

## 워크플로 {#workflow-comparison}

[!DNL Recommendations] 워크플로가 단순해졌습니다. 복잡한 양식 대신 시각적 워크플로우는 다음 단계를 안내합니다.

1. 기준을 선택합니다.
1. 미리 구성된 [디자인](/help/main/c-recommendations/c-design-overview/create-design.md#create-design)을(를) 선택하십시오.
1. 결과 권장 사항을 미리 봅니다.

## 시각적 미리보기 {#visual-preview}

권장 사항은 설정된 후 미리 볼 수 있으며, 페이지에서 권장 사항을 만든 다음 테스트하지 않고 필요한 사항을 변경할 수 있습니다. 미리보기는 [!DNL Target] 내에서 사용할 수 있습니다.

## 타겟 지정 {#targeting-comparison}

[!DNL Recommendations Classic]에 6개의 타깃팅 옵션이 있습니다. [!DNL Recommendations] 활동에서 [!DNL Target] 타깃팅 옵션의 전체 범위를 사용합니다. 대상은 [!DNL Target] 또는 다른 [!DNL Adobe Experience Cloud] 대상(예: [!DNL Audience Manager] 및 [!DNL Analytics])을 사용하여 정의됩니다. 그러면 각 디자인을 보게 되는 활동 참여자의 백분율과 통제군을 보게 되는 백분율이 선택됩니다.

![모든 방문자 대상, 상향 판매 기준, 각각 트래픽의 30%를 갖는 디자인 3개 및 권장 사항 없음 컨트롤 그룹이 포함된 흐름 다이어그램](assets/overview_targeting.png)

## 보고 {#reporting-comparison}

[!DNL Target]에서 [!DNL Recommendations]은(는) [!DNL Target] 및 [!DNL Experience Cloud]의 기능을 활용하는 향상된 보고 기능을 제공합니다. [!DNL Recommendations]이(가) 제공하지 않은 결과와 비교하여 제공하는 상승도만 표시하는 대신 보고서에는 [!DNL Recommendations] 활동에 대한 전체 정보가 표시됩니다.

