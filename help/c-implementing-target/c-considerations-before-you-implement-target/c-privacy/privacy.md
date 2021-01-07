---
keywords: privacy;ip address;geosegmentation;opt out;optout;opt-out;data privacy;government regulations;regulations;gdpr;ccpa
description: Adobe Target은 적용 가능한 데이터 개인 정보 보호 법률에 따라 Target을 사용할 수 있도록 허용하는 프로세스 및 설정을 제공합니다.
title: 개인 정보 보호
feature: Privacy & Security
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 76%

---


# 개인 정보 보호

[!DNL Adobe Target] 사용 가능한 프로세스 및 설정을 사용하여 해당 데이터 개인 정보 보호 법 [!DNL Target] 을 준수하는 데 사용할 수 있습니다.

## IP 주소 모음 {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

웹 사이트에 대한 방문자의 IP 주소가 Adobe Data Processing Center(DPC)로 전송됩니다. 방문자에 대한 네트워크 구성에 따라서는, 이 IP 주소가 꼭 방문자의 컴퓨터 IP 주소를 나타내지는 않습니다. 예를 들어 IP 주소가 NAT(Network Address Translation) 방화벽, HTTP 프록시 또는 인터넷 게이트웨이의 외부 IP 주소일 수 있습니다. Target은 사용자의 IP 주소 또는 PII(개인 식별이 가능한 정보)를 저장하지 않습니다. IP 주소는 세션 기간 동안(메모리 내, 지속되지 않음) Target에서만 사용됩니다.

## IP 주소 {#section_AE84EB0D7CE04E93B279B77732ADD61E}의 마지막 8진수 교체

Adobe는 Adobe Target에 대해 Adobe Client Care에서 활성화할 수 있는 새로운 “Privacy by Design” 설정을 개발했습니다. 이 설정을 활성화할 경우, 이 IP 주소가 Adobe에 의해 수집되면 즉시 IP 주소의 마지막 옥텟(마지막 부분)이 표시되지 않게 됩니다. 이러한 익명화는 선택 사항인 IP 주소의 지역 조회를 포함하여, IP 주소의 모든 처리 이전에 수행됩니다.

이 기능이 활성화되어 있으면 IP 주소가 충분히 익명으로 변경되므로 더 이상 개인 정보로 식별되지 않습니다. 결과적으로, Adobe Target은 개인 정보 수집을 허용하지 않는 국가의 데이터 개인 정보 보호 법률을 준수하며 사용할 수 있습니다. 도시 수준의 정보를 획득하는 것은 IP 주소 난독화의 영향을 크게 받을 수 있습니다. 지역 및 국가 수준의 정보를 획득하는 것은 IP 주소 난독화의 영향을 약간만 받아야 합니다.

다음 설정을 사용할 수 있습니다.

* 난독화 없음:Target은 IP 주소의 일부를 숨기지 않습니다.
* 마지막 8진수:Target은 IP 주소의 마지막 8진수를 숨깁니다.
* 전체 IP:Target은 전체 IP 주소를 숨깁니다.

Target은 지정된 대로 전체 IP 주소를 수신하고 이를 난독화(마지막 8진수 또는 전체 IP로 설정된 경우)합니다. 그런 다음 Target은 세션 동안 난독화된 IP 주소를 메모리에 저장합니다.

>[!NOTE]
>
>[Adobe Client Care에 ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) 문의하여 현재 사용 중인 설정을 결정하거나 IP 난독화 기능을 사용하도록 설정하십시오.

## 지리 특성 {#section_BB69F96559BD44BDA4177537C4A5345A}

IP 주소의 마지막 옥텟 대체를 활성화하는 경우, IP 주소의 나머지 값은 Adobe Target에서 보고서를 사용하여 분석할 수 있습니다. IP 주소의 마지막 옥텟이 난독화되지 않는다면, Adobe Target에서 전체 IP 주소를 분석할 수 있습니다. 지리 특성 기능을 사용하여 지리적 영역별로 방문자 위치를 매핑할 수 있습니다. 지리 특성 데이터는 개인 수준이 아니라 도시 수준이나 우편 번호 수준으로만 세분화됩니다.

IP 주소가 완전히 난독화된 경우 지리 특성 및 지역 타깃팅을 사용할 수 없습니다.

## 옵트아웃 링크 {#section_E7A62B7B99C94B3A806CB262D16E27FC}

옵트아웃 링크를 사이트에 추가하여 방문자가 모든 계산 및 컨텐츠 제공을 옵트아웃(탈퇴)할 수 있도록 합니다.

1. 사이트에 다음 링크를 추가합니다. 

   `<a href="https://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>`
1. `clientcode` 텍스트를 사용자의 클라이언트 코드로 바꾸고 옵트아웃 URL에 연결할 텍스트나 이미지를 추가합니다.

이 링크를 클릭하는 모든 방문자는 쿠키를 삭제하기 전까지 또는 2년 동안(어느 쪽이든 먼저 만족되는 조건 적용) 브라우징 세션에서 호출된 어떤 mbox 요청에도 포함되지 않습니다. 이 기능은 `disableClient`라는 방문자의 쿠키를 `clientcode.tt.omtrdc.net` 도메인에서 설정하면 작동합니다.

퍼스트 파티 쿠키 구현을 사용하더라도 제공된 옵트아웃은 타사 쿠키를 통해 설정됩니다. 클라이언트가 퍼스트 파티 쿠키만 사용하는 경우 Target은 옵트아웃 쿠키가 설정되어 있는지 여부를 확인합니다.

## 개인 정보 보호 및 데이터 보호 규정

유럽연합(EU)의 개인 정보 보호 규정(GDPR), 캘리포니아 소비자 개인 정보 보호 법(CPA) 및 기타 국제 개인 정보 보호 요구 사항에 대한 정보와 이러한 규정이 조직 및 Adobe Target에 미치는 영향을 확인하려면 [개인 정보 보호 및 데이터 보호 규정](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md)을 참조하십시오.
