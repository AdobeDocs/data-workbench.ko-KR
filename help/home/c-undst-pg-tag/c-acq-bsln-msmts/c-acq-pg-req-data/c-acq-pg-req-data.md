---
description: 센서는 설치된 웹 서버에 대한 페이지 요청(GET 요청)에 수행된 모든 측정 데이터를 가져옵니다.
title: 페이지 요청 데이터 가져오기
uuid: 06cf2b14-8d2c-483e-8a75-ce772798978f
exl-id: e42566a3-d5b4-4f1a-b8cd-1ea646041101
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 4%

---

# 페이지 요청 데이터 가져오기{#acquiring-page-request-data}

센서는 설치된 웹 서버에 대한 페이지 요청(GET 요청)에 수행된 모든 측정 데이터를 가져옵니다.

[!DNL Sensor] 웹 서버에서 실행되는 웹 서버 소프트웨어의 인스턴스 또는 인스턴스에서 직접 웹 서버의 응용 프로그램 프로그래밍 인터페이스를 통해 이 측정 데이터를 가져옵니다. [!DNL Sensor] 은 웹 서버에서 생성한 로그 파일에 액세스할 수 없습니다. 실제로 [!DNL Sensor] 및 데이터 워크벤치 서버가 설치 및 테스트된 후 데이터 수집에 영향을 주지 않고 웹 서버의 기본 로깅 기능을 비활성화할 수 있습니다. 대부분의 경우 웹 서버 시스템의 로컬 디스크에 파일 로깅을 비활성화하면 웹 서버 시스템의 로컬 디스크에 이 정보를 기록하기 위해 필요한 비교적 많은 양의 고정 디스크 입출력이 필요하므로 해당 웹 서버의 페이지 제공 용량이 향상됩니다.

[!DNL Sensor] 각 웹 서버 프로세스 및 가상 웹 서버 프로세스에서 직접 측정 및 웹 요청 데이터를 수집하고(해당되는 경우) 웹 서버 시스템에서 고정 디스크 백업이 있는 내결함성이 있는 메모리 큐인 대기열 파일에 데이터를 임시로 씁니다. Sensor Transmitter 서비스(플랫폼에 따라 달라지는 데몬)는 큐 파일에서 데이터를 검색한 다음 장기 보관을 위해 데이터 워크벤치 서버로 전송하기 전에 압축 및 암호화합니다. [!DNL Sensor]을 사용하면 네트워크 또는 전송을 방해하는 다른 문제가 있는 경우에만 대기열 파일의 웹 서버 컴퓨터에 데이터가 누적됩니다. 대기열 파일을 사용하면 네트워크 또는 시스템 장애로 인해 데이터를 실시간으로 데이터 워크벤치 서버로 전송할 수 없는 경우 웹 요청 데이터를 보호하는 데 몇 시간 내지 며칠의 효율적인 로컬 저장소를 사용할 수 있습니다.

[!DNL Sensor] 각 물리적 및 논리적 웹 서버 프로세스로부터 측정 데이터를 수집하고 컨텐츠 유형별로 필터링하며 압축 후 암호화하여 데이터 워크벤치 서버로 스트리밍합니다.

다음 표에는 [!DNL Sensor’s] 구성 파일을 기준으로 필터링되지 않은 각 GET 요청에 대해 [!DNL Sensor]이(가) 취득하는 로그 정보 필드가 포함되어 있습니다.

<table id="table_5F65474150EC41648B35D0B031FB9B15"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> W3C 이름 </th> 
   <th colname="col2" class="entry"> 수집된 데이터 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> x-trackingid </td> 
   <td colname="col2"> 추적 식별자(고유 방문자) </td> 
   <td colname="col3"> 방문자의 초기 요청에서 <span class="wintitle"> Sensor </span>가 사용자의 브라우저에 배치된 쿠키에서 읽은 식별자 </td> 
   <td colname="col4"> V1st=3C94007B4E01F9C2 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>날짜 </p> <p>시간 </p> </td> 
   <td colname="col2"> 타임스탬프 </td> 
   <td colname="col3"> 서버에서 요청을 처리한 시간(100ns 정밀도)정확성은 서버 환경 및 NTP에 따라 다름) </td> 
   <td colname="col4"> 2002-11-21 17:21:45.123 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc(content-type) </td> 
   <td colname="col2"> 컨텐츠 유형 </td> 
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
   <td colname="col2"> URI 시스템 </td> 
   <td colname="col3"> 클라이언트가 요청한 URI의 시스템 부분 </td> 
   <td colname="col4"> <span class="filepath"> pagedir/page.asp  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> c-ip </td> 
   <td colname="col2"> 클라이언트 IP </td> 
   <td colname="col3"> 요청한 클라이언트의 IP 주소 </td> 
   <td colname="col4"> 127.0.0.1 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s-dns </td> 
   <td colname="col2"> 서버 도메인 이름 </td> 
   <td colname="col3"> 요청을 처리하는 웹 서버의 도메인 이름 </td> 
   <td colname="col4"> <span class="filepath"> www.domain.com  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(referrer) </td> 
   <td colname="col2"> 참조 URL </td> 
   <td colname="col3"> 클라이언트가 보낸 HTTP 레퍼러 필드의 내용 </td> 
   <td colname="col4"> <span class="filepath"> http://www.referringsite.com  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(user-agent) </td> 
   <td colname="col2"> 사용자 에이전트 </td> 
   <td colname="col3"> HTTP 서버에 대한 요청을 수행하는 데 사용되는 장치 </td> 
   <td colname="col4"> Mozilla/4.0+(compatible;+MSIE+6.0;+Windows+NT+5.1) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(cookie) </td> 
   <td colname="col2"> 도메인의 클라이언트 쿠키 </td> 
   <td colname="col3"> 사이트에 대한 모든 사용자 쿠키의 컨텐츠 </td> 
   <td colname="col4"> <p>KL_TC1 1038058778312 </p> <p>KL972x1038058778312282052 </p> <p>KL_PVKL972 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> 쿼리 문자열 </td> 
   <td colname="col3"> 클라이언트가 요청한 URI가 있는 경우 쿼리 문자열 부분 </td> 
   <td colname="col4"> PAGENAME=dynamic1&amp;link=3001 </td> 
  </tr> 
 </tbody> 
</table>
