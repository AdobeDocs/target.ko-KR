---
keywords: 시각적 경험 작성기;VEC;캐러셀
description: Adobe [!DNL Target] VEC(시각적 경험 작성기)에서 편집할 수 있는 회전 메뉴를 만드는 방법을 알아봅니다.
title: 시각적 경험 작성기에서 회전 메뉴를 만들려면 어떻게 해야 합니까?
feature: Visual Experience Composer (VEC)
exl-id: 50bc11d2-c9fc-4b53-8218-49842b59269a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 58%

---

# 시각적 경험 작성기에서 작동하는 회전 메뉴 만들기

이 항목에서는 [!DNL Adobe Target] [!UICONTROL Visual Experience Composer](VEC)에서 편집할 수 있는 회전 메뉴를 만드는 방법을 보여 줍니다.

아래 단계를 사용하면 [!DNL Target]에서는 항상 선택한 슬라이드가 몇 초 후에 시각적 경험 작성기에서 변경되더라도 선택한 슬라이드에 올바른 슬라이드에 대한 &#39;선택기&#39;가 있다는 것을 알고 있습니다.

1. 정적 HTML 자리 표시자를 만듭니다.

   ```html
   <ul>
   <li class="show"> slide 1 </li>
   <li class="hidden"> slide 2 </li>
   <li class="hidden"> slide 3 </li>
   </ul>
   ```

1. CSS를 추가하여 모양과 느낌을 디자인합니다.

   이 작업을 위해서는 자바스크립트를 사용하지 마십시오.

   >[!NOTE]
   >
   >시각적 경험 작성기에서 사용자 지정 코드와 함께 사용할 경우 [!UICONTROL Render Using JavaScript] 옵션은 현재 지원되지 않습니다.

1. 타이머/애니메이션을 사용하여 다른 항목은 숨기고 다음 항목은 표시하도록 하려면 classNames만 업데이트합니다.

   자바스크립트를 사용하여 DOM 구조를 절대 업데이트하지 마십시오.
