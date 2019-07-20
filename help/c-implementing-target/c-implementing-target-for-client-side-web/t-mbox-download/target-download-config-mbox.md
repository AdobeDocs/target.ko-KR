---
description: Target Standard 및 Premium은 수정된 버전의 Adobe Target mbox.js 파일을 사용합니다.
keywords: 구현;Mbox;mbox.js;mbox.js 다운로드;mbox.js 구성
seo-description: Target Standard 및 Premium은 수정된 버전의 Adobe Target mbox.js 파일을 사용합니다.
seo-title: mbox.js 다운로드
solution: Target
subtopic: 시작하기
title: mbox.js 다운로드
topic: Standard
uuid: b2a46321-cac7-4924-92dd-a80b50e27cee
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# mbox.js 다운로드{#download-mbox-js}를 참조하십시오.

Target Standard 및 Premium은 수정된 버전의 Adobe Target mbox.js 파일을 사용합니다.

[!DNL Adobe Target][!UICONTROL  시각적 경험 편집기]를 사용하려면 추가 자바스크립트 줄을 [!DNL mbox.js] 파일의 일부로 포함해야 합니다.

1. [!DNL Target Standard]에서 **[!UICONTROL 설정]** &gt; **[!UICONTROL 구현]**&#x200B;을 클릭합니다.
1. **[!UICONTROL mbox.js 다운로드]**&#x200B;를 클릭하고 프롬프트에 따라 파일을 저장합니다.
1. (조건부) [!DNL mbox.js] 버전 60 이상을 사용하는 경우, mbox가 로드되어 응답형 사이트에서 깜박임이 줄어들 때까지 기본적으로 페이지 컨텐츠를 자동으로 숨기도록 라이브러리를 구성할 수 있습니다.

   자세한 내용은 [mbox.js 고급 설정](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/advanced-mboxjs-settings.md#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C)에서 "페이지 로드 플리커 억제"를 참조하십시오.

1. 웹 사이트에서 [!DNL mbox.js] 참조를 만듭니다.

   [!DNL mbox.js] 버전 57부터 [!DNL mbox.js] 참조를 페이지의 `<head>` 섹션 내 어디에나 배치할 수 있습니다.

   >[!IMPORTANT]
   >
   >57 이전 버전의 [!DNL mbox.js]를 사용하는 경우 해당 참조가 페이지의 `<head>` 섹션에서 마지막 항목이어야 합니다. 참조가 마지막 항목이 아닌 경우에는 심각한 표시 또는 성능 문제가 발생할 수 있습니다. 자세한 내용은 [기술 구현 세부 사항](https://marketing.adobe.com/resources/help/en_US/target/ov/c_mbox_technical.html)을 참조하십시오.

1. 저장된 [!DNL mbox.js] 파일을 코드에서 지정한 호스팅 환경의 위치로 업로드합니다.
