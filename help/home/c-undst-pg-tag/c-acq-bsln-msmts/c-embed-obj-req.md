---
description: 브라우저가 페이지의 HTML을 요청한 후 브라우저는 브라우저에서 브라우저에서 브라우저가 표시하는 페이지를 채우도록 해당 페이지의 HTML에 참조된 포함된 개체를 웹 서버에서 요청합니다.
solution: Analytics
title: 포함된 개체 요청(페이지 태그) 가져오기
topic: Data workbench
uuid: 7fe561d1-aa5a-4ac9-82ba-aa27c7d208dd
translation-type: tm+mt
source-git-commit: 8f5c69541bdd97aefbad3840f75f06846615f222
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 4%

---


# 포함된 개체 요청(페이지 태그) 가져오기{#acquiring-embedded-object-requests-page-tags}

브라우저가 페이지의 HTML을 요청한 후 브라우저는 브라우저에서 브라우저에서 브라우저가 표시하는 페이지를 채우도록 해당 페이지의 HTML에 참조된 포함된 개체를 웹 서버에서 요청합니다.

이러한 임베디드 객체 요청은 오늘날 인터넷에서 사용되는 수백 또는 수천 종류의 임베디드 개체가 있더라도 이미지 파일 또는 JavaScript 파일에 대한 가장 일반적으로 요청입니다. 이러한 포함된 개체 요청 중 대부분은 일반적으로 인터넷 사이트의 비즈니스 활동을 분석하거나 보고하는 데 유용하지 않습니다.따라서 광고 표시나 사이트 활동 측정 등 특정 비즈니스 목적을 가지고 있지 않은 경우 이러한 요청이 많으면 인수에는 바람직하지 않습니다.

예를 들어, 이미지는 광고일 수 있으며 광고가 방문자에게 깊은 인상을 주었음을 알고 싶을 수 있습니다. JavaScript 코드 조각은 특정 브라우저가 특정 특성을 가지고 있고 이를 획득하기 위해 JavaScript 코드 조각에 다시 전달하는 데 사용할 수 [!DNL Sensor] 있습니다. 사이트의 각 페이지에는 10개 또는 100개의 포함된 개체 요청이 있을 수 있습니다. 사이트가 이러한 각 요청에 대한 로그 정보를 저장하는 경우, 향후 분석에 사용할 수 있는 로그 데이터를 유지하는 데 필요한 데이터 저장소의 양에 요청된 각 페이지에 대한 포함된 개체 요청 수를 곱합니다. 따라서 불필요한 스토리지 비용을 발생시키기 전에 분석에 중요한 요청을 유지하고 다른 요청을 삭제할 [!DNL Site] 수 있습니다.

포함된 개체 요청 URL의 쿼리 문자열에 [!DNL Sensor] &quot;Log=1&quot;을 추가하는 컨텐츠 유형 필터링 기능에 제공된 무시 기능을 사용하면 사이트 관리자가 해당 유형의 모든 요청을 저장할 필요 없이 특정 포함된 개체 요청 및 관련 측정 데이터를 가져올 수 있습니다(예: 모든 `<image>` 요청).

[!DNL Sensor] 웹 서버에서 수행된 포함된 각 개체 요청에 대해 다음 표에 있는 측정 데이터 [!DNL Sensor] 를 수집합니다. 이는 필터링하도록 구성되지 않았거나 필터가 무시되었다고 가정합니다. 수집된 정보는 x-trackingid 또는 cs(cookie) 로그 필드 항목을 통해 방문자 및 세션 및 후속 세션과 관련되어 있습니다.

<table id="table_11BE08A798E743EC8E76F738F0CE5884"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> W3C 이름 </th> 
   <th colname="col2" class="entry"> 수집된 데이터 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
   <th colname="col4" class="entry"> 예 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> x-trackingid </td> 
   <td colname="col2"> 추적 식별자(고유 방문자) </td> 
   <td colname="col3"> 초기 요청 시 Sensor가 사용자의 브라우저에 배치된 쿠키에서 읽은 <span class="wintitle"> </span> 식별자 </td> 
   <td colname="col4"> V1st=3C94007B4E01F9C2 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>날짜 </p> <p>시간 </p> </td> 
   <td colname="col2"> 타임스탬프 </td> 
   <td colname="col3"> 서버에서 요청이 처리된 시간(정확히 100ns)정확성은 서버 환경 및 NTP에 따라 다름) </td> 
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
   <td colname="col4"> 200 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-stem </td> 
   <td colname="col2"> URI 시스템 </td> 
   <td colname="col3"> 클라이언트가 요청한 URI의 "stem" 부분 </td> 
   <td colname="col4"> pagedir/page.asp </td> 
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
   <td colname="col4"> <span class="filepath"> www.domain.com </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(referrer) </td> 
   <td colname="col2"> 참조 URL </td> 
   <td colname="col3"> 클라이언트가 보낸 HTTP 레퍼러 필드의 내용 </td> 
   <td colname="col4"> <span class="filepath"> http://www.referringsite.com </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(user-agent) </td> 
   <td colname="col2"> 사용자 에이전트 </td> 
   <td colname="col3"> HTTP 서버에 요청하는 데 사용되는 장치 </td> 
   <td colname="col4"> <p>Mozilla/4.0+(compatible;+MSIE+6.0; </p> <p>+Windows+NT+5.1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(cookie) </td> 
   <td colname="col2"> 도메인의 클라이언트 쿠키 </td> 
   <td colname="col3"> 사이트에 대한 모든 사용자 쿠키의 컨텐츠 </td> 
   <td colname="col4"> <p>KL_TC1 1038058778312 </p> <p>KL972 x1038058778312282052 </p> <p>KL_PVKL972 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs-uri-query </td> 
   <td colname="col2"> 쿼리 문자열 </td> 
   <td colname="col3"> 클라이언트가 요청한 URI의 쿼리 문자열 부분(있는 경우) </td> 
   <td colname="col4"> PAGENAME=dynamic1&amp;link=3001 </td> 
  </tr> 
 </tbody> 
</table>

