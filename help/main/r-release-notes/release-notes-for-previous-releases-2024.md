---
keywords: 릴리스 노트;프리릴리스 노트;향후 개선 사항;향후 수정 사항;향후 기능;예정된 릴리스
description: Adobe Target의 이전 릴리스에 포함된 기능, 개선 사항 및 수정 사항 목록을 봅니다.
title: 이전 릴리스에는 어떤 기능이 포함됩니까?
feature: Release Notes
source-git-commit: 53cd01d2406b8a2f8560fe380ebb5044872e6711
workflow-type: tm+mt
source-wordcount: '1232'
ht-degree: 15%
---
# 이전 릴리스에 대한 릴리스 정보

[!DNL Target Standard/Premium], [!DNL Target] 플랫폼 및 [!DNL Target] JavaScript 라이브러리(at.js)에 대한 릴리스 정보를 포함하는 이전 [!DNL Adobe Target] 릴리스에 대한 릴리스 정보입니다.

릴리스 노트는 릴리스 월 및 연도별로 내림차순으로 나열됩니다.

>[!NOTE]
>
>현재 월의 Target 릴리스(플랫폼 및 Target Standard/Premium)에 대한 정보는 [Target 릴리스 정보 (현재)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A)를 참조하십시오.

## 릴리스 정보 - 2024

### [!DNL Adobe Experience Platform Web SDK] `__view__` 범위 최적화(2024년 10월 22일)

2024년 7월 22일부터 2024년 8월 15일 사이에 [!DNL Target] 팀은 `__view__` 범위를 최적화하여 활동 노출, 방문 및 방문자 보고의 정확도를 개선했습니다. 이 최적화는 자동 렌더링된 제안에 대한 보고 데이터를 자동으로 캡처하는 것을 목표로 하며 대부분의 계정에 투명해야 합니다.

모든 새 [!DNL Adobe Experience Platform Web SDK] 고객은 이 최적화를 사용할 수 있습니다. 그러나 at.js에서 마이그레이션하고 아래의 구현 단계를 따르지 않은 고객은 최적화를 사용할 수 없습니다. 이러한 고객은 2025년 2월 3일까지 구현을 검토해야 합니다. 이 날짜 이후, 모든 고객을 위해 최적화를 활성화합니다. 그때까지 구현을 검토하고 조정하지 않으면 아래 언급된 대로 보고서에 영향을 줄 수 있습니다. 구현이 영향을 받는지 확인하거나 구현을 조정하는 데 더 많은 시간이 필요한 경우 [!DNL Adobe Customer Care]에 문의하십시오.

>[!IMPORTANT]
>
>구현 검토를 완료하고 2025년 2월 3일까지 문제를 해결할 수 없는 경우 6개월 1회 연장을 요청할 수 있습니다. 2025년 1월 31일까지 요청이 제출되었는지 확인합니다. Adobe에서 요청을 검토하고 결정합니다.

수동 제안 렌더링의 경우 이 최적화를 활용하려면 [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep/aep-web-sdk-overview){target=_blank}을(를) 검토하여 경험을 수동으로 렌더링한 후 또는 `applyPropositions` 메서드(또는 해당 [!DNL Launch] 작업을 도우미로 사용)를 사용하여 경험을 렌더링할 때 알림을 보내고 있는지 확인하십시오.

경험을 수동으로 렌더링할 때 가장 일반적인 시나리오는 다음과 같습니다.

* JSON 오퍼 사용
* [[!UICONTROL 양식 기반 경험 작성기]](/help/main/c-experiences/form-experience-composer.md)에서 만든 활동에서 사용자 지정 결정 범위 사용
* 전역 `__view__` 범위를 사용하는 [!UICONTROL 양식 기반 경험 작성기]를 사용하여 만든 활동을 가져올 때 `renderDecisions: true`을(를) 사용하지 않음

알림이 *데이터 수집* 가이드의 [개인화된 콘텐츠 렌더링](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/personalization/rendering-personalization-content){target=_blank}에 설명된 대로 구현되지 않으면 보고 데이터가 [!DNL Target] 및 [Analytics for Target 보고](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)에서 누락될 수 있습니다. 특정 시나리오에서는 보고 데이터가 캡처되지 않기 때문에 잘못된 트래픽 분할을 볼 수 있습니다. 또는 다른 시나리오에서 동일한 이벤트를 반복적으로 보고합니다.

구현에 따라 [!DNL Analytics] 및 A4T 보고 영향을 확인하십시오.

[!DNL Platform Web SDK]은(는) 경험과 개인화를 렌더링하기 위해 두 가지 구현 형식을 지원합니다.

* **개인화 및 측정을 위한 단일 호출입니다.**

  처음 권장되는 경우 [!DNL Platform Web SDK]에 대한 단일 호출 접근 방식은 분할 호출 접근 방식을 위해 더 이상 사용되지 않도록 예약되어 있습니다. Adobe은 모든 새로운 구현에 새로운 분할 호출 접근 방식을 사용하도록 권장하며 기존 고객도 분할 호출 방법으로 전환할 것을 권장합니다.

  단일 호출 접근 방식을 계속 사용하면 [!DNL Analytics] 보고서에서 다음과 같은 예기치 않은 변경 사항을 확인할 수 있습니다.

  * 한 방울도 튀었다.
  * A4T와 [!UICONTROL 페이지 보기] 히트가 함께 결합되지 않으므로 [!DNL Analytics] eVar 및 이벤트를 사용하여 A4T 보고서의 특정 분류 및 상관 관계를 수행하기 어렵습니다.

* **분할 호출(페이지 이벤트의 상단 및 하단이라고도 함)을 사용합니다.**

  이 구현 유형은 [!DNL Adobe]이(가) 권장하는 새로운 [분할 호출 구현 접근 방식](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events){target=_blank}입니다. 이 방법을 사용하면 새 최적화는 [!DNL Analytics] 또는 A4T 보고서에 영향을 주지 않습니다.

질문이 있는 경우 [Adobe 고객 지원 센터](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C)에 문의하십시오. (KB-2179)

### at.js 버전 2.11.6(2024년 9월 29일)

* [!UICONTROL VEC(시각적 경험 작성기]) 또는 [!UICONTROL 양식 기반 경험 작성기]에서 리디렉션 오퍼를 사용하여 [!DNL Target]이(가) 올바르게 작동하지 않는 문제를 해결했습니다.

at.js 릴리스에 대한 자세한 내용은 *Adobe Target 개발자 안내서*&#x200B;의 [at.js 버전 세부 사항](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank}을 참조하십시오.

### [!DNL Adobe Customer Journey Analytics]의 [!DNL Target] 보고(2024년 5월 8일)

[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank}과(와) [!DNL Target] 간의 통합은 최적화 프로그램에 강력한 분석과 시간 절약에 유용한 도구를 제공합니다.

[!DNL Customer Journey Analytics]를 [!DNL Target]에 대한 보고 소스로 사용하는 경우의 주요 이점은 다음과 같습니다.

* 마케터가 언제든지 [!DNL Customer Journey Analytics] 성공 지표 또는 보고 세그먼트를 [!DNL Target] 활동 보고서에 동적으로 적용할 수 있습니다. 활동을 실행하기 전에 모든 항목을 지정할 필요는 없습니다.
* 마케터는 [실험 패널](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}과 같은 [!DNL Customer Journey Analytics] 기능을 사용하여 웹 사이트 개인화를 추가로 분석할 수 있습니다.

자세한 내용은 [Adobe Customer Journey Analytics의 Target 보고](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md)를 참조하십시오.

### [!UICONTROL 시각적 경험 작성기] Helper 확장 프로그램(2024년 4월 23일)

매니페스트 V2를 사용하여 레거시 [!DNL Target] 시각적 경험 작성기 Helper 확장이 만들어졌습니다. [!DNL Google]이(가) 2024년 6월부터 Manifest V2를 사용하여 만든 확장을 더 이상 허용하지 않는다고 발표했습니다. 자세한 내용은 [[!UICONTROL 시각적 경험 작성기] Helper 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)을 참조하십시오.

[!DNL Adobe]에서는 가능한 한 빨리 고객이 최신 [Visual Editing Helper 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)(으)로 이동할 것을 권장합니다.

### [!UICONTROL 브라우저] 대상 특성의 `Browser:iPad` 및 `Browser:iPhone` 업데이트(2024년 4월 30일)

| 업데이트 | 세부 사항 |
|--- |--- |
| 대상을 만들 때 사용되는 [브라우저 특성](/help/main/c-target/c-audiences/c-target-rules/browser.md)에서 [!UICONTROL 브라우저:iPad] 및 [!UICONTROL 브라우저:iPhone]이(가) 업데이트되었습니다. | [!DNL Adobe Target]을(를) 사용하면 페이지를 방문할 때 특정 [브라우저 또는 브라우저 옵션](/help/main/c-target/c-audiences/c-target-rules/browser.md)을 사용하는 방문자를 포함하여 [여러 범주 특성 중 하나를 타깃팅할 수 있습니다](/help/main/c-target/c-audiences/c-target-rules/target-rules.md).<P>[!DNL Target] Standard/Premium 24.3.1(2024년 3월 4~6일)부터 Target UI를 사용하여 만든 기본 제공 대상(예: `Browser:iPad` 및 `Browser:iPhone`)이 `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` 및 `profile.mobile.isTablet`을(를) 사용하여 [!DNL iPad] 및 [!DNL iPhone]에 대한 적절한 타깃팅을 수행하도록 업데이트됩니다.<P>이 업데이트에는 고객 측에서 작업을 수행할 필요가 없습니다.<p><B>중요</b>: 고객이 프로필 스크립트(및 JavaScript 세그먼트)에서 [!DNL iPad] 및 [!DNL iPhone]에 대한 적절한 타깃팅을 수행하려면 **2024년 4월 30일**&#x200B;까지 고객이 수동으로 변경해야 합니다. 수동으로 변경해야 하는 대체 설정의 예는 [!UICONTROL 브라우저]대상 특성](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates)에서 [및 [!DNL iPad] 및 [!DNL iPhone] 에 대한 업데이트를 참조하십시오. |

### [!UICONTROL Visual Editing Helper] 확장 기능(2024년 3월 14일)

이번 릴리스에는 [!DNL Google Chrome]의 [[!DNL Adobe Experience Cloud Editing Helper]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) 확장에 대한 다음과 같은 개선 사항 및 수정 사항이 포함되어 있습니다.

* 고객 웹 사이트에서 작성을 수행할 때 iFrame 로드 메커니즘을 개선했습니다.
* VEC([!UICONTROL 시각적 경험 작성기])에서 작성을 수행하는 동안 확장 프로그램이 쿠키를 복제하는 문제를 해결했습니다.

### [!DNL Target] Standard/Premium 24.3.1(2024년 3월 4~6일)

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 활동에서 고유 선택기의 수를 계산하는 논리를 수정했습니다. (TGT-47878)
* [!UICONTROL Analytics for Target]&#x200B;(A4T) 보고로 구성된 [!UICONTROL MVT(다변량]) 활동이 제대로 표시되지 않는 문제를 해결했습니다. (TGT-47490)
* 트래픽이 없는 경험을 제어 경험으로 사용할 때 보고에 표시되는 경고 메시지가 개선되었습니다. (TGT-47537)
* 많은 백엔드 및 현지화 수정 사항이 추가되었습니다.

### [!DNL Target] Standard/Premium 24.1.1 (2024년 1월 22일, 23일 및 25일)

이번 릴리스에는 다음과 같은 개선 및 수정 사항이 포함되어 있습니다.

* 매출 목표 지표가 있는 [!UICONTROL Analytics for Target]&#x200B;(A4T) 활동에서 &quot;매출&quot;이 열 이름으로 표시되지 않았고 매출 지표가 보고에 ($) 형식으로 표시되지 않았습니다. 이는 이미 해결된 표시용 문제였습니다. (TGT-46995)
* 보고 일자 간격이 올바르게 작동하지 않는 문제를 수정했습니다. (TGT-47396)
* 고객이 [!UICONTROL 추가 작업] 아이콘을 사용하여 활동을 활성화하거나 비활성화한 후 [!UICONTROL 모든 활동] 페이지에 잘못된 상태가 표시되는 문제를 해결했습니다. (TGT-47367)
* 단일 고객에 대해 [!UICONTROL 중요 특성] 보고서가 표시되지 않는 문제를 해결했습니다. (TGT-47272)
* 단일 고객이 “인증 요구”를 활성화하려고 하면 “잘못된 페이로드” 메시지가 표시되는 문제를 수정했습니다. (TGT-47195)
* [!DNL Target] UI에서 여러 현지화된 문자열을 업데이트했습니다.
