---
keywords: 다중 페이지;여정 테스트;다중 페이지 활동
description: Adobe Target에서 여러 페이지 활동을 만드는 방법을 살펴보고 각 페이지에 맞는 디자인을 사용하여 여러 페이지에 걸쳐 스토리를 만들 수 있습니다.
title: 여러 페이지 활동을 만들려면 어떻게 합니까?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 85%

---


# 다중 페이지 활동

[!DNL Adobe Target]의 여러 페이지 활동을 사용하면 각 페이지에 맞는 디자인을 사용하여 여러 페이지에 걸쳐 스토리를 만들 수 있습니다.

예를 들어, 특정 금액을 초과하는 구매 항목을 무료로 배송하는 오퍼를 테스트할 수 있습니다. 해당 페이지가 랜딩 페이지, 카테고리 페이지 및 특정 제품 페이지에 나타나되, 각 페이지 유형에서 다른 위치에 다른 크기로 표시되도록 할 수 있습니다. 홈페이지에 눈에 띄는 오퍼를 표시한 다음, 다른 관련 페이지에서 더 작은 오퍼로 해당 오퍼를 보강할 수도 있습니다.

다중 페이지 활동을 사용하여 데스크톱 사이트와 비응답형 모바일 사이트용으로 서로 다른 레이아웃을 정의할 수도 있습니다. 사이트에 [!DNL m.mysite.com] 대신 [!DNL `www.mysite.com`]과 같은 별도의 모바일 사이트가 있는 경우 대신 [다중 페이지 활동](/help/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48)을 만들고 [!DNL m.mysite.com]을 별도의 페이지로 추가한 다음, 모바일 편집을 적용하여 동일한 경험에서 데스크탑 버전과 모바일 버전을 적절하게 변경해야 합니다. 응답형 모바일 사이트의 경우 [모바일 경험 편집](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md#concept_8E45527C4ABC41D59AA3553BEDC76FA5)을 사용하십시오.

>[!NOTE]
>
>다중 페이지 활동은 동일한 오퍼가 여러 페이지에서 다른 모양을 갖는 활동용으로 디자인되었습니다. 오퍼가 모든 페이지에 동일하게 표시된다면 [템플릿 테스트](/help/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781)가 더 효율적입니다.

다중 페이지 테스트의 각 페이지에 대해 템플릿 규칙을 지정할 수 있습니다. 예를 들어, 다중 페이지 테스트의 카테고리 페이지에 템플릿 규칙을 적용하여 홈페이지와 모든 카테고리 페이지에서 다중 페이지 테스트를 실행할 수 있습니다. 활동에서 지리 기반의 타깃팅을 사용하는 방법에 대한 자세한 내용은 [유사한 페이지에 동일한 경험 포함](/help/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781).

테스트에 페이지를 추가하려면 다음을 수행하십시오.

1. **[!UICONTROL 구성]** 톱니바퀴 아이콘을 클릭합니다.
1. **[!UICONTROL 추가 페이지 추가를 클릭합니다]**.

   화면 왼쪽에 탐색 막대가 나타납니다.

   ![](assets/multipage_nav.png)

1. 탐색 막대를 사용하여 페이지를 지정하고 기본 페이지를 설정합니다.

   **[!UICONTROL 페이지 추가]**&#x200B;를 클릭하여 페이지를 더 추가합니다.

   작업 메뉴를 표시하려면 세 개의 수직 줄임표 아이콘을 클릭하십시오.

   ![](assets/multipage_menu.png)

   이 메뉴를 사용하여 페이지의 이름을 바꾸거나, 다중 페이지 활동 내에서 리디렉션 테스트를 수행하거나, 페이지를 삭제하십시오.

1. 시각적 경험 작성기를 사용하여 각 페이지에서 오퍼가 표시되는 방식을 디자인합니다.

