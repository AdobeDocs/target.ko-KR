---
keywords: 권장 사항;백업;백업
description: Adobe [!DNL Target Recommendations]에서 백업 권장 사항을 사용하는 방법을 알아봅니다.
title: 백업 권장 사항 사용
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
TQID: 'https://experienceleague.adobe.com/TziWJoAuEdCqa7uMTpX0O0InnlnjtbPXP-0wzQ-FCM0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 18%
---
# 백업 권장 사항 사용 {#backup-recommendations}

>[!BEGINSHADEBOX]

**이 페이지에서:** 백업 권장 사항이 [!DNL Adobe Target Recommendations]의 나머지 디자인 슬롯을 채우는 방법을 알아봅니다.

>[!ENDSHADEBOX]

권장 사항에 디자인을 채울 권장 항목이 부족한 경우 [!DNL Adobe Target]의 백업 권장 사항 기능은 기본 콘텐츠 대신 백업 알고리즘의 결과를 표시합니다. 백업 권장 사항이 없으면 기본 컨텐츠가 사용자에게 표시됩니다.

>[!NOTE]
>
>**[!UICONTROL 부분 디자인 렌더링]** 및 **[!UICONTROL 백업 콘텐츠 표시]** 옵션을 함께 사용하거나 따로 사용한 결과를 설명하는 매트릭스를 포함하여 자세한 내용은 [기준 만들기](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)의 백업 콘텐츠 섹션을 참조하십시오.

백업 권장 사항 기능은 항상 알고리즘 데이터가 사용된 후 사이트에서 가장 많이 본 항목을 사용하여 나머지 슬롯을 채웁니다. 예를 들어, 5개의 권장 항목을 표시하도록 설계가 구성되었지만, 알고리즘에는 5개의 슬롯 중 2개만 채우기에 충분한 데이터가 있습니다. 그런 다음 백업 권장 사항 기능은 다른 세 슬롯을 위에서 본 항목으로 채웁니다.

백업 권장 사항은 전체 사이트에서 가장 많이 본 상위 500개 제품에서 임의로 선택됩니다. 백업 권장 사항의 데이터 기간은 일주일입니다.

가장 많이 본 500개의 결과가 순차적으로 정렬된 다음, 20개의 버킷으로 분할됩니다. 버킷은 순서대로 제공되지만 각 버킷 내의 결과는 무작위화되어 페이지에 반환되므로 페이지를 새로 고치는 사용자는 무작위화된 새로운 결과를 제공합니다. 컬렉션과 필터링 규칙의 결합 결과 집합이 20개보다 작은 경우 컬렉션에서 항목이 임의로 선택됩니다.

이 버킷 지정 프로세스는 백업 권장 사항이 다음 순서로 표시됨을 의미합니다.

1. 가장 많이 본 20개 항목, 임의 지정.
1. 다음으로 가장 많이 본 항목 20개(임의).
1. 다음으로 가장 많이 본 항목 20개, 임의 지정 등입니다.

버킷이 없으면 가장 많이 본 항목 499번째, 가장 많이 본 항목 200번째, 가장 많이 본 항목 380번째 등이 표시될 수 있습니다. 버킷팅을 수행하면 가장 많이 본 항목이 먼저 추천됩니다.

항목을 컬렉션으로 그룹화할 경우 각 기준에 대해 생성된 백업 권장 사항도 컬렉션을 사용하므로 해당 컬렉션의 항목만 백업 권장 사항에 포함됩니다. 글로벌 제외 규칙으로 제외된 모든 항목은 백업 권장 사항으로 사용되지 않습니다. 권장 사항 배치에서 중복은 제거됩니다.

백업 권장 사항은 기본적으로 활성화되고 사이트의 가장 인기 있는 항목을 임의로 선택하여 디자인의 추가 슬롯을 채웁니다.

백업 권장 사항 사용은 일반적으로 초기 설정 시 구현 팀과 논의의 일부입니다. 구현 후 백업 권장 사항 설정을 변경하려면 계정 관리자에게 문의하십시오.

**[!UICONTROL 부분 디자인 렌더링]**([백업 콘텐츠](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) 참조)이 사용되지 않고 디자인을 채울 수 없는 경우 백업 권장 사항(활성화된 경우) 또는 기본 콘텐츠가 대신 표시됩니다.
