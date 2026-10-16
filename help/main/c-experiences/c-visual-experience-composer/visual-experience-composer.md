---
keywords: 시각적 경험 작성기;vec;wysiwyg
description: Adobe Target에서 시각적 경험 작성기(VEC) 사용의 기본 사항에 대해 알아봅니다. VEC는 개인화된 경험을 쉽게 만들 수 있는 WYSIWYG 편집기입니다.
title: 시각적 경험 작성기(VEC)를 사용하려면 어떻게 해야 합니까?
feature: Visual Experience Composer (VEC)
exl-id: 51650f2a-1f24-40c7-8692-77f55656b4f6
TQID: 'https://experienceleague.adobe.com/X4nfYuOtD3TVusnVIIEZhXwUdCZ-dMvbZeJlrkmI9Hs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 140a7287246905d47bf02a84348627017a619386
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 0%
---
# [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)

[!DNL Adobe Target]의 [!UICONTROL 시각적 경험 작성기]&#x200B;(VEC)는 코드를 편집하지 않고 웹 사이트 및 모바일 웹 페이지에서 직접 개인화된 경험을 만들고 테스트하기 위한 WYSIWYG 편집기입니다.

요소를 드래그 앤 드롭하고, 콘텐츠를 교체하고, 페이지 레이아웃을 변경하여 [!DNL Target] 활동에 대한 경험과 오퍼를 만드십시오. 작성기는 HTML 및 JavaScript 편집 옵션도 제공합니다.

## 브라우저 요구 사항 {#browser-requirements}

[!DNL Adobe Target] 인터페이스에 대해 [!DNL Safari]이(가) 지원됩니다. [!DNL Safari]에서 양식 기반 활동을 만들고 VEC 및 [!UICONTROL 고급 경험 작성기]&#x200B;(EEC)를 제외한 모든 기능을 사용할 수 있습니다. [!DNL Safari]에서 시각적 경험 작성기를 열면 경험을 편집하려면 [!DNL Google Chrome]&#x200B;(으)로 전환하라는 오버레이가 표시됩니다.

[!DNL Firefox]과(와) 같은 브라우저에서는 보안 사이트 내의 비보안 페이지와 같이 혼합 콘텐츠가 포함된 페이지가 VEC에 표시되지 않도록 차단할 수 있습니다. 페이지가 표시되지 않으면 브라우저 주소 표시줄에서 URL 옆에 있는 아이콘을 클릭한 다음 **[!UICONTROL 이 페이지에서 보호 사용 안 함을 클릭합니다]**. 이 문제는 사이트 방문자에게 페이지가 표시되는 방식에는 영향을 주지 않습니다.

## VEC 열기 {#open-the-vec}

VEC에서 기본적으로 열리는 페이지를 설정하려면 [!DNL Target] **[!UICONTROL 관리]** > **[!UICONTROL 시각적 경험 작성기]** 탭에 기본 [!UICONTROL 시각적 경험 작성기] URL을 입력하십시오.

기본 URL을 설정하지 않으면 VEC가 열리고 URL을 지정할 수 있는 빈 페이지가 표시됩니다.

![강조 표시된 VEC](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

## 경험 편집 {#edit-experiences}

### 경험 보기 및 이름 지정 {#view-and-name-experiences}

[!UICONTROL 경험] 레일의 탭을 사용하여 다양한 대상자 또는 다양한 경험을 가진 사용자에게 페이지가 표시되는 방식을 확인합니다. 목록에서 더 쉽게 식별할 수 있도록 각 경험에 수사적 이름을 지정합니다.

예를 들어 탐색 막대에서 홈 링크의 위치를 테스트할 때 처음 표시되는 경험의 이름을 &quot;홈 링크 우선&quot;으로 지정합니다.

![경험 레일에서 경험 이름 바꾸기](/help/main/c-experiences/c-visual-experience-composer/assets/rename_exp.png)

### 요소 선택 및 수정 {#select-and-modify-elements}

커서를 페이지 위로 이동하면 상황에 맞는 상자로 개별 요소를 강조 표시합니다.

강조 표시된 요소를 클릭하여 해당 요소 유형에 대한 편집 옵션을 표시합니다. 예를 들어 이미지를 선택하고 **[!UICONTROL 이미지 소스 변경]**&#x200B;을 클릭하여 바꾸거나 단추를 선택하여 텍스트 색상을 변경합니다.

![선택한 요소에 대한 옵션 편집](/help/main/c-experiences/c-visual-experience-composer/assets/properties-exp.png)

페이지에 포함된 iframe 내의 컨텐츠는 편집할 수 없습니다. 해당 콘텐츠를 편집하려면 iframe 문서가 [!DNL Target]에서 사용할 수 있도록 설정되어 있는지 확인한 다음 VEC에서 직접 iframe URL을 로드하십시오.

VEC 외부의 페이지 구조를 변경하면 활동에서 사용하는 위치에 영향을 줄 수 있습니다. 해당 위치가 변경되면 [!DNL Target]에서 수정한 요소를 찾지 못할 수 있으며 이로 인해 환경을 편집할 때 문제가 발생할 수 있습니다.

### 찾아보기 및 디자인 {#browse-and-design}

배송 페이지나 장바구니와 같이 현재 페이지에서 액세스할 수 있는 페이지로 이동하여 변경 내용을 테스트하려면 **[!UICONTROL 찾아보기]**&#x200B;를 클릭합니다.

![VEC에서 찾아보기 모드](/help/main/c-experiences/c-visual-experience-composer/assets/browse_exp.png)

찾아보기 모드에서 플라이아웃 메뉴 및 미니 장바구니와 같이 마우스로 가리키면 표시되는 요소에 액세스할 수도 있습니다. 편집할 페이지 또는 요소에 도달하면 **[!UICONTROL 디자인]**&#x200B;을 클릭하여 환경을 편집합니다.

마우스로 가리키기 상태가 JavaScript에 따라 다를 경우 **[!UICONTROL JavaScript 비활성화]**&#x200B;가 선택되어 있지 않은지 확인하십시오. 종속된 요소를 편집하려면 JavaScript을 활성화해야 합니다.

사용 가능한 편집 옵션에 대한 자세한 내용은 [시각적 경험 작성기 옵션](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81)을 참조하십시오.

## 페이지 로드 관리 {#manage-page-loading}

일부 편집 옵션은 페이지가 로드되는 동안 또는 페이지 로드가 실패한 후에도 계속 사용할 수 있습니다. 기다리지 않고 이러한 옵션에 액세스하기 위해 페이지 로드를 취소할 수도 있습니다.

### 페이지를 로드하는 동안 또는 페이지 로드가 실패한 후 페이지 편집 {#loading}

예를 들어 사용자 지정 코드가 더 이상 작동하지 않으므로 VEC에서 페이지 로드가 완료되기 전이나 페이지 로드가 실패한 후 일부 내용을 변경할 수 있습니다.

사용 가능한 편집 옵션을 사용하여 다음을 수행합니다.

* 사용자 지정 코드 추가 또는 경험 이름 변경과 같은 간단한 변경 작업 수행
* 더 이상 액세스할 수 없는 페이지에서 기존 사용자 지정 코드 복사
* VEC에서 로드할 수 없는 페이지를 간단하게 편집합니다.

[!UICONTROL 경험] 레일, [!UICONTROL 구성 요소] 레일 및 [!UICONTROL 구성] 옵션은 페이지가 로드되는 동안 또는 페이지 로드가 실패한 후에도 계속 액세스할 수 있습니다.

### VEC 내에서 페이지 로드 취소 {#cancel-loading}

페이지 로드가 완료될 때까지 기다리지 않고 활동을 편집하려면 VEC에서 페이지 로드를 취소하십시오.

페이지 로드 취소는 다음과 같은 경우에 유용합니다.

* 기존 수정 사항을 약간 편집합니다.
* 하나 이상의 기존 수정 사항 삭제
* 사용자 지정 코드 삽입 또는 편집
* 잘못 입력한 페이지 URL 수정
* VEC에서 페이지를 로드하기 전에 JavaScript을 활성화하거나 비활성화합니다.
* [!UICONTROL 페이지 게재] 기준에 템플릿 테스트 규칙 추가
* EEC를 통해 페이지를 로드할 때 또는 iframe 전용 모드에서 전역 [!UICONTROL 고급 경험 작성기]&#x200B;(EEC) 전환을 재정의합니다.

페이지 로드를 취소한 후 페이지가 로드될 때까지 기다리지 않고 활동에서 경험 간에 전환할 수 있습니다. VEC에서 페이지를 다시 표시하려면 **[!UICONTROL 다시 로드]**&#x200B;를 클릭합니다.

>[!IMPORTANT]
>
>페이지 로드를 취소한 후 사용자 지정 코드를 편집하거나 다른 내용을 수정하는 경우 QA(품질 보증) 테스트를 수행하여 변경 사항이 예상대로 전달되는지 확인하십시오.

페이지 로드를 중지하려면 페이지를 로드하는 동안 **[!UICONTROL 로드 취소]**&#x200B;를 클릭합니다. 페이지를 다시 로드하지 않는 한 현재 편집 세션 중에 이 활동에 대해 페이지가 언로드된 상태로 유지됩니다.

현재 활동에서 환경 관리를 다시 시작하거나 새로운 수정 사항을 추가하려면 **[!UICONTROL 다시 로드]**&#x200B;를 클릭하세요.
