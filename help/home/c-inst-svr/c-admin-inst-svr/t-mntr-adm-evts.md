---
description: 정기적으로 이벤트 로그 파일을 모니터링하여 Insight Server 설치 디렉토리 내의 Events 폴더에 기본적으로 있는 <YYYYYMMDD>-event.txt 파일에 기록된 Insight Server 시스템 이벤트 메시지를 추적해야 합니다.
title: 관리 이벤트 모니터링
uuid: 92d71478-0857-4af8-909c-0cf800b081f4
exl-id: e468a7d0-ed09-4367-88ce-b68964511e76
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 2%

---

# 관리 이벤트 모니터링{#monitoring-administrative-events}

정기적으로 이벤트 로그 파일을 모니터링하여 Insight Server 설치 디렉토리 내의 Events 폴더에 기본적으로 있는 `<YYYYMMDD>-event.txt` 파일에 기록된 Insight Server 시스템 이벤트 메시지를 추적해야 합니다.

**권장 빈도:** 5-10분마다

[!DNL Insight]의 [!DNL Server Files Manager], 자동화된 관리 도구, [!DNL *-event.txt] 파일 또는 Windows 이벤트 뷰어를 사용하여 이러한 이벤트를 모니터링할 수 있습니다.

>[!NOTE]
>
>관리 이벤트 로그는 Windows 이벤트 로그와 완전히 별도이지만 일부 동일한 이벤트를 포함합니다. 관리 이벤트 로그에는 [!DNL Insight Server] 이벤트에 대한 정보만 포함됩니다.

**를 통해 events.txt 파일을 보려면[!DNL Server Files Manager]**

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 활성 [!DNL Insight Server]의 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]**&#x200B;을 클릭합니다.
1. [!DNL Server Files Manager]에서 **[!UICONTROL Events]**&#x200B;을 클릭하여 콘텐트를 봅니다.
1. 원하는 파일 옆에 있는 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;를 클릭합니다. [!DNL Temp] 열의 파일 이름 옆에 확인 표시가 나타납니다.
1. [!DNL Temp] 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**&#x200B;를 클릭합니다. 이벤트 파일이 새 Microsoft Windows 메모장 창에 표시됩니다.

   ![단계 정보](assets/vis_FileManager_eventfile.png)

   [!DNL Insight Server] 설치 디렉터리 내의 [!DNL Trace] 폴더에 있는 [!DNL Server.log] 파일에는 보다 자세한 로깅 정보가 들어 있습니다.

**Windows 이벤트 뷰어를 통해 이벤트 보기**

* 클릭 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.

**관리 이벤트 로그 디렉토리를 변경하려면**

관리 이벤트 로그 구성 파일 [!DNL Administrative Events Log.cfg]은 이벤트 로깅이 출력되는 디렉터리를 지정합니다.

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.

1. 구성할 [!DNL Insight Server] 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]** 을 클릭합니다.

1. [!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 콘텐트를 봅니다. [!DNL Administrative Event Logs.cfg] 파일이 이 디렉터리 내에 있습니다.

1. [!DNL Administrative Event Logs.cfg]에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. [!DNL Administrative Event Logs.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.

1. [!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**&#x200B;를 클릭합니다.

1. [!DNL Administrative Event Logs.cfg] 창에서 **[!UICONTROL component]**&#x200B;을 클릭하여 내용을 봅니다. 기본 경로는 [!DNL Insight Server] 설치 디렉토리 내의 [!DNL Events] 폴더입니다.

   ![](assets/cfg_adminevents_examplevalues.png)

1. Path 매개 변수에서 이벤트 로깅 데이터를 출력할 디렉토리 이름을 입력합니다.
1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.
   1. [!DNL Server Files Manager]에서 [!DNL Temp] 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > **[!UICONTROL server name]**&#x200B;를 선택합니다.
