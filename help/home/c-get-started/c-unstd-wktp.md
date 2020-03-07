---
description: 이 워크맨에서는 모든 작업 영역과 보고서를 구성하고 액세스할 수 있습니다.
solution: Analytics
title: 작업 영역
topic: Data workbench
uuid: ae6e475c-fc91-4c76-883b-894c9eb2933c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 작업 영역{#worktops}

이 워크맨에서는 모든 작업 영역과 보고서를 구성하고 액세스할 수 있습니다.

대부분의 경우, 데이터 워크벤치를 연 직후 [!DNL Worktop] 이 표시됩니다. 사이드바와 탭 방식의 인터페이스가 포함되어 [!DNL Worktop] 있습니다. 또한 사이드바를 사용하면 시각화를 추가하고 정기적으로 사용되는 기능에 액세스할 수 있습니다.

**Worktop**

![](assets/client-wktp.png)

또한 [!DNL Worktop] 새 작업 영역 및 업데이트된 보고서를 만들어 저장할 수 있을 뿐만 아니라 다른 사람이 액세스할 수 있도록 작업 영역 및 보고서를 데이터 워크벤치 서버에 게시할 수 있습니다.

아래 [!DNL Worktop] 요소 표는 각 요소에 대해 설명합니다 [!DNL Worktop].

<table id="table_CB1DBB7DE8E2450A8C57601531BBD689"> 
 <tbody> 
  <tr> 
   <td colname="col1"> 사이드바 </td> 
   <td colname="col2"> <p>사이드바는 작업 영역에 대한 컨텍스트와 컨트롤, 작업 영역의 현재 상태에 대한 인식 및 정기적으로 사용되는 기능에 대한 액세스를 제공합니다. 세로 막대에서 다음 기능을 사용할 수 있습니다. </p> <p> <b>연결:</b> 온라인 상태를 보여주는 상태 표시기. 연결 상태를 클릭하여 온라인 작업을 활성화하거나 비활성화합니다 <span class="wintitle"></span>. 오프라인 <a href="../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54"> 및 온라인 작업을 참조하십시오</a>. </p> <p> <b>프로필:</b> 사용 중인 현재 프로필의 표시기. </p> <p> <b>기준:프로필의 </b>데이터 세트에 데이터가 얼마나 최신 상태인지 보여주는 상태 표시기입니다. 이 데이터는 DPU 서버에서 다운로드 및 처리되며, 이는 온라인으로 작업하는 경우에만 발생할 수 있습니다. </p> <p> <b>쿼리/샘플 신뢰도:</b> 쿼리 완료 지표. 상태가 100%로 쿼리되면 모든 데이터가 쿼리되었습니다. </p> <p> <b>추가:</b> 패널, 범례 및 표와 같은 시각화를 세로 막대에 추가할 수 있습니다. 사이드바에 <a href="../../home/c-get-started/c-config-sidebar.md#section-666f70a405db4f8d8eaffa567ffcac06"> 시각화 추가를 참조하십시오</a>. </p> <p> <b>옵션:</b> 이전 세로 막대 설정으로 되돌아가서 세로 막대를 자동으로 숨길 수 있습니다. </p> <p>사이드바 설정은 데이터 워크벤치를 닫을 때 <span class="filepath"> sidebar.vw</span> 파일에 저장됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>탭 및 하위 탭 또는 드롭다운 하위 디렉토리(표시되지 않음) </p> </td> 
   <td colname="col2"> <p>작업 <span class="wintitle"> 상단에</span> 나타나는 각 탭은 Data Workbench <i>설치 디렉토리 내의 탭의</i>작업 프로필 이름<i>\Workspaces\</i> 탭 이름폴더에 해당하며 대시보드, 활동, 획득, 방문자 등과 같은 특정 유형의 정보를 나타냅니다. 탭 이름 폴더의 하위 폴더는 기본적으로 하위 탭으로 표시되지만 하위 디렉터리로 표시될 수도 있습니다. 작업 <a href="../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-wktp-tabs/c-cstm-wktp-tabs.md#concept-0f1e6061b03949199326dc6df71a52bc"> 상단 탭 사용자 지정을 참조하십시오</a>. </p> <p> <p>참고: 각 데이터 워크벤치 프로파일은 표준 탭 세트로 제공됩니다. 구현은 완전히 사용자 정의할 수 있으므로 표시되는 작업 영역(및 탭)은 이 안내서에 설명된 작업 영역과 다를 수 있습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프로필 상태 </td> 
   <td colname="col2"> 데이터 워크벤치 서버에 대한 연결 상태와 현재 로드된 프로필의 이름을 제공합니다. 프로필의 데이터 세트에 있는 데이터의 기준 날짜 및 시간이 온라인 지표 아래에 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최소화, 최대화, 닫기 </td> 
   <td colname="col2"> 표준 Windows 기능. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 축소판 </td> 
   <td colname="col2"> <p>축소판은 작업 영역에 표시되는 작업 영역의 <span class="wintitle"> 스냅샷입니다</span>. 작업 영역을 저장할 때마다 새 스냅샷이 생성됩니다. 축소판을 사용하면 작업대에서 특정 작업 영역을 신속하게 식별할 수 <span class="wintitle"> 있습니다</span>. </p> <p>작업 영역을 열려면 축소판을 클릭합니다. </p> <p> <p>참고: 각 데이터 워크벤치 프로파일은 표준 작업 영역 세트와 함께 제공됩니다. 구현은 완전히 사용자 정의할 수 있으므로 표시되는 작업 영역(및 축소판)은 이 안내서에 설명된 작업 영역과 다를 수 있습니다. </p> </p> <p>작업 영역에 대한 자세한 내용은 사이드바 <a href="../../home/c-get-started/c-config-sidebar.md#concept-41db771b302e43018e5a9daa40b397e6"> 구성을 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 오류 메시지 </td> 
   <td colname="col2"> <p>오류 메시지는 상태 아래에 빨간색으로 표시됩니다. 상태 코드 설명은 http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html을 참조하십시오 <a href="http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html" format="http" scope="external"></a>. </p> <p>예:403_금지. </p> </td> 
  </tr> 
 </tbody> 
</table>

