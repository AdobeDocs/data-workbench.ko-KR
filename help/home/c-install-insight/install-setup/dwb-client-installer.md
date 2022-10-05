---
description: Data Workbench은 워크스테이션(클라이언트) 응용 프로그램을 설치하기 위한 설정 마법사를 제공합니다.
title: 워크스테이션 설정 마법사
uuid: e2bf6606-e7ba-439f-b50c-118706ab5b7d
exl-id: bfd9f2ad-282a-4be8-9f66-53e045648ef1
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 1%

---

# 워크스테이션 설정 마법사{#workstation-setup-wizard}

{{eol}}

Data Workbench은 워크스테이션(클라이언트) 응용 프로그램을 설치하기 위한 설정 마법사를 제공합니다.

## 설치 마법사를 사용하여 워크스테이션 설치 {#section-58da9bb6196c46eab3b54146913fdcb8}

설치 마법사 실행 파일을 시작하고 각 단계를 수행하여 워크스테이션 클라이언트 프로그램을 설치합니다. 워크스테이션을 설치한 후 서버 및 프로필에 연결할 수 있습니다.

1. 워크스테이션 설치 프로그램 실행 파일을 두 번 클릭합니다.
1. 클릭 **예** 프로그램을 Windows에 설치할 수 있도록 허용
1. 선택 **언어** 설정 마법사:

   마법사가 열립니다.

   ![](assets/6_4_workstation_wizard.png)

1. 클릭 **다음** on **Data Workbench 설정 마법사 시작** 대화 상자.

1. 을(를) 설치하려면 선택합니다. **새 설치** 또는 **업그레이드 또는 복구** 기존 설치.

   **새 설치** 이전에 설치한 파일을 모두 덮어씁니다.

   **업그레이드** 워크스테이션을 최신 버전으로 업데이트하거나 기존 설치를 복구할 수 있습니다. 설치된 Data Workbench 비교 **Insight.exe** 파일을 사용하여 최신 버전의 클라이언트를 사용할 수 있는 경우 워크스테이션 설정 마법사를 실행합니다.

1. 설치 위치 선택:

   **일반** 는 기본 폴더 및 위치에 설치됩니다.

   * 프로그램 파일은 기본적으로 다음과 같이 저장됩니다.

      ```
      C:\Program Files\Adobe\Adobe Analytics\Data Workbench
      ```

   * 데이터 파일(프로필, 인증서, 추적 로그 및 사용자 파일)은 기본적으로 다음과 같이 저장됩니다.

      ```
      C:\Users\<username>\AppData\Local\Adobe\Adobe Analytics\Data Workbench\
      ```

      >[!IMPORTANT]
      >
      >일반 ***Insight.cfg*** 서버 세부 정보가 없는 파일은 처음에 설치됩니다. 새로 설치한 을 사용하는 것이 좋습니다 ***Insight.cfg*** 이전 설치에서 파일을 이동하지 않고 파일을 사용자 지정하고 사용자 지정합니다. 워크스테이션의 설치 경로가 변경되었으므로 글꼴이 추가되어 *사용자 폴더*&#x200B;및 *TraceFileComponent * 를 제거하는 것이 좋습니다.

1. (선택 사항) **사용자 지정** 언어 패키지 및 프로그램 및 데이터 파일의 위치를 선택합니다.
1. 위치 선택 **시작 메뉴의 바로 가기**.

   ![](assets/6_4_workstation_wizard_folder.png)

   클릭 **시작 메뉴 폴더를 만들지 않음** Windows 시작 메뉴에 바로 가기를 설치하지 않으려면

1. **다음을 클릭합니다.** 선택한 파일 위치 경로 및 언어에 대한 요약이 표시됩니다. 클릭 **설치.**

1. 을(를) 찾습니다 **Data Workbench 인증서**.

   설치 마법사가 설치 중에 Data Workbench 인증서를 찾을 수 없으면 대화 상자를 열어 인증서 위치(즉, **.pem** 기본적으로 클라이언트에 있는 파일 **인증서** 폴더)를 클릭하거나 **건너뛰기** 를 클릭하여 설치한 후 인증서를 찾습니다.

   클릭 **설치** 인증서를 찾은 후

1. 설치 마법사가 완료되고 Data Workbench이 설치된 후 **완료** 설정을 완료하려면

   >[!NOTE]
   >
   >워크스테이션 설정 마법사의 기본 로그 위치  `C:\Users\<userName>\AppData\Local\Temp`.

   을(를) 선택합니다 **애플리케이션 시작** 확인란을 선택하여 설정 후 workbench를 엽니다.

1. **연결 구성** 대상 **[!DNL Insight.cfg]** 파일.

   워크스테이션을 설치한 후에 Enhanced Workstation Configuration Experience Workspace가 열리고 [서버 연결 정보 입력](/help/home/c-get-started/c-insght-config-param.md) 에서 *Insight.cfg* 파일 및 드롭다운에서 프로필을 선택하는 옵션입니다. 서버에 대한 연결 상태를 볼 수도 있습니다.

   ![](assets/6_4_workstation_install_conf_conn.png)

## 설치 폴더 {#section-b5ea5a3b3ecb4622aef713972f3f8ebd}

Data Workbench 폴더 구조에는 두 개의 설치 위치가 있습니다.

* **프로그램 파일** 다음 **Insight.exe** 및 지원 클라이언트 파일(**Insight.ini**)가 이제 기본적으로 다음 위치에 있습니다.

   ```
   C:\Program Files\Adobe\Analytics\DataWorkbench
   ```

* 다음 **Appdata** 폴더를 입력합니다.

   **Insight.cfg**, 프로필, 인증서, 추적 로그 및 사용자 파일은 이제 기본적으로

   ```
   C:\Users\<Winuser>\AppData\Adobe\Analytics\DataWorkbench\ 
   ```

   의 경로를 설정할 수 있습니다 **Appdata** 폴더의 `Insight.ini` 파일:

   ```
   [InitialSettings] 
   AppDataFolder=C:\Users\mhiatt\AppData\Local\Adobe\Adobe Analytics\Data Workbench\ 
   Locale=en-us
   ```

## 워크스테이션 제거 {#section-5ce2e233fe4348469ef1b3c451dd5b70}

이제 Data Workbench에 워크스테이션을 제거할 실행 파일이 포함되어 있습니다(기본적으로 다음 위치에 있음). **`Program Files\Adobe\Adobe Analytics\Data Workbench\ unins000.exe`**).

시작 및 단계에 따라 하드 드라이브에서 Data Workbench 워크스테이션 파일을 제거합니다.

>[!NOTE]
>
>을(를) 시작할 수 있습니다 **unins000.exe** 폴더에서 실행 가능한 다음 **제거 Data Workbench** 시작 메뉴 또는 **[!UICONTROL Control Panel]** > **[!UICONTROL Program and Features]**.
