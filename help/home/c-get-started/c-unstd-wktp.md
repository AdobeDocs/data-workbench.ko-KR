---
description: Worktop은 모든 작업 공간 및 보고서를 구성하고 액세스하는 위치입니다.
title: Worktop
uuid: ae6e475c-fc91-4c76-883b-894c9eb2933c
exl-id: e714ca25-5e94-408a-9d4e-6e1c13e2a3ef
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Worktop{#worktops}

Worktop은 모든 작업 공간 및 보고서를 구성하고 액세스하는 위치입니다.

대부분의 경우 Data Workbench을 연 직후에 [!DNL Worktop]이 표시됩니다. [!DNL Worktop] 의 기능에는 사이드바 및 탭 인터페이스가 포함됩니다. 또한 사이드바를 사용하면 시각화를 추가하고 정기적으로 사용되는 기능에 액세스할 수 있습니다.

**Worktop**

![](assets/client-wktp.png)

또한 [!DNL Worktop]을 사용하면 새 작업 공간과 업데이트된 보고서를 만들고 저장할 수 있을 뿐만 아니라, 다른 사용자가 액세스할 수 있도록 작업 공간 및 보고서를 Data Workbench 서버에 게시할 수도 있습니다.

아래의 [!DNL Worktop] 요소 테이블은 [!DNL Worktop]의 각 요소를 설명합니다.

<table id="table_CB1DBB7DE8E2450A8C57601531BBD689"> 
 <tbody> 
  <tr> 
   <td colname="col1"> 사이드바 </td> 
   <td colname="col2"> <p>사이드바는 작업 공간에 대한 컨텍스트 및 제어뿐만 아니라 작업 공간의 현재 상태에 대한 인식 및 정기적으로 사용되는 기능에 대한 액세스를 제공합니다. 사이드바에서 다음 기능을 사용할 수 있습니다. </p> <p> <b>연결:</b> 온라인 상태를 보여주는 상태 표시기입니다. 연결 상태를 클릭하여 <span class="wintitle"> Work Online</span>을 활성화하거나 비활성화합니다. <a href="../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54"> Working Offline and Online</a> 을 참조하십시오. </p> <p> <b>프로필: </b> 사용 중인 현재 프로필의 표시기입니다. </p> <p> <b>기준: </b>프로필의 데이터 세트에 데이터가 얼마나 최신 상태인지를 보여주는 상태 표시기입니다. 이 데이터는 DPU 서버에서 다운로드 및 처리되며, 온라인으로 작업하는 경우에만 발생할 수 있습니다. </p> <p> <b>쿼리/샘플 신뢰도:</b>  쿼리 완료의 지표입니다. 상태가 100%로 쿼리되면 모든 데이터가 쿼리되었습니다. </p> <p> <b>추가:</b> 패널, 범례 및 테이블과 같은 시각화를 사이드바에 추가할 수 있습니다. <a href="../../home/c-get-started/c-config-sidebar.md#section-666f70a405db4f8d8eaffa567ffcac06"> 사이드바에 시각화 추가</a>를 참조하십시오. </p> <p> <b>옵션: </b> 이전 사이드바 설정으로 되돌아가서 사이드바를 자동으로 숨길 수 있습니다. </p> <p>사이드바 설정은 Data Workbench을 닫을 때 <span class="filepath"> 사이드바.vw</span> 파일에 저장됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>탭 및 하위 탭 또는 드롭다운 하위 디렉토리(표시되지 않음) </p> </td> 
   <td colname="col2"> <p><span class="wintitle"> Worktop</span>에 나타나는 각 탭은 Data Workbench 설치 디렉토리 내의 탭의 <i>작업 프로필 이름</i>\Workspaces\<i>탭 이름</i> 폴더에 해당되며 대시보드, 활동, 획득, 방문자 등과 같은 특정 유형의 정보를 나타냅니다. 탭 이름 폴더의 하위 폴더는 기본적으로 하위 탭으로 표시되지만 하위 디렉터리로 표시될 수도 있습니다. <a href="../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-wktp-tabs/c-cstm-wktp-tabs.md#concept-0f1e6061b03949199326dc6df71a52bc"> worktop 탭 사용자 정의</a> 를 참조하십시오. </p> <p> <p>참고: 각 Data Workbench 프로필은 표준 탭 세트와 함께 제공됩니다. 구현을 완전히 사용자 지정할 수 있으므로 표시되는 작업 공간(및 탭)은 이 안내서에 설명된 작업 공간과 다를 수 있습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프로필 상태 </td> 
   <td colname="col2"> Data Workbench 서버에 연결 상태 및 현재 로드된 프로필의 이름을 제공합니다. 프로필의 데이터 세트에 있는 데이터의 기준 날짜 및 시간이 온라인 지표 아래에 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최소화, 최대화, 닫기 </td> 
   <td colname="col2"> 표준 Windows 함수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 축소판 그림 </td> 
   <td colname="col2"> <p>축소판은 <span class="wintitle"> Worktop</span>에 나타나는 작업 공간의 스냅샷입니다. 작업 공간을 저장할 때마다 새 스냅샷이 생성됩니다. 미리 보기를 사용하면 <span class="wintitle"> Worktop</span>에서 특정 작업 영역을 빠르게 식별할 수 있습니다. </p> <p>작업공간을 열려면 축소판을 클릭합니다. </p> <p> <p>참고: 각 Data Workbench 프로필은 표준 작업 공간 세트와 함께 제공됩니다. 구현을 완전히 사용자 지정할 수 있으므로 표시되는 작업 공간(및 축소판)은 이 안내서에 설명된 작업 공간과 다를 수 있습니다. </p> </p> <p>작업 공간에 대한 자세한 내용은 <a href="../../home/c-get-started/c-config-sidebar.md#concept-41db771b302e43018e5a9daa40b397e6"> 사이드바 구성</a> 을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 오류 메시지 </td> 
   <td colname="col2"> <p>오류 메시지는 상태 아래에 빨간색으로 표시됩니다. 상태 코드 설명은 <a href="http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html" format="http" scope="external"> http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html</a> 를 참조하십시오. </p> <p>예:403_Forbidden </p> </td> 
  </tr> 
 </tbody> 
</table>
