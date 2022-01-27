---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에 포함된 것은 무엇입니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 3009b232c3f0208c7632ad6369bf5d96334fe377
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 73%

---

# Target 릴리스 정보 (현재)

이러한 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 Target API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 사항에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.)

## [!DNL Target Standard/Premium] 22.1.2(2022년 1월 26일)

| 기능 | 세부 사항 |
| --- | --- |
| [!DNL Adobe Experience Platform] 대상 [!DNL Target] | 이제 소비하고 사용할 수 있습니다 [!DNL Adobe Experience Platform] 대상 [!DNL Target]. 다음 [!DNL Target] 팀, [!DNL Experience Platform] [!DNL Destinations] 팀 및 [!DNL Unified Profile Service] 팀은 &quot;동일한 페이지/다음 페이지 개인화&quot; 사용 사례의 일반 가용성을 발표하게 되어 기쁩니다.<br>에서 만든 대상 사용 [!DNL Adobe Experience Platform] 는 더 효과적인 개인화를 생성하는 더 풍부한 고객 데이터를 제공합니다. 다음 [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank}(RTCP), 기본 제공 [!DNL Adobe Experience Platform] 은 회사가 여러 엔터프라이즈 소스에서 알려진 데이터와 익명의 데이터를 결합하여 고객 프로필을 생성하고, 이 프로필을 작성하여 모든 채널 및 장치에서 실시간으로 개인화된 고객 경험을 제공할 수 있도록 지원합니다.<br>자세한 내용은 [Adobe Experience Platform의 대상 사용](/help/c-target/c-audiences/audiences.md#aep) in *대상자 만들기*.<br>Adobe 블로그를 읽고 비디오를 시청하십시오. [[!DNL Adobe] announces Same Page Enhanced Personalization with [!DNL Adobe Target] 및 [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}. |
| [!UICONTROL 대상] UI 새로 고침 | [!DNL Target] 사용자의 사용자 경험을 개선하기 위한 [!DNL Adobe Target] 팀의 지속적인 노력의 일부로 이 릴리스는 [!DNL Target] UI의 [!UICONTROL 대상] 및 [!UICONTROL 프로필 스크립트] 페이지를 새로 고칩니다. 이 업데이트는 다음과 같은 새로운 개선 사항을 추가하면서 이전에 일관되지 않고 디자인 패턴을 통합하고 표준화합니다.<ul><li>여러 대상을 동시 선택하고 삭제할 수 있는 기능</li><li>새로 단장된 [대상 빌더 디자인](/help/c-target/c-audiences/create-audience.md)</li><li>[!UICONTROL 대상] 라이브러리 규칙 빌더의 제외 규칙 지원</li><li>신속한 대상 검색을 위한 새로운 “대상 소스” 필터</li><li>세션 영구 검색 및 필터 옵션</li><li>의 작업 공간 간에 대상을 이동하는 기능 [!DNL Target Premium] 고객.</li></ul>자세한 내용은 [대상](/help/c-target/target.md)을 참조하십시오.<br>**참고**: 이 기능은 다음 8주 내에 다른 지역의 고객에게 롤아웃됩니다. |
| [!UICONTROL 프로필 스크립트] UI 새로 고침 | 또한 [!UICONTROL 프로필 스크립트] 라이브러리가 업데이트되고, 새로운 인터페이스와 몇 가지 생산성 업데이트가 여기에 포함됩니다.<ul><li>여러 프로필 스크립트를 동시 선택하고 삭제할 수 있는 기능</li><li>프로필 스크립트용 새로운 편집기 코드</li><li>코드 편집기 내 구문 강조 표시 및 오류 검사</li><li>키보드 단축키를 통한 자동 완성 토큰(mbox 또는 프로필) 매개 변수</li></ul>자세한 내용은 [방문자 프로필](/help/c-target/c-visitor-profile/visitor-profile.md)을 참조하십시오.<br>**참고**: 이 기능은 다음 8주 내에 다른 지역의 고객에게 롤아웃됩니다. |

## [!DNL Target Standard/Premium] 22.1.1(2022년 1월 12일)

이 릴리스에는 향후 통합을 위한 버그 수정 및 전제 조건 기능이 포함되어 있습니다.

## at.js 버전 2.8.0 (2022년 1월 7일)

이제 [!DNL Target] at.js JavaScript 라이브러리가 기능 사용 및 성능 원격 분석 데이터를 수집합니다. 개인 데이터는 수집되지 않습니다. 이 기능은 `targetGlobalSettings`에서 `telemetryEnabled`를 false로 설정하여 옵트아웃할 수 있습니다. 자세한 내용은 [telemetryEnabled in targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#telemetry)를 참조하십시오.

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
