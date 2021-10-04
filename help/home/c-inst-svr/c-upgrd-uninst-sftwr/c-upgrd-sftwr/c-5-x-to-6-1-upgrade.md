---
description: 다음 단계에 따라 Insight v5.5x 설치에서 Data Workbench v6.1로 업데이트하십시오.
title: Data Workbench 5.5에서 6.1로 업그레이드
uuid: 14e3612e-11a2-402a-9478-904ec55df23c
exl-id: c730f6d5-2171-4d97-a967-509dc2517c86,3f25917b-b929-4e3b-84f0-1a81b30ba641
source-git-commit: b21da6d12175fa8570b1b366049baa9c8e8ea862
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 1%

---

# Data Workbench 5.5에서 6.1로 업그레이드{#data-workbench-to-upgrade}

다음 단계에 따라 Insight v5.5x 설치에서 Data Workbench v6.1로 업데이트하십시오.

**1단계**:  [서버 업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-08bd6fe3da8740fcb19688e8cac6f223)

**2단계**:  [보고서 서버 업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-afd9560a446242e9b06490e5f98aaaec)

**3단계**:  [클라이언트 업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-c896e57ecd2847afb18f4d8ef7cc0e06)

>[!IMPORTANT]
>
>서버, 보고서 서버 및 클라이언트 구성 요소가 64비트 Windows 운영 체제에서 실행되도록 업그레이드됩니다.

## 서버 업그레이드 {#section-08bd6fe3da8740fcb19688e8cac6f223}

다음 단계에 따라 **[!UICONTROL Server v6.1]** 구성 요소를 업데이트하십시오.

1. **[!UICONTROL Software and Docs]** 프로필을 사용하여 **[!UICONTROL Start Here]** 작업 공간을 열고 필요한 모든 서버 패키지를 로컬 폴더로 다운로드합니다.

   * **[!UICONTROL Server Packages]** \ **[!UICONTROL v6.1]** zip 폴더를 다운로드하고 모든 파일을 추출합니다.

      **[!UICONTROL Server]** 패키지에는 서버를 업데이트하기 위해 추가 및 바꿀 **[!UICONTROL Lookup]** 및 **[!UICONTROL Profile]** 조회 파일이 있습니다.**[!UICONTROL Base]****[!UICONTROL Transform]**

   * 새 **[!UICONTROL Profiles]** 폴더를 다운로드합니다.
   * 업데이트된 **[!UICONTROL Lookup]** 폴더를 다운로드합니다.
   * **[!UICONTROL Report Server]** \ **[!UICONTROL v6.1]** 패키지를 다운로드합니다.
   * 시스템에 필요한 추가 **[!UICONTROL Sensor]**, **[!UICONTROL Documentation]** 및 **[!UICONTROL Dashboard]** 파일을 다운로드하십시오.

1. **[!UICONTROL Adobe Insight Server]** 서비스를 중지합니다.

   ![](assets/install_server_download1.png)

1. 다운로드한 **[!UICONTROL Server]** 패키지에서 다음을 수행합니다.

   1. [!DNL Server\Bin] 폴더를 교체하여 [!DNL InsightServer64.exe] 및 지원 파일을 업데이트합니다.

   1. [!DNL Server\Profiles] 폴더를 바꿉니다. 모든 파일을 덮어쓸 수 있습니다.
   1. [!DNL Server\Lookups] 폴더를 업데이트합니다. 새로 다운로드한 파일을 폴더에 이미 있는 사용자 정의 파일에 추가할 수 있습니다.
   1. [!DNL Insight.exe] 및 [!DNL ReportServer.exe]를 업데이트하려면 [!DNL Server\Software] 폴더를 바꾸십시오

   1. [!DNL Server\Scripts] 폴더를 업데이트하여 [!DNL TnTSend.exe] 을 업데이트합니다.

1. **[!UICONTROL DeviceAtlas]**&#x200B;을 사용하는 경우 [!DNL Server\Lookups] 폴더에 있는 번들](/help/home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-deviceatlas-update.md)을 업데이트해야 합니다.[
1. [!DNL Profile.cfg] 파일에서 [!DNL Directories]을 설정하여 각 프로필에 대한 항목 수를 반영하도록 벡터가 업데이트되도록 합니다.

   예를 들어 **[!UICONTROL Predictive Analytics]** 프로필을 활성화하려면 이 설정을 업데이트해야 합니다.

   ```
   Directories = vector: 5 items
       0 = string: Base\\
       1 = string: Geography\\
       2 = string: Predictive Analytics\\
       3 = string: Adobe SC\\
       4 = string: Profile Name\\
   ```

1. Predictive Analytics 기능을 업그레이드하도록 [!DNL PAServer.cfg] 파일을 구성하고 저장합니다.

   Predictive Analytics 작업을 서버에 제출하려는 경우 서버측 클러스터링을 관리하도록 [!DNL Server > Predictive Analytics > Dataset > PAServer.cfg] 파일을 구성해야 합니다.

   사용자 지정 프로필은 Predictive Analytics 구성 프로필에서 설정을 상속해야 하므로 사이트의 구현에 따라 [!DNL PAServer.cfg] 을 구성하고 저장할 수 있습니다.

1. **[!UICONTROL Log Source ID]**&#x200B;을(를) 정의합니다.

   **[!UICONTROL Recording of Rows per Log Source]**&#x200B;이(가) **[!UICONTROL v6.04]**&#x200B;에 추가되고, 이름이 **[!UICONTROL Log Source ID]**&#x200B;인 고유하게 를 추가하여 사용자 지정 프로필의 [!DNL Log Processing.cfg] 파일에 정의됩니다.

   ```
   Log Processing.cfg
   Log Source ID = string: <Name your ID Here>
   ```

   로그 소스 ID가 정의되지 않은 경우 다음 오류가 표시됩니다.

   ```
   Missing Log Source ID in log processing.cfg.
   Log Source ID must be defined for all log sources.
   ```

1. [!DNL EventMessages.dll]이 업데이트되었으므로 등록을 취소한 다음 클러스터에 **[!UICONTROL Adobe Insight Server]**&#x200B;을 등록해야 합니다.

   * [!DNL InsightServer64.exe /unregserver]
   * [!DNL InsightServer64.exe /regserver]

1. 클러스터에서 **[!UICONTROL Adobe Insight Server]** 서비스를 시작합니다.

이제 서버 설치가 완료되었습니다.

## 보고서 서버 업그레이드 {#section-afd9560a446242e9b06490e5f98aaaec}

>[!IMPORTANT]
>
>**[!UICONTROL Report Server v6.1]**(으)로 업그레이드하기 전에 먼저 **[!UICONTROL Server v6.1]**(으)로 업그레이드해야 합니다.

1. **[!UICONTROL Software and Docs]** 프로필을 사용하여 **[!UICONTROL Report Server]** 패키지의 **[!UICONTROL v6.1]**&#x200B;을(를) 로컬 폴더로 다운로드합니다.
1. 다운로드한 패키지에서 **[!UICONTROL Report Server 6.1]** 을(를) 복사하고 프로필 패키지를 바꿉니다.

   >[!NOTE]
   >
   >[!DNL install] 폴더의 [!DNL Insight.zbin] 파일은 지역화에 사용되는 백업 파일이며 [!DNL install] 디렉터리에 있어야 합니다. 이 파일 또는 다른 [!DNL .zbin] 파일은 시작할 때 전달된 명령줄 설정에 따라 사용됩니다.

1. (선택 사항) 더블바이트 문자를 지원하도록 보고서 서버 구성 파일을 수정합니다.

   Data Workbench는 현재 영어(-en-us) 및 중국어(-zh-cn)를 지원합니다. 단일 및 2바이트 문자를 지원하려면 글꼴을 설정해야 합니다.

   ```
   Report Server.cfg - Add Fonts
      Fonts = vector: 2 items
      0 = string: SimSun
      1 = string: Arial
   ```

   Windows 운영 체제에는 나열된 글꼴도 설치되어 있어야 합니다.

1. 메시지에 대한 [!DNL Report Server v6.1].

   1. **[!UICONTROL Adobe Insight Report Server]** 서비스를 중지합니다.
   1. 명령 프롬프트를 &quot;관리자&quot;로 시작합니다.
   1. 보고서 서버 [!DNL install] 폴더로 이동합니다.
   1. 다음 명령을 사용하여 보고서 서버 서비스를 삭제합니다.

      ```
      ReportServer.exe /unregserver
      ```

1. 언어 설정에 따라 서비스를 시작합니다.

   ```
   ReportServer.exe -RegServer -Locale -en-us (English)
   ReportServer.exe -RegServer -Locale -zh-cn (Simplified Chinese)
   ```

1. 보고서 서버가 올바른 설정으로 실행 중인지 확인하려면 **[!UICONTROL Windows Service Manager]** 을 열고 **[!UICONTROL Adobe Insight Report Server - Properties]** 을 마우스 오른쪽 단추로 클릭합니다. 실행 파일의 경로에 업데이트된 명령줄 설정이 표시됩니다.

이제 보고서 서버 설치가 완료되었습니다.

## 클라이언트 업그레이드 {#section-c896e57ecd2847afb18f4d8ef7cc0e06}

>[!IMPORTANT]
>
>**[!UICONTROL Client v6.1]** 로 업그레이드하기 전에 먼저 관리자가 **[!UICONTROL Server v6.1.]** (으)로 업그레이드해야 합니다.

1. [!DNL Insight.exe]을(를) 시작하되 프로필에 연결하지 마십시오.
1. 소프트웨어를 자동으로 업데이트하지 않으려면 [!DNL Insight.cfg] 파일을 편집합니다.

   ```
   Update Software = bool: false
   ```

1. **[!UICONTROL Software and Docs]** 프로필(소프트 문서)에 연결합니다.
1. 다운로드 [!DNL Software\Insight Client\v6.10].
1. (선택 사항) 더블바이트 문자를 지원하려면 [!DNL insight.cfg]을 수정합니다.

   Data Workbench는 현재 영어 및 중국어 간체를 모두 지원합니다. 다음 언어를 모두 지원하려면 글꼴을 선택하십시오.

   ```
   Fonts = vector: 2 items
   0 = string: SimSun
   1 = string: Arial
   ```

1. 클라이언트를 종료합니다.
1. 다운로드한 **v6.1** 클라이언트 패키지의 파일을 [!DNL Install] 폴더에 복사합니다.

   >[!NOTE]
   >
   >설치 폴더의 [!DNL Insight.zbin] 파일은 지역화에 사용되는 백업 파일이며 설치 디렉터리에 있어야 합니다. 이 파일 또는 다른 [!DNL .zbin] 파일은 시작할 때 전달된 명령줄 설정에 따라 사용됩니다.
   >
   >예를 들어, 중국어 간체를 시작하려면 명령줄 설정에서 전달되는 단축키를 만듭니다.
   >
   >
   ```
   >Insight.exe -zh-cn
   >```
   >
   >영어(기본값)로 시작하려면 명령줄 변경이 필요하지 않습니다.

1. 영어 또는 다른 언어로 만든 바로 가기 [!DNL Insight.exe]을 시작합니다.
1. 프로필에 연결하고 클라이언트가 서버와 동기화되도록 합니다.
1. (선택 사항) IME를 사용하려면 [!DNL Insight.cfg] 파일을 다음과 같이 변경합니다.

   ```
   Localized IME = bool: true
   ```

   IME(입력 방법 편집기)를 사용하여 국제 문자를 입력할 수 있습니다.

1. (선택 사항) [!DNL Insight.cfg] 파일을 편집하여 소프트웨어를 자동으로 업데이트합니다.

   ```
   Update Software = bool: true
   ```

   IME 구현에 대한 지침을 참조하십시오.
1. 프로필 동기화 후 다시 시작하여 가장 최근 [!DNL .zbin] 파일을 사용합니다.

이제 클라이언트 설치가 완료되었습니다.
