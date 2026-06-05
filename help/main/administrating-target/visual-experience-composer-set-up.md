---
keywords: 시각적 경험 작성기;vec;기본 url;고급 경험 작성기;eec;혼합 컨텐츠;경험 스냅샷;모바일 뷰포트;css;css 선택기
description: 일반 설정, 모바일 뷰포트 구성 및 CSS 선택기를 지정하여 Adobe [!DNL Target] VEC(시각적 경험 작성기)를 구성하는 방법에 대해 알아봅니다.
title: 시각적 경험 작성기(VEC)를 구성하려면 어떻게 해야 합니까?
feature: Administration & Configuration
role: Admin
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
TQID: https://experienceleague.adobe.com/E1ck4-aG4txqaFLs3t3-8bN-BQIoY8stRASTRJfhZMY
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
subfeature_v2:
  - id: b1d5cd6a-4ed3-43f6-9a52-2721acea1129
  - id: c011fe9c-b94b-4a88-93d8-f2acece55112
  - id: fc9c2184-9102-403f-bd6c-0055021e4bea
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 721
ht-degree: 47%

---

# [!UICONTROL 시각적 경험 작성기 구성]

일반 설정, 모바일 뷰포트 구성 및 CSS 선택기를 지정하여 [!DNL Adobe Target] [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)를 구성하십시오.

[!UICONTROL 시각적 경험 작성기] 구성 페이지에 액세스하려면 **[!UICONTROL 관리]** > **[!UICONTROL 시각적 경험 작성기]를 클릭하십시오.**

{{permissions-update}}

>[!NOTE]
>
>이 페이지의 설정은 전체 [!DNL Target] 계정에 적용됩니다.

## 일반 설정

[!UICONTROL 시각적 경험 작성기]에 일반 설정을 지정할 수 있습니다.

![일반 설정 섹션](/help/main/administrating-target/assets/general-settings.png)

다음 설정을 사용할 수 있습니다.

### 기본 URL

[!UICONTROL 시각적 경험 작성기]에서 사용되는 기본 URL을 설정합니다. 이것은 홈 페이지와 같이 각 새 활동에 대한 경험을 설정할 때마다 사용되는 기본 페이지입니다. 기본 URL을 설정하지 않은 경우, 활동을 만들 때 각 활동의 URL을 입력해야 합니다.

### 고급 경험 작성기 활성화 {#eec}

iFrame 버스팅 사이트 및 혼합 콘텐츠가 있는 사이트에서 편집할 수 있도록 허용합니다. 일부 사이트가 확장 버전과 호환되지 않을 수 있습니다. 원래 [!UICONTROL 시각적 경험 작성기]&#x200B;(으)로 되돌리려면 이 옵션을 선택 취소합니다. 사이트의 활동 전달은 이 선택 옵션의 영향을 받지 않습니다.

자세한 내용은 [시각적 경험 작성기 문제 해결](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.

활동 수준에서 [!UICONTROL 향상된 경험 작성기]를 사용하도록 설정할 수도 있습니다.

### 혼합 콘텐츠 로드

[!UICONTROL 향상된 경험 작성기]&#x200B;(EEC)를 사용하여 웹 사이트를 여는 동안 혼합 콘텐츠를 사용하도록 설정하십시오. 이 옵션을 사용하면 [!DNL Target] 프록시 서버를 통해 정적 리소스를 로드하는 추가 오버헤드가 발생하지 않습니다.

이 옵션은 다음과 같은 경우에 유용합니다.

* CSP(콘텐츠 보안 정책) 헤더를 사용하면 EEC가 활성화된 상태에서 프록시 서버를 사용하지 않고도 혼합된 콘텐츠를 로드할 수 있습니다.
* HTTP 웹 사이트는 EEC에서 로드 시간이 늘어났지만, JavaScript, 이미지 등이 프록시를 통해 로드되는 데 더 오래 걸립니다.

### 활동 흐름 다이어그램에서 경험 스냅숏 생성

경험 스냅샷을 활성화하면 활동 워크플로우 다이어그램에서 경험에 대한 썸네일이 생성됩니다. 스냅샷을 비활성화하면 일부 사용자의 경우 성능이 더 빨라질 수 있습니다.

## 모바일 뷰포트 구성

>[!NOTE]
>
>[!UICONTROL 모바일 뷰포트 구성] 설정은 [Target Premium](/help/main/c-intro/intro.md#premium) 기능입니다.


경험을 미리 볼 때 사용할 장치를 추가할 수 있습니다. 각 장치에는 연결된 대상이 있습니다.

![모바일 뷰포트 구성 섹션](/help/main/administrating-target/assets/mobile-viewport-configuration.png)

**[!UICONTROL 추가]**&#x200B;를 클릭하고, 모바일 뷰포트에 대한 수사적 이름을 지정하고, 너비와 높이를 지정하고, 원하는 운영 체제를 선택한 다음 [!UICONTROL 저장]을 클릭합니다.

모바일 뷰포트를 추가하는 방법에 대한 내용은 [모바일 뷰포트 구성](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md)을 참조하십시오.

## CSS 선택기 {#css}

[!DNL Target]이 CSS 선택기를 생성하는 방법을 지정하십시오.

![CSS 선택기 섹션](/help/main/administrating-target/assets/css-selectors.png)

이러한 선택 사항은 [!DNL Target]에서 사이트 구조를 이해하여 콘텐츠 전달을 위한 더 나은 CSS 선택기를 생성하는 데 도움이 됩니다. 기본적으로 [!DNL Target]은 페이지의 요소 ID를 기준으로 선택기를 생성합니다. 사이트에서 소수의 ID를 사용하거나 같은 페이지에서 ID를 복제하는 경우 클래스를 사용하는 것이 더 나은 옵션이 될 수 있습니다.

다음 옵션 중 하나 또는 둘 다를 선택할 수 있습니다.

### 요소 ID 사용

동일한 ID를 여러 요소에 사용하거나 요소 ID가 페이지 로드 시 변경될 경우 이 옵션을 선택 취소하십시오.

### 요소 클래스 사용

기본적으로 [!DNL Target]은 요소 ID만 사용합니다. 그러나 페이지가 [!DNL Adobe Experience Manager]&#x200B;(으)로 작성된 페이지와 같이 클래스를 사용하여 요소를 식별하도록 디자인된 경우 [!UICONTROL 요소 클래스 사용]도 선택해야 합니다.

>[!NOTE]
>
>정확도를 위해 모든 작업을 수행했지만 클래스를 사용하면 오류가 발생할 수 있습니다. 어떤 옵션도 선택하지 않으면 정확도도 영향을 받습니다. 정확도 순서는 ID > 클래스 > 두 옵션을 모두 선택하지 않은 경우입니다. 항상 페이지를 테스트하여 선택기가 올바른지 확인해야 합니다.

활동별로 이 설정을 재정의할 수 있습니다. [!UICONTROL 설정] 톱니바퀴 아이콘을 클릭한 다음 [!UICONTROL CSS 선택기]를 선택합니다. 이 기능은 여러 사이트가 서로 다르게 구성된 경우에 특히 유용합니다.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] 및 [!UICONTROL Multivariate Testing] 활동에서는 활동별 설정을 재정의할 수 없습니다.  선택기에 대한 추가 정보는 [&#128279;](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md)시각적 경험 작성기에서 사용되는 요소 선택기를 참조하십시오.

## 교육 비디오: 계정 환경 설정(7:33) ![개요 배지](/help/main/assets/overview.png)

이 비디오에는 계정 기본 설정에 대한 정보가 포함되어 있습니다.

* [!DNL Target Standard]에서 사용할 수 있는 계정 설정을 설명합니다.

>[!NOTE]
>
>[!DNL Target] [!UICONTROL 관리] 메뉴 UI(이전 [!UICONTROL 설정])는 향상된 성능을 제공하고, 새로운 기능을 출시할 때 필요한 유지 관리 시간을 줄이고, 제품 전반에 걸쳐 사용자 경험을 개선할 수 있도록 새롭게 디자인되었습니다. 다음 비디오에서 설명하는 정보는 일반적으로 정확하지만 옵션이 약간 다른 위치에 있을 수 있습니다. 업데이트된 비디오는 곧 게시될 예정입니다.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
