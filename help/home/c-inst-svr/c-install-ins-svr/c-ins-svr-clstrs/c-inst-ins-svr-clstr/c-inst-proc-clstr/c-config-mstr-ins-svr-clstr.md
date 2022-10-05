---
description: 기본 Insight Server에서 클러스터를 구성하고 클러스터에 대한 액세스 제어 파일 업데이트 등에 대한 정보입니다.
title: 클러스터링을 위한 기본 Insight Server 구성
uuid: c3ac38e3-79c5-4863-9156-194589a6bcbd
exl-id: 28126ba4-6d81-4ca4-895c-4e8b1a54a693
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 1%

---

# 클러스터링을 위한 기본 Insight Server 구성{#configuring-the-master-insight-server-for-clustering}

{{eol}}

기본 Insight Server에서 클러스터를 구성하고 클러스터에 대한 액세스 제어 파일 업데이트 등에 대한 정보입니다.

클러스터를 구성하려면 마스터에서 다음 단계를 수행합니다 [!DNL Insight Server]:

* 처리 추가 [!DNL Insight Servers’] 주소 파일에 대한 공통 이름 및 주소입니다.
* 모두 추가 [!DNL Insight Servers] 클러스터 서버 그룹 [!DNL Access Control.cfg] 파일.

* 업데이트 [!DNL Synchronize.cfg] 마스터를 가리키도록 Components for Processing Server 디렉토리에 있는 파일 [!DNL Insight Server].

* 필요한 경우 를 수정합니다 [!DNL Disk Files.cfg] 파일을 Components for Processing Server 디렉토리에 추가하여 [!DNL temp.db] 처리 중인 파일 [!DNL Insight Servers].

이 단계를 완료하려면 개인의 디지털 인증서에 지정된 일반 이름을 알고 있어야 합니다 [!DNL Insight Server]) 및 각 IP 주소의 [!DNL Insight Server] 입니다. 이 정보가 없는 경우 계속하기 전에 해당 정보를 얻으십시오.

>[!NOTE]
>
>이 섹션에 설명된 절차는 다음과 같습니다 [!DNL Insight]. 설치하지 않은 경우 [!DNL Insight]를 채울 때는 **[!DNL Insight]사용 안내서** 계속 진행하기 전에

## 주소 파일에 처리 Insight Server 추가 {#section-2fe5298180164e8dbaa59ea6b6ff682d}

다음 절차를 사용하여 처리를 추가합니다 [!DNL Insight Servers’] 일반 이름 및 IP 주소를 마스터의 주소 파일에 추가 [!DNL Insight Server]. 주소 파일이 마스터에서 유지 관리되고 관리되지만 [!DNL Insight Server]로 설정되면 모든 [!DNL Insight Servers] 입니다.)

>[!NOTE]
>
>다음은 주소 파일이 마스터에 대해 이미 구성되어 있다고 가정합니다 [!DNL Insight Server]. 마스터를 아직 추가하지 않은 경우 [!DNL Insight Server’s] 주소 파일에 대한 IP 주소, [서버의 네트워크 위치 정의](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649) 시작하기 전에

**처리를 추가하려면 [!DNL Insight Servers] 주소 파일로**

1. 시작 [!DNL Insight] 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 를 클릭하여 구성 프로필을 로드합니다(아직 열려 있지 않은 경우). **[!UICONTROL Switch Profile]** > **[!UICONTROL Configuration]**.

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.

1. 마스터의 아이콘을 마우스 오른쪽 단추로 누릅니다 **[!UICONTROL Insight Server]** 을(를) 클릭합니다. **[!UICONTROL Server Files]**.

1. 에서 [!DNL Server Files Manager]를 열고 주소 디렉토리를 열고 다음을 수행하여 을 엽니다. [!DNL Insight Server’s] 주소 파일:

   1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 및 클릭 **[!UICONTROL Make Local]**.

   1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. 의 컨텐츠를 확장합니다. [!DNL Locations] 그런 다음 NetworkLocation 0, Addresses 및 AddressDefinition을 확장합니다.
1. 각 처리에 대해 NetworkLocation 0에 AddressDefinition을 추가하려면 다음을 수행합니다 [!DNL Insight Server] 클러스터:

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL AddressDefinition]** 을(를) 클릭합니다. **[!UICONTROL Add New]** > **[!UICONTROL Address Definition]**.

   1. Name 매개 변수에서 처리를 지정합니다 [!DNL Insight Server’s] 일반 이름.
   1. Address 매개 변수에서 처리를 지정합니다 [!DNL Insight Server’s] IP 주소.

      10.10.116과 같이 주소 필드에서 별표를 와일드카드로 사용할 수 있습니다.&#42;를 눌러 클러스터링을 단순화합니다. 자세한 내용은 [액세스 수준 이해](../../../../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-undst-acc-lvls.md#concept-6b292edf79214750a8d0525097b8795a).

      다음 예제에서는 두 개의 클러스터를 정의합니다 [!DNL Insight Servers]:

      ![](assets/cfg_cluster_AddressDefinition1IP.png)

1. 서버가 여러 네트워크에 연결되어 있는 경우 6단계를 반복하여 처리를 추가합니다 [!DNL Insight Servers] NetworkLocations에 연결할 수도 있습니다.

   다음 예는 네 개의 클러스터를 보여줍니다 [!DNL Insight Servers] 두 네트워크에 연결됨(&quot;회사 인트라넷&quot; 및 &quot;인터넷&quot;).

   ![](assets/cfg_cluster_AddressDefinition2IP.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 선택 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## 클러스터의 액세스 제어 파일 업데이트 {#section-fce1367d92a445168c35e9ca506e7d6b}

를 사용하려면 [!DNL Insight Servers] 클러스터에서 각각 [!DNL Insight Server] 클러스터(마스터 포함) [!DNL Insight Server])은 클러스터 서버 액세스 제어 그룹에 속해야 합니다. 클러스터 서버 그룹은 클러스터에 참여할 수 있는 서버(IP 주소별)를 식별합니다. 이 파일은 마스터에서 유지 관리되고 관리되지만 [!DNL Insight Server]를 채울 수 있도록 [!DNL Insight Servers] 입니다.

**액세스 제어 파일을 편집하려면**

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.

1. 마스터의 아이콘을 마우스 오른쪽 단추로 누릅니다 [!DNL Insight Server] 을(를) 클릭합니다. **[!UICONTROL Server Files]**.

1. 에서 [!DNL Server Files Manager]액세스 제어 디렉터리를 엽니다.
1. 다음을 수행하여 을 엽니다. [!DNL Access Control.cfg] 파일:

   1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 및 클릭 **[!UICONTROL Make Local]**.

   1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. 액세스 제어 그룹 구조를 확장한 다음 액세스 그룹(클러스터 서버)을 확장합니다.
1. 각 [!DNL Insight Server] 클러스터(마스터 포함) [!DNL Insight Server])에서 다음을 수행합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Members]** 을(를) 클릭합니다. **[!UICONTROL Add New]** > **[!UICONTROL New Member]**.

   1. 을(를) 지정합니다. [!DNL Insight Server’s] IP 주소(이름이 아닌 숫자 IP 주소) 만약 [!DNL Insight Servers] 여러 네트워크에 연결되어 있는 경우 이 액세스 그룹은 [!DNL Insight Servers] 클러스터 내에서 서버 간 통신에 사용합니다.

      다음은 네 개의 클러스터에 대한 AccessGroup(클러스터 서버)을 보여 줍니다 [!DNL Insight Servers].

      ![](assets/cfg_cluster_AccessControlMembers.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Server Files Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## 동기화 파일 구성 {#section-d23e751771c84da6bab6a34a8db867bc}

다음 절차를 사용하여 [!DNL Synchronize.cfg] 파일. 이 파일의 중앙 복사본은 마스터에서 유지됩니다 [!DNL Insight Server]. 처리 [!DNL Insight Servers] 클러스터에서 마스터와 통신 시작 [!DNL Insight Server] 이 파일의 업데이트된 복사본을 검색하려면

다음 [!DNL Synchronize.cfg] 파일이 마스터 위치를 지정합니다. [!DNL Insight Server]. 또한 각 처리가 수행된 관리 파일 세트를 식별합니다 [!DNL Insight Servers] 클러스터에서 마스터에서 [!DNL Insight Server]. 처리 [!DNL Insight Servers] 마스터에서 이러한 파일을 자동으로 다운로드합니다. [!DNL Insight Server] 시작할 때 또한 마스터에서 이러한 파일의 업데이트된 복사본을 동적으로 검색합니다 [!DNL Insight Server] 파일이 변경될 때.

>[!NOTE]
>
>구성 [!DNL Synchronize.cfg] 마스터의 파일 [!DNL Insight Server], 마스터 [!DNL Insight Server] 자체는 이 파일을 사용하지 않습니다. 마스터에서 이 파일을 업데이트합니다 [!DNL Insight Server] 처리 시 제대로 구성되도록 [!DNL Insight Servers] 파일을 검색합니다.

**마스터에서 Synchronize.cfg 파일을 업데이트하려면[!DNL Insight Server]**

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.

1. 마스터의 아이콘을 마우스 오른쪽 단추로 누릅니다 [!DNL Insight Server] 을(를) 클릭합니다. **[!UICONTROL Server Files]**.

1. in [!DNL Server Files Manager]를 열고 **[!UICONTROL Components]** 처리 서버 디렉토리.

1. 열려면 다음을 수행하십시오 [!DNL Synchronize.cfg]:

   1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 및 클릭 **[!UICONTROL Make Local]**.

   1. 마우스 오른쪽 단추를 클릭합니다. [!DNL Temp] 확인 표시 를 클릭한 다음 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. 구성 요소 구조를 확장합니다.
1. Cluster Primary Server Address 매개 변수에서 마스터의 IP 주소(기본)를 지정합니다 **[!UICONTROL Insight Server]**.

   ![](assets/cfg_cluster_SyncFile_CentralCopy.png)

   마스터 간에 동기화가 발생할 때마다 기록되는 로그를 만들려면 [!DNL Insight Server] 처리 [!DNL Insight Servers]동기화 로그 활성화 매개 변수가 &quot;true&quot;로 설정되어 있는지 확인합니다.

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. in [!DNL Server Files Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## 데이터 세트 위치 구성(temp.db) {#section-5ec257a4b4c64fb58baec1f12119a822}

처리를 원하는 경우 다음 절차를 수행합니다 [!DNL Insight Servers] 유지 관리 [!DNL temp.db] (데이터 세트)를 기본 위치가 아니거나 배포하려는 경우 [!DNL temp.db] 여러 드라이브에 걸쳐

>[!NOTE]
>
>왜냐하면 [!DNL Insight Servers] 모두 동일함 [!DNL Disk Files.cfg]로 설정되면 모두 이 파일에서 지정하는 파일 위치를 지원해야 합니다. 예를 들어, [!DNL temp.db] 아래와 같이 변경하는 것을 의미합니다. 드라이브, 모든 처리 [!DNL Insight Server] 클러스터에서 에는 E가 있어야 합니다. 드라이브.

**temp.db의 위치를 구성하려면**

1. in [!DNL Insight], [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.

1. 마스터의 아이콘을 마우스 오른쪽 단추로 누릅니다 [!DNL Insight Server] 을(를) 클릭합니다. **[!UICONTROL Server Files]**.

1. 에서 [!DNL Server Files Manager]를 열고 **[!UICONTROL Components for Processing Servers]** 디렉토리.

1. 열려면 다음을 수행하십시오 [!DNL Disk Files.cfg]:

   1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 및 클릭 **[!UICONTROL Make Local]**.

   1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp]열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. DiskSpaceManagerComponent 구조를 확장한 다음 디스크 파일 목록을 확장합니다.
1. 항목 0을 편집하여 위치 변경 [!DNL temp.db] 파일.
1. 배포하려면 [!DNL temp.db] 여러 드라이브에 걸쳐 아래 단계를 사용하여 각 추가 드라이브에 대한 추가 항목을 만듭니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Disk Files]** 을(를) 클릭합니다. **[!UICONTROL Add New]** > **[!UICONTROL Disk File]**.

   1. 새 항목에서 원하는 위치를 지정합니다 [!DNL temp.db] 작성됩니다.
   다음은 다음과 같습니다 [!DNL temp.db] 4개의 드라이브에 걸쳐 작성됩니다.

   ![](assets/cfg_diskfiles_exampleNewValues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. in [!DNL Server Files Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
