---
description: 페이지에 예상되는 컨텐츠가 표시되지 않으면 몇 가지 단계를 진행하여 컨텐츠 제공을 디버깅할 수 있습니다.
keywords: mbox 디버그;mbox 문제 해결;mbox 문제;깜박임;mboxDebug;mboxTrace;토큰;디버거;우선순위;활동 우선순위;Adobe Experience Cloud Debugger;orderConfirmPage mbox;SiteCatalyst 구매 mbox;최상위 판매;최상위 판매자
seo-description: 페이지에 예상되는 컨텐츠가 표시되지 않으면 몇 가지 단계를 진행하여 컨텐츠 제공을 디버깅할 수 있습니다.
seo-title: 컨텐츠 전달 문제 해결
solution: Target
subtopic: 다변량 테스트
title: 컨텐츠 전달 문제 해결
topic: Standard
uuid: 8837d07a-f793-495e-a6c1-b9c35fbe18b1
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# 컨텐츠 전달 문제 해결{#troubleshoot-content-delivery}

페이지에 예상되는 컨텐츠가 표시되지 않으면 몇 가지 단계를 진행하여 컨텐츠 제공을 디버깅할 수 있습니다.

* 활동 또는 캠페인 코드를 주의깊게 확인합니다. 입력 또는 기타 오류로 인해 예상 컨텐츠가 표시되지 않을 수 있습니다.
* mboxTrace 또는 mboxDebug를 사용하여 mbox 문제를 해결합니다.
* mbox의 문제를 해결하려면, mboxDebug와 거의 동일한 정보를 제공하고 사용하기 쉬운 도구인 Adobe Experience Cloud Debugger를 사용하십시오.

mboxDebug는 mbox가 실행되고 쿠키가 설정되는지 확인하도록 페이지에서 Target을 설정하는 경우에 특히 유용합니다. 그러나 컨텐츠 전달을 디버깅할 때 유용한 세부 정보로 이동하지는 않습니다. 사용자 활동이 페이지에 나타나지 않거나 원치 않는 컨텐츠가 나타나면 mboxTrace를 사용하여 페이지를 자세히 검사하고 디버깅하십시오.

## 디버깅 도구에 사용할 인증 토큰 검색 {#section_BED130298E794D1FA229DB7C3358BA54}

mboxTrace 및 mboxDebug는 캠페인 데이터 및 프로필 데이터를 외부 당사자에게 노출할 수 있으므로 인증 토큰이 필요합니다. 인증 토큰은 [!DNL Target] UI에서 검색할 수 있습니다. 토큰은 6시간 동안 유효합니다.

인증 토큰을 검색하려면 다음을 수행하십시오.

1. **[!UICONTROL 설정]** &gt; **[!UICONTROL 구현]**&#x200B;을 클릭합니다.
1. **[!UICONTROL mbox.js]** 또는 **[!UICONTROL at.js]**&#x200B;를 선택합니다.
1. **[!UICONTROL 인증 토큰 생성을 클릭합니다]**.

   ![인증 토큰 생성](/help/c-activities/c-troubleshooting-activities/assets/generate-auth-token.png)

1. 생성된 토큰을 URL에 매개 변수로 추가하여 고급 디버깅 도구 중 하나를 활성화합니다.

   ![인증 토큰](/help/c-activities/c-troubleshooting-activities/assets/gen-auth-token.png)

## mboxTrace {#section_256FCF7C14BB435BA2C68049EF0BA99E}

mboxTrace를 사용하여 mbox 회신에 첨부된 추적 정보를 수신할 수 있습니다. 추적 정보는 mbox 호출의 결과(예: 대화 또는 노출) 및 이 특정 결과가 발생한 이유를 확인하는 데 도움이 되는 추가 데이터(예: 캠페인에서 해당 선택 영역이 포함되는 사용 가능한 분기 세트)를 반영합니다. 이 정보를 사용하여 컨텐츠 전달을 디버깅하십시오.

다음 매개 변수를 사용할 수 있습니다.

| mboxTrace 옵션 | 결과 |
|--- |--- |
| `?mboxTrace=console` | 콘솔 로그에 개체로 출력합니다.<br>at.js의 경우 mbox.js의 경우처럼 새 브라우저 창을 팝업하거나 콘솔에 출력하지 않고, 네트워크 요청을 조사한 후 Preview(Chrome) 또는 Response(Firefox)에서 확인해야 합니다. |
| `?mboxTrace=json` | 콘솔 로그에 리터럴 JSON 문자열로 출력합니다. |
| `?mboxTrace=window` | 팝업 창에 JSON 문자열로 출력합니다. |
| `?mboxTrace=disable` | 추적 세션 모드를 해제합니다. |

**mboxTrace 호출 예**

`https://www.mysite.com/page.html?mboxTrace=window&authorization=f543abf-0111-4061-9619-d41d665c59a6`

출력에는 컨텐츠에 대한 아주 자세한 정보가 표시됩니다. mboxTrace는 캠페인이나 활동 및 프로필에 대한 세부 정보를 표시합니다. 또한 실행 전에 프로필 스냅숏과 실행 후 변경된 사항에 대한 스냅숏도 제공합니다. 그뿐 아니라 각 위치에 대해 평가된 캠페인 또는 활동도 표시합니다.

일부 정보에는 일치하거나 일치하지 않는 세그먼트 및 타겟 ID가 포함됩니다.

* **SegmentId**: 재사용 가능한 세그먼트 라이브러리 또는 특정 캠페인에 대해 생성된 익명 세그먼트의 세그먼트 ID입니다.
* **TargetId**: 타겟 표현식 라이브러리 또는 캠페인의 세그먼트에 대한 익명 타겟의 타겟 ID입니다.
* **Unmatched**: 요청이 이 호출에서 해당 세그먼트 또는 타겟에 자격을 부여하지 않았습니다.
* **Matched**: 요청이 지정된 세그먼트 또는 타겟에 자격을 부여했습니다.

**권장 사항 페이지에서 mboxTrace 사용**: 권장 사항이 있는 페이지에 mboxTrace를 쿼리 매개 변수로 추가하면 페이지의 권장 사항 디자인이 mboxTrace 세부 정보 창으로 바뀝니다. 이 창에는 다음을 비롯하여 권장 사항에 대한 자세한 정보가 표시됩니다.

* 반환된 권장 사항 및 요청된 권장 사항
* 사용된 키 및 권장 사항을 생성하는지 여부
* 조건에 따라 생성된 권장 사항 및 백업 권장 사항
* 조건 구성
* 적용되는 제외 및 포함
* 컬렉션 규칙

쿼리 매개 변수에 `=console`, `=json` 또는 `=window`는 포함할 필요가 없습니다. mboxTrace 세부 정보를 다 지정했으면 `=disable`을 추가하고 **[!UICONTROL Enter]** 키를 눌러 일반 표시 모드로 돌아갑니다.

사이트의 일반적인 기능 및 모양은 mboxTrace의 영향을 받지 않습니다. 방문자는 일반 권장 사항 디자인을 보게 됩니다.

## mboxDebug {#section_DC92A0E4388A4A2787365AD9D556FEFA}

mboxDebug를 사용하려면 URL 끝에 mboxDebug 매개 변수를 추가합니다. 다음 표에서는 mbox와 관련 있는 URL 매개 변수에 대한 정보를 보여줍니다.

>[!NOTE]
>
>일부 mboxDebug 매개 변수는 인증이 있거나 없는 상태로 사용할 수 있습니다.

| URL 매개 변수 | 목적 |
|--- |--- |
| `mboxDebug=1` | 디버거<br>이 매개 변수를 mbox가 정의된 URL에 추가하면 중요한 디버깅 세부 정보가 있는 팝업 창이 열립니다. 쿠키 정보, PCid 및 세션 ID 값이 작성되고 모든 mbox URL이 표시됩니다. mbox URL을 클릭하여 해당 mbox에 대한 응답을 표시합니다. 자세한 내용은 [mbox_debug.pdf](/help/assets/mbox_debug.pdf)에서 볼 수 있습니다. |
| `mboxDebug=x-cookie` |  쿠키 수정 |
| `mboxDisable=1` | 페이지에서 mbox 비활성화 |
| `mboxDebug=x-profile` | 프로필 세트 보기 |
| `mboxDebug=x-time` | 각 mbox 요청에 대한 응답 표시 |
| `mboxOverride.browserIp=<Insert IP address>` | 지리 기반의 타깃팅 테스트<br>이 URL 매개 변수로 지리 기반의 타깃팅을 테스트합니다. IP 주소를 이 속성의 값으로 입력하면 Test&amp;Target의 지리 기반의 타깃팅은 캠페인에 설정된 지리 기반의 타깃팅 또는 세그먼테이션 세트에 대해 해당 IP 주소가 일치하는지 평가합니다. |

## Adobe Experience Cloud Debugger {#section_A2798ED3A431409690A4BE08A1BFCF17}

Adobe Experience Cloud Debugger를 사용하면 쉽고 빠르게 대상 구현을 이해할 수 있습니다. 라이브러리 구성을 빠르게 보고, 요청을 검토하여 사용자 지정 매개 변수가 올바르게 전달되고 있는지 확인한 다음, 콘솔 로깅을 켜고, Target 요청을 모두 비활성화할 수 있습니다. Experience Cloud를 인증하면 강력한 Mbox 추적 도구를 사용하여 활동 및 대상 자격과 방문자 프로필을 검사할 수 있습니다.

자세한 내용은 아래 교육 비디오를 참조하십시오.

자세한 내용은 [*Adobe Experience Cloud Debugger Extension* 설명서](https://marketing.adobe.com/resources/help/en_US/experience-cloud-debugger/)를 참조하십시오.

## 전달 중 target.js가 로드되지 않는 경우 {#section_ABBA5EFDFFB749D8BEE172DB1F973058}

전달 중에 target.js가 로드되지 않으면 Mbox.js에서는 방문자에게 "em-disabled"라는 쿠키를 보냅니다. 이 쿠키는 Visual Experience Composer를 사용하여 만든 오퍼가 사이트에서 렌더링되지 못하게 합니다. 이 쿠키가 있는 방문자는 테스트 컨텐츠를 보지 못하고 해당 활동 보고서에서 카운트되지도 않습니다. 다른 모든 오퍼 컨텐츠(예: Target Classic의 캠페인)는 계속 로드됩니다. 이 쿠키의 수명은 로드 실패 시간부터 30분입니다.

## 최상위 판매자가 권장 사항에 나타나지 않습니다. {#section_3920C857270A406C80BE6CBAC8221ECD}

*`SIteCatalyst: purchase`* mbox는 구매 알고리즘 트래픽 데이터에 사용할 수 없습니다. 대신 *`orderConfirmPage`* mbox를 사용하십시오.

## 활동 우선 순위 확인 {#section_3D0DD07240F0465BAF655D0804100AED}

[!DNL Target Standard/Premium]으로 만들어진 양식 기반 활동은 [!DNL Target Classic] UI에서 만들어지고 우선 순위가 같고 동일한 mbox를 사용하는 활동과 충돌할 수 있습니다.

## 사용자 지정 코드가 Internet Explorer 8에서 예상한 결과를 생성하지 않습니다. {#section_FAC3651F19144D12A37A3E4F14C06945}

Target에서는 더 이상 IE 8을 지원하지 않습니다.

## 글로벌 mbox.js에 의해 전달된 JavaScript 컨텐츠가 mbox.js{#section_03EC9B9C410B4F52A7FCD81840311709} 사용 시 로드되지 않습니다. 

[!DNL mbox.js] 버전 58 이상으로 업그레이드하십시오.

Mbox.js 버전 58 이상에서는 HTML `BODY` 태그가 제공된 직후에 글로벌 mbox에 대한 비 JavaScript 컨텐츠를 실행합니다. 글로벌 mbox에 대한 `<script>` 태그 내의 JavaScript 컨텐츠는 `DOMContentLoaded` 이벤트가 실행된 이후에 실행됩니다. 이 컨텐츠 전달 순서에 따라 글로벌 mbox에 대한 JavaScript 컨텐츠가 제대로 전달되고 렌더링될 수 있습니다.

## Target 쿠키가 설정되지 않습니다. {#section_77AFEB541C0B495EB67E29A4475DF960}

사이트에 [!DNL us.domain.com]과 같은 하위 도메인이 있지만 [!DNL domain.com] ([!DNL us.domain.com]이 아님)에 Target 쿠키 세트가 필요한 경우 `cookieDomain` 설정을 무시해야 합니다. 자세한 내용은 [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)를 참조하십시오.

## 요소가 AEM 개인화에도 속하면 Target 컨텐츠가 깜박이거나 표시되지 않습니다. {#section_9E1DABEB75AB431FB9F09887E6DD07D3}

DOM 요소가 Adobe Experience Manager(AEM) 개인화 타깃팅 및 Target 활동의 일부인 경우 Target 컨텐츠가 깜박이거나 표시되지 않을 수 있습니다.

이를 해결하려면 Target이 실행 중인 페이지에서 AEM 개인화를 비활성화하면 됩니다.

## 잘못된 URL로 인해 리디렉션 및 원격 오퍼가 전달에 실패했습니다. {#section_7D09043B687F43B39DAEDF17D00375AC}

리디렉션 또는 원격 오퍼가 잘못된 URL을 사용하는 경우 배달되지 않을 수 있습니다.

리디렉션 오퍼의 경우 mbox 응답이 `/* invalid redirect offer URL */`을 포함할 수 있습니다.

또는

원격 오퍼의 경우에는 mbox 응답이 `/* invalid remote offer URL */`을 포함할 수 있습니다.

브라우저에서 또는 mboxTrace를 사용하여 mbox 응답을 확인할 수 있습니다. 올바른 URL에 대한 자세한 내용은 [https://tools.ietf.org/html/std66](https://tools.ietf.org/html/std66)을 참조하십시오.

## mbox가 내 사이트에서 실행되지 않습니다.

at. js 에서는 잘못된 doctype를 사용하는 경우 Target mbox를 실행하지 않습니다. at. s에는 HTML5 doctype이 필요합니다.

## 교육 비디오

다음 비디오에는 이 문서에서 설명한 개념에 대한 자세한 정보가 포함되어 있습니다.

### 확장 추가

>[!VIDEO](https://video.tv.adobe.com/v/23114t2/?captions=kor)

### 기본 Target 디버깅

>[!VIDEO](https://video.tv.adobe.com/v/23115t2/?captions=kor)

### Mbox 추적

>[!VIDEO](https://video.tv.adobe.com/v/23113t2/?captions=kor)