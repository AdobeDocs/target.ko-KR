---
keywords: 타깃팅;시각적 경험 작성기;허용 목록;허용 목록에 추가하다;허용 목록;고급 시각적 경험 작성기;vec;시각적 경험 작성기 문제 해결;문제 해결;eec;고급 경험 작성기;tls;tls 1.2
description: 특정 조건에서 [!DNL Target] [!UICONTROL 시각적 경험 작성기](VEC) 및 [!UICONTROL 향상된 경험 작성기](EEC)에서 발생하는 문제를 해결하는 방법에 대해 알아봅니다.
title: '[!UICONTROL 시각적 경험 작성기] 및 [!UICONTROL 향상된 경험 작성기]와 관련된 문제를 해결하려면 어떻게 합니까?'
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
TQID: 'https://experienceleague.adobe.com/4v7Qe-Yzjke-GceUSRDO2SMZGkxvrkdsSXQt8TR-bic'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1218'
ht-degree: 13%
---
# [!DNL Adobe Target] [!UICONTROL 시각적 경험 작성기] 및 [!UICONTROL 향상된 경험 작성기]와 관련된 문제 해결 {#vec-eec-issues}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL 시각적 경험 작성기]**(VEC) 및 **[!UICONTROL 향상된 경험 작성기]**(EEC)에 모두 영향을 주는 문제를 해결하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

특정 조건에서 [!DNL Target] **[!UICONTROL 시각적 경험 작성기]**(VEC) 및 **[!UICONTROL 향상된 경험 작성기]**(EEC)에서 표시 문제 및 기타 문제가 발생하는 경우가 있습니다. 다음 항목에서는 두 작성기에 영향을 주는 문제와 해결 방법에 대해 설명합니다.

## 브라우저 및 보안

### Google Chrome samesite 쿠키 정책 {#samesite}

[!DNL Google Chrome]의 SameSite 쿠키 시행 정책은 다음 릴리스의 VEC 및 EEC에 영향을 줍니다.

>[!NOTE]
>
>다음 변경 사항은 세 릴리스 모두에 적용됩니다. [VEC Helper 확장 프로그램](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)이 설치되어 있고 활성화되어 있지 않으면 사이트의 암호로 보호된 페이지에서 VEC를 사용할 수 없습니다. 사이트의 로그인 쿠키는 서드파티 쿠키로 간주되므로 **[!UICONTROL 찾아보기]** 모드에서 VEC 편집기 내에서 로그인 요청과 함께 전송되지 않습니다. 유일한 예외는 로그인 쿠키에 이미 `SameSite=None` 및 `Secure` 특성이 설정되어 있는 경우입니다.

* **Chrome 94(2021년 9월 21일):** Chrome 94 이상을 사용하는 모든 사용자의 경우 명령줄 플래그 `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure`이(가) 제거되었습니다.
* **Chrome 91(2021년 5월 25일):** Chrome 91 이상을 사용하는 모든 사용자의 경우 `#same-site-by-default-cookies` 및 `#cookies-without-same-site-must-be-secure` 플래그가 `chrome://flags`에서 제거되었습니다. 이제 이 동작은 기본적으로 활성화됩니다.
* **Chrome 80(2020년 8월):** Chrome 80 이상을 사용하는 모든 사용자:

  * 사이트에 아직 없는 경우 활동을 편집하는 동안 [!DNL Target] 라이브러리를 다운로드할 수 없습니다. 고객 도메인에서 보안 [!DNL Adobe] 도메인으로 다운로드 호출이 수행되며 인증되지 않은 것으로 거부됩니다.
  * EEC가 `adobemc.com` 도메인의 쿠키에 대해 SameSite 특성을 설정할 수 없으므로 작동하지 않습니다. 이 속성이 없으면 브라우저가 이러한 쿠키를 거부하여 EEC가 실패합니다.

+++ 차단된 쿠키 확인

SameSite 쿠키 시행 정책에 의해 차단된 쿠키를 확인하려면 [!DNL Chrome]의 [!DNL Developer Tools]을(를) 사용합니다.

1. [!DNL Chrome]에서 VEC를 보는 동안 Chrome > **[!UICONTROL 추가 도구]** > **[!UICONTROL 개발자 도구]**&#x200B;의 오른쪽 상단 모서리에 있는 **[!UICONTROL 줄임표]** 아이콘을 클릭합니다.
1. **[!UICONTROL 네트워크]** 탭을 클릭한 다음 차단된 쿠키를 찾습니다.

   >[!NOTE]
   >
   >**[!UICONTROL 쿠키를 차단했습니다]** 확인란을 사용하여 차단된 쿠키를 더 쉽게 찾을 수 있습니다.

+++

+++ CSP(콘텐츠 보안 정책) 헤더가 웹 사이트의 [!DNL Target] 라이브러리를 차단합니다.

웹 사이트의 CSP 헤더가 [!DNL Target] 라이브러리를 차단하면 웹 사이트가 로드되지만 편집할 수 없습니다. [!DNL Target] 라이브러리가 차단되지 않았는지 확인하십시오.

>[!NOTE]
>
>다음 정보 외에 [!DNL Google Chrome]에 대한 [Adobe Target VEC Helper 브라우저 확장 프로그램](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)을 사용할 수 있습니다.

![콘텐츠 보안 정책 지시문이 위반되었다는 메시지와 함께 target.js에 대한 차단된 요청을 표시하는 브라우저 콘솔](assets/cps_headers.png)

해결 방법으로, 다음 그림과 같이 CSP 헤더를 제거하도록 [!DNL Requestly] 규칙을 구성하십시오.

![HTTP 요청 및 응답에서 Content-Security-Policy 헤더를 제거하는 Content-Security-Policy라는 규칙을 사용하여 요청 대화 상자, 헤더 수정](assets/cps_headers_2.png)

VEC 내에서 리소스가 로드되지 않는 모든 헤더에 대해 유사한 [!DNL Requestly] 규칙을 구성할 수 있습니다. [!DNL Requestly]을(를) 사용하여 헤더를 제거해야 할 때마다 다음 중 하나를 수행하십시오.

* VEC에서 열 URL에 대한 URL 규칙을 추가하여 해당 URL에 대한 헤더만 제거합니다.
* VEC에서 편집하는 동안 규칙을 활성화하고 VEC가 사용 중이 아닌 경우 규칙을 비활성화합니다.

+++

+++ 다중 수준 iframe은 지원되지 않습니다.

[!DNL Target]은(는) 다중 수준 iframe을 지원하지 않습니다. 웹 사이트가 하위 iframe이 있는 iframe을 로드하는 경우 at.js는 상위 iframe과만 상호 작용합니다. [!DNL Target] 라이브러리가 하위 iframe과 상호 작용하지 않습니다.

해결 방법으로, 하위 iframe의 URL을 사용하여 경험에 페이지를 추가합니다.

+++

+++ iFrame 버스팅 사이트 또는 [!DNL Target] 구현이 없는 페이지에서는 경험을 편집할 수 없습니다.

이 문제를 해결하려면 **[!UICONTROL 향상된 경험 작성기]**(EEC)를 사용하도록 설정하십시오. **[!UICONTROL 관리]** > **[!UICONTROL 시각적 경험 작성기]**&#x200B;를 클릭한 다음 **[!UICONTROL 향상된 경험 작성기]**&#x200B;를 활성화하는 확인란을 선택하십시오.

EEC는 [!DNL Adobe] 관리 프록시를 사용하여 편집할 페이지를 로드합니다. 이 프록시를 사용하면 iFrame 버스팅 사이트 및 [!DNL Adobe Target] 코드가 아직 추가되지 않은 사이트 및 페이지에서 편집할 수 있습니다. 코드가 추가될 때까지 활동은 사이트로 전달되지 않습니다. 일부 사이트는 EEC를 통해 로드되지 않을 수 있으며, 이 경우 이 옵션을 지우면 iFrame을 통해 페이지가 로드됩니다.

>[!NOTE]
>
>로컬로 호스팅된 페이지 및 네트워크 외부에서 액세스할 수 없는 페이지는 [!DNL Adobe] 프록시 서버에서 액세스할 수 없으며 EEC에서 열 수 없습니다. 이러한 페이지에는 스테이징 URL, UAT(사용자 승인 테스트) URL 또는 로컬로 호스팅된 페이지가 포함될 수 있습니다.

+++

## 페이지 로드 및 표시

+++ 페이지를 편집할 때 페이지 대신 회전자가 표시됩니다

이 상황은 URL에 # 문자가 포함된 경우 발생할 수 있습니다. 문제를 해결하려면 VEC 또는 EEC에서 **[!UICONTROL 찾아보기]** 모드로 전환한 다음 **[!UICONTROL 작성]** 모드로 다시 전환합니다. 회전자가 사라지고 페이지가 로드됩니다.

+++

+++ 저장된 활동을 다시 편집할 때 VEC 또는 EEC가 손상되었거나 초기화되지 않습니다

경험이 정의된 후 웹 사이트가 VEC 외부에서 변경된 경우 활동을 다시 편집하기 위해 열면 이전에 작업을 수행한 선택기를 찾을 수 없습니다. 페이지가 손상된 것처럼 보이고 경고는 표시되지 않습니다.

+++

+++ 회전 배너 및 JavaScript이 포함된 기타 콘텐츠는 VEC 또는 EEC에 표시되지 않습니다

기본적으로 VEC는 JavaScript 요소를 차단합니다. JavaScript을 비활성화하면 이러한 요소로 작업할 수 있습니다. 사이트가 설정되는 방식에 따라, 일부 항목은 계속 잘못 표시되거나 사용 불가능한 상태로 남아 있을 수 있습니다.

+++

+++ Automated Personalization 활동의 경우, VEC 또는 EEC에서 이미지 대체 기능이 손상된 것으로 표시됩니다

이미지 오퍼를 위치에 추가하면 VEC 또는 EEC에서 원래 이미지 공간의 전체 차원이 사용됩니다. 전달 시에는 이미지가 확장되지 않으며 원래 그대로 표시되므로 전달에는 영향을 주지 않습니다.

+++

## 결과 편집

+++ 페이지에서 한 요소를 변경하면 여러 요소가 변경됩니다

페이지의 여러 요소에 동일한 DOM 요소 ID를 사용하는 경우, 해당 요소 중 하나를 변경하면 해당 ID를 사용하는 모든 요소가 변경됩니다. 이를 방지하려면 각 페이지에서 ID를 한 번만 사용하십시오. 이것이 표준 HTML 우수 사례입니다. 자세한 내용은 [페이지 수정 시나리오](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#vec-scenarios)를 참조하십시오.

+++

+++ 텍스트 편집/HTML 편집 또는 텍스트 변경/HTML 변경을 적용한 후 굵게 및 기울임체 텍스트 스타일이 표시되지 않거나 텍스트가 사라짐

**[!UICONTROL A/B 테스트]** 또는 **[!UICONTROL 경험 타깃팅]** 활동에 대해 VEC에서 **[!UICONTROL 텍스트 편집]**/**[!UICONTROL HTML 편집]**&#x200B;을 사용하거나 **[!UICONTROL Automated Personalization]** 또는 **[!UICONTROL 다변량 테스트]** 활동에 **[!UICONTROL 텍스트 변경]**/**[!UICONTROL HTML 변경]**&#x200B;을 사용하여 텍스트를 굵게 또는 기울임체로 설정하는 경우 페이지에 스타일이 적용되지 않거나 VEC의 페이지에서 텍스트가 사라질 수 있습니다. 이 문제는 서식 있는 텍스트 편집기에서 이러한 스타일을 적용하는 방법이 웹 사이트 마크업을 방해할 수 있기 때문에 발생합니다.

이 문제가 발생하는 경우:

1. 서식 있는 텍스트 편집기에서 **[!UICONTROL HTML]** 단추를 클릭하여 소스 편집 모드에 들어갑니다.
1. 스타일이 지정된 텍스트 요소를 찾습니다.

   * 굵게 텍스트의 경우 `<strong>` 요소를 `<b>`로 변경하십시오.
   * 기울임체 텍스트의 경우 `<em>` 요소를 `<i>`로 변경하십시오.

+++
