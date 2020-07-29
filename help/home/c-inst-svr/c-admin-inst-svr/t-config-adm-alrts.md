---
description: 관리 경고는 정상적인 작업 과정 동안 Insight Server에서 오류가 감지되면 지정된 이메일 주소로 이메일 알림을 보냅니다.
solution: Insight
title: 관리 경고 구성
uuid: 398e088b-ff83-46ae-a20c-ba0b50d85702
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 관리 경고 구성{#configuring-administrative-alerts}

관리 경고는 정상적인 작업 과정 동안 Insight Server에서 오류가 감지되면 지정된 이메일 주소로 이메일 알림을 보냅니다.

**권장 빈도:** 제작 전

>[!NOTE]
>
>관리 경고를 사용하려면 전달 SMTP 서버에 대한 액세스 권한이 [!DNL Insight Server] 있어야 이메일을 통해 경고를 전송할 수 있습니다.

이메일 알림 수신자는 주요 시스템 관리 담당자 및 주요 이해 관계자입니다.

관리 경고 파일 [!DNL Administrative Alerts.cfg]은 에 대한 관리 경고를 구성하는 데 사용됩니다 [!DNL Insight Server].

>[!NOTE]
>
>클러스터를 실행하는 경우 클러스터의 마스터에 대한 경고를 생성하거나 수정해야 [!DNL Insight Server] 합니다.

**관리 경고를 만들거나 수정하려면**

1. &#x200B;> [!DNL Insight]탭에서 [!DNL Admin] [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 구성할 아이콘 을 마우스 오른쪽 단추로 [!DNL Insight Server] 클릭하고 **[!UICONTROL Server Files]**&#x200B;클릭합니다.
1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Components]** 봅니다. 이 [!DNL Administrative Alerts.cfg] 파일은 이 디렉토리 내에 있습니다.
1. 에 대한 *server name *열의 확인 표시를 마우스 오른쪽 단추로 [!DNL Administrative Alerts.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. 에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다 [!DNL Administrative Alerts.cfg].
1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Insight]**&#x200B;을 클릭합니다.
1. 창에서 [!DNL Administrative Alerts.cfg] 을 클릭하여 내용을 **[!UICONTROL component]** 봅니다.
1. 원하는 대로 매개 변수를 채웁니다. 이 파일에서 사용할 수 있는 매개 변수의 목록은 관리 경고 구성 [설정을 참조하십시오](../../../home/c-inst-svr/c-cfg-stgs-ref/c-admin-alts-cfg-stgs.md#concept-14c3c3ed797f47c5900ec04cae2fc491).

   ![단계 정보](assets/cfg_adminalerts_examplevalues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager]열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *를 선택합니다&#x200B;**[!UICONTROL server name]***.

1. (선택 사항) 클러스터에서 작업 중이고 각 데이터 처리 장치에 동일한 관리 경고를 적용하려면 업데이트된 [!DNL Administrative Alerts.cfg] 파일을 복사하여 마스터 [!DNL Components for Processing Servers] 설치 디렉토리 내의 [!DNL Insight Server] 폴더에 붙여 넣어야 합니다.
