---
description: Insight Server 파일 서버 유닛 및 파일 서버 구성 프로세스에 대한 정보입니다.
title: Data Workbench 서버 파일 서버 유닛 구성
uuid: ccb65952-f017-4434-b2f8-74c274450834
exl-id: 19b8c08a-e9f2-47ab-ad9f-1fddfbd9d249
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1784'
ht-degree: 1%

---

# Data Workbench 서버 파일 서버 유닛 구성{#configuring-a-data-workbench-server-file-server-unit}

{{eol}}

Insight Server 파일 서버 유닛 및 파일 서버 구성 프로세스에 대한 정보입니다.

<!--
c_abt_file_svr_units.xml
-->

에서 매개 변수를 완료하여 FSU(파일 서버 유닛)로 실행되도록 Data Workbench 서버(InsightServer64.exe)를 구성할 수 있습니다 **[!UICONTROL Log Sources]** > **[!UICONTROL Log Server]** 노드 [!DNL Log Processing.cfg] 파일. Data Workbench 서버가 FSU로 실행되도록 구성되면 소스 파일( [!DNL .vsl] 여러 DPU(처리 서버)에서 빠르게 액세스할 수 있는 파일, 텍스트 파일 또는 XML 파일 Data Workbench 서버 클러스터의 DPU가 FSU에 액세스하여 로그 파일을 읽으면 로그 파일을 구분하여 동일한 파일이 두 번 이상 처리되지 않도록 합니다.

>[!NOTE]
>
>5~10개의 DPU로 구성된 Data Workbench 서버 클러스터를 제공하는 FSU를 설정할 때 클러스터의 마스터 서버를 FSU로 만들어야 합니다.

Data Workbench 서버 클러스터 설치에 대한 자세한 내용은 *서버 제품 설치 및 관리 안내서*.

<!--
c_file_svr_config_proc.xml
-->

위치가 원격 위치인 경우 데이터를 처리하는 Data Workbench 서버 시스템은 지정된 원격 시스템에 연결하여 로그를 읽습니다.

FSU로 실행되도록 지정된 Data Workbench 서버 시스템에서 [!DNL Access Control.cfg] 파일을 사용하면 DPU가 FSU와 [!DNL Communications.cfg] 파일은 원격 데이터 파일의 위치를 매핑합니다. FSU를 구성하는 프로세스 단계는 다음과 같습니다.

1. 에서 [!DNL Log Processing.cfg] 마스터 data workbench 서버에 있는 파일에서 데이터 소스의 유형과 소스의 위치를 지정합니다. 자세한 내용은 [데이터 소스 지정](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-d2b545db7ab142ffb4be32e040395383).

1. 에서 [!DNL Access Control.cfg] FSU의 파일에서 DPU가 FSU에 연결하여 로그 데이터를 읽을 수 있도록 권한을 편집합니다. 자세한 내용은 [파일 서버 단위의 권한 편집](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-b4a54b591b4e4435a728a67f194057ef).

1. 에서 [!DNL Communications.cfg] 파일에서 [!DNL LoggingServer] 및 [!DNL FileServer] 로그 파일의 위치를 지정하는 항목입니다. 자세한 내용은 [로그 파일의 위치 지정](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-f9a649bf1b2544feb10ad8820384edb0).

1. Data Workbench 서버 클러스터에서 실행되도록 데이터 세트 프로필을 구성하는 경우 클러스터의 FSU도 모든 프로필의 차원이 구성된 서버로 만들어야 합니다. (Data Workbench 서버 클러스터만 해당) [!DNL Communications.cfg] 및 [!DNL cluster.cfg] FSU의 파일에서는 &quot;정규화 서버&quot;에 대한 항목을 추가하여 모든 차원이 구성된 클러스터 내에서 FSU를 서버로 만듭니다. 자세한 내용은 [클러스터의 중앙 표준화 서버 생성](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#section-2c1f57b683f94cc193bc069e886bba28).

Data Workbench 서버 클러스터에서 처리할 데이터 집합 프로필을 구성하는 방법은 다음을 참조하십시오. *서버 제품 설치 및 관리 안내서*.

>[!NOTE]
>
>다음 지침은 모든 로그 파일이 기본 디렉토리에 있다고 가정합니다. 다른 디렉토리에 로그를 저장하거나 여러 로그 경로를 만들려면 Adobe 컨설팅 서비스에 문의하여 특정 구성에 대해 알아보십시오.

## 데이터 소스 지정 {#section-d2b545db7ab142ffb4be32e040395383}

데이터 집합에 대한 원격 데이터 소스를 지정할 때 마스터 Data Workbench 서버에서 데이터 소스 유형과 로그 파일의 위치를 지정해야 합니다.

**데이터 소스 및 해당 위치를 지정하려면**

1. 를 엽니다. [!DNL Log Processing.cfg] 파일. 자세한 내용은 [로그 처리 구성 파일 편집](../../../home/c-dataset-const-proc/c-log-proc-config-file/t-edit-log-proc-config-file.md#task-6a2fa1b735cb4eefad730f0a3a7858e5).

1. 추가 [!DNL Sensor], 로그 파일 또는 XML 데이터 소스 자세한 내용은 [로그 파일](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e).

1. 로그 경로 매개 변수를 완료합니다. 자세한 내용은 [센서 파일](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009), [로그 파일](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e), 또는 [XML 로그 소스](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887). 올바른 URI를 지정해야 합니다.

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
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> 원격 파일 서버를 식별하는 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 서버 공통 이름 </td> 
   <td colname="col2"> <p> <span class="wintitle"> 서버 공통 이름</span> 파일 서버의 SSL 인증서에 나열됩니다. </p> <p> 이 매개 변수는 <span class="wintitle"> SSL 사용</span> 가 false로 설정되어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주소 </td> 
   <td colname="col2"> <p>파일 서버 컴퓨터의 주소입니다. 비워 둘 수 있습니다. <span class="wintitle"> 이름</span> matches <span class="wintitle"> SSL 서버 공통 이름</span>. </p> <p> 예: <span class="filepath"> visual.mycompany.com</span> 또는 192.168.1.90. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 포트 </td> 
   <td colname="col2"> Data Workbench 서버 컴퓨터가 파일 서버와 통신하는 포트입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 클라이언트 인증서 </td> 
   <td colname="col2"> 의 이름 <span class="wintitle"> SSL 인증서</span> data workbench 서버에 대한 파일(<span class="filepath"> server_cert.pem</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 사용 </td> 
   <td colname="col2"> True 또는 False입니다. True는 파일 서버가 <span class="wintitle"> SSL</span>. </td> 
  </tr> 
 </tbody> 
</table>

DPU에서 FSU에 연결하려면 프록시 서버가 필요한 경우 다음 매개 변수를 완료해야 합니다.

| 매개 변수 | 설명 |
|---|---|
| 프록시 주소 | Data Workbench 서버가 파일 서버에 액세스하는 데 사용해야 하는 프록시 서버의 주소입니다. |
| 프록시 암호 | 선택 사항. 프록시 서버의 암호입니다. |
| 프록시 포트 | 프록시 서버의 포트입니다. 기본값은 8080입니다. |
| 프록시 사용자 이름 | 선택 사항. 프록시 서버의 사용자 이름입니다. |

다음은 정의된 예제입니다 [!DNL Log Server] 에서 [!DNL Log Processing.cfg] 파일. Log Source #1는 FSU01이라는 이름의 컴퓨터의 Logs(Log Paths 매개 변수에 지정된 URI에 참고)라는 디렉토리를 가리키는 LogFile 소스입니다.

![](assets/cfg_LogProcessing_LogServer.png)

## 파일 서버 단위의 권한 편집 {#section-b4a54b591b4e4435a728a67f194057ef}

이전 프로세스에서는 FSU에서 로그 파일을 읽도록 지정된 데이터 세트에 대한 프로필을 구성했습니다. 이제 프로필을 실행 중인 DPU에서 연결을 허용하려면 FSU의 권한을 편집해야 합니다. 다음 단계는 권한 파일 편집을 안내합니다 [!DNL Access Control.cfg].

**FSU에 대한 권한을 편집하려면**

1. 를 엽니다. [!DNL Server Files Manager] fsu로 설정하는 data workbench 서버 시스템의 경우 를 클릭하고 **[!UICONTROL Access Control]** 콘텐츠를 표시합니다.

   열기 및 작업에 대한 자세한 내용은 [!DNL Server Files Manager]를 참조하고 *Data Workbench 사용 안내서*.

1. 에서 [!DNL Server Files Manager] 창 **[!UICONTROL Access Control]** 콘텐츠를 표시합니다. 다음 [!DNL Access Control.cfg] 파일이 이 디렉터리 내에 있습니다.

1. 서버 이름 열의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Access Control.cfg]를 클릭한 다음 **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL Access Control.cfg].

1. 아래에 있는 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**.

1. 에서 [!DNL Access Control] 창 **[!UICONTROL Access Control Groups]** 콘텐츠를 표시합니다.

1. 최종 페이지의 숫자 레이블을 마우스 오른쪽 단추로 클릭합니다. [!DNL AccessGroup] 목록에서 을(를) 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Group]**.

1. 을(를) 입력합니다. [!DNL Name] 새로운 [!DNL AccessGroup]. 예: 서버를 연결하는 중입니다.

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Member]** 새로운 [!DNL AccessGroup]를 클릭한 다음 **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

1. 이 파일 서버에 연결하는 Data Workbench 서버의 DPU의 IP 주소를 입력합니다.
1. 이 FSU에 연결하는 다른 Data Workbench 서버 DPU에 대해 로그 파일에 액세스해야 하는 클러스터의 Data Workbench 서버 DPU를 포함하여 4단계와 5단계를 반복합니다.
1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Read-Only Access]** 새로운 [!DNL AccessGroup]를 클릭한 다음 **[!UICONTROL Add new]** > **[!UICONTROL URI]**.

1. 파일 서버 시스템에서 저장된 로그 파일의 위치를 입력합니다. 경로 사양에 슬래시(/)를 사용합니다. 기본 위치는 /Logs/ 입니다.
1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭한 다음 **[!UICONTROL Save]**.

1. 에서 [!DNL Server Files Manager] 창의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Access Control.cfg] 에서 [!DNL Temp] 열을 누른 다음 **[!UICONTROL Save to]** > **[!UICONTROL server name]** data workbench 서버의 FSU에 로컬로 수행된 변경 사항을 저장하려면

## 로그 파일의 위치 지정 {#section-f9a649bf1b2544feb10ad8820384edb0}

를 편집해야 합니다 [!DNL Communications.cfg] 파일을 FSU에 추가하여 로그 파일의 위치를 지정합니다.

**로그 파일의 위치를 지정하려면**

1. 에서 [!DNL Server Files Manager] 창 **[!UICONTROL Components]** 콘텐츠를 표시합니다. 다음 [!DNL Communications.cfg] 파일이 이 디렉터리 내에 있습니다.

1. 서버 이름 열의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Communications.cfg]를 클릭한 다음 **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL Communications.cfg].

1. 아래에 있는 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Workstation.]**.

1. 에서 [!DNL Communications.cfg] 창 **[!UICONTROL component]** 콘텐츠를 표시합니다.

1. 에서 [!DNL Communications.cfg] 창 **[!UICONTROL Servers]** 콘텐츠를 표시합니다. 몇 개의 서버가 나타날 수 있습니다. 파일 서버, 로깅 서버, 초기화 서버, 상태 서버, 전송 서버 또는 복제 서버

1. (대상 [!DNL Sensor] 로그 소스만 해당) [!DNL LoggingServer]: [!DNL Sensor] data workbench 서버에서 처리할 로그 파일을 작성한 다음 해당 번호를 클릭하여 메뉴를 봅니다. 로그 디렉토리 매개 변수를 편집하여 로그 파일의 원하는 위치를 반영합니다. 기본 로그 디렉토리는 Data Workbench 서버의 설치 디렉토리 내의 로그 폴더입니다.

   에 대한 다른 매개 변수는 수정하지 마십시오 [!DNL LoggingServer].

   ![](assets/cfg_Communications_LoggingServer.png)

1. 로그 파일의 위치를 지정하는 FileServer를 찾습니다. 서버 아래에 여러 개의 파일 서버가 나열될 수 있으므로 원하는 서버를 찾으려면 많은 파일 서버(서버 번호 클릭)의 내용을 확인해야 할 수 있습니다.
1. 편집 [!DNL Local Path] 로그 파일의 위치를 반영하기 위해 FileServer에 대한 URI 매개 변수를 사용합니다. 다음 예는 로그 파일이 Data Workbench 서버의 설치 디렉토리 내의 Logs 폴더에 있음을 보여줍니다.

   ![](assets/cfg_Communications_FS.png)

   >[!NOTE]
   >
   >만약 [!DNL Local Path] 및 URI 매개 변수가 표시되는 대로 채워지면 Data Workbench 서버에서 를 클릭하여 FSU의 로그 파일에 액세스할 수 있습니다 [!DNL Logs] 에서 [!DNL Server Files Manager].

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 구성 창 상단에서 을 클릭한 다음 **[!UICONTROL Save]**.

1. 에서 [!DNL Server Files Manager] 창의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Communications.cfg] 에서 [!DNL Temp] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>* data workbench 서버의 FSU에 로컬로 수행된 변경 사항을 저장하려면

## 클러스터의 중앙 표준화 서버 생성 {#section-2c1f57b683f94cc193bc069e886bba28}

Data Workbench 서버 클러스터에서 실행되도록 데이터 세트 프로필을 구성하는 경우 클러스터의 FSU를 모든 프로필의 차원이 구성된 서버로 만들어야 합니다.

Adobe은 클러스터의 FSU가 클러스터의 마스터 서버 및 중앙 표준화 서버로 사용될 것을 강력히 권장합니다.

FSU를 중앙 표준화 서버로 만들려면 FSU를 열고 편집해야 합니다 [!DNL Communications.cfg] 및 [!DNL Cluster.cfg] FSU의 파일.

**FSU를 중앙 표준화 서버로 만들려면**

1. 추가 [!DNL NormalizeServer] 에 대한 항목 [!DNL Communications.cfg] 파일을 FSU에 저장합니다.

   >[!NOTE]
   >
   >Data Workbench 서버 v5.0 이상을 위한 전체 릴리스 패키지를 설치한 경우 [!DNL Communications.cfg] FSU의 파일은 [!DNL NormalizeServer] 항목이 이미 있습니다. 아래 단계에 따라 항목이 있는지 확인할 수 있습니다.

   1. 를 엽니다. [!DNL Communications.cfg] 에 설명된 대로 data workbench의 파일 [로그 파일의 위치 지정](#section-f9a649bf1b2544feb10ad8820384edb0).

   1. 클릭 **[!UICONTROL component]** 콘텐츠를 표시합니다.
   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Servers]** 을(를) 클릭합니다. **[!UICONTROL Add New]** > **[!UICONTROL Centralized Normalization Server]**.

   1. 의 URI 매개 변수에서 [!DNL NormalizeServer], 유형 [!DNL /Cluster/].

      ![](assets/cfg_Communications_NormalizeServer.png)

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager] 창의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Communications.cfg] 에서 [!DNL Temp] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server]**>* data workbench 서버 FSU에 로컬로 수행된 변경 사항을 저장하는 이름입니다.

1. 에서 중앙 정규화 서버를 정의합니다 [!DNL Cluster.cfg] data workbench 서버 클러스터의 마스터 서버에 있는 파일입니다.

   >[!NOTE]
   >
   >중앙 표준화 서버를 설정하는 FSU가 클러스터의 마스터 Data Workbench 서버가 아닌 경우 클러스터에 있는 DPU의 IP 주소를 [!DNL Cluster Servers] FSU의 액세스 그룹 [!DNL Access Control.cfg] 파일. 서버에 서버를 추가하는 방법은 [!DNL Cluster Servers] 그룹에 대한 액세스 제어 파일 갱신의 *서버 제품 설치 및 관리 안내서.*

   1. 를 엽니다. [!DNL Profile Manager] 데이터 세트 프로필 내에서 를 클릭한 다음 **[!UICONTROL Dataset]** 콘텐츠를 표시합니다. 다음 [!DNL Cluster.cfg] 파일이 이 디렉터리 내에 있습니다.

   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Cluster.cfg]를 클릭한 다음 **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.

   1. 다음 파일 조각에서 강조 표시된 텍스트를 추가합니다.

      [!DNL Cluster = ClusterConfig:]

      [!DNL Normalize Server = serverInfo:]

      [!DNL Address = string:]

      [!DNL Port = int: 80]

      [!DNL SSL Server Common Name = string: server common name]

      [!DNL Use SSL = bool: false]

      >[!NOTE]
      >
      >SSL Server Common Name 매개 변수에 대한 FSU의 공통 이름을 입력하면 FSU는 해당 이름을 사용합니다 [!DNL .address] 파일을 사용하여 일반 이름을 확인합니다. 에 대한 정보 [!DNL .address] 파일, 자세한 내용은 *서버 제품 설치 및 관리 안내서*.

   1. 파일을 저장합니다.
   1. 에서 [!DNL Profile Manager]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Cluster.cfg] 에서 [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > ***[!UICONTROL dataset profile name]*** 로컬에서 변경한 데이터 세트 프로필을 저장하려면 다음을 수행하십시오.
