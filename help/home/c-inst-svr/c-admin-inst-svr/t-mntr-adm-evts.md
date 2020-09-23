---
description: 정기적으로 이벤트 로그 파일을 모니터링하여 Insight Server 설치 디렉토리 내의 Events 폴더에 기본적으로 있는 <YYYYYYMMDD>-event.txt 파일에 기록된 Insight Server 시스템 이벤트 메시지를 추적해야 합니다.
solution: Analytics
title: 관리 이벤트 모니터링
uuid: 92d71478-0857-4af8-909c-0cf800b081f4
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 2%

---


# 관리 이벤트 모니터링{#monitoring-administrative-events}

정기적으로 이벤트 로그 파일을 모니터링하여 Insight Server 설치 디렉토리 내의 Events 폴더에서 기본적으로 `<YYYYMMDD>-event.txt` 위치한 파일에 기록된 Insight Server 시스템 이벤트 메시지를 추적해야 합니다.

**권장 빈도:** 5-10분마다

in, your automated management tool, the [!DNL Server Files Manager] [!DNL Insight][!DNL *-event.txt] files, or the Windows Event Viewer.

>[!NOTE]
>
>관리 이벤트 로그는 Windows 이벤트 로그와 완전히 별개인 반면 일부 동일한 이벤트를 포함합니다. 관리 이벤트 로그에는 [!DNL Insight Server] 이벤트에 대한 정보만 포함됩니다.

**events.txt 파일을[!DNL Server Files Manager]**

1. 서버 관리자 작업 영역 [!DNL Insight]을 열려면 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭합니다.
1. 활성 상태의 아이콘을 마우스 오른쪽 단추로 [!DNL Insight Server] 클릭하고 을 클릭합니다 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]을 클릭하여 콘텐츠 **[!UICONTROL Events]** 를 봅니다.
1. 원하는 파일 옆의 *서버 이름* 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Make Local]**. 열의 파일 이름 옆에 확인 표시가 [!DNL Temp] 나타납니다.
1. 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Notepad]**&#x200B;을 클릭합니다. 이벤트 파일이 새 Microsoft Windows 메모장 창에 나타납니다.

   ![단계 정보](assets/vis_FileManager_eventfile.png)

   설치 디렉토리 내의 [!DNL Server.log] 폴더에 있는 [!DNL Trace] [!DNL Insight Server] 파일에 보다 자세한 로깅 정보가 포함되어 있습니다.

**Windows 이벤트 뷰어를 통해 이벤트 보기**

* 클릭 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.

**관리 이벤트 로그 디렉토리를 변경하려면**

관리 이벤트 로그 구성 파일 [!DNL Administrative Events Log.cfg]은 이벤트 로깅이 출력되는 디렉토리를 지정합니다.

1. 서버 관리자 작업 영역 [!DNL Insight]을 열려면 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭합니다.

1. 구성할 아이콘 [!DNL Insight Server] 을 마우스 오른쪽 단추로 클릭하고 클릭합니다 **[!UICONTROL Server Files]**.

1. 에서 [!DNL Server Files Manager]을 클릭하여 콘텐츠 **[!UICONTROL Components]** 를 봅니다. 이 디렉터리 내에 [!DNL Administrative Event Logs.cfg] 파일이 있습니다.

1. 에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 [!DNL Administrative Event Logs.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 에 대한 열에 확인 표시가 [!DNL Temp] 나타납니다 [!DNL Administrative Event Logs.cfg].

1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** 를 **[!UICONTROL in Insight]**&#x200B;클릭합니다.

1. 창에서 [!DNL Administrative Event Logs.cfg] 을 클릭하여 내용 **[!UICONTROL component]** 을 봅니다. 기본 경로는 설치 디렉토리 [!DNL Events] 내의 [!DNL Insight Server] 폴더입니다.

   ![](assets/cfg_adminevents_examplevalues.png)

1. Path 매개 변수에서 이벤트 로깅 데이터를 출력할 디렉토리 이름을 입력합니다.
1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 위쪽 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
   1. 에서 열 [!DNL Server Files Manager]의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 > [!DNL Temp] 을 **[!UICONTROL Save to]** 선택합니다 **[!UICONTROL server name]**.

