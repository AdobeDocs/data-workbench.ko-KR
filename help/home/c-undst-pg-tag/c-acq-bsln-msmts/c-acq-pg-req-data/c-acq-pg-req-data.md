---
description: 센서는 센서가 설치된 웹 서버에 대한 페이지 요청(GET 요청)에 전달되는 모든 측정 데이터를 획득합니다.
title: 페이지 요청 데이터 가져오기
uuid: 06cf2b14-8d2c-483e-8a75-ce772798978f
exl-id: e42566a3-d5b4-4f1a-b8cd-1ea646041101
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 4%

---

# 페이지 요청 데이터 가져오기{#acquiring-page-request-data}

{{eol}}

센서는 센서가 설치된 웹 서버에 대한 페이지 요청(GET 요청)에 전달되는 모든 측정 데이터를 획득합니다.

[!DNL Sensor] 웹 서버에서 실행되는 웹 서버 소프트웨어의 인스턴스 또는 인스턴스에서 직접 웹 서버의 응용 프로그램 프로그래밍 인터페이스를 통해 이 측정 데이터를 가져옵니다. [!DNL Sensor] 웹 서버에서 생성한 로그 파일에 액세스할 수 없습니다. 사실, 이후 [!DNL Sensor] data workbench 서버가 설치 및 테스트되어 데이터 수집에 영향을 주지 않고 웹 서버의 네이티브 로깅 기능을 비활성화할 수 있습니다. 많은 경우, 웹 서버 시스템의 로컬 디스크에 파일 로깅을 비활성화하면 웹 서버 시스템의 로컬 디스크에 이 정보를 기록하는 데 필요한 고정 디스크 입출력이 상대적으로 많기 때문에 웹 서버의 페이지 서비스 용량이 향상됩니다.

[!DNL Sensor] 각 웹 서버 프로세스 및 가상 웹 서버 프로세스(해당되는 경우)에서 직접 측정 및 웹 요청 데이터를 수집하고 웹 서버 시스템에서 고정 디스크 백업이 있는 내결함성 메모리 큐인 큐 파일에 데이터를 임시 기록합니다. 센서 송신기 서비스(또는 플랫폼에 따라 데몬이)는 큐 파일에서 데이터를 검색한 다음, 데이터를 압축하고 암호화한 후 장기간 보관을 위해 Data Workbench 서버로 전송합니다. 사용 [!DNL Sensor]를 지정하면 네트워크 또는 다른 문제가 발생하여 전송을 방지하는 경우에만 대기열 파일의 웹 서버 시스템에 데이터가 누적됩니다. 큐 파일을 사용하면 네트워크 또는 시스템 오류로 인해 데이터를 실시간으로 Data Workbench 서버로 전송할 수 없는 경우 데이터를 보호하기 위해 몇 시간에서 몇 일 동안의 효율적인 로컬 저장소를 사용할 수 있습니다.

[!DNL Sensor] 각 물리적 및 논리적 웹 서버 프로세스에서 측정 데이터를 수집하고, 컨텐츠 유형별로 필터링하고, 압축하고, 암호화하고, data workbench 서버로 스트리밍합니다.

다음 표에는 [!DNL Sensor] 를 기반으로 필터링되지 않은 각 GET 요청에 대해 [!DNL Sensor’s] 구성 파일:

<table id="table_5F65474150EC41648B35D0B031FB9B15">
 <thead>
  <tr>
   <th colname="col1" class="entry"> W3C 이름 </th>
   <th colname="col2" class="entry"> 수집한 데이터 </th>
   <th colname="col3" class="entry"> 설명 </th>
   <th colname="col4" class="entry"> 설명 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> x-trackingid </td>
   <td colname="col2"> 추적 식별자(고유 방문자) </td>
   <td colname="col3"> 사용자의 브라우저에 배치된 쿠키에서 읽은 식별자입니다. <span class="wintitle"> Sensor </span> 방문자의 초기 요청 시 </td>
   <td colname="col4"> V1st=3C94007B4E01F9C2 </td>
  </tr>
  <tr>
   <td colname="col1"> <p>날짜 </p> <p>시간 </p> </td>
   <td colname="col2"> 타임스탬프 </td>
   <td colname="col3"> 서버에서 요청을 처리한 시간(100ns 전체 자릿수) 정확성은 서버 환경 및 NTP에 따라 다릅니다. </td>
   <td colname="col4"> 2002-11-21 17:21:45.123 </td>
  </tr>
  <tr>
   <td colname="col1"> sc(content-type) </td>
   <td colname="col2"> 콘텐츠 유형 </td>
   <td colname="col3"> 서버에서 반환된 개체 유형 </td>
   <td colname="col4"> 텍스트/html </td>
  </tr>
  <tr>
   <td colname="col1"> sc-status </td>
   <td colname="col2"> HTTP 응답 상태 코드 </td>
   <td colname="col3"> HTTP 서버의 응답 상태를 기록하는 서버에서 생성된 숫자 코드 </td>
   <td colname="col4"> 404년 </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-stem </td>
   <td colname="col2"> URI 줄기 </td>
   <td colname="col3"> 클라이언트가 요청한 URI의 줄기 부분 </td>
   <td colname="col4"> <span class="filepath"> pagedir/page.asp </span> </td>
  </tr>
  <tr>
   <td colname="col1"> c-ip </td>
   <td colname="col2"> 클라이언트 IP </td>
   <td colname="col3"> 요청하는 클라이언트의 IP 주소 </td>
   <td colname="col4"> 127.0.0.1 </td>
  </tr>
  <tr>
   <td colname="col1"> s-dns </td>
   <td colname="col2"> 서버 도메인 이름 </td>
   <td colname="col3"> 요청을 처리하는 웹 서버의 도메인 이름 </td>
   <td colname="col4"> <span class="filepath"> www.domain.com </span> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(referrer) </td>
   <td colname="col2"> 참조 URL </td>
   <td colname="col3"> 클라이언트가 보낸 HTTP 레퍼러 필드의 콘텐츠입니다 </td>
   <td colname="col4"> <span class="filepath"> https://www.referringsite.com </span> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(user-agent) </td>
   <td colname="col2"> 사용자 에이전트 </td>
   <td colname="col3"> HTTP 서버에 요청을 하는 데 사용되는 장치 </td>
   <td colname="col4"> Mozilla/4.0+(호환;+MSIE+6.0; +Windows+NT+5.1) </td>
  </tr>
  <tr>
   <td colname="col1"> cs(cookie) </td>
   <td colname="col2"> 도메인의 클라이언트 쿠키 </td>
   <td colname="col3"> 사이트에 대한 모든 사용자 쿠키의 콘텐츠입니다 </td>
   <td colname="col4"> <p>KL_TC1 1038058778312 </p> <p>KL972x1038058778312282052 </p> <p>KL_PVKL972 0 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-query </td>
   <td colname="col2"> 쿼리 문자열 </td>
   <td colname="col3"> 클라이언트가 요청한 URI 중 쿼리 문자열 부분(있는 경우) </td>
   <td colname="col4"> PAGENAME=dynamic1&amp;link=3001 </td>
  </tr>
 </tbody>
</table>
