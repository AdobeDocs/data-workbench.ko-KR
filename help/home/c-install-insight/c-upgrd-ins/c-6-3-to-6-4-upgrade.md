---
description: 다음 단계에 따라 Data Workbench v6.4로 업그레이드하십시오.
title: 6.3에서 6.4로 업그레이드
uuid: 2461c1ab-cf99-4fb5-b431-d7062df7a53d
translation-type: tm+mt
source-git-commit: 2930bd3ae06e700e75144221fc993efdd6bd1e85
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---


# Upgrading 6.3 to 6.4{#upgrading-to}

다음 단계에 따라 Data Workbench v6.4로 업그레이드하십시오.

## 업그레이드 요구 사항 및 권장 사항 {#section-8704a9ac358246cd81233dd0982d534f}

Data Workbench 6.4로 업그레이드할 때 다음 요구 사항 및 권장 사항을 따르십시오.

>[!IMPORTANT]
>
>이전 설치에서 파일을 이동하는 대신 새로 설치된 기본 구성 파일을 사용하고 사용자 지정하는 것이 좋습니다. 단, 다음과 같습니다.

* **다음 실행** 에 ***대해*** Windows 2012 서버의 *MS System Center Endpoint Protection에* 대해 제외된 프로세스 추가:

   * **[!DNL InsightServer64.exe]**
   * **[!DNL ReportServer.exe]**
   * **[!DNL ExportIntegration.exe]**
   이렇게 하면 이러한 인터페이스 실행 파일에 대한 허용 목록 권한이 활성화됩니다.

* **서버에서&#x200B;*Trust_ca_cert.pem*인증서를 업데이트합니다**.
* **속성 프로필**&#x200B;재구성.

   * 속성 ** 폴더 ***의 이름이 Attribution*** - Premium *으로*&#x200B;변경되었습니다(Profiles\*Attribution - Premium*의 기본 설치에서 찾을 수 있습니다.).

   * Premium ** 프로필이 제거되고 작업 공간이 새 Attribution ***- Premium*** 폴더로 이동되었습니다.

* **Attribution *-Premium*설정을 업데이트합니다**. 기본 *Adobe SC* 프로필을 재정의하는 매개 변수 설정으로 프로파일을 사용자 정의한 경우 다음 구성 파일에서 사용자 정의 필드를 업데이트해야 합니다.

   * **[!DNL Decoding Instructions.cfg]**
   * **[!DNL SC Fields.cfg]**

* 이러한 재구성 때문에 서버 설치에서 이전 *기여도* 및 *프리미엄* 폴더를 제거하게 됩니다.

   **이 설정 변경**

   ```
   Profile = profileInfo:  
     Active = bool: true 
     Directories = vector: 6 items 
       0 = string: Base\\ 
       1 = string: Geography\\ 
       2 = string: Predictive Analytics\\ 
       3 = string: Adobe SC\\ 
   
       4 = string: Attribution\\ 
       5 = string: Premium\\
   ```

   다음 설정을 참조하십시오.

   ```
   Profile = profileInfo:  
     Active = bool: true 
     Directories = vector: 5 items 
       0 = string: Base\\ 
       1 = string: Geography\\ 
       2 = string: Predictive Analytics\\ 
       3 = string: Adobe SC\
       4 = string: Attribution - Premium\\
   ```

* **사용자 지정 Meta.cfg 파일을** 업데이트합니다(필요한 경우).

   이 릴리스에서 폴더 **[!DNL Meta.cfg]** 의 **[!DNL Base\Context and AdobeSC\Context]** 파일이 업데이트되었습니다.

   설치 중에 **meta.cfg** 파일을 재정의하면 프로필 사본을 이 매개 변수와 적절히 입력한 **메타데이터 벡터로** 업데이트해야 합니다.

   ```
   94 = meta: 
     path = string: SegmentExport:CRS Configuration/CRS Attributes 
     acceptable children = vector: 1 items 
       0 = Template: 
         name = string: CRS Attributes 
         value = CRSAttributeConfiguration: 
           Attribute Name = string: 
           Attribute Type(int,string) = string: 
           Field Name = string: 
   
   95 = meta: 
     path = string: SegmentExportQuery:CRS Configuration/Report Suite 
     acceptable children = vector: 1 items 
       0 = Template 
         name = string: Add Report Suite 
         value = string:
   ```

* **Windows 2012 서버에서 Microsoft Excel 보고서를 생성하려면 보고서 서버 권한을** 설정합니다.

   1. 루트 폴더(**[!DNL E:\ReportServer\]**)의 사용 권한을 *모든 사람 = 모든 제어로 설정합니다*.

   1. 적절한 권한이 있는 다음 폴더를 만듭니다.

      ```
      C:\Windows\SysWOW64\config\systemprofile\AppData\Local\Microsoft\Windows\INetCac‌he 
      C:\Windows\System32\config\systemprofile\AppData\Local\Microsoft\Windows\INetCac‌he 
      C:\Windows\System32\config\systemprofile\Desktop 
      C:\Windows\SysWOW64\config\systemprofile\Desktop
      ```

      >[!NOTE]
      >
      >Windows Server 2012에서 보고서 서버를 실행 중인 경우 Windows Server 2012 R2를 설치해야 합니다.

   1. 이러한 폴더의 소유자로 &quot;SYSTEM&quot;을 할당합니다.

* **보고서 서버에 글꼴을 추가합니다.** **[!DNL ReportServer.cfg]**파일에 다음 글꼴을 추가합니다(모든 언어용).

   ```
   Fonts = vector: 3 items 
     0 = string: Arial 
     1 = string: SimSun 
     2 = string: MS Mincho
   ```

* **Microsoft Excel **(필요한 경우) 버전을 업데이트합니다.

   Data Workbench 6.4가 릴리스되면서 Excel 2007에 대한 지원이 중단되었습니다. 또한 데이터 워크벤치는 64비트 아키텍처용 Microsoft Windows에서만 실행되므로 64비트 버전의 Microsoft Excel도 설치하는 것이 좋습니다.

* **워크스테이션(클라이언트) 설치에 필요한 64비트 아키텍처** .
* **워크스테이션 설정 마법사를 실행합니다**.

   InsightSetup.exe를 다운로드하여 실행하고 설치 지침을 따라 ***단계별로*** 실행하여 워크스테이션(클라이언트)의 새 버전을 설치합니다. 설치 마법사는 기본적으로 새 위치에 파일을 설치합니다.

   이제 프로그램 파일은 기본적으로 다음과 같이 저장됩니다.

   ```
   C:\Program Files\Adobe\Adobe Analytics\Data Workbench
   ```

   이제 데이터 파일(프로필, 인증서, 추적 로그 및 사용자 파일)이 기본적으로 다음과 같이 저장됩니다.

   ```
   C:\Users\<username>\AppData\Local\Adobe\Adobe Analytics\Data Workbench\
   ```

* **워크스테이션에 글꼴을 추가합니다**.

   파일에 **[!DNL Insight.cfg]** 다음 글꼴을 추가합니다(모든 언어용).

   ```
   Fonts = vector: 3 items 
     0 = string: Arial 
     1 = string: SimSun 
     2 = string: MS Mincho
   ```

