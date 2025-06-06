---
keywords: 타깃팅;시각적 경험 작성기;vec;시각적 경험 작성기 문제 해결;문제 해결;tls;tls 1.2
description: '[!UICONTROL Visual Experience Composer]​(VEC)의 문제를 해결하는 방법을 알아봅니다.'
title: '[!UICONTROL Visual Experience Composer]과(와) 관련된 문제를 해결하려면 어떻게 합니까?'
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
source-git-commit: ef5df0ae37ca1d07c0e51c06ed78739b2d2983fc
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 23%

---

# [!UICONTROL Visual Experience Composer]과(와) 관련된 문제 해결

특정 조건에서 [!DNL Adobe Target] [!UICONTROL Visual Experience Composer]&#x200B;(VEC)에 문제가 발생하는 경우가 있습니다.

## [!UICONTROL Visual Experience Composer]에서 웹 사이트를 열면 [!DNL Target] 라이브러리가 로드되지 않습니다. (VEC만 해당) {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

+++세부 정보
[!DNL Target]이(가) [!UICONTROL Visual Experience Composer]에서 웹 사이트를 여는 동안 두 개의 매개 변수(`mboxEdit=1` 및 `mboxDisable=1`)를 추가합니다.

한 페이지에서 다른 페이지로 이동하는 동안(페이지 다시 로드 없이) 웹 사이트(특히 단일 페이지 앱)가 매개 변수를 자르거나, 실제로 매개 변수를 제거하는 경우 [!DNL Target] 기능이 중단되고 [!DNL Target] 라이브러리가 로드되지 않습니다.

이 문제점을 방지하려면 이러한 두 매개 변수를 자르거나 제거하지 않아야 합니다.

+++

## 내 페이지가 EEC에서 열리지 않거나 느리게 로드됩니다. VEC에서 활동 또는 경험이 느리게 로드됩니다. (VEC만 해당) {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

+++세부 정보
여러 문제가 [!UICONTROL Target] 경험 작성기의 페이지 성능에 영향을 줄 수 있습니다. 일반적인 몇 가지 문제는 다음과 같습니다.

* 페이지에 mbox가 없습니다.
* 사이트가 프록시 차단을 사용하여 어떤 경험 작성기에서도 페이지를 열 수 없습니다.
* 사이트가 자체적으로 iFrame에서 열리는 것을 허용하지 않습니다.

[!UICONTROL Enhanced Experience Composer]에서 문제가 발생하면 [!UICONTROL Enhanced Experience Composer]을(를) 끄고 대신 [!UICONTROL Visual Experience Composer]을(를) 사용하십시오.

[!UICONTROL Enhanced Experience Composer]을(를) 비활성화하려면 **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**(으)로 이동하여 **[!UICONTROL Enable Enhanced Experience Composer]** 옵션을 끕니다.

일부 사용자의 경우 콘솔에 다음과 같은 오류 메시지가 표시됩니다.

![콘솔 오류 메시지](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

[!UICONTROL Visual Experience Composer]과(와) [!UICONTROL Enhanced Experience Composer]이(가) 모두 작동하지 않는 경우 사이트의 X-Frame 헤더 옵션을 덮어쓰고 iFrame에서 로드되도록 하여 VEC를 활성화하는 응답 헤더 수정(Firefox)이나 [!DNL Requestly]&#x200B;([!DNL Chrome] 또는 [!DNL Firefox])과 같은 브라우저 확장 프로그램을 사용하십시오. 브라우저 확장을 사용할 수 없는 경우 [양식 기반 경험 작성기](/help/main/c-experiences/form-experience-composer.md)를 사용하십시오.

>[!NOTE]
>
>다음 정보 외에 [!DNL Google Chrome]에 대해 [[!DNL Adobe Target] [!UICONTROL Visual Editing Helper] 확장 ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)을(를) 사용할 수 있습니다.

>[!NOTE]
>
>이러한 플러그인은 VEC 편집 컨텍스트에서만 사용해야 합니다.
>
>[!DNL Requestly] 확장의 경우 헤더를 제거해야 할 때마다 다음 중 하나를 수행해야 합니다.
>
>* 해당 URL에 대해서만 헤더가 제거되도록 VEC에서 열려고 하는 URL에 대한 URL 규칙을 추가하십시오.
>
>* VEC에서 편집할 때 규칙을 활성화하고 VEC를 사용하지 않을 때 규칙을 비활성화하십시오.
>
>[!UICONTROL Modify Response Header] 확장([!DNL Firefox])의 경우 URL 규칙을 추가할 수 없으므로 다음을 수행해야 합니다.
>
>* VEC에서 편집할 때 규칙을 활성화하고 VEC를 사용하지 않을 때 규칙을 비활성화하십시오.

**[!DNL Chrome] 또는 [!DNL Firefox]에서 [!DNL Requestly] 확장을 사용하려면:**

1. [!UICONTROL Enhanced Experienced Composer]을(를) 끕니다.
1. [!DNL Chrome] 또는 [!DNL Firefox]에 [!DNL Requestly] 브라우저 확장을 설치합니다.
1. 확장을 열고 다음을 사용하여 구성합니다.
1. **[!UICONTROL Modify headers]**&#x200B;을(를) 선택합니다.
1. 다음을 입력하십시오.

   * 규칙 이름
   * 수정 규칙

      * **[!UICONTROL Add]**&#x200B;에서 **[!UICONTROL Remove]**(으)로 전환합니다.
      * **[!UICONTROL Request]**&#x200B;에서 **[!UICONTROL Response]**(으)로 전환합니다.
      * 헤더 이름으로 &quot;X-Frame-Options&quot;를 입력합니다.
      * 이전 단계를 반복하고 헤더 이름으로 &quot;x-frame-options&quot;를 입력합니다.

        >[!NOTE]
        >
        >[!DNL Requestly]을(를) 통해 조작되는 헤더는 대/소문자를 구분합니다.

      * 소스 URL에 대한 조건으로 **[!UICONTROL Equals]**&#x200B;을(를) **[!UICONTROL Contains]**(으)로 변경하고 VEC에 로드하려는 활동의 URL을 입력합니다.

     ![chrome_extension 이미지](assets/chrome_extension.png)

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

   ![요청 이미지](assets/requestly.png)

   이제 [!UICONTROL Visual Experience Composer]을(를) 사용하여 페이지를 빠르게 로드할 수 있습니다.

**[!UICONTROL Firefox]에서 [!DNL Modify Response Headers] 확장을 사용하려면:**

1. [!DNL Firefox]에 [!UICONTROL Modify Response Headers]을(를) 설치하고 브라우저를 다시 시작합니다.
1. [!DNL Firefox] 확장에서 응답 헤더 수정 확장을 선택합니다.
1. **[!UICONTROL Preferences]** 아이콘을 클릭합니다.
1. [!UICONTROL Action] 드롭다운에서 **[!UICONTROL Filter]** 선택.
1. [!UICONTROL Header Name] 필드에 **[!UICONTROL X-Frame-Options]**&#x200B;을(를) 입력합니다.
1. **[!UICONTROL x-frame-options]**&#x200B;을(를) 사용하여 필터를 추가하려면 4단계와 5단계를 반복합니다.
1. **[!UICONTROL Add]** 아이콘을 클릭합니다.
1. **[!UICONTROL Start]** 아이콘을 클릭합니다.

![Firefox 확장 프로그램](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox_extension.png)

확장을 설정한 후 [!DNL Target]을(를) 엽니다. [!UICONTROL Enhanced Experience Composer]이(가) 비활성화되어 있더라도 이제 페이지가 [!UICONTROL Visual Experience Composer]에 로드됩니다.

+++

## VEC(VEC 전용)에 내 페이지가 표시되지 않습니다. {#does-not-load}

+++세부 사항
* 최신 버전의 확장 [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper extension]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)에서는 VEC와의 호환성을 최상으로 유지합니다.

  최신 버전을 사용 중인지 확인하려면 [!UICONTROL Extensions] > [!UICONTROL Manage Extensions]&#x200B;(으)로 이동한 다음 [!UICONTROL Details]을(를) 클릭합니다.

* [!UICONTROL Visual Experience Composer]에서 웹 페이지를 수정하려면 라이브러리를 작성해야 합니다. 이러한 라이브러리는 at.js 라이브러리에 포함되어 있으며 VEC를 사용할 때마다 [!DNL Adobe] 서버에서 확장을 통해 다운로드됩니다.

  확장 프로그램은 at.js 또는 [!DNL Adobe Experience Platform Web SDK]이(가) 페이지에 이미 포함되어 있는지 여부에 관계없이 at.js 라이브러리를 다운로드합니다.

  [!UICONTROL Administration] > [!UICONTROL Implementation] 섹션에 구성된 at.js 헤더에 잘못된 변경 내용이 추가되지 않았는지 확인하십시오.

* 웹 페이지가 iFrame 내에 임베드된 경우 로드에 필수적인 요청을 차단하지 않는지 확인하십시오. 여기에는 고객 웹 사이트, 메타 HTML 태그 또는 x-frame-options 헤더에 포함된 프레임-상위 CSP 지시문 또는 사용자 지정 JS 코드 사용이 포함됩니다.

* 웹 페이지의 Javascript가 작성 라이브러리를 방해하지 않는지 확인합니다. 다음 예약된 이름을 사용하는 파일을 사용하거나 포함하지 마십시오.

   * `target-vec-helper.js`
   * `target-vec.js`
   * `target.js`
   * `admin.css`
   * `sizzle.js`
   * `mixContentCheck.html`

     또한 이러한 파일 내에 정의된 변수나 이벤트를 실수로 무시하면 VEC에 문제가 발생할 수 있습니다.

* 브라우저가 보안 사이트에서 비보안 페이지를 차단하고 있습니다.

  브라우저 주소 표시줄에서 URL 왼쪽에 있는 아이콘을 클릭하고 **[!UICONTROL Disable protection on this page]**&#x200B;을(를) 클릭합니다

* 올바르지 않은 URL을 입력했습니다.
* 웹 사이트가 VEC에서 로드되지 않거나 예기치 않게 작동하는 경우, 잠재적인 해결 방법은 [!DNL Target]에서 웹 사이트를 로드하기 전에 브라우저에서 웹 사이트의 쿠키를 수락하는 것입니다.

+++

## [!UICONTROL Browse] 모드를 사용하면 VEC가 손상된 것으로 나타납니다. (VEC만 해당) {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

+++세부 정보
[!UICONTROL Browse] 모드를 사용하는 동안 [!DNL Target] 라이브러리가 구현되지 않았거나([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank} 또는 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}) Frame-Buster 헤더가 포함된 URL에 액세스하면 VEC가 손상된 것으로 표시됩니다. 브라우저 보안 문제로 인해 [!DNL Target]이(가) 탐색한 URL에 제대로 액세스할 수 없거나 페이지가 로드될 경우 VEC URL이 일관되게 업데이트되지 않습니다.

이 문제는 VEC가 `<iframe>`에서 웹 페이지를 로드하기 때문에 발생합니다. 브라우저의 현재 보안 메커니즘은 동일한 원본 정책으로 인해 [!DNL Target] UI가 지정된 프레임의 요소에 액세스하지 못하도록 합니다. 브라우저는 `location.href`과(와) 같은 정보를 포함하는 다른 원본의 프레임에 액세스하려는 스크립트를 차단합니다.

최적의 상태로 탐색하려면 새 [Visual Editing Helper 확장 기능](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md)을 사용하여 [!DNL Target] 라이브러리를 페이지에 삽입해야 합니다.

+++

## [!UICONTROL Visual Experience Composer]의 CSS 충돌로 인해 발생하는 문제

+++세부 정보
편집기에서 웹 페이지를 로드하는 동안 가시성에 영향을 줄 수 있는 CSS 파일이 있는지 확인합니다. 예를 들어 페이지 본문에서 `overflow: hidden` 속성을 사용하면 스크롤 문제가 발생하거나 메뉴를 작성하는 데 방해가 될 수 있는 클릭 이벤트가 트리거될 수 있습니다.

+++
