---
description: RedHat Linux 7.x 이상, Sun Solaris SPARC 2.6 이상 또는 Sun Solaris x86 9 이상에서 실행되는 J2EE 구현을 위한 Sensor 설치 및 구성에 대한 자세한 지침
title: RedHat Linux 또는 Sun Solaris 기반 JBoss, Tomcat 및 WebLogic 서버
uuid: 7977fb9b-1737-4e1d-80c6-aabf968974dd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# RedHat Linux 또는 Sun Solaris 기반 JBoss, Tomcat 및 WebLogic 서버{#jboss-tomcat-and-weblogic-servers-on-redhat-linux-or-sun-solaris}

RedHat Linux 7.x 이상, Sun Solaris SPARC 2.6 이상 또는 Sun Solaris x86 9 이상에서 실행되는 J2EE 구현을 위한 Sensor 설치 및 구성에 대한 자세한 지침

센서용 프로그램 파일은 Adobe 다운로드 사이트에서 다운로드한 설치 파일로 패키지되어 있습니다. 특정 웹 서버에 대한 Sensor 설치 파일이 없는 경우 다음 절차를 시작하기 전에 해당 파일을 다운로드(또는 Adobe 담당자에게 제공)하십시오.

지원되는 J2EE 구현은 다음과 같습니다.

* JBoss Server 3.2.x 이상
* Apache Jakarta Tomcat Server 4.1 이상
* WebLogic Server 6.x 이상

센서를 설치하고 구성하려면 다음 단계를 수행해야 합니다.

## 프로그램 파일 설치 {#section-2f3e85083b4f4aa989a85997330e86ae}

센서용 프로그램 파일을 추출하고 설치하는 절차.

1. 루트 사용자 또는 루트 권한이 있는 사용자로 로그온합니다.
1. 다음 명령을 사용하여 설치 파일의 압축을 풀고 압축을 해제합니다.

   * Linux의 경우:

      ```
      tar -zxf installationFilename.tar.gz
      ```

   * Solaris의 경우:

      ```
      unzip -d installationFilename.tar.gz 
       tar -xf installationFilename.tar
      ```

1. 압축을 푼 프로그램 파일을 다음 표에 나와 있는 디렉토리에 복사합니다.

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
   <td colname="col1"> mod_visual_sciences.so </td> 
   <td colname="col2"> 컬렉터 로드 모듈입니다. </td> 
   <td colname="col3"> <i> IBMHttpServer/모듈</i> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogd </p> </td> 
   <td colname="col2"> 송신기 프로그램 </td> 
   <td colname="col3"> <p><i>/usr/local/bin</i> </p> <p><i>--또는--</i> </p> <p><i>/usr/local/sbin</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> 센서 구성 파일입니다. </td> 
   <td colname="col3"> <i>/etc</i> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> 연결 프로세스 동안 Insight Server가 제공하는 디지털 인증서의 유효성을 확인하는 데 사용되는 인증서 </td> 
   <td colname="col3"> <i>/usr/local/visual_sciences</i> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>설치 패키지에는 TestExperiment.xls라는 스프레드시트 파일이 들어 있습니다. 이 스프레드시트는 설계자가 제어 실험을 구성하는 데 사용하는 도구입니다. 센서 자체에서 이 파일을 사용하지 않으므로 센서 실행 중인 시스템에 파일을 설치할 필요는 없습니다(선택할 수 있지만). 대신 파일을 설계자가 액세스할 수 있는 위치에 복사하거나 필요에 따라 설치 패키지에서 파일을 추출할 수 있습니다. 제어된 실험에 대한 자세한 내용은 인사이트 제어 실험 안내서를 참조하십시오.

**프로그램 파일에 대한 권한**

>[!NOTE]
>
>프로그램 파일에 대한 권한이 잘못되면 센서가 설치될 때 발생하는 대부분의 문제가 발생합니다. 이 섹션에 명시된 대로 권한을 설정해야 합니다.
>
>기본적으로 tar 파일의 프로그램 파일에는 다음 권한이 있습니다. 시스템 구성 방식에 따라 파일을 추출할 때 이러한 설정이 변경(마스크 해제)될 수 있습니다. 사용 권한을 권장 기본 설정으로 재설정하려면 아래 chmod 명령을 사용합니다. 파일을 설치한 디렉토리에 이 수준의 액세스가 허용되는지 확인합니다.

| 파일 | 기본 권한 | chmod 명령 |
|---|---|---|
| mod_visual_sciences.so | rwx r-x r-x | chmod 775 |
| txlogd | rwx —x —x | chmod 711 |
| txlogd.conf | rw- r— r— r— | chmod 664 |
| trust_ca_cert.pem | rw- r— r— r— | chmod 664 |

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

1. 디스크 큐가 있는 디렉토리가 없는 경우 해당 디렉토리를 만듭니다. 디렉토리에 Collector 모듈과 송신기 프로그램이 모두 파일에 대한 읽기/쓰기 액세스 권한을 제공하는지 확인합니다.

   디스크 큐 파일에 필요한 권한에 대한 자세한 내용은 Sensor UNIX 파일 권한을 참조하십시오.
1. 센서가 설치된 컴퓨터에서 다음 명령을 실행하여 송신기를 시작합니다.

   ```
   /usr/local/bin/txlogd -ic -f /etc/txlogd.conf
   ```

   * 이 명령의 &quot;i&quot; 옵션은 송신기를 &quot;대화형 모드&quot;로 시작합니다. 이 모드는 송신기 메시지를 화면에 표시하고 키보드 명령을 사용하여 송신기와 상호 작용할 수 있도록 해줍니다.
   * &quot;c&quot; 옵션은 전송기가 디스크 큐를 만들도록 합니다.
   * &quot;f&quot; 옵션은 구성 파일의 위치를 지정합니다.
   송신기를 시작할 때 사용할 수 있는 옵션에 대한 자세한 내용은 센서 전송기 명령줄 옵션을 참조하십시오.

1. 전송기가 QueueFile 매개 변수에 지정된 위치 및 QueueSize 매개 변수에 지정된 크기의 디스크 큐를 만들었는지 확인합니다.
1. 큐가 올바르게 생성되지 않은 경우 Ctrl+C를 입력하여 전송기를 종료한 다음 다음을 수행합니다.

   1. txtlogd.conf 파일을 검토하고 QueueFile 및 QueueSize 매개 변수가 올바르게 설정되어 있는지 확인합니다.
   1. 디스크 큐가 할당된 장치가 작동하고 QueueSize 매개 변수에 지정된 크기의 파일을 저장할 수 있는 충분한 공간이 있는지 확인합니다.
   1. 필요한 수정을 수행하고 이 절차를 반복합니다.

## 웹 서버에 Collector 추가 {#section-c5b83ae4ebce430aa764f951e849b333}

Apache 서버의 경우 수집기는 웹 서버 프로세스로 로드하는 동적 공유 오브젝트입니다.

Collector를 웹 서버에 추가하려면 아래 설명에 따라 [!DNL httpd.conf] 파일을 편집하고 웹 서버를 다시 시작해야 합니다.

>[!NOTE]
>
>Sensor가 서버 컴퓨터에 있는 여러 웹 서버에 대한 데이터를 캡처하는 경우 각 웹 서버에 대해 다음 절차를 수행해야 합니다.

1. 텍스트 편집기를 사용하여 Sensor가 캡처하는 이벤트가 있는 웹 서버의 [!DNL httpd.conf]파일을 엽니다.
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
       <param-value>/etc/txlogd.conf</param-value> 
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

## 센서 테스트 {#section-0dae181ef8884f10a57f6cfda8500969}

수집기가 이벤트 데이터를 수집하고 있고 전송기가 이를 대상 Insight Server로 전송하는지 확인합니다.

>[!NOTE]
>
>전송기가 이벤트 데이터를 Insight Server로 성공적으로 전송할 수 있는지 확인하려면 다음 테스트를 시작하기 전에 대상 Insight Server가 설치되어 실행 중인지 확인하십시오.

1. 전송기가 아직 실행되고 있지 않으면 다음 명령을 사용하여 다시 시작합니다.

   ```
   /usr/local/bin/txlogd -i -f /etc/txlogd.conf 
   ```

1. 브라우저를 열고(모든 컴퓨터에서) 센서가 실행 중인 웹 서버에서 페이지를 요청합니다(센서가 모니터링하고 있는 페이지 선택).
1. 요청을 발행한 후 전송자의 콘솔에서 이벤트 데이터를 대상 Insight Server로 전송하고 있음을 나타내는 메시지를 확인합니다.
1. 센서가 데이터를 성공적으로 전송하지 않으면 다음을 확인하십시오.

   * 대상 Insight 서버가 실행 중입니다.
   * ServerAddress 및 ServerPort 매개 변수는 txtlogd.conf에서 올바르게 설정됩니다. 서버 이름을 사용하여 ServerAddress를 지정한 경우 숫자 IP 주소를 대신 사용하십시오.
   * CertName 매개 변수의 값은 대상 Insight Server의 디지털 인증서에 표시되는 일반 이름과 정확히 일치합니다.

## 시스템 시작 스크립트에 송신기 추가 {#section-19a38f27c9f44adf88f8910f5ed483a3}

전송기를 시스템 시작 스크립트에 자동으로 로드하는 방법에 대한 정보입니다.

웹 서버 시스템을 다시 시작할 때 전송기가 자동으로 로드되도록 하려면 시스템 시작 스크립트에 다음 명령(전송기 시작)을 추가합니다.

```
/usr/local/bin/txlogd -f /etc/txlogd.conf
```

이 명령은 송신기를 데몬으로 시작합니다. 전송자가 생성하는 운영 및 오류 메시지는 에 [!DNL syslog]기록됩니다.

기본 Solaris 설정은 60입니다. Sensor에서 수행한 테스트를 기준으로, 각 인스턴스에 대해 세 개의 세미나를 사용하는 경우, Adobe는 1024를 설정으로 사용하는 것이 좋습니다. 이 수는 센서가 세미아포어가 필요할 수 있지만 성능에 영향을 주지 않는 서버의 다른 응용 프로그램과 함께 작동할 수 있을 만큼 높습니다. 이 권장 사항을 지지하기 위해, 애드리안 콕크로프트는 그의 저서 선퍼포먼스 및 튜닝(1994년 10월 플래스티홀)에서 다음 사항을 적었습니다.&quot;데이터베이스는 많은 공유 메모리와 세마포 설정을 사용하는 경향이 있습니다. 성능에는 영향을 주지 않습니다.큰 것이면 프로그램이 진행될 것이다.&quot;

## 추가 데이터 캡처 {#section-9483b663cbd0432daaca50c1089c7fca}

모든 플랫폼에 대한 센서는 HTTP 요청 및 응답 헤더에서 사용할 수 있는 모든 데이터를 수집할 수 있습니다.

J2EE 플랫폼용 센서는 다른 플랫폼에서 사용할 수 없는 데이터를 수집하는 메커니즘을 제공합니다. J2EE 플랫폼(J2EE 수집기)용 컬렉터는 애플리케이션 레이어에 배치하여 애플리케이션에서만 사용할 수 있고 페이지 태그 지정 또는 헤더를 통해 노출되어서는 안 되는 중요한 데이터를 수집할 수 있습니다.

>[!NOTE]
>
>페이지 태그 및 헤더 수정 기능은 데이터를 숨길 수 있지만, 페이지의 소스 코드를 검사하거나 브라우저 플러그인 도구를 사용하여 헤더를 보는 사람도 여전히 데이터를 볼 수 있습니다.

예를 들어 J2EE 수집기를 사용하여 페이지에 표시되는 링크의 CPC(Cost Per Click) 데이터, 페이지의 중요한 파트너 정보 및 기타 많은 데이터 포인트를 캡처할 수 있습니다. J2EE 환경을 사용하면 Adobe의 수집기 클래스를 사용하여 이 사용자 지정 데이터를 캡처하도록 WEBAPP을 쉽게 수정할 수 있습니다.

J2EE 플랫폼용 센서가 요청을 받으면 appendToLog 함수를 가져오는 컬렉터 클래스를 호출합니다. appendToLog 함수는 appendToLog 함수에 지정된 쿼리 문자열 매개 변수를 초기 요청에 추가합니다. 이렇게 하면 캡처되는 데이터의 이름 및 값에 해당하는 추가 쿼리 문자열 이름-값 쌍을 포함하는 초기 요청의 URI가 생성됩니다. 예를 들어 CPC=20은 특정 광고 배치 또는 클릭스루 링크의 값이 20센트일 때 초기 요청에 추가됩니다. Insight Server는 분석을 위해 이러한 값을 데이터 세트에 처리합니다. 이 수집 방법의 한 가지 또 다른 이점은 페이지 태그 지정 방법을 사용하여 만들 수 있는 추가 로그 항목을 만들지 않고도 추가 데이터를 수집할 수 있다는 것입니다.

처리에 대한 자세한 내용은 데이터 집합 구성 안내서를 참조하십시오.

**페이지에서 추가 데이터를 캡처하려면**

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

