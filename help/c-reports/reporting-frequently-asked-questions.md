---
description: Target의 보고에 대한 FAQ 목록
keywords: 문제 해결;지표 불일치;FAQ;보고서
seo-description: Adobe Target에서 보고하기에 대한 FAQ 목록입니다.
seo-title: Adobe Target에 대한 FAQ 보고
solution: Target
title: 보고 FAQ
topic: Standard
uuid: 0be40d3f-3274-493d-899b-cb7bb3612baf
translation-type: tm+mt
source-git-commit: a6f2eceaddf67653b36a1687ba071f7226169516

---


# 보고 FAQ{#reporting-faq}

[!DNL Target]의 보고에 대한 FAQ 목록

## [!UICONTROL 내 경험 타깃팅] (XT) 보고서에 제어 경험에 대한 지표가 포함되는 이유는 무엇입니까?

XT 활동에는 항상 제어 경험이 있어야 합니다. If you are using an XT activity in a similar manner to an [!UICONTROL A/B Test] activity, which is a fairly common scenario, the control experience data is useful. 보고서에서 유용하지 않은 경우 제어 경험 데이터를 무시할 수 있습니다.

## Why are the number of visits lower in [!DNL Target] than in other [!DNL Adobe Experience Cloud] solutions? {#section_7E626FDB417E41B8B58BBF30FB207409}

예를 들어 [!DNL Target]에 의해 보고된 방문 횟수와 같은 지표 수치는 다음과 같은 여러 가지 이유로 다른 [!DNL Experience Cloud] 솔루션에서 보고된 수치보다 항상 낮습니다.

* [!DNL Target]은 활동에 대해 자격이 되는 방문자에 대해서만 방문을 카운트하고, 다른 솔루션에서는 방문자를 페이지로 유도한 활동과 관계없이 페이지를 표시하는 방문자에 대한 방문을 카운트합니다.
* 동일한 위치에 대해 서로 다른 활동이 경쟁하는 경우가 있을 수 있습니다 (상호 배타적). 그 결과, 방문자는 웹 페이지에 있는 [!DNL Target]에서 보고하는 지표 수치에 영향을 주는 다른 컨텐츠를 보게 됩니다.

## 내 활동의 보고서에 사용할 수 있는 데이터가 없는 이유는 무엇입니까? {#section_E4722F6445884130951DF79981C8289B}

If an activity's content was successfully delivered to users but its report contains no data, ensure that you have the correct environment ([host group](/help/administrating-target/hosts.md)) selected in the report's settings.

개발 환경을 선택한 경우 "선택한 보고서 설정에 사용 가능한 데이터가 없습니다"라는 오류 메시지가 표시될 수 있습니다.

활동의 보고서에 대한 환경을 변경하려면 다음을 수행하십시오.

1. **[!UICONTROL 활동]**&#x200B;을 클릭하고 목록에서 원하는 활동을 클릭한 다음, **보고서[!UICONTROL 탭을 클릭합니다.]**
1. 톱니바퀴 아이콘을 클릭하여 보고서 설정을 구성합니다.

   ![A/B 설정 대화 상자](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >The gear icon is not available for [!UICONTROL Automated Personalization] (AP) reports.

1. **[!UICONTROL 환경]** 드롭다운 목록에서 **[!UICONTROL 프로덕션]**&#x200B;을 선택합니다.

   개발 환경이 선택되어 있지 않은 경우에는 보고서 데이터를 사용하지 못할 수 있습니다.

1. **[!UICONTROL 저장을 클릭합니다]**.

환경에 대한 자세한 내용은 [호출](../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E)를 참조하십시오.
