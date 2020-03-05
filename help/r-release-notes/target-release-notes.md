---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes
description: 최신 또는 예정된 DNL Adobe Target 릴리스의 기능, 개선 사항 및 수정 사항에 대한 정보를 제공하는 릴리스 노트입니다.
title: Adobe Target 베타 버전 정보
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 336726bef7a8a3a8cf4abed37ccdeb63b8efa369

---


# Target 릴리스 노트(사전 릴리스){#target-release-notes-prerelease}

이러한 릴리스 노트는 최신 또는 예정된 [!DNL Adobe Target] 릴리스의 기능, 향상된 기능 및 수정 사항에 대한 정보를 제공합니다.

**마지막 업데이트 날짜: 2020년 2월 18일**

>[!NOTE]
>
>* 이 문서에는 베타 버전 정보가 포함되어 있습니다. 릴리스 날짜, 기능 및 기타 정보는 예고 없이 변경될 수 있습니다. 현재 릴리스에 대한 정보를 보려면 [Target 릴리스 노트](release-notes.md)를 참조하십시오. 이러한 페이지에 대한 정보는 릴리스 날짜에 따라 동일하거나 다를 수 있습니다.
   >
   >
* 괄호로 묶인 문제 번호는 내부 [!DNL Adobe]용입니다.
   >
   >
* **TLS 지원 변경 사항**:2020년 3월 1일부터 Target은 TLS 1.1 및 TLS 1.0 암호화를 지원하지 않습니다. TLS(전송 계층 보안)는 네트워크를 통해 데이터를 안전하게 교환해야 하는 웹 브라우저 및 애플리케이션에서 현재 사용되는 가장 널리 배포된 보안 프로토콜입니다. 이 변경 사항은 일반적으로 받아들여지는 TLS 1.2 이상의 보안 규정 준수 표준을 충족하기 위해 필요합니다. 현재 사용 중인 TLS 버전을 확인합니다. 버전이 1.2보다 낮은 경우 Target을 예상대로 계속 사용하려면 2020년 3월 1일 이전에 필요한 변경 사항을 구현하십시오.
   >
   >   
   가능한 영향 및 구현을 업데이트하는 데 필요한 단계에 대한 자세한 내용은 TLS(전송 [레이어 보안) 암호화 변경을](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)참조하십시오.
   >
   >
* **mbox.js 사용 중단**:2020년 8월 30일에 Adobe Target은 더 이상 mbox.js 라이브러리를 지원하지 않습니다. 2020년 8월 30일 이후 mbox.js에서 수행된 모든 호출이 실패하고 Target 활동이 실행되는 페이지에 영향을 줍니다. 모든 고객은 사이트에서 발생할 수 있는 문제를 방지하려면 이 날짜 이전에 at.js 라이브러리의 최신 버전으로 마이그레이션할 것을 권장합니다. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
   >
   >   
   현재 mbox.js가 지원되지만 2017년 7월 이후로 이 라이브러리에 대한 기능 업데이트를 제공하지 않았습니다. 최신 at.js는 mbox.js보다 많은 이점을 제공합니다. 그 외 다른 혜택 중 at.js는 웹 구현을 위한 페이지 로드 시간을 향상시키고 보안을 향상시키며 단일 페이지 애플리케이션에 대한 더 나은 구현 옵션을 제공합니다.
   >
   >   
   모든 고객을 at.js로 이동시킴으로써 Adobe 엔지니어 및 지원 담당자는 새로운 기능을 제공하고 Adobe로부터 기대하는 지원을 제공할 수 있습니다.


## Target Standard/Premium 20.2.1(2020년 3월 3일)

>[!IMPORTANT]
>
>mbox.js 사용 중단에 대한 위의 정보를 참조하십시오.

이 릴리스에는 다음과 같은 개선 사항, 수정 사항 및 변경 사항이 포함됩니다.

* 카탈로그 검색을 수행할 때 고객이 컬렉션을 선택할 수 없는 문제를 해결했습니다. (TGT-36230)
* API를 통해 생성되었지만 타겟 UI에서 만든 활동에서 참조되지 않는 기준이 UI에서 잘못 삭제되는 문제를 수정했습니다. (TGT-35917)
* CSP(Content Security Policy)에 대한 보안 개선 사항을 구현했습니다. (TGT-36190)
* 속성 가중치 백분율 막대를 왼쪽으로 밀면 &quot;NaN%&quot;가 표시되는 문제를 해결했습니다. (TGT-36211)
* 다양한 언어의 UI 텍스트가 올바로 표시되도록 현지화 문제를 해결했습니다.
* 다음 Adobe Analytics 지표는 2020년 3월 Target 릴리스부터 Analytics for Target(A4T)에서 더 이상 지원되지 않습니다.
   * averagevisdepth
   * 보트
* 다음 지표는 더 이상 지원되지 않으며 사용자가 지표를 포함하는 활동을 처음 수정할 때 지표의 새 버전으로 자동 변환됩니다.

   | 가치 하락 지표 | 새 지표 |
   |--- |--- |
   | `averagetimespentonpage` | `averagetimespentonsite` (참고:초 대신 분 단위 측정) |
   | `instances` | `occurrences` |
   | `singleaccess` | `singlepagevisits` |
   | `uniquevisitors` | `visitors` |
   | `visitorsdaily`, `visitorshourly`, `visitorsmonthly`, `visitorsquarterly`, `visitorsweekly`, `visitorsyearly` | `visitors` |

## 사전 릴리스 정보 {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Target 및 기타 Adobe Experience Cloud 솔루션에 대한 향후 제품 개선 사항에 대한 사전 알림을 받으려면 Adobe 우선순위 제품 업데이트에 등록하십시오.

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
