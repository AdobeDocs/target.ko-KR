---
keywords: 릴리스 정보;릴리스;업데이트;향후 릴리스;향상;새로운 기능;수정;업데이트;프리릴리스
description: SDK, API 및 JavaScript 라이브러리를 포함하여 Adobe Target의 예정된 릴리스에 포함된 새로운 기능, 개선 사항 및 수정 내용에 대해 알아봅니다.
title: 예정된 릴리스에는 어떤 새로운 기능이 포함됩니까?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 89b995f20491fe0a51c91f8a1fe7e6b1ccc7f974
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 100%

---

# Target 릴리스 정보 (프리릴리스)

이 문서에는 프리릴리스 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트: 2021년 10월 28일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 정보](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일할 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe] 용입니다.

>[!IMPORTANT]
>
>**mbox.js 서비스 종료**: 2021년 3월 31일부터 [!DNL Adobe Target] 에서는 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2021년 3월 31일 이후, mbox.js에서 발송된 모든 호출은 정상적으로 실패하고 기본 콘텐츠를 제공하여 [!DNL Target] 활동이 실행되는 페이지에 영향을 줍니다.
>
>사이트에 문제가 발생하지 않도록 하려면 새 [!DNL Adobe Experience Platform Web SDK] 또는 at.js JavaScript 라이브러리의 최신 버전으로 마이그레이션합니다. 자세한 내용은 [개요: 클라이언트측 웹용 Target 구현](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md)을 참조하십시오.

## at.js 버전 2.7.0(2021년 10월 28일)

이번 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

* [웹 구성 요소](https://developer.mozilla.org/en-US/docs/Web/Web_Components)에 대한 지원이 추가되었습니다. 이 버전의 at.js는 맞춤형 요소 및 맞춤형 요소 내부의 요소에 대한 개인화된 경험과 오퍼를 만들고 테스트하는 데 필요합니다. 이 기능은 [!DNL Target Standard/Premium] 21.10.5 릴리스에 포함되어 있습니다.

## [!DNL Target Standard/Premium] 21.10.5 (2021년 10월 28일)

이 유지 관리 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

| 기능 | 세부 사항 |
| --- | --- |
| [!UICONTROL 시각적 경험 작성기] (VEC) | [웹 구성 요소](https://developer.mozilla.org/en-US/docs/Web/Web_Components)에 대한 지원이 추가되었습니다. 맞춤형 요소 및 맞춤형 요소 내부의 요소에 대해 개인화된 경험과 오퍼를 만들고 테스트할 수 있습니다.<br>자세한 내용은 [시각적 경험 작성기 선택 사항](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#custom)을 참조하십시오. |

## [!DNL Target Standard/Premium] 21.10.4 (2021년 10월 21일)

이 유지 관리 릴리스에는 다음과 같은 개선 사항이 포함됩니다.

| 기능 | 세부 사항 |
| --- | --- |
| 장바구니 기반 추천 | 방문자 장바구니의 콘텐츠를 기반으로 추천을 제공하는 새로운 알고리즘 제품군을 추가했습니다.<br>자세한 내용은 [기준 만들기](/help/c-recommendations/c-algorithms/create-new-algorithm.md)의 “장바구니 기반” 및 [추천 계획 및 구현](/help/c-recommendations/plan-implement.md)의 “장바구니 추가/장바구니 보기/체크아웃 페이지“와 “방문자의 장바구니에 이미 있는 항목 제외“를 참조하십시오. |

## [!DNL Target Standard/Premium] 21.10.3 (2021년 10월 19일)

이 유지 보수 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함되어 있습니다.

* 고객이[!DNL Target] 활동 보고에서 [!UICONTROL Analytics에서 보기] 버튼을 클릭하여 [!DNL Analysis Workspace]에서 [!UICONTROL A4T] 패널을 열지 못하는 문제가 해결되었습니다. (TGT-42099, TGT-42100)
* [!UICONTROL A/B 테스트] 및 [!UICONTROL 경험 타기팅] (XT) 활동을 [!UICONTROL 양식 기반 경험 작성기]를 사용하여 편집하는 동안 [!UICONTROL 디자인 편집] 버튼이 표시되지 않는 문제가 해결되었습니다. (TGT-41980)
* 새로운 [!UICONTROL 추천] 활동을 생성하는 동안 [!UICONTROL 호환 가능] 확인란이 기준 선택에 표시되지 않는 문제가 해결되었습니다. (TGT-42053)
* [!DNL Analytics] 권한이 없어 [!DNL Analytics]를 보고 소스(A4T)로 선택할 수 없을 때 표시되는 잘못된 오류 메시지가 수정되었습니다. (TGT-41954)
* [!DNL Target] UI에서 키보드 탐색을 개선하기 위해 여러 접근성 수정 사항이 구현되었습니다.

## 프리릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/kr/subscription/priority-product-update.html](https://www.adobe.com/kr/subscription/priority-product-update.html)
