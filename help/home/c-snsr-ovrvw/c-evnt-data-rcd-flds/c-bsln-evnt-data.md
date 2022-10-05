---
description: 센서에서 기록한 기준 이벤트 데이터 레코드 필드에 대한 정보입니다.
title: 기준 이벤트 데이터 레코드 필드
uuid: aa36d332-089c-4ae2-98e2-a93d2fa023b7
exl-id: ad3d8806-863a-4871-a35b-6680163f00ac
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 2%

---

# 기준 이벤트 데이터 레코드 필드{#baseline-event-data-record-fields}

{{eol}}

센서에서 기록한 기준 이벤트 데이터 레코드 필드에 대한 정보입니다.

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
   <td colname="col2"> <p>요청과 함께 클라이언트가 보낸 쿠키입니다. </p> <p>예: v1st=42FDF66DE610CF36; ASPSESSIONIDQCATDQC=GPIBKEIBFBFIPLOJMCAEPM; </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(referrer) </td>
   <td colname="col2"> <p>클라이언트가 요청을 사용하여 서버에 보낸 HTTP 레퍼러 문자열입니다. </p> <p>예: https://www.mysite.net/cgi-bin/websearch?qry </p> <p>페이지 태그를 사용하는 경우 cs(레퍼러)는 HTTP 또는 HTTP를 포함하여 태그 이미지가 포함된 문서의 전체 URL입니다. </p> <p>또한 Apache(1.3, 2.0 및 2.2)와 IIS 센서를 구성하여 요청에 사용된 포트를 캡처할 수 있으며, 이 포트는 HTTP와 HTTPS 요청을 식별할 수 있습니다. </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs(user-agent) </td>
   <td colname="col2"> <p>클라이언트가 클라이언트에 보낸 사용자 에이전트의 유형을 나타내는 요청을 서버에 보내는 문자열입니다. </p> <p>예: Mozilla/5.0(Windows; U; Windows NT 5.1; 미국 rv:1.7) Gecko/20040707 Firefox/0.9.2 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs 메서드 </td>
   <td colname="col2"> <p>HTTP 요청의 메서드 유형입니다 </p> <p>예: GET </p> <p>참조: https://www.w3.org/TR/2000/NOTE-shoplogfileformat-20001115/#field_method </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-query </td>
   <td colname="col2"> <p>URI의 쿼리 문자열 부분(stem + 쿼리 문자열 = URI) </p> <p>앞에 물음표(?)가 있습니다 및 에는 앰퍼샌드(&amp;)로 구분된 하나 이상의 이름-값 쌍을 포함할 수 있습니다. </p> <p>예: page=homepage </p> </td>
  </tr>
  <tr>
   <td colname="col1"> cs-uri-stem </td>
   <td colname="col2"> <p>URI의 줄기 부분(stem + 쿼리 문자열 = URI) </p> <p>스템은 서버에서 요청된 리소스의 실제 또는 논리적 경로입니다. </p> <p>예: /index.asp </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc(content-type) </td>
   <td colname="col2"> <p>서버에서 보고한 대로 클라이언트가 요청하는 리소스의 컨텐츠 유형입니다. </p> <p>예: 텍스트/html, 이미지/png, 이미지/gif, 비디오/mpeg </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc-bytes </td>
   <td colname="col2"> <p>요청에 대한 응답으로 서버에서 클라이언트로 보낸 데이터 바이트 수입니다. </p> <p>예: 4996년 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> sc-status </td>
   <td colname="col2"> <p>서버가 클라이언트에 반환한 상태 코드입니다. </p> <p>예: 200년 </p> <p>참조: https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html </p> </td>
  </tr>
  <tr>
   <td colname="col1"> s-dns </td>
   <td colname="col2"> <p>요청된 리소스의 호스트의 정규화된 도메인 이름 또는 IP 주소입니다. </p> <p>예: www.omniture.com </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-실험 </td>
   <td colname="col2"> <p>요청 시 클라이언트가 구성원으로 있는 모든 통제 실험 이름 및 그룹의 목록입니다. </p> <p>예: Home_Exp.Group_1,Registration_Exp.Group_2 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-timestamp </td>
   <td colname="col2"> <p>서버에서 요청을 받은 날짜 및 시간(GMT)입니다. </p> <p>이 시간은 1600년 1월 1일 이후 100나노초 수로 표시됩니다. </p> <p>예: 127710989320000000 11에 대한 x-timestamp 값이 됩니다.:28:2005년 9월 13일 화요일 52.0000000 </p> </td>
  </tr>
  <tr>
   <td colname="col1"> x-trackingid </td>
   <td colname="col2"> <p>영구적 쿠키에 설정된 대로 찾은 고유한 브라우저 식별자의 64비트 16진수 값입니다. <span class="wintitle"> Sensor </span> 및 가 서버에 대한 요청을 통해 클라이언트가 제공합니다. </p> <p>예: 42FDF66DE610CF36 </p> </td>
  </tr>
 </tbody>
</table>

다음 [!DNL data workbench server] 기준 이벤트 데이터 레코드 필드에서 많은 변수를 파생시킬 수 있습니다. 자세한 내용은 *데이터 집합 구성 안내서*.
