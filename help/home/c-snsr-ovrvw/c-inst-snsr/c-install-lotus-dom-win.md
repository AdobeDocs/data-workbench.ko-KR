---
description: Microsoft Windows Server 2000 이상에서 실행 중인 Windows 3.1 이상용 Lotus Domino Server 6용 센서를 설치하고 구성하는 방법에 대한 지침입니다.
title: Windows Server 2000 이상에서 Lotus Domino Server
uuid: e3fb1478-92d1-4488-a4b8-244d258cc00a
exl-id: b736c8e6-0642-419c-8715-6586c21f2182
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 2%

---

# Windows Server 2000 이상에서 Lotus Domino Server{#lotus-domino-server-on-windows-server-or-later}

{{eol}}

Microsoft Windows Server 2000 이상에서 실행 중인 Windows 3.1 이상용 Lotus Domino Server 6용 센서를 설치하고 구성하는 방법에 대한 지침입니다.

센서용 프로그램 파일은 Adobe 다운로드 사이트에서 가져온 설치 파일에 패키지되어 있습니다. 특정 웹 서버에 대한 센서 설치 파일이 아직 없는 경우 다음 절차를 시작하기 전에 해당 파일을 다운로드(또는 Adobe 담당자로부터 획득)하십시오.

센서를 설치하고 구성하려면 다음 단계를 수행해야 합니다.

## 프로그램 파일 설치 {#section-2f3e85083b4f4aa989a85997330e86ae}

1. Lotus Domino 컴퓨터에서 센서 프로그램 파일을 설치할 디렉터리를 만듭니다. 디스크 큐도 이 디렉터리에 있으므로 선택한 장치에 필요한 크기의 큐를 저장할 충분한 공간이 있는지 확인하십시오.

   ```
   C:\VisualSensor
   ```

1. 설치 파일의 내용을 Lotus Domino 디렉터리에 추출합니다. 이 단계에서 Sensor는 다음 파일을 설치합니다.

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
   <td colname="col2"> 이벤트 뷰어 메시지 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> stchatlog.dll </td> 
   <td colname="col2"> 컬렉터 모듈 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>TestExperiment.xls </p> </td> 
   <td colname="col2"> <p>설계자가 제어 실험을 구성하는 데 사용할 수 있는 Excel 스프레드시트 파일입니다 </p> <p>센서에서 이 파일을 사용하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> 연결 프로세스 중에 Insight Server가 제공하는 디지털 인증서의 유효성을 검사하는 데 사용되는 인증서입니다 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TXLog.exe </td> 
   <td colname="col2"> 송신기 프로그램 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>txlogd.conf </p> </td> 
   <td colname="col2"> 센서 구성 파일 </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>설치 패키지에는 TestExperiment.xls라는 스프레드시트 파일이 들어 있습니다. 이 스프레드시트는 설계자가 통제 실험을 구성하는 데 사용하는 도구입니다. 센서 자체는 이 파일을 사용하지 않으므로 센서가 실행 중인 시스템에 파일을 설치할 필요는 없습니다(설치하도록 선택할 수 있지만). 대신 설계자가 액세스할 수 있는 위치에 파일을 복사하거나 필요에 따라 설치 패키지에서 파일을 추출할 수 있습니다. 통제 실험에 대한 자세한 내용은 Insight 통제 실험 안내서를 참조하십시오.

## Lotus Domino 서버 구성 {#section-2e2f1875a5304cdfa2cbcd0680683cfd}

Lotus Domino 서버를 구성하는 단계입니다.

1. Lotus Domino 관리자에 로그인하고 **[!UICONTROL Domain]**.

   ![](assets/dom_svr1.png)

1. Lotus Domino 관리자에서 **[!UICONTROL Configuration]**.

   ![](assets/dom_svr2.png)

1. 서버 노드를 확장하고 **[!UICONTROL Current Server Document]**.

   ![](assets/dom_svr3.png)

1. **[!UICONTROL Current Server Document]**&#x200B;를 클릭한 다음 **[!UICONTROL Internet Protocols]**&#x200B;을 클릭합니다.

   ![](assets/dom_svr4.png)

1. HTTP 탭의 DSAPI 섹션에서 단어 뒤에 두 번 클릭합니다 [!DNL ndolextn].

   ![](assets/dom_svr5.png)

1. 누르기 **[!UICONTROL Enter]** 및에 대한 경로를 입력합니다. [!DNL dominosensor.dll] 파일.

   ![](assets/dom_svr6.png)

1. 클릭 **[!UICONTROL Save & Close]**.

   ![](assets/dom_svr7.png)

## 센서 구성 파일 편집 {#section-de0eb4a646394b61abb6cd5a2b706de0}

txlogd.conf 파일에는 센서에 대한 구성 매개 변수가 포함되어 있습니다.

이 파일을 편집하여 디스크 큐 파일의 크기 및 위치, Insight Server 주소 및 이 센서에서 생성한 이벤트 데이터에 첨부할 ID를 지정해야 합니다.

구성 파일에는 필수 매개 변수와 선택적 매개 변수가 포함되어 있습니다.

* **필수 매개 변수** 은 센서를 설치할 때 지정해야 하는 설정입니다. 이 설정이 없으면 센서가 제대로 실행되지 않습니다.
* **선택적 매개 변수** 기본적으로 사전 정의된 값(수정할 수 있음)으로 설정되거나 선택적 기능을 활성화할 수 있습니다.

**센서 구성 파일을 편집하려면**

* 를 엽니다. `<Sensor directory>/txlogd.conf` 파일을 텍스트 편집기에 넣고 필요한 매개 변수와 원하는 선택적 매개 변수를 설정합니다.
* 파일을 저장하고 닫습니다.

## 전송기를 시작하고 디스크 큐 만들기 {#section-55630de65f264274aefd771da2002852}

txlogd.conf 파일을 구성한 후 전송 프로그램을 시작하고 Windows 서비스로 등록하고 디스크 큐를 만들 수 있습니다.

1. Windows의 시작 메뉴에서 **액세서리** > **명령 프롬프트**.

1. 명령 프롬프트 창에서 Sensor를 설치한 디렉토리로 이동하여 다음 명령을 실행합니다.

   ```
   txlog /regserver
   ```

   이 명령은 전송기를 시작하고 디스크 큐를 만들고 Sensor를 Windows 서비스로 등록합니다.

1. 전송기가 올바르게 실행 중인지 확인하려면 를 클릭합니다. **시작 > Campaign 컨트롤 패널 > 관리 도구 > 서비스**.

   >[!NOTE]
   >
   >이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.

   1. 서비스 목록에서 센서의 항목을 찾아 상태가 시작이고 시작 유형이 자동인지 확인합니다.
   1. 서비스 제어판을 닫습니다.

1. 시작 중에 전송기에 오류가 있는지 확인하려면 [시작] > [Campaign 컨트롤 패널] > [관리 도구] > [이벤트 뷰어]를 클릭하여 이벤트 뷰어를 엽니다.

   >[!NOTE]
   >
   >이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.

   1. 이벤트 뷰어 창의 왼쪽 창에서 응용 프로그램 로그를 선택합니다.
   1. 오른쪽 창에서 소스 열에서 &quot;Adobe&quot;이 있는 이벤트를 찾습니다.
   1. &quot;Adobe&quot;에서 오류가 발견되면 오류를 두 번 클릭하여 이벤트 속성 창을 표시합니다. 이 창에서는 오류에 대한 자세한 정보를 제공합니다.

1. 응용 프로그램 로그 검사를 마치면 이벤트 뷰어를 닫습니다.
1. 전송기가 디스크 큐( [!DNL Diskq2000.log])을 클릭하여 센서 프로그램 파일을 설치한 디렉토리에서 지정된 크기인지 확인합니다. [!DNL QueueSize] 의 매개 변수 [!DNL txlogd.conf] 파일.

   큐가 올바르게 생성되지 않은 경우:

   1. txtlogd.conf 파일을 검사하고 QueueSize 매개 변수가 올바르게 설정되어 있는지 확인하십시오.
   1. QueueSize 매개 변수에 지정된 크기의 파일을 저장할 수 있는 충분한 공간이 센서 설치 장치에 있는지 확인합니다.
   1. Windows에서 서비스 제어판을 사용하여 전송기를 중지합니다.
   1. 큐 파일을 삭제합니다.
   1. 센서를 Windows 서비스로 다시 등록: Windows의 시작 메뉴에서 액세서리 > 명령 프롬프트를 선택합니다. 명령 프롬프트 창에서 Sensor를 설치한 디렉토리로 이동하여 다음 명령을 실행합니다.

      ```
      txlog /regserver
      ```

      송신기는 연속적으로 실행되도록 설계되었습니다. 시스템을 다시 시작하면 전송기가 자동으로 다시 시작됩니다. 전송기를 수동으로 시작 및 중지해야 하는 경우 Windows에서 서비스 제어판을 사용하여 이 작업을 수행할 수 있습니다.
