---
description: Flash를 사용하여 설계된 웹 사이트에서는 리치 미디어 컨텐츠 내에서 수행되는 방문자 작업의 캡처와 관련하여 특별한 주의가 필요합니다.
solution: Analytics
title: Flash 리치 미디어 컨텐츠 내에서 방문자 활동 추적
topic: Data workbench
uuid: fe2e75eb-0897-4f63-b582-b4f1fdce02a1
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Flash 리치 미디어 컨텐츠 내에서 방문자 활동 추적{#tracking-visitor-activity-within-flash-rich-media-content}

Flash를 사용하여 설계된 웹 사이트에서는 리치 미디어 컨텐츠 내에서 수행되는 방문자 작업의 캡처와 관련하여 특별한 주의가 필요합니다.

ActionScript [!DNL Flash] 를 사용하면 기존 [!DNL Flash] 동영상을 간단하게 변경하여 버튼 클릭 또는 마우스 움직임과 같은 동영상과 모든 방문자 상호 작용을 추적할 수 있습니다.

동영상 내에서 방문자 활동 추적을 용이하게 하려면 아래 나열된 단계를 따르십시오. [!DNL Flash]

1. 다음 ActionScript 코드를 동영상에 추가합니다. 이 코드는 추적하려는 [!DNL Flash] 동영상 내의 이벤트에서 호출할 수 있는 함수를 나타냅니다.

   ```
   // FLASH TAG CODE BEGIN 
   var FLASHTAGURI = "[PATH_TO_WEB_SERVER]/flashtag.txt"; 
   function tag(PAGENAME,VARIABLES) { 
   loadVariablesNum(FLASHTAGURI+”?”+"PAGENAME="+PAGENAME+"&"+VARIABLES,0); 
   } 
   // FLASH TAG CODE END
   ```

1. 이름이 [!DNL flashtag.txt] 있는 빈 파일을 만들어 웹 서버에 배치합니다.
1. 1단계의 함수 내에서 [!DNL PATH_ [TO_WEB_SERVER]] 자리 표시자를 해당 [!DNL flashtag.txt] 파일의 위치에 대한 정규화된 경로 또는 상대 경로로 바꿉니다. 예:

   ```
   var FLASHTAGURI = http://www.mysite.com/flashtag/flashtag.txt”;
   ```

1. 추적할 모든 이벤트에 다음 ActionScript 코드를 추가합니다. 이 코드는 이벤트에 대한 데이터를 캡처하는 데 사용되는 함수 호출을 나타냅니다.

   ```
   on(release) {tag("[PUT_PAGE_NAME_HERE]","[PUT_ADDITIONAL_VAR_HERE]");}
   ```

   이 예에서는 on(release) 이벤트의 사용을 보여 줍니다.그러나 on(press), on(rollover), on(rollout), on(rollout) 또는 on(keypress) 이벤트와 같이 추적할 수 있는 모든 이벤트를 통해 tag() 함수를 참조할 수 있습니다.

   [!DNL [PUT_PAGE_NAME]_HERE] 자리 표시자는 추적하고 있는 페이지 또는 이벤트의 이름을 나타내는 문자열로 대체해야 합니다. [!DNL [PUT_PAGE_NAME_HERE]] 변수를 수동으로 또는 변수 참조를 통해 수정하여 [!DNL Flash] 응용 프로그램 내의 페이지나 이벤트에 대한 고유한 이름을 표시할 수 있습니다. [!DNL PUT_ [PAGE_NAME_HERE]] 자리 표시자를 대체하는 값은 간단한 이름으로 구성되거나 전체 URI와 유사한 계층적 구조를 나타내는 구조로 구성될 수 있습니다. 예:

   ```
   on(release) {tag(“/about_us/index.swf","[PUT_ADDITIONAL_VAR_HERE]");}
   ```

   Adobe는 코드 배포 전에 비즈니스 요구 사항 및 개발 작업의 정렬을 용이하게 하고 추가 개발 주기 가능성을 줄이기 위해 페이지 이름 및 이벤트 이름에 대한 문서 사양을 컴파일할 것을 권장합니다.

1. 원하는 경우 추가 변수를 수집하여 [!DNL Flash] 동영상의 페이지 또는 이벤트와 연결할 수 있습니다. 이렇게 하려면 [!DNL PUT_ [ADDITIONAL_VAR_HERE]] 자리 표시자를 앰퍼샌드(&amp;)로 구분된 이름=값 쌍 집합으로 바꿉니다. 예:

   ```
   on(release) {tag(“/about_us/index.swf"," var1=value1&var2=value2");}
   ```

   변수를 수동으로 또는 변수 참조를 통해 수정하여 수집하여 페이지나 이벤트와 연결할 추가 속성을 나타낼 수 있습니다. 수집할 추가 변수가 없는 경우 [!DNL PUT_ADDITIONAL_VAR_ [HERE]를]제거합니다.

   이제 [!DNL Flash] 리치 미디어 컨텐츠 내에서 방문자 추적 설정이 완료되었습니다. 이벤트가 호출되면 태그 [!DNL (PAGENAME,VARIABLES)] 함수가 호출되어 다음 파일에 대한 HTTP 요청이 수행됩니다. 이 함수는 [!DNL Flash] 무비 내에 정의된 대로 트리거될 수 있는 다른 함수와 함께 호출됩니다.

   ```
   http://www.mysite.com/flashtag/flashtag.txt?PAGENAME=/about_us/index.swf&var1=value1&var2=value2
   ```

Tag ActionScript 함수로 인해 [!DNL Flash] 발생한 HTTP 요청은 [!DNL Flash] 동영상 내의 각 이벤트와 관련된 다음 정보를 수집합니다. 표의 마지막 행(W3C 이름 cs-uri-query)은 함수 호출에 지정된 추가 변수에 대해 수집된 정보를 나타냅니다.

<table id="table_A7ED9D38F36B4405947B2F48EA94D3C4"> 
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
   <td colname="col3"> 방문자의 초기 요청에서 Sensor가 사용자의 브라우저에 배치된 <span class="wintitle"> 쿠키에서 </span> 읽은 식별자 </td> 
   <td colname="col4"> v1st=3C94007B4E01F9C2 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>날짜 </p> <p>시간 </p> </td> 
   <td colname="col2"> 타임스탬프 </td> 
   <td colname="col3"> 서버에서 요청을 처리한 시간(정확히 100ns)정확성은 서버 환경 및 NTP에 따라 다름) </td> 
   <td colname="col4"> 2002-11-21 17:21:45.123 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> sc(content-type) </td> 
   <td colname="col2"> 컨텐츠 유형 </td> 
   <td colname="col3"> 서버에서 반환되는 개체 유형 </td> 
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
   <td colname="col3"> 클라이언트가 요청한 URI의 시스템 부분 </td> 
   <td colname="col4"> /flashtag/flashtag.txt </td> 
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
   <td colname="col4"> www.mysite.com </td> 
  </tr> 
  <tr> 
   <td colname="col1"> cs(referrer) </td> 
   <td colname="col2"> 참조 URL </td> 
   <td colname="col3"> 클라이언트가 보낸 HTTP 레퍼러 필드의 내용 </td> 
   <td colname="col4"></td> 
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
   <td colname="col3"> 클라이언트가 요청한 URI의 쿼리 문자열 부분(있는 경우) </td> 
   <td colname="col4"> PAGENAME=/about_us/index.swf&amp;var1=value1&amp;var2=value2 </td> 
  </tr> 
 </tbody> 
</table>

