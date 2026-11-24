---
keywords: 다중 값;속성;권장 사항;다중 값;다중 값;다중 값
description: 특수 다중 값 연산자를 사용하여 [!DNL Target Recommendations]에서 다중 값 필드로 작업하는 방법을 알아봅니다.
title: 다중 값 속성 관련 작업
feature: Recommendations
exl-id: 82018a9a-0983-458c-9387-3602dab4409b
TQID: 'https://experienceleague.adobe.com/FrjVxvYfGh2o-qomXRbVh6WS6f65Mja41gBMhejEPlE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 2%
---
# 다중 값 속성 관련 작업 {#multi-value-attributes}

>[!BEGINSHADEBOX]

**이 페이지에서:** 다중 값 데이터를 [!DNL Adobe Target Recommendations]에 보내는 방법과 다중 값 연산자를 사용하는 포함 규칙에 사용하는 방법을 알아봅니다.

>[!ENDSHADEBOX]

다중 값 필드는 동일한 항목 또는 방문자에 대한 여러 값을 보유합니다. 예:

* 사용자에게 제공되는 영화: 해당 영화에는 여러 명의 배우가 출연합니다.
* 콘서트 티켓 판매: 주어진 사용자는 여러 좋아하는 밴드를 보유하고 있습니다.
* 판매된 의류: 셔츠는 여러 크기로 제공됩니다.

이러한 시나리오에서 권장 사항을 처리하기 위해 다중 값 데이터를 [!DNL Target Recommendations]에 전달하고 특수 다중 값 연산자와 함께 사용할 수 있습니다.

## 다중 값 데이터 보내기 {#send}

[!DNL Recommendations]이(가) 다중 값 데이터를 식별하도록 하려면 JSON 배열로 전송해야 합니다.

JavaScript(`targetPageParams`)의 다중 값 매개 변수에 대해서는 *사용자 지정 엔터티 특성*&#x200B;에서 [다중 값 특성 구현](/help/main/c-recommendations/c-products/custom-entity-attributes.md#section_80FEFE49E8AF415D99B739AA3CBA2A14)을 참조하십시오.

CSV 파일에서 다중 값 엔티티 속성은 다음 샘플과 같이 속성 셀에서 JSON 배열로 전송됩니다.

+++ 다중 값 속성이 있는 샘플 CSV 파일

```
## RECSRecommendations Upload File,,,,,,,,,,,,,,,,,,,
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines.,,,,,,,,,,,,,,,,,,,
## RECS,,,,,,,,,,,,,,,,,,,
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left.,,,,,,,,,,,,,,,,,,,
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'.,,,,,,,,,,,,,,,,,,,
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations.,,,,,,,,,,,,,,,,,,,
## RECSentity.id ,entity.name,entity. categoryId ,entity. message ,entity.thumbnailUrl ,entity.value ,entity.pageUrl ,entity.inventory ,entity.margin ,entity.custom1 ,entity.custom2 ,entity.custom3 ,entity.custom4,entity.custom5,entity.custom6,entity.custom7,entity.custom8,entity.custom9,entity.custom10,
1,Sample Product 1,category1,Save 10%,http://sample.store/products/images/product1_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=1,1000,48,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
2,Sample Product 2,category1,Save 10%,http://sample.store/products/images/product2_th.jpg,369,http://sample.store/products/product_detail.jsp?productId=2,1000,52,a,"[ ""v1"", ""v2"" ]",, , , , , , , ,
3,Sample Product 3,category1,Save 10%,http://sample.store/products/images/product3_th.jpg,479,http://sample.store/products/product_detail.jsp?productId=3,1000,78,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
4,Sample Product 4,category1,Save 10%,http://sample.store/products/images/product4_th.jpg,409,http://sample.store/products/product_detail.jsp?productId=4,1000,66,a,"[ ""v1"", ""v2"" ]",,,,,,,,,
5,Sample Product 5,category1,Save 10%,http://sample.store/products/images/product5_th.jpg,325,http://sample.store/products/product_detail.jsp?productId=5,1000,45,a,"[ ""v1"", ""v2"" ]",,,,,,,,, 
```

+++

엔터티 특성, 프로필 특성 또는 mbox 매개 변수가 이 형식의 다중 값으로 제공되면 [!DNL Recommendations]에서 필드가 다중 값임을 자동으로 유추합니다.

## 포함 규칙에서 다중 값 속성 사용 {#multi-value-inclusion-rules}

다음 연산자는 다중 값 엔티티, 프로필 및 mbox 속성과 함께 사용할 수 있습니다.

* **[!UICONTROL 이(가) 목록에 포함되어 있음]**
* **[!UICONTROL 이(가) 목록에 포함되어 있지 않습니다]**

>[!NOTE]
>
>다중 값 속성에 대한 동적 일치의 지원은 현재 왼쪽의 단일 값을 오른쪽의 다중 값과 비교하는 프로필 속성 일치 또는 매개 변수(mbox) 속성 일치 규칙을 사용하는 기준에서만 사용할 수 있습니다. 다중 값 속성은 현재 프로모션, 엔티티 속성 일치 또는 포함 규칙 왼쪽의 목록에 대해 지원되지 않습니다.

### 예: 최근에 시청한 항목 제외

사용자의 최근 10개의 시청 동영상에 포함된 영화가 추천되지 않도록 하려면 먼저 최근 10개의 시청 동영상을 JSON 배열로 추적하는 `user.lastWatchedMovies`이라는 프로필 스크립트를 작성하십시오. 그런 다음 다음 다음 포함 규칙을 사용하여 항목을 제외할 수 있습니다.

```
Profile Attribute Matching
id - is not contained in list - user.lastWatchedMovies
```

포함 규칙의 JSON API 표시:

```
{
    "attribute": "id",
    "operation": "isNotContainedInList",
    "source": {
        "name": "user.lastWatchedMovies",
        "type": "PROFILE"
    }
} 
```

### 예: 사용자의 즐겨찾기에서 항목 추천

사용자가 좋아하는 밴드 중 하나인 경우에만 콘서트 티켓을 추천하려면 사용자의 좋아하는 밴드가 포함된 프로필 변수(`profile.favoriteBands`)와 콘서트에서 공연하는 아티스트가 포함된 카탈로그의 속성 `entity.artistPerforming`)의 두 가지 항목이 필요합니다. 그런 다음 다음 다음 포함 규칙을 사용할 수 있습니다.

```
Profile Attribute Matching
artistPerforming - is contained in list - profile.favoriteBands
```

포함 규칙의 JSON API 표시:

```
{
    "attribute": "artistPerforming",
    "operation": "isContainedInList",
    "source": {
        "name": "profile.favoriteBands",
        "type": "PROFILE"
    }
}
```

### 예: 사용자의 즐겨찾기에서 항목을 추천하는 기준의 API 생성

다중 값 필터링 규칙을 사용하는 기준은 모든 기준처럼 [!DNL Adobe Target] API를 통해 만들 수 있습니다. 다음 예제 API 호출은 엔터티 특성 `id`이(가) mbox 매개 변수 목록 `favorites`에 포함된 기준을 만듭니다.

```
curl -X POST \
  https://<serverhost>/api/recs/<client>/criteria/item \
  -H 'Accept: application/vnd.adobe.target.v1+json' \
  -H 'Accept-Encoding: gzip, deflate' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/json' \
  -H 'User-Agent: <from API client>' \
  -H 'X-Target-user-email: <email address>' \
  -H 'cache-control: no-cache' \
  -d '{
    "name": "viewed criteria",
    "criteriaTitle": "test title",
    "type": "VIEWED_CF",
    "key": "CURRENT",
    "daysCount": "TWO_WEEKS",
    "aggregation": "NONE",
    "backupDisabled": false,
    "partialDesignAllowed": true,
    "configuration": {
        "inclusionRules": [
            {
                "attribute": "id",
                "operation": "isContainedInList",
                "source": {
                    "name": "mbox.favorites",
                    "type": "MBOX"
                }
            }
        ]
    }
}'
```

이 호출은 즐겨찾기의 콘텐츠를 전달하는 페이지의 JavaScript과 쌍을 이룹니다.

```
<!-- pass in the value of mbox parameter "favorites" as JSON array -->
<script type="text/javascript">
   mboxCreate('myMbox','entity.id=<key>','favorites=["a","b","c"]');
</script>
```
