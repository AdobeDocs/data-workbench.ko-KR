---
description: 시스템 관리자가 사용하는 기본 도구는 서버 관리자입니다.
title: 서버 관리자
uuid: 96c8f060-ffd4-46b9-b039-b2ac024400b6
exl-id: e8b22d9f-3f1b-4a97-942a-85786bd3c547
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 3%

---

# 서버 관리자{#servers-manager}

{{eol}}

시스템 관리자가 사용하는 기본 도구는 서버 관리자입니다.

전체 시스템 상태를 확인하고 시스템 구성, 파일 관리 및 오류 모니터링 기능을 수행하는 기본 인터페이스입니다.

서버 관리자는 각 Data Workbench 서버에 대해 색칠된 점(노드)을 표시하고 [!DNL Sensor] 시스템에 설치하고 각 설치에 대한 시스템 상태를 한 눈에 확인합니다. Data Workbench 설치 노드도 표시됩니다.

녹색 노드는 활성 연결을 나타내고, 빨간색 노드는 비활성화되거나 액세스할 수 없는 연결을 나타내고, 회색 노드는 상태가 확인되지 않은 연결을 나타냅니다.

![](assets/vis_SysStat_RedGreenDots.png)

노드를 마우스 오른쪽 버튼으로 클릭하면 연결 구성 요소에 대한 정보가 표시되고 관련 메뉴에 액세스할 수 있습니다.

다음 표에서는 Data Workbench, Data Workbench 서버(클러스터의 마스터 Data Workbench 서버 포함)에 대한 노드를 마우스 오른쪽 단추로 누를 때 제공되는 정보에 대해 설명합니다. [!DNL Sensor].

<table id="table_C459CAAB07D34144B5BFFCCC84C2BB37"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 항목 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>제품 </p> </td> 
   <td colname="col2"> <p>제품 이름, 버전 및 빌드 번호입니다. </p> <p>예: Data Workbench 5.3 (00000001) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>주소 </p> </td> 
   <td colname="col2"> <p>Data Workbench 컴퓨터의 IP 주소입니다. </p> <p>예: 100.0.0.1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>메시지에 대한 </p> </td> 
   <td colname="col2"> <p>링크 <span class="keyword"> Data Workbench </span> 구성 파일. 클릭 <span class="uicontrol"> 구성 </span> &gt; <span class="uicontrol"> Insight.cfg </span> Data Workbench 구성 창을 표시하려면 다음을 수행하십시오. 이 창에서 작성하고 저장하는 변경 내용은 <span class="filepath"> Insight.cfg </span> 파일을 Data Workbench 설치 디렉토리에 저장합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제품 </p> </td> 
   <td colname="col2"> <p>제품 이름, 버전 및 빌드 번호입니다. </p> <p>예: Data Workbench 서버 5.3 (00000001) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>CN </p> </td> 
   <td colname="col2"> <p>Data Workbench 서버 컴퓨터의 일반 이름입니다. </p> <p>예: <span class="filepath"> myserver1.mycompany.com </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>주소 </p> </td> 
   <td colname="col2"> <p>컴퓨터의 Addresses 파일과 의 Network Location 매개 변수에 구성된 서버의 IP 주소 또는 정규화된 도메인 이름 <span class="filepath"> Insight.cfg </span> 파일. </p> <p>예: 100.0.0.1 </p> <p>주소 파일에 대한 자세한 내용은 <i>서버 제품 설치 및 관리 안내서</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>상태 </p> </td> 
   <td colname="col2"> <p>Data Workbench 서버의 현재 상태입니다. 이 필드는 Data Workbench 서버가 정상적으로 실행 중일 때 확인을 표시합니다. 오류가 발생하여 Data Workbench 서버 노드가 빨간색으로 표시되는 경우 필드에 오류가 표시됩니다(예: "403 금지됨"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>자세한 상태 </p> </td> 
   <td colname="col2"> <p>링크 <span class="keyword"> Data Workbench 서버 </span> <span class="wintitle"> 자세한 상태 </span> 인터페이스. Data Workbench 서버의 오류 또는 기타 문제를 해결하는 데 유용합니다. </p> <p>자세한 내용은 <a href="../../../home/c-get-started/c-admin-intrf/c-det-stat-interf.md"> 자세한 상태 인터페이스</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>원격 데스크톱 </p> </td> 
   <td colname="col2"> <p>를 엽니다. <span class="wintitle"> 원격 데스크톱 </span> Data Workbench 서버 컴퓨터에 대한 세션입니다. </p> <p>자세한 내용은 <a href="../../../home/c-get-started/c-admin-intrf/t-rmt-dsktp-opt.md#task-dc0bdb4630474a17af67b931bc22d9ef"> 원격 데스크톱 옵션 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>서버 파일 </p> </td> 
   <td colname="col2"> <p>링크 <span class="wintitle"> 서버 파일 관리자 </span>- Data Workbench 서버 설치 디렉토리에 디렉토리와 파일을 표시합니다. </p> <p>자세한 내용은 <a href="../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4"> 서버 파일 관리자 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>서버 모니터 </p> </td> 
   <td colname="col2"> <p>링크 <span class="wintitle"> 서버 모니터 </span> 인터페이스. 성능 매개 변수의 문제 해결 또는 추적에 유용합니다. </p> <p>자세한 내용은 <a href="../../../home/c-get-started/c-admin-intrf/c-svr-mtr-intfc.md#concept-3bea7441de20409585e63060d5489f45"> 서버 모니터 인터페이스 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>관련 서버 </p> </td> 
   <td colname="col2"> <p>Data Workbench 서버 클러스터의 경우에만 해당됩니다. </p> <p>마스터에 나열된 컴퓨터의 공통 이름을 나열하는 메뉴 <span class="filepath"> Data Workbench 서버의 *.address </span> 파일. 이 목록에는 보통 모든 처리가 포함됩니다 <span class="keyword"> Data Workbench 서버 </span> 입니다. 이 메뉴는 Data Workbench에 마스터 사본이 있는 경우에만 나타납니다 <span class="filepath"> Data Workbench 서버의 *.address </span> 파일. </p> <p>를 클릭하면 <span class="uicontrol"> 관련 서버 </span>를 클릭하거나 다음 중 하나를 클릭할 수 있습니다. 
     <ul id="ul_3B28B8579B1945FD80669EDFDFDA84A6"> 
      <li id="li_90094B46CB304C179136BB75FF0D6DBD"> <span class="uicontrol"> 서버 모니터 목록 </span>: <span class="wintitle"> 서버 모니터 </span> 모든 관련 서버에 대한 인터페이스 목록 세부 정보 </li> 
      <li id="li_CD6FF5BB52874ABCB536C2DE2376587A">특정 서버에 대해 다음 중 하나를 열 수 있는 컨텍스트 메뉴를 표시하는 Data Workbench 서버의 일반 이름입니다. 
       <ul id="ul_928510D1DE68471583F2EE7547AEB824"> 
        <li id="li_8399338137354A59B9B4D24AF7EEE868"> <span class="uicontrol"> 자세한 상태 </span>. 자세한 내용은 <a href="../../../home/c-get-started/c-admin-intrf/c-det-stat-interf.md"> 자세한 상태 인터페이스 </a>. </li> 
        <li id="li_0FE569C56B3F4583BC1F3DF3B4F55765"> <span class="uicontrol"> 원격 데스크톱 </span>. 자세한 내용은 <a href="../../../home/c-get-started/c-admin-intrf/t-rmt-dsktp-opt.md#task-dc0bdb4630474a17af67b931bc22d9ef"> 원격 데스크톱 옵션 </a>. </li> 
        <li id="li_2B6F8419CB5945C9B411F6A7C2C859FF"> <span class="uicontrol"> 서버 파일 관리자 </span>. 자세한 내용은 <a href="../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4"> 서버 파일 관리자 </a>. </li> 
        <li id="li_F22F974EB4DE4F0F93623AE98C7DCEBC"> <span class="uicontrol"> 서버 모니터 </span>. 자세한 내용은 <a href="../../../home/c-get-started/c-admin-intrf/c-svr-mtr-intfc.md#concept-3bea7441de20409585e63060d5489f45"> 서버 모니터 인터페이스 </a>. </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_5BFA0AFE2D9A4337BF04343879DAD03B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 항목 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>제품 </p> </td> 
   <td colname="col2"> <p>제품 이름, 버전 및 빌드 번호입니다. </p> <p>예: Sensor 3.76; J3.67 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID </p> </td> 
   <td colname="col2"> 다음 <span class="wintitle"> Sensor </span> 에 지정된 ID <span class="wintitle"> Sensor </span> 이 설치에 대한 구성 파일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IP </p> </td> 
   <td colname="col2"> <p>웹 또는 응용 프로그램 서버의 IP 주소 <span class="wintitle"> Sensor </span> 가 설치되어 있습니다. </p> <p>예: 100.0.0.1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PID </p> </td> 
   <td colname="col2"> <p>운영 체제에서 지정한 프로세스 ID입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL </p> </td> 
   <td colname="col2"> <p>다음 <span class="wintitle"> Sensor </span> 및 Data Workbench 서버는 SSL을 사용하여 통신합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>시간 </p> </td> 
   <td colname="col2"> <p>시간 (HH:MM:SS) <span class="wintitle"> Sensor </span> 마지막으로 Data Workbench 서버와의 연결을 설정했습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
