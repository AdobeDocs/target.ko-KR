---
keywords: 권장 사항;설정;이름;목표;우선순위;지속 기간;보고 설정;기타 메타데이터
description: Adobe Target에서 권장 사항 활동을 설명하고 제어하는 데 사용되는 설정을 구성하는 방법에 대해 알아봅니다.
title: 권장 사항 활동 설정을 구성하는 방법
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=ko#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
TQID: 'https://experienceleague.adobe.com/pfMAvl6MmLCtH3PZfOR4Ve-WFIc3e2iN2Bh-cIzjeC0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 13%
---
# 권장 사항 활동 설정 {#recs-activity-settings}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Adobe Target]에서 [!DNL Recommendations] 활동을 설명하고 제어하는 설정에 대해 알아봅니다.

>[!ENDSHADEBOX]

활동 설정은 [!DNL Recommendations] 활동을 식별하고, 활동 표시 시기와 위치를 제어하고, 결과를 보고하는 방법을 정의합니다.

## 이름

추가 작업 아이콘(![추가 작업 아이콘](/help/main/assets/icons/MoreSmallListVert.svg))을 클릭한 다음 **[!UICONTROL 이름 바꾸기]**&#x200B;를 클릭하여 활동을 식별하는 데 도움이 되는 수사적 이름을 지정합니다.

`/`, `?`, `#`, `:`, `=`, `+`, `-` 및 `@` 문자는 활동 이름에 사용할 수 없습니다.

[!UICONTROL Recommendations Classic]의 다른 활동에 대해 [!DNL Recommendations] 활동의 이름이 이미 있는 경우 새 활동이 새 이름으로 다시 동기화됩니다. 새 이름은 고유한 이름을 만들기 위해 타임스탬프가 추가된 원래 이름입니다. [!DNL Target Standard/Premium]과(와) [!UICONTROL Recommendations Classic]에 모두 표시됩니다.

## 목표

(선택 사항) 활동의 목표를 설명합니다.

## 우선순위

슬라이더를 조정하여 우선 순위 수준을 설정합니다.

대상이 같은 동일한 위치에 여러 개의 활동이 지정될 때 우선순위가 사용됩니다. 위치에 둘 이상의 활동이 지정되는 경우 우선순위가 가장 높은 활동이 표시됩니다.

## 지속 시간

활동의 지속 기간을 설정하십시오.

활동은 활성화될 때 또는 특정 날짜 및 시간에 시작할 수 있습니다. 마찬가지로 비활성화될 때 또는 특정 날짜 및 시간에 종료될 수 있습니다.

시간 선택기는 24시간 형식을 사용하며 00:00은 자정을 나타냅니다. 시간대는 브라우저에서 구성된 시간대입니다. 다른 시간대를 사용하려면 브라우저를 해당 시간대로 설정하고 브라우저를 다시 시작합니다.

## 보고 설정

다음 설정은 활동 결과를 보고하는 방법을 정의합니다.

* **[!UICONTROL 보고 Source]:** 데이터를 수집하는 솔루션을 지정합니다. [!DNL Adobe Target], [!DNL Adobe Analytics] 또는 [!DNL Adobe Customer Journey Analytics].

  [계정 설정](/help/main/administrating-target/reporting.md)에 보고 솔루션을 지정한 경우 해당 솔루션이 사용되며 이 설정은 표시되지 않습니다. 보고서 일관성을 유지하기 위해 활동이 활성 상태가 되면 보고 소스를 변경할 수 없습니다.

  **[!DNL Adobe Analytics]**: 보고 솔루션과 각 솔루션의 이점 간의 차이점에 대해서는 [[!DNL Adobe Analytics] 의 보고 소스로 [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md)를 참조하십시오. [!DNL Analytics] 보고서 세트 및 추적 서버를 선택하려면 [Source 보고](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reporting-source)를 참조하십시오.

  **[!DNL Adobe Customer Journey Analytics]**: [!DNL Adobe Customer Journey Analytics]과(와) [!DNL Target] 간의 통합에 대한 자세한 내용은 [[!DNL Target] 보고 위치 [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md)를 참조하십시오.

* **[!UICONTROL 목표 지표]:** 활동이 성공적인지를 결정하는 성공 지표를 선택합니다.
* **[!UICONTROL 추가 지표]:** 보고서에 대한 추가 성공 지표를 구성합니다.
* **[!UICONTROL 보고할 대상]:** 보고서를 필터링하는 데 사용할 수 있는 대상을 정의합니다.

## 기타 메타데이터

활동에 대한 메모를 입력합니다.

## 교육 비디오: 활동 설정(3:02) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오는 다음 활동 설정을 다룹니다.

* 활동의 목표를 입력합니다.
* 활동의 우선 순위 수준을 설정합니다.
* 시작 및 종료 시간을 예약합니다.
* 보고서 필터를 만들려면 보고 대상을 추가하십시오.
* 활동에 대한 메모를 입력합니다.

>[!VIDEO](https://video.tv.adobe.com/v/17381)
