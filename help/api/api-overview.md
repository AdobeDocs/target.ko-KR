---
keywords: api;apis;admin api;delivery api;reporting api;profile api
description: 관리, 전달, 보고 및 프로필 API를 비롯한 Adobe Target API에 대한 정보입니다.
title: Adobe Target API 개요
feature: APIs/SDKs
translation-type: tm+mt
source-git-commit: 9b57d5554884b06d278c3baef3b2c1d5f37bdeb5
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

---


# Adobe Target API 개요

[!DNL Adobe Target] API는 유형에 따라 그룹화할 수 있습니다.

| API 유형 | 이 기능을 통해 얻을 수 있는 이점 | 다운로드 링크 | 기타 유용한 링크 |
| --- | --- | --- |--- |
| 관리 | 활동, 대상, 오퍼 및 기타 개체([!DNL Recommendations] 개체, 기준, 디자인 등 포함)를 만들고 수정하고 삭제합니다. [!DNL Recommendations] API는 관리자 API의 유형입니다.) | <UL><li>[Target 관리 API Postman 컬렉션](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Adobe Target Tutorials에서 Recommendations ](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html) API  *사용* |
| 배달 | 최종 사용자에게 전달하기 위해 [!DNL Target]에서 최적화된 개인화된 컨텐츠를 검색합니다. | [Target 배달 API Postman 컬렉션](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| 보고 | 활동 결과 및 기타 보고 결과를 내보낼 수 있습니다. | 보고 API는 [Target Admin API Postman 컬렉션](https://developers.adobetarget.com/api/#admin-postman-collection)에 포함됩니다. |  |
| 프로필 | Adobe Target에 저장된 사용자 프로필을 검색하고 수정합니다. | [Target 프로필 API Postman 컬렉션](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>[!DNL Target] 관리 API([!DNL Recommendations] API 포함)와 [!DNL Target] 배달 API 사이에는 중요한 차이가 있습니다.
>
>* 관리 API를 사용하여 [!DNL Target]의 다양한 측면을 구성하여 [!DNL Target] UI에서도 구성할 수 있습니다. 관리 API는 인증이 필요합니다.
   >
   >
* 배달 API를 사용하여 콘텐츠를 검색할 수 있습니다. 배달 API는 인증이 필요하지 않습니다.
>
>
[!DNL Target] 관리 API를 사용하려면 먼저 Adobe I/O을 사용하여 인증을 구성해야 합니다.자세한 내용은 *Adobe Target Tutorials*&#x200B;의 [인증 ](https://experienceleague.adobe.com/docs/target-learn/tutorials/apis/configure-io-target-integration.html) 구성을 참조하십시오.
