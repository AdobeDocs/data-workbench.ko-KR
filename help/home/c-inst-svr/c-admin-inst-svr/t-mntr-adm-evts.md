---
description: 이벤트 로그 파일을 정기적으로 모니터링하여 <yyyymmdd>Insight Server 설치 디렉토리 내의 이벤트 폴더에 기본적으로 있는 -event.txt 파일입니다.
title: 관리 이벤트 모니터링(Insight Server)
uuid: 92d71478-0857-4af8-909c-0cf800b081f4
exl-id: e468a7d0-ed09-4367-88ce-b68964511e76
source-git-commit: 235b8816c7397ac1ab71df650a1d4c2d681b3b2d
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---

# 관리 이벤트 모니터링{#monitoring-administrative-events}

이벤트 로그 파일을 정기적으로 모니터링하여 `<YYYYMMDD>-event.txt` Insight Server 설치 디렉토리 내의 이벤트 폴더에 기본적으로 있는 파일입니다.

**권장 빈도:** 5-10분마다

를 사용하여 이러한 이벤트를 모니터링할 수 있습니다 [!DNL Server Files Manager] in [!DNL Insight], 자동화된 관리 툴, [!DNL *-event.txt] 파일 또는 Windows 이벤트 뷰어

>[!NOTE]
>
>관리 이벤트 로그는 Windows 이벤트 로그와 완전히 분리되지만 일부 동일한 이벤트를 포함합니다. 관리 이벤트 로그에는 [!DNL Insight Server] events.

**를 통해 events.txt 파일을 보려면[!DNL Server Files Manager]**

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.
1. 활성 아이콘을 마우스 오른쪽 단추로 클릭합니다. [!DNL Insight Server] 을(를) 클릭합니다. **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Events]** 콘텐츠를 보려면 클릭하십시오.
1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 원하는 파일 옆에 있는 열을 클릭하고 **[!UICONTROL Make Local]**. 에서 파일 이름 옆에 확인 표시가 나타납니다 [!DNL Temp] 열.
1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. 새 Microsoft Windows 메모장 창에 이벤트 파일이 나타납니다.

   ![단계 정보](assets/vis_FileManager_eventfile.png)

   다음 [!DNL Server.log] 파일의 [!DNL Trace] 폴더 내 [!DNL Insight Server] 설치 디렉터리에 더 자세한 로깅 정보가 포함되어 있습니다.

**Windows 이벤트 뷰어를 통해 이벤트 보기**

* 클릭 **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**.

**관리 이벤트 로그 디렉토리를 변경하려면**

관리 이벤트 로그 구성 파일, [!DNL Administrative Events Log.cfg]를 지정하는 경우 이벤트 로깅이 출력되는 디렉터리를 지정합니다.

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.

1. 아이콘을 마우스 오른쪽 단추로 클릭합니다. [!DNL Insight Server] 을(를) 구성하고 **[!UICONTROL Server Files]**.

1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Components]** 콘텐츠를 보려면 클릭하십시오. 다음 [!DNL Administrative Event Logs.cfg] 파일이 이 디렉터리 내에 있습니다.

1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 [!DNL Administrative Event Logs.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL Administrative Event Logs.cfg].

1. 에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. 에서 [!DNL Administrative Event Logs.cfg] 창 **[!UICONTROL component]** 콘텐츠를 보려면 클릭하십시오. 기본 경로는 입니다 [!DNL Events] 폴더 내 [!DNL Insight Server] 설치 디렉토리.

   ![](assets/cfg_adminevents_examplevalues.png)

1. Path 매개 변수에 이벤트 로깅 데이터를 출력할 디렉토리의 이름을 입력합니다.
1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.
   1. 에서 [!DNL Server Files Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 선택 **[!UICONTROL Save to]** > **[!UICONTROL server name]**.
