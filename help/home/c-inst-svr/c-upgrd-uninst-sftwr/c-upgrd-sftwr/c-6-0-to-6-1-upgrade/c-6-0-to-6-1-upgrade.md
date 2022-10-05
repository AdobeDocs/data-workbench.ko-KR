---
description: 다음 단계에 따라 Data Workbench v6.0x 설치에서 data workbench v6.1로 업데이트하십시오.
title: Data Workbench 6.0에서 6.1로 업그레이드
uuid: 4671c2bf-06ab-49c4-8dd1-24115facd83b
exl-id: 559e1942-561c-4270-9670-550177730cdb,2a337d2e-c70e-4f35-a6c2-c3a7f50a0800
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%

---

# Data Workbench 6.0에서 6.1로 업그레이드{#data-workbench-to-upgrade}

{{eol}}

다음 단계에 따라 Data Workbench v6.0x 설치에서 data workbench v6.1로 업데이트하십시오.

**1단계**: [서버 업그레이드](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-7845393f76214aa7ad53ac4b2cca9e5b)

**2단계**: [보고서 서버 업그레이드](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-afd9560a446242e9b06490e5f98aaaec)

**3단계**: [클라이언트 업그레이드](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-6-0-to-6-1-upgrade.md#section-c896e57ecd2847afb18f4d8ef7cc0e06)

>[!IMPORTANT]
>
>서버, 보고서 서버 및 클라이언트 구성 요소가 64비트 Windows 운영 체제에서 실행되도록 업그레이드됩니다.

## 서버 업그레이드 {#section-7845393f76214aa7ad53ac4b2cca9e5b}

다음 단계에 따라 을(를) 업데이트합니다 **[!UICONTROL Server v6.1]** 구성 요소:

1. 사용 **[!UICONTROL Software and Docs]** 프로필, 열기 **[!UICONTROL Start Here]** 작업 공간에서 필요한 모든 서버 패키지를 로컬 폴더로 다운로드합니다.

   * 다운로드 **[!UICONTROL Server Packages]** \ **[!UICONTROL v6.1]** zip 폴더를 압축하고 모든 파일을 추출합니다.

      서버 패키지에는 다음이 포함됩니다 **[!UICONTROL Lookup]** 및 **[!UICONTROL Profile]** 폴더 **[!UICONTROL Base]** 및 **[!UICONTROL Transform]** 프로필을 업데이트하여 서버를 업데이트합니다.

      * 다운로드 **[!UICONTROL Profiles]** 폴더.
      * 다운로드 **[!UICONTROL Lookup]** 폴더.
      * 다운로드 **[!UICONTROL Report Server]** \ **[!UICONTROL v6.1]** 패키지.
      * 추가 다운로드 **[!UICONTROL Sensor]**, **[!UICONTROL Documentation]**, 및 **[!UICONTROL Dashboard]** 시스템에 필요한 파일입니다.

1. 를 중지합니다. **[!UICONTROL Adobe Insight Server]** 서비스.

   ![](assets/install_server_download1.png)

1. 다운로드한 **[!UICONTROL Server]** 패키지:

   1. 바꾸기 [!DNL Server\Bin] 폴더를 업데이트하여 [!DNL InsightServer64.exe] 및 지원 파일

   1. 바꾸기 [!DNL Server\Profiles] 폴더를 입력합니다. 모든 파일을 덮어쓸 수 있습니다.
   1. 업데이트 [!DNL Server\Lookups] 폴더를 입력합니다. 새로 다운로드한 파일을 폴더에 이미 있는 사용자 정의 파일에 추가할 수 있습니다.
   1. 바꾸기 [!DNL Server\Software] 업데이트할 폴더 [!DNL Insight.exe] 및 [!DNL ReportServer.exe]
   1. 업데이트 [!DNL Server\Scripts] 업데이트할 폴더 [!DNL TnTSend.exe].

1. 만약 **[!UICONTROL DeviceAtlas]**&#x200B;를 채울 필요가 있습니다. [번들 업데이트](/help/home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-deviceatlas-update.md) 에 위치 [!DNL Server\Lookups] 폴더를 입력합니다.

1. 구성 [!DNL Profile.cfg] 파일에서 각 프로필에 대한 항목 수를 반영하도록 벡터를 업데이트할 수 있습니다.

   예를 들어 **[!UICONTROL Predictive Analytics]** 프로필 이 설정을 업데이트해야 합니다.

   ```
   Directories = vector: 5 items
       0 = string: Base\\
       1 = string: Geography\\
       2 = string: Predictive Analytics\\
       3 = string: Adobe SC\\
       4 = string: Profile Name\\
   ```

1. Predictive Analytics 기능을 위해 PAServer.cfg 파일을 구성하고 저장합니다.

   예측 분석 작업을 서버에 제출하려는 경우 다음을 구성해야 합니다 [!DNL Server > Predictive Analytics > Dataset > PAServer.cfg] 파일 을 사용하여 서버 측 클러스터링 제출을 관리할 수 있습니다.

   사용자 지정 프로필은 Predictive Analytics 구성 프로필에서 설정을 상속해야 하므로 을(를) 구성하고 저장할 수 있습니다 [!DNL PAServer.cfg] 사이트의 구현을 기반으로 한 파일입니다.

1. 을(를) 정의합니다 **[!UICONTROL Log Source ID]**.

   다음 **[!UICONTROL Recording of Rows per Log Source]** 에 추가됨 **[!UICONTROL v6.04]** 사용자 지정 프로필의 [!DNL Log Processing.cfg] 파일 이름을 고유하게 지정하여 **[!UICONTROL Log Source ID]**.

   ```
   Log Processing.cfg
   Log Source ID = string: <Name your ID Here>
   ```

   로그 소스 ID가 정의되지 않은 경우 다음 오류가 표시됩니다.

   ```
   Missing Log Source ID in log processing.cfg.
   Log Source ID must be defined for all log sources.
   ```

1. 왜냐하면 [!DNL EventMessages.dll] 이(가) 업데이트되면 등록을 취소한 다음 등록해야 합니다 **[!UICONTROL Adobe Insight Server]** 클러스터 간에 매핑됩니다.

   * [!DNL InsightServer64.exe /unregserver]
   * [!DNL InsightServer64.exe /regserver]

1. 시작 **[!UICONTROL Adobe Insight Server]** 클러스터 간 서비스.

이제 서버 설치가 완료되었습니다.

## 보고서 서버 업그레이드 {#section-afd9560a446242e9b06490e5f98aaaec}

>[!IMPORTANT]
>
>로 업그레이드하기 전에 **[!UICONTROL Report Server v6.1]**, 로 먼저 업그레이드해야 합니다. **[!UICONTROL Server v6.1]**.

1. 사용 **[!UICONTROL Software and Docs]** 프로필, 다운로드 **[!UICONTROL v6.1]** 에서 **[!UICONTROL Report Server]** 패키지를 로컬 폴더로

1. 복사 **[!UICONTROL Report Server 6.1]** 다운로드한 패키지에서 프로필 패키지를 바꿉니다.

   >[!NOTE]
   >
   >다음 [!DNL Insight.zbin] 파일의 [!DNL install] 폴더는 로컬라이제이션에 사용되는 백업 파일이며 [!DNL install] 디렉토리. 이 파일 또는 기타 [!DNL .zbin] 파일은 시작할 때 전달된 명령줄 설정에 따라 사용됩니다.

1. (선택 사항) Data Workbench는 현재 영어(-en-us) 및 중국어(-zh-cn)를 지원합니다. 단일 및 2바이트 문자를 지원하려면 글꼴을 설정해야 합니다.

   ```
   Report Server.cfg - Add Fonts
      Fonts = vector: 2 items
      0 = string: SimSun
      1 = string: Arial
   ```

   Windows 운영 체제에는 나열된 글꼴도 설치되어 있어야 합니다.

1. 구성 [!DNL Report Server v6.1] 로컬라이제이션용.

   1. 를 중지합니다. **[!UICONTROL Adobe Insight Report Server]** 서비스.
   1. 명령 프롬프트를 &quot;관리자&quot;로 시작합니다.
   1. 보고서 서버로 이동합니다 [!DNL install] 폴더를 입력합니다.
   1. 다음 명령을 사용하여 보고서 서버 서비스를 삭제합니다.

      ```
      ReportServer.exe /unregserver
      ```

   1. 언어 설정에 따라 서비스를 시작합니다.

      ```
      ReportServer.exe -RegServer -Locale -en-us (English)
      ReportServer.exe -RegServer -Locale -zh-cn (Simplified Chinese)
      ```

1. 보고서 서버가 올바른 설정으로 실행 중인지 확인하려면 다음을 엽니다 **[!UICONTROL Windows Service Manager]** 마우스 오른쪽 단추 클릭 **[!UICONTROL Adobe Insight Report Server - Properties]**. 실행 파일의 경로에 업데이트된 명령줄 설정이 표시됩니다.

이제 보고서 서버 설치가 완료되었습니다.

## 클라이언트 업그레이드 {#section-c896e57ecd2847afb18f4d8ef7cc0e06}

>[!IMPORTANT]
>
>로 업그레이드하기 전에 **[!UICONTROL Client v6.1]**&#x200B;로 업그레이드하려면 먼저 관리자가 **[!UICONTROL Insight Server v6.1.]**

1. Launch [!DNL Insight.exe] 하지만 프로필에 연결하지 마십시오.
1. 편집 [!DNL Insight.cfg] 파일.

   ```
   Update Software = bool: true
   ```

1. 프로필에 연결합니다.

   클라이언트가 서버와 동기화할 수 있도록 하고 클라이언트가 최신 v6.1클라이언트 프로필, 실행 파일 및 구성 파일로 업그레이드됩니다.

   >[!NOTE]
   >
   >다음 [!DNL Insight.zbin] 파일의 [!DNL install] 폴더는 로컬라이제이션에 사용되는 백업 파일이며 반드시 있어야 합니다. 이 파일 또는 기타 [!DNL .zbin] 파일은 시작할 때 전달된 명령줄 설정에 따라 사용됩니다.

   자세한 내용은 [현지화 언어 설정](../../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-0-to-6-1-upgrade/c-localized-ime.md#concept-86d7602cd6ec416b8d4a518f325e001e) 를 추가하려면 [!DNL insight.zbin] 지역화된 설정에 필요한 파일입니다.

**추가 클라이언트 설정**

구성하기 전 [!DNL Insight.exe] 및 지원 파일은 클라이언트 응용 프로그램을 종료해야 합니다.

중국어 간체를 설치하려면

1. 명령줄 설정에서 로 전달되는 바로 가기를 만듭니다. [!DNL Insight.exe] 파일.

   ```
   Insight.exe -zh-cn
   ```

1. 구성 [!DNL Insight.cfg] 단일 및 2바이트 글꼴 문자를 지원합니다.

   Data Workbench는 현재 영어 및 중국어 간체를 모두 지원합니다. 다음 언어를 모두 지원할 글꼴을 선택할 수 있습니다.

   ```
   Fonts = vector: 2 items
   0 = string: SimSun
   1 = string: Arial
   ```

   Windows 운영 체제에는 요청된 글꼴도 설치되어 있어야 합니다.

1. 만든 바로 가기를 시작하여 프로필과 업데이트된 을 동기화합니다. [!DNL zbin] 파일.

IME(입력 방법 편집기)를 사용하려면

IME에서 국제 문자를 입력할 수 있습니다.

1. 업데이트 [!DNL Insight.cfg] 다음 설정을 사용하는 파일:

   ```
   Localized IME = bool: true
   ```

1. 만든 바로 가기를 시작하여 프로필과 업데이트된 정보를 동기화합니다 [!DNL .zbin] 파일.

이제 클라이언트 설치가 완료되었습니다.
