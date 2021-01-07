---
keywords: visual experience composer;vec;wysiwyg
description: Adobe Target의 시각적 경험 작성기(VEC) 사용에 대한 정보.
title: Adobe Target VEC(시각적 경험 작성기)
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 8110807a73e4d6d9848a52224db04faba033c98c
workflow-type: tm+mt
source-wordcount: '1378'
ht-degree: 95%

---


# 시각적 경험 작성기(VEC)

[!DNL Adobe Target]에서 [!UICONTROL Visual Experience Composer](VEC) 사용에 대한 정보입니다.

VEC는 사이트 컨텍스트에서 개인화된 경험과 오퍼를 쉽게 만들고 테스트할 수 있는 WYSIWYG 사용자 인터페이스입니다. 웹 페이지(또는 오퍼) 또는 모바일 웹 페이지의 레이아웃 및 콘텐츠를 드래그 앤 드롭하고, 교체하고, 수정하여 타겟 활동에 대한 경험과 오퍼를 만들 수 있습니다.

VEC는 [!DNL Adobe Target]의 주요 기능 중 하나입니다. VEC를 통해 마케터와 디자이너가 시각적 인터페이스를 사용하여 콘텐츠를 만들고 변경할 수 있습니다. 코드를 직접 편집하지 않고도 많은 디자인을 작성할 수 있습니다. 또한 작성기에서 사용 가능한 편집 선택 사항을 사용하여 HTML 및 JavaScript를 편집할 수도 있습니다.

Target **[!UICONTROL 관리]** > **[!UICONTROL Visual Experience Composer]** 탭에서 기본 Visual Experience Composer URL을 입력할 수 있습니다.

![기본 VEC URL 설정](/help/c-experiences/c-visual-experience-composer/assets/pref-default-url-new.png)

이 URL은 VEC를 열 때 시작되는 위치를 결정합니다. 기본값을 입력하지 않는 경우 편집기를 열 때 빈 페이지로 시작한 후에 URL을 지정합니다.

>[!NOTE]
>
>특정 브라우저(예: Firefox)는 페이지에 혼합 콘텐츠(예: 보안 사이트의 비-보안 페이지)가 포함된 경우 VEC에 표시되지 않도록 페이지를 차단할 수 있습니다. 페이지가 표시되지 않는 경우 브라우저 주소 표시줄에서 URL 옆에 있는 아이콘을 클릭하고 **[!UICONTROL 이 페이지에서 보호 비활성화]**&#x200B;를 클릭합니다. 이 문제는 사이트 방문자에 대한 페이지 표시에는 영향을 주지 않습니다.

페이지에서 iframe 내에 있는 콘텐츠는 VEC에서 수정할 수 없습니다. iframe 내의 콘텐츠를 편집하려면 iframe 문서가 Target에서 사용할 수 있도록 설정되어 있는지 확인한 다음 VEC에서 해당 iframe URL을 로드하십시오.

페이지 상단에 있는 드롭다운 메뉴를 사용하여 페이지를 다른 대상이나 경험에 표시되는 모습으로 볼 수 있습니다. 두 번째 드롭다운 목록에서 각 경험에 대한 이름을 입력할 수 있습니다. 예를 들어, 탐색 막대에서 홈 링크의 위치를 테스트하는 경우, 목록에서 경험을 보다 쉽게 식별할 수 있도록 홈 링크가 표시되는 경험의 이름을 &quot;홈 링크&quot; 등으로 지정할 수 있습니다.

>[!NOTE]
>
>해당 페이지에서 만든 활동에 사용된 위치에 영향을 주는 페이지의 구조를 변경하면 경험 편집에 문제가 발생할 수 있습니다. 위치가 VEC 외부에서 변경된 경우에는 Target에서 콘텐츠가 변경된 위치를 찾지 못할 수 있습니다.

페이지 주변으로 마우스를 이동하면 상황에 맞는 상자가 커서를 따르면서 페이지의 요소를 강조 표시합니다.

![강조 표시된 VEC](/help/c-experiences/c-visual-experience-composer/assets/vec-highlight-new.png)

강조 표시가 표시되는 방식을 변경하려면 **[!UICONTROL 오버레이]** 아이콘을 클릭합니다. 예를 들어 이미지, 링크, 지역 mbox, 수정 사항 또는 JavaScript만 강조 표시하도록 선택할 수 있습니다. 강조 표시의 색상을 변경할 수 있습니다. 또한 다양한 요소 유형을 강조 표시하는 데 사용되는 강조 표시 색상과 채우기 유형을 지정할 수도 있습니다.

![오버레이 설정 변경](/help/c-experiences/c-visual-experience-composer/assets/change-overlay.png)

해당 요소 유형에 사용할 수 있는 옵션 메뉴에 대해 강조 표시된 요소를 클릭합니다. 예를 들어 이미지를 클릭하고 **[!UICONTROL 편집 > 텍스트/HTML]**&#x200B;을 선택하여 텍스트를 변경하거나, 단추를 클릭하고 배경색을 변경할 수 있습니다. 페이지 왼쪽 위에 있는 단추를 사용하여 오버레이 켜기와 끄기를 전환할 수 있습니다.

**[!UICONTROL 찾아보기]**&#x200B;를 클릭한 다음 배송 페이지나 장바구니와 같은 기본 페이지에서 사용할 수 있는 페이지로 이동하여 해당 페이지의 변경 사항을 테스트할 수도 있습니다. 플라이아웃 메뉴나 미니 장바구니와 같이 마우스로 가리키고 사용할 수 있는 페이지 요소에 액세스할 수도 있습니다. 페이지 탐색을 마쳤으면 **[!UICONTROL 작성]**&#x200B;을 클릭하여 경험을 편집합니다. 예를 들어, 장바구니 드롭다운이나 이미지 회전 메뉴의 디자인을 변경할 수 있습니다.

>[!NOTE]
>
>마우스로 가리키기 상태가 JavaScript에 따라 다를 경우 **[!UICONTROL JavaScript 비활성화]**&#x200B;가 선택되어 있지 않은지 확인하십시오. JavaScript 요소를 편집하려면 JavaScript를 활성화해야 합니다.

VEC에서 사용할 수 있는 옵션에 대한 자세한 내용은 [시각적 경험 작성기 선택 사항](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81)을 참조하십시오.

페이지를 로드하는 동안(또는 페이지 로드가 실패한 후) 페이지에서 일부 수정 작업을 수행하거나 VEC에서 페이지 로드를 취소할 수 있습니다. 자세한 내용은 다음 문서를 참조하십시오.

* [페이지를 로드하는 동안 또는 페이지 로드가 실패한 후 페이지 편집](#loading)
* [VEC 내에서 페이지 로드 취소](#cancel-loading)

## 페이지를 로드하는 동안 또는 페이지 로드가 실패한 후 페이지 편집 {#loading}

페이지가 VEC에 로드되기 전에 또는 페이지가 완전히 로드되지 않은 경우에도 여러 작업을 수행할 수 있습니다(예: 사용자 지정 코드가 더 이상 작동하지 않음).

VEC 내에서 로드하는 동안 또는 페이지 로드가 실패한 후 페이지에 액세스하거나 페이지를 편집할 수 있는 몇 가지 이유는 다음과 같습니다.

* 사용자 지정 코드 추가 또는 경험 이름 변경 등을 위해 페이지를 간단하게 수정하기 위해
* 더 이상 액세스할 수 없는 페이지에서 기존 사용자 지정 코드를 복사하기 위해
* 페이지가 VEC 내에서 로드되지 않는다는 것을 알고 있지만 간단하게 편집하기 위해

페이지가 로드되는 동안(또는 페이지 로드가 실패한 후) [!UICONTROL 경험] 패널, [!UICONTROL 수정 사항] 패널 및 경험 상단에 있는 설정(오버레이, 수정 사항, 구성 등)에 모두 액세스할 수 있습니다.

다음 그림은 페이지가 로드되는 동안 사용자 지정 코드를 삽입하거나 다른 작업을 수행할 수 있음을 보여줍니다.

![페이지 로드](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/loading-page.png)

## VEC 내에서 페이지 로드 취소 {#cancel-loading}

페이지가 로드될 때까지 기다리지 않고 활동 편집을 잠금 해제하기 위해 VEC 내에서 페이지 로드를 취소할 수 있습니다. 이 기능을 사용하면 시간을 절약할 수 있고, VEC 내에서 페이지가 로드될 때까지 기다릴 필요 없이 사용자 지정 코드를 보다 효율적으로 편집하거나 삽입할 수 있습니다.

VEC 내에서 페이지 로드를 취소할 수 있는 몇 가지 이유는 다음과 같습니다.

* 기존 수정 사항을 약간 편집하려는 경우
* 하나 이상의 기존 수정 사항을 삭제하려는 경우
* 사용자 지정 코드를 삽입하거나 편집하려는 경우
* 페이지 URL을 실수로 잘못 입력한 경우
* VEC에서 페이지를 로드하기 전에 JavaScript를 활성화하거나 비활성화하려는 경우
* 페이지 전달 기준에 템플릿 테스트 규칙을 더 많이 추가하려는 경우
* EEC를 통해 페이지를 로드할 때 또는 iframe만 페이지마다 다를 수 있을 때 전역 또는 글로벌 EEC(향상된 경험 작성기) 전환을 재정의하려는 경우

VEC에서 페이지 로드를 취소한 후 페이지가 로드될 때까지 기다리지 않고 활동에서 경험 간에 전환할 수 있습니다. VEC 내에서 다시 페이지를 보려면 **[!UICONTROL 다시 로드]** 단추를 클릭해야 합니다.

>[!IMPORTANT]
>
>사용자 지정 코드 또는 수정 사항이 있는 경우 VEC 내에서 로드를 취소하도록 선택하여 코딩 또는 변경이 제대로 수행되었는지 확인해야 합니다. 사용자 지정 코드와 기타 수정 사항이 예상대로 전달되도록 하려면 적절한 QA를 수행했는지 확인합니다.

VEC 내에서 페이지 로드를 취소하려면 페이지가 로드되는 동안 **[!UICONTROL 로드 취소]** 단추를 클릭합니다. 현재 편집 세션 중에는 이 활동에 대한 페이지가 VEC에서 로드되지 않습니다.

![로드 취소 단추](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/cancel-loading.png)

현재 활동에서 경험을 계속 관리하거나 새로운 수정 사항을 추가하려면 **[!UICONTROL 다시 로드]** 단추를 클릭해야 합니다.

![다시 로드 단추](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/reload-in-vec.png)

>[!NOTE]
>
>이 기능에 대해 현재 알려진 문제는 다음 릴리스에서 수정됩니다. 자세한 내용은 [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md#cancel) 페이지에서 &quot;VEC 내에서 페이지 로드 취소&quot;를 참조하십시오.

## 교육 비디오

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### Visual Experience Composer (1/2) (7:17) ![자습서 배지](/help/assets/tutorial.png)

* 페이지 콘텐츠 변경
* 페이지 레이아웃 변경

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### Visual Experience Composer (2/2) (7:29) ![자습서 배지](/help/assets/tutorial.png)

* 경험 이름 변경 및 경험 복제
* 리디렉션 경험 만들기
* 활동을 단일 URL 또는 URL 그룹에 타깃팅
* 다중 페이지 활동 만들기
* 응답형 웹 사이트용 경험 미리 보기 및 빌드
* 오버레이를 사용하여 요소 유형을 강조 표시

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### 업무 시간:Visual Experience Composer ![자습서 배지](/help/assets/tutorial.png)

이 비디오는 Adobe 고객 지원 팀에서 진행한 이니셔티브인 &quot;[운영시간](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot; 기록입니다.

* VEC 작동 방식
* VEC에서 일반적인 문제가 발생하지 않도록 하는 방법
* VEC에서 사용할 수 있는 해결 방법 사례

>[!VIDEO](https://video.tv.adobe.com/v/20784/)