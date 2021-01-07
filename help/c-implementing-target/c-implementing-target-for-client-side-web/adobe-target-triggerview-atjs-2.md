---
keywords: adobe.target.triggerView;triggerView;triggerview;trigger view;at.js;functions;function;viewName;viewname;view name
description: Adobe Target at.js JavaScript 라이브러리에 대한 adobe.target.triggerView (viewName, options) 함수 정보입니다.
title: adobe.target.triggerView (viewName, options) - at.js 2.x
feature: at.js
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 92%

---


# adobe.target.triggerView(viewName, options) - at.js 2.x

이 함수는 새 페이지를 로드할 때마다 또는 페이지의 구성 요소가 다시 렌더링될 때 호출할 수 있습니다. 시각적 경험 작성기(VEC)를 사용하여 A/B 테스트 및 경험 타깃팅(XT) 활동을 만들려면 단일 페이지 애플리케이션(SPA)에 대해 `adobe.target.triggerView()`를 구현해야 합니다. 사이트에서 `adobe.target.triggerView()`가 구현되지 않으면 SPA에 VEC를 활용할 수 없습니다. 자세한 내용은 [단일 페이지 애플리케이션 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md)을 참조하십시오.

>[!NOTE]
>
>이 함수는 at.js 2.x에서 도입되었으며, at.js 버전 1.*x*&#x200B;와 다른 2.0에 도입된 차이점을 자세히 알 수 있습니다.

| 매개 변수 | 유형 | 필수? | 설명 |
| --- | --- | --- | --- |
| viewName | 문자열 | 예 | 보기를 표현할 문자열 유형으로 모든 이름을 전달합니다. 이 보기 이름은 마케터가 작업을 만들고 A/B 및 XT 활동을 실행하는 VEC의 [!UICONTROL 수정 사항] 패널에 표시됩니다. |
| options | 개체 | 아니오 |  |
| options > page | 부울 | 아니오 | **TRUE**: 페이지의 기본값은 true입니다. page=true일 때 노출 수가 증가하면 [!DNL Target] 백엔드에 알림이 전송됩니다.<br>[옵션] > [페이지]가 false로 설정된  `triggerView` 경우를 제외하고, 을 호출하면 기본적으로 알림이 전송됩니다.<br>**FALSE:** page=false일 때 노출 수가 증가하면 알림이 전송되지 않습니다. 이 값은 오퍼가 있는 페이지에서 구성 요소를 다시 렌더링하려는 경우에만 사용해야 합니다. |

## 예: True

활동 노출 횟수 및 기타 지표를 늘리기 위해 Target 백엔드로 알림을 전송하는 `triggerView()` 호출.

```javascript
adobe.target.triggerView("homeView")
```

## 예: False

노출 계산을 위해 Target 백엔드에 전송된 알림을 전송하지 않은 `triggerView()` 호출.

```javascript
adobe.target.triggerView("homeView", {page: false})
```
