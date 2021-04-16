---
description: 필요한 Sensor txlogd.conf 매개 변수에 대한 정보입니다.
title: 필수 매개 변수
uuid: 187f4199-ec7f-4d5a-93eb-64a62d51ec7b
exl-id: 782e11e9-b11b-4003-9669-f31187208ec3
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 1%

---

# 필수 매개 변수{#required-parameters}

필요한 Sensor txlogd.conf 매개 변수에 대한 정보입니다.

<table id="table_69CFE10A3707403F9793137B128E706A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수에서.. </th> 
   <th colname="col2" class="entry"> 분류에 사용할... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> SensorID </td> 
   <td colname="col2"> <p>이 <span class="wintitle"> 센서</span>를 고유하게 식별하는 문자열입니다. </p> <p> <span class="wintitle"> 센서소리지</span> 는 센서가  <span class="keyword"> 데이터 워크벤치 서버로 전송하는 각 이벤트 레코드에 SensorID를 첨부합니다</span>. SensorID를 사용하면 이 웹 서버의 이벤트 데이터를 다른 <span class="wintitle"> 센서</span>에서 캡처한 이벤트 데이터와 구별할 수 있습니다. </p> <p>SensorID는 모든 문자열을 문자로 구성할 수 있지만, 규칙에 따라 <span class="wintitle"> Sensor</span>가 캡처하는 이벤트의 웹 서버 이름이 사용됩니다. 서버 이름을 SensorID로 사용하면 분석 단계 중 이벤트 소스를 쉽게 확인할 수 있습니다. 또한 구현 내에서 SensorID가 고유한지 확인합니다. </p> <p>예:<span class="filepath"> SensorID web001a</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 서버 주소 </td> 
   <td colname="col2"> <p>이 <span class="wintitle"> 센서</span>가 이벤트 데이터를 전송하는 데이터 워크벤치 서버</span>의 주소입니다.<span class="keyword"> </span></p> <p>참고:  <p>클러스터 환경에서 작업할 때 동기화 문제를 방지하기 위해 마스터 <span class="keyword"> 데이터 워크벤치 서버</span>에 액세스하도록 <span class="wintitle"> 센서</span>를 구성해야 합니다. Data Workbench에서는 <span class="wintitle"> 서버 관리자</span>의 관련 서버 메뉴 항목을 사용하여 클러스터의 <span class="keyword"> 데이터 워크벤치 서버</span>에 대한 처리 정보를 볼 수 있습니다. <span class="wintitle"> 서버 관리자</span>에 대한 자세한 내용은 <i><span class="keyword"> Data Workbench</span><span class="wintitle"> 센서</span> 안내서</i>를 참조하십시오. </p> <p>웹 서버가 DNS를 통해 서버 이름을 확인할 수 있는 경우 이름별로 서버 주소를 지정할 수 있습니다. 그렇지 않은 경우 서버의 숫자 IP 주소를 지정해야 합니다. </p> <p>예:<span class="filepath"> ServerAddress 10.1.0.7</span> 또는 </p> <p> <span class="filepath"> ServerAddress vserver01.mycompany.com</span> </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL </td> 
   <td colname="col2"> <p><span class="wintitle"> 센서</span>가 HTTP 또는 HTTPS를 사용하여 <span class="keyword"> 데이터 워크벤치 서버</span>와 통신하는지 여부. HTTPS의 경우 "on", HTTP의 경우 "off"로 설정합니다. </p> <p>예:<span class="filepath"></span>의 SSL </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerPort </td> 
   <td colname="col2"> <p><span class="keyword"> 데이터 워크벤치 서버</span>가 이벤트 데이터를 수신하는 포트입니다. </p> <p>예:<span class="filepath"> ServerPort 443</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertName </td> 
   <td colname="col2"> <p>SSL 매개 변수가 "on"으로 설정된 경우에만 필요합니다. </p> <p>이 <span class="wintitle"> 센서</span>가 이벤트 데이터를 전송하는 <span class="keyword"> 데이터 워크벤치 서버</span>의 일반 이름입니다. </p> <p>지정한 값은 <span class="keyword"> 데이터 워크벤치 서버</span> 라이센스 인증서에 나타나는 일반 이름과 정확히 일치해야 합니다. </p> <p>예:<span class="filepath"> CertName vserver01.mycompany.com</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertPath </td> 
   <td colname="col2"> <p>SSL 매개 변수가 "on"으로 설정된 경우에만 필요합니다. </p> <p>인증 기관(<span class="filepath"> trust_ca_cert.pem</span>) 파일이 있는 디렉터리 </p> <p>예: </p> <p> <span class="filepath"> CertPath /usr/local/visualsensor</span> </p> <p> <span class="filepath"> CertPath C:\VisualSensor</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueFile </td> 
   <td colname="col2"> <p>IIS(Internet Information Service) 버전 5.x 또는 6.x를 실행하는 Microsoft Windows 2000 또는 2003 Server 컴퓨터에 Sensor</span> 설치가 필요하지 않습니다.<span class="wintitle"> </span></p> <p>디스크 큐 파일의 정규화된 이름입니다. </p> <p>이 파일에 이름을 할당할 수는 있지만 규칙 상 큐 파일의 이름은 <span class="filepath"> VisualSensor.dat</span>입니다. </p> <p>Unix에 설치된 <span class="wintitle"> 센서</span>의 경우 이 파일을 아무 곳에나 가져올 수 있습니다. Java 웹 서버를 실행하는 Windows의 경우 이 파일을 전송기와 동일한 디렉토리에 저장해야 합니다. 다른 모든 웹 서버의 경우 이 파일은 /var/queue 디렉토리에 있어야 합니다. </p> <p>예:<span class="filepath"> QueueFile /var/queue/VisualSensor.dat</span> </p> <p> <p>참고: 이 파일을 할당하는 장치에 필요한 크기의 큐를 수용할 수 있는 충분한 여유 공간이 있는지 확인하십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueSize </td> 
   <td colname="col2"> <p>디스크 큐 파일의 크기를 MB 단위로 나타내는 정수입니다. </p> <p>Microsoft Windows에서 <span class="wintitle"> Sensor</span> 설치 시 큐 파일 자체는 전송기와 동일한 디렉토리에 생성되며 이름은 <span class="filepath"> Diskq2000.log</span>입니다. </p> <p>다음 예제에서는 큐 크기를 200MB로 설정합니다. </p> <p>QueueSize 200 </p> <p>다음 예제에서는 큐 크기를 2GB로 설정합니다. </p> <p>QueueSize 2000 </p> </td> 
  </tr> 
 </tbody> 
</table>
