---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 25b448ad99618dca8b5aa4b698976a3d9aa76dec
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 14%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트 날짜: 2025년 2월 7일 토요일**

>[!NOTE]
>
>릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 일자에 따라 동일하거나 다를 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

## Target Standard/Premium 25.2.1 (2025년 2월 11일 수요일)

이번 릴리스에는 다음 업데이트가 포함됩니다.

* [!UICONTROL Activities] 사용자 인터페이스 업데이트
* [!DNL Recommendations] 사용자 인터페이스 업데이트

### [!UICONTROL Activities] 사용자 인터페이스 업데이트

[!DNL Adobe Target] UI 현대화 작업이 계속됨에 따라 업데이트된 [!UICONTROL Activities] 사용자 인터페이스의 일반 가용성을 알려드립니다.

>[!NOTE]
>
>2월 11일부터 고객은 점진적으로 새로운 [!UICONTROL Activities] UI에 액세스할 수 있습니다. 모든 고객을 위한 원활한 롤아웃을 보장하기 위해 이 릴리스는 제어된 단계로 배포됩니다. 첫 번째 단계에서는 [!DNL Target] 고객의 초기 그룹을 새 [!UICONTROL Activities] UI로 업그레이드합니다. 이후 단계에서는 나머지 고객을 업그레이드합니다.

최신 [!DNL Adobe Spectrum] 디자인 시스템을 기반으로 업데이트는 다음과 같은 새로운 개선 사항을 추가하면서 이전에 일관되지 않은 디자인 패턴을 표준화합니다.

* 활동 결과에 대한 더 나은 통찰력을 위해 [다시 디자인된 보고](/help/main/administrating-target/reporting.md)
* [!UICONTROL Audit] 페이지가 업데이트되어 [!DNL Audit API]에서 실시간 인사이트에 대한 정보를 가져옵니다.
* 서로 다른 팀 요구 사항에 대해 보다 유연하게 사용할 수 있도록 [사용자 지정 가능한 목록 보기](/help/main/c-activities/activities.md)
* 보다 쉽게 정보에 액세스할 수 있도록 [빠른 정보 및 세부 정보 화면 향상](/help/main/c-activities/activities.md)
* [세션 영구 검색 및 필터 옵션](/help/main/c-activities/activities.md)
* 브라우저 공급자의 최신 보안 업데이트 및 최신 사용자 인터페이스를 지원하여 [다시 빌드된 [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md)
* 보안을 강화하고 자사 쿠키에 대한 지원을 개선하기 위해 매니페스트 V3을 지원하는 [업데이트 [!DNL Chrome] 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)

![활동 새로 고침](/help/main/r-release-notes/assets/activities-refresh.png)

### [!DNL Recommendations] 사용자 인터페이스 업데이트

[!DNL Adobe Target] UI 현대화 작업이 계속됨에 따라 업데이트된 [!DNL Recommendations] 사용자 인터페이스의 일반 가용성을 알려드립니다.

>[!NOTE]
>
>2월 11일부터 고객은 점진적으로 새로운 [!UICONTROL Recommendations] UI에 액세스할 수 있습니다. 모든 고객을 위한 원활한 롤아웃을 보장하기 위해 이 릴리스는 제어된 단계로 배포됩니다. 첫 번째 단계에서는 [!DNL Target] 고객의 초기 그룹을 새 [!UICONTROL Activities] UI로 업그레이드합니다. 이후 단계에서는 나머지 고객을 업그레이드합니다.

최신 [!DNL Adobe Spectrum] 디자인 시스템을 기반으로 업데이트는 다음과 같은 새로운 개선 사항을 추가하면서 이전에 일관되지 않은 디자인 패턴을 표준화합니다.

* 이제 [제품 카탈로그 검색](/help/main/c-recommendations/c-products/catalog-search.md)에 제품의 실시간 동기화를 허용하는 업데이트된 데이터베이스가 제공됩니다
* API를 통해 만든 [!UICONTROL Recommendations]개 개체([!UICONTROL Criteria], [!UICONTROL Designs], [!UICONTROL Collections] 및 [!UICONTROL Exclusions]) [를 이제 UI에서 사용할 수 있습니다](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md)
* [Recommendations 설정](/help/main/administrating-target/recommendations-settings.md)이 [!UICONTROL Administration] 섹션 아래에 통합되었습니다.
* 다양한 팀 요구 사항에 대해 보다 나은 유연성을 위해 사용자 정의 가능한 목록 보기
* [구문 강조 표시 및 줄 번호 매기기](/help/main/c-experiences/c-manage-content/create-json-offer.md)로 HTML 및 JSON 코드 편집기를 새로 고쳤습니다.
* 정보에 쉽게 액세스할 수 있도록 빠른 정보 및 세부 정보 화면 개선
* 세션 영구 검색 및 필터 옵션

![Recommendations UI 새로 고침](/help/main/r-release-notes/assets/recs-ui-refresh.png)

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

자세한 내용은 이 섹션의 [오퍼](/help/main/c-experiences/c-manage-content/manage-content.md) 및 하위 문서를 참조하십시오.

다음은 이 릴리스의 변경 사항을 강조 표시하는 짧은 비디오입니다.

![오퍼 UI 비디오 새로 고침](/help/main/r-release-notes/assets/offers-video-v2.gif)

## [!DNL Adobe Experience Platform Web SDK] `__view__` 범위 최적화(2024년 10월 22일)

2024년 7월 22일부터 2024년 8월 15일 사이에 [!DNL Target] 팀은 `__view__` 범위를 최적화하여 활동 노출, 방문 및 방문자 보고의 정확도를 개선했습니다. 이 최적화는 자동 렌더링된 제안에 대한 보고 데이터를 자동으로 캡처하는 것을 목표로 하며 대부분의 계정에 투명해야 합니다.

모든 새 [!DNL Adobe Experience Platform Web SDK] 고객은 이 최적화를 사용할 수 있습니다. 그러나 at.js에서 마이그레이션하고 아래의 구현 단계를 따르지 않은 고객은 최적화를 사용할 수 없습니다. 이러한 고객은 2025년 2월 3일까지 구현을 검토해야 합니다. 이 날짜 이후, 모든 고객을 위해 최적화를 활성화합니다. 그때까지 구현을 검토하고 조정하지 않으면 아래 언급된 대로 보고서에 영향을 줄 수 있습니다. 구현이 영향을 받는지 확인하거나 구현을 조정하는 데 더 많은 시간이 필요한 경우 [!DNL Adobe Customer Care]에 문의하십시오.

>[!IMPORTANT]
>
>구현 검토를 완료하고 2025년 2월 3일까지 문제를 해결할 수 없는 경우 6개월 1회 연장을 요청할 수 있습니다. 2025년 1월 31일까지 요청이 제출되었는지 확인합니다. Adobe이 요청을 검토하고 결정합니다.

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

질문이 있는 경우 [고객 지원 Adobe](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오. (KB-2179)

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 정보: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=ko) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 정보](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
