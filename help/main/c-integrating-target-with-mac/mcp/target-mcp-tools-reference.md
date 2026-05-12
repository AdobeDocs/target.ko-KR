---
solution: Target
product: target
title: Adobe Target MCP 서버 도구 참조
description: Adobe Target MCP 서버에 의해 노출된 21개의 모든 읽기 전용 도구에 대한 전체 매개 변수 참조입니다.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer, User
level: Intermediate, Experienced
source-git-commit: 216b1103f501a3fcf955523d4bcc8254a8ea418d
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 11%

---

# [!DNL Adobe Target] MCP 서버 도구 참조 {#target-mcp-tools-reference}

>[!AVAILABILITY]
>
>[!DNL Adobe Target] MCP 서버는 **공개 Beta**&#x200B;의 모든 고객이 사용할 수 있습니다. 현재 **클라우드 웹**, **클라우드 데스크톱**, **클라우드 코드**, **커서** 및 **ChatGPT**&#x200B;에서 지원됩니다.

이 페이지는 [!DNL Adobe Target] MCP 서버에서 노출된 모든 읽기 전용 도구에 대한 전체 참조입니다. 각 도구에 대해 설명, 매개변수 세부 정보, 반환 값 및 예제 자연어 프롬프트를 찾을 수 있습니다. 설치 지침 및 사용 사례는 [시작하기](target-mcp-get-started.md) 및 [사용 사례 및 연습](target-mcp-use-cases.md)을 참조하세요.

>[!IMPORTANT]
>
>MCP(Model Context Protocol)는 새로운 오픈 소스 표준이며 보안 또는 신뢰성 위험을 제시할 수 있습니다. Adobe MCP 서버 통합 및 관련 설명서는 어떠한 종류의 보증도 없이 &quot;있는 그대로&quot; 제공됩니다.
>
>MCP 클라이언트 또는 서버를 Adobe 제품에 연결하는 것은 고객이 선택한 구성이며 고객은 MCP 통합의 보안 및 적합성을 평가할 책임이 있습니다. Adobe은 잘못된 구성, MCP 오용, 서드파티 구현의 취약점 또는 MCP 지원 워크플로우를 통해 수행된 의도하지 않은 작업으로 인해 발생하는 문제에 대해 책임을 지지 않습니다.
>
>위험을 줄이기 위해 Adobe에서는 생산적인 사용을 시작하기 전에 샌드박스 환경에서 통합을 테스트하고, 이를 확인하거나 의존하기 전에 모든 MCP에서 시작한 작업과 응답을 주의 깊게 검토하고 확인하는 것을 권장합니다.

## 사전 요구 사항 {#tools-prerequisites}

[!DNL Adobe Target] 역할에 따라 사용 가능한 도구가 결정됩니다.

* **관찰자** 역할 이상: 모든 읽기 도구에 액세스
* **편집기** 역할: 읽기 및 쓰기(만들기) 도구에 액세스
* **승인자** 역할: 도구를 읽고 쓰고 활성화/비활성화하는 액세스 권한

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

<!--
+++Create an A/B activity

**Tool:** `create_ab_activity`

Create a new A/B test activity.

Creates a new A/B test with the specified configuration including experiences, offers, and targeting.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the activity |
| `state` | string | No | Initial state: `approved`, `deactivated`, or `saved` (default: `saved`) |
| `priority` | integer | No | Activity priority (0–999, default: 0) |
| `starts_at` | string | No | Activity start date (ISO 8601) |
| `ends_at` | string | No | Activity end date (ISO 8601) |
| `experiences` | array | Yes | List of experience configurations |
| `locations` | array | Yes | List of location/mbox configurations |
| `goals` | object | No | Primary and secondary goal metrics |
| `audiences` | array | No | Target audience configurations |
| `workspace_id` | string | No | Workspace ID for the activity |

**Returns:** The created activity object with its assigned ID.

**Example prompt:** "Create an A/B test called 'Homepage Hero Test' with two experiences testing different hero images on the homepage-hero mbox."

+++
-->

<!--
+++Create an Experience Targeting activity

**Tool:** `create_xt_activity`

Create a new Experience Targeting (XT) activity.

Creates an XT activity that delivers different experiences to different audiences based on targeting rules.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the activity |
| `state` | string | No | Initial state: `approved`, `deactivated`, or `saved` (default: `saved`) |
| `priority` | integer | No | Activity priority (0–999, default: 0) |
| `starts_at` | string | No | Activity start date (ISO 8601) |
| `ends_at` | string | No | Activity end date (ISO 8601) |
| `experiences` | array | Yes | List of experience configurations with audience mappings |
| `locations` | array | Yes | List of location/mbox configurations |
| `goals` | object | No | Primary and secondary goal metrics |
| `workspace_id` | string | No | Workspace ID for the activity |

**Returns:** The created activity object with its assigned ID.

**Example prompt:** "Create an Experience Targeting activity called 'Geo Personalization' that shows different content to visitors from different regions."

+++
-->

<!--
+++Update an A/B activity

**Tool:** `update_ab_activity`

Update an existing A/B activity.

Uses a read-modify-write pattern: fetches the current state, merges your changes, validates, and sends the update.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity to update |
| `activity` | object | Yes | Fields to update (name, priority, experiences, locations, goals, etc.) |

**Returns:** The updated activity object.

**Example prompt:** "Update activity 12345 to change the traffic allocation to 70/30."

+++
-->

<!--
+++Update an Experience Targeting activity

**Tool:** `update_xt_activity`

Update an existing Experience Targeting activity.

Uses a read-modify-write pattern.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the XT activity to update |
| `activity` | object | Yes | Fields to update |

**Returns:** The updated activity object.

**Example prompt:** "Update XT activity 12345 to add a new experience for mobile visitors."

+++
-->

<!--
+++Update an Automated Personalization activity

**Tool:** `update_abt_activity`

Update an existing Automated Personalization activity.

Uses a read-modify-write pattern.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the AP activity to update |
| `activity` | object | Yes | Fields to update |

**Returns:** The updated activity object.

**Example prompt:** "Update Auto-Personalization activity 12345 to change the optimization goal."

+++
-->

<!--
+++Update activity schedule

**Tool:** `update_activity_schedule`

Update activity start and end dates.

Updates the schedule for an activity without modifying other settings.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `activity_type` | string | Yes | Type of activity: `ab`, `xt`, or `abt` |
| `starts_at` | string | No | New start date (ISO 8601) |
| `ends_at` | string | No | New end date (ISO 8601) |

**Returns:** Confirmation of the schedule update.

**Example prompt:** "Update the schedule for A/B activity 12345 to run from May 1st to May 31st."

+++
-->

<!--
+++Change activity state

**Tool:** `update_activity_state`

Change activity state (activate, deactivate, or pause).

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `state` | string | Yes | New state: `approved` (live/active), `deactivated` (inactive), `paused`, or `saved` (draft) |

**Returns:** The updated activity state.

**Example prompt:** "Activate activity 12345" or "Pause the Homepage Hero Test."

+++
-->

<!--
+++Rename an activity

**Tool:** `update_activity_name`

Rename an activity.

Updates only the name without modifying the full configuration.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `name` | string | Yes | New activity name |

**Returns:** The updated activity object.

**Example prompt:** "Rename activity 12345 to 'Summer Campaign Hero Test'."

+++
-->

<!--
+++Change activity priority

**Tool:** `update_activity_priority`

Change activity priority.

Higher-priority activities take precedence when multiple activities target the same location.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `priority` | integer | Yes | New priority value (0–999; higher = higher priority) |

**Returns:** The updated activity object.

**Example prompt:** "Set the priority of activity 12345 to 100."

+++
-->

<!--
+++Add a variant to an activity

**Tool:** `add_activity_variant`

Add a new experience/variant to an activity.

Handles all structural coordination including creating options, mapping to locations, and rebalancing traffic.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name for the new experience/variant |
| `offer_id` | integer | No | (Form-based) Existing offer ID to use |
| `offer_content` | string | No | (Form-based) HTML content for a new inline offer |
| `traffic_percentage` | integer | No | Traffic % for the new variant (1–99). If omitted, traffic is rebalanced evenly |
| `audience_id` | integer | No | Audience ID for the variant (XT activities) |
| `modifications` | array | No | (VEC) List of CSS selector-based modifications |

**Returns:** The updated activity object.

**Example prompt:** "Add a new variant called 'Holiday Theme' to A/B activity 12345 using offer 67890."

+++
-->

<!--
+++Update traffic split

**Tool:** `update_traffic_split`

Update traffic allocation across variants.

The percentages must sum to exactly 100.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab` or `abt` (XT not supported — audience-targeted) |
| `splits` | object | Yes | Dictionary mapping experience name to percentage. Must include all experiences and sum to 100 |

**Returns:** The updated activity object.

**Example prompt:** "Change the traffic split for activity 12345 to 70% Control and 30% Variant A."

+++
-->

<!--
+++Change a variant's offer

**Tool:** `update_variant_offer`

Change the offer for a specific variant.

Works for both form-based activities (using `offer_id`) and VEC activities (using `modifications`).

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name of the experience/variant to update |
| `offer_id` | integer | No | (Form-based) New offer ID |
| `offer_content` | string | No | (Form-based) HTML content for a new inline offer |
| `modifications` | array | No | (VEC) New list of CSS selector-based modifications |

**Returns:** The updated activity object.

**Example prompt:** "Update the 'Variant A' experience in activity 12345 to use offer 99999."

+++
-->

<!--
+++Remove a variant from an activity

**Tool:** `remove_activity_variant`

Remove an experience/variant from an activity.

Removes the experience, cleans up orphaned options, and rebalances traffic evenly across remaining variants.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name of the experience/variant to remove |

**Returns:** The updated activity object.

**Example prompt:** "Remove the 'Test Variant' experience from A/B activity 12345."

+++
-->

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

<!--
+++Create an HTML offer

**Tool:** `create_target_offer`

Create a new HTML content offer.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the offer |
| `content` | string | Yes | HTML or text content for the offer |
| `workspace_id` | string | No | Workspace ID for the offer |

**Returns:** The created offer with its assigned ID.

**Example prompt:** "Create an HTML offer called 'Summer Sale Banner' with a promotional banner."

+++

+++Create a JSON offer

**Tool:** `create_target_json_offer`

Create a new JSON offer for delivering structured data.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the offer |
| `content` | object | Yes | JSON content for the offer |
| `workspace_id` | string | No | Workspace ID for the offer |

**Returns:** The created offer with its assigned ID.

**Example prompt:** "Create a JSON offer called 'Feature Flags Config' with feature toggle settings."

+++

+++Update an offer

**Tool:** `update_target_offer`

Update an existing offer.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `offer_id` | integer | Yes | The unique identifier of the offer to update |
| `name` | string | No | Updated offer name |
| `content` | string or object | No | Updated offer content |

**Returns:** The updated offer object.

**Example prompt:** "Update offer 67890 with new promotional content."

+++
-->

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

<!--
+++Create an audience

**Tool:** `create_target_audience`

Create a new audience with targeting rules.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the audience |
| `description` | string | No | Description of the audience |
| `targetRule` | object | No | Targeting rules (geo, browser, custom attributes, etc.) |
| `workspace_id` | string | No | Workspace ID for the audience |

**Returns:** The created audience with its assigned ID.

**Example prompt:** "Create an audience called 'Mobile Visitors from California' targeting mobile users in CA."

+++
-->

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

<!--
+++Create a response token

**Tool:** `create_target_response_token`

Create a new custom response token for collecting additional data in [!DNL Target] responses.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `token_name` | string | Yes | Name of the response token |
| `token_type` | string | Yes | Type of token: `SCRIPT`, `ACTIVITY`, `MBOX`, `GEO`, or `CRS` |

**Returns:** The created response token object.

**Example prompt:** "Create a custom response token called 'campaign_id' of type ACTIVITY."

+++
-->

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
| 활동 | 4 | `list_target_activities`, `get_ab_activity`, `get_xt_activity`, `get_abt_activity` |
| 오퍼 | 2 | `list_target_offers`, `get_target_offer` |
| 대상자 | 1 | `list_target_audiences` |
| Mbox | 3 | `list_target_mboxes`, `get_target_mbox`, `list_target_mbox_profile_attributes` |
| 속성 | 1 | `list_target_properties` |
| 보고 | 5 | `get_ab_performance_report`, `get_ab_orders_report`, `get_xt_performance_report`, `get_xt_orders_report`, `get_activity_report_by_name` |
| 미리보기 | 1 | `preview_activity` |
| 응답 토큰 | 1 | `list_target_response_tokens` |
| 개정 | 2 | `get_target_revisions`, `get_target_entity_revisions` |
| 템플릿 | 1 | `list_target_templates` |
| **합계** | **21** | |

## 관련 리소스 {#tools-related}

* [MCP 클라이언트 작업](target-mcp.md)
* [[!DNL Adobe Target] 관리 API 참조](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
