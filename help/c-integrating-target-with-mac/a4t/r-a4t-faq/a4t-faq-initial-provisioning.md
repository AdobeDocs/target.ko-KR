---
keywords: faq;자주 묻는 질문;analytics for target;a4t;사용 권한 제공;사용 권한 제공;adobe Experience Cloud
description: ' [!DNL Target] (A4T), which lets you use Analytics reporting for [!DNL Target] 활동 제공에 대해 Analytics를 제공하는 것에 대해 자주 묻는 질문에 대한 답변을 찾습니다.'
title: A4T 초기 프로비저닝에 대한 정보는 어디에서 찾을 수 있습니까?
feature: Analytics for Target (A4T)
exl-id: 4b098444-3e5b-45e3-b635-1857c2c8d183
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 66%

---

# 초기 사용 권한 제공 - A4T FAQ

이 주제에는 [!DNL Adobe Target](A4T)의 보고 소스로 [!DNL Adobe Analytics]을(를) 프로비저닝하는 것에 대해 자주 묻는 질문에 대한 답변이 포함되어 있습니다.

## 다중 페이지 A4T 활동을 설정하려면 어떻게 해야 합니까?

기본 다중 페이지 A4T 사용 사례를 구현하려면 다음을 수행합니다.

* 활동 랜딩 URL/페이지에서 Target(at.js 또는 mbox.js)과 Analytics에 대한 JavaScript 라이브러리를 구현합니다. 두 솔루션을 모두 구현하면 Target 데이터가 각 방문자에 대한 Analytics 데이터와 연결됩니다. 이 데이터는 기본 만료 기간이 90일로 설정된 상태로 만료되기 전까지 Analytics에 유지됩니다.

* Analytics 지표를 추적할 사이트의 나머지 페이지에 대해서는 해당 페이지에서 Analytics를 구현합니다. 그러한 페이지에서 Target을 구현할 필요는 없습니다. 해당 페이지 간에 캡처된 Analytics 지표는 이전 글머리 기호에서 해당 방문자에 첨부된 Target 정보를 기반으로 사용자가 처음에 자격을 부여한 Target 활동에 자동으로 연결됩니다.

## 내 [!DNL Target] 계정에서 A4T가 활성화되어 있는지 어떻게 알 수 있습니까?{#section_4437D284448F4313BF953D4B6EDBACA6}

Analytics 활동을 정의할 때 보고서 세트를 선택하려면 Analytics 사용자 계정과 Target 사용자 계정 둘 다 필요합니다. 문서에 설명된 대로 사용자 계정을 구성해야 합니다. 자세한 내용은 [사용자 권한 요구 사항](/help/c-integrating-target-with-mac/a4t/account-reqs.md#concept_4BC06CAB00BF46FF9362AFE98656B083)을 참조하십시오.

Analytics 및 Target에 대한 액세스 권한이 있는 하나 이상의 Experience Cloud 그룹의 구성원이고 모든 보고서 세트에 대한 액세스 권한이 있으면 **[!UICONTROL 활동 만들기]** 아래에 Analytics를 사용하여 A/B 테스트를 만드는 옵션이 표시됩니다.

제공 문제가 발생할 경우 A4T가 올바르게 제공되어 있는지 확인하십시오.

## 내 보고서 세트가 로드되지 않는 이유는 무엇입니까? {#section_6CC8B2B3568A46C499895EB9811FDC2E}

이러한 문제가 발생하면 다음 사항을 확인하십시오.

* Analytics 및 Target 계정이 Experience Cloud에 연결되어 있는지 확인합니다.
* 일부 고객은 동일한 Experience Cloud 회사에서 여러 Analytics 회사 로그인을 사용합니다. 여러 로그인을 사용하는 경우 마지막으로 로그인한 Analytics 회사가 통합을 위해 Target 계정에 연결된 회사인지 확인하십시오.
* Experience Cloud에 몇 시간 동안 로그인되어 있는 상태일 경우 Analytics 세션이 만료될 수 있습니다. 로그아웃했다가 로그인한 후 다시 시도하십시오.

## Target에 Analytics 선택 사항이 표시되지 않는 이유는 무엇입니까?  {#section_EDD996AFB08B4DB196DD934BE55BF48D}

위의 &quot;내 보고서 세트가 로드되지 않는 이유는 무엇입니까?&quot;를 위. 이 문제의 근본 원인은 같습니다.

## Analytics에 A4T 보고서가 표시되지 않는 이유는 무엇입니까?  {#section_FEB41E7B7E4F4F78897E4D9F021DEA59}

위의 &quot;내 보고서 세트가 로드되지 않는 이유는 무엇입니까?&quot;를 참조하십시오. 이 문제의 근본 원인은 같습니다.

## [!DNL Target]에 있는 보고서가 왜 비어 있습니까?{#section_3837104757464CB488C5A83014A669A1}

위의 &quot;내 보고서 세트가 로드되지 않는 이유는 무엇입니까?&quot;를 참조하십시오. 이 문제의 근본 원인은 같습니다.
