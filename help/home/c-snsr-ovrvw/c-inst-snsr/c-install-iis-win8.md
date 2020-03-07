---
description: Microsoft Windows Server 2008 이상에서 실행 중인 Microsoft IIS 7.x 또는 8.x용 Sensor를 설치하고 구성합니다.
title: Windows Server 2008 이상 버전의 Microsoft IIS
uuid: 7fd8da68-1553-4395-b13e-b08a6ee1948e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Windows Server 2008 이상 버전의 Microsoft IIS{#microsoft-iis-on-windows-server-or-later}

Microsoft Windows Server 2008 이상에서 실행 중인 Microsoft IIS 7.x 또는 8.x용 Sensor를 설치하고 구성합니다.

센서용 프로그램 파일은 Adobe 다운로드 사이트에서 다운로드한 설치 파일로 패키지되어 있습니다. 특정 웹 서버에 대한 Sensor 설치 파일이 없는 경우 다음 절차를 시작하기 전에 해당 파일을 다운로드(또는 Adobe 담당자에게 제공)하십시오.

센서를 설치하고 구성하려면 다음 고급 단계를 수행해야 합니다.

1. [프로그램 파일 설치](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-cb51e5932a6d40c5b00758a7a51b7578)
1. [센서 구성 파일 편집](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-1e1590a92222430e92066292512ae0df)
1. [전송기를 시작하고 디스크 대기열을 만듭니다.](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-2b8dfd06996d4ab49998eeb99bd9f5f0)
1. [웹 서버에 컬렉터 추가](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-088960c986cf449cb712152298b3518d)
1. [추가 데이터 캡처](../../../home/c-snsr-ovrvw/c-inst-snsr/c-install-iis-win8.md#section-98db9625efdc4b60bfd76f7adf4af74d)

## 프로그램 파일 설치 {#section-cb51e5932a6d40c5b00758a7a51b7578}

Windows IIS에서 Sensor를 실행할 때 프로그램 파일과 디스크 큐 파일은 동일한 디렉토리에 있어야 합니다.

프로그램 파일을 설치하기 전에 먼저 디스크 대기열을 유지할 위치를 결정합니다. 이 위치는 프로그램 파일을 설치해야 하기 때문입니다.

다음 절차를 사용하여 센서용 프로그램 파일을 추출하고 설치합니다.

1. Windows 컴퓨터에서 Sensor 프로그램 파일을 설치할 디렉토리를 만듭니다. 디스크 대기열이 이 디렉토리에도 상주하므로 선택한 장치에 필요한 크기의 큐를 저장할 충분한 공간이 있는지 확인하십시오.

   예:C:\VisualSensor

1. 설치 파일의 내용을 방금 만든 디렉토리에 추출합니다. 이 단계 동안 Sensor는 다음 파일을 설치합니다.

<table id="table_C9E8803E51D046FD8FCCA38F8DAC04D1"> 
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
   <td colname="col1"> qlog.dll </td> 
   <td colname="col2"> 컬렉터 모듈(ISAPI 필터)입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TestExperiment.xls </td> 
   <td colname="col2"> <p>제어 실험을 구성하는 데 사용할 수 있는 Excel 스프레드시트 파일입니다. </p> <p>센서가 이 파일을 사용하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> trust_ca_cert.pem </td> 
   <td colname="col2"> 연결 프로세스 중에 Insight Server가 제공하는 디지털 인증서의 유효성을 확인하는 데 사용되는 인증서입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> TXLog.exe </td> 
   <td colname="col2"> 송신기 프로그램 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> txlogd.conf </td> 
   <td colname="col2"> 센서 구성 파일입니다. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>설치 패키지에는 TestExperiment.xls라는 스프레드시트 파일이 들어 있습니다. 이 스프레드시트는 설계자가 제어 실험을 구성하는 데 사용하는 도구입니다. 센서 자체에서 이 파일을 사용하지 않으므로 센서 실행 중인 시스템에 파일을 설치할 필요는 없습니다(선택할 수 있지만). 대신 파일을 설계자가 액세스할 수 있는 위치에 복사하거나 필요에 따라 설치 패키지에서 파일을 추출할 수 있습니다. 제어된 실험에 대한 자세한 내용은 인사이트 제어 실험 안내서를 참조하십시오.

## 센서 구성 파일 편집 {#section-1e1590a92222430e92066292512ae0df}

txlogd.conf 파일에는 센서의 구성 매개 변수가 포함되어 있습니다.

디스크 큐의 크기, Insight Server 주소, 그리고 이 센서가 생성하는 데이터에 연결될 ID를 지정하려면 파일을 편집해야 합니다. 구성 파일에는 필수 매개 변수와 선택적 매개 변수가 포함되어 있습니다.

* **필수 매개 변수는** Sensor를 설치할 때 지정해야 하는 설정입니다. 이러한 설정이 없으면 센서가 제대로 실행되지 않습니다.
* **선택적 매개 변수는** 기본적으로 사전 정의된 값(수정할 수 있음)으로 설정되거나 선택적 기능을 활성화하는 설정입니다.

**센서 구성 파일을 편집하려면**

1. 텍스트 편집기에서 파일을 열고 필요한 매개 변수와 원하는 선택적 매개 변수를 설정합니다. `<SensorDirectory>/txlogd.conf`

   매개 변수에 대한 [!DNL txlogd.conf] 설명은 Sensor Txlogd.conf [파일 매개 변수를 참조하십시오](../../../home/c-snsr-ovrvw/sensor-txlogd-params/sensor-txlogd-params.md#concept-4bb629f058894b4abc65a31eb02eebed).

1. 파일을 저장하고 닫습니다.

## 전송기를 시작하고 디스크 대기열을 만듭니다. {#section-2b8dfd06996d4ab49998eeb99bd9f5f0}

파일을 구성한 후 [!DNL txlogd.conf]전송기 프로그램을 시작하고 Windows 서비스로 등록하고 디스크 큐를 만들 수 있습니다.

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

   >[!NOTE]
   >
   >이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.

   1. [이벤트 뷰어] 창의 왼쪽 창에서 응용 프로그램 로그를 선택합니다.
   1. 오른쪽 창에서 소스 열에 &quot;Adobe&quot;가 있는 이벤트를 찾습니다.
   1. &quot;Adobe&quot;에서 오류가 발견되면 오류를 두 번 클릭하여 이벤트 속성 창을 표시합니다. 이 창은 오류에 대한 자세한 정보를 제공합니다.

1. 응용 프로그램 로그 검사를 마치면 이벤트 뷰어를 닫습니다.
1. 전송기가 Sensor 프로그램 파일을 설치한 디렉토리에 디스크 대기열(Diskq2008.log)을 생성했는지, 그리고 이 크기가 txlogd.conf 파일의 QueueSize 매개 변수에서 지정한 크기인지 확인합니다.

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

## 웹 서버에 컬렉터 추가 {#section-088960c986cf449cb712152298b3518d}

IIS 파섹

1. [시작] > [관리 도구] **> [IIS(인터넷 정보 서비스) 관리자]를 사용하여 IIS 관리자를 엽니다**.
1. 로컬 컴퓨터 **및 사이트** 노드를 **확장합니다** .
1. 웹 사이트를 선택하고 오른쪽 창에서 ISAPI 필터를 두 번 **클릭합니다**.
1. 작업 **창에서** 추가를 **클릭합니다**.

1. 필터 **이름** 필드에 필터의 표시 이름을 입력합니다. 제안된 필터 이름은 &quot;센서&quot;입니다.
1. 찾아보기를 **클릭하고**, qlog.dll 파일(센서가 설치된 디렉토리)을 선택한 다음 확인을 **클릭합니다**.

1. 확인을 **클릭하여** 필터를 추가합니다.

   필터를 추가하면 컬렉터가 즉시 작동하고 데이터를 수집할 준비가 됩니다.

트래픽 흐름 후 녹색 화살표가 컬렉터에 나타나지 않으면 다음 단계를 완료하십시오.

1. [시작] > [관리 도구] > [이벤트 뷰어]를 클릭하여 이벤트 뷰어에서 오류를 확인합니다.

   >[!NOTE]
   >
   >이 명령 시퀀스는 사용 중인 Windows 버전에 따라 달라질 수 있습니다.

1. [이벤트 뷰어] 창의 왼쪽 창에서 응용 프로그램 **로그를 선택합니다** .
1. 오른쪽 창에서 소스 열에 &quot;Adobe&quot;가 있는 이벤트를 **찾습니다** .
1. 오류가 발생하면 오류를 두 번 클릭하여 [이벤트 속성] **창을 표시합니다** .

## 추가 데이터 캡처 {#section-98db9625efdc4b60bfd76f7adf4af74d}

웹 페이지는 ASP(Active Server Pages) 프로그래밍 언어를 사용하여 구조화되어 있는 경우가 많습니다.

ASP는 IIS 내에서 실행되는 Microsoft 기술입니다. 브라우저가 ASP 파일을 요청하면 IIS가 요청을 ASP 엔진에 전달합니다. ASP 엔진은 ASP 파일을 순서대로 읽고 파일에서 스크립트를 실행합니다. 마지막으로 ASP 파일은 일반 HTML로 브라우저로 반환됩니다. ASP는 다른 유틸리티 외에도 HTML 양식에서 제출한 사용자 쿼리 또는 데이터의 응답이나 요청을 허용하는 RESPONSE 또는 REQUEST 개체를 제공합니다.

경우에 따라, 사용자 브라우저의 주소 표시줄에 표시되거나 HTML 코드 자체에 표시되는 양식에 입력된 값을 URL에 추가하지 않을 수 있습니다. 간단한 서버측 ASP 스크립트를 사용하면 사용자의 브라우저에서 사용할 수 있도록 하거나 HTML 파일에 포함하지 않고도 양식 필드 이름과 해당 값을 로그 파일에 추가할 수 있습니다. 웹 사이트 내의 특정 양식에 입력된 실제 양식 값을 캡처하려면, 양식 값을 로그 요청에 추가하기 위해 몇 줄의 코드를 추가해야 합니다.

양식의 처리 페이지 내에 다음 코드를 포함하여 입력된 양식 값을 요청 데이터에 추가합니다(외부 데이터베이스 또는 다른 위치에 양식 값을 쓰는 것 외에도).

```
var sName= Request.Form("Name"); 
var sCity= Request.Form("City"); 
var sState= Request.Form("State"); 
var sZip= Request.Form("Zip"); 
 
Response.AppendToLog("&v_1=" +  sName); 
Response.AppendToLog("&v_2=" +  sCity); 
Response.AppendToLog("&v_3=" +  sState); 
Response.AppendToLog("&v_4=" +  sZip);
```

이 프로세스에서는 양식 처리 페이지에 대한 요청 데이터에 정의된 대로 양식 값을 추가합니다. 로그 데이터 내에서 추가된 값은 아래 그림과 같이 양식 처리 페이지의 쿼리 문자열로 사용할 수 있습니다. 예를 들어, v_1, v_2, v_3 및 v_4는 이제 적절한 양식 필드에 입력된 데이터를 포함하는 쿼리 문자열이 됩니다. 이전 예제에 설명된 구문은 캡처할 추가 양식 필드 및 값에 대해 복제할 수 있습니다.

```
http://www.myserver.com/path/to/formprocessingpage.asp?v_1=John+Smith&v_2=Los+Angeles&v_3=California&v_4=90210
```

모든 양식 필드 및 값을 캡처하여 분석에 사용할 수 있게 하려면 다음 구문을 사용할 수 있습니다.

```
var formvalues = Response.Form; 
Response.AppendToLog(formvalues);
```

이 예에서는 해당 값과 함께 HTML 내에 있는 모든 양식 필드를 가져와 양식 처리 페이지의 로그 항목에 쿼리 문자열로 추가합니다. 여기에는 양식 내에 있는 숨김 필드가 포함됩니다.

로그 데이터는 다음 표에 자세히 나와 있습니다.

| 수집된 데이터 | 설명 | 예 |
|---|---|---|
| v_1 | NAME 쿼리 문자열과 연결된 값 | v_1=John Smith |
| v_2 | CITY 쿼리 문자열과 연결된 값 | v_2=로스앤젤레스 |
| v_3 | STATE 쿼리 문자열과 연결된 값 | v_3=California |
| v_4 | ZIP 쿼리 문자열과 연결된 값 | v_4=90210 |

<!-- <a id="section_55C623AC973246DC9EBECD48DA1EE0F7"></a> -->

