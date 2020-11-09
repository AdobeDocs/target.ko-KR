---
keywords: mixed content;secure;insecure;chrome;troubleshooting;vec;visual experience composer;unsecure;http;https;firefox;internet explorer
description: 일부 브라우저의 경우 보안 컨텐츠가 비보안 컨텐츠와 혼합된 경우 페이지 표시를 차단합니다.
title: 브라우저에서 혼합 컨텐츠 활성화
feature: vec
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 34%

---


# Enabling mixed content in your browser{#enabling-mixed-content-in-your-browser}

HTTPS(보안) *및* HTTP(비보안) 컨텐츠가 모두 동일한 웹 페이지를 표시하도록 로드되고 초기 요청이 HTTPS를 통해 안전하면 혼합 컨텐츠가 발생합니다.

보안 컨텐츠가 안전하지 않은 컨텐츠와 섞여 있는 경우 최신 브라우저에서 페이지 표시를 차단하거나 경고 메시지를 표시할 수 있습니다.

If the [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Target] tries to open a page containing mixed content, a message displays showing how to disable blocking in your browser so you can open an HTTP site or a site that has mixed calls (HTTPS and HTTP).

![혼합 컨텐츠 경고](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

이전에는 혼합 컨텐츠가 허용되지 않는 경우 활동을 작성할 때 3단계 안내가 있는 워크플로우의 1단계에서 일부 작업을 수행할 수 있었습니다. [!DNL Target] 이제 1단계에서 작업을 차단합니다. 이 메시지가 표시되면 활동을 계속 만들기 전에 혼합 컨텐츠를 활성화해야 합니다.

브라우저의 보안 설정이 혼합 컨텐츠나 비보안(HTTP) 컨텐츠가 보안(HTTPS) 페이지나 프레임(예: VEC)으로 로드되는 것을 차단할 수 있습니다. 브라우저의 보안 설정을 비활성화하지 않으려면 HTTPS 웹 사이트가 있어야 합니다.

웹 사이트가 비보안(HTTP) 도메인에서 실행 중인 경우에는 VEC이 활성 상태 혼합 컨텐츠를 로드하는 것을 허용해야 합니다.

>[!NOTE]
>
>혼합 컨텐츠 허용은 여러분의 라이브 웹 사이트에는 영향을 주지 않고 VEC에만 영향을 줍니다.

자세한 내용은 *Mozilla Developer Network*(MDN) 웹 사이트의 [Mixed Content](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content)(혼합 컨텐츠)를 참조하십시오.

## Enabling mixed content in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

보안 연결을 통해 사이트를 방문하는 경우 Chrome은 웹 페이지의 컨텐츠가 안전하게 전송되었는지 확인합니다.

Google Chrome 도움말에서 [이 페이지에 안전하지 않은 콘텐츠가 있음](https://support.google.com/chrome/answer/1342714?hl=en)을 참조하십시오.

최신 버전의 Chrome에서 VEC를 사용하는 경우(버전 79.0.3945.117 이상) 사이트 설정을 업데이트해야 합니다. 사이트 방문자는 이러한 단계를 완료할 필요가 없습니다.

1. 잠금 또는 주의 아이콘을 클릭한 다음 **[!UICONTROL 사이트 설정을 클릭합니다]**.

   ![사이트 설정](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. 비보안 **[!UICONTROL 콘텐츠로]**&#x200B;스크롤한 다음 드롭다운 목록을 사용하여 &quot;블록(기본값)&quot;을 &quot;허용&quot;으로 변경합니다.

   ![안전하지 않은 콘텐츠](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. VEC 페이지를 다시 로드합니다.

## Enabling mixed content in Mozilla Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

기본적으로 Firebox에서는 보안 및 비보안 컨텐츠를 혼합하는 페이지를 차단합니다. 이 설정을 [!DNL Target]을 사용하도록 영구적으로 변경하는 것이 좋습니다. 사이트 방문자는 이러한 단계를 완료할 필요가 없습니다.

1. Firefox에서 주소 표시줄에 `about:config`를 입력합니다.
1.  Firefox에서 표시되는 경고 메시지를 확인합니다. 

   ![Firefox 경고](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. 검색 막대에서 `block_active`을 입력합니다.

   ![Firefox 블록 활성 설정](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. ` **[!UICONTROL security.mixed_content.block_active_content]**`를 두 번 클릭합니다.

   값이 &quot;True&quot;에서 &quot;False&quot;로 변경됩니다. 값이 &quot;False&quot;를 표시하면 끝난 것입니다.

   ![Firefox 보안](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

이 설정을 변경한 후 컴퓨터를 다시 시작하는 것이 좋습니다.

## Microsoft Edge에서 혼합 컨텐츠 사용

보안 연결을 통해 사이트를 방문하는 경우 Edge는 웹 페이지의 컨텐츠가 안전하게 전송되었는지 확인합니다.

최신 버전의 Edge에서 VEC를 사용하는 경우 사이트 설정을 업데이트해야 합니다. 사이트 방문자는 이러한 단계를 완료할 필요가 없습니다.

1. 잠금 또는 주의 아이콘을 클릭한 다음 **[!UICONTROL 사이트 권한을 클릭합니다]**.

   ![Microsoft Edge의 사이트 권한](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge.png)

1. 비보안 **[!UICONTROL 콘텐츠로]**&#x200B;스크롤한 다음 드롭다운 목록을 사용하여 &quot;블록(기본값)&quot;을 &quot;허용&quot;으로 변경합니다.

   ![안전하지 않은 콘텐츠](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge-2.png)

1. VEC 페이지를 다시 로드합니다.