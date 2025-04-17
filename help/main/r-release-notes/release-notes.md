---
keywords: 릴리스 노트;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트,현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 938351d258746031a6e47a935a37e2caccbf6e36
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 30%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target Standard/Premium] 25.4.4(2025년 4월 17일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 활동에서 중복 옵션을 확인하는 방법을 사용자에게 안내하는 오류 메시지를 추가했습니다. (TGT-51927)
* 리디렉션 오퍼가 있는 페이지 또는 경험을 삭제할 때 `ClickTrack` 선택기가 제거되지 않았던 문제를 수정했습니다. (TGT-51952)
* 빈 `ClickTrack` 선택기를 허용하여 발생하는 문제를 해결했습니다. 이제 [!DNL Target]을(를) 사용하려면 선택기 필드가 비어 있지 않아야 합니다. (TGT-52107)
* 중복 이름이 있는 지표를 잘못 허용하는 문제가 수정되었습니다. 이제 지표에 고유한 이름이 필요합니다. (TGT-52201)
* [!UICONTROL Automated Personalization]&#x200B;(AP) 활동에서 오퍼 수준 타깃팅을 편집할 때 대상 정의가 표시되지 않던 문제를 수정했습니다. (TGT-52148)
* [!UICONTROL Editor] 권한이 있는 고객이 활동을 저장할 수 없는 문제를 해결했습니다. (TGT-52227)
* 옵션이 변경되지 않은 상태로 유지되면 `OptionLocalIDs`이(가) 더 이상 잘못 증가하지 않습니다. (TGT-52139)
* 활동을 만들려고 할 때 &quot;잘못된 `optionLocalIds`&quot; 메시지가 표시되는 문제를 해결했습니다. (TGT-52154)
* 활동에 대해 정의된 `OptionLocalIDs`과(와) 경험을 정의하는 데 사용된  간의 불일치가 수정되었습니다. (TGT-52215)
* A/B 활동을 만들려고 할 때 유효성 검사 오류가 발생하는 문제를 해결했습니다. (TGT-51923)

## [!DNL Target Standard/Premium] 25.4.3(2025년 4월 11일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 고객이 특정 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동에 대한 대상 정보 팝업을 열 수 없도록 하는 오류가 수정되었습니다. (TGT-52049)
* VEC([!UICONTROL Visual Experience Composer])에서 변경한 후 대상 설정이 &quot;[!UICONTROL All Visitors]&quot;(으)로 되돌아가는 문제가 해결되었습니다. (TGT-52132)
* 특정 활동에 대해 대상 세분화가 표시되지 않던 문제를 수정했습니다(TGT-52057).
* 고객이 기본 작업 영역에 [!UICONTROL Experience Fragment]을(를) 삽입할 수 없는 문제를 해결했습니다. (TGT-52073)
* 오퍼가 &quot;콘텐츠를 찾을 수 없음&quot;으로 표시되고 [!UICONTROL Automated Personalization]&#x200B;(AP) 활동의 [!UICONTROL Offers] 페이지에 표시되지 않는 문제가 해결되었습니다. (TGT-52150)
* 활동 내에 중복 대상을 허용하는 기능이 추가되었습니다. (TGT-51200)
* 편집한 후 XT 활동에 대한 [!UICONTROL Goals & Settings] 페이지에 잘못된 mbox 이름이 표시되는 문제를 해결했습니다. (TGT-52026)
* `defaultContent`이(가) `experiences/optionLocations`에 없음에도 불구하고 옵션에 표시되는 문제를 해결했습니다. (TGT-52036)
* 빈 문자열이 null 값으로 변환되지 않도록 하는 문제를 해결했습니다. (TGT-52037)
* 고객이 편집 후 [!UICONTROL Goals & Settings] 페이지의 [!UICONTROL Reporting Settings]에서 [!UICONTROL Optimization Goal]을(를) 다시 구성해야 하는 문제를 해결했습니다. (TGT-52071)
* 페이지 전달 규칙이 없는 활동에서 [!UICONTROL Overview] 페이지에 여러 규칙이 표시되는 문제를 해결했습니다. (TGT-52084)
* 이모지와 같은 기본 다국어 평면 외부에 있는 문자가 있는 오퍼를 저장하려는 사용자에 대한 오류 메시지가 추가되었습니다. (TGT-52105)
* 활동을 열면 오류 메시지가 트리거되는 문제가 해결되었습니다. &quot;이 활동은 소스에서 삭제된 하나 이상의 대상을 사용합니다.&quot; (TGT-52120)
* 편집하는 동안 업데이트된 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 ClickTrack 지표가 표시되지 않던 문제를 수정했습니다. (TGT-52152)
* 쿼리 매개 변수를 활동 위치로 사용하는 URL에 활동의 [!UICONTROL Overview] 페이지에 쿼리 매개 변수가 표시되지 않던 문제를 해결했습니다. (TGT-51635)
* 전체 경험 URL이 [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 내의 [!UICONTROL Browse mode]에 표시되지 않는 문제를 해결했습니다. (TGT-52101)
* 활동을 편집하면 페이지 게재가 URL 끝에 &quot;/&quot;를 추가하여 유효하지 않게 되는 문제를 해결했습니다. (TGT-52114)
* [!UICONTROL Form-Based Experience Composer]의 [!UICONTROL Activity QA] 링크가 [!DNL Adobe Experience Cloud] 홈 페이지로 잘못 리디렉션되는 문제가 해결되었습니다. (TGT-52055)
* 저장하고 다시 연 후 [!UICONTROL A/B Test] 활동에 추가된 추가 페이지가 유지되지 않던 문제를 수정했습니다. (TGT-51994)
* 고객이 인라인 스타일 섹션에서 스타일을 삭제할 수 없는 문제를 해결했습니다. (TGT-52070)
* 기존 UI와 유사한 [!UICONTROL Activity QA] 대화 상자에서 [대상 정의 카드](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780)에 대한 액세스를 복원했습니다. (TGT-52056)
* 업데이트된 UI는 수정 없이 페이지 또는 대상자를 저장하지 않았습니다. 고객이 새 페이지나 대상을 활동에 추가했지만 변경하지 않는 경우 [!DNL Target]이(가) 저장 시 수정되지 않은 대상을 삭제했습니다. 이 동작을 사용자에게 알리기 위해 관련 위치에 알림이 추가되었습니다. (TGT-52104)

## [!DNL Target Standard/Premium] 25.4.1(2025년 4월 2일)

이번 릴리스에는 다음과 같은 수정 사항 및 업데이트가 포함됩니다.

* 경험 대상이 활동에서 사라지는 문제를 해결했습니다. (TGT-52003)
* 게재 중 예기치 않은 요소가 발생하는 문제를 해결했습니다. (TGT-52011)
* 고객이 활동 편집 중에 [!UICONTROL r]보기 페이지의 타깃팅 그래프에서 대상을 볼 수 없도록 하는 문제를 해결했습니다. (TGT-52050)
* 고객이 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동에서 우선순위 순서대로 경험을 재정렬할 수 없는 문제를 해결했습니다. (TGT-52054)
* 텍스트 스타일 변경을 실행 취소할 때 잘못된 렌더링이 발생하는 문제를 해결했습니다. (TGT-51876)
* 리디렉션 오퍼를 수정할 때 [!DNL Target]이(가) 해당 오퍼와 연결된 [!UICONTROL ClickTrack] 선택기도 제거하는 문제를 해결했습니다. (TGT-51936)
* [!UICONTROL ClickTrack]을(를) 취소할 때 [!DNL Target]이(가) 선택기를 잘못 저장하는 문제를 해결했습니다. (TGT-51937)
* [!UICONTROL Goals & Settings] 페이지에서 mbox 선택기를 열고 닫은 후 변경하지 않고 잘못된 이름 오류를 트리거하는 문제를 해결했습니다. (TGT-51983)
* 기존 [!DNL Target] UI에서 만든 임시 오퍼 편집을 차단하는 문제를 해결했습니다. (TGT-51984)
* 사용자 지정 코드가 포함된 임시 오퍼가 있는 편집 활동을 차단하는 문제를 해결했습니다. (TGT-51995)
* 결합된 대상 정의를 편집할 때 제외 규칙이 포함 규칙으로 표시되던 문제를 수정했습니다. (TGT-51999)
* 경험 편집 중에 사용자 지정 코드가 올바르게 표시되지 않는 문제를 해결했습니다. (TGT-52005)
* 탐색 모음 앞에 콘텐츠를 삽입할 때 [!UICONTROL Insert Before] 옵션을 사용할 수 없는 문제를 해결했습니다. (TGT-52031)
* 보고에서 기본 경험이 올바르게 강조 표시되지 않는 문제를 해결했습니다. (TGT-51716)
* 활동을 만들 때 `default message [Invalid optionLocalIds: xx]]` 메시지를 트리거하는 문제를 해결했습니다. (TGT-52038)

## at.js 버전 2.11.8(2025년 3월 31일)

* 크기 조정 및 이동 작업 중 에지 사례를 방지하기 위해 문자열 접미사 유효성 검사에서 CodeQL로 식별된 취약성이 해결되었습니다. (TNT-51516)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 설명서 변경 내용, 이전 릴리스 정보 및 Experience Cloud 릴리스 정보

각 릴리스에 대한 정보 외에도, 다음 리소스를 통해 추가 정보를 구할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [설명서 변경 내용](/help/main/r-release-notes/doc-change.md) | 이 릴리스 정보에 포함되지 않은 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다. |
| [이전 릴리스에 대한 릴리스 정보](/help/main/r-release-notes/release-notes-for-previous-releases.md). | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하십시오. |
| [Adobe Experience Cloud 릴리스 노트](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ko-KR){target=_blank} | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 정보를 표시합니다. |

## 프리릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| [Adobe 우선순위 제품 업데이트](https://www.adobe.com/kr/subscription/priority-product-update.html){target=_blank} | [!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으십시오. |
| [Target 릴리스 정보 (프리릴리스)](/help/main/r-release-notes/target-release-notes.md){target=_blank} | 프리릴리스 정보를 포함하여 현재 달의 Target 릴리스에 대한 정보입니다. |
