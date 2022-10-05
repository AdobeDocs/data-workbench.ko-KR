---
description: 자세한 상태 인터페이스는 Data Workbench 서버 컴퓨터의 오류 또는 기타 문제를 해결하는 데 유용합니다.
title: 자세한 상태 인터페이스
uuid: c4d375d9-431f-4b0a-ba15-b7a10501b2e2
exl-id: 6a460ebd-fb8f-4486-9849-dad2ff745cb5
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# 자세한 상태 인터페이스{#detailed-status-interface}

{{eol}}

자세한 상태 인터페이스는 Data Workbench 서버 컴퓨터의 오류 또는 기타 문제를 해결하는 데 유용합니다.

여기에는 다음이 포함됩니다 [!DNL Transform] 해당 컴퓨터에서 실행 중인 프로필 또는 [!DNL Report] Data Workbench 서버의 클라이언트인 컴퓨터 액세스할 수 있습니다 [!DNL Master Server] 및 [!DNL Query Server Detailed Status] 를 통한 인터페이스 [!DNL Admin] 메뉴 아래의 제품에서 사용할 수 있습니다. 에 액세스하려면 [!DNL Detailed Status] 다른 컴퓨터의 인터페이스, [!DNL Servers Manager]를 클릭하고, 상태를 보려는 서버의 노드를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Detailed Status]**. 자세한 내용은 [서버 관리자](../../../home/c-get-started/c-admin-intrf/c-svrs-mgr.md#concept-2dfff1ca5bce470a8ee854ed57cbe5ba).

Data Workbench 서버에 대한 자세한 내용은 *서버 제품 설치 및 관리 안내서*.

![](assets/vis_DetailedStatus.png)

>[!NOTE]
>
>에서 정보를 업데이트하려면 [!DNL Detailed Status] 인터페이스에서 마우스 오른쪽 단추를 클릭합니다. **[!UICONTROL Detailed Status]** 을(를) 클릭하고 **[!UICONTROL Refresh]**.

다음 표에는 [!DNL Detailed Status] 인터페이스.

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
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 구성 요소 상태</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>컴퓨터에서 사용 중인 메모리 양을 표시하려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 메모리 상태</span> &gt; <span class="uicontrol"> 주소 공간 로드</span>. </p> <p>주소 공간 로드 모니터링에 대한 자세한 내용은 <i>서버 제품 설치 및 관리 안내서</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>컴퓨터가 /3GB 스위치를 사용하도록 구성되어 있는지 확인하려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 메모리 상태</span> &gt; <span class="uicontrol"> 프로세스 주소 공간</span>. </p> <p>만약 <span class="wintitle"> 합계</span> 필드에 3000000 KB가 더 표시됩니다. 컴퓨터가 /3GB 스위치를 사용하도록 구성되어 있습니다. </p> <p>/3GB 스위치에 대한 자세한 내용은 <i>서버 제품 설치 및 관리 안내서</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>각 차원을 저장하는 데 사용되는 디스크 공간 및 메모리와 해당 요소의 이름을 저장하는 데 사용되는 메모리를 모니터링합니다 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 성능</span> &gt; <span class="uicontrol"> Dimension</span> &gt; <span class="uicontrol"> 디스크 사용</span> &gt; <i>&lt;<span class="uicontrol"> 프로필 이름</span>&gt; </i>또는 <span class="uicontrol"> 성능</span> &gt; <span class="uicontrol"> Dimension</span> &gt; <span class="uicontrol"> 메모리 사용</span> &gt; <i>&lt;<span class="uicontrol"> 프로필 이름</span>&gt;</i>. </p> <p>다음 <span class="wintitle"> 디스크 사용</span> 필드는 각 차원을 저장하는 데 필요한 디스크 공간(MB)의 이름과 크기를 제공합니다. Data Workbench 서버가 관련 쿼리를 완료하기 위해 모든 데이터를 읽어야 하므로 디스크 사용량 수치가 크면 쿼리 시간에 부정적인 영향을 줄 수 있습니다. 차원에 대한 디스크 사용을 줄이면 관련 쿼리를 완료하는 데 걸리는 시간을 줄일 수 있습니다. </p> <p>다음 <span class="wintitle"> 메모리 사용</span> 필드는 각 차원의 요소 수와 요소 이름 목록을 저장하는 데 필요한 메모리 양을 제공합니다. Data Workbench 서버가 각 요소를 통해 읽어야 하므로 많은 요소가 쿼리 중에 사용되는 메모리 양에 부정적인 영향을 줄 수 있습니다. 차원에서 요소 수를 줄이면 관련 쿼리를 완료하는 데 걸리는 시간이 줄어들 수 있습니다. </p> <p>예: <code>+&nbsp;Performance
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
   <td colname="col1"> <p>로그 처리 및 변환 내의 단계에 대한 CPU 사용을 모니터하려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 성능</span> &gt; <span class="uicontrol"> CPU 사용</span> &gt; <span class="uicontrol"> 로그 처리</span> &gt; <i>&lt;<span class="uicontrol"> 프로필 이름</span>&gt;</i> 또는 <span class="uicontrol"> 성능</span> &gt; <span class="uicontrol"> CPU 사용</span> &gt; <span class="uicontrol"> 변환</span> &gt; &lt;<span class="uicontrol"> 프로필 이름</span>&gt;. </p> <p>이러한 각 필드 세트는 로그 처리 및 변환 내의 각 단계에 대한 CPU 사용량(초)을 제공합니다. </p> <p>예: <code>+&nbsp;Performance
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;CPU&nbsp;Usage&nbsp;
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Log&nbsp;Processing
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;ProfileName&nbsp;158.9&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Built-in&nbsp;158.1&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;StageName&nbsp;13.0&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;.&nbsp;.&nbsp;.
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;Log&nbsp;Processing\ProfileName&nbsp;0.8&nbsp;sec
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;StageName&nbsp;0.8&nbsp;sec</code> </p> <p>쿼리를 완료하는 데 걸리는 시간은 일반적으로 모든 차원의 총 크기에 비례합니다. 각 차원의 크기를 검토한 후 특정 차원이 충분히 유용한지 여부를 평가할 수 있으며 자주 사용되어 차원의 성능 비용을 정당화할 수 있습니다. 그렇지 않으면, <span class="wintitle"> 프로필 관리자</span>.<p>요소 이름 목록이 너무 큰 차원(즉, 128MB 이상)은 총 주소 공간 사용량이 제한에 근접하지 않더라도 "메모리 부족" 오류가 발생할 수 있습니다. </p> <p>또한 Data Workbench 서버 클러스터를 사용하지만 중앙 정규화를 사용하지 않는 경우 요소 이름 목록이 큰 차원이 전송 메모리 예산에 큰 영향을 줍니다. 중앙 표준화에 대한 자세한 내용은 <i>데이터 집합 구성 안내서</i>. 모든 요소 이름 목록을 저장하는 데 필요한 메모리 양이 클러스터의 모든 서버에서 100MB를 초과하는 경우 쿼리 활동이 가볍더라도 "메모리 예산 초과 보내기" 오류가 발생할 수 있습니다. 예를 들어, 요소 이름 목록을 저장하는 데 사용되는 각 서버에 25MB가 넘는 4개의 서버 클러스터가 있는 경우 오류가 발생할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>로그 처리 및 변환에서 보낸 시간을 모니터링하려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 성능</span> &gt; <span class="uicontrol"> CPU 사용</span> &gt; <span class="uicontrol"> 로그 처리</span> &gt; <i>&lt;<span class="uicontrol"> 프로필 이름</span>&gt;</i> 또는 <span class="uicontrol"> 성능</span> &gt; <span class="uicontrol"> CPU 사용</span> &gt; <span class="uicontrol"> 변환</span> &gt; <i>&lt;<span class="uicontrol"> 프로필 이름</span>&gt;</i>. </p> <p>이러한 섹션의 필드를 검토하여 로그 처리 및 변환에 필요한 시간에 부정적인 영향을 줄 수 있는 필터 및 변형을 식별할 수 있습니다. 그런 다음 처리 시간이 긴 개별 필터 및 변형에 대한 디자인 결정을 내릴 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>디스크 공간 사용량을 모니터링하고 쿼리 속도를 높이려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 성능</span> &gt; <span class="uicontrol"> 로그 처리 필드</span> &gt; <i>&lt;<span class="uicontrol"> 프로필 이름</span>&gt;</i>. </p> <p>이 섹션의 각 라인 항목은 <span class="filepath"> Log Processing.cfg</span> 파일. 이러한 필드를 검토하면 각 매개 변수가 사용하는 메모리를 확인할 수 있습니다. 그런 다음 매우 큰 개별 항목에 대한 디자인 결정을 내릴 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이전 재처리 또는 변환의 경과 시간을 확인하려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 처리 상태</span> &gt; <i>&lt;<span class="uicontrol"> 프로필 이름</span>&gt;</i> &gt; <span class="uicontrol"> 처리 모드 기록</span>. </p> <p> 
     <ul id="ul_B7CC0DF54E004C72B220F928CF223F8E"> 
      <li id="li_2707D8C0D52A44C8BADA4D9AFB5EB2BC">실시간 - Data Workbench 서버가 쿼리를 만들 수 있었던 시간입니다. </li> 
      <li id="li_3A3B490D70864A259780FC9FFC9AC15E">빠른 입력 - 이번에는 빠른 병합 시간과 함께 데이터 세트를 처리하는 데 필요한 총 시간입니다. </li> 
      <li id="li_B754C6DECD924170A15721EA4C942E3D">빠른 병합 - 데이터 세트를 변환하는 데 필요한 총 시간입니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>"기준 시간" 문제를 진단하려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 처리 상태</span> &gt; <i>&lt;<span class="uicontrol"> 프로필 이름</span>&gt;</i> &gt; <span class="uicontrol"> 기준 시간</span> &gt; <span class="uicontrol"> 소스 기준</span>. </p> <p>각 소스에 대한 현재 시간을 검토하면 전체 기준(Overall As-of)에 부정적인 영향을 줄 수 있는 소스를 확인할 수 있습니다. 그런 다음 특정 출처의 문제를 해결할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>실행 중인 쿼리를 완료하는 데 걸리는 시간을 예상하려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 실행 엔진</span>. </p> <p>검토 <span class="wintitle"> 데이터 청소 시간</span> 필드는 쿼리가 완료되는 데 걸리는 시간을 예상합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이 컴퓨터에서 사용 가능한 모든 프로필과 해당 상태에 대한 세부 정보를 나열하려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 프로필</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>복제 상태를 보려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 구성 요소 상태</span>. </p> <p>복제 구성 요소의 상태를 확인합니다. 복제가 실행 중이면 확인 이 표시됩니다. 복제 구성 요소가 실패하면 오류 메시지가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보려면 <span class="wintitle"> 보고서 서버</span> 상태 <span class="keyword"> 보고서</span> Data Workbench 서버에 연결되는 컴퓨터 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 보고서 서버 상태</span>. </p> <p>의 이 섹션 <span class="wintitle"> 자세한 상태</span> 인터페이스에는 <span class="filepath"> 보고서 서버.cfg</span> 파일, 실행 중인 보고서 수(현재 슬라이스)에 대한 정보 및 가장 최근 오류에 대한 정보(마지막 오류) </p> <p>를 편집하는 단계는 <span class="filepath"> 보고서 서버.cfg</span> 파일, 자세한 내용은 <i>Data Workbench 보고서 안내서</i>. </p> <p> <p>참고: 만약 <span class="wintitle"> 보고서 서버 상태</span> 섹션이 <span class="wintitle"> 자세한 상태</span> 인터페이스, 표시할 Data Workbench 서버를 구성해야 할 수 있습니다 <span class="wintitle"> 보고서 서버 상태</span>. 단계에 대해서는 <i>Data Workbench 보고서 안내서</i>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>변환에 대한 메모리 사용 정보를 보려면 </p> </td> 
   <td colname="col2"> <p>클릭 <span class="uicontrol"> 처리 상태</span> &gt; <span class="uicontrol"> 변형</span>. </p> <p>변형에 대한 자세한 내용은 <i>서버 제품 설치 및 관리 안내서</i> 그리고 <i>데이터 집합 구성 안내서</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>를 저장하려면 <span class="wintitle"> 자세한 상태</span> 인터페이스 <span class="filepath"> *.cfg</span> 메모장과 같은 텍스트 편집기에서 열거나 다른 사람에게 배포할 수 있는 파일 </p> </td> 
   <td colname="col2"> <p>마우스 오른쪽 단추를 클릭합니다. <span class="uicontrol"> 자세한 상태</span> 을(를) 클릭하고 <span class="uicontrol"> 다른 이름으로 복사 저장</span>. </p> <p>참고:  <p>마우스 오른쪽 단추 클릭 <span class="uicontrol"> 자세한 상태</span> 제목 및 클릭 <span class="uicontrol"> 저장</span> to <i>서버 이름</i>/Status/ 는 <span class="wintitle"> 자세한 상태</span> 인터페이스. 다음 오류 메시지가 나타납니다. </p> <p>/Status/ 를 저장할 수 없습니다. 403 금지 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>보려면 <span class="uicontrol"> 로그 소스당 행 수</span> 지표 </p> </td> 
   <td colname="col2"> <p>로그 소스당 행 수 지표를 세부 상태에서 보고해야 하는 경우 Data Workbench 관리자는 "로그 소스 ID"를 정의하고 사용자 지정 프로필의 Log Processing.cfg에 고유한 이름을 제공해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
