---
keywords: 사용자 지정 기준 만들기;알고리즘;기준;권장 사항 기준;csv;ftp;csv 업로드
description: CSV 파일을 업로드하여 Adobe에서 권장 사항을 사용자 지정하는 방법을 알아봅니다 [!DNL Target] Recommendations.
title: Recommendations에서 사용자 지정 기준을 업로드하려면 어떻게 합니까?
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 39%

---

# ![PREMIUM](/help/main/assets/premium.png) 사용자 지정 기준 업로드

CSV 파일을 업로드하여 권장 사항을 사용자 지정합니다. [!DNL Adobe Target].

[!UICONTROL 새 기준 만들기] 화면에 도달하는 여러 방법이 있습니다. 일부 화면 옵션은 화면에 도달하는 방법에 따라 달라집니다.

* 설정 **[!UICONTROL Recommendations]** > **[!UICONTROL 기준]** 라이브러리 화면에서 **[!UICONTROL 기준 만들기]** > **[!UICONTROL 기준 만들기]**. 여기서 만드는 기준은 자동으로 모든 [!DNL Recommendations] 활동에 사용 가능해집니다.
* 만들기 [!DNL Recommendations] 활동을 사용하여 [!UICONTROL 시각적 경험 작성기] (VEC) 즉시 로 이동됩니다. [!UICONTROL 기준 선택] 페이지에서 요소를 선택한 후 화면을 선택하고 [!UICONTROL Recommendations으로 바꾸기], [!UICONTROL 앞에 Recommendations 삽입], 또는 [!UICONTROL 다음 항목 뒤에 Recommendations 삽입]. 그런 다음 사용 가능한 기준을 선택하거나 **[!UICONTROL 기준 만들기]**. 새 기준을 만드는 경우 다른 기준과 함께 사용할 기준을 저장할 수 있습니다 [!DNL Recommendations] 활동. 자세한 내용은 [Recommendations 활동 만들기](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* [!DNL Recommendations] 활동을 편집하는 경우 페이지에서 [!UICONTROL 권장 사항 위치] 상자를 클릭하고 **[!UICONTROL 기준 변경]**&#x200B;을 선택합니다. 설정 [!UICONTROL 기준 선택] 을 클릭하고 **[!UICONTROL 기준 만들기]**. 다른 사용자와 함께 사용할 새 기준을 저장할 수 있습니다 [!DNL Recommendations] 활동.

다음 절차에서는 [!UICONTROL 새 기준 만들기] 첫 번째 방법을 사용하여 화면: a **[!UICONTROL Recommendations]** > **[!UICONTROL 기준]** 라이브러리 화면.

1. 클릭 **[!UICONTROL Recommendations]** > **[!UICONTROL 기준]**.

1. **[!UICONTROL 기준 만들기]**&#x200B;를 클릭합니다.

1. 정보를 [기본 정보](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) 섹션을 참조하십시오.

   1. 에서 **[!UICONTROL 알고리즘 선택]** 드롭다운 목록을 입력하고 다음을 선택합니다 **[!UICONTROL 사용자 지정 기준]**.

   1. 에서 **[!UICONTROL 알고리즘]** 드롭다운 목록에서 **[!UICONTROL 사용자 지정 알고리즘]**.

      >[!NOTE]
      >
      >이전 단계로 인해 [!UICONTROL CSV 업로드] 섹션 아래쪽에서 표시할 섹션 [!UICONTROL 새 기준 만들기] 대화 상자

1. (조건부) [백업 컨텐츠](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) 섹션을 참조하십시오.

1. (조건부) [포함 규칙 을 참조하십시오](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) 섹션을 참조하십시오.

1. 에서 **[!UICONTROL CSV 업로드]** 섹션에서 **[!UICONTROL 위치]** CSV 파일로 내보낼 때 시간별 세부기간이 작동하지 않는 문제를 해결했습니다.

   ![CSV 섹션 업로드](assets/upload-csv.png)

   CSV 파일을 성공적으로 업로드하려면 형식이 올바르게 지정되어야 합니다. **[!UICONTROL CSV 템플릿 다운로드]**&#x200B;를 클릭하여 올바른 형식의 CSV 파일을 가져옵니다.

   다음 두 가지 위치 옵션이 있습니다.

   * **FTP:** FTP 서버에서 CSV 파일을 업로드하려면 **[!UICONTROL FTP]**&#x200B;를 선택한 다음, 필요한 정보를 입력합니다. SSL을 사용할 수 있습니다. SSL은 FTPS 프로토콜을 사용하여 CSV 파일을 안전하게 전송합니다.
   * **URL:** URL에서 CSV 파일을 업로드하려면 을(를) 선택합니다 **[!UICONTROL URL]**&#x200B;를 입력한 다음 피드 URL을 입력합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 고려 사항

* 사용자 지정 기준 엔티티(행)에는 최대 1,000개의 권장 항목(열)이 포함될 수 있습니다.

* 사용자 지정 기준 업데이트는 기본적으로 &quot;누적&quot;입니다. CSV 업로드 파일에 지정된 새 키-값 쌍이 기존 키-값 쌍을 덮어씁니다. CSV 업로드에 지정된 키가 없는 기존 키-값 쌍은 계속 제공할 수 있으며, CSV 파일의 일부로 마지막으로 업로드한 후 31일 후에 만료됩니다.

   Client Care에 문의하여 다음 CSV 업로드에 포함되지 않은 기존 결과를 삭제하도록 설정을 활성화합니다. 이 설정이 활성화되어 있으면 사용자 지정 CSV 피드 파일에 있는 키만 전달할 수 있습니다. 이 설정은 모든 사용자 지정 기준에 적용됩니다.

* 사용자 지정 기준 피드는 24시간마다 한 번씩 업데이트됩니다.

   의 각 기준 카드 하단에 있는 사용자 지정 기준 업로드의 업로드 및 동기화 상태를 확인할 수 있습니다 [!UICONTROL Recommendations] > [!UICONTROL 기준] 페이지. 에서 상태를 확인할 수도 있습니다 [!UICONTROL 편집] 사용자 지정 기준을 편집할 때 나타나는 대화 상자

* 오류가 없는 업로드의 흐름은 다음과 같습니다. [!UICONTROL 예약됨] > [!UICONTROL 피드 파일 다운로드 중] > [!UICONTROL 가져오는 중] > [!UICONTROL 성공].

* 다음은 발생 가능한 오류 메시지입니다 [!DNL Target] 업로드에 문제가 발생합니다.

   | 오류 메시지 | 세부 사항 |
   |--- |--- |
   | 알 수 없는 오류 | 내부 기술 오류를 나타냅니다. |
   | 구문 분석 오류 | 피드 파일 형식에 문제가 있을 수 있습니다. 파일 형식을 수정하고 알고리즘을 다시 저장하여 파일 다운로드 프로세스를 다시 시작합니다. |
   | 서버를 찾을 수 없음 | 인터넷에 표시되는 IP 또는 호스트 이름을 제공하십시오. |
   | 자격 증명 오류 | 서버의 활성 계정에 대한 유효한 사용자 및 암호를 제공합니다. |
   | 디렉토리를 찾을 수 없음 | 서버에 존재하는 디렉토리를 지정합니다. |
   | 파일을 찾을 수 없음 | 표시된 디렉토리의 서버에 있는 파일의 이름을 제공합니다. |

## 교육 비디오: 추천에서 기준 만들기(12:33) ![튜토리얼 배지](/help/main/assets/tutorial.png)

이 비디오에는 다음 정보가 포함되어 있습니다(사용자 지정 기준 업로드에 대한 자세한 내용은 11:43부터 시작).

* 기준 만들기
* 기준 시퀀스 만들기
* 사용자 지정 기준 업로드

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
