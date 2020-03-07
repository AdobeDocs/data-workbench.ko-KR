---
description: Insight Server 파일 서버 단위 및 파일 서버 구성 프로세스에 대한 정보입니다.
solution: Analytics
title: 데이터 워크벤치 서버 파일 서버 단위 구성
topic: Data workbench
uuid: ccb65952-f017-4434-b2f8-74c274450834
translation-type: tm+mt
source-git-commit: 72761a57e4bb9f230581b2cd37bff04ba7be8e37

---


# 데이터 워크벤치 서버 파일 서버 단위 구성{#configuring-a-data-workbench-server-file-server-unit}

Insight Server 파일 서버 단위 및 파일 서버 구성 프로세스에 대한 정보입니다.

<!--
c_abt_file_svr_units.xml
-->

파일의 **[!UICONTROL Log Sources]** > **[!UICONTROL Log Server]** 노드에서 매개 변수를 완료하여 데이터 워크벤치 서버(InsightServer64.exe)를 FSU(파일 서버 장치)로 실행하도록 구성할 수 [!DNL Log Processing.cfg] 있습니다. 데이터 워크벤치 서버가 FSU로 실행되도록 구성되면 여러 처리 서버(DPU)에서 빠르게 액세스할 수 있는 소스 파일( [!DNL .vsl] 파일, 텍스트 파일 또는 XML 파일)이 저장됩니다. 데이터 워크벤치 서버 클러스터의 DPU가 로그 파일을 읽기 위해 FSU에 액세스하면 로그 파일을 해당 파일로 나누어 동일한 파일이 두 번 이상 처리되지 않도록 합니다.

>[!NOTE]
>
>5-10DPU로 구성된 데이터 워크벤치 서버 클러스터를 제공하는 FSU를 설정할 때 클러스터의 마스터 서버를 FSU로 만들어야 합니다.

데이터 워크벤치 서버 클러스터 설치에 대한 자세한 내용은 서버 *제품 설치 및 관리 안내서를 참조하십시오*.

<!--
c_file_svr_config_proc.xml
-->

위치가 원격 위치인 경우 데이터를 처리하는 데이터 워크벤치 서버 시스템은 지정된 원격 시스템에 연결하여 로그를 읽습니다.

FSU로 실행되도록 지정된 데이터 워크벤치 서버 시스템에서 DPU가 FSU에 연결되도록 [!DNL Access Control.cfg] 파일을 사용하고 [!DNL Communications.cfg] 파일이 원격 데이터 파일의 위치를 매핑합니다. FSU를 구성하는 프로세스 단계는 다음과 같습니다.

1. 마스터 데이터 워크벤치 서버의 [!DNL Log Processing.cfg] 파일에서 데이터 소스 유형과 소스 위치를 지정합니다. 데이터 [소스 지정을 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-d2b545db7ab142ffb4be32e040395383).

1. FSU의 [!DNL Access Control.cfg] 파일에서 DPU가 FSU에 연결하여 로그 데이터를 읽을 수 있도록 권한을 편집합니다. 파일 [서버 단위의 권한 편집을 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-b4a54b591b4e4435a728a67f194057ef).

1. FSU의 [!DNL Communications.cfg] 파일에서 로그 파일의 위치를 지정할 [!DNL LoggingServer] 수 있도록 및 [!DNL FileServer] 항목의 설정을 편집합니다. 로그 [파일의 위치 지정을 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-f9a649bf1b2544feb10ad8820384edb0).

1. 데이터 워크벤치 서버 클러스터에서 실행되도록 데이터 집합 프로필을 구성하는 경우 클러스터의 FSU를 모든 프로필의 차원이 구성되는 서버로 만들어야 합니다.(데이터 워크벤치 서버 클러스터만 해당) FSU의 [!DNL Communications.cfg] 및 [!DNL cluster.cfg] 파일에서 &quot;정규화 서버&quot;에 대한 항목을 추가하여 모든 차원이 구성되는 클러스터 내의 서버를 FSU로 만듭니다. 클러스터의 [중앙 표준화 서버 만들기를 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-2c1f57b683f94cc193bc069e886bba28).

데이터 워크벤치 서버 클러스터에서 처리할 데이터 집합 프로필을 구성하는 방법은 서버 제품 설치 *및 관리 안내서를 참조하십시오*.

>[!NOTE]
>
>다음 지침은 모든 로그 파일이 기본 디렉토리에 있다고 가정합니다. 다른 디렉토리에 로그를 저장하거나 여러 로그 경로를 만들려면 Adobe 컨설팅 서비스에 문의하여 특정 구성에 대해 논의하십시오.

## 데이터 소스 지정 {#section-d2b545db7ab142ffb4be32e040395383}

데이터 세트에 대한 원격 데이터 소스를 지정할 때는 데이터 소스 유형과 마스터 데이터 워크벤치 서버에서 로그 파일의 위치를 지정해야 합니다.

**데이터 소스 및 해당 위치를 지정하려면**

1. Open the [!DNL Log Processing.cfg] file. 로그 [처리 구성 파일 편집을 참조하십시오](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5).

1. 로그 파일 [!DNL Sensor]또는 XML 데이터 소스를 추가합니다. See [Log Files](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e).

1. 로그 경로 매개 변수를 완료합니다. 센서 [파일](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009), [로그 파일](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e)또는 [XML 로그 소스를](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887)참조하십시오. 올바른 URI를 지정해야 합니다.

1. 다음 표에 정의된 로그 서버 매개 변수를 완료합니다.

<table id="table_5881B8DEFF984BC7A620CEEA3A637912"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">  이름  </td> 
   <td colname="col2"> 원격 파일 서버를 식별하는 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 서버 일반 이름 </td> 
   <td colname="col2"> <p> <span class="wintitle"> 파일</span> 서버의 SSL 인증서에 나열된 서버 일반 이름입니다. </p> <p> 이 매개 변수는 SSL 사용이 <span class="wintitle"> false로</span> 설정된 경우 선택 사항입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주소 </td> 
   <td colname="col2"> <p>파일 서버 컴퓨터의 주소입니다. 이름이 SSL 서버 공통 이름과 <span class="wintitle"> 일치하는</span> 경우 <span class="wintitle"> 비워 둘 수 있습니다</span>. </p> <p> 예:visual.mycompany.com <span class="filepath"></span> 또는 192.168.1.90. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 포트 </td> 
   <td colname="col2"> 데이터 워크벤치 서버 컴퓨터가 파일 서버와 통신하는 포트입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 클라이언트 인증서 </td> 
   <td colname="col2"> 데이터 워크벤치 서버에 대한 <span class="wintitle"> SSL 인증서</span> 파일의 이름입니다(<span class="filepath"> server_cert.pem</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 사용 </td> 
   <td colname="col2"> 참 또는 거짓 True는 파일 서버가 SSL을 사용함을 <span class="wintitle"> 나타냅니다</span>. </td> 
  </tr> 
 </tbody> 
</table>

DPU가 FSU에 연결하려면 프록시 서버가 필요한 경우 다음 매개 변수를 완료해야 합니다.

| 매개 변수 | 설명 |
|---|---|
| 프록시 주소 | 데이터 워크벤치 서버가 파일 서버에 액세스하는 데 사용해야 하는 프록시 서버의 주소입니다. |
| 프록시 암호 | 선택 사항입니다. 프록시 서버의 암호입니다. |
| 프록시 포트 | 프록시 서버의 포트입니다. 기본값은 8080입니다. |
| 프록시 사용자 이름 | 선택 사항입니다. 프록시 서버의 사용자 이름입니다. |

다음은 [!DNL Log Server] [!DNL Log Processing.cfg] 파일에 정의된 예시입니다. 로그 소스 #1은 FSU01이라는 컴퓨터의 Logs(로그 경로 매개 변수에 지정된 URI를 참고)라는 디렉토리를 가리키는 LogFile 소스입니다.

![](assets/cfg_LogProcessing_LogServer.png)

## 파일 서버 단위의 권한 편집 {#section-b4a54b591b4e4435a728a67f194057ef}

이전 프로세스에서는 지정된 데이터 세트에 대한 프로파일을 FSU에서 로그 파일을 읽도록 구성했습니다. 이제 프로필을 실행 중인 DPU에서 연결을 허용하려면 FSU에 대한 권한을 편집해야 합니다. 다음 단계에서는 권한 파일 편집을 안내합니다 [!DNL Access Control.cfg].

**FSU에 대한 권한을 편집하려면**

1. FSU로 [!DNL Server Files Manager] 설정할 데이터 워크벤치 서버 시스템의 내용을 열고 을 클릭하여 **[!UICONTROL Access Control]** 표시합니다.

   데이터 워크벤치 사용자 안내서를 [!DNL Server Files Manager]참조하여 데이터 워크벤치를 *엽니다*.

1. 창에서 [!DNL Server Files Manager] 아이콘을 클릭하여 내용을 **[!UICONTROL Access Control]** 표시합니다. 이 [!DNL Access Control.cfg] 파일은 이 디렉토리 내에 있습니다.

1. 에 대한 서버 이름 열에서 확인 표시를 마우스 오른쪽 단추로 [!DNL Access Control.cfg]클릭한 다음 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다 [!DNL Access Control.cfg].

1. 열 아래에 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Workstation]**&#x200B;을 클릭합니다.

1. 창에서 [!DNL Access Control] 아이콘을 클릭하여 내용을 **[!UICONTROL Access Control Groups]** 표시합니다.

1. 목록에서 최종 [!DNL AccessGroup] 목록의 숫자 레이블을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Group]**&#x200B;을 클릭합니다.

1. 새 [!DNL Name] 항목에 대해 a를 입력합니다 [!DNL AccessGroup]. 예:서버 연결.

1. 새 항목 **[!UICONTROL Member]** 아래에서 마우스 오른쪽 단추를 [!DNL AccessGroup]클릭한 다음 **[!UICONTROL Add new]** > **[!UICONTROL Member]**&#x200B;를 클릭합니다.

1. 이 파일 서버에 연결하는 데이터 워크벤치 서버의 DPU의 IP 주소를 입력합니다.
1. 로그 파일에 액세스해야 하는 클러스터의 데이터 워크벤치 서버 DPU를 비롯하여 이 FSU에 연결되는 다른 데이터 워크벤치 서버 DPU에 대해 4 및 5단계를 반복합니다.
1. 새 항목 **[!UICONTROL Read-Only Access]** 아래에서 마우스 오른쪽 단추를 [!DNL AccessGroup]클릭한 다음 **[!UICONTROL Add new]** > **[!UICONTROL URI]**&#x200B;를 클릭합니다.

1. 파일 서버 시스템에 저장된 로그 파일의 위치를 입력합니다. 경로 사양에 슬래시(/)를 사용합니다. 기본 위치는 /Logs/입니다.
1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 단추를 클릭한 다음 을 클릭합니다 **[!UICONTROL Save]**.

1. 창에서 [!DNL Server Files Manager] 열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Access Control.cfg] >을 클릭하여 [!DNL Temp] **[!UICONTROL Save to]** **[!UICONTROL server name]** 로컬에서 변경한 데이터 워크벤치 서버의 FSU를 저장합니다.

## 로그 파일의 위치 지정 {#section-f9a649bf1b2544feb10ad8820384edb0}

로그 파일의 위치를 지정하려면 FSU에서 [!DNL Communications.cfg] 파일을 편집해야 합니다.

**로그 파일의 위치를 지정하려면**

1. 창에서 [!DNL Server Files Manager] 아이콘을 클릭하여 내용을 **[!UICONTROL Components]** 표시합니다. 이 [!DNL Communications.cfg] 파일은 이 디렉토리 내에 있습니다.

1. 에 대한 서버 이름 열에서 확인 표시를 마우스 오른쪽 단추로 [!DNL Communications.cfg]클릭한 다음 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다 [!DNL Communications.cfg].

1. 열 아래에 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Workstation.]**&#x200B;을 클릭합니다.

1. 창에서 [!DNL Communications.cfg] 아이콘을 클릭하여 내용을 **[!UICONTROL component]** 표시합니다.

1. 창에서 [!DNL Communications.cfg] 아이콘을 클릭하여 내용을 **[!UICONTROL Servers]** 표시합니다. 여러 서버가 나타날 수 있습니다.파일 서버, 로깅 서버, 초기화 서버, 상태 서버, 전송 서버 또는 복제 서버.

1. (로그 [!DNL Sensor] 소스에만 해당) 데이터 워크벤치 서버에서 처리할 로그 파일을 쓰는 [!DNL LoggingServer][!DNL Sensor] 위치를 찾은 다음 해당 번호를 클릭하여 메뉴를 표시합니다. 로그 디렉토리 매개 변수를 편집하여 원하는 로그 파일의 위치를 반영합니다. 기본 로그 디렉토리는 데이터 워크벤치 서버의 설치 디렉토리 내의 로그 폴더입니다.

   에 대한 다른 매개 변수는 수정하지 마십시오 [!DNL LoggingServer].

   ![](assets/cfg_Communications_LoggingServer.png)

1. 로그 파일의 위치를 지정하는 FileServer를 찾습니다. 서버 아래에 여러 개의 파일 서버가 있을 수 있으므로 원하는 서버를 찾으려면 서버 번호를 클릭하여 여러 파일의 컨텐츠를 확인해야 합니다.
1. 로그 파일의 위치를 반영하도록 FileServer의 [!DNL Local Path] 및 URI 매개 변수를 편집합니다. 다음 예는 로그 파일이 데이터 워크벤치 서버의 설치 디렉토리 내의 로그 폴더에 있는 것을 보여줍니다.

   ![](assets/cfg_Communications_FS.png)

   >[!NOTE]
   >
   >표시된 대로 [!DNL Local Path] 및 URI 매개 변수를 채우는 경우 데이터 워크벤치 서버에서 을 클릭하여 FSU의 로그 파일에 액세스할 [!DNL Logs] 수 [!DNL Server Files Manager]있습니다.

1. 구성 창 **[!UICONTROL (modified)]** 맨 위에서 마우스 오른쪽 버튼을 클릭한 다음 을 클릭합니다 **[!UICONTROL Save]**.

1. 창에서 [!DNL Server Files Manager] 열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Communications.cfg] > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *을 클릭하여 로컬에서 변경한 데이터 워크벤치 서버의 FSU를 저장합니다&#x200B;**[!UICONTROL server name]*** .

## 클러스터의 중앙 표준화 서버 만들기 {#section-2c1f57b683f94cc193bc069e886bba28}

데이터 워크벤치 서버 클러스터에서 실행되도록 데이터 집합 프로필을 구성하는 경우 클러스터의 FSU를 모든 프로필의 차원이 구성되는 서버로 만들어야 합니다.

클러스터의 FSU가 클러스터의 마스터 서버 및 중앙 표준화 서버로 사용되는 것이 좋습니다.

FSU를 중앙 표준화 서버로 만들려면 FSU에서 [!DNL Communications.cfg] 및 [!DNL Cluster.cfg] 파일을 열고 편집해야 합니다.

**FSU를 중앙 집중식 표준화 서버로 만들려면**

1. FSU의 파일에 [!DNL NormalizeServer] 항목을 [!DNL Communications.cfg] 추가합니다.

   >[!NOTE]
   >
   >데이터 워크벤치 서버 v5.0 이상용 전체 릴리스 패키지를 설치한 경우 FSU의 [!DNL Communications.cfg] 파일에 이미 [!DNL NormalizeServer] 항목이 있어야 합니다. 아래 절차에 따라 항목이 있는지 확인할 수 있습니다.

   1. 로그 파일의 위치 지정에 설명된 대로 데이터 [!DNL Communications.cfg] 워크벤치에서 [파일을 엽니다](#section-f9a649bf1b2544feb10ad8820384edb0).

   1. 아이콘을 **[!UICONTROL component]** 클릭하여 컨텐츠를 표시합니다.
   1. 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL Servers]** > **[!UICONTROL Add New]** **[!UICONTROL Centralized Normalization Server]**&#x200B;를 클릭합니다.

   1. 의 URI 매개 변수에 [!DNL NormalizeServer]을 입력합니다 [!DNL /Cluster/].

      ![](assets/cfg_Communications_NormalizeServer.png)

   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Save]**&#x200B;클릭합니다.

   1. 창에서 [!DNL Server Files Manager] 열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Communications.cfg] > [!DNL Temp] &lt; **[!UICONTROL Save to]** > ***[!UICONTROL server]*** 이름을 클릭하여 로컬에서 변경한 데이터 워크벤치 서버 FSU를 저장합니다.

1. 데이터 워크벤치 서버 클러스터의 마스터 서버에 있는 [!DNL Cluster.cfg] 파일에서 중앙 표준화 서버를 정의합니다.

   >[!NOTE]
   >
   >중앙 표준화 서버를 설정하는 FSU가 클러스터의 마스터 데이터 워크벤치 서버가 아닌 경우 클러스터의 DPU의 IP 주소를 FSU [!DNL Cluster Servers] [!DNL Access Control.cfg] 파일의 액세스 그룹에 추가해야 합니다. 그룹에 서버를 추가하는 방법에 대한 지침은 서버 제품 설치 및 관리 안내서의 클러스터에 대한 액세스 제어 [!DNL Cluster Servers] *파일 업데이트를 참조하십시오.*

   1. 데이터 세트 프로필 [!DNL Profile Manager] 내에서 해당 콘텐츠를 **[!UICONTROL Dataset]** 표시하려면 을(를) 클릭합니다. 이 [!DNL Cluster.cfg] 파일은 이 디렉토리 내에 있습니다.

   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭한 [!DNL Cluster.cfg]다음 을 클릭합니다 **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**&#x200B;를 클릭합니다.

   1. 다음 파일 조각에서 강조 표시된 텍스트를 추가합니다.

      [!DNL Cluster = ClusterConfig:]

      [!DNL Normalize Server = serverInfo:]

      [!DNL Address = string:]

      [!DNL Port = int: 80]

      [!DNL SSL Server Common Name = string: server common name]

      [!DNL Use SSL = bool: false]

      >[!NOTE]
      >
      >SSL 서버 공통 이름 매개 변수에 FSU의 공통 이름을 입력하면 FSU는 해당 [!DNL .address] 파일을 사용하여 일반 이름을 확인합니다. 파일에 대한 자세한 내용은 [!DNL .address] 서버 제품 *설치 및 관리 가이드를 참조하십시오*.

   1. 파일을 저장합니다.
   1. 에서 [!DNL Profile Manager]열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Cluster.cfg] >을 클릭하여 [!DNL User] **[!UICONTROL Save to]** ***[!UICONTROL dataset profile name]*** 로컬에서 변경한 데이터 세트 프로필을 저장합니다.
