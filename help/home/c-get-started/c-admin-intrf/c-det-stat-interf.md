---
description: 세부 상태 인터페이스는 데이터 워크벤치 서버 컴퓨터의 오류 또는 기타 문제를 해결하는 데 유용합니다.
solution: Analytics
title: 자세한 상태 인터페이스
topic: Data workbench
uuid: c4d375d9-431f-4b0a-ba15-b7a10501b2e2
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 자세한 상태 인터페이스{#detailed-status-interface}

세부 상태 인터페이스는 데이터 워크벤치 서버 컴퓨터의 오류 또는 기타 문제를 해결하는 데 유용합니다.

여기에는 해당 컴퓨터에서 실행되는 모든 [!DNL Transform] 프로파일 또는 데이터 워크벤치 서버의 클라이언트인 [!DNL Report] 컴퓨터가 포함됩니다. 메뉴를 통해 [!DNL Master Server] 액세스 및 [!DNL Query Server Detailed Status] 인터페이스를 사용할 수 [!DNL Admin] 있습니다. 다른 컴퓨터의 [!DNL Detailed Status] 인터페이스에 액세스하려면 [!DNL Servers Manager]에서 상태를 보려는 서버의 노드를 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Detailed Status]**. 서버 [관리자를 참조하십시오](../../../home/c-get-started/c-admin-intrf/c-svrs-mgr.md#concept-2dfff1ca5bce470a8ee854ed57cbe5ba).

데이터 워크벤치 서버에 대한 자세한 내용은 서버 제품 *설치 및 관리 안내서를 참조하십시오*.

![](assets/vis_DetailedStatus.png)

>[!NOTE]
>
>인터페이스에서 정보를 업데이트하려면 [!DNL Detailed Status] 머리글을 마우스 오른쪽 단추로 클릭하고 을 **[!UICONTROL Detailed Status]** **[!UICONTROL Refresh]**&#x200B;클릭합니다.

다음 표에는 [!DNL Detailed Status] 인터페이스를 사용하여 완료할 수 있는 작업이 나와 있습니다.

<table id="table_E685F31DCDB343F49FFA1019F2E8DA85"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 작업을 수행하려면... </th> 
   <th colname="col2" class="entry"> 방법... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>각 컴퓨터 구성 요소와 현재 상태를 표시하려면 </p> </td> 
   <td colname="col2"> <p>구성 <span class="uicontrol"> 요소 상태를 클릭합니다</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>사용 중인 컴퓨터의 메모리 양을 표시하려면 </p> </td> 
   <td colname="col2"> <p>메모리 <span class="uicontrol"> 상태</span> &gt; 주소 공간 로드를 <span class="uicontrol"> 클릭합니다</span>. </p> <p>주소 공간 로드 모니터링에 대한 자세한 내용은 서버 제품 <i>설치 및 관리 안내서를 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>컴퓨터가 /3GB 스위치를 사용하도록 구성되어 있는지 확인하려면 </p> </td> 
   <td colname="col2"> <p>[메모리 <span class="uicontrol"> 상태</span> ] &gt; [프로세스 주소 <span class="uicontrol"> 공간]을 클릭합니다</span>. </p> <p>[ <span class="wintitle"> 합계</span> ] 필드에 3000000KB가 더 많이 표시되면 컴퓨터가 /3GB 스위치를 사용하도록 구성됩니다. </p> <p>/3GB 스위치에 대한 자세한 내용은 서버 제품 <i>설치 및 관리 가이드를 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>각 차원을 저장하는 데 사용되는 디스크 공간 및 메모리와 해당 요소의 이름을 저장하는 데 사용되는 메모리 양을 모니터링합니다 </p> </td> 
   <td colname="col2"> <p>성능 <span class="uicontrol"> &gt;</span> 차원 <span class="uicontrol"> &gt;</span> 차원 <span class="uicontrol"> &gt;</span> 사용 <i>디스크<span class="uicontrol"> &gt;</span>&lt;프로필 이름&gt; </i>또는 성능 <span class="uicontrol"></span> <span class="uicontrol"></span> <span class="uicontrol"></span> <i><span class="uicontrol"></span></i>&gt; 성능 &gt; 차원 &gt; 메모리 사용 &gt; 메모리 사용 &gt; 프로필 이름&gt;을 클릭합니다. </p> <p>디스크 <span class="wintitle"> 사용량</span> 필드는 각 차원을 저장하는 데 필요한 디스크 공간(MB)의 이름과 크기를 제공합니다. Data Workbench 서버는 관련 쿼리를 완료하기 위해 모든 데이터를 읽어야 하므로 디스크 사용량 수치가 크면 쿼리 시간에 부정적인 영향을 줄 수 있습니다. 차원에 대한 디스크 사용량을 줄이면 관련 쿼리를 완료하는 데 걸리는 시간을 줄일 수 있습니다. </p> <p>메모리 <span class="wintitle"> 사용량</span> 필드는 각 차원의 요소 수와 요소 이름 목록을 저장하는 데 필요한 메모리 양을 제공합니다. Data Workbench 서버는 각 요소를 읽어야 하므로 많은 수의 요소가 쿼리 중에 사용되는 메모리 양에 부정적인 영향을 줄 수 있습니다. 차원의 요소 수를 줄이면 관련 쿼리를 완료하는 데 걸리는 시간을 줄일 수 있습니다. </p> <p>예: <code>+&nbsp;Performance
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Dimensions&nbsp;
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Disk&nbsp;Usage
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;ProfileName
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;DimensionName&nbsp;1.386&nbsp;MB
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.&nbsp;.&nbsp;.
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Memory&nbsp;Usage
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;ProfileName
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;DimensionName&nbsp;21&nbsp;elements,&nbsp;0.001&nbsp;MB
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.&nbsp;.&nbsp;.</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그 처리 및 변환 내에서 단계에 대한 CPU 사용을 모니터링하려면 </p> </td> 
   <td colname="col2"> <p>[ <span class="uicontrol"> 성능</span> ] &gt; <span class="uicontrol"> [CPU 사용량</span> 로그 처리 <span class="uicontrol"> ] &gt; [</span> 로그 처리 <i>] &gt; &lt;프로필 이름&gt;<span class="uicontrol"></span></i> <span class="uicontrol"></span> <span class="uicontrol"></span> <span class="uicontrol"></span><span class="uicontrol"></span>또는 성능 &gt; [CPU 사용] &gt; [변환]변환 &gt; [프로필 이름]을 클릭합니다. </p> <p>이러한 각 필드 세트는 로그 처리 및 변환 내의 각 단계에 대한 CPU 사용량(초)을 제공합니다. </p> <p>예: <code>+&nbsp;Performance
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;CPU&nbsp;Usage&nbsp;
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Log&nbsp;Processing
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;ProfileName&nbsp;158.9&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Built-in&nbsp;158.1&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;StageName&nbsp;13.0&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.&nbsp;.&nbsp;.
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Log&nbsp;Processing\ProfileName&nbsp;0.8&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;StageName&nbsp;0.8&nbsp;sec</code> </p> <p>쿼리를 완료하는 데 걸리는 시간은 일반적으로 모든 차원의 전체 크기에 비례합니다. 각 차원의 크기를 검토한 후 특정 차원이 유용한지 여부를 평가하고 차원의 성능 비용을 정당화할 수 있는 경우가 많습니다. 그렇지 않으면 프로필 관리자에서 차원을 삭제할 수 <span class="wintitle"> 있습니다</span>. 프로필 관리자를<a href="../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-prof-mgr.md"> 참조하십시오</a>. </p> <p>요소 이름 목록이 너무 큰 차원(즉, 128MB 이상)은 전체 주소 공간 사용이 제한에 가까이 있지 않더라도 "메모리 부족" 오류를 초래할 수 있습니다. </p> <p>또한 데이터 워크벤치 서버 클러스터를 사용하고 있지만 중앙 표준화를 사용하지 않는 경우 요소 이름 목록이 큰 차원은 전송 메모리 예산에 큰 영향을 줍니다. 중앙 표준화에 대한 자세한 내용은 데이터 세트 구성 <i>안내서를 참조하십시오</i>. 결합된 요소 이름 목록을 모두 저장하는 데 필요한 메모리 용량이 클러스터의 모든 서버에서 100MB를 초과하는 경우 쿼리 활동이 가볍더라도 "메모리 예산 초과 전송" 오류가 발생할 수 있습니다. 예를 들어, 요소 이름 목록을 저장하는 데 사용되는 각 서버에 25MB가 넘는 4개의 서버 클러스터가 있으면 오류가 발생할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그 처리 및 변환에서 보낸 시간을 모니터링하려면 </p> </td> 
   <td colname="col2"> <p>[ <span class="uicontrol"> CPU 사용량</span> ] &gt; <span class="uicontrol"> [CPU 사용량</span> 로그 처리 <span class="uicontrol"> ] &gt; [</span> 로그 처리 <i>] &gt; &lt;프로필 이름&gt;<span class="uicontrol"></span></i> <span class="uicontrol"></span> <span class="uicontrol"></span> <span class="uicontrol"></span> <i><span class="uicontrol"></span></i>또는 성능 &gt; &gt; [CPU 사용] &gt; [변환] &gt; [변환] &gt; [프로필 이름]을 클릭합니다. </p> <p>이러한 섹션의 필드를 검토하여 로그 처리 및 변환에 필요한 시간에 부정적인 영향을 줄 수 있는 필터 및 변형을 식별할 수 있습니다. 그런 다음 처리 시간이 길어질 때 개별 필터 및 변형과 관련된 디자인 결정을 내릴 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디스크 공간 사용을 모니터링하고 쿼리 속도를 높이려면 </p> </td> 
   <td colname="col2"> <p>성능 <span class="uicontrol"></span> &gt; <span class="uicontrol"></span> 로그 처리 필드 <i>&gt;<span class="uicontrol"> &lt;</span>프로필 이름</i>&gt;배정을 클릭합니다. </p> <p>이 섹션의 각 라인 항목은 Log Processing.cfg <span class="filepath"> 파일의 매개 변수에</span> 해당합니다. 이 필드를 검토하여 각 매개 변수가 사용하는 메모리 양을 확인할 수 있습니다. 그런 다음 매우 큰 개별 항목에 대해 디자인 결정을 내릴 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이전 재처리 또는 변환의 경과 시간을 확인하려면 </p> </td> 
   <td colname="col2"> <p>처리 <span class="uicontrol"> 상태</span> &gt;&lt;프로필 이름 <i>&gt;<span class="uicontrol"> &gt; 처리 모드</span>내역을</i> <span class="uicontrol"></span>클릭합니다. </p> <p> 
     <ul id="ul_B7CC0DF54E004C72B220F928CF223F8E"> 
      <li id="li_2707D8C0D52A44C8BADA4D9AFB5EB2BC">실시간 - 데이터 워크벤치 서버가 쿼리를 만들 수 있었던 시간입니다. </li> 
      <li id="li_3A3B490D70864A259780FC9FFC9AC15E">빠른 입력 - 이번에는 빠른 병합 시간이 데이터 세트 처리에 필요한 총 시간입니다. </li> 
      <li id="li_B754C6DECD924170A15721EA4C942E3D">빠른 병합 - 데이터 세트 변환에 필요한 총 시간입니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>"기준 시간" 문제 진단 </p> </td> 
   <td colname="col2"> <p>상태 <span class="uicontrol"> &gt;&lt;프로필 이름</span> &gt; <i>&gt; 시간<span class="uicontrol"></span></i> 으로 &gt; 소스 처리 <span class="uicontrol"></span> <span class="uicontrol"></span>as-of-Time을 클릭합니다. </p> <p>각 소스에 대한 현재 시간을 검토하면 전체 기준 값에 부정적인 영향을 줄 수 있는 소스를 확인할 수 있습니다. 그런 다음 특정 출처의 문제를 해결할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>실행 중인 쿼리를 완료하는 데 걸리는 시간을 측정하려면 </p> </td> 
   <td colname="col2"> <p>실행 <span class="uicontrol"> 엔진을 클릭합니다</span>. </p> <p>데이터 <span class="wintitle"> 이월</span> 시간 필드를 검토하면 쿼리가 완료하는 데 걸리는 시간을 예측할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이 컴퓨터에서 사용할 수 있는 모든 프로필 및 해당 상태에 대한 세부 정보를 나열하려면 </p> </td> 
   <td colname="col2"> <p>프로필을 <span class="uicontrol"> 클릭합니다</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>복제 상태를 보려면 </p> </td> 
   <td colname="col2"> <p>구성 <span class="uicontrol"> 요소 상태를 클릭합니다</span>. </p> <p>복제 구성 요소의 상태를 확인합니다. 복제가 실행 중인 경우 확인 이 표시됩니다. 복제 구성 요소가 실패한 경우 오류 메시지가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>데이터 워크벤치 <span class="wintitle"> 서버에</span> 연결하는 보고서 <span class="keyword"> 컴퓨터의</span> 보고서 서버 상태를 보려면 </p> </td> 
   <td colname="col2"> <p>보고서 <span class="uicontrol"> 서버 상태를 클릭합니다</span>. </p> <p>세부 상태 <span class="wintitle"> 인터페이스의 이</span> 섹션에는 Report Server.cfg <span class="filepath"></span> 파일 복사본, 실행 중인 보고서 수(현재 슬라이스)에 대한 정보 및 최신 오류(마지막 오류)에 대한 정보가 포함되어 있습니다. </p> <p>보고서 서버.cfg <span class="filepath"> 파일을 편집하는</span> 단계는 데이터 워크벤치 보고서 <i>안내서를 참조하십시오</i>. </p> <p> <p>참고:보고서 <span class="wintitle"> 서버 상태</span> 섹션이 세부 상태 인터페이스에 <span class="wintitle"> 나타나지 않는 경우</span> 데이터 워크벤치 서버를 구성하여 보고서 서버 상태를 표시해야 <span class="wintitle"> 할 수 있습니다</span>. 단계에 대해서는 데이터 워크벤치 <i>보고서 안내서를 참조하십시오</i>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>변환에 대한 메모리 사용 정보를 보려면 </p> </td> 
   <td colname="col2"> <p>처리 <span class="uicontrol"> 상태</span> &gt; 변형을 <span class="uicontrol"> 클릭합니다</span>. </p> <p>변환에 대한 자세한 내용은 서버 제품 <i>설치 및 관리 안내서</i> 및 데이터 세트 구성 <i>안내서를 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>세부 상태 <span class="wintitle"> 인터페이스를</span> *.cfg <span class="filepath"></span> 파일로 저장하려면 메모장과 같은 텍스트 편집기에서 열거나 다른 사람에게 배포할 수 있습니다 </p> </td> 
   <td colname="col2"> <p>세부 상태 <span class="uicontrol"> 머리글을 마우스 오른쪽 단추로</span> 클릭하고 다른 이름으로 사본 <span class="uicontrol"> 저장을 클릭합니다</span>. </p> <p>참고:  <p>세부 상태 <span class="uicontrol"> 머리글을 마우스 오른쪽 단추로 클릭하고</span> 서버 이름 <span class="uicontrol"> /상태</span> /에 저장을 <i>클릭해도</i>자세한 상태 인터페이스에서 <span class="wintitle"> 작동하지</span> 않습니다. 다음 오류 메시지가 나타납니다. </p> <p>/Status/를 저장할 수 없습니다. 403 금지 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그 소스 <span class="uicontrol"> 지표당 행을 보려면</span> 선택 </p> </td> 
   <td colname="col2"> <p>로그 소스 지표당 행을 세부 상태로 보고해야 하는 경우 데이터 워크벤치 관리자는 "로그 소스 ID"를 정의하고 사용자 정의 프로필의 Log Processing.cfg에 고유한 이름을 제공해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

