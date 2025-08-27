---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: cc0bf794e366f304b52db309d4e3a66292d7ea32
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 20%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트: 2025년 8월 27일**

>[!NOTE]
>
>* 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 이 문서의 정보는 특히 릴리스 전에 자주 업데이트됩니다.
>
>* 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하세요.
>
>* 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target Standard/Premium] 25.8.4(2025년 9월 1일)

이번 릴리스에는 다음과 같은 업데이트 및 수정 사항이 포함되어 있습니다.

**[!UICONTROL Activities]**

+++세부 정보 보기
* **고객은[!UICONTROL Activity Overview]**&#x200B;에서 활동 또는 문서 이름을 복사할 수 없습니다. 이전에는 업데이트된 활동 만들기 프로세스에서 [!UICONTROL Activity Overview]에서 직접 활동 또는 관련 오퍼/문서를 복사할 수 없었습니다. 이 제한 사항은 특히 작은 화면에서 유용성에 영향을 주었습니다. 이제 고객은 해결 방법 없이 활동과 문서 이름을 모두 쉽게 복사할 수 있습니다. (TGT-51850)
* **활동을 만드는 동안 조정된 [!DNL Target] 고객 데이터를 사전에 수집**: [!DNL Target] 고객의 보고서, 콘텐츠 및 스크린샷을 사전에 수집하도록 설정하여 활동 만들기 프로세스를 개선했습니다. 이러한 향상된 기능은 기존 사용 사례에서 식별된 데이터 차이를 해결하고 활동 및 실험 설정 중 더 정확한 통찰력을 확보하는 데 도움이 됩니다. (TGT-52415)

+++

**[!UICONTROL Recommendations]**

+++세부 정보 보기
* **제품 목록이 [!UICONTROL View Collection] 대화 상자에 표시되지 않았습니다.** 이전에는 [!UICONTROL Recommendations] 탭에서 컬렉션을 볼 때 고객이 제품 목록을 볼 수 없었습니다. 이제 [!UICONTROL View Collection] 대화 상자에 연결된 제품이 올바르게 표시되므로 업데이트된 Recommendations UI의 투명성과 유용성이 향상되었습니다. (TGT-50531)
* **[!UICONTROL Product Catalog Search] 고급 검색에서 대소문자를 구분하는 필터링을 수행하는 문제가 해결되었습니다**: 이제 [!UICONTROL Product Catalog Search] 페이지의 고급 검색 필터링에서 백엔드와 GraphQL 서비스 모두의 동작에 맞게 대소문자를 구분하는 것을 올바르게 무시합니다. 이 업데이트는 텍스트 대소문자에 관계없이 고객을 위한 일관되고 정확한 제안 결과를 보장합니다. (TGT-53585)

+++

**[!UICONTROL Reports]**

+++세부 정보 보기
* **잘못된 대상 이름 오류로 인해 데스크톱 대상에 대한 보고서를 로드하지 못했습니다.**: 고객이 활동 만들기 프로세스에서 한 대상에 대한 보고서를 보려고 하면 GraphQL 오류가 발생했습니다. 시스템에서 &quot;잘못된 대상 이름: XXXXX&quot; 메시지를 반환하여 보고 데이터에 액세스할 수 없습니다. 이제 보고서가 데스크탑 대상자에 대해 올바르게 로드됩니다. (TGT-53371)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++세부 정보 보기
* **함수 누락으로 인해 [!UICONTROL Enhanced Experience Composer]&#x200B;(EEC)을(를) 사용하여 &quot;쿠키 수락&quot;을 클릭하지 못했습니다**: 고객이 EEC를 통해 쿠키를 수락하려고 하면 콘솔 오류가 발생한다고 보고했습니다. `handleclickAcceptAllButton is not defined`. 이제 쿠키 수락 기능이 예상대로 작동하여 업데이트된 UI에서 활동을 만드는 동안 더 원활한 경험을 보장합니다. (TGT-52794)
* **새 EEC UI가 이전 UI에서 이전에 지원된 특정 페이지를 로드하지 못했습니다.**: 고객이 새 EEC가 사이트에서 iframe 버스팅 코드가 있어도 레거시 UI에서 액세스할 수 있었던 일부 페이지를 로드할 수 없다고 보고했습니다. 업데이트된 활동 만들기 프로세스는 이제 이러한 페이지 로드를 지원하며, 활동 만들기 워크플로우에 대한 호환성을 복원합니다. (TGT-53061)
* **경험을 편집할 때 VEC에 빈 흰색 화면이 표시됨**: 특정 테넌트의 고객이 업데이트된 VEC에서 경험을 편집하려고 할 때 VEC 화면이 비어 있다고 보고했습니다. 이 문제는 새로 생성된 활동과 이전 활동 모두에 영향을 주어 워크플로우 연속성을 방해했습니다. 이제 VEC가 올바르게 로드되어 고객이 중단 없이 경험을 편집할 수 있습니다. (TGT-53547)
* **특정 활동을 로드할 때 VEC가 충돌하여 빈 화면이 표시됨**: 특정 테넌트의 고객이 VEC가 특정 활동을 로드하지 못했다고 보고했습니다. 경험 편집기가 충돌하기 전에 &quot;초기 수정 사항 적용&quot;에 멈춰 있어 빈 화면이 표시됩니다. 콘솔 오류가 정의되지 않은 속성을 읽지 못했음을 나타냅니다. 이제 편집기는 업데이트된 VEC에서 오류 없이 영향을 받는 활동을 로드합니다. (TGT-53548)

+++

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 노트: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=ko){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
