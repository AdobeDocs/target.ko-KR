---
keywords: target 설명서 변경 로그;설명서 업데이트;새 주제;편집;업데이트;업데이트
description: Adobe [!DNL Target] 제품 설명서에 대한 중요한 추가 사항 및 변경 사항을 항상 최신 상태로 두십시오.
title: Target의 설명서 업데이트는 어디에서 볼 수 있습니까?
feature: 릴리스 정보
exl-id: 36d19598-eb46-4be6-a652-658b653287cb
translation-type: tm+mt
source-git-commit: a69737f49a52cde703627f91d4b97609c1796ee6
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 60%

---

# 설명서 변경 내용

이 페이지에는 [!DNL Adobe Target] 제품 설명서의 중요 변경 사항이 기재되어 있습니다.

## Adobe [!DNL Target] Standard/Premium 21.4.1(2021년 4월 19일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 5월 10일 | [권장 사항 FAQ](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | 다음과 같은 FAQ가 추가되었습니다.&quot;[!DNL Recommendations Premium]의 [!DNL Adobe Recommendations Classic]에서 만든 알고리즘을 사용할 수 있습니까?&quot; |
|  | [구현 [!DNL Target] using [!DNL Dynamic Tag Manager] (DTM)](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md) | [!DNL Adobe Dynamic Tag Manager]은(는) 더 이상 지원되지 않음을 나타냅니다. 대신 [!DNL Adobe]은 [[!DNL Adobe Experience Platform Launch]](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)로 구현하는 것이 좋습니다. |
| 5월 6일 | [권장 사항 FAQ](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | 다음과 같은 FAQ가 추가되었습니다.<ul><li>내 사이트에 반영될 [!UICONTROL Recommendations] 활동, 오퍼, 프로모션 또는 기준 설정의 구성을 변경하는 데 얼마나 걸립니까?</li><li>사용자가 받는 권장 사항 *에 제품 A를 클릭하고 제품 B를 구입하는 등의 사용자 행동이 반영되는 데 얼마나 걸립니까?*</li><li>사용자 행동(예: 제품 A 클릭 및 제품 B 구입)이 권장 사항 *기타* 사용자가 받는 경우 얼마나 걸립니까?</li></ul> |
|  | [디바이스에서 의사 결정](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md) | Adobe 기술 블로그에서 다음 블로그 게시물에 링크를 추가했습니다.<ul><li>1부:에지 플랫폼에서 실험 및 개인화를 위해 Adobe Target NodeJS SDK 실행(Akamai Edge Workers)</li></ul> |
| 5월 5일 | [Target 알림 및 이벤트](/help/r-release-notes/target-announcements.md) | 2021년 5월 12일 수요일 오전 8시에 열리는 Adobe Target 커뮤니티 Q&amp;A 커피 휴대에 대한 정보가 추가되었습니다.(GMT-7). |
| 4월 27일 | [쿠키 설정](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-cookies.md) | 쿠키 지속 시간(`deviceIdLifetime` 설정)이 at.js 버전 2.3.1 이상에서 오버라이드됨을 나타내는 항목을 업데이트했습니다. |
|  | [Adobe Target 가이드](/help/target-home.md) | Adobe Summit에 대한 정보가 추가되었습니다. |
| 4월 26일 | [at.js에 대한 장치 내 의사 결정 문제 해결](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/troubleshooting-on-device-decisioning.md) | 새 주제입니다. |
| 4월 19일 | [디바이스에서 의사 결정](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) | 다음과 같은 새 아티클이 추가되었습니다.<ul><li>[디바이스에서 의사 결정](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md)</li><li>[장치 내 의사 결정을 위한 지원 기능](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md)</li><li>[장치 내 의사 결정 규칙 아티팩트](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md)</li></ul> |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#on-device-decisioning) | `decisioningMethod`에 대한 정보가 추가되었습니다. |
|  | [adobe.target.getOffers() - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | 다음을 추가했습니다.<ul><li>`decisioningMethod` 키에 대한 정보입니다.</li><li>&quot;getCallOffers()가 장치에서 의사 결정을 내리는 예&quot;입니다.</li></ul> |
|  | [at.js 사용자 지정 이벤트](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) | 다음과 같은 정보가 추가되었습니다.<ul><li>장치 내 의사 결정 아티팩트에 성공했습니다.</li><li>장치 내 의사 결정 아티팩트에 실패했습니다.</li></ul> |
|  | [활동](/help/c-activities/activities.md) | 장치 내 의사 결정에 대한 정보가 추가되었습니다. |
|  | [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | at.js 2.5.0에 대한 정보가 추가되었습니다. |
|  | [태그 관리자 없이 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md) | 장치 내 의사 결정에 대한 정보가 추가되었습니다. |
|  | [활동 QA](/help/c-activities/c-activity-qa/activity-qa.md) | [!UICONTROL Automated Personalization] 활동에 대한 미리 보기 링크 지원이 [at.js 2.5.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)와 함께 추가되었습니다. |
|  | [동적 및 정적 포함 규칙 사용](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators) | 다음 새 연산자에 대한 정보가 추가되었습니다.<ul><li>목록에 포함</li><li> 목록에 포함되지 않음</li><li>목록에</li><li>목록에</li><li>목록에</li><li>목록에</li></ul> |
|  | [Adobe Target 쿠키](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html)<br>(*Experience Cloud 서비스 및* 관리 가이드) | &quot;세션 ID&quot;에 대한 추가 정보가 추가되었습니다. |
|  | [릴리스 정보](/help/r-release-notes/release-notes.md): 21.4.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 정보에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |

## Adobe [!DNL Target] Standard/Premium 21.2.1(2021년 3월 9일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 4월 9일 | [Target 릴리스 정보(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | at.js 버전 2.5.0 릴리스(2021년 4월 19일)에 대한 베타 버전 정보가 추가되었습니다. |
| 4월 9일 | [Target 릴리스 정보(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | Target Standard/Premium 21.4.1 릴리스에 대한 프리릴리스 정보 추가(2021년 4월 19일) |
|  | [이메일에 권장 사항 통합](/help/c-recommendations/c-recommendations-faq/integrating-recs-email.md) | 옵션 1 및 2에 대한 용량 지침을 설명하는 참고가 추가되었습니다. |
| 3월 29일 | [권장 사항 FAQ](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md#persist-across-devices) | 추가된 새 FAQ:<ul><li>한 명의 방문자에 대해 최근에 본 항목을 기반으로 한 권장 사항이 여러 장치에서 지속됩니까?</li></ul> |
| 3월 23일 | [릴리스 노트](/help/r-release-notes/release-notes.md) | at.js 버전 2.4.1에 대한 릴리스 노트가 추가되었습니다. |
|  | [at.js 버전 세부 사항](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | at.js 버전 2.4.1에 대한 릴리스 노트가 추가되었습니다. |
|  | [권장 사항 FAQ](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | 다음 FAQ가 업데이트되었습니다.<ul><li>내 카탈로그에 있는 항목에 대한 업데이트를 내 사이트에 반영하는 데 얼마나 걸립니까?</li></ul> |
| 3월 22일 | [권장 사항 피드 처리 서버에서 사용하는 IP 주소](/help/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md) | IP 주소 목록이 업데이트되었습니다. |
|  | [제한](/help/r-troubleshooting-target/target-limits.md) | &quot;엔티티&quot; 아래의 &quot;엔티티 수&quot; 섹션을 업데이트했습니다. |
|  | [지역](/help/c-target/c-audiences/c-target-rules/geo.md) | at.js 2에 대한 정보가 추가되었습니다.*&quot;다른 위치에서 온 사용자로 내 활동을 테스트하려면 어떻게 합니까?&quot;를* 참조하십시오. |
|  | [릴리스 정보](/help/r-release-notes/release-notes.md): 21.2.1 | 다음 섹션이 추가되었습니다. <ul><li>Recommendations 피드 처리 서버의 IP 주소 변경 사항(2021년 3월 16일)</li></ul> |
| 3월 19일 | [보고서 보기 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#deactivated) | 다음 FAQ가 추가되었습니다.<ul><li>활동이 비활성화된 후에도 더 많은 노출 횟수를 계속 볼 수 있는 이유는 무엇입니까?</li></ul> |
| 3월 12일 | [자동 할당 및 자동 타겟 활동에 대한 A4T 지원](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md#tutorial) | 다음 새 튜토리얼이 추가되었습니다.<ul><li>자동 타겟 활동을 위한 Analysis Workspace에서 A4T 보고서를 설정하는 방법</li></ul> |
| 3월 9일 | [제한](/help/r-troubleshooting-target/target-limits.md#offer-size) | <ul><li>허용 가능한 오퍼 크기 제한을 업데이트했습니다.</li><li>categoryId 매개 변수에 대한 문자 제한을 수정했습니다.</li></ul> |
|  | [Target 에지 노드를 허용 목록에 추가](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md) | [!DNL Target] 에지 IP 주소를 업데이트했습니다. |
|  | [엔티티 속성](/help/c-recommendations/c-products/entity-attributes.md) | entity.value가 십진수 형식이어야 함을 나타내는 텍스트를 추가했습니다(예: 15,99가 아니라 15.99). |
|  | [릴리스 정보](/help/r-release-notes/release-notes.md): 21.2.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 정보에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |

## Adobe [!DNL Target] Standard/Premium 21.1.1(2021년 1월 19일)

| 날짜 | 주제 | 변경 사항 |
| --- | --- | --- |
| 2월 22일 | [보고서 보기 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | 다음 FAQ가 업데이트되었습니다.<ul><li>Analysis Workspace에서 세그먼트를 적용할 수 있는 위치는 어디입니까?</li></ul> |
| 2월 16일 | [Target 릴리스 정보(사전 릴리스)](/help/r-release-notes/target-release-notes.md) | 사전 릴리스 정보에서 오퍼 제한 크기에 대한 텍스트가 업데이트되었습니다. |
| 2월 11일 | [Target 작동 방식](/help/c-intro/how-target-works.md) | &quot;봇&quot; 섹션이 업데이트되었습니다. |
| 2월 10일 | [Target 알림 및 이벤트](/help/r-release-notes/target-announcements.md) | 2021년 2월 24일 수요일에 Adobe Target Community Q&amp;A Coffee Break에 대한 정보가 추가되었습니다. |
| 2월 8일 | [타겟 모바일 미리보기](/help/c-target-mobile-app/target-mobile-preview.md) | Adobe Mobile SDK 버전 4의 AndroidManifest.xml 파일에 추가해야 하는 코드 스니펫을 추가했습니다. |
|  | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md) | 다음 알려진 문제를 명확히 설명했습니다.<ul><li>API를 통해 생성된 컬렉션, 제외, 기준 및 디자인은 Target 사용자 인터페이스에 표시되지 않으며 API를 통해서만 편집할 수 있습니다. 마찬가지로, Target UI에서 이러한 항목을 생성한 후 나중에 API를 통해 편집하면 이러한 변경 내용이 Target UI에 반영되지 않습니다. API를 통해 편집된 항목은 API를 통해 계속 편집되어야 수정 사항이 손실되지 않습니다.</li></ul> |
| 2월 1일 | [자동화된 개인화 요약 보고서](/help/c-reports/reports-ap.md) | 새로운 섹션: &quot;자주 묻는 질문(FAQ)&quot;이 추가되었습니다. |
| 1월 27일 | [리디렉션 오퍼 만들기](/help/c-experiences/c-manage-content/offer-redirect.md) | 주제가 업데이트됨. |
|  | [원격 오퍼 만들기](/help/c-experiences/c-manage-content/about-remote-offers.md) | 주제가 업데이트됨. |
| 1월 26일 | [전환율](/help/c-reports/conversion-rate.md) | Target이 학생의 t-테스트에서 &quot;제곱 합&quot;을 사용하는 방법을 명확히 설명했습니다. |
| 1월 22일 | [전환율](/help/c-reports/conversion-rate.md#t-test) | 다음 섹션 추가: &quot;Target이 학생의 t-테스트 사용을 권장하는 이유는 무엇입니까?&quot; |
| 1월 21일 | [Analytics 및 Target 통합 문제 해결(A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md) | 새 섹션 추가: &quot;A4T 활동 보고서에는 &quot;지정되지 않은&quot; 이벤트가 많은 행이 포함됩니다.&quot; |
|  | [보고서 보기 - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | 다음 섹션 업데이트: &quot;Analytics 보고서에 &quot;지정되지 않음&quot;이 표시되는 이유는 무엇입니까? 어떤 의미입니까?&quot; |
| 1월 20일 | [Adobe Experience Platform 웹 SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) | 새 주제입니다. |
| 1월 19일 | [Target 릴리스 정보 (현재)](/help/r-release-notes/release-notes.md) | Target 21.1.1 릴리스(2021년 1월 19일)에 대한 정보가 추가되었습니다. |
|  | [제한](/help/r-troubleshooting-target/target-limits.md) | `productPurchasedID` 매개 변수에 대한 텍스트가 업데이트되었습니다. |
|  | [알려진 문제 및 해결된 문제](/help/r-release-notes/known-issues-resolved-issues.md) | 활성 프로모션을 사용하여 [!UICONTROL 권장 사항] 활동을 복사할 때 알려진 문제가 추가되었습니다. 중복 활동의 변경 사항은 원래 활동에도 영향을 미치며, 그 반대의 경우도 마찬가지입니다. 임시 해결 방법이 포함되었습니다. |
|  | [릴리스 정보](/help/r-release-notes/release-notes.md): 21.1.1 | 이 릴리스에는 개선 사항 및 수정 사항이 포함되어 있습니다. 릴리스 정보에서 해당 사항을 읽어보고 링크를 클릭하여 설명서를 확인할 수 있습니다. 또한 이 릴리스에는 도움말 전체의 여러 문서 업데이트 내용도 포함되어 있습니다. |
