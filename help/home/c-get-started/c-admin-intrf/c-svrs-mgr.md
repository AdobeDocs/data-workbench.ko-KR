---
description: 시스템 관리자가 사용하는 기본 도구는 서버 관리자입니다.
solution: Analytics
title: 서버 관리자
topic: Data workbench
uuid: 96c8f060-ffd4-46b9-b039-b2ac024400b6
translation-type: tm+mt
source-git-commit: 948c6dd04819e939b45745db573a53c8be51ce37

---


# 서버 관리자{#servers-manager}

시스템 관리자가 사용하는 기본 도구는 서버 관리자입니다.

전체 시스템 상태를 확인하고 시스템 구성, 파일 관리 및 오류 모니터링 기능을 수행하기 위한 기본 인터페이스입니다.

서버 관리자는 각 데이터 워크벤치 서버 및 시스템의 [!DNL Sensor] 설치에 대해 색상이 지정된 점(노드)을 표시하고 각 설치에 대한 시스템 상태를 한 눈에 표시합니다. Data Workbench 설치에 대한 노드도 표시됩니다.

녹색 노드는 활성 연결을 나타내고, 빨간색 노드는 비활성화되거나 액세스할 수 없는 연결을 나타내고, 회색 노드는 상태가 확인되지 않은 연결을 나타냅니다.

![](assets/vis_SysStat_RedGreenDots.png)

노드를 마우스 오른쪽 단추로 클릭하면 연결 구성 요소에 대한 정보가 표시되고 관련 메뉴에 액세스할 수 있습니다.

다음 표에서는 데이터 워크벤치, 데이터 워크벤치 서버(클러스터의 마스터 데이터 워크벤치 서버 포함)에 대한 노드를 마우스 오른쪽 단추로 누를 때 제공된 정보를 [!DNL Sensor]설명합니다.

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
   <td colname="col2"> <p>제품 이름, 버전 및 빌드 번호 </p> <p>예:데이터 워크벤치 5.3(00000001) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>주소 </p> </td> 
   <td colname="col2"> <p>데이터 워크벤치 컴퓨터의 IP 주소입니다. </p> <p>예: 100.0.0.1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>구성 </p> </td> 
   <td colname="col2"> <p>데이터 워크벤치의 <span class="keyword"> 구성 파일에 대한 </span> 링크. 구성 <span class="uicontrol"> &gt; </span> Insight <span class="uicontrol"> .cfg를 </span> 클릭하여 데이터 워크벤치 구성 창을 표시합니다. 이 창에서 변경한 후 저장하는 내용은 Data Workbench 설치 디렉토리의 <span class="filepath"> Insight.cfg </span> 파일에 반영됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제품 </p> </td> 
   <td colname="col2"> <p>제품 이름, 버전 및 빌드 번호 </p> <p>예:데이터 워크벤치 서버 5.3(00000001) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>CN </p> </td> 
   <td colname="col2"> <p>데이터 워크벤치 서버 컴퓨터의 일반 이름입니다. </p> <p>예: <span class="filepath"> myserver1.mycompany.com </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>주소 </p> </td> 
   <td colname="col2"> <p>컴퓨터의 주소 파일과 Insight.cfg 파일의 네트워크 위치 매개 변수에 구성된 서버의 IP 주소 또는 정규화된 도메인 <span class="filepath"></span> 이름입니다. </p> <p>예: 100.0.0.1 </p> <p>주소 파일에 대한 자세한 내용은 서버 제품 <i>설치 및 관리 안내서를 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>상태 </p> </td> 
   <td colname="col2"> <p>데이터 워크벤치 서버의 현재 상태입니다. 이 필드는 데이터 워크벤치 서버가 정상적으로 실행될 때 확인을 표시합니다. 오류가 발생하고 데이터 워크벤치 서버 노드가 빨간색이면 필드에 오류가 표시됩니다(예: "403 금지"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>세부 상태 </p> </td> 
   <td colname="col2"> <p>데이터 워크벤치 서버 세부 <span class="keyword"> 상태 </span> 인터페이스에 대한 링크로서, <span class="wintitle"> </span> 오류 또는 데이터 워크벤치 서버의 기타 문제를 해결하는 데 유용합니다. </p> <p>자세한 내용은 자세한 상태 <a href="../../../home/c-get-started/c-admin-intrf/c-det-stat-interf.md"> 인터페이스를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>원격 데스크톱 </p> </td> 
   <td colname="col2"> <p>Data Workbench <span class="wintitle"> 서버 컴퓨터에 대한 원격 데스크톱 </span> 세션을 엽니다. </p> <p>자세한 내용은 원격 데스크톱 <a href="../../../home/c-get-started/c-admin-intrf/t-rmt-dsktp-opt.md#task-dc0bdb4630474a17af67b931bc22d9ef"> 옵션을 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>서버 파일 </p> </td> 
   <td colname="col2"> <p>Data Workbench <span class="wintitle"> 서버 설치 디렉토리에 디렉토리 및 파일을 </span>표시하는 Server Files Manager에 대한 링크. </p> <p>자세한 내용은 서버 파일 <a href="../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4"> 관리자를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>서버 모니터 </p> </td> 
   <td colname="col2"> <p>서버 모니터 <span class="wintitle"> 인터페이스에 대한 </span> 링크로서 성능 매개 변수를 문제 해결하거나 추적하는 데 유용합니다. </p> <p>자세한 내용은 서버 모니터 <a href="../../../home/c-get-started/c-admin-intrf/c-svr-mtr-intfc.md#concept-3bea7441de20409585e63060d5489f45"> 인터페이스를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>관련 서버 </p> </td> 
   <td colname="col2"> <p>데이터 워크벤치 서버 클러스터에만 해당됩니다. </p> <p>마스터 데이터 워크벤치 서버의 *. <span class="filepath"> address </span> 파일에 나열된 컴퓨터의 공통 이름을 나열하는 메뉴입니다. 이 목록에는 일반적으로 클러스터의 모든 처리 <span class="keyword"> 데이터 워크벤치 서버가 </span> 포함됩니다. 이 메뉴는 데이터 워크벤치에 마스터 데이터 워크벤치 서버의 *. <span class="filepath"> address </span> 파일의 복사본이 있는 경우에만 나타납니다. </p> <p>[관련 서버] <span class="uicontrol"> 를 클릭하면 </span>다음 중 하나를 클릭할 수 있습니다. 
     <ul id="ul_3B28B8579B1945FD80669EDFDFDA84A6"> 
      <li id="li_90094B46CB304C179136BB75FF0D6DBD"> <span class="uicontrol"> 서버 모니터 </span>목록 - 모든 관련 서버에 대한 <span class="wintitle"> 서버 모니터 </span> 인터페이스 목록 세부 사항을 표시합니다. </li> 
      <li id="li_CD6FF5BB52874ABCB536C2DE2376587A">해당 특정 서버에 대해 다음 중 하나를 열 수 있는 컨텍스트 메뉴를 표시하는 데이터 워크벤치 서버의 공통 이름입니다. 
       <ul id="ul_928510D1DE68471583F2EE7547AEB824"> 
        <li id="li_8399338137354A59B9B4D24AF7EEE868"> <span class="uicontrol"> 세부 상태 </span>. 자세한 <a href="../../../home/c-get-started/c-admin-intrf/c-det-stat-interf.md"> 상태 인터페이스를 </a>참조하십시오. </li> 
        <li id="li_0FE569C56B3F4583BC1F3DF3B4F55765"> <span class="uicontrol"> 원격 데스크톱 </span>. 원격 <a href="../../../home/c-get-started/c-admin-intrf/t-rmt-dsktp-opt.md#task-dc0bdb4630474a17af67b931bc22d9ef"> 데스크톱 옵션을 </a>참조하십시오. </li> 
        <li id="li_2B6F8419CB5945C9B411F6A7C2C859FF"> <span class="uicontrol"> 서버 파일 관리자를 </span>참조하십시오. 서버 <a href="../../../home/c-get-started/c-admin-intrf/c-svr-files-mgr.md#concept-73a0808487c8424285ae7302f53bc5f4"> 파일 관리자를 </a>참조하십시오. </li> 
        <li id="li_F22F974EB4DE4F0F93623AE98C7DCEBC"> <span class="uicontrol"> 서버 모니터 </span>. 서버 <a href="../../../home/c-get-started/c-admin-intrf/c-svr-mtr-intfc.md#concept-3bea7441de20409585e63060d5489f45"> 모니터 인터페이스를 </a>참조하십시오. </li> 
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
   <td colname="col2"> <p>제품 이름, 버전 및 빌드 번호 </p> <p>예:Sensor 3.76;J3.67 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID </p> </td> 
   <td colname="col2"> 이 <span class="wintitle"> 설치의 Sensor </span> 구성 파일에 지정된 <span class="wintitle"> 센서 </span> ID. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IP </p> </td> 
   <td colname="col2"> <p>센서가 설치된 웹 또는 응용 프로그램 서버의 <span class="wintitle"> IP </span> 주소입니다. </p> <p>예: 100.0.0.1 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>PID </p> </td> 
   <td colname="col2"> <p>운영 체제에서 할당한 프로세스 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL </p> </td> 
   <td colname="col2"> <p>센서와 <span class="wintitle"> 데이터 워크벤치 </span> 서버가 SSL을 사용하여 통신하는지 여부. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>시간 </p> </td> 
   <td colname="col2"> <p>시간 (HH:MM:SS) 센서가 <span class="wintitle"> 데이터 워크벤치 서버와 </span> 마지막으로 연결했습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
