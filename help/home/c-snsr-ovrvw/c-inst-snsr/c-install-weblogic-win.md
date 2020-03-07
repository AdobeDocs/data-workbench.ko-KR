---
description: Microsoft Windows Server 2000 이상에서 실행 중인 WebLogic Server 6.x 이상용 센서의 설치 및 구성에 대한 자세한 지침
title: Windows Server 2000 이상 버전의 WebLogic Server
uuid: 80dbf544-bd09-4af8-bb05-4032eb49dd5d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Windows Server 2000 이상 버전의 WebLogic Server{#weblogic-server-on-windows-server-or-later}

Microsoft Windows Server 2000 이상에서 실행 중인 WebLogic Server 6.x 이상용 센서의 설치 및 구성에 대한 자세한 지침

센서용 프로그램 파일은 Adobe 다운로드 사이트에서 다운로드한 설치 파일로 패키지되어 있습니다. 특정 웹 서버에 대한 Sensor 설치 파일이 없는 경우 다음 절차를 시작하기 전에 해당 파일을 다운로드(또는 Adobe 담당자에게 제공)하십시오.

센서를 설치하고 구성하려면 다음 단계를 수행해야 합니다.

## 프로그램 파일 설치 {#section-2f3e85083b4f4aa989a85997330e86ae}

센서용 프로그램 파일을 추출하고 설치하는 절차.

1. WebLogic Server에서 Sensor 프로그램 파일을 설치할 디렉토리를 만듭니다. 디스크 대기열이 이 디렉토리에 있으므로 선택한 장치에 필요한 크기의 큐를 저장할 충분한 공간이 있는지 확인하십시오.

   ```
   C:\VisualSensor
   ```

1. 설치 파일의 내용을 방금 만든 디렉토리에 추출합니다. 이 단계 동안 Sensor는 다음 파일을 설치합니다.

<table id="table_ABFF5F92271B4F3CB0AC68DAB6A5709F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 파일 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 대상 디렉토리 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> visual_sciences.dll </td> 
   <td colname="col2"> 컬렉터 로드 모듈입니다. </td> 
   <td colname="col3"> 모든 디렉토리에 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> J2EECollector.jar </td> 
   <td colname="col2"> 컬렉터 로드 모듈 라이브러리 </td> 
   <td colname="col3"> WEB-INF/lib </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogd.exe </p> </td> 
   <td colname="col2"> 송신기 프로그램 </td> 
   <td colname="col3"> 모든 디렉토리 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> 센서 구성 파일입니다. </td> 
   <td colname="col3"> 모든 디렉토리 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> 연결 프로세스 동안 Insight Server가 제공하는 디지털 인증서의 유효성을 확인하는 데 사용되는 인증서 </td> 
   <td colname="col3"> 모든 디렉토리 </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>설치 패키지에는 호출된 스프레드시트 파일이 들어 [!DNL TestExperiment.xls]있습니다. 이 스프레드시트는 설계자가 제어 실험을 구성하는 데 사용하는 도구입니다. 센서 자체에서 이 파일을 사용하지 않으므로 센서 실행 중인 시스템에 파일을 설치할 필요는 없습니다(선택할 수 있지만). 대신 파일을 설계자가 액세스할 수 있는 위치에 복사하거나 필요에 따라 설치 패키지에서 파일을 추출할 수 있습니다. 제어된 실험에 대한 자세한 내용은 인사이트 제어 실험 안내서를 참조하십시오.

## 센서 구성 파일 편집 {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

이 [!DNL txlogd.conf] 파일에는 센서의 구성 매개 변수가 포함되어 있습니다.

이 파일을 편집하여 디스크 큐 파일의 크기와 위치, Insight Server 주소, 그리고 이 센서가 제작한 이벤트 데이터에 연결될 ID를 지정해야 합니다.

구성 파일에는 필수 매개 변수와 선택적 매개 변수가 포함되어 있습니다.

* **필수 매개 변수는** Sensor를 설치할 때 지정해야 하는 설정입니다. 이러한 설정이 없으면 센서가 제대로 실행되지 않습니다.
* **선택적 매개 변수는** 기본적으로 사전 정의된 값(수정할 수 있음)으로 설정되거나 선택적 기능을 활성화하는 설정입니다.

**센서 구성 파일을 편집하려면**

* 텍스트 편집기에서 파일을 열고 필요한 매개 변수와 원하는 선택적 매개 변수를 설정합니다. [!DNL /etc/txlogd.conf]
* 파일을 저장하고 닫습니다.

**센서 구성 파일을 편집하려면**

1. 텍스트 편집기에서 파일을 열고 필요한 매개 변수와 원하는 선택적 매개 변수를 설정합니다. [!DNL /etc/txlogd.conf]
1. 파일을 저장하고 닫습니다.

## 전송기 시작 및 디스크 대기열 만들기 {#section-55630de65f264274aefd771da2002852}

txlogd.conf 파일을 구성한 후 전송기 프로그램을 시작하고 Windows 서비스로 등록하고 디스크 대기열을 만들 수 있습니다.

1. Windows의 시작 메뉴에서 보조프로그램 > 명령 프롬프트를 선택합니다.
1. 명령 프롬프트 창에서 Sensor를 설치한 디렉토리로 이동하여 다음 명령을 실행합니다.

   ```
   txlog /regserver
   ```

   이 명령은 전송기를 시작하고 디스크 큐를 만들고 Sensor를 Windows 서비스로 등록합니다.

1. 전송기가 제대로 실행되는지 확인하려면 시작 > 제어판 > 관리 도구 > 서비스를 클릭합니다.

   >[!NOTE]
   >
   >이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.

   1. 서비스 목록에서 센서의 항목을 찾아 상태가 시작이고 시작 유형이 자동인지 확인합니다.
   1. 서비스 제어판을 닫습니다.

1. 시작 중에 전송기에 오류가 있는지 확인하려면 [시작] > [제어판] > [관리 도구] > [이벤트 뷰어]를 클릭하여 이벤트 뷰어를 엽니다.

   1. [이벤트 뷰어] 창의 왼쪽 창에서 응용 프로그램 로그를 선택합니다.
   1. 오른쪽 창에서 소스 열에 &quot;Adobe&quot;가 있는 이벤트를 찾습니다.
   1. &quot;Adobe&quot;에서 오류가 발견되면 오류를 두 번 클릭하여 이벤트 속성 창을 표시합니다. 이 창은 오류에 대한 자세한 정보를 제공합니다.

1. 응용 프로그램 로그 검사를 마치면 이벤트 뷰어를 닫습니다.
1. 전송기가 Sensor 프로그램 파일을 설치한 디렉토리에 디스크 대기열(Diskq2000.log)을 생성했는지, 그리고 이 크기가 txlogd.conf 파일의 QueueSize 매개 변수에서 지정한 크기인지 확인합니다.

   큐가 올바르게 생성되지 않은 경우:

   1. txtlogd.conf 파일을 검사하고 QueueSize 매개 변수가 올바르게 설정되어 있는지 확인합니다.
   1. Sensor를 설치한 장치에 QueueSize 매개 변수에 지정된 크기의 파일을 저장할 수 있는 충분한 공간이 있는지 확인합니다.
   1. Windows에서 서비스 제어판을 사용하여 전송기를 중지합니다.
   1. 큐 파일을 삭제합니다.
   1. Windows 서비스로 센서 재등록:windows의 시작 메뉴에서 보조프로그램 > 명령 프롬프트를 선택합니다. 명령 프롬프트 창에서 Sensor를 설치한 디렉토리로 이동하여 다음 명령을 실행합니다.

      ```
      txlog /regserver
      ```

송신기는 지속적으로 실행되도록 설계되었습니다. 시스템을 다시 시작하면 전송기가 자동으로 다시 시작됩니다. 전송기를 수동으로 시작 및 중지해야 하는 경우 Windows의 서비스 제어판을 사용하여 시작할 수 있습니다.

## 웹 서버에 Collector 추가 {#section-c5b83ae4ebce430aa764f951e849b333}

JBoss 서버의 경우 수집기는 서블릿 컨테이너에서 필터로 작동합니다.

Collector를 웹 서버에 추가하려면 아래 설명에 따라 [!DNL web.xml] 파일을 편집하고 웹 애플리케이션을 다시 시작해야 합니다.

1. 텍스트 편집기를 사용하여 Sensor가 캡처하는 이벤트가 있는 웹 서버의 [!DNL web.xml] 파일을 엽니다.
1. 설명자 파일에 다음 `<filter>` 및 `<filter-mapping>` 요소를 추가합니다. /etc 디렉토리에 txlogd.conf를 설치하지 않은 경우 `<param-value>` 요소에 이 파일의 올바른 경로를 입력해야 합니다.

   ```
   <filter> 
     <filter-name>VSCollectorFilter</filter-name> 
     <description></description> 
     <filter-class> 
         com.visualsciences.collector.VSCollectorFilter 
       </filter-class> 
     <init-param> 
       <param-name>configPath</param-name> 
       <param-value>C:/VisualSensor/txlogd.conf</param-value> 
     <description></description> 
     </init-param> 
   </filter> 
   
   <filter-mapping> 
     <filter-name>VSCollectorFilter</filter-name> 
     <url-pattern>/*</url-pattern> 
   </filter-mapping> 
   ```

   >[!NOTE]
   >
   >이 줄은 대소문자를 구분합니다. 위에 표시되는 그대로 입력합니다.

1. 웹 서버 프로세스를 다시 시작합니다. 전체 서버 컴퓨터를 다시 부팅하지 않아도 되고 웹 서버 프로세스를 다시 시작하면 됩니다. 수집기는 웹 서버와 함께 로드되고 이벤트 데이터를 수집하여 디스크 큐에 쓰기 시작합니다.

## 시작 스크립트 수정 {#section-0dae181ef8884f10a57f6cfda8500969}

시작 스크립트 수정을 위한 지침

WebLogic을 시작하는 데 사용되는 스크립트(예: C:\bea\user_projects\mydomain\startServer.cmd)에서 &quot;set JAVA_OPTIONS=&quot; 줄을 편집하여 java.library.path 정의를 visual_sciences.dll 파일이 들어 있는 디렉토리로 설정합니다.

```
set JAVA_OPTIONS=-Djava.library.path=C:\Sensor 
    directory
```

## 추가 데이터 캡처 {#section-9483b663cbd0432daaca50c1089c7fca}

appendToLog() 기능을 사용하여 J2EE 기반 웹 응용 프로그램에서 추가 측정 데이터를 캡처할 수 있습니다.

1. 데이터를 캡처할 .jsp 페이지의 맨 위에 다음 코드를 추가합니다.

   ```
   <%@ page import="com.visualsciences.collector.VSCollector" %> 
   ```

1. 컬렉터 객체의 appendToLog() 메서드를 사용하여 원하는 이름-값 쌍을 요청된 .jsp 페이지의 쿼리 문자열에 추가합니다. 다음 예는 &quot;A=1&quot; 및 &quot;B=2&quot;를 요청한 .jsp 페이지의 /index.jsp 페이지에 대한 쿼리 문자열에 추가합니다.

   ```
   <html> 
   <body> 
     <h1>Hello World</h1> 
     <% 
       VSCollector collector = new VSCollector(request, response); 
       collector.appendToLog("A", "1"); 
       collector.appendToLog("B", "2"); 
     %> 
   </body> 
   </html> 
   ```

   결과 요청 URI는 /index.jsp?A=1&amp;B=2입니다.

1. 추가 데이터를 캡처할 각 .jsp 페이지에 대해 이 절차를 반복합니다.

