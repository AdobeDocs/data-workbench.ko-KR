---
description: 액세스 수준에서는 사용자 그룹이 읽거나 수정할 수 있는 시스템의 URI를 설명합니다.
title: 액세스 수준 이해
uuid: e9091ae1-9a34-4e00-a928-20d04119ee9e
exl-id: 64e2dc39-1ca1-425b-bec7-acb10a8819c0
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 3%

---

# 액세스 수준 이해{#understanding-access-levels}

액세스 수준에서는 사용자 그룹이 읽거나 수정할 수 있는 시스템의 URI를 설명합니다.

다음 지침을 따라 조직의 사용자에게 필요한 액세스 수준을 정의합니다.

* 후행 슬래시 문자가 없는 특정 URI는 해당 URI에만 대한 액세스를 제한합니다. 예를 들어 [!DNL /Components/Communications.cfg]은 [!DNL Communications.cfg]파일 전용 액세스를 제공합니다.

* 디렉토리를 지정하는 후행 슬래시(/)는 해당 문자열로 시작하는 모든 URI에 대한 액세스를 그룹 구성원에게 제공합니다. 예를 들어 /Profiles/는 전체 Profiles 디렉토리에 대한 액세스를 제공합니다.
* 후행 달러 기호($)는 디렉토리인 경우에도 정확한 URI에 대한 액세스만 제한합니다. 예를 들어 /Profiles/$은 기본 프로필 디렉토리를 읽을 수 있는 액세스 권한을 제공하지만 해당 디렉터리 내의 파일을 읽을 수는 없습니다.

   특정 파일에 액세스하려면 후행 $를 사용할 필요가 없습니다.

   예를 들어 [!DNL /Components/Communications.cfg] 및 [!DNL /Components/Communications.cfg$]은 동일한 액세스를 제공합니다.

* 퍼센트 기호(%)는 CN(일반 이름)과 함께 사용하여 액세스를 허용할 수 있습니다. 예를 들어 /Users/%CN%[!DNL Insight] 사용자의 SSL 인증서 일반 이름과 일치하는 사용자 디렉토리에 대한 액세스를 허용합니다. 이 구문은 URI에서 한 번만 사용할 수 있습니다.

사전 정의된 액세스 제어 그룹의 URI는 다음과 같이 구성되었습니다.

<table id="table_8E6FDD741BF24E2DAD96A2919FAE6C7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 그룹 이름 </th> 
   <th colname="col2" class="entry"> 읽기 전용 액세스 </th> 
   <th colname="col3" class="entry"> 읽기-쓰기 액세스 </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>관리자 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>/ </p> </td> 
   <td colname="col4"> <p>모든 <span class="keyword"> Insight Server</span> 디렉토리에 대한 읽기 및 쓰기 액세스. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>센서 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>/SensorInit.vsp </p> <p>/Submit.vsp </p> </td> 
   <td colname="col4"> <p><span class="wintitle"> 센서</span>가 <span class="keyword"> Insight 서버</span>와 통신하는 데 사용하는 두 파일에 대한 읽기 및 쓰기 액세스 권한을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 참조 </p> </td> 
   <td colname="col2"> <p>/프로필/ </p> <p>/상태/ </p> <p>/Software/ </p> <p>/주소/ </p> <p>/사용자 참조/$ </p> </td> 
   <td colname="col3"> /Users/%CN%/ </td> 
   <td colname="col4"> <p><span class="keyword"> Insight</span> 사용자의 SSL 인증서 일반 이름과 일치하는 사용자 디렉토리에 대한 읽기 및 쓰기 액세스. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파워 유저 </p> </td> 
   <td colname="col2"> <p>/프로필/$ </p> <p>/상태/ </p> <p>/Software/ </p> <p>/주소/ </p> <p>/사용자 참조/$ </p> </td> 
   <td colname="col3"> <p>/프로필/ </p> <p>/Users/%CN%/ </p> </td> 
   <td colname="col4"> <p>Power User는 Profiles 디렉토리에 쓰는 추가 기능과 함께 Users와 동일한 액세스가 허용됩니다. 이러한 사용자는 프로파일을 편집하고 새로 정의된 작업 영역을 배포할 때와 같이 다른 <span class="keyword"> Insight</span> 사용자에 대해 변경 사항이 자동으로 업데이트되도록 설정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>클러스터 서버 </p> </td> 
   <td colname="col2"> <p>/처리 서버용 구성 요소/ </p> <p>/주소/ </p> <p>/프로필/ </p> <p>/Lookups/ </p> <p>/액세스 제어/ </p> <p>/Bin/ </p> <p>/로그/ </p> </td> 
   <td colname="col3"> <p>/Cluster/ </p> </td> 
   <td colname="col4"> <p>클러스터 디렉토리에 대한 읽기 및 쓰기 액세스 권한 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보고서 서버 </p> </td> 
   <td colname="col2"> <p>/프로필/$ </p> <p>/상태/ </p> <p>/Software/ </p> <p>/주소/ </p> <p>/사용자 참조/$ </p> </td> 
   <td colname="col3"> <p>/프로필/ </p> <p>/Users/%CN%/ </p> <p>/ReportStatus.vsp </p> </td> 
   <td colname="col4"> <p>보고서 컴퓨터는 <span class="filepath"> ReportStatus.vsp</span> 파일에 쓰는 기능이 추가되어 전원 사용자와 동일한 액세스가 허용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**액세스 제어를 구성하려면**

액세스 제어 그룹을 정의할 때 이 [!DNL Insight Server] 컴퓨터에 액세스해야 하는 모든 시스템 관리자, 사용자, 클러스터 서버 및 보고서 서버 사용자를 포함해야 합니다. IP 주소 또는 일반 이름 또는 조직과 같은 SSL 인증서 정보를 사용하여 액세스 권한을 부여할 수 있습니다.

>[!NOTE]
>
>[!DNL Access Control.cfg] 파일이 [!DNL Insight Server]에서 변경되면 기존의 모든 연결이 종료되어 다시 연결해야 합니다. 업데이트된 [!DNL Access Control.cfg] 파일의 권한에 대해 연결이 확인됩니다. 서버 관리자 인터페이스에서 [!DNL Insight Server] 아이콘은 연결이 종료되고 다른 모든 사람과 다시 강제로 연결되므로 일시적으로 빨간색으로 바뀌고 다시 녹색으로 바뀝니다.

1. [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.

1. 구성할 [!DNL Insight Server] 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Files]** 을 클릭합니다.

1. [!DNL Server Files Manager]에서 **[!UICONTROL Access Control]**&#x200B;을 클릭하여 콘텐트를 봅니다. [!DNL Access Control.cfg] 파일이 이 디렉터리 내에 있습니다.

1. [!DNL Access Control.cfg]에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;을 클릭합니다. [!DNL Access Control.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.

1. [!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**&#x200B;를 클릭합니다.

1. [!DNL Access Control.cfg] 창에서 **[!UICONTROL Access Control Groups]**&#x200B;을 클릭하여 내용을 봅니다.

   ![](assets/access_ctrl_cfg.png)

1. 새 액세스 제어 그룹을 추가하려면:

   1. **[!UICONTROL Access Control Groups]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Group]**&#x200B;를 클릭합니다.

   1. **[!UICONTROL Members]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Member]**&#x200B;를 클릭합니다.

      기본 그룹의 구성원은 사전 정의되지 않았습니다. 기본적으로 관리자 액세스 권한은 127.0.0.1(로컬 호스트)에 부여되며 [!DNL Sensor] 액세스 권한은 IP:*에 부여됩니다. 다른 모든 액세스 제어 그룹 구성원을 정의해야 합니다.

   1. 매개 변수를 완료합니다.

1. 기존 액세스 제어 그룹에 새 구성원을 추가하려면:

   1. 해당 액세스 제어 그룹 아래의 **[!UICONTROL Members]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Member]**&#x200B;를 클릭합니다.

1. 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save]**&#x200B;을 클릭하여 파일을 저장합니다.

1. 로컬로 변경한 [!DNL Insight Server] 컴퓨터를 저장하려면 [!DNL Server Files Manager]에서 [!DNL Temp] 열에서 [!DNL Access Control.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** *&lt;**[!UICONTROL server name]***&#x200B;을 클릭합니다.
