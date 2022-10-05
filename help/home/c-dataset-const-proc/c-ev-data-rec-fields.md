---
description: Data Workbench 서버가 데이터 집합을 구성하기 위해 처리할 수 있는 데이터 필드에 대한 정보입니다.
title: 이벤트 데이터 레코드 필드
uuid: b0232bfa-0a3b-4e3d-876e-6a15a3764eae
exl-id: 35433b87-991a-4fb9-ba6a-3217e89eb769
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 2%

---

# 이벤트 데이터 레코드 필드{#event-data-record-fields}

{{eol}}

Data Workbench 서버가 데이터 집합을 구성하기 위해 처리할 수 있는 데이터 필드에 대한 정보입니다.

* [이벤트 데이터 정보](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-3a0705f8c1824017aa4effed9903efbe)
* [기준 이벤트 데이터 레코드 필드](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-a882ed7aa6af41eeb45a55bf8c1ca3d7)
* [파생 필드](../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#section-b6c57ee2aa31469fbd5dab90e52bc677)

## 이벤트 데이터 정보 {#section-3a0705f8c1824017aa4effed9903efbe}

데이터 집합을 만드는 데 사용되는 이벤트 데이터는 로그 소스라는 파일에 있습니다. 각 데이터 레코드는 연결된 타임스탬프가 있는 이벤트의 단일 인스턴스 또는 트랜잭션 레코드를 나타내므로 로그 소스에서 사용할 수 있는 데이터를 이벤트 데이터라고 합니다.

로그 소스의 이벤트 데이터는 [!DNL Sensors]. 에 의해 수집된 이벤트 데이터 [!DNL Sensors] http 및 애플리케이션 서버에서 는 Data Workbench 서버로 전송되며, 이 서버는 데이터를 압축 로그( [!DNL .vsl]) 파일로 내보낼 때 시간별 세부기간이 작동하지 않는 문제를 해결했습니다. 플랫 파일, XML 파일 또는 ODBC 데이터 소스에 있는 이벤트 데이터는 이러한 다른 형식에서 공통 데이터 필드 세트를 추출하도록 정의하는 디코더를 제공하는 Data Workbench 서버에서 읽습니다.

다음 섹션에서는 다음을 통해 수집된 데이터 필드(이벤트 데이터 레코드 필드 또는 로그 항목 필드라고 함)에 대한 정보를 제공합니다 [!DNL Sensors] 또는 data workbench 서버에서 읽고 사용할 수 있게 되었습니다.

>[!NOTE]
>
>필드의 이름은 일반적으로 W3C 확장 로그 파일 형식에 대한 이름 지정 규칙을 따릅니다. 많은 필드에 필드에 포함된 정보의 소스를 나타내는 접두사가 있습니다.

* cs는 클라이언트로부터 서버로의 통신을 나타냅니다.
* sc는 서버에서 클라이언트로의 통신을 나타냅니다.
* s는 서버의 정보를 나타냅니다.
* c 는 클라이언트의 정보를 나타냅니다.
* x는 Adobe 소프트웨어 제품이 만드는 정보를 나타냅니다.

## 기준 이벤트 데이터 레코드 필드 {#section-a882ed7aa6af41eeb45a55bf8c1ca3d7}

로그 ( [!DNL .vsl]) 파일에는 서버에서 수집되는 이벤트 데이터의 필드가 포함되어 있습니다 [!DNL Sensors] 데이터 집합 구성 프로세스에서 data workbench 서버에서 사용됩니다. 다음 표에는 [!DNL Sensor]:

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
   <td colname="col2"> <p>요청과 함께 클라이언트가 보낸 쿠키입니다. </p> <p> 예: v1st=42FDF66DE610CF36; ASPSESSIONIDQCATDQC=GPIBKEIBFBFIPLOJMCAEPM; </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(referrer) </td>
   <td colname="col2"> <p>클라이언트가 요청을 사용하여 서버에 보낸 HTTP 레퍼러 문자열입니다. </p> <p> 예: <span class="filepath"> https://www.mysite.net/cgi-bin/websearch?qry </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(user-agent) </td>
   <td colname="col2"> <p>클라이언트가 클라이언트에 보낸 사용자 에이전트의 유형을 나타내는 요청을 서버에 보내는 문자열입니다. </p> <p> 예: Mozilla/5.0(Windows; U; Windows NT 5.1; 미국 rv:1.7) Gecko/20040707 Firefox/0.9.2 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs 메서드 </td>
   <td colname="col2"> <p>HTTP 요청의 메서드 유형입니다. </p> <p> 예: GET </p> <p> 참조: <span class="filepath"> https://www.w3.org/TR/2000/NOTE-shoplogfileformat-20001115/#field_method </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-query </td>
   <td colname="col2"> <p>URI의 쿼리 문자열 부분(stem + 쿼리 문자열 = URI). 앞에 물음표(?)가 있습니다 및 에는 앰퍼샌드(&amp;)로 구분된 하나 이상의 이름-값 쌍을 포함할 수 있습니다. </p> <p> 예: page=homepage </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-stem </td>
   <td colname="col2"> <p>URI의 줄기부(stem + 쿼리 문자열 = URI). 스템은 서버에서 요청된 리소스의 실제 또는 논리적 경로입니다. </p> <p> 예: <span class="filepath"> /index.asp </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc(content-type) </td>
   <td colname="col2"> <p>서버에서 보고한 대로 클라이언트가 요청하는 리소스의 컨텐츠 유형입니다. </p> <p> 예: 텍스트/html, 이미지/png, 이미지/gif, 비디오/mpeg </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc-bytes </td>
   <td colname="col2"> <p>요청에 대한 응답으로 서버에서 클라이언트로 전송되는 데이터의 바이트 수입니다 </p> <p> 예: 4996년 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc-status </td>
   <td colname="col2"> <p>서버가 클라이언트에 반환한 상태 코드입니다. </p> <p> 예: 200년 </p> <p> 참조: <span class="filepath"> https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> s-dns </td>
   <td colname="col2"> <p>요청된 리소스의 호스트의 정규화된 도메인 이름 또는 IP 주소입니다. </p> <p> 예: <span class="filepath"> www.adobe.com </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-실험 </td>
   <td colname="col2"> <p>요청 시 클라이언트가 구성원으로 있는 모든 통제 실험 이름 및 그룹의 목록입니다. </p> <p> 예: VSHome_Exp.Group_1,VSRegiation_Exp.Group_2 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-timestamp </td>
   <td colname="col2"> <p>서버에서 요청을 받은 날짜 및 시간(GMT)입니다. 이 시간은 1600년 1월 1일 이후 100나노초 수로 표시됩니다. </p> <p> 예: 127710989320000000 11에 대한 x-timestamp 값이 됩니다.:28:2005년 9월 13일 화요일 52.0000000 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-trackingid </td>
   <td colname="col2"> <p>영구적 쿠키에 설정된 대로 찾은 고유한 브라우저 식별자의 64비트 16진수 값입니다. <span class="wintitle"> Sensor </span> 및 가 서버에 대한 요청을 통해 클라이언트가 제공합니다. </p> <p> 예: 42FDF66DE610CF36 </p> </td>
  </tr>
 </tbody>
</table>

## 파생 필드 {#section-b6c57ee2aa31469fbd5dab90e52bc677}

아래 표에는 기준 이벤트 데이터 레코드 필드에서 Data Workbench 서버가 파생된 필드의 예가 나와 있습니다.

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
   <td colname="col2"> 쿠키 내에 지정된 이름-값 쌍의 값입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> cs(referrer-domain) </td>
   <td colname="col2"> <p>HTTP 참조 URI의 도메인 이름 또는 IP 주소입니다. </p> <p> <p>참고: 이 필드는 읽기 전용입니다. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(referrer-host) </td>
   <td colname="col2"> <p>레퍼러의 전체 호스트 이름. </p> <p> 예: cs(referrer)가 <span class="filepath"> https://my.domain.com/my/page </span>, cs(referrer-host)는 <span class="filepath"> my.domain.com </span>. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(referrer-query)(name) </td>
   <td colname="col2"> <p>레퍼러 쿼리 문자열의 값입니다. </p> <p> <p>참고: cs(referrer)(name) 필드를 사용하여 레퍼러 쿼리 문자열 값에 액세스할 수 없습니다. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri </td>
   <td colname="col2"> <p>전체 URI(stem + 쿼리 문자열 = 전체 URI)입니다. </p> <p> 예: <span class="filepath"> /shopping/checkout.html?product1=8Track&amp;product2=cassette&amp;product3=cd </span> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-query(name) </td>
   <td colname="col2"> <p>지정된 이름과 연결된 값입니다. 지정된 이름에 여러 값이 있는 경우 이 필드는 해당 값의 마지막 값을 반환합니다. </p> 예:
    <ul id="ul_47BBB2E3076A46629BFCDB2A460F700B">
     <li id="li_AC9BB29505A54AE4AFF49438530C9EA4"> URI의 경우 <span class="filepath"> /shopping/checkout.html?product1=8Track&amp;product2=cassette&amp;product3=cd </span>, cs-uri-query(product3)는 cd를 반환합니다. </li>
     <li id="li_B036C1D0B25748E0A155DDC9B1B999CB"> URI의 경우 <span class="filepath"> /shopping/checkout.html?product1=8Track&amp;product1=cassette </span>, <span class="wintitle"> cs-uri-query(product1) </span> 카세트가 반환될 겁니다 </li>
    </ul> <p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> ctime </td>
   <td colname="col2"> x 타임스탬프가 1970년 1월 1일 이후 초 수로 표시됩니다. 이 필드를 x-unixtime이라고도 합니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 날짜 </td>
   <td colname="col2"> YYYY-MM-DD 형식의 x-타임스탬프입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> 시간 </td>
   <td colname="col2"> HH 형식의 x 타임스탬프:MM:SS. </td>
  </tr>
  <tr>
   <td colname="col1"> x-local-timestring </td>
   <td colname="col2"> <p>x 타임스탬프가 <span class="filepath"> Transformation.cfg </span> 데이터 세트에 대한 파일입니다. 형식은 YYYY-MM-DD HH입니다:MM:음.. </p> <p> <p>참고: 에서 x-local-timestring과 같은 시간 전환을 정의할 수도 있습니다 <span class="filepath"> Log Processing.cfg </span> 파일. 자세한 내용은 <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 로그 처리 구성 파일 </a>. </p> </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-log-source-id </td>
   <td colname="col2"> <p>특정 로그 항목의 로그 소스에 해당하는 식별자입니다. 식별자를 기록하려면 ID를에서 지정해야 합니다. <span class="wintitle"> 로그 소스 ID </span> 필드 <span class="filepath"> Log Processing.cfg </span> 정의할 때 파일 <span class="wintitle"> Sensor </span>, 로그 파일 또는 ODBC 데이터 소스 자세한 내용은 <a href="../../home/c-dataset-const-proc/c-log-proc-config-file/c-abt-log-proc-config-file.md"> 로그 처리 구성 파일 </a>. </p> <p> 예: VSensor01. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-mask </td>
   <td colname="col2"> 마스크의 패턴 <span class="wintitle"> Sensor </span> 데이터 소스(에서 파생됨) <span class="filepath"> .vsl </span> 파일 이름). 파일 이름이 <span class="filepath"> YYYMMDD-SENSORID.VSL </span>, x-mask 는 SENSORID입니다. </td>
  </tr>
  <tr>
   <td colname="col1"> x-timestring </td>
   <td colname="col2"> YYYY-MM-DD HH 형식의 x-타임스탬프:MM:음.. </td>
  </tr>
  <tr>
   <td colname="col1"> x-unixtime </td>
   <td colname="col2"> x-timestamp에서 파생된 십진수 UNIX 시간입니다. </td>
  </tr>
 </tbody>
</table>

[!DNL Sensor]서버에서 를 사용하는 경우 는 유효한 HTTP 요청 또는 응답 헤더에서 이벤트 데이터의 필드를 수집하거나 서버의 API를 통해 사용할 수 있는 변수에서 수집할 수 있습니다. 이러한 데이터 필드를 수집하려면, [!DNL txlogd.conf]구성 파일 [!DNL Sensor]. 자세한 내용은 *Data Workbench [!DNL Sensor] 안내서*.
