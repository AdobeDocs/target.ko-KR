---
description: 항목이 추천되지 않도록 하려면 제외 목록을 만드십시오.
keywords: 제외
seo-description: 항목이 추천되지 않도록 하려면 제외 목록을 만드십시오.
seo-title: 제외
solution: Target
title: 제외
topic: Premium
uuid: 1970846e-37d8-4b69-a0d9-ff45bb840bef
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# 제외{#exclusions}

항목이 추천되지 않도록 하려면 제외 목록을 만드십시오.

>[!IMPORTANT]
>
>정적 및 동적 제외 규칙은 마케팅 활동에 도움이 될 수 있는 강력한 기능입니다. 자세한 정보, 예 및 사용 사례 시나리오가 필요하면 [동적 및 정적 포함 규칙 사용](../../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F)을 참조하십시오.

1. **[!UICONTROL 권장 사항]** &gt; **[!UICONTROL 제외]**&#x200B;를 클릭하여 기존 제외 목록을 표시합니다.

   [!UICONTROL 제외] 목록 보기의 각 제외에 대해 보고된 "항목 수"는 구성된 기본 권장 사항 [호스트 그룹](/help/administrating-target/hosts.md)(환경)에서 해당 제외에 대한 규칙과 일치하는 제품의 수입니다. 기본 호스트 그룹을 변경하려면 [설정](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84)을 참조하십시오.

   ![](assets/exclusions_list.png)

1. **[!UICONTROL 제외 만들기]**&#x200B;를 클릭합니다.

1. (조건부) 제외를 만들거나 업데이트하여 해당 환경에서 제외의 컨텐츠를 미리 보는 동안 **[!UICONTROL 환경]** 필터에서 환경을 선택합니다. 기본적으로 기본 호스트 그룹의 결과가 표시됩니다.

   ![제외 만들기](/help/c-recommendations/c-products/assets/CreateExclusion.png)

1. 제외 **[!UICONTROL 이름]**&#x200B;을 입력하고 선택적 설명을 입력합니다.

1. 규칙 빌더를 사용하여 제외 항목을 만듭니다.

   규칙 목록에서 매개 변수를 선택하고 연산자를 선택한 다음, 하나 이상의 값을 입력하여 제품을 식별하십시오. 여러 값을 입력할 경우에는 쉼표로 구분합니다.

1. **[!UICONTROL 저장을 클릭합니다]**.

   카탈로그 검색 페이지의 고급 검색([!UICONTROL 권장 사항] &gt; [!UICONTROL 카탈로그 검색] &gt; [!UICONTROL 고급 검색])을 사용하여 제외를 만들 수도 있습니다. 예를 들어 "id &gt; 포함"을 사용하여 검색을 작성한 후 [!UICONTROL 다른 이름으로 저장] &gt; [!UICONTROL 제외]를 클릭할 수 있습니다.

>[!IMPORTANT]
>
>고급 검색 기능은 대소문자를 구분하지 않습니다. 그러나 배송 시 반환되는 제품은 대소문자를 구분하는 검색을 기반으로 합니다. 이러한 불일치로 인해 혼동이 발생할 수 있습니다. 따라서 고급 검색 기능을 사용하는 결과를 기반으로 제외를 작성할 때에는 대소문자 구분을 고려해야 합니다. 예를 들어, "Holiday"를 검색할 때 초기 검색 목록에는 "Holiday"와 "holiday"를 포함하는 결과가 나열됩니다. 그런 다음 "holiday"를 포함하는 제품을 제외할 의도로 제외를 만드는 경우 "holiday"를 포함하는 제품만 제외됩니다. "Holiday"를 포함하는 제품은 제외되지 않습니다.