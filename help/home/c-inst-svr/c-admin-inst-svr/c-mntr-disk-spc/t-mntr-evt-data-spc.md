---
description: 이벤트 데이터 공간 모니터링 및 센서 데이터의 로그 디렉토리 변경에 대한 정보입니다.
solution: Insight
title: 이벤트 데이터 공간 모니터링
uuid: e514e8fb-e735-4003-ab21-17470c73af37
translation-type: tm+mt
source-git-commit: 25366087936dfa5e31c5921aac400535ec259f2e

---


# 이벤트 데이터 공간 모니터링{#monitoring-event-data-space}

이벤트 데이터 공간 모니터링 및 센서 데이터의 로그 디렉토리 변경에 대한 정보입니다.

**권장 빈도:** 5-10분마다

[!DNL Insight Server] 구성에 따라 하루에 한 개의 로그 파일을 데이터 처리 장치 또는 파일 서버 장치에 [!DNL Sensor] 저장합니다. 로그 파일의 크기와 이에 필요한 데이터 저장소 공간의 크기는 로깅되는 웹 사이트의 수와 초당 웹 서버에서 받는 요청 수를 포함하여 많은 변수에 따라 다릅니다.

일반적인 설치 [!DNL Insight Server] (또는 [!DNL Insight Server] 클러스터)는 여러 TB의 데이터를 저장할 수 있으며, 이는 구현이 [!DNL Insight Server] 컴퓨터에 대해 Adobe에서 권장하는 하드웨어를 사용한다고 가정할 때 발생합니다.

일반적으로 모든 로그 데이터는 [!DNL Insight Server] 컴퓨터에 남아 있습니다. 시스템에서 더 많은 데이터 저장 공간을 사용할 수 있게 하기 위해 필요한 경우 최신 로그 파일을 제외한 모든 파일을 다른 컴퓨터 또는 데이터 저장소 미디어(zip 드라이브, 테이프 등)로 이동할 수 있습니다. 데이터를 이동하더라도 중지하지 않아도 [!DNL Insight Server]되며, 지속적인 데이터에 연결되어 [!DNL Insights] 작업할 수 [!DNL Insight Server] 있는 기능에는 영향을 주지 않습니다. 분석 데이터 세트를 처리하거나 다시 처리하지 않으면 모든 이전 데이터에 대한 액세스 권한이 유지되며 새 데이터는 에서 계속 사용할 수 [!DNL Insight]있습니다. 분석 데이터 세트를 처리하거나 재처리하는 경우 처리가 완료될 때까지 데이터에 액세스할 수 없습니다.

기본적으로 에서 생성되어 전송한 이벤트 데이터는 [!DNL Sensor] 설치 디렉토리 [!DNL Insight Server] [!DNL Logs] [!DNL Insight Server] 내의 폴더에 저장됩니다. 통신 구성 파일은 [!DNL Communications.cfg]이벤트 데이터 로그 파일을 읽을 위치를 지정합니다. [!DNL Insight Server]

**데이터의 로그 디렉토리를 변경하려면[!DNL Sensor]다음을 수행합니다.**

1. &#x200B;> [!DNL Insight]탭에서 [!DNL Admin] [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.
1. 구성할 아이콘 을 마우스 오른쪽 단추로 [!DNL Insight Server] 클릭하고 **[!UICONTROL Server Files]**&#x200B;클릭합니다.
1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Components]** 봅니다. 이 [!DNL Communications.cfg] 파일은 이 디렉토리 내에 있습니다.
1. 에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Communications.cfg] **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. 에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다 [!DNL Communications.cfg].
1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Insight]**&#x200B;을 클릭합니다.
1. 창에서 [!DNL Communications.cfg] 을 클릭하여 내용을 **[!UICONTROL component]** 봅니다.
1. 창에서 [!DNL Communications.cfg] 을 클릭하여 내용을 **[!UICONTROL Servers]** 봅니다. 여러 유형의 서버가 나타날 수 있습니다.파일 서버, 로깅 서버, 초기화 서버, 상태 서버, 전송 서버 또는 복제 서버.
1. 로그 파일을 [!DNL Sensor] 쓰는 LoggingServer를 [!DNL Insight Server]찾아 해당 번호를 클릭하여 메뉴를 표시합니다.

   ![단계 정보](assets/cfg_communications_examplevalues_logging.png)

   기본 로그 디렉토리는 [!DNL Logs] 설치 디렉토리 내의 [!DNL Insight Server] 폴더입니다.

1. 로그 디렉토리 매개 변수를 편집하여 원하는 로그 파일의 위치를 반영합니다.

   >[!NOTE]
   >
   >LoggingServer에 대한 다른 매개 변수는 수정하지 마십시오.

   ![](assets/cfg_communicates_logslocalpath_egvalues.png)

   Servers 노드 아래에 여러 FileServer가 나열될 수 있으므로, 수정할 로컬 로그 경로가 있는 서버를 찾기 위해( [!DNL Servers] 목록에서 해당 번호를 클릭하여) 많은 파일의 컨텐츠를 확인해야 합니다.

1. 로컬 경로를 편집하여 [!DNL .vsl] 파일의 원하는 위치를 반영합니다.

   >[!NOTE]
   >
   >FileServer에 대한 다른 매개 변수는 수정하지 마십시오.

   로그 파일의 위치가 파일에서 변경되었지만 이러한 파일은 FileServer의 URI로 /Logs/를 지정하여 [!DNL Communications.cfg] [!DNL Server Files Manager] 의 Logs 디렉토리에 매핑할 수 있습니다.

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager]열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *를 선택합니다&#x200B;**[!UICONTROL server name]***.

