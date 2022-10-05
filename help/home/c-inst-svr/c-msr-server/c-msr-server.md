---
description: Data Workbench에 대한 최소 요구 사항 및 권장 사항 식별(이전 [!DNL Insight]) 시스템을 계획 및 구현하기 전에 서버 구성 요소를 구성합니다.
title: 서버 시스템 요구 사항
uuid: c4487c76-03b9-4755-893b-555d451b1e69
exl-id: 6dd78331-8370-400e-b580-9b9bad13e62c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 1%

---

# 서버 시스템 요구 사항{#server-system-requirements}

{{eol}}

시스템을 계획 및 구현하기 전에 Data Workbench 서버 구성 요소에 대한 최소 요구 사항 및 권장 사항을 확인합니다.

## DPU 요구 사항{#dpu-requirements}

서버 DPU(데이터 처리 유닛)는 Data Workbench의 기본 데이터 처리 구성 요소입니다. Data Workbench에서 네트워크 연결을 수신하고 FSU(File Server Unit)에서 원시 소스 데이터를 읽고 상당한 컴퓨터 및 스토리지 리소스를 사용합니다.

### 라이센스 용량 {#section-71850e13783443798b3df9eb22cc63dc}

의 서비스 설명을 참조하십시오. *Adobe [!DNL Data Workbench (Insight)] 서비스 계약* 라이센스 용량 정보

>[!NOTE]
>
>대상 *MS System Center Endpoint Protection* Windows 2012 Server에서는 이러한 실행 파일을 ***제외된 프로세스:*** >
>* [!DNL InsightServer64.exe]
>* [!DNL ReportServer.exe]
>* [!DNL ExportIntegration.exe]
>


### DPU 시스템 Recommendations 및 요구 사항 {#section-ae30555959bf4a309c76d0fd597b5162}

Adobe은 비즈니스 요구 사항을 충족하는 Data Workbench 디자인에 대한 권장 사항을 제공합니다. 그러나 DPU 소프트웨어의 최적화된 특성으로 인해 OS/하드웨어 플랫폼에 특정 요구 사항이 있으므로 운영 체제(OS)와 하드웨어를 선택할 때 다음 지침이 유용합니다.

단일 데이터 세트가 단일 DPU의 용량 또는 속도에 의해 제한된 경우 클러스터링할 수 있습니다. 예를 들어 더 큰 데이터 세트를 더 빨리 실행하기 위해 함께 사용되는 DPU 소프트웨어의 라이센스 복사본이 3개 있다고 가정합니다. 데이터가 시스템 간에 균등하게 분할되므로 데이터 집합에 대해 라이선스가 있는 용량에 3을 곱합니다. 또한 행당 처리 속도가 단일 DPU보다 3배 빠릅니다.

DPU 투자에서 최상의 성능을 얻으려면 Adobe은 다음 표에 설명된 고성능 구성 요소를 권장합니다.

<table id="table_DA0A60CFBA7D4EF98B5ED5A3D8D6777B">
 <thead>
  <tr>
   <th colname="col1" class="entry"> </th>
   <th colname="col2" class="entry"> 필수 여부 </th>
   <th colname="col3" class="entry"> 권장 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> <p>운영 체제 </p> </td>
   <td colname="col2"> <p>Microsoft Windows Server 2008 x64 </p> </td>
   <td colname="col3"> <p>Microsoft Windows Server 2012 x64 </p> <p> Microsoft Windows Server 2016 x64 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>CPU </p> </td>
   <td colname="col2"> <p>권장 사항 를 참조하십시오. </p> </td>
   <td colname="col3"> Intel 또는 AMD의 최신 4세대 코어+ 프로세서가 권장됩니다. 최적의 성능을 위해 8코어 속도와 비용 간의 교환은 4코어가 권장됩니다. </td>
  </tr>
  <tr>
   <td colname="col1"> <p>RAM </p> </td>
   <td colname="col2"> <p>8GB </p> </td>
   <td colname="col3"> <p>12GB </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>작업 데이터 저장소 </p> </td>
   <td colname="col2"> <p>1TB 이상의 총 논리 임시 스토리지. </p> <p>디스크 하위 시스템에 대한 대기 시간이 짧습니다. </p> </td>
   <td colname="col3"> <p>임시 저장소 Adobe의 경우 다음 중 하나를 권장합니다. </p>
    <ul id="ul_F3D033B90CF94F44A2A773B3F6852283">
     <li id="li_B902CF7CC6A44F02838B285ADC725A75">(4~8) * (750GB 이상) SATA HDD(3.5인치 스핀들) </li>
     <li id="li_A378F4E1443F4BB2B54DC7E8372EE572">(6~10) * (300GB 이상) SATA HDD(2.5인치 스핀들) </li>
    </ul> <p>JBOD 배열에서 구성해야 합니다. 또는 총 디스크 용량이 2TB를 초과하는 경우 2디스크 RAID1 볼륨 어레이를 사용할 수 있습니다. 예를 들어 6개의 디스크를 3*(2*750GB RAID 1 페어)로 구성합니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>시스템 데이터 스토리지 </p> </td>
   <td colname="col2"> <p>또한 Adobe을 사용하려면 OS, DPU 소프트웨어 및 기타 시스템 소프트웨어에 적절한 크기(20GB)의 고가용성 스토리지가 필요합니다. </p> </td>
   <td colname="col3"> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>하드웨어 클러스터링 </p> </td>
   <td colname="col2"> <p>권장 사항 를 참조하십시오. </p> </td>
   <td colname="col3"> <p>동일한 서버 세트를 사용합니다. DPU 클러스터에서 가장 느린 서버는 전체 데이터 집합의 성능을 낮춥니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> 네트워크 성능 클러스터링 </td>
   <td colname="col2"> 스위치 기가비트 이더넷 접속 이상 </td>
   <td colname="col3"> </td>
  </tr>
 </tbody>
</table>

### 대체 디스크 하위 시스템 {#section-6f984eabe8074759aa9deaf17e3a68b7}

임시 스토리지에 대한 대체 디스크 하위 시스템을 고려할 때 다음 요인과 지침을 고려하십시오.

* DPU는 고성능 디스크 시스템의 요구 사항이 매우 높기 때문에 디스크 하위 시스템을 잘못 설정하면 성능 병목 현상이 발생할 수 있습니다.
* DPU 소프트웨어는 JBOD 디스크 집합에 대해 고유한 성능 지향 데이터 스트라이핑을 수행합니다. 속도를 높이기 위해 RAID를 사용하지 마십시오.
* Adobe은 DPU에 디스크에 대해 400MB/s의 총 지속 대역폭을 사용할 것을 권장합니다.
* 평균 읽기 크기는 매우 높습니다(2MB+). 이러한 이유로 15K 또는 10K SAS 디스크는 상당한 비용 및 용량 면에서 SATA 디스크보다 약간 더 나은(또는 더 나쁜) 성능을 발휘합니다.
* SAN 아키텍처를 사용하지 마십시오. SAN을 필요한 수준으로 구현하는 데 드는 비용은 일반적으로 매우 큰 것으로 나타났습니다.
* 로컬 디스크 하위 시스템은 스크래치 공간으로 사용됩니다. HDD 오류로 인해 데이터가 영구적으로 손실되지 않으므로 비용이 많이 들고 속도가 느리며 고가용성 시스템을 사용하지 않는 것이 좋습니다.

### 속도 고려 사항 {#section-01330be232894e08a526d8d82b7c4eb2}

Adobe은 다음을 포함하되 이에 제한되지 않는 다양한 요소가 데이터 처리 속도에 영향을 주므로 구성된 Data Workbench에서 데이터를 처리하는 속도에 대한 보증 또는 표현을 제공할 수 없습니다.

* 데이터 행 수
* 데이터 차원(열) 수
* 사용자 지정 처리 단계의 수 및 복잡성
* 클러스터링 사용
* 하드웨어 속도

## 파일 서버 단위 요구 사항{#file-server-unit-requirements}

서버의 FSU(File Serving Unit)는 Data Workbench의 기본 데이터 저장 및 관리 구성 요소입니다. FSU는 DPU에 대한 원시 소스 데이터의 파일 서버 역할을 하며 적절한 경우 DPU의 클러스터링을 조정합니다. 각 FSU에는 최대 5개의 DPU까지 소스 데이터를 제공할 수 있는 라이센스가 부여됩니다.

<table id="table_45CF36583DFE4536BB31F6A1F6CC181E">
 <thead>
  <tr>
   <th colname="col1" class="entry"> FSU 구성 요소 </th>
   <th colname="col2" class="entry"> 추천 항목 </th>
   <th colname="col3" class="entry"> </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> <p>운영 체제, CPU, RAM </p> </td>
   <td colname="col2"> <p>이러한 요구 사항은 DPU의 요구 사항과 동일합니다. 그러나 FSU의 경우 권장 사항을 따르지 않고 최소 요구 사항을 사용하는 것이 좋습니다. </p> </td>
   <td colname="col3"> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>디스크 시스템 </p> <p>FSU를 사용하려면 대용량 데이터를 위한 고가용성 이중 스토리지가 필요합니다. Adobe은 사용자와 협력하여 정확한 요구 사항을 결정합니다. </p> </td>
   <td colname="col1"> <p>Adobe 권장 사항: </p>
    <ul id="ul_FFEEE5052FFD4876BA9A6476DD096539">
     <li id="li_F98750D509D640C68885D53FC691ED43">(12 이상) * (750GB 이상) RAID 5/6 구성의 SATA HDD </li>
     <li id="li_3F84F63F9541476987015C27FDE8251B">100MB/s 이상의 지속 대역폭을 지원하는 고성능 SAN 연결 </li>
    </ul> <p>FSU는 원시 소스 데이터를 보유하므로 손실된 내용을 복구할 수 없으며 Adobe은 정기적으로 이 데이터를 백업하는 것을 권장합니다. </p> </td>
   <td colname="col2"> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>네트워크 성능 </p> </td>
   <td colname="col2"> <p>Adobe을 사용하려면 FSU와 DPU 간의 스위치 기가비트 이더넷 연결이 함께 작동해야 합니다. </p> </td>
   <td colname="col3"> </td>
  </tr>
 </tbody>
</table>

## 센서 요구 사항{#sensor-requirements}

Data Workbench 센서는 웹, 애플리케이션 및 데이터 수집 서버에서 모든 서버로 전송할 이벤트 데이터를 수집합니다. [!DNL Sensor’s] 계측에서는 인터넷 채널에서 발생하는 이벤트를 일관되게 정확하게 측정할 수 있습니다. [!DNL Sensor] 에서는 웹 서버 소프트웨어 및 운영 체제의 여러 조합을 지원합니다.

### 센서 시스템 Recommendations {#section-0a981c3a47b644c1a1a56974ba033b9c}

다음 표에서는 [!DNL Sensor]:

<table id="table_A132E06D6B8146C1B199B82464EA0898">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 기능 </th>
   <th colname="col2" class="entry"> 권장 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> <p>디스크 스토리지 </p> </td>
   <td colname="col2"> <p>최소 512MB </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>RAM </p> </td>
   <td colname="col2"> <p>32MB의 RAM을 사용할 수 있어야 함 <span class="wintitle"> Sensor </span> HTTP 또는 해당 호스트인 다른 서버 컴퓨터에서 실행 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>네트워크 성능 </p> </td>
   <td colname="col2"> <p>반복 서버에 대한 1Mbps 이상의 네트워크 연결 또는 <span class="keyword"> data workbench 서버 </span>. <span class="wintitle"> Sensor </span> 일반적으로 1Mbps보다 훨씬 적은 대역폭을 사용합니다. Adobe 컨설턴트는 일상적인 기준으로 필요한 실제 대역폭 양을 예측할 수 있도록 지원합니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>네트워크 포트 및 방화벽 </p> </td>
   <td colname="col2"> <p> <span class="wintitle"> Sensor </span> 에 연결 <span class="keyword"> data workbench 서버 </span> HTTPS 사용(일반적으로 구성 가능하지만 포트 443) 또는 HTTP(일반적으로 구성 가능하지만 포트 80). </p> <p>방화벽의 적절한 포트 <span class="wintitle"> Sensor </span> 타겟과 <span class="keyword"> data workbench 서버 </span> 또는 반복 서버는 각 서버 사이에 열려야 합니다 <span class="wintitle"> Sensor </span> 호스팅 컴퓨터 및 <span class="keyword"> data workbench 서버 </span> 또는 서버 시작 전 반복 <span class="wintitle"> Sensor </span> 설치 프로세스. <span class="wintitle"> Sensor </span> 는 단방향 HTTPS 또는 HTTP 연결을 <span class="keyword"> data workbench 서버 </span> 또는 반복 서버. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>네트워크 관리 시스템 </p> </td>
   <td colname="col2"> <p>기존 네트워크 관리 시스템은 기본 컴퓨터 하드웨어(예: 디스크 공간, 네트워크 서비스) 및 네트워크 연결과 Windows 이벤트 로그 또는 UNIX 시스템 로그를 모니터링해야 합니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>서버 시간 동기화 </p> </td>
   <td colname="col2"> <p>컴퓨터 시스템 시간이 컴퓨터를 호스트하는 모든 컴퓨터에서 연속적으로 동기화되는지 확인합니다. <span class="wintitle"> Sensor </span>. 웹 서버 응용 프로그램 및 컴퓨터 <span class="wintitle"> Sensor </span> 데이터에서 수집한 이벤트 데이터가 정확하려면 동기화된 시스템 시간이 있어야 합니다. NTP 또는 기타 시간 동기화 기능을 통해 시스템 시간을 지속적으로 동기화하는 단계는 운영 체제 설명서를 참조하십시오. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>DNS 이름 사용 </p> </td>
   <td colname="col2"> <p>Adobe은 <span class="wintitle"> 센서 </span> IP 주소 대신 DNS 이름을 사용하여 <span class="keyword"> data workbench 서버 </span> 또는 반복 서버. 다음의 경우 <span class="wintitle"> Sensor </span> 은 DNS 이름을 사용하여 호스트 웹 서버의 DNS 또는 로컬 호스트 파일을 구성하여 <span class="keyword"> data workbench 서버 </span> 또는 반복 서버. </p> </td>
  </tr>
 </tbody>
</table>

### 지원 서버 소프트웨어 {#section-d6071706539f49d9a861d87b98e6f382}

다음 표에는 [!DNL Sensor] 지원:

<table id="table_99EA23BBC1A148B49643F4B5E4341C08">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 웹 서버 소프트웨어 </th>
   <th colname="col2" class="entry"> 운영 체제 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> <p>Apache Server / IBM HTTP Server 2.2 </p> </td>
   <td colname="col2"> <p>Microsoft Windows Server 2003 이상 RedHat Enterprise Linux 6.x 이상 Sun Solaris 8.x 이상 IBM AIX 5.1x 이상 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Apache Server 2.4 </p> </td>
   <td colname="col2"> <p>RedHat Enterprise Linux 6.x 이상 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Microsoft IIS </p> </td>
   <td colname="col2"> <p>Microsoft Windows Server 2003 이상 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> <p>Java 애플리케이션 서버(Tomcat, JBoss, iPlanet, Weblogic) </p> </td>
   <td colname="col2"> <p>Microsoft Windows Server 2003 이상 RedHat Enterprise Linux 6.x 이상 Sun Solaris 8.x 이상 IBM AIX 5.1x 이상 </p> </td>
  </tr>
 </tbody>
</table>

다른 서버 및 운영 체제 조합의 경우 사용 가능 여부에 대한 Adobe을 참조하십시오. 의 일부 기능은 아님 [!DNL Sensor] 웹/애플리케이션 서버와 운영 체제의 모든 조합으로 사용할 수 있습니다. 특정 항목에 대한 자세한 정보 [!DNL Sensor] 릴리스는 Adobe 지원에 문의하십시오.

## 보고서 서버 요구 사항{#report-server-requirements}

Data Workbench 보고서 서버는 예약된 보고의 출력을 허용하는 구성 요소입니다. 출력되는 보고서는 파일 시스템에 배치된 .PNG 이미지 또는 .XLS 스프레드시트의 형식이나 전자 메일로 출력될 수 있습니다. 하드웨어 요구 사항은 [Data Workbench 클라이언트](https://experienceleague.adobe.com/docs/data-workbench/using/install/c-data-workbench-client-install.html?lang=ko-KR).

다음 요구 사항이에 해당됩니다 [!DNL report server]:

* 데이터 출력(네트워크 공유 또는 로컬 드라이브)을 위한 파일 시스템에 액세스합니다.
* 구성된 SMTP 서버에 대한 액세스 권한
* 에 설치된 Microsoft Excel 2003 이상 [!DNL report] server. 자세한 내용은 [Office의 서버측 자동화를 위한 고려 사항](https://support.microsoft.com/kb/257757) 추가 정보.

## 네트워크 관리{#network-management}

Adobe은 기존 네트워크 관리 시스템이 Data Workbench 플랫폼이 사용하는 하드웨어와 네트워크를 모니터링하도록 권장합니다.

또한 Adobe은 오류가 발생할 때 로 기록되는 FSU 및 DPU의 Windows 이벤트 로그를 모니터링하는 것을 권장합니다.

>[!NOTE]
>
>로그 파일을 호스팅하는 모든 네트워크 스토리지 시스템은 DPU당 최소 10MB의 지속적인 대역폭을 제공해야 합니다.

## 데이터 가용성{#data-availability}

서버 DPU가 데이터를 새로운 또는 새로 고친 데이터 세트에 처리하고 다시 처리하는 것이 일반적이고 필요한 방법입니다.

구성 변경, 데이터 소스 변경, 하드웨어 변경, 부적절한 구성, 하드웨어 장애, 소프트웨어 장애, 전원 장애 등으로 인해 이러한 문제가 발생할 수 있습니다. 이러한 처리 또는 재처리가 발생하면 DPU 및 FSU 구성 요소에서 모든 데이터 세트 및 시스템 데이터를 즉시 사용할 수 있어야 합니다. 이 요구 사항을 준수하지 않으면 시스템 다운타임이 발생하며,

## DPU 및 FSU 네트워크 문제{#dpu-and-fsu-network-issues}

DPU 및 FSU 네트워크를 사용할 때 고려해야 할 사항입니다.

* 네트워크 로그 파일 배포의 경우 로그 파일을 호스팅하는 모든 네트워크 스토리지 시스템은 DPU당 최소 10MB의 지속적인 대역폭을 제공해야 합니다.
* DPU, FSU 및 Data Workbench은 기본적으로 포트 80 또는 443에서 HTTP 또는 HTTPS를 통해 양방향 통신을 수행합니다. 포트를 선택적으로 구성할 수 있습니다.
* Data Workbench [!DNL Sensor(s)] 서버에 연결할 수 있어야 합니다(단방향).
* DPU에서 SMTP를 통해 경고 메시지를 보내도록 허용하려면 구성된 SMTP 서버에 연결할 수 있어야 합니다.
* Adobe은 IP 주소가 변경되는 경우 재구성을 방지하기 위해 FSU 및 DPU에 FSU01.CLIENT.COM과 같은 네트워크 이름을 지정할 것을 권장합니다.
