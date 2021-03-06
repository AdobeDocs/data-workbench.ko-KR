---
description: 보고서 서버.cfg 매개 변수에 대한 정보입니다.
title: 보고서 서버.cfg 매개 변수
uuid: 506f30f7-c8c6-4580-8423-7da8d00b0d57
exl-id: 339e4219-ff4d-4df6-b45a-7144927a843b
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 2%

---

# 보고서 서버.cfg 매개 변수{#report-server-cfg-parameters}

보고서 서버.cfg 매개 변수에 대한 정보입니다.

[Insight Server에 연결 구성](../../../home/c-rpt-oview/c-inst-rpt/t-config-conn-ins-svr.md#task-a3ca949c43244782b658fb4437fd724c)에 표시된 샘플 [!DNL Report Server.cfg]에는 기본적으로 [!DNL Report Server.cfg] 파일에 포함된 매개 변수만 포함되어 있습니다.

프록시 서버를 통해 Adobe 라이센스 서버에 문의하는 경우 라이센스 벡터와 해당 매개 변수를 [!DNL Report Server.cfg]에 추가해야 합니다. 다음은 라이선스 벡터에 모델을 사용할 수 있는 이 벡터 및 그 매개 변수의 예입니다.

```
Licensing = serverInfo:  
Proxy Address = string: ProxyIPAddress 
Proxy Password = string: ProxyPassword 
Proxy Port = int: ProxyPort 
Proxy User Name = string: ProxyUserName 
```

다음 표에서는 [!DNL Report Server.cfg] 파일 매개 변수에 대한 설명을 제공합니다.

<table id="table_9DA4A3124A9D444CBB4CBFF6FA279A42"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Excel 확장 </td> 
   <td colname="col2"> <p>지원되는 Excel 확장명은 다음과 같습니다. </p> <p>Excel 확장 = 문자열: <span class="filepath">.xlsx </span> </p> <p>Excel 확장 = 문자열: <span class="filepath">.xls </span> (기본값) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 글꼴 </td> 
   <td colname="col2"> <p>선택 사항입니다. <span class="keyword"> 보고서 서버 </span>에서 UTF8 기반 유니코드 특수 문자를 렌더링하는 데 사용해야 하는 글꼴을 나열하는 벡터입니다. 목록에 있는 글꼴 수는 제한이 없습니다. </p> <p>첫 번째 글꼴은 항상 Lucida Sans Console이어야 합니다. 이 매개 변수가 <span class="filepath"> 보고서 서버.cfg </span> 파일에 포함되지 않으면 <span class="keyword"> 보고서 서버 </span>에서는 Lucida Sans 콘솔만 사용하여 텍스트를 표시합니다. </p> <p> <span class="keyword"> 보고서  </span> 서버는 목록의 첫 번째 글꼴을 사용하여 렌더링할 수 없는 문자가 나타날 때까지 모든 문자를 렌더링합니다. 그런 다음 목록의 두 번째 글꼴을 사용하여 해당 문자를 렌더링합니다. 해당 글꼴이 문자를 렌더링하지 않으면 <span class="keyword"> 보고서 서버 </span>에서는 목록에 있는 세 번째 글꼴을 사용하여 해당 문자를 렌더링하고, 이러한 글꼴이 글꼴 목록의 끝에 도달할 때까지 해당 문자를 렌더링합니다. 벡터에 올바른 글꼴이 나열되지 않으면 <span class="keyword"> 보고서 서버 </span>에 문자의 16진수 값이 표시됩니다. </p> <p> <p>참고:  <span class="keyword"> 보고서 서버 </span>가 실행 중인 동안에는 이 매개 변수를 변경하지 마십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 감마 </td> 
   <td colname="col2"> <p> <span class="wintitle"> 감마  </span> 설정  <span class="filepath"> .png  </span> 파일 출력. 기본값은 1.6입니다. </p> <p> <p>참고:  Adobe은 이 값을 변경하지 않는 것이 좋습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 라이선스 </td> 
   <td colname="col2"> <p>선택 사항입니다. 프록시 서버를 통해 Adobe의 라이선스 서버에 문의하는 경우에만 이 벡터의 매개 변수를 수정해야 합니다. </p> <p>프록시 서버를 통해 Adobe의 라이선스 서버에 연락하도록 설정한 매개 변수에 대한 섹션 식별자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프록시 주소 </td> 
   <td colname="col2"> <span class="keyword"> 보고서 서버 </span>가 Adobe의 라이선스 서버에 액세스하는 데 사용해야 하는 프록시 서버의 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프록시 암호 </td> 
   <td colname="col2"> 선택 사항입니다. <span class="wintitle"> 프록시 사용자 이름 </span>에 연결된 암호입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프록시 포트 </td> 
   <td colname="col2"> 프록시 서버의 포트입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프록시 사용자 이름 </td> 
   <td colname="col2"> 선택 사항입니다. 프록시 서버에 액세스하는 데 사용되는 사용자 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 네트워크 위치 </td> 
   <td colname="col2"> <span class="keyword"> 보고서 서버 </span>에서 서버의 일반 이름을 IP 주소로 확인하는 데 사용하는 네트워크 위치입니다. 네트워크 위치는 Data Workbench 서버 시스템의 주소 디렉토리에 있는 주소 파일에 정의됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 서버 </td> 
   <td colname="col2"> <p>보고서를 생성하기 위해 Data Workbench 서버 시스템 <span class="keyword"> 보고서 서버 </span>이(가) 연결해야 하는 매개 변수를 구성하도록 설정한 매개 변수의 섹션 식별자입니다. 여기에는 이 벡터에 나열되는 항목의 수를 나타내는 숫자가 포함됩니다. </p> <p>각 서버에 대해 serverInfo 항목을 추가하고 필요에 따라 매개 변수를 완료합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 주소 </td> 
   <td colname="col2"> 보고서를 생성하기 위해 <span class="keyword"> 보고서 서버 </span>가 연결해야 하는 Data Workbench 서버 시스템의 IP 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> <span class="keyword"> 보고서 서버 </span>가 내부적으로 사용하여 Data Workbench 서버를 식별하는 이름입니다. 내부 레이블이므로 원하는 이름을 사용할 수 있습니다. 일관성을 위해 서버의 디지털 인증서에 나열된 일반 이름을 사용하는 것이 좋습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 포트 </td> 
   <td colname="col2"> <span class="keyword"> 보고서 서버 </span>가 Data Workbench 서버와 통신하는 포트입니다. 보안 연결의 경우 이 값은 일반적으로 443입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프록시 주소 </td> 
   <td colname="col2"> <span class="keyword"> 보고서 서버 </span>가 Data Workbench 서버에 액세스하는 데 사용해야 하는 프록시 서버의 주소입니다. 이 매개 변수는 서버 컴퓨터에 연결하는 데 프록시 서버가 필요한 경우에만 필요합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프록시 암호 </td> 
   <td colname="col2"> 프록시 서버의 암호입니다. 이 매개 변수는 Data Workbench 서버 컴퓨터에 연결하는 데 프록시 서버가 필요한 경우에만 필요합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프록시 포트 </td> 
   <td colname="col2"> 프록시 서버의 포트입니다. 기본값은 8080입니다. 이 매개 변수는 Data Workbench 서버 컴퓨터에 연결하는 데 프록시 서버가 필요한 경우에만 필요합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프록시 사용자 이름 </td> 
   <td colname="col2"> 프록시 서버에 대한 사용자 이름입니다. 이 매개 변수는 Data Workbench 서버 컴퓨터에 연결하는 데 프록시 서버가 필요한 경우에만 필요합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 클라이언트 인증서 </td> 
   <td colname="col2"> <span class="keyword"> 보고서 서버 </span> 컴퓨터에 대한 SSL 인증서 파일의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 서버 공통 이름 </td> 
   <td colname="col2"> <span class="wintitle"> Data  </span> Workbench 서버의 디지털 인증서에 나열된 서버 일반 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL 사용 </td> 
   <td colname="col2"> Data Workbench 서버와 <span class="keyword"> 보고서 서버 </span> 간의 보안 통신에 SSL이 사용되는지 여부를 나타냅니다. 옵션은 true 또는 false입니다. 기본값은 true입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 결과 메모리 제한(KB) </td> 
   <td colname="col2"> <p>보고서 및 경고에 사용할 수 있도록 하려는 메모리 양(KB)입니다. 기본값은 50000입니다. </p> <p>보고서를 실행할 때 <span class="keyword"> 보고서 서버 </span>는 이 값을 먼저 확인한 다음 최대 슬라이스 크기 매개 변수의 값을 확인합니다. 예를 들어, 이 매개 변수를 50,000으로 설정하고 최대 슬라이스 크기를 50으로 설정하면 추가 작업 공간을 실행할 수 있는 공간이 있어도 보고서 서버 <span class="keyword"> 보고서 서버 </span>는 한 번에 50개의 작업 영역만 실행합니다. </p> <p> <p>참고:  이 제한은 Data Workbench 서버의 쿼리 메모리 제한 매개 변수에 설정된 값을 초과해서는 안 되며, 동시에 보고서를 실행할 수 있는 다른 사용자에게 좀 더 나은 방법을 제공하기 위해 <span class="wintitle"> 쿼리 메모리 제한 </span>보다 약간 낮게 설정해야 합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최대 슬라이스 크기 </td> 
   <td colname="col2"> <span class="keyword"> 보고서 서버 </span>가 한 번에 실행할 수 있는 최대 보고서 작업 공간 수입니다. 기본값은 50입니다. <span class="keyword"> 보고서 서버 </span>에서 이 설정을 사용하는 방법에 대한 자세한 내용은 <span class="wintitle"> 결과 메모리 제한(KB) </span> 매개 변수 설명을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 소프트웨어 업데이트 </td> 
   <td colname="col2"> <p>Data Workbench 서버에서 이 <span class="keyword"> 보고서 서버의 </span> 소프트웨어를 업데이트하도록 허용할지 여부를 나타냅니다. 옵션은 true 또는 false입니다. 기본값은 true입니다. </p> <p>다음은 모델을 사용할 수 있는 이 매개변수의 예입니다. </p> <p> <code> Update&amp;nbsp;Software&amp;nbsp;=&amp;nbsp;bool:&amp;nbsp;false </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> OpenGL 하드웨어 렌더링 사용 </td> 
   <td colname="col2"> <p><span class="keyword"> 보고서 서버 </span>에서 하드웨어 렌더링(예: 컴퓨터의 그래픽 카드)을 사용하여 보고서 출력을 생성하는지 여부를 제어합니다. 옵션은 true 또는 false입니다. 기본값은 true입니다. </p> <p>이 매개 변수는 그래픽 카드에 문제가 발생하는 경우에만 false로 설정해야 합니다. false로 설정하면 <span class="keyword"> 보고서 서버 </span>가 하드웨어 렌더링을 사용하지 않고 기본적으로 소프트웨어 렌더링을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 보고 </td> 
   <td colname="col2"> 보고 구성을 위해 설정한 매개 변수의 섹션 식별자입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 완료 메시지 간격 </td> 
   <td colname="col2"> <p>보고서 또는 경고 생성 중에 쿼리를 실행할 때 <span class="keyword"> 보고서 서버 </span>에서 완료 상태 메시지를 출력하는 빈도(초)입니다. 기본값은 120초입니다. </p> <p>예: 작업 공간 쿼리는 62.145672% 완료되었습니다. </p> <p>완료 메시지는 <span class="filepath"> reportserver.log </span>에 기록되며 서버에 동기화됩니다. 이 설정은 각 보고서 세트에 대해 전송되는 <span class="filepath"> status.txt </span> 파일을 제어하므로 완료율이 축소판과 함께 표시될 수 있습니다. 보고서 세트가 완료될 때마다 또는 간격에 도달할 때(어느 쪽이든 첫 번째로 걸릴 때) 메시지가 전송됩니다. 이 값을 높게 설정하면 클라이언트 인터페이스에 축소판으로 생성된 보고서가 표시되는 속도가 영향을 받지 않지만 표시되는 중간 메시지의 개수에 영향을 줍니다. 낮은 값을 지정하면 데이터가 <span class="keyword"> 보고서 서버 </span> 서버에서 프로필, 모든 DPU 및 연결된 모든 클라이언트로 동기화되기 때문에 <span class="filepath"> status.txt </span> 메시지가 변경될 때마다 시스템에서 데이터를 동기화하는 데 많은 시간이 소요될 수 있습니다. </p> <p>시스템은 이 구성 매개 변수의 설정에 관계없이 보고서 세트가 완료되면 항상 <span class="filepath"> status.txt </span> 파일을 보냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 프로필 </td> 
   <td colname="col2"> <p>이 벡터에 나열된 항목의 수를 나타내는 숫자입니다. 보고서를 만들 각 프로필에 대해 Profiles 벡터에 <span class="wintitle"> ReportProfile </span> 항목을 추가하고 서버 및 프로필 매개 변수를 완료합니다. </p> <p> <span class="wintitle"> 서버  </span> -  <span class="keyword"> 보고서 서버가  </span> 내부적으로 Data Workbench 서버를 식별하는 데 사용하는 이름입니다. 이 이름은 Data Workbench 서버의 SSL 인증서에 나열된 서버 일반 이름이어야 합니다. </p> <p> <span class="wintitle"> 프로필  </span> - 보고서를 만들 프로필의 이름입니다. 이 이름은 Data Workbench 서버 컴퓨터의 명명된 프로필과 일치해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 오류에 대한 SMTP 서버 </td> 
   <td colname="col2"> <p>전자 메일을 통해 <span class="wintitle"> 보고서 서버 </span> 오류를 보낼 SMTP 서버의 주소입니다. </p> <p>예: <span class="filepath"> mail.mycompany.com </span> </p> <p>설명한 기능을 사용하려면 SMTP 서버가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 오류 암호를 위한 SMTP 서버 </td> 
   <td colname="col2"> <p>SMTP 서버에 로그인하기 위한 암호입니다. 이 매개 변수는 메일을 보내는 데 로그인이 필요하지 않으면 선택 사항입니다. </p> <p>설명한 기능을 사용하려면 SMTP 서버가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 보낸 사람에 대한 SMTP 서버 오류 보내기 </td> 
   <td colname="col2"> <span class="wintitle"> 보고서 서버 </span> 오류를 보낼 이메일 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SMTP 서버에서 보낸 오류 보내기 </td> 
   <td colname="col2"> <p>경고가 전송되는 이메일 주소입니다. </p> <p>예: <span class="filepath"> adm1@company.com,adm2@company.com </span> </p> <p>설명한 기능을 사용하려면 SMTP 서버가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 오류 사용자 이름에 대한 SMTP 서버 </td> 
   <td colname="col2"> <p>SMTP 서버에 로그인하기 위한 사용자 이름입니다. 이 매개 변수는 메일을 보내는 데 로그인이 필요하지 않으면 선택 사항입니다. </p> <p>설명한 기능을 사용하려면 SMTP 서버가 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상태 간격 </td> 
   <td colname="col2"> <p><span class="wintitle"> 보고서 서버 </span>가 상태 정보를 생성하여 <span class="wintitle"> 세부 상태 </span>에 표시할 Data Workbench 서버로 전송하는 빈도(초)입니다. </p> <p>기본값은 120초입니다. 보고 큐를 실행하는 데 시간이 걸릴 수 있으므로 이 값을 2분 등의 작은 값으로 설정하지 않는 것이 좋습니다. 이 경우 600~1200초 설정을 고려할 수 있습니다. </p> <p><span class="wintitle"> 세부 상태 </span>에 대한 자세한 내용은 <a href="https://experienceleague.adobe.com/docs/data-workbench/using/client/admin-ui/c-admin-intrf.html" format="http" scope="external"> Insight 사용 안내서 </a>의 관리 인터페이스 장을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 업데이트 간격 </td> 
   <td colname="col2"> <p><span class="keyword"> 보고서 서버 </span>가 프로필 벡터에 나열된 모든 프로필을 모니터링하여 새 보고서 및 경고를 수행하는 빈도(분)입니다. 기본값은 10분입니다. </p> <p>지정하는 시간은 나열된 모든 프로필로 나누어집니다. 예를 들어 간격이 10분으로 설정되고 두 프로필을 모니터링하는 경우 각 프로필은 5분 동안 모니터링됩니다. 새 보고서 또는 수정된 보고서 또는 경고를 프로필에 저장할 때 프로필이 모니터링되는 경우 보고서나 경고를 즉시 생성하여 사용할 수 있습니다. </p> <p><span class="wintitle"> 업데이트 간격 </span>이 두 개 이상의 프로필을 모니터링하도록 구성된 경우 이 설정이 구성된 시간 내에 모든 프로필을 로드하기에 충분해야 합니다. 많은 큰 차원이 구성된 시스템(예: 모든 요소 이름으로 초기 데이터 연결을 검색하는 데 몇 분이 걸릴 수 있는 경우, 이 설정이 전체 동기화가 발생할 때까지 충분히 길어야 합니다. 그렇지 않으면 시스템에서 프로파일 동기화 오류가 발생합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
