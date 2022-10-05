---
description: Insight Server에 설치된 파일 및 등록 후 있는 파일 목록을 나열하고 처음 실행합니다.
title: Insight Server 디렉터리 구조
uuid: 8339b275-f118-4d5d-937e-4df9f8a56b50
exl-id: 568391d0-e0f7-4a5a-ad71-de33c52968a0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 4%

---

# Insight Server 디렉터리 구조{#insight-server-directory-structure}

{{eol}}

Insight Server에 설치된 파일 및 등록 후 있는 파일 목록을 나열하고 처음 실행합니다.

## 설치 패키지에 포함된 파일 {#section-daec17dab3e34c3c9e1ef65842cb91f1}

다음 디렉토리는 [!DNL Insight Server] 설치 패키지:

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
   <td colname="col2"> <span class="keyword"> Insight Server </span> 액세스 그룹 목록을 지정하는 구성 파일입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주소 </td> 
   <td colname="col2"> 통신용 주소 <span class="keyword"> Insight Server </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 감사 </td> 
   <td colname="col2"> 일별 액세스 로그에는 시도한 모든 연결에 대한 세부 사항이 포함되어 있습니다 <span class="keyword"> Insight Server </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> bin </td> 
   <td colname="col2"> <span class="keyword"> Insight Server </span> 실행 프로그램 파일. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 인증서 </td> 
   <td colname="col2"> SSL 디지털 인증서. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 구성 요소 </td> 
   <td colname="col2"> <span class="keyword"> Insight Server </span> 구성 요소 구성 파일. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 처리 서버용 구성 요소 </td> 
   <td colname="col2"> <span class="keyword"> Insight Server </span> 처리를 위한 구성 요소 구성 파일 <span class="keyword"> Insight Server </span> 내 <span class="keyword"> Insight Server </span> 클러스터 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이벤트 </td> 
   <td colname="col2"> 오류 메시지를 포함한 자세한 이벤트 상태 메시지가 포함된 일별 이벤트 로그입니다. 에 의해 캡처되고 기록된 이벤트 <span class="keyword"> Insight Server </span> Windows 이벤트 뷰어에도 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 </td> 
   <td colname="col2"> <p>에서 생성한 로그 파일 <span class="wintitle"> Sensor </span>초. </p> <p>"Logs"는 기본 로깅 디렉터리이지만 <span class="filepath"> communications.cfg </span> 파일. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조회 </td> 
   <td colname="col2"> 로봇 및 검색 엔진 목록과 같은 조회 파일. <span class="keyword"> Insight Server </span> 모든 조회 파일을 메모리에 로드해야 합니다. 구성 요소 구성 파일에서 참조되는 모든 조회 파일의 총 크기와 오버헤드(예: <span class="filepath"> 플랫 파일 조회 </span> 파일)를 지정하면 다른 모든 소프트웨어 응용 프로그램이 로드된 후 사용할 수 있는 실제 또는 가상 메모리를 초과할 수 없습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프로필 </td> 
   <td colname="col2"> <p>각 프로필(구성, 작업 공간 및 시각화 파일)과 관련된 파일. 프로필은 데이터 집합의 데이터로 채워집니다. 데이터 세트에는 이벤트 데이터("로그 데이터")가 포함됩니다. 이러한 데이터는 설치 시 캡처될 수 있습니다. <span class="wintitle"> 센서 </span>: 웹 비콘이나 페이지 태그에 의해 전송되거나 데이터 웨어하우스에서 입력됩니다. <span class="keyword"> 인사이트 </span> 주어진 프로필에 액세스할 수 있는 사용자는 해당 프로필에 대해 처리된 데이터 세트와 해당 프로필 내에 정의된 작업 공간 및 시각화를 사용할 수 있습니다. </p> <p>작업 공간은 시스템 관리 또는 분석을 위한 작업 영역입니다. 작업 공간에는 시스템 성능에 대한 다른 세부 사항을 보여주는 여러 인터페이스가 포함될 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 소프트웨어 </td> 
   <td colname="col2"> <span class="keyword"> 인사이트 </span> 소프트웨어 업데이트. 보고서 소프트웨어 업데이트도 여기에 저장됩니다. </td> 
  </tr> 
 </tbody> 
</table>

## 시작 후 만든 디렉터리 및 파일 {#section-ef7408e8fae64454b326ec07453d4628}

아래 나열된 디렉터리는 다음 후에 만들어집니다 [!DNL Insight Server] 가 등록되고 처음 실행됩니다.

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
   <td colname="col2"> 생성된 처리 정보 <span class="keyword"> Insight Server </span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 임시 </td> 
   <td colname="col2"> <p>에서 사용하는 임시 파일의 위치 <span class="keyword"> Insight Server </span> 재처리 및 작업 중에 일반적으로 파일 이름이 <span class="filepath"> temp.db </span> 기본적으로)(실제 드라이브당). </p> <p> <span class="keyword"> Insight Server </span> 이 디렉터리에 쓰도록 구성해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Trace </td> 
   <td colname="col2"> 이벤트 데이터 기록 <span class="keyword"> Insight Server </span>. 문제 해결에 유용합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 사용자 참조 </td> 
   <td colname="col2"> 이름이 지정됨 ( <span class="keyword"> 인사이트 </span>) 서버에 있는 프로필에 액세스할 수 있는 사용자입니다. 사용자가 처음 액세스할 때 Users\ 디렉토리 내에 권한이 부여된 각 사용자에 대한 디렉토리가 생성됩니다 <span class="keyword"> Insight Server </span> via <span class="keyword"> 인사이트 </span>. 이름이 지정된 각 사용자의 디렉토리에는 사용자가 해당 사용자에서 액세스한 모든 프로필에 해당하는 디렉토리가 있습니다 <span class="keyword"> Insight Server </span> 및 로컬 주소 파일도 함께 사용할 수 있습니다. </td> 
  </tr> 
 </tbody> 
</table>
