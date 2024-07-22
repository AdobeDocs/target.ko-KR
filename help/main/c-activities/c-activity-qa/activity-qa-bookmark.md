---
keywords: qa;미리 보기;북마클릿;미리 보기 링크
description: Adobe [!DNL Target] QA 북마클릿을 사용하여  [!DNL Target] QA 모드를 강제로 해제하는 방법을 알아봅니다.
title: 활동 QA 북마클릿을 사용하려면 어떻게 해야 합니까?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 13%

---

# 활동 QA 북마클릿

[!DNL Target] QA 북마클릿을 사용하여 [!DNL Target]에서 QA 모드를 해제하도록 하는 데 도움이 되는 정보입니다.

>[!NOTE]
>
>북마클릿을 만드는 프로세스는 브라우저 종류와 버전에 따라 다릅니다. 구체적인 지침이 필요하면 브라우저의 도움말을 참조하거나 인터넷에서 검색하십시오.

## at.js 1용 활동 QA 북마클릿.*x*

[QA 모드](/help/main/c-activities/c-activity-qa/activity-qa.md)는 고정되어 있으므로 QA 모드에서 웹 사이트를 탐색한 후 일반 방문자처럼 사이트를 볼 수 있으려면 먼저 [!DNL Target] 세션이 만료되거나 [!DNL Target]에서 사용자를 QA 모드로부터 해제해야 합니다. QA 모드를 해제하려면 QA [!DNL Target] 북마클릿을 사용하십시오.

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

값이 비어 있는 `at_preview_token` 매개 변수로 사이트의 페이지를 로드하여 QA 모드를 수동으로 나올 수도 있습니다.

예:

`https://www.mysite.com/?at_preview_token=`

## at.js 2용 활동 QA 북마클릿.*x*

at.js 1.*x*, at.js 2.*x*&#x200B;은(는) 타사 쿠키를 지원하지 않으며 QA 모드는 자사 도메인에 대해서만 고정입니다(at.js에서 설정한 자사 쿠키를 사용함). 따라서 at.js 2.*x*, QA 모드 세션은 클라이언트측에서만 관리되며 QA 모드 쿠키가 Target으로 전송되지 않습니다.

[!DNL Target] QA 북마클릿을 사용하려면 다음 JavaScript 코드가 들어 있는 북마클릿을 만들어 브라우저의 책갈피 도구 모음에 추가하십시오.

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
