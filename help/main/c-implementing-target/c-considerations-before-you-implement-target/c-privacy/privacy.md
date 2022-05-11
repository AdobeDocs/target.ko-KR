---
keywords: 개인정보 보호;IP 주소;지리 특성;옵트아웃;옵트아웃;옵트아웃;데이터 개인정보 보호;정부 규정;규정;GDPR;CCPA
description: Adobe [!DNL Target] 이 IP 주소 수집 및 처리, 옵트아웃 지침을 포함하여 해당하는 데이터 개인정보 보호법을 준수하는 방법에 대해 알아봅니다.
title: ' [!DNL Target] 은 개인정보 보호 문제를 어떻게 처리합니까?'
feature: Privacy & Security
role: Developer
exl-id: fb632923-fa36-4553-88a6-f27860472eb6
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: ht
source-wordcount: '738'
ht-degree: 100%

---

# 개인정보 보호

[!DNL Adobe Target]은 사용자가 해당하는 데이터 개인정보 보호법을 준수하여 [!DNL Target]을 사용할 수 있도록 하는 프로세스 및 설정을 활성화했습니다.

## 기능 사용 데이터 수집

개별 기능 사용 데이터는 [!DNL Target] 기능이 의도한 대로 작동되는지 확인하거나 활용도가 낮은 기능을 식별하기 위해 [!DNL Adobe] 내부용으로 수집됩니다. 성능 관련 문제를 해결하기 위해 다양한 지연 시간 측정값이 수집됩니다. 개인 데이터는 수집되지 않습니다.

클라이언트 초기화 옵션에서 `telemetryEnabled`를 false로 설정하여 SDK의 사용 데이터를 보고하지 않도록 선택할 수 있습니다. 자세한 내용은 [telemetryEnabled in targetGlobalSettings](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#telemetry)를 참조하십시오.

## IP 주소 수집 {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

웹 사이트에 대한 방문자의 IP 주소가 Adobe Data Processing Center(DPC)로 전송됩니다. 방문자에 대한 네트워크 구성에 따라서는 이 IP 주소가 반드시 방문자의 컴퓨터 IP 주소를 나타내지는 않습니다. 예를 들어 IP 주소가 NAT(Network Address Translation) 방화벽, HTTP 프록시 또는 인터넷 게이트웨이의 외부 IP 주소일 수 있습니다. Target은 사용자의 IP 주소 또는 PII(개인 식별이 가능한 정보)를 저장하지 않습니다. IP 주소는 세션 중에 Target에서만 사용됩니다(인메모리, 유지되지 않음)

## IP 주소의 마지막 옥텟 대체 {#section_AE84EB0D7CE04E93B279B77732ADD61E}

Adobe는 Adobe Target에 대해 Adobe Client Care에서 활성화할 수 있는 새로운 “Privacy by Design” 설정을 개발했습니다. 이 설정을 활성화할 경우, 이 IP 주소가 Adobe에 의해 수집되면 즉시 IP 주소의 마지막 옥텟(마지막 부분)이 표시되지 않게 됩니다. 이러한 익명화는 선택 사항인 IP 주소의 지역 조회를 포함하여, IP 주소의 모든 처리 이전에 수행됩니다.

이 기능이 활성화되어 있으면 IP 주소가 충분히 익명으로 변경되므로 더 이상 개인 정보로 식별되지 않습니다. 결과적으로 Adobe Target은 개인 정보 수집을 허용하지 않는 국가의 데이터 개인정보 보호 법률을 준수하며 사용할 수 있습니다. 도시 수준의 정보를 획득하는 것은 IP 주소 난독화의 영향을 크게 받을 수 있습니다. 지역 및 국가 수준의 정보를 획득하는 것은 IP 주소 난독화의 영향을 약간만 받아야 합니다.

다음 설정을 사용할 수 있습니다.

* 난독화 없음: Target이 IP 주소의 어떤 부분도 숨기지 않습니다.
* 마지막 옥텟: Target이 IP 주소의 마지막 옥텟을 숨깁니다.
* 전체 IP: Target이 전체 IP 주소를 숨깁니다.

Target은 전체 IP 주소를 수신하고 지정된 대로 이를 난독화합니다([마지막 옥텟] 또는 [전체 IP]로 설정한 경우). 그런 다음 Target은 난독화된 IP 주소를 세션 동안 메모리에 보관합니다.

>[!NOTE]
>
>현재 사용 중인 설정을 확인하거나 IP 난독화 기능을 활성화하려면 [Adobe 클라이언트 지원 센터에 문의](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)하십시오.

## 지리 특성 {#section_BB69F96559BD44BDA4177537C4A5345A}

IP 주소의 마지막 옥텟 대체를 활성화하는 경우, IP 주소의 나머지 값은 Adobe Target에서 보고서를 사용하여 분석할 수 있습니다. IP 주소의 마지막 옥텟이 난독화되지 않는다면 Adobe Target에서 전체 IP 주소를 분석할 수 있습니다. 지리 특성 기능을 사용하여 지리적 영역별로 방문자 위치를 매핑할 수 있습니다. 지리 특성 데이터는 개인 수준이 아니라 도시 수준이나 우편번호 수준으로만 세분화됩니다.

IP 주소가 완전히 난독화된 경우 지리 특성 및 지역 타기팅을 사용할 수 없습니다.

## 옵트아웃 링크 {#section_E7A62B7B99C94B3A806CB262D16E27FC}

옵트아웃 링크를 사이트에 추가하여 방문자가 모든 계산 및 콘텐츠 제공을 옵트아웃(탈퇴)할 수 있도록 합니다.

1. 사이트에 다음 링크를 추가합니다.

   `<a href="https://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>`

1. (조건부) CNAME을 사용 중인 경우 링크는 “client=`clientcode`” 매개변수를 포함해야 합니다.
(예: https://my.cname.domain/optout?client=clientcode.)

1. `clientcode`를 귀하의 클라이언트 코드로 대체한 다음 옵트아웃 URL에 연결할 텍스트 또는 이미지를 추가하십시오.

이 링크를 클릭하는 모든 방문자는 쿠키를 삭제하기 전까지 또는 2년 동안(어느 쪽이든 먼저 만족되는 조건 적용) 브라우징 세션에서 호출된 어떤 mbox 요청에도 포함되지 않습니다. 이 기능은 `disableClient`라는 방문자의 쿠키를 `clientcode.tt.omtrdc.net` 도메인에서 설정하면 작동합니다.

퍼스트 파티 쿠키 구현을 사용하더라도 제공된 옵트아웃은 서드파티 쿠키를 통해 설정됩니다. 클라이언트가 퍼스트 파티 쿠키만 사용하는 경우 Target은 옵트아웃 쿠키가 설정되어 있는지 여부를 확인합니다.

## 개인정보 보호 및 데이터 보호 규정

유럽 연합의 일반 데이터 정보 보호 규정(GDPR), 캘리포니아 소비자 개인정보 보호법(CCPA) 및 기타 국제 개인정보 보호 요구 사항, 그리고 이러한 규정이 귀사 및 Adobe Target에 미치는 영향에 대한 자세한 내용은 [개인정보 보호 및 데이터 보호 규정](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md)을 참조하십시오.
