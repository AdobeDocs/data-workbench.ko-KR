---
description: 기본 Insight Server에서 클러스터를 구성하고 클러스터에 대한 액세스 제어 파일 업데이트 등에 대한 정보입니다.
title: 클러스터링을 위한 기본 Insight Server 구성
uuid: c3ac38e3-79c5-4863-9156-194589a6bcbd
exl-id: 28126ba4-6d81-4ca4-895c-4e8b1a54a693
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 1%

---

# 클러스터링을 위한 기본 Insight Server 구성{#configuring-the-master-insight-server-for-clustering}

기본 Insight Server에서 클러스터를 구성하고 클러스터에 대한 액세스 제어 파일 업데이트 등에 대한 정보입니다.

클러스터를 구성하려면 마스터 [!DNL Insight Server]에서 다음 단계를 수행하십시오.

* 처리 [!DNL Insight Servers’] 공통 이름 및 주소를 주소 파일에 추가합니다.
* [!DNL Access Control.cfg] 파일의 클러스터 서버 그룹에 모든 [!DNL Insight Servers]을 추가합니다.

* Components for Processing Servers 디렉터리에서 [!DNL Synchronize.cfg] 파일을 업데이트하여 마스터 [!DNL Insight Server]를 가리킵니다.

* 필요한 경우 처리 중인 Components for Processing Servers 디렉터리에서 [!DNL Disk Files.cfg] 파일을 수정하여 처리 [!DNL Insight Servers]에서 [!DNL temp.db] 파일의 위치를 지정합니다.

이 단계를 완료하려면 일반 이름([!DNL Insight Server] 개인의 디지털 인증서에 지정된 대로) 및 클러스터에 있는 각 [!DNL Insight Server]의 IP 주소를 알고 있어야 합니다. 이 정보가 없는 경우 계속하기 전에 해당 정보를 얻으십시오.

>[!NOTE]
>
>이 섹션에 설명된 절차는 [!DNL Insight]이 필요합니다. [!DNL Insight]을 설치하지 않은 경우 계속하기 전에 **[!DNL Insight]사용 안내서**&#x200B;의 지침을 따르십시오.

## 주소 파일 {#section-2fe5298180164e8dbaa59ea6b6ff682d}에 처리 Insight Server 추가

다음 절차를 사용하여 처리 [!DNL Insight Servers’] 공통 이름 및 IP 주소를 마스터 [!DNL Insight Server]의 주소 파일에 추가합니다. (주소 파일이 마스터 [!DNL Insight Server]에서 유지 관리되지만 클러스터의 모든 [!DNL Insight Servers]에서 사용됩니다.)

>[!NOTE]
>
>다음은 마스터 [!DNL Insight Server]에 대해 주소 파일이 이미 구성되어 있다고 가정합니다. 마스터 [!DNL Insight Server’s] IP 주소를 주소 파일에 아직 추가하지 않은 경우 시작하기 전에 [서버의 네트워크 위치 정의](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649)에 설명된 절차를 완료하십시오.

**주소 파일 [!DNL Insight Servers] 에 처리를 추가하려면**

1. [!DNL Insight] 을 시작하고 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Switch Profile]** > **[!UICONTROL Configuration]** 를 클릭하여 구성 프로필을 로드합니다(아직 열려 있지 않은 경우).

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 Servers Manager 작업 영역을 엽니다.

1. 마스터 **[!UICONTROL Insight Server]** 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]** 를 클릭합니다.

1. [!DNL Server Files Manager]에서 Addresses 디렉토리를 열고 다음을 수행하여 [!DNL Insight Server’s] 주소 파일을 엽니다.

   1. *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다.

   1. [!DNL Temp] 열에서 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]** 를 클릭합니다.

1. [!DNL Locations] 구조의 내용을 확장한 다음 NetworkLocation 0, Addresses 및 AddressDefinition을 확장합니다.
1. 다음을 수행하여 클러스터의 각 처리 [!DNL Insight Server]에 대해 NetworkLocation 0에 AddressDefinition을 추가합니다.

   1. **[!UICONTROL AddressDefinition]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add New]** > **[!UICONTROL Address Definition]** 를 클릭합니다.

   1. Name 매개 변수에서 처리 [!DNL Insight Server’s] 공통 이름을 지정합니다.
   1. Address 매개 변수에서 처리 [!DNL Insight Server’s] IP 주소를 지정합니다.

      10.10.116과 같이 주소 필드에서 별표를 와일드카드로 사용할 수 있습니다.* 클러스터링을 단순화하는 것이 좋습니다. [액세스 수준 이해](../../../../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-undst-acc-lvls.md#concept-6b292edf79214750a8d0525097b8795a)를 참조하십시오.

      다음 예제는 두 개의 [!DNL Insight Servers]을 포함하는 클러스터를 정의합니다.

      ![](assets/cfg_cluster_AddressDefinition1IP.png)

1. 서버가 여러 네트워크에 연결되어 있는 경우 6단계를 반복하여 해당 네트워크에 대한 NetworkLocations에 처리 [!DNL Insight Servers]를 추가합니다.

   다음 예는 두 네트워크(&quot;회사 인트라넷&quot; 및 &quot;인터넷&quot;)에 연결된 4개의 [!DNL Insight Servers] 클러스터를 보여줍니다.

   ![](assets/cfg_cluster_AddressDefinition2IP.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. [!DNL Server Files Manager]에서 [!DNL Temp] 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 선택합니다.

## 클러스터 {#section-fce1367d92a445168c35e9ca506e7d6b}에 대한 액세스 제어 파일 업데이트

클러스터에서 [!DNL Insight Servers]을 사용하려면 클러스터(마스터 [!DNL Insight Server] 포함)의 각 [!DNL Insight Server]이(가) 클러스터 서버 액세스 제어 그룹에 속해야 합니다. 클러스터 서버 그룹은 클러스터에 참여할 수 있는 서버(IP 주소별)를 식별합니다. 이 파일은 마스터 [!DNL Insight Server]에서 유지 관리되지만 클러스터의 모든 [!DNL Insight Servers]에서 사용됩니다.

**액세스 제어 파일을 편집하려면**

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 Servers Manager 작업 영역을 엽니다.

1. 마스터 [!DNL Insight Server] 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]** 를 클릭합니다.

1. [!DNL Server Files Manager]에서 액세스 제어 디렉터리를 엽니다.
1. 다음을 수행하여 [!DNL Access Control.cfg] 파일을 엽니다.

   1. *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다.

   1. [!DNL Temp] 열에서 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]** 를 클릭합니다.

1. 액세스 제어 그룹 구조를 확장한 다음 액세스 그룹(클러스터 서버)을 확장합니다.
1. 클러스터의 각 [!DNL Insight Server](마스터 [!DNL Insight Server] 포함)에 대해 다음을 수행합니다.

   1. **[!UICONTROL Members]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add New]** > **[!UICONTROL New Member]** 를 클릭합니다.

   1. [!DNL Insight Server’s] IP 주소(해당 이름이 아닌 숫자 IP 주소)를 지정합니다. [!DNL Insight Servers]이(가) 여러 네트워크에 연결되어 있는 경우 이 AccessGroup은 클러스터 내의 서버 간 통신에 사용하는 내부 주소만 포함해야 합니다.[!DNL Insight Servers]

      다음은 네 개의 [!DNL Insight Servers] 클러스터에 대한 AccessGroup(클러스터 서버)을 보여 줍니다.

      ![](assets/cfg_cluster_AccessControlMembers.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. [!DNL Server Files Manager]에서 [!DNL Temp] 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 클릭합니다.

## 동기화 파일 구성 {#section-d23e751771c84da6bab6a34a8db867bc}

다음 절차를 사용하여 [!DNL Synchronize.cfg] 파일의 중앙 복사본을 구성할 수 있습니다. 이 파일의 중앙 복사본은 마스터 [!DNL Insight Server]에서 유지됩니다. 클러스터의 처리 [!DNL Insight Servers]에서는 마스터 [!DNL Insight Server]와의 통신을 시작하여 이 파일의 업데이트된 복사본을 검색합니다.

[!DNL Synchronize.cfg] 파일은 마스터 [!DNL Insight Server]의 위치를 지정합니다. 또한 클러스터에서 처리 [!DNL Insight Servers]이(가) 마스터 [!DNL Insight Server]에서 각각 검색하는 관리 파일 세트를 식별합니다. 처리 [!DNL Insight Servers]은(는) 이러한 파일을 시작할 때 마스터 [!DNL Insight Server]에서 자동으로 다운로드합니다. 또한 파일이 변경될 때 마스터 [!DNL Insight Server]에서 이러한 파일의 업데이트된 복사본을 동적으로 검색합니다.

>[!NOTE]
>
>마스터 [!DNL Insight Server]에서 [!DNL Synchronize.cfg] 파일을 구성하지만 마스터 [!DNL Insight Server] 자체는 이 파일을 사용하지 않습니다. 이 파일은 처리 [!DNL Insight Servers]에서 파일을 검색할 때 올바르게 구성되도록 마스터 [!DNL Insight Server]에서 업데이트합니다.

**마스터에서 Synchronize.cfg 파일을 업데이트하려면[!DNL Insight Server]**

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 Servers Manager 작업 영역을 엽니다.

1. 마스터 [!DNL Insight Server] 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]** 를 클릭합니다.

1. [!DNL Server Files Manager]에서 Processing Server용 **[!UICONTROL Components]** 디렉토리를 엽니다.

1. 다음을 수행하여 [!DNL Synchronize.cfg]을 엽니다.

   1. *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다.

   1. [!DNL Temp] 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]** 를 클릭합니다.

1. 구성 요소 구조를 확장합니다.
1. 클러스터 주 서버 주소 매개 변수에서 마스터(기본) **[!UICONTROL Insight Server]**&#x200B;의 IP 주소를 지정합니다.

   ![](assets/cfg_cluster_SyncFile_CentralCopy.png)

   마스터 [!DNL Insight Server] 및 처리 [!DNL Insight Servers] 간에 동기화가 발생할 때마다 기록하는 로그를 생성하려면 동기화 로그 활성화 매개 변수가 &quot;true&quot;로 설정되어 있는지 확인합니다.

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. [!DNL Server Files Manager]에서 [!DNL Temp] 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 클릭합니다.

## 데이터 세트 위치 구성(temp.db) {#section-5ec257a4b4c64fb58baec1f12119a822}

처리 [!DNL Insight Servers]이(가) 기본 위치가 아닌 다른 디렉터리나 드라이브에서 [!DNL temp.db](데이터 세트)를 유지하거나 여러 드라이브에 [!DNL temp.db]을(를) 배포하려는 경우 다음 절차를 수행하십시오.

>[!NOTE]
>
>처리 [!DNL Insight Servers]은 모두 동일한 [!DNL Disk Files.cfg]을 공유하므로 이 파일에서 지정하는 파일 위치를 모두 지원해야 합니다. 예를 들어 E에 [!DNL temp.db]을 지정하는 경우:드라이브, 클러스터의 모든 처리 [!DNL Insight Server]에 E가 있어야 합니다.드라이브.

**temp.db의 위치를 구성하려면**

1. [!DNL Insight]의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 Servers Manager 작업 영역을 엽니다.

1. 마스터 [!DNL Insight Server] 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]** 를 클릭합니다.

1. [!DNL Server Files Manager]에서 **[!UICONTROL Components for Processing Servers]** 디렉토리를 엽니다.

1. 다음을 수행하여 [!DNL Disk Files.cfg]을 엽니다.

   1. *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다.

   1. [!DNL Temp]열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**&#x200B;를 클릭합니다.

1. DiskSpaceManagerComponent 구조를 확장한 다음 디스크 파일 목록을 확장합니다.
1. 항목 0을 편집하여 [!DNL temp.db] 파일의 위치를 변경합니다.
1. 여러 드라이브에 [!DNL temp.db]을 분배하려면 아래 단계를 사용하여 각 추가 드라이브에 대한 추가 항목을 만드십시오.

   1. **[!UICONTROL Disk Files]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add New]** > **[!UICONTROL Disk File]** 를 클릭합니다.

   1. 새 항목에서 [!DNL temp.db]을 작성할 위치를 지정합니다.
   다음은 4개의 드라이브에 작성된 [!DNL temp.db]을 보여 줍니다.

   ![](assets/cfg_diskfiles_exampleNewValues.png)

1. 다음을 수행하여 서버에 변경 내용을 저장합니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. [!DNL Server Files Manager]에서 [!DNL Temp] 열의 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 클릭합니다.
