---
description: RedHat Linux 7.x 이상, Sun Solaris SPARC 2.6 이상 또는 Sun Solaris x86 9 이상에서 실행되는 J2EE 구현을 위한 Sensor 설치 및 구성에 대한 자세한 지침
title: RedHat Linux 또는 Sun Solaris 기반 JBoss, Tomcat 및 WebLogic 서버
uuid: 7977fb9b-1737-4e1d-80c6-aabf968974dd
exl-id: 09c2f266-2ecc-42fc-98b6-b91f8883af0c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1823'
ht-degree: 1%

---

# RedHat Linux 또는 Sun Solaris 기반 JBoss, Tomcat 및 WebLogic 서버{#jboss-tomcat-and-weblogic-servers-on-redhat-linux-or-sun-solaris}

{{eol}}

RedHat Linux 7.x 이상, Sun Solaris SPARC 2.6 이상 또는 Sun Solaris x86 9 이상에서 실행되는 J2EE 구현을 위한 Sensor 설치 및 구성에 대한 자세한 지침

센서용 프로그램 파일은 Adobe 다운로드 사이트에서 가져온 설치 파일에 패키지되어 있습니다. 특정 웹 서버에 대한 센서 설치 파일이 아직 없는 경우 다음 절차를 시작하기 전에 해당 파일을 다운로드(또는 Adobe 담당자로부터 획득)하십시오.

지원되는 J2EE 구현은 다음과 같습니다.

* JBoss Server 3.2.x 이상
* Apache Jakarta Tomcat Server 4.1 이상
* WebLogic Server 6.x 이상

센서를 설치하고 구성하려면 다음 단계를 수행해야 합니다.

## 프로그램 파일 설치 {#section-2f3e85083b4f4aa989a85997330e86ae}

센서용 프로그램 파일을 추출 및 설치하는 절차.

1. 루트 사용자로 또는 루트 권한을 가진 사용자로 로그온합니다.
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

1. 압축을 푼 프로그램 파일을 다음 표에서 식별된 디렉토리에 복사합니다.

<table id="table_ABFF5F92271B4F3CB0AC68DAB6A5709F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 파일 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> Target 디렉토리 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> mod_visual_sciences.so </td> 
   <td colname="col2"> 컬렉터 로드 모듈입니다. </td> 
   <td colname="col3"> <i> IBMHttpServer/modules</i> </td> 
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
   <td colname="col2"> 연결 프로세스 중에 Insight Server가 제공하는 디지털 인증서의 유효성을 검사하는 데 사용되는 인증서입니다 </td> 
   <td colname="col3"> <i>/usr/local/visual_sciences</i> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>설치 패키지에는 TestExperiment.xls라는 스프레드시트 파일이 들어 있습니다. 이 스프레드시트는 설계자가 통제 실험을 구성하는 데 사용하는 도구입니다. 센서 자체는 이 파일을 사용하지 않으므로 센서가 실행 중인 시스템에 파일을 설치할 필요는 없습니다(설치하도록 선택할 수 있지만). 대신 설계자가 액세스할 수 있는 위치에 파일을 복사하거나 필요에 따라 설치 패키지에서 파일을 추출할 수 있습니다. 통제 실험에 대한 자세한 내용은 Insight 통제 실험 안내서를 참조하십시오.

**프로그램 파일에 대한 권한**

>[!NOTE]
>
>프로그램 파일에 대한 권한이 잘못되어 센서를 설치할 때 발생하는 대부분의 문제가 발생합니다. 이 섹션에 설명된 대로 권한을 정확히 설정했는지 확인하십시오.
>
>기본적으로 tar 파일의 프로그램 파일에는 다음 권한이 있습니다. 시스템 구성 방식에 따라 파일을 추출할 때 이러한 설정을 변경(마스크 해제)할 수 있습니다. 사용 권한을 권장 기본 설정으로 재설정하려면 아래의 chmod 명령을 사용하십시오. 파일을 설치한 디렉터리가 이 수준의 액세스를 허용하는지 확인합니다.

| 파일 | 기본 권한 | chmod 명령 |
|---|---|---|
| mod_visual_sciences.so | rwx r-x r-x | chmod 775 |
| txlogd | rwx —x —x | chmod 711 |
| txlogd.conf | rw- r— r— | chmod 664 |
| trust_ca_cert.pem | rw- r— r— | chmod 664 |

## 센서 구성 파일 편집 {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

다음 [!DNL txlogd.conf] 파일에 센서에 대한 구성 매개 변수가 포함되어 있습니다.

이 파일을 편집하여 디스크 큐 파일의 크기 및 위치, Insight Server 주소 및 이 센서에서 생성한 이벤트 데이터에 첨부할 ID를 지정해야 합니다.

구성 파일에는 필수 매개 변수와 선택적 매개 변수가 포함되어 있습니다.

* **필수 매개 변수** 은 센서를 설치할 때 지정해야 하는 설정입니다. 이 설정이 없으면 센서가 제대로 실행되지 않습니다.
* **선택적 매개 변수** 기본적으로 사전 정의된 값(수정할 수 있음)으로 설정되거나 선택적 기능을 활성화할 수 있습니다.

**센서 구성 파일을 편집하려면**

* 를 엽니다. [!DNL /etc/txlogd.conf] 파일을 텍스트 편집기에 넣고 필요한 매개 변수와 원하는 선택적 매개 변수를 설정합니다.
* 파일을 저장하고 닫습니다.

**센서 구성 파일을 편집하려면**

1. 를 엽니다. [!DNL /etc/txlogd.conf] 파일을 텍스트 편집기에 넣고 필요한 매개 변수와 원하는 선택적 매개 변수를 설정합니다.
1. 파일을 저장하고 닫습니다.

## 전송기를 시작하고 디스크 큐 만들기 {#section-55630de65f264274aefd771da2002852}

txlogd.conf 파일을 구성한 후 전송 프로그램을 시작하고 Windows 서비스로 등록하고 디스크 큐를 만들 수 있습니다.

1. 디스크 큐가 있는 디렉토리가 없는 경우 해당 디렉토리를 만듭니다. 디렉토리는 해당 파일에 대한 읽기/쓰기 액세스를 수집기 모듈과 송신기 프로그램 모두에 제공하도록 합니다.

   디스크 큐 파일에 필요한 권한에 대한 자세한 내용은 Sensor UNIX 파일 권한 을 참조하십시오.
1. 센서가 설치된 컴퓨터에서 다음 명령을 실행하여 전송기를 시작합니다.

   ```
   /usr/local/bin/txlogd -ic -f /etc/txlogd.conf
   ```

   * 이 명령의 &quot;i&quot; 옵션은 전송기를 &quot;대화형 모드&quot;로 시작합니다. 이 모드에서는 전송 메시지가 화면에 표시되고, 키보드 명령을 사용하여 송신기와 상호 작용할 수도 있습니다.
   * &quot;c&quot; 옵션은 전송기가 디스크 큐를 생성하도록 지시합니다.
   * &quot;f&quot; 옵션은 구성 파일의 위치를 지정합니다.

   전송기를 시작할 때 사용할 수 있는 옵션에 대한 자세한 내용은 센서 송신기 명령줄 옵션을 참조하십시오.

1. 전송기가 QueueFile 매개 변수에 지정된 위치와 QueueSize 매개 변수에 지정된 크기의 디스크 큐를 만들었는지 확인합니다.
1. 큐가 올바르게 생성되지 않은 경우 Ctrl+C 를 입력하여 전송기를 종료한 다음 작업을 수행합니다.

   1. txtlogd.conf 파일을 검토하고 QueueFile 및 QueueSize 매개 변수가 올바르게 설정되었는지 확인합니다.
   1. 디스크 큐가 할당된 장치가 작동 중이고 QueueSize 매개 변수에 지정된 크기의 파일을 보관할 수 있는 충분한 공간이 있는지 확인합니다.
   1. 필요한 수정을 수행하고 이 절차를 반복합니다.

## 웹 서버에 Collector 추가 {#section-c5b83ae4ebce430aa764f951e849b333}

Apache 서버의 경우 수집기는 웹 서버 프로세스에 로드하는 동적 공유 객체입니다.

웹 서버에 컬렉터를 추가하려면 [!DNL httpd.conf] 아래 설명된 대로 파일을 작성한 후 웹 서버를 다시 시작합니다.

>[!NOTE]
>
>Sensor가 서버 컴퓨터의 여러 웹 서버에 대한 데이터를 캡처하는 경우 각 웹 서버에 대해 다음 절차를 수행해야 합니다.

1. 텍스트 편집기를 사용하여 [!DNL httpd.conf]센서가 캡처하는 웹 서버의 파일입니다.
1. 다음을 추가합니다 `<filter>` 및 `<filter-mapping>` 설명자 파일에 요소를 추가합니다. /etc 디렉토리에 txlogd.conf를 설치하지 않은 경우 `<param-value>` 요소:

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
   >이 줄은 대/소문자를 구분합니다. 위에 표시된 그대로 입력합니다.

1. 웹 서버 프로세스를 다시 시작합니다. 전체 서버 컴퓨터를 다시 부팅하지 않아도 됩니다. 웹 서버 프로세스를 다시 시작하면 됩니다. 수집기는 웹 서버와 함께 로드되어 이벤트 데이터를 수집하여 디스크 큐에 쓰기 시작합니다.

## 센서 테스트 {#section-0dae181ef8884f10a57f6cfda8500969}

수집기가 이벤트 데이터를 수집하고 있고 전송기가 이를 대상 Insight Server로 전송하는지 확인합니다.

>[!NOTE]
>
>전송기가 이벤트 데이터를 Insight Server에 성공적으로 전송할 수 있는지 확인하려면 다음 테스트를 시작하기 전에 대상 Insight Server가 설치 및 실행 중인지 확인하십시오.

1. 전송기가 아직 실행되고 있지 않으면 다음 명령을 사용하여 다시 시작하십시오.

   ```
   /usr/local/bin/txlogd -i -f /etc/txlogd.conf 
   ```

1. 브라우저를 열고(어느 시스템에서든) 센서가 실행 중인 웹 서버에서 페이지를 요청합니다(센서가 모니터링 중인 페이지를 선택).
1. 요청을 실행한 후 전송기의 콘솔에서 이벤트 데이터를 target Insight Server로 전송하고 있음을 나타내는 메시지를 확인합니다.
1. 센서가 데이터를 성공적으로 전송하지 않으면 다음을 확인하십시오.

   * 대상 Insight Server가 실행 중입니다.
   * ServerAddress 및 ServerPort 매개 변수가 txtlogd.conf에 올바르게 설정되어 있습니다. 서버 이름을 사용하여 ServerAddress를 지정한 경우 해당 숫자 IP 주소를 대신 사용해 보십시오.
   * CertName 매개 변수 값은 대상 Insight Server의 디지털 인증서에 표시되는 일반 이름과 정확히 일치합니다.

## 시스템 시작 스크립트에 송신기 추가 {#section-19a38f27c9f44adf88f8910f5ed483a3}

시스템 시작 스크립트에 전송기를 자동으로 로드하는 방법에 대한 정보입니다.

웹 서버 시스템을 다시 시작할 때 전송기가 자동으로 로드되도록 하려면 시스템 시작 스크립트에 다음 명령(전송기를 시작하는 명령)을 추가합니다.

```
/usr/local/bin/txlogd -f /etc/txlogd.conf
```

이 명령은 전송기를 데몬으로 시작합니다. 송신기가 생성하는 운영 및 오류 메시지에 [!DNL syslog].

기본 Solaris 설정은 60입니다. 각 인스턴스에 대해 세 개의 세미풀을 사용하는 Sensor에서 수행한 테스트를 기반으로, Adobe은 1024를 설정으로 사용하는 것을 권장합니다. 이 숫자는 센서가 세미포어가 필요할 수 있지만 성능에 영향을 주지 않는 서버의 다른 애플리케이션과 함께 작동하기에 충분할 만큼 높습니다. 이 권고사항을 지지하기 위해, 애드리안 콕크로프트는 그의 책 선퍼포먼스 앤 튜닝(1994년 10월, 공관장)에서 다음과 같은 내용을 적었다는 것을 주의하십시오. &quot;데이터베이스는 공유 메모리와 세마포 설정을 많이 사용하는 경향이 있습니다. 성능에 영향을 주지 않습니다. &quot;충분히 커지면 프로그램이 진행될 것입니다.&quot;

## 추가 데이터 캡처 {#section-9483b663cbd0432daaca50c1089c7fca}

모든 플랫폼에 대한 센서는 HTTP 요청 및 응답 헤더에서 사용할 수 있는 데이터를 수집할 수 있습니다.

J2EE 플랫폼용 센서는 다른 플랫폼에서 사용할 수 없는 데이터를 수집하는 메커니즘을 제공합니다. J2EE Platform(J2EE Collector)용 컬렉터는 응용 프로그램 레이어에 배치되어 응용 프로그램에서만 사용할 수 있고 페이지 태깅이나 헤더에서 노출되어서는 안 되는 중요한 데이터를 수집할 수 있습니다.

>[!NOTE]
>
>페이지 태그 및 헤더 수정 사항은 데이터를 숨길 수 있지만 페이지의 소스 코드를 검사하거나 브라우저 플러그인 도구를 사용하여 헤더를 보는 사람은 여전히 사용할 수 있습니다.

예를 들어, J2EE 수집기는 페이지에 표시되는 링크에 대한 CPC(Cost per Click) 데이터, 페이지의 중요한 파트너 정보 및 기타 많은 데이터 포인트를 캡처하는 데 사용할 수 있습니다. J2EE 환경을 사용하면 수집기 클래스를 사용하여 이 사용자 지정 데이터를 캡처하도록 WEBAPP을 쉽게 수정할 수 있습니다.

J2EE 플랫폼용 센서가 요청을 받으면 appendToLog 함수를 가져오는 컬렉터 클래스를 호출합니다. appendToLog 함수는 appendToLog 함수에 지정된 쿼리 문자열 매개 변수를 초기 요청에 추가합니다. 이렇게 하면 캡처되는 데이터의 이름 및 값에 해당하는 추가 쿼리 문자열 이름-값 쌍이 포함된 초기 요청의 URI가 됩니다. 예를 들어, 특정 광고 배치나 클릭스루 링크의 값이 20센트가 되면 CPC=20이 초기 요청에 추가됩니다. Insight Server는 이러한 값을 분석을 위해 데이터 세트에 처리합니다. 이 수집 방법의 한 가지 추가 이점은 페이지 태그 지정 방법을 사용하여 만들 수 있듯이 추가 로그 항목을 만들지 않고 추가 데이터를 수집할 수 있다는 것입니다.

처리에 대한 자세한 내용은 데이터 집합 구성 안내서를 참조하십시오.

**페이지에서 추가 데이터를 캡처하려면**

1. 데이터를 캡처할 .jsp 페이지의 맨 위에 다음 코드를 추가합니다.

   ```
   <%@ page import="com.visualsciences.collector.VSCollector" %>
   ```

1. collector 객체의 appendToLog() 메서드를 사용하여 원하는 이름-값 쌍을 요청된 .jsp 페이지의 쿼리 문자열에 추가합니다. 다음 예제에서는 /index.jsp 페이지에 대해 요청된 .jsp 페이지의 쿼리 문자열에 &quot;A=1&quot; 및 &quot;B=2&quot;를 추가합니다.

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

   결과 요청 URI는 /index.jsp?A=1&amp;B=2 입니다.

1. 추가 데이터를 캡처할 각 .jsp 페이지에 대해 이 절차를 반복합니다.
