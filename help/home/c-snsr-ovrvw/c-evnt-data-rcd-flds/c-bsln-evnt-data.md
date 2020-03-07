---
description: 센서가 기록한 기준 이벤트 데이터 레코드 필드에 대한 정보입니다.
solution: Insight
title: 기준 이벤트 데이터 레코드 필드
uuid: aa36d332-089c-4ae2-98e2-a93d2fa023b7
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 기준 이벤트 데이터 레코드 필드{#baseline-event-data-record-fields}

센서가 기록한 기준 이벤트 데이터 레코드 필드에 대한 정보입니다.

<table id="table_E29606BB010E4DB48C463979B7BEC769"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> c-ip </td> 
   <td colname="col2"> <p>서버에 대한 요청에 포함된 클라이언트의 IP 주소입니다. </p> <p>예: 207.68.146.68 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(cookie) </td> 
   <td colname="col2"> <p>요청과 함께 클라이언트가 보낸 쿠키입니다. </p> <p>예:v1st=42FDF66DE610CF36;ASPSESSIONIDQCATDQC=GPIBKEIBFBFIPLIJMKCAEPM; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(referrer) </td> 
   <td colname="col2"> <p>클라이언트가 요청과 함께 서버로 보낸 HTTP 레퍼러 문자열. </p> <p>예:http://www.mysite.net/cgi-bin/websearch?qry </p> <p>페이지 태그를 사용하는 경우 cs(referrer)는 HTTP 또는 HTTP를 포함하여 태그 이미지가 포함된 문서의 전체 URL입니다. </p> <p>또한 Apache(1.3, 2.0 및 2.2) 및 IIS 센서가 요청에 사용되는 포트를 캡처하도록 구성하여 HTTP와 HTTPS 요청을 식별할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(user-agent) </td> 
   <td colname="col2"> <p>클라이언트가 클라이언트에 어떤 유형의 사용자 에이전트 유형을 나타내는 요청을 서버에 보낸 문자열입니다. </p> <p>예:Mozilla/5.0(Windows;U;Windows NT 5.1;en-US;rv:1.7) Gecko/20040707 Firefox/0.9.2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-method </td> 
   <td colname="col2"> <p>HTTP 요청의 메서드 유형 </p> <p>예:GET </p> <p>참조:http://www.w3.org/TR/2000/NOTE-shoplogfileformat-20001115/#field_method </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> <p>URI의 쿼리 문자열 부분(stem + 쿼리 문자열 = URI) </p> <p>앞에 물음표(?)가 표시됩니다. 앰퍼샌드(&amp;)로 구분된 하나 이상의 이름-값 쌍을 포함할 수 있습니다. </p> <p>예:page=homepage </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-stem </td> 
   <td colname="col2"> <p>URI의 시스템 부분(stem + 쿼리 문자열 = URI) </p> <p>시스템은 서버에서 요청된 리소스의 실제 또는 논리적 경로입니다. </p> <p>예:/index.asp </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc(content-type) </td> 
   <td colname="col2"> <p>서버에서 보고한 클라이언트에서 요청하는 리소스의 컨텐츠 유형입니다. </p> <p>예:text/html, image/png, image/gif, video/mpeg </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc-bytes </td> 
   <td colname="col2"> <p>요청에 대한 응답으로 서버에서 클라이언트로 전송된 데이터의 바이트 수입니다. </p> <p>예: 4996 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc-status </td> 
   <td colname="col2"> <p>서버에서 클라이언트에 반환된 상태 코드입니다. </p> <p>예: 200 </p> <p>참조:http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> s-dns </td> 
   <td colname="col2"> <p>요청된 리소스의 호스트의 정규화된 도메인 이름 또는 IP 주소입니다. </p> <p>예:www.omniture.com </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-experiment </td> 
   <td colname="col2"> <p>클라이언트가 요청 시 구성원인 모든 제어 실험 이름 및 그룹 목록입니다. </p> <p>예:Home_Exp.Group_1,Registration_Exp.Group_2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-timestamp </td> 
   <td colname="col2"> <p>서버에서 요청을 받은 날짜 및 시간(GMT)입니다. </p> <p>이 시간은 1600년 1월 1일 이후 100나노초 수로 표현됩니다. </p> <p>예:1271098932000000은 2005년 9월 13일 화요일에 11:28:52.000000의 x-timestamp 값이 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> x-trackingid </td> 
   <td colname="col2"> <p>센서가 설정해서 클라이언트가 서버에 대한 요청을 가지고 제공한 영구 쿠키에 있는 고유 브라우저 식별자의 64비트 <span class="wintitle"> 16진수 </span> 값입니다. </p> <p>예:42FDF66DE610CF36 </p> </td> 
  </tr> 
 </tbody> 
</table>

기준 이벤트 데이터 레코드 필드에서 여러 변수를 파생시킬 [!DNL data workbench server] 수 있습니다. For more information, see the *Dataset Configuration Guide*.
