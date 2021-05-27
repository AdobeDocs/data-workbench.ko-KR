---
description: 관리 경고는 일반 작업 과정 중에 Insight Server에서 오류가 감지되면 지정된 이메일 주소로 이메일 알림을 보냅니다.
title: 관리 경고 구성
uuid: 398e088b-ff83-46ae-a20c-ba0b50d85702
exl-id: 886e390f-fb2c-4922-8b01-9e5133a94e1b
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 2%

---

# 관리 경고 구성{#configuring-administrative-alerts}

관리 경고는 일반 작업 과정 중에 Insight Server에서 오류가 감지되면 지정된 이메일 주소로 이메일 알림을 보냅니다.

**권장 빈도:** 프로덕션 전

>[!NOTE]
>
>관리 경고를 사용하려면 [!DNL Insight Server]이(가) 전자 메일로 경고를 보내기 위한 전달 SMTP 서버에 액세스할 수 있어야 합니다.

전자 메일 알림의 수신자는 주요 시스템 관리 담당자 및 주요 이해 당사자입니다.

관리 경고 파일 [!DNL Administrative Alerts.cfg]은 [!DNL Insight Server]에 대한 관리 경고를 구성하는 데 사용됩니다.

>[!NOTE]
>
>클러스터를 실행 중인 경우 클러스터의 마스터 [!DNL Insight Server]에 대한 경고를 만들거나 수정해야 합니다.

**관리 경고를 생성하거나 수정하려면**

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 Servers Manager 작업 영역을 엽니다.
1. 구성할 [!DNL Insight Server] 아이콘을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Server Files]** 를 클릭합니다.
1. [!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 해당 콘텐츠를 봅니다. [!DNL Administrative Alerts.cfg] 파일이 이 디렉터리 내에 있습니다.
1. [!DNL Administrative Alerts.cfg]에 대한 *서버 이름 *열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다. [!DNL Administrative Alerts.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.
1. [!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]** 를 클릭합니다.
1. [!DNL Administrative Alerts.cfg] 창에서 **[!UICONTROL component]** 을 클릭하여 해당 콘텐츠를 봅니다.
1. 원하는 대로 매개 변수를 채웁니다. 이 파일에서 사용할 수 있는 매개 변수 목록은 [관리 경고 구성 설정](../../../home/c-inst-svr/c-cfg-stgs-ref/c-admin-alts-cfg-stgs.md#concept-14c3c3ed797f47c5900ec04cae2fc491)을 참조하십시오.

   ![단계 정보](assets/cfg_adminalerts_examplevalues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. [!DNL Server Files Manager]에서 [!DNL Temp] 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 선택합니다.

1. (선택 사항) 클러스터에서 작업 중이고 각 데이터 처리 단위에 동일한 관리 경고가 적용되도록 하려면 업데이트된 [!DNL Administrative Alerts.cfg] 파일을 마스터 [!DNL Insight Server] 설치 디렉토리 내의 [!DNL Components for Processing Servers] 폴더에 복사하여 붙여넣어야 합니다.
