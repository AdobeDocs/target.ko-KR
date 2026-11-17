---
keywords: 여러 대상자;경험 버전;target 경험 버전
description: A/B 활동에서 동일한 경험의 버전으로 다른 대상 세그먼트를 타깃팅하는 방법을 알아봅니다.
title: A/B 활동에서 여러 경험 버전을 사용할 수 있습니까?
feature: A/B Tests
exl-id: 7afe36f0-ec46-4d63-bfff-45d2c8923a04
TQID: 'https://experienceleague.adobe.com/FleyH-u5cWI5vku9E4-RMWeIc95WgPy-VQ-eytxka18'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4876228feee28031373f7e0abe62a66b05b15274
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 8%
---
# A/B 테스트의 여러 경험 대상자 {#multiple-experience-audiences}

>[!BEGINSHADEBOX]

**이 페이지에서:** A/B 활동에서 동일한 경험의 버전으로 다른 대상을 타깃팅하는 방법을 알아봅니다. 사용 사례에서 따라야 할 단계 및 모범 사례를 확인할 수 있습니다.

>[!ENDSHADEBOX]

[!DNL Adobe Target] A/B 활동에서 동일한 경험의 버전을 다른 대상자에게 타깃팅할 수 있습니다. **[!UICONTROL 시각적 경험 작성기]**(VEC) 또는 양식 기반 경험 작성기에서 경험에 대한 여러 대상을 설정할 수 있습니다.

버전에 관계없이 경험에 대한 데이터가 수집되므로 보고서는 각 버전이 아닌 경험의 성능을 보여줍니다. 방문자는 프로필이 변경될 때 경험 대상 간에 전환할 수도 있습니다. 활동 기간 동안 동일한 경험에 머무르지 않습니다.

## 사용 사례 {#use-case}

다음 두 가지 경험을 테스트하고 있습니다.

* 지리 기반의 타깃팅 배너

* 일반 배너.

각 지역에 대한 배너는 달라야 하지만 테스트의 목표는 지역 타깃팅이 일반 콘텐츠보다 더 잘 수행되는지 여부를 결정하는 것입니다.

각 위치에 대해 별도의 경험을 설정하는 경우 각 지역이 다른 지역과 비교하여 수행되는 방식을 측정합니다. 일반 배너와 비교할 때 지리 기반의 타깃팅이 성공 목표를 충족하는 데 도움이 되는지 여부는 측정하지 않습니다.

이 경우 지리 기반의 타깃팅되지 않은 컨트롤에 대해 지리 기반의 타깃팅된 경험을 테스트할 수 있도록 경험의 지리 기반의 버전이 필요합니다.

지역별 버전을 설정하려면 다음을 수행하십시오.

1. [평소대로 A/B 활동을 만듭니다.](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)

   여러 버전이 있는 경험을 구성할 때에는 다음 단계에 설명된 대로 각 버전의 대상을 선택합니다.

1. 경험을 선택한 다음 **[!UICONTROL 구성]** > **[!UICONTROL 여러 대상]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 경험 대상]** 창에서 **[!UICONTROL 대상 추가]** 아이콘(![추가 아이콘](/help/main/assets/icons/Add.svg))을 클릭한 다음 타깃팅할 첫 번째 대상을 선택합니다. 각 대상자에 대해 이 작업을 반복합니다.

   대상이 아직 없으면 [대상을 만들고](/help/main/c-target/c-audiences/create-audience.md)설정합니다.

1. 활동을 계속 설정합니다.

## 모범 사례 {#best-practices}

* 함께 수행할 수 없는 대상을 선택하십시오. 방문자가 둘 이상의 대상에 적격인 경우, 이러한 모든 대상에 대한 콘텐츠가 반환되고 마지막에 나열된 대상의 콘텐츠가 페이지에 표시됩니다. 이는 VEC에서 만들어진 활동에 적용됩니다.
* 다이어그램에 정의된 활동 시작 대상은 AND 조건을 사용하여 경험 대상과 결합됩니다. 활동을 입력하려면 방문자가 활동 대상 및 경험 대상 중 하나에 대한 자격이 있어야 합니다.
* 보고서에 대해 세그먼트와 동일한 대상을 추가합니다. 이렇게 하면 &quot;browser lang ja_JP&quot;에 대해서만 경험 A와 B의 상위 수준 및 경험 A와 B의 하위 수준에서 테스트 결과를 볼 수 있습니다. 이 기능은 [!DNL Target] 기반 보고서에만 작동하며 [!DNL Analytics] 기반 보고서에는 작동하지 않습니다.
