---
keywords: 사이트 페이지;타겟 사이트 페이지;타깃팅;현재 페이지;타겟 현재 페이지;이전 페이지;타겟 이전 페이지;랜딩 페이지;타겟 랜딩 페이지;http 헤더
description: 사이트의 특정 페이지에 있는  [!DNL Adobe Target] 명을 사용하여 방문자를 타깃팅하는 방법에 대해 알아봅니다.
title: 사이트 페이지에 따라 방문자를 타깃팅할 수 있습니까?
feature: Audiences
exl-id: 4c770b7b-775f-4483-aced-43f18a9a68c1
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 19%

---

# 사이트 페이지

사이트의 특정 페이지에 액세스하는 [!DNL Adobe Target]을(를) 사용하여 방문자를 타깃팅할 수 있습니다.

1. [!DNL Target] 인터페이스에서 **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**&#x200B;을(를) 클릭합니다.
1. 대상자의 이름을 지정하고 선택적 설명을 추가합니다.
1. **[!UICONTROL Site Pages]**&#x200B;을(를) 대상 빌더 창으로 끌어서 놓습니다.

   ![사이트 페이지 대상자](assets/target_site_pages.png)

1. **[!UICONTROL Select]** 드롭다운 목록을 클릭하고 다음 옵션 중 하나를 선택한 다음 원하는 대로 규칙을 구성합니다.

   규칙의 후속 드롭다운 목록에서 사용할 수 있는 옵션 및 평가자는 선택하는 옵션에 따라 달라집니다. 다음 그림은 [!UICONTROL Current Page]을(를) 선택하는 경우 사용할 수 있는 옵션을 보여 줍니다.

   ![현재 페이지](assets/current-page.png)

   [!UICONTROL Select]을(를) 선택하면 초기 드롭다운 목록에서 다음 옵션을 사용할 수 있습니다.

   * **[!UICONTROL Current Page]:** 사용자가 보고 있는 페이지입니다.

     이 옵션을 선택하는 경우 두 번째 드롭다운 목록에서 다음 옵션을 사용할 수 있습니다.

      * [!UICONTROL URL]&#x200B;([!DNL Target]이(가) URL을 평가하는 방법에 대한 자세한 내용은 [대상 및 대상 FAQ](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md)를 참조하십시오.)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]
      * [!UICONTROL Hash (#) fragment]

   * **[!UICONTROL Previous Page]:** 현재 페이지를 클릭하기 전에 사용자가 본 페이지입니다. 페이지를 추적하려면 이전 페이지에서 현재 페이지까지 클릭해야 합니다. 사용자가 브라우저에서 새 URL을 입력하면 이전 페이지가 추적되지 않습니다. 이 페이지의 실제 내용은 사이트의 디자인에 따라 다릅니다. 예를 들어 현재 페이지에 특정 제품에 대한 정보가 표시되면 이전 페이지는 방문자가 특정 항목을 선택하는 카테고리 페이지일 수 있습니다. 예를 들어 특정 유형의 여러 카메라를 표시하는 페이지이거나 최종 페이지로 이어지는 홈 페이지일 수 있습니다.

     이 옵션을 선택하는 경우 두 번째 드롭다운 목록에서 다음 옵션을 사용할 수 있습니다.

      * [!UICONTROL URL]&#x200B;(Target에서 URL을 평가하는 방법에 대한 자세한 내용은 [Target 및 대상 FAQ](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md)를 참조하십시오.)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]

   * **[!UICONTROL Landing Page]:** 랜딩 페이지는 사이트에 액세스할 때 방문자가 보는 첫 페이지입니다. 예를 들어 방문자가 범주 페이지로 이동하는 Google에 대한 링크를 클릭하는 경우 범주 페이지는 랜딩 페이지입니다. 링크가 홈페이지로 이동하는 경우 홈페이지는 랜딩 페이지입니다. 랜딩 페이지는 방문자의 세션을 기억합니다. 방문자의 랜딩 페이지가 이 세션에 있었던 것을 기준으로 더 깊이 타깃팅할 수 있습니다.

     이 옵션을 선택하는 경우 두 번째 드롭다운 목록에서 다음 옵션을 사용할 수 있습니다.

      * [!UICONTROL URL]&#x200B;(Target에서 URL을 평가하는 방법에 대한 자세한 내용은 [Target 및 대상 FAQ](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md)를 참조하십시오.)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]
      * [!UICONTROL Hash (#) fragment]

     >[!NOTE]
     >
     >`landing.url` 개체는 하위 도메인 변경 시 또는 직접적인 URL 대체 시 재설정됩니다.

   * **[!UICONTROL HTTP Header]:** 이 옵션은 [!DNL Target] 요청의 HTTP 헤더에 있는 정보를 평가합니다. 예를 들어 HTTP 헤더에 언어 정보가 포함된 경우 스페인어로 페이지에 액세스하는 방문자를 타깃팅하기 위해 `Accept-Language: es` 조건을 포함하는 규칙을 만들 수 있습니다.

     이 옵션을 선택하는 경우 두 번째 드롭다운 목록에서 다음 옵션을 사용할 수 있습니다.

      * [!UICONTROL Accept]
      * [!UICONTROL Accept-Charset]
      * [!UICONTROL Accept-Encoding]
      * [!UICONTROL Accept-Language]
      * [!UICONTROL Authorization]
      * [!UICONTROL Cache-Control]
      * [!UICONTROL Connection]
      * [!UICONTROL Content-Length]
      * [!UICONTROL Content-MDS]
      * [!UICONTROL Content-Type]
      * [!UICONTROL Date]
      * [!UICONTROL Expect]
      * [!UICONTROL From]
      * [!UICONTROL Host]
      * [!UICONTROL If-Match]
      * [!UICONTROL If-Modified-Since]
      * [!UICONTROL If-None-Match]
      * [!UICONTROL If-Range]
      * [!UICONTROL If-Unmodified-Since]
      * [!UICONTROL Max-Forwards]
      * [!UICONTROL Pragma]
      * [!UICONTROL Proxy-Authorization]
      * [!UICONTROL Range]
      * [!UICONTROL Referrer]
      * [!UICONTROL TE]
      * [!UICONTROL Upgrade]
      * [!UICONTROL User-Agent]
      * [!UICONTROL Via]
      * [!UICONTROL Warning]

   [!UICONTROL Current Page], [!UICONTROL Previous Page] 또는 [!UICONTROL Landing Page]을(를) 선택한 경우 [!UICONTROL Domain] 및 [!UICONTROL Query] 옵션을 사용할 수 있습니다. 이러한 옵션을 선택할 때는 다음 사항을 고려하십시오.

   * **도메인:**&#x200B;페이지의 전체 도메인. 도메인을 지정할 때는 &quot;contains&quot;를 사용하는 것이 좋습니다. 예를 들어 &quot;Domain equals facebook.com&quot;은 `m.facebook.com` 또는 `www.facebook.com`을(를) 허용하지 않습니다. &quot;Domain contains facebook.com&quot;은 모든 변형 facebook.com을 허용합니다.
   * **쿼리:** 첫 번째 물음표(?) 다음의 URL 콘텐츠입니다.

     `foo.html?e0a72cb2a2c7`

1. (선택 사항) 대상에 대한 추가 규칙을 설정합니다.
1. **[!UICONTROL Done]** 아이콘을 클릭합니다.

자신만의 &quot;사용자 정의 쿼리 매개 변수&quot; 또는 &quot;사용자 정의 헤더&quot;를 사용하여 사이트 페이지 대상을 만들 수도 있습니다.

아래 그림과 같이

* 사용자가 선택한 규칙이 [!UICONTROL Current Page], [!UICONTROL Landing Page] 또는 [!UICONTROL Previous Page]인 경우 쿼리 매개 변수
* 사용자가 선택한 규칙이 HTTP 헤더인 경우 헤더

## 문제 해결 {#ts}

* 랜딩 페이지 대상이 제대로 작동하려면 요청에 at.js JavaScript 라이브러리가 `mboxReferrer` 특성을 사용하여 페이지에서 가져오는 `context.address.referringUrl` 매개 변수 집합(배달 API의 경우 `document.referrer` 매개 변수)이 있어야 합니다. 이 `HTMLDocument` 특성은 사용자가 탐색한 페이지의 URI를 반환합니다. 이 속성의 값은 사용자가 페이지로 직접 이동할 때(링크가 아니라 책갈피 등을 통해) 빈 문자열입니다.

  이 동작이 요구 사항과 일치하지 않으면 다음 작업 중 하나를 수행하는 것이 좋습니다.

   * 타깃팅용으로 사용하려면 [mbox 매개 변수](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/global-mbox/pass-parameters-to-global-mbox.html){target=_blank}을(를) [!DNL Target]에 전달하십시오.
   * 랜딩 페이지 활동 대신 [A/B 테스트 활동](/help/main/c-activities/t-test-ab/test-ab.md)을 사용하십시오. A/B 테스트 활동은 동일한 방문자에 대한 경험을 전환하지 않습니다.
   * 대신 [방문자 프로필](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md)을 사용하십시오.

* 쉼표를 포함하는 문자열에서 &quot;다음으로 시작/다음으로 끝남&quot; 평가자를 사용할 때 이러한 문자열은 값 배열로 평가되며, 여기에서 쉼표로 구분된 각 값이 평가됩니다. 예를 들어 헤더 `Accept-Language: en,zh;q=0.9,en-IN;q=0.8,zh-CN;q=0.7`에 대한 값이 있는 경우 다음과 같은 조건에 적합합니다.
   * zh로 시작,
   * en으로 시작,
   * 0.7로 끝남,
   * 0.8로 끝남.

## 교육 비디오: 대상자 만들기

다음 비디오에는 대상 카테고리 사용에 대한 정보가 포함되어 있습니다.

* 대상자 만들기
* 대상 카테고리 정의

>[!VIDEO](https://video.tv.adobe.com/v/17392)
