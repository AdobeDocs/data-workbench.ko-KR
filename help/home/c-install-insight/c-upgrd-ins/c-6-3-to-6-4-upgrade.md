---
description: 다음 단계에 따라 Data Workbench v6.4로 업그레이드하십시오.
title: 6.3에서 6.4로 업그레이드
uuid: 2461c1ab-cf99-4fb5-b431-d7062df7a53d
exl-id: 540deb86-2463-4820-b67a-a32d68b4346e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# 6.3에서 6.4로 업그레이드{#upgrading-to}

{{eol}}

다음 단계에 따라 Data Workbench v6.4로 업그레이드하십시오.

## 업그레이드 요구 사항 및 Recommendations {#section-8704a9ac358246cd81233dd0982d534f}

Data Workbench 6.4로 업그레이드할 때 이러한 요구 사항과 권장 사항을 따르십시오.

>[!IMPORTANT]
>
>다음과 같은 예외를 제외하고 이전 설치에서 파일을 이동하는 대신 새로 설치된 기본 구성 파일을 사용하고 사용자 지정하는 것이 좋습니다.

* **추가** ***제외된 프로세스*** 대상 *Windows 2012 서버의 MS System Center Endpoint Protection* 다음 실행 파일의 경우:

   * **[!DNL InsightServer64.exe]**
   * **[!DNL ReportServer.exe]**
   * **[!DNL ExportIntegration.exe]**

   이렇게 하면 허용 목록에 추가하다 이러한 인터페이스 실행 파일에 대한 권한이 활성화됩니다.

* **업데이트 *Trust_ca_cert.pem* 서버의 인증서**.
* **속성 프로필 재구성**.

   * 다음 *속성* 폴더 이름이 ***속성 - Premium*** (기본 설치에서 찾을 수 있음) *프로필*\*기여도 분석 - Premium*).

   * 다음 *Premium* 프로필이 제거되고 작업 공간이 새 페이지로 이동되었습니다. ***속성 - Premium*** 폴더를 입력합니다.

* **업데이트 *Attribution-Premium* 설정**. 기본값을 무시하는 매개 변수 설정으로 프로파일을 사용자 정의한 경우 *Adobe SC* 프로필을 업데이트했다면 다음 구성 파일의 사용자 지정 필드를 업데이트해야 합니다.

   * **[!DNL Decoding Instructions.cfg]**
   * **[!DNL SC Fields.cfg]**

* 이 재구성 때문에 이전 *속성* 및 *Premium* 서버 설치의 폴더입니다.

   **다음 설정 변경**

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

* **사용자 지정 Meta.cfg 파일 업데이트** (필요한 경우).

   다음 **[!DNL Meta.cfg]** 파일 **[!DNL Base\Context and AdobeSC\Context]** 폴더가 이번 릴리스에서 업데이트되었습니다.

   를 재정의하는 경우 **meta.cfg** 설치하는 동안 파일을 업데이트해야 하며 이러한 매개 변수와 **메타데이터 벡터** 적절히 입력한 다음

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

* **보고서 서버 권한 설정** windows 2012 서버에서 Microsoft Excel 보고서를 생성하려면

   1. 루트 폴더의 권한 설정(**[!DNL E:\ReportServer\]**) *모든 사용자 = 전체 제어*.

   1. 적절한 권한을 사용하여 다음 폴더를 만듭니다.

      ```
      C:\Windows\SysWOW64\config\systemprofile\AppData\Local\Microsoft\Windows\INetCac‌he 
      C:\Windows\System32\config\systemprofile\AppData\Local\Microsoft\Windows\INetCac‌he 
      C:\Windows\System32\config\systemprofile\Desktop 
      C:\Windows\SysWOW64\config\systemprofile\Desktop
      ```

      >[!NOTE]
      >
      >Windows Server 2012에서 보고서 서버를 실행하는 경우 Windows Server 2012 R2가 설치되어 있어야 합니다.

   1. 이러한 폴더의 소유자로 &quot;SYSTEM&quot;을 할당합니다.

* **보고서 서버에 글꼴을 추가합니다.** **[!DNL ReportServer.cfg]**파일, 다음 글꼴 추가(모든 언어):

   ```
   Fonts = vector: 3 items 
     0 = string: Arial 
     1 = string: SimSun 
     2 = string: MS Mincho
   ```

* **Microsoft Excel ** 버전을 업데이트합니다(필요한 경우).

   Data Workbench 6.4가 릴리스되면서 Excel 2007에 대한 지원이 중단되었습니다. 또한 Data Workbench은 64비트 아키텍처용 Microsoft Windows에서만 실행되므로 64비트 버전의 Microsoft Excel도 설치하는 것이 좋습니다.

* **64비트 아키텍처** 워크스테이션(클라이언트) 설치에 필요합니다.
* **워크스테이션 설정 마법사 실행**.

   다운로드하여 실행하여 새로운 버전의 워크스테이션(클라이언트)을 설치합니다 ***InsightSetup.exe*** 설치 지침을 단계별로 안내합니다. 설치 마법사는 기본적으로 파일을 새 위치에 설치합니다.

   이제 프로그램 파일이 기본적으로 다음과 같이 저장됩니다.

   ```
   C:\Program Files\Adobe\Adobe Analytics\Data Workbench
   ```

   이제 데이터 파일(프로필, 인증서, 추적 로그 및 사용자 파일)이 기본적으로 다음과 같이 저장됩니다.

   ```
   C:\Users\<username>\AppData\Local\Adobe\Adobe Analytics\Data Workbench\
   ```

* **워크스테이션에 글꼴 추가**.

   에서 **[!DNL Insight.cfg]** 파일, 다음 글꼴 추가(모든 언어용):

   ```
   Fonts = vector: 3 items 
     0 = string: Arial 
     1 = string: SimSun 
     2 = string: MS Mincho
   ```
