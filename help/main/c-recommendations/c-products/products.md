---
keywords: 제품;컬렉션
description: Adobe [!DNL Target] Recommendations의 엔터티에 대해 알아봅니다. 엔터티는 문서, 동영상 또는 제품과 같이 [!DNL Target]을(를) 사용하여 추천할 항목을 참조합니다.
title: 엔티티를 사용하려면 어떻게 합니까?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Target Premium에 포함된 내용을 확인합니다."
feature: Recommendations
exl-id: ffe23eea-b914-4c86-ad54-c63c1cc1c0d7
TQID: 'https://experienceleague.adobe.com/zfISb59XJ5qrD1-FA0syglPPswIL8cA0N0pBpY4tgIE'
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
source-git-commit: 5ed511322cc9f04c349471f8ad84a17526d4925f
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%
---
# 엔티티 시작 {#get-started-entities}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Adobe Target Recommendations]에 있는 엔터티와 해당 엔터티를 관리할 위치를 알아봅니다.

>[!ENDSHADEBOX]

엔터티는 [!DNL Recommendations]이(가) 추천할 수 있는 항목입니다. 엔티티는 제품, 컨텐츠(예: 문서, 슬라이드 쇼, 이미지, 동영상 또는 TV 프로그램), 구인 목록, 레스토랑 등이 될 수 있습니다.

[!DNL Recommendations]은(는) 설정한 기준에 따라 컬렉션의 항목을 표시합니다.

## 엔티티가 권장 사항에 도달하는 방법

엔터티에 대한 정보는 다음을 포함하여 여러 가지 방법으로 [!DNL Recommendations]에 전달할 수 있습니다.

* mbox 또는 `targetPageParams`을(를) 사용하여 페이지에서 [엔티티 특성](/help/main/c-recommendations/c-products/entity-attributes.md)을(를) 보냈습니다.
* CSV 파일, [!DNL Google Product Search] 피드 형식 또는 [!DNL Adobe Analytics] 제품 분류를 사용할 수 있는 [피드](/help/main/c-recommendations/c-products/feeds.md)를 사용합니다.
* 게재 API 사용.

[!DNL Target]이(가) 피드와 mbox 모두에서 항목에 대한 데이터를 수집하는 경우 가장 최근 데이터가 사용됩니다.

업로드된 엔티티 및 엔티티 속성값은 61일 후에 만료됩니다. 적어도 60일마다 한 번씩 각 항목을 다시 보냅니다. 그렇지 않으면 [!DNL Target]이(가) 더 이상 관련성이 없는 항목을 고려하여 카탈로그에서 제거합니다.

## 엔티티 관리

다음 페이지를 사용하여 엔티티로 작업합니다.

* [엔터티 특성](/help/main/c-recommendations/c-products/entity-attributes.md) 및 [사용자 지정 엔터티 특성](/help/main/c-recommendations/c-products/custom-entity-attributes.md): [!DNL Recommendations]에 전달하는 제품 또는 콘텐츠 정보를 정의합니다.
* [피드](/help/main/c-recommendations/c-products/feeds.md): 엔터티 또는 콘텐츠 정보를 권장 사항으로 가져옵니다.
* [카탈로그 검색](/help/main/c-recommendations/c-products/catalog-search.md): 카탈로그에서 항목을 찾습니다.
* [컬렉션](/help/main/c-recommendations/c-products/collections.md): 컬렉션을 설정합니다. [!DNL Recommendations] 활동을 만들 때 각 경험에 대해 컬렉션이 선택됩니다.
* [제외](/help/main/c-recommendations/c-products/exclusions.md): 특정 항목이 권장 사항에 표시되지 않도록 합니다. 제외는 계정의 모든 활동에 적용됩니다.
