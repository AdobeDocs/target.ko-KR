---
keywords: 타깃팅;시각적 경험 작성기;허용 목록;허용 목록에 추가하다;허용 목록;고급 시각적 경험 작성기;vec;시각적 경험 작성기 문제 해결;문제 해결;eec;고급 경험 작성기;tls;tls 1.2
description: 특정 조건에서  [!DNL Target] [!UICONTROL Visual Experience Composer](VEC) 및 [!UICONTROL Enhanced Experience Composer]​(EEC)에서 가끔 발생하는 문제를 해결하는 방법에 대해 알아봅니다.
title: '[!UICONTROL Visual Experience Composer] 및 [!UICONTROL Enhanced Experience Composer]과(와) 관련된 문제를 해결하려면 어떻게 합니까?'
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
source-git-commit: ef5df0ae37ca1d07c0e51c06ed78739b2d2983fc
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 26%

---

# [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] 및 [!UICONTROL Enhanced Experience Composer]과(와) 관련된 문제 해결

표시 문제 및 기타 문제는 특정 조건에서 [!DNL Target] [!UICONTROL Visual Experience Composer]&#x200B;(VEC) 및 [!UICONTROL Enhanced Experience Composer]&#x200B;(EEC)에서 발생하는 경우가 있습니다.

## Google Chrome SameSite 쿠키 시행 정책이 VEC 및 EEC에 어떤 영향을 미칩니까? {#samesite}

+++세부 정보
다음 [!DNL Chrome] 릴리스를 사용할 때 VEC 및 EEC에 영향을 주는 변경 사항에 유의하십시오.

>[!NOTE]
>
>다음 변경 사항은 아래에 설명된 세 가지 업데이트에 모두 영향을 줍니다.
>
> * [VEC Helper 확장 프로그램](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)이 설치되어 있고 사이트의 암호로 보호된 페이지에 대해 활성화되지 않으면 *사용할 수 없게*&#x200B;됩니다. 사이트 로그인 쿠키는 타사 쿠키로 간주되며 [!UICONTROL Browse] 모드에서 VEC 편집기 내에서 로그인 요청과 함께 전송되지 않습니다. 유일한 예외는 사이트 로그인 쿠키에 이미 `SameSite=None` 및 `Secure` 특성이 설정되어 있는 경우입니다.

**Chrome 94(2021년 9월 21일)**: Chrome 94 릴리스(2021년 9월 21일)에 대해 예정된 변경 사항이 적용되면 다음 변경 사항은 Chrome 94 이상 브라우저 버전을 사용하는 모든 사용자에게 영향을 줍니다.

* 명령줄 플래그 `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure`이(가) 제거됩니다.

**Chrome 91(2021년 5월 25일)**: Chrome 91 릴리스(2021년 5월 25일)에 대해 구현된 변경 사항으로 인해 Chrome 91 이상 브라우저 버전의 모든 사용자에게 다음 변경 사항이 적용됩니다.

* `chrome://flags`에서 `#same-site-by-default-cookies` 및 `#cookies-without-same-site-must-be-secure` 플래그를 제거했습니다. 이제 이 동작은 기본적으로 활성화됩니다.

**Chrome 80(2020년 8월)**: 2020년 8월에 적용된 변경 내용으로 Chrome 80 이상 브라우저 버전을 사용하는 모든 사용자:

* 활동을 편집하는 동안 *not*&#x200B;에서 [!DNL Target] 라이브러리를 다운로드할 수 있습니다(아직 사이트에 없는 경우). 이는 고객 도메인에서 보안 [!DNL Adobe] 도메인 방향으로 다운로드 호출이 수행되며 인증되지 않은 것으로 거부되기 때문입니다.

* EEC가 `adobemc.com domain`에서 쿠키에 대한 SameSite 특성을 설정할 수 없으므로 모든 사용자에 대해 *not* 함수가 사용됩니다. 이 속성이 없으면 브라우저가 이러한 쿠키를 거부하여 EEC가 실패합니다.

+++

### 차단된 쿠키 확인

+++세부 정보
SameSite 쿠키 시행 정책으로 인해 차단된 쿠키를 확인하려면 [!DNL Chrome]의 [!DNL Developer Tools]을(를) 사용합니다.

1. [!DNL Chrome]에서 VEC를 보는 동안 [!DNL Developer Tools]에 액세스하려면 Chrome > **[!UICONTROL More Tools]** > **[!UICONTROL Developer Tools]**&#x200B;의 오른쪽 상단 모서리에 있는 **[!UICONTROL ellipsis]** 아이콘을 클릭합니다.
1. **[!UICONTROL Network]** 탭을 클릭한 다음 차단된 쿠키를 찾습니다.

   >[!NOTE]
   >
   >**[!UICONTROL Has blocked cookies]** 확인란을 사용하여 차단된 쿠키를 더 쉽게 찾을 수 있습니다.

+++

## [!DNL Target]에서 다중 수준 iframe을 지원합니까?

+++세부 정보
[!DNL Target]은(는) 다중 수준 iframe을 지원하지 않습니다. 웹 사이트에서 하위 iframe이 있는 iframe을 로드하는 경우 at.js는 상위 iframe과만 상호 작용합니다. [!DNL Target] 라이브러리가 하위 iframe과 상호 작용하지 않습니다.

해결 방법으로, 하위 iframe의 URL을 사용하여 경험에 페이지를 추가할 수 있습니다.

+++

## 페이지를 편집하려고 할 때 페이지 대신 회전기가 표시됩니다. (VEC 및 EEC) {#section_313001039F79446DB28C70D932AF5F58}

+++세부 정보
이 상황은 URL에 # 문자가 포함된 경우 발생할 수 있습니다. 문제를 해결하려면 VEC 또는 EEC에서 [!UICONTROL Browse] 모드로 전환한 다음 [!UICONTROL Compose] 모드로 다시 전환합니다. 회전자가 사라지고 페이지가 로드됩니다.

+++

## CSP(콘텐츠 보안 정책) 헤더가 웹 사이트의 [!DNL Target] 라이브러리를 차단합니다. (VEC 및 EEC) {#section_89A30C7A213D43BFA0822E66B482B803}


+++세부 정보
웹 사이트의 CSP 헤더가 [!DNL Target] 라이브러리를 차단한 다음 웹 사이트를 로드하지만 편집할 수 없는 경우 [!DNL Target] 라이브러리가 차단되지 않았는지 확인하십시오.

>[!NOTE]
>
>다음 정보 외에 [!DNL Google Chrome]에 대해 [Adobe Target VEC Helper 브라우저 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)을 사용할 수 있습니다.

![cps_headers 이미지](assets/cps_headers.png)

해결 방법으로 아래와 같이 CSP 헤더를 제거하도록 [!DNL Requestly] 규칙을 구성할 수 있습니다.

![cps_headers_2 이미지](assets/cps_headers_2.png)

VEC 내에서 리소스가 로드되지 않도록 하는 모든 헤더에 대해 유사한 [!DNL Requestly] 규칙을 구성할 수 있습니다.

[!DNL Requestly]의 경우 헤더를 제거해야 할 때마다 다음 중 하나를 수행해야 합니다.

* 해당 URL에 대해서만 헤더가 제거되도록 VEC에서 열려고 하는 URL에 대한 URL 규칙을 추가하십시오.
* VEC에서 편집할 때 규칙을 활성화하고 VEC를 사용하지 않을 때 규칙을 비활성화하십시오.

+++

## VEC 또는 EEC가 손상된 것으로 나타나거나 저장된 활동을 다시 편집할 때 초기화되지 않습니다. (VEC 및 EEC) {#section_5AC3BA8F8FBB451EA814F298D0645E54}

+++세부 정보
경험이 정의된 후 웹 사이트가 VEC 외부에서 변경된 경우 활동을 다시 편집하기 위해 열면 이전에 작업을 수행한 선택기를 찾을 수 없습니다. 페이지가 손상된 것처럼 보이고 경고는 표시되지 않습니다.

+++

## VEC 또는 EEC가 회전 배너와 자바스크립트를 포함하는 기타 콘텐츠를 표시하지 않습니다. (VEC 및 EEC) {#section_8B5BE6EB050B42D6A14A054724C41330}

+++세부 정보
기본적으로 VEC는 JavaScript 요소를 차단합니다. JavaScript을 비활성화하는 경우 이러한 요소로 작업할 수 있습니다. 사이트가 설정되는 방식에 따라, 일부 항목은 계속 잘못 표시되거나 사용 불가능한 상태로 남아 있을 수 있습니다.

+++

## 페이지에서 한 요소를 변경하면 여러 요소가 변경됩니다. (VEC 및 EEC) {#section_309188ACF34942989BE473F63C5710AF}

+++세부 정보
동일한 DOM 요소 ID가 페이지의 여러 요소에 사용되는 경우, 이러한 요소 중 하나를 변경하면 해당 ID가 있는 모든 요소가 변경됩니다. 이러한 문제가 발생하지 않도록 하려면 각 페이지에서 ID를 한 번만 사용해야 합니다. 이 방법은 표준 HTML 우수 사례입니다. 자세한 내용은 [페이지 수정 시나리오](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB)를 참조하십시오.

+++

## iFrame 버스팅 사이트에 대한 경험을 편집할 수 없습니다. (VEC 및 EEC) {#section_9FE266B964314F2EB75604B4D7047200}

+++세부 정보
이 문제는 EEC([!UICONTROL Enhanced Experience Composer])를 활성화하여 해결할 수 있습니다. **[!UICONTROL Administation]** > **[!UICONTROL Visual Experience Composer]**&#x200B;을(를) 클릭한 다음 [!UICONTROL Enhanced Experience Composer]을(를) 활성화하는 확인란을 선택합니다. EEC는 [!DNL Adobe] 관리 프록시를 사용하여 편집할 페이지를 로드합니다. 이 프록시를 사용하면 iFrame 버스팅 사이트에서 편집할 수 있으며 [!DNL Adobe Target] 코드를 아직 추가하지 않은 사이트 및 페이지에서 편집할 수 있습니다. 코드가 추가될 때까지 활동은 사이트로 전달되지 않습니다. 일부 사이트는 EEC를 통해 로드되지 않을 수 있습니다. 이 경우 이 옵션을 선택 취소하고 iFrame을 통해 EEC를 로드할 수 있습니다.

>[!NOTE]
>
>로컬로 호스팅된 페이지 또는 네트워크 외부에서 액세스할 수 없는 페이지는 [!DNL Adobe] 프록시 서버에서 액세스할 수 없으며 EEC에서 열 수 없습니다. 이러한 페이지에는 스테이징 URL, UAT(사용자 승인 테스트) URL 또는 로컬로 호스팅된 페이지가 포함될 수 있습니다.

+++

## mbox/[!DNL Target] 구현이 아직 완료되지 않은 페이지에 테스트를 설정하려고 합니다. (VEC 및 EEC) {#section_DE63BCCB5B124E10A71FA579B582A80A}

+++세부 정보
위의 &quot;iFrame 버스트 사이트에 대한 경험을 편집할 수 없음&quot;을 참조하십시오.

+++

## [!UICONTROL Edit Text]/[!UICONTROL Edit HTML] 또는 [!UICONTROL Change Text]/[!DNL Change HTML]이(가) 있는 굵은 기울임꼴 텍스트 스타일이 내 페이지에 표시되지 않습니다. 이러한 스타일 변경 사항을 적용한 후에 텍스트가 사라지는 경우도 있습니다. (VEC 및 EEC) {#section_7A71D6DF41084C58B34C18701E8774E5}

+++세부 정보
[!UICONTROL A/B Test] 또는 [!UICONTROL Experience Targeting] 활동의 경우 VEC에서 **[!UICONTROL Edit Text]/[!UICONTROL Edit HTML]**, [!UICONTROL Automated Personalization] 또는 [!UICONTROL Multivariate Test] 활동의 경우 **[!UICONTROL Change Text]/[!UICONTROL Change HTML]**&#x200B;을(를) 사용하여 텍스트를 굵게 또는 기울임체로 설정하는 경우 해당 스타일이 페이지에 적용되지 않거나 VEC에서 텍스트가 사라질 수 있습니다. 이러한 문제는 서식 있는 텍스트 편집기에서 이러한 스타일을 적용하는 방식이 웹 사이트 마크업을 방해할 수 있기 때문에 발생합니다.

이 문제가 표시되면 다음을 수행합니다.

1. 서식 있는 텍스트 편집기에서 **[!UICONTROL HTML]** 단추를 클릭하여 소스 편집 모드에 들어갑니다.
1. 스타일 텍스트 요소를 찾습니다.

   * 굵게 텍스트의 경우 `<strong>` 요소를 `<b>`로 변경하십시오.

   * 기울임체 텍스트의 경우 `<em>` 요소를 `<i>`로 변경하십시오.

+++

## 자동화된 개인화 활동의 경우, VEC 또는 EEC에서 이미지 대체 기능이 손상된 것으로 나타납니다. (VEC 및 EEC) {#section_88AABFDFE6A3420299B0D508B12A3994}

+++세부 정보
위치에 이미지 오퍼를 추가하면 VEC 또는 EEC에서 원본 이미지 공간의 전체 차원이 사용됩니다. 전달 시에는 이미지가 확장되지 않으며 원래 그대로 표시되므로 전달에는 영향을 주지 않습니다.

+++
