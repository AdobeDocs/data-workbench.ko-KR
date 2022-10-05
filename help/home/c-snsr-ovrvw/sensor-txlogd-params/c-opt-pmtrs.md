---
description: 선택적 Sensor txlogd.conf 파일 매개 변수에 대한 정보입니다.
title: 선택적 매개 변수
uuid: 8515a571-93ce-49cd-9ded-c9273259d0ee
exl-id: 5141f215-979c-4eb8-8c2c-94eef5815743
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1484'
ht-degree: 1%

---

# 선택적 매개 변수{#optional-parameters}

{{eol}}

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
   <td colname="col2"> <p>지정된 IP 주소를 필터링할 수 있습니다. </p> <p>특정 주소를 필터링할 때 "패킷"이 기록되지 않습니다. 이 기능을 사용하면 로그 처리 전에 내부 또는 모니터링되는 에이전트를 제거하므로 로그 처리 속도가 빨라지고 데이터 스토리지 요구 사항이 줄어듭니다. 주소를 지정할 때 와일드카드를 사용할 수 있습니다. </p> <p>예: <span class="filepath"> 주소 필터 10.0.0.000</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ContentFilterInclude </p> <p>ContentFilterExclude </p> </td> 
   <td colname="col2"> <p>특정 유형의 컨텐츠를 로깅에서 포함할지 또는 제외할지를 지정합니다. </p> <p>매개 변수 값은 응답의 컨텐츠 유형에 대해 접두사와 일치합니다. </p> <p>예를 들어, "image/"는 모든 이미지 컨텐츠 유형과 일치하는 반면, "image/gif"는 해당 유형만 정확히 일치합니다. 주어진 컨텐츠 유형에 대해 여러 개의 일치 항목이 발생하면 가장 구체적인 일치 항목이 사용됩니다. 따라서 ContentFilterInclude 매개 변수에 "image/gif"를 입력하고 ContentFilterExclude 매개 변수에 "image/"를 둘 수 있으며, "image/gif" 응답이 허용되지만 다른 모든 이미지 유형은 필터링됩니다. </p> <p>예: <span class="filepath"> ContentFilterInclude *</span> </p> <p>예: <span class="filepath"> ContentFilterExclude 이미지/,text/css,application/x-javascript</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> DebugLogPath </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe 컨설팅 서비스를 사용할 때만 설정하십시오. </p> <p>웹 모듈 및 전송기에 대한 디버그 로깅을 활성화합니다. </p> <p>이 매개 변수는 <span class="wintitle"> Sensor</span> 가 제대로 작동하지 않습니다. 이 매개 변수를 설정한 후에는 지정된 경로 위치에 빈 파일을 만들고 모든 사용자에 대해 "쓰기" 권한을 지정해야 합니다. 예를 들어, 웹 서버의 unix 셸 내에서 다음을 수행합니다. 
     <ul id="ul_7A067014A78048BF9D2F23DC66FF9E24"> 
      <li id="li_11C51EB9B9CC431585ECE9E8648F6122"><span class="filepath"> % cd /var/log</span> </li> 
      <li id="li_C56B2B5D49A543DBB258C5DE099B4AE5"><span class="filepath"> % touch vslog.txt</span> </li> 
      <li id="li_DA914383F813453AB6EF4F89279FD786"><span class="filepath"> % chmod a+w vslog.txt</span> </li> 
     </ul> </p> <p>로그 파일을 분석 대상 Adobe 컨설팅 서비스로 전송한 후 짧은 시간 동안 디버그 로깅을 활성화해야 합니다. </p> <p>예: <span class="filepath"> DebugLogPath /var/log/vslog.txt</span> </p> <p>Adobe은 이 매개 변수를 먼저 테스트 환경에서 설정하여 시스템에 미치는 영향을 확인할 것을 권장합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> DisableField </td> 
   <td colname="col2"> <p>지정된 필드를 사용하지 않도록 설정합니다 </p> <p>사용자는 사용하지 않거나 저장하지 않으려는 필드를 제거할 수 있습니다. 필드에 문자열 값이 있으면 비활성화하여 빈 문자열을 전달합니다. 필드에 숫자 값이 있으면 비활성화하여 숫자 0(0)을 전달합니다. 다음 필드를 비활성화할 수 있습니다. 
     <ul id="ul_4537B345EFAE449A9946DA0B52EA5C43"> 
      <li id="li_D674BC1982344C49B25A73EFF095C34A">sc-status </li> 
      <li id="li_6D647C845EB54B1B84C756DCDD7DD4CC">x-new-visitor </li> 
      <li id="li_65EB695B223040BCB9888375354B6E8B">x-trackingid </li> 
      <li id="li_41197A9CB961496B9CD26AA8457233FD">sc-bytes </li> 
      <li id="li_DCD45D7E21964B959299494FA719F453">c-ip </li> 
      <li id="li_7650796C6246484C8267ED9923596AFB">cs 메서드 </li> 
      <li id="li_8941FCBBAA5E42EA9F04DA06EB91CAC5">cs-uri-stem </li> 
      <li id="li_A10438D2DEBB4ADFB574BF7094F9F0C4">cs-uri-query </li> 
      <li id="li_1D83BA59AC8543319D1966BB8ED1D931">s-dns </li> 
      <li id="li_34A23CE1944F4AEFBE7D74E8D6D5BEE6">cs(referrer) </li> 
      <li id="li_B85D93C381BD440F82C711C9A6D56CE9">cs(cookie) </li> 
      <li id="li_18D9C084450149D6A8713EBDA0C02E5B">cs(user-agent) </li> 
      <li id="li_A175CAF03E51473E990BE4F31F198B42">cs(useragent) </li> 
      <li id="li_ED38ED31B2644F2FA1C86FF93ADB9CEF">sc(content-type) </li> 
      <li id="li_1173C0027C8A4638BDF35E9719CD9D4C">x-실험 </li> 
     </ul> </p> <p>예: <span class="filepath"> DisableField x-trackingid</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpFile </td> 
   <td colname="col2"> <p>통제 실험 구성 파일의 경로입니다. </p> <p>예: <span class="filepath"> ExpFile C:\VisualSensor\experiment.txt</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpCookieURL </td> 
   <td colname="col2"> <p>요청한 경우 리소스가 새 추적 ID가 생성되고 사용자가 실험 그룹에 배치되는 것입니다. </p> <p> <p>참고: 이 리소스는 웹 서버에 물리적으로 존재하지 않아도 됩니다. </p> </p> <p>예: <span class="filepath"> ExpCookieURL /setcookie.htm</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ExpPartialMatch </td> 
   <td colname="col2"> <p>제어된 실험이 전체 사이트 또는 사이트의 전체 하위 디렉터리를 다른 위치에 다시 매핑하도록 하려면 이 매개 변수를 "on"으로 설정하십시오. 기본값은 "off"입니다. </p> <p>예: <span class="filepath"> ExpPartialMatch 해제</span> </p> <p> <p>참고: 이 매개 변수를 "on"으로 설정할 때는 주의하십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> LogAllNewUsers </td> 
   <td colname="col2"> <p>사용자가 ContentFilterExclude 매개 변수로 필터링된 문서 유형을 요청하는 경우에도 새 사용자의 첫 번째 클릭이 모두 기록되는지 여부를 결정합니다. </p> <p>기본값은 "no"입니다. </p> <p>일반적으로 이미지 파일은 ContentFilterExclude 매개 변수로 필터링됩니다. LogAllNewUsers가 "yes"로 설정되어 있고 서버에서 새 사용자가 가져오는 첫 번째 문서가 이미지인 경우 해당 요청이 기록됩니다. LogAllNewUsers 매개 변수가 "no"로 설정되어 있거나 설정되지 않은 경우(그리고 이미지가 ContentFilterExclude 매개 변수로 필터링된다고 가정) 새 사용자가 서버에서 받는 첫 번째 문서가 이미지이면 해당 요청은 기록되지 않습니다. </p> <p>예: <span class="filepath"> LogAllNewUsers 아니요</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> MaxPageLoadTime </td> 
   <td colname="col2"> <p>전송기가 다음 패킷 일괄 전송을 대기하는 시간(초)입니다. </p> <p>기본값은 15입니다. </p> <p>예: <span class="filepath"> MaxPageLoadTime 15</span> </p> <p> <p>참고: Adobe 컨설팅 서비스에 먼저 문의하지 않으면 이 매개 변수 값을 변경하지 마십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> PrivacyID </td> 
   <td colname="col2"> <p>옵트아웃 정책을 준수하는 데 사용할 수 있는 방문자 추적을 비활성화할 수 있습니다. </p> <p>활성화되면, <span class="wintitle"> Sensor</span> V1st 쿠키가 지정된 PrivacyID로 설정된 방문자에 대해 "패킷"을 기록하지 않습니다. 해당 방문자에 대해 기록된 정보가 없으므로 해당 방문자에 대한 정보는 로 전송되지 않습니다 <span class="keyword"> data workbench 서버</span> 참조하십시오. </p> <p>이 기능을 사용하려면 다음 단계를 완료해야 합니다. 
     <ol id="ol_5D658C5E4AB14F419029E0FFC52F1310"> 
      <li id="li_BF056439F92148169BF592731264C3CD"> PrivacyID는 <span class="filepath"> txlogd.conf</span> 파일 <span class="wintitle"> Sensor</span>. <p>예: <span class="filepath"> PrivacyID 0</span> </p> </li> 
      <li id="li_3E20F068C2F94512A92F284C80273B1C">웹 사이트 소유자는 쿠키 ID 값이 정의된 PrivacyID 값과 일치하도록 방문자(V1st) 쿠키를 설정하는 코드를 작성해야 합니다. "<span class="filepath"> txlogd.conf</span>." </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SiteTest </td> 
   <td colname="col2"> <p>전송기(txlogd)가 주기적으로 요청을 보내는 위치로, 웹 사이트가 올바르게 작동하는지 확인합니다. </p> <p>위치는 URL이 아니라 다음 형식으로 지정됩니다. </p> <p>http,<i>serverAddress,port,/resource</i> </p> <p>여기서 <i>serverAddress</i> 서버 이름 또는 IP 주소, <i>포트</i> 은 서버의 HTTP 수신 포트이며 <i>리소스</i> 은 요청할 특정 리소스입니다(쿼리 문자열을 포함할 수 있음). </p> <p>여러 SiteTest 라인을 지정할 수 있습니다. </p> <p>예: <span class="filepath"> SiteTest http,localhost,80,/test.html</span> </p> <p> <p>참고: 현재 http만 지원됩니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TrackingCookie </td> 
   <td colname="col2"> <p>방문자의 브라우저에 설정된 쿠키의 이름입니다. </p> <p>기본값은 "v1st"입니다. </p> <p>예: <span class="filepath"> TrackingCookie v1st</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> VerifyCertName </td> 
   <td colname="col2"> <p>CertName 매개 변수에 대해 서버의 유효성을 검사할지 여부를 나타냅니다. </p> <p>기본값은 "on"입니다. </p> <p>예: <span class="filepath"> VerifyCertName 설정</span> </p> </td> 
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
   <td colname="col2"> <p>이 매개 변수는 Adobe 컨설팅 서비스를 사용할 때만 설정하십시오. </p> <p>IIS에 알림 <span class="wintitle"> Sensor</span> 패킷을 기록하는 데 사용할 수 있는 두 개의 로깅 "후크" 중 어느 것을 사용해야 합니까? </p> <p>IIS에서 이 매개 변수를 사용합니다 <span class="wintitle"> Sensor</span> 가 패킷을 올바르게 로깅하지 않습니다. 기본 로깅 후크가 제대로 작동하지 않으면 이 매개 변수가 "해제"로 설정됩니다. 기본값은 "on"입니다. </p> <p>예: <span class="filepath"> IISCaptureBytesSent on</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IISUseAlternateHandler </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe 컨설팅 서비스를 사용할 때만 설정하십시오. </p> <p>에 <span class="wintitle"> Sensor</span> v1st 쿠키를 설정하는 데 사용할 수 있는 "후크"가 두 개 있습니다. </p> <p>IIS에서 이 매개 변수를 사용합니다 <span class="wintitle"> Sensor</span> 가 v1st 쿠키를 올바로 설정하지 않습니다. 기본 후크가 v1st 쿠키를 올바로 설정하지 않은 경우 이 매개 변수는 "예"로 설정됩니다. 기본값은 "no"입니다. </p> <p>예: <span class="filepath"> IISUseAlternateHandler가 없습니다.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>NewUserCacheControl </p> <p>CacheControl </p> </td> 
   <td colname="col2"> <p>기본적으로 <span class="wintitle"> Sensor</span> 각 요청에 대해 캐시 제어 응답 헤더를 보냅니다. 캐시 제어 기능이 활성화된 경우 <span class="wintitle"> Sensor</span> 가 01, 1994 12월 16인 값으로 만료 헤더를 보냅니다:00:00 GMT를 브라우저에 추가합니다. </p> <p>에서 다음 두 줄을 편집하여 원하는 대로 응답 문자열을 수정할 수 있습니다 <span class="filepath"> txlogd.conf</span> 파일: </p> <p> <span class="filepath"> NewUserCacheControl</span> <i>&lt;<span class="filepath"> string1</span>&gt;</i> </p> <p> <span class="filepath"> CacheControl</span> <i>&lt;<span class="filepath"> string2</span>&gt;</i> </p> <p>예: </p> <p> <span class="filepath"> NewUserCacheControl no-cache=Set-Cookie</span> </p> <p> <span class="filepath"> CacheControl private,max-age=0,must-revalidate</span> </p> <p>캐시 제어 응답 헤더 전송을 비활성화하려면 아래에 표시된 대로 각 행에 하이픈을 입력합니다. </p> <p> <span class="filepath"> NewUserCacheControl -</span> </p> <p> <span class="filepath"> CacheControl -</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_88696CCA93874BB683538BD614E07890"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수에서.. </th> 
   <th colname="col2" class="entry"> 분류에 사용할... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ApacheUseAlternateHandler </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe 컨설팅 서비스를 사용할 때만 설정하십시오. </p> <p>에 <span class="wintitle"> Sensor</span> v1st 쿠키를 설정하는 데 사용할 수 있는 "후크"가 두 개 있습니다. </p> <p>Apache에서 이 매개 변수를 사용합니다 <span class="wintitle"> Sensor</span> 가 v1st 쿠키를 올바로 설정하지 않습니다. 기본 후크가 v1st 쿠키를 올바로 설정하지 않은 경우 이 매개 변수는 "예"로 설정됩니다. 기본값은 "no"입니다. </p> <p>예: <span class="filepath"> ApacheUseAlternateHandler 아니요</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ApacheUseBothHandlers </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe 컨설팅 서비스를 사용할 때만 설정하십시오. </p> <p>지시 <span class="wintitle"> Sensor</span> 를 눌러 두 후크에서 v1st 쿠키를 설정합니다. </p> <p>Apache에서 이 매개 변수를 사용합니다 <span class="wintitle"> Sensor</span> 가 v1st 쿠키를 올바로 설정하지 않습니다. 기본값은 "예"입니다. </p> <p>"yes"로 설정하고 v1st 쿠키가 첫 번째 후크에서 제대로 설정되지 않은 경우 두 번째 후크가 사용됩니다. "no"로 설정하면 ApacheUseAlternateHandler 매개 변수를 설정하여 v1st 쿠키를 설정하는 데 사용할 후크를 지정합니다. </p> <p>예: <span class="filepath"> ApacheUseBothHandlers 예</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>NewUserCacheControl </p> <p>CacheControl </p> </td> 
   <td colname="col2"> <p>기본적으로 <span class="wintitle"> Sensor</span> 각 요청에 대해 캐시 제어 응답 헤더를 보냅니다. 캐시 제어 기능이 활성화된 경우 <span class="wintitle"> Sensor</span> 가 01, 1994 12월 16인 값으로 만료 헤더를 보냅니다:00:00 GMT를 브라우저에 추가합니다. </p> <p>에서 다음 두 줄을 편집하여 원하는 대로 응답 문자열을 수정할 수 있습니다 <span class="filepath"> txlogd.conf</span> 파일: </p> <p> <span class="filepath"> NewUserCacheControl</span> <i>&lt;<span class="filepath"> string1</span>&gt;</i> </p> <p> <span class="filepath"> CacheControl</span> <i>&lt;<span class="filepath"> string2</span>&gt;</i> </p> <p>예: </p> <p> <span class="filepath"> NewUserCacheControl no-cache=Set-Cookie</span> </p> <p> <span class="filepath"> CacheControl private,max-age=0,must-revalidate</span> </p> <p>캐시 제어 응답 헤더 전송을 비활성화하려면 아래에 표시된 대로 각 행에 하이픈을 입력합니다. </p> <p> <span class="filepath"> NewUserCacheControl -</span> </p> <p> <span class="filepath"> CacheControl -</span> </p> <p> <p>참고: Adobe은 이 기능을 비활성화하지 않도록 권장합니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_BF01F6265B8544DA9D9AD2C80A64C0F3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수에서.. </th> 
   <th colname="col2" class="entry"> 분류에 사용할... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ApacheUseAlternateHandler </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe 컨설팅 서비스를 사용할 때만 설정하십시오. </p> <p>에 <span class="wintitle"> Sensor</span> v1st 쿠키를 설정하는 데 사용할 수 있는 "후크"가 두 개 있습니다. </p> <p>Apache에서 이 매개 변수를 사용합니다 <span class="wintitle"> Sensor</span> 가 v1st 쿠키를 올바로 설정하지 않습니다. 기본 후크가 v1st 쿠키를 올바로 설정하지 않은 경우 이 매개 변수는 "예"로 설정됩니다. 기본값은 "no"입니다. </p> <p>예: <span class="filepath"> ApacheUseAlternateHandler 아니요</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ApacheUseBothHandlers </td> 
   <td colname="col2"> <p>이 매개 변수는 Adobe 컨설팅 서비스를 사용할 때만 설정하십시오. </p> <p>지시 <span class="wintitle"> Sensor</span> 를 눌러 두 후크에서 v1st 쿠키를 설정합니다. </p> <p>Apache에서 이 매개 변수를 사용합니다 <span class="wintitle"> Sensor</span> 가 v1st 쿠키를 올바로 설정하지 않습니다. 기본값은 "예"입니다. </p> <p>"yes"로 설정하고 v1st 쿠키가 첫 번째 후크에서 제대로 설정되지 않은 경우 두 번째 후크가 사용됩니다. "no"로 설정하면 ApacheUseAlternateHandler 매개 변수를 설정하여 v1st 쿠키를 설정하는 데 사용할 후크를 지정합니다. </p> <p>예: <span class="filepath"> ApacheUseBothHandlers 예</span> </p> </td> 
  </tr> 
 </tbody> 
</table>
