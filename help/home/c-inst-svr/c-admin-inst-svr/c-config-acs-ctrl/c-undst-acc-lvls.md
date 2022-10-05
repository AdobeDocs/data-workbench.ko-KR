---
description: 액세스 수준에서는 사용자 그룹이 읽거나 수정할 수 있는 시스템의 URI를 설명합니다.
title: 액세스 수준 이해
uuid: e9091ae1-9a34-4e00-a928-20d04119ee9e
exl-id: 64e2dc39-1ca1-425b-bec7-acb10a8819c0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 3%

---

# 액세스 수준 이해{#understanding-access-levels}

{{eol}}

액세스 수준에서는 사용자 그룹이 읽거나 수정할 수 있는 시스템의 URI를 설명합니다.

다음 지침에 따라 조직의 사용자에 대해 원하는 액세스 수준을 정의합니다.

* 후행 슬래시 문자가 없는 특정 URI는 해당 URI에만 대한 액세스를 제한합니다. 예, [!DNL /Components/Communications.cfg] 에 대한 액세스 권한 제공 [!DNL Communications.cfg]파일 전용.

* 디렉토리를 지정하는 후행 슬래시(/)는 그룹 구성원에게 해당 문자열로 시작되는 모든 URI에 대한 액세스 권한을 제공합니다. 예를 들어 /Profiles/ 는 전체 Profiles 디렉토리에 대한 액세스를 제공합니다.
* 후행 달러 기호($)는 디렉터리인 경우에도 정확한 URI에 대한 액세스를 제한합니다. 예를 들어 /Profiles/$ 은 기본 Profiles 디렉토리를 읽을 수 있지만 해당 디렉토리 내의 파일을 읽을 수는 없습니다.

   특정 파일에 액세스하려면 후행 $ 를 사용할 필요가 없습니다.

   예, [!DNL /Components/Communications.cfg] 및 [!DNL /Components/Communications.cfg$] 동일한 액세스 권한을 제공합니다.

* 퍼센트 기호(%)는 CN(일반 이름)과 함께 사용하여 액세스를 허용할 수 있습니다. 예를 들어 /Users/%CN%/ 에서는 [!DNL Insight] 사용자. 이 구문은 URI에서 한 번만 사용할 수 있습니다.

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
   <td colname="col4"> <p>모든 파일에 대한 읽기 및 쓰기 액세스 <span class="keyword"> Insight Server</span> 디렉토리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>센서 </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>/SensorInit.vsp </p> <p>/Submit.vsp </p> </td> 
   <td colname="col4"> <p>다음 두 파일에 대한 읽기 및 쓰기 액세스 권한 <span class="wintitle"> 센서</span> 와 통신하는 데 사용 <span class="keyword"> Insight Server</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용자 참조 </p> </td> 
   <td colname="col2"> <p>/프로필/ </p> <p>/상태/ </p> <p>/Software/ </p> <p>/Addresses/ </p> <p>/사용자 참조/$ </p> </td> 
   <td colname="col3"> /Users/%CN%/ </td> 
   <td colname="col4"> <p>SSL 인증서 공통 이름과 일치하는 사용자 디렉토리에 대한 읽기 및 쓰기 액세스 <span class="keyword"> 인사이트</span> 사용자. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>고급 사용자 </p> </td> 
   <td colname="col2"> <p>/프로필/$ </p> <p>/상태/ </p> <p>/Software/ </p> <p>/Addresses/ </p> <p>/사용자 참조/$ </p> </td> 
   <td colname="col3"> <p>/프로필/ </p> <p>/Users/%CN%/ </p> </td> 
   <td colname="col4"> <p>Power Users는 Profiles 디렉터리에 쓸 수 있는 기능이 추가되어 Users와 동일한 액세스가 허용됩니다. 이러한 사용자는 프로필을 편집하고 다른 사용자에 대해 변경 사항을 자동으로 업데이트할 수 있습니다 <span class="keyword"> 인사이트</span> 새로 정의된 작업 공간을 배포할 때와 같은 사용자. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>클러스터 서버 </p> </td> 
   <td colname="col2"> <p>/처리 서버용 구성 요소/ </p> <p>/Addresses/ </p> <p>/프로필/ </p> <p>/조회/ </p> <p>/액세스 제어/ </p> <p>/Bin/ </p> <p>/로그/ </p> </td> 
   <td colname="col3"> <p>/Cluster/ </p> </td> 
   <td colname="col4"> <p>클러스터 디렉터리에 대한 읽기 및 쓰기 액세스 권한을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보고서 서버 </p> </td> 
   <td colname="col2"> <p>/프로필/$ </p> <p>/상태/ </p> <p>/Software/ </p> <p>/Addresses/ </p> <p>/사용자 참조/$ </p> </td> 
   <td colname="col3"> <p>/프로필/ </p> <p>/Users/%CN%/ </p> <p>/ReportStatus.vsp </p> </td> 
   <td colname="col4"> <p>보고서 시스템은 고급 사용자와 동일한 액세스 권한을 가질 수 있으며 여기에 쓸 수 있는 기능이 추가되었습니다 <span class="filepath"> ReportStatus.vsp</span> 파일. </p> </td> 
  </tr> 
 </tbody> 
</table>

**액세스 제어를 구성하려면**

액세스 제어 그룹을 정의할 때 이 그룹에 대한 액세스 권한이 필요한 모든 시스템 관리자, 사용자, 클러스터 서버 및 보고서 서버 사용자를 포함해야 합니다 [!DNL Insight Server] 컴퓨터. 공통 이름 또는 조직과 같은 IP 주소나 SSL 인증서 정보를 사용하여 액세스 권한을 부여할 수 있습니다.

>[!NOTE]
>
>이 [!DNL Access Control.cfg] 파일 변경 [!DNL Insight Server]을 눌러 기존 모든 연결이 종료되고 다시 연결되어야 합니다. 업데이트된 사용자 권한에 대해 연결이 확인됩니다 [!DNL Access Control.cfg] 파일. 서버 관리자 인터페이스에서 [!DNL Insight Server] 연결이 끊기고 다른 사용자와 함께 다시 연결해야 하므로 아이콘이 일시적으로 빨간색 다음 다시 녹색으로 바뀝니다.

1. 설정 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 사용하여 Server Manager 작업 공간을 엽니다.

1. 아이콘을 마우스 오른쪽 단추로 클릭합니다. [!DNL Insight Server] 을(를) 구성하고 **[!UICONTROL Files]**.

1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Access Control]** 콘텐츠를 보려면 클릭하십시오. 다음 [!DNL Access Control.cfg] 파일이 이 디렉터리 내에 있습니다.

1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. *서버 이름* 열 [!DNL Access Control.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL Access Control.cfg].

1. 에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**.

1. 에서 [!DNL Access Control.cfg] 창 **[!UICONTROL Access Control Groups]** 콘텐츠를 보려면 클릭하십시오.

   ![](assets/access_ctrl_cfg.png)

1. 새 액세스 제어 그룹을 추가하려면 다음을 수행합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Access Control Groups]** 을(를) 클릭합니다. **[!UICONTROL Add new]** > **[!UICONTROL Group]**.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Members]** 을(를) 클릭합니다. **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

      기본 그룹의 구성원이 미리 정의되어 있지 않습니다. 기본적으로 관리자 액세스 권한은 127.0.0.1(로컬 호스트)에 부여되며, [!DNL Sensor] 액세스 권한은 IP에 부여됩니다.&#42;. 다른 모든 액세스 제어 그룹 구성원을 정의해야 합니다.

   1. 매개 변수를 완료합니다.

1. 기존 액세스 제어 그룹에 새 구성원을 추가하려면

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Members]** 적절한 액세스 제어 그룹 아래에서 **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

1. 마우스 오른쪽 단추를 클릭하여 파일을 저장합니다 **[!UICONTROL (modified)]** 창 상단에서 을 클릭한 다음 **[!UICONTROL Save]**.

1. 로컬에서 변경한 내용을 저장하려면 [!DNL Insight Server] 시스템, [!DNL Server Files Manager]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Access Control.cfg] 에서 [!DNL Temp] 열을 누른 다음 **[!UICONTROL Save to]** *&lt;**[!UICONTROL server name]**>*.
