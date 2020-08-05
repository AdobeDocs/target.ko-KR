---
description: 모든 경험의 유효성을 확인할 수 있도록 Target 브라우저 쿠키를 삭제합니다.
title: Adobe Target 쿠키 삭제
topic: Standard
uuid: 6e95ee4d-dbf2-4432-8abe-cfd9bc928f0c
translation-type: tm+mt
source-git-commit: 79bcd452a9faa0883272d2e686efd7c4ddfa34a2
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---


# Target 쿠키 삭제{#delete-the-target-cookie}

테스트하는 동안 모든 경험의 유효성을 검사할 수 있도록 [!DNL Target] 브라우저 쿠키(mbox)를 삭제할 수 있습니다.

If there is no [!DNL Target] cookie (mbox), you are considered a new visitor and shown a new experience. There are several ways to delete your [!DNL Target] cookies without deleting all of your browser cookies.

>[!NOTE]
>
>나열된 브라우저 및 버전에 대해 다음 지침이 올바릅니다. 특정 브라우저 또는 버전에 대한 지침을 인터넷에서 검색합니다.

## Google Chrome에서 Target 쿠키 삭제

버전 84.0.4147.105

1. Chrome **메뉴** > 환경 설정을 **클릭합니다**.
1. 개인 **정보 및 보안** 탭을 클릭합니다.
1. 쿠키 **및 기타 사이트 데이터를 클릭합니다**.
1. 모든 쿠키 및 사이트 데이터 **보기를 클릭합니다**.
1. 섹션을 `adobe.com` 확장하고 **mbox** 쿠키를 선택한 다음 삭제 아이콘(X)을 클릭합니다.

## Mozilla Firefox에서 Target 쿠키 삭제

버전 79.0

1. Firefox **메뉴** > 환경 설정을 **클릭합니다**.
1. 개인 **정보 및 보안** 탭을 클릭합니다.
1. 쿠키 **및 사이트 데이터에서**&#x200B;데이터 **관리를 클릭합니다**.
1. 사이트를 `adobe.com` 선택한 다음 선택한 항목 **제거를 클릭합니다**.

   >[!NOTE]
   >
   >사이트와 연관된 모든 쿠키가 `adobe.com` 삭제됩니다. 사이트에 대한 개별 쿠키를 삭제하거나 편집하려면 개발자 도구의 [저장소 관리자에서 쿠키를 삭제할 수 있습니다](https://developer.mozilla.org/en-US/docs/Tools/Storage_Inspector). 삭제할 특정 쿠키의 이름은 &quot;mbox&quot;입니다.

## Microsoft Edge에서 Target 쿠키 삭제

버전 84.0.522.52

1. Microsoft **Edge** 메뉴 > 환경 설정을 **클릭합니다**.
1. Click the **Site Permissions** tab.
1. 쿠키 **및 사이트 데이터를 클릭합니다**.
1. 모든 쿠키 및 사이트 데이터 **보기를 클릭합니다**.
1. 섹션을 `adobe.com` 확장하고 **mbox** 쿠키를 선택한 다음 삭제 아이콘(X)을 클릭합니다.

## Apple Safari에서 Target 쿠키 삭제

버전 13.1.2

1. Safari **메뉴** > 환경 설정을 **클릭합니다**.
1. Click the **Privacy** tab.
1. 웹 사이트 **데이터 관리를 클릭합니다**.
1. 삭제할 쿠키의 사이트를 선택한 다음 **제거를 클릭합니다**.

>[!NOTE]
>
>사이트와 연관된 모든 쿠키가 `adobe.com` 삭제됩니다. 사이트에 대한 개별 쿠키를 삭제하려면 아래 지침을 따르십시오.

1. Safari **메뉴** > 환경 설정을 **클릭합니다**.
1. Click the **Advanced** tab.
1. 메뉴 모음에서 **현상 표시 메뉴** 옵션을 선택합니다.
1. 삭제할 쿠키가 있는 웹 페이지로 이동합니다.
1. 현상 **메뉴** > 웹 **검사기 표시를 클릭합니다**.
1. Click the **Storage** tab.
1. 쿠키 **섹션을** 확장한 다음 을 클릭합니다 `www.adobe.com`.
1. mbox 쿠키를 마우스 오른쪽 단추로 **클릭한** 다음 **삭제를 클릭합니다**.