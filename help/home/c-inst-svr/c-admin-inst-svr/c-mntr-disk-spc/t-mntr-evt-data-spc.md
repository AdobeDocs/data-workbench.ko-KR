---
description: 이벤트 데이터 공간 모니터링 및 센서 데이터의 로그 디렉토리 변경에 대한 정보입니다.
title: 이벤트 데이터 공간 모니터링
uuid: e514e8fb-e735-4003-ab21-17470c73af37
exl-id: 1016d00f-e0a0-47f1-a600-528c4811fcf6
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 1%

---

# 이벤트 데이터 공간 모니터링{#monitoring-event-data-space}

{{eol}}

이벤트 데이터 공간 모니터링 및 센서 데이터의 로그 디렉토리 변경에 대한 정보입니다.

**권장 빈도:** 5-10분마다

[!DNL Insight Server] 당 하나의 로그 파일 저장 [!DNL Sensor] 구성에 따라 하루에 데이터 처리 단위 또는 파일 서버 단위로 설정합니다. 로그 파일의 크기와 로그 파일에 필요한 데이터 저장소 공간의 양은 기록되는 웹 사이트 수와 웹 서버가 초당 받는 요청 수를 포함하여 많은 변수에 따라 다릅니다.

일반적인 [!DNL Insight Server] (또는 [!DNL Insight Server] 클러스터)에서는 구현에서 Adobe에서 권장하는 하드웨어를 사용한다고 가정할 때, 여러 테라바이트의 데이터를 저장할 수 있습니다 [!DNL Insight Server] 시스템

일반적으로 모든 로그 데이터는 [!DNL Insight Server] 시스템. 시스템에서 더 많은 데이터 저장 공간을 사용할 수 있도록 해야 하는 경우, 가장 최근의 로그 파일을 제외한 모든 파일을 다른 컴퓨터 또는 데이터 저장 매체(zip 드라이브, 테이프 등)로 이동할 수 있습니다. 데이터 이동을 중지하지 않아도 됩니다 [!DNL Insight Server], 및에서 사용할 수 있는 기능에는 영향을 주지 않습니다 [!DNL Insights] 에 연결되어 있을 수 있습니다. [!DNL Insight Server] 지속적인 데이터를 사용하여 작업할 수 있습니다. 분석 데이터 세트를 처리하거나 재처리하지 않는 경우 모든 이전 데이터에 대한 액세스 권한을 유지하고 새 데이터는에서 계속 사용할 수 있습니다. [!DNL Insight]. 분석 데이터 세트를 처리하거나 재처리하는 경우 처리가 완료될 때까지 데이터에 액세스할 수 없습니다.

기본적으로 [!DNL Sensor] 및 [!DNL Insight Server] 에 저장됩니다. [!DNL Logs] 폴더 내 [!DNL Insight Server] 설치 디렉토리. 통신 구성 파일, [!DNL Communications.cfg]를 지정하는 경우, 읽은 이벤트 데이터 로그 파일의 위치를 지정합니다 [!DNL Insight Server].

**로그 디렉토리 변경 [!DNL Sensor] 데이터**

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.
1. 아이콘을 마우스 오른쪽 단추로 클릭합니다. [!DNL Insight Server] 을(를) 구성하고 **[!UICONTROL Server Files]**.
1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Components]** 콘텐츠를 보려면 클릭하십시오. 다음 [!DNL Communications.cfg] 파일이 이 디렉터리 내에 있습니다.
1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 [!DNL Communications.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL Communications.cfg].
1. 에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. 에서 [!DNL Communications.cfg] 창 **[!UICONTROL component]** 콘텐츠를 보려면 클릭하십시오.
1. 에서 [!DNL Communications.cfg] 창 **[!UICONTROL Servers]** 콘텐츠를 보려면 클릭하십시오. 다음과 같은 여러 유형의 서버가 나타날 수 있습니다. 파일 서버, 로깅 서버, 초기화 서버, 상태 서버, 전송 서버 또는 복제 서버
1. LoggingServer를 찾습니다. [!DNL Sensor] 로그 파일을에서 처리할 수 있습니다. [!DNL Insight Server]를 클릭하고 해당 번호를 클릭하여 메뉴를 표시합니다.

   ![단계 정보](assets/cfg_communications_examplevalues_logging.png)

   기본 로그 디렉토리는 다음과 같습니다. [!DNL Logs] 폴더 내 [!DNL Insight Server] 설치 디렉토리.

1. 로그 디렉토리 매개 변수를 편집하여 로그 파일의 원하는 위치를 반영합니다.

   >[!NOTE]
   >
   >LoggingServer에 대한 다른 매개 변수는 수정하지 마십시오.

   ![](assets/cfg_communicates_logslocalpath_egvalues.png)

   여러 FileServer가 Servers 노드 아래에 나열될 수 있으므로, 여러 FileServer의 내용을 확인해야 할 수 있습니다. [!DNL Servers] 목록) 수정할 로컬 로그 경로가 있는 서버를 찾습니다.

1. 로컬 경로를 편집하여 [!DNL .vsl] 파일.

   >[!NOTE]
   >
   >FileServer에 대한 다른 매개 변수는 수정하지 마십시오.

   로그 파일의 위치가 [!DNL Communications.cfg] 파일을 만들면 이러한 파일을 [!DNL Server Files Manager] /Logs/ 를 FileServer의 URI로 지정하여

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 선택 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
