---
keywords: 구현;Mbox;mbox.js;mbox.js 다운로드;mbox.js 구성
description: Adobe Target의 이전 mbox.js 구현에 대해 알아봅니다. Adobe Experience Platform 웹 SDK(AEP 웹 SDK) 또는 최신 at.js 버전으로 마이그레이션합니다.
title: ' [!DNL Target] mbox.js 라이브러리를 다운로드하려면 어떻게 합니까?'
feature: at.js
role: Developer
exl-id: 92096b1b-a8a5-435b-8e62-24b5d15d392f
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 74%

---

# mbox.js 다운로드

Target Standard 및 Premium은 수정된 버전의 Adobe Target mbox.js 파일을 사용합니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js로부터의 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 미칩니다.
>
>이 날짜 이전에 모든 고객이 사이트에서 발생할 수 있는 문제를 방지하기 위해 새로운 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션하는 것이 좋습니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

[!DNL Adobe Target][!UICONTROL  시각적 경험 편집기]를 사용하려면 추가 자바스크립트 줄을 [!DNL mbox.js] 파일의 일부로 포함해야 합니다.

1. [!DNL Target Standard]관리&#x200B;]**>**[!UICONTROL &#x200B;구현&#x200B;]**을 클릭합니다.**[!UICONTROL 
1. **[!UICONTROL mbox.js 다운로드]**&#x200B;를 클릭하고 프롬프트에 따라 파일을 저장합니다.
1. (조건부) [!DNL mbox.js] 버전 60 이상을 사용하는 경우, mbox가 로드되어 응답형 사이트에서 깜박임이 줄어들 때까지 기본적으로 페이지 컨텐츠를 자동으로 숨기도록 라이브러리를 구성할 수 있습니다.

1. 웹 사이트에서 [!DNL mbox.js] 참조를 만듭니다.

   [!DNL mbox.js] 버전 57부터 [!DNL mbox.js] 참조를 페이지의 `<head>` 섹션 내 어디에나 배치할 수 있습니다.

   >[!IMPORTANT]
   >
   >57 이전 버전의 [!DNL mbox.js]를 사용하는 경우 해당 참조가 페이지의 `<head>` 섹션에서 마지막 항목이어야 합니다. 참조가 마지막 항목이 아닌 경우에는 심각한 표시 또는 성능 문제가 발생할 수 있습니다.

1. 저장된 [!DNL mbox.js] 파일을 코드에서 지정한 호스팅 환경의 위치로 업로드합니다.
