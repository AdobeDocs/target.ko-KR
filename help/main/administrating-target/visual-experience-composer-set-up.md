---
keywords: 시각적 경험 작성기;vec;기본 url;고급 경험 작성기;eec;혼합 컨텐츠;경험 스냅샷;모바일 뷰포트;css;css 선택기
description: Adobe 구성 방법 알아보기 [!DNL Target] 일반 설정, 모바일 뷰포트 구성 및 CSS 선택기를 지정하여 VEC(시각적 경험 작성기)입니다.
title: 시각적 경험 작성기(VEC)를 구성하려면 어떻게 해야 합니까?
feature: Administration & Configuration
role: Admin
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
source-git-commit: fa11f93058b69e5e59e0ee20c65cffa4a1344ca0
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 57%

---

# 시각적 경험 작성기 구성

구성 [!DNL Adobe Target] [!UICONTROL 시각적 경험 작성기] (VEC) 일반 설정, 모바일 뷰포트 구성 및 CSS 선택기를 지정합니다.

에 액세스하려면 [!UICONTROL 시각적 경험 작성기] 구성 페이지에서 **[!UICONTROL 관리]** > **[!UICONTROL 시각적 경험 작성기].**

>[!NOTE]
>
>이 페이지의 설정은 전체에 적용됩니다. [!DNL Target] 계정입니다.

![시각적 경험 작성기 구성 페이지](/help/main/administrating-target/assets/vec.png)

## 일반 설정

시각적 경험 작성기에 대한 일반 설정을 지정할 수 있습니다.

![일반 설정 섹션](/help/main/administrating-target/assets/general-settings.png)

다음 설정을 사용할 수 있습니다.

### 기본 URL

[!UICONTROL 시각적 경험 작성기]에서 사용되는 기본 URL을 설정합니다. 이것은 홈 페이지와 같이 각 새 활동에 대한 경험을 설정할 때마다 사용되는 기본 페이지입니다. 기본 URL을 설정하지 않은 경우, 활동을 만들 때 각 활동의 URL을 입력해야 합니다.

### 고급 경험 작성기 활성화 {#eec}

iFrame 버스팅 사이트 및 혼합 콘텐츠가 있는 사이트에서 편집할 수 있도록 허용합니다. 일부 사이트가 확장 버전과 호환되지 않을 수 있습니다. 원래 상태로 되돌리려면 이 옵션을 선택 취소합니다 [!UICONTROL 시각적 경험 작성기]. 사이트의 활동 전달은 이 선택 옵션의 영향을 받지 않습니다.

자세한 내용은 [ 시각적 경험 작성기 문제 해결 ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)을 참조하십시오.

또한 을 활성화할 수 있습니다. [!UICONTROL 향상된 경험 작성기] 활동 수준입니다.

### 혼합 콘텐츠 로드

다음을 사용하여 웹 사이트를 여는 동안 혼합 컨텐츠 활성화 [!UICONTROL 향상된 경험 작성기] (EEC) 이 옵션을 활성화하면 를 통해 정적 리소스를 로드하는 추가 오버헤드가 발생하지 않습니다. [!DNL Target] 프록시 서버.

이 옵션은 다음과 같은 경우에 유용합니다.

* CSP(콘텐츠 보안 정책) 헤더를 사용하면 EEC가 활성화된 상태에서 프록시 서버를 사용하지 않고도 혼합된 콘텐츠를 로드할 수 있습니다.
* HTTP 웹 사이트는 EEC에서 로드 시간이 늘어났지만, JavaScript, 이미지 등이 프록시를 통해 로드되는 시간이 오래 걸립니다.

### 활동 흐름 다이어그램에서 경험 스냅숏 생성

경험 스냅샷을 활성화하면 활동 워크플로우 다이어그램에서 경험에 대한 썸네일이 생성됩니다. 스냅샷을 비활성화하면 일부 사용자의 경우 성능이 더 빨라질 수 있습니다.

## [!BADGE 프리미엄]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인하십시오."}

경험을 미리 볼 때 사용할 장치를 추가할 수 있습니다. 각 장치에는 연결된 대상이 있습니다.

![모바일 뷰포트 구성 섹션](/help/main/administrating-target/assets/mobile-viewport-configuration.png)

클릭 **[!UICONTROL 추가]**, 모바일 뷰포트에 대한 수사적 이름을 지정하고, 너비와 높이를 지정한 후 원하는 운영 체제를 선택하고 [!UICONTROL 저장].

모바일 뷰포트를 추가하는 방법에 대한 내용은 [모바일 뷰포트 구성](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md)을 참조하십시오.

## CSS 선택기 {#css}

[!DNL Target]이 CSS 선택기를 생성하는 방법을 지정하십시오.

![CSS 선택기 섹션](/help/main/administrating-target/assets/css-selectors.png)

이러한 선택 사항은 [!DNL Target]에서 사이트 구조를 이해하여 콘텐츠 전달을 위한 더 나은 CSS 선택기를 생성하는 데 도움이 됩니다. 기본적으로 [!DNL Target]은 페이지의 요소 ID를 기준으로 선택기를 생성합니다. 사이트에서 소수의 ID를 사용하거나 같은 페이지에서 ID를 복제하는 경우 클래스를 사용하는 것이 더 나은 옵션이 될 수 있습니다.

다음 옵션 중 하나 또는 둘 다를 선택할 수 있습니다.

### 요소 ID 사용

동일한 ID를 여러 요소에 사용하거나 요소 ID가 페이지 로드 시 변경될 경우 이 옵션을 선택 취소하십시오.

### 요소 클래스 사용

기본적으로 [!DNL Target]은 요소 ID만 사용합니다. 그러나 페이지가 [!DNL Adobe Experience Manager]로 작성한 페이지처럼 클래스를 사용하여 요소를 식별하도록 디자인된 경우 [!UICONTROL 요소 클래스 사용]도 선택해야 합니다.

>[!NOTE]
>
>정확도를 위해 모든 작업을 수행했지만 클래스를 사용하면 오류가 발생할 수 있습니다. 어떤 옵션도 선택하지 않으면 정확도도 영향을 받습니다. 정확도 순서는 ID > 클래스 > 두 옵션을 모두 선택하지 않은 경우입니다. 항상 페이지를 테스트하여 선택기가 올바른지 확인해야 합니다.

활동별로 이 설정을 재정의할 수 있습니다. 설정 톱니바퀴 아이콘을 클릭한 다음, [!UICONTROL CSS 선택기]를 선택합니다. 이 기능은 여러 사이트가 서로 다르게 구성된 경우에 특히 유용합니다.

>[!NOTE]
>
>활동당 설정 재정의는에서 사용할 수 없습니다. [!UICONTROL Automated Personalization] 및 [!UICONTROL Multivariate Testing] 활동.  선택기에 대한 추가 정보는 ](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md)시각적 경험 작성기에서 사용되는 요소 선택기[를 참조하십시오.

## 교육 비디오: 계정 환경 설정(7:33) ![개요 배지](/help/main/assets/overview.png)

이 비디오에는 계정 기본 설정에 대한 정보가 포함되어 있습니다.

* [!DNL Target Standard]에서 사용할 수 있는 계정 설정을 설명합니다.

>[!NOTE]
>
>[!DNL Target] [!UICONTROL 관리] 메뉴 UI(이전명: [!UICONTROL 설정])는 향상된 성능을 제공하고, 새로운 기능을 출시할 때 필요한 유지 관리 시간을 줄이고, 제품 전반에 걸쳐 사용자 경험을 개선할 수 있도록 새롭게 디자인되었습니다. 다음 비디오에서 설명하는 정보는 일반적으로 정확하지만 옵션이 약간 다른 위치에 있을 수 있습니다. 업데이트된 비디오는 곧 게시될 예정입니다.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
