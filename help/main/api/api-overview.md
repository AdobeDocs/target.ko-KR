---
keywords: api;api;관리 api;배달 api;보고 api;프로필 api
description: Adobe 찾기 [!DNL Target] 관리, 배달, 보고 및 프로필 API를 포함한 API입니다.
title: 어디에 있습니까 [!DNL Target] API 및 SDK 설명서?
feature: APIs/SDKs
role: Developer
exl-id: 2a0232cc-9a6a-42f4-afb6-4b3e2b13939c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---

# Adobe [!DNL Target] API 개요

[!DNL Adobe Target] API는 유형에 따라 그룹화할 수 있습니다. 관리, 게재, 보고 및 프로필 API.

| API 유형 | 다음을 수행할 수 있는 기능 | 다운로드 링크 | 기타 유용한 링크 |
| --- | --- | --- |--- |
| 관리 | 활동, 대상, 오퍼 및 기타 개체(포함) 만들기, 수정 및 삭제 [!DNL Recommendations] 엔티티, 기준, 디자인 등. 다음 [!DNL Recommendations] API는 관리 API 유형입니다.) | <UL><li>[Target 관리 API Postman Collection](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Recommendations API 사용](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html) in *Adobe Target Tutorials* |
| 배달 | 에서 최적화 및 개인화된 콘텐츠 검색 [!DNL Target] 최종 사용자에게 전달할 수 있습니다. | [Target 배달 API Postman Collection](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| 보고 | 활동 결과 및 기타 보고 결과를 내보냅니다. | 보고 API는 [Target 관리 API Postman 컬렉션](https://developers.adobetarget.com/api/#admin-postman-collection). |  |
| 프로필 | Adobe Target에 저장된 사용자 프로필을 검색하고 수정합니다. | [Target 프로필 API Postman Collection](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>사이에는 중요한 차이점이 있다 [!DNL Target] 관리 API(다음을 포함) [!DNL Recommendations] API) 및 [!DNL Target] 배달 API:
>
>* 관리 API를 사용하면 다음과 같은 다양한 측면을 구성할 수 있습니다 [!DNL Target] 다음에서 [!DNL Target] UI. 관리 API에는 인증이 필요합니다.
>
>* 배달 API를 사용하여 콘텐츠를 검색할 수 있습니다. 배달 API에는 인증이 필요하지 않습니다.
>
>를 사용하려면 [!DNL Target] 관리 API인 경우 먼저 Adobe I/O을 사용하여 인증을 구성해야 합니다. 자세한 내용은 [인증 구성](https://experienceleague.adobe.com/docs/target-learn/tutorials/apis/configure-io-target-integration.html) in *Adobe Target Tutorials*.
