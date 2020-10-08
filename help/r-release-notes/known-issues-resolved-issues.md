---
keywords: known issues;resolved issues;release notes;bugs;issues;fixes
description: 이 릴리스의 Adobe Target에 대한 알려진 문제 정보입니다. 또한 해결된 문제에 대한 정보도 포함되어 있습니다.
title: Adobe Target의 알려진 문제 및 해결된 문제
feature: known issues
uuid: f8e8e057-1842-4922-ab7f-4d5441048573
translation-type: tm+mt
source-git-commit: 2092247f235233d9628dc001a5e898df0aa9da8c
workflow-type: tm+mt
source-wordcount: '3793'
ht-degree: 80%

---


# 알려진 문제 및 해결된 문제{#known-issues-and-resolved-issues}

이 릴리스의 Target에 대한 알려진 문제 정보입니다. 또한 해결된 문제에 대한 정보도 포함되어 있습니다.

>[!NOTE]
>
>괄호로 묶인 문제 번호는 내부 Adobe용입니다.

## 알려진 문제 {#section_AEDC98B67CF24C9F8E0CF0D2EB9ACAEF}

다음 섹션에서는 [!DNL Target]에 대한 알려진 문제들을 나열합니다.

### 페이지 게재 {#page-delivery}

URL 포함 사항(/checkout, /cart)과 같은 템플릿 규칙을 [페이지 게재](/help/c-activities/t-experience-target/t-xt-create/xt-activity-url.md)에 추가하면 추가 공백이 규칙에 접두사로 추가됩니다. 이것은 사소한 문제이며 대상-정의 작성 및 오퍼 게재에 영향을 주지 않습니다. (TGT-35920)

### QA 미리 보기 링크

계정에 저장된 활동이 너무 많으면 저장된 활동에 대한 활동 QA 미리 보기 링크가 로드되지 않을 수 있습니다. 미리 보기 링크를 다시 시도하면 작동합니다. 이 문제가 계속 발생하지 않도록 하기 위해 더 이상 활발하게 사용되지 않는 저장된 활동을 보관합니다. (TNT-37294)

### Recommendations 활동에 대한 QA 모드

알려진 문제로 인해 활동에 사용된 기준이 항목 기반 또는 카테고리 기반 항목인지 미리 볼 수 없습니다. (TNT-37455)

### 리디렉션 오퍼 {#redirect}

다음은 리디렉션 오퍼에 대한 알려진 문제입니다.

* 경우에 따라 A4T(타겟 분석)로 구성된 활동에서 리디렉션 오퍼를 사용할 때 제한된 수의 고객이 트래픽 분포에서 높은 차이를 보고했습니다. Adobe 엔지니어가 현재 이 문제를 해결하기 위해 노력하고 있습니다.
* at.js 구현의 리디렉션 활동으로 인해 미리 보기 URL이 루프에 들어가게 됩니다(오퍼가 반복적으로 전달됨). 대신 [QA 모드](../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40)를 사용하여 미리 보기와 QA를 수행할 수 있습니다. 이 문제는 오퍼의 실제 전달에는 영향을 주지 않습니다. (TGT-23019)

### VEC 내에서 페이지 로드 취소 {#cancel}

* 리디렉션 URL이 포함된 VEC 내에서 [!UICONTROL A/B 테스트] 또는 XT([!UICONTROL Experience Targeting]) 활동 로드를 취소할 때 현재 알려진 다음 문제가 나타납니다.

   VEC 내의 3단계 안내식 워크플로우의 1단계에서 페이지 로드를 취소하면 VEC에 [!UICONTROL 수정 사항] 패널이 표시되고 URL로 리디렉션 템플릿이 경험에 적용됩니다(예: &quot;경험 B&quot;). 2단계 또는 3단계로 진행한 다음 다시 1단계로 이동하면 다음과 같은 상황이 발생합니다.

   &quot;경험 B&quot;에서 기본적으로 템플릿 로드를 취소한 웹 사이트가 렌더링되고 [!UICONTROL 수정 사항] 패널에 액세스할 수 있습니다. 이는 이 경험에서 URL 템플릿에 리디렉션이 적용되었기 때문에 문제가 되지 않습니다. URL로 리디렉션 템플릿이 표시됩니다.

   VEC에서 올바른 경험 상태를 표시하려면 다음을 수행하십시오.

   다른 경험으로 전환한 다음 다시 &quot;경험 B&quot;로 전환하는 경우 이 경험에 적용된 URL로 리디렉션 템플릿이 [!DNL Target]에 표시되고 [!UICONTROL 수정 사항] 패널에 액세스할 수 없습니다. (TGT-32138)

* SPA(단일 페이지 애플리케이션) 웹 사이트의 경우 로드를 취소하면 [!UICONTROL 수정 사항] 패널에서 작업을 편집할 수 없습니다.

### Recommendations

다음은 Recommendations 활동에 대한 알려진 문제입니다.

* 피드나 API를 통해 업데이트를 받지 못한 후 60일이 지나면 엔티티가 올바르게 만료됩니다. 그러나 만료된 엔티티는 만료 후 카탈로그 검색 색인에서 제거되지 않습니다. (IRI-857)
* 기준 및 디자인에 대한 &quot;사용 정보&quot; 오버레이는 A/B 및 Experience 타깃팅 활동의 사용을 반영하지 않습니다(TGT-34331).
* A/B 및 Experience 타깃팅 활동의 Recommendations 오퍼는 Recommendations 트레이의 시각적 미리 보기를 표시하지 않습니다(TGT-33426).
* API를 통해 생성된 컬렉션, 제외, 기준 및 디자인은 Target 사용자 인터페이스에 표시되지 않으며 API를 통해서만 편집할 수 있습니다. (TGT-35777)
* API를 통해 생성된 Recommendations 활동은 사용자 인터페이스에서 볼 수 있지만 API를 통해서만 편집할 수 있습니다.
* 기준 목록(카드) 보기에 표시된 사용자 지정 기준 피드 상태는 10분마다 새로 고침되며 특수한 상황에서 10분 이상 걸릴 수 있습니다. 사용자 지정 기준 편집 보기에 표시된 상태를 실시간으로 가져오며 상태는 항상 최신입니다. (TGT-35896, TGT-36173)

### MVT(다변량 테스트) 활동

MVT 활동에서 테이블 및 그래프에 표시되는 승자가 지표를 확인할 때 일관되지 않습니다. 사용자가 요약 보기에서 그래프 보기로 전환한 후 요약 보기로 다시 전환하고 지표를 변경한 후 그래프 보기로 다시 전환하면 이 문제가 발생합니다. 이 문제가 발생해도 요약 보기에는 항상 올바른 승자가 표시됩니다. 사용자가 요약 보기 중간에 그래프 보기로 절대 전환하지 않으면 그래프 보기에 올바른 승자가 표시됩니다.

### at.js {#atjs}

다음은 at.js의 알려진 문제입니다.

* Adobe Analytics 코드가 페이지 요소(예: 단추)에 없는 경우 2.2.0 이전 버전의 at.js를 사용하면 클릭 추적은 Analytics for Target(A4T)에서 전환을 보고하지 않습니다. at.js 2.2.0에서 이 문제에 대한 수정 사항이 도입되었습니다. 이 문제가 발생하는 경우 [최신 at.js 버전으로 업그레이드하십시오](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).
* at.js 2.1.1 이하 버전(예: 기본 경험)을 사용하여 수정 없이 경험을 생성하는 경우 보고서, Analytics for Target(A4T), Adobe Analytics 또는 Google Analytics에서 경험이 계산되지 않을 수 있습니다. 또한 [ttMeta 플러그인](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md)이 제대로 작동하지 않을 수 있습니다.

   해결 방법으로 경험 컨텐츠에 공백을 사용하십시오. (TNT-33366)

   >[!NOTE]
   >
   >이 문제에 대한 수정 사항이 at.js 2.2.0에 포함되어 있습니다. [최신 버전 또는 at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)로 업그레이드하거나 2.2.0 이하 버전의 at.js에 대해서만 위에 언급된 해결 방법을 사용해야 합니다.

* 페이지가 VEC(시각적 경험 작성기)에 로드되면 Target은 글로벌 mbox 설정이 활성화되었는지와, 사용자가 VEC에서 권장 사항을 적용하려고 하는 위치에 entityID 또는 categoryID가 있는지를 확인해야 합니다. 이 정보에 따라 기준 목록이 필터링됩니다. 기본 목록에는 필터링된 알고리즘이 있지만 [호환 확인란](/help/c-recommendations/t-create-recs-activity/algo-select-recs.md)을 사용하여 전체 알고리즘 목록을 볼 수 있습니다.

   at.js를 사용하는 경우 호환성 확인란이 숨겨지므로 호환되지 않는 알고리즘을 볼 수 없습니다.

   이 문제는 VEC를 사용하는 Recommendations 활동에만 적용됩니다.

   **해결 방법**: [!UICONTROL Recommendations > 설정]에서 [!UICONTROL 호환되지 않는 기준 필터링] 선택 사항을 비활성화합니다. 이 설정을 비활성화하면 모든 기준(호환 및 비호환)이 기준 선택기에 표시됩니다. (TGT-25949)

* at.js 버전 1.0으로 업그레이드한 후 at.js 및 Visitor API 2.2.0 간의 상호 작용으로 인해 Mbox가 Microsoft Explorer 11 브라우저에서 실행되지 않습니다. 이 문제는 at.js 버전 0.9.6 이상에 영향을 미칩니다. (TNT-27600)
* Cordova/Hybrid 앱에서는 퍼스트 파티 쿠키가 현재 지원되지 않으므로 이 앱에서 at.js가 작동하지 않을 수 있습니다. (TNT-26166)

   **해결 방법**: &quot;x-only&quot; 선택 사항을 활성화한 상태로 at.js를 구성한 후 호출에 `mboxThirdPartyId`를 전달하여 사용자를 관리합니다.

### 성공 지표

고급 옵션 &quot;카운트는 어떻게 증분됩니까?&quot;가 &quot;모든 노출&quot; 또는 &quot;모든 노출(새로 고침 제외)&quot;로 설정된 성공 지표는 다른 지표가 종속되는 성공 지표로 사용할 수 없습니다.

성공 지표가 노출 시마다 증분되도록 설정되면 Target에서는 방문자가 이 성공 지표를 방문할 때마다 방문자를 다시 카운트합니다. 그런 다음 Target은 성공 지표 &quot;멤버십&quot;을 0으로 재설정하여 다음 노출 시 다시 카운트될 수 있도록 합니다. 따라서 해당 지표를 먼저 확인해야 하는 다른 지표가 있다고 해도, Target은 사용자가 첫 번째 지표를 확인했다는 사실을 절대 인식하지 못합니다.

### Analytics for Target (A4T)

Analysis Workspace에서 Target 활동 노출 및 전환을 사용할 때 지표에 &quot;동일한 터치&quot; Attribution IQ 모델을 적용하여 정확한 카운트를 확인하십시오. 기본이 [아닌 속성 모델을](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/column-settings.html)적용하려면 지표를 마우스 오른쪽 단추로 클릭하여 열 설정 > 기본이 아닌 속성 모델 사용 **설정 > 동일한 터치 모델**&#x200B;선택 이 모델이 적용되지 않으면 지표가 부풀려집니다.

현재 모든 Analytics 패키지에는 Attribution IQ에 이 모델을 추가할 수 있습니다. Attribution IQ에 액세스할 수 없는 경우 보고 및 분석의 A4T 데이터를 사용하십시오.

### Target API

고객은 Adobe I/O에서 A/B 활동 API의 v3 버전을 통해 자동 할당 활동에 대한 CRUD 작업을 수행할 수 없습니다.

### GEO 타깃팅

2020년 5월 10일에 GEO 공급자 파일이 업데이트되었으며, 이러한 파일이 일치하지 않습니다. 예를 들어 쉼표를 포함하는 일부 값이 추가되었습니다.하지만 기존 대상의 값은 쉼표가 없습니다. 이 변경 사항으로 인해 모든 배달 서버가 영향을 받지 않았습니다. 따라서 이러한 값을 사용하는 대상이 2020년 5월 10일부터 7월 22일 사이에 올바른 방문자를 모두 적격한 것이 아닐 수 있습니다.

### &quot;처리&quot; 레이블을 표시하는 이미지 오퍼

오퍼 페이지의 이미지 오퍼에는 이미지가 업로드된 후 몇 시간 동안 &quot;처리&quot; 레이블이 유지되는 경우가 있습니다. 대부분의 경우 레이블에만 문제가 발생합니다.이미지 오퍼는 여전히 활동에 사용할 수 있으며 배달됩니다. 그러나 일부 경우에는 컨텐츠 바꾸기 > 이미지 작업에 이미지 오퍼를 사용할 수 없을 수도 있습니다. 이러한 경우 이미지 오퍼를 다시 업로드하고 몇 시간 후에 이미지 오퍼를 교체할 수 있는지 확인해야 합니다. (TGT-37458)

## 해결된 문제 {#section_FD2FC86E7C734D60B1EDC9DEF60E1014}

위의 알려진 문제가 해결되면 다음 섹션으로 이동되고, 필요한 경우 다른 메모가 더 추가됩니다.

### 자동 Target 보고 {#at-metrics}

9월 15일, 오후 2:30부터 [!DNL Adobe Target Premium] 사용자의 [!UICONTROL 자동 Target] 보고에 영향을 주는 문제가 해결되었습니다.(PDT) - 10월 6일 오전 9시 25분(PDT). 영향을 받은 전환 지표에 대한 보고서를 볼 때(&quot;페이지를[!UICONTROL 보았습니다]&quot; 또는 &quot;mbox에서[!UICONTROL 클릭함]&quot; 옵션을 사용하여 구성됨) 전환율이 잘못 보고됩니다. 현재 알려진 배달 문제가 없습니다.

보고서를 다시 동기화하고 수정하려면:

1. 영향을 받은 [!UICONTROL 자동 Target 활동을 복사하고] 저장합니다.
1. 새로 저장한 활동을 활성화합니다(영향을 받은 활동이 라이브된 경우).
1. 원본(영향을 받은) 활동을 삭제합니다.

(TGT-38522, CSO 20201006007)

### 보고 {#conversions-audiences}

현재 전환은 사용된 고객에 따라 다르게 증가합니다.

예를 들어 동일한 방문자의 경우 전환 카운트가 &quot;참가자당 한 번:&quot;을 증가하도록 설정된 경우

* 대상:방문 수준 전환에 대한 &quot;모든 적격한 방문자&quot;는 한 번만 증가합니다. 이는 예상 행동입니다.
* 대상:방문 수준 전환에 대한 &quot;새 방문자&quot;는 한 번만 증가시키지 않고 매번 잘못 증가합니다. 이는 예상 동작이 아닙니다.

전환 카운트가 &quot;모든 노출 시:&quot;로 증가하도록 설정된 경우

* 대상:방문자 수준 전환에 대한 &quot;모든 적격한 방문자&quot;는 매번 증가하지 않고 한 번만 잘못 증가시킵니다. 이는 예상 동작이 아닙니다.
* 대상:방문자 수준 전환을 위한 &quot;새 방문자&quot;가 매번 증가합니다. 이는 예상 행동입니다.

이 문제는 [!DNL Target] 보고에만 관련되어 있습니다. Target [!UICONTROL (A4T) 보고를 위해] Analytics를 사용할 때는 문제가 되지 않습니다.

이 문제가 해결되었습니다.

### Google Chrome 버전 80+를 사용할 때 VEC(Visual Experience Composer) 또는 EEC(Enhanced Experience Composer)에서 페이지가 로드되지 않음

이 알려진 문제는 Chrome 버전 80부터 시작되는 SameSite 특성 없이 쿠키의 기본 동작을 변경하는 Google의 결정과 관련이 있습니다. 크롬을 변경하기 전에 SameSite 특성이 &quot;SameSite=None&quot;으로 설정된 모든 쿠키의 기본값은 &quot;SameSite=Lax&quot;로 설정되었으며, 이렇게 하면 쿠키가 GET 및 POST 요청에 전송되는 방식이 변경됩니다. SameSite [Updates를 참조하십시오](https://www.chromium.org/updates/same-site).

자세한 내용 및 수정 사항은 &quot;최근에 발표된 Google Chrome SameSite 쿠키 실행 정책이 VEC 및 EEC에 어떤 영향을 줍니까?&quot;를 참조하십시오. in [Troubleshooting Issues Related to the Visual Experience Composer and Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

### 사용자 지정 경험을 제어로 사용할 때 자동 타겟 활동에 대한 그래프 보고서가 렌더링되지 않습니다.

경험에 데이터가 없는 경우(방문 횟수 0) 자동 타겟 활동에 대한 그래프 보고서가 &quot;차등&quot; 모드(평균 리프트 및 일별 리프트)에 대해 렌더링되지 않습니다. 이러한 상황은 제어 경험이 사용자 지정으로 설정된 경우 활동의 초기 단계에서 발생할 수 있습니다. 다른 모드(평균 제어 실행 및 타깃팅됨, 일별 제어 및 타깃팅됨, 방문 횟수)에서는 제대로 작동합니다. 데이터가 있으면(방문 횟수가 0이 아님) 바로 보고서가 예상대로 렌더링됩니다.

이 문제는 Target 19.7.1 릴리스에서 해결되었습니다.

### mbox.js

mbox.js 라이브러리는 Handlebars 및 Mustache와 같은 클라이언트 측 템플릿 언어를 지원하지 않습니다. at.js 라이브러리는 이러한 언어를 *지원합니다*.

**참고**: mbox.js 라이브러리는 더 이상 개발되지 않습니다. 모든 고객은 mbox.js에서 at.js로 마이그레이션해야 합니다. 자세한 내용은 [mbox.js에서 at.js로 마이그레이션](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)을 참조하십시오.

### 구현: 글로벌 Mbox를 자동으로 만들기

On the Implementation tab ([!UICONTROL Administration > Implementation]) the [!UICONTROL Global Mbox Auto Create] field will be &quot;false&quot; by default for a newly provisioned tenant.

프로비저닝 후 처음으로 mbox.js가 다운로드되면 다운로드된 mbox.js 파일 및 [!UICONTROL  백엔드에서 ]글로벌 Mbox를 자동으로 만들기[!DNL Target] 필드가 &quot;true&quot;로 설정되지만, UI의 [!UICONTROL 구현] 페이지에는 페이지를 새로 고칠 때까지 계속 &quot;false&quot;로 표시됩니다(페이지를 새로 고친 후 상태는 &quot;true&quot;로 표시됨).

at.js는 새로 제공된 임차인에 대해 `global_mbox_autocreate = false`로 다운로드됩니다. mbox.js를 처음 다운로드하면 global\_mbox\_autocreate가 &quot;true&quot;로 설정되고 at.js도 `global_mbox_autocreate = true`로 다운로드됩니다. (TGT-15929)

### Target API의 엔터프라이즈 권한 지원 {#api}

GET API를 사용하여 오퍼 목록을 가져오는 경우 오퍼 라이브러리의 Target UI에서 생성된 코드 오퍼가 기본 작업 공간에 표시될 수 있습니다. 이 문제는 2019년 3월 첫 주에 수정됩니다. 이 수정 사항이 적용되면 API에서 가져올 때 코드 오퍼가 적합한 작업 공간에 표시됩니다. 이 문제는 API에서 만든 오퍼에 영향을 주지 *않습니다*. 예를 들어 API에서 생성된 코드 오퍼는 GET API를 사용하여 가져오든 아니면 Target UI 내에서 가져오든 간에 생성될 때 작업 공간에 표시됩니다.

### 보고 및 예외적인 주문

2019년 11월 25일부터 2020년 4월 26일까지, 한 Target 서버에서 매출 기반 보고서 지표(AOV, RPV)에서 예외적인 주문 값을 계산하는 문제를 경험했습니다. 2019년 12월 19일부터 2020년 4월 23일까지 다른 서버에서 동일한 문제가 발생했습니다. 이 문제는 모든 Target 서버 또는 모든 Target 고객에게 영향을 주지 않았습니다.

다음의 경우 *영향을 받지* 않았습니다.

* Target 구현에서 서로 다른 서버를 사용합니다.
* 보고서에서 예외적인 주문을 제외하지 않았습니다.
* 전환 지표를 사용하여 활동을 측정했습니다.
* Target 활동에서는 Target(A4T)에 Analytics를 사용합니다.
* APAC 지역에 있습니다.

이 문제가 Target 보고에 영향을 미치는지 확인하려면 [클라이언트 지원팀에 문의하십시오](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB).

### Recommendations

* 피드의 항목이 이전 실행과 동일한 경우 Recommendations 피드 색인이 &quot;색인 큐 대기 중&quot;을 표시할 수 있습니다. 배달을 위한 제품 섭취는 영향을 받지 않습니다. (RECS-6663)

   이 문제는 Target 19.4.2 릴리스에서 해결되었습니다.

* Recommendations 피드를 처리하는 데 예상보다 시간이 더 오래 걸립니다. (COR-2836)

   Target 16.10.1 릴리스에서 수정되었습니다.

* Recommendation 피드 UI에 올바른 색인화 상태가 표시되지 않습니다. 백엔드 작업은 제대로 작동하지만 UI가 현재 상태를 가져와 표시할 수 없습니다.

   이 오류는 17.10.1 릴리스에서 수정되었습니다.

### 리디렉션 오퍼

페이지에서 경합 조건을 사용하면 원래 페이지 및 리디렉션 페이지의 페이지 보기가 카운트될 수 있습니다. 이 경합 조건을 피할 수 있도록 at.js 구현에 대한 업데이트가 예정되어 있습니다.

이 문제는 at.js 1.6.3에서 해결되었습니다.

### 제외 그룹

* 제외 그룹을 만든 후 자동 중복 해제를 적용하면 활동 다이어그램의 카운트가 UI에 올바르게 표시되지 않을 수 있습니다.
* 제외 그룹이 있는 기존 활동이 편집되면 UI에 수동 포함 내용이 제대로 반영되지 않을 수 있습니다.

이러한 문제가 해결되었습니다.

### Target API

Adobe I/O에서 v1 버전의 오퍼 API는 Target을 통해 생성된 모든 오퍼를 기본 작업 공간에 있는 것으로 처리합니다. (TTTEAM-41957)

이 문제가 해결되었습니다.

### at.js

at.js 버전 1.0으로 업그레이드한 후 at.js 및 Visitor API 2.2.0 간의 상호 작용으로 인해 Mbox가 Microsoft Explorer 11 브라우저에서 실행되지 않습니다. 이 문제는 at.js 버전 0.9.6 이상에 영향을 미칩니다. (TNT-27600)

API 2.3.0 이상 릴리스에서 해결됨

### 지역 타깃팅

지역 타깃팅 대상을 작성할 때 특수 문자(예: 공백 또는 쉼표)가 포함된 문자열 검색은 현재 사용할 수 없습니다. 이 문제는 도시, 주, 국가 등을 기반으로 대상을 작성할 때 나타납니다. 예를 들어, &quot;new york&quot;을 검색하는 경우 유효한 검색 결과를 반환하지 않습니다.

2018년 11월에 수정됨

### at.js

at.js 버전 1.6.0을 사용하는 경우, Analytics for Target (A4T) 리디렉션이 발생하지만 활동 자격이 없습니다.

at.js1.6.2 릴리스에서 해결됨

### 활동, 작업 공간 및 활동 삭제 API

API를 통해 삭제된 기본 작업 공간의 활동이 Target UI에 계속 표시됩니다. 임시 해결책으로, Target UI를 사용하는 기본 작업 영역에서 모든 활동을 삭제하십시오. (TGT-31315)

2018년 10월 25일 해결됨

### 자동화된 개인화(AP) 오퍼 수준 보고

자동화된 개인화(AP) 활동의 보고서에서 타깃팅된 경험을 클릭하면 현재 빈 결과와 함께 오류 메시지 또는 회전하는 아이콘이 표시됩니다. (TNT-30695)

2018년 9월 27일 해결됨

### 코드 편집기

Firefox 및 Internet Explorer에서 코드 편집기로 작업하는 동안 3단계 안내식 작업 과정의 1단계에서 VEC을 다시 로드하는 경우, 수정 사항 탭이 올바르게 렌더링되지 않지만 VEC의 기능은 영향을 받지 않습니다. (TGT-28730)

이 오류는 18.9.1 릴리스에서 수정되었습니다.

### 속성 프로모션 규칙을 사용하는 Recommendations 활동입니다

속성 프로모션 규칙을 사용하는 Recommendations 활동을 편집하거나 복사하는 경우 저장을 클릭하면 &quot;누락된 필드 있음&quot; 오류가 표시됩니다 .

이 오류는 17.8.1 릴리스에서 수정되었습니다.

### 백업 Recommendations

백업 Recommendations에서는 Target UI의 최근에 본 항목 카드에 &quot;활성화됨&quot;을 잘못 표시합니다. (TGT-29308)

이 오류 &quot;비활성화&quot;가 표시되도록 18.4.1 릴리스에서 수정되었습니다.

### 자동 Target 활동 및 보고 대상

자동 Target 활동에서 사용되는 보고 대상 이름이 변경되면 Target에서 해당 활동에 대한 추가 업데이트가 실패하고 오류 메시지가 표시될 수 있습니다.

이 문제는 Target 18.5.1(2018년 5월 22일) 릴리스에서 수정되었습니다.

### at.js

쿠키를 저장할 때 사용해야 하는 최상위 도메인을 추출하는 알고리즘이 at.js 버전 0.9.6에서 변경되었습니다. 이러한 변경으로 인해 쿠키를 IP를 사용하는 주소에 저장할 수 없습니다. 대부분의 경우 IP 주소는 테스트 용도로 사용되지만, 해결 방법으로 DNS 항목을 사용하거나, 로컬 상자에서 호스트 파일을 조정하거나, targetGlobalSettings() at.js 함수를 사용하여 IP 주소를 지원하는 코드 조각을 삽입할 수 있습니다.

이 문제는 at.js 버전 1.2에서 해결되었습니다.

### Target Premium에 대한 엔터프라이즈 사용자 권한

엔터프라이즈 권한 마이그레이션의 일부로, 모든 Target Premium 사용자 관리가 Adobe Target UI에서 Adobe Admin Console로 이동되었습니다.

마이그레이션의 결과로, 다음과 같은 두 가지 잠재적인 문제가 있을 수 있습니다.

* 관리자가 아닌 사용자가 이제 Adobe Target에 액세스할 수 있음을 나타내는 이메일을 받았습니다. 이것은 조직에 대한 마이그레이션이 완료되었음을 나타냅니다. 이메일 자체는 무시해도 됩니다.
* 마이그레이션 후에는 이전에 비활성화되었던 사용자에 대한 일부 보고서가 Adobe Admin Console에 다시 나타났습니다. Adobe Admin Console의 비활성화된 사용자가 마이그레이션 전에 Target의 사용자 목록에 계속 표시되는 경우 조직에 문제가 될 수 있습니다. 관리자는 Admin Console에서 사용자 목록을 검토하여 액세스 권한을 확인하는 것이 좋습니다.

이 문제는 2017년 8월 30일에 수정되었습니다.

### 활동 만들기

17.6.2 릴리스의 문제는 2017년 6월 22일과 2017년 6월 29일 사이에 만들어졌거나 업데이트된 활동에 영향을 주었을 수 있습니다. 다음과 같은 활동이 영향을 받았습니다.

* 경험 타깃팅(XT)에서 재배열된 경험이 원래 오퍼로 복구되었습니다.
* 활동에 로컬인 모든 세그먼트 규칙(대상 내에 저장되지 않음), 즉 조합된 대상, 위치 세분화 및 성공 지표에 대한 모든 규칙이 손실되었습니다. 

다른 활동은 영향을 받지 않았습니다.

**중요**: 이 문제는 자동으로 수정되지 않습니다. 이 문제를 해결하려면 영향을 받은 모든 활동을 다시 저장해야 합니다.

이 문제는 2017년 6월 29일에 수정되었습니다.

### 양식 기반 경험 작성기

양식 기반 경험 작성기를 사용할 때 다음과 같은 알려진 문제가 보고되었습니다.

* 자동으로 만든 글로벌 mbox(target-global-mbox) 이외의 mbox와 함께 양식 기반 경험 작성기를 사용한 다음, 참여 지표를 성공 지표로 선택하는 경우, 지표는 활동에 해당 mbox가 사용된 페이지에서만 증분됩니다. 예를 들어 mbox가 homepage\_mbox면 방문당 페이지 수 지표는 방문하는 동안 homepage\_mbox에 대한 히트 수가 됩니다. (TGT-22789)
* 프로세스의 1단계 동안 양식 기반 경험 작성기를 사용할 때 경험 타깃팅(XT) 활동에서 경험을 삭제할 경우 JavaScript 예외가 발생합니다. (TGT-24366)

첫 번째 문제는 Target 17.3.1 릴리스(2017년 3월)에서 수정되었습니다.

두 번째 문제는 Target 17.6.1 릴리스(2017년 6월)에서 수정되었습니다.

### at.js

Target 17.4.1(2017년 4월 27일) 릴리스 이후부터 VEC(시각적 경험 작성기)에서 이미지 삽입 작업을 사용하면 at.js 라이브러리를 사용할 때 오퍼 콘텐츠가 전달되지 않습니다.

이 문제는 2017년 5월 22일에 릴리스된 at.js 버전 0.9.7에서 수정되었습니다.

### 보고: A/B 및 경험 타깃팅(XT) 활동

4월 27일 PST, 오후 9시부터 5월 5일 오전 6시 사이에 &quot;페이지 확인함&quot; 전환 작업을 사용하는 지표로 생성 또는 편집한 A/B 및 XT 활동(다른 지표를 기준으로 하지 않음)이 전환을 잘못 기록했을 수 있습니다. 이 문제는 현재 해결되었지만 영향을 받는 기간 동안 이러한 활동에 대한 &quot;페이지 확인함&quot; 전환 작업에 대한 보고가 정확하지 않을 수 있으며, 이러한 오류는 수정할 수 없습니다. 이러한 활동에 대해 &quot;페이지 확인함&quot; 전환 작업을 기준으로 진행된 모든 의사 결정의 경우 영향을 받는 기간 전후에 기록된 데이터에만 의존하는 것이 좋습니다.

다른 지표에 대한 보고 데이터는 영향을 받지 않았으므로 계속 사용할 수 있습니다.

Target 17.4.3 핫픽스에서 수정되었습니다.

### 오퍼: A/B 및 경험 타깃팅(XT) 활동

2개 이상의 경험이 있고 4월 28일 금요일(PT 오후 9시)과 5월 1일 월요일(PT 오후 9시 15분) 사이에 양식 기반 경험 작성기를 사용하여 생성 또는 편집된 A/B 및 XT 활동의 오퍼에 대한 전달 및 미리 보기가 영향을 받았습니다. 기본 콘텐츠가 있는 오퍼만 표시되었습니다.

Target 17.4.3 핫픽스에서 수정되었습니다.

### at.js

VEC(시각적 경험 작성기) 및 at.js를 사용할 때 이동 및 재배열 작업을 수행하면 오퍼가 전달되지 않았습니다.

이 문제는 at.js 버전 0.9.6에서 수정되었습니다.

### 보고서

Target 17.3.1 릴리스(2017년 3월 30일)에 포함된 보고서에서 여러 지표를 보는 기능이 예기치 않은 동작으로 인해 제거되었습니다. 이 기능은 향후 릴리스에서 다시 사용할 수 있게 될 예정입니다.

보고서에서 여러 지표를 보는 기능이 Target 17.4.1 릴리스(2017년 4월 27일)에 포함되었습니다.

### 오퍼

이미지 오퍼 라이브러리(오퍼 \> 이미지 오퍼)에서 삭제된 이미지가 UI에 계속 표시됩니다. 향후 릴리스에서는 이러한 삭제된 이미지가 더 이상 표시되지 않습니다. 당분간은 삭제된 이미지가 UI에 표시되지만, 상태는 삭제됨입니다. (TGT-23793)

Target 17.4.1 릴리스(2017년 4월 27일)에서 수정되었습니다.

### 리디렉션 오퍼

최근 조회 기준의 경우, entity.id 매개 변수가 mbox 요청에 전달되지 않으면 엔티티 기반 다이내믹 규칙이 권장 사항을 표시하지 않습니다. (RECS-6241)

이 문제는 Recommendations 릴리스(2018년 3월 22일) 이후에 수정되었습니다. Recommendations 릴리스 이후에 entity.id가 mbox 요청에 전달되지 않은 경우 Target에서 엔티티 기반 다이내믹 규칙을 건너뜁니다.

### at.js

사용자가 at.js 설정을 업데이트한 후 구현 세부 사항 페이지에서 at.js를 다운로드하려고 하면 at.js 대신 mbox.js가 다운로드됩니다. (TGT-23069)

Target 17.3.1 릴리스(2017년 3월 30일)에서 수정되었습니다.

### 글로벌 제외 규칙

글로벌 제외 규칙은 Premium Recommendations용 에지로 전파되는 데 10~20분이 소요됩니다. (RECS-5270)

Recommendations 17.2.2.0 릴리스(2017년 3월 6일)에서 수정되었습니다.

### A4T(Analytics for Target) 보고

보고 지표가 전환되면 보고서가 업데이트되지 않습니다. 이것은 UI 문제입니다. 보고 데이터 수집 또는 전달에는 영향을 미치지 않습니다. (TGT-22970)

Target 17.2.2.0 릴리스(2017년 2월 24일)에서 수정되었습니다.

### CSV 보고서

다운로드된 보고서는 예외적인 주문 제외 설정을 준수하지 않습니다. (TGT-21871)

Target 17.2.1.0 릴리스에서 수정되었습니다.
