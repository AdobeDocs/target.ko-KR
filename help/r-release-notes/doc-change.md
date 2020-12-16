---
keywords: target documentation change log;documentation updates;new topics;edits;updates;update
description: 이 페이지에는 릴리스 순으로 정렬된 Adobe Target 문서의 중요한 변경 내용이 나열됩니다.
title: Adobe Target 제품 설명서의 내용이 변경되었습니다.
feature: release notes
translation-type: tm+mt
source-git-commit: 7f35d23897675e970012ad506d057de6ca2c2b2d
workflow-type: tm+mt
source-wordcount: '3144'
ht-degree: 28%

---


# 설명서 변경 내용{#documentation-changes}

이 페이지에는 [!DNL Adobe Target] 제품 설명서에 대한 중요한 변경 내용이 나와 있습니다.

## Adobe Target Standard/Premium 20.10.1(2020년 10월 28일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 9년 12월 | [디바이스에서 의사 결정](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md) | 새 주제입니다.  |
|  | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md) | 다음 문제를 알려진 문제 섹션에서 해결된 문제 섹션으로 옮겼습니다.&quot;&quot;처리 중&quot; 레이블을 표시하는 이미지 오퍼입니다.&quot; |
| 1년 12월 | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | &quot;Adobe Target의 디바이스에서 의사 결정을 내림하여 지연 없이 개인화 및 테스트&quot;를 위한 웨비나 녹화를 포함했습니다. |
| 24년 11월 | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md) | 다음과 같은 알려진 문제가 추가되었습니다.<ul><li>[보고 - 다운로드 가능한 .csv 보고서에 있는 데이터와 Target UI에 표시된 보고서의 데이터가 일치하지 않습니다.](/help/r-release-notes/known-issues-resolved-issues.md#csv)</li></ul>다음과 같은 해결된 문제가 추가되었습니다.<ul><li>[A4T(Analytics for Target) 보고](/help/r-release-notes/known-issues-resolved-issues.md#section_FD2FC86E7C734D60B1EDC9DEF60E1014)</li></ul> |
|  | [지표 정의 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md) | 다음과 같은 FAQ가 추가되었습니다.&quot;목표 지표를 구성하는 동안 고급 설정 옵션에 액세스할 수 없는 이유는 무엇입니까?&quot; |
|  | [성공 지표](/help/c-activities/r-success-metrics/success-metrics.md) | A4T를 사용하는 활동에 대한 메모의 텍스트가 조정되었습니다. |
| 17년 11월 | [활동 설정 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-activity-setup.md) | 다음과 같은 FAQ가 추가되었습니다.&quot;방문자가 A4T를 사용하는 자동 Target 활동에서 서로 다른 방문에서 타깃팅된 경험과 제어된 경험 간을 전환할 수 있습니까?&quot; |
|  | [자동 Target 문제 해결 및 FAQ](/help/c-activities/auto-target/auto-target-troubleshooting-faqs.md) | 다음과 같은 FAQ가 추가되었습니다.&quot;모델이 빌드될 때까지 90(컨트롤)/10(타깃팅됨) 분할이 있는 자동 Target을 사용하는 것이 권장됩니까?&quot; |
|  | [보고서 보기 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | 다음과 같은 FAQ가 추가되었습니다.&quot;A4T를 사용하는 자동 Target 활동에서 Analytics 방문 및 전환 크레딧이 어떻게 카운트됩니까?&quot; |
| 13년 11월 | [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | at.js 2.3.3에 대한 정보가 추가되었습니다. |
| 10년 11월 | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 11월 11일로 예정된 Adobe Target 커뮤니티 Q&amp;A 커피 휴가에 대한 정보가 추가되었습니다. |
| 3년 11월 | [Analytics 및 Target 통합 문제 해결(A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md) | 다음 문제 해결 항목을 업데이트했습니다.&quot;필요한 보고서 세트가 표시되지 않습니다.&quot; |
| 10월 28일 | [서버 측: Target 구현](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | 첫 번째 방문자는 서버측에서 아니라 클라이언트측으로만 초기화할 수 있다는 메모를 추가했습니다. |
| 10월 27일 | [서버 측: Target 구현](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | 새 *[Adobe Target SDK](https://adobetarget-sdks.gitbook.io/docs/)* 포털에 링크가 추가되었습니다. |
|  | [Analytics를 보고 소스로 사용하는 활동 만들기](/help/c-integrating-target-with-mac/a4t/campaign-creation.md) | `analyticsLogging = client_side`을(를) 사용하는 경우 Analytics를 자동 Target 활동과 함께 보고 소스(A4T)로 사용할 때 `sessionId` 값을 [!DNL Analytics]에 전달해야 한다는 내용의 정보가 추가되었습니다. |
|  | [Analytics for Target 구현](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) | `analyticsLogging = client_side`을(를) 사용하는 [!UICONTROL 자동 할당] 및 [!UICONTROL 자동 Target] 활동에 대해서도 sessionId를 전달해야 한다는 내용의 정보가 추가되었습니다. |
|  | [릴리스 노트](/help/r-release-notes/release-notes.md): 20.10.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 노트에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |

## Adobe Target Standard/Premium 20.9.1(2020년 9월 30일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 10월 26일 | [Target 보안 개요](/help/c-implementing-target/c-considerations-before-you-implement-target/target-security-overview.md) | *Adobe Target 보안 개요* 백서를 업데이트했습니다. |
| 10월 22일 | [CNAME 및 Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | at.js 버전 1.8.2 및 2.3.1에서 CNAME 지원에 대한 수정 사항에 대한 정보가 추가되었습니다. |
|  | [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | at.js 버전 1.8.2 및 2.3.1에서 CNAME 지원에 대한 수정 사항에 대한 정보가 추가되었습니다. |
| 10월 15일 | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | Target Standard/Premium 20.10.1 릴리스(2020년 10월 27일)의 베타 버전 노트를 업데이트했습니다. |
| 10월 14일 | [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 두 개의 경험만 있는 자동 할당 활동에 대한 트래픽 할당에 대한 메모를 추가했습니다. |
| 10월 13일 | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 2020년 11월 10일로 예정된 다음 라이브 웨비나에 대한 정보가 추가되었습니다.<ul><li>Adobe Target의 디바이스에서 의사 결정을 내림으로써 지연 없이 개인화 및 테스트</li></ul> |
|  | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | 2020년 11월 10일로 예정된 다음 라이브 웨비나에 대한 정보가 추가되었습니다.<ul><li>Adobe Target의 디바이스에서 의사 결정을 내림으로써 지연 없이 개인화 및 테스트</li></ul> |
| 10월 12일 | [콘텐츠 전달 문제 해결](/help/c-activities/c-troubleshooting-activities/content-trouble.md) | 인증 토큰을 생성해야 하는 권한 수준을 나타내기 위해 디버깅 도구[에 사용할 인증 토큰을 검색합니다.](/help/c-activities/c-troubleshooting-activities/content-trouble.md#section_BED130298E794D1FA229DB7C3358BA54) |
|  | [프로필 API 설정](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md) | 인증 토큰을 생성해야 하는 권한 수준을 나타내도록 항목을 업데이트했습니다. |
|  | [자동 타깃팅](/help/c-activities/auto-target/auto-target-to-optimize.md) | 자동 Target을 사용하여 실제 성공 스토리가 추가되었습니다. |
|  | [유사한 페이지에 동일한 경험 포함](/help/c-experiences/c-visual-experience-composer/temtest.md) | 전체 도메인에서 동일한 활동을 렌더링하는 방법을 설명하는 섹션이 추가되었습니다. |
|  | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md) | 다음과 같은 알려진 문제가 추가되었습니다.<ul><li>자동 할당 및 자동 Target 활동에 대한 Target(A4T) 지표 분석</li></ul> |
| 10월 8일 | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics) | 다음과 같은 해결된 문제가 추가되었습니다.<ul><li>[자동 Target 보고](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics)</li></ul>다음 문제를 알려진 문제 섹션에서 해결된 문제 섹션으로 옮겼습니다.<ul><li>[보고](/help/r-release-notes/known-issues-resolved-issues.md#conversions-audiences)</li></ul> |
|  | [하이브리드 구현](/help/c-implementing-target/hybrid-implementation.md) | 새 주제입니다.  |
| 10월 7일 | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | Target Standard/Premium 20.10.1 릴리스에 대한 정보가 추가되었습니다. |
| 10월 1일 | [성공에 필요한 트래픽 예측](/help/c-activities/t-automated-personalization/ap-traffic-estimator.md) | FAQ 섹션이 추가되었습니다. |
| 9월 30일 | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 다음 라이브 웨비나에 대한 정보가 추가되었습니다.<ul><li>Adobe Target 및 Analytics를 사용하여 규모에 맞게 조정 가능한 개인화</li></ul> |
|  | [릴리스 노트](/help/r-release-notes/release-notes.md): 20.9.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 노트에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |

## Adobe Target Standard/Premium 20.8.1(2020년 9월 2일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 9월 29일 | [Analytics 및 Target 통합 문제 해결(A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md#section_75002584FA63456D8D9086172925DD8D) | at.js 1.x 및 at.js 2.x에서 보충 ID를 검사하는 방법에 대한 정보가 추가되었습니다. |
| 9월 24일 | [활동 QA 북마클릿](/help/c-activities/c-activity-qa/activity-qa-bookmark.md) | at.js 2에 대한 활동 QA 북마클릿에 대한 코드를 업데이트했습니다.*x*&#x200B;에는 사용할 수 없습니다. |
|  | [카탈로그 검색](/help/c-recommendations/c-products/catalog-search.md#faq) | 숫자 값으로 사용자 지정 속성을 검색하는 방법에 대한 참고가 추가되었습니다. |
|  | [권장 사항 FAQ](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | 다음과 같은 FAQ가 추가되었습니다.&quot;숫자 값이 있는 사용자 지정 속성을 검색할 때 카탈로그 검색에 올바른 결과가 표시되지 않는 이유는 무엇입니까?&quot; |
|  | [Target 작동 방식](/help/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934) | &quot;에지 네트워크&quot;에 나열된 Target 클러스터 및 Target Central 클러스터 위치를 업데이트했습니다. |
| 9월 23일 | [Analytics 추적 서버 사용](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md) | 전체 항목을 [!DNL Adobe Experience Platform Debugger] 및 브라우저 개발자 도구의 정보로 업데이트했습니다. |
|  | [프로필 및 변수 용어집](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | &quot;user.header(&#39;x-forwarded-for&#39;)&quot;가 더 이상 사용되지 않음을 나타내도록 &quot;user.header(&#39;x-cluster-client-ip&#39;)&quot; 행을 업데이트했습니다. |
|  | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | Target Standard/Premium 20.9.1(2020년 9월 30일) 릴리스에 대한 정보가 추가되었습니다. |
| 9월 15일 | [Target 릴리스 노트(현재)](/help/r-release-notes/release-notes.md) | 자동 Target 활동에 대한 Target(A4T) 지원을 포함하는 Target Standard/Premium 20.8.3 릴리스에 대한 정보가 추가되었습니다. 이전 릴리스에서 자동 할당 활동에 대한 지원이 추가되었습니다. |
|  | [자동 할당 및 자동 Target 활동에 대한 Target(A4T) 분석 지원](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa). | 자동 Target 활동에서 A4T 지원에 대한 정보가 추가되었습니다. |
|  | [활동 QA 북마클릿](/help/c-activities/c-activity-qa/activity-qa-bookmark.md) | 값이 비어 있는 `at_preview_token` 매개 변수를 사용하여 사이트에서 페이지를 로드하여 QA 모드에서 수동으로 자신을 강제로 나오게 하는 방법이 at.js 1에 적용됨을 나타내는 텍스트가 업데이트되었습니다.*x*&#x200B;에만 사용할 수 있습니다. |
|  | [카탈로그 검색](/help/c-recommendations/c-products/catalog-search.md) | 전체 주제가 업데이트되었습니다. |
| 9월 10일 | [Target 릴리스 노트(현재)](/help/r-release-notes/release-notes.md) | 다음과 같은 새로운 기능을 포함하는 Target Standard/Premium 20.9.2 릴리스에 대한 정보가 추가되었습니다.기준 시퀀스 내에서 추천 슬롯을 제어합니다. |
|  | [기준 시퀀스 만들기](/help/c-recommendations/c-algorithms/create-criteria-sequence.md) | &quot;반환된 항목 수 제한&quot; 기능에 대한 정보가 추가되었습니다. |
| 9월 9일 | [활동 QA 북마클릿](/help/c-activities/c-activity-qa/activity-qa-bookmark.md) | at.js 2에서 사용할 JavaScript 코드를 추가했습니다.*x*&#x200B;에는 사용할 수 없습니다. |
| 9월 3일 | [시각적 경험 작성기 Helper 확장 프로그램](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) | 쿠키 이름 및 도메인에 대한 정보와 함께 &quot;VEC 도우미 브라우저 확장 다운로드 및 설치&quot; 섹션을 업데이트했습니다. |
|  | [시각적 경험 작성기 및 고급 경험 작성기 관련 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md) | &quot;최근에 발표된 Google Chrome SameSite 쿠키 실행 정책이 VEC 및 EEC에 어떤 영향을 줍니까?&quot; 섹션을 참조하십시오. |
| 9월 2일 | [릴리스 노트](/help/r-release-notes/release-notes.md): 20.8.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 노트에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |

## Adobe Target Standard/Premium 20.7.1(2020년 7월 27일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 8월 31일 | [Recommendations과 함께 Adobe Analytics 사용](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md) | FAQ 섹션이 추가되었습니다. |
| 8월 28일 | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md) | 다음을 업데이트했습니다.<ul><li>알려진 문제 섹션에 추가되었습니다.&quot;보고 - 현재 전환은 사용된 고객을 기준으로 다르게 증가합니다.&quot;</li><li>해결된 문제 섹션에 추가되었습니다.&quot;Google Chrome 버전 80+을 사용할 때 VEC(Visual Experience Composer) 또는 EEC(Enhanced Experience Composer)에서 페이지가 로드되지 않습니다.&quot;</li></ul> |
|  | [Target 릴리스 노트(현재)](/help/r-release-notes/release-notes.md) | mbox.js의 사용 중단 날짜가 2020년 8월 30일에서 2021년 1월 18일로 변경되었습니다. |
| 8월 26일 | [Target Recommendations과 함께 Adobe Analytics 사용](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md) | 새 주제입니다.  |
| 8월 24일 | [성공 지표](/help/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) | &quot;고급 설정&quot; 섹션이 업데이트되었습니다. |
| 8월 21일 | [Adobe Target 시작 키트 개요](/help/c-intro/target-welcome-kit.md) | 새 아티클 및 하위 주제입니다. |
| 8월 20일 | [시각적 경험 작성기 및 고급 경험 작성기 관련 문제 해결](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md) | 다음 섹션이 추가되었습니다.&quot;최근에 발표된 Google Chrome SameSite 쿠키 실행 정책은 VEC 및 EEC에 어떤 영향을 줍니까?&quot; |
|  | [클릭 추적](/help/c-activities/r-success-metrics/click-tracking.md) | 다음 텍스트가 업데이트되었습니다.&quot;두 개 이상의 요소를 선택하는 경우 참가자가 선택한 요소 중 하나를 클릭하면 클릭이 계산됩니다. 각 항목을 별도로 카운트하려면 각 요소에 대해 개별 성공 지표를 설정하십시오. 한 페이지에서 여러 요소를 클릭하여 하나의 항목을 카운트하려면 CSS 요소 선택기를 편집하여 여러 요소와 일치시킵니다.&quot; |
|  | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | Target Standard/Premium 20.9.1(2020년 9월 2일) 릴리스에 대한 정보가 추가되었습니다. |
| 8월 14일 | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md) | Recommendations 활동의 QA에 대한 알려진 문제가 추가되었습니다. |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | `serverState`을 사용하고 반환된 컨텐츠에서 `<script>` 태그를 사용하는 경우 HTML 컨텐츠에 `</script>` 대신 `<\/script>`가 사용되는지 확인하는 텍스트가 추가되었습니다. |
| 8월 12일 | [Target UI 이해](/help/c-intro/understand-the-target-ui.md) | 새 주제입니다.  |
|  | [Adobe Target API 개요](/help/api/api-overview.md) | 새 주제입니다.  |
| 8월 10일 | [CNAME 및 Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | CNAME 사용 시 쿠키 헤더의 크기가 증가함을 나타내는 텍스트가 추가되었습니다. |
|  | [Adobe Audience Manager과 Target 통합](/help/c-integrating-target-with-mac/audience-manager-target-integration.md) | 새 주제입니다.  |
|  | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 다음 보관된 웨비나를 보는 링크가 추가되었습니다.&quot;HSBC가 Adobe Target 및 AI를 활용하여 개인화를 규모에 맞게 신속하게 최적화하고 전달하는 방법&quot; |
| 8월 6일 | [자동 타깃팅](/help/c-activities/auto-target/auto-target-to-optimize.md#how-long) | 다음 FAQ에 대한 텍스트가 업데이트되었습니다.&quot;모델 제작에 얼마나 기다려야 합니까?&quot; |
|  | [분류 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-classifications.md) | 대상 유형에 대한 텍스트를 업데이트했습니다. |
| 8월 5일 | [Target 쿠키 삭제](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cookie-deleting.md) | 전체 주제가 업데이트되었습니다. |
| 8월 4일 | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 8월 13일로 예정된 &quot;인공 지능(AI) 및 Adobe Target을 사용한 개인화 전략&quot; 웨비나에 대한 등록 정보가 추가되었습니다. |
|  | [브라우저에서 혼합 컨텐츠 사용](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md) | 주제가 업데이트됨. |
| 8월 3일 | [성공 지표](/help/c-activities/r-success-metrics/success-metrics.md) | 방문자 대 방문 수와 관련하여 [!UICONTROL 증분 카운트] 옵션이 의미하는 바를 설명하는 참고가 추가되었습니다. |
| 31년 7월 | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md) | 새롭게 알려진 문제 추가:&quot;&quot;처리&quot; 레이블을 표시하는 이미지 오퍼.&quot; |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | pageLoad를 수행하기 위해 `getoffers()`을(를) 사용하기 위한 코드 샘플이 추가되었습니다. |
|  | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 8월 5일 예정된 Adobe Target 커뮤니티 커피 브레이크에 대한 등록 정보가 추가되었습니다. |
| 28년 7월 | [개인화 통찰력 보고서](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md),<br>[ 자동화된 세그먼트 보고서](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md) <br>및  [중요 속성 보고서](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) | 주제 상단에 있는 메모에서 텍스트가 업데이트되었습니다. |
|  | [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | 다음과 같은 FAQ가 추가되었습니다.<ul><li>자동 할당 활동을 실행하는 동안 보고서 데이터 재설정 옵션을 사용할 수 있습니까?</li><li>환경에 대한 빌드 모델의 자동 할당 기능은 무엇입니까?</li></ul> |
|  | [자동 타깃팅](/help/c-activities/auto-target/auto-target-to-optimize.md) | 다음 FAQ가 추가되었습니다.<ul><li>자동 Target 활동을 실행하는 동안 보고서 데이터 재설정 옵션을 사용할 수 있습니까?</li></ul>&quot;고려 사항&quot; 섹션의 텍스트가 업데이트되었습니다. |
|  | [Automated Personalization FAQ](/help/c-activities/t-automated-personalization/automated-personalization-faq.md) | 다음과 같은 FAQ가 추가되었습니다.<ul><li>Automated Personalization 활동을 실행하는 동안 보고서 데이터 재설정 옵션을 사용할 수 있습니까?</li><li>Automated Personalization은 환경과 관련하여 어떻게 모델을 구축합니까?</li></ul> |
|  | [지원되는 브라우저](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | Internet Explorer 및 알 수 없는 요소에 대한 정보가 추가되었습니다. |
|  | [고객 속성](/help/c-target/c-visitor-profile/working-with-customer-attributes.md) | 다음 단락을 업데이트했습니다.<br>[!DNL Adobe]은 CRM 데이터베이스의 고객 속성(방문자 프로필) 데이터의 100%가 [!DNL Experience Cloud]에 매핑되므로 [!DNL Target]에서 타깃팅에 사용할 수 있습니다. 현재 디자인에서 적은 양의 데이터(큰 제작 배치의 최대 0.1%까지)가 온보드 방식이 아닐 가능성이 있습니다. |
| 27년 7월 | [Target 관리](/help/administrating-target/administrating-target.md) | [!UICONTROL 관리] 페이지에 대한 새 UI 변경 사항을 반영하도록 이 페이지의 모든 연결된 항목의 텍스트가 업데이트되었습니다. |
|  | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 다음과 같이 변경되었습니다. <ul><li>다음 웨비나에 대한 등록 정보를 추가했습니다.&quot;HSBC가 Adobe Target 및 AI를 활용하여 개인화를 규모에 맞게 신속하게 최적화하고 전달하는 방법&quot;</li><li>개인화 엔진 부문 Gartner Magic Quadrant에서 Adobe이 리더로 선정되는 것에 대한 정보가 추가되었습니다.</li></ul> |
|  | [양식 기반 경험 작성기](/help/c-experiences/form-experience-composer.md) | 4단계 아래의 명확한 정보:위치를 선택합니다. |
| 24년 7월 | <br>[at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | at.js 2.3.2에 대한 정보가 추가되었습니다. |
|  | [릴리스 노트](/help/r-release-notes/release-notes.md): 20.7.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 노트에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |

## Adobe Target Standard/Premium 20.5.1(2020년 6월 17일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 17년 7월 | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 7월 22일 Adobe Target Coffee Break에 대한 정보가 추가되었습니다. |
| 15년 7월 | [자동 할당을 사용하면 수동 테스트보다 테스트 결과를 빠르게 얻고 매출을 높일 수 있습니다](/help/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md) | 새 주제입니다.  |
| 14년 7월 | [자동 할당](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md),<br>[ 자동 Target](/help/c-activities/auto-target/auto-target-to-optimize.md) <br><br>[및 자동화된 개인화 FAQ](/help/c-activities/t-automated-personalization/automated-personalization-faq.md) | 활동을 통해 중간에 목표 지표를 변경해서는 안 된다는 권장 FAQ가 추가되었습니다. |
| 7년 7월 | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 7월 8일 Adobe Target Coffee Break에 대한 정보가 추가되었습니다. |
| 6월 25일 | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | Target Standard/Premium 20.6.1 릴리스(2020년 7월)에 대한 정보가 추가되었습니다. |
|  | [Target 설명서 개요](/help/r-release-notes/target-documentation.md) | [!DNL Target] 설명서의 다른 소스를 자세히 설명하는 새 주제입니다. |
| 6월 23일 | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 6월 24일 Adobe Target Coffee Break에 대한 정보가 추가되었습니다. |
|  | [프로필 속성](/help/c-target/c-visitor-profile/profile-parameters.md) | 다른 프로필 스크립트에서 한 프로필 스크립트의 결과를 사용하는 종속 프로필 스크립트를 만드는 것은 권장되지 않습니다. |
|  | [at.js 작동 방식](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | 다음 비디오를 추가했습니다.업무 시간:at.js 팁 및 개요 |
| 6월 17일 | [CNAME 및 Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | 주제가 업데이트됨. |
|  | [응답 토큰](/help/administrating-target/response-tokens.md) | [!UICONTROL 자동 Target] 및 [!UICONTROL Automated Personalization] 활동에 대한 트래픽 할당 방법에 대한 응답 토큰에 대한 정보가 추가되었습니다. |
|  | [활동 만들기](/help/c-integrating-target-with-mac/a4t/campaign-creation.md) | 자동 할당 활동에 대한 Target(A4T) 지원에 대한 분석에 대한 정보가 추가되었습니다. |
|  | [사용자](/help/administrating-target/c-user-management/c-user-management/user-management.md) | *역할 및 권한 지정*&#x200B;에 새 [!UICONTROL 게시자] 역할에 대한 정보가 추가되었습니다. |
|  | [Enterprise 권한 구성](/help/administrating-target/c-user-management/property-channel/properties-overview.md) | *6단계 아래의 새 [!UICONTROL 게시자] 역할에 대한 정보가 추가되었습니다.역할 및 권한*&#x200B;을 지정합니다. |
|  | [Enterprise 사용자 권한](/help/administrating-target/c-user-management/property-channel/property-channel.md) | *업무 시간에 대한 링크를 추가했습니다.Target 프리미엄 작업 영역 세션*. |
|  | [릴리스 노트](/help/r-release-notes/release-notes.md): 20.5.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 노트에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |

## Adobe Target Standard/Premium 20.4.1(2020년 5월 6일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 6월 15일 | [Target 릴리스 노트(현재)](/help/r-release-notes/release-notes.md) | at.js 1.8.2 및 at.js 2.3.1 릴리스에 대한 정보가 추가되었습니다. |
|  | [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | at.js 1.8.2 및 at.js 2.3.1 릴리스에 대한 정보가 추가되었습니다. |
|  | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | [!DNL Analysis Workspace]에서 A4T 지원에 대한 정보를 포함하도록 [!DNL Target Standard/Premium] 20.5.1 릴리스(2020년 6월 17일)에 대한 메모를 업데이트했습니다. |
| 6월 12일 | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | `deviceIdLifetime` 설정에 대한 정보가 추가되었습니다. |
|  | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | at.js 1.8.2 및 at.js 2.3.1 릴리스에 대한 정보가 추가되었습니다. |
| 6월 8일 | [모바일 앱용 Target FAQ](/help/c-target-mobile-app/target-for-mobile-apps-faq.md) | 다음 FAQ에 대한 텍스트가 업데이트되었습니다.&quot;Target Mobile은 Adobe Target Premium 제품 SKU의 기능만 제공합니까?&quot; |
|  | [보고서 보기 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | 전체 주제가 업데이트되었습니다. |
| 6월 5일 | [Target 공지 및 이벤트](/help/r-release-notes/target-announcements.md) | 6월 10일 Adobe Target Coffee Break에 대한 정보가 추가되었습니다. |
|  | [상승도 및 신뢰도 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md) | 다음 FAQ에 대한 텍스트가 업데이트되었습니다.&quot;계산된 지표에서 향상도 및 신뢰도가 표시되지 않는 이유는 무엇입니까?&quot; |
| 6월 4일 | [A4T 보고](/help/c-integrating-target-with-mac/a4t/reporting.md) | &quot;Analytics의 보고서&quot; 섹션이 업데이트되었습니다. |
| 6월 1일 | [Target 공지](/help/r-release-notes/target-announcements.md) | 예정된 Target 이벤트를 알리는 새 페이지가 추가되었습니다. |
|  | [응답형 경험을 위한 모바일 뷰포트](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md) | Apple iPhone 11, Apple iPhone SE 및 Google Pixel 2 XL 모델의 뷰포트 크기 및 해상도가 업데이트되었습니다. |
| 28년 5월 | [보고 FAQ](/help/c-reports/reporting-frequently-asked-questions.md) | 다음과 같은 새로운 FAQ가 추가되었습니다. <ul><li>새 방문자 및 돌아온 방문자 지표는 어떻게 카운트됩니까?</li></ul> |
| 27년 5월 | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | 자동 할당 활동에 대한 Target(A4T) 지원에 대한 분석에 대한 정보가 추가되었습니다. |
| 26년 5월 | [프로필 속성](/help/c-target/c-visitor-profile/profile-parameters.md) | 다음 정보가 추가되었습니다.&quot;스크립트를 비활성화한 후 매개 변수가 프로필에 남아 있습니다. 프로필에 활동의 잠재고객에게 사용된 매개 변수가 이미 들어 있는 사용자는 해당 활동에서 자격을 얻게 됩니다.&quot; |
| 21년 5월 | [허용 목록에 추가하다 Target 에지 노드](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md) | 목록에 `mboxedge30.tt.omtrdc.net`을(를) 추가했습니다. |
| 20년 5월 | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | 예정된 Target Standard/Premium 20.6.1(2020년 6월 10일) 릴리스에 대한 정보가 추가되었습니다. |
|  | [호스트](/help/administrating-target/hosts.md) | &quot;보안 우수 사례&quot; 섹션에 메모를 추가했습니다. |
| 14년 5월 | [Target 릴리스 노트(현재)](/help/r-release-notes/release-notes.md) | 프로필 배치 상태 API v2 변경 사항에 대한 정보가 추가되었습니다. |
| 13년 5월 | [CNAME 및 Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | &quot;알려진 제한 사항&quot; 섹션이 추가되었습니다. |
| 11년 5월 | [호스트](/help/administrating-target/hosts.md) | 리디렉션 및 허용 목록에서 ubox 기능 사용에 대한 정보가 추가되었습니다. |
|  | [리디렉터 작업](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) | 열린 리디렉션 취약점을 방지하기 위해 호스트를 사용하는 방법에 대한 정보가 추가되었습니다. |
|  | [이메일에 권장 사항 통합](/help/c-recommendations/c-recommendations-faq/integrating-recs-email.md) | 열린 리디렉션 취약점을 방지하기 위해 호스트를 사용하는 방법에 대한 정보가 추가되었습니다. |
|  | [이메일: Target 구현](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md) | 열린 리디렉션 취약점을 방지하기 위해 호스트를 사용하는 방법에 대한 정보가 추가되었습니다. |
|  | [활동 QA](/help/c-activities/c-activity-qa/activity-qa.md) | &quot;고려 사항&quot; 섹션을 업데이트했습니다. |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | &quot;설정&quot; 아래의 &quot;overrideMboxEdgeServer&quot; 행을 업데이트했습니다. |
| 6년 5월 | [Apple ITP(Intelligent Tracking Prevention) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md) | ITP 2.3에 대한 정보가 추가되었습니다. |
|  | [릴리스 노트](/help/r-release-notes/release-notes.md): 20.4.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 노트에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |

## Adobe Target Standard/Premium 20.2.1(2020년 2월 19일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 4년 5월 | [보고 FAQ](/help/c-reports/reporting-frequently-asked-questions.md#uneven) | 추가된 새 FAQ:&quot;A/B 또는 MVT 활동에서 내 경험 간에 트래픽이 분리된 이유는 무엇입니까?&quot; |
| 29년 4월 | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md) | 예외적인 주문 시 보고에 대해 알려진 문제가 추가되었습니다. |
| 28년 4월 | [프로필 및 변수 용어집](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | 사용자의 IP 주소를 검색하기 위해 새로운 AWS 가장자리와 `user.header('x-forwarded-for')`을(를) 함께 사용하는 방법에 대한 정보가 제거되었습니다. 이제 이 명령은 최신 AWS 가장자리에서도 작동합니다. |
|  | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | Target Standard/Premium 릴리스(20.4.1)의 날짜가 5월 6일로 변경되었습니다. |
| 23년 4월 | [CNAME 및 Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | 주제가 업데이트됨. |
| 22년 4월 | [Target 릴리스 노트(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | 새 섹션이 추가되었습니다.*프로필 배치 상태 API v2 변경 사항(2020년 5월 4일).* |
| 14년 4월 | [허용 목록에 추가하다 Target 에지 호스트](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md) | 새 주제입니다.  |
| 10년 4월 | [단일 페이지 애플리케이션 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md#bp) | 새 섹션이 추가되었습니다.&quot;구현 우수 사례&quot; |
| 7년 4월 | [상승도 및 신뢰도 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md#lift-condidence) | &quot;계산된 지표에 향상도 및 신뢰도가 표시되지 않는 이유는 무엇입니까?&quot;에 대한 텍스트가 업데이트되었습니다. |
| 2년 4월 | [프로필 및 변수 용어집](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | 사용자의 IP 주소를 검색하기 위해 새로운 AWS 가장자리와 `user.header('x-forwarded-for')`을(를) 함께 사용하는 방법에 대한 정보가 추가되었습니다. |
|  | [at.js 1.*x*&#x200B;에서 at.js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md)&#x200B;로 업그레이드 | 다음 참고가 추가되었습니다.<ul><li>ECID library v4.3.0+ 및 at.js 2.*x*&#x200B;를 설치한 뒤 고유한 도메인을 확장하고 사용자를 추적할 수 있는 활동을 만들 수 있습니다. 이 기능은 세션이 만료된 후에만 작동합니다.</li></ul> |
| 3월 30일 | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md#atjs) | at.js 2.2.0 이전 at.js 버전에 영향을 주는 알려진 문제가 추가되었습니다. 이 문제로 인해 Adobe Analytics 코드가 페이지 요소에 없을 때 Analytics에서 Target(A4T)에 대한 전환을 보고하지 않는 문제가 발생했습니다. |
|  | [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | at.js 버전 2.2.0 세부 정보에 다음 정보가 추가되었습니다.<ul><li>Adobe Analytics 코드가 페이지 요소에 없을 때 Analytics for Target(A4T)에서 클릭 추적이 전환을 보고하지 않던 문제를 수정했습니다.</li></ul> |
| 3월 25일 | [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | at.js의 다음 새 버전에 대한 정보가 추가되었습니다.<ul><li>at.js 버전 2.3.0</li><li>at.js 버전 1.8.1</li></ul> |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | &quot;설정&quot; 섹션에 다음과 같은 새 행을 추가했습니다.<ul><li>cspScriptNonce</li><li>cspStyleNonce</li></ul>다음 새 섹션이 추가되었습니다.<ul><li>콘텐츠 보안 정책</li></ul> |
| 3월 24일 | [Apple ITP(Intelligent Tracking Prevention) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md#impact) | 다음 사항에 대한 영향에 대한 정보가 추가되었습니다.<ul><li>3rdPartyID를 기반으로 하는 프로필 스크립트</li><li>iOS 장치의 QA/미리 보기 URL</li></ul> |
| 3월 20일 | [릴리스 노트(현재)](/help/r-release-notes/release-notes.md) | Target Standard/Premium 20.2.1 릴리스는 2020년 3월 23일이 될 것임을 나타냅니다. |
| 3월 13일 | [제한](/help/r-troubleshooting-target/target-limits.md) | &quot;대상자, 계정당 재사용 가능&quot; 수를 업데이트했습니다. |
| 3월 12일 | [릴리스 노트(현재)](/help/r-release-notes/release-notes.md#summit) | 온라인 디지털 Summit 컨퍼런스에 무료로 액세스하기 위한 등록 정보를 추가했습니다. |
| 3월 9일 | [개인 정보 보호](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md) | &quot;IP 주소의 마지막 8진수 대체&quot; 섹션에 더 많은 정보를 추가했습니다. |
|  | [다중 값 특성을 사용한 작업](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md) | *JavaScript*&#x200B;에서 다중 값 매개 변수를 전달하는 코드 샘플이 업데이트되었습니다. |
|  | [사용자 지정 엔티티 속성](/help/c-recommendations/c-products/custom-entity-attributes.md) | *다중 값 특성 구현*&#x200B;에서 *API 사용*&#x200B;에 코드 샘플이 추가되었습니다. |
| 3월 4일 | [프로필 속성](/help/c-target/c-visitor-profile/profile-parameters.md) | &quot;우수 사례&quot; 섹션의 광범위한 개정으로 전체 주제를 업데이트했습니다. |
| 2월 21일 | [릴리스 노트(현재)](/help/r-release-notes/release-notes.md) | 새로운 Adobe Experience Cloud 탐색에 대한 정보가 추가되었습니다. |
| 2월 20일 | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | `enabled` 설정에 대한 설명을 업데이트했습니다. 다음 설정에 대한 정보가 추가되었습니다.`pageLoadEnabled` 및 `viewsEnabled`. |
|  | [지역](/help/c-target/c-audiences/c-target-rules/geo.md) | `mboxOverride.browserIp`이(가) at.js 1에서 지원된다는 참고가 추가되었습니다.*x*&#x200B;에만 사용할 수 있습니다. |
|  | [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Target 팀에서 지원하는 at.js 버전을 설명하는 텍스트가 정리되었습니다. |
|  | [릴리스 노트](/help/r-release-notes/release-notes.md): 20.2.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 노트에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |

## Adobe Target Standard/Premium 20.1.1(2020년 2월 4일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 2월 4일 | [릴리스 노트](/help/r-release-notes/release-notes.md): 20.1.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 노트에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |
