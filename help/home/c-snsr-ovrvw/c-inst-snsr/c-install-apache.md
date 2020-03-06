---
description: Linux, Sun Solaris 또는 FreeBSD에서 Apache Server 2.0.40, 2.0.42 이상, Apache Server 2.2 또는 Apache Server 2.4를 설치 및 구성하는 방법에 대한 지침
title: Linux, Solaris 또는 FreeBSD의 Apache Server 2.0.40, 2.0.42 이상 및 Apache Server 2.2 또는 2.4
uuid: 3703e2c1-5b8d-4def-b146-49e59d78a669
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Linux, Solaris 또는 FreeBSD의 Apache Server 2.0.40, 2.0.42 이상 및 Apache Server 2.2 또는 2.4{#apache-server-or-later-and-apache-server-or-on-linux-solaris-or-freebsd}

Linux, Sun Solaris 또는 FreeBSD에서 Apache Server 2.0.40, 2.0.42 이상, Apache Server 2.2 또는 Apache Server 2.4를 설치 및 구성하는 방법에 대한 지침

센서용 프로그램 파일은 Adobe 다운로드 사이트에서 다운로드한 설치 파일로 패키지되어 있습니다. 특정 웹 서버에 대한 Sensor 설치 파일이 없는 경우 다음 절차를 시작하기 전에 해당 파일을 다운로드(또는 Adobe 담당자에게 제공)하십시오.

센서를 설치하고 구성하려면 다음 고급 단계를 수행해야 합니다.

다음 Apache 서버가 지원됩니다.

* RedHat Linux 7.x 이상 또는 Sun Solaris SPARC 2.6 이상에서 실행되는 Apache Server 2.0.40
* Linux, Sun Solaris 또는 FreeBSD의 Apache Server 2.0.40, 2.0.42 이상, Apache Server 2.2 또는 Apache Server 2.4
* RedHat Linux 7.x 이상, Sun Solaris SPARC 2.6 이상, SUSE Linux 9.x 이상 또는 FreeBSD 5.3에서 실행되는 Apache Server 2.0.42 이상
* 64비트 버전의 RedHat Linux ES 4 및 ES 5에서 실행되는 Apache Server 2.0.42 이상
* RedHat Linux 7.x 이상 또는 Sun Solaris SPARC 2.6 이상에서 실행되는 Apache Server 2.2
* RedHat Linux 7.x 이상, Sun Solaris x86_64 또는 FreeBSD에서 실행되는 Apache Server 2.4

>[!NOTE]
>
>Apache Server 버전 2.0.40, 2.0.42 이상(32비트 및 64비트) 또는 2.2를 실행하는 웹 서버에 Sensors를 설치하는 지침은 동일하지만(다음 절차에 언급된 경우 제외) 각 버전에 대한 설치 파일은 다릅니다. 센서를 설치하기 전에 실행 중인 Apache Server 및 운영 체제 버전에 대한 올바른 설치 파일을 받았는지 확인하십시오.

## 프로그램 파일 설치 {#section-2f3e85083b4f4aa989a85997330e86ae}

센서용 프로그램 파일을 추출하고 설치하는 절차.

1. 루트 사용자 또는 루트 권한이 있는 사용자로 로그온합니다.
1. 다음 명령을 사용하여 설치 파일의 압축을 풀고 압축을 해제합니다.

   * Linux의 경우:

      ```
      tar -zxf installationFilename
      ```

      ```
      unzip -d installationFilename.tar.gz 
       tar -xf installationFilename.tar
      ```

   * Solaris의 경우:

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

## Sametime Server에서 로깅 사용 {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

Sametime Server에 로그온하는 데 사용하는 단계입니다.

1. Lotus Domino 관리자 클라이언트를 사용하여 Sametime을 실행 중인 Lotus Domino 서버에 연결합니다.
1. Lotus Domino 관리자에서 파일 탭을 클릭한 다음 Sametime 구성 - stconfig.nsf를 두 번 클릭하여 Sametime 구성 파일을 엽니다.
1. Sametime 구성 파일에서 커뮤니티 서비스 양식을 열고 양식의 아무 곳이나 두 번 클릭하여 편집 모드로 전환합니다.
1. 채팅 로깅 플래그를 &quot;strict&quot;로 설정하고 캡처 서비스 유형을 &quot;0x1000&quot;으로 설정합니다.
1. 커뮤니티 서비스 양식을 저장하고 닫은 다음 Sametime 구성 파일을 닫습니다.
1. Sametime 서버를 다시 시작합니다.

## 센서 구성 파일 편집 {#section-de0eb4a646394b61abb6cd5a2b706de0}

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

IBM HTTP 서버의 경우 수집기는 웹 서버 프로세스에 로드하는 동적 공유 객체입니다.

Collector를 웹 서버에 추가하려면 아래 설명된 대로 httpd.conf 파일을 편집하고 웹 서버를 다시 시작해야 합니다.

Sensor가 서버 컴퓨터에 있는 여러 웹 서버에 대한 데이터를 캡처하는 경우 각 웹 서버에 대해 다음 절차를 수행해야 합니다.

1. 텍스트 편집기를 사용하여 Sensor가 캡처하는 이벤트가 있는 웹 서버의 httpd.conf 파일을 엽니다.
1. 파일 끝에 다음 두 줄을 추가합니다.

   ```
   LoadModule visual_sciences_module modules/mod_visual_sciences.so 
   VisualSciencesConfig /etc/txlogd.conf
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

이 명령은 송신기를 데몬으로 시작합니다. 전송자가 생성하는 운영 및 오류 메시지는 syslog에 기록됩니다.
