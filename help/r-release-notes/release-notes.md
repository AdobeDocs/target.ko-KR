---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 68670f0b7753ee34c186a380004620ae4ba0cfd1
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 42%

---

# Target 릴리스 정보 (현재)

이러한 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 Target API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 사항에 대한 릴리스 정보도 포함됩니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js로부터의 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 미칩니다.
>
>새로운 [!DNL Adobe Experience Platform Web SDK] 의 가장 최근 또는 사이트에 문제가 발생할 가능성을 피하기 위해 at.js JavaScript 라이브러리로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.)

## [!DNL Target Standard/Premium] 21.10.4(2021년 10월 21일)

이 유지 관리 릴리스에는 다음과 같은 향상된 기능이 포함되어 있습니다.

| 기능 | 세부 사항 |
| --- | --- |
| 장바구니 기반 Recommendations | 방문자 장바구니의 컨텐츠를 기반으로 권장 사항을 제공하는 새로운 알고리즘 그룹입니다.<br>자세한 내용은 [기준 만들기](/help/c-recommendations/c-algorithms/create-new-algorithm.md) 및 의 &quot;장바구니 추가/장바구니 보기/체크아웃 페이지&quot; 및 &quot;방문자의 장바구니에 이미 있는 항목 제외&quot;를 참조하십시오 [Recommendations 계획 및 구현](/help/c-recommendations/plan-implement.md). |

## [!DNL Target Standard/Premium] 21.10.3(2021년 10월 19일)

이 유지 보수 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함되어 있습니다.

* 고객이 [!UICONTROL A4T] 패널 [!DNL Analysis Workspace] 다음을 클릭하여 [!UICONTROL Analytics에서 보기] 버튼 [!DNL Target] 활동 보고. (TGT-42099, TGT-42100)
* 이(가) [!UICONTROL 디자인 편집] 편집하는 동안 표시되지 않는 단추 [!UICONTROL A/B 테스트] 및 [!UICONTROL 경험 타깃팅] (XT) 활동을 사용할 때 [!UICONTROL 양식 기반 경험 작성기]. (TGT-41980)
* Adobe Social이 사용자 지정 브랜드 도메인을 인식하지 못하는 문제를 해결했습니다. [!UICONTROL 호환 가능] 새 항목을 만드는 동안 기준 선택에 표시되지 않는 확인란 [!UICONTROL Recommendations] 활동. (TGT-42053)
* 선택할 수 없을 때 표시되는 잘못된 오류 메시지가 수정되었습니다 [!DNL Analytics] 를 보고 소스로 사용(A4T)할 필요는 없습니다 [!DNL Analytics] 사용 권한. (TGT-41954)
* 여러 액세스 가능성 수정 사항을 구현하여 [!DNL Target] UI.

## [!DNL Target Standard/Premium] 21.10.2(2021년 10월 13일)

사용 시 다음과 같은 향상된 기능을 추가했습니다 [!DNL Target] [!UICONTROL 대상] 사용 [!DNL Adobe Experience Platform Web SDK]:

* 의 다양한 위치에 경고 아이콘, 팝오버와 메시지를 추가했습니다 [!DNL Target] 대상이 소스에서 삭제되었으며 더 이상 을 사용할 수 없음을 나타내는 UI입니다 [!DNL Target] 활동.

   다음 그림은 아이콘, 팝오버 및 메시지가 표시되는 몇 가지 위치를 보여줍니다.

   * [!UICONTROL 활동] 목록 페이지

      ![활동 목록 페이지의 소스 메시지에서 삭제된 대상](assets/deleted-at-source-audiences-list.png)

   * 활동 [!UICONTROL 개요] 페이지:

      ![개요 페이지의 소스 메시지에서 삭제된 대상](assets/deleted-at-source-overview.png)

   * [!UICONTROL 경험] 활동 만들기 워크플로우의 단계:

      ![소스 메시지에서 삭제된 대상 [!UICONTROL 경험] 페이지](assets/deleted-at-source-experiences.png)

   * [!UICONTROL 타깃팅] 활동 만들기 워크플로우의 단계:

      ![소스 메시지에서 삭제된 대상 [!UICONTROL 타깃팅] 페이지](assets/deleted-at-source-targeting.png)

   * [!UICONTROL 목표 및 설정] 활동 만들기 워크플로우의 단계:

      ![소스 메시지에서 삭제된 대상 [!UICONTROL 목표 및 설정] 페이지](assets/deleted-at-source-goals-settings.png)

   * 대상 개선([!UICONTROL 대상 바꾸기] on [!UICONTROL 타깃팅] 활동 작성 워크플로우 단계):

* 대상 결합 기능을 사용하려고 하는데 소스에서 대상 중 하나가 삭제된 경우 [!UICONTROL 저장] 이 비활성화되어 있습니다.

## [!DNL Target Standard/Premium] 21.10.1 (2021년 10월 6일)

이번 릴리스에는 다음과 같은 새 기능이 포함되어 있습니다.

| 기능 | 세부 사항 |
| --- | --- |
| [!UICONTROL 대상자 UI 새로 고침] | 의 일부로 [!DNL Adobe Target] 사용자 경험을 향상시키기 위한 팀의 지속적인 노력 [!DNL Target] 사용자, 이 릴리스는 새로 고침됩니다. [!UICONTROL 대상] 및 [!UICONTROL 프로필 스크립트] 페이지의 페이지 [!DNL Target] UI. 이 업데이트는 다음과 같은 새로운 개선 사항을 추가하면서 이전에 일관성이 없는 디자인 패턴을 통합 및 표준화합니다.<ul><li>여러 대상을 동시에 선택하고 삭제하는 기능</li><li>새로 고친 [audience builder 디자인](/help/c-target/c-audiences/create-audience.md)</li><li>에서 제외 규칙 지원 [!UICONTROL Audience] 라이브러리 규칙 빌더</li><li>대상 검색 속도를 높일 수 있는 새로운 &quot;대상 소스&quot; 필터</li><li>세션 영구 검색 및 필터 옵션</li></ul>자세한 내용은 [대상](/help/c-target/target.md)을 참조하십시오.<br>**참고**: 새로운 [!UICONTROL 대상] 현재 [!DNL Target] 베타 프로그램. 이 UI 새로 고침은 10월 19일 화요일 및 2021년 10월 21일 목요일에 나머지 모든 고객에 대해 다시 활성화됩니다. |
| [!UICONTROL 프로필 스크립트] UI 새로 고침 | 다음 [!UICONTROL 프로필 스크립트] 라이브러리도 업데이트되었으며, 다음과 같이 새로 고친 인터페이스와 몇 가지 생산성 업데이트가 포함됩니다.<ul><li>여러 프로필 스크립트를 동시에 선택하고 삭제할 수 있는 기능</li><li>프로필 스크립트를 위한 새 코드 편집기</li><li>코드 편집기 내에서 구문 강조 표시 및 오류 확인</li><li>키보드 단축키를 통해 토큰(mbox 또는 프로필) 매개 변수 자동 완료</li></ul>자세한 내용은 [방문자 프로필](/help/c-target/c-visitor-profile/visitor-profile.md). |
| ![Premium 배지](/help/assets/premium.png) Recommendations 기준 만들기 및 편집 | 다음 [!UICONTROL Recommendations 기준] 만들기 및 편집 워크플로우는 목표를 달성하기 위해 올바른 권장 사항 알고리즘 및 설정을 선택하는 작업을 간소화하기 위해 간소화되었습니다.<br>자세한 내용은 [기준 만들기](/help/c-recommendations/c-algorithms/create-new-algorithm.md). |
| ![Premium 배지](/help/assets/premium.png) Recommendations 전환 확인 기간 및 알고리즘 새로 고침 비율 개선 사항 | 이제 6시간 전환 확인 기간과 함께 &quot;가장 많이 본 항목&quot; 및 &quot;최상위 판매자&quot; 알고리즘을 실행하여 가장 최근 트렌드를 표시하는 콘텐츠를 캡처할 수 있습니다. 6시간 전환 확인 기간을 선택하면 권장 사항 결과가 하루 종일 3-6시간마다 업데이트됩니다.<br>자세한 내용은 [데이터 소스](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in *기준 만들기*. |

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko_KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 정보 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 정보](/help/r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 정보 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다.<br>자세한 내용은 [Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR)을 참조하십시오. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html))에 등록하십시오. |
| 향후 릴리스 정보 | 프리릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 정보 - 프리릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |
