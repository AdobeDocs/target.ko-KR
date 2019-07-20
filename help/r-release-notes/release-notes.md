---
description: 이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
keywords: 릴리스 노트;사전 릴리스
seo-description: 이러한 릴리스 노트는 Adobe Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항, 수정 사항 및 알려진 문제에 대한 정보를 제공합니다.
seo-title: Adobe Target 릴리스 노트 (최신)
solution: Target
title: Target 릴리스 노트(현재)
topic: 권장 사항
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: ce1758df44740213a2d9011ee43f84cb52f6a29d

---


# Target 릴리스 노트(현재){#target-release-notes-current}

이러한 릴리스 노트는 Target Standard 및 Target Premium 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다.

## 공지

다음 중요 알림을 확인하십시오.

* 2019년 2월 20일, EMEA, 일본 및 APAC 지역에서 Adobe Target 인프라가 업그레이드되어 더 이상 TLS 1.1 이상을 지원하지 않는 이전 장치나 웹 브라우저를 사용자는 최종 사용자의 데이터를 수집하지 않습니다. 북미 지역에 대해서도 이러한 동일한 업그레이드가 **2019년 4월 1일**&#x200B;에 예정되어 있습니다. TLS 1.2로 마이그레이션하면 보안이 강화됩니다. 세부 사항을 살펴보고 원활한 전환을 위해 IT 팀과 변경을 계획하는 것이 중요합니다. 자세한 내용은 [TLS(전송 계층 보안) 암호화 변경 사항](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)을 참조하십시오.
* [!DNL Target]과 [!DNL Adobe Marketing Cloud]는 2019년 3월부터 Microsoft Internet Explorer 11에 대한 지원을 중단할 예정입니다. 이 변경 사항은 [!DNL Target] 작성에만 영향을 주며, 경험 전달에는 영향을 주지 않습니다. Microsoft Edge나 다른 브라우저로 전환하십시오. 자세한 내용은 [지원되는 브라우저](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md)를 참조하십시오.

## Target Standard/Premium 19.6.1(2019년 6월 26일)

이 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

(괄호로 묶인 문제 번호는 내부 Adobe용입니다.)

| 기능/향상 | 설명 |
| --- | --- |
| 시각적 경험 작성기(VEC) | **새 VEC 메뉴 옵션**: vec에서 페이지 요소를 클릭하면 메뉴에 해당 요소 유형에 사용할 수 있는 옵션이 표시됩니다.<ul><li>You can now use the [!UICONTROL Styles &gt; Background] option to change the background image and color for the selected element. (TGT-15001)</li></ul>See *Styles* in [Visual Experience Options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles).<br>**클릭 추적 개선**&#x200B;사항: VEC 및 SPA (Single Page Application) VEC 내에서 클릭 추적을 구성하는 과정을 개선했습니다.<ul><li>클릭 추적에서 사용할 요소를 선택할 때 사용 가능한 모든 요소의 이름이 오른쪽의 수정 패널에 표시되므로 원하는 요소를 빠르고 손쉽게 선택할 수 있습니다.</li><li>The [!UICONTROL Goals &amp; Settings] page of the three-part guided activity workflow displays a number representing the number of elements selected for click tracking. 이 숫자 위로 마우스를 가져가면 선택한 모든 요소의 이름이 표시됩니다. (TGT-33878)</li></ul>See [Click tracking](/help/c-activities/r-success-metrics/click-tracking.md). |
| SPA VEC(Single Page App Visual Experience Composer) | **가이드 워크플로우**: 새로운 안내 워크플로우는 단일 페이지 앱에 대해 활동을 실행하고 실행하는 페이지 배달 규칙 설정을 구성하는 방법을 이해하는 데 도움이 됩니다. (TGT-33718)<br> See [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md#page-delivery-settings).<br>**복제 수정**&#x200B;사항: 이제 SPA VEC를 사용하여 수정 사항을 정의한 다음 단일 페이지 앱에서 다른 보기에 사용하기 위해 해당 수정 내용을 복제할 수 있습니다. (TGT-33882)<br>See [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md). |
| 모바일 시각적 경험 작성기 | **다양한 앱 버전**: 이제 여러 버전의 모바일 앱용 활동을 제작할 수 있습니다. 따라서 버전이 유사하고 앱의 UI를 크게 변경할 필요가 없을 때 시간과 노력을 절약할 수 있습니다. (TGT-34231)<br>See "Manage multiple app versions" in [Mobile App Visual Experience Composer](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#using-the-mobile-vec). |
| ![프리미엄 배지](/help/assets/premium.png) 자동 개인화 (AP) 및 자동 타깃팅 | **제어 기능**: AP 또는 자동 타겟 활동을 만드는 동안 컨트롤로 사용할 경험을 선택할 수 있습니다. 이 기능을 사용하면 활동에 구성된 트래픽 할당 비율에 따라 전체 제어 트래픽을 특정 경험으로 라우팅할 수 있습니다. 그런 다음 해당 경험의 제어 트래픽에 대한 개인화된 트래픽의 성능 보고서를 평가할 수 있습니다. 현재 제어 옵션 (임의로 제공된 경험) 는 계속 사용할 수 있습니다. (TGT-32801, TGT-26572, &amp; TGT-26571)<br>See [Select the control for your Automated Personalization or Auto-Target Activity](/help/c-activities/t-automated-personalization/experience-as-control.md). Note that there is a [current known issue](/help/r-release-notes/known-issues-resolved-issues.md) with this feature.<br>**개인화 인사이트 보고서**: 방문자가 특정 위치에서 특정 컨텐츠를 볼 때 속성에 대한 마케터 친화적인 이름은 보다 의미 있는 정보를 제공합니다. (TGT-33421 &amp; TGT-34957)<br>See [Data collection for the Target personalization algorithms](/help/c-activities/t-automated-personalization/ap-data.md). |
| ![프리미엄 배지](/help/assets/premium.png) 추천 | 최근에 본 항목 로직을 생성하는 동안 이전에 구입한 추천 항목 전환을 사용할 수 있습니다. (TGT-34030)<br>자세한 내용은 "기준 만들기" 에서 [최근에 본 항목을](/help/c-recommendations/c-algorithms/create-new-algorithm.md#previously-purchased) 참조하십시오. |
| Google Chrome samesite 쿠키 정책 | 최근 Google는 2019 년 7 월 30 일 릴리스로 예정되어 있는 Chrome 76 부터 시작하여 웹 사이트에서 사용할 수 있는 쿠키와 사용자를 추적할 수 있는 쿠키가 명시적으로 지정되어야 한다고 발표했습니다.<br>소비자가 소비자를 위해 보다 안전한 웹을 만들기 위해 노력함에 따라 Target는 방문자의 개인 정보 보호 기대치를 충족시키는 동시에 개인화된 경험을 제공하기 위해 절대적으로 노력하고 있습니다.<br>[Google Chrome Samesite 쿠키 정책을 참조하십시오](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md). |

## at. js 버전 2.1.0 (2019 년 6 월 3 일)

이제. js 2.1.0에서 다음과 같은 흥미로운 기능을 알려드립니다.

| 기능/향상 | 설명 |
| --- | --- |
| Adobe 옵트인 지원 | Adobe 옵트인(Opt-in)은 동의 관리 플랫폼과 Adobe 솔루션과의 통합을 간소화하는 방법입니다.<br>Adobe 옵트인에 대한 자세한 내용은 [개인 정보 보호 및 개인 정보 보호 규정 (GDPR) 를 참조하십시오](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md). |
| 업계 표준의 CSP 규격 | at. js는 더 이상 eval () 를 사용하여 JavaScript를 실행하지 않습니다. |
| 클라이언트측 분석 로깅 | 고객이 클라이언트측 또는 서버측에서 Adobe Analytics로 분석 데이터를 어떻게 전송할지 완전히 제어할 수 있습니다.<br>자세한 내용은 구현하기 전에 [Client-Side Analytics 로그인을](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side) *참조하십시오*. |
| 알림 보내기 | Allows developers to send notifications when an experience is rendered by their code instead of using `applyOffer()` or `applyOffers()`.<br>자세한 내용은 [adobe. target. sendnotifications (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md)를 참조하십시오. |
| 파일 크기 감소 | at. js의 크기는 ~ 24% 줄어듭니다. 파일 크기가 작을수록 페이지 로드 성능이 향상되고 페이지의 at. js 다운로드 시간도 줄어듭니다. |
| . js 설명서 업데이트 | For a full list of all articles updated due to the at.js 2.1.0 release, see the June 3, 2019 entries in [Documentation changes](/help/r-release-notes/doc-change.md). |

## 설명서 변경 내용, 이전 릴리스 노트 및 Experience Cloud 릴리스 노트 {#section_1BC5F5208DA548E9B4344A0836E4B943}

각 릴리스에 대한 노트 이외에 다음 리소스에서 추가 정보를 제공합니다.

| 리소스 | 세부 사항 |
|--- |--- |
| 설명서 변경 내용 | 이 릴리스 노트에 포함되지 않았을 수 있는 이 안내서의 업데이트에 대한 자세한 정보를 제공합니다.<br>자세한 내용은 [설명서 변경 내용](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)을 참조하십시오. |
| 이전 릴리스에 대한 릴리스 노트 | 이전 릴리스의 Target Standard 및 Target Premium에서 새로운 기능 및 향상된 기능에 대한 정보를 확인하세요.<br>자세한 내용은 [이전 릴리스에 대한 릴리스 노트](../r-release-notes/release-notes-for-previous-releases.md)를 참조하십시오. |
| Adobe Experience Cloud 릴리스 노트 | Adobe Experience Cloud 솔루션에 대한 최신 릴리스 노트를 표시합니다.<br>자세한 내용은 [Experience Cloud 릴리스 노트를](https://marketing.adobe.com/resources/help/en_US/whatsnew/)참조하십시오. |

## 사전 릴리스 정보 {#section_5D588F0415A2435B851A4D0113ACA3A0}

아래 리소스를 통해 다음 Target 릴리스에 추가될 내용을 확인할 수 있습니다.

| 리소스 | 세부 사항 |
|--- |--- |
| Adobe 우선순위 제품 업데이트 목록 | Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트(<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html)에 등록하십시오. |
| 향후 릴리스 노트 | 사전 릴리스 정보를 포함하여 이번 달 Target 릴리스에 대한 자세한 내용은 [Target 릴리스 노트 - 사전 릴리스](/help/r-release-notes/target-release-notes.md) 페이지를 참조하십시오. |