---
solution: Target
product: target
title: Adobe Target MCP 서버 도구 참조
description: 읽기 및 쓰기 작업을 포함하여 Adobe Target MCP 서버에 의해 노출된 모든 도구에 대한 전체 매개 변수 참조입니다.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer, User
level: Intermediate, Experienced
source-git-commit: 40e87a3a70d51ccda99f046609ba9633719ea540
workflow-type: tm+mt
source-wordcount: '3195'
ht-degree: 13%

---

# [!DNL Adobe Target] MCP 서버 도구 참조 {#target-mcp-tools-reference}

>[!AVAILABILITY]
>
>[!DNL Adobe Target] MCP 서버는 **공개 Beta**&#x200B;의 모든 고객이 사용할 수 있습니다. 현재 **클라우드 웹**, **클라우드 데스크톱**, **클라우드 코드**, **커서** 및 **ChatGPT**&#x200B;에서 지원됩니다.

이 페이지는 [!DNL Adobe Target] MCP 서버에서 노출된 모든 도구에 대한 전체 참조입니다. 각 도구에 대해 설명, 매개변수 세부 정보, 반환 값 및 예제 자연어 프롬프트를 찾을 수 있습니다. 설치 지침 및 사용 사례는 [시작하기](target-mcp-get-started.md) 및 [사용 사례 및 연습](target-mcp-use-cases.md)을 참조하세요.

>[!IMPORTANT]
>
>MCP(Model Context Protocol)는 새로운 오픈 소스 표준이며 보안 또는 신뢰성 위험을 제시할 수 있습니다. Adobe MCP 서버 통합 및 관련 설명서는 어떠한 종류의 보증도 없이 &quot;있는 그대로&quot; 제공됩니다.
>
>MCP 클라이언트 또는 서버를 Adobe 제품에 연결하는 것은 고객이 선택한 구성이며 고객은 MCP 통합의 보안 및 적합성을 평가할 책임이 있습니다. Adobe은 잘못된 구성, MCP 오용, 서드파티 구현의 취약점 또는 MCP 지원 워크플로우를 통해 수행된 의도하지 않은 작업으로 인해 발생하는 문제에 대해 책임을 지지 않습니다.
>
>위험을 줄이기 위해 Adobe에서는 생산적인 사용을 시작하기 전에 샌드박스 환경에서 통합을 테스트하고, 이를 확인하거나 의존하기 전에 모든 MCP에서 시작한 작업과 응답을 주의 깊게 검토하고 확인하는 것을 권장합니다.

## 사전 요구 사항 {#tools-prerequisites}

[!DNL Adobe Target] 역할에 따라 사용 가능한 도구가 결정됩니다.

* **관찰자** 역할 이상: 모든 읽기 전용 도구에 액세스
* **편집기** 역할 이상: 읽기 도구 및 쓰기 도구(만들기, 업데이트)에 액세스
* **승인자** 역할: 활성화 및 비활성화를 포함한 모든 도구에 액세스

전체 설치 지침은 [시작](target-mcp-get-started.md)을 참조하세요.

## 활동 도구 {#tools-activities}

+++활동 나열

**도구:** `list_target_activities`

[!DNL Adobe Target] 활동을 서버측 필터링 및 정렬과 함께 나열합니다.

활동의 페이지가 매겨진 목록을 검색합니다. 모든 필터는 [!DNL Target] 관리 API에 의해 서버측에서 적용됩니다. 서버는 페이지당 최대 200개의 활동을 반환합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `limit` | 정수 | 아니요 | 반환할 최대 활동 수(서버 최대: 200개) |
| `offset` | 정수 | 아니요 | 페이지 매김을 위해 건너뛸 활동 수 |
| `sort_by` | string | 아니요 | 정렬 기준 필드. 내림차순(예: `-modifiedAt`)에 대해 `-`을(를) 접두사로 사용합니다. 옵션: `id`, `name`, `state`, `priority`, `startsAt`, `endsAt`, `lifetimeStart`, `lifetimeEnd`, `createdAt`, `createdBy`, `modifiedAt`, `modifiedBy`, `type`, `thirdPartyId` |
| `state` | string | 아니요 | 활동 상태별로 필터링: `approved`(실시간/활성), `deactivated`(비활성), `paused`, `saved`(초안) |
| `activity_type` | string | 아니요 | 유형별 필터링: `ab`(A/B 테스트), `xt`(경험 타깃팅), `abt`(Automated Personalization) |
| `name_contains` | string | 아니요 | 이름에 이 문자열이 포함된 활동 필터링(대/소문자 구분 안 함) |
| `starts_after` | string | 아니요 | ISO 8601 날짜 - 이 날짜 이후에 시작하는 활동 |
| `starts_before` | string | 아니요 | ISO 8601 날짜 - 이 날짜 이전에 시작하는 활동 |
| `modified_after` | string | 아니요 | ISO 8601 날짜 — 이 날짜 이후에 수정된 활동 |
| `ends_after` | string | 아니요 | ISO 8601 날짜 - 이 날짜 이후에 종료되는 활동 |
| `ends_before` | string | 아니요 | ISO 8601 날짜 — 이 날짜 이전에 끝나는 활동 |
| `workspace` | string | 아니요 | 작업 공간 ID로 필터링 |
| `segment_id` | string | 아니요 | 대상 세그먼트 ID로 필터링 |
| `profile_attribute_id` | string | 아니요 | 프로필 속성 ID로 필터링 |
| `priority` | 정수 | 아니요 | 정확한 우선순위 값으로 필터링(0-999) |
| `mbox` | string | 아니요 | mbox/위치 이름으로 필터링 |
| `offer_id` | string | 아니요 | 오퍼 ID로 필터링 |
| `view_id` | string | 아니요 | SPA 보기 ID로 필터링 |

**반환:** `activities`(개체 목록: `id`, `name`, `state`, `type`, `priority`, `modifiedAt`, `startsAt`, `endsAt`) 및 `total`(총 개수, 반환된 페이지 크기를 초과할 수 있음)인 JSON 개체.

**예제 프롬프트:** &quot;가장 최근에 수정한 항목별로 정렬된 모든 활성 A/B 테스트를 나열합니다.&quot;

+++

+++A/B 활동 가져오기

**도구:** `get_ab_activity`

A/B 활동에 대한 자세한 정보를 가져옵니다.

경험, 위치, 지표 및 타깃팅 규칙을 포함한 특정 A/B 테스트의 전체 구성을 검색합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | A/B 활동의 고유 식별자 |

**반환:** 메타데이터(이름, 상태, 우선 순위, 날짜), 경험, 위치 및 오퍼, 목표 및 지표, 타깃팅 규칙을 포함한 전체 활동 세부 정보.

**예제 프롬프트:** &quot;A/B 활동 상태에 대한 세부 정보를 12345.&quot;

+++

+++경험 타깃팅 활동 가져오기

**도구:** `get_xt_activity`

XT(경험 타기팅) 활동에 대한 자세한 정보를 제공합니다.

대상-경험 매핑, 위치 및 지표를 포함하여 특정 XT 활동의 전체 구성을 검색합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | XT 활동에 대한 고유 식별자 |

**반환:** 메타데이터, 대상 매핑이 있는 경험, 위치 및 오퍼, 목표 및 지표를 포함한 전체 활동 세부 정보.

**예제 프롬프트:** &quot;Experience Targeting Activity Map에 대한 세부 정보를 12345.&quot;

+++

+++Automated Personalization 활동 가져오기

**도구:** `get_abt_activity`

Automated Personalization(AP) 활동에 대한 자세한 정보를 가져옵니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | AP 활동의 고유 식별자 |

**반환:** 메타데이터, 경험, 위치 및 알고리즘 설정을 포함한 전체 활동 세부 정보.

**예제 프롬프트:** &quot;자동 Personalization 활동 유형에 대한 세부 정보를 12345.&quot;

+++

+++A/B 활동 만들기

**도구:** `create_ab_activity`

새 A/B 테스트 활동을 만듭니다.

경험, 오퍼 및 타겟팅을 포함하여 지정된 구성으로 새 A/B 테스트를 만듭니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `name` | string | 예 | 활동 이름 |
| `state` | string | 아니오 | 초기 상태: `approved`, `deactivated` 또는 `saved`(기본값: `saved`) |
| `priority` | 정수 | 아니요 | 활동 우선 순위(0~999, 기본값: 0) |
| `starts_at` | string | 아니오 | 활동 시작 날짜(ISO 8601) |
| `ends_at` | string | 아니오 | 활동 종료일(ISO 8601) |
| `experiences` | 배열 | 예 | 경험 구성 목록 |
| `locations` | 배열 | 예 | 위치/mbox 구성 목록 |
| `goals` | 오브젝트 | 아니오 | 기본 및 보조 목표 지표 |
| `audiences` | 배열 | 아니요 | Target 대상 구성 |
| `workspace_id` | string | 아니오 | 활동용 Workspace ID |

**반환:** ID가 할당된 활동 개체가 만들어졌습니다.

**예제 프롬프트:** &quot;homepage-hero mbox에서 서로 다른 영웅 이미지를 테스트하는 두 가지 경험을 사용하여 &#39;Homepage Hero Test&#39;라는 A/B 테스트를 만듭니다.&quot;

+++

+++경험 타깃팅 활동 만들기

**도구:** `create_xt_activity`

새 XT(경험 타깃팅) 활동을 만듭니다.

타깃팅 규칙을 기반으로 다양한 대상에게 다양한 경험을 전달하는 XT 활동을 만듭니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `name` | string | 예 | 활동 이름 |
| `state` | string | 아니오 | 초기 상태: `approved`, `deactivated` 또는 `saved`(기본값: `saved`) |
| `priority` | 정수 | 아니요 | 활동 우선 순위(0~999, 기본값: 0) |
| `starts_at` | string | 아니오 | 활동 시작 날짜(ISO 8601) |
| `ends_at` | string | 아니오 | 활동 종료일(ISO 8601) |
| `experiences` | 배열 | 예 | 대상 매핑이 포함된 경험 구성 목록 |
| `locations` | 배열 | 예 | 위치/mbox 구성 목록 |
| `goals` | 오브젝트 | 아니오 | 기본 및 보조 목표 지표 |
| `workspace_id` | string | 아니오 | 활동용 Workspace ID |

**반환:** ID가 할당된 활동 개체가 만들어졌습니다.

**예제 프롬프트:** &quot;다른 지역의 방문자에게 다른 콘텐츠를 표시하는 &#39;지역 Personalization&#39;라는 경험 타깃팅 활동을 만듭니다.&quot;

+++

+++A/B 활동 업데이트

**도구:** `update_ab_activity`

기존 A/B 활동을 업데이트합니다.

읽기-수정-쓰기 패턴 사용: 현재 상태를 가져오고, 변경 사항을 병합하고, 유효성을 검사하고, 업데이트를 전송합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 업데이트할 활동의 고유 식별자 |
| `activity` | 오브젝트 | 예 | 업데이트할 필드(이름, 우선 순위, 경험, 위치, 목표 등) |

**반환:** 업데이트된 활동 개체입니다.

**예제 프롬프트:** &quot;트래픽 할당을 70/30으로 변경하려면 활동을 12345.&quot;

+++

+++경험 타깃팅 활동 업데이트

**도구:** `update_xt_activity`

기존 경험 타깃팅 활동을 업데이트합니다.

읽기-수정-쓰기 패턴을 사용합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 업데이트할 XT 활동의 고유 식별자입니다. |
| `activity` | 오브젝트 | 예 | 업데이트할 필드 |

**반환:** 업데이트된 활동 개체입니다.

**예제 프롬프트:** &quot;XT 활동 12345을 업데이트하여 모바일 방문자에 대한 새 경험을 추가하십시오.&quot;

+++

+++Automated Personalization 활동 업데이트

**도구:** `update_abt_activity`

기존 Automated Personalization 활동을 업데이트합니다.

읽기-수정-쓰기 패턴을 사용합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 업데이트할 AP 활동의 고유 식별자입니다 |
| `activity` | 오브젝트 | 예 | 업데이트할 필드 |

**반환:** 업데이트된 활동 개체입니다.

**예제 프롬프트:** &quot;자동 Personalization 활동 12345을 업데이트하여 최적화 목표를 변경하십시오.&quot;

+++

+++활동 일정 업데이트

**도구:** `update_activity_schedule`

활동 시작 및 종료 날짜를 업데이트합니다.

다른 설정을 수정하지 않고 활동의 일정을 업데이트합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 활동에 대한 고유 식별자 |
| `activity_type` | string | 예 | 활동 유형: `ab`, `xt` 또는 `abt` |
| `starts_at` | string | 아니오 | 새 시작 날짜(ISO 8601) |
| `ends_at` | string | 아니오 | 새 종료일(ISO 8601) |

**반환:** 일정 업데이트 확인.

**예제 프롬프트:** &quot;A/B 활동 12345이 5월 1일부터 5월 31일까지 실행되도록 일정을 업데이트합니다.&quot;

+++

+++활동 상태 변경

**도구:** `update_activity_state`

활동 상태 변경(활성화, 비활성화 또는 일시 중지).

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 활동에 대한 고유 식별자 |
| `state` | string | 예 | 새 상태: `approved`(실시간/활성), `deactivated`(비활성), `paused` 또는 `saved`(초안) |

**업데이트된 활동 상태를 반환합니다:**.

**예제 프롬프트:** &quot;활동 12345 활성화&quot; 또는 &quot;홈 페이지 히어로 테스트 일시 중지&quot;

+++

+++활동 이름 바꾸기

**도구:** `update_activity_name`

활동 이름을 변경합니다.

전체 구성을 수정하지 않고 이름만 업데이트합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 활동에 대한 고유 식별자 |
| `name` | string | 예 | 새 활동 이름 |

**반환:** 업데이트된 활동 개체입니다.

**예제 프롬프트:** &quot;Name activity 12345 to &#39;Summer Campaign Hero Test&#39;.&quot;

+++

+++활동 우선 순위 변경

**도구:** `update_activity_priority`

활동 우선 순위 변경.

여러 활동이 동일한 위치를 타깃팅하는 경우 우선순위가 높은 활동이 우선합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 활동에 대한 고유 식별자 |
| `priority` | 정수 | 예 | 새 우선 순위 값(0~999, 높음 = 높은 우선 순위) |

**반환:** 업데이트된 활동 개체입니다.

**예제 프롬프트:** &quot;활동 12345 우선 순위를 100으로 설정합니다.&quot;

+++

+++활동에 변형 추가

**도구:** `add_activity_variant`

활동에 새 경험/변형을 추가합니다.

옵션 만들기, 위치 매핑, 트래픽 밸런싱 조정 등 모든 구조적 조정을 처리합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 수정할 활동의 ID |
| `activity_type` | string | 예 | 활동 유형: `ab`, `xt` 또는 `abt` |
| `variant_name` | string | 예 | 새 경험/변형 이름 |
| `offer_id` | 정수 | 아니요 | (양식 기반) 사용할 기존 오퍼 ID |
| `offer_content` | string | 아니오 | (양식 기반) 새 인라인 오퍼에 대한 HTML 컨텐츠 |
| `traffic_percentage` | 정수 | 아니요 | 새 변형에 대한 트래픽 %(1-99)입니다. 생략하면 트래픽의 균형이 균일하게 조정됩니다. |
| `audience_id` | 정수 | 아니요 | 변형에 대한 대상 ID(XT 활동) |
| `modifications` | 배열 | 아니요 | (VEC) CSS 선택기 기반 수정 사항 목록 |

**반환:** 업데이트된 활동 개체입니다.

**예제 프롬프트:** &quot;A/B 활동에 오퍼 테마를 사용하여 &#39;휴일 테마&#39;라는 새 변형12345 추가하십시오67890&quot;

+++

+++트래픽 분할 업데이트

**도구:** `update_traffic_split`

변형 간 트래픽 할당을 업데이트합니다.

백분율은 정확히 합해서 100이 되어야 한다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 수정할 활동의 ID |
| `activity_type` | string | 예 | 활동 유형: `ab` 또는 `abt`(XT는 지원되지 않음 — 대상 타깃팅) |
| `splits` | 오브젝트 | 예 | 경험 이름을 백분율에 사전 매핑합니다. 모든 경험을 포함해야 하며 합계는 100입니다. |

**반환:** 업데이트된 활동 개체입니다.

**예제 프롬프트:** &quot;활동 12345에 대한 트래픽 분할을 70% 컨트롤 및 30% Variant A로 변경합니다.&quot;

+++

+++변형 오퍼 변경

**도구:** `update_variant_offer`

특정 변형에 대한 오퍼를 변경합니다.

양식 기반 활동(`offer_id` 사용)과 VEC 활동(`modifications` 사용) 모두에 대해 작동합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 수정할 활동의 ID |
| `activity_type` | string | 예 | 활동 유형: `ab`, `xt` 또는 `abt` |
| `variant_name` | string | 예 | 업데이트할 경험/변형의 이름 |
| `offer_id` | 정수 | 아니요 | (양식 기반) 새 오퍼 ID |
| `offer_content` | string | 아니오 | (양식 기반) 새 인라인 오퍼에 대한 HTML 컨텐츠 |
| `modifications` | 배열 | 아니요 | (VEC) CSS 선택기 기반 수정 사항의 새 목록 |

**반환:** 업데이트된 활동 개체입니다.

**예제 프롬프트:** &quot;오퍼 설정을 사용하려면 활동 12345에서 &#39;변형 A&#39; 경험을 99999.&quot;

+++

+++활동에서 변형 제거

**도구:** `remove_activity_variant`

활동에서 경험/변형을 제거합니다.

경험을 제거하고, 고립된 옵션을 정리하며, 나머지 변형에서 트래픽의 균형을 균등하게 조정합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 수정할 활동의 ID |
| `activity_type` | string | 예 | 활동 유형: `ab`, `xt` 또는 `abt` |
| `variant_name` | string | 예 | 제거할 경험/변형의 이름 |

**반환:** 업데이트된 활동 개체입니다.

**예제 프롬프트:** &quot;A/B 활동 목록에서 &#39;테스트 변형&#39; 경험을 12345.&quot;

+++

## 오퍼 도구 {#tools-offers}

+++오퍼 나열

**도구:** `list_target_offers`

[!DNL Target] 테넌트의 모든 오퍼를 나열합니다.

선택적 필터링으로 페이지가 매겨진 콘텐츠 오퍼 목록을 검색합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `limit` | 정수 | 아니요 | 반환할 최대 오퍼 수 |
| `offset` | 정수 | 아니요 | 페이지 매김을 위해 건너뛸 오퍼 수 |
| `type` | string | 아니요 | 오퍼 유형별로 필터링: `content`(HTML), `json` 또는 `redirect` |
| `name` | string | 아니요 | 오퍼 이름으로 필터링(부분 일치) |

**반환:** `offers`(개체 목록: `id`, `name`, `type`, `content`, `modifiedAt`) 및 `total` 포함) JSON 개체.

**예제 프롬프트:** &quot;모든 JSON 오퍼를 나열합니다.&quot;

+++

+++오퍼 가져오기

**도구:** `get_target_offer`

특정 오퍼에 대한 자세한 정보를 제공합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `offer_id` | 정수 | 예 | 오퍼에 대한 고유 식별자 |

**반환:** `id`, `name`, `type`, `content`, `workspace` 및 `modifiedAt`을(를) 포함한 전체 오퍼 세부 정보.

**예제 프롬프트:** &quot;오퍼 요청에 대한 세부 정보를 67890.&quot;

+++

+++HTML 오퍼 만들기

**도구:** `create_target_offer`

새 HTML 컨텐츠 오퍼를 만듭니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `name` | string | 예 | 오퍼 이름 |
| `content` | string | 예 | 오퍼에 대한 HTML 또는 텍스트 컨텐츠 |
| `workspace_id` | string | 아니오 | 오퍼에 대한 Workspace ID |

**반환:** 할당된 ID로 만들어진 오퍼입니다.

**예제 프롬프트:** &quot;홍보 배너를 사용하여 &#39;여름 판매 배너&#39;라는 HTML 오퍼를 만듭니다.&quot;

+++

+++JSON 오퍼 만들기

**도구:** `create_target_json_offer`

구조화된 데이터를 제공하기 위해 새 JSON 오퍼를 만듭니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `name` | string | 예 | 오퍼 이름 |
| `content` | 오브젝트 | 예 | 오퍼에 대한 JSON 콘텐츠 |
| `workspace_id` | string | 아니오 | 오퍼에 대한 Workspace ID |

**반환:** 할당된 ID로 만들어진 오퍼입니다.

**예제 프롬프트:** &quot;기능 전환 설정을 사용하여 &#39;기능 플래그 구성&#39;이라는 JSON 오퍼를 만듭니다.&quot;

+++

+++오퍼 업데이트

**도구:** `update_target_offer`

기존 오퍼를 업데이트합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `offer_id` | 정수 | 예 | 업데이트할 오퍼의 고유 식별자 |
| `name` | string | 아니오 | 업데이트된 오퍼 이름 |
| `content` | 문자열 또는 개체 | 아니요 | 업데이트된 오퍼 콘텐츠 |

**반환:** 업데이트된 오퍼 개체입니다.

**예제 프롬프트:** &quot;새 프로모션 콘텐츠로 오퍼 67890 업데이트&quot;

+++

## 대상 도구 {#tools-audiences}

+++대상자 나열

**도구:** `list_target_audiences`

[!DNL Target] 테넌트의 모든 대상을 나열합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `limit` | 정수 | 아니요 | 반환할 최대 대상자 수 |
| `offset` | 정수 | 아니요 | 페이지 매김을 위해 건너뛸 대상자 수 |

**반환:** `audiences`(개체 목록: `id`, `name`, `description`, `origin`, `modifiedAt`) 및 `total` 포함) JSON 개체.

**예제 프롬프트:** &quot;모든 대상을 나열합니다.&quot;

+++

+++대상자 가져오기

**도구:** `get_target_audience`

타깃팅 규칙을 포함한 대상 세부 정보를 가져옵니다.

타깃팅 규칙 및 조건을 포함하여 특정 대상의 전체 구성을 검색합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `audience_id` | 정수 | 예 | 대상자에 대한 고유 식별자 |

**반환:** `id`, `name`, `description`, `origin`, 타깃팅 규칙 및 관련 활동 수를 포함한 전체 대상 세부 정보.

**예제 프롬프트:** &quot;대상 그룹에 대한 세부 정보를 12345 해당 타깃팅 규칙을 보여 주십시오.&quot;

+++

+++대상자 만들기

**도구:** `create_target_audience`

타깃팅 규칙으로 새 대상을 만듭니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `name` | string | 예 | 대상자 이름 |
| `description` | string | 아니오 | 대상자에 대한 설명 |
| `targetRule` | 오브젝트 | 아니오 | 타깃팅 규칙(지역, 브라우저, 사용자 지정 속성 등) |
| `workspace_id` | string | 아니오 | 대상자용 Workspace ID |

**반환:** 할당된 ID로 생성된 대상자입니다.

**예제 프롬프트:** &quot;CA에서 모바일 사용자를 타깃팅하는 &#39;캘리포니아에서 모바일 방문자&#39;라는 대상을 만듭니다.&quot;

+++

## Mbox 도구 {#tools-mboxes}

+++mbox 나열

**도구:** `list_target_mboxes`

[!DNL Target] 테넌트의 모든 mbox를 나열합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `limit` | 정수 | 아니요 | 반환할 최대 mbox 수 |
| `offset` | 정수 | 아니요 | 페이지 매김을 위해 건너뛸 mbox 수 |
| `name` | string | 아니요 | mbox 이름으로 필터링(부분 일치) |
| `status` | string | 아니요 | 상태별로 필터링 |

**반환:** `mboxes`(개체 목록: `name`, `status`, `lastRequestTime`) 및 `total` 포함.

**예제 프롬프트:** &quot;List all mbox containing &#39;homepage&#39;.&quot;

+++

+++mbox 가져오기

**도구:** `get_target_mbox`

특정 mbox에 대한 자세한 정보를 가져옵니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `mbox_name` | string | 예 | mbox 이름 |

**반환:** Mbox 세부 정보(예: `name`, `status` 및 mbox를 사용하는 활동 목록).

**예제 프롬프트:** &quot;mbox &#39;homepage-hero&#39;에 대한 세부 정보를 가져옵니다.&quot;

+++

+++mbox 프로필 속성 나열

**도구:** `list_target_mbox_profile_attributes`

타깃팅에 사용할 수 있는 모든 mbox 프로필 속성을 나열합니다.

매개 변수가 필요하지 않습니다.

**프로필 특성 개체의 JSON 배열**&#x200B;을(를) 반환합니다.

**예제 프롬프트:** &quot;타깃팅에 사용할 수 있는 프로필 특성은 무엇입니까?&quot;

+++

## 속성 도구 {#tools-properties}

+++목록 속성

**도구:** `list_target_properties`

[!DNL Target] 테넌트의 모든 속성을 나열합니다.

속성은 활동을 구성하고 액세스를 제어합니다.

매개 변수가 필요하지 않습니다.

**반환:** `id`, `name`, `description` 및 `channel`을(를) 포함하는 속성 개체 목록입니다.

**예제 프롬프트:** &quot;모든 Target 속성을 나열합니다.&quot;

+++

## 보고 도구 {#tools-reporting}

+++A/B 성능 보고서 가져오기

**도구:** `get_ab_performance_report`

A/B 활동에 대한 성과 보고서를 가져옵니다.

전환율, 상승도 및 신뢰도 수준을 검색합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | A/B 활동의 고유 식별자 |
| `report_interval` | string | 아니요 | 보고서의 기간(예: `last7days`, `last30days` 또는 사용자 지정 날짜 범위) |

**반환:** 경험 수준 지표(방문자, 전환, 전환율), 상승도 계산, 통계적 신뢰 수준 및 매출 지표(구성된 경우).

**예제 프롬프트:** &quot;지난 30일 동안의 A/B 테스트 12345에 대한 성능 보고서를 표시합니다.&quot;

+++

+++A/B 주문 보고서 가져오기

**도구:** `get_ab_orders_report`

A/B 활동에 대한 주문/매출 보고서를 가져옵니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | A/B 활동의 고유 식별자 |
| `report_interval` | string | 아니요 | 보고서 기간 |

**반환:** 경험별 주문 수, 매출 및 평균 주문 가격.

**예제 프롬프트:** &quot;활동 상태에 대한 주문 보고서를 12345.&quot;

+++

+++경험 타깃팅 성과 보고서 가져오기

**도구:** `get_xt_performance_report`

경험 타깃팅 활동에 대한 성과 보고서를 가져옵니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | XT 활동에 대한 고유 식별자 |
| `report_interval` | string | 아니요 | 보고서 기간 |

**반환:** 경험 수준 성능 지표.

**예제 프롬프트:** &quot;내 경험 타깃팅 활동 상태에 대한 성능 54321&quot;

+++

+++경험 타깃팅 주문 보고서 가져오기

**도구:** `get_xt_orders_report`

경험 타깃팅 활동에 대한 주문/매출 보고서를 가져옵니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | XT 활동에 대한 고유 식별자 |
| `report_interval` | string | 아니요 | 보고서 기간 |

**반환:** 경험별 지표를 정렬합니다.

**예제 프롬프트:** &quot;XT 활동 요청에 대한 주문 데이터를 54321.&quot;

+++

+++활동 이름별 성과 보고서 가져오기

**도구:** `get_activity_report_by_name`

이름으로 활동을 검색하고 성과 보고서를 가져옵니다.

활동 이름은 알지만 ID는 알지 못하는 경우 유용합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_name` | string | 예 | 검색할 활동의 이름 |
| `report_interval` | string | 아니요 | 보고서 기간 |

**반환:** 활동 세부 정보 및 성능 지표.

**예제 프롬프트:** &quot;내 &#39;홈 페이지 히어로 테스트&#39; 활동에 대한 성과 보고서를 가져옵니다.&quot;

+++

+++A4T(Analytics for Target) 보고서 가져오기

**도구:** `get_a4t_report`

[!DNL Target] 활동에 대한 A4T(Analytics for Target) 보고서를 가져옵니다.

활동에 대한 A4T 구성을 확인한 다음 [!DNL Adobe Analytics]에 대해 GraphQL 쿼리를 실행하여 Analytics측 지표를 검색합니다. A4T 보고가 구성된 활동에만 사용할 수 있습니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | [!DNL Target] 활동의 고유 식별자입니다. |
| `report_interval` | string | 아니요 | 보고서의 기간(예: `last7days`, `last30days` 또는 사용자 지정 날짜 범위) |

**반환:** 방문자 수, 전환, 매출 및 경험별 리프트를 포함하여 활동에 대한 Analytics 측 지표를 [!DNL Adobe Analytics]에서 직접 가져온 것입니다.

**예제 프롬프트:** &quot;내 체크아웃 최적화 테스트를 위해 A4T 보고서를 가져오고 Analytics측 전환 데이터를 요약합니다.&quot;

+++

## 미리보기 도구 {#tools-preview}

+++활동 미리 보기

**도구:** `preview_activity`

[!DNL Target] 활동에 대한 브라우저 QA 미리 보기 URL을 생성합니다.

대상자 타기팅 규칙을 우회하여 특정 경험을 표시하도록 하는 클릭 가능한 미리보기 링크를 만듭니다. A/B, XT 및 Automated Personalization 활동에 작동합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `activity_id` | 정수 | 예 | 미리 볼 [!DNL Target] 활동 ID |
| `experience_index` | 정수 | 아니요 | 0 기반 경험 색인입니다. 생략하면 모든 경험에 대한 URL을 반환합니다. |
| `url` | string | 아니요 | 미리 보기용 페이지 URL. 양식 기반 활동에 필요합니다. VEC 활동의 경우, 이 제공되면 작성된 위치를 무시합니다 |

**반환:** 활동 정보(이름, 유형, 상태), 각 경험에 대한 미리 보기 URL, 경험 이름 및 색인.

**예제 프롬프트:** &quot;브라우저에서 각 경험을 테스트할 수 있도록 활동 12345에 대한 미리 보기 URL을 생성합니다.&quot;

+++

## 응답 토큰 도구 {#tools-response-tokens}

+++응답 토큰 나열

**도구:** `list_target_response_tokens`

[!DNL Target] 테넌트의 모든 응답 토큰을 나열합니다.

기본 제공 및 사용자 지정으로 구성된 모든 응답 토큰을 검색합니다.

매개 변수가 필요하지 않습니다.

**반환:** `name`, `type` 및 `enabled` 상태의 응답 토큰 개체의 JSON 배열입니다.

**예제 프롬프트:** &quot;모든 응답 토큰을 나열합니다.&quot;

+++

+++응답 토큰 만들기

**도구:** `create_target_response_token`

[!DNL Target] 응답에서 추가 데이터를 수집하기 위한 새 사용자 지정 응답 토큰을 만듭니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `token_name` | string | 예 | 응답 토큰 이름 |
| `token_type` | string | 예 | 토큰 유형: `SCRIPT`, `ACTIVITY`, `MBOX`, `GEO` 또는 `CRS` |

**반환:** 만들어진 응답 토큰 개체입니다.

**예제 프롬프트:** &quot;ACTIVITY 유형의 &#39;campaign_id&#39;라는 사용자 지정 응답 토큰을 만듭니다.&quot;

+++

## 개정 도구 {#tools-revisions}

+++감사 로그 가져오기

**도구:** `get_target_revisions`

리소스 유형에 대한 감사 로그를 가져옵니다.

작성자별 선택적 필터링을 사용하여 [!DNL Target] 리소스에 대한 변경 사항을 검색합니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `revision_resource_type` | string | 예 | 리소스 유형: `activity`, `offer` 또는 `audience` |
| `modified_by` | string | 아니요 | 변경한 사용자별로 필터링 |
| `limit` | 정수 | 아니요 | 반환할 최대 개정 수 |
| `offset` | 정수 | 아니요 | 페이지 매김을 위해 건너뛸 개정 수 |

**반환:** 타임스탬프, 사용자 및 변경 내용이 포함된 개정 내역입니다.

**예제 프롬프트:** &quot;활동 변경에 대한 감사 로그를 표시합니다.&quot;

+++

+++특정 엔티티에 대한 개정 버전 가져오기

**도구:** `get_target_entity_revisions`

ID별로 특정 엔티티의 모든 수정 사항을 가져옵니다.

| 매개 변수 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `revision_resource_type` | string | 예 | 리소스 유형: `activity`, `offer` 또는 `audience` |
| `entity_id` | 정수 | 예 | 엔티티의 고유 식별자 |

**반환:** 지정한 엔터티에 대한 모든 수정 버전의 JSON 배열입니다.

**예제 프롬프트:** &quot;Show me all changes to activity 12345.&quot;

+++

## 템플릿 도구 {#tools-templates}

+++사용 가능한 템플릿 나열

**도구:** `list_target_templates`

활동 및 오퍼 생성에 사용 가능한 MCP 리소스 및 템플릿을 나열합니다.

매개 변수가 필요하지 않습니다.

**반환:** 사용 가능한 템플릿과 리소스를 나열하는 JSON 개체입니다.

**예제 프롬프트:** &quot;활동을 만드는 데 사용할 수 있는 템플릿은 무엇입니까?&quot;

+++

## 도구 요약 {#tools-summary}

| 카테고리 | 계수 | 도구 |
|---|---|---|
| 활동 | 17 | `list_target_activities`, `get_ab_activity`, `get_xt_activity`, `get_abt_activity`, `create_ab_activity`, `create_xt_activity`, `update_ab_activity`, `update_xt_activity`, `update_abt_activity`, `update_activity_schedule`, `update_activity_state`, `update_activity_name`, `update_activity_priority`, `add_activity_variant`, `update_traffic_split`, `update_variant_offer`, `remove_activity_variant` |
| 오퍼 | 5 | `list_target_offers`, `get_target_offer`, `create_target_offer`, `create_target_json_offer`, `update_target_offer` |
| 대상자 | 3 | `list_target_audiences`, `get_target_audience`, `create_target_audience` |
| Mbox | 3 | `list_target_mboxes`, `get_target_mbox`, `list_target_mbox_profile_attributes` |
| 속성 | 1 | `list_target_properties` |
| 보고 | 6 | `get_ab_performance_report`, `get_ab_orders_report`, `get_xt_performance_report`, `get_xt_orders_report`, `get_activity_report_by_name`, `get_a4t_report` |
| 미리보기 | 1 | `preview_activity` |
| 응답 토큰 | 2 | `list_target_response_tokens`, `create_target_response_token` |
| 개정 | 2 | `get_target_revisions`, `get_target_entity_revisions` |
| 템플릿 | 1 | `list_target_templates` |
| **합계** | **41** | |

## 관련 리소스 {#tools-related}

* [MCP 클라이언트 작업](target-mcp.md)
* [[!DNL Adobe Target] 관리 API 참조](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
