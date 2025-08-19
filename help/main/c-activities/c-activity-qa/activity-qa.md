---
keywords: qa;qa 모드; 활동 qa;qa url;qa url;미리 보기 url;미리 보기 url
description: Adobe [!DNL Target] QA URL을 사용하여, 변경되지 않는 미리 보기 링크를 통한 간편한 엔드 투 엔드 활동 QA, 선택적 대상 타깃팅, 라이브 활동 데이터에서 세그멘테이션된 상태를 유지하는 QA 보고를 수행하는 방법에 대해 알아봅니다.
title: 활동을 QA하려면 어떻게 합니까?
feature: Activities
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: 99ea312405e397e97e64e32d2685e8a6966d8928
workflow-type: tm+mt
source-wordcount: '1658'
ht-degree: 28%

---

# 활동 QA

[!DNL Adobe Target]의 QA URL을 사용하여, 변경되지 않는 미리 보기 링크를 통한 간편한 엔드 투 엔드 활동 QA, 선택적 대상 타깃팅, 라이브 활동 데이터에서 세그먼트화된 QA 보고를 수행할 수 있습니다.

[!UICONTROL Activity QA]에서는 [!DNL Target] 활동을 라이브로 시작하기 전에 완전히 테스트할 수 있습니다. [!UICONTROL Activity QA] 기능에는 다음이 포함됩니다.

* 경험 또는 활동에 수행된 업데이트에 상관없이 변경되지 않고 재생성이 필요 없는, 팀 구성원과 공유하는 링크가 있습니다. 이 기능을 사용하면 전체 사용자 여정에서 활동을 완전히 테스트할 수 있습니다.
* 선택적으로 준수하는 대상자 조건. 대상자 조건을 충족하지 않고도 마케터가 타기팅 기준을 테스트하거나 타기팅 기준을 무시하여 경험의 모양을 QA할 수 있습니다.
* 지표가 예상대로 증가하고 있는지, 그리고 QA 보고서 데이터가 프로덕션 보고(비A4T 보고의 경우)와 별도로 유지되는지를 마케터가 확인할 수 있도록 QA 보고가 생성됩니다.
* 배달 기준(페이지/[!DNL Target] 요청/대상)을 충족하는 다른 라이브 활동과 별개로 경험을 미리 볼 수 있는 기능입니다.
* 전체 사용자 경험을 QA할 수 있습니다. QA 링크로 사이트에 한 번 액세스한 다음, 활동 QA 동안 전체 사이트를 탐색할 수 있습니다. 세션을 종료하거나 [QA 대상 북마클릿](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879)을 사용하여 [!UICONTROL Activity QA]에서 강제로 나올 때까지 활동 QA에 남아 있습니다. 이 기능은 여러 웹 페이지에 걸친 활동이 있는 경우 유용합니다.

  >[!NOTE]
  >
  >이 기능은 버전 2가 있는 at.js 구현에 적용됩니다.*x* 이상 at.js 1.*x* 구현, 이 기능은 방문자의 브라우저가 서드파티 쿠키를 차단하지 않는 경우에만 적용됩니다.

## QA URL 액세스 및 공유 {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. 활동의 [!UICONTROL Overview] 페이지에서 **[!UICONTROL Activity QA]**&#x200B;을(를) 클릭합니다.

1. 다음 설정을 구성합니다.

   * **[!UICONTROL Match audience rules to see experiences]:** 때로는 대상 일치가 작동하는지 확인해야 합니다. 다른 경우에는 활동의 모양과 느낌을 확인해야 합니다. 이 설정을 &quot;켬&quot; 위치로 전환할 경우, 테스터는 타깃팅 요구 사항을 충족해야 경험을 볼 수 있는 자격이 생깁니다. 경험 타깃팅(XT) 활동의 경우 하나의 활동 URL이 제공됩니다. 사용자에게 표시되는 경험은 타깃팅 규칙 중 하나에 대한 사용자 자격에 의해 결정됩니다.

     이 설정을 &quot;끔&quot; 위치로 전환할 경우, 링크를 클릭하면 자격 여부에 관계없이 경험이 표시됩니다. QA를 수행할 때, 대상 타깃팅을 따라야 되는지, 따르지 않아도 되는지 사이에 전환할 수 있습니다.

   * **다른 모든 활동에 대한 기본 콘텐츠 표시:** 이 옵션을 &quot;켜짐&quot; 위치로 전환하면 다른 모든 활동에 대해 기본 콘텐츠가 표시됩니다. 예를 들어 동일한 페이지/[!DNL Target] 요청에 있는 다른 모든 라이브 활동을 고려하지 않고 미리 보기가 별도로 표시됩니다.

     이 설정을 &quot;끔&quot;으로 전환하는 경우, 다음을 고려하십시오.

      * 테스트 중인 활동과 다른 라이브 활동 간에 충돌이 있으면 [일반 우선 순위 규칙](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F)이 적용됩니다. 충돌 때문에 QA하려는 활동을 볼 수 없을 수도 있습니다.
      * 표시된 활동에 대한 지표 증가가 QA 보고 환경에서만 발생합니다.

1. 변경 내용을 저장하려면 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.
1. 테스트를 위해 조직의 구성원과 활동 링크 URL을 공유합니다.

   활동 링크는 만료되지 않으며, 다른 사람이 활동이나 경험을 변경하는 경우 링크를 다시 보낼 필요가 없습니다. 그러나 단순히 활동을 편집하는 대신 [!UICONTROL Audience Library]과(와) 다른 대상을 적용하는 경우 다시 공유해야 하는 새 링크가 생성됩니다.

   각 활동 여정 URL(경험 A, 경험 B 등의 경우)을 사용하면 해당 경험에서 사용자 링크를 시작할 수 있습니다. 경험에 대해 생성된 URL을 클릭한 다음 일반 사이트 탐색을 계속하여 여러 페이지에서 경험을 확인합니다(여러 페이지가 있는 경우). 경험이 여러 페이지(템플릿 테스트 또는 다중 페이지 테스트)에 걸쳐 있는 경우에도 경험당 하나의 URL만 생성됩니다.

   [!UICONTROL Activity QA] 모드가 고정되어 있으므로 사이트를 탐색하여 다른 페이지를 볼 수 있습니다. 이 상황은 버전 2의 at.js 구현에 적용됩니다.*x* 이상 at.js 1.*x* 구현, 이 상황은 방문자의 브라우저가 서드파티 쿠키를 차단하지 않는 경우에만 적용됩니다.

1. 활동 링크 URL에서 생성된 보고서를 보려면 활동의 **[!UICONTROL Reports]** 페이지를 클릭하고 **[!UICONTROL Settings]** 아이콘(![icon_gear 이미지](assets/icon_gear.png))을 클릭한 다음, **[!UICONTROL QA Mode Traffic]** 드롭다운 목록에서 **[!UICONTROL Environment]**&#x200B;을(를) 선택하십시오.

## QA 모드에서 해제

[!UICONTROL Activity QA]이(가) 고정되었습니다. [!UICONTROL Activity QA]에서 웹 사이트를 탐색한 후 일반 방문자처럼 사이트를 볼 수 있으려면 먼저 [!DNL Target] 세션이 만료되거나 [!DNL Target]에서 [!UICONTROL Activity QA]을(를) 해제해야 합니다.

### at.js 2.*x*

사이트에 at.js 2.*x*&#x200B;을(를) 배포했습니다. [Target QA 북마클릿](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879)을(를) 사용하여 [!UICONTROL Activity QA]에서 나가세요. 다음 글머리 기호에 설명된 대로 빈 값으로 사이트의 페이지를 로드하면 at.js 2일 때 브라우저에서 QA 쿠키가 *제거되지*&#x200B;않습니다.*x*&#x200B;이(가) 배포됩니다.

### at.js 1.*x*

사이트에 at.js 1이 있는 경우.*x*&#x200B;이(가) 배포되었으며 [Target QA 북마클릿](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879)을(를) 사용하는 것 외에도 빈 값이 있는 `at_preview_token` 매개 변수로 사이트의 페이지를 로드하여 수동으로 나올 수도 있습니다. 예:

`https://www.mysite.com/?at_preview_token=`

### [!DNL Adobe Experience Platform Web SDK]

사이트에 [[!UICONTROL Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}이(가) 배포된 경우 값이 비어 있는 `at_qa_mode` 매개 변수로 사이트의 페이지를 로드하여 수동으로 나올 수 있습니다. 예:

`https://www.mysite.com/?at_qa_mode=`

## 고려 사항 {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* 이제 모든 [!DNL Target] 활동 유형에 활동 QA를 사용할 수 있으므로 &quot;경험 미리 보기 URL을 사용하여 Automated Personalization 활동 미리 보기&quot; 기능이 더 이상 필요하지 않습니다.
* 계정에 저장된 활동이 너무 많으면 저장된 활동에 대한 [!UICONTROL Activity QA] 미리 보기 링크가 로드되지 않을 수 있습니다. 미리 보기 링크를 다시 시도하면 작동합니다. 이 상황이 계속 발생하지 않도록 하려면 더 이상 적극적으로 사용되지 않는 저장된 활동을 보관하십시오.
* [!UICONTROL Activity QA] URL은 [Analytics를 보고 소스로](/help/main/c-integrating-target-with-mac/a4t/a4t.md)(A4T)하는 활동에서 사용할 수 있습니다. [!UICONTROL Activity QA]을(를) 사용하여 QA를 수행하는 동안 생성된 히트는 활동이 라이브로 전환된 후에도 활동의 데이터가 흐르는 동일한 보고서 세트로 이동합니다.
* [!UICONTROL Activity QA]은(는) 보관된 활동이나 종료 날짜가 지난 활동에 대한 콘텐츠를 표시하지 않습니다. 종료된 활동을 비활성화하는 경우 [!UICONTROL Activity QA]이(가) 작동하도록 활동을 다시 저장해야 합니다.
* [!DNL Target Standard/Premium]에서 [!DNL Target Classic]&#x200B;(으)로 가져온 활동은 QA URL을 지원하지 않습니다.
* [!UICONTROL Auto-Allocate] 및 [!UICONTROL Recommendations] 활동에서 모델은 [!UICONTROL Activity QA]에서 캡처된 방문의 영향을 받지 않습니다.
* 활동을 만드는 동안 &quot;URL은&quot;을 지정한 경우([양식 기반 작성기에서 개선](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) 또는 [시각적 경험 작성기에서 페이지 전달 옵션)](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81), [!UICONTROL Activity QA]이(가) URL 매개 변수를 추가하므로 QA URL이 작동하지 않습니다. 이 문제를 해결하려면 QA URL을 클릭하여 사이트로 이동하고 추가된 매개 변수를 URL에서 제거한 다음, 새 URL을 로드하십시오.
* at.js 1이 있는 경우Safari나 타사 쿠키를 차단하는 다른 브라우저를 사용하는 경우 *x*, [!UICONTROL Activity QA] 모드가 고정되지 않습니다. 이러한 경우 탐색하는 각 URL에 미리보기 매개 변수를 추가해야 합니다. [CNAME](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/implement-cname-support-in-target.html?lang=ko){target=_blank}을(를) 구현한 경우에도 마찬가지입니다.
* 활동에서 여러 경험 대상을 사용하는 경우(예를 들어, 동일한 활동에 포함된 미국 및 영국 사이트), QA 링크가 4개의 조합(경험 A/미국 사이트, 경험 A/영국 사이트, 경험 B/미국 사이트, 경험 B/영국 사이트)에 대해 생성되지 않습니다. 두 개의 QA 링크(경험 A와 경험 B)만 생성되고, 사용자는 페이지를 보려면 적절한 대상에 대한 자격이 있어야 합니다. 영국 QA 사람은 미국 사이트를 볼 수 없습니다.
* 모든 `at_preview` 매개 변수와 값이 이미 URL로 인코딩되어 있습니다. 대부분의 경우 모든 것이 예상대로 작동합니다. 그러나 일부 고객은 쿼리 문자열 매개 변수를 다시 인코딩하려는 밸런서나 웹 서버를 로드해야 합니다.

  이러한 이중 인코딩 때문에 [!DNL Target]에서 `at_preview_token`을(를) 디코딩하려 할 때 [!DNL Target]에서 올바른 토큰 값을 추출할 수 없으므로 미리 보기가 작동하지 않습니다.

  [!DNL Adobe]은(는) IT 팀에 얘기해서 모든 미리 보기 매개 변수가 허용 목록에추가된으로 설정되어 있는지 확인하여 이러한 값이 어떤 식으로든 변환되지 않도록 하는 것이 좋습니다.

  다음 표에는 도메인에서 허용 목록에추가된으로 사용할 수 있는 매개 변수가 나와 있습니다.

  | 매개 변수 | 유형 | 값 | 설명 |
  |--- |--- |--- |--- |
  | `at_preview_token` | 암호화된 문자열 | 필수, 기본값 없음 | QA 모드에서 실행할 수 있는 캠페인 ID 목록이 포함된 암호화된 엔티티입니다. |
  | `at_preview_index` | 문자열 | Empty | 매개 변수의 형식은 `<campaignIndex>` 또는 `<campaignIndex>_< experienceIndex>`<br>두 색인이 모두 1로 시작합니다. |
  | `at_preview_listed_activities_only` | 부울(true/false) | 기본값: false | &quot;true&quot;면 `at_preview_index` 매개 변수에 지정된 모든 캠페인이 처리됩니다.<br>&quot;false&quot;이면 페이지의 모든 캠페인이 미리 보기 토큰에 지정되지 않았더라도 처리됩니다. |
  | `at_preview_evaluate_as_true_audience_ids` | 문자열 | Empty | [!DNL Target] 요청 범위에서 항상(타깃팅 및 보고 수준에서) &quot;true&quot;로 평가되어야 하는 segmentId-s의 밑줄로 구분된(&quot;_&quot;) 목록입니다. |
  | `_AT_Debug` | 문자열 | 창 또는 콘솔 | 콘솔 로깅 또는 새 창입니다. |
  | `adobe_mc_ref` |  |  | 기본 페이지의 참조 URL을 새 페이지에 전달합니다. `AppMeasurement.js` 버전 2.1 이상에서 사용하는 경우 [!DNL Adobe Analytics]는 이 매개 변수값을 새 페이지의 참조 URL로 사용합니다. |
  | `adobe_mc_sdid` |  |  | [!DNL Supplemental Data Id]&#x200B;(SDID) 및 [!DNL Experience Cloud Org Id]을(를) 기본 페이지에서 새 페이지로 전달합니다. 이 ID를 전달하면 [!UICONTROL Analytics for Target]&#x200B;(A4T)이(가) 기본 페이지의 [!DNL Target] 요청을 새 페이지의 [!DNL Analytics] 요청과 함께 &quot;결합&quot;할 수 있습니다. |

* [!UICONTROL Target QA Mode] UI는 다중 페이지 활동에서 경험의 첫 번째 URL만 표시합니다. 여정 테스트를 만들고 URL1에서 URL2로 이동한다고 가정합니다. 그러나 URL2로 이동하려는 경우 URL1에 대해 제공된 모든 URL 매개 변수를 복사하여 URL1에 표시된 대로 &quot;?&quot;를 지정한 후 URL2에 적용합니다.
* 계정에 저장된 활동이 너무 많으면 저장된 활동에 대한 활동 QA 미리보기 링크가 로드되지 않을 수 있습니다. 미리보기 링크를 다시 시도하십시오. 이 문제가 계속 발생하지 않도록 하기 위해 더 이상 적극적으로 사용되지 않는 저장된 활동을 보관하십시오.

## Target JavaScript 라이브러리 [!UICONTROL QA Mode] 호환성 {#compatibility}

[!DNL Target]은(는) 다음 JavaScript 라이브러리를 지원합니다.

* [at.js 1.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html?lang=ko)
* [at.js 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html?lang=ko)
* [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html)

다음 표는 다양한 활동 유형을 나열하고 각 라이브러리에 대해 [!UICONTROL Activity QA] 모드가 지원되는지 여부를 나타냅니다.

| 활동 유형 | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL A/B Test] | 예 | 예 | 예 |
| [!UICONTROL Auto-Allocate] | 예 | 예 | 예 |
| [!UICONTROL Auto-Target] | 예 | 예 | 예 |
| [!UICONTROL Automated Personalization]&#x200B;(AP) | 예 | 예 | 예 |
| [!UICONTROL Experience Targeting]&#x200B;(XT) | 예 | 예 | 예 |
| [!UICONTROL Multivariate Test]&#x200B;(MVT) | 예 | 예 | 예 |
| [!UICONTROL Recommendations] | 예 | 예 | 예 |