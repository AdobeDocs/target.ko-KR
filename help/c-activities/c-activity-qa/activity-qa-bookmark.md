---
keywords: qa;preview;bookmarklet;preview links
description: Adobe Target QA 북마클릿을 사용하여 Target이 QA 모드에서 사용자를 릴리스하도록 하는 데 도움이 되는 정보입니다.
title: Adobe Target용 활동 QA 북마클릿
feature: qa
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 11%

---


# 활동 QA 북마클릿{#activity-qa-bookmarklet}

Information to help you use the [!DNL Target] QA bookmarklet to force [!DNL Target] to release you from QA mode.

>[!NOTE]
>
>북마클릿을 만드는 프로세스는 브라우저 종류와 버전에 따라 다릅니다. 구체적인 지침이 필요하면 브라우저의 도움말을 참조하거나 인터넷에서 검색하십시오.

## at.js 1용 활동 QA 북마클릿.*x*

Because [QA mode](/help/c-activities/c-activity-qa/activity-qa.md) is sticky, after you browse a website in QA mode, your [!DNL Target] session must expire or you need to have [!DNL Target] release you from QA mode before you can view your site like a typical visitor. Use the QA [!DNL Target] bookmarklet to force yourself out of QA mode.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser&#39;s Bookmarks Toolbar:

```
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

You can also manually force yourself out of QA mode by loading a page on your site with the `at_preview_token` parameter with an empty value.

예:

`https://www.mysite.com/?at_preview_token=`

## at.js 2에 대한 활동 QA 북마클릿.*x*

at.js 1과 대조됩니다.*x*, at.js 2.*x* a는 타사 쿠키를 지원하지 않으며, QA 모드는 퍼스트 파티 도메인에 대해서만 고정됩니다(at.js에서 설정한 퍼스트 파티 쿠키를 통해). 따라서 at.js 2에서 가능합니다.*x*, QA 모드 세션은 클라이언트 쪽에서만 관리되며 QA 모드 쿠키가 Target으로 전송되지 않습니다.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser&#39;s Bookmarks Toolbar:

```
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

