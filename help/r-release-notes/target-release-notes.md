---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
title: Adobe Target 베타 버전 정보
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 1d34000b446c0fd37c6894bf5066f3cd16fc92a7

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이 문서에는 베타 버전 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다.

**마지막 업데이트 날짜: 2020년 25월 3일**

현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 릴리스 시기에 따라 이러한 페이지의 정보가 같을 수 있습니다. 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.

>[!NOTE]
>
>* **mbox.js 사용 중단**:2020년 8월 30일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2020년 8월 30일 이후 mbox.js에서 수행된 모든 호출이 실패하고 Target 활동이 실행되는 페이지에 영향을 줍니다. 모든 고객은 사이트에서 발생할 수 있는 문제를 방지하려면 이 날짜 이전에 at.js 라이브러리의 최신 버전으로 마이그레이션할 것을 권장합니다. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
   >
   >   
   현재 mbox.js가 지원되지만 2017년 7월 이후로 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외 다른 혜택 중 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고 보안을 향상시키며 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe로부터 기대하는 지원을 제공할 수 있습니다.


## at.js 타깃팅(2020년 3월 25일)

다음 새 버전의 Target at.js JavaScript 라이브러리를 사용할 수 있습니다.

* at.js 버전 2.3.0
* at.js 버전 1.8.1

For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

## Target Standard/Premium 20.2.1(2020년 3월 23일)

>[!IMPORTANT]
>
>mbox.js 사용 중단에 대한 위의 정보를 참조하십시오.

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* 카탈로그 검색을 수행할 때 고객이 컬렉션을 선택할 수 없는 문제를 해결했습니다. (TGT-36230)
* API를 통해 생성되었지만 타겟 UI에서 만든 활동에서 참조되지 않는 기준이 UI에서 잘못 삭제되는 문제를 수정했습니다. (TGT-35917)
* CSP(Content Security Policy)에 대한 보안 개선 사항을 구현했습니다. (TGT-36190)
* 속성 가중치 백분율 막대를 왼쪽으로 밀면 &quot;NaN%&quot;가 표시되는 문제를 해결했습니다. (TGT-36211)
* 다양한 언어의 UI 텍스트가 올바로 표시되도록 현지화 문제를 해결했습니다.
* 현재 버전의 Adobe Analytics API에서 지원되지 않는 Adobe Analytics 지표를 비활성화하여 Adobe Analytics for Target(A4T) 활동의 사용 가능한 지표 목록을 표준화했습니다. 이를 통해 향후 Adobe Target 릴리스에서 A4T 지원을 확장할 수 있습니다.

   다음 변경 사항이 적용되었습니다.

   * &quot;페이지에서 보낸 평균 시간&quot;이 &quot;사이트에서 보낸 평균 시간&quot;으로 대체되었습니다. 이 지표를 지표로 사용하는 모든 활동에는 &quot;사이트에서 보낸 평균 시간&quot;이 있습니다(참고:다음 번에 활동이 편집될 때 기본 목표 지표로 선택한 시간(초 단위)입니다.
   * &quot;방문자 수&quot;는 &quot;고유 방문자 수&quot;로 대체되었습니다. 이 지표를 기본 목표 지표로 사용하는 모든 활동은 다음에 활동을 편집할 때 기본 목표 지표로 선택됩니다.

* 다음 지표는 더 이상 사용되지 않으며 새 A4T 활동을 만들 때 기본 목표 지표로 선택할 수 없습니다.

   | 가치 하락 지표 | 제안된 대체 지표 |
   |--- |--- |
   | 일일 방문자, 시간별 방문자, 월별 방문자, 분기별 방문자, 주별 방문자, 연간 방문자 | 고유 방문자 수 |
   | 평균 방문 깊이 | n/a.기본 목표 지표로 제안되지 않음 |
   | 보트 | n/a.기본 목표 지표로 제안되지 않음 |
   | 모바일 충돌 비율, 모바일 평균 이전 세션 길이, 모바일 앱 스토어 평균 등급, 모바일 앱 성능 충돌 비율, 모바일 앱 스토어 평균 등급 | n/a.기본 목표 지표로 제안되지 않음 |

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
