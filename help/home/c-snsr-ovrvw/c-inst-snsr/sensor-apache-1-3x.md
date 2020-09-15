---
description: RedHat Linux 7.x 이상, SUSE Linux 9.x 이상, Sun Solaris SPARC 2.6 이상, Sun Solaris x86 9 이상, FreeBSD 4 이상 또는 Mac OS X PowerPC에서 Apache Server 1.3.x에 대한 Sensor 설치 및 구성에 대한 자세한 지침
title: Linux, Sun Solaris, FreeBSD 또는 Mac OS X 기반의 Apache Server 1.3.x
uuid: bd46dd0f-fe36-4f8b-a87c-8ca7b64da609
translation-type: tm+mt
source-git-commit: 98452ba81d71db65c75e3d07712eefa18c003f53
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 2%

---


# Linux, Sun Solaris, FreeBSD 또는 Mac OS X 기반의 Apache Server 1.3.x{#apache-server-x-on-linux-sun-solaris-freebsd-or-mac-os-x}

RedHat Linux 7.x 이상, SUSE Linux 9.x 이상, Sun Solaris SPARC 2.6 이상, Sun Solaris x86 9 이상, FreeBSD 4 이상 또는 Mac OS X PowerPC에서 Apache Server 1.3.x에 대한 Sensor 설치 및 구성에 대한 자세한 지침

센서용 프로그램 파일은 Adobe 다운로드 사이트에서 가져오는 설치 파일로 패키지되어 있습니다. 특정 웹 서버에 대한 Sensor 설치 파일이 없는 경우 다음 절차를 시작하기 전에 해당 파일을 다운로드(또는 Adobe 담당자에게 제공)하십시오.

센서를 설치하고 구성하려면 다음 고급 단계를 수행해야 합니다.

## 프로그램 파일 설치 {#section-aae323e252394212bf4096d65fdd280c}

센서용 프로그램 파일을 서버 시스템에 추출 및 설치하는 지침

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

<table id="table_A97CF630633C4543A742D96C302D1138"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 파일 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> Target 디렉터리 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> mod_visual_sciences.so </td> 
   <td colname="col2"> 수집기 로드 모듈 </td> 
   <td colname="col3"> apachePath/libexec </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tlp </p> </td> 
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

기본적으로 tar 파일의 프로그램 파일은 다음 권한을 갖습니다. 시스템 구성 방식에 따라 파일을 추출할 때 이러한 설정이 변경(마스크 해제)될 수 있습니다. 권한을 권장 기본 설정으로 재설정하려면 아래 chmod 명령을 사용하십시오. 파일을 설치한 디렉토리에 이 이상의 액세스 권한이 있는지 확인합니다.

| 파일 | 기본 권한 | chmod 명령 |
|---|---|---|
| mod_visual_sciences.so | rwx r-x r-x | chmod 755 |
| tlp | rwx —x —x | chmod 711 |
| txlogd.conf | rw- rw- r— | chmod 664 |
| trust_ca_cert.pem | rw- rw- r— | chmod 664 |

## Edit the Sensor configuration file {#section-3f22a1c91d7d43b6b4c30f1b7448b17f}

이 [!DNL txlogd.conf] 파일에는 센서의 구성 매개 변수가 포함되어 있습니다.

디스크 큐 크기, Insight Server 주소, 이 센서에서 생성된 데이터에 연결될 ID 등을 지정하려면 파일을 편집해야 합니다.

구성 파일에는 필수 매개 변수와 선택적 매개 변수가 포함되어 있습니다.

* 필수 매개 변수는 센서를 설치할 때 지정해야 하는 설정입니다. 이러한 설정이 없으면 센서가 제대로 실행되지 않습니다.
* 선택적 매개 변수는 기본적으로 사전 정의된 값(수정할 수 있음)으로 설정되거나 선택적 기능을 활성화하는 설정입니다.

센서 구성 파일을 편집하려면

1. 텍스트 편집기에서 /etc/txlogd.conf 파일을 열고 필요한 매개 변수와 원하는 선택적 매개 변수를 설정합니다.
1. 파일을 저장하고 닫습니다.

## 전송기 시작 및 디스크 큐 만들기 {#section-a453d912ec3d47aa8e40ccacf527119d}

txlogd.conf 파일을 구성한 후 디스크 대기열을 만드는 지침

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

## Collector를 웹 서버에 추가 {#section-a7fb6425956f4f518ae3a7db091b33d2}

Apache 서버의 경우 수집기는 웹 서버 프로세스로 로드하는 동적 공유 오브젝트입니다.

컬렉터를 웹 서버에 추가하려면 아래에 설명된 대로 httpd.conf 파일을 편집하고 웹 서버를 다시 시작해야 합니다.

센서가 서버 컴퓨터의 여러 웹 서버에 대한 데이터를 캡처하는 경우 각 웹 서버에 대해 다음 절차를 수행해야 합니다.

1. 텍스트 편집기를 사용하여 Sensor가 캡처하는 이벤트가 있는 웹 서버의 [!DNL httpd.conf] 파일을 엽니다.
1. 파일 끝에 다음 줄을 추가합니다.

   ```
   LoadModule  visual_sciences_module  libexec/mod_visual_sciences.so 
   VisualSciencesConfig  /etc/txlogd.conf 
   AddModule mod_visual_sciences.c
   ```

   >[!NOTE]
   >
   >이 선은 대소문자를 구분합니다. 위에 표시되는 그대로 입력합니다.

1. 웹 서버를 다시 시작합니다. 수집기가 웹 서버와 함께 로드되고 이벤트 데이터를 수집하여 디스크 큐에 쓰기 시작합니다.

## 센서 테스트 {#section-83d9f60b39a6474f9c76bee3e19b2575}

전송기를 시작하고 성공적으로 Insight Server에 연결하고 이벤트 데이터를 전송하는지 확인합니다.

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
   * 매개 변수 [!DNL ServerAddress] 와 [!DNL ServerPort] 는 에서 올바르게 설정됩니다 [!DNL txtlogd.conf].

   * 서버 이름을 [!DNL ServerAddress] 사용하여 지정한 경우 숫자 IP 주소를 대신 사용하십시오. 매개 변수의 값은 [!DNL CertName] 대상 Insight Server의 디지털 인증서에 표시되는 일반 이름과 정확히 일치합니다.

## 시스템 시작 스크립트에 송신기 추가 {#section-4e1ffa6e043941ab91411d91d596477a}

웹 서버 시스템을 다시 시작할 때 전송기가 자동으로 로드되도록 하는 정보입니다.

시스템 시작 스크립트에 다음 명령(전송기 실행)을 추가합니다.

```
/usr/local/bin/txlogd -f /etc/txlogd.conf
```

이 명령은 송신기를 데몬으로 시작합니다. 전송자가 생성하는 작동 및 오류 메시지는 syslog에 기록됩니다.

>[!NOTE]
>
>일부 Solaris 사용자는 &quot;mutex를 가져올 수 없음&quot; 오류가 발생할 수 있습니다. 센서가 이러한 시스템에서 제대로 작동하려면 /etc/system 파일에 다음 줄을 추가하거나 편집해야 합니다.
>
>
```
>semsys:seminfo_semmnu=1024
>```
>
>기본 Solaris 설정은 60입니다. 각 인스턴스에 대해 3개의 세미아포를 사용하는 센서와 함께 수행된 테스트를 기반으로 Adobe은 사용자가 설정으로 1024를 사용하는 것을 권장합니다. 이 숫자는 센서가 세미아포어가 필요할 수 있지만 성능에 영향을 주지 않는 서버의 다른 응용 프로그램과 함께 작동할 수 있을 만큼 높습니다. 아드리안 콕크로프트는 저서 선퍼포먼스 및 튜닝(1994년 10월 플래스티스 홀)에서 다음과 같은 사항을 발표했다.&quot;데이터베이스는 많은 공유 메모리와 세마포 설정을 사용하는 경향이 있습니다. 성능에는 영향을 주지 않습니다.큰 만큼 프로그램을 실행할 것이라고 말했다.

