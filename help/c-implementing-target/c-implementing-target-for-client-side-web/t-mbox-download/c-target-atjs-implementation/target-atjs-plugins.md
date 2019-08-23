---
description: Target 의. js 플러그인에서 지원되고 지원되지 않는 정보입니다.
keywords: at. js plugins; 지원되는 플러그인; 지원되지 않는 플러그인; ttmeta; ttmeta; Mboxtrack
seo-description: Adobe Target 용. js 플러그인에서 지원되고 지원되지 않는 정보입니다.
seo-title: at. js 플러그인 (Adobe Target 용)
solution: Target
title: at.js 플러그인
topic: Standard
uuid: ef36b2b2-bf6d-497e-b3f5-2b572a1b8a8d
translation-type: tm+mt
source-git-commit: c3afa420f33f98d7c4bb332acdef7a248fe4670a

---


# at.js plug-ins{#at-js-plug-ins}

Adobe Target 의. js 플러그인에서 지원되고 지원되지 않는 정보입니다.

많은 사용자가 [!DNL mbox.js]에 대해 사용자 지정된 플러그인 및 응답 플러그인을 빌드했습니다. 이러한 사용자 지정 플러그인은 업데이트하지 않으면 [!DNL at.js]에서 지원하지 않을 수 있습니다.

여기에 나열되지 않은 플러그인을 사용 중인데 상태를 알고 싶다면 계정 담당자에게 문의하십시오.

다음은 [!DNL at.js]와 함께 사용할 때 많은 고객이 사용하는 일부 플러그인의 현재 상태입니다.

| 플러그인 | 세부 사항 |
|--- |--- |
| mboxTrack | 지원되지 않음.<br>이 플러그인은 [adobe.target.trackEvent(선택 사항)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) 함수로 대체됩니다. 새 기능을 적용하려면 플러그인을 업데이트하십시오.<br>[통합](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md) 페이지를 참조하십시오. |
| Persistent Profile Backup Plugin(영구 프로필 백업 플러그인) | 지원되지 않음.<br>이 플러그인은 Target 프로필 라이프타임이 2주에서 90일로 연장되면서 더 이상 사용되지 않습니다. 계정의 프로필 라이프타임 설정을 확인하려면 mbox 쿠키의 만료 날짜를 확인하십시오.<br>프로필 라이프타임을 90일로 연장하려면 고객 지원팀에 문의하십시오. |
| ttMeta | Old SiteCatalyst plugins should be disabled and replaced with [Adobe Analytics as the reporting source for Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). ttMeta 플러그인은 비활성화하고 [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj)로 교체해야 합니다. |