---
description: 관리 경고는 정상적인 작업 과정 동안 Insight 서버에서 오류가 감지되면 지정된 이메일 주소로 이메일 알림을 보냅니다.
solution: Analytics
title: 관리 경고 구성
uuid: 398e088b-ff83-46ae-a20c-ba0b50d85702
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 2%

---


# 관리 경고 구성{#configuring-administrative-alerts}

관리 경고는 정상적인 작업 과정 동안 Insight 서버에서 오류가 감지되면 지정된 이메일 주소로 이메일 알림을 보냅니다.

**권장 빈도:** 제작 전

>[!NOTE]
>
>관리 경고를 사용하려면 전송 SMTP 서버에 액세스할 수 [!DNL Insight Server] 있어야 이메일로 경고를 전송할 수 있습니다.

이메일 알림의 수신자는 핵심 시스템 관리 담당자 및 주요 이해 관계자입니다.

관리 경고 파일 [!DNL Administrative Alerts.cfg]은 관리 경고를 구성하는 데 사용됩니다 [!DNL Insight Server].

>[!NOTE]
>
>클러스터를 실행 중인 경우 클러스터의 마스터에 대한 경고를 생성하거나 수정해야 [!DNL Insight Server] 합니다.

**관리 경고를 생성하거나 수정하려면**

1. 서버 관리자 작업 영역 [!DNL Insight]을 열려면 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭합니다.
1. 구성할 아이콘 [!DNL Insight Server] 을 마우스 오른쪽 단추로 클릭하고 클릭합니다 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]을 클릭하여 콘텐츠 **[!UICONTROL Components]** 를 봅니다. 이 디렉터리 내에 [!DNL Administrative Alerts.cfg] 파일이 있습니다.
1. 에 대해 *server name *열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 [!DNL Administrative Alerts.cfg] 클릭합니다 **[!UICONTROL Make Local]**. 에 대한 열에 확인 표시가 [!DNL Temp] 나타납니다 [!DNL Administrative Alerts.cfg].
1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** 를 **[!UICONTROL in Insight]**&#x200B;클릭합니다.
1. 창에서 [!DNL Administrative Alerts.cfg] 을 클릭하여 내용 **[!UICONTROL component]** 을 봅니다.
1. 원하는 대로 매개 변수를 채웁니다. 이 파일에서 사용할 수 있는 매개 변수의 목록은 관리 경고 [구성 설정을 참조하십시오](../../../home/c-inst-svr/c-cfg-stgs-ref/c-admin-alts-cfg-stgs.md#concept-14c3c3ed797f47c5900ec04cae2fc491).

   ![단계 정보](assets/cfg_adminalerts_examplevalues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 위쪽 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 열 [!DNL Server Files Manager]에 있는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *을 선택합니다&#x200B;**[!UICONTROL server name]***.

1. (선택 사항) 클러스터에서 작업하는 경우 각 데이터 처리 장치에 동일한 관리 경고를 적용하려면 업데이트된 [!DNL Administrative Alerts.cfg] 파일을 복사하여 마스터 [!DNL Components for Processing Servers] 설치 디렉토리 내의 [!DNL Insight Server] 폴더에 붙여넣어야 합니다.
