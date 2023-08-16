---
keywords: 릴리스 정보;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: e130c68c838e799228956c598c583038a2f68ecf
workflow-type: ht
source-wordcount: '494'
ht-degree: 100%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Adobe Target] Edge 예정된 인프라 업그레이드 {#edge}

예정된 Edge 인프라 업그레이드를 수행하려면 추가 IP 또는 도메인이 허용 목록에 있어야 합니다. Edge 배포 41-48에 대한 NAT 및 IP/도메인을 검토하고 허용 목록에 추가하십시오. 인프라 업그레이드는 2023년 8월 9일에 시작됩니다.

자세한 내용은 *Adobe Target 개발자 안내서*&#x200B;의 [Target Edge 노드를 허용 목록에 추가](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/privacy/allowlist-edges.html){target=_blank}를 참조하십시오.

## [!DNL Target] Standard/Premium 23.8.1 (2023년 8월 9일)

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* [!UICONTROL 활동] 목록 페이지의 “[!UICONTROL 상태]” 열에 표시된 것처럼 때때로 활동이 제대로 동기화되지 않는 문제가 해결되었습니다. (TGT-46010 및 TGT-44831)
* [!UICONTROL Analytics for Target](A4T)을 보고 소스로 사용하는 활동의 [!UICONTROL 보고서] 페이지에 “[!UICONTROL Analytics에서 보기]” 링크가 표시되지 않는 문제가 해결되었습니다. (TGT-45808)
* 소수 자릿수가 포함 숫자 대신 백분율로 표시되도록 테이블의 값 표시가 조정되었습니다. 예를 들어 .08대신 8%가 표시됩니다. (TGT-45548)
* 고객이 [!UICONTROL 경험 타기팅](XT) 활동에 대한 [!UICONTROL 목표 및 설정] 페이지에서 키보드 포커스를 사용하여 다음 요소로 이동하지 못하는 문제가 해결되었습니다. (TGT-44526)
* 활동을 생성하는 도중 “[!UICONTROL 대상자 추가]” 대화 상자를 연 후 키보드 포커스가 사라지는 문제가 해결되었습니다. (TGT-44525)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko-KR) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [설명서 변경 내용](/help/main/r-release-notes/doc-change.md) | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다. |
| [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md). | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오. |
| [Adobe Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR){target=_blank} | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [Adobe 우선순위 제품 업데이트](https://www.adobe.com/kr/subscription/priority-product-update.html){target=_blank} | [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으십시오. |
| [Target 릴리스 정보 (프리릴리스)](/help/main/r-release-notes/target-release-notes.md){target=_blank} | 프리릴리스 정보를 포함하여 현재 달의 Target 릴리스에 대한 정보입니다. |
