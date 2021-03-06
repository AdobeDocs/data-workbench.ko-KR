---
description: Insight Server에 설치된 파일 및 등록 후 있는 파일 목록을 나열하고 처음 실행합니다.
title: Insight Server 디렉터리 구조
uuid: 8339b275-f118-4d5d-937e-4df9f8a56b50
exl-id: 568391d0-e0f7-4a5a-ad71-de33c52968a0
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 5%

---

# Insight Server 디렉터리 구조{#insight-server-directory-structure}

Insight Server에 설치된 파일 및 등록 후 있는 파일 목록을 나열하고 처음 실행합니다.

## 설치 패키지에 포함된 파일 {#section-daec17dab3e34c3c9e1ef65842cb91f1}

다음 디렉토리는 [!DNL Insight Server] 설치 패키지에 포함되어 있습니다.

<table id="table_CE713A3D671C453A87986E4CD4620EF3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 디렉토리 </th> 
   <th colname="col2" class="entry"> 디렉토리 내용 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 액세스 제어 </td> 
   <td colname="col2"> <span class="keyword"> 액세스 그룹 목록을 지정하는 Insight Server  </span> 구성 파일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주소 </td> 
   <td colname="col2"> <span class="keyword"> Insight Server </span>와의 통신에 사용되는 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 감사 </td> 
   <td colname="col2"> 일별 액세스 로그에는 <span class="keyword"> Insight Server </span>에 대해 시도한 모든 연결에 대한 세부 사항이 포함되어 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> bin </td> 
   <td colname="col2"> <span class="keyword"> Insight Server  </span> 실행 프로그램 파일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 인증서 </td> 
   <td colname="col2"> SSL 디지털 인증서. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 구성 요소 </td> 
   <td colname="col2"> <span class="keyword"> Insight Server  </span> 구성 요소 구성 파일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 처리 서버용 구성 요소 </td> 
   <td colname="col2"> <span class="keyword"> Insight Server  </span> 클러스터 내에서  <span class="keyword"> Insight Server </span> 를 처리하기 위한  <span class="keyword"> Insight Server 구성  </span> 파일. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 오류 메시지를 포함한 자세한 이벤트 상태 메시지가 포함된 일별 이벤트 로그입니다. <span class="keyword"> Insight Server </span>에 의해 캡처되고 기록된 이벤트도 Windows 이벤트 뷰어에 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 </td> 
   <td colname="col2"> <p><span class="wintitle"> 센서 </span>에서 생성한 로그 파일입니다. </p> <p>"Logs"는 기본 로깅 디렉터리이지만 <span class="filepath"> communications.cfg </span> 파일에 대체 디렉터리가 지정되어 있을 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조회 </td> 
   <td colname="col2"> 로봇 및 검색 엔진 목록과 같은 조회 파일. <span class="keyword"> Insight Server는 모든 조회 파일을 메모리에 로드해야  </span> 합니다. 구성 요소 구성 파일에서 참조되는 모든 조회 파일의 총 크기와 오버헤드(예: <span class="filepath"> FlatFileLookup </span> 파일에 대해 행당 12바이트)는 다른 모든 소프트웨어 응용 프로그램이 로드된 후 사용할 수 있는 실제 또는 가상 메모리를 초과해서는 안 됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프로필 </td> 
   <td colname="col2"> <p>각 프로필(구성, 작업 공간 및 시각화 파일)과 관련된 파일. 프로필은 데이터 집합의 데이터로 채워집니다. 데이터 세트에는 이벤트 데이터("로그 데이터")가 포함됩니다.이러한 데이터는 설치된 <span class="wintitle"> Sensors </span>, 웹 비콘 또는 페이지 태그에 의해 전송되거나, 데이터 웨어하우스에서 입력할 수 있습니다. <span class="keyword"> 주어진  </span> 프로필에 액세스할 수 있는 Insight 사용자는 해당 프로필에 대해 처리된 데이터 세트와 해당 프로필 내에 정의된 작업 공간 및 시각화를 사용할 수 있습니다. </p> <p>작업 공간은 시스템 관리 또는 분석을 위한 작업 영역입니다. 작업 공간에는 시스템 성능에 대한 다른 세부 사항을 보여주는 여러 인터페이스가 포함될 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 소프트웨어 </td> 
   <td colname="col2"> <span class="keyword"> 인사이트  </span> 소프트웨어 업데이트. 보고서 소프트웨어 업데이트도 여기에 저장됩니다. </td> 
  </tr> 
 </tbody> 
</table>

## 시작 후 만든 디렉터리 및 파일 {#section-ef7408e8fae64454b326ec07453d4628}

아래 나열된 디렉터리는 [!DNL Insight Server] 이 등록되고 처음 실행된 후에 만들어집니다.

<table id="table_89CC9F3E568044C8A0072BF0A6EDCCEF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 디렉토리 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 주/도 </td> 
   <td colname="col2"> <span class="keyword"> Insight Server </span>에서 생성된 처리 정보. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 임시 </td> 
   <td colname="col2"> <p>재처리 및 작업 중에 <span class="keyword"> Insight Server </span>에서 사용하는 임시 파일의 위치입니다. 일반적으로 물리적 드라이브당 이름이 <span class="filepath"> temp.db </span>인 파일이 한 개 있습니다. </p> <p> <span class="keyword"> 이 디렉토리에 쓰도록 Insight Server를 구성해야  </span> 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Trace </td> 
   <td colname="col2"> <span class="keyword"> Insight Server </span>에 대한 로그 및 이벤트 데이터입니다. 문제 해결에 유용합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 사용자 참조 </td> 
   <td colname="col2"> 서버의 프로필에 액세스할 수 있는 ( <span class="keyword"> Insight </span>) 사용자가 지명되었습니다. 사용자가 <span class="keyword"> Insight </span>를 통해 <span class="keyword"> Insight Server </span>에 처음 액세스할 때 이름이 지정된 각 사용자의 디렉토리가 Users\ 디렉토리 내에 생성됩니다. 명명된 각 사용자의 디렉토리에는 사용자가 해당 <span class="keyword"> Insight Server </span>에서 액세스한 모든 프로필에 해당하는 디렉토리와 해당 로컬 주소 파일이 포함되어 있습니다. </td> 
  </tr> 
 </tbody> 
</table>
