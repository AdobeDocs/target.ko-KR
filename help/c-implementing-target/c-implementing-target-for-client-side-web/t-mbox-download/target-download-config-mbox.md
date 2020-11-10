---
keywords: Implementation;Mbox;mbox.js;download mbox.js;configure mbox.js
description: Target Standard 및 Premium은 수정된 버전의 Adobe Target mbox.js 파일을 사용합니다.
title: mbox.js 다운로드
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 94%

---


# mbox.js 다운로드{#download-mbox-js}를 참조하십시오.

Target Standard 및 Premium은 수정된 버전의 Adobe Target mbox.js 파일을 사용합니다.

[!DNL Adobe Target][!UICONTROL  시각적 경험 편집기]를 사용하려면 추가 자바스크립트 줄을 [!DNL mbox.js] 파일의 일부로 포함해야 합니다.

1. 에서 **[!UICONTROL 관리]** > **[!UICONTROL 구현을]** 클릭합니다 [!DNL Target Standard].
1. **[!UICONTROL mbox.js 다운로드]**&#x200B;를 클릭하고 프롬프트에 따라 파일을 저장합니다.
1. (조건부) [!DNL mbox.js] 버전 60 이상을 사용하는 경우, mbox가 로드되어 응답형 사이트에서 깜박임이 줄어들 때까지 기본적으로 페이지 컨텐츠를 자동으로 숨기도록 라이브러리를 구성할 수 있습니다.

   자세한 내용은 [mbox.js 고급 설정](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/advanced-mboxjs-settings.md#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C)에서 &quot;페이지 로드 플리커 억제&quot;를 참조하십시오.

1. 웹 사이트에서 [!DNL mbox.js] 참조를 만듭니다.

   [!DNL mbox.js] 버전 57부터 [!DNL mbox.js] 참조를 페이지의 `<head>` 섹션 내 어디에나 배치할 수 있습니다.

   >[!IMPORTANT]
   >
   >57 이전 버전의 [!DNL mbox.js]를 사용하는 경우 해당 참조가 페이지의 `<head>` 섹션에서 마지막 항목이어야 합니다. 참조가 마지막 항목이 아닌 경우에는 심각한 표시 또는 성능 문제가 발생할 수 있습니다. 자세한 [내용은 mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-technical.md) 작업을 참조하십시오.

1. 저장된 [!DNL mbox.js] 파일을 코드에서 지정한 호스팅 환경의 위치로 업로드합니다.
