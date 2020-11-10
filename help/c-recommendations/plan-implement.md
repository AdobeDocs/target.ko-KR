---
keywords: Recommendations;settings;preferences;industry vertical;filter incompatible criteria;default host group;thumb base url;recommendations api token
description: 권장 사항 활동을 작성하기 전에 알아야 할 사항.
title: 권장 사항 계획 및 구현
feature: recommendations general
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1592'
ht-degree: 96%

---


# ![프리미엄](/help/assets/premium.png) 플랜 및 Recommendations 구현 {#plan-and-implement-recommendations}

권장 사항 활동을 작성하기 전에 알아야 할 사항.

## 권장 사항 계획 및 구현 {#concept_02AA644A4C7D4D5CB1D9CADA208CF8D1}

[!DNL Recommendations] 활동을 작성하기 전에 알아야 할 사항.

[!DNL Recommendations]를 사용하려면 다음 정보 계층 구조를 설정해야 합니다.

| 단계 | 정보 | 세부 사항 |
|--- |--- |--- |
| ![1단계](/help/c-recommendations/assets/step1_red.png) | JavaScript 라이브러리 | 각 페이지는 at.js 버전 0.9.1(또는 이상) 또는 mbox.js 버전 55(또는 이상)을 참조해야 합니다. 이 구현 단계는 Target 활동이 사용될 모든 페이지에서 필요하며, 제품 또는 카테고리 ID와 같은 키를 포함할 수 있습니다.<BR>at.js에 대해서는 [at.js 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md)을 참조하십시오.<br>mbox.js에 대한 자세한 내용은 [mbox.js 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)을 참조하십시오. |
| ![2단계](/help/c-recommendations/assets/step2_red.png) | 키 | 키는 권장 사항에 표시되는 제품 또는 콘텐츠의 유형을 결정합니다. 예를 들어, 제품 카테고리가 키일 수 있습니다. 활동에서 지리 기반의 타깃팅을 사용하는 방법에 대한 자세한 내용은 [권장 사항 키를 기반으로 권장 사항 만들기](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md)를 참조하십시오. |
| ![3단계](/help/c-recommendations/assets/step3_red.png) | 속성 | 속성은 표시할 제품에 대한 보다 구체적인 정보를 제공합니다. 예를 들어, 특정 가격 범위 내 제품을 표시하거나 재고 임계값을 충족하는 항목을 표시할 수 있습니다. 속성은 mbox에서 또는 [피드](/help/c-recommendations/c-products/feeds.md).<br>포함 [규칙 지정을 참조하십시오](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion). |
| ![4단계](/help/c-recommendations/assets/step4_red.png) | 제외 | 제외는 권장 사항에 표시되지 않는 특정 항목을 결정합니다.<br>[제외](/help/c-recommendations/c-products/exclusions.md)를 참조하십시오. |
| ![5단계](/help/c-recommendations/assets/step5_red.png) | 구매 세부 사항 | 구매 세부 사항에서는 구매한 항목과 구매가 완료된 주문에 대한 정보를 제공합니다. |

## 기본 구현 {#concept_D1154A3FB0FB4467A29AD2BDD21C82D5}

기본 구현에서는 권장 사항에 표시되는 제품 또는 서비스를 결정하는 매개 변수를 페이지에 전달해야 합니다.

[!DNL Recommendations] 활동 설정을 시작하려면 먼저 제품 데이터가 [!DNL Recommendations]에 제공되는 방법을 이해하고 필요에 가장 적합한 방법을 결정해야 합니다.

[!DNL Recommendations]에 제품 및 서비스에 대한 정보를 제공하는 방법에는 두 가지가 있습니다.

| 메서드 | 설명 |
|--- |--- |
| 페이지에 바로 매개 변수 전달 | 이 방법은 자주 변경되는 항목에 적합합니다. 하지만, 변경 사항을 페이지에 바로 적용해야 하므로 많은 조직의 경우 이 방법을 사용하려면 IT 및 페이지 구현 담당자가 있어야 합니다. |
| Google 또는 CSV 피드를 통해 매개 변수 전달 | 이 방법은 자주 변경되지 않는 컬렉션에 적합합니다. 피드를 통해 제품 정보를 제공하는 데에는 일반적으로 구현이나 기타 페이지 코드를 변경할 필요가 없습니다. 하지만, 제품 목록이 계속 고정되어 있어서 빠른 변경은 더 어렵습니다. 자세한 내용은 [피드](/help/c-recommendations/c-products/feeds.md)를 참조하십시오. |

다음 예와 같이 이 방법들을 따로 사용하거나 함께 사용할 수도 있습니다.

## 예 1: 페이지와 피드 결합 {#section_DF6BAE4BF11548BD9C44D0A426BCF5A7}

하나의 공통 [!DNL Recommendations] 구현 선택 사항이 페이지 매개 변수와 피드를 모두 사용합니다.

이 방법은 상대적으로 설정된 제품 카탈로그가 있지만 특정 시즌별 항목이나 판매 중인 항목을 강조하고 싶은 소매업자가 선호할 수 있습니다. 대부분의 고객은 가끔씩 페이지 조정만 하고, 주로 피드를 통해 정보를 제공할 수 있습니다.

자주 변경되지 않는 정보를 제공하려면 피드를 사용합니다. CSV 파일을 사용하든 Google 피드를 사용하든 다음 매개 변수를 사용합니다.

* 필수 매개 변수

   * `entity.id`

* 유용한 매개 변수

   * `entity.name`
   * `entity.categoryId`
   * `entity.brand`
   * `entity.pageUrl`
   * `entity.thumbnailUrl`
   * `entity.message`
   * 모든 사용자 지정 속성

피드가 설정되고 [!DNL Recommendations]에 전달되면 자주 변경(예: 매일보다 자주 변경)되는 속성에 대한 매개 변수를 전달합니다.

* 필수 매개 변수

   * `entity.id`
   * `entity.categoryId`

* 유용한 매개 변수

   * `entity.inventory`
   * `entity.value`

가장 최근에 실행되는 데이터 세트에 우선 순위가 지정됩니다. 먼저 피드를 전달한 다음, 페이지 매개 변수를 업데이트하면 페이지 매개 변수에서 적용된 변경 사항이 표시되고 피드에 전달된 항목 정보가 교체됩니다.

## 예 2: 제품(또는 콘텐츠) 세부 사항 페이지의 모든 매개 변수 전달 {#section_D5A4F69457604CA7AACFD7BFF79B58A9}

페이지의 모든 매개 변수를 전달하면 페이지를 업데이트하여 신속하게 업데이트할 수 있습니다. 일부 조직에서는 IT나 웹 디자인 팀의 작업이 있어야 합니다.

이 예는 특히 지속적으로 변경되는 콘텐츠가 있는 미디어 회사에 유용할 수 있습니다.

* 필수 매개 변수

   * `entity.id`
   * `entity.categoryId`
   * 기타 모든 속성

## 샘플 코드 {#section_6E8A73376F30468BB549F337C4C220B1}

예를 들어, 제품이나 컨텐츠 페이지의 헤더 섹션에서 다음 코드를 사용할 수 있습니다.

```
function targetPageParams() {
 return {
    "entity": {
       "id": "32323",
       "categoryId": "My Category",
       "value": 105.56,
       "inventory": 329
    }
 }
}
```

다양한 유형의 페이지에서 사용할 수 있는 코드에 대한 예가 더 필요하면 [페이지 유형에 따른 구현](/help/c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC).

## 페이지 유형에 따른 구현 {#reference_DE38BB07BD3C4511B176CDAB45E126FC}

페이지 유형은 [!DNL Recommendations] 구현에 영향을 줍니다.

예를 들어, 제품 페이지에서 표시하고 싶은 권장 사항 유형이 범주 페이지 또는 홈 페이지와는 다를 수 있습니다. 각 페이지에 대해 mbox 호출 전에 특정 함수를 실행하여 적절한 권장 사항을 표시할 수 있습니다.

예제의 속성에 대한 내용은 [엔티티 속성](/help/c-recommendations/c-products/entity-attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F)을 참조하십시오.

유효한 JSON 형식이 필요합니다.

아래 표시된 `targetPageParams` 함수는 태그 관리 솔루션을 사용하여 페이지를 구현하는 경우에 특히 유용합니다. [!DNL Adobe Launch] 또는 DTM([!DNL Adobe Dynamic Tag Manager])은 at.js/mbox.js 참조 및 `targetPageParams` 함수를 사용자 페이지에 지정하므로 사용자가 이 값을 구성할 수 있습니다. at.js/mbox.js 호출 앞에 해당 함수를 두거나 at.js/mbox.js의 추가 JavaScript 섹션에 배치해야 합니다.

## 모든 페이지 {#section_A22061788BAB42BB82BA087DEC3AA4AD}

권장 사항을 포함하는 모든 페이지에는 [!DNL at.js] 또는 [!DNL mbox.js] 참조가 필요합니다. 권장 사항이 있는 모든 페이지에 다음 참조 중 하나를 추가하십시오.

```
<script src="/help/at.js /></script>
```

```
<script src="/help/mbox.js /></script>
```

이 구현에는 다음이 필요합니다.

* [!DNL at.js] 버전 0.9.2 이상 또는 [!DNL mbox.js] 버전 55 이상

* [!DNL mbox.js]에는 [!DNL target.js]에 대한 참조가 포함되어야 합니다([!DNL at.js]에는 [!DNL target.js]에 대한 참조가 필요하지 않음).

[!DNL at.js] 구현에 대한 자세한 내용은 [at.js를 배포하는 방법](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md#topic_ECF2D3D1F3384E2386593A582A978556)을 참조하십시오.

[!DNL mbox.js] 구현에 대한 자세한 내용은 [mbox.js 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420)을 참조하십시오.

두 Target Javascript 라이브러리의 차이점에 대한 자세한 내용은 [at.js의 이점](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits)을 참조하십시오.

## 카테고리 페이지 {#section_F51A1AAEAC0E4B788582BBE1FEC3ABDC}

카테고리 페이지에서는 해당 카테고리 내의 제품 또는 콘텐츠로 권장 사항을 제한할 수 있습니다. 카테고리 페이지를 설정하려면 페이지에서 사용되는 키를 설정합니다. 키에 대한 자세한 내용은 [권장 사항 키를 기반으로 권장 사항 만들기](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md)를 참조하십시오.

```
function targetPageParams() { 
   return { 
      "entity": { 
         "categoryId": "My Category" 
      } 
   } 
}
```

## 제품 페이지 {#section_205B3953C9664125A17CA8574FA6B2A3}

제품 페이지에서 특정 품목이나 특정 가격 또는 재고 수준을 갖는 품목을 추천할 수 있습니다. 제품 페이지의 경우 카테고리 페이지에 필요한 키 외에도 자주 변경되는 속성(예: 가격 및 재고)을 설정해야 할 수 있습니다.

```
function targetPageParams() { 
   return { 
      "entity": { 
         "id": "32323", 
         "categoryId": "My Category", 
         "value": 105.56, 
         "inventory": 329 
      } 
   } 
}
```

## 장바구니 페이지 {#section_D37E48700F074556B925D0CA0291405E}

장바구니 페이지에서는 이미 장바구니에 들어 있는 항목 등의 일부 항목을 권장 사항에서 제외할 수 있습니다.

```
<script type="text/javascript">
function targetPageParams() {
   return {
      "excludedIds": [352, 223, 23432, 432, 553]
      }
}
</script>
```

## 감사 페이지 {#section_C6126A4517A1478693AB7EC2A1D4ACCA}

감사 페이지에서는 추가 품목을 권장하지 않으면서 주문 합계 및 주문 ID를 표시하고, 구입한 제품을 표시할 수 있습니다. 두 번째 mbox를 구현하여 주문 정보를 캡처할 수 있습니다.

* at.js를 사용하는 경우 [변환 추적](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).
* mbox.js를 사용 중이라면 [주문 확인 mbox 만들기 - mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/orderconfirm-create.md#task_0036D5F6C062442788BB55E872816D82)를 참조하십시오.

## 설정{#concept_C1E1E2351413468692D6C21145EF0B84}의 지침을 완료하여 이 설정을 변경할 수 있습니다 

설정을 사용하여 [!DNL Recommendations] 구현을 관리하십시오.

To access the [!UICONTROL Recommendations Settings] options, open [!DNL Target] in the [!DNL Adobe Experience Cloud], then click **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

![](assets/recs_settings.png)

다음 옵션을 사용할 수 있습니다.

| 설정 | 설명 |
|--- |--- |
| 사용자 지정 글로벌 mbox | (선택 사항) [!DNL Target] 활동을 제공하는 데 사용되는 사용자 지정 글로벌 mbox를 지정합니다. By default, the global mbox used by [!DNL Target] is used for [!DNL Recommendations].<br>참고:이 옵션은 [관리] [!DNL Target][!UICONTROL 페이지에서] 설정됩니다. [관리] [!DNL Target]> [!UICONTROL Visual Experience] Composer를 [!UICONTROL 차례로 클릭합니다]. |
| 업계 카테고리 | 업계 카테고리는 권장 사항 기준을 분류하는 데 사용됩니다. 따라서 팀 구성원이 장바구니 페이지나 미디어 페이지에 가장 적합한 기준과 같이 특정 페이지에 적합한 기준을 찾는 데 도움이 됩니다. |
| 호환되지 않는 기준 필터링 | 선택한 페이지가 필수 데이터를 전달하는 기준만 표시하려면 이 선택 사항을 사용하십시오. 모든 기준이 모든 페이지에서 올바르게 실행되지는 않습니다. 페이지 또는 mbox는 호환될 현재 항목/현재 카테고리에 대한 `entity.id` 또는 `entity.categoryId`를 제공해야 합니다. 일반적으로 호환 가능한 기준만 표시하는 것이 가장 좋습니다. 그러나 호환되지 않는 기준을 활동에 사용할 수 있게 하려면 이 선택 사항을 선택 취소하십시오.<br>태그 관리 솔루션을 사용하는 경우에는 이 선택 사항을 비활성화하는 것이 좋습니다.<br>이 선택 사항에 대한 자세한 내용은 [권장 사항 FAQ](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md)를 참조하십시오. |
| 기본 호스트 그룹 | 기본 호스트 그룹을 선택합니다.<br>호스트 그룹을 사용하여 카탈로그에 있는 사용 가능한 항목을 다양한 용도로 구분할 수 있습니다. 예를 들어 개발 및 프로덕션 환경, 다양한 브랜드 또는 다양한 지역용으로 호스트 그룹을 사용할 수 있습니다. 기본적으로 카탈로그 검색, 컬렉션 및 제외의 미리 보기 결과는 기본 호스트 그룹을 기반으로 합니다. (환경 필터를 사용하여 다른 결과를 미리 볼 호스트 그룹을 선택할 수도 있습니다.) 기본적으로 항목을 만들거나 업데이트할 때 환경 ID를 지정하지 않는 한, 새로 추가된 항목은 모든 호스트 그룹에서 사용할 수 있습니다. 전달되는 권장 사항은 요청에 지정된 호스트 그룹에 따라 다릅니다.<br>제품이 보이지 않는다면 올바른 호스트 그룹을 사용하고 있는지 확인하십시오. 예를 들어, 스테이징 환경을 사용하도록 권장 사항을 설정하고 호스트 그룹을 스테이징으로 설정하는 경우, 제품을 표시할 스테이징 환경에서 컬렉션을 다시 만들어야 합니다. 각 환경에서 사용 가능한 제품을 확인하려면 각 환경에서 카탈로그 검색을 사용하십시오. 선택한 환경(호스트 그룹)에 대한 권장 사항 컬렉션 및 제외 콘텐츠를 미리 볼 수도 있습니다.<br>**참고:** 선택한 환경을 변경한 후 검색을 클릭하여 반환된 결과를 업데이트해야 합니다.<br>[!UICONTROL 환경] 필터는 [!DNL Target] UI의 다음 위치에서 사용할 수 있습니다.<ul><li>카탈로그 검색(권장 사항 > 카탈로그 검색)</li><li>컬렉션 만들기 대화 상자([!UICONTROL 권장 사항 > 컬렉션 > 새로 만들기])</li><li>컬렉션 업데이트 대화 상자([!UICONTROL 권장 사항 > 컬렉션 > 편집])</li><li>제외 만들기 대화 상자([!UICONTROL 권장 사항 > 제외 > 새로 만들기])</li><li>제외 업데이트 대화 상자([!UICONTROL 권장 사항 > 제외 > 편집])</li></ul>자세한 내용은 [호스트](/help/administrating-target/hosts.md)를 참조하십시오. |
| 썸네일 기본 URL | 제품 카탈로그용의 기본 URL을 설정하면 썸네일 URL을 전달할 때, 제품의 썸네일을 지정할 때 상대 URL을 사용할 수 있습니다.<br>예를 들어<br>`"entity.thumbnailURL=/Images/Homepage/product1.jpg"`<br>는 썸네일 기본 URL에 상대적인 URL을 설정합니다. |
| Recommendations API 토큰 | Download API와 같은 권장 사항 API 호출에서 이 토큰을 사용하십시오. |
