---
description: 이러한 릴리스 노트는 최신 또는 예정된 타겟 릴리스의 기능, 향상된 기능, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
keywords: 릴리스 노트
seo-description: 이러한 릴리스 노트는 최신 또는 예정된 Adobe Target 릴리스의 기능, 향상된 기능, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다
seo-title: Adobe Target 릴리스 노트 (베타 버전)
solution: Target
title: Target 릴리스 노트(사전 릴리스)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: e50ae8c95774716ea484f02b276b2d66cb228364

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이러한 릴리스 노트는 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 향상된 기능 및 수정 사항에 대한 정보를 제공합니다.

**마지막 업데이트: 2019년 6월 6일**

>[!NOTE]
>
>이러한 릴리스 노트에는 사전 릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트를 참조하십시오](release-notes.md). 이러한 페이지에 대한 정보는 동일하거나 다를 수 있습니다.
>
>괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## Target Standard/Premium 19.6.1(2019년 6월 25일) {#tgt-19-6-1}

이 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

### 시각적 경험 작성기(VEC)

* **새 VEC 메뉴 옵션**: vec에서 페이지 요소를 클릭하면 메뉴에 해당 요소 유형에 사용할 수 있는 옵션이 표시됩니다.

   * **스타일 &gt; 배경**: 이제 [!UICONTROL 스타일 &gt; 배경] 옵션을 사용하여 선택한 요소의 배경 이미지와 색상을 변경할 수 있습니다. (TGT-15001)

   * **[!UICONTROL 대체 &gt; HTML]및[!UICONTROL 바꾸기 &gt; 경험 조각으로 바꿉니다]**. 이미지를 클릭하고로 [!UICONTROL ]바꾸기를 클릭하면 두 개의 새 옵션이 표시됩니다.

      * **HTML**: HTML 옵션에 액세스하기 위해 상위 요소를 선택하지 않고도 요소를 완전히 제어할 수 있도록 HTML로 이미지를 바꿀 수 있습니다.
      * **경험 조각**: 이미지를 AEM (Adobe Experience Manager [) 경험 조각으로](/help/c-experiences/c-manage-content/aem-experience-fragments.md) 대체하여 Target 활동에 AEM에서 만든 요소를 빠르게 삽입할 수 있습니다. (TGT-34097)

* **클릭 추적 개선** 사항: VEC 및 SPA (Single Page Application) VEC 내에서 클릭 추적을 구성하는 과정을 개선했습니다.

   * 클릭 추적에서 사용할 요소를 선택할 때 사용 가능한 모든 요소의 이름이 오른쪽의 수정 패널에 표시되므로 원하는 요소를 빠르고 손쉽게 선택할 수 있습니다.
   * 세 부분으로 구성된 안내 활동 워크플로우의 [!UICONTROL 목표 및 설정] 페이지에는 클릭 추적에 대해 선택한 요소의 수를 나타내는 숫자가 표시됩니다. 이 숫자 위로 마우스를 가져가면 선택한 모든 요소의 이름이 표시됩니다. (TGT-33878)

### SPA VEC

* **가이드 워크플로우**: 새로운 안내 워크플로우는 단일 페이지 앱에 대해 활동을 실행하고 실행하는 페이지 배달 규칙 설정을 구성하는 방법을 이해하는 데 도움이 됩니다. (TGT-33718)

* **복제 수정** 사항: 이제 SPA VEC를 사용하여 수정 사항을 정의한 다음 단일 페이지 앱에서 다른 보기에 사용하기 위해 해당 수정 내용을 복제할 수 있습니다. (TGT-33882)

### Mobile VEC

* **다양한 앱 버전**: 이제 여러 버전의 모바일 앱용 활동을 제작할 수 있습니다. 따라서 버전이 유사하고 앱의 UI를 크게 변경할 필요가 없을 때 시간과 노력을 절약할 수 있습니다. (TGT-34231)

### ![프리미엄 배지](/help/assets/premium.png) 자동 개인화 (AP) 및 자동 타깃팅

* **제어 기능**: AP 또는 자동 타겟 활동을 만드는 동안 컨트롤로 사용할 경험을 선택할 수 있습니다. 이 기능을 사용하면 활동에 구성된 트래픽 할당 비율에 따라 전체 제어 트래픽을 특정 경험으로 라우팅할 수 있습니다. 그런 다음 해당 경험의 제어 트래픽에 대한 개인화된 트래픽의 성능 보고서를 평가할 수 있습니다. 현재 제어 옵션 (임의로 제공된 경험) 는 계속 사용할 수 있습니다. (TGT-32801 및 TGT-26572)

### 기타 개선 사항, 수정 사항 및 변경 사항

* 이제 페이지에서 요소를 클릭하면 vec 아래쪽에 표시되는 DOM 경로에 `<BODY>` 태그가 표시되어 `<BODY>` 태그에 대해 작업을 수행할 수 있습니다. (TGT-33736)

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선 순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
