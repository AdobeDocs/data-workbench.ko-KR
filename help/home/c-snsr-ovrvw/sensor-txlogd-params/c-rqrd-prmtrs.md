---
description: 필요한 Sensor txlogd.conf 매개 변수에 대한 정보입니다.
title: 필수 매개 변수
uuid: 187f4199-ec7f-4d5a-93eb-64a62d51ec7b
exl-id: 782e11e9-b11b-4003-9669-f31187208ec3
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 1%

---

# 필수 매개 변수{#required-parameters}

{{eol}}

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
   <td colname="col2"> <p>이 항목을 고유하게 식별하는 문자 문자열입니다 <span class="wintitle"> Sensor</span>. </p> <p> <span class="wintitle"> Sensor</span> 는 전송한 각 이벤트 레코드에 SensorID를 연결합니다 <span class="keyword"> data workbench 서버</span>. SensorID를 사용하면 이 웹 서버의 이벤트 데이터를 다른 사용자가 캡처하는 이벤트 데이터와 구별할 수 있습니다 <span class="wintitle"> 센서</span>. </p> <p>SensorID는 어떤 문자열로도 구성될 수 있지만 규칙을 사용하여 이벤트가 발생한 웹 서버의 이름입니다. <span class="wintitle"> Sensor</span> 이 캡처되고 있습니다. 서버 이름을 SensorID로 사용하면 분석 단계에서 이벤트 소스를 쉽게 확인할 수 있습니다. 또한 SensorID가 구현 내에서 고유한지 확인합니다. </p> <p>예: <span class="filepath"> SensorID web001a</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerAddress </td> 
   <td colname="col2"> <p>주소 <span class="keyword"> data workbench 서버</span> 여기에 <span class="wintitle"> Sensor</span> 은 이벤트 데이터를 보냅니다. </p> <p>참고:  <p>클러스터 환경에서 작업할 경우 <span class="wintitle"> Sensor</span> 마스터에 액세스하도록 구성해야 합니다. <span class="keyword"> data workbench 서버</span> 동기화 문제를 피하려면 Data Workbench에서 처리에 대한 정보를 볼 수 있습니다 <span class="keyword"> data workbench 서버</span> 클러스터의 <span class="wintitle"> 서버 관리자</span>. 에 대한 자세한 정보 <span class="wintitle"> 서버 관리자</span>를 참조하고 <i><span class="keyword"> Data Workbench</span><span class="wintitle"> Sensor</span> 안내서</i>. </p> <p>웹 서버가 DNS를 통해 서버 이름을 확인할 수 있는 경우 이름을 기준으로 서버 주소를 지정할 수 있습니다. 그렇지 않은 경우 서버의 숫자 IP 주소를 지정해야 합니다. </p> <p>예: <span class="filepath"> ServerAddress 10.1.0.7</span> 또는 </p> <p> <span class="filepath"> ServerAddress vserver01.mycompany.com</span> </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL </td> 
   <td colname="col2"> <p>다음 <span class="wintitle"> Sensor</span> 통신사 <span class="keyword"> data workbench 서버</span> HTTP 또는 HTTPS를 사용하는 경우 HTTPS의 경우 "on" 또는 HTTP의 경우 "off"로 설정합니다. </p> <p>예: <span class="filepath"> SSL 켜기</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ServerPort </td> 
   <td colname="col2"> <p>포트 <span class="keyword"> data workbench 서버</span> 이벤트 데이터를 수신합니다. </p> <p>예: <span class="filepath"> ServerPort 443</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertName </td> 
   <td colname="col2"> <p>SSL 매개 변수가 "on"으로 설정된 경우에만 필요합니다. </p> <p>의 공통 이름 <span class="keyword"> data workbench 서버</span> 여기에 <span class="wintitle"> Sensor</span> 은 이벤트 데이터를 보냅니다. </p> <p>지정하는 값은 <span class="keyword"> data workbench 서버</span> 라이센스 인증서. </p> <p>예: <span class="filepath"> CertName vserver01.mycompany.com</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CertPath </td> 
   <td colname="col2"> <p>SSL 매개 변수가 "on"으로 설정된 경우에만 필요합니다. </p> <p>인증 기관(<span class="filepath"> trust_ca_cert.pem</span>) 파일이 있습니다. </p> <p>예: </p> <p> <span class="filepath"> CertPath /usr/local/visualsensor</span> </p> <p> <span class="filepath"> CertPath C:\VisualSensor</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueFile </td> 
   <td colname="col2"> <p>에 필요하지 않음 <span class="wintitle"> Sensor</span> iis(인터넷 정보 서비스) 버전 5.x 또는 6.x를 실행하는 Microsoft Windows 2000 또는 2003 Server 시스템에 설치 </p> <p>디스크 큐 파일의 정규화된 이름입니다. </p> <p>이 파일에 어떤 이름이든 할당할 수 있지만 규칙에 따라 대기열 파일의 이름은 로 지정됩니다 <span class="filepath"> VisualSensor.dat</span>. </p> <p>대상 <span class="wintitle"> Sensor</span> Unix에 설치하면 이 파일을 어디에나 배치할 수 있습니다. Java 웹 서버를 실행하는 Windows에서는 이 파일을 전송기와 동일한 디렉토리에 배치해야 합니다. 다른 모든 웹 서버의 경우 이 파일은 /var/queue 디렉토리에 있어야 합니다. </p> <p>예: <span class="filepath"> QueueFile /var/queue/VisualSensor.dat</span> </p> <p> <p>참고: 이 파일을 할당하는 장치에 필요한 크기의 큐를 수용할 수 있는 충분한 공간이 있는지 확인하십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> QueueSize </td> 
   <td colname="col2"> <p>디스크 큐 파일 크기(MB)를 나타내는 정수입니다. </p> <p>대상 <span class="wintitle"> Sensor</span> Microsoft Windows에 설치하는 경우 대기열 파일 자체는 송신기와 동일한 디렉토리에 생성되며 이름이 지정됩니다 <span class="filepath"> Diskq2000.log</span>. </p> <p>다음 예제에서는 큐 크기를 200MB로 설정합니다. </p> <p>큐 크기 200 </p> <p>다음 예제에서는 큐 크기를 2GB로 설정합니다. </p> <p>큐 크기 2000 </p> </td> 
  </tr> 
 </tbody> 
</table>
