---
keywords: 브라우저 선택 사항;유형;브라우저 유형;브라우저 언어;언어;버전;브라우저 버전
description: 에서 대상자를 만드는 방법을 알아봅니다. [!DNL Adobe Target] 페이지를 방문할 때 특정 브라우저나 특정 브라우저 선택 사항을 사용하는 사용자를 타깃팅합니다.
title: 브라우저 유형에 따라 방문자를 타깃팅할 수 있습니까?
feature: Audiences
exl-id: 8420bbe3-b58a-4ddb-89bb-0265dab6b5fc
source-git-commit: c79b1d40e0bf0495dc3f3d5accd196f14d18b934
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 53%

---

# 브라우저

페이지를 방문할 때 특정 브라우저나 특정 브라우저 선택 사항을 사용하는 사용자를 타깃팅할 수 있습니다.

다음 브라우저를 타깃팅할 수 있습니다.

* Chrome
* Firefox
* Safari
* Internet Explorer
* Microsoft Edge
* Opera
* iPad
* iPhone

>[!IMPORTANT]
>
>2024년 4월 30일부터 iPad 및 iPhone이 사용 가능한 항목에서 제거됩니다 [!UICONTROL 브라우저] 대상의 범주를 만들 때 드롭다운 목록을 입력합니다. 해결 방법 설정에 대해서는 을 참조하십시오. [브라우저 대상 속성에서 iPad 및 iPhone 사용 중단(2024년 4월 30일)](#deprecation) 아래요.

브라우저를 타깃팅하는 방법에는 두 가지가 있습니다.

* **사전에 만들어진 대상:**&#x200B;특정 브라우저를 사용하여 사이트를 방문하는 방문자만 타깃팅하려는 경우 사전에 만들어진 대상을 사용하십시오. 예를 들어 Chrome 확장 프로그램을 제공하는 경우 Chrome 사용자만 타깃팅할 수 있습니다.

   1. 활동을 설정할 때 드롭다운 목록에서 브라우저를 선택합니다.

      이 선택 사항은 활동을 지정된 브라우저를 사용하는 방문자에게만 타깃팅합니다.

      ![Chrome 사용자 타기팅](/help/main/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **사용자 지정된 브라우저 대상 규칙:** 사용자 지정된 대상을 사용하면 여러 브라우저를 타깃팅하거나 특정 브라우저, 브라우저 버전 또는 브라우저 언어에 대한 규칙 또는 제외를 설정할 수 있습니다. 이 기능은 브라우저 속성을 기반으로 활동을 타깃팅할 때 상당한 유연성을 제공합니다.

   1. 다음에서 [!DNL Target] 인터페이스, 클릭 **[!UICONTROL 대상]** > **[!UICONTROL 대상자 만들기]**.
   1. 대상자의 이름을 지정하고 선택적 설명을 추가합니다.
   1. 드래그 앤 드롭 **[!UICONTROL 브라우저]** 대상 빌더로 이동합니다.

      ![규칙 > 브라우저](assets/target_browser.png)

   1. **[!UICONTROL 선택]**&#x200B;을 클릭한 후, 다음 선택 사항 중 하나를 선택합니다.

      * **유형:** 특정 브라우저를 타깃팅하거나 제외합니다. [유형](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56)을 참조하십시오.
      * **언어:** 특정 언어를 사용하도록 설정된 특정 브라우저를 타깃팅하거나 제외합니다. [언어](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1)를 참조하십시오.
      * **버전:** 특정 브라우저 버전을 타깃팅하거나 제외합니다. [버전](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF)을 참조하십시오.

   1. (선택 사항) 대상에 대한 추가 규칙을 설정합니다.
   1. **[!UICONTROL 완료를 클릭합니다]**.

  다음 예는 버전 91 또는 92의 Microsoft Edge 사용자를 포함하는 대상을 보여줍니다.

  ![Target Edge 91 또는 92](assets/target_edge.png)

## 브라우저 선택 사항 {#concept_221D8EEF53CC45AEACEB17CF336A3658}

브라우저 유형, 언어 또는 버전을 기반으로 활동 참여자를 타깃팅하거나 제외하십시오.

### 유형 {#section_6ADC758F23F145B3A310151546D83D56}

특정 브라우저를 타깃팅하거나 제외합니다.

**[!UICONTROL 유형]**&#x200B;을 선택한 다음, [다음과 같음] 또는 [다음과 같지 않음]을 선택하십시오.

* 다음과 같음: 선택한 브라우저를 타깃팅합니다.
* 다음과 같지 않음: 선택한 브라우저를 제외합니다.

브라우저를 하나 이상 선택하십시오. 여러 선택 사항은 OR로 연결됩니다.

### 언어 {#section_7520D1AA464A45A6843EABE2D2B431A1}

특정 언어를 사용하도록 설정된 특정 브라우저를 타깃팅하거나 제외합니다.

예를 들어 오퍼가 영어로만 제공되는 경우 해당 언어가 영어로 설정된 브라우저를 타깃팅할 수 있습니다. 또는 페이지에 더블바이트가 활성화되어 있지 않은 경우 동아시아 언어로 설정된 브라우저를 제외할 수 있습니다.

브라우저 언어를 포함하거나 제외하면 언어가 위치보다 중요한 경우 지역을 기반으로 타깃팅하는 것보다 더 정확한 방문자 타깃팅을 수행할 수 있습니다. 예를 들어 영어로 작성된 문서를 제공하는 경우 영어 사용 국가를 타깃팅하거나 영어로 설정된 브라우저를 타깃팅할 수 있습니다. 브라우저에 타깃팅하면 영어가 기본 언어가 아닌 국가에 있는 영어 사용자가 문서를 사용할 수 있게 됩니다.

**[!UICONTROL 언어]**&#x200B;를 선택한 다음, [다음과 같음] 또는 [다음과 같지 않음]을 선택하십시오.

* 다음과 같음: 선택한 브라우저 언어를 타깃팅합니다.
* 다음과 같지 않음: 선택한 브라우저 언어를 제외합니다.

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

예를 들어, 페이지가 Internet Explorer 버전 11 이하에서 올바르게 표시되지 않는 경우 해당 버전을 제외하는 대상을 만들 수 있습니다. 이 경우 브라우저 유형이 Internet Explorer와 같은 규칙을 설정하고 버전이 11 이하인 두 번째 규칙을 추가하십시오.

**[!UICONTROL 버전]**&#x200B;을 선택한 다음 연산자를 선택하십시오.

* 다음과 같음
* 다음과 같지 않음
* 다음보다 큼
* 다음보다 크거나 같음
* 다음보다 작음
* 다음보다 작거나 같음

버전 번호를 입력합니다. 텍스트 필드에는 주 버전만 입력할 수 있습니다. 지정된 버전은 해당 릴리스의 모든 부 버전이 포함되어 있습니다. 예를 들어 버전 10을 지정하는 경우 버전 10.1의 방문자도 포함됩니다.

여러 선택 사항은 OR로 연결됩니다.

## 교육 비디오: 대상자 만들기 ![튜토리얼 배지](/help/main/assets/tutorial.png)

다음 비디오에는 대상 카테고리 사용에 대한 정보가 포함되어 있습니다.

* 대상자 만들기
* 대상 카테고리 정의

>[!VIDEO](https://video.tv.adobe.com/v/17392)

## 브라우저 대상자 속성에서 iPad 및 iPhone 사용 중단(2024년 4월 30일) {#deprecation}

[!DNL Adobe Target] 다음 작업을 수행할 수 있습니다. [여러 범주 속성 중 하나를 타깃팅합니다.](/help/main/c-target/c-audiences/c-target-rules/target-rules.md): 페이지를 방문할 때 특정 브라우저나 브라우저 선택 사항을 사용하는 사용자를 포함합니다.

2024년 4월 30일부터 iPad 및 iPhone이 사용 가능한 항목에서 제거됩니다 [!UICONTROL 브라우저] 대상의 범주를 만들 때 드롭다운 목록을 입력합니다.

[!UICONTROL 브라우저] 속성을 사용하여 iPad 또는 iPhone을 타겟팅하는 대상자가 있는 경우, 이러한 대상자가 예상대로 계속 작동하도록 하려면 2024년 4월 30일 이전에 이러한 설정을 변경해야 합니다.

### 를 사용하여 생성된 대상자 [!DNL Target] UI

다음 설정을 앞으로 사용할 수 있습니다.

* **브라우저 일치의 경우[!DNL Apple]**: [!UICONTROL 모바일] > [!UICONTROL 장치 공급업체] [!UICONTROL 일치] [!DNL Apple]

  ![Apple](/help/main/r-release-notes/assets/apple.png)

* **브라우저가 태블릿과 일치하면**: [!UICONTROL 모바일] > [!UICONTROL 태블릿임] > [!UICONTROL true]

  ![모바일이 태블릿입니다](/help/main/r-release-notes/assets/is-tablet.png)

* **브라우저가 iPad과 일치함**: [!UICONTROL 모바일] > [!UICONTROL 장치 마케팅 이름] [!UICONTROL 일치] [!DNL iPad] 및 컨테이너 포함 [!UICONTROL 모바일] > [!UICONTROL 태블릿임] 은(는) [!DNL true]

  ![iPad](/help/main/r-release-notes/assets/ipad.png)

* **브라우저가 iPhone과 일치함**: [!UICONTROL 모바일] > [!UICONTROL 장치 마케팅 이름] [!UICONTROL 일치] [!DNL iPhone] 및 컨테이너 포함 [!UICONTROL 모바일] > [!UICONTROL 휴대 전화임] 은(는) [!DNL true]

  ![iPhone](/help/main/r-release-notes/assets/iphone.png)

조건이 무효화된 경우 등 사용할 수 있는 다른 가능한 설정이 많이 있습니다. 무효화된 조건의 예는 다음과 같습니다.

* **의 브라우저가 iPhone과 일치하지 않음**: [!UICONTROL 모바일] > [!UICONTROL 장치 공급업체] [!UICONTROL 다음과 일치하지 않음] [!UICONTROL Apple] 또는 컨테이너가 있는 [!UICONTROL 모바일] > [!UICONTROL 휴대 전화임] 은(는) [!UICONTROL false]

  ![휴대폰 아님](/help/main/r-release-notes/assets/mobile-phone-false.png)

* **의 브라우저가 iPad과 일치하지 않음**: [!UICONTROL 모바일] > [!UICONTROL 장치 공급업체] [!UICONTROL 다음과 일치하지 않음] [!UICONTROL Apple] 또는 컨테이너가 있는 [!UICONTROL 모바일] > [!UICONTROL 태블릿임] 은(는) [!UICONTROL false].

  ![타블렛 아님](/help/main/r-release-notes/assets/tablet-false.png)

### 프로필 스크립트를 사용하여 생성된 대상자

를 사용하는 경우 `user.browserType` 에 설명된 대로 JavaScript 세그먼트 [프로필 및 변수 용어집](/help/main/c-target/c-visitor-profile/variables-profiles-parameters-methods.md)변경 사항에는 다음 사항이 포함되어야 합니다.

>[!NOTE]
>
>다음 프로필은 2024년 1월 24일부터 며칠 내에 공개될 예정입니다. 다음 [최신 릴리스 정보](/help/main/r-release-notes/release-notes.md) 이 프로필을 사용할 수 있게 되면 업데이트됩니다.

이러한 프로파일을 사용하면 다음과 같은 변경이 가능합니다.
>>
* `profile.mobile.isTablet`
>>
* `profile.mobile.isMobilePhone`

* **BrowserType이 iPhone임**:

  바꾸기:

  `user.browserType=="iphone"`

  포함:

  `profile.mobile.deviceVendor == "Apple" && profile.mobile.isMobilePhone`

* **BrowserType이 iPhone이 아님**:

  바꾸기:

  `user.browserType!="iphone"`

  포함:

  `profile.mobile.deviceVendor != "Apple" || !profile.mobile.isMobilePhone`

* **BrowserType이 iPad임**:

  바꾸기:

  `user.browserType=="ipad"`

  포함:

  `profile.mobile.deviceVendor == "Apple" && profile.mobile.isTablet`

* **BrowserType이 iPad이 아님**:

  바꾸기:

  `user.browserType!="ipad"`

  포함:

  `profile.mobile.deviceVendor != "Apple" || !profile.mobile.isTablet`