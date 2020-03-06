---
description: Insight Server 또는 Repeater에 대한 통신을 구성하는 지침입니다.
solution: Insight
title: 통신 구성 설정
uuid: 03297cf0-eb55-4db0-b692-eba24fcf947c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 통신 구성 설정{#communications-configuration-settings}

Insight Server 또는 Repeater에 대한 통신을 구성하는 지침입니다.

다음 파일에서 매개 변수를 완료합니다.

[!DNL Product Name installation directory\Components\Communications.cfg]

>[!NOTE]
>
>이 표에 나열되지 않은 매개 변수를 수정하기 전에 Adobe에 문의하십시오.

<table id="table_C87F1150E53548F484A8C0CFE91F1079"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 액세스 제어 파일 </td> 
   <td colname="col2"> <p>Access Control <span class="filepath"> .cfg </span> 파일의 위치입니다. 기본 위치는 <span class="filepath"> Insight Server </span> 또는 <span class="keyword"> Repeter </span> 설치 디렉토리 내의 액세스 제어 <span class="wintitle"> </span> 폴더입니다. </p> <p>예: <filepath></filepath> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 액세스 로그 디렉토리 </td> 
   <td colname="col2"> <p>감사 로그를 매핑할 폴더입니다. </p> <p>예: <filepath></filepath> </p> <p> <p>참고: 감사 로그를 다른 로컬 드라이브에 매핑할 수 있습니다(예:문자열: <span class="filepath"> P:\\Audit\\ </span>)를 제외하고 감사 로그를 네트워크 드라이브에 매핑하지 마십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 액세스 로그 자세한 정보 </td> 
   <td colname="col2"> 이 매개 변수는 true 또는 false로 설정할 수 있습니다. 감사 로그 필터링을 활성화 및 비활성화하는 데 사용됩니다. 모든 요청이 기록되도록 하려면 매개 변수를 True로 설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> IP 인터페이스 </td> 
   <td colname="col2"> <p>두 개의 서로 다른 네트워크에 액세스하는 데 사용할 수 있는 두 개의 네트워크 카드를 사용하는 IP 주소입니다. </p> <p>예:I <filepath></filepath><i>&lt; <span class="filepath"> IP 주소 </span>&gt;</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 포트 </td> 
   <td colname="col2"> <p>Insight Server <span class="keyword"> 또는 </span> Repeater가 <span class="wintitle"> </span> 수신하는 비보안(HTTP) 포트입니다. 기본 포트는 80입니다. 값을 0으로 입력하면 비보안 연결이 비활성화됩니다. </p> <p>예: <filepath></filepath> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 암호 </td> 
   <td colname="col2"> 일부 환경에서는 다른 환경보다 더 강력한 통신 보안이 필요합니다. 특정 SSL 암호화 세트를 사용하려면 이 매개 변수로 지정할 수 있습니다. <p>예: <filepath></filepath> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 포트 </td> 
   <td colname="col2"> <p>Insight Server <span class="keyword"> 또는 </span> Repeater가 <span class="wintitle"> </span> 수신 대기하는 SSL(Secure) 포트입니다. 기본 포트는 443입니다. 값을 0으로 입력하면 보안 연결이 비활성화됩니다. </p> <p>예: <span class="filepath"></span> </p> <filepath></filepath> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>n=</i>LoggingServer: </td> 
   <td colname="col2"> 로깅 서버 설정에 대한 제목입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 고객 이름 </td> 
   <td colname="col2"> <p>다음 예와 같이 관리 경고에서 지정되지 않은 고객에 대해 표시할 고객 이름: </p> <p>"15에서 고객 '지정되지 않음'에 대한 센서 XYZ로부터 데이터를 받지 못했습니다." </p> <p>예: <code> 1&nbsp;=&nbsp;LoggingServer:&nbsp; 
      &nbsp;&nbsp;Customer&nbsp;Name&nbsp;=&nbsp;string:&nbsp;CompanyAB </code> </p> <p>위의 예를 사용하면 지정되지 않은 고객에 대한 관리 경고를 다음과 같이 읽습니다. </p> <p>"15년 고객 'CompanyAB'에 대해 센서 XYZ로부터 데이터를 받지 못했습니다." </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <i>n=</i>FileServer: </p> <p> 로컬 경로 = 문자열:로그\\ </p> </td> 
   <td colname="col2"> <p>로그 파일을 저장할 폴더. </p> <p>예: </p> <code> 9&nbsp;=&nbsp;FileServer:&nbsp; 
     &nbsp;&nbsp;Local&nbsp;Path&nbsp;=&nbsp;string:&nbsp;Logs\\ </code> <p>서버 파일 관리자에서 이 폴더에 액세스하려면 이 <span class="wintitle"> 매개 변수에 지정된 </span>위치가 Log Processing.cfg <span class="filepath"> 파일의 로그 경로 매개 변수에서 지정한 </span> 위치와 일치해야 합니다. Log Processing.cfg 파일에서 로그 디렉토리를 수정하는 방법에 대한 자세한 내용은 <span class="filepath"> 데이터 세트 구성 </span> 안내서의 로그 처리 구성 파일 <i>장을 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <i>n=</i>FileServer: </p> <p> 로컬 경로 = 문자열:감사\\ </p> </td> 
   <td colname="col2"> <p>감사 로그를 매핑할 폴더입니다. </p> <p>예: </p> <code> 5&nbsp;=&nbsp;FileServer:&nbsp; 
     &nbsp;&nbsp;Local&nbsp;Path&nbsp;=&nbsp;string:&nbsp;Audit\\ </code> <p>참고:  <p>감사 로그를 다른 로컬 드라이브에 매핑할 수 있습니다(예:문자열: <span class="filepath"> P:\\Audit\\ </span>)를 제외하고 감사 로그를 네트워크 드라이브에 매핑하지 마십시오. </p> <p>서버 파일 관리자에서 이 폴더에 액세스하려면 이 <span class="wintitle"> 매개 변수에 지정된 </span>위치가 이 파일의 액세스 로그 디렉토리 매개 변수에 있는 위치와 일치해야 합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>n=</i>NormalizeServer: </td> 
   <td colname="col2"> <p>이 매개 변수는 Insight Server에만 <span class="keyword"> 적용됩니다 </span>. </p> <p>Insight 서버 클러스터에 대한 중앙 표준화 서버를 지정하는 방법에 대한 <span class="keyword"> 자세한 내용은 데이터 세트 구성 </span> 안내서의 로그 처리 구성 파일 <i>장을 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <i>n=</i>ReportStatusServer: </p> <p> URI = 문자열:/ReportStatus.vsp </p> </td> 
   <td colname="col2"> <p>이 매개 변수는 Insight Server에만 <span class="keyword"> 적용됩니다 </span>. </p> <p>Insight Server <span class="keyword"> 의 세부 상태 인터페이스에서 보고서 </span> 상태를 볼 <span class="keyword"> 수 </span>있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

