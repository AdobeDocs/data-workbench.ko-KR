---
description: 센서 오류를 가능한 한 빨리 감지하여 주요 문제 또는 정전을 발생하기 전에 복구하려면 이벤트 로그를 정기적으로 모니터링해야 합니다.
title: 관리 이벤트 모니터링(센서)
uuid: c43d6509-6950-4436-8d6c-be7b00664f05
exl-id: 70894074-b8aa-4f6c-87d1-d0403f4c3319
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 0%

---

# 관리 이벤트 모니터링{#monitoring-administrative-events}

{{eol}}

센서 오류를 가능한 한 빨리 감지하여 주요 문제 또는 정전을 발생하기 전에 복구하려면 이벤트 로그를 정기적으로 모니터링해야 합니다.

**권장 빈도:** 적어도 시간별

Windows 이벤트 뷰어 또는 Unix Syslog 파일과 [!DNL *.sensor-log] 기본적으로 [!DNL Logs] 폴더 내 [!DNL Sensor] 설치 디렉토리. 이러한 파일은 데이터 수집 중에 특히 [!DNL Sensor] 대상에 연결할 수 없습니다. [!DNL data workbench server] 그리고 데이터 대기열을 시작합니다.

## Windows에서 이벤트 모니터링 {#section-7c0443a356af4381bf22259654f5cd17}

센서는 &quot;Adobe&quot; 소스로 Windows 이벤트 뷰어의 응용 프로그램 로그에 오류를 기록합니다.

메시지는 심각도에 따라 &quot;정보&quot;, &quot;경고&quot; 또는 &quot;오류&quot;로 기록됩니다.

**Windows 이벤트 뷰어를 열려면**:

* 클릭 **시작 > Campaign 컨트롤 패널 > 관리 도구 > 이벤트 뷰어**.

## Unix에서 이벤트 모니터링 {#section-5de3947891fb47ac88b7c855e545d54a}

센서가 오류를 [!DNL syslog] 데몬.

syslog 데몬은 syslog.conf 파일에 지정한 규칙에 따라 오류 메시지를 로그 파일에 기록합니다. 오류는 심각도에 따라 &quot;LOG_DAEMON&quot; 플래그와 &quot;LOG_NOTICE&quot; 또는 &quot;LOG_ERR&quot;로 기록됩니다.

**Unix syslog를 열려면**

Unix syslog는 일반적으로 [!DNL /var/adm/messages] 또는 [!DNL /var/log/messages].

해당 위치로 이동하여 syslog를 엽니다.

## 메시지 형식 이해 {#section-a0899add30fd4b2da58a23b9e3324693}

모든 센서 메시지에는 문자열 &quot;센서&quot;가 포함되며 표시되는 메시지의 중요도를 반영하도록 번호가 지정됩니다.

| 메시지 번호 | 메시지 의미 | 메시지 문자열 |
|---|---|---|
| 1xxx | 정보 | 센서 정보 번호 |
| 2xxx | 경고 | 센서 경고 번호 |
| 3xxx | 구성 오류 | 센서 오류 번호 |
| 4xxx | 운영 오류 | 센서 오류 번호 |
| 5xxx | 내부 오류 | 센서 오류 번호 |

>[!NOTE]
>
>경고(2xxx)가 현재 사용 중이 아닙니다. 이 번호는 나중에 사용하기 위해 예약되어 있습니다.

네트워크 관리 도구를 설정하여 5-10분마다 &quot;센서&quot; 소스를 사용한 오류에 대해 메시지를 모니터링하고 개입이 필요할 수 있는 문제에 대해 적절한 담당자에게 알릴 수 있습니다. &quot;센서 오류&quot; 문자열과 같은 특정 유형의 이벤트 메시지만 시스템을 모니터링하도록 선택할 수 있습니다. 또는 &quot;센서 정보&quot;, &quot;센서 경고&quot; 및 &quot;센서 오류&quot; 문자열이 앞에 있는 이벤트에 다른 규칙을 적용할 수 있습니다.

## 중요한 메시지 식별 {#section-5a20f5dc18ca4012931d194db855e54e}

이벤트 로그 내에서 큐 크기와 관련된 모든 메시지에 특별히 주의를 기울여야 하며 즉시 주소를 지정해야 합니다.

예를 들어 &quot; [!DNL Sensor Info 1012: Adobe disk queue is #% full]&quot;에 주의하십시오.

## 센서 이벤트 메시지에 응답 {#section-0004c4a169dc4a8882d9bd87dd326ad4}

지원되는 웹 서버 플랫폼에 대한 센서 이벤트 및 제안된 작업을 설명하는 테이블입니다.

**모든 플랫폼**

<table id="table_F8835AC0AD8F43E2B4494D8D35EBC0FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이벤트 메시지 </th> 
   <th colname="col2" class="entry"> 추천 작업 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 센서 정보 1010: 센서가 초기화되었습니다. </td> 
   <td colname="col2"> 필요한 작업이 없습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 정보 1011: 센서가 종료되었습니다. 대기 중인 총 클릭 수 ## </td> 
   <td colname="col2"> 필요한 작업이 없습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 정보 1012: Adobe 디스크 큐가 #% 가득 찼습니다. </td> 
   <td colname="col2"> 이 메시지는 디스크 큐 사용률이 10% 임계값을 넘을 때마다 기록됩니다. 이 비율이 계속 증가하는 경우 큐가 가득 차서 데이터가 손실되기 전에 작업을 수행해야 합니다. 가장 가능성 있는 문제는 센서가 Insight Server와의 통신을 중지했다는 것입니다. Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 정보 1013: 센서 구성이 변경되었습니다. </td> 
   <td colname="col2"> 필요한 작업이 없습니다. 센서가 구성 파일 중 하나에서 변경 내용을 감지하여 다시 로드합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 정보 1014: 난수 생성기의 시드 문제 </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 정보 1016: 구성 파일 이름이 로드됨 </td> 
   <td colname="col2"> 필요한 작업이 없습니다. 센서가 나열된 구성 파일을 로드했습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 정보 1017: 실험 파일 이름이 로드됨 </td> 
   <td colname="col2"> 필요한 작업이 없습니다. 센서가 나열된 실험 파일을 로드했습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 3016: 구성 파일 /mypath/myfile을 로드할 수 없습니다. </td> 
   <td colname="col2"> 웹 서버 구성에 지정된 센서 구성 파일이 있고 웹 서버 프로세스에서 읽어야 하는 권한이 있는지 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sensor 3017: 제어된 실험 구성 파일 /mypath/myfile을 로드할 수 없습니다. </p> </td> 
   <td colname="col2"> <p>txlogd.conf에 지정된 통제 실험 파일이 있고 txlogd 프로세스에 파일을 읽는 데 필요한 권한이 있는지 확인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 3018: 콘텐츠 필터 목록을 구문 분석할 수 없습니다. txlogd 구성 파일 확인 </td> 
   <td colname="col2"> txlogd.conf에서 ContentFilterInclude 및 ContentFilterExclude 항목의 구문을 확인합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 3023: 잠금(g_lockThrottle)을 만들지 못했습니다. </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 3024: 잠금(g_lockConfigCheck)을 만들지 못했습니다. </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 4014: 디스크 큐를 열 수 없습니다. </td> 
   <td colname="col2"> txlogd.conf에서 QueueFile 파일 이름을 확인하고 올바른 경우 Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 4020: 큐 파일이 아님 </td> 
   <td colname="col2"> txlogd.conf에서 QueueFile 파일 이름을 확인하고 올바른 경우 Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 4021: 큐가 꽉 찼습니다. </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 4022: 길이 메모리 블록을 매핑할 수 없습니다. &lt;x&gt; 오프셋 &lt;y&gt; </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 5012: 뮤텍스를 만들 수 없습니다. </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 5013: 뮤텍스를 가져올 수 없습니다. </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 5030: 포크 오류를 발생시킵니다. </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 5031: setsid가 실패했습니다. </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 5032: 포크 오류를 발생시킵니다. </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 5033: chdir에 실패했습니다. </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 5034: 신호 수신 </td> 
   <td colname="col2"> 외부 신호에 의해 프로그램이 종료되었을 수 있습니다. 이 신호의 소스를 확인할 수 없는 경우 Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 5035: 외부 주 밖에서 가 호출됨 </td> 
   <td colname="col2"> Adobe ClientCare에 문의하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 센서 오류 5036: txlogd가 이미 실행 중입니다. </td> 
   <td colname="col2"> txlogd 데몬의 다른 인스턴스가 이미 실행 중입니다. 새 인스턴스를 실행하려면 먼저 다른 인스턴스를 중지합니다. </td> 
  </tr> 
 </tbody> 
</table>

**Apache/IBM HTTP 서버**

| 이벤트 메시지 | 추천 작업 |
|---|---|
| 센서 오류 3015: VisualSciencesConfig 지시문이 httpd.conf에서 누락되었습니다. | 구성 오류입니다. VisualSciencesConfig 지시문은 txlogd.conf의 위치인 매개 변수와 함께 httpd.conf에 있어야 합니다. |
| 센서 오류 3019: vys-cookie가 vys-log 전에 호출되지 않았습니다. 지원 센터에 문의하십시오. | Adobe ClientCare에 문의하십시오. |
| 센서 오류 3025: 하위 요청은 자신을 다시 가리킵니다 | Adobe ClientCare에 문의하십시오. |

**AOL 서버**

| 이벤트 메시지 | 추천 작업 |
|---|---|
| 센서 오류 3015: ns/server/[server]/module/[모듈] 섹션이 AOLServer 구성 파일에 없습니다. | 구성 오류입니다. 오차에 명시된 대로 정확합니다. |
| 센서 오류 3019: vys-cookie가 vys-log 전에 호출되지 않았습니다. 지원 센터에 문의하십시오. Adobe ClientCare에 문의하십시오. | 지원 센터에 문의하십시오. Adobe ClientCare에 문의하십시오. |
| 센서 오류 3020: 의 첫 번째 항목으로 VisualSciencesConfig가 없습니다. [섹션] 섹션 을 참조하십시오. | 구성 오류입니다. 오차에 명시된 대로 정확합니다. |
| 센서 오류 3021: VisualSciencesConfig에 값이 없습니다. [섹션] 섹션 을 참조하십시오. | 구성 오류입니다. 오차에 명시된 대로 정확합니다. |

**iPlanet 및 Java System 웹 서버**

| 이벤트 메시지 | 추천 작업 |
|---|---|
| 센서 오류 3011: Init 지시문이 필요합니다. Init fn=vys-init config-file=&quot;/mypath/myfile&quot;과 같이 설정합니다. | 구성 오류입니다. iPlanet init 지시문이 누락되었습니다. |
| 센서 오류 3015: config-file이 iPlanet Init 지시문에 지정되지 않았습니다. | 구성 오류입니다. iPlanet Init 지시문에서 구성 파일의 경로를 제공하지 않았습니다. |
| 센서 오류 3019: vys-cookie가 vys-log 전에 호출되지 않았습니다. 구성 파일을 확인하십시오. | vys-cookie는 각 소프트웨어 가상 서버에 대한 첫 번째 NameTrans 지시어로 지정해야 합니다. |
