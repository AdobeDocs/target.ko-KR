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
source-git-commit: 542366ce4c14eab4ee15e3614888f4b335b9a0df

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다.

## 공지

다음 중요 알림을 확인하십시오.

* 2019 년 2 월 20 일, EMEA, 일본 및 APAC 지역에서 Adobe Target 인프라가 더 이상 TLS 1.1 이상을 지원하지 않는 이전 장치나 웹 브라우저에서 최종 사용자의 데이터를 수집하지 않도록 업그레이드되었습니다. 동일한 업그레이드가 2019 년 4 월 1 일에 **북미 지역에 대해서도 예정되어**있습니다. TLS 1.2로 마이그레이션하면 보안이 강화됩니다. 세부 사항을 검토하고 IT 팀에 변경 사항을 계획하여 원활한 전환을 수행해야 합니다. 자세한 내용은 [TLS (Transport Layer Security) 암호화 변경을 참조하십시오](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).
* [!DNL Target]과 [!DNL Adobe Marketing Cloud]는 2019년 3월부터 Microsoft Internet Explorer 11에 대한 지원을 중단할 예정입니다. 이 변경 사항은 [!DNL Target] 작성에만 영향을 주며, 경험 전달에는 영향을 주지 않습니다. Microsoft Edge나 다른 브라우저로 전환하십시오. 자세한 내용은 [지원되는 브라우저](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md)를 참조하십시오.

## [!DNL Target] Standard/Premium 19.5.1 (2019 년 5 월 21 일) {#tgt-19-5-1}

이 릴리스에는 다음과 같은 기능, 변경 사항 및 개선 사항이 포함되었습니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

### 기능 업데이트

| 기능/향상 | 설명 |
| --- | --- |
| 단일 페이지 앱 시각적 경험 작성기 (SPA VEC) | SPA VEC에는 작업을 보다 빠르고 효율적으로 수행할 수 있도록 다음과 같은 개선 사항이 포함되어 있습니다.<ul><li>SPA에서 작업을 클릭하면 사이트에서 이 작업이 적용될 요소를 강조 표시합니다. A view 아래에 만들어진 각 vec 작업에는 4 개의 해당 아이콘이 있습니다. 정보, 편집, 이동 및 삭제. 이 릴리스의 새로운 &quot;이동&quot; 기능을 사용하면 작업을 페이지 로드 이벤트나 수정 패널에 이미 존재하는 다른 보기로 이동할 수 있습니다. (TGT-33746)</li><li>페이지가 VEC에 로드되기 전에 또는 페이지가 완전히 로드되지 않은 경우에도 여러 작업을 수행할 수 있습니다(예: 사용자 지정 코드가 더 이상 작동하지 않음). 사이트가 로드되기 전에 편집할 수 없는 작업은 Target UI에서 비활성화됩니다. (TGT-33851 및 TGT-34149)</li></ul>자세한 내용은 [SPA(단일 페이지 앱) 시각적 경험 작성기](/help/c-experiences/spa-visual-experience-composer.md)를 참조하십시오. |

### 개선 사항, 수정 및 변경 사항

* VEC 내에서 페이지 로드를 취소하면 도구 모음 아이콘이 적절하게 표시됩니다. 페이지가 완전히 로드될 때까지 특정 작업을 수행할 수 없는 경우 연관된 도구 모음 아이콘이 비활성화됩니다. (TGT-33811)

## Mobile App Visual Experience Composer (2019 년 5 월 14 일) {mobile-vec}

| 기능/향상 | 설명 |
| --- | --- |
| Mobile App Visual Experience Composer (VEC) | 모바일 앱 VEC를 사용하면 지속적인 개발 종속성 및 앱 릴리스 주기를 사용하지 않고도 고유한 방식으로 기본 모바일 앱에서 콘텐츠를 맞춤화하고 콘텐츠를 개인화할 수 있습니다.<br>자세한 내용은 다음 문서를 참조하십시오.<ul><li>[모바일 앱 시각적 경험 작성기](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android - 모바일 앱 설정](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS - 모바일 앱 설정](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[모바일 VEC에서 클릭 추적 설정](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li><li>[비디오: 모바일 앱 Visual Experience Composer](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#video)</li></ul> |

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