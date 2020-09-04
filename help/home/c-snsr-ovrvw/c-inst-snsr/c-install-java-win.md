---
description: Windows Server 2000 이상에서 실행 중인 Sun Java System Application Server Standard Edition 7용 센서의 설치 및 구성에 대한 지침
title: Windows Server 2000 이상 버전의 Sun Java Server
uuid: 43f3eee0-2633-4bda-af6c-6c15433dd539
translation-type: tm+mt
source-git-commit: 8f5c69541bdd97aefbad3840f75f06846615f222
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 2%

---


# Windows Server 2000 이상 버전의 Sun Java Server{#sun-java-server-on-windows-server-or-later}

Windows Server 2000 이상에서 실행 중인 Sun Java System Application Server Standard Edition 7용 센서의 설치 및 구성에 대한 지침

센서용 프로그램 파일은 Adobe 다운로드 사이트에서 가져오는 설치 파일로 패키지되어 있습니다. 특정 웹 서버에 대한 Sensor 설치 파일이 없는 경우 다음 절차를 시작하기 전에 해당 파일을 다운로드(또는 Adobe 담당자에게 제공)하십시오.

Sensor는 RedHat Linux 7.x 이상 또는 Sun Solaris SPARC 2.6 이상에서 실행되는 다음 서버를 지원합니다.

센서를 설치하고 구성하려면 다음 단계를 수행해야 합니다.

## 프로그램 파일 설치 {#section-2f3e85083b4f4aa989a85997330e86ae}

센서용 프로그램 파일을 추출하고 서버에 설치하는 절차입니다.

1. Netscape Enterprise, iPlanet, Sun ONE 또는 Sun Java System Server에서 Sensor 프로그램 파일을 설치할 디렉토리를 만듭니다. 디스크 대기열이 이 디렉터리에 있으므로 선택한 장치에 필요한 크기의 큐를 저장할 충분한 공간이 있는지 확인하십시오.

   ```
   C:\VisualSensor
   ```

1. 방금 만든 디렉토리에 설치 파일의 내용을 추출합니다. 이 단계 동안 Sensor는 다음 파일을 설치합니다.

<table id="table_ABFF5F92271B4F3CB0AC68DAB6A5709F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 파일 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> Target 디렉터리 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> saf_visual_sciences.dll </td> 
   <td colname="col2"> 수집기 로드 모듈입니다. </td> 
   <td colname="col3"> <i>/usr/local/aolserver/ visual_sciences</i> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tlp </p> </td> 
   <td colname="col2"> 송신기 프로그램 </td> 
   <td colname="col3"> <p><i>/usr/local/bin</i> </p> <p><i>--또는--</i> </p> <p><i>/usr/local/sbin</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> Sensor 구성 파일입니다. </td> 
   <td colname="col3"> <i>/etc</i> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> 연결 프로세스 중에 Insight Server가 제공하는 디지털 인증서의 유효성을 검사하는 데 사용되는 인증서 </td> 
   <td colname="col3"> <i>/usr/local/visual_sciences</i> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>설치 패키지에는 TestExperiment.xls라는 스프레드시트 파일이 들어 있습니다. 이 스프레드시트는 설계자가 제어 실험을 구성하는 데 사용하는 도구입니다. 센서 자체에서 이 파일을 사용하지 않으므로 센서가 실행 중인 시스템에 파일을 설치할 필요는 없습니다(선택할 수 있지만). 대신 파일을 설계자가 액세스할 수 있는 위치에 복사하거나 필요한 경우 설치 패키지에서 파일을 추출하면 됩니다. 제어된 실험에 대한 자세한 내용은 인사이트 제어 실험 안내서를 참조하십시오.

## Edit the Sensor Configuration File {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

이 [!DNL txlogd.conf] 파일에는 센서의 구성 매개 변수가 포함되어 있습니다.

디스크 큐 파일의 크기와 위치, Insight Server 주소, 그리고 이 센서에서 생성된 이벤트 데이터에 연결될 ID를 지정하려면 이 파일을 편집해야 합니다.

구성 파일에는 필수 매개 변수와 선택적 매개 변수가 포함되어 있습니다.

* **필수 매개** 변수는 센서를 설치할 때 지정해야 하는 설정입니다. 이러한 설정이 없으면 센서가 제대로 실행되지 않습니다.
* **선택적 매개** 변수는 기본적으로 사전 정의된 값(수정할 수 있음)으로 설정되거나 선택적 기능을 사용하도록 설정하는 설정입니다.

**센서 구성 파일을 편집하려면**

* 텍스트 편집기에서 [!DNL /etc/txlogd.conf] 파일을 열고 필요한 매개 변수와 원하는 선택적 매개 변수를 설정합니다.
* 파일을 저장하고 닫습니다.

**센서 구성 파일을 편집하려면**

1. 텍스트 편집기에서 [!DNL /etc/txlogd.conf] 파일을 열고 필요한 매개 변수와 원하는 선택적 매개 변수를 설정합니다.
1. 파일을 저장하고 닫습니다.

## 전송기 시작 및 디스크 큐 만들기 {#section-55630de65f264274aefd771da2002852}

txlogd.conf 파일을 구성한 후 전송기 프로그램을 시작하고 Windows 서비스로 등록하고 디스크 대기열을 만들 수 있습니다.

1. Windows의 시작 메뉴에서 보조프로그램 > 명령 프롬프트를 선택합니다.
1. 명령 프롬프트 창에서 Sensor를 설치한 디렉토리로 이동하고 다음 명령을 실행합니다.

   ```
   txlog /regserver
   ```

   이 명령은 전송기를 시작하고 디스크 큐를 만들고 Sensor를 Windows 서비스로 등록합니다.

1. 전송기가 올바르게 실행되고 있는지 확인하려면 [시작] > [Campaign 컨트롤 패널] > [관리 도구] > [서비스]를 클릭합니다. 서비스 목록에서 센서의 항목을 찾아 상태가 시작이고 시작 유형이 자동인지 확인합니다. 그런 다음 서비스 제어판을 닫습니다.
1. 시작 중에 전송기에 오류가 있는지 확인하려면 [시작] > [Campaign 컨트롤 패널] > [관리 도구] > [이벤트 뷰어]를 클릭하여 이벤트 뷰어를 엽니다.

   1. [이벤트 뷰어] 창의 왼쪽 창에서 응용 프로그램 로그를 선택합니다.
   1. 오른쪽 창에서 [소스] 열에 &quot;Adobe&quot;이 있는 이벤트를 찾습니다.
   1. &quot;Adobe&quot;에서 오류가 발견되면 오류를 두 번 클릭하여 이벤트 속성 창을 표시합니다. 이 창은 오류에 대한 자세한 정보를 제공합니다.

1. 응용 프로그램 로그 검사를 마치면 이벤트 뷰어를 닫습니다.
1. 전송기가 Sensor 프로그램 파일을 설치한 디렉토리에 디스크 큐(Diskq2000.log)를 생성했으며, 이 크기가 txlogd.conf 파일의 QueueSize 매개 변수에서 지정한 크기인지 확인합니다.

   큐를 올바르게 만들지 않은 경우:

   1. txtlogd.conf 파일을 검토하고 QueueSize 매개 변수가 올바르게 설정되어 있는지 확인합니다.
   1. 센서를 설치한 장치에 QueueSize 매개 변수에 지정된 크기의 파일을 저장할 수 있는 충분한 공간이 있는지 확인합니다.
   1. Windows에서 서비스 제어판을 사용하여 전송기를 중지합니다.
   1. 큐 파일을 삭제합니다.
   1. Windows 서비스로 Sensor 재등록:Windows의 시작 메뉴에서 보조프로그램 > 명령 프롬프트를 선택합니다. 명령 프롬프트 창에서 Sensor를 설치한 디렉토리로 이동하고 다음 명령을 실행합니다.

      ```
      txlog /regserver
      ```

송신기는 계속 작동되도록 설계되었습니다. 시스템을 다시 시작하면 전송기가 자동으로 다시 시작됩니다. 전송기를 수동으로 시작 및 중지해야 하는 경우 Windows의 서비스 제어판을 사용하여 시작할 수 있습니다.

## 시작 스크립트 수정 {#section-19a38f27c9f44adf88f8910f5ed483a3}

init.conf 파일(예: C:\Sun\AppServer7\domains\domain1\server1\config\ init.conf)에서 파일 끝에 다음 줄을 추가합니다.

```
Init fn="load-modules" shlib="C:/VisualSciences/saf_visual_sciences.dll" 
funcs="vys-cookie,vys-log,vys-init,vys-content-type" 
Init fn="vys-init" config-file="C:/VisualSciences/txlogd.conf"
```

obj.conf 파일(예: C:\Sun\AppServer7\domains\domain1\server1\config\ server1-obj.conf)에서 다음 줄을 기존 `<Object name="default">` 줄 바로 아래에 추가합니다.

```
NameTrans fn="vys-cookie" 
ObjectType fn="vys-content-type" 
AddLog fn="vys-log"
```

