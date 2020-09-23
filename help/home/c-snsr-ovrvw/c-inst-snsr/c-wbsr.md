---
description: AIX 5.1 이상에서 실행되는 WebSphere 5.x용 Sensor 설치 및 구성에 대한 자세한 지침
solution: Analytics
title: AIX의 WebSphere
uuid: a5a3fd79-a7f0-4861-adca-8da3a185d0df
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '1645'
ht-degree: 0%

---


# AIX의 WebSphere{#websphere-on-aix}

AIX 5.1 이상에서 실행되는 WebSphere 5.x용 Sensor 설치 및 구성에 대한 자세한 지침

의 프로그램 파일 [!DNL Sensor] 은 Adobe 다운로드 사이트에서 가져오는 설치 파일로 패키지되어 있습니다. 특정 웹 서버에 대한 [!DNL Sensor] 설치 파일을 아직 가지고 있지 않은 경우 다음 절차를 시작하기 전에 해당 파일을 다운로드(또는 Adobe 담당자에게 제공)하십시오.

>[!NOTE]
>
>WebSphere 서버 [!DNL Sensor] 는 제어 실험을 지원하지 않습니다. 제어된 실험에 대한 자세한 내용은 *Data Workbench 제어 실험 안내서를 참조하십시오.*

## 프로그램 파일 설치 {#section-86f69127278c41bc90b97b68bb40bc6e}

서버 컴퓨터에 Sendorto용 프로그램 파일을 추출하고 설치하는 절차입니다.

1. 루트 사용자 또는 루트 권한이 있는 사용자로 로그온합니다.
1. 다음 명령을 사용하여 설치 파일의 압축을 풀고 압축을 해제합니다.

   ```
   gunzip installationFilename.tar.gz 
   tar -xf installationFilename.tar
   ```

1. 압축을 푼 프로그램 파일을 다음 표에 나와 있는 디렉토리에 복사합니다.

<table id="table_0E3B403071EF44AFBF0DD673EFEBBFE5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 파일 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> Target 디렉터리 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> libvisual_sciences.so </td> 
   <td colname="col2"> 수집기 로드 모듈 </td> 
   <td colname="col3"> /usr/local/visual_sciences </td> 
  </tr> 
  <tr> 
   <td colname="col1"> J2EECollector.jar </td> 
   <td colname="col2"> 수집기 로드 모듈 라이브러리 </td> 
   <td colname="col3"> WebSphere /lib 디렉토리 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> tlp </td> 
   <td colname="col2"> 송신기 프로그램 </td> 
   <td colname="col3"> <p>/usr/local/bin </p> <p>--또는-- </p> <p>/usr/local/sbin </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> Sensor 구성 파일 </td> 
   <td colname="col3"> /etc </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> 연결 프로세스 중에 Insight Server가 제공하는 디지털 인증서의 유효성을 검사하는 데 사용되는 인증서 </td> 
   <td colname="col3"> /usr/local/visual_sciences </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>설치 패키지에는 TestExperiment.xls라는 스프레드시트 파일이 들어 있습니다. 이 스프레드시트는 설계자가 제어 실험을 구성하는 데 사용하는 도구입니다. 센서 자체는 이 파일을 사용하지 않으므로 센서가 실행 중인 시스템에 파일을 설치할 필요는 없습니다(선택할 수 있지만). 대신 파일을 설계자가 액세스할 수 있는 위치에 복사하거나 필요한 경우 설치 패키지에서 파일을 추출하면 됩니다. 제어된 실험에 대한 자세한 내용은 인사이트 제어 실험 안내서를 참조하십시오.

**프로그램 파일에 대한 권한**

프로그램 파일에 대한 권한이 잘못되면 센서를 설치할 때 발생하는 대부분의 문제가 발생합니다.

이 섹션에 명시된 대로 권한을 정확하게 설정해야 합니다.

기본적으로 tar 파일의 프로그램 파일은 다음 권한을 갖습니다. 시스템 구성 방식에 따라 파일을 추출할 때 이러한 설정이 변경(마스크 해제)될 수 있습니다.

권한을 권장 기본 설정으로 재설정하려면 아래 chmod 명령을 사용하십시오.

>[!NOTE]
>
>파일을 설치한 디렉토리에 이 이상의 액세스 권한이 있는지 확인합니다.

| 파일 | 기본 권한 | chmod 명령 |
|---|---|---|
| libvisual_sciences.so | rwx —x —x | chmod 711 |
| J2EECollector.jar | rw- rw- r— | chmod 664 |
| tlp | rwx —x —x | chmod 711 |
| txlogd.conf | rw- rw- r— | chmod 664 |
| trust_ca_cert.pem | rw- rw- r— | chmod 664 |

권장 기본값 이외의 사용 권한을 사용하려면 Sensor UNIX 파일 사용 권한에 있는 정보를 검토하여 이러한 파일의 사용 방법을 이해해야 합니다.

## Edit the Sensor Configuration file {#section-283c8a92fa8841c1b6034e5f834ef4e7}

txlogd.conf 파일은 센서의 구성 매개 변수를 포함합니다.

디스크 큐 크기, Insight Server 주소, 이 센서에서 생성된 데이터에 연결될 ID 등을 지정하려면 파일을 편집해야 합니다.

구성 파일에는 필수 매개 변수와 선택적 매개 변수가 포함되어 있습니다.

* 필수 매개 변수는 센서를 설치할 때 지정해야 하는 설정입니다. 이러한 설정이 없으면 센서가 제대로 실행되지 않습니다.
* 선택적 매개 변수는 기본적으로 사전 정의된 값(수정할 수 있음)으로 설정되거나 선택적 기능을 활성화하는 설정입니다.

**구성 파일을 편집하려면**

1. 텍스트 편집기에서 /etc/txlogd.conf 파일을 열고 필요한 매개 변수와 원하는 선택적 매개 변수를 설정합니다.
1. 파일을 저장하고 닫습니다.

## 전송기 시작 및 디스크 큐 만들기 {#section-63285a2328604f20a2cb31b3d5cb80e6}

txlogd.conf 파일을 구성한 후 디스크 큐를 만드는 절차입니다.

1. 디스크 대기열에 있는 디렉토리가 없는 경우 해당 디렉토리를 생성합니다. 디렉토리에 파일에 대한 읽기/쓰기 액세스 권한이 있는 컬렉터 모듈과 송신기 프로그램이 모두 있는지 확인합니다.

1. 센서가 설치된 컴퓨터에서 다음 명령을 실행하여 송신기를 시작합니다.

   ```
   /usr/local/bin/txlogd -ic -f /etc/txlogd.conf
   ```

   * 이 명령의 &quot;i&quot; 옵션은 송신기를 대화형 모드로 시작합니다. 이 모드는 송신기 메시지를 화면에 표시하고 키보드 명령을 사용하여 송신기와 상호 작용할 수 있도록 해줍니다.
   * &quot;c&quot; 옵션은 전송기가 디스크 큐를 만들도록 합니다.
   * &quot;f&quot; 옵션은 구성 파일의 위치를 지정합니다.

1. 전송기가 QueueFile 매개 변수에 지정된 위치와 QueueSize 매개 변수에 지정된 크기의 디스크 큐를 만들었는지 확인합니다.
1. 대기열이 올바르게 생성되지 않은 경우 Ctrl+C를 입력하여 전송기를 종료한 다음 다음을 수행합니다.

   1. txtlogd.conf 파일을 검토하고 QueueFile 및 QueueSize 매개 변수가 올바르게 설정되었는지 확인합니다.
   1. 디스크 큐가 할당된 장치가 작동하고 QueueSize 매개 변수에 지정된 크기의 파일을 저장할 수 있는 충분한 공간이 있는지 확인합니다.
   1. 필요에 따라 수정하고 이 절차를 반복합니다.

## 웹 애플리케이션에 컬렉터 추가 {#section-d17297b1193f4e3cb150fb41f754ef12}

WebSphere 서버의 경우 컬렉터는 서블릿 컨테이너에서 필터로 작동합니다.

웹 응용 프로그램에 컬렉터를 추가하려면 웹 응용 프로그램의 web.xml 배포 설명자에 필터를 추가하고 웹 응용 프로그램을 다시 시작합니다.

1. 텍스트 편집기를 사용하여 Sensor가 캡처하는 이벤트가 있는 웹 서버의 web.xml 파일을 엽니다.
1. 다음 `<filter>` 및 `<filter-mapping>` 요소를 설명자 파일에 추가합니다. /etc 디렉토리에 txlogd.conf를 설치하지 않은 경우 요소에 이 파일의 올바른 경로를 입력해야 `<param-value>` 합니다.

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
   >이 선은 대소문자를 구분합니다. 위에 표시되는 그대로 입력합니다.

1. 웹 응용 프로그램을 다시 시작합니다. 수집기가 응용 프로그램과 함께 로드되고 이벤트 데이터를 수집하여 디스크 큐에 쓰기 시작합니다.

## 컬렉터 및 공유 객체 파일의 위치 선언 {#section-e641f08999d34a648aaee2111b69ca25}

Websphere 시작 스크립트를 편집하여 J2EEColector.jar 및 libvisual_sciences.so 파일의 위치를 선언하는 절차입니다.

1. Websphere /bin 디렉토리에서 setupCmdLine.sh 파일을 엽니다.
1. $WAS_CLASSPATH 변수를 정의하는 줄 뒤에 다음 줄을 추가합니다.

   ```
   WAS_CLASSPATH="$WAS_CLASSPATH":"$WAS_HOME"/lib/J2EECollector.jar
   ```

1. $WAS_LIBPATH 변수를 정의하는 대/소문자 블록 뒤에 다음 줄을 추가합니다.

   ```
   WAS_LIBPATH="$WAS_LIBPATH":/usr/local/visual_sciences
   ```

1. Save the [!DNL setupCmdLine.sh] file.

## 센서 테스트 {#section-07f2da5c4caa46bf9dd1cb4ae4b61af5}

전송기를 시작하고 성공적으로 Insight 서버에 연결하여 이벤트 데이터를 전송하는지 확인하는 절차입니다.

>[!NOTE]
>
>전송기가 이벤트 데이터를 Insight Server로 성공적으로 전송할 수 있는지 확인하려면 다음 테스트를 시작하기 전에 대상 Insight Server가 설치되어 실행 중인지 확인하십시오.

1. 전송기가 아직 실행되고 있지 않으면 다음 명령을 사용하여 다시 시작하십시오.

   ```
   /usr/local/bin/txlogd -i -f /etc/txlogd.conf 
   ```

1. 브라우저를 열고 센서가 실행 중인 웹 서버에서 페이지를 요청합니다(센서가 모니터링 중인 페이지를 선택하십시오).
1. 요청을 발행한 후 전송자의 콘솔에서 이벤트 데이터를 대상 Insight Server로 전송하고 있음을 나타내는 메시지를 확인합니다.
1. 센서가 데이터를 성공적으로 전송하지 않는 경우 다음을 확인하십시오.

   * 대상 Insight 서버가 실행 중입니다.
   * ServerAddress 및 ServerPort 매개 변수가 txtlogd.conf에서 올바르게 설정됩니다. 서버 이름을 사용하여 ServerAddress를 지정한 경우 숫자 IP 주소를 대신 사용하십시오.
   * CertName 매개 변수의 값은 대상 Insight Server의 디지털 인증서에 표시되는 일반 이름과 정확히 일치합니다.

## 시스템 시작 스크립트에 송신기 추가 {#section-23bb905100d04f018af93873dd4d5f68}

웹 서버 시스템을 다시 시작할 때 전송기가 자동으로 로드되도록 하는 정보입니다.

시스템 시작 스크립트에 다음 명령(전송기 실행)을 추가합니다.

```
/usr/local/bin/txlogd -f /etc/txlogd.conf
```

이 명령은 송신기를 데몬으로 시작합니다. 전송자가 생성하는 작동 및 오류 메시지는 syslog에 기록됩니다.

## 추가 데이터 캡처 {#section-d5ccf8ee50914a87938e0c17480757e6}

모든 플랫폼에 대한 센서는 HTTP 요청 및 응답 헤더에서 사용할 수 있는 모든 데이터를 수집할 수 있습니다.

J2EE 플랫폼용 센서는 다른 플랫폼에서 사용할 수 없는 데이터를 수집하는 메커니즘을 제공합니다. J2EE 플랫폼(J2EE 수집기)용 수집기는 응용 프로그램 레이어에 배치하여 응용 프로그램에서만 사용할 수 있고 페이지 태그 지정 또는 헤더를 통해 노출되어서는 안 되는 민감한 데이터를 수집할 수 있습니다.

>[!NOTE]
>
>페이지 태그 및 헤더 수정 기능은 데이터를 숨길 수 있지만, 페이지의 소스 코드를 검사하거나 브라우저 플러그인 도구를 사용하여 헤더를 보는 사람도 여전히 사용할 수 있습니다.

예를 들어 J2EE 수집기를 사용하여 페이지에 표시된 링크에 대한 CPC(클릭당 비용) 데이터, 페이지의 중요한 파트너 정보 및 기타 여러 데이터 포인트를 캡처할 수 있습니다. J2EE 환경을 사용하면 Adobe의 수집기 클래스를 사용하여 이 사용자 지정 데이터를 캡처하도록 WEBAPP을 쉽게 수정할 수 있습니다.

J2EE 플랫폼의 센서가 요청을 받으면 appendToLog 함수를 가져오는 컬렉터 클래스를 호출합니다. appendToLog 함수는 appendToLog 함수에 지정된 쿼리 문자열 매개 변수를 초기 요청에 추가합니다. 이렇게 하면 캡처되는 데이터의 이름 및 값에 해당하는 추가 쿼리 문자열 이름-값 쌍을 포함하는 초기 요청의 URI가 됩니다. 예를 들어 특정 광고 배치 또는 클릭스루 링크의 값이 20센트가 되면 CPC=20이 초기 요청에 추가됩니다. Insight Server는 분석을 위해 이러한 값을 데이터 세트에 처리합니다. 이 수집 방법론에 대한 또 다른 이점은 페이지 태그 지정 방법을 사용하여 만들 수 있는 추가 로그 항목을 만들지 않고도 추가 데이터를 수집할 수 있다는 것입니다.

처리에 대한 자세한 내용은 데이터 세트 *구성 안내서를 참조하십시오*.

1. 데이터를 캡처할 .jsp 페이지의 맨 위에 다음 코드를 추가합니다.

   ```
   <%@ page import="com.visualsciences.collector.VSCollector" %>
   ```

1. 컬렉터 객체의 appendToLog() 메서드를 사용하여 원하는 이름-값 쌍을 요청한 .jsp 페이지의 쿼리 문자열에 추가합니다. 다음 예는 /index.jsp 페이지에 대한 요청된 .jsp 페이지의 쿼리 문자열에 &quot;A=1&quot; 및 &quot;B=2&quot;를 추가합니다.

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

