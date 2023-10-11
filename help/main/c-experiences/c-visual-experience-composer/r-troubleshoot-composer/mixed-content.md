---
keywords: 혼합 콘텐츠;보안;비보안;Chrome;문제 해결;VEC;시각적 경험 작성기;비보안;HTTP;HTTPS;Firefox;Internet Explorer
description: 에서 혼합 콘텐츠를 활성화하는 방법 알아보기 [!DNL Chrome], [!DNL Firefox], 및 [!DNL Edge].
title: 내 브라우저에서 혼합 콘텐츠를 활성화하는 방법
feature: Visual Experience Composer (VEC)
exl-id: a2209af6-65e5-427e-b2cb-53b803728ef3
source-git-commit: c5b43faa2fc55c2c8737e586cfdfaa1444a05880
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 64%

---

# 브라우저에서 혼합 콘텐츠 사용

혼합 콘텐츠는 초기 요청이 HTTPS에서는 안전하지만 HTTPS *및* HTTP 콘텐츠가 로드되어 웹 페이지를 표시하는 경우 발생합니다. HTTPS 콘텐츠는 안전합니다. HTTP 콘텐츠는 불안전합니다.

최신 브라우저는 보안 콘텐츠가 비보안 콘텐츠와 혼합된 경우 페이지 표시를 차단하거나 경고 메시지를 표시할 수 있습니다.

경고 메시지는 [!DNL Adobe Target]의 [!UICONTROL 시각적 경험 작성기] (VEC)가 혼합 콘텐츠가 포함된 페이지를 열려고 할 때 표시됩니다. 이 메시지는 브라우저에서 차단을 비활성화하는 방법을 알려 줍니다. 차단을 비활성화하면 HTTP 사이트 또는 혼합 콘텐츠(HTTPS 및 HTTP)가 있는 사이트를 열 수 있습니다.

![혼합 콘텐츠 경고](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

이전에는 혼합 콘텐츠가 허용되지 않는 경우 활동을 작성할 때 3단계 안내가 있는 워크플로의 1단계에서 일부 작업을 수행할 수 있었습니다. 이제 [!DNL Target]에서는 1단계에서 작업을 수행할 수 없습니다. 이 메시지가 표시되면 활동을 계속 만들기 전에 혼합 콘텐츠를 활성화해야 합니다.

브라우저의 보안 설정이 혼합 콘텐츠 또는 비보안(HTTP) 콘텐츠가 보안(HTTPS) 페이지 또는 프레임(예: VEC)으로 로드되는 것을 차단할 수 있습니다. 브라우저의 보안 설정을 비활성화하지 않으려면 HTTPS 웹 사이트가 있어야 합니다.

웹 사이트가 비보안(HTTP) 도메인에서 실행 중인 경우 VEC가 활성 혼합 콘텐츠를 로드하도록 허용해야 합니다.

>[!IMPORTANT]
>
>혼합 콘텐츠 허용은 사용자의 라이브 웹 사이트에는 영향을 주지 않고 VEC에만 영향을 줍니다.

자세한 내용은 *Mozilla Developer Network*(MDN) 웹 사이트의 [혼합 콘텐츠](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content)를 참조하십시오.

## 에서 혼합 컨텐츠 활성화 [!DNL Google Chrome] {#task_FF297A08F66E47A588C14FD67C037B3A}

보안 연결을 통해 사이트를 방문하는 경우 [!DNL Chrome] 웹 페이지의 콘텐츠가 안전하게 전송되었는지 확인합니다.

를 참조하십시오.[안전하지 않은 사이트에 대한 경고 관리](https://support.google.com/chrome/answer/99020?hl=en)Google Chrome 도움말의 &quot;.

최신 버전의 VEC를 사용하는 경우 [!DNL Chrome] (버전 79.0.3945.117 이상) 사이트 설정을 업데이트해야 합니다. 사이트 방문자는 이러한 단계를 수행할 필요가 없습니다.

1. 잠금(경고) 아이콘을 클릭한 다음 **[!UICONTROL 사이트 설정]**&#x200B;을 클릭합니다.

   ![사이트 설정](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. **[!UICONTROL 비보안 콘텐츠]**&#x200B;로 스크롤한 다음 드롭다운 목록을 사용하여 “차단(기본)”을 “허용”으로 변경합니다.

   ![비보안 콘텐츠](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. VEC 페이지를 다시 로드합니다.

## 에서 혼합 컨텐츠 활성화 [!DNL Mozilla Firefox] {#task_5448763B8DC941FD80F84041AEF0A14D}

기본적으로, [!DNL Firebox] 는 보안 및 비보안 콘텐츠를 혼합하는 페이지를 차단합니다. 을 사용하려면 이 설정을 영구적으로 변경해야 합니다. [!DNL Target]. 사이트 방문자는 이러한 단계를 수행할 필요가 없습니다.

1. Firefox에서 주소 표시줄에 `about:config`를 입력합니다.
1. 다음에서 표시되는 경고 메시지 확인 [!DNL Firefox].

   ![Firefox 경고](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. 검색 창에서 `block_active`를 입력합니다.

   ![Firefox block_active 설정](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. ` **[!UICONTROL security.mixed_content.block_active_content]**`를 더블 클릭합니다.

   값이 &quot;True&quot;에서 &quot;False&quot;로 변경됩니다. 값이 “False”로 표시되면 끝난 것입니다.

   ![Firefox 보안](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

1. 이 설정을 변경한 후 컴퓨터를 다시 시작합니다.

## 에서 혼합 컨텐츠 활성화 [!DNL Microsoft Edge]

보안 연결을 통해 사이트를 방문하는 경우 [!DNL Edge] 웹 페이지의 콘텐츠가 안전하게 전송되었는지 확인합니다.

최신 버전의 VEC를 사용하는 경우 [!DNL Edge], 사이트 설정을 업데이트해야 합니다. 사이트 방문자는 이러한 단계를 수행할 필요가 없습니다.

1. 위치 [!DNL Edge], 클릭 **[!DNL Microsoft Edge]** 메뉴 모음에서 **[!UICONTROL 설정]**&#x200B;을 클릭한 다음 을 클릭합니다 **쿠키 및 사이트 권한**.

1. 다음으로 스크롤 **[!UICONTROL 비보안 콘텐츠]**.

1. 클릭 **[!UICONTROL 비보안 콘텐츠]**&#x200B;을 클릭한 다음 을 클릭합니다 **[!UICONTROL 추가]** 다음에 **[!UICONTROL 허용]**&#x200B;비보안 콘텐츠를 허용할 사이트를 추가한 다음 을 클릭합니다. **[!UICONTROL 추가]**.

1. VEC 페이지를 다시 로드합니다.
