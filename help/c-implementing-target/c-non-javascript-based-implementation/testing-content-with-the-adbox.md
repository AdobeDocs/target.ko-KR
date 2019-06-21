---
description: AdBox를 사용하여 오프사이트 구현에서 이미지를 전달하십시오.
keywords: 구현;mbox.js 비JavaScript;mbox;adbox
seo-description: AdBox를 사용하여 오프사이트 구현에서 이미지를 전달하십시오.
seo-title: 이미지용 Adbox 만들기
solution: Target
subtopic: 시작하기
title: 이미지용 Adbox 만들기
topic: Standard
uuid: 6b1763f7-08de-4bde-9e20-e79b92b02f20
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# 이미지용 Adbox 만들기{#create-an-adbox-for-an-image}

AdBox를 사용하여 오프사이트 구현에서 이미지를 전달하십시오.

AdBox는 mbox와 비슷하지만 JavaScript가 아니라 URL로 제어됩니다. AdBox는 &quot;광고&quot; mbox(또는 AdBox)를 자신의 Adobe 계정으로 로드하는 특별한 AdBox URL로 만들어집니다. 이 AdBox를 활동에서 mbox 대신 사용합니다. 이메일 또는 기타 비 자바스크립트 구현에서 직접 이미지 참조 대신 AdBox URL을 사용합니다.

올바른 설정을 선택하는 데 도움이 필요하면  [비 JavaScript 기반 구현](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4).

1. AdBox URL을 만듭니다.

   ```
   https://myClientCode.tt.omtrdc.net/m2/myClientCode/ubox/
   image?mbox=emailHeroImage123_320x200
   mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif
   ```

   * 여기서 `myClientCode`는 회사의 클라이언트 코드입니다. 회사의 클라이언트 코드는 모두 소문자이고 특수 문자를 포함하지 않습니다.

      * **at.js**: 클라이언트 코드는 [!UICONTROL 인터페이스의 ]설정 &gt; 구현 &gt; at.js 설정 편집[!DNL Target] 페이지 맨 위에서 사용할 수 있습니다.

      * **mbox.js**: 클라이언트 코드는 [!UICONTROL 설정 &gt; 구현 &gt; Mbox.js 설정 편집] 페이지 맨 위에서 사용할 수 있습니다.
   * 여기서 `image`는 호출 유형입니다. 이 경우 이미지입니다.

   * 여기서 `emailHeroImage123_320x200`은 AdBox의 이름입니다.

   * 여기서 `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif`는 mbox의 기본 콘텐츠입니다. 이것은 이미지여야 합니다.

      이것은 URL로 인코딩되어야 하고 절대 참조여야 합니다. [HTML URL 인코딩 참조](https://www.w3schools.com/tags/ref_urlencode.asp)를 사용하여 URL을 신속하게 인코딩할 수 있습니다.


1. 각 대체 이미지에 대한 [리디렉션 오퍼](../../c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94)를 만듭니다.

   >[!NOTE] {class=&quot;- topic/note &quot;}
   >
   >AdBox는 리디렉션 오퍼 또는 기본 컨텐츠 오퍼와 함께 로드되어야 합니다. 다른 오퍼 유형은 작동하지 않습니다. AdBox는 URL이므로 수신하는 URL만 표시할 수 있으며, 따라서 리디렉션 오퍼만 작동합니다.

1. 활동을 만듭니다.

   목표를 충족하는 올바른 설정을 알려면 [비JavaScript 기반 구현](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4)을 참조하십시오.
1. 활동에 대한 QA를 완료합니다.

   우수 사례로, 더미 페이지를 만들고 모든 경험, 기본 컨텐츠 및 보고서가 모든 브라우저 유형에서 모든 환경에 대해 예상대로 작동하는지 확인합니다. 1. 활동을 실행합니다.
