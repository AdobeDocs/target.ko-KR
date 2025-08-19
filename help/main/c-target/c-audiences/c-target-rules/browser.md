---
keywords: 브라우저 선택 사항;유형;브라우저 유형;브라우저 언어;언어;버전;브라우저 버전
description: 페이지를 방문할 때 특정 브라우저나 특정 브라우저 옵션을 사용하는 사용자를 타깃팅하기 위해  [!DNL Adobe Target] 에서 대상을 만드는 방법에 대해 알아봅니다.
title: 브라우저 유형에 따라 방문자를 타깃팅할 수 있습니까?
feature: Audiences
exl-id: 8420bbe3-b58a-4ddb-89bb-0265dab6b5fc
source-git-commit: 784f41a73941877135a5902f2331972ba9d0e880
workflow-type: tm+mt
source-wordcount: '1015'
ht-degree: 33%

---

# [!UICONTROL Browser]

페이지를 방문할 때 특정 브라우저나 특정 브라우저 선택 사항을 사용하는 사용자를 타깃팅할 수 있습니다.

다음 브라우저를 타깃팅할 수 있습니다.

* [!UICONTROL Chrome]
* [!UICONTROL Firefox]
* [!UICONTROL Safari]
* [!UICONTROL Internet Explorer]
* [!UICONTROL Microsoft Edge]
* [!UICONTROL Opera]
* [!DNL iPad]
* [!DNL iPhone]

>[!IMPORTANT]
>
>[!DNL Target] Standard/Premium 24.3.1(2024년 3월 4~6일)부터 Target UI를 사용하여 만든 기본 제공 대상(예: `Browser:iPad` 및 `Browser:iPhone`)이 [!DNL iPad], [!DNL iPhone] 및 `profile.mobile.deviceVendor`을(를) 사용하여 `profile.mobile.isMobilePhone` 및 `profile.mobile.isTablet`에 대한 적절한 타깃팅을 수행하도록 업데이트되었습니다.
>
>이 업데이트에는 고객 측에서 작업을 수행할 필요가 없습니다. [!DNL Target] UI의 레이블은 나중에 변경되며 이러한 변경이 이루어지면 [[!DNL Target] 릴리스 노트(현재)](/help/main/r-release-notes/release-notes.md)에 발표됩니다.
>
>해결 방법 설정은 아래의 [대상 특성  [!DNL iPad] 의  [!DNL iPhone] 및[!UICONTROL Browser]업데이트(2024년 4월 30일)](#updates)를 참조하십시오.

브라우저를 타깃팅하는 방법에는 두 가지가 있습니다.

* **사전에 만들어진 대상:**&#x200B;특정 브라우저를 사용하여 사이트를 방문하는 방문자만 타깃팅하려는 경우 사전에 만들어진 대상을 사용하십시오. 예를 들어 [!DNL Chrome] 확장을 제공하는 경우 [!DNL Chrome]명의 사용자만 대상으로 합니다.

   1. 활동을 설정할 때 드롭다운 목록에서 브라우저를 선택합니다.

      이 선택 사항은 활동을 지정된 브라우저를 사용하는 방문자에게만 타깃팅합니다.

      ![Chrome 사용자 타깃팅](/help/main/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **사용자 지정된 브라우저 대상 규칙:** 사용자 지정된 대상을 사용하면 여러 브라우저를 대상으로 하거나 특정 브라우저, 브라우저 버전 또는 브라우저 언어에 대한 규칙 또는 제외를 설정할 수 있습니다. 이 기능은 브라우저 속성을 기반으로 활동을 타깃팅할 때 상당한 유연성을 제공합니다.

   1. [!DNL Target] 인터페이스에서 **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**&#x200B;을(를) 클릭합니다.
   1. 대상자의 이름을 지정하고 선택적 설명을 추가합니다.
   1. **[!UICONTROL Browser]**&#x200B;을(를) 대상 빌더로 끌어서 놓습니다.

      ![규칙 > 브라우저](assets/target_browser.png)

   1. **[!UICONTROL Select]**&#x200B;을(를) 클릭한 후 다음 옵션 중 하나를 선택합니다.

      * **유형:** 특정 브라우저를 타깃팅하거나 제외합니다. [유형](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56)을 참조하십시오.
      * **언어:** 특정 언어를 사용하도록 설정된 특정 브라우저를 타깃팅하거나 제외합니다. [언어](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1)를 참조하십시오.
      * **버전:** 특정 브라우저 버전을 타깃팅하거나 제외합니다. [버전](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF)을 참조하십시오.

   1. (선택 사항) 대상에 대한 추가 규칙을 설정합니다.
   1. **[!UICONTROL Done]** 아이콘을 클릭합니다.

  다음 예제는 버전 91 또는 92에서 [!DNL Microsoft Edge]명의 사용자를 포함하는 대상을 보여줍니다.

  ![Target Edge 91 또는 92](assets/target_edge.png)

## 브라우저 옵션 {#concept_221D8EEF53CC45AEACEB17CF336A3658}

브라우저 유형, 언어 또는 버전을 기반으로 활동 참여자를 타깃팅하거나 제외하십시오.

### 유형 {#section_6ADC758F23F145B3A310151546D83D56}

특정 브라우저를 타깃팅하거나 제외합니다.

**[!UICONTROL Type]**&#x200B;을(를) 선택한 다음 [다음과 같음] 또는 [다음과 같지 않음]을 선택하십시오.

* [!UICONTROL Equals]: 선택한 브라우저를 타깃팅합니다.
* [!UICONTROL Does not equal]: 선택한 브라우저를 제외합니다.

브라우저를 하나 이상 선택하십시오. 여러 선택 사항은 OR로 연결됩니다.

### 언어 {#section_7520D1AA464A45A6843EABE2D2B431A1}

특정 언어를 사용하도록 설정된 특정 브라우저를 타깃팅하거나 제외합니다.

예를 들어 오퍼가 영어로만 제공되는 경우 해당 언어가 영어로 설정된 브라우저를 타깃팅할 수 있습니다. 또는 페이지에 더블바이트가 활성화되어 있지 않은 경우 동아시아 언어로 설정된 브라우저를 제외할 수 있습니다.

브라우저 언어를 포함하거나 제외하면 언어가 위치보다 중요한 경우 지역을 기반으로 타깃팅하는 것보다 더 정확한 방문자 타깃팅을 수행할 수 있습니다. 예를 들어 영어로 작성된 문서를 제공하는 경우 영어 사용 국가를 타깃팅하거나 영어로 설정된 브라우저를 타깃팅할 수 있습니다. 브라우저에 타깃팅하면 영어가 기본 언어가 아닌 국가에 있는 영어 사용자가 문서를 사용할 수 있게 됩니다.

**[!UICONTROL Language]**&#x200B;을(를) 선택한 다음 [다음과 같음] 또는 [다음과 같지 않음]을 선택하십시오.

* [!UICONTROL Equals]: 선택한 브라우저 언어를 타깃팅합니다.
* [!UICONTROL Does not equal]: 선택한 브라우저 언어를 제외합니다.

언어를 하나 이상 선택하십시오. 여러 선택 사항은 OR로 연결됩니다.

다음 브라우저 언어는 타깃팅하거나 제외할 수 있습니다.

* 영어
* 프랑스어
* 독일어
* 일본어
* 한국어
* 포르투갈어
* 러시아어
* 스페인어
* 중국어 번체

### 버전 {#section_37CC8CE45DA04E8682AE6388321BA6EF}

특정 브라우저 버전을 타깃팅하거나 제외합니다.

예를 들어, 페이지가 [!DNL Internet Explorer] 버전 11 또는 이전 버전에서 올바르게 표시되지 않으면 해당 버전을 제외하는 대상을 만들 수 있습니다. 이 경우 브라우저 유형이 [!DNL Internet Explorer]인 규칙을 설정하고 버전이 11보다 작거나 같은 두 번째 규칙을 추가합니다.

**[!UICONTROL Version]**&#x200B;을(를) 선택한 다음 연산자를 선택하십시오.

* [!UICONTROL Equals]
* [!UICONTROL Does not equal]
* [!UICONTROL Is greater than]
* 다음보다 크거나 같음
* [!UICONTROL Is less than]
* [!UICONTROL Is less than or equal to]

버전 번호를 입력합니다. 텍스트 필드에는 주 버전만 입력할 수 있습니다. 지정된 버전은 해당 릴리스의 모든 부 버전이 포함되어 있습니다. 예를 들어 버전 10을 지정하는 경우 버전 10.1의 방문자도 포함됩니다.

여러 선택 사항은 OR로 연결됩니다.

## 교육 비디오: 대상자 ![튜토리얼 배지](/help/main/assets/tutorial.png) 만들기

다음 비디오에는 대상 카테고리 사용에 대한 정보가 포함되어 있습니다.

* 대상자 만들기
* 대상 카테고리 정의

>[!VIDEO](https://video.tv.adobe.com/v/17392)

## [!DNL iPad] 대상 특성의 [!DNL iPhone] 및 [!UICONTROL Browser]에 대한 업데이트(2024년 4월 30일) {#updates}

[!DNL Adobe Target]을(를) 사용하면 페이지를 방문할 때 특정 브라우저나 브라우저 옵션을 사용하는 사용자를 포함하여 [여러 범주 특성 중 하나를 타깃팅할 수 있습니다](/help/main/c-target/c-audiences/c-target-rules/target-rules.md).

[!DNL Target] Standard/Premium 24.3.1(2024년 3월 4~6일)부터 Target UI를 사용하여 만든 기본 제공 대상(예: `Browser:iPad` 및 `Browser:iPhone`)이 [!DNL iPad], [!DNL iPhone] 및 `profile.mobile.deviceVendor`을(를) 사용하여 `profile.mobile.isMobilePhone` 및 `profile.mobile.isTablet`에 대한 적절한 타깃팅을 수행하도록 업데이트되었습니다.

[!DNL Target] 및 `Browser:iPad`과(와) 같이 `Browser:iPhone` UI를 사용하여 만든 기본 제공 대상은 자동으로 새 대상 정의로 이동되며 고객 측에서 작업을 수행할 필요가 없습니다. 그러나 앞으로 [아래 설명](#ui)된 설정을 사용해야 합니다.

프로필 스크립트에서 `user.browserType`을(를) 사용하여 [!DNL iPhone] 또는 [!DNL iPad]인지(예: `user.browserType == 'iphone'` 또는 `user.browserType != 'ipad'`) 확인하는 경우 이러한 대상이 예상대로 계속 작동하도록 하려면 해당 프로필 스크립트를 2024년 4월 30일 전에 [아래 지시](#profile-scripts)로 변경해야 합니다.

JavaScript 대상은 [!DNL Target] UI에서 더 이상 사용되지 않는 [!DNL Target Classic] 식을 사용하는 레거시 대상입니다. 이러한 대상은 API를 통해서만 수정할 수 있습니다. 고객은 활동에서 이전 대상을 계속 사용하는 경우에만 이러한 대상을 업데이트해야 합니다.

### [!DNL Target] UI를 사용하여 만든 대상자 {#ui}

다음 설정을 앞으로 사용할 수 있습니다.

* **브라우저 일치 항목[!DNL Apple]**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL matches] [!DNL Apple]

  ![Apple](/help/main/r-release-notes/assets/apple.png)

* **브라우저가 태블릿과 일치함**: [!UICONTROL Mobile] > [!UICONTROL is Tablet] > [!UICONTROL true]

  ![모바일이 태블릿입니다](/help/main/r-release-notes/assets/is-tablet.png)

* **브라우저가 iPad과 일치함**: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPad] 및 [!UICONTROL Mobile] > [!UICONTROL Is Tablet]이(가) 있는 And 컨테이너는 [!DNL true]입니다.

  ![iPad](/help/main/r-release-notes/assets/ipad.png)

* **브라우저가 iPhone과 일치함**: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPhone] 및 [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone]이(가) 있는 And 컨테이너는 [!DNL true]입니다.

  ![iPhone](/help/main/r-release-notes/assets/iphone.png)

조건이 무효화된 경우 등 사용할 수 있는 다른 가능한 설정이 많이 있습니다. 무효화된 조건의 예는 다음과 같습니다.

* **브라우저가 iPhone과 일치하지 않습니다**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple]&#x200B;([!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone]이(가) 있는 Or 컨테이너는 [!UICONTROL false]임)

  ![휴대폰이 아님](/help/main/r-release-notes/assets/mobile-phone-false.png)

* **브라우저가 iPad과 일치하지 않습니다**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple]&#x200B;([!UICONTROL Mobile] > [!UICONTROL Is Tablet]이(가) 있는 Or 컨테이너는 [!UICONTROL false]임).

  ![태블릿 아님](/help/main/r-release-notes/assets/tablet-false.png)

### 프로필 스크립트를 사용하여 생성된 대상자 {#profile-scripts}

기존 `user.browserType` 대상자 또는 프로필 스크립트에서 [!DNL Target Classic]을(를) 사용하는 경우 변경 사항에 다음이 포함되어야 합니다.

* **BrowserType이 iPhone입니다**:

  바꾸기:

  `user.browserType=="iphone"`

  포함:

  `profile.mobile.deviceVendor == "Apple" && profile.mobile.isMobilePhone`

* **BrowserType이 iPhone이 아닙니다**:

  바꾸기:

  `user.browserType!="iphone"`

  포함:

  `profile.mobile.deviceVendor != "Apple" || !profile.mobile.isMobilePhone`

* **BrowserType이 iPad입니다**:

  바꾸기:

  `user.browserType=="ipad"`

  포함:

  `profile.mobile.deviceVendor == "Apple" && profile.mobile.isTablet`

* **BrowserType이 iPad이 아닙니다**:

  바꾸기:

  `user.browserType!="ipad"`

  포함:

  `profile.mobile.deviceVendor != "Apple" || !profile.mobile.isTablet`