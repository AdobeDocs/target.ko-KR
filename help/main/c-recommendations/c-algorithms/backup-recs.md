---
keywords: 권장 사항;백업;백업
description: Adobe에서 백업 권장 사항을 사용하는 방법 알아보기 [!DNL Target] Recommendations. 권장 항목이 충분하지 않은 권장 사항에는 백업 알고리즘의 결과가 표시됩니다.
title: Recommendations에서 백업 권장 사항을 사용하려면 어떻게 해야 합니까?
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 82%

---

# ![PREMIUM](/help/main/assets/premium.png) 백업 권장 사항 사용

Adobe Target에서 백업 권장 사항 기능을 사용하는 경우, 권장 항목이 충분하지 않은 권장 사항에는 기본 콘텐츠가 표시되지 않습니다. 대신 권장 사항이 백업 알고리즘의 결과를 표시합니다.

백업 권장 사항을 사용하지 않을 경우 권장 사항에 디스플레이를 채우기에 충분한 항목이 없으면 시스템은 사용자에게 기본 컨텐츠를 표시합니다.

>[!NOTE]
>
>추가 정보는 [기준 만들기 의 컨텐츠 섹션](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) 항목(사용 시 관찰할 결과를 설명하는 매트릭스 포함) [!UICONTROL 부분 디자인 렌더링] 및 [!UICONTROL 백업 Recommendations 표시] 옵션을 함께 사용하거나 개별적으로 선택할 수 있습니다.

백업 권장 사항 기능은 항상 사이트에서 가장 많이 본 항목을 사용하여 알고리즘의 데이터가 사용된 후 나머지 슬롯을 채웁니다. 예를 들어, 템플릿이 권장된 5개 항목을 표시하도록 구성되었고 *구매 친화성* 알고리즘을 사용하고 있지만 데이터가 5개 슬롯 중 2개만 채울 수 있는 경우 백업 권장 사항 기능은 가장 많이 본 항목으로 다른 세 개의 슬롯을 채웁니다.

백업 권장 사항은 전체 사이트에서 가장 많이 본 상위 500개 제품에서 임의로 선택됩니다. 백업 권장 사항의 데이터 기간은 일주일입니다.

가장 많이 본 500개의 결과가 순차적으로 정렬된 다음, 20개의 버킷으로 분할됩니다. 버킷은 순서대로 제공되지만 각 버킷 내의 결과는 순서가 무작위로 지정되어 페이지에 반환됩니다. 사용자가 페이지를 새로 고치면 새롭고 순서가 무작위로 지정된 결과가 표시됩니다. 컬렉션과 필터링 규칙의 결합에서 비롯된 결과 세트가 20보다 작으면 컬렉션에서 무작위로 선택됩니다.

이 버킷 지정 프로세스는 백업 권장 사항이 다음 순서로 표시됨을 의미합니다.

1. 가장 많이 본 20개의 항목이 순서가 무작위로 지정되어 표시된 다음,
1. 다음으로 가장 많이 본 20개의 항목이 순서가 무작위로 지정되어 표시된 다음,
1. 다음으로 가장 많이 본 20개의 항목이 순서가 무작위로 지정되어 표시된 다음,
1. 등등

백업 권장 사항의 버킷이 지정되지 않으면, 499번째로 가장 많이 본 항목이 표시되고 그 다음에 200번째로 가장 많이 본 항목이, 그 다음에 380번째로 가장 많이 본 항목이 표시되는 식으로 계속 표시될 수 있습니다. 버킷 지정 프로세스가 있으면 가장 많이 본 항목이 먼저 추천됩니다.

>[!NOTE]
>
>항목을 카탈로그에 그룹화할 경우 권장 사항 내 각 알고리즘에 대해 생성된 백업 권장 사항도 해당 카탈로그를 사용하므로 카탈로그에 있는 항목만 백업 권장 사항에 포함됩니다.

글로벌 제외 규칙으로 제외된 모든 항목은 백업 권장 사항으로 사용되지 않습니다.

백업 권장 사항은 기본적으로 활성화되고 사이트에서 가장 인기 있는 항목을 임의 선택하여 템플릿의 추가 슬롯을 채웁니다.

권장 사항 배치에서 중복은 제거됩니다.

일반적으로 백업 권장 사항의 사용은 초기 설정 중 구현 팀과 논의하는 과정의 일부입니다. 구현 후 백업 권장 사항 설정을 변경하려면 계정 관리자에게 문의하십시오.

부분 디자인 렌더링 사용( [컨텐츠 설정](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) 참조)이 사용되도록 설정되어 있지 않고 템플릿이 표시되지 않으면 대신 백업 권장 사항이나 기본 컨텐츠가 표시됩니다.