---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 8f5e2c5025dc4b9caf31f51c03fb073ddd9ba756
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 41%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2021년 10월 6일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js에서 발송된 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 줍니다.
>
>사이트에 문제가 발생하지 않도록 하려면 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

## [!DNL Target Standard/Premium] 21.10.1(2021년 10월 6일)

이번 릴리스에는 다음과 같은 새 기능이 포함되어 있습니다.

| 기능 | 세부 사항 |
| --- | --- |
|  AudiencesUI 새로 고침 | [!DNL Adobe Target] 팀이 [!DNL Target] 사용자에 대한 사용자 경험을 향상시키기 위한 지속적인 노력의 일환으로 이 릴리스는 [!DNL Target] UI에서 [!UICONTROL Audiences] 및 [!UICONTROL 프로필 스크립트] 페이지를 새로 고칩니다. 이 업데이트는 다음과 같은 새로운 개선 사항을 추가하면서 이전에 일관성이 없는 디자인 패턴을 통합 및 표준화합니다.<ul><li>여러 대상을 동시에 선택하고 삭제하는 기능</li><li>새로 고친 [대상 빌더 디자인](/help/c-target/c-audiences/create-audience.md)</li><li>[!UICONTROL Audience] 라이브러리 규칙 빌더에서 제외 규칙 지원</li><li>대상 검색 속도를 높일 수 있는 새로운 &quot;대상 소스&quot; 필터</li><li>세션 영구 검색 및 필터 옵션</li></ul>자세한 내용은 [대상](/help/c-target/target.md)을 참조하십시오.<br>**참고**: 이 UI 새로 고침은 EMEA 지역의 고객에게만 영향을 줍니다. 북미 등 전 세계 다른 지역의 고객은 다음 주에 새로 고친 UI를 볼 수 있습니다. |
| [!UICONTROL 프로필 ] 스크립트 UI 새로 고침 | [!UICONTROL 프로필 스크립트] 라이브러리도 업데이트되었으며, 다음과 같이 새로 고쳐진 인터페이스와 몇 가지 생산성 업데이트가 포함됩니다.<ul><li>여러 프로필 스크립트를 동시에 선택하고 삭제할 수 있는 기능</li><li>프로필 스크립트를 위한 새 코드 편집기</li><li>코드 편집기 내에서 구문 강조 표시 및 오류 확인</li><li>키보드 단축키를 통해 토큰(mbox 또는 프로필) 매개 변수 자동 완료</li></ul>자세한 내용은 [방문자 프로필](/help/c-target/c-visitor-profile/visitor-profile.md)을 참조하십시오.<br>**참고**: 이 UI 새로 고침은 EMEA 지역의 고객에게만 영향을 줍니다. 북미 등 전 세계 다른 지역의 고객은 다음 주에 새로 고친 UI를 볼 수 있습니다. |
| ![Premium ](/help/assets/premium.png) 배지권장 사항 기준 만들기 및 편집 | [!UICONTROL Recommendations 기준] 만들기 및 편집 워크플로우는 목표를 달성하기 위해 적합한 권장 사항 알고리즘과 설정을 선택하는 작업을 간소화할 수 있게 간소화되었습니다.<br>자세한 내용은  [기준 만들기](/help/c-recommendations/c-algorithms/create-new-algorithm.md)를 참조하십시오. |
| ![Premium ](/help/assets/premium.png) 배지권장 사항 전환 확인 기간 및 알고리즘 새로 고침 비율 개선 사항 | 이제 6시간 전환 확인 기간과 함께 &quot;가장 많이 본 항목&quot; 및 &quot;최상위 판매자&quot; 알고리즘을 실행하여 가장 최근 트렌드를 표시하는 콘텐츠를 캡처할 수 있습니다. 6시간 전환 확인 기간을 선택하면 권장 사항 결과가 하루 종일 3-6시간마다 업데이트됩니다.<br>자세한 내용은  [기준 만들기](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) 에서  *데이터 소스*&#x200B;를 참조하십시오. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
