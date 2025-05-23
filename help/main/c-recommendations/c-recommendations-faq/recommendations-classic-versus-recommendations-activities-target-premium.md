---
keywords: 권장 사항, 권장 사항 알고리즘, 권장 사항 활동, recommendations classic
description: 정보를 검토하면,  [!DNL Target]  Premium의 기존 Recommendations Classic과 Recommendations 활동의 차이점을 이해하는 데 도움이 됩니다.
title: ' [!DNL Target]  Premium에서 Recommendations Classic과 Recommendations 간의 차이점은 무엇입니까?'
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 07548155-9548-4870-b886-6cb4ff37a0bd
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 88%

---

# Recommendations Classic과 Recommendations 활동 비교: [!DNL Target] Premium

권장 사항 Classic과 Target Premium의 권장 사항 활동 중에 선택하는 데 도움이 되는 정보.

>[!NOTE]
>
>권장 사항 활동은 [!DNL Target Premium] 솔루션의 일부로 사용할 수 있습니다. 이 기능은 [!DNL Target Standard] 라이선스가 없는 [!DNL Target Premium] 에서는 사용할 수 없습니다.

클래식 [!DNL Recommendations] 제품에서, 권장 사항은 페이지에 데이터 컬렉션 mbox를 만든 다음 특정 페이지 위치에 디스플레이 mbox를 추가하여 표시했습니다. . [!DNL Recommendations] 활동( [!DNL Target Premium] )은 제품이나 콘텐츠를 추천하려는 각 위치에 대해 mbox를 만들지 않아도 페이지의 어디에서든 방문자 정보를 수집하고 권장 사항을 만들 수 있도록 해 줍니다. 페이지 헤더에 있는 단순 JavaScript 참조는 페이지의 어디에서나 권장 사항 기능을 사용할 수 있습니다. 이 JavaScript 참조를 사용하여 [!DNL Target] 및 `entity.id` 키와 같은 글로벌 `entity.categoryId` mbox에 키를 전달하십시오.

[!DNL Recommendations Classic] 은 [!DNL Experience Cloud] UI에서 자체 카드로 표시됩니다. [!DNL Recommendations] 활동은 [!DNL Target Premium] 워크플로에서 사용할 수 있습니다.

[!DNL Recommendations Classic] 사용자는 [!DNL Target Recommendations]에서 [!DNL Recommendations] mbox를 계속 사용할 수 있습니다. 또한 mbox를 유지하고 헤더에서 JavaScript 코드를 사용하여 이전의 접근 방식과 [!DNL Target] 접근 방식을 조합함으로써 페이지의 다른 요소에 대해 [!DNL Recommendations] 기능을 활성화할 수도 있습니다. 그러나 전체 [!DNL Target] 기능을 이용하려면 [!DNL Recommendations Classic] 사용자의 경우 이전 mbox를 삭제하고 [!DNL Target Recommendations]에만 의존하는 것이 좋을 수 있습니다.

[!DNL Target] 의 [!DNL Recommendations] 활동은 다음 기본 영역에서 [!DNL Recommendations Classic] 보다 개선되어 있습니다.

## 오퍼로서의 Recommendations

[!UICONTROL A/B Test] ([!UICONTROL Auto-Allocate] 및 [!UICONTROL Auto-Target] 포함)와 [!UICONTROL Experience Targeting] (XT) 활동 내에 권장 사항을 포함할 수 있습니다.

이 기능은 다음과 같이 완전히 새로운 기능을 사용할 수 있도록 해 줍니다.

* 동일한 활동에서 권장 사항 및 비권장 사항 콘텐츠를 테스트하고 타기팅할 수 있습니다.
* 권장 사항들의 순서를 포함하여 페이지에서의 권장 사항 배치를 쉽게 실험할 수 있습니다.
* [!UICONTROL Auto-Allocate]을(를) 사용하여 트래픽을 가장 성과가 가장 좋은 권장 사항 경험에 자동으로 푸시합니다.
* [!UICONTROL Auto-Target]을(를) 사용하여 방문자를 프로필에 따라 맞춤 권장 사항 경험에 동적으로 지정할 수 있습니다.

시작하려면 [!UICONTROL Visual Experience Composer]을(를) 사용하여 [!UICONTROL A/B Test] 또는 [!UICONTROL Experience Targeting] 활동을 만들고 [!UICONTROL Insert Before], [!UICONTROL Insert After] 또는 [!UICONTROL Replace With] 작업을 사용하여 권장 사항을 경험에 추가하십시오.

자세한 내용은 [오퍼로서의 Recommendations](/help/main/c-recommendations/recommendations-as-an-offer.md)를 참조하십시오.

## 기준 {#section_117709846DAA404580EBE879FFCBD9BA}

[!DNL Target Recommendations] 는 사전 패키징된 규칙 및 구성 세트가 들어 있는 기준 라이브러리를 포함합니다. [!DNL Recommendations Classic]에서 각 권장 사항은 양식에 입력하고 큰 규칙 목록에서 선택하여 수동으로 빌드되었습니다. 이제 [!DNL Recommendations] 활동을 작성할 때에는 사전 구성된 기준 세트를 선택하면 됩니다. 여전히 사용자 지정 권장 사항을 만들 수 있지만, 기준 라이브러리에는 프로세스를 단순화하도록 사전 빌드되어 있고 사용자가 이해하는 언어를 사용하는 가장 공통적인 구성들이 많이 포함되어 있습니다. 이렇게 사전 패키징된 기준은 그대로 사용하거나, 복사하여 특정 요구에 맞게 편집할 수 있습니다.

![overview_criteria 이미지](assets/overview_criteria.png)

기준은 업계 카테고리, 페이지 유형 및 구현 별로 사전 구성 및 정렬됩니다. 예를 들어 제품 페이지에서 사용할 목적으로 소매 범주에 적용되는 기준을 찾아 특정 범주( `entity.categoryID` 매개 변수로 정의되는 범주) 내의 제품을 표시할 수 있습니다.

기준 사용 및 작성에 대한 자세한 내용은 [기준](/help/main/c-recommendations/c-algorithms/algorithms.md)을 참조하십시오.

## 워크플로 {#section_76B4A26297BF422382DE2C79A2713D3C}

[!DNL Recommendations] 워크플로가 단순해졌습니다. 복잡한 양식을 채우는 대신 다음 작업을 수행하는 시각적 워크플로를 수행합니다.

1. 기준을 선택합니다.
1. 미리 구성된 [디자인](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14)을(를) 선택하십시오.
1. 결과 권장 사항을 미리 봅니다.

## 시각적 미리보기 {#section_639B9E38C9EC4093BF9023EE0F2A15AC}

페이지에서 권장 사항을 만들고, 테스트하지 않아도 권장 사항을 설정하고 필요한 변경 작업을 수행한 후 권장 사항을 미리 볼 수 있습니다. 미리보기는 [!DNL Target] 내에서 사용할 수 있습니다.

## 타겟 지정 {#section_93295EA0DBA14210B8518AF4802A459F}

[!DNL Recommendations Classic]에는 6개의 타기팅 선택 사항이 있었습니다. 권장 사항 활동은 Target의 전체 타기팅 선택 사항을 사용합니다. [!DNL Target] 또는 기타 [!DNL Adobe Experience Cloud] 대상자(예: [!DNL Audience Manager] 및 [!DNL Analytics])를 사용하여 대상자를 정의한 다음, 각 디자인을 보게 되는 활동 참여자의 백분율과 통제군을 보게 되는 백분율을 선택하십시오.

![overview_targeting 이미지](assets/overview_targeting.png)

## 보고 {#section_25C2FCCE4BC1488496C517C0470B5CD6}

[!DNL Target]의 [!DNL Recommendations] 에서는 [!DNL Target] 및 [!DNL Experience Cloud]가 제공하는 기능을 활용하는 향상된 보고 기능을 제공합니다. 따라서 이러한 기능을 활용하지 않고 결과와 비교하여 [!DNL Recommendations] 로 제공된 상승도를 단순히 표시하는 대신 [!DNL Recommendations] 활동에 대한 전체 정보를 볼 수 있습니다.

![개요_보고서 이미지](assets/overview_report.png)
