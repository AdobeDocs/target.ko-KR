---
keywords: 시각적 경험 작성기;VEC;슬라이드
description: Adobe [!DNL Target] VEC(시각적 경험 작성기)에서 편집할 수 있는 회전 메뉴를 만드는 방법을 알아봅니다.
title: 시각적 경험 작성기에서 회전 메뉴를 만들려면 어떻게 해야 합니까?
feature: Visual Experience Composer (VEC)
exl-id: 50bc11d2-c9fc-4b53-8218-49842b59269a
TQID: 'https://experienceleague.adobe.com/RN04MJgC49BI2-h2e-i-kgSRTejpLHzKACm-hOv2VCE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%
---
# [!UICONTROL 시각적 경험 작성기]에서 작동하는 회전 메뉴를 만드는 중 {#vec-carousels}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL 시각적 경험 작성기]**(VEC)에서 편집할 수 있는 회전 메뉴를 만드는 방법을 알아봅니다.

>[!ENDSHADEBOX]

다음 구조로 만들어진 회전 메뉴를 [!DNL Adobe Target] **[!UICONTROL VEC(시각적 경험 작성기)에서 편집할 수 있습니다.]**&#x200B;구조에서는 각 슬라이드의 선택기를 유효하게 유지하므로 VEC에 페이지가 로드된 후 표시된 슬라이드가 몇 초 후에 변경되는 경우에도 [!DNL Target]에서 항상 올바른 슬라이드를 식별합니다.

1. 슬라이드를 정적 HTML 자리 표시자로 만듭니다. 슬라이드에는 하나가 표시되고 다른 슬라이드에는 클래스별로 숨겨집니다.

   ```html
   <ul>
   <li class="show"> slide 1 </li>
   <li class="hidden"> slide 2 </li>
   <li class="hidden"> slide 3 </li>
   </ul>
   ```

1. CSS로만 모양과 느낌을 디자인할 수 있습니다. 이 작업에는 JavaScript을 사용하지 마십시오.

   >[!NOTE]
   >
   >**[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 사용자 지정 코드와 함께 사용할 경우 **[!UICONTROL JavaScript을 사용하여 렌더링]** 옵션은 현재 지원되지 않습니다.

1. 클래스 이름만 업데이트하여 다음 슬라이드 표시: 다른 슬라이드는 숨기고 타이머 또는 애니메이션으로 다음 슬라이드 표시 JavaScript으로 DOM 구조를 절대 업데이트하지 마십시오.
