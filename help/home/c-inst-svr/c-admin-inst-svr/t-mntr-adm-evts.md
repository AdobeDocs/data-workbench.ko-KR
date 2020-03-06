---
description: 정기적으로 이벤트 로그 파일을 모니터링하여 Insight Server 설치 디렉토리 내의 Events 폴더에 기본적으로 있는 <YYYYYYYMMDD>-event.txt 파일에 기록된 Insight Server 시스템 이벤트 메시지를 추적해야 합니다.
solution: Insight
title: 관리 이벤트 모니터링
uuid: 92d71478-0857-4af8-909c-0cf800b081f4
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 관리 이벤트 모니터링{#monitoring-administrative-events}

정기적으로 이벤트 로그 파일을 모니터링하여 Insight Server 설치 디렉토리 내의 Events 폴더에서 기본적으로 `<YYYYMMDD>-event.txt` 파일에 기록된 Insight Server 시스템 이벤트 메시지를 추적해야 합니다.

**권장 빈도:** 5-10분마다

인, 자동 관리 도구, [!DNL Server Files Manager] 파일 또는 Windows 이벤트 뷰어를 사용하여 이러한 이벤트를 모니터링할 [!DNL Insight][!DNL *-event.txt] 수 있습니다.

>[!NOTE]
>
>관리 이벤트 로그는 Windows 이벤트 로그와 완전히 별개인 반면 일부 동일한 이벤트를 포함합니다. 관리 이벤트 로그에는 [!DNL Insight Server] 이벤트에 대한 정보만 포함됩니다.

**events.txt 파일을[!DNL Server Files Manager]**

1. > [!DNL Insight]탭에서 [!DNL Admin] [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 활성 상태의 아이콘을 마우스 오른쪽 단추로 [!DNL Insight Server] 클릭하고 **[!UICONTROL Server Files]**&#x200B;클릭합니다.
1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Events]** 봅니다.
1. 원하는 파일 옆의 *서버 이름* 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 열의 파일 이름 옆에 확인 표시가 [!DNL Temp] 나타납니다.
1. 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Notepad]**&#x200B;을 클릭합니다. 새 Microsoft Windows 메모장 창에 이벤트 파일이 나타납니다.

   ![단계 정보](assets/vis_FileManager_eventfile.png)

   설치 디렉토리 내의 [!DNL Server.log] 폴더에 있는 [!DNL Trace] [!DNL Insight Server] 파일에는 보다 자세한 로깅 정보가 들어 있습니다.

**Windows 이벤트 뷰어를 통해 이벤트 보기**

* 클릭 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.

**관리 이벤트 로그 디렉토리를 변경하려면**

관리 이벤트 로그 구성 [!DNL Administrative Events Log.cfg]파일에서 이벤트 로깅이 출력되는 디렉토리를 지정합니다.

1. > [!DNL Insight]탭에서 [!DNL Admin] [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.

1. 구성할 아이콘 을 마우스 오른쪽 단추로 [!DNL Insight Server] 클릭하고 **[!UICONTROL Server Files]**&#x200B;클릭합니다.

1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Components]** 봅니다. 이 [!DNL Administrative Event Logs.cfg] 파일은 이 디렉토리 내에 있습니다.

1. 에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Administrative Event Logs.cfg] **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. 에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다 [!DNL Administrative Event Logs.cfg].

1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Insight]**&#x200B;을 클릭합니다.

1. 창에서 [!DNL Administrative Event Logs.cfg] 을 클릭하여 내용을 **[!UICONTROL component]** 봅니다. 기본 경로는 [!DNL Events] 설치 디렉토리 내의 [!DNL Insight Server] 폴더입니다.

   ![](assets/cfg_adminevents_examplevalues.png)

1. Path 매개 변수에서 이벤트 로깅 데이터를 출력할 디렉토리의 이름을 입력합니다.
1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
   1. 에서 [!DNL Server Files Manager]열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Save to]** **[!UICONTROL server name]**&#x200B;을 선택합니다.

