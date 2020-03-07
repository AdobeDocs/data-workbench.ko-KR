---
description: 선택적 Sensor txlogd.conf 파일 매개 변수에 대한 정보입니다.
solution: Insight
title: 선택적 매개 변수
uuid: 8515a571-93ce-49cd-9ded-c9273259d0ee
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Optional Parameters{#optional-parameters}

선택적 Sensor txlogd.conf 파일 매개 변수에 대한 정보입니다.

<table id="table_5FF491A7A6C24E43A06A5C344BF05430"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 주소 필터 </td> 
   <td colname="col2"> <p>지정된 IP 주소를 필터링할 수 있습니다. </p> <p>특정 주소를 필터링하면 "패킷"이 기록되지 않습니다. 이 기능은 로그 처리 전에 내부 또는 모니터링된 에이전트를 제거하므로 로그 처리 속도를 높이고 데이터 스토리지 요구 사항을 줄일 수 있습니다. 주소를 지정할 때 와일드카드를 사용할 수 있습니다. </p> <p>예:주소 <span class="filepath"> 필터 10.0.0.000</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ContentFilterInclude </p> <p>ContentFilterExclude </p> </td> 
   <td colname="col2"> <p>특정 유형의 컨텐츠를 로깅에서 포함할지 또는 제외할지를 지정합니다. </p> <p>매개 변수 값은 응답의 컨텐츠 유형에 대해 접두사와 일치합니다. </p> <p>예를 들어 "image/"는 모든 이미지 컨텐츠 유형과 일치하지만 "image/gif"는 해당 유형만 정확히 일치시킵니다. 지정된 컨텐츠 유형에 대해 여러 일치 항목이 발생하면 가장 구체적인 일치 항목이 사용됩니다. 따라서 ContentFilterInclude 매개 변수에 "image/gif"를 배치하고 ContentFilterExclude 매개 변수에 "image/"를 넣을 수 있으며 "image/gif" 응답은 허용되지만 다른 모든 이미지 유형은 필터링됩니다. </p> <p>예:ContentFilterInclude <span class="filepath"> *</span> </p> <p>예:ContentFilter <span class="filepath"> Exclude image/,text/css,application/x-javascript</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> DebugLogPath </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe Consulting Services로 작업하는 경우에만 설정합니다. </p> <p>웹 모듈 및 전송기에 대한 디버그 로깅을 활성화합니다. </p> <p>센서가 제대로 작동하지 않을 때 이 매개 <span class="wintitle"> 변수를</span> 사용합니다. 이 매개 변수를 설정한 후에는 지정된 경로 위치에 빈 파일을 만들고 모든 사용자에 대해 해당 파일에 "쓰기" 권한을 부여해야 합니다. 예(웹 서버의 unix 셸 내부): 
     <ul id="ul_7A067014A78048BF9D2F23DC66FF9E24"> 
      <li id="li_11C51EB9B9CC431585ECE9E8648F6122"><span class="filepath"> % cd /var/log</span> </li> 
      <li id="li_C56B2B5D49A543DBB258C5DE099B4AE5"><span class="filepath"> % 터치 vslog.txt</span> </li> 
      <li id="li_DA914383F813453AB6EF4F89279FD786"><span class="filepath"> % chmod a+w vslog.txt</span> </li> 
     </ul> </p> <p>로그 파일을 분석하기 위해 Adobe Consulting Services로 보내야 하는 경우 짧은 기간 동안 디버그 로깅을 활성화해야 합니다. </p> <p>예:DebugLogPath <span class="filepath"> /var/log/vslog.txt</span> </p> <p>Adobe에서는 먼저 이 매개 변수를 테스트 환경에서 설정하여 시스템에 영향을 줄 것을 권장합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> DisableField </td> 
   <td colname="col2"> <p>지정된 필드를 비활성화합니다. </p> <p>사용자는 사용하지 않거나 저장하지 않으려는 필드를 제거할 수 있습니다. 필드에 문자열 값이 있으면 비활성화하면 빈 문자열이 전달됩니다. 필드에 숫자 값이 있으면 비활성화하면 숫자 0(0)이 전달됩니다. 다음 필드를 비활성화할 수 있습니다. 
     <ul id="ul_4537B345EFAE449A9946DA0B52EA5C43"> 
      <li id="li_D674BC1982344C49B25A73EFF095C34A">sc-status </li> 
      <li id="li_6D647C845EB54B1B84C756DCDD7DD4CC">x-new-visitor </li> 
      <li id="li_65EB695B223040BCB9888375354B6E8B">x-trackingid </li> 
      <li id="li_41197A9CB961496B9CD26AA8457233FD">sc-bytes </li> 
      <li id="li_DCD45D7E21964B959299494FA719F453">c-ip </li> 
      <li id="li_7650796C6246484C8267ED9923596AFB">cs-method </li> 
      <li id="li_8941FCBBAA5E42EA9F04DA06EB91CAC5">cs-uri-stem </li> 
      <li id="li_A10438D2DEBB4ADFB574BF7094F9F0C4">cs-uri-query </li> 
      <li id="li_1D83BA59AC8543319D1966BB8ED1D931">s-dns </li> 
      <li id="li_34A23CE1944F4AEFBE7D74E8D6D5BEE6">cs(referrer) </li> 
      <li id="li_B85D93C381BD440F82C711C9A6D56CE9">cs(cookie) </li> 
      <li id="li_18D9C084450149D6A8713EBDA0C02E5B">cs(user-agent) </li> 
      <li id="li_A175CAF03E51473E990BE4F31F198B42">cs(useragent) </li> 
      <li id="li_ED38ED31B2644F2FA1C86FF93ADB9CEF">sc(content-type) </li> 
      <li id="li_1173C0027C8A4638BDF35E9719CD9D4C">x-experiment </li> 
     </ul> </p> <p>예:DisableField <span class="filepath"> x-trackingid</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpFile </td> 
   <td colname="col2"> <p>제어된 실험 구성 파일의 경로입니다. </p> <p>예:ExpFile <span class="filepath"> C:\VisualSensor\experiment.txt</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpCookieURL </td> 
   <td colname="col2"> <p>요청 시 새 추적 ID가 생성되어 사용자가 실험 그룹에 배치되도록 하는 리소스입니다. </p> <p> <p>참고: 이 리소스는 웹 서버에 실제로 존재하지 않아도 됩니다. </p> </p> <p>예:ExpCookieURL <span class="filepath"> /setcookie.htm</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpPartialMatch </td> 
   <td colname="col2"> <p>제어된 실험이 전체 사이트 또는 사이트의 전체 하위 디렉토리를 다른 위치에 다시 매핑하도록 하려면 이 매개 변수를 "on"으로 설정합니다. 기본값은 "off"입니다. </p> <p>예:ExpPartialMatch <span class="filepath"> off</span> </p> <p> <p>참고: 이 매개 변수를 "on"으로 설정할 때는 주의하십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> LogAllNewUsers </td> 
   <td colname="col2"> <p>사용자가 ContentFilterExclude 매개 변수로 필터링된 문서 유형을 요청할 경우에도 새 사용자의 첫 번째 클릭이 기록되는지 여부를 결정합니다. </p> <p>기본값은 "no"입니다. </p> <p>일반적으로 이미지 파일은 ContentFilterExclude 매개 변수로 필터링됩니다. LogAllNewUsers가 "yes"로 설정되어 있고 새 사용자가 서버에서 받는 첫 번째 문서가 이미지인 경우 해당 요청이 기록됩니다. LogAllNewUsers 매개 변수가 "no"로 설정되거나 전혀 설정되지 않은 경우(그리고 이미지가 ContentFilterExclude 매개 변수로 필터링되었다고 가정할 때) 새 사용자가 서버에서 받는 첫 번째 문서가 이미지이면 해당 요청이 기록되지 않습니다. </p> <p>예:로그모두 <span class="filepath"> 새로운 사용자새 사용자</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> MaxPageLoadTime </td> 
   <td colname="col2"> <p>전송자가 다음 묶음 묶음을 전송하기 위해 대기하는 시간(초)입니다. </p> <p>기본값은 15입니다. </p> <p>예:MaxPageLoadTime <span class="filepath"> 15</span> </p> <p> <p>참고: Adobe 컨설팅 서비스에 먼저 연락하지 않고 이 매개 변수 값을 변경하지 마십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 개인 정보 ID </td> 
   <td colname="col2"> <p>옵트아웃 정책을 준수하는 데 사용할 수 있는 방문자 추적을 비활성화할 수 있습니다. </p> <p>활성화되면 <span class="wintitle"> 센서는</span> V1st 쿠키가 지정된 PrivacyID로 설정된 모든 방문자에 대해 "패킷"을 기록하지 않습니다. 이러한 방문자에 대해 기록된 정보가 없으므로 이러한 방문자에 대한 정보는 처리를 위해 <span class="keyword"> 데이터 워크벤치 서버로</span> 전송되지 않습니다. </p> <p>이 기능을 활성화하려면 다음 단계를 완료해야 합니다. 
     <ol id="ol_5D658C5E4AB14F419029E0FFC52F1310"> 
      <li id="li_BF056439F92148169BF592731264C3CD"> PrivacyID는 센서의 txlogd.conf <span class="filepath"> 파일에서 0(영)으로 정의해야</span> 합니다 <span class="wintitle"></span>. <p>예:개인 <span class="filepath"> 정보 ID 0</span> </p> </li> 
      <li id="li_3E20F068C2F94512A92F284C80273B1C">웹 사이트 소유자는 쿠키 ID 값이 "txlogd.conf"로 정의된 PrivacyID 값과 일치하도록 방문자(V1st) 쿠키를 설정하는 코드를 작성해야 합니다<span class="filepath"></span>. </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SiteTest </td> 
   <td colname="col2"> <p>전송기(txlogd)가 주기적으로 요청을 보내는 위치로, 웹 사이트가 제대로 작동하는지 확인합니다. </p> <p>위치는 URL이 아니라 다음 형식으로 지정됩니다. </p> <p>http,<i>serverAddress,port/resource</i> </p> <p>여기서 <i>server</i> Address는 서버 이름 또는 IP 주소이고 <i>포트는</i> 서버의 HTTP 수신 포트이며 <i>리소스는</i> 요청할 특정 리소스(쿼리 문자열 포함)입니다. </p> <p>여러 SiteTest 라인을 지정할 수 있습니다. </p> <p>예:SiteTest http, <span class="filepath"> localhost,80,/test.html</span> </p> <p> <p>참고: 현재 http만 지원됩니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TrackingCookie </td> 
   <td colname="col2"> <p>방문자의 브라우저에 설정된 쿠키의 이름입니다. </p> <p>기본값은 "v1st"입니다. </p> <p>예:Tracking <span class="filepath"> Cookie v1st</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VerifyCertName </td> 
   <td colname="col2"> <p>CertName 매개 변수에 대해 서버의 유효성 검사 여부를 나타냅니다. </p> <p>기본값은 "on"입니다. </p> <p>예:VerifyCertName <span class="filepath"> 설정</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_598C3CDA5AA440228AF88C3BE4A8F77C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> IISCaptureBytesSent </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe Consulting Services로 작업하는 경우에만 설정합니다. </p> <p>패킷을 기록하는 데 사용할 <span class="wintitle"> 수 있는 두 가지 로깅</span> "후크" 중 어떤 것이 사용되어야 하는지 IIS 센서에 알려줍니다. </p> <p>IIS 센서가 <span class="wintitle"> 패킷을</span> 올바르게 로깅하지 않는 경우 이 매개 변수를 사용합니다. 기본 로깅 후크가 올바르게 작동하지 않는 경우 이 매개 변수가 "off"로 설정됩니다. 기본값은 "on"입니다. </p> <p>예:IISCaptureBytesSent on <span class="filepath"></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IISUseAlternateHandler </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe Consulting Services로 작업하는 경우에만 설정합니다. </p> <p>v1st <span class="wintitle"> 쿠키를</span> 설정하는 데 사용할 가능한 두 가지 "후크"를 센서에 알려줍니다. </p> <p>IIS 센서가 v1st 쿠키를 <span class="wintitle"> 올바로</span> 설정하지 않을 때 이 매개 변수를 사용합니다. v1st 쿠키를 올바로 설정하지 않은 경우 이 매개 변수는 "yes"로 설정됩니다. 기본값은 "no"입니다. </p> <p>예:ISUseAlternateHandler <span class="filepath"> no</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>NewUserCacheControl </p> <p>CacheControl </p> </td> 
   <td colname="col2"> <p>기본적으로 센서는 <span class="wintitle"></span> 각 요청에 대해 캐시 제어 응답 헤더를 전송합니다. 캐시 제어 기능이 활성화되면 센서는 <span class="wintitle"> 만료</span> 헤더를 목요일, 1994년 12월 1일, 16시 00분 GMT로 브라우저에 전송합니다. </p> <p>txlogd.conf 파일에서 다음 두 줄을 편집하여 원하는 대로 응답 문자열을 수정할 수 <span class="filepath"> 있습니다</span> . </p> <p> <span class="filepath"> NewUserCacheControl</span> <i>&lt;<span class="filepath"> string1</span>&gt;</i> </p> <p> <span class="filepath"> CacheControl</span> <i>&lt;<span class="filepath"> string2</span>&gt;</i> </p> <p>예: </p> <p> <span class="filepath"> NewUserCacheControl no-cache=Set-Cookie</span> </p> <p> <span class="filepath"> CacheControl private,max-age=0,must-revalidate</span> </p> <p>캐시 제어 응답 헤더 전송을 비활성화하려면 아래에 표시된 대로 각 행에 하이픈을 입력합니다. </p> <p> <span class="filepath"> NewUserCacheControl -</span> </p> <p> <span class="filepath"> CacheControl -</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_88696CCA93874BB683538BD614E07890"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수에서... </th> 
   <th colname="col2" class="entry"> 분류에 사용할... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ApacheUseAlternateHandler </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe Consulting Services로 작업하는 경우에만 설정합니다. </p> <p>v1st <span class="wintitle"> 쿠키를</span> 설정하는 데 사용할 가능한 두 가지 "후크"를 센서에 알려줍니다. </p> <p>이 매개 변수는 Apache 센서가 <span class="wintitle"> v</span> 1st 쿠키를 올바로 설정하지 않을 때 사용합니다. v1st 쿠키를 올바로 설정하지 않은 경우 이 매개 변수는 "yes"로 설정됩니다. 기본값은 "no"입니다. </p> <p>예:ApacheUseAlternateHandler <span class="filepath"> no</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ApacheUseBothHandlers </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe Consulting Services로 작업하는 경우에만 설정합니다. </p> <p>센서에 <span class="wintitle"> v</span> 1st 쿠키를 두 갈고리로 설정하도록 지시합니다. </p> <p>이 매개 변수는 Apache 센서가 <span class="wintitle"> v</span> 1st 쿠키를 올바로 설정하지 않을 때 사용합니다. 기본값은 "yes"입니다. </p> <p>"yes"로 설정되고 v1st 쿠키가 첫 번째 후크에 제대로 설정되지 않은 경우 두 번째 후크가 사용됩니다. "no"로 설정하면 ApacheUseAlternateHandler 매개 변수를 설정하여 v1st 쿠키를 설정하는 데 사용할 후크를 지정합니다. </p> <p>예:ApacheUseBothHandlers <span class="filepath"> 예</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>NewUserCacheControl </p> <p>CacheControl </p> </td> 
   <td colname="col2"> <p>기본적으로 센서는 <span class="wintitle"></span> 각 요청에 대해 캐시 제어 응답 헤더를 전송합니다. 캐시 제어 기능이 활성화되면 센서는 <span class="wintitle"> 만료</span> 헤더를 목요일, 1994년 12월 1일, 16시 00분 GMT로 브라우저에 전송합니다. </p> <p>txlogd.conf 파일에서 다음 두 줄을 편집하여 원하는 대로 응답 문자열을 수정할 수 <span class="filepath"> 있습니다</span> . </p> <p> <span class="filepath"> NewUserCacheControl</span> <i>&lt;<span class="filepath"> string1</span>&gt;</i> </p> <p> <span class="filepath"> CacheControl</span> <i>&lt;<span class="filepath"> string2</span>&gt;</i> </p> <p>예: </p> <p> <span class="filepath"> NewUserCacheControl no-cache=Set-Cookie</span> </p> <p> <span class="filepath"> CacheControl private,max-age=0,must-revalidate</span> </p> <p>캐시 제어 응답 헤더 전송을 비활성화하려면 아래에 표시된 대로 각 행에 하이픈을 입력합니다. </p> <p> <span class="filepath"> NewUserCacheControl -</span> </p> <p> <span class="filepath"> CacheControl -</span> </p> <p> <p>참고: 이 기능을 비활성화하지 않는 것이 좋습니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_BF01F6265B8544DA9D9AD2C80A64C0F3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수에서... </th> 
   <th colname="col2" class="entry"> 분류에 사용할... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ApacheUseAlternateHandler </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe Consulting Services로 작업하는 경우에만 설정합니다. </p> <p>v1st <span class="wintitle"> 쿠키를</span> 설정하는 데 사용할 가능한 두 가지 "후크"를 센서에 알려줍니다. </p> <p>이 매개 변수는 Apache 센서가 <span class="wintitle"> v</span> 1st 쿠키를 올바로 설정하지 않을 때 사용합니다. v1st 쿠키를 올바로 설정하지 않은 경우 이 매개 변수는 "yes"로 설정됩니다. 기본값은 "no"입니다. </p> <p>예:ApacheUseAlternateHandler <span class="filepath"> no</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ApacheUseBothHandlers </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe Consulting Services로 작업하는 경우에만 설정합니다. </p> <p>센서에 <span class="wintitle"> v</span> 1st 쿠키를 두 갈고리로 설정하도록 지시합니다. </p> <p>이 매개 변수는 Apache 센서가 <span class="wintitle"> v</span> 1st 쿠키를 올바로 설정하지 않을 때 사용합니다. 기본값은 "yes"입니다. </p> <p>"yes"로 설정되고 v1st 쿠키가 첫 번째 후크에 제대로 설정되지 않은 경우 두 번째 후크가 사용됩니다. "no"로 설정하면 ApacheUseAlternateHandler 매개 변수를 설정하여 v1st 쿠키를 설정하는 데 사용할 후크를 지정합니다. </p> <p>예:ApacheUseBothHandlers <span class="filepath"> 예</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

