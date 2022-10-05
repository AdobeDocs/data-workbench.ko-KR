---
description: Microsoft Windows Server 2000 이상에서 실행되는 Apache Server 1.3, Apache Server 2.0.42 이상 또는 Apache Server 2.2용 센서를 설치하고 구성하기 위한 지침
title: Windows Server 2000 이상 버전의 Apache Server 1.3, 2, 2.2 또는 2.4
uuid: e159ed83-6004-4f65-a3b7-502cac1d0862
exl-id: d1bd0fc1-da5b-4183-8270-73c46195f724
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 1%

---

# Windows Server 2000 이상 버전의 Apache Server 1.3, 2, 2.2 또는 2.4{#apache-server-or-on-windows-server-or-later}

{{eol}}

Microsoft Windows Server 2000 이상에서 실행되는 Apache Server 1.3, Apache Server 2.0.42 이상 또는 Apache Server 2.2용 센서를 설치하고 구성하기 위한 지침

센서용 프로그램 파일은 Adobe 다운로드 사이트에서 가져온 설치 파일에 패키지되어 있습니다. 특정 웹 서버에 대한 센서 설치 파일이 아직 없는 경우 다음 절차를 시작하기 전에 해당 파일을 다운로드(또는 Adobe 담당자로부터 획득)하십시오.

* Apache Server 1.3
* Apache Server 2.0.42 이상
* Microsoft Windows Server 2000 이상에서 실행되는 Apache Server 2.2

## 프로그램 파일 설치 {#section-2f3e85083b4f4aa989a85997330e86ae}

프로그램 파일을 설치하기 전에 디스크 큐를 유지할 위치를 결정해야 합니다. 디스크 큐도 프로그램 파일을 설치해야 하기 때문입니다.Sensor용 프로그램 파일을 추출하고 설치하려면 이 절차를 따르십시오.

센서를 설치하고 구성하려면 다음 단계를 수행해야 합니다.

1. Windows 시스템에서 센서 프로그램 파일을 설치할 디렉터리를 만듭니다. 디스크 큐도 이 디렉터리에 있으므로 선택한 장치에 필요한 크기의 큐를 저장할 충분한 공간이 있는지 확인하십시오.

   ```
   C:\VisualSensor
   ```

1. 설치 파일의 내용을 방금 만든 디렉토리에 추출합니다. 이 단계에서 Sensor는 다음 파일을 설치합니다.

<table id="table_ABFF5F92271B4F3CB0AC68DAB6A5709F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 파일 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> EventMessages.dll </td> 
   <td colname="col2"> 이벤트 뷰어 메시지. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> mod_visual_sciences.dll </td> 
   <td colname="col2"> 컬렉터 모듈입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>TestExperiment.xls </p> </td> 
   <td colname="col2"> <p>설계자가 제어 실험을 구성하는 데 사용할 수 있는 Excel 스프레드시트 파일입니다. 센서에서 이 파일을 사용하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> 연결 프로세스 중에 Insight Server가 표시하는 디지털 인증서의 유효성을 검사하는 데 사용되는 인증서입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TXLog.exe </td> 
   <td colname="col2"> 송신기 프로그램 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> 센서 구성 파일 </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>설치 패키지에는 TestExperiment.xls라는 스프레드시트 파일이 들어 있습니다. 이 스프레드시트는 설계자가 통제 실험을 구성하는 데 사용하는 도구입니다. 센서 자체는 이 파일을 사용하지 않으므로 센서가 실행 중인 시스템에 파일을 설치할 필요는 없습니다(설치하도록 선택할 수 있지만). 대신 설계자가 액세스할 수 있는 위치에 파일을 복사하거나 필요에 따라 설치 패키지에서 파일을 추출할 수 있습니다. 통제 실험에 대한 자세한 내용은 Insight 통제 실험 안내서를 참조하십시오.

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
1. 파일 끝에 다음 두 줄을 추가합니다.

   ```
   LoadModule visual_sciences_module modules/mod_visual_sciences.so 
   VisualSciencesConfig /etc/txlogd.conf
   ```

   >[!NOTE]
   >
   >이 줄은 대/소문자를 구분합니다. 위에 표시된 그대로 입력합니다.

1. 웹 서버 프로세스를 다시 시작합니다. 전체 서버 컴퓨터를 다시 부팅하지 않아도 됩니다. 웹 서버 프로세스를 다시 시작하면 됩니다. 수집기는 웹 서버와 함께 로드되어 이벤트 데이터를 수집하여 디스크 큐에 쓰기 시작합니다.
