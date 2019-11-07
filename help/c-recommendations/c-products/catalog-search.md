---
keywords: 카탈로그;검색
description: Adobe Target의 카탈로그 검색은 카탈로그에서 제품이나 콘텐츠를 찾는 데 도움이 됩니다.
title: Adobe Target의 카탈로그 검색
uuid: e0876963-5905-4850-a615-953e435f26e9
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# ![PREMIUM](/help/assets/premium.png) 카탈로그 검색 {#catalog-search}

카탈로그 검색은 카탈로그에서 제품이나 컨텐츠를 찾는 데 도움이 됩니다.

카탈로그 검색에 액세스하려면 **[!UICONTROL 추천]** &gt; **[!UICONTROL 카탈로그 검색]**&#x200B;을 클릭합니다.

검색 필드에서 아래쪽 화살표를 클릭하면 표시되는 선택 사항 메뉴에서 검색 선택 사항을 선택하여 검색을 개선할 수 있습니다.

![](assets/searchproductsmenu.png)

검색 옵션에는 다음이 포함됩니다.

* ALL
* 이름
* 브랜드
* 카테고리
* ID
* 메시지

**[!UICONTROL 모두]**&#x200B;는 OR 논리를 사용하여 기타 모든 검색 기준으로 검색합니다.

검색 결과에서 **[!UICONTROL 환경]**&#x200B;을 클릭하여 표시하는 카탈로그의 프로덕션 호스트 그룹 환경을 지정합니다. [](/help/administrating-target/hosts.md) 검색 결과에 있는 항목들을 스크롤하여 썸네일 및 기타 제품 정보를 볼 수도 있습니다.

"제품" 옆에 표시되는 숫자는 지정된 환경에서 사용 가능한 전체 개수 중 검색어와 일치하는 제품의 수입니다.

피드 파일, API 또는 mbox 업데이트를 통해 업데이트가 수신되면 카탈로그가 자동으로 새로고침됩니다. 업데이트는 일반적으로 한 시간 내에 완료됩니다. 업데이트가 진행 중인 경우 가장 최근 업데이트가 시작된 시간이 표시됩니다. 진행 중인 업데이트가 없으면 가장 최근 업데이트가 시작되고 완료된 시간이 표시됩니다.

## 고급 검색을 기반으로 컬렉션 또는 제외 만들기

카탈로그 검색 페이지의 고급 검색([!UICONTROL 추천] &gt; [!UICONTROL 카탈로그 검색] &gt; [!UICONTROL 고급 검색])을 사용하여 [컬렉션](/help/c-recommendations/c-products/collections.md)이나 [제외](/help/c-recommendations/c-products/exclusions.md)를 만들 수 있습니다.

![다른 이름으로 저장](/help/c-recommendations/c-products/assets/save-as.png)

예를 들어 "id &gt; 포함"을 사용하여 검색을 작성한 후 [!UICONTROL 다른 이름으로 저장] &gt; [!UICONTROL 컬렉션 또는 제외]를 클릭할 수 있습니다.

>[!IMPORTANT]
>
>고급 검색 기능은 대소문자를 구분하지 않습니다. 그러나 배송 시 반환되는 제품은 대소문자를 구분하는 검색을 기반으로 합니다. 이러한 불일치로 인해 혼동이 발생할 수 있습니다. 따라서 고급 검색 기능을 사용하는 결과를 기반으로 컬렉션이나 제외를 작성할 때에는 대소문자 구분을 고려해야 합니다. 예를 들어, "Holiday"를 검색할 때 초기 검색 목록에는 "Holiday"와 "holiday"를 포함하는 결과가 나열됩니다. 그런 다음 "holiday"를 포함하는 제품을 반환할 의도로 카탈로그를 만드는 경우 "holiday"를 포함하는 제품만 반환됩니다. "Holiday"를 포함하는 제품은 반환되지 않습니다. 제외도 유사한 방식으로 처리됩니다.
