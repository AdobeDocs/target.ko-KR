---
title: 기능 플래그 보고를 위한 CJA 설정
description: Customer Journey Analytics을 통해 기능 플래그 및 기능 그룹 보고서를 보는 데 필요한 데이터스트림, 연결 및 데이터 보기를 구성합니다.
badge: label="Beta" type="Informative"
hide: true
exl-id: 57bd1106-2b3d-4e03-882a-acfef1c0df66
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 4%

---

# 기능 플래그 보고를 위한 CJA 설정 {#set-up-cja-reporting}

플래그와 Adobe Customer Journey Analytics(CJA) 간의 통합은 기능 플래그 변형의 비즈니스 영향을 측정하는 통합된 방법을 제공합니다. 언제든지 CJA 성공 지표를 플래그 보고서에 적용하고 [실험 패널](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-workspace/panels/experimentation)과 같은 Customer Journey Analytics 기능을 활용하여 실험 성능을 평가하고 기능 변형이 고객 행동에 미치는 영향을 파악합니다.

## 고려 사항 {#considerations}

Customer Journey Analytics 및 플래그 통합을 사용하기 전에 다음 정보를 고려하십시오.

* 귀하와 귀하의 조직은 Adobe Customer Journey Analytics(CJA)에 액세스할 수 있어야 합니다.
* 플래그 노출 이벤트에 대한 **AJO ExD 결정 이벤트 데이터 집합**&#x200B;을(를) 샌드박스에서 프로비저닝해야 합니다.
* 성공 지표로 사용하려는 성공 전환 이벤트가 포함된 데이터 세트를 사용할 수 있어야 합니다.

## 데이터 스트림 설정 {#set-up-datastream}

>[!NOTE]
>
>이 안내서에서는 Commerce 경험 이벤트 데이터 세트와 `commerce.purchases.value`을(를) 예로만 사용합니다. 사용 사례에 적합한 스키마 및 매핑된 성공 지표 필드를 선택합니다.

1. 데이터 수집에서 **데이터스트림**(으)로 이동하여 플래그 노출 데이터스트림을 만들거나 엽니다.
1. 매핑 스키마를 **AJO ExD 결정 이벤트 스키마**(으)로 설정합니다.
1. 데이터 스트림을 열고 **서비스 추가**&#x200B;를 선택합니다.
1. 기존 **AJO ExD 결정 이벤트 데이터 세트**&#x200B;를 이벤트 데이터 세트로 선택하고 저장합니다.

![데이터 스트림 매핑 스키마로 AJO ExD 결정 이벤트 스키마 선택](assets/flags-datastream-select-mapping-schema-2026-07-21.jpeg)

![데이터 스트림에 서비스 옵션 추가](assets/flags-datastream-add-service-2026-07-21.jpeg)

![이벤트 데이터 세트로 AJO ExD 결정 이벤트 데이터 세트 선택](assets/flags-datastream-select-event-dataset-2026-07-21.jpeg)

>[!NOTE]
>
>방금 만든 데이터 스트림 ID는 데이터 수집 태그에서 플래그 확장을 구성하는 데 사용됩니다.

## Customer Journey Analytics 연결 설정 {#set-up-connection}

이미 연결을 설정한 경우 기존 연결을 사용하고 아래 3단계로 건너뛸 수 있습니다. 연결을 통해 Customer Journey Analytics은 보고를 위해 데이터 세트에서 데이터를 가져오기 시작할 수 있습니다.

1. Customer Journey Analytics의 **연결** 페이지에서 **새 연결 만들기**&#x200B;를 선택합니다.
1. 올바른 정보로 [연결 및 데이터 설정](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-connections/overview)을 구성하십시오.
1. 데이터 스트림을 구성할 때 사용한 ExD 이벤트 데이터 세트를 추가합니다.
1. 전환 이벤트로 사용할 데이터 집합을 추가한 다음 **다음**&#x200B;을 선택합니다.
1. **데이터 세트 추가** 대화 상자에서 선택한 각 데이터 세트에 대한 [설정](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-connections/create-connection#dataset-settings)을 하나씩 구성합니다.

![데이터 세트를 추가하기 전에 데이터 세트 추가 대화 상자](assets/cja-connection-new-add-datasets-empty.png)

![연결에 추가할 플래그 및 상거래 데이터 세트 선택](assets/cja-connection-select-datasets-flags-commerce.png)

![ID 맵 구성을 표시하는 데이터 집합 설정 대화 상자](assets/cja-connection-dataset-settings-identity-map.png)

## 데이터 보기 설정 {#set-up-data-view}

Customer Journey Analytics에서 데이터 보기를 설정합니다. 데이터 보기는 연결의 데이터가 올바르게 사용될 수 있는지 보장합니다.

1. 데이터 보기를 설정하고 위에서 만든 연결을 가리키는지 확인합니다. 자세한 내용은 *Adobe Customer Journey Analytics 안내서*&#x200B;에서 [데이터 보기 만들기 또는 편집](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-dataviews/create-dataview)을 참조하세요.
1. **데이터 관리** > **데이터 보기**(으)로 이동합니다.
1. **새 데이터 보기 만들기**&#x200B;를 선택하고 플래그 CJA 연결을 선택합니다.
1. 데이터 보기 이름 및 안정적인 외부 ID를 입력합니다.
1. 표준 시간대 및 일정 설정을 확인한 다음 **구성 요소**&#x200B;를 계속합니다.

![새 데이터 보기 구성](assets/cja-dataview-create-configure-2026-07-21.jpeg)

### 실험 및 변형 차원 구성 {#configure-experiment-variant-dimensions}

1. **플래그 엔터티 ID**&#x200B;에 매핑된 `_experience.decisioning.propositions.scopeDetails.activity.id`을(를) 차원에 추가하고 이름을 &quot;플래그 엔터티 ID&quot; 또는 다른 분석가에게 친숙한 이름으로 바꾸십시오.
1. 컨텍스트 레이블을 &quot;실험 실험&quot;으로 설정합니다.
1. `_experience.decisioning.propositions.scopeDetails.experience.id`(기능 플래그 또는 기능 그룹의 변형에 매핑됨)을(를) 차원에 추가합니다.
1. 컨텍스트 레이블을 &quot;실험 변형&quot;으로 설정합니다.

![스키마에서 활동 및 경험 식별자 찾기 및 추가](assets/cja-dataview-components-activity-identifier.png)

![실험 및 실험 변형 컨텍스트 레이블 할당](assets/cja-dataview-flags-entity-context-labels.png)

>[!WARNING]
>
>두 실험 컨텍스트 레이블이 모두 없으면 CJA 실험 패널은 플래그 실험 및 변형을 식별할 수 없습니다.

### 지속성 및 속성 구성 {#configure-persistence-attribution}

노출이 나중에 전환하기 위해 크레딧을 받을 수 있도록 차원 및 지표를 구성합니다. 적절한 지속성 또는 속성이 없으면 CJA은 노출과 동일한 이벤트에서 발생하는 결과만 연결할 수 있습니다.

1. 지표 아래에 `commerce.purchases.value`과(와) 같은 필수 전환 필드를 추가합니다.
1. 지표에 **구매 값**&#x200B;과 같이 명확한 이름을 지정하십시오.
1. 속성을 활성화하고 분석에 필요한 모델(마지막 터치, 첫 번째 터치, 기여도 또는 동일 터치)을 선택합니다. 기여도 분석 모델, 컨테이너 및 전환 확인 기간에 대한 자세한 내용은 [기여도 분석 구성 요소](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-workspace/attribution/models)를 참조하십시오.
1. 실험 전략과 일치하는 컨테이너 및 전환 확인 기간을 선택하십시오. 방문 또는 세션 인식 전환 확인이 있는 개인 컨테이너는 일반적인 시작점이지만, 사용 사례에 맞게 유효성을 검사합니다.
1. 데이터 보기를 저장합니다.

![변형에 대한 구매 값 지표 이름 지정](assets/cja-dataview-metrics-variant-purchase.png)

![속성 모델 옵션](assets/cja-dataview-attribution-models.png)

## 참조: {#see-also}

* [보고](reporting.md)

<!-- -->
