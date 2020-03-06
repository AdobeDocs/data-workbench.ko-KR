---
description: 데이터 워크벤치 서버가 데이터 세트를 구성하기 위해 처리할 수 있는 데이터 필드에 대한 정보입니다.
solution: Analytics
title: 이벤트 데이터 레코드 필드
topic: Data workbench
uuid: b0232bfa-0a3b-4e3d-876e-6a15a3764eae
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 이벤트 데이터 레코드 필드{#event-data-record-fields}

데이터 워크벤치 서버가 데이터 세트를 구성하기 위해 처리할 수 있는 데이터 필드에 대한 정보입니다.

* [이벤트 데이터 정보](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-3a0705f8c1824017aa4effed9903efbe)
* [기준 이벤트 데이터 레코드 필드](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-a882ed7aa6af41eeb45a55bf8c1ca3d7)
* [파생 필드](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-b6c57ee2aa31469fbd5dab90e52bc677)

## 이벤트 데이터 정보 {#section-3a0705f8c1824017aa4effed9903efbe}

데이터 세트를 작성하는 데 사용되는 이벤트 데이터는 로그 소스라는 파일에 있습니다. 각 데이터 레코드는 연결된 타임스탬프가 있는 이벤트의 단일 인스턴스 또는 거래 레코드를 나타내므로 로그 소스에서 사용할 수 있는 데이터를 이벤트 데이터라고 합니다.

로그 소스의 이벤트 데이터는 실시간으로 수집됩니다 [!DNL Sensors]. HTTP 및 응용 프로그램 서버에서 수집된 이벤트 데이터는 데이터 워크벤치 서버로 전송되어 데이터를 압축 로그( [!DNL Sensors] [!DNL .vsl]) 파일로 변환합니다. 플랫 파일, XML 파일 또는 ODBC 데이터 소스에 있는 이벤트 데이터는 이러한 다른 형식에서 일반적인 데이터 필드 집합을 추출하도록 정의하는 디코더를 제공하는 데이터 워크벤치 서버에서 읽습니다.

다음 섹션에서는 데이터 워크벤치 서버에서 [!DNL Sensors] 읽거나 사용할 수 있도록 만들어진 데이터 필드(이벤트 데이터 레코드 필드 또는 로그 입력 필드)에 대한 정보를 제공합니다.

>[!NOTE]
>
>필드의 이름은 일반적으로 W3C 확장 로그 파일 형식에 대한 이름 지정 규칙을 따릅니다. 필드의 대부분은 필드에 포함된 정보의 소스를 나타내는 접두사가 있습니다.

* cs는 클라이언트에서 서버로의 통신을 나타냅니다.
* sc는 서버에서 클라이언트로의 통신을 나타냅니다.
* s는 서버의 정보를 나타냅니다.
* c는 클라이언트의 정보를 나타냅니다.
* x는 Adobe 소프트웨어 제품이 만든 정보를 나타냅니다.

## 기준 이벤트 데이터 레코드 필드 {#section-a882ed7aa6af41eeb45a55bf8c1ca3d7}

로그( [!DNL .vsl]) 파일에는 데이터 집합 구성 프로세스의 데이터 워크벤치 서버에서 수집된 [!DNL Sensors] 이벤트 데이터 필드가 들어 있습니다. 다음 표에는 일반적인 이벤트 데이터 레코드의 필드가 기록되어 [!DNL Sensor]있습니다.

<table id="table_98E135FE4EAF44D6ADEB3C6C1C0BF6A4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> c-ip </td> 
   <td colname="col2"> <p>서버에 대한 요청에 포함된 클라이언트의 IP 주소입니다. </p> <p> 예: 207.68.146.68 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(cookie) </td> 
   <td colname="col2"> <p>요청과 함께 클라이언트가 보낸 쿠키입니다. </p> <p> 예:v1st=42FDF66DE610CF36;ASPSESSIONIDQCATDQC=GPIBKEIBFBFIPLIJMKCAEPM; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(referrer) </td> 
   <td colname="col2"> <p>클라이언트가 요청과 함께 서버로 보낸 HTTP 레퍼러 문자열. </p> <p> 예:http://www.mysite.net/cgi-bin/websearch?qry <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(user-agent) </td> 
   <td colname="col2"> <p>클라이언트가 클라이언트에 어떤 유형의 사용자 에이전트 유형을 나타내는 요청을 서버에 보낸 문자열입니다. </p> <p> 예:Mozilla/5.0(Windows;U;Windows NT 5.1;en-US;rv:1.7) Gecko/20040707 Firefox/0.9.2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-method </td> 
   <td colname="col2"> <p>HTTP 요청의 메서드 유형입니다. </p> <p> 예:GET </p> <p> 참조:http://www.w3.org/TR/2000/NOTE-shoplogfileformat-20001115/#field_method <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> <p>URI의 쿼리 문자열 부분(stem + 쿼리 문자열 = URI). 앞에 물음표(?)가 표시됩니다. 앰퍼샌드(&amp;)로 구분된 하나 이상의 이름-값 쌍을 포함할 수 있습니다. </p> <p> 예:page=homepage </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-stem </td> 
   <td colname="col2"> <p>URI의 시스템 부분(stem + 쿼리 문자열 = URI). 시스템은 서버에서 요청된 리소스의 실제 또는 논리적 경로입니다. </p> <p> 예:/index.asp <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc(content-type) </td> 
   <td colname="col2"> <p>서버에서 보고한 클라이언트에서 요청하는 리소스의 컨텐츠 유형입니다. </p> <p> 예:text/html, image/png, image/gif, video/mpeg </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc-bytes </td> 
   <td colname="col2"> <p>요청에 대한 응답으로 서버에서 클라이언트로 전송된 데이터의 바이트 수 </p> <p> 예: 4996 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc-status </td> 
   <td colname="col2"> <p>서버에서 클라이언트에 반환된 상태 코드입니다. </p> <p> 예: 200 </p> <p> 참조:http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s-dns </td> 
   <td colname="col2"> <p>요청된 리소스의 호스트의 정규화된 도메인 이름 또는 IP 주소입니다. </p> <p> 예:www.adobe.com <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-experiment </td> 
   <td colname="col2"> <p>클라이언트가 요청 시 구성원인 모든 제어 실험 이름 및 그룹 목록입니다. </p> <p> 예:VSH 파섹 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-timestamp </td> 
   <td colname="col2"> <p>서버에서 요청을 받은 날짜 및 시간(GMT)입니다. 이 시간은 1600년 1월 1일 이후 100나노초 수로 표현됩니다. </p> <p> 예:1271098932000000은 2005년 9월 13일 화요일에 11:28:52.000000의 x-timestamp 값이 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-trackingid </td> 
   <td colname="col2"> <p>센서가 설정해서 클라이언트가 서버에 대한 요청을 가지고 제공한 영구 쿠키에 있는 고유 브라우저 식별자의 64비트 <span class="wintitle"> 16진수 </span> 값입니다. </p> <p> 예:42FDF66DE610CF36 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 파생 필드 {#section-b6c57ee2aa31469fbd5dab90e52bc677}

아래 표에는 기준 이벤트 데이터 레코드 필드에서 데이터 워크벤치 서버에서 파생된 필드의 예가 나와 있습니다.

<table id="table_3B008F1314804A69AE69E8F94908F497"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> cs(cookie)(name) </td> 
   <td colname="col2"> 쿠키 내의 지정된 이름-값 쌍의 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(referrer-domain) </td> 
   <td colname="col2"> <p>HTTP 참조 URI의 도메인 이름 또는 IP 주소입니다. </p> <p> <p>참고: 이 필드는 읽기 전용입니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(referrer-host) </td> 
   <td colname="col2"> <p>레퍼러의 전체 호스트 이름입니다. </p> <p> 예:cs(referrer)가 <span class="filepath"> http://my.domain.com/my/page인 </span>경우 cs(referrer-host)는 <span class="filepath"> my.domain.com </span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(referrer-query)(name) </td> 
   <td colname="col2"> <p>레퍼러 쿼리 문자열의 값입니다. </p> <p> <p>참고: cs(referrer)(name) 필드를 사용하여 레퍼러 쿼리 문자열 값에 액세스할 수 없습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri </td> 
   <td colname="col2"> <p>전체 URI(stem + 쿼리 문자열 = 전체 URI)입니다. </p> <p> 예:/shopping/checkout.html?product1=8Track&amp;product2=casette&amp;product3=cd <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query(name) </td> 
   <td colname="col2"> <p>지정된 이름과 연결된 값입니다. 지정된 이름에 여러 값이 있으면 이 필드는 해당 값의 마지막 값을 반환합니다. </p> 예: 
    <ul id="ul_47BBB2E3076A46629BFCDB2A460F700B"> 
     <li id="li_AC9BB29505A54AE4AFF49438530C9EA4"> URI /shopping/checkout.html? <span class="filepath"> product1=8Track&amp;product2=casette&amp;product3=cd </span>의 경우 cs-uri-query(product3)가 cd를 반환합니다. </li> 
     <li id="li_B036C1D0B25748E0A155DDC9B1B999CB"> URI /shopping/checkout.html? <span class="filepath"> ?product1=8Track&amp;product1=casette </span>의 경우 <span class="wintitle"> cs-uri-query(product1) </span> 가 casette를 반환합니다. </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ctime </td> 
   <td colname="col2"> 1970년 1월 1일 이후 초 단위로 표현된 x-timestamp 이 필드를 x-unixtime이라고도 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> date </td> 
   <td colname="col2"> yyyy-MM-DD 형식의 x-timestamp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> time </td> 
   <td colname="col2"> HH:MM:SS 형식의 x 타임스탬프 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-local-timestring </td> 
   <td colname="col2"> <p>데이터 세트에 대한 Transformation.cfg 파일에 지정된 <span class="filepath"> 로컬 </span> 시간대로 변환된 x-timestamp 형식은 YYYY-MM-DD HH:MM:SS.mmm입니다. </p> <p> <p>참고: Log Processing.cfg <span class="filepath"> </span> 파일에서 x-local-timestring과 같은 시간 변환을 정의할 수도 있습니다. 자세한 내용은 로그 처리 <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 구성 파일을 참조하십시오 </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-log-source-id </td> 
   <td colname="col2"> <p>특정 로그 항목의 로그 소스에 해당하는 식별자입니다. 식별자를 기록하려면 센서, 로그 파일 또는 ODBC 데이터 <span class="wintitle"> 소스를 정의할 때 Log Processing.cfg </span> 파일의 <span class="filepath"> Log Source ID </span> 필드에 식별자를 지정해야 <span class="wintitle"> 합니다 </span>. 자세한 내용은 로그 처리 <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 구성 파일을 참조하십시오 </a>. </p> <p> 예:출처: VSensor01. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-mask </td> 
   <td colname="col2"> 센서 데이터 소스의 마스크 <span class="wintitle"> 패턴입니다(.vsl </span> <span class="filepath"> </span> 파일 이름에서 파생된). 이름이 YYYYYMMDD-SENDORID.VSL 포맷인 파일의 경우 <span class="filepath"> x- </span>mask는 SENDORID입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-timestring </td> 
   <td colname="col2"> yyyy-MM-DD HH:MM:SS.mmm 형식의 x-timestamp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-unixtime </td> 
   <td colname="col2"> x-timestamp에서 파생된 십진수 UNIX 시간입니다. </td> 
  </tr> 
 </tbody> 
</table>

[!DNL Sensor], when used on a server, can collect fields of event data from any valid HTTP request or response header or variable available to it through the server&#39;s API. 이러한 데이터 필드를 수집하려면 [!DNL txlogd.conf]구성 파일에서 원하는 헤더 필드 또는 변수를 지정해야 [!DNL Sensor]합니다. For more information, see the *Data Workbench[!DNL Sensor]Guide*.
