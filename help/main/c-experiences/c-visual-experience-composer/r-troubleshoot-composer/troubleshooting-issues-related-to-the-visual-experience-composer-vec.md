---
keywords: 타깃팅;시각적 경험 작성기;vec;시각적 경험 작성기 문제 해결;문제 해결;tls;tls 1.2
description: Adobe에서 가끔 발생하는 문제를 해결하는 방법을 알아봅니다 [!DNL Target] 특정 조건에서 VEC(시각적 경험 작성기)를 참조하십시오.
title: 시각적 경험 작성기와 관련된 문제를 해결하려면 어떻게 해야 합니까?
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
source-git-commit: ed6b1ef266f2e26cd80b6fa5099a42f6031448b5
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 78%

---

# 시각적 경험 작성기에 관련된 문제 해결

에서 경우에 따라 문제가 발생합니다 [!DNL Adobe Target] [!UICONTROL 시각적 경험 작성기] (VEC) 를 사용할 수 있습니다.

## 시각적 경험 작성기에서 웹 사이트를 열면 [!DNL Target] 라이브러리가 로드되지 않습니다. (VEC만 해당) {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

Target은 시각적 경험 작성기에서 웹 사이트를 열 때 두 개의 매개 변수(`mboxEdit=1` 및 `mboxDisable=1`)를 추가합니다.

한 페이지에서 다른 페이지로 이동할 때(페이지 다시 로드 없이) 웹 사이트(특별히 단일 페이지 앱)가 매개 변수를 자르거나, 실제로 매개 변수를 제거할 경우 Target 기능이 중단되고 Target 라이브러리가 로드되지 않습니다.
이 문제점을 방지하려면 이러한 두 매개 변수를 자르거나 제거하지 않아야 합니다.

## 내 페이지가 EEC에서 열리지 않거나 느리게 로드됩니다. VEC에서 활동 또는 경험이 느리게 로드됩니다. (VEC만 해당) {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

몇 가지 문제가 Target 경험 작성기의 페이지 성능에 영향을 줄 수 있습니다. 일반적인 몇 가지 문제는 다음과 같습니다.

* 페이지에 mbox가 없습니다.
* 사이트가 프록시 차단을 사용하여 어떤 경험 작성기에서도 페이지를 열 수 없습니다.
* 사이트가 자체적으로 iFrame에서 열리는 것을 허용하지 않습니다.

고급 경험 작성기에서 문제가 발생할 경우 고급 경험 작성기를 끄고 시각적 경험 작성기를 대신 사용합니다.

고급 경험 작성기를 비활성화하려면 **[!UICONTROL 관리]** > **[!UICONTROL 시각적 경험 작성기]** 꺼서 **[!UICONTROL 고급 경험 작성기 활성화]** 선택 사항입니다.

일부 사용자의 경우 콘솔에 다음과 같은 오류 메시지가 표시됩니다.

![콘솔 오류 메시지](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

시각적 경험 작성기와 고급 경험 작성기가 둘 다 작동하지 않으면 Requestly(Chrome 또는 Firefox) 또는 사이트에 대한 X-Frames 헤더 옵션을 덮어쓸 수 있는 응답 헤더 수정(Firefox)과 같은 브라우저 확장을 사용하고, iFrames에서 로드되도록 하여 VEC를 활성화하십시오. 브라우저 확장을 사용할 수 없는 경우 양식 작성기를 사용하십시오.

>[!NOTE]
>
>다음 정보 외에 Google Chrome용 [Adobe Target VEC Helper 브라우저 확장 프로그램](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)을 사용할 수 있습니다.


>[!NOTE]
>
>이러한 플러그인은 VEC 편집 컨텍스트에서만 사용해야 합니다.
>
>Requestly 확장 프로그램의 경우 헤더를 제거해야 할 때마다 다음 중 하나를 수행해야 합니다.
>
>* 해당 URL에 대해서만 헤더가 제거되도록 VEC에서 열려고 하는 URL에 대한 URL 규칙을 추가하십시오.
>
>* VEC에서 편집할 때 규칙을 활성화하고 VEC를 사용하지 않을 때 규칙을 비활성화하십시오.
>
>응답 헤더 수정 확장 프로그램(Firefox)의 경우 URL 규칙을 추가할 수 없으므로 다음을 수행해야 합니다.
>
>* VEC에서 편집할 때 규칙을 활성화하고 VEC를 사용하지 않을 때 규칙을 비활성화하십시오.


**Chrome 또는 Firefox에서 Requestly 확장을 사용하려면**

1. 고급 경험 작성기를 끕니다.
1. Chrome 또는 Firefox에 Requestly 브라우저 확장을 설치합니다.
1. 확장을 열고 다음을 사용하여 구성합니다.
1. **[!UICONTROL 헤더 수정을 선택합니다]**.
1. 다음을 입력하십시오.

   * 규칙 이름
   * 수정 규칙

      * **[!UICONTROL 추가]**&#x200B;에서 **[!UICONTROL 제거]**&#x200B;로 전환합니다.
      * **[!UICONTROL 요청]**&#x200B;에서 **[!UICONTROL 응답]**&#x200B;으로 전환합니다.
      * 헤더 이름으로 &quot;X-Frame-Options&quot;를 입력합니다.
      * 이전 단계를 반복하고 헤더 이름으로 &quot;x-frame-options&quot;를 입력합니다.

         >[!NOTE]
         >
         >Requestly를 통해 조작되는 헤더는 대/소문자를 구분합니다.

      * 소스 URL에 대한 조건으로 **[!UICONTROL 다음과 같음]**&#x200B;을 **[!UICONTROL 포함]**&#x200B;으로 변경하고, VEC에 로드하려는 활동의 URL을 입력합니다.

      ![chrome_extension 이미지](assets/chrome_extension.png)


1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![요청 이미지](assets/requestly.png)

   이제 시각적 경험 작성기로 페이지를 빠르게 로드할 수 있습니다.

**Firefox에서 응답 헤더 수정 확장을 사용하려면 다음을 수행합니다.**

1. Firefox에서 응답 헤더 수정을 설치하고 브라우저를 다시 시작하십시오.
1. Firefox 확장에서 응답 헤더 수정 확장을 선택하십시오.
1. **[!UICONTROL 기본 설정을 클릭합니다]**.
1. 작업 드롭다운에서 **[!UICONTROL 필터]**&#x200B;를 선택합니다.
1. 헤더 이름 필드에 **[!UICONTROL X-Frame-Options를 입력합니다]**.
1. 4~5단계를 반복하고 **[!UICONTROL X-Frame-Options를 사용하여 필터를 추가합니다]**.
1. **[!UICONTROL 추가를 클릭합니다]**.
1. **[!UICONTROL 시작을 클릭합니다]**.

![firefox_extension 이미지](assets/firefox_extension.png)

확장을 설정한 후 Target을 엽니다. 이제 고급 경험 작성기가 비활성화되더라도 페이지가 시각적 경험 작성기에 로드됩니다.

## VEC(VEC 전용)에 내 페이지가 표시되지 않습니다. {#does-not-load}

* 브라우저가 지원되지 않습니다.
* 브라우저가 보안 사이트에서 비보안 페이지를 차단하고 있습니다.

   브라우저 주소 표시줄에서 URL 왼쪽에 있는 아이콘을 클릭하고 **[!UICONTROL 이 페이지에서 보호 비활성화를 클릭합니다.]**
* 올바르지 않은 URL을 입력했습니다.
* 계정 설정 페이지에 기본 URL을 입력하지 않았습니다.

   이 설정이 활성화되어 있는지 확인한 다음, 웹 사이트에서 at.js를 다운로드하여 업데이트하십시오.

* 를 사용해 보면 [새 [!UICONTROL 시각적 편집 도우미] 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) 그리고 다시 [이전 확장](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) 및 [!DNL Target] 웹 사이트를 로드하지 못하고 모든 브라우저 데이터를 지우고 새 확장을 비활성화합니다.

* 웹 사이트가 VEC에서 로드되지 않거나 예기치 않게 동작하는 경우 웹 사이트를 로드하기 전에 브라우저에서 웹 사이트에서 쿠키를 허용하는 것이 잠재적 수정 사항입니다 [!DNL Target].

## 찾아보기 모드를 사용할 때 VEC가 손상된 것으로 나타납니다. (VEC만 해당) {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

찾아보기 모드를 사용하는 동안 target.js가 없거나 frame-buster 헤더를 포함하는 URL에 액세스하면 시각적 경험 작성기가 중단된 것으로 나타납니다. 브라우저 보안 때문에, Target이 탐색한 URL에 액세스할 수 없습니다.
