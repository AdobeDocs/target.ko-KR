---
keywords: 개요 및 참조;webkit;쿠키;자사;타사;자사;타사;타사
description: 알아보기 [!DNL Target] 쿠키 동작(퍼스트 파티 쿠키, 퍼스트 파티 쿠키가 포함된 타사 쿠키 또는 타사 쿠키만).
title: 어디에서 정보를 찾을 수 있습니까 [!DNL Target] 쿠키?
feature: at.js
role: Developer
exl-id: 1c4e5b0b-8ae4-4526-aea0-318a33f4d247
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '1553'
ht-degree: 55%

---

# Target 쿠키

쿠키 동작은 퍼스트 파티 쿠키, 퍼스트 파티 쿠키가 포함된 타사 쿠키 또는 타사 쿠키만인지 여부에 따라 다릅니다.

>[!NOTE]
>
>이 주제에는 `mboxSession`과 `mboxPC`에 대한 정보가 포함되어 있습니다. 구현 우수 사례에 따라 쿠키 데이터를 사용하여 민감한 정보를 링크하거나 저장하지 않도록 권장합니다. `mboxSession` 또는 `mboxPC`.

참조 - [Target 쿠키 삭제](https://developer.adobe.com/target/before-implement/privacy/cookie-deleting/).

## 퍼스트 파티 또는 타사 쿠키를 사용하는 경우 {#section_F71B29420C004A7FA3B1921E619B326E}

사이트 설정에 따라 사용할 쿠키가 결정됩니다. 이렇게 하면 [!DNL Target] 는 자사 및 타사 쿠키를 이해하려고 할 때 작동합니다. 자세한 내용은 [방법 [!DNL Adobe Target] Works](/help/main/c-intro/how-target-works.md#concept_459AB4DEE7364A9290C2FD405DC29584) 추가 정보.

쿠키에 대한 주요 사용 사례로는 다음 세 가지가 있습니다.

1. 1개 도메인.

   모든 테스트가 하나의 최상위 도메인(`www.domain.com`, `store.domain.com`, `anysub.domain.com`등)

   접근 방법: 자사 쿠키(기본값)만 사용합니다.

1. 사용자가 도메인을 교차하며 이러한 도메인에서 사용자 행동을 추적하고 테스트하려고 합니다.

   예: 사용자가 쇼핑을 위해 사이트를 방문하지만 Yahoo 상점을 통해 체크아웃합니다. 세 가지 방법(계정 담당자에게 문의하여 최상의 방법 확인):

   * 퍼스트 파티 쿠키와 타사 쿠키를 활성화합니다.
   * 타사 쿠키만 활성화합니다(드문 경우이며 mbox 쿠키를 도메인 외부에 보관하는 이점이 있음).
   * 퍼스트 파티 쿠키만 활성화하고 도메인을 교차할 때 `mboxSession` 매개 변수를 전달합니다.

      다음 `mboxSession` 매개 변수를 랜딩 페이지로 전달하여 JavaScript 라이브러리(Adobe Experience Platform Web SDK 또는 at.js)에서 참조해야 합니다. 중간 리디렉터 페이지일 수 없습니다.

1. 타사 사이트에서 Adbox 또는 Flashbox만 사용합니다.

   두 가지 방법(계정 담당자와 협력하여 최상의 방법을 결정):

   * 퍼스트 파티 쿠키와 타사 쿠키를 활성화합니다.

      Flashbox 및 동적 크리에이티브를 사용하려면 퍼스트 파티 쿠키와 타사 쿠키가 필요합니다.

   * 타사 쿠키만 활성화합니다.

      이 방법은 AdBox 구현이 온사이트 타깃팅 없이 사용되는 드문 경우에만 적용됩니다.

## 퍼스트 파티 쿠키 동작 {#section_CE6313D979EA4D0897D2F661E7A8AFA7}

퍼스트 파티 쿠키는 [!DNL clientdomain.com]에 저장됩니다. 여기서 `clientdomain`은 사용자 도메인입니다.

JavaScript 라이브러리는 `mboxSession ID` 그리고 그걸 [!DNL Target] 쿠키 . 첫 번째 mbox 응답에는 오퍼와 오퍼를 저장할 JavaScript가 포함됩니다 `mboxPC ID` mbox 쿠키에 있는 애플리케이션에서 생성합니다.

>[!NOTE]
>
>[!DNL AMCV_###@AdobeOrg] 퍼스트 파티 쿠키는 항상 [!DNL Experience Cloud Visitor ID]를 사용하여 설정됩니다.

## 타사 쿠키 동작 {#section_4C3A83990BF8415BB1806602D84AED48}

타사 쿠키는 [!DNL clientcode.tt.omtrdc.net]에 저장되고 퍼스트 파티 쿠키는 [!DNL clientdomain.com]에 저장됩니다. 여기서 `clientdomain`은 사용자 도메인입니다.

JavaScript 라이브러리는 `mboxSession ID`. 첫 번째 위치 요청은 `mboxSession` 및 `mboxPC`라는 타사 쿠키를 설정하는 HTTP 응답 헤더를 반환하며 리디렉션 요청이 추가 매개 변수(`mboxXDomainCheck=true`)를 사용하여 다시 전송됩니다.

브라우저가 타사 쿠키를 수락하면 리디렉션 요청에 해당 쿠키가 포함되고 오퍼가 반환됩니다.

브라우저가 타사 쿠키를 거부하면 리디렉션 요청에 해당 쿠키가 포함되지 않고 페이지의 모든 위치에 대해 기본 컨텐츠가 표시됩니다. 설정된 쿠키가 없으므로 모든 페이지 요청에서 위와 동일한 프로세스가 다시 발생합니다.

>[!NOTE]
>
>[!DNL demdex.net] 쿠키는 타사 쿠키가 차단되지 않은 경우에 설정됩니다.

## 타사 및 퍼스트 파티 쿠키 동작 {#section_F0C9AD8BFDF8457A999C4A07A0F7A981}

타사 쿠키는 [!DNL clientcode.tt.omtrdc.net]에 저장되고 퍼스트 파티 쿠키는 [!DNL clientdomain.com]에 저장됩니다. 여기서 `clientdomain`은 사용자 도메인입니다.

JavaScript 라이브러리는 `mboxSession ID`. 첫 번째 위치 요청은 `mboxSession` 및 `mboxPC`라는 타사 쿠키를 설정하는 HTTP 응답 헤더를 반환하며 리디렉션 요청이 추가 매개 변수(`mboxXDomainCheck=true`)를 사용하여 다시 전송됩니다.

브라우저가 타사 쿠키를 수락하면 리디렉션 요청에 해당 쿠키가 포함되고 오퍼가 반환됩니다.

일부 브라우저는 타사 쿠키를 거부합니다. 타사 쿠키가 차단되는 경우에는 퍼스트 파티 쿠키가 계속 작동합니다. [!DNL Target]은 타사 쿠키 설정을 시도하며, 설정할 수 없을 경우 [!DNL Target]은 클라이언트의 특정 도메인에 대해서만 추적할 수 있습니다. 타사 쿠키가 차단되는 경우, `mboxSession` 도메인들을 연결하는 링크에 추가됩니다. 이 경우, 다른 퍼스트 파티 쿠키가 설정되고 이전 도메인의 퍼스트 파티 쿠키와 동기화됩니다.

## 쿠키 설정 {#section_B498B8D1A34A444BBF84CC720EE9D87F}

 쿠키에는 여러 가지 기본 설정이 있습니다. 필요한 경우 쿠키 지속 시간을 제외하고 이러한 설정을 변경할 수 있습니다. 쿠키 설정을 변경하는 경우 계정 담당자에게 문의하십시오.

| 설정 | 정보 |
|--- |--- |
| 쿠키 이름 | mbox. |
| 쿠키 도메인 | 컨텐츠를 제공하는 도메인의 두 번째 및 최상위 수준입니다. 회사 도메인에서 제공되기 때문에 쿠키는 자사 쿠키입니다.<br>예: `mycompany.com`. |
| 서버 도메인 | `clientcode.tt.omtrdc.net`( 계정에 대해 클라이언트 코드 사용) |
| 쿠키 지속 시간 | 쿠키는 마지막 로그인부터 2주 후에 방문자의 브라우저에 유지됩니다. 쿠키 지속 시간은 변경할 수 없습니다. |
| P3P 정책 | 쿠키는 대부분의 브라우저에서 기본 설정으로 요구되는 P3P 정책을 사용하여 게시됩니다. P3P 정책은 쿠키를 제공하는 브라우저와 해당 정보가 사용되는 방식을 나타냅니다. |

쿠키는 방문자가 캠페인을 경험하는 방식을 관리하기 위해 다양한 값을 유지합니다.

| 값 | 정의 |
|--- |--- |
| session ID | 사용자 세션의 고유 ID입니다. 기본적으로 이 ID는 30분 동안 지속됩니다. |
| pc ID | 방문자 브라우저의 반영구 ID입니다. 14일 동안 지속됩니다. |
| check | 방문자가 쿠키를 지원하는지 여부를 확인하는 간단한 테스트 값입니다. 방문자가 페이지를 요청할 때마다 설정합니다. |
| disable | 방문자의 로드 시간이 JavaScript 라이브러리 파일에 구성된 시간을 초과하는 경우 설정됩니다. 기본적으로 이 값은 1시간 동안 지속됩니다. |

## 영향 [!DNL Target] Apple WebKit 추적 변경 사항으로 인한 Safari 방문자용 {#section_2A2E5730ED7D4A0985C904AFEA310AAE}

**어떻게 [!DNL Adobe Target] 추적 작업?**

| 쿠키 | 세부 사항 |
|--- |--- |
| 퍼스트 파티 도메인 | 에 대한 표준 구현 [!DNL Target] 고객. &quot;mbox&quot; 쿠키가 고객의 도메인에 설정되어 있습니다. |
| 타사 추적 | 타사 추적은 의 광고 및 타깃팅 사용 사례에 중요합니다 [!DNL Target] 및 [!DNL Adobe Audience Manager] (AAM). 타사 추적을 사용하려면 교차 사이트 스크립팅 기술이 필요합니다. [!DNL Target] 에서는 mboxSession과 mboxPC, 이 두 개의 쿠키를 사용합니다. `clientcode.tt.omtrd.net` 도메인. |
**Apple은 어떻게 접근하고 있습니까?**

Apple의 메시지:

&quot;Intelligent Tracking Prevention(지능형 추적 방지)는 쿠키 및 기타 웹 사이트 데이터를 추가로 제한하여 교차 사이트 추적을 줄이는 새로운 WebKit 기능입니다.&quot;

&quot;이것이 교차 사이트 추적이라는 것이며, `example-tracker.com`이 사용한 쿠키는 타사 쿠키라고 합니다. 테스트에서 저희는 70개가 넘는 추적기가 있는 인기 웹 사이트를 찾았는데 이 사이트들은 모두 사용자에 대한 데이터를 자동으로 수집하고 있습니다.&quot;

| 접근 방식 | 세부 사항 |
|--- |--- |
| Intelligent tracking prevention(지능형 추적 방지) | 자세한 내용은 WebKit Open Source Web Browser Engine 웹 사이트에서 [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention/)을 참조하십시오. |
| 쿠키 | Safari의 쿠키 처리 방법:<ul><li>사용자가 직접 액세스하는 도메인에 없는 타사 쿠키는 저장되지 않습니다. 이 동작은 새로운 동작이 아닙니다. 타사 쿠키는 이미 Safari에서 지원되지 않습니다.</li><li>사용자가 직접 액세스하는 도메인에 설정된 타사 쿠키는 24시간 후에 삭제됩니다.</li><li>해당 퍼스트 파티 도메인이 여러 사이트에서 사용자를 추적하는 것으로 분류된 경우 30일 후에 퍼스트 파티 쿠키가 삭제됩니다. 이 문제는 다양한 도메인에 온라인으로 사용자를 보내는 대형 회사에 적용될 수 있습니다. Apple은 이러한 도메인이 어떻게 분류되는지 또는 도메인이 사이트 간에 사용자를 추적하는 것으로 분류되었는지 확인하는 방법에 대해서는 명확히 밝히지 않았습니다.</li></ul> |
| 여러 사이트에 걸친 도메인을 식별하는 기계 학습 | Apple의 메시지:<br>기계 학습 분류기: 기계 학습 모델은 수집된 통계 수치를 기반으로 사이트 간 사용자를 추적할 수 있는 최상위 민간 제어 도메인을 분류하는 데 사용됩니다. 수집된 다양한 통계 수치 중, 고유 도메인의 하위 리소스 할당 번호, 고유 도메인의 하위 프레임 할당 번호, 리디렉션되는 고유 도메인의 번호, 이렇게 세 개의 벡터가 현재 추적 사례를 기반으로 분류에 대한 강력한 신호를 갖고 있는 것으로 드러났습니다. 모든 데이터 수집 및 분류는 장치를 통해 이루어집니다.<br>그러나 사용자가 `example.com` 종종 퍼스트 파티 도메인이라고도 하는 최상위 도메인으로서, Intelligent Tracking Prevention은 사용자가 웹 사이트에 관심이 있다는 신호로 간주하고 이 타임라인에 묘사된 대로 동작을 일시적으로 조절합니다.<br>사용자가 `example.com` 지난 24시간 동안 쿠키를 사용할 수 있는 경우 `example.com` 는 제3자입니다. 이 연습에서는 &quot;Y에서 내 X 계정으로 로그인&quot;하는 로그인 상황을 감안합니다.<ul><li>최상위 도메인으로 방문하는 도메인은 영향을 받지 않습니다. 예를 들어 OKTA와 같은 사이트</li><li>여러 고유 도메인에서 현재 페이지의 하위 도메인이나 하위 프레임인 도메인을 식별합니다.</li></ul> |

**Adobe은 어떤 영향을 받습니까?**

| 영향을 받는 기능 | 세부 사항 |
|--- |--- |
| 옵트아웃 지원 | Apple의 WebKit 변경 사항 추적에서는 옵트아웃 지원을 중단합니다.<br>[!DNL Target] 옵트아웃은 `clientcode.tt.omtrdc.net` 도메인의 쿠키를 사용합니다. 자세한 내용은.[개인 정보 보호](https://developer.adobe.com/target/before-implement/privacy/privacy/)를 참조하십시오.<br>[!DNL Target] 에서는 두 개의 옵트아웃을 지원합니다.<ul><li>클라이언트당 하나(클라이언트는 옵트아웃 링크를 관리합니다.)</li><li>1개 [!DNL Adobe] 이 옵션을 선택하면 사용자가 모든 작업 중에서 선택 취소됩니다 [!DNL Target] 모든 고객을 위한 기능입니다.</li></ul>두 방법 모두 타사 쿠키를 사용합니다. |
| [!DNL Target] 활동 | 고객은 자신의 [프로필 라이프타임 길이](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md) 그들의 [!DNL Target] 계정(최대 90일). 문제는 계정의 프로필 라이프타임이 30일보다 길고, 고객의 도메인이 사이트 간에 사용자를 추적하는 것으로 표시되었기 때문에 퍼스트 파티 쿠키가 삭제되는 경우 Safari 방문자에 대한 동작이 의 다음 영역에서 영향을 받는다는 것입니다 [!DNL Target]:<br>**[!DNL Target] 보고서&#x200B;**: Safari 사용자가 활동에 들어갔다가 30일 후에 재방문한 다음 전환하는 경우 해당 사용자는 2명의 방문자와 하나의 전환으로 계산됩니다.<br>이 동작은 [!DNL Analytics] 를 보고 소스로 사용(A4T)합니다.<br>**&#x200B;프로필 및 활동 멤버십&#x200B;**:<ul><li>퍼스트 파티 쿠키가 만료되면 프로필 데이터가 지워집니다.</li><li>퍼스트 파티 쿠키가 만료되면 활동 멤버십이 지워집니다.</li><li> [!DNL Target] 타사 쿠키 구현을 사용하거나 퍼스트 파티 쿠키와 타사 쿠키 구현을 사용을 사용하는 계정의 경우 Safari에서 작동하지 않습니다. 이 동작은 새로운 동작이 아닙니다. Safari는 잠시 동안 타사 쿠키를 허용하지 않습니다.</li></ul><br>**추천**: 고객 도메인이 세션 간 방문자를 추적하는 도메인으로 표시될 수 있다는 걱정이 있다면, 에서 프로필 라이프타임을 30일 이하로 설정하는 것이 가장 안전합니다 [!DNL Target]. 이 제한은 사용자가 Safari 및 기타 모든 브라우저에서 유사하게 추적되도록 합니다. |
