---
keywords: qa;qa 모드; 활동 qa;qa url;qa url;미리 보기 url;미리 보기 url
description: Adobe 사용 방법 알아보기 [!DNL Target] 절대 변경되지 않는 미리보기 링크를 통한 간편한 엔드 투 엔드 활동 QA, 선택적 대상 타기팅, 라이브 활동 데이터에서 세그멘테이션된 상태를 유지하는 QA 보고를 수행하는 QA URL입니다.
title: 활동을 QA하려면 어떻게 합니까?
feature: Activities
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: 7c15a0795e94b6c6317cb5b4018899be71f03a40
workflow-type: tm+mt
source-wordcount: '1886'
ht-degree: 37%

---

# 활동 QA

에서 QA URL 사용 [!DNL Adobe Target] 변경되지 않는 미리 보기 링크, 선택적 대상 타깃팅 및 라이브 활동 데이터에서 세그먼트화된 QA 보고를 사용하여 간편한 엔드 투 엔드 활동 QA를 수행할 수 있습니다.

[!UICONTROL 활동 QA] 을(를) 완전히 테스트할 수 있습니다 [!DNL Target] 활동을 라이브로 시작하기 전에 다음 [!UICONTROL 활동 QA] 기능에는 다음이 포함됩니다.

* 경험 또는 활동에 수행된 업데이트에 상관없이 변경되지 않고 재생성이 필요 없는, 팀 구성원과 공유하는 링크가 있습니다. 이 기능을 사용하면 전체 사용자 여정에서 활동을 완전히 테스트할 수 있습니다.
* 선택적으로 준수하는 대상 조건. 대상 조건을 충족하지 않고도 마케터가 타깃팅 기준을 테스트하거나 타깃팅 기준을 무시하여 경험의 모양을 QA할 수 있습니다.
* 지표가 예상대로 증가하고 있는지, 그리고 QA 보고서 데이터가 프로덕션 보고(비A4T 보고의 경우)와 별도로 유지되는지를 마케터가 확인할 수 있도록 QA 보고가 생성됩니다.
* 게재 기준(페이지/)을 충족하는 개별 또는 기타 라이브 활동으로 경험을 미리 볼 수 있는 기능[!DNL Target] request/audience).
* 전체 사용자 경험을 QA할 수 있습니다. QA 링크로 사이트에 한 번 액세스한 다음, 활동 QA 동안 전체 사이트를 탐색할 수 있습니다. 세션을 종료하거나 [QA Target 북마클릿](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) 억지로 빠져 나오다 [!UICONTROL 활동 QA]. 이 기능은 여러 웹 페이지에 걸친 활동이 있는 경우 유용합니다.

   >[!NOTE]
   >
   >이 기능은 버전 2가 있는 at.js 구현에 적용됩니다.*x* 나중에 at.js 1.*x* 이 기능은 방문자의 브라우저가 서드파티 쿠키를 차단하지 않는 경우에만 적용됩니다.

## QA URL 액세스 및 공유 {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. 활동에서 [!UICONTROL 개요] 페이지, 클릭 **[!UICONTROL 활동 QA]**.

   ![활동 QA 링크](assets/qa_link.png)

1. 다음 설정을 구성합니다.

   ![QA 링크 구성 옵션](assets/qa_link_config.png)

   * **[!UICONTROL 대상 규칙을 일치시켜 경험 보기]:** 때로 대상 일치가 작동하는지 확인해야 합니다. 다른 경우에는 활동의 모양과 느낌을 확인해야 합니다. 이 설정을 &quot;켬&quot; 위치로 전환할 경우, 테스터는 타깃팅 요구 사항을 충족해야 경험을 볼 수 있는 자격이 생깁니다. 경험 타깃팅(XT) 활동의 경우 하나의 활동 URL이 제공됩니다. 사용자에게 표시되는 경험은 타깃팅 규칙 중 하나에 대한 사용자 자격에 의해 결정됩니다.

      이 설정을 &quot;끔&quot; 위치로 전환할 경우, 링크를 클릭하면 자격 여부에 관계없이 경험이 표시됩니다. QA를 수행할 때, 대상 타깃팅을 따라야 되는지, 따르지 않아도 되는지 사이에 전환할 수 있습니다.

   * **다른 모든 활동에 대한 기본 컨텐츠 표시:** 이 선택 사항을 &quot;켜짐&quot; 위치로 전환하면 다른 모든 활동에 대해 기본 콘텐츠가 표시됩니다. 예를 들어 동일한 페이지에서 다른 모든 라이브 활동을 고려하지 않고 미리 보기를 개별적으로 표시합니다.[!DNL Target] 요청.

      이 설정을 &quot;끔&quot;으로 전환하는 경우, 다음을 고려하십시오.

      * 테스트하는 활동과 다른 라이브 활동 사이에 충돌이 있는 경우, [일반 우선순위 규칙](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F)이 적용됩니다. 충돌 때문에 QA하려는 활동을 볼 수 없을 수도 있습니다.
      * 표시된 활동에 대한 지표 증가가 QA 보고 환경에서만 발생합니다.

1. **[!UICONTROL 완료]**&#x200B;를 클릭하여 변경 내용을 저장합니다.
1. 테스트를 위해 조직의 구성원과 활동 링크 URL을 공유합니다.

   활동 링크는 만료되지 않으며, 다른 사람이 활동이나 경험을 변경하는 경우 링크를 다시 보낼 필요가 없습니다. 하지만 과 다른 대상을 적용하는 경우 [!UICONTROL 대상 라이브러리]를 사용하면 활동을 단순히 편집하지 않고 다시 공유해야 하는 새 링크가 생성됩니다.

   각 활동 여정 URL(경험 A, 경험 B 등의 경우)을 사용하면 해당 경험에서 사용자 링크를 시작할 수 있습니다. 경험에 대해 생성된 URL을 클릭한 다음 일반 사이트 탐색을 계속하여 여러 페이지에서 경험을 확인합니다(여러 페이지가 있는 경우). 경험이 여러 페이지(템플릿 테스트 또는 다중 페이지 테스트)에 걸쳐 있는 경우에도 경험당 하나의 URL만 생성됩니다. 

   다음과 같은 이유로 사이트를 탐색하여 다른 페이지를 볼 수 있습니다. [!UICONTROL 활동 QA] 모드는 고정적입니다. 이 상황은 버전 2의 at.js 구현에 적용됩니다.*x* 나중에 at.js 1.*x* 구현에서는 방문자의 브라우저가 서드파티 쿠키를 차단하지 않는 경우에만 이 상황이 참입니다.

1. 활동 링크 URL에서 생성된 보고서를 보려면 활동의 **[!UICONTROL 보고서]** 페이지를 클릭하고 **[!UICONTROL 설정]** 아이콘(  ![icon_gear 이미지](assets/icon_gear.png) )을 선택한 다음 를 선택합니다 **[!UICONTROL QA 모드 트래픽]** 다음에서 **[!UICONTROL 환경]** 드롭다운 목록입니다.

## 고려 사항 {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* 다음 [!UICONTROL 활동 QA] 에 링크가 표시됩니다. [!UICONTROL 개요] 을 제외한 모든 활동 유형의 페이지 [!UICONTROL Automated Personalization] (AP)

   >[!NOTE]
   >
   >[활동 QA](/help/main/c-activities/c-activity-qa/activity-qa.md) ap 활동의 경우 현재 베타 프로그램에서 일부 고객이 사용할 수 있습니다. 이 기능은 초기 테스트 단계 후에 모든 고객이 사용할 수 있습니다.

* [!UICONTROL 계정에 저장된 활동이 너무 많으면 저장된 활동에 대한 활동 QA 미리보기 링크가 로드되지 않을 수 있습니다. ] 미리 보기 링크를 다시 시도하면 작동합니다. 이 상황이 계속 발생하지 않도록 하려면 더 이상 적극적으로 사용되지 않는 저장된 활동을 보관하십시오.
* [!UICONTROL 활동 QA] URL은 활동이 있는 경우 사용할 수 있습니다. [보고 소스로서의 Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). 을 사용하여 QA를 수행하는 동안 생성된 히트 [!UICONTROL 활동 QA] 활동이 라이브로 전환된 후에도 활동 데이터가 흐르는 동일한 보고서 세트로 이동합니다.
* [!UICONTROL 활동 QA에서는 종료 일자가 지난 보관된 활동용 콘텐츠를 표시하지 않습니다. ] 종료된 활동을 비활성화하는 경우 다음에 대한 활동을 다시 저장해야 합니다. [!UICONTROL 활동 QA] 일 때문에.
* 활동 가져옴 [!DNL Target Standard/Premium] (출처: [!DNL Target Classic], 예를 들어 )는 QA URL을 지원하지 않습니다.
* 위치 [!UICONTROL 자동 할당] 및 [!UICONTROL Recommendations] 활동:에서 캡처한 방문의 영향을 받지 않습니다. [!UICONTROL 활동 QA].
* [!UICONTROL 활동 QA] 끈적끈적합니다. 에서 웹 사이트를 탐색한 후 [!UICONTROL 활동 QA], 사용자 [!DNL Target] 세션이 만료되거나 다음 권한이 있어야 합니다. [!DNL Target] 에서 해제 [!UICONTROL 활동 QA] 먼저 일반적인 방문자처럼 사이트를 볼 수 있습니다. 사용 [Target QA 북마클릿](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) 억지로 빠져 나오다 [!UICONTROL 활동 QA].

   값이 비어 있는 `at_preview_token` 매개 변수로 사이트의 페이지를 로드하여(예: `https://www.mysite.com/?at_preview_token=`) 수동으로 나올 수도 있습니다.

* 활동을 만드는 동안 &quot;URL은&quot;을 지정한 경우 [양식 기반 작성기의 개선 사항](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) 또는 [시각적 경험 작성기의 페이지 전달 옵션)](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81), QA URL이 작동하지 않는 이유는 [!UICONTROL 활동 QA] URL 매개 변수를 추가합니다. 이 문제를 해결하려면 QA URL을 클릭하여 사이트로 이동하고 추가된 매개 변수를 URL에서 제거한 다음, 새 URL을 로드하십시오.
* at.js 1이 있는 경우&#x200B;*x*, [!UICONTROL 활동 QA] safari 또는 타사 쿠키를 차단하는 다른 브라우저를 사용하는 경우에는 모드가 고정되지 않습니다. 이러한 경우 탐색하는 각 URL에 미리보기 매개 변수를 추가해야 합니다. 를 구현한 경우에도 마찬가지입니다 [CNAME](https://experienceleague.corp.adobe.com/docs/target-dev/developer/implementation/implement-cname-support-in-target.html){target=_blank}.
* 활동에서 여러 경험 대상을 사용하는 경우(예를 들어, 동일한 활동에 포함된 미국 및 영국 사이트), QA 링크가 4개의 조합(경험 A/미국 사이트, 경험 A/영국 사이트, 경험 B/미국 사이트, 경험 B/영국 사이트)에 대해 생성되지 않습니다. 두 개의 QA 링크(경험 A와 경험 B)만 생성되고, 사용자는 페이지를 보려면 적절한 대상에 대한 자격이 있어야 합니다. 영국 QA 사람은 미국 사이트를 볼 수 없습니다.
* 모든 `at_preview` 매개 변수와 값이 이미 URL로 인코딩되어 있습니다. 대부분의 경우 모든 것이 예상대로 작동합니다. 그러나 일부 고객은 쿼리 문자열 매개 변수를 다시 인코딩하려는 밸런서나 웹 서버를 로드해야 합니다.

   이러한 이중 인코딩으로 인해 [!DNL Target] 을(를) 디코딩하려고 합니다. `at_preview_token`, [!DNL Target] 올바른 토큰 값을 추출할 수 없어 미리 보기가 작동하지 않습니다.

   [!DNL Adobe] 는 IT 팀에 얘기해서 모든 미리보기 매개 변수가 허용 목록에추가된으로 제공되어 이러한 값이 어떤 식으로든 변환되지 않도록 할 것을 권장합니다.

   다음 표에는 도메인에서 허용 목록에추가된으로 사용할 수 있는 매개 변수가 나와 있습니다.

   | 매개 변수 | 유형 | 값 | 설명 |
   |--- |--- |--- |--- |
   | `at_preview_token` | 암호화된 문자열 | 필수, 기본값 없음 | QA 모드에서 실행할 수 있는 캠페인 ID 목록이 포함된 암호화된 엔티티입니다. |
   | `at_preview_index` | 문자열 | Empty | 매개 변수의 형식은 `<campaignIndex>` 또는 `<campaignIndex>_< experienceIndex>`<br>입니다.두 색인이 모두 1로 시작합니다. |
   | `at_preview_listed_activities_only` | 부울(true/false) | 기본값: false | &quot;true&quot;면 `at_preview_index` 매개 변수에 지정된 모든 캠페인이 처리됩니다.<br>&quot;false&quot;이면 페이지의 모든 캠페인이 미리 보기 토큰에 지정되지 않았더라도 처리됩니다. |
   | `at_preview_evaluate_as_true_audience_ids` | 문자열 | Empty | 대상 및 보고 수준에서 항상 (true)로 평가되어야 하는 segmentId-s의 밑줄로 구분된 (&quot;_&quot;) 목록은 의 범위에서 &quot;true&quot;로 평가됩니다. [!DNL Target] 요청. |
   | `_AT_Debug` | 문자열 | 창 또는 콘솔 | 콘솔 로깅 또는 새 창입니다. |
   | `adobe_mc_ref` |  |  | 기본 페이지의 참조 URL을 새 페이지에 전달합니다. `AppMeasurement.js` 버전 2.1 이상에서 사용하는 경우 [!DNL Adobe Analytics]는 이 매개 변수값을 새 페이지의 참조 URL로 사용합니다. |
   | `adobe_mc_sdid` |  |  | 를 전달합니다. [!DNL Supplemental Data Id] (SDID) 및 [!DNL Experience Cloud Org Id] 기본 페이지에서 새 페이지로 이동합니다. 이 ID 전달 허용 [!UICONTROL Target 분석] (A4T) 을 사용하여 [!DNL Target] 을(를) 사용하여 기본 페이지에서 요청 [!DNL Analytics] 새 페이지에 을 요청합니다. |

* 다음 [!UICONTROL Target QA 모드] UI는 다중 페이지 활동에서 경험의 첫 번째 URL만 표시합니다. 여정 테스트를 만들고 URL1에서 URL2로 이동한다고 가정합니다. 그러나 URL2로 이동하려는 경우 URL1에 대해 제공된 모든 URL 매개 변수를 복사하여 URL1에 표시된 대로 &quot;?&quot;를 지정한 후 URL2에 적용합니다.
* 계정에 저장된 활동이 너무 많으면 저장된 활동에 대한 활동 QA 미리보기 링크가 로드되지 않을 수 있습니다. 미리보기 링크를 다시 시도하십시오. 이 문제가 계속 발생하는 것을 방지하기 위해 더 이상 적극적으로 사용되지 않는 저장된 활동을 보관하십시오.

## Target JavaScript 라이브러리 [!UICONTROL QA 모드] 호환성 {#compatibility}

[!DNL Target] 는 다음 JavaScript 라이브러리를 지원합니다.

* [at.js 1.x](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html){target=_blank}
* [at.js 2.x](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html){target=_blank}
* [Adobe Experience Platform Web SDK](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}

다음 표에는 다양한 활동 유형이 나열되어 있으며, 활동 유형을 나타내는지 여부가 표시됩니다. [!UICONTROL 활동 QA] 모드는 각 라이브러리에 대해 지원됩니다.

| 활동 유형 | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL A/B 테스트] | 예 | 예 | 예 |
| [!UICONTROL 자동 할당] | 예 | 예 | 예 |
| [!UICONTROL 자동 타깃팅] | 아니오 | 아니오 | 아니오 |
| [!UICONTROL Automated Personalization] (AP) | 아니오 | 아니오 | 아니오 |
| [!UICONTROL 경험 타겟팅] (XT) | 예 | 예 | 예 |
| [!UICONTROL 다변량 테스트] (MVT) | 예 | 예 | 예 |
| [!UICONTROL Recommendations] | 예 | 예 | 예 |

>[!NOTE]
>
>[활동 QA](/help/main/c-activities/c-activity-qa/activity-qa.md) ap 활동의 경우 현재 베타 프로그램에서 일부 고객이 사용할 수 있습니다. 이 기능은 초기 테스트 단계 후에 모든 고객이 사용할 수 있습니다.

## 미리보기 URL {#preview}

모든 항목에 대해 경험 미리보기 URL을 생성할 수 있습니다. [!DNL Target] 활동 유형. 미리보기 URL을 사용하면 미리보기 및 QA 목적으로 활동이 라이브 상태가 되기 전에 사이트에서 직접 경험 콘텐츠를 볼 수 있습니다. 경험 미리보기 URL은 타깃팅을 우회하여 특정 경험을 강제로 볼 수 있습니다.

미리보기 URL이 [!UICONTROL Automated Personalization] (AP) 활동, 참조: [경험 미리보기 URL을 사용하여 Automated Personalization 활동 미리보기](/help/main/c-activities/t-automated-personalization/experience-preview.md).

미리보기 URL에 액세스하고 공유하려면 **[!UICONTROL 개요]** 페이지를 클릭하고 **[!UICONTROL 활동 QA]** 링크를 클릭합니다.

>[!NOTE]
>
>다음 [!UICONTROL 활동 QA] 링크 및 미리보기 URL은 를 제외한 모든 활동에 대해 동일합니다. [!DNL Target] AP 활동.

다음 표는 다양한 활동 유형을 나열하고 각 라이브러리 또는 API에 대해 미리보기 URL 기능이 지원되는지 여부를 나타냅니다.

| 활동 유형 | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL A/B 테스트] | 예 | 예 | 예 |
| [!UICONTROL 자동 할당] | 예 | 예 | 예 |
| [!UICONTROL 자동 타기팅] | 예 | 예 | 예 |
| [!UICONTROL Automated Personalization] (AP) | 예 | 예 | 예 |
| [!UICONTROL 경험 타겟팅] (XT) | 예 | 예 | 예 |
| [!UICONTROL 다변량 테스트] (MVT) | 예 | 예 | 예 |
| [!UICONTROL Recommendations] | 예 | 예 | 예 |

