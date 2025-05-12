---
keywords: 호스트;호스트 그룹;문제 해결;우수 사례;ubox;리디렉션;리디렉션;목록;허용 목록;차단 목록;차단 목록;허용 목록 차단 목록에 추가하다
description: Adobe Target에서 간편한 관리 및 개별 보고를 위해 웹 사이트 및 사전 프로덕션 환경을 구성하는 방법에 대해 알아봅니다.
title: 호스트는 무엇이며 어떻게 사용할 수 있습니까?
feature: Administration & Configuration
role: Admin
exl-id: 31c661c0-686d-440e-ad58-864fb853b1c4
source-git-commit: 0ab5b7d7cbfaef86b9a045883f597900dba72416
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 17%

---

# 호스트

[!DNL Adobe Target]에서 쉽게 관리하고 개별적으로 보고하도록 사이트 및 사전 프로덕션 환경을 구성하십시오.

호스트 관리의 기본 목적은 비활성화 상태 컨텐츠가 실수로 웹 사이트에 나타나지 않도록 하는 것입니다. 호스트 관리를 사용하면 보고서 데이터를 [환경](/help/main/administrating-target/environments.md)별로 구분할 수도 있습니다.

호스트는 [!DNL Target] 요청이 수행된 모든 도메인입니다. 웹 사이트에서는 일반적으로 [!DNL Target]을(를) 요청하는 URL의 `location.hostname` 속성입니다.

기본적으로 [!DNL Target]은(는) [!DNL Target]개의 요청을 하고 [!DNL Target]개의 응답을 받을 수 있는 호스트를 제한하지 않습니다. 새 호스트가 요청을 수행하면 자동으로 작동합니다. 이 프로세스를 통해 알 수 없거나 예상할 수 없는 다른 도메인에서 테스트할 수도 있습니다. 이 기본 동작을 재정의하려는 경우 허용 목록에 추가하다 차단 목록에 추가하다 작업을 재정의하거나 재정의하여 [!DNL Target]을(를) 사용하는 호스트를 제한하도록 설정할 수 있습니다.

{{permissions-update}}

호스트를 관리하려면 **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**&#x200B;을(를) 클릭합니다.

## 호스트 인식 {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

호스트를 인식하고 [!UICONTROL Hosts] 목록에 추가하려면 다음 조건을 충족해야 합니다.

* 호스트에 하나 이상의 [!DNL Target] 요청이 있어야 합니다.
* 호스트의 페이지에는 다음 항목이 있어야 합니다.

   * 정확한 at.js 참조
   * [!DNL Target] 요청 또는 자동 생성된 글로벌 [!DNL Target] 요청

* [!DNL Target] 요청이 있는 페이지는 브라우저에서 봐야 합니다.

페이지를 본 후 호스트가 [!UICONTROL Hosts] 목록에 나열되므로 이를 환경에서 관리하고 활동 및 테스트를 미리 보고 시작할 수 있습니다.

>[!NOTE]
>
>여기에는 개인 개발 서버가 모두 포함됩니다.

호스트가 [!UICONTROL Host] 목록에 추가되면 호스트가 인식되는지 확인하십시오.

1. **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**&#x200B;을(를) 클릭합니다.
1. 해당 호스트가 나열되지 않으면 브라우저를 새로 고치십시오.

   기본적으로 새로 인식된 호스트는 [!UICONTROL Production] 환경에 배치됩니다. [!UICONTROL Production] 환경은 이러한 호스트에서 비활성 활동을 볼 수 없기 때문에 가장 안전한 환경입니다.

1. (조건부) 호스트를 [!UICONTROL Development], [!UICONTROL Staging] 또는 다른 환경으로 이동하려면 **[!UICONTROL Move]** 아이콘(![이동 아이콘](/help/main/assets/icons/MoveTo.svg))을 클릭합니다.

>[!NOTE]
>
>[!UICONTROL Production] 환경은 이름을 바꾸더라도 삭제할 수 없습니다. 이 환경은 마지막 활성 활동 및 테스트를 수행하는 환경이라고 가정합니다. 기본 환경은 비활성 상태 캠페인을 보도록 허용하지 않습니다.

## 호스트 목록 정렬 또는 검색 {#section_068B23C9D8224EB78BC3B7C8580251B0}

[!UICONTROL Hosts] 목록을 정렬하려면 열 머리글([!UICONTROL Name], [!UICONTROL Environment] 또는 [!UICONTROL Last Requested])을 클릭하여 목록을 오름차순 또는 내림차순으로 정렬하십시오.

[!UICONTROL Hosts] 목록을 검색하려면 [!UICONTROL Search Hosts] 상자에 검색어를 입력하십시오.

## [!DNL Target] 요청을 [!DNL Target]&#x200B;(으)로 보내도록 승인된 호스트를 지정하는 허용 목록을 만듭니다. {#allowlist}

[!DNL Target]개의 요청을 [!DNL Target]에 보내도록 승인된 호스트(도메인)를 지정하는 허용 목록에 추가하다를 만들 수 있습니다. 요청을 생성하는 다른 모든 호스트는 주석 처리된 인증 오류 응답을 받게 됩니다. 기본적으로 [!DNL Target] 요청이 포함된 모든 호스트는 [!UICONTROL Production] 환경에서 [!DNL Target]에 등록되며 모든 활성 상태의 승인된 활동에 액세스할 수 있습니다. 이 방법을 원하지 않는 경우 대신 허용 목록에 추가하다를 사용하여 [!DNL Target]개의 요청을 하고 [!DNL Target]개의 콘텐츠를 수신할 수 있는 특정 호스트를 기록할 수 있습니다. 모든 호스트는 [!UICONTROL Hosts] 목록에 계속 표시되며, 환경은 여전히 이러한 호스트를 그룹화하고 호스트에 활성 및/또는 비활성 활동을 볼 수 있는지 여부와 같이 각 호스트에 다른 수준을 할당하는 데 사용할 수 있습니다.

허용 목록에 추가하다를 만들려면:

1. [!UICONTROL Hosts] 목록에서 **[!UICONTROL Authorize Hosts]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Enable Authorized Hosts for content delivery]** 토글을 사용하도록 설정합니다.
1. 원하는 대로 **[!UICONTROL Host contains]** 상자에 원하는 호스트를 추가합니다.

   여러 호스트가 각각 고유한 행에 나열될 수 있습니다.

1. 원하는 대로 **[!UICONTROL Host does not contains]** 상자에 원하는 호스트를 추가합니다.

   여러 호스트가 각각 고유한 행에 나열될 수 있습니다.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

승인되지 않은 호스트에서 [!DNL Target] 요청이 수행된 경우 호출이 `/* no display - unauthorized mbox host */`(으)로 응답합니다.

>[!IMPORTANT]
>
>**보안 모범 사례**: [!DNL Target]을(를) 사용하는 경우 이 허용 목록에 추가하다의 ubox 기능은 [리디렉터](https://experienceleague.adobe.com/docs/target-dev/developer/implement-email/working-with-redirectors.html?lang=ko){target=_blank}가 탐색할 수 있는 도메인 목록도 제어합니다. ubox를 구현의 일부로 사용할 때 리디렉션할 도메인을 추가해야 합니다. 허용 목록에 추가하다를 지정하지 않고 [!DNL Adobe]을(를) 지정하지 않으면 리디렉션 URL을 확인할 수 없습니다.
>
>허용 목록이 환경보다 우선합니다. 허용 목록에 추가하다 기능을 사용하기 전에 허용 목록에 추가하다에서 허용된 호스트를 모두 지운 다음 호스트 목록에 만 나타납니다. 그런 후 호스트를 원하는 환경으로 이동할 수 있습니다.

다른 사이트의 도메인이 환경에 표시되는 경우가 있습니다. 도메인이 at.js를 호출하면 목록에 표시됩니다. 예를 들어 웹 페이지 중 하나를 서버로 복사하면 해당 도메인이 환경에 표시됩니다. 스파이더 엔진, 언어 번역기 사이트 또는 로컬 디스크 드라이브에서 도메인을 볼 수도 있습니다.

`mboxHost`가 API 호출에서 전달되는 경우 전달된 환경에 대해 전환이 기록됩니다. 환경이 전달되지 않으면 호출에 있는 호스트의 기본값이 [!UICONTROL Production]&#x200B;(으)로 설정됩니다.

[!UICONTROL Host Does Not Contain] 상자에서 원하는 호스트를 추가하여 [!DNL Target]에 [!DNL Target] 요청을 보낼 수 없는 호스트(도메인)를 지정하는 차단 목록에 추가하다를 만들 수도 있습니다.

>[!NOTE]
>
>[!UICONTROL Authorized Hosts] 목록은 [!DNL Target] 호스트와 기본 리디렉션 호스트 모두에 사용됩니다. [!DNL Adobe Target] JavaScript SDK(at.js) *및* ubox 기본 리디렉션 URL에 사용된 모든 도메인을 사용하도록 승인된 기존 도메인을 모두 추가합니다. 향후 새로운 유사한 도메인을 허용 목록에 추가하다에 추가합니다.

## 호스트 삭제 {#section_F56355BA4BC54B078A1A8179BC954632}

더 이상 필요하지 않은 호스트를 삭제할 수 있습니다.

1. [!UICONTROL Hosts] 목록에서 **[!UICONTROL Delete]** 아이콘(![삭제 아이콘](/help/main/assets/icons/DeleteOutline.svg))을 클릭합니다.
1. **[!UICONTROL Delete]**&#x200B;을(를) 클릭하여 삭제를 확인합니다.

>[!NOTE]
>
>호스트에서 [!DNL Target] 요청이 포함된 페이지로 이동하면 호스트가 다시 나열됩니다.

## 호스트 문제 해결 {#concept_B3D7583FA4BB480382CC7453529FE1B7}

호스트에 문제가 발생하는 경우 다음의 문제 해결 팁을 사용해 보십시오.

**계정의 목록에 호스트가 표시되지 않습니다.**

* 브라우저에서 [!UICONTROL Hosts] 페이지를 새로 고칩니다.
* at.js 참조를 포함한 [!DNL Target] 요청이 올바른지 확인하십시오.
* 호스트에서 [!DNL Target]개 요청 중 하나를 검색해 보십시오. 브라우저에서 호스트의 [!DNL Target] 요청이 렌더링되지 않았을 수 있습니다.

**무작위 또는 알 수 없는 도메인이 [!UICONTROL Host] 목록에 나타납니다.**

도메인에서 [!DNL Target]에 대한 요청이 있는 경우 도메인이 이 목록에 표시됩니다. 대체로 스파이더 엔진, 언어 번역기 사이트 또는 로컬 디스크 드라이브에서 도메인을 볼 수 있습니다. 나열된 도메인이 팀에서 사용하는 도메인이 아닌 경우 [!UICONTROL Delete]을(를) 클릭하여 제거할 수 있습니다.

**내 [!DNL Target] 요청이 /&#42; no display - unauthorized mbox host &#42;/.** 반환

승인되지 않은 호스트에서 [!DNL Target] 요청이 수행된 경우, 이 요청은 /&#42; no display - unauthorized mbox host &#42;/(으)로 응답합니다.
