---
description: 이러한 릴리스 노트는 최신 또는 예정된 타겟 릴리스의 기능, 향상된 기능, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
keywords: 릴리스 노트
seo-description: 이러한 릴리스 노트는 최신 또는 예정된 Adobe Target 릴리스의 기능, 향상된 기능, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다
seo-title: Target 릴리스 노트(사전 릴리스)
solution: Target
title: Target 릴리스 노트(사전 릴리스)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: fe022b641580e33afdac446f71cec85fd232b275

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이러한 릴리스 노트는 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 향상된 기능 및 수정 사항에 대한 정보를 제공합니다.

**최종 업데이트일: 2019 년 5 월 28 일**

>[!NOTE]
>
>이러한 릴리스 노트에는 사전 릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 변경될 수 있습니다. 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트를 참조하십시오](release-notes.md). 이러한 페이지에 대한 정보는 동일하거나 다를 수 있습니다.

## at. js 버전 2.1.0 (2019 년 6 월 3 일)

이제. js 2.1.0에서 다음과 같은 흥미로운 기능을 알려드립니다.

| 기능/향상 | 설명 |
| --- | --- |
| Adobe 옵트인 지원 | Adobe 옵트인(Opt-in)은 동의 관리 플랫폼과 Adobe 솔루션과의 통합을 간소화하는 방법입니다.<br>Adobe 옵트인에 대한 자세한 내용은 [개인 정보 보호 및 개인 정보 보호 규정 (GDPR) 를 참조하십시오](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md). |
| 업계 표준의 CSP 규격 | at. js는 더 이상 eval () 를 사용하여 JavaScript를 실행하지 않습니다. |
| 클라이언트측 분석 로깅 | 고객이 클라이언트측 또는 서버측에서 Adobe Analytics로 분석 데이터를 어떻게 전송할지 완전히 제어할 수 있습니다. |
| 알림 보내기 | 개발자가 또는 사용 경험이 아닌 코드로 렌더링될 때 알림을 전송할 `applyOffer()` 수 있습니다 `applyOffers()`. |
| 파일 크기 감소 | at. js의 크기는 ~ 24% 줄어듭니다. 파일 크기가 작을수록 페이지 로드 성능이 향상되고 페이지의 at. js 다운로드 시간도 줄어듭니다. |

## [!DNL Target] Standard/Premium 19.5.1 (2019 년 5 월 21 일) {#release-19-5-1-prerelease}

이 릴리스에는 다음과 같은 기능, 변경 사항 및 개선 사항이 포함되었습니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

### 기능 업데이트

| 기능/향상 | 설명 |
| --- | --- |
| 단일 페이지 앱 시각적 경험 작성기 (SPA VEC) | SPA VEC에는 작업을 보다 빠르고 효율적으로 수행할 수 있도록 다음과 같은 개선 사항이 포함되어 있습니다.<ul><li>SPA에서 작업을 클릭하면 사이트에서 이 작업이 적용될 요소를 강조 표시합니다. A view 아래에 만들어진 각 vec 작업에는 4 개의 해당 아이콘이 있습니다. 정보, 편집, 이동 및 삭제. 이 릴리스의 새로운 &quot;이동&quot; 기능을 사용하면 작업을 페이지 로드 이벤트나 수정 패널에 이미 존재하는 다른 보기로 이동할 수 있습니다. (TGT-33746)</li><li>페이지가 VEC에 로드되기 전에 또는 페이지가 완전히 로드되지 않은 경우에도 여러 작업을 수행할 수 있습니다(예: 사용자 지정 코드가 더 이상 작동하지 않음). 사이트가 로드되기 전에 편집할 수 없는 작업은 Target UI에서 비활성화됩니다. (TGT-33851 및 TGT-34149)</li></ul>자세한 내용은 [SPA(단일 페이지 앱) 시각적 경험 작성기](/help/c-experiences/spa-visual-experience-composer.md)를 참조하십시오. |

### 개선 사항, 수정 및 변경 사항

* VEC 내에서 페이지 로드를 취소하면 도구 모음 아이콘이 적절하게 표시됩니다. 페이지가 완전히 로드될 때까지 특정 작업을 수행할 수 없는 경우 연관된 도구 모음 아이콘이 비활성화됩니다. (TGT-33811)

## Mobile App Visual Experience Composer (2019 년 5 월 14 일) {mobile-vec-may 14}

| 기능/향상 | 설명 |
| --- | --- |
| Mobile App Visual Experience Composer (VEC) | 모바일 앱 VEC를 사용하면 지속적인 개발 종속성 및 앱 릴리스 주기를 사용하지 않고도 고유한 방식으로 기본 모바일 앱에서 콘텐츠를 맞춤화하고 콘텐츠를 개인화할 수 있습니다.<br>자세한 내용은 다음 문서를 참조하십시오.<ul><li>[모바일 앱 시각적 경험 작성기](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android - 모바일 앱 설정](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS - 모바일 앱 설정](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[모바일 VEC에서 클릭 추적 설정](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li><li>[비디오: 모바일 앱 Visual Experience Composer](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#video)</li></ul> |

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선 순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
