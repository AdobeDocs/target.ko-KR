---
keywords: spa vec;react;angular;react.js;spa visual experience composer;spa experience composer options;single page apps;single-page-app;spa;mobile experience options;target view
description: Adobe Target에서 SPA(단일 페이지 앱)용 VEC(시각적 경험 작성기)를 사용하면 마케터가 지속적인 개발에 의존하지 않고 자체적인 방식으로 SPA에 대한 테스트를 만들고 콘텐츠를 개인화할 수 있습니다. VEC는 React 및 Angular와 같은 가장 인기 있는 프레임워크의 활동을 작성하는 데 사용할 수 있습니다.
title: SPA(단일 페이지 앱) 시각적 경험 작성기
feature: spa vec
topic: Standard
uuid: 4dcd6d9c-b2e3-4759-a2e0-3696c572faba
translation-type: tm+mt
source-git-commit: e18f18e6d6e0b8fc6eb5ada845e2fe5377d6c5d0
workflow-type: tm+mt
source-wordcount: '3692'
ht-degree: 93%

---


# SPA(단일 페이지 앱) 시각적 경험 작성기 {#single-page-app-spa-visual-experience-composer}

[!DNL Adobe Target]에서 [!UICONTROL 시각적 경험 작성기] (VEC)는 마케터에게 Adobe Target의 글로벌 mbox를 통해 기존의 다중 페이지 애플리케이션에 동적으로 전달할 수 있는 경험을 개인화하고 활동을 만들 수 있는 DIY 기능을 제공합니다. 하지만, 이것은 아래 다이어그램에 표시된 것처럼, 지연을 초래하는 페이지 로드 또는 후속 서버 호출에서의 오퍼 검색에 의존합니다. 이 접근 방식은 사용자 경험과 애플리케이션 성능을 저하하므로 단일 페이지 애플리케이션(SPA)에서는 잘 작동하지 않습니다.

![기존 라이프사이클과 SPA 라이프사이클 비교](/help/c-experiences/assets/trad-vs-spa.png)

최신 릴리스에서는 SPA용 VEC를 도입했습니다. SPA용 VEC를 사용하면 마케터가 지속적인 개발에 의존하지 않고 자체적인 방식으로 SPA에 대한 테스트를 만들고 콘텐츠를 개인화할 수 있습니다. VEC는 React 및 Angular와 같이 인기 있는 프레임워크의 [A/B 테스트](/help/c-activities/t-test-ab/test-ab.md) 및 [경험 타깃팅](/help/c-activities/t-experience-target/experience-target.md) (XT) 활동을 만드는 데 사용할 수 있습니다.

## Adobe Target 보기 및 단일 페이지 애플리케이션

SPA용 Adobe Target VEC는 &quot;보기&quot;라는 새로운 개념(예: SPA 경험을 함께 구성하는 시각적 요소의 논리 그룹)을 활용합니다. 따라서 SPA는 사용자 상호 작용을 기반으로 하여 URL 대신 보기를 통해 전환으로 간주할 수 있습니다. &quot;보기&quot;는 일반적으로 전체 사이트를 나타내거나 사이트 내의 그룹화된 시각적 요소를 나타낼 수 있습니다.

&quot;보기&quot;에 대해 더 설명하기 위해 React에 구현된 이러한 가상의 온라인 전자 상거래 사이트를 탐색하고 몇 가지 &quot;보기&quot; 예를 살펴보겠습니다. 아래 링크를 클릭하여 새 브라우저 탭에서 이 사이트를 엽니다.

**링크: [홈 사이트](https://target.enablementadobe.com/react/demo/#/)**

![홈 사이트](/help/c-experiences/assets/home.png)

홈 사이트로 이동하면 사이트에서 판매되는 최신 제품과 부활절 판매를 홍보하는 영웅 이미지가 바로 표시됩니다. 이 경우 보기는 전체 홈 사이트로 정의할 수 있습니다. 아래의 Adobe Target 보기 구현 섹션에서 이에 대해 자세히 설명할 예정이므로 이것은 기록해 두면 편리합니다.

**링크: [제품 사이트](https://target.enablementadobe.com/react/demo/#/products)**

![제품 사이트](/help/c-experiences/assets/product-site.png)

제품에 대한 관심이 높아짐에 따라 제품 링크를 클릭하기로 했습니다. 홈 사이트와 유사하게, 제품 사이트 전체를 보기로 정의할 수 있습니다. 이 보기의 이름을 `https://target.enablementadobe.com/react/demo/#/products`의 경로 이름처럼 &quot;products&quot;로 지정할 수 있습니다.

![제품 사이트 2](/help/c-experiences/assets/product-site-2.png)

이 섹션의 시작 부분에서 &quot;보기&quot;를 전체 사이트나 사이트에 있는 시각적 요소들의 그룹으로 정의했습니다. 위에 표시된 것처럼 사이트에 표시된 4개의 제품을 그룹화하고 &quot;보기&quot;로 간주할 수도 있습니다. 이 보기의 이름을 지정하려면 이름을 &quot;products&quot;로 지정할 수 있습니다.

![제품 사이트 3](/help/c-experiences/assets/product-site-3.png)

추가 로드 단추를 클릭하여 사이트에서 더 많은 제품을 탐색하려 합니다. 이 경우에는 웹 사이트 URL은 변경되지 않습니다. 그러나 여기에서 &quot;보기&quot;는 위에 표시된 두 번째 제품 행만 나타낼 수 있습니다. 보기 이름은 &quot;PRODUCTS-PAGE-2&quot;이라고 할 수 있습니다.

**링크: [체크아웃](https://target.enablementadobe.com/react/demo/#/checkout)**

![체크아웃 페이지](/help/c-experiences/assets/checkout.png)

사이트에 표시된 일부 제품이 마음에 들어서 두 제품을 구매하기로 했습니다. 이제 체크아웃 사이트에서는 일반 배달이나 빠른 배달을 선택하는 선택 사항이 제공됩니다. &quot;보기&quot;는 사이트에서 임의의 시각적 요소 그룹일 수 있으므로 이 보기의 이름을 &quot;배달 환경 설정 보기&quot;로 지정할 수 있습니다.

또한 &quot;보기&quot; 개념은 이보다 훨씬 더 확장될 수 있습니다. 마케터가 선택된 배송 환경 설정에 따라 사이트에서 콘텐츠를 개인화하려는 경우 각 배달 환경 설정에 대해 &quot;보기&quot;를 만들 수 있습니다. 이 경우 일반 배달을 선택하면 보기의 이름을 &quot;일반 배달&quot;로 지정할 수 있습니다. 빠른 배달을 선택한 경우 보기의 이름을 &quot;빠른 배달&quot;로 지정할 수 있습니다.

이제 마케터는 빠른 배달을 선택했을 때 단추 색상을 두 배달 선택 사항 모두에 대해 파란색으로 유지하는 것과 대조적으로 색상을 파란색에서 빨간색으로 변경하는 것이 전환을 더 끌어올릴 수 있을지 여부를 확인하기 위해 A/B 테스트를 실행할 수 있습니다.

## Adobe Target 보기 구현

Adobe Target 보기에 대해 살펴보았으므로, 이제 Target에서 이 개념을 활용하여 마케터가 VEC를 통해 SPA에서 A/B 및 XT 테스트를 실행하도록 지원할 수 있습니다. 이렇게 하려면 일회용 개발자 설정이 필요합니다. 이 설정을 수행하는 절차를 살펴보겠습니다.

1. at.js 2.x를 설치합니다.

   먼저 at.js 2.x를 설치해야 합니다. 이 at.js 버전은 SPA를 염두에 두고 개발되었습니다. 이전 at.js 및 mbox.js 버전은 Adobe Target 보기와 SPA용 VEC를 지원하지 않습니다.

   ![구현 세부 사항 대화 상자](/help/c-experiences/assets/imp-200.png)

   Download the at.js 2.x via the Adobe Target UI located in [!UICONTROL Administration > Implementation]. at.js 2.x는 [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)를 통해 배포할 수도 있습니다. 그러나 Adobe Target 확장 프로그램은 현재 최신 상태가 아니며 지원되지 않습니다.

1. at.js 2.x의 최신 함수인 [triggerView()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md)를 사이트에 구현합니다.

   A/B 또는 XT 테스트를 실행할 SPA의 보기를 정의한 후에는 매개 변수로서 전달된 보기를 사용하여 at.js 2.x의 `triggerView()` 함수를 구현하십시오. 이렇게 하면 마케터는 VEC를 사용하여 정의된 해당 보기에 대한 A/B 및 XT 테스트를 디자인하고 실행할 수 있습니다. 해당 보기에 대해 `triggerView()` 함수가 정의되지 않은 경우 VEC가 보기를 감지하지 않으므로 마케터는 VEC를 사용하여 A/B 및 XT 테스트를 디자인하고 실행할 수 없습니다.

   **`adobe.target.triggerView(viewName, options)`**

   | 매개 변수 | 유형 | 필수? | 유효성 검사 | 설명 |
   | --- | --- | --- | --- | --- |
   | viewName | 문자열 | 예 | 1. 후행 공백이 없습니다.<br>2. 비워 둘 수 없습니다.<br>3. 보기 이름이 모든 페이지에 대해 고유해야 합니다.<br>4. **경고**: 보기 이름을 &#39;`/`&#39;로 시작하거나 종료해서는 안 됩니다. 일반적으로 고객은 URL 경로에서 보기 이름을 추출하기 때문입니다. 우리의 경우 &quot;홈&quot;과 &quot;`/home`&quot;이 다릅니다.<br>5. **경고**: `{page: true}` 선택 사항을 사용하여 동일한 보기를 여러 번 연속적으로 트리거할 수 없습니다. | 보기를 표현할 문자열 유형으로 모든 이름을 전달합니다. 이 보기 이름은 마케터가 작업을 만들고 A/B 및 XT 활동을 실행하는 VEC의 [!UICONTROL 수정 사항] 패널에 표시됩니다. |
   | options | 개체 | 아니오 |  |  |
   | options > page | 부울 | 아니오 |  | **TRUE**: 페이지의 기본값은 true입니다. `page=true`일 때 노출 수가 증가하면 Edge Server에 알림이 전송됩니다.<br>**FALSE**: `page=false`일 때 노출 수가 증가하면 알림이 전송되지 않습니다. 이 값은 오퍼가 있는 페이지에서 구성 요소를 다시 렌더링하려는 경우에만 사용해야 합니다. |

   이제 가상의 전자 상거래 SPA에 대해 React에서 `triggerView()` 함수를 호출하는 방법에 대한 몇 가지 사용 사례를 살펴보겠습니다.

   **링크: [홈 사이트](https://target.enablementadobe.com/react/demo/#/)**

   ![home-react-1](/help/c-experiences/assets/react1.png)

   마케터는 전체 홈 사이트에서 A/B 테스트를 실행하려는 경우 URL에서 추출할 수 있는 &quot;홈&quot; 보기의 이름을 지정할 수 있습니다.

   ```
   function targetView() {
     var viewName = window.location.hash; // or use window.location.pathName if router works on path and not hash
   
     viewName = viewName || 'home'; // view name cannot be empty
   
     // Sanitize viewName to get rid of any trailing symbols derived from URL
     if (viewName.startsWith('#') || viewName.startsWith('/')) {
       viewName = viewName.substr(1);
     }
   
     // Validate if the Target Libraries are available on your website
     if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
       adobe.target.triggerView(viewName);
     }
   }
   
   // react router v4
   const history = syncHistoryWithStore(createBrowserHistory(), store);
   history.listen(targetView);
   
   // react router v3
   <Router history={hashHistory} onUpdate={targetView} >
   ```

   **링크: [제품 사이트](https://target.enablementadobe.com/react/demo/#/products)**

   이제 좀 더 복잡한 예를 살펴보겠습니다. 마케터는 사용자가 추가 로드 단추를 클릭한 후 가격 레이블 색상을 빨간색으로 변경함으로써 제품의 두 번째 행을 개인화하려고 합니다.

   ![React 제품](/help/c-experiences/assets/react4.png)

   ```
   function targetView(viewName) {
     // Validate if the Target Libraries are available on your website
     if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
       adobe.target.triggerView(viewName);
     }
   }
   
   class Products extends Component {
     render() {
       return (
         <button type="button" onClick={this.handleLoadMoreClicked}>Load more</button>
       );
     }
   
     handleLoadMoreClicked() {
       var page = this.state.page + 1; // assuming page number is derived from component’s state
       this.setState({page: page});
       targetView('PRODUCTS-PAGE-' + page);
     }
   }
   ```

   **링크: [체크아웃](https://target.enablementadobe.com/react/demo/#/checkout)**

   ![React 체크아웃](/help/c-experiences/assets/react6.png)

   마케터가 선택된 배송 환경 설정에 따라 사이트에서 콘텐츠를 개인화하려는 경우 각 배달 환경 설정에 대해 &quot;보기&quot;를 만들 수 있습니다. 이 경우 일반 배달을 선택하면 보기의 이름을 &quot;일반 배달&quot;로 지정할 수 있습니다. 빠른 배달을 선택한 경우 보기의 이름을 &quot;빠른 배달&quot;로 지정할 수 있습니다.

   이제 마케터는 빠른 배달을 선택했을 때 단추 색상을 두 배달 선택 사항 모두에 대해 파란색으로 유지하는 것과 대조적으로 색상을 파란색에서 빨간색으로 변경하는 것이 전환을 더 끌어올릴 수 있을지 여부를 확인하기 위해 A/B 테스트를 실행할 수 있습니다.

   ```
   function targetView(viewName) {
     // Validate if the Target Libraries are available on your website
     if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
       adobe.target.triggerView(viewName);
     }
   }
   
   class Checkout extends Component {
     render() {
       return (
         <div onChange={this.onDeliveryPreferenceChanged}>
           <label>
             <input type="radio" id="normal" name="deliveryPreference" value={"Normal Delivery"} defaultChecked={true}/>
             <span> Normal Delivery (7-10 business days)</span>
           </label>
   
           <label>
             <input type="radio" id="express" name="deliveryPreference" value={"Express Delivery"}/>
             <span> Express Delivery* (2-3 business days)</span>
           </label>
         </div>
       );
     }
     onDeliveryPreferenceChanged(evt) {
       var selectedPreferenceValue = evt.target.value;
       targetView(selectedPreferenceValue);
     }
   }
   ```

1. VEC를 통해 A/B 또는 XT 활동을 실행합니다.

   `adobe.target.triggerView()`가 매개 변수로서 전달되는 보기 이름이 있는 SPA에서 구현되면 VEC는 이러한 보기를 감지하고 사용자가 A/B 또는 XT 활동에 대한 작업 및 수정 사항을 만드는 것을 허용할 수 있습니다.

   >[!NOTE]
   >
   >SPA용 VEC는 일반적인 웹 페이지에서 사용하는 것과 같은 VEC지만, 일부 추가 기능은 `triggerView()`가 구현된 단일 페이지 앱을 열 때 사용할 수 있습니다.

VEC가 SPA에서 잘 작동할 수 있도록 해주는, VEC에 대한 [수정 사항](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) 패널 및 작업에 대한 두 가지 주요 개선 사항이 있습니다.

**수정 패널**

아래 표시된 대로 [!UICONTROL 수정 사항] 패널에서는 특정 보기용으로 만들어진 작업을 캡처합니다. 보기에 대한 모든 작업은 해당 보기에서 그룹화됩니다.

**작업**

작업을 클릭하면 이 작업이 적용될 사이트의 요소가 강조 표시됩니다. 보기 아래에 작성된 각 VEC 작업에는 아래에 표시된 대로 정보, 편집, 복제, 이동 및 삭제 아이콘이 있습니다.

![수정 사항](/help/c-experiences/assets/modifications.png)

다음 표는 각 작업에 대해 설명합니다.

| 페이지 | 설명 |
| --- | --- |
| 정보 | 작업의 세부 사항을 표시합니다. |
| 편집 | 작업의 속성을 직접 편집할 수 있습니다. |
| 복제 | 작업을 [!UICONTROL 수정] 패널에 있는 하나 이상의 보기에 복제하거나 VEC에서 탐색하고 이동한 하나 이상의 보기에 복제합니다. 이 작업은 반드시 [!UICONTROL 수정] 패널에 있지 않아도 됩니다.<br>**참고**: 복제 작업이 수행된 후에는 [!UICONTROL 찾아보기]를 통해 VEC의 보기로 이동해야 이동이 올바른 작업인지 확인할 수 있습니다. 작업을 보기에 적용할 수 없으면 오류가 표시됩니다. |
| 이동 | 작업을 페이지 로드 이벤트나 수정 패널에 이미 있는 다른 보기로 이동합니다.<br>[!UICONTROL 페이지 로드 이벤트] - 페이지 로드 이벤트에 해당하는 모든 작업은 웹 애플리케이션의 초기 페이지 로드 시 적용됩니다.<br>**참고** 이동 작업이 수행된 후에는 찾아보기를 통해 VEC의 보기로 이동해야 이동이 올바른 작업인지 확인할 수 있습니다. 작업을 보기에 적용할 수 없으면 오류가 표시됩니다. |
| 삭제 | 작업을 삭제합니다. |

>[!NOTE]
>
>VEC에 페이지가 로드되기 전에 또는 페이지를 완전히 로드하지 못한 경우에도 여러 작업을 수행할 수 있습니다. 사이트가 로드되기 전에 편집할 수 없는 작업은 UI에서 비활성화됩니다.

**예제 1**

홈 보기를 만든 위의 예를 살펴보겠습니다. 본 보기의 목표는 두 가지입니다.

1. 장바구니에 추가 및 좋아요 단추를 연한 파란색으로 변경합니다. 머리글의 구성 요소를 변경하고 있으므로 이것은 &quot;페이지 로드&quot;에서 수행되어야 합니다.
1. &quot;2019년 최신 제품&quot; 레이블을 &quot;2019년 가장 인기 있는 제품&quot;으로 변경하고 텍스트 색상을 자주색으로 변경합니다.

이러한 목표를 실행하려면 VEC에서 [!UICONTROL 작성] 클릭하고 홈 보기에서 해당 변경 사항을 적용합니다.

![예제 1](/help/c-experiences/assets/example1.png)

**예제 2**

PRODUCTS-PAGE-2 보기를 만든 위의 예를 살펴보겠습니다. 우리의 목표는 &quot;가격&quot; 레이블을 레이블 색상이 빨간색인 &quot;판매 가격&quot;으로 변경하는 것입니다.

1. [!UICONTROL 찾아보기]를 클릭한 다음, 머리글에서 [!UICONTROL 제품] 링크를 클릭합니다.
1. [!UICONTROL 추가 로드]를 한 번 더 클릭하여 두 번째 제품 행을 표시합니다.
1. [!UICONTROL 작성]을 클릭합니다.
1. 동작을 적용하여 텍스트 레이블을 &quot;세일 가격&quot;으로 변경하고 색상을 빨간색으로 변경합니다.

![예제 2](/help/c-experiences/assets/example2.png)

**예제 3**

마지막으로 앞에서 언급한 바와 같이, 보기는 세부적으로 정의할 수 있습니다. 보기는 라디오 단추의 상태나 선택 사항도 될 수 있습니다. 앞서 Checkout-EXPRESS와 CHECKOUT-NORMAL 보기를 만들었습니다. 우리의 목표는 CHECKOUT-EXPRESS 보기용으로 단추 색상을 빨간색으로 변경하는 것입니다.

1. [!UICONTROL 찾아보기]를 클릭합니다.
1. 장바구니에 제품 두 개를 추가합니다.
1. 오른쪽 상단의 장바구니 아이콘을 클릭합니다.
1. 주문 체크아웃을 클릭합니다.
1. 빠른 배달 라디오 단추를 클릭합니다.
1. [!UICONTROL 작성]을 클릭합니다.
1. &quot;결제&quot; 단추를 &quot;주문 완료&quot; 단추로 변경하고 색상을 빨간색으로 변경합니다.

![예제 3](/help/c-experiences/assets/example3.png)

>[!NOTE]
>
>CHECKOUT-EXPRESS 보기는 빠른 배달 라디오 단추를 클릭하기 전까지 수정 패널에 표시되지 않습니다. 이것은 빠른 배달 라디오 단추가 선택되어 있을 때 `triggerView()` 함수가 트리거되며 이것은 VEC가 수정 패널에 표시할 보기가 있음을 알 때 뿐이기 때문입니다.

## at.js 및 SPA에 대해 깊이 들여다보기

**SPA에서 초기에 페이지가 로드된 후 작업에 의해 하이드레이션된 최신 대상 데이터의 보기를 검색하려면 어떻게 합니까?**

at.js 2.x의 일반적인 워크플로우는 사이트가 로드될 때 사이트에서 후속 사용자 작업이 오퍼를 검색하는 서버 호출을 트리거하지 않도록 모든 보기 및 작업을 캐시합니다. 후속 사용자 작업에 따라 업데이트되었을 수 있는 최신 프로필 데이터에 따라 보기를 검색하려는 경우, 전달된 최신 대상 사용자 또는 프로필 데이터로 `getOffers()` 및 `applyOffers()`를 호출할 수 있습니다.

예를 들어 at.js 2.x을 사용하는 SPA를 보유한 통신 회사라고 가정할 때, 기업으로서 다음 목표를 달성하려고 합니다.

* 로그아웃한 사용자나 익명 사용자에 대해 `http://www.telecom.com/home`에서 &quot;첫째 달 무료&quot; 주인공 오퍼 표시와 같은 최신 회사 프로모션을 보여줍니다.
* 로그인한 사용자에 대해서는 `http://www.telecom.com/loggedIn/home`에서 &quot;무료 전화를 사용할 수 있습니다!&quot;와 같이 계약이 예정된 사용자를 위한 업그레이드 프로모션 오퍼를 표시합니다.

이제 개발자는 다음의 방식으로 보기를 확인하고 `triggerView()`를 호출합니다.

* `http://www.telecom.com/home`의 경우 보기 이름은 &quot;Logged Out Home&quot;입니다.
   * `triggerView(“Logged Out Home”)`이 호출됩니다.
* `http://www.telecom.com/loggedIn/home`의 경우 보기 이름은 &quot;Logged In Home&quot;입니다.
   * 경로 변경 시 `triggerView(“Logged In Home”)`이 호출됩니다.

그러면 마케터는 VEC를 통해 다음의 A/B 활동을 실행합니다.

* `http://www.telecom.com/home`에 표시할 매개 변수 &quot;`loggedIn= false`&quot;를 사용하는 대상에 대해 &quot;첫째 달 무료&quot; 오퍼가 있는 A/B 활동. 여기서 보기 이름은 Logged Out Home입니다.
* &quot;무료 전화를 받을 수 있습니다!&quot;가 포함된 A/B 활동 `http://www.telecom.com/loggedIn/home`에 표시할 매개 변수 &quot;`loggedIn=true`&quot;를 사용하는 대상에 대해 &quot;무료 전화를 사용할 수 있습니다!&quot; 오퍼가 있는 A/B 활동. 여기서 보기 이름은 Logged In Hero Offer입니다.

이제 다음 사용자 흐름을 고려해 보십시오.

1. 익명의 로그아웃 사용자가 페이지에 도달합니다.
1. at.js 2.x를 사용하고 있으므로, 페이지 로드 시 매개 변수 &quot;`loggedIn = false`&quot;를 전달하여 대상에 &quot;`loggedIn = false`&quot; 매개 변수가 있을 때 자격이 있는 활성 활동에 있는 모든 보기를 검색합니다.
1. 그런 다음 at.js 2.x는 Logged Out Home 보기 및 작업을 검색하여 &quot;첫째 달 무료&quot; 오퍼를 표시하고 캐시에 저장합니다.
1. `triggerView(“Logged Out Home”)`이 호출되면 &quot;첫째 달 무료&quot; 오퍼가 캐시에서 검색되고 오퍼가 서버 호출 없이 표시됩니다.
1. 이제 사용자가 &quot;로그인&quot;을 클릭하고 자격 증명을 제공합니다.
1. 웹 사이트가 SPA이므로 전체 페이지를 로드하지 않고 대신 사용자를 `http://www.telecom.com/loggedIn/home`으로 보냅니다.

이제 문제가 있습니다. 경로 변경 시 우리가 이 코드를 배치했으므로 사용자가 로그인하면 우리에게 `triggerView(“Logged In Home”)`이 실행됩니다. 이 호출은 at.js 2.x가 캐시에서 보기와 작업을 검색하도록 하지만 캐시에 있는 유일한 보기는 Logged Out Home입니다.

따라서 어떻게 하면 이때 Logged In View을 검색하고 &quot;무료 전화를 사용할 수 있습니다!&quot; 오퍼를 표시할 수 있습니까? 또한 사이트에 대한 모든 후속 작업은 로그인한 사용자 관점에서 비롯되므로 어떻게 하면 모든 후속 작업이 로그인한 사용자를 위해 개인화된 오퍼를 생성하도록 할 수 있습니까?

at.js 2.x에서 지원되는 새로운 `getOffers()` 및 `applyOffers()` 함수를 사용할 수 있습니다.

```
adobe.target.getOffers({
  request: {
  prefetch: {
    "views": [
      {
        "parameters": {
          "loggedIn": true
        },
      }
    ]
  },
});
```

`getOffers()`의 응답을 `applyOffers()`에 전달하십시오. 그러면 이제 &quot;Loggedin = true&quot;와 연관된 모든 보기와 작업에 의해 at.js 캐시가 업데이트됩니다.

다시 말해, at.js 2.x에서는 온디맨드 방식으로 최신 대상 데이터로 보기, 작업 및 오퍼를 검색하는 방법을 지원합니다.

**at.js 2.x가 단일 페이지 애플리케이션용 A4T를 지원합니까?**

예. at.js 2.x에서는 Adobe Analytics와 Experience Cloud 방문자 ID 서비스를 구현한 경우 `triggerView()` 함수를 통해 SPA용 A4T를 지원합니다. 단계별 설명이 있는 아래 다이어그램을 참조하십시오.

![Target 흐름](/help/c-experiences/assets/atjs-spa-flow.png)

| 단계 | 설명 |
| --- | --- |
| 1 | 보기를 렌더링하고 작업을 적용하여 보기와 연관된 시각적 요소를 수정하기 위해 SPA에서 `triggerView()`가 호출됩니다. |
| 2 | 보기용으로 타깃팅된 콘텐츠를 캐시에서 읽습니다. |
| 3 | 타깃팅된 콘텐츠는 기본 콘텐츠의 플리커 없이 가능한 한 빨리 나타납니다. |
| 4 | 활동 및 증분 지표에서 방문자를 계산하기 위해 알림 요청이 Target 프로필 스토어에 전송됩니다. |
| 5 | Analytics 데이터가 데이터 수집 서버로 전송됩니다. |
| 6 | Target 데이터는 SDID를 통해 Analytics 데이터에 대응되며 Analytics 보고 저장소로 처리됩니다. 그런 다음 Analytics 데이터는 A4T 보고서를 통해 Analytics 및 Target 모두에서 볼 수 있게 됩니다. |

>[!NOTE]
>보기가 트리거될 때마다 노출수 계산을 위해 Adobe Analytics에 알림을 보내지 않으려면, 지속적으로 다시 렌더링되는 구성 요소에 대해 보기가 여러 번 트리거될 때 노출수 계산이 부풀려지지 않도록 `{page: false}`를 `triggerView()` 함수에 전달합니다. 예:
>
>`adobe.target.triggerView(“PRODUCTS-PAGE-2”, {page:false})`

## 지원되는 활동

| 활동 유형 | 지원됨? |
| --- | --- |
| [A/B 테스트](/help/c-activities/t-test-ab/test-ab.md) | 예 |
| [A/B 테스트 및 경험 타깃팅(XT) 활동에서](/help/c-recommendations/recommendations-as-an-offer.md)<br> 오퍼로서 권장 사항 | 예 |
| [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 예 |
| [경험 타깃팅](/help/c-activities/t-experience-target/experience-target.md) | 예 |
| [다변량 테스트](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | 아니오 |
| [자동 타깃팅](/help/c-activities/auto-target/auto-target-to-optimize.md) | 아니오 |
| [자동화된 개인화](/help/c-activities/t-automated-personalization/automated-personalization.md) | 아니오 |
| [권장 사항](/help/c-recommendations/recommendations.md) | 아니오 |

**at.js 2.x를 설치하고 사이트에 `triggerView()`를 구현한 경우, SPA VEC가 자동 타겟을 지원하지 않는데 어떻게 자동 타겟 A/B 활동을 실행합니까?**

자동 타겟 A/B 활동을 사용하려는 경우, VEC의 페이지 로드 이벤트에서 실행되도록 모든 작업을 이동하면 됩니다. 각 작업 위로 마우스를 가져간 다음 [!UICONTROL 페이지 로드 이벤트로 이동] 단추를 클릭하십시오. 이 과정이 완료되면, 다음 단계에서 트래픽 할당 방법을 위해 자동 타겟을 선택할 수 있습니다.

## 지원되는 통합

| 통합 | 지원됨? |
| --- | --- |
| [Analytics for Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) | 예 |
| [Experience Cloud 대상자](/help/c-integrating-target-with-mac/mmp.md) | 예 |
| [고객 속성](/help/c-target/c-visitor-profile/working-with-customer-attributes.md) | 예 |
| [AEM 경험 구성요소](/help/c-experiences/c-manage-content/aem-experience-fragments.md) | 예 |

## 지원되는 기능 {#supported-features}

| 기능 | 지원됨? |
| --- | --- |
| [작업 공간 및 속성](/help/administrating-target/c-user-management/property-channel/property-channel.md) | 예 |
| [QA 링크](/help/c-activities/c-activity-qa/activity-qa.md) | 예 |
| [양식 기반 경험 작성기](/help/c-experiences/form-experience-composer.md) | 아니오 |
| [사용자 지정 코드](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) | 예 |
| [VEC 선택 사항](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | 모든 |
| [클릭 추적](/help/c-activities/r-success-metrics/click-tracking.md) | 예 |
| [여러 활동 전달](/help/c-experiences/c-visual-experience-composer/multipage-activity.md) | 예 |

## SPA VEC에 대한 페이지 전달 설정{#page-delivery-settings}

[!UICONTROL 페이지 전달] 설정을 사용하면 타겟 활동이 대상에 대해 자격을 부여하고 실행하는 시기를 결정하는 규칙을 구성할 수 있습니다.

VEC의 세 부분으로 구성된 안내 활동 만들기 워크플로우 내에서 [!UICONTROL 페이지 전달] 옵션에 액세스하려면 **[!UICONTROL 경험]** 단계에서 **[!UICONTROL 구성]**(톱니바퀴 아이콘) > **[!UICONTROL 페이지 전달]**&#x200B;을 클릭합니다.

![페이지 전달 옵션 대화 상자](/help/c-experiences/assets/page-delivery.png)

예를 들어, 위에 표시된 [!UICONTROL 페이지 전달] 설정에 정의된 대로 방문자가 바로 `https://www.adobe.com`에 방문하거나 *또는* 방문자가 `https://www.adobe.com/products`를 포함한 URL에 도달하면 타겟 활동이 정규화되고 실행됩니다. 이 활동은 페이지와의 모든 상호 작용이 페이지 재로드를 호출하는 모든 다중 페이지 애플리케이션에 완벽하게 작동합니다. 여기서 at.js는 사용자가 탐색하는 URL을 대상으로 하는 활동을 검색합니다.

그러나 SPA는 다르게 작동하므로 SPA VEC 활동에 정의된 대로 모든 작업을 보기에 적용할 수 있는 방식으로 [!UICONTROL 페이지 전달] 설정을 구성해야 합니다.

### 예제 사용 사례

다음 예제 사용 사례를 고려하십시오.

![SPA VEC 수정 패널](/help/c-experiences/assets/page-delivery-example.png)

다음 사항이 변경되었습니다.

* URL 아래 있는 홈 보기에서 배경색을 변경했습니다. [/#/](https://target.enablementadobe.com/react/demo/#/)https://target.enablementadobe.com/react/demo/#/.
* Changed the button color in the Products view, which is located under the URL: [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).

With the example above in mind, what would happen when we configure [!UICONTROL Page Delivery] settings to only include: [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/) in an SPA with at.js 2.*x*&#x200B;를 사용하는 SPA에서)하면 어떻게 될까요.

![페이지 전달 대화 상자](/help/c-experiences/assets/spa-page-delivery.png)

다음 그림은 타겟 흐름을 보여줍니다 - 페이지 로드 요청을 보여줍니다.*x*:

![Target 흐름 - at.js 2.0 페이지 로드 요청](/help/c-experiences/assets/page-load-request.png)

**사용자 여정 1**

* A user navigates directly to [https://target.enablementadobe.com/react/demo/#/](https://target.enablementadobe.com/react/demo/#/).
* at.js 2.*x*&#x200B;는 Edge에 대한 쿼리를 수행하여 다음 URL에 대해 활동을 실행해야 하는지 확인합니다. [/#/https://target.enablementadobe.com/react/demo/](https://target.enablementadobe.com/react/demo/#/)#/
* 6단계에서 Target Edge는 브라우저 내에서 캐시되도록 홈 및 제품 보기에 대한 작업을 반환합니다.

**결과**: 사용자는 홈 보기에서 녹색 배경색을 보게 됩니다. 사용자가 [](https://target.enablementadobe.com/react/demo/#/products)https://target.enablementadobe.com/react/demo/#/products로 이동하면 해당 작업이 제품 보기 아래의 브라우저에서 캐시되므로 단추의 파란색 배경색이 표시됩니다.

Note: The user navigating to [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products) did not trigger a page load.

**사용자 여정 2**

* A user navigates directly to [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* at.js 2.*x*&#x200B;는 Edge에 대한 쿼리를 수행하여 다음 URL에 대해 활동을 실행해야 하는지 확인합니다. [](https://target.enablementadobe.com/react/demo/#/products)https://target.enablementadobe.com/react/demo/#/products.
* There are no activities qualified for [https://target.enablementadobe.com/react/demo/#/products](https://target.enablementadobe.com/react/demo/#/products).
* 적합한 활동이 없으므로 트리거할 at.js 2.*x*&#x200B;에 대해 캐시되는 작업 및 보기가 없습니다.

**결과**: 제품 보기에 대해 정의하고 SPA VEC를 통해 제품 보기에 작업을 수행한 경우에도 `triggerView()` 페이지 전달 설정에서 [](https://target.enablementadobe.com/react/demo/#/products)https://target.enablementadobe.com/react/demo/#/products를 포함한 규칙을 만들지 않았기 때문에 예상한 작업이 표시되지 않습니다.

### 우수 사례

사용자가 SPA의 URL에 도달하여 다른 페이지로 이동할 수 있으므로 사용자 경로를 관리하는 것은 매우 어려울 수 있습니다. 따라서 전체 SPA가 포함되도록 기본 URL이 포함된 페이지 전달 규칙을 지정하는 것이 가장 좋습니다. 이러한 방식으로 A/B 테스트 또는 XT(경험 타깃팅) 활동을 표시할 페이지에 도달하기 위해 사용자가 취할 수 있는 다양한 여정 및 경로에 대해 신경쓰지 않아도 됩니다.

예를 들어 위에 직면한 문제를 해결하기 위해 페이지 전달 설정에서 기본 URL를 다음과 같이 지정할 수 있습니다.

![페이지 전달 대화 상자](/help/c-experiences/assets/conclusion.png)

이렇게 하면 방문자가 SPA에 도달하여 홈 또는 페이지 보기로 이동하는 곳마다 적용된 작업이 표시됩니다.

이제 SPA VEC에서 보기에 작업을 추가할 때마다 [!UICONTROL 페이지 전달] 규칙에 대해 고려해야 함을 알리는 다음 팝업 메시지가 표시됩니다.

![페이지 전달 설정 메시지](/help/c-experiences/assets/pop-up-message.png)

이 메시지는 새로 만든 모든 활동에 대해 첫 번째 작업을 보기에 추가할 때 표시됩니다. 이 메시지는 조직의 모든 구성원이 이러한 [!UICONTROL 페이지 전달] 규칙을 올바르게 적용하는 방법을 알 수 있도록 해줍니다.

## 교육 비디오: Adobe Target에서의 SPA용 VEC 사용

>[!VIDEO](https://video.tv.adobe.com/v/26249)

See [Using the Visual Experience Composer for Single Page Application (SPA VEC) in Adobe Target](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) for more information.
