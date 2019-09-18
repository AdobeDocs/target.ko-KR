---
description: Adobe Target QA 북마클릿을 사용하여 Target에서 QA 모드에서 사용자를 릴리스하도록 하는 데 도움이 되는 정보입니다.
keywords: qa;미리 보기;북마클릿;미리 보기 링크
seo-description: Adobe Target QA 북마클릿을 사용하여 Target에서 QA 모드에서 사용자를 릴리스하도록 하는 데 도움이 되는 정보입니다.
seo-title: Adobe Target용 활동 QA 북마클릿
solution: Target
title: 활동 QA 북마클릿
topic: 고급,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
translation-type: tm+mt
source-git-commit: 1df7fbf78f9e20d8a907809b228ed591036c1a24

---


# 활동 QA 북마클릿{#activity-qa-bookmarklet}

Information to help you use the [!DNL Target] QA bookmarklet to force [!DNL Target] to release you from QA mode.

Because [QA mode](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) is sticky, after you browse a website in QA mode, your [!DNL Target] session must expire or you need to have [!DNL Target] release you from QA mode before you can view your site like a typical visitor. Use the QA [!DNL Target] bookmarklet to force yourself out of QA mode.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser's Bookmarks Toolbar:

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

그러면 재사용할 수 있도록 도구 막대에 북마클릿이 나타납니다.

>[!NOTE]
>
>북마클릿을 만드는 프로세스는 브라우저 종류와 버전에 따라 다릅니다. 구체적인 지침이 필요하면 브라우저의 도움말을 참조하거나 인터넷에서 검색하십시오.

You can also manually force yourself out of QA mode by loading a page on your site with the `at_preview_token` parameter with an empty value.

예:

`https://www.mysite.com/?at_preview_token=`
