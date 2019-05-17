---
description: Target QA 북마클릿을 사용하여 사용자를 QA 모드로부터 강제로 나오도록 하는 데 도움이 되는 정보입니다.
keywords: qa;미리 보기;북마클릿;미리 보기 링크
seo-description: Target QA 북마클릿을 사용하여 사용자를 QA 모드로부터 강제로 나오도록 하는 데 도움이 되는 정보입니다.
seo-title: 활동 QA 북마클릿
solution: Target
title: 활동 QA 북마클릿
topic: 고급,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 활동 QA 북마클릿{#activity-qa-bookmarklet}

Target QA 북마클릿을 사용하여 사용자를 QA 모드로부터 강제로 나오도록 하는 데 도움이 되는 정보입니다.

[QA 모드](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40)는 고정되어 있으므로 QA 모드에서 웹 사이트를 탐색한 후 일반 방문자처럼 사이트를 볼 수 있으려면 먼저 Target 세션이 만료되거나 Target에서 사용자를 QA 모드로부터 해제해야 합니다. QA 모드를 해제하려면 QA Target 북마클릿을 사용하십시오.

Target QA 북마클릿을 사용하려면 다음 JavaScript 코드가 들어 있는 북마클릿을 만들어 브라우저의 책갈피 도구 모음에 추가하십시오.

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

값이 비어 있는 `at_preview_token` 매개 변수로 사이트의 페이지를 로드하여(예: `https://www.mysite.com/?at_preview_token=`) QA 모드를 수동으로 나올 수도 있습니다.
