---
keywords: 릴리스 노트;새로운 기능;릴리스;업데이트;업데이트;릴리스;향상;향상;수정;버그 수정;업데이트,현재 업데이트
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
landing-page-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
short-description: ' [!DNL Adobe Target]의 현재 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 사항에 대해 알아봅니다.'
title: 현재 릴리스에는 무엇이 포함됩니까?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: b68c3d2e7e884e176a61598d1ab4a423aa1c9088
workflow-type: tm+mt
source-wordcount: '1520'
ht-degree: 20%

---

# [!DNL Target] 릴리스 정보 (현재)

이들 릴리스 정보는 [!DNL Adobe Target Standard] 및 [!DNL Target Premium] 릴리스 각각에 대한 기능, 개선 사항 및 수정 사항에 대한 정보를 제공합니다. 뿐만 아니라 해당되는 경우 [!DNL Target] API, SDK, [!DNL Adobe Experience Platform Web SDK], at.js 및 기타 플랫폼 변경 내용에 대한 릴리스 정보도 포함됩니다.

(괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.)

## [!DNL Target Standard/Premium] 25.2.3(2025년 2월 26일)

이번 릴리스에는 다음 업데이트가 포함됩니다.

* 일부 활동에 대해 활동 업데이트 후 [!DNL Target] 25.2.1 릴리스를 업데이트하지 못하는 문제를 해결했습니다. (TGT-51781)
* 활동 만들기 프로세스를 취소([!UICONTROL Add Audience] 대신 [!UICONTROL Cancel] 선택)할 때 모든 상태 대상 변경 내용이 제거되던 문제를 해결했습니다. (TGT-51769 및 TGT-51770)
* 특히 사용자 지정 코드를 사용할 때 일부 활동에 대해 [!UICONTROL Visual Experience Composer]&#x200B;(VEC)을(를) 로드하지 못하던 문제를 해결했습니다.  문제로 인해 VEC에 빈 화면이 표시되거나 [!DNL Target] UI가 이전 버전으로 되돌아갔습니다. (TGT-51758)
* 대상에 대한 페이지 전달을 편집한 후 수정 사항이 삭제되는 문제를 해결했습니다. (TGT-51756)
* [!UICONTROL Goals & Settings] 페이지에서 지표 유형을 변경할 때 모든 비지표 대상(페이지 및 경험 대상)이 활동에서 제거되던 문제를 해결했습니다. (TGT-51753)
* 활동을 편집하는 동안 [!UICONTROL Cancel]을(를) 클릭하면 Target UI가 [!UICONTROL Activity Details] 페이지 대신 [!UICONTROL Activities List] 페이지로 이동하는 문제가 해결되었습니다. (TGT-51731)
* 고객이 [!UICONTROL Export Reports to CSV] 옵션을 통해 보고서를 다운로드할 수 없는 문제를 해결했습니다. (TGT-51708)
* [!DNL Target Standard] 고객이 [!DNL Target Premium] 기능인 [!UICONTROL Properties]을(를) 사용하는 것으로 잘못 표시되는 양식 기반 경험 작성기의 문제를 해결했습니다. (TGT-51678)
* 새 오퍼를 만들 때 [!DNL Adobe Experience Platform] 특성이 표시되지 않도록 차단하는 문제를 해결했습니다. (TGT-51665)
* [!DNL Recommendations] 인벤토리에 대한 모든 활성 필터를 빠른 검색으로 이동하여 UI를 [!UICONTROL Filter] 레일이 아닌 [!UICONTROL Catalog Search]과(와) 맞췄습니다. (TGT-50723)

## at.js 버전 2.11.7(2025년 2월 26일)

이번 릴리스에는 다음 업데이트가 포함됩니다.

* `localStorage`을(를) 사용할 수 없을 때 원격 분석 로깅을 수정했습니다. 원격 분석으로 인해 일부 고객의 브라우저에서 `localStorage`을(를) 사용하지 않도록 설정한 문제가 발생했습니다.

## Target Standard/Premium 25.2.1 (2025년 2월 17일 화요일)

이번 릴리스에는 다음 업데이트가 포함됩니다.

* [!UICONTROL Activities] 사용자 인터페이스 업데이트
* [!DNL Recommendations] 사용자 인터페이스 업데이트

### [!UICONTROL Activities] 사용자 인터페이스 업데이트

[!DNL Adobe Target] UI 현대화 작업이 계속됨에 따라 업데이트된 [!UICONTROL Activities] 사용자 인터페이스의 일반 가용성을 알려드립니다.

>[!NOTE]
>
>2월 17일부터 고객은 점진적으로 새로운 [!UICONTROL Activities] UI에 액세스할 수 있습니다. 모든 고객을 위한 원활한 롤아웃을 보장하기 위해 이 릴리스는 제어된 단계로 배포됩니다. 첫 번째 단계에서는 [!DNL Target] 고객의 초기 그룹을 새 [!UICONTROL Activities] UI로 업그레이드합니다. 이후 단계에서는 나머지 고객을 업그레이드합니다.

최신 [!DNL Adobe Spectrum] 디자인 시스템을 기반으로 업데이트는 다음과 같은 새로운 개선 사항을 추가하면서 이전에 일관되지 않은 디자인 패턴을 표준화합니다.

* 활동 결과에 대한 더 나은 통찰력을 위해 [다시 디자인된 보고](/help/main/administrating-target/reporting.md).
* [[!UICONTROL Updated Change Log]](/help/main/c-activities/change-log.md) 페이지, 이제 실시간 인사이트를 위해 [[!DNL Audit Query API]](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/audit-api/overview){target=_blank}에서 정보를 가져옵니다.
* 서로 다른 팀 요구 사항에 대해 보다 유연하게 작업하도록 [사용자 지정 가능한 목록 보기](/help/main/c-activities/activities.md)입니다.
* 보다 쉽게 정보에 액세스할 수 있도록 [빠른 정보 및 세부 정보 화면을 개선했습니다](/help/main/c-activities/activities.md).
* [세션 영구 검색 및 필터 옵션](/help/main/c-activities/activities.md).
* 브라우저 공급자의 최신 보안 업데이트 및 최신 사용자 인터페이스를 지원하여 [다시 빌드된 [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md)입니다.

  업데이트된 VEC가 이전 버전과 어떻게 다른지에 대한 자세한 내용은 다음을 참조하십시오.

   * [시각적 경험 작성기 변경 사항](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md)
   * [시각적 경험 작성기 옵션](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

* 보안을 강화하고 자사 쿠키에 대한 지원을 개선하기 위해 매니페스트 V3을 지원하는 [업데이트됨 [!DNL Chrome] 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md).

![활동 새로 고침](/help/main/r-release-notes/assets/activities-refresh.png)

### [!DNL Recommendations] 사용자 인터페이스 업데이트

[!DNL Adobe Target] UI 현대화 작업이 계속됨에 따라 업데이트된 [!DNL Recommendations] 사용자 인터페이스의 일반 가용성을 알려드립니다.

>[!NOTE]
>
>2월 17일부터 고객은 점진적으로 새로운 [!UICONTROL Recommendations] UI에 액세스할 수 있습니다. 모든 고객을 위한 원활한 롤아웃을 보장하기 위해 이 릴리스는 제어된 단계로 배포됩니다. 첫 번째 단계에서는 [!DNL Target] 고객의 초기 그룹을 새 [!UICONTROL Activities] UI로 업그레이드합니다. 이후 단계에서는 나머지 고객을 업그레이드합니다.

최신 [!DNL Adobe Spectrum] 디자인 시스템을 기반으로 업데이트는 다음과 같은 새로운 개선 사항을 추가하면서 이전에 일관되지 않은 디자인 패턴을 표준화합니다.

* 이제 [제품 카탈로그 검색](/help/main/c-recommendations/c-products/catalog-search.md)에 제품의 실시간 동기화를 허용하는 업데이트된 데이터베이스가 있습니다.
* API를 통해 만든 [!UICONTROL Recommendations]개 개체([!UICONTROL Criteria], [!UICONTROL Designs], [!UICONTROL Collections] 및 [!UICONTROL Exclusions]) [를 이제 UI에서 사용할 수 있습니다](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md).
* [권장 사항 설정](/help/main/administrating-target/recommendations-settings.md)이(가) [!UICONTROL Administration] 섹션 아래에 통합되었습니다.
* 다양한 팀 요구 사항에 대해 더 나은 유연성을 위해 사용자 정의 가능한 목록 보기.
* [구문 강조 표시 및 줄 번호 매기기](/help/main/c-experiences/c-manage-content/create-json-offer.md)로 HTML 및 JSON 코드 편집기를 새로 고쳤습니다.
* 빠른 정보 및 세부 정보 화면을 개선하여 정보에 보다 쉽게 액세스할 수 있습니다.
* 세션 영구 검색 및 필터 옵션.

![권장 사항 UI 새로 고침](/help/main/r-release-notes/assets/recs-ui-refresh.png)

## Target Standard/Premium 25.1.1(2025년 1월 9일)

이번 릴리스에는 다음 업데이트가 포함됩니다.

### [!UICONTROL Offers Library] 사용자 인터페이스 업데이트

[!DNL Adobe Target] 사용자의 사용자 환경을 개선하기 위해 이 릴리스는 [!UICONTROL Offers Library] 사용자 인터페이스를 업데이트합니다.

>[!NOTE]
>
>모든 고객을 위한 원활한 롤아웃을 보장하기 위해 이 릴리스는 제어된 단계로 배포됩니다. 첫 번째 단계에서 Target 고객의 초기 그룹이 새 오퍼 UI로 업그레이드되었습니다. 이후 단계에서는 나머지 고객을 업그레이드합니다.

이 업데이트는 최신 [!DNL Adobe Spectrum] 디자인 시스템을 사용하여 일관되지 않은 디자인 패턴을 표준화하고 다음과 같은 새로운 개선 사항을 도입했습니다.

* **일괄 오퍼 관리**: 여러 오퍼를 동시에 선택하고 삭제하거나 이동합니다.

* **[!UICONTROL Code Editor]업그레이드**: 구문 강조 표시 및 줄 번호를 사용하여 HTML 및 JSON 편집기를 새로 고쳤습니다.

* **향상된 오퍼 카드**: 더 쉬운 정보 액세스를 위해 빠른 정보 및 세부 정보 카드를 개선했습니다.

* **영구 검색 및 필터**: 세션 영구 검색 및 필터 옵션을 추가합니다.

자세한 내용은 이 섹션의 [오퍼](/help/main/c-experiences/c-manage-content/manage-content.md) 및 하위 문서를 참조하십시오. 이 UI 변경 사항을 반영하도록 이 섹션의 모든 오퍼 문서가 업데이트되었습니다.

다음은 이 릴리스의 변경 사항을 강조 표시하는 짧은 비디오입니다.

![오퍼 UI 비디오 새로 고침](/help/main/r-release-notes/assets/offers-video-v2.gif)

## [!DNL Adobe Experience Platform Web SDK] `__view__` 범위 최적화(2024년 10월 22일)

2024년 7월 22일부터 2024년 8월 15일 사이에 [!DNL Target] 팀은 `__view__` 범위를 최적화하여 활동 노출, 방문 및 방문자 보고의 정확도를 개선했습니다. 이 최적화는 자동 렌더링된 제안에 대한 보고 데이터를 자동으로 캡처하는 것을 목표로 하며 대부분의 계정에 투명해야 합니다.

모든 새 [!DNL Adobe Experience Platform Web SDK] 고객은 이 최적화를 사용할 수 있습니다. 그러나 at.js에서 마이그레이션하고 아래의 구현 단계를 따르지 않은 고객은 최적화를 사용할 수 없습니다. 이러한 고객은 2025년 2월 3일까지 구현을 검토해야 합니다. 이 날짜 이후, 모든 고객을 위해 최적화를 활성화합니다. 그때까지 구현을 검토하고 조정하지 않으면 아래 언급된 대로 보고서에 영향을 줄 수 있습니다. 구현이 영향을 받는지 확인하거나 구현을 조정하는 데 더 많은 시간이 필요한 경우 [!DNL Adobe Customer Care]에 문의하십시오.

>[!IMPORTANT]
>
>구현 검토를 완료하고 2025년 2월 3일까지 문제를 해결할 수 없는 경우 6개월 1회 연장을 요청할 수 있습니다. 2025년 1월 31일까지 요청이 제출되었는지 확인합니다. Adobe에서 요청을 검토하고 결정합니다.

수동 제안 렌더링의 경우 이 최적화를 활용하려면 [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank}을(를) 검토하여 경험을 수동으로 렌더링한 후 또는 경험을 렌더링하기 위해 `applyPropositions` 메서드(또는 해당 [!DNL Launch] 작업을 도우미로 사용)를 사용할 때 알림을 보내고 있는지 확인하십시오.

경험을 수동으로 렌더링할 때 가장 일반적인 시나리오는 다음과 같습니다.

* JSON 오퍼 사용
* [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md)에서 만든 활동에서 사용자 지정 결정 범위 사용
* 전역 `__view__` 범위를 사용하는 [!UICONTROL Form-Based Experience Composer]을(를) 사용하여 만든 활동을 가져올 때 `renderDecisions: true`을(를) 사용하지 않음

알림이 *데이터 수집* 가이드의 [개인화된 콘텐츠 렌더링](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/personalization/rendering-personalization-content){target=_blank}에 설명된 대로 구현되지 않으면 보고 데이터가 [!DNL Target] 및 [Analytics for Target 보고](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)에서 누락될 수 있습니다. 특정 시나리오에서는 보고 데이터가 캡처되지 않기 때문에 잘못된 트래픽 분할을 볼 수 있습니다. 또는 다른 시나리오에서 동일한 이벤트를 반복적으로 보고합니다.

구현에 따라 [!DNL Analytics] 및 A4T 보고 영향을 확인하십시오.

[!DNL Platform Web SDK]은(는) 경험과 개인화를 렌더링하기 위해 두 가지 구현 형식을 지원합니다.

* **개인화 및 측정을 위한 단일 호출입니다.**

  처음 권장되는 경우 [!DNL Platform Web SDK]에 대한 단일 호출 접근 방식은 분할 호출 접근 방식을 위해 더 이상 사용되지 않도록 예약되어 있습니다. Adobe은 모든 새로운 구현에 새로운 분할 호출 접근 방식을 사용하도록 권장하며 기존 고객도 분할 호출 방법으로 전환할 것을 권장합니다.

  단일 호출 접근 방식을 계속 사용하면 [!DNL Analytics] 보고서에서 다음과 같은 예기치 않은 변경 사항을 확인할 수 있습니다.

   * 한 방울도 튀었다.
   * A4T와 [!UICONTROL Page View] 히트가 함께 결합되지 않으므로 [!DNL Analytics] eVar 및 이벤트를 사용하여 A4T 보고서의 특정 분류 및 상관 관계를 수행하기 어렵습니다.

* **분할 호출(페이지 이벤트의 상단 및 하단이라고도 함)을 사용합니다.**

  이 구현 유형은 [!DNL Adobe]에서 권장하는 새로운 [분할 호출 구현 접근 방식](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events){target=_blank}입니다. 이 방법을 사용하면 새 최적화는 [!DNL Analytics] 또는 A4T 보고서에 영향을 주지 않습니다.

질문이 있는 경우 [Adobe 고객 지원 센터](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오. (KB-2179)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 정보](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

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
