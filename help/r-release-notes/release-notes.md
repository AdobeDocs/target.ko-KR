---
description: 이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
keywords: 릴리스 노트;사전 릴리스
seo-description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
seo-title: Target 릴리스 노트(현재)
solution: Target
title: Target 릴리스 노트(현재)
topic: 권장 사항
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다.

## 공지

다음 중요 알림을 확인하십시오.

* 2019 년 2 월 20 일, EMEA, 일본 및 APAC 지역에서 Adobe Target 인프라가 더 이상 TLS 1.1 이상을 지원하지 않는 이전 장치나 웹 브라우저에서 최종 사용자의 데이터를 수집하지 않도록 업그레이드되었습니다. 동일한 업그레이드가 2019 년 4 월 1 일에 **북미 지역에 대해서도 예정되어**있습니다. TLS 1.2로 마이그레이션하면 보안이 강화됩니다. 세부 사항을 검토하고 IT 팀에 변경 사항을 계획하여 원활한 전환을 수행해야 합니다. 자세한 내용은 [TLS (Transport Layer Security) 암호화 변경을 참조하십시오](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).
* [!DNL Target]과 [!DNL Adobe Marketing Cloud]는 2019년 3월부터 Microsoft Internet Explorer 11에 대한 지원을 중단할 예정입니다. 이 변경 사항은 [!DNL Target] 작성에만 영향을 주며, 경험 전달에는 영향을 주지 않습니다. Microsoft Edge나 다른 브라우저로 전환하십시오. 자세한 내용은 [지원되는 브라우저](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md)를 참조하십시오.

## Mobile App Visual Experience Composer (2019 년 5 월 14 일) {mobile-vec}

| 기능/향상 | 설명 |
| --- | --- |
| Mobile App Visual Experience Composer (VEC) | 모바일 앱 VEC를 사용하면 지속적인 개발 종속성 및 앱 릴리스 주기를 사용하지 않고도 고유한 방식으로 기본 모바일 앱에서 콘텐츠를 맞춤화하고 콘텐츠를 개인화할 수 있습니다.<br>자세한 내용은 다음 문서를 참조하십시오.<ul><li>[모바일 앱 시각적 경험 작성기](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android - 모바일 앱 설정](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS - 모바일 앱 설정](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[모바일 VEC에서 클릭 추적 설정](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li></ul> |

## [!DNL Target] Standard/Premium 19.4.2 (2019 년 4 월 30 일) {#release-19-4-2}

이 릴리스에는 다음의 기능, 변경 및 개선 사항이 포함되었습니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

### 기능 업데이트

| 기능/향상 | 설명 |
| --- | --- |
| [!UICONTROL 시각적 경험 작성기] | Visual [!UICONTROL Experience Composer] (VEC) 에는 다음 개선 사항이 포함되어 있어 작업을 보다 빠르고 효율적으로 수행할 수 있습니다.<ul><li>이제 클릭 추적을 설정할 때 DOM 경로 기능을 사용할 수 있습니다.<br>자세한 내용은 클릭 추적을 참조하십시오 [](/help/c-activities/r-success-metrics/click-tracking.md#considerations).</li><li>스타일 패널을 사용하여 선택한 요소의 기존 스타일 값을 보거나 편집할 수 있습니다. 또한 스타일을 추가할 수도 있습니다.<br>스타일 패널에 액세스하려면 VEC 내에서 페이지 요소를 클릭한 다음 [!UICONTROL 편집] &gt; [!UICONTROL 스타일을 클릭합니다].<br>VEC 오른쪽에 스타일 패널이 표시됩니다. 패널에는 선택한 요소를 편집하거나 추가할 수 있는 스타일 목록이 포함되어 있습니다. CSS (Cascading Style Sheet) 를 사용하거나 개발자로부터 코드를 받은 경우 CSS 편집기를 사용하면 변경 사항을 보고 스타일을 추가할 수 있습니다.<br>자세한 내용은 Visual Experience Composer 옵션 [스타일을](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) **참조하십시오.</li><li>리치 텍스트 편집기에서는 이제 중첩 HTML 5 요소를 지원합니다.<br>HTML 5 사양에서는 중첩할 태그의 새 조합을 사용할 수 있습니다. 이전 버전의 리치 텍스트 편집기에서는 HTML 5 사양에서 허용되는 태그 중첩을 지원하지 않았습니다. 그 결과 VEC에서 선택한 중첩된 요소가 제대로 처리되지 않아 원하지 않는 HTML로 변경되었습니다. (TGT -33618)<br>자세한 내용은 Visual Experience [Composer 옵션에서 텍스트/HTML](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#edit-text-html) *편집을 참조하십시오*.</li> |

### 개선 사항, 수정 및 변경 사항

* VEC를 사용하여 자산을 삭제할 때 워크플로를 개선했습니다. 삭제된 자산은 [!UICONTROL 이제 오퍼 라이브러리] 및 ( [!DNL Scene7] 해당하는 경우) 에서 제거됩니다. 삭제된 자산은 더 이상 검색 결과에 표시되지 않습니다. (TGT-31981)
* 이제 이미지가 포함되어 있는 경우 (비어 있지 않은 폴더) 에셋 폴더를 삭제할 수 있습니다. (TGT-33265)

   이전에는 타겟 이미지 오퍼 라이브러리에서 비어 있지 않은 폴더를 삭제할 수 없었습니다 ([!UICONTROL 오퍼] &gt; [!UICONTROL 이미지 오퍼]). «폴더가 비어 있지 않음» 이 표시됩니다. UI에서 폴더를 삭제하려고 할 때 알림이 표시됩니다. 이 기능을 사용하면 폴더 삭제를 수행하여 내부의 에셋 및 하위 폴더가 수에 관계없이 포함된 전체 폴더를 제거할 수 있습니다. 이 기능은 Adobe Experience Cloud Assets UI 뿐만 아니라 Target UI 에서도 사용할 수 있습니다.

   * 이미지 오퍼 라이브러리의 비어 있지 않은 폴더는 삭제할 수 있습니다. 폴더 내의 모든 이미지가 활동에서 참조되지 않으면 전체 폴더 및 해당 컨텐츠가 삭제됩니다. 폴더 내의 일부 이미지가 모든 활동에서 참조되는 경우 참조되지 않은 모든 이미지가 삭제되지만 해당 이미지가 들어 있는 참조된 이미지와 폴더는 그대로 유지됩니다.
   * 이미지 에셋 피커에서 이미지 오퍼 렌더링이 보다 빠르고 효율적으로 이루어집니다.
   자세한 내용은 라이브러리에서 컨텐츠 [작업을](/help/c-experiences/c-manage-content/assets-working.md)참조하십시오. (TGT-32897)

* 자산 선택기에서 이미지 제공 렌더링을 개선했습니다. 이제 이미지 표시 및 선택이 더 빠르고 효율적입니다. (TGT-32897)
* VEC 내에서 페이지 로드를 취소할 때 URL에 대한 리디렉션 처리를 개선했습니다. (TGT-33815)
* 컬렉션 선택기에서 [!UICONTROL Recommendations] 컬렉션을 선택한 후 [!UICONTROL 저장] 단추를 클릭해야 합니다. 이 워크플로우는 다른 워크플로우와 동일합니다 [!DNL Target]. (TGT-33205)
* 일부 인사이트 보고서가 실제 전환율 대신 0%의 전환율을 반환하는 문제를 해결했습니다. (TNT-32125)

## [!DNL Target] Standard/Premium 19.4.1 (2019 년 4 월 15 일) {#release-19-4-1}

이 릴리스는 유지보수 릴리스이며, 다음 변경 사항을 포함합니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

* 브랜딩 및 제품 변경 사항을 반영하도록 [!DNL Adobe Experience Cloud] UI를 업데이트했습니다. (TGT-33546, TGT-33272 및 TGT-33331)

## 문서 변경, 이전 릴리스 노트 및 Experience Cloud 릴리스 노트 {#section_1BC5F5208DA548E9B4344A0836E4B943}

각 릴리스에 대한 노트 이외에 다음 리소스에서 추가 정보를 제공합니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 노트에 포함되지 않았을 수 있는 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경을](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)참조하십시오. |
| 이전 릴리스에 대한 릴리스 노트 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하세요.<br>자세한 내용은 이전 릴리스에 대한 [릴리스 노트를 참조하십시오](../r-release-notes/release-notes-for-previous-releases.md). |
| Adobe Experience Cloud 릴리스 노트 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 노트를 표시합니다.<br>자세한 내용은 [Experience Cloud 릴리스 노트를](https://marketing.adobe.com/resources/help/en_US/whatsnew/)참조하십시오. |

## 사전 릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 목록 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선 순위 제품 업데이트에 등록하십시오.<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| 향후 릴리스 노트 | 사전 릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 노트 - 사전 릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |