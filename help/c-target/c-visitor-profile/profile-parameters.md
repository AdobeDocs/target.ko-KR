---
keywords: 프로필 스크립트;프로필 스크립트 속성;프로필 스크립트 우수 사례;디버그;디버깅;스크립트;프로필 스크립트;속성;속성;매개 변수
description: Adobe [!DNL Target] 활동에 사용할 수 있는 정보에 대한 정보를 제공하기 위해 방문자 프로필에 저장된 방문자별 속성에 대해 알아봅니다.
title: 프로필 속성이란 무엇입니까?
feature: 대상자
exl-id: 6c689629-bbd3-461e-9a68-5b16d4eb4250
source-git-commit: c78598da8f13f1e2c4489a317ce151779ca4be61
workflow-type: tm+mt
source-wordcount: '2403'
ht-degree: 49%

---

# 프로필 속성

[!DNL Adobe Target]의 프로필 속성은 방문자와 관련된 매개 변수입니다. 이러한 속성은 방문자의 프로필에 저장되어 활동에 사용할 수 있는 방문자에 대한 정보를 제공합니다.

사용자 프로필에는 웹 페이지 방문자의 인구 분포 및 동작 정보가 포함되어 있습니다. 이 정보에는 연령, 성별, 구매한 제품, 마지막 방문 시간 등이 포함될 수 있으며 이 정보에는 [!DNL Target]에서 방문자가 제공하는 콘텐츠를 개인화하는 데 사용하는 것입니다.

방문자가 웹 사이트를 찾아보거나 다른 세션을 위해 돌아가면 프로필에 저장된 프로필 속성을 사용하여 콘텐츠를 타깃팅하거나 세그먼트 필터링을 위해 정보를 기록할 수 있습니다.

프로필 속성을 설정하려면 다음을 수행하십시오.

1. **[!UICONTROL Audiences]** > **[!UICONTROL 프로필 스크립트를 클릭합니다.]**

   ![프로필 스크립트 탭](/help/c-target/c-visitor-profile/assets/create-script.png)

1. **[!UICONTROL 스크립트 만들기]**&#x200B;를 클릭합니다.

   ![프로필 스크립트 만들기 대화 상자](/help/c-target/c-visitor-profile/assets/profile-script.png)

   다음 유형의 프로필 속성을 사용할 수 있습니다.

   | 매개 변수 유형 | 설명 |
   |--- |--- |
   | mbox | mbox를 만들 때 페이지 코드를 통해 직접 전달됩니다. 활동에서 지리 기반의 타깃팅을 사용하는 방법에 대한 자세한 내용은 [글로벌 mbox에 매개 변수 전달](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md)을 참조하십시오.<br>**참고**:  [!DNL Target] 의 mbox 호출당 고유한 프로필 속성 제한은 50개입니다. 50개가 넘는 프로필 속성을 [!DNL Target]에 전달해야 하는 경우 프로필 업데이트 API 방법을 사용하여 전달하십시오. 자세한 내용은 API 설명서의 [ [!DNL Adobe Target] 프로필 업데이트를 참조하십시오](http://developers.adobetarget.com/api/#updating-profiles). |
   | 프로필 | JavaScript 코드 조각으로 바로 정의됩니다. 이러한 코드 조각은 소비자가 사용한 총 비용과 같은 실행 합계를 저장할 수 있으며, 각 mbox 요청에서 실행됩니다. 아래의 프로필 스크립트 속성 을 참조하십시오. |

## 프로필 스크립트 속성 {#concept_8C07AEAB0A144FECA8B4FEB091AED4D2}

연결된 JavaScript 코드 조각으로 프로필 스크립트 속성을 정의합니다.

프로필 스크립트를 사용하여 여러 방문에서 방문자 속성을 캡처할 수 있습니다. 프로필 스크립트는 서버 측 JavaScript의 한 형태를 사용하여 [!DNL Target] 내에 정의된 코드 조각입니다. 예를 들어 프로필 스크립트를 사용하여 방문자가 사이트를 방문하는 빈도와 해당 방문자가 마지막으로 방문한 시점을 캡처할 수 있습니다.

프로필 스크립트가 프로필 매개 변수와는 같지 않습니다. 프로필 매개 변수는 [!DNL Target] 의 mbox 코드 구현을 사용하여 방문자에 대한 정보를 캡처합니다.

## 프로필 스크립트 만들기 {#section_CB02F8B97CAF407DA84F7591A7504810}

프로필 스크립트는 [!UICONTROL  인터페이스의 ]대상자[!DNL Target] 탭에서 사용할 수 있습니다.

프로필 스크립트를 추가하려면 **[!UICONTROL 프로필 스크립트]** 탭, **[!UICONTROL 스크립트 만들기]**&#x200B;를 클릭한 다음 스크립트를 작성합니다.

또는

기존 프로필 스크립트를 복사하려면 [!UICONTROL 프로필 스크립트] 목록에서 원하는 스크립트의 줄임표 아이콘을 클릭한 다음 **[!UICONTROL 복제]**&#x200B;를 클릭합니다.

그러면 대상을 편집하여 유사한 대상을 만들 수 있습니다.

프로필 스크립트는 각 위치 요청에서 프로필 속성 &quot;catchers&quot;를 실행합니다. 위치 요청이 수신되면 [!DNL Target]은 실행해야 하는 활동을 결정하고 해당 활동 및 해당 경험에 적합한 콘텐츠를 표시합니다. [!DNL Target] 또한 활동의 성공을 추적하고 모든 관련 프로필 스크립트를 실행합니다. 이 프로세스를 통해 방문자의 위치, 시간, 방문자가 이전에 구매한 경우 등 방문에 대한 정보를 추적할 수 있습니다. 그런 다음 이러한 정보가 방문자의 프로필에 추가되므로 방문자의 사이트 활동을 더 잘 추적할 수 있습니다.

프로필 스크립트 속성은 속성 이름 앞에 `user.` 태그가 삽입되어 있습니다. 예:

```
if (mbox.name == 'Track_Interest') { 
    if (profile.get('model') == "A5" &&; profile.get('subcat') == "KS6") { 
        return (user.get('A5KS6') || 0) + 1; 
    } 
}
```

다음 정보에 주의하십시오.

* `user.get('parameterName')`을 사용하는 코드에서 프로필 스크립트 속성(자신 포함)을 참조하십시오.
* 다음 mbox 요청에서 `user.setLocal('variable_name', 'value')`으로 스크립트가 다음에 실행될 때 액세스할 수 있는 변수를 저장합니다. `user.getLocal('variable_name')`을 사용하여 변수를 참조합니다. 이 프로세스는 마지막 요청의 날짜와 시간을 참조하려는 경우에 유용합니다.
* 매개 변수와 값은 대/소문자를 구분합니다. 활동이나 테스트 중에 받은 매개 변수 및 값의 대소문자를 맞추십시오.
* 자세한 JavaScript 구문에 대해서는 아래의 &quot;스크립트 프로필 매개 변수에 대해 JavaScript 참조&quot; 섹션을 참조하십시오.
* 매개 변수는 스크립트를 비활성화한 후 프로필에 유지됩니다. 이미 프로필에 활동 대상에 사용되는 매개 변수가 포함된 사용자는 해당 활동에서 자격을 갖습니다.
* 프로필 스크립트는 활동에서 사용되는 동안에는 삭제할 수 없습니다.
* 다른 프로필 스크립트에서 한 프로필 스크립트의 결과를 사용하는 종속 프로필 스크립트를 만들지 않는 것이 좋습니다. 프로필 스크립트 실행 순서는 보장되지 않습니다.

## 프로필 스크립트 정보 카드 보기 {#section_18EA3B919A8E49BBB09AA9215E1E3F17}

오퍼 정보 카드와 유사한 프로필 스크립트 정보 팝업 카드를 볼 수 있습니다. 이러한 프로필 스크립트 정보 카드를 사용하면 선택한 프로필 스크립트를 참조하는 활동 목록과 함께 다른 유용한 메타데이터를 볼 수 있습니다.

예를 들어, 다음 프로필 스크립트 정보 카드는 목록에서 원하는 프로필 스크립트에 대한 [!UICONTROL 정보] 아이콘을 클릭하여 액세스합니다([!UICONTROL 대상] > [!UICONTROL 프로필 스크립트]).

[!UICONTROL 스크립트 정보] 탭에는 다음 정보가 포함되어 있습니다. 이름, 설명 및 스크립트 코드입니다.

![프로필 스크립트 정보 카드](assets/profile_script_info_card.png)

**[!UICONTROL 전체 세부 정보 보기]**&#x200B;를 클릭하여 선택한 프로필 스크립트를 참조하는 대상 및 활동을 확인합니다.

![프로필 스크립트 정보 카드 > 스크립트 사용 탭](assets/profile_script_info_card_usage_tab.png)

>[!NOTE]
>
>[!UICONTROL 스크립트 사용] 탭에는 다음 상황에서 선택한 프로필 스크립트를 참조하는 활동이 표시되지 않습니다.
>
> * 활동이 [!UICONTROL 초안] 상태입니다.
> * 활동에 사용된 콘텐츠 또는 오퍼가 스크립트 변수(활동 내의 인라인 오퍼 또는 오퍼 라이브러리 내의 오퍼)를 사용합니다.


## Target이 프로필 스크립트를 비활성화하는 특정 상황 {#section_C0FCB702E60D4576AD1174D39FBBE1A7}

[!DNL Target] 프로필 스크립트가 실행하는 데 너무 오래 걸리거나 너무 많은 명령어를 포함하고 있는 경우와 같은 특정 상황에서 프로필 스크립트를 자동으로 비활성화합니다.

프로필 스크립트를 비활성화하는 경우, 아래 그림과 같이 Target UI의 프로필 스크립트 옆에 노란색 경고 아이콘이 표시됩니다.

![](assets/profile_script_invalid.png)

마우스로 가리키면 아래 그램과 같이 오류에 대한 세부 사항이 표시됩니다.

![](assets/profile_script_hover.png)

시스템이 프로필 스크립트를 비활성화하는 일반적인 이유는 다음과 같습니다.

* 정의되지 않은 변수가 참조되었습니다.
* 올바르지 않은 값이 참조되었습니다. 이 오류는 적절한 유효성 검사 없이 URL 값 및 기타 사용자 입력 데이터를 참조하여 발생하는 경우가 많습니다.
* 너무 많은 JavaScript 명령어가 사용되었습니다. [!DNL Target] 에는 스크립트당 2,000개의 JavaScript 지침이 있지만 JavaScript를 수동으로 읽는 것만으로는 이 제한을 계산할 수 없습니다. 예를 들어 Rhino는 모든 함수 호출 및 &quot;새로운&quot; 호출을 100개의 명령어로 처리합니다. 모든 함수에 대한 호출에는 100개의 지침이 사용됩니다. 또한 URL 값과 같은 임의 항목 데이터의 크기는 명령어 개수에 영향을 줄 수 있습니다.
* 아래의 [우수 사례](/help/c-target/c-visitor-profile/profile-parameters.md#section_64AFE5D2B0C8408A912FC2A832B3AAE0) 섹션에서 강조 표시된 항목을 따르지 않습니다.

## 우수 사례 {#best}

다음 지침은 시스템 스크립트 중지를 강제하지 않고 스크립트가 처리되도록 정상적으로 실패하는 코드를 작성하여 가능한 한 오류 실패가 없는 간소화된 프로필 스크립트를 작성하기 위한 것입니다. 이러한 지침은 효율적으로 실행되는 것으로 입증된 우수 사례의 결과이며, Rhino 개발 커뮤니티에서 작성된 원칙 및 권장 사항과 함께 적용됩니다.

* 현재 스크립트 값을 사용자 스크립트에서 로컬 변수로 설정하고 페일오버를 빈 문자열로 설정합니다.
* 빈 문자열이 아니도록 하여 로컬 변수의 유효성을 확인합니다.
* 문자열 기반 조작 함수와 정규 표현식을 사용합니다.
* 제한된 for 루프와 개방된 for 또는 while 루프를 비교 사용합니다.
* 1,300자 또는 50개 루프 반복을 초과하지 않도록 합니다.
* JavaScript 명령어 2,000개를 초과하지 않도록 합니다. [!DNL Target] 에는 스크립트당 2,000개의 JavaScript 지침이 있지만 JavaScript를 수동으로 읽는 것만으로는 이 제한을 계산할 수 없습니다. 예를 들어 Rhino는 모든 함수 호출 및 &quot;새로운&quot; 호출을 100개의 명령어로 처리합니다. 또한 URL 값과 같은 임의 항목 데이터의 크기는 명령어 개수에 영향을 줄 수 있습니다.
* 스크립트 성능뿐만 아니라 모든 스크립트를 결합한 성능에 주의하십시오. 가장 좋은 방법으로서, [!DNL Adobe]은 총 5,000개 이하의 지침을 권장합니다. 명령 수를 카운트하는 것은 분명하지 않지만, 2,000개가 넘는 스크립트는 자동으로 비활성화됩니다. 활성 프로필 스크립트 수는 300개를 초과할 수 없습니다. 각 스크립트는 모든 단일 mbox 호출로 실행됩니다. 필요만 만큼만 스크립트를 실행합니다.
* 정규 표현식에서 시작 부분에 점-별이 있음(예: `/.*match/`, `/a|.*b/`)은 거의 필요하지 않습니다. 정규 표현식 검색은 `^`으로 묶이지 않는 한 문자열의 모든 위치에서 시작하므로 이미 점-별이 가정되었습니다. 그러한 정규 표현식이 충분히 긴 입력 데이터(최저 700자까지 가능)와 일치하면 스크립트 실행이 중단될 수 있습니다.
* 모두 실패하는 경우 try/catch에 스크립트를 래핑합니다.
* 다음 권장 사항을 사용하면 프로필 스크립트의 복잡성을 줄이는 데 도움이 될 수 있습니다. 프로필 스크립트는 제한된 수의 지침을 실행할 수 있습니다.

   우수 사례:

   * 프로필 스크립트를 가능한 한 작게 유지합니다.
   * 정규 표현식을 사용하지 않거나 간단한 정규 표현식만 사용하십시오. 간단한 표현이라도 여러 가지 지침을 따라 평가할 수 있습니다.
   * 재귀를 피하십시오.
   * 프로필 스크립트는 [!DNL Target]에 추가되기 전에 성능 테스트를 거쳐야 합니다. 모든 프로필 스크립트는 모든 mbox 요청에서 실행됩니다. 프로필 스크립트가 올바르게 실행되지 않으면 mbox 요청을 실행하는 데 시간이 더 오래 걸리며 트래픽 및 전환에 영향을 줄 수 있습니다.
   * 프로필 스크립트가 너무 복잡해지면 대신 [응답 토큰](/help/administrating-target/response-tokens.md)을 사용해 보십시오.

* 자세한 내용은 JS Rhino 엔진 설명서 를 참조하십시오.

## 프로필 스크립트 디버그 {#section_E9F933DE47EC4B4E9AF2463B181CE2DA}

다음 메서드를 사용하여 프로필 스크립트를 디버그할 수 있습니다.

>[!NOTE]
>
>프로필 스크립트는 서버 측에서 실행되므로, 프로필 스크립트 내에 [!DNL console.log]을 사용하면 프로필 값이 출력되지 않습니다.

* **프로필 스크립트를 응답 토큰으로 추가하여 프로필 스크립트 디버그:**

   [!DNL Target]에서 **[!UICONTROL 관리]**&#x200B;를 클릭하고 **[!UICONTROL 응답 토큰]**&#x200B;을 클릭한 다음 디버그하려는 프로필 스크립트를 활성화합니다.

   [!DNL Target] 이 있는 사이트의 페이지를 로드할 때마다 [!DNL Target] 응답의 일부에 지정된 프로필 스크립트에 대한 값이 다음과 같이 포함됩니다.

   ![](assets/debug_profile_script_1.png)

* **mboxTrace 디버깅 도구를 사용하여 프로필 스크립트를 디버깅합니다.**

   이 메서드는 **[!UICONTROL Target]** > **[!UICONTROL 관리]** > **[!UICONTROL 구현]** > **[!UICONTROL 디버거 도구] 섹션에서 인증 토큰 생성]**&#x200B;을 클릭하여 생성할 수 있는 승인 토큰이 필요합니다.[!UICONTROL 

   그런 다음 &quot;?&quot; 뒤에 있는 페이지 URL에 다음 두 매개 변수를 추가합니다. `mboxTrace=window&authorization=YOURTOKEN`

   이러한 매개 변수를 추가하면 사전 실행된 스냅샷과 프로필의 사후 스냅숏이 표시되므로 응답 토큰보다 훨씬 더 도움이 됩니다. 사용 가능한 모든 프로필도 표시됩니다.

   ![](assets/debug_profile_script_2.png)

## 프로필 스크립트 FAQ {#section_1389497BB6D84FC38958AE43AAA6E712}

**이 프로필 스크립트를 사용하여 데이터 계층에 있는 페이지에서 정보를 캡처할 수 있습니까?**

프로필 스크립트는 서버 측을 실행하므로 페이지를 직접 읽을 수 없습니다. 데이터는 mbox 요청 또는 데이터를 Target으로 가져오는 다른 방법을 통해 [](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17) 전달해야 합니다. 데이터가 [!DNL Target]에 있으면 프로필 스크립트는 mbox 매개 변수 또는 프로필 매개 변수로 데이터를 읽을 수 있습니다.

## 스크립트 프로필 매개 변수에 대해 JavaScript 참조

스크립트 프로필을 효과적으로 사용하려면 간단한 Javascript 지식이 필요합니다
매개 변수. 이 섹션은 단 몇 분 만에 이 기능을 사용하여 생산성을 발휘하는 데 도움이 되는 빠른 참조 역할을 합니다.

스크립트 프로필 매개 변수는 mbox/프로필 탭 아래에 있습니다. Javascript 유형(문자열, 정수, 배열 등)을 반환하는 Javascript 프로그램을 작성할 수 있습니다.

### 스크립트 프로필 매개 변수 예 {#examples}

**이름:** *user.recency*

```
var dayInMillis = 3600 * 24 * 1000;
if (mbox.name == 'orderThankyouPage') {
    user.setLocal('lastPurchaseTime', new Date().getTime());
}
var lastPurchaseTime = user.getLocal('lastPurchaseTime');
if (lastPurchaseTime) {
    return ((new Date()).getTime() - lastPurchaseTime) / dayInMillis;
}
```

측정된 일에 대한 변수(밀리초)를 만듭니다. mbox 이름이 `orderThankyouPage`이면 `lastPurchaseTime`라는 로컬(보이지 않음) 사용자 프로필 속성을 설정하여 현재 날짜 및 시간 값을 표시합니다. 마지막 구매 시간 값을 읽고, 정의된 경우 [!DNL Target] 은 마지막 구매 시간 이후 경과된 시간을 하루의 밀리초 수로 나누어서 반환합니다(마지막 구매 이후 일수).

**이름:** *user.frequency*

```
var frequency = user.get('frequency') || 0;
if (mbox.name == 'orderThankyouPage') {
    return frequency + 1;
}
```

이전 값이 없는 경우 이전 값 또는 0으로 초기화하는 `frequency` 변수를 만듭니다. mbox 이름이 `orderThankyouPage`이면 증분 값이 반환됩니다.

**이름:** *user.monetaryValue*

```
var monetaryValue = user.get('monetaryValue') || 0;
if (mbox.name == 'orderThankyouPage') {
    return monetaryValue + parseInt(mbox.param('orderTotal'));
}
```

지정된 방문자에 대한 현재 값을 조회(또는 이전 값이 없는 경우 0으로 설정)하는 `monetaryValue`라는 변수를 만듭니다. mbox 이름이 `orderThankyouPage`이면 이전 통화 값과 mbox에 전달된 `orderTotal` 매개 변수의 값을 추가하여 새 통화 값이 반환됩니다.

**이름:** adobeQA

```
if (page.param("adobeQA"))
     return page.param("adobeQA");
else if (page.param("adobeqa"))
     return page.param("adobeqa");
else if (mbox.param("adobeQA"))
     return mbox.param("adobeQA");
```

[활동 QA](/help/c-activities/c-activity-qa/activity-qa.md)에 대한 사용자를 추적하기 위해 `adobeQA`라는 변수를 만듭니다.

### 개체 및 메서드

스크립트 프로필 매개 변수에서 다음 속성 및 메서드를 참조할 수 있습니다.

| 개체 또는 메서드 | 세부 사항 |
| --- | --- |
| `page.url` | 현재 URL입니다. |
| `page.protocol` | 페이지에 사용된 프로토콜(http, https)입니다. |
| `page.domain` | 현재 URL 도메인(첫 번째 슬래시 앞에 있는 모든 것)입니다. 예: `http://www.acme.com/categories/men_jeans?color=blu e&size=small`에서 `www.acme.com`. |
| `page.query` | 현재 페이지에 대한 쿼리 문자열입니다. &#39;?&#39; 뒤에 있는 모든 것입니다. 예: `http://www.acme.com/categories/mens_jeans?color=blue&size=small`에서 `blue&size=small`. |
| `page.param(‘<par_name>’)` | `<par_name>`으로 표시된 매개 변수의 값입니다. 현재 URL이 Google의 검색 페이지이고 `page.param('hl')`을 입력한 경우, URL `http://www.google.com/search?hl=en& q=what+is+asdf&btnG=Google+Search`에 대해 “en”이 표시됩니다. |
| `page.referrer` | 위와 동일한 일련의 작업이 레퍼러 및 랜딩에 적용됩니다(referrer.url이 레퍼러의 URL 주소). |
| `landing.url`, `landing.protocol`, `landing.query`, 및 `landing.param` | 페이지의 값과 비슷하지만 랜딩 페이지용입니다. |
| `mbox.name` | 활성 mbox 이름입니다. |
| `mbox.param(‘<par_name>’)` | 활성 mbox에서 제공된 이름의 mbox 매개 변수입니다. |
| `profile.get(‘<par_name>’)` | `<par_name>`이라는 이름으로 클라이언트가 생성한 사용자 프로필 매개 변수입니다. 예를 들어 사용자가 &quot;gender&quot;라는 프로필 매개 변수를 설정하면 &quot;profile.gender&quot;를 사용하여 값을 추출할 수 있습니다. 현재 방문자에 대해 설정된 &quot;`profile.<par_name>`&quot; 값을 반환합니다. 설정된 값이 없으면 null를 반환합니다. `profile.get(<par_name>)`은 함수 호출로 검증됩니다. |
| `user.get(‘<par_name>’)` | 현재 방문자에 대해 설정된 &quot;`user.<par_name>`&quot; 값을 반환합니다. 설정된 값이 없으면 null를 반환합니다. |
| `user.categoryAffinity` | 가장 적합한 카테고리의 이름을 반환합니다. |
| `user.categoryAffinities` | 가장 적합한 카테고리가 있는 배열을 반환합니다. |
| `user.isFirstSession` | 방문자의 첫 번째 세션인 경우 true를 반환합니다. |
| `user.browser` | HTTP 헤더에서 사용자-에이전트를 반환합니다. 예를 들어 Safari 사용자만 대상으로 하는 표현식 타겟을 만들 수 있습니다. `if (user.browser != null && user.browser.indexOf('Safari') != -1) { return true; }` |

### 일반 연산자


모든 표준 JavaScript 연산자가 존재하며 사용할 수 있습니다. JavaScript 연산자는 문자열 및 숫자(및 기타 데이터 유형)에서 사용할 수 있습니다. 요약하면 다음과 같습니다.

| 연산자 | 설명 |
| --- | --- |
| `==` | 같음을 나타냅니다. 양쪽에 있는 피연산자가 동일한 경우 true입니다. |
| `!=` | 같지 않음을 나타냅니다. 양쪽에 있는 피연산자가 동일하지 않은 경우 true입니다. |
| `<` | 왼쪽에 있는 변수가 오른쪽에 있는 변수보다 작음을 나타냅니다. 변수가 동일한 경우 false로 평가됩니다. |
| `>` | 왼쪽의 변수가 오른쪽의 변수보다 큼을 나타냅니다. 변수가 동일한 경우 false로 평가됩니다. |
| `<=` | 변수가 동일한 경우를 제외하고 `<`과 동일하면 true로 평가됩니다. |
| `>=` | 변수가 동일한 경우를 제외하고 `>`과 동일하면 true로 평가됩니다. |
| `&&` | 표현식의 왼쪽과 오른쪽에 있는 논리적 &quot;AND&quot;는 양쪽이 true인 경우에만 true이고, 그렇지 않으면 false입니다. |
| `||` | 표현식의 왼쪽과 오른쪽에 있는 논리적 &quot;OR&quot;은 한쪽이 true인 경우에만 true이고, 그렇지 않으면 false입니다. |
| `//` | 부울에 포함된 타겟의 모든 요소(Array source, Array target)가 소스에 포함되어 있는지 확인합니다.<br>`//`는 타겟(regexp에 해당함)에서 하위 문자열을 추출하여 `Array/*String*/ decode(String encoding, String regexp, String target)`로 디코딩합니다.<br>이 기능은 상수 문자열 값, 그룹화(`condition1 || condition2) && condition3` 및 정규식(`/[^a-z]$/.test(landing.referring.url)` 사용을 지원합니다. |

## 교육 비디오: 프로필 스크립트 ![자습서 배지](/help/assets/tutorial.png)

다음 비디오에는 프로필 스크립트 사용 및 작성에 대한 정보가 포함되어 있습니다.

* 프로필 스크립트가 무엇인지 설명
* 프로필 스크립트와 프로필 매개 변수의 차이점 설명
* 간단한 프로필 스크립트 만들기
* 사용 가능한 토큰 메뉴를 사용하여 사용 가능한 선택 사항에 액세스
* 프로필 스크립트 활성화 및 비활성화

>[!VIDEO](https://video.tv.adobe.com/v/17394)
