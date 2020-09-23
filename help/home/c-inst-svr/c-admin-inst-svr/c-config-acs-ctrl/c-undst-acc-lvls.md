---
description: 액세스 수준에서는 사용자 그룹이 읽거나 수정할 수 있는 시스템의 URI를 설명합니다.
solution: Analytics
title: 액세스 수준 이해
uuid: e9091ae1-9a34-4e00-a928-20d04119ee9e
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 3%

---


# 액세스 수준 이해{#understanding-access-levels}

액세스 수준에서는 사용자 그룹이 읽거나 수정할 수 있는 시스템의 URI를 설명합니다.

조직의 사용자에 대해 원하는 대로 액세스 수준을 정의하려면 다음 지침을 따르십시오.

* 후행 슬래시 문자가 없는 특정 URI는 해당 URI에만 액세스할 수 있습니다. 예를 들어 [!DNL /Components/Communications.cfg] 파일 [!DNL Communications.cfg]에 대한 액세스 권한만 제공합니다.

* 디렉토리를 지정하는 후행 슬래시(/)는 해당 문자열로 시작하는 모든 URI에 대한 액세스를 그룹 구성원에게 제공합니다. 예를 들어 /Profiles/는 전체 Profiles 디렉토리에 대한 액세스를 제공합니다.
* 후행 달러 기호($)는 디렉터리인 경우에도 정확한 URI에 대한 액세스만 제한합니다. 예를 들어 /Profiles/$ 은 기본 프로필 디렉토리를 읽을 수 있는 액세스 권한을 제공하지만 해당 디렉터리 내의 파일을 읽을 수는 없습니다.

   특정 파일에 액세스하려면 후행 $를 사용할 필요가 없습니다.

   예를 들어, [!DNL /Components/Communications.cfg] 그리고 동일한 액세스 권한을 [!DNL /Components/Communications.cfg$] 제공합니다.

* 퍼센트 기호(%)를 CN(일반 이름)과 함께 사용하여 액세스를 허용할 수 있습니다. 예를 들어 /Users/%CN%/ 사용자에게는 SSL 인증서 일반 이름과 일치하는 사용자 디렉토리에 액세스할 수 [!DNL Insight] 있습니다. 이 구문은 URI에서 한 번만 사용할 수 있습니다.

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
   <td colname="col4"> <p>모든 Insight Server 디렉토리에 대한 읽기 및 <span class="keyword"> 쓰기 액세스</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>센서 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>/SensorInit.vsp </p> <p>/Submit.vsp </p> </td> 
   <td colname="col4"> <p>센서가 <span class="wintitle"> Insight 서버와 통신하는 데 사용하는 두 개의 파일에 대한 읽기 및 쓰기 액세스</span> 권한입니다 <span class="keyword"></span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 참조 </p> </td> 
   <td colname="col2"> <p>/프로필/ </p> <p>/상태/ </p> <p>/Software/ </p> <p>/주소/ </p> <p>/사용자 참조/$ </p> </td> 
   <td colname="col3"> /Users/%CN%/ </td> 
   <td colname="col4"> <p>Insight 사용자의 SSL 인증서 일반 이름과 일치하는 사용자 디렉토리에 대한 읽기 및 쓰기 액세스 <span class="keyword"></span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>파워 유저 </p> </td> 
   <td colname="col2"> <p>/프로필/$ </p> <p>/상태/ </p> <p>/Software/ </p> <p>/주소/ </p> <p>/사용자 참조/$ </p> </td> 
   <td colname="col3"> <p>/프로필/ </p> <p>/Users/%CN%/ </p> </td> 
   <td colname="col4"> <p>Power Users는 Profiles 디렉토리에 쓸 수 있는 기능이 추가되어 사용자와 동일한 액세스가 허용됩니다. 이러한 사용자는 프로파일을 편집하고 새로 정의된 작업 영역을 배포할 때와 같이 다른 <span class="keyword"> Insight</span> 사용자에 대해 변경 사항이 자동으로 업데이트되도록 설정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>클러스터 서버 </p> </td> 
   <td colname="col2"> <p>/처리 서버용 구성 요소/ </p> <p>/주소/ </p> <p>/프로필/ </p> <p>/Lookups/ </p> <p>/액세스 제어/ </p> <p>/Bin/ </p> <p>/로그/ </p> </td> 
   <td colname="col3"> <p>/Cluster/ </p> </td> 
   <td colname="col4"> <p>클러스터 디렉토리를 읽고 쓸 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보고서 서버 </p> </td> 
   <td colname="col2"> <p>/프로필/$ </p> <p>/상태/ </p> <p>/Software/ </p> <p>/주소/ </p> <p>/사용자 참조/$ </p> </td> 
   <td colname="col3"> <p>/프로필/ </p> <p>/Users/%CN%/ </p> <p>/ReportStatus.vsp </p> </td> 
   <td colname="col4"> <p>보고서 컴퓨터는 ReportStatus.vsp 파일에 쓰는 기능이 추가되어 전원 사용자와 동일한 액세스가 <span class="filepath"> 가능합니다</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

**액세스 제어 구성**

액세스 제어 그룹을 정의할 때 이 컴퓨터에 액세스해야 하는 모든 시스템 관리자, 사용자, 클러스터 서버 및 보고서 서버 사용자를 포함해야 합니다 [!DNL Insight Server] . IP 주소 또는 일반 이름 또는 조직과 같은 SSL 인증서 정보를 사용하여 액세스를 부여할 수 있습니다.

>[!NOTE]
>
>파일을 [!DNL Access Control.cfg] 변경하면 [!DNL Insight Server]기존 연결이 모두 종료되고 다시 연결해야 합니다. 업데이트된 [!DNL Access Control.cfg] 파일의 권한에 대해 연결이 확인됩니다. Servers Manager 인터페이스에서 연결이 종료되고 다른 모든 사용자와 다시 강제로 연결되었기 때문에 아이콘이 일시적으로 빨간색으로 표시된 다음 다시 녹색으로 바뀝니다. [!DNL Insight Server]

1. > [!DNL Admin] 탭 [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** 에서 축소판을 클릭하여 서버 관리자 작업 영역을 엽니다.

1. 구성할 아이콘 [!DNL Insight Server] 을 마우스 오른쪽 단추로 클릭하고 클릭합니다 **[!UICONTROL Files]**.

1. 에서 [!DNL Server Files Manager]을 클릭하여 콘텐츠 **[!UICONTROL Access Control]** 를 봅니다. 이 디렉터리 내에 [!DNL Access Control.cfg] 파일이 있습니다.

1. 에 대한 *서버 이름* 열의 확인 표시를 마우스 오른쪽 단추로 [!DNL Access Control.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 에 대한 열에 확인 표시가 [!DNL Temp] 나타납니다 [!DNL Access Control.cfg].

1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** 를 **[!UICONTROL in Workstation]**&#x200B;클릭합니다.

1. 창에서 [!DNL Access Control.cfg] 을 클릭하여 내용 **[!UICONTROL Access Control Groups]** 을 봅니다.

   ![](assets/access_ctrl_cfg.png)

1. 새 액세스 제어 그룹을 추가하려면:

   1. 마우스 오른쪽 단추 **[!UICONTROL Access Control Groups]** 를 클릭하고 **[!UICONTROL Add new]** > 을 **[!UICONTROL Group]**&#x200B;클릭합니다.

   1. 마우스 오른쪽 단추 **[!UICONTROL Members]** 를 클릭하고 **[!UICONTROL Add new]** > 을 **[!UICONTROL Member]**&#x200B;클릭합니다.

      기본 그룹의 구성원은 사전 정의되지 않습니다. 기본적으로 관리자 액세스 권한은 127.0.0.1(로컬 호스트)에 부여되며 IP:*에 대한 액세스 권한이 [!DNL Sensor] 부여됩니다. 다른 모든 액세스 제어 그룹 구성원을 정의해야 합니다.

   1. 매개 변수를 완료합니다.

1. 기존 액세스 제어 그룹에 새 구성원을 추가하려면:

   1. 해당 액세스 제어 그룹 **[!UICONTROL Members]** 아래에서 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL Add new]** > 를 **[!UICONTROL Member]**&#x200B;클릭합니다.

1. 창 맨 위에서 마우스 오른쪽 단추 **[!UICONTROL (modified)]** 를 클릭한 다음 을 클릭하여 파일을 저장합니다 **[!UICONTROL Save]**.

1. 컴퓨터에 대한 변경 내용을 저장하려면 [!DNL Insight Server] 시스템 [!DNL Server Files Manager]에서 열에 있는 확인 표시 [!DNL Access Control.cfg] 를 마우스 오른쪽 단추로 클릭한 다음 로컬에서 [!DNL Temp] &lt; **[!UICONTROL Save to]** > ***[!UICONTROL server name]***&#x200B;를 클릭합니다.

