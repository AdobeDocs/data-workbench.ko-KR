---
description: 수집기 모듈, 전송기 프로세스, 구성 파일 등과 같은 Sensor UNIX 파일 권한에 대한 정보입니다.
title: Sensor UNIX 파일 권한
uuid: 04d159b5-6569-48b6-a2db-9a0b40118ffe
exl-id: 07cbc7df-c628-437d-9ca1-b006da8de242
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 5%

---

# Sensor UNIX 파일 권한{#sensor-unix-file-permissions}

{{eol}}

수집기 모듈, 전송기 프로세스, 구성 파일 등과 같은 Sensor UNIX 파일 권한에 대한 정보입니다.

## 컬렉터 모듈 {#section-49c855baece24c4695184bfcbeeddebf}

<table id="table_0B972ABD2A5342CA8A6FE80EB666298A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 품질 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>파일 이름 </p> </td> 
   <td colname="col2"> <p>mod_visual_sciences.so(Apache 웹 서버 및 IBM HTTP 서버) </p> <p>libvisual_sciences.so 및 J2EECollector.jar(J2EE 애플리케이션 서버의 경우) </p> <p>aol_visual_sciences.so (AOL 웹 서버에서) </p> <p>saf_visual_sciences.so(Sun Java 웹 서버) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>기본 권한 </p> </td> 
   <td colname="col2"> <p>rwx r-x r-x(IBM HTTP 및 Apache 1.3.x) </p> <p>rwx rwx r-x(Apache 2.0.x) </p> <p>rwx —x (J2EE, AOL 및 Sun Java 웹 서버) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>읽은 사람 </p> </td> 
   <td colname="col2"> <p>경우에 따라 루트 사용자로 실행되지만 특정 사용자 계정에서 실행되는 웹 서버입니다 </p> <p>웹 서버가 루트가 아닌 계정으로 실행되는 경우 이 파일에 대한 권한을 통해 해당 계정이 해당 계정을 읽을 수 있도록 해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다음으로 실행 </p> </td> 
   <td colname="col2"> <p>웹 서버의 하위 프로세스 </p> <p>하위 프로세스는 웹 서버 구성에 지정된 사용자 계정에서 실행됩니다. 많은 서버에서 "nobody"라고 하는 매우 제한된 권한을 가진 특별 계정이지만 모든 웹 서버에서 이 계정을 사용하는 것은 아닙니다. 웹 서버의 구성 파일을 확인하여 설정된 사용자 계정을 확인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>다음에서 읽기 </p> </td> 
   <td colname="col2"> <p>txlogd.conf </p> <p>diskQueue 파일 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 쓰기 대상 </td> 
   <td colname="col2"> diskQueue 파일 </td> 
  </tr> 
 </tbody> 
</table>

## 송신기 프로세스 {#section-8af432472e9d4bd9a42270bf27adf33a}

<table id="table_3028CC9640D54016BD8CA7F9CAA34280"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 품질 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 파일 이름 </td> 
   <td colname="col2"> trust_ca_cert.pem </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>기본 권한 </p> </td> 
   <td colname="col2"> <p>rw- r— r—(IBM HTTP, AOL 및 Sun Java 웹 서버) </p> <p>rw-rw-r—(Apache 웹 서버 및 J2EE 애플리케이션 서버) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 읽은 사람 </td> 
   <td colname="col2"> 송신기 프로그램 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작성자 </td> 
   <td colname="col2"> — </td> 
  </tr> 
 </tbody> 
</table>

## 구성 파일 {#section-341d85f2abf34a69970a0ff91b7e9123}

<table id="table_79AC614F5435443CB3CFB457B8375704"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 품질 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 파일 이름 </td> 
   <td colname="col2"> txlogd.conf </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>기본 권한 </p> </td> 
   <td colname="col2"> <p>rw- r— r—(IBM HTTP, AOL 및 Sun Java 웹 서버) </p> <p>rw-rw-r—(Apache 웹 서버 및 J2EE 애플리케이션 서버) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 읽은 사람 </td> 
   <td colname="col2"> <p>컬렉터 모듈 </p> <p>송신기 프로그램 </p> <p>센서 설치, 구성 및 유지 관리를 담당하는 관리자 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작성자 </td> 
   <td colname="col2"> 센서 설치, 구성 및 유지 관리를 담당하는 관리자 </td> 
  </tr> 
 </tbody> 
</table>

## 인증 기관 파일 {#section-2818dff887b8456992bdc589fd8510f3}

<table id="table_ED8BEEEFA91245C3A6645D27B148A5A7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 품질 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 파일 이름 </td> 
   <td colname="col2"> trust_ca_cert.pem </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>기본 권한 </p> </td> 
   <td colname="col2"> <p>rw- r— r—(IBM HTTP, AOL 및 Sun Java 웹 서버) </p> <p>rw-rw-r—(Apache 웹 서버 및 J2EE 애플리케이션 서버) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 읽은 사람 </td> 
   <td colname="col2"> 송신기 프로그램 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작성자 </td> 
   <td colname="col2"> — </td> 
  </tr> 
 </tbody> 
</table>

## 디스크 큐 {#section-0407c52744de41af867d0b7933a69256}

<table id="table_35DB32228E7443FF90BE24AB14CBE54B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 품질 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 파일 이름 </td> 
   <td colname="col2"> 사용자 정의 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기본 권한 </td> 
   <td colname="col2"> rw- rw-(모든 서버 유형) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>읽은 사람 </p> </td> 
   <td colname="col2"> <p>컬렉터 모듈 </p> <p>송신기 프로그램 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>작성자 </p> </td> 
   <td colname="col2"> <p>컬렉터 모듈 </p> <p>송신기 프로그램 </p> </td> 
  </tr> 
 </tbody> 
</table>
