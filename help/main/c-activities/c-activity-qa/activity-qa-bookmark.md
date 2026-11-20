---
keywords: qa;미리 보기;북마클릿;미리 보기 링크
description: Adobe [!DNL Target] QA 북마클릿을 사용하여 [!DNL Target]에서 QA 모드를 해제하도록 하는 방법에 대해 알아봅니다.
title: 활동 QA 북마클릿을 사용하려면 어떻게 해야 합니까?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
TQID: 'https://experienceleague.adobe.com/kOQcdF2WgiAGkOS3rrLWfDSFTvRJX8jb-IeaahWnM0c'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0a683f6e68bb7481b9e45c91a275a46b84a1ffd8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 6%
---
# 활동 QA 북마클릿 {#activity-qa-bookmarklet}

>[!BEGINSHADEBOX]

**이 페이지에서:** [!DNL Target] QA 북마클릿을 사용하여 **[!UICONTROL 활동 QA]** 모드를 종료하고 일반적인 방문자처럼 사이트를 보는 방법에 대해 알아봅니다.

>[!ENDSHADEBOX]

[QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md)에서 웹 사이트를 탐색한 후 [!DNL Target] 세션이 만료될 때까지 페이지 전체에서 QA 모드가 유지됩니다. 북마클릿은 JavaScript을 실행하는 브라우저 책갈피입니다. [!DNL Target] QA 북마클릿은 [!DNL Target]이(가) 사용자를 QA 모드에서 해제하도록 하므로 세션이 만료될 때까지 기다릴 필요가 없습니다. 사이트에 배포된 at.js 버전과 일치하는 버전을 사용합니다.

>[!NOTE]
>
>북마클릿을 만드는 프로세스는 브라우저 종류와 버전에 따라 다릅니다. 구체적인 방법은 브라우저의 도움말을 참조하거나 인터넷에서 검색하십시오.

## at.js 1.*x*&#x200B;에 대한 활동 QA 북마클릿

[!DNL Target] QA 북마클릿을 사용하려면 다음 JavaScript 코드가 들어 있는 북마클릿을 만들어 브라우저의 책갈피 도구 모음에 추가하십시오.

```javascript
javascript:(
    function () {
        if (window.location.href.indexOf('?') != -1) {
            var parts = window.location.href.split('at_preview_token',2);
            if (parts.length > 1) {
                window.location.href = parts[0].concat('at_preview_token=');
            } else {
                window.location.href = window.location.href.concat("&at_preview_token=")
            }
        } else {
            window.location.href = window.location.href.concat("?at_preview_token=")
        }
    }
)();
```

`at_preview_token` 매개 변수를 빈 값으로 설정하여 사이트의 페이지를 로드하여 수동으로 QA 모드를 종료할 수도 있습니다. 예:

`https://www.mysite.com/?at_preview_token=`

## at.js 2.*x*&#x200B;에 대한 활동 QA 북마클릿

at.js 1.*x*&#x200B;과 달리 at.js 2.*x*&#x200B;은(는) 서드파티 쿠키를 지원하지 않습니다. QA 모드는 at.js에서 설정한 자사 쿠키를 통해 자사 도메인에 대해서만 지속됩니다. 따라서 QA 모드 세션은 클라이언트측에서만 관리되며 QA 모드 쿠키가 [!DNL Target]&#x200B;(으)로 전송되지 않습니다.

[!DNL Target] QA 북마클릿을 사용하려면 다음 JavaScript 코드가 들어 있는 북마클릿을 만들어 브라우저의 책갈피 도구 모음에 추가하십시오.

```javascript
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {            
            document.cookie = AT_QA_MODE + ';domain='+window.location.hostname+";Path=/; Max-Age=-0;";
            var token = window.location.href.indexOf("?at_preview_token")<0? "&at_preview_token" : "?at_preview_token";
            var url = window.location.href.split(token,2)[0];
            window.open(url, '_self', 'noreferrer');
        }
    })(); 
```

## 활동 QA 북마클릿 사용

at.js 버전과 일치하는 북마클릿을 브라우저에 추가한 후 QA 모드를 종료하려는 경우 항상 사용합니다.

1. QA 모드에 있는 동안 사이트의 페이지를 엽니다.
1. 브라우저의 책갈피 도구 모음에서 북마클릿을 클릭합니다.
1. 사이트의 페이지를 로드합니다. [!DNL Target]은(는) QA 모드에서 세션을 해제하고 사이트는 일반 방문자의 경우처럼 표시됩니다.
