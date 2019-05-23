---
description: AdBox 또는 리디렉터 사용과 같이 비JavaScript 상황에서 Target을 구현하는 방법에 대한 정보입니다.
keywords: 구현;mbox.js 비javascript;adbox;리디렉터;mbox
seo-description: AdBox 또는 리디렉터 사용과 같이 비JavaScript 상황에서 Target을 구현하는 방법에 대한 정보입니다.
seo-title: '이메일: Target 구현'
solution: Target
subtopic: 시작하기
title: '이메일: Target 구현'
topic: Standard
uuid: 07abc419-0253-47c6-80b8-0bd0734d2c9d
translation-type: tm+mt
source-git-commit: 2c329fdfe0047740ed803b9b0478ce107a23c8dc

---


# 이메일: Target 구현{#email-implement-target}

AdBox 또는 리디렉터 사용과 같이 비JavaScript 상황에서 Target을 구현하는 방법에 대한 정보입니다.

광고와 다른 오프사이트 컨텐츠에 대한 방문을 추적할 수 있습니다. 사이트 내부 및 외부에서 동일한 사용자를 식별하며 전체적으로 웹에서 일관된 웹 경험을 제공할 수 있습니다. 단일 URL을 사용하는 AdBox에서는 JavaScript나 [!DNL at.js] 또는 [!DNL mbox.js] 없이 테스트할 수 있습니다.

AdBox는 [!DNL at.js]나 [!DNL mbox.js]가 없는 사이트(예: 계열사)에 유용합니다. 활동에 동적 크리에이티브가 필요한 경우(예를 들어 장바구니에서 중단된 광고에 제품을 표시해야 하는 경우) AdBox를 사용할 수 없습니다.

AdBox 광고 및 리디렉터는 모든 종류의 활동에 사용할 수 있습니다. 다음 표에서는 AdBox 및 리디렉터의 특징과 각각을 사용하는 시점을 비교하여 설명합니다.

|  | 목적 | 사용 조건 | URL 구조 | 오퍼 유형 | 오퍼 컨텐츠 |
|--- |--- |--- |--- |--- |--- |
| AdBox | 여러 가지 이미지를 광고에 반환 | 광고 컨텐츠를 변경하기 위해 | `clientcode​.tt.​omtrdc​.net/​m2​/​clientcode/ubox/​image?` | 리디렉션 오퍼 | 이미지의 URL |
| 리디렉터 | 방문자를 다른 웹 페이지로 리디렉션 | 광고의 랜딩 페이지를 변경하기 위해 | `clientcode​.tt.omtrdc.net/​m2/clientcode​/ubox/page?` | 리디렉션 오퍼 | 페이지의 URL |

## 제한 {#section_38F559DCF1324271926608BCD4AB1227}

* 표준 mbox와 같은 클라이언트측 시간 제한이 없습니다. Target이 완전히 다운된 경우 광고 방문자에게는 기본 컨텐츠를 포함하여 아무 컨텐츠도 표시되지 않습니다.
* 타사 쿠키를 사용하여 방문을 추적합니다. PCId가 다를 경우, 기본적으로 방문자의 타사 프로필은 기존의 자사 프로필과 병합됩니다.
* AdBox 자체에서 자사 쿠키를 사용하려면 URL에 mbox 세션을 전달해야 합니다. 계정 담당자에게 이 작업을 수행하도록 요청하십시오.
* 자사 쿠키를 사용하여 광고 클릭을 추적하려면 URL에 mbox 세션을 전달합니다. 계정 담당자에게 이 작업을 수행하도록 요청하십시오.
* 동일한 페이지에서 AdBox를 두 개 이상 사용하려면 URL에 mbox 세션을 전달해야 합니다. 계정 담당자에게 이 작업을 수행하도록 요청하십시오. 리디렉터가 실제로 두 번째 페이지에 있으므로 동일한 페이지에 AdBox와 리디렉터 링크가 각각 하나씩 있을 수 있습니다.

