---
description: 버그 수정 및 알려진 문제 등 Data Workbench 6.0.4에 도입된 새로운 기능
title: Data Workbench 6.0 릴리스 정보
uuid: b348425e-3304-4db7-a280-479a34452bdb
exl-id: be69b3be-24e7-4a8c-9dc8-1360a9b6fb3a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1679'
ht-degree: 2%

---

# Data Workbench 6.0 릴리스 정보

버그 수정 및 알려진 문제 등 Data Workbench 6.0.4에 도입된 새로운 기능

## 새로운 기능 {#section-1225066ea8f44cf68e42e019d0bca816}

데이터 워크벤치(Insight 6.0)에는 추가된 보고 기능과 예측 분석 도구에 대한 이러한 새로운 기능과 시각화가 포함되어 있습니다.

| Data Workbench 기능 | 설명 |
|---|---|
| [단계 시각화](../../../home/c-get-started/c-analysis-vis/c-funnel-visualization/c-funnel-visualization.md#concept-79a0854325324bb9a60906cf79ef66da) | 단계 시각화 기능을 사용하면 고객의 순차적 프로세스 흐름을 정의할 수 있으며 프로세스의 각 단계에서 방문자의 폴아웃을 확인할 수 있습니다. |
| [방문자 클러스터링](../../../home/c-get-started/c-analysis-vis/c-visitor-cluster/c-visitor-cluster.md#concept-1c2406ef7b284a56a02daa38eaa2e73d) | 클러스터링을 사용하면 고객 특성을 활용하여 방문자를 동적으로 분류하고 고객 분석 및 타깃팅을 위해 선택한 데이터 입력을 기반으로 클러스터 세트를 생성할 수 있습니다. |
| [상관 관계 분석](../../../home/c-get-started/c-analysis-vis/c-correlation-analysis/c-correlation-analysis.md#concept-a7c8766b40be43aaa4084612689b630c) | 상관 관계 분석을 사용하면 연관성 있는 데이터 관계를 신속하게 식별하고 분석을 확장할 수 있습니다. |
| [업데이트된 DeviceAtlas 배포](../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-deviceatlas-update.md#concept-28b7bd5c0d854e73834261c431bed1e0) | 이제 DeviceAtlas JSON 파일이 DeviceAtlas.dll 및 DeviceAtlas64.dll과 함께 .bundle 파일(이름이 변경된 .tar.gz)로 배포됩니다. |

## 클라이언트 업그레이드 요구 사항 {#section-f316103b48374b6eac77e8feb5c47ecf}

데이터 워크벤치(Insight 6.0) 클라이언트 기능에 대해 다음 업그레이드 작업을 완료합니다.

**클라이언트에 대한 .zbin 파일 업데이트**

이제 데이터 워크벤치에서는 부동 텍스트 상자를 사용하여 키보드의 국제 문자를 입력할 수 있는 보조 텍스트 입력 프로세스로 IME(Input Method Editor)를 지원합니다. 데이터 워크벤치는 기본적으로 영어를 지원하지만 가상 중국어 키보드(IME 병음)와 같은 국제 언어를 지원하기 위해 다른 파일을 로드할 수도 있습니다.

버전 6.0으로 업데이트하기 전에 클라이언트 응용 프로그램에서 새 사전 파일(.zbin 파일)이 필요합니다. 소프트웨어 및 문서 프로필(Softdocs)에서 필요한 .zbin 파일을 가져올 수 있습니다.

전제 조건:

* Insight 6.0 클라이언트 및 보고서 서버 6.0으로 업그레이드하기 전에 Insight 관리자가 먼저 Insight Server 6.0으로 업그레이드해야 합니다.
* Insight 관리자는 언어(en-us.zbin, zh-cn.zbin)를 기반으로 zbin 파일을 선택하고, 언어 파일을 복사한 다음, insight.zbin으로 이름을 바꾸고, 실행 파일이 있는 보고서 서버의 루트 디렉토리에 이름이 변경된 파일을 저장해야 합니다. 그런 다음 Insight 보고서 서버를 다시 시작합니다.

추가 서버측 업그레이드 정보는 [서버 업그레이드 요구 사항](../../../home/c-release-notes-insight/release-notes.md)을 참조하십시오.

**클라이언트에 대한 zbin 파일을 업그레이드하려면(버전 5.x에서 6.0으로)**

1. 이 업그레이드 동안 클라이언트가 Insight Server에서 업데이트되지 않도록 하려면 Insight.cfg 인수를 false로 설정합니다.

   ```
   Update Software = bool: false
   ```

1. Insight 클라이언트를 다시 시작합니다.
1. 소프트웨어 및 문서 프로파일(SoftDocs 프로파일)로 이동하여 필요한 **[!UICONTROL Insight.zbin]** 파일을 다운로드합니다.[!DNL Software\Insight Client\v6.00\Insight_6.00.zip]

1. Insight.zbin 파일을 Insight.exe 파일과 동일한 폴더에 복사합니다.
1. 이제 Insight 클라이언트가 Insight Server에서 업데이트되도록 하려면 Insight.cfg 파일 인수를 true로 변경합니다.

   ```
   Update Software = bool: true
   ```

1. 클라이언트를 다시 시작합니다.

   클라이언트가 서버와 동기화되고 클라이언트가 다운로드 중이라는 메시지가 표시됩니다. 다운로드가 완료되면 Insight 클라이언트를 다시 시작할 것인지 묻는 메시지가 표시됩니다.
1. **확인**&#x200B;을 클릭하여 클라이언트를 다시 시작합니다.

   클라이언트가 버전 6.0을 시작하고 업그레이드합니다.

1. Insight.zbin 클라이언트 동기화를 적용하려면 클라이언트를 다시 시작합니다.

   다음 메시지가 표시되면 zbin이 Insight.exe 파일과 함께 올바른 폴더 위치에 배치되지 않은 것입니다.

   ```
   Insight Terminated: The backup dictionary file insight.zbin 
   is missing.
   ```

   문제를 해결하려면 Insight.exe를 삭제하고 최신 버전의 Insight.exe.old를 Insight.exe로 이름을 바꾼 다음 위의 1단계로 다시 시작하십시오.

## 서버 업그레이드 요구 사항 {#section-d6edba8b36234957ba8d06b555667a5a}

Insight 6.0 서버 기능에 대해 다음 업그레이드 작업을 완료하십시오.

**모든 Insight Server 6.0 패키지를 업데이트합니다**. Insight 6.0에는 새로운 예측 분석 프로필을 포함하여 업데이트해야 하는 서버 패키지가 포함되어 있습니다.

>[!IMPORTANT]
>
>Adobe에서는 사용자가 업데이트할 때 Insight Server 6.0의 새로 설치된 서버 클러스터를 업그레이드하는 것이 좋습니다.

또한 클라이언트는 Insight Server 6.0을 새로 설치하여 해당 서버 클러스터를 업그레이드하는 것이 좋습니다.

## 업그레이드 서버 클러스터

**언어 파일(.zbin 파일)을 준비합니다.** Insight 관리자는 필요한  `<language>.zbin` 언어(예:폴더에 있는 en-us.zbin , zh-cn.zbin) `/localization/<language>.zbin` 입니다. 그런 다음 관리자는 언어 파일을 복사하여 &quot;insight.zbin&quot;에 이름을 변경합니다.

언어 파일(.zbin)을 준비한 후 Insight 클라이언트와 보고서 서버를 모두 업데이트해야 합니다. Insight 클라이언트는 [클라이언트 업그레이드 프로세스](../../../home/c-release-notes-insight/release-notes.md) 중에 업데이트되지만 대부분의 경우 Insight 관리자는 보고서 서버를 업데이트합니다.

**언어 파일(.zbin 파일)로 보고서 서버를 업데이트합니다**.

모든 언어의 경우 보고서 서버 6.0에는 &quot;insight.zbin&quot; 파일이 보고서 서버 루트 폴더에 복사되어야 합니다.

보고서 서버 언어 파일을 업데이트합니다.

1. 이름이 변경된 &quot;insight.zbin&quot; 파일을 루트 ReportServer 디렉토리에 추가합니다.
1. 보고서 서버 구성 파일(reportserver.cfg)에는 더블바이트 언어에 대한 글꼴 설정이 필요합니다. 예를 들어 중국어 번체에 SimSun을 사용하는 글꼴이 추가되었습니다.

   ```
   Report Server.cfg - Add Fonts 
   
   Fonts = vector: 2 items 
     0 = string: SimSun 
     1 = string: Arial
   ```

1. 로컬라이제이션을 위해 보고서 서버 6.0에 대한 매개 변수를 명령줄에 전달해야 합니다. 예:

   ```
   ReportServer.exe -Locale -zh-cn 
   ReportServer.exe -Locale -en-us
   ```

   >[!NOTE]
   >
   >로케일이 지정되지 않은 경우 보고서 서버는 insight.zbin 파일에서 선택한 언어로 기본 설정됩니다.

   다음 단계에 따라 Locale 매개 변수를 사용하여 서비스로 ReportServer를 실행합니다.

   1. 관리자로 명령 프롬프트를 실행합니다.
   1. ReportServer 설치 폴더로 이동합니다.
   1. 서비스를 시작하려면 다음 명령을 입력합니다.

      * 영어:[!DNL ReportServer.exe -RegServer -Locale -en-us]
      * 중국어:[!DNL ReportServer.exe -RegServer -Locale -zh-cn]

1. ReportServer가 올바른 매개 변수로 실행되고 있는지 확인하려면:

   1. Windows 서비스 관리자를 엽니다.
   1. [!DNL Adobe Insight Report Server - Properties]을(를) 마우스 오른쪽 단추로 클릭합니다.

   실행 파일 경로에는 다음과 같은 매개 변수가 포함됩니다.

   ```
   ReportServer.exe -Service ReportServer -Locale -en-us
   ```

**예측 분석용 프로필 구성 파일을 수정합니다**. Insight 관리자는 Insight에서 사용할 수 있는 예측 분석 프로필을 포함하도록 사용자 지정 profile.cfg 파일을 수정해야 합니다.

profile.cfg 항목의 예:

```
Example ("profile.cfg"): 
Profile = profileInfo:  
  Active = bool: true 
  Directories = vector: 5 items 
    0 = string: Base\\  
    1 = string: Predictive Analytics\\ 
    2 = string: Geography\\ 
    3 = string: Adobe SC\\ 
    4 = string: Custom Profile\\ 
```

**PAServer.cfg 파일을 업데이트합니다**. Insight 서버에 Predictive Analytics 클러스터링 작업을 제출하려면 서버측 클러스터링 제출 처리를 위해 PAServer.cfg 파일을 구성해야 합니다.

사용자 지정 프로필은 예측 분석 프로필(Server\Profiles\Predictive Analytics\Dataset)에서 PAServer.cfg를 상속해야 합니다. 구현 사이트별로 PAServer.cfg를 구성하고 저장합니다.

>[!NOTE]
>
>PAServer.cfg가 구성되어 사용자 지정 프로필에 저장되면 사이트 전체에 Insight Server를 다시 시작해야 합니다.

**보고서 서버 업그레이드.** 보고서 서버의 글꼴과 시작 매개 변수를 업데이트해야 합니다.

전제 조건:

* 보고서 서버 6.0을 업그레이드하기 전에 Insight 관리자가 먼저 Insight Server 6.0으로 업그레이드해야 합니다.
* 모든 언어의 경우 보고서 서버 6.0에는 보고서 서버 루트 폴더에 Insight.zbin이 추가해야 합니다. `base/localization/<language>.zbin`이(가) 복사되고 &quot;insight.zbin&quot;으로 이름이 변경되었는지 확인합니다. 보고서 서버 디렉토리의 루트에 복사합니다.

글꼴 및 시작 매개 변수를 업데이트합니다.

1. 보고서 서버를 다른 언어로 출력하려면 더블바이트에 대한 글꼴 설정이 필요합니다.

   예를 들면 다음과 같습니다.

   보고서 서버.cfg - 글꼴 추가

   ```
   Fonts = vector: 2 items 
   0 = string: SimSun 
   1 = string: Arial
   ```

1. 보고서 서버 6.0의 매개 변수는 현지화를 위해 명령줄에 전달해야 합니다.

   로케일 매개 변수를 사용하여 서비스로 보고서 서버를 실행하려면:

   1. 보고서 서버 서비스를 중지합니다.
   1. 관리자로 명령 프롬프트를 실행합니다.
   1. 보고서 서버 설치 폴더로 이동합니다.
   1. 서비스를 시작하려면 다음 명령을 입력합니다.

      ```
      ReportServer.exe -RegServer -Locale -en-us
      ```

보고서 서버가 올바른 매개 변수로 실행되고 있는지 확인하려면:

1. Windows 서비스 관리자 열기
1. [!DNL Adobe Insight Report Server - Properties]을(를) 마우스 오른쪽 단추로 클릭합니다.
1. 실행 파일 경로에는 다음과 같은 매개 변수가 포함됩니다.

   ```
   ReportServer.exe -Service ReportServer -Locale -en-us
   ```

**Insight 6.0용 SiteCatalyst 데이터 피드를 업그레이드합니다**. Insight 6.0용 SiteCatalyst 데이터 피드의 파일 이름 형식이 변경되었습니다.

현재 파일 이름 형식:

```
 RSID_YYYYMMDD_HH0000.tsv.gz
```

새 파일 이름 형식:

```
YYYYMMDD-RSID_HH0000.tsv.gz
```

>[!NOTE]
>
>이 변경 사항은 SiteCatalyst 데이터 피드의 *wbench/ecom* 버전으로 현재 배포된 사용자에게 영향을 주지 않습니다.

파일 이름 형식 변경을 사용하면 로그 처리 중에 인사이트 시작 및 종료 시간 선언을 완전히 사용할 수 있습니다. 이렇게 하면 행 검색별로 행을 사용하여 모든 소스 파일을 필터링하지 않고 파일 내용을 읽어야 하는지 여부를 평가할 수 있습니다.

대부분의 경우 이 기능을 완전히 사용할 수 있도록 파일 수신 시 이름 변경 프로세스가 구현되었습니다. 이 수정 사항은 보조 프로세스의 필요성과 오버헤드 없이 기본적으로 필요한 명명 규칙을 제공합니다.

새 SiteCatalyst 데이터 피드를 사용하려면:

1. 수신 프로세스에서 새 파일 이름 형식을 처리하는 방법을 결정합니다.

   구현 중에 배포된 표준 이름 바꾸기/이동 스크립트는 확장명이 &quot;.gz&quot;인 파일을 이동하며 파일 이름이 이전 RSID와 일치하는 경우에만 이름 바꾸기를 수행합니다.

   새 파일 이름 형식:

   ```
    YYYYMMDD-RSID_HH0000.tsv.gz
   ```

1. 정의된 로그 소스 경로를 평가하여 모든 파일을 읽을 수 있는지 확인합니다.

   이름 변경 스크립트가 이미 구현된 경우 이미 이 새 파일 이름 형식을 읽도록 로그 소스를 정의하고 있습니다.

## 수정 사항 {#section-203f917dd6224114a1f801309c4c2cee}

* 이제 변경 내용을 저장하지 않고 작업 영역을 떠나는 키 조합이 **[!UICONTROL `<Ctrl>`+`<Backspace>`]**&#x200B;으로 업데이트되었습니다. 이전에는 `<Ctrl>` + `<Delete>`을(를) 눌러 변경 사항을 취소하고 작업 영역을 닫았습니다.

## Data Workbench 6.0.4 릴리스 정보{#data-workbench-release-notes}

버그 수정 및 알려진 문제 등 Data Workbench 6.0.4에 도입된 새로운 기능

이전 릴리스의 이전 기능과 수정 사항을 보려면 [릴리스 노트 아카이브](https://docs.adobe.com/content/help/ko-KR/data-workbench/using/release-notes/release-notes.html)를 참조하십시오.

## 새로운 기능 {#section-2-1225066ea8f44cf68e42e019d0bca816}

Data Workbench 6.0.4에는 보고 기능 및 예측 분석 도구에 대한 이러한 새로운 기능과 시각화가 포함되어 있습니다.

**성향 점수 시각화**. 데이터 워크벤치는 지정된 이벤트가 발생할 수 있는 예상 확률로 각 방문자의 점수를 계산합니다. 방문자 점수 시각화 기능을 사용하면 입력 변수를 기반으로 모든 관심 있는 방문자에 대해 지정된 이벤트가 발생할 확률을 제공하는 점수 차원을 만들 수 있습니다.

![](assets/visitor_scoring_visual.png)

이 기능에 대한 자세한 내용은 [성향 점수](../../../home/c-get-started/c-analysis-vis/c-visitor-propensity/c-visitor-propensity.md#concept-2958f4640dd44b9d86ad51c4f6165f40)를 참조하십시오.

## 업그레이드 요구 사항 {#section-08bd6fe3da8740fcb19688e8cac6f223}

**로그 소스 ID를 정의해야 합니다**. 버전 6.04부터 로그 소스 ID가 정의되지 않은 경우 다음 오류가 표시됩니다.

```
Missing Log Souce ID in log processing.cfg. Log Source ID must be  
defined for all log sources.
```

로그 소스당 행 기록이 Data Workbench 6.0에 추가되었으며 고유한 이름을 가진 로그 소스 ID를 추가하여 사용자 지정 프로필 로그 처리.cfg에서 정의할 수 있습니다. 빈 로그 소스 ID가 있는 경우 로그 소스 데이터의 불완전 읽기 및 기타 불일치와 같은 로그 처리 문제를 볼 수 있습니다.

```
Log Processing.cfg 
Log Sources = vector: 2 items 
  0 = VisualSensor: 
    Compressed = bool: false 
    Log Paths = vector: 1 items 
      0 = Path: \some path\ 
    Log Server = serverInfo:  
      Address = string:  
      Name = string:  
      Port = int: 80 
      Proxy Address = string:  
      Proxy Password = string:  
      Proxy Port = int: 8080 
      Proxy User Name = string:  
      SSL Client Certificate = string: Certificates\\server_cert.pem 
      SSL Server Common Name = string:  
      Use SSL = bool: false 
     
Log Source ID = string: <Name your ID Here>
    Name = string:  
    Recursive = bool: false
```

**FSU 리소스 위임 기능**

이제 [!DNL Profiles/`<profilename>`/dataset/Cluster.cfg]에서 표준화 및 소스 목록 서버에 대해 별도의 FSU(File Server Units)를 지정할 수 있습니다. 이러한 서비스는 더 이상 FSU에 연결되지 기본 않습니다.

>[!NOTE]
>
>목록 서버를 지정하지 않으면 목록 서버가 표준화 서버의 구성 설정을 상속합니다.

[!DNL cluster.cfg] 파일의 예.

```
Cluster = ClusterConfig: 
  Normalize Server = serverInfo: 
    Address = string: normalizeserver.domain.com 
    Port = int: 80 
    Use SSL = bool: false 
  List Server = serverInfo: 
    Address = string: sourcelistserver.domain.com 
    Port = int: 80 
    Use SSL = bool: false
```

## 수정된 버그 {#section-3b4b85a35f534288adf8a5246ef028cc}

* Data Workbench 6.0에서 상관 관계 매트릭스 및 클러스터 빌더는 백그라운드에서 계산 기능을 지원하지 않았습니다. 이제 버전 6.0.4에서 이 문제가 수정되었습니다.
* 이전에는 단계를 선택하고 단계를 제거한 경우 액세스 위반이 발생할 수 있습니다. 이 문제가 해결되었습니다.
* 무거운 로드 조건에서 문제를 일으킬 수 있는 세그먼트 내보내기의 잠재적 잠금 조건을 수정했습니다.
