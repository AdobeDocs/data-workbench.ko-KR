---
description: 로그 소스는 데이터 세트를 작성하는 데 사용할 데이터가 들어 있는 파일입니다.
title: 로그 소스
uuid: ea21c3d7-9188-4ba8-bacd-052d678bd799
exl-id: 36e0799b-197d-4c59-84ae-7a4350584ab1
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '3664'
ht-degree: 1%

---

# 로그 소스{#log-sources}

로그 소스는 데이터 세트를 작성하는 데 사용할 데이터가 들어 있는 파일입니다.

각 데이터 레코드는 트랜잭션 레코드 또는 이벤트의 단일 인스턴스를 나타내기 때문에 로그 소스에서 사용할 수 있는 데이터를 이벤트 데이터라고 합니다. 데이터 워크벤치 서버는 [!DNL Sensors]에 의해 수집되거나 다른 데이터 소스에서 추출된 데이터에서 파생된 로그 소스를 처리할 수 있습니다.

* **데이터 수집: [!DNL Sensors]:** HTTP 및 응용 프로그램 서버에서 [!DNL Sensors]로 수집된 데이터는 데이터를 압축률이 높은 로그( [!DNL .vsl]) 파일로 변환하는 데이터 워크벤치 서버로 전송됩니다. [센서 파일](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009)을 참조하십시오.

* **Insight Server에서 추출한 데이터: 데이터 워크벤치 서버** 는 플랫 파일, XML 파일 또는 ODBC 호환 데이터베이스에 포함된 이벤트 데이터를 읽고 해당 디코더를 사용하여 원하는 데이터 요소를 추출합니다. 이러한 이벤트 데이터는 메모리에 상주할 필요는 없지만 데이터가 포함된 레코드에는 추적 ID가 포함되어야 합니다. [로그 파일](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e), [XML 로그 소스](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887) 및 [ODBC 데이터 소스](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3)를 참조하십시오.

**로그 소스를 추가하려면**

1. 데이터 워크벤치에서 [!DNL Log Processing.cfg]을(를) 엽니다.
1. **[!UICONTROL Log Sources]**&#x200B;을 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Add New]**&#x200B;을 클릭합니다.

1. 다음 중 하나를 선택합니다.

   * **[!UICONTROL Sensor]**
   * **[!UICONTROL Log File]**
   * **[!UICONTROL XML Log Source]**
   * **[!UICONTROL ODBC Data Source]**

1. 데이터 세트를 정의하는 데 사용되는 특정 매개 변수는 데이터 세트의 구성 프로세스에서 사용할 로그 소스 유형에 따라 달라집니다. 해당 로그 소스에 해당하는 섹션에 지정된 대로 매개 변수를 지정합니다.

   * [센서 파일](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-b25f11c477b54032a15b6117b3bf9009)
   * [로그 파일](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e)
   * [XML 로그 소스](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-c7b154e93748447b986e97f6ef688887)
   * [ODBC 데이터 소스](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3)

1. [!DNL Log Processing.cfg] 파일에서 로그 소스를 정의하고 다른 매개 변수를 변경한 후 파일을 로컬로 저장하고 데이터 워크벤치 서버의 데이터 세트 프로필에 저장합니다.

   >[!NOTE]
   >
   >데이터 워크벤치 서버 [!DNL File Server Unit]는 [!DNL Sensor] 파일, 로그 파일 및 XML 파일을 수신하여 저장하고 데이터 세트를 구성하는 데이터 워크벤치 서버의 [!DNL Data Processing Units]에 제공할 수 있습니다. [Insight 서버 파일 서버 단위 구성](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d)을 참조하십시오.

   [!DNL Transformation Dependency Map]에서 모든 로그 소스의 구성을 열 수 있습니다. [!DNL Transformation Dependency Map]에 대한 자세한 내용은 [데이터 집합 구성 도구](../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-tools.md#concept-6e058b7691834cf79dcfd1573f78d4f5)를 참조하십시오.

<!--
c_sensor_files.xml
-->

## 요구 사항 {#section-d5901a4872774ad5bd01a18db114f1f2}

HTTP 및 응용 프로그램 서버에서 [!DNL Sensors]에 의해 수집된 이벤트 데이터는 데이터를 압축률이 높은 로그( [!DNL .vsl]) 파일로 변환하는 데이터 워크벤치 서버로 전송됩니다. [!DNL .vsl] 파일 형식은 데이터 워크벤치 서버에서 관리되며 각 파일의 이름은 다음과 같습니다.

YYYYMMDD-*SENDSORID*.VSL

여기서 YYYYYMMDD는 파일 날짜이고 *SENDSORID*&#x200B;는 데이터를 수집하여 데이터 워크벤치 서버로 전송한 [!DNL Sensor]를 나타내는 이름(조직에서 할당함)입니다.

## 매개 변수 {#section-5c3f1e341c284486aeba3452057da7f3}

[!DNL Sensor] 파일의 경우 다음 매개 변수를 사용할 수 있습니다.

<table id="table_F583B475600041AFA3B9399AE0592146"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 로그 경로 </td> 
   <td colname="col2"> <p><span class="filepath"> .vsl</span> 파일이 저장되는 디렉토리입니다. 기본 위치는 로그 디렉토리입니다. 상대 경로는 데이터 워크벤치 서버의 설치 디렉토리를 나타냅니다. </p> <p>와일드카드 문자를 사용하여 처리할 <span class="filepath"> .vsl</span> 파일을 지정할 수 있습니다. 
     <ul id="ul_AE144ED0FAB94FE8B32599A058659DE1"> 
      <li id="li_1E4E4CFD72C34B5EB71A3C59877950A9"> * 개수에 관계없이 일치합니다. </li> 
      <li id="li_4664400FC12E44B39B28438B85D20ED8"> ? 단일 문자와 일치 </li> 
     </ul> </p> <p> 예를 들어 로그 경로 <span class="filepath"> Logs\*.vsl</span>은 <span class="filepath"> .vsl</span>으로 끝나는 Logs 디렉토리의 모든 파일을 일치시킵니다. 로그 경로 <span class="filepath"> Logs\*-SENSOR?.vsl</span>은 SENSOR1에서와 같이 로그 디렉토리의 파일(YYYYYMMDD)과 SENSOR 뒤의 단일 문자와 일치합니다. </p> <p> 지정된 경로의 모든 하위 디렉토리를 검색하려면 Recursive 매개 변수를 true로 설정해야 합니다. </p> <p> <p>참고:데이터 워크벤치 서버의 <span class="wintitle"> 파일 서버 단위</span>에서 파일을 읽으려면 로그 경로 매개 변수에 적절한 URI를 입력해야 합니다. 예를 들어 <span class="filepath"> URI /Logs/*-*.vsl</span>은 로그 디렉토리의 <span class="filepath"> .vsl</span> 파일과 일치합니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Insight 서버 파일 서버 단위 구성</a>을 참조하십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 서버 </td> 
   <td colname="col2">파일 서버에 연결하는 데 필요한 정보(주소, 이름, 포트 등) 로그 서버 매개 변수에 항목이 있으면 <span class="wintitle"> 로그 경로</span>는 URI로 해석됩니다. 그렇지 않으면 로컬 경로로 해석됩니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Insight 서버 파일 서버 단위 구성</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 소스 ID </td> 
   <td colname="col2"> <p>이 매개 변수의 값은 임의의 문자열일 수 있습니다. 값이 지정된 경우 이 매개 변수를 사용하여 소스 식별 또는 대상 처리를 위해 다른 로그 소스의 로그 항목을 구분할 수 있습니다. x-log-source-id 필드는 각 로그 항목의 로그 소스를 식별하는 값으로 채워집니다. 예를 들어 이름이 VSensor01인 <span class="wintitle"> Sensor</span> Sensor에서 로그 항목을 식별하려면 VSensor01</span>에서 <span class="filepath">를 입력하면 해당 소스의 모든 로그 항목에 대한 x-log-source-id 필드에 해당 문자열이 전달됩니다. </span></p> <p> x-log-source-id 필드에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> 이벤트 데이터 레코드 필드</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 재귀 </td> 
   <td colname="col2"> True 또는 False. true로 설정하면 <span class="wintitle"> 로그 경로</span>에 지정된 각 경로의 모든 하위 디렉토리가 지정된 파일 이름 또는 와일드카드 패턴과 일치하는 파일을 검색합니다. 기본값은 false입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시작/종료 시간 사용 </td> 
   <td colname="col2"> <p>True 또는 False. true로 설정되고 시작 시간 또는 종료 시간이 지정된 경우 이 로그 소스의 모든 파일에는 YYYYMMDD(ISO 형식 날짜)로 시작하는 파일 이름이 있어야 합니다. 각 파일에는 GMT일 1일의 데이터가 포함되어 있다고 가정합니다. 예를 들어 시간 범위는 1일에 0000 GMT로 시작하고 그 다음 날 000 GMT로 끝납니다. 로그 소스 파일에 GMT에 해당하지 않는 데이터가 포함되어 있는 경우 잘못된 결과를 방지하려면 이 매개 변수를 false로 설정해야 합니다. </p> <p> <p>참고:기본적으로 <span class="filepath"> Sensor</span>에서 수집한 데이터가 포함된 </span>파일은 위에서 설명한 이름 지정 및 시간 범위 요구 사항을 자동으로 충족합니다. <span class="wintitle"> 이 매개 변수를 true로 설정하면 데이터 워크벤치 서버는 항상 지정된 시작 시간과 종료 시간 사이에 있는 ISO 날짜가 포함된 파일의 데이터를 처리합니다. 이 매개 변수를 false로 설정하면 데이터 워크벤치 서버는 로그 처리 중에 모든 <span class="filepath"> .vsl</span> 파일을 읽어서 시작 시간 및 종료 시간 범위 내에 데이터가 포함된 파일을 결정합니다. </span></p> </p> <p> 시작 시간 및 종료 시간 매개 변수에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> 데이터 필터</a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>데이터 세트에 포함할 로그 파일 내의 로그 항목을 결정하려면 [!DNL Sensor] 데이터 소스에 대한 구성 매개 변수를 사용하지 마십시오. 대신 데이터 소스를 설정하여 디렉토리 내의 모든 로그 파일을 가리킵니다. 그런 다음 [!DNL Log Processing.cfg]의 시작 시간 및 종료 시간 매개 변수를 사용하여 데이터 세트 구성에 사용할 로그 항목을 결정합니다. [데이터 필터](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d)를 참조하십시오.

<!--
c_log_files.xml
-->

이벤트 데이터가 포함된 파일은 다음 요구 사항을 충족해야 합니다.

* 파일의 각 이벤트 데이터 레코드는 한 줄로 표시되어야 합니다.
* 레코드 내의 필드는 비워 두든 아니든 ASCII 구분 기호로 구분해야 합니다. 데이터 워크벤치 서버에서는 특정 구분 기호를 사용할 필요가 없습니다. 행 끝 문자가 아니며 이벤트 데이터 자체 내의 아무 위치에도 나타나지 않는 모든 문자를 사용할 수 있습니다.
* 파일의 각 레코드에는 다음이 포함되어야 합니다.

   * 추적 ID
   * 타임스탬프

* 데이터 처리에 대한 시작 및 종료 시간을 지정하려면 각 파일 이름은 형식이어야 합니다.

   * [!DNL YYYYMMDD-SOURCE.log]

   여기서 *YYYMMDD*&#x200B;은 파일의 모든 데이터의 그리니치 평균 시간(GMT)이고, *SOURCE*&#x200B;는 파일에 포함된 데이터의 소스를 식별하는 변수입니다.

   >[!NOTE]
   >
   >데이터 세트에 통합하려는 로그 파일을 검토하려면 Adobe 컨설팅 서비스에 문의하십시오.

## 매개 변수 {#section-83a861ac24954d54bbb9530e4d8bf23c}

로그 파일 로그 소스의 경우 다음 표의 매개 변수를 사용할 수 있습니다.

>[!NOTE]
>
>로그 파일 로그 소스를 처리하려면 [!DNL Log Processing Dataset Include] 파일에 정의된 추가 매개 변수가 필요합니다. 이 파일에는 [!DNL Log Processing.cfg] 파일에 포함된 매개 변수의 하위 집합과 로그 파일에서 데이터를 추출하기 위한 디코더를 정의하는 특수 매개 변수가 포함되어 있습니다. 로그 파일 로그 소스의 디코더 정의에 대한 자세한 내용은 [텍스트 파일 디코더 그룹](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd)을 참조하십시오.

<table id="table_F33735B5B90A48B0B21FA02D9198CCA9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> 로그 파일 소스의 식별자입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 경로 </td> 
   <td colname="col2"> <p>로그 파일이 저장되는 디렉토리입니다. 기본 위치는 로그 디렉토리입니다. 상대 경로는 데이터 워크벤치 서버의 설치 디렉토리를 나타냅니다. </p> <p> 와일드카드 문자를 사용하여 처리할 로그 파일을 지정할 수 있습니다. 
     <ul id="ul_1F02D26A08D846E2A3114E5C33F60ECF"> 
      <li id="li_ECAE1C03A1C448A1B86AE00B3A955708"> * 개수에 관계없이 일치합니다. </li> 
      <li id="li_24FDB500C5934CAAA4124C435DF4B290"> ? 단일 문자와 일치하는 항목을 찾습니다. </li> 
     </ul> </p> <p> 예를 들어 로그 경로 <span class="filepath"> Logs\*.log</span>는 <span class="filepath"> .log</span>로 끝나는 Logs 디렉토리의 모든 파일을 찾습니다. </p> <p> 지정된 경로의 모든 하위 디렉토리를 검색하려면 Recursive 매개 변수를 true로 설정해야 합니다. </p> <p> 데이터 워크벤치 서버의 <span class="wintitle"> 파일 서버 단위</span>에서 파일을 읽으려면 로그 경로 매개 변수에 적절한 URI를 입력해야 합니다. 예를 들어 <span class="filepath"> URI/Logs/*.log</span>는 Logs 디렉토리의 <span class="filepath"> .log</span> 파일과 일치합니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Insight 서버 파일 서버 단위 구성</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 서버 </td> 
   <td colname="col2"> 파일 서버에 연결하는 데 필요한 정보(주소, 이름, 포트 등) 로그 서버 매개 변수에 항목이 있으면 <span class="wintitle"> 로그 경로</span>는 URI로 해석됩니다. 그렇지 않으면 로컬 경로로 해석됩니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Insight 서버 파일 서버 단위 구성</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 압축 </td> 
   <td colname="col2"> True 또는 False. 데이터 워크벤치 서버에서 읽을 로그 파일이 압축 gzip 파일인 경우 이 값을 true로 설정해야 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 디코더 그룹 </td> 
   <td colname="col2"> 로그 파일 로그 소스에 적용할 텍스트 파일 디코더 그룹의 이름입니다. 이 이름은 <span class="wintitle"> 로그 처리 데이터 세트 포함</span> 파일에 지정된 해당 텍스트 파일 디코더 그룹의 이름과 정확히 일치해야 합니다. <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#concept-0db34988e17c41bfb1797f1d8e78aabd"> 텍스트 파일 디코더 그룹</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 소스 ID </td> 
   <td colname="col2"> <p>이 매개 변수의 값은 임의의 문자열일 수 있습니다. 값이 지정된 경우 이 매개 변수를 사용하여 소스 식별 또는 대상 처리를 위해 다른 로그 소스의 로그 항목을 구분할 수 있습니다. x-log-source-id 필드는 각 로그 항목의 로그 소스를 식별하는 값으로 채워집니다. 예를 들어 LogFile01이라는 로그 파일 소스에서 로그 항목을 식별하려면 LogFile01</span>에서 <span class="filepath">을 입력하면 해당 소스의 모든 로그 항목에 대한 x-log-source-id 필드에 해당 문자열이 전달됩니다. </span></p> <p> x-log-source-id 필드에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> 이벤트 데이터 레코드 필드</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 마스크 패턴 </td> 
   <td colname="col2"> <p>일련의 로그 파일의 소스를 식별하는 데 사용되는 일관된 이름을 추출하는 단일 캡처 하위 패턴이 있는 일반 표현식. 파일 이름만 고려됩니다. 경로 및 확장명은 정규 표현식 일치에 대해 고려하지 않습니다. <span class="wintitle"> 마스크 패턴</span>을 지정하지 않으면 마스크가 자동으로 생성됩니다. </p> <p> <span class="filepath"> 로그\010105server1.log</span> 및 <span class="filepath"> 로그\0105server2.log</span> 파일의 경우 <span class="wintitle"> 마스크 패턴</span>은 <code>[0-9]{6}(.*)</code>입니다. 이 패턴은 위의 파일 이름에서 "server1" 또는 "server2" 문자열을 추출합니다. </p> <p> <a href="../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c"> 정규 표현식</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 재귀 </td> 
   <td colname="col2"> True 또는 False. 이 매개 변수를 true로 설정하면 <span class="wintitle"> 로그 경로</span>에 지정된 각 경로의 모든 하위 디렉토리가 지정된 파일 이름 또는 와일드카드 패턴과 일치하는 파일을 검색합니다. 기본값은 false입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 파일 거부 </td> 
   <td colname="col2"> 디코더의 조건을 충족하지 않는 로그 항목이 포함된 파일의 경로와 파일 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시작/종료 시간 사용 </td> 
   <td colname="col2"> <p>True 또는 False. 이 매개 변수가 true로 설정되어 있고 시작 시간 또는 종료 시간이 지정된 경우 이 로그 소스의 모든 파일에는 YYYYYMMDD(ISO 형식)의 날짜로 시작하는 파일 이름이 있어야 합니다. 각 파일에는 GMT일 1일의 데이터가 포함되어 있다고 가정합니다. 예를 들어 시간 범위는 1일에 0000 GMT로 시작하고 그 다음 날 000 GMT로 끝납니다. 로그 소스 파일 이름이 ISO 날짜로 시작되지 않거나 파일에 GMT일에 해당하지 않는 데이터가 포함되어 있는 경우 잘못된 결과를 방지하려면 이 매개 변수를 false로 설정해야 합니다. </p> <p> <p>참고: 위에 설명된 이름 지정 및 시간 범위 요구 사항이 로그 파일에 대해 만족스러우며 이 매개 변수를 true로 설정하는 경우 지정된 텍스트 파일 디코더 그룹은 지정된 시작 시간과 종료 시간 사이에 있는 ISO 날짜가 있는 파일을 읽도록 제한합니다. 이 매개 변수를 false로 설정하면 데이터 워크벤치 서버는 로그 처리 중 모든 로그 파일을 읽고 시작 시간 및 종료 시간 범위 내에 데이터가 포함된 파일을 확인합니다. </p> </p> <p> 시작 시간 및 종료 시간 매개 변수에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> 데이터 필터</a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

이 예에서 데이터 세트는 두 가지 유형의 로그 소스에서 생성됩니다.

로그 소스 0은 [!DNL Sensor]에서 캡처한 이벤트 데이터에서 생성된 로그 파일을 지정합니다. 이 데이터 소스는 Logs라는 디렉터리와 [!DNL .vsl] 파일 이름 확장자를 가진 해당 디렉토리의 모든 파일을 가리킵니다.

로그 소스 1은 파일 이름 확장명이 [!DNL .txt]인 로그 디렉토리의 모든 파일을 가리킵니다. 이 로그 소스에 대한 디코더 그룹을 &quot;텍스트 로그&quot;라고 합니다.

![](assets/cfg_LogProcessing_LogSources.png)

데이터 세트에 대한 데이터 소스가 정의된 후에는 로그 파일을 삭제하거나 이동해서는 안 됩니다. 새로 만든 로그 파일만 데이터 소스의 디렉토리에 추가해야 합니다.

<!--
c_xml_log_sources.xml
-->

이벤트 데이터가 포함된 파일은 다음 요구 사항을 충족해야 합니다.

* 이벤트 데이터는 적절한 부모-자식 관계를 갖는 올바른 형식의 XML 파일에 포함되어야 합니다.
* 각 XML 파일 형식에 대해 고유한 디코더 그룹이 있어야 합니다. 디코더 그룹 구성에 대한 자세한 내용은 [XML 디코더 그룹](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3)을 참조하십시오.
* 파일의 각 방문자 레코드에는 다음이 포함되어야 합니다.

   * 추적 ID
   * 타임스탬프

* 데이터 처리에 대한 시작 및 종료 시간을 지정하려면 각 파일 이름은 형식이어야 합니다.

[!DNL YYYYMMDD-SOURCE.log]

여기서 *YYYMMDD*&#x200B;은 파일의 모든 데이터의 그리니치 평균 시간(GMT)이고, *SOURCE*&#x200B;는 파일에 포함된 데이터의 소스를 식별하는 변수입니다.

이러한 요구 사항을 충족하는 XML 파일의 예를 보려면 [XML 디코더 그룹](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3)을 참조하십시오.

>[!NOTE]
>
>데이터 세트에 통합하려는 XML 로그 파일을 검토하려면 Adobe 컨설팅 서비스에 문의하십시오.

## 매개 변수 {#section-d07b96d7f6ad4affb9cc0a0bc1b88c4d}

XML 로그 소스의 경우 다음 표의 매개 변수를 사용할 수 있습니다.

>[!NOTE]
>
>XML 로그 소스를 처리하려면 [!DNL Log Processing Dataset Include] 파일에 정의된 추가 매개 변수가 필요합니다. 이 파일에는 [!DNL Log Processing.cfg] 파일에 포함된 매개 변수의 하위 집합과 XML 파일에서 데이터를 추출하기 위한 디코더를 정의하는 특수 매개 변수가 포함되어 있습니다. XML 로그 소스에 대한 디코더 정의에 대한 자세한 내용은 [XML 디코더 그룹](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3)을 참조하십시오.

<table id="table_86B849F379CF4FEBA9294ACEF8F55184"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> XML 로그 소스의 식별자입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 경로 </td> 
   <td colname="col2"> <p>XML 로그 소스가 저장되는 디렉토리입니다. 기본 위치는 로그 디렉토리입니다. 상대 경로는 데이터 워크벤치 서버의 설치 디렉토리를 나타냅니다. </p> <p> 와일드카드 문자를 사용하여 처리할 XML 로그 소스를 지정할 수 있습니다. 
     <ul id="ul_0AE5D0ADE0F64CFAA856492A49239F58"> 
      <li id="li_4CBC0D1733F04258B3A55CC6FA714538 "> * 개수에 관계없이 일치합니다. </li> 
      <li id="li_81B597436A1241FF94E73C18A0ABBFA1"> ? 단일 문자와 일치 </li> 
     </ul> </p> <p>예를 들어 로그 경로 <span class="filepath"> Logs\*.xml</span>은 <span class="filepath"> .xml</span>으로 끝나는 Logs 디렉토리의 모든 파일을 일치시킵니다. </p> <p> 지정된 경로의 모든 하위 디렉토리를 검색하려면 <span class="wintitle"> 재귀</span> 필드를 true로 설정해야 합니다. </p> <p> <p>참고:데이터 워크벤치 서버의 <span class="wintitle"> 파일 서버 단위</span>에서 파일을 읽으려면 <span class="wintitle"> 로그 경로</span> 필드에 해당 URI를 입력해야 합니다. 예를 들어 <span class="filepath"> URI/Logs/*.xml</span>은 Logs 디렉토리의 <span class="filepath"> .xml</span> 파일과 일치합니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Insight 서버 파일 서버 단위 구성</a>을 참조하십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 서버 </td> 
   <td colname="col2"> 파일 서버에 연결하는 데 필요한 정보(주소, 이름, 포트 등) <span class="wintitle"> 로그 서버</span> 필드에 항목이 있으면 <span class="wintitle"> 로그 경로</span>은 URI로 해석됩니다. 그렇지 않으면 로컬 경로로 해석됩니다. <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md#concept-995abff3fce34e439fb3f7f47191c80d"> Insight 서버 파일 서버 단위 구성</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 압축 </td> 
   <td colname="col2"> True 또는 False. 데이터 워크벤치 서버에서 읽을 XML 로그 소스가 압축 gzip 파일인 경우 이 값을 true로 설정해야 합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 디코더 그룹 </td> 
   <td colname="col2"> XML 로그 소스에 적용할 XML 디코더 그룹의 이름입니다. 이 이름은 <span class="wintitle"> 로그 처리 데이터 세트 포함</span> 파일에 지정된 해당 XML 디코더 그룹의 이름과 정확히 일치해야 합니다. <a href="../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-xml-dec-grps.md#concept-5eda5ab253724674832f6951e2a0d1c3"> XML 디코더 그룹</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 로그 소스 ID </td> 
   <td colname="col2"> <p>이 필드의 값은 임의의 문자열일 수 있습니다. 값이 지정된 경우 이 필드를 사용하여 소스 식별 또는 대상 처리를 위해 다른 로그 소스의 로그 항목을 구분할 수 있습니다. x-log-source-id 필드는 각 로그 항목의 로그 소스를 식별하는 값으로 채워집니다. 예를 들어 XMLFile01이라는 로그 파일 소스에서 로그 항목을 식별하려면 XMLFile01</span>의 <span class="filepath">을 입력하면 해당 소스의 모든 로그 항목에 대한 x-log-source-id 필드에 해당 문자열이 전달됩니다. </span></p> <p> x-log-source-id 필드에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> 이벤트 데이터 레코드 필드</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 마스크 패턴 </td> 
   <td colname="col2"> <p>일련의 로그 파일의 소스를 식별하는 데 사용되는 일관된 이름을 추출하는 단일 캡처 하위 패턴이 있는 일반 표현식. 파일 이름만 고려됩니다. 경로 및 확장명은 정규 표현식 일치에 대해 고려하지 않습니다. <span class="wintitle"> 마스크 패턴</span>을 지정하지 않으면 마스크가 자동으로 생성됩니다. </p> <p> <span class="filepath"> 로그\010105server1.xml</span> 및 <span class="filepath"> 로그\010105server2.xml</span> 파일의 경우 마스크 패턴은 <code>[0-9]{6}(.*)</code>입니다. 이 패턴은 위의 파일 이름에서 "server1" 또는 "server2" 문자열을 추출합니다. </p> <p> <a href="../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c"> 정규 표현식</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 재귀 </td> 
   <td colname="col2"> True 또는 False. 이 매개 변수를 true로 설정하면 <span class="wintitle"> 로그 경로</span>에 지정된 각 경로의 모든 하위 디렉토리가 지정된 파일 이름 또는 와일드카드 패턴과 일치하는 파일을 검색합니다. 기본값은 false입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 파일 거부 </td> 
   <td colname="col2"> 디코더의 조건을 충족하지 않는 로그 항목이 포함된 파일의 경로와 파일 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시작/종료 시간 사용 </td> 
   <td colname="col2"> <p>True 또는 False. 이 매개 변수가 true로 설정되어 있고 시작 시간 또는 종료 시간이 지정된 경우 이 로그 소스의 모든 파일에는 YYYYYMMDD(ISO 형식)의 날짜로 시작하는 파일 이름이 있어야 합니다. 각 파일에는 GMT일 1일의 데이터가 포함되어 있다고 가정합니다. 예를 들어 시간 범위는 1일에 0000 GMT로 시작하고 그 다음 날 000 GMT로 끝납니다. 로그 소스 파일 이름이 ISO 날짜로 시작되지 않거나 파일에 GMT일에 해당하지 않는 데이터가 포함되어 있는 경우 잘못된 결과를 방지하려면 이 매개 변수를 false로 설정해야 합니다. </p> <p> <p>참고: 위에서 설명한 이름 지정 및 시간 범위 요구 사항이 XML 파일에 대해 만족하고 이 매개 변수를 true로 설정한 경우 지정된 XML 디코더 그룹은 이름을 지정한 시작 시간과 종료 시간 사이에 있는 ISO 날짜가 있는 파일로 읽히는 파일을 제한합니다. 이 매개 변수를 false로 설정하면 데이터 워크벤치 서버는 로그 처리 중 모든 XML 파일을 읽고 시작 시간 및 종료 시간 범위 내에 데이터가 포함된 파일을 확인합니다. </p> </p> <p> 시작 시간 및 종료 시간 매개 변수에 대한 자세한 내용은 <a href="../../../home/c-dataset-const-proc/c-log-proc-config-file/c-info-log-proc-param.md#concept-41bd49bf6b64442d91c232ec67529a3d"> 데이터 필터</a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>데이터 세트에 대한 데이터 소스가 정의된 후에는 XML 로그 소스를 삭제하거나 이동해서는 안됩니다. 새로 만든 XML 파일만 데이터 소스의 디렉토리에 추가해야 합니다.

<!--
AVRO-log-file.xml
-->

Avro 데이터 피드는 데이터를 Data Workbench에 통합하는 보다 효율적인 방법을 제공합니다.

<!-- <a id="section_45E3105B971C4220AE9CF573BEBF6080"></a> -->

* Avro는 트래픽 및 상거래 데이터에 대한 단일 소스 형식을 제공합니다.
* Avro 피드는 하루에 제공되는 여러 소스 청크의 압축 데이터입니다. 채워진 필드만 프로비저닝하고 모니터링 및 알림 기능, 내역 데이터에 대한 액세스 및 자동 복구를 제공합니다.
* Avro 로그 파일의 자체 정의 레이아웃인 스키마는 각 파일의 시작 부분에 포함됩니다.
* 디코더에 필요한 변경 사항 없이 Data Workbench 데이터를 인제스트하기 위해 지원 정보와 함께 새 필드가 추가됩니다. 다음과 같은 보고서가 포함됩니다.

   * Evar:1-250(이전 1-75)
   * 사용자 지정 이벤트:1-1000(1-100 대비)
   * 모바일, 소셜 및 비디오 데이터에 대한 솔루션 변수 액세스

>[!NOTE]
>
>또한 Avro 피드를 사용하면 종료 없이 피드의 모든 새 필드에 즉시 액세스할 수 있으므로 시간 요구 사항 없이 필드를 업데이트할 수 있습니다.

Avro 데이터 피드는 별도의 파일로 설정됩니다.

* **Avro 로그 파일**:이것은 트래픽 및 상거래 데이터의 형식을 지정하기 위해 디코더에서 생성된 Avro 로그 형식입니다.
* **Avro 디코더 파일**:이 파일을 사용하면 값을 새로운 Avro 형식으로 매핑할 수 있습니다. Avro 디코더 마법사를 사용하여 디코더를 설정할 수 있습니다.

## Avro 디코더 마법사 {#section-9a824b4c3d5549e7952a7111232035b2}

이 마법사는 Avro 디코더 로그 파일을 설정합니다.

열려면 작업 공간을 마우스 오른쪽 단추로 클릭하고 **관리** > **마법사** > **Avro 디코더 마법사**&#x200B;를 선택합니다.

**1단계:** **Avro 로그 파일을 선택합니다**.

이 단계에서 Avro 스키마의 소스 파일을 선택할 수 있습니다. 로그 파일(.log) 또는 기존 디코더 파일(.avro)에서 스키마에 액세스할 수 있습니다. 스키마는 두 파일에서 가져올 수 있습니다.

| **Avro 로그 파일 ** | 로그(.log) 파일을 클릭하여 로그 파일의 맨 위에서 스키마를 보고 디코더 파일을 생성합니다. |
|---|---|
| **Avro 디코더 파일** | 기존 디코더(.avro) 파일의 스키마를 열고 편집하려면 클릭합니다. |

**2단계:입력 필드를 선택합니다**.

로그 처리를 통과하기 위해 데이터 세트에서 사용할 입력 필드를 선택합니다. 파일의 모든 필드가 표시되므로 피드에 대한 필드를 선택할 수 있습니다.

>[!NOTE]
>
>데이터에 배열이 발견되면 [!DNL x-product(Generates row)] 필드가 제공됩니다. 이 필드는 배열의 중첩 데이터에 대한 새 행을 입력 필드로 생성합니다. 예를 들어 배열에 많은 제품 값이 있는 히트 행이 있는 경우 각 제품에 대한 입력 파일에 행이 생성됩니다.

| **기본값 선택** | 표준 기본 필드 세트로 식별할 필드를 선택합니다. |
|---|---|
| **모두 선택** | 파일의 모든 필드를 선택합니다. |
| **모두 선택 취소** | 파일의 모든 필드를 지웁니다. |

**3단계:행을 생성하기 위해 복사할 필드를 선택합니다.**

배열의 중첩 값으로 새 행을 만들 수 있으므로 새로 만든 모든 행에는 추적 ID와 타임스탬프가 있어야 합니다. 이 단계에서는 추적 ID 및 타임스탬프와 같이 상위 레코드의 행에 복사할 필드를 선택할 수 있습니다. 각 행에 추가할 다른 값을 선택할 수도 있습니다.

| **기본값 선택** | 추적 ID 및 타임스탬프와 같이 각 행에 새 열 값을 추가해야 하는 표준 기본 필드 세트를 선택합니다. 예를 들어 [!DNL hit_source] 필드는 각 새 행에 추가해야 하는 기본 값입니다(목록에 기본값으로 정의됨). 필요에 따라 각 행에 다른 열 값을 추가할 수 있습니다. |
|---|---|
| **모두 선택** | 파일의 모든 필드를 선택합니다. |
| **모두 선택 취소** | 파일의 모든 필드를 지웁니다. |

목록에서 값을 찾으려면 **검색** 상자를 사용합니다.

**4단계: 디코더 이름 지정**

필드 그룹의 이름을 지정하고 디코더 파일로 저장합니다. 이름은 로그 소스에 지정된 디코더 그룹 이름과 일치해야 합니다.

**5단계:디코더 파일을 저장합니다.**

파일 메뉴가 열려서 디코더 파일의 이름을 지정하고 **로그** 폴더에 [!DNL .cfg] 파일로 저장됩니다.
