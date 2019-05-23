---
description: Adobe Analytics를 Target(A4T)의 보고 소스로 구현할 때 몇 가지 단계가 필요합니다.
keywords: A4T;Adobe Analytics;Analytics 기반 활동;Analytics 보고서 세트;보고서 세트;Analytics Target 통합;보고서 세트 구성
seo-description: Adobe Analytics를 Target(A4T)의 보고 소스로 구현할 때 몇 가지 단계가 필요합니다.
seo-title: Analytics for Target 구현
solution: Target
title: Analytics for Target 구현
topic: Premium
uuid: da6498c8-1549-4c36-ae42-38c731a28f08
translation-type: tm+mt
source-git-commit: 1be00210754e8fa3237fdbccf48af625c2aafe65

---


# Analytics for Target 구현{#analytics-for-target-implementation}

Adobe Analytics를 Target(A4T)의 보고 소스로 구현할 때 몇 가지 단계가 필요합니다.

## 구현 절차 {#section_73961BAD5BB4430A95E073DE5C026277}

다음 표에서는 이 통합을 사이트에 배포하는 데 필요한 단계에 대해 설명합니다.

## 1단계: Analytics 및 Target 제공 요청

Analytics를 Target의 보고 소스로 구현한 후에는 Analytics 및 Target 제공을 요청해야 합니다. [이 양식을 사용하여 제공을 요청합니다](http://www.adobe.com/go/audiences).

## 2단계: 사용자 권한 설정

Adobe Target에서 Adobe Analytics 기반 활동을 만들려면 사용자 계정 요구 사항을 충족해야 합니다. 자세한 내용은 [사용자 권한 요구 사항](/help/c-integrating-target-with-mac/a4t/account-reqs.md)을 참조하십시오.

## 3단계: Experience Cloud 방문자 ID 서비스 구현

방문자 ID 서비스를 통해 Experience Cloud 솔루션에서 사용자를 식별할 수 있습니다. 필요한 Experience Cloud 방문자 ID 버전을 구현하거나 이 버전으로 마이그레이션해야 합니다. 자세한 내용은 [구현하기 전에](/help/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

Experience Cloud 방문자 ID 서비스 설명서의 [Target용 Experience Cloud ID 서비스 구현](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-target.html)을 참조하십시오.

## 4단계: AppMeasurement for JavaScript 또는 s_code의 AppMeasurement 업데이트

필요한 appMeasurement.js 버전을 구현하거나 이 버전으로 마이그레이션해야 합니다. 자세한 내용은 [구현하기 전에](/help/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

신규 구현에 대해서는 [Analytics JavaScript 구현](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html)을 참조하십시오.

마이그레이션에 대해서는 [JavaScript용 AppMeasurement로 마이그레이션](https://marketing.adobe.com/resources/help/en_US/sc/implement/?f=appmeasure_mjs_migrate)을 참조하십시오.

## 5단계: at.js 또는 mbox.js 다운로드하여 업데이트

프로덕션 계정을 사용하여 필요한 at.js 또는 mbox.js 버전을 구현하거나 이 버전으로 마이그레이션해야 합니다. 이 코드를 수정할 필요가 없습니다.

자세한 내용은 [구현하기 전에](/help/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

## 6단계: at.js 또는 mbox.js 호스팅

이전에 at.js나 mbox.js를 배포한 경우에는 기존 파일을 업데이트된 버전으로 대체할 수 있습니다. 자세한 내용은 [구현하기 전에](/help/c-integrating-target-with-mac/a4t/before-implement.md)의 &quot;구현 요구 사항&quot;을 참조하십시오.

그렇지 않으면, JavaScript 파일용 AppMeasurement 및 방문자 ID 서비스와 함께 이 파일을 호스트할 수 있습니다. 이러한 파일은 사이트의 모든 페이지에서 액세스할 수 있는 웹 서버에 호스트되어야 합니다. 다음 단계에서 이 파일에 대한 경로가 필요합니다.

## 7단계: 모든 사이트 페이지에서 at.js 또는 mbox.js 참조

각 페이지의 <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> 태그에 다음 코드 행을 추가하여 VisitorAPI.js 아래 at.js 또는 mbox.js를 포함합니다.

at.js의 경우:

```
<script language="JavaScript" type="text/javascript" 
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

mbox.js의 경우:

```
<script language="JavaScript" type="text/javascript" 
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/mbox.js"></script>
```

VisitorAPI.js가 at.js 또는 mbox.js보다 먼저 로드되어야 합니다. 따라서 기존 at.js 또는 mbox.js 파일을 업데이트하는 경우 로드 순서를 확인해야 합니다.

## 8단계: 구현의 유효성 검사

JavaScript 라이브러리를 업데이트한 후 페이지를 로드하여 Target 호출의 mboxMCSDID 매개 변수 값이 Analytics page-view 호출의 sdid 매개 변수 값과 일치하는지 확인하십시오.

이 검사는 호출 순서가 항상 예측 가능하지는 않은 단일 페이지 애플리케이션(SPA)에서 확인하는 데 특히 중요합니다.

**참고:** A4T가 올바로 작동하려면 이 값이 일치해야 합니다.

## 9단계: (선택 사항) 이전 통합 코드 제거

구현을 간소화하고 시스템 간의 불일치를 처리할 필요가 없도록 이전 통합을 제거하는 것이 좋습니다. `mboxLoadSCPlugin`을 비롯하여 이전 SC에 배포한 모든 코드를 T&amp;T 통합으로 이동할 수 있습니다.

## 10단계: Analytics를 Target의 보고 소스로 사용하기 위한 선택 사항 활성화

Target에서 [!UICONTROL 설정 &gt; 환경 설정]을 클릭하고 [!UICONTROL 활동당 선택] 또는 [!UICONTROL Adobe Analytics]를 선택하여 선택 사항을 활성화합니다.

* 활동당 선택옵션을 사용하면 각 활동을 만들 때 Target과 Analytics 중에서 선택할 수 있습니다.
* Adobe Analytics에서는 만들어지는 모든 활동에 대해 Analytics를 보고 소스로 설정합니다.

