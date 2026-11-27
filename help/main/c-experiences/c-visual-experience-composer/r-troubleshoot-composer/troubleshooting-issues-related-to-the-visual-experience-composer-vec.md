---
keywords: 타깃팅;시각적 경험 작성기;vec;시각적 경험 작성기 문제 해결;문제 해결;tls;tls 1.2
description: '[!UICONTROL 시각적 경험 작성기](VEC)에서 문제를 해결하는 방법을 알아봅니다.'
title: '[!UICONTROL 시각적 경험 작성기]와 관련된 문제를 해결하려면 어떻게 합니까?'
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
TQID: 'https://experienceleague.adobe.com/VNkydzzU-WRRAL0pqQPOs-sKrY8a6DS5Go764UGh0Hs'
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1150'
ht-degree: 4%
---
# [!UICONTROL 시각적 경험 작성기]와 관련된 문제 해결 {#vec-issues}

>[!BEGINSHADEBOX]

**이 페이지에서:** **[!UICONTROL 시각적 경험 작성기]**(VEC)에만 영향을 주는 문제를 해결하는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

특정 조건에서 [!DNL Adobe Target] **[!UICONTROL 시각적 경험 작성기]**(VEC)에 표시 문제가 발생하는 경우가 있습니다. 다음 항목에서는 VEC에만 영향을 주는 문제와 해결 방법을 설명합니다.

+++ VEC에서 웹 사이트를 열 때 [!DNL Target] 라이브러리가 로드되지 않습니다.

**[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 웹 사이트를 열면 [!DNL Target]이(가) URL에 매개 변수 `mboxEdit=1` 및 `mboxDisable=1`을(를) 추가합니다.

페이지를 다시 로드하지 않고 한 페이지에서 다른 페이지로 이동하는 동안 이러한 매개 변수를 자르거나 제거하는 웹 사이트(특히 단일 페이지 애플리케이션)는 [!DNL Target] 기능을 중단하며 [!DNL Target] 라이브러리가 로드되지 않습니다. 이 문제를 방지하려면 두 매개 변수를 모두 URL에 유지하십시오.

+++

+++ 페이지가 EEC에서 열리지 않거나 느리게 로드되거나 활동 및 경험이 VEC에서 느리게 로드됩니다

여러 문제가 [!DNL Target] 경험 작성기의 페이지 성능에 영향을 줄 수 있습니다. 가장 일반적인 방법은 다음과 같습니다.

* 페이지에 mbox가 없습니다.
* 사이트는 프록시 차단을 사용하여 두 경험 작성기에서 페이지가 열리지 않도록 합니다.
* 사이트는 iFrame에서 열리지 않습니다.

**[!UICONTROL 향상된 경험 작성기]**&#x200B;에서 문제가 발생하면 이를 끄고 대신 **[!UICONTROL 시각적 경험 작성기]**&#x200B;를 사용하십시오. 이렇게 하려면 **[!UICONTROL 관리]** > **[!UICONTROL 시각적 경험 작성기]**(으)로 이동하여 **[!UICONTROL 향상된 경험 작성기 사용]** 옵션을 끕니다.

콘솔에 다음 오류 메시지가 표시될 수 있습니다.

![X-Frame-Options가 SAMEORIGIN으로 설정되어 있으므로 페이지에서 프레임 표시를 거부했다는 브라우저 콘솔 오류 메시지](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

두 작성기가 모두 작동하지 않으면 [!DNL Requestly]&#x200B;([!DNL Chrome] 또는 [!DNL Firefox])이나 응답 헤더 수정([!DNL Firefox])과 같은 사이트의 X-Frame-Options 헤더를 덮어쓰는 브라우저 확장 프로그램에서 사이트를 iFrame으로 로드하여 VEC를 사용하도록 설정합니다. 브라우저 확장을 사용할 수 없으면 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 사용하십시오. [!DNL Google Chrome]에 대한 [[!DNL Adobe Target] **[!UICONTROL Visual Editing Helper ]**확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)은(는) 다음 절차 외에 사용할 수도 있습니다.

>[!NOTE]
>
>이러한 확장은 VEC 편집용으로만 사용됩니다.
>
>[!DNL Requestly]을(를) 사용하여 헤더를 제거해야 할 때마다 다음 중 하나를 수행합니다.
>
>* VEC에서 열 URL에 대한 URL 규칙을 추가하여 해당 URL에 대한 헤더만 제거합니다.
>* VEC에서 편집하는 동안 규칙을 활성화하고 VEC가 사용 중이 아닌 경우 규칙을 비활성화합니다.
>
>**[!UICONTROL 응답 헤더 수정]**([!DNL Firefox])을 사용하면 URL 규칙을 사용할 수 없으므로 VEC에서 편집할 때는 규칙을 사용하도록 설정하고 VEC가 사용되지 않을 때는 사용하지 않도록 설정해야 합니다.

확장이 설정되면 **[!UICONTROL 향상된 경험 작성기]**&#x200B;를 사용하지 않도록 설정한 경우에도 **[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 페이지가 로드됩니다.

+++

+++ Requestly(Chrome 또는 Firefox)를 사용하여 X-Frame-Options 헤더를 제거합니다.

1. **[!UICONTROL 향상된 경험 작성기]**&#x200B;를 끕니다.
1. [!DNL Chrome] 또는 [!DNL Firefox]에 [!DNL Requestly] 브라우저 확장을 설치합니다.
1. 확장을 열고 **[!UICONTROL 헤더 수정]**&#x200B;을 선택합니다.
1. 규칙 이름을 입력합니다.
1. 수정 규칙에서 헤더를 제거하는 규칙을 만듭니다.

   * **[!UICONTROL 추가]**&#x200B;에서 **[!UICONTROL 제거]**&#x200B;로 전환합니다.
   * **[!UICONTROL 요청]**&#x200B;에서 **[!UICONTROL 응답]**&#x200B;으로 전환합니다.
   * 헤더 이름으로 &quot;X-Frame-Options&quot;를 입력합니다.

1. 이전 단계를 반복하고 헤더 이름으로 &quot;x-frame-options&quot;를 입력합니다.

   >[!NOTE]
   >
   >[!DNL Requestly]&#x200B;(으)로 조작되는 헤더는 대/소문자를 구분합니다.

1. 소스 URL의 조건으로 **[!UICONTROL 같음]**&#x200B;을(를) **[!UICONTROL 포함]**(으)로 변경하고 VEC에 로드할 활동의 URL을 입력하십시오.

   ![adobe.com이 포함된 URL에 대한 X-Frame-Options 응답 헤더를 제거하는 Bypass iframe 버스팅 코드라는 Requestly 규칙](assets/chrome_extension.png)

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![모든 URL에 대해 X-FRAME-OPTIONS 및 X-Frame-OPTIONS 응답 헤더를 제거하는 Requestly 규칙](assets/requestly.png)

이제 페이지가 **[!UICONTROL 시각적 경험 작성기]**&#x200B;에서 빠르게 로드됩니다.

+++

+++ 수정 응답 헤더(Firefox)를 사용하여 X-Frame-Options 헤더를 제거합니다.

1. [!DNL Firefox]에 [!DNL Modify Response Headers] 확장을 설치하고 브라우저를 다시 시작합니다.
1. [!DNL Firefox] 확장에서 [!DNL Modify Response Headers] 확장을 선택합니다.
1. **[!UICONTROL 기본 설정]**&#x200B;을 클릭합니다.
1. **[!UICONTROL 작업]** 드롭다운 목록에서 **[!UICONTROL 필터]**&#x200B;을(를) 선택하십시오.
1. **[!UICONTROL 헤더 이름]** 필드에 **[!UICONTROL X-Frame-Options]**&#x200B;을(를) 입력하십시오.
1. 앞의 두 단계를 반복하여 **[!UICONTROL x-frame-options]**&#x200B;이(가) 있는 필터를 추가합니다.
1. **[!UICONTROL 추가]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 시작]**&#x200B;을 클릭합니다.

![X-Frame-Options 헤더에 필터를 사용하여 Firefox의 응답 헤더 수정](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox_extension.png)

+++

+++ 페이지가 VEC에 표시되지 않음

다음 원인을 확인하십시오.

* **확장 버전:** 최신 버전의 [[!DNL Adobe Experience Cloud] **[!UICONTROL Visual Editing Helper ]**확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)은(는) VEC와 가장 잘 호환됩니다. 설치된 버전을 확인하려면**[!UICONTROL &#x200B;확장&#x200B;]**>**[!UICONTROL &#x200B;확장 관리&#x200B;]**(으)로 이동한 다음**[!UICONTROL &#x200B;세부 정보&#x200B;]**를 클릭합니다.
* **작성 라이브러리:** VEC에서 웹 페이지를 수정하려면 작성 라이브러리가 필요합니다. 이 매개 변수는 at.js 라이브러리에 포함되어 있으며, at.js 또는 [!DNL Adobe Experience Platform Web SDK]이(가) 페이지에 이미 있는지 여부에 관계없이 VEC를 사용할 때마다 확장 프로그램이 [!DNL Adobe] 서버에서 다운로드합니다. **[!UICONTROL 관리]** > **[!UICONTROL 구현]**&#x200B;에 구성된 at.js 헤더에 잘못된 변경 사항이 없는지 확인하십시오.
* **차단된 요청:** 페이지는 iFrame에 포함되어 있을 때 로드에 필수적인 요청을 차단해서는 안 됩니다. 이러한 차단에는 `frame-ancestors` CSP 지침, 웹 사이트의 사용자 지정 JavaScript 코드, 메타 HTML 태그 및 `x-frame-options` 헤더가 포함됩니다.
* **예약된 파일 이름:** 페이지의 JavaScript은 작성 라이브러리를 방해하지 않아야 합니다. 다음 예약된 이름의 파일을 사용하거나 포함하지 마십시오.

  * `target-vec-helper.js`
  * `target-vec.js`
  * `target.js`
  * `admin.css`
  * `sizzle.js`
  * `mixContentCheck.html`

  이러한 파일에 정의된 변수나 이벤트를 실수로 무시하면 VEC에 문제가 발생할 수도 있습니다.

* **보안 사이트의 비보안 페이지:** 브라우저에서 페이지를 차단합니다. 주소 표시줄에서 URL 왼쪽에 있는 아이콘을 클릭한 다음 **[!UICONTROL 이 페이지에서 보호 사용 안 함]**&#x200B;을 클릭합니다.
* **잘못된 URL:** 입력한 URL이 잘못되었습니다.
* **쿠키:** 웹 사이트가 VEC에서 로드되지 않거나 예기치 않게 동작하는 경우 [!DNL Target]에서 웹 사이트를 로드하기 전에 브라우저에서 해당 쿠키를 수락하면 문제가 해결될 수 있습니다.

+++

+++ VEC가 찾아보기 모드에서 끊어진 상태로 표시됩니다

**[!UICONTROL 찾아보기]** 모드에서 [!DNL Target] 라이브러리([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank} 또는 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank})가 없거나 프레임 버스터 헤더가 포함된 URL을 열면 VEC가 손상된 것으로 표시됩니다. 브라우저 보안상의 이유로 [!DNL Target]이(가) 탐색된 URL에 제대로 액세스할 수 없거나 페이지가 로드될 때 VEC URL이 일관되게 업데이트되지 않습니다.

VEC가 `<iframe>`에 웹 페이지를 로드하고 브라우저의 현재 보안 메커니즘으로 인해 [!DNL Target] UI가 동일한 원본 정책에 따른 프레임의 요소에 액세스하지 못합니다. 브라우저는 `location.href`과(와) 같은 정보를 포함하여 다른 원본이 있는 프레임에 액세스하려고 시도하는 스크립트를 차단합니다.

페이지를 최적으로 탐색할 수 있도록 새 [Visual Editing Helper 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)을 사용하여 [!DNL Target] 라이브러리를 페이지에 삽입하십시오.

+++

+++ 문제는 VEC에서 CSS 충돌로 인해 발생합니다

편집기에서 페이지가 로드되는 동안 CSS 파일이 가시성에 영향을 주는지 확인하십시오. 예를 들어 페이지 본문의 `overflow: hidden` 속성은 스크롤 문제를 일으키거나 작성 메뉴를 방해하는 클릭 이벤트를 트리거할 수 있습니다.

+++
