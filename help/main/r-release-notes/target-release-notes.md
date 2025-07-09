---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스;조기 액세스
description: SDK, API, JavaScript 라이브러리를 포함하여 [!DNL Adobe Target]의 예정된 릴리스에 포함된 새로운 기능 및 개선, 수정 사항에 대해 알아봅니다.
title: 예정된 [!DNL Target] 릴리스에는 어떤 새로운 기능과 개선 사항이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: dd7ec2fe38ea5bb6d34bdbf44876c291b356fc17
workflow-type: tm+mt
source-wordcount: '1896'
ht-degree: 12%

---

# [!DNL Target] 릴리스 정보 (프리릴리스)

이 문서에는 SDK, API 및 JavaScript 라이브러리를 포함하여 예정된 [!DNL Adobe Target] 릴리스에 대한 프리릴리스 정보가 포함되어 있습니다.

**마지막 업데이트 날짜: 2025년 7월 9일**

>[!NOTE]
>
>* 릴리스 일자, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.
>
>* 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하세요.
>
>* 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

## [!DNL Target Standard/Premium] 25.7.1(2025년 7월 9일)

주로 복잡한 고객 맞춤화와 관련된 최근 문제가 확인되어 이 릴리스에는 다음 수정 사항 및 업데이트가 포함되어 있습니다.

**활동**

* [!UICONTROL Activity QA] URL에 불필요한 쿼리 매개 변수가 포함된 문제가 해결되었습니다. `at_preview_evaluate_as_true_audience_ids`. (TGT-52907)
* 미리보기 URL이 사용자가 명시적으로 입력한 대상 이외의 추가 대상을 잘못 포함하던 문제를 수정했습니다. QA 또는 미리 보기 링크를 생성할 때 지정된 대상만 적용되도록 이 동작이 수정되었습니다. (TGT-52912)
* 트래픽 할당을 설정하는 동안 [!UICONTROL Auto-Target]&#x200B;(AA)를 먼저 선택한 경우 사용자가 [!UICONTROL Auto-Allocate]&#x200B;(AT) 활동을 만들 수 없는 문제를 해결했습니다. 이 문제로 인해 백엔드 유효성 검사 오류가 발생하고 활동이 저장되지 않습니다. (TGT-53096)

**대상자**

* [!UICONTROL Approver] 역할을 가진 사용자가 활동 전용 대상 세분화를 추가하거나 저장할 수 없는 문제를 해결했습니다. 사용자에게 활동을 승인하고 관리할 권한이 충분함에도 불구하고 &quot;[editor]&quot; 권한이 필요함을 알리는 403 금지된 오류가 발생했습니다. (TGT-52984)
* [!UICONTROL Remove Audience Refinement] 옵션을 사용하여 활동별 대상을 제거하면 동일한 활동 내에서 다시 선택할 수 있도록 대상이 대상 목록에 더 이상 표시되지 않는 문제가 해결되었습니다. 이 비헤이비어는 사용자가 동일한 대상자를 처음부터 다시 만들지 않는 한 다시 추가하지 못하도록 했습니다. (TGT-52979)
* 활동이 저장되기 전이라도 위치에서 제거된 후 바로 UI에서 활동 전용 대상 세분화가 사라지는 문제를 해결했습니다. 이 동작은 예상 기능 및 도구 설명 지침과 모순됩니다. 이 지침에는 &quot;활동이 저장되면 이 라이브러리에서 사용되지 않은 모든 대상이 삭제됩니다.&quot;가 표시됩니다. (TGT-52982)
* [!UICONTROL All Visitors] 이외의 대상을 활동에 할당하려고 할 때 발생하는 문제를 해결했습니다. 저장하면 다음과 같은 오류 메시지가 표시됩니다. &quot;요청을 완료할 수 없습니다. 문제가 지속되면 [!UICONTROL Adobe Client Care]에 문의하십시오.&quot; (TGT-53008)
* 활동 편집기 내에서 새 대상을 만들고 할당한 후 활동 저장을 차단하는 문제를 해결했습니다. 표시되는 오류 메시지: &quot;요청을 완료할 수 없습니다. 문제가 지속되면 [!UICONTROL Adobe Client Care]에 문의하십시오.&quot; (TGT-52977)

**[!UICONTROL Analytics for Target](A4T)**

* 기존 활동을 복사하고 보고 소스를 [!DNL Adobe Analytics]&#x200B;(A4T)으로 변경하면 &quot;잘못된 사용자 입력&quot; 오류가 발생하는 문제를 해결했습니다. [!DNL Analytics], `restart_same_experience` 및 `restart_random_experience`과(와) 같이 `restart_new_experience` 보고와 호환되지 않는 특정 지표 작업이 원래 활동에서 유지된 경우 오류가 트리거되었습니다. (TGT-52900)
* [!DNL Adobe Analytics] 단계에서 [!UICONTROL Goals & Settings]&#x200B;(A4T)을(를) 보고 소스로 선택할 때 고객이 활동을 만들거나 저장할 수 없도록 하는 문제를 해결했습니다. 특히 [!UICONTROL Custom Event] 지표(예: &quot;사용자 지정 이벤트 16&quot;)를 선택할 때 문제가 발생하여 다음 오류가 발생했습니다. &quot;잘못된 사용자 입력&quot; (TGT-52910)
* &quot;[!UICONTROL View in Analytics]&quot; 링크를 클릭하면 의도한 [!DNL Analytics] 대시보드가 아닌 홈 페이지로 리디렉션되는 문제가 해결되었습니다. (TGT-53092 및 TGT-53093)
* 기존 활동을 복제하고 보고 소스를 [!DNL Target]에서 [!DNL Adobe Analytics]&#x200B;(으)로 변경할 때 사용자에게 &quot;400 - 잘못된 사용자 입력&quot; 오류가 발생하여 활동이 저장되지 않는 문제를 해결했습니다. (TGT-52875)
* [!DNL Recommendations]&#x200B;(A4T)을(를) 보고 소스로 선택하면 업데이트된 [!UICONTROL Overview] UI에서 [!UICONTROL Goals & Settings] 활동을 볼 때 [!DNL Adobe Analytics] 섹션이 로드되지 않는 문제를 해결했습니다. 다음 오류 메시지가 표시되었습니다. &quot;문제가 발생했습니다. 요청을 완료할 수 없습니다. 문제가 지속되면 Adobe 클라이언트 지원 센터에 문의하십시오.”라는 오류 메시지가 표시됩니다. (TGT-52999)

**[!UICONTROL Experiences]및[!UICONTROL Offers]**

* AP([!UICONTROL Manage Content]) 활동에서 [!UICONTROL Automated Personalization] 기능을 사용하면 페이지가 충돌하여 비어 있는 문제가 해결되었습니다. 이 문제는 특히 업데이트된 UI에서 만들거나 편집한 활동에서 콘텐츠 관리자에서 [!UICONTROL Done]을(를) 클릭한 후 발생했습니다. (TGT-53047)
* 모든 콘텐츠 옵션이 제거된 후 [!UICONTROL Manage Content] 기능이 위치 상태를 제대로 확인하지 못하는 문제를 해결했습니다. 이렇게 하면 활동 구성을 저장하거나 진행하려고 할 때 일관되지 않은 동작이나 오류가 발생할 수 있습니다. (TGT-52801)
* 새 페이지를 추가하고 다른 경험 내에서 특정 요소를 삭제할 때 사용자에게 &quot;잘못된 입력&quot; 오류가 발생하는 문제를 해결했습니다. 요소 조작 중, 특히 경험 간에 전환하고 공유 페이지 구조를 수정할 때 중복 `LocalIds`이(가) 발생하여 오류가 트리거되었습니다. (TGT-52720)
* [!UICONTROL Generate Adhoc Offer] 기능을 사용하면 정의되지 않은 위치가 [!UICONTROL Manage Content] 패널에 표시되는 문제가 해결되었습니다. (TGT-53076 및 TGT-53070)
* [!UICONTROL Targeting]에서 [!UICONTROL Experiences]&#x200B;(으)로 다시 이동할 때 HTML 오퍼를 사용하여 수정한 내용이 누락된 것으로 표시되는 고객의 동작을 명확히 했습니다. 이 고객의 경우 영향을 받는 웹 사이트에서 각 페이지 로드와 함께 변경된 여러 DOM 선택기를 동적으로 생성했습니다. 따라서 편집기를 다시 열 때 원래 수정에 사용된 선택기를 찾을 수 없으므로 수정 사항이 누락되거나 유효하지 않은 것으로 표시됩니다. 설계대로 작동합니다. 수정 사항이 편집기에서 시각적으로 지속되도록 하려면 클라이언트가 페이지 다시 로드 간에 변경되지 않는 안정적이고 일관된 선택기를 사용하는 것이 좋습니다. (TGT-52874)
* 제외된 경험의 일부인 오퍼를 삭제하거나 비활성화하려고 할 때 &quot;잘못된 사용자 입력&quot; 오류가 트리거되는 문제를 해결했습니다. 이 문제는 오퍼가 포함된 경험에서 활발하게 사용되지 않았음에도 불구하고 발생했습니다. (TGT-52917)

**양식 기반 경험 작성기**

* 경험을 복제하고 복제된 경험 중 하나에서 사용자 지정 코드를 편집하면 의도하지 않게 이러한 변경 사항이 모든 복제된 경험에 적용되는 양식 기반 활동의 문제를 해결했습니다. 이제 각 경험은 복제 후 독립적으로 자체 사용자 지정 코드를 유지합니다. (TGT-51600)

**로컬라이제이션**

* 문자열 &quot;Preview Experience&quot;에 대한 한국어 로케일(ko-KR)의 컨텍스트 번역 문제를 해결했습니다. (TGT-52928)
* 여러 텍스트 문자열의 중국어 간체(zh_CN) 변환에서 식별된 용어 불일치가 수정되었습니다. (TGT-52954 및 TGT-52955)

**[!DNL Recommendations]**

* 새 [!DNL Recommendations] 피드를 추가했습니다. [상태](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Partial Import Failed]. (KB-2215)
* [!DNL Recommendations]과(와) 함께 [!UICONTROL promotions]을(를) 추가할 때 활동 만들기 워크플로에 영향을 주는 문제를 해결했습니다. 사용자가 &quot;[!UICONTROL Promote by Attribute]&quot;을(를) 선택하고 필터링 규칙을 추가한 경우(예: [!UICONTROL Parameter Matching]) 활동을 저장하고 다시 편집한 후 선택한 규칙 유형 및 피연산자 값이 유지되지 않았습니다. 다시 열면 필터링 규칙 유형이 예기치 않게 변경되고 피연산자 값이 누락됩니다. (TGT-53059)
* 단일 규칙으로 만든 프로모션이 규칙의 논리에 관계없이 &quot;항목 목록&quot; 프로모션 유형으로 잘못 해석되어 표시되는 [!DNL Recommendations] UI의 문제가 해결되었습니다. (TGT-53063)
* 업데이트된 [!UICONTROL Overview]UI를 사용할 때 [!UICONTROL Download Recommendations Data]을(를) 포함하는 [!UICONTROL Experience Targeting]&#x200B;(XT) 활동에 대해 &quot;[!DNL Recommendations]&quot; 단추가 누락되는 문제를 해결했습니다. (TGT-52730 및 TGT-52756)
* 이전에는 피드에서 성공적으로 가져온 엔티티 수만 권장 사항 UI에 표시되었습니다. 그러나 백엔드 메시지 형식에는 가져온 엔티티 수와 형식의 총 엔티티 수가 모두 포함됩니다.

  `# of entities imported / # of total entities`

  이러한 불일치로 인해 사용자는 UI에서 첫 번째 값(가져온 개수)만 볼 수 있었고, 이로 인해 혼동이 발생했습니다. 이제 UI에 두 숫자가 모두 표시됩니다. (TGT-53073)

**보고서**

* [!UICONTROL Export order details to CSV] 페이지에서 &quot;[!UICONTROL Reports]&quot;을(를) 선택하면 다운로드되는 빈 파일이 발생하는 문제가 해결되었습니다. 이 문제는 활동에 유효한 주문 데이터가 있는 경우에도 발생했습니다. (TGT-52225)
* 새 보고 대상을 만들고 할당한 후 활동을 저장하려고 할 때 발생하는 문제를 해결했습니다. 반환된 오류 메시지: &quot;액세스 거부됨. 이 작업을 수행하려면 [editor] 권한이 모두 필요합니다.&quot; 이 문제는 사용자가 승인자 수준 액세스 권한을 가지고 있음에도 불구하고 발생했습니다. (TGT-53103)

**[!UICONTROL Visual Experience Composer](VEC)**

* 보기에 수정 사항을 적용하면 보기가 복제되고 활동이 &quot;잘못된 사용자 입력&quot; 오류를 반환하는 문제를 해결했습니다. 이 수정 사항은 중복 또는 유효성 검사 오류를 트리거하지 않고 보기 수정 사항이 올바르게 적용되도록 합니다. (TGT-52886)
* 사용자 지정 코드 수정 사항이 잘못된 경험에 대해 잘못 표시되던 문제를 수정했습니다. 구체적으로, 한 경험을 위해 의도된 변경 사항이 다른 경험에서 나타나, 라이브 활동의 혼란과 잠재적인 오구성을 초래했다. (TGT-52776)
* 새 VEC UI에서 사용자 지정 코드 수정 사항을 편집하거나 저장할 수 없는 문제를 해결했습니다. 특히:

   * 사용자 지정 코드 블록을 편집하고 저장한 후 변경 사항이 UI나 QA 미리 보기에 반영되지 않았습니다.
   * 경우에 따라 활동을 닫고 다시 열지 않으면 수정 사항을 삭제할 수 없습니다.
   * 해결 방법으로, 사용자는 코드를 복사하고 수정 사항을 삭제한 다음 업데이트된 콘텐츠로 수동으로 다시 만들어야 했습니다. (TGT-53072)

* 사용자 지정 코드를 편집하고 저장하면 [!UICONTROL Modifications] 패널이 응답하지 않는 문제를 해결했습니다. (TGT-53075)
* 변형 경험에서 사용자 지정 코드에 대한 수정 사항이 의도하지 않게 [!UICONTROL Control] 경험에 반영되던 문제를 수정했습니다. 이로 인해 게재 동작이 의도하지 않게 변경되었습니다. 이제 [!UICONTROL Control] 경험은 다른 경험에 대한 사용자 지정 코드 편집에서 격리된 상태로 유지됩니다. (TGT-52413)
* 편집기가 완전히 로드되기 전에 사용자가 두 번째 경험을 클릭한 경우 한 경험(예: 경험 B)에 대한 수정 사항이 의도하지 않게 다른 경험(경험 A)에 복제되는 문제가 해결되었습니다. 처음 선택한 경험에 변경 사항이 없는 경우 이 동작으로 인해 수정 사항이 손실될 수도 있습니다. (TGT-52597)
* 활동 만들기 [!UICONTROL Modifications] 단계의 변경 내용이 일관되게 저장되지 않던 문제를 수정했습니다. 경우에 따라 모든 단계를 완료하고 [!UICONTROL Save]을(를) 클릭하면 저장 프로세스 중에 표시되는 오류가 없더라도 [!UICONTROL Modifications] 섹션에 추가된 사용자 지정 스크립트가 라이브 사이트에서 반영되지 않습니다. (TGT-52661)
* 사용자 지정 코드 변경 사항이 올바르게 저장되지 않고 동일한 활동 내의 여러 경험에 의도하지 않게 미러링되는 문제가 수정되었습니다. 또한 특정 활동을 열거나 새로 고칠 때 액세스 문제가 발생하여 화면이 비어 있습니다. 이제 안정적인 활동 편집과 정확한 경험 격리를 위해 이러한 문제가 해결되었습니다. (TGT-52594)
* 사용자가 [!UICONTROL Browse Mode]에서 다른 URL을 탐색할 수 없는 문제를 해결했습니다. 이렇게 하면 테스터와 편집자가 동일한 활동 세션 내에서 대체 페이지를 확인하거나 미리 볼 수 없습니다. (TGT-53052)
* 활동을 만드는 동안 여러 [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 인스턴스가 동시에 열리는 문제를 해결했습니다. 이 문제는 사용자가 [!UICONTROL Enhanced Experience Composer]&#x200B;(EEC)을(를) 사용하지 않도록 설정하고 [!UICONTROL Page Delivery] 단계에서 웹 사이트 URL에서 슬래시를 제거할 때 발생했습니다. (TGT-52782)
* 사용자가 다른 지표를 선택한 후에도 [!UICONTROL Revenue] 단계의 [!UICONTROL Goals & Settings] 지표 드롭다운이 [!UICONTROL Revenue per Visit]&#x200B;(RPVISIT)으로 잘못 설정되던 문제를 수정했습니다.  지표 구성 패널을 축소하고 다시 확장하는 동안 문제가 발생하여 이전에 선택한 값이 재설정되었습니다. (TGT-52811 및 TGT-52878)
* [!UICONTROL Automated Personalization]&#x200B;(AP) 및 [!UICONTROL Multivariate Testing]&#x200B;(MVT) 활동의 오퍼 이름 지정 및 콘텐츠 변환과 관련된 활동 만들기 워크플로의 몇 가지 문제를 해결했습니다.

  해결된 주요 문제:

   * 이름이 같은 여러 HTML 오퍼를 만들면(예: &quot;경험&quot;) &quot;중복된 오퍼 이름은 허용되지 않습니다&quot; 오류가 발생했지만 UI에서 충돌을 일으키는 오퍼를 명확하게 표시하지 않았습니다.
   * 오른쪽 패널을 통해 오퍼의 이름을 바꾸면 UI에서 이름이 업데이트되었지만 변경 내용이 [!UICONTROL Manage Content] 탭 또는 [!UICONTROL Offers] 탭에 반영되지 않아 지속적인 유효성 검사 오류가 발생했습니다.
   * MVT 활동에서는 이름을 바꾼 후에도 중복 이름 오류가 지속되지 않지만 UI는 탭 간에 업데이트된 오퍼 이름을 일관되게 반영하지 못했습니다. (TGT-52933)

## 추가 릴리스 정보 및 버전 세부 정보

| 리소스 | 세부 사항 |
|--- |--- |
| [릴리스 노트: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Platform Web SDK의 각 버전 변경 내용에 대한 세부 사항입니다. |
| [at.js 버전 세부 사항](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | [!DNL Adobe Target] at.js JavaScript 라이브러리의 각 버전 변경 내용에 대한 세부 사항입니다. |

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

[!DNL Target] 및 기타 [!DNL Adobe Experience Cloud] 솔루션의 향후 제품 개선 사항에 대한 사전 알림을 받으려면 [!DNL Adobe Priority Product Update]에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
