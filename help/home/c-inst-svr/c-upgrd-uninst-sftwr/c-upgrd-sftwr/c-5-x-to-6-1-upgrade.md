---
description: 다음 단계에 따라 Insight v5.5x 설치에서 데이터 워크벤치 v6.1로 업데이트합니다.
solution: Analytics
title: Data Workbench 5.5 - 6.1 업그레이드
topic: Data workbench
uuid: 14e3612e-11a2-402a-9478-904ec55df23c
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Data Workbench 5.5 - 6.1 업그레이드{#data-workbench-to-upgrade}

다음 단계에 따라 Insight v5.5x 설치에서 데이터 워크벤치 v6.1로 업데이트합니다.

**1단계**:서버 [업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-08bd6fe3da8740fcb19688e8cac6f223)

**2단계**:보고서 [서버 업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-afd9560a446242e9b06490e5f98aaaec)

**3단계**:클라이언트 [업그레이드](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-5-x-to-6-1-upgrade.md#section-c896e57ecd2847afb18f4d8ef7cc0e06)

>[!IMPORTANT]
>
>서버, 보고서 서버 및 클라이언트 구성 요소는 64비트 Windows 운영 체제에서 실행되도록 업그레이드됩니다.

## 서버 업그레이드 {#section-08bd6fe3da8740fcb19688e8cac6f223}

다음 단계에 따라 **[!UICONTROL Server v6.1]** 구성 요소를 업데이트합니다.

1. 프로필을 **[!UICONTROL Software and Docs]** **[!UICONTROL Start Here]** 사용하여 작업 공간을 열고 필요한 모든 서버 패키지를 로컬 폴더에 다운로드합니다.

   * Download **[!UICONTROL Server Packages]** \ **[!UICONTROL v6.1]** zip folders and extract all files.

      이 **[!UICONTROL Server]** 패키지에는 서버를 업데이트하기 위해 추가 및 대체할 수 있는 **[!UICONTROL Lookup]** 및 **[!UICONTROL Profile]** 조회 파일과 함께 **[!UICONTROL Base]** 및 **[!UICONTROL Transform]** 폴더가 포함됩니다.

   * 새 **[!UICONTROL Profiles]** 폴더를 다운로드합니다.
   * 업데이트된 **[!UICONTROL Lookup]** 폴더를 다운로드합니다.
   * \ **[!UICONTROL Report Server]** 패키지를 다운로드합니다 **[!UICONTROL v6.1]** .
   * 시스템에 필요한 추가 **[!UICONTROL Sensor]**&#x200B;및 **[!UICONTROL Documentation]****[!UICONTROL Dashboard]** 파일을 다운로드합니다.

1. 서비스를 **[!UICONTROL Adobe Insight Server]** 중지합니다.

   ![](assets/install_server_download1.png)

1. 다운로드한 **[!UICONTROL Server]** 패키지에서:

   1. 폴더를 [!DNL Server\Bin] 교체하여 [!DNL InsightServer64.exe] 및 지원 파일을 업데이트합니다.

   1. 폴더를 [!DNL Server\Profiles] 교체합니다. 모든 파일을 덮어쓸 수 있습니다.
   1. 폴더를 [!DNL Server\Lookups] 업데이트합니다. 새로 다운로드한 파일을 폴더에 이미 있는 사용자 정의 파일에 추가할 수 있습니다.
   1. 업데이트할 [!DNL Server\Software] 폴더 [!DNL Insight.exe] 바꾸기 및 [!DNL ReportServer.exe]

   1. 업데이트할 [!DNL Server\Scripts] 폴더를 업데이트합니다 [!DNL TnTSend.exe].

1. 사용하는 **[!UICONTROL DeviceAtlas]**&#x200B;경우 [폴더에 있는 번들을](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/trans-config-file/c-deviceatlas-update.html) [!DNL Server\Lookups] 업데이트해야 합니다.
1. 각 프로필에 대한 항목 수를 반영하도록 벡터가 업데이트되도록 [!DNL Directories] [!DNL Profile.cfg] 파일에 설정합니다.

   예를 들어 프로필을 활성화하려면 이 **[!UICONTROL Predictive Analytics]** 설정을 업데이트해야 합니다.

   ```
   Directories = vector: 5 items 
       0 = string: Base\\ 
       1 = string: Geography\\ 
       2 = string: Predictive Analytics\\ 
       3 = string: Adobe SC\\ 
       4 = string: Profile Name\\
   ```

1. 예측 분석 기능을 업그레이드하도록 [!DNL PAServer.cfg] 파일을 구성하고 저장합니다.

   예측 분석 작업을 서버에 제출하려면 서버측 클러스터링 제출을 관리할 [!DNL Server > Predictive Analytics > Dataset > PAServer.cfg] 파일을 구성해야 합니다.

   사용자 지정 프로필은 예측 분석 구성 프로필의 설정을 상속해야 하므로 사이트의 구현을 [!DNL PAServer.cfg] 기반으로 설정을 구성하고 저장할 수 있습니다.

1. Define the **[!UICONTROL Log Source ID]**.

   사용자 **[!UICONTROL Recording of Rows per Log Source]** 지정 프로필의 파일에 고유한 이름을 추가하여 **[!UICONTROL v6.04]** 사용자 지정 프로필의 [!DNL Log Processing.cfg] 파일에 **[!UICONTROL Log Source ID]**&#x200B;추가되고 정의되었습니다.

   ```
   Log Processing.cfg
   Log Source ID = string: <Name your ID Here>
   ```

   로그 소스 ID가 정의되지 않은 경우 다음 오류가 표시됩니다.

   ```
   Missing Log Source ID in log processing.cfg.  
   Log Source ID must be defined for all log sources.
   ```

1. 이 [!DNL EventMessages.dll] 업데이트되었으므로 등록을 취소하고 클러스터 전체에 **[!UICONTROL Adobe Insight Server]** 등록해야 합니다.

   * [!DNL InsightServer64.exe /unregserver]
   * [!DNL InsightServer64.exe /regserver]

1. 클러스터 전체에서 **[!UICONTROL Adobe Insight Server]** 서비스를 시작합니다.

이제 서버 설치가 완료되었습니다.

## 보고서 서버 업그레이드 {#section-afd9560a446242e9b06490e5f98aaaec}

>[!IMPORTANT]
>
>로 업그레이드하기 **[!UICONTROL Report Server v6.1]**&#x200B;전에 먼저 로 업그레이드해야 합니다 **[!UICONTROL Server v6.1]**.

1. 프로필을 사용하여 **[!UICONTROL Software and Docs]** 패키지에서 로컬 폴더로 **[!UICONTROL v6.1]** **[!UICONTROL Report Server]** 다운로드합니다.
1. 다운로드한 **[!UICONTROL Report Server 6.1]** 패키지에서 복사하고 프로필 패키지를 교체합니다.

   >[!NOTE]
   >
   >폴더의 [!DNL Insight.zbin] 파일은 로컬라이제이션에 사용되는 백업 파일이며 [!DNL install] [!DNL install] 디렉토리에 있어야 합니다. 이 파일 또는 기타 [!DNL .zbin] 파일은 시작할 때 전달된 명령줄 설정에 따라 사용됩니다.

1. (선택 사항) 더블바이트 문자를 지원하도록 보고서 서버 구성 파일을 수정합니다.

   데이터 워크벤치는 현재 영어(-en-us) 및 중국어(-zh-cn)를 지원합니다. 단일 및 더블바이트 문자를 지원하려면 글꼴을 설정해야 합니다.

   ```
   Report Server.cfg - Add Fonts 
      Fonts = vector: 2 items  
      0 = string: SimSun  
      1 = string: Arial 
   ```

   Windows 운영 체제에도 나열된 글꼴이 설치되어 있어야 합니다.

1.  [!DNL Report Server v6.1].

   1. 서비스를 **[!UICONTROL Adobe Insight Report Server]** 중지합니다.
   1. 명령 프롬프트를 &quot;관리자&quot;로 실행합니다.
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

1. 보고서 서버가 올바른 설정으로 실행 중인지 확인하려면 열고 **[!UICONTROL Windows Service Manager]** 마우스 오른쪽 단추를 클릭합니다 **[!UICONTROL Adobe Insight Report Server - Properties]**. 실행 파일의 경로에 업데이트된 명령줄 설정이 표시됩니다.

이제 보고서 서버 설치가 완료되었습니다.

## 클라이언트 업그레이드 {#section-c896e57ecd2847afb18f4d8ef7cc0e06}

>[!IMPORTANT]
>
>로 업그레이드하기 **[!UICONTROL Client v6.1]**&#x200B;전에 관리자는 먼저 **[!UICONTROL Server v6.1.]**

1. 실행은 [!DNL Insight.exe] 하되 프로파일에는 연결하지 마십시오.
1. 소프트웨어를 자동으로 업데이트하지 않도록 [!DNL Insight.cfg] 파일을 편집합니다.

   ```
   Update Software = bool: false
   ```

1. 프로필에 **[!UICONTROL Software and Docs]** 연결합니다(softdocs).
1. 다운로드 [!DNL Software\Insight Client\v6.10].
1. (선택 사항) 더블바이트 문자를 [!DNL insight.cfg] 지원하도록 수정합니다.

   데이터 워크벤치에서는 현재 영어 및 중국어 간체를 모두 지원합니다. 두 언어를 모두 지원하려면 글꼴을 선택하십시오.

   ```
   Fonts = vector: 2 items  
   0 = string: SimSun 
   1 = string: Arial
   ```

1. 클라이언트를 종료합니다.
1. 다운로드한 **v6.1** 클라이언트 패키지의 파일을 [!DNL Install] 폴더에 복사합니다.

   >[!NOTE]
   >
   >설치 폴더의 [!DNL Insight.zbin] 파일은 로컬라이제이션에 사용되는 백업 파일이며 설치 디렉토리에 있어야 합니다. 이 파일 또는 기타 [!DNL .zbin] 파일은 시작할 때 전달된 명령줄 설정에 따라 사용됩니다.
   >
   >예를 들어 중국어 간체를 시작하려면 명령줄 설정에서 전달하는 단축키를 만듭니다.
   >
   >```
   >Insight.exe -zh-cn
   >```
   >
   >영어(기본값)로 시작하려면 명령줄 변경이 필요하지 않습니다.

1. Launch for English [!DNL Insight.exe] 또는 다른 언어로 만든 바로 가기입니다.
1. 프로필에 연결하여 클라이언트가 서버와 동기화할 수 있도록 합니다.
1. (선택 사항) IME를 사용하려면 [!DNL Insight.cfg] 파일을 변경합니다.

   ```
   Localized IME = bool: true
   ```

   IME(Input Method Editor)를 사용하여 국제 문자를 입력할 수 있습니다.

1. (선택 사항) [!DNL Insight.cfg] 파일을 편집하여 소프트웨어를 자동으로 업데이트합니다.

   ```
   Update Software = bool: true
   ```

   IME 구현 지침을 참조하십시오.
1. 프로필 동기화 후 다시 시작하여 가장 최근 [!DNL .zbin] 파일을 사용합니다.

이제 클라이언트 설치가 완료되었습니다.
