---
keywords: qa;preview;bookmarklet;preview links
description: Adobe Target QA 북마클릿을 사용하여 Target을 강제로 QA 모드에서 해제시키는 데 도움이 되는 정보입니다.
title: Adobe Target용 활동 QA 북마클릿
feature: Activities
translation-type: tm+mt
source-git-commit: 9b57d5554884b06d278c3baef3b2c1d5f37bdeb5
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 11%

---


# 활동 QA 북마클릿{#activity-qa-bookmarklet}

[!DNL Target] QA 북마클릿을 사용하여 [!DNL Target]을(를) 강제로 QA 모드에서 해제하도록 하는 데 도움이 되는 정보입니다.

>[!NOTE]
>
>북마클릿을 만드는 프로세스는 브라우저 종류와 버전에 따라 다릅니다. 구체적인 지침이 필요하면 브라우저의 도움말을 참조하거나 인터넷에서 검색하십시오.

## at.js 1에 대한 활동 QA 북마클릿.*x*

[QA 모드](/help/c-activities/c-activity-qa/activity-qa.md)는 고정되어 있으므로 QA 모드에서 웹 사이트를 찾은 후 [!DNL Target] 세션이 만료되어야 하며, 일반적인 방문자와 같이 사이트를 보려면 [!DNL Target] QA 모드에서 해제해야 합니다. QA [!DNL Target] 북마클릿을 사용하여 자신을 QA 모드에서 강제로 종료합니다.

[!DNL Target] QA 북마클릿을 사용하려면 다음 JavaScript 코드가 포함된 북마클릿을 만들고 브라우저의 [책갈피 도구 모음]에 추가합니다.

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

빈 값으로 `at_preview_token` 매개 변수를 사용하여 사이트에서 페이지를 로드하여 QA 모드에서 수동으로 자신을 강제로 삭제할 수도 있습니다.

예:

`https://www.mysite.com/?at_preview_token=`

## at.js 2에 대한 활동 QA 북마클릿.*x*

at.js 1과 대조됩니다.*x*, at.js 2.*xdoes* 는 타사 쿠키를 지원하지 않으며, QA 모드는 퍼스트 파티 도메인에 대해서만 고정됩니다(at.js에서 설정한 퍼스트 파티 쿠키를 통해). 따라서 at.js 2에서 가능합니다.*x*, QA 모드 세션은 클라이언트측에서 관리하며 QA 모드 쿠키가 Target으로 전송되지 않습니다.

[!DNL Target] QA 북마클릿을 사용하려면 다음 JavaScript 코드가 포함된 북마클릿을 만들고 브라우저의 [책갈피 도구 모음]에 추가합니다.

```javascript
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {
            document.cookie = AT_QA_MODE + '; Path=/; Max-Age=-0;';
            var url = window.location.href.split('at_preview_token',2)[0];
            window.open(url.substring(0, url.length - 1), '_self', 'noreferrer');
        }
    })();
```

## 활동 QA 북마클릿 사용

브라우저의 도구 모음에서 북마클릿을 클릭합니다.

