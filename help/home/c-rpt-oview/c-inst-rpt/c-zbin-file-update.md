---
description: 모든 언어의 경우 보고서 서버 6.0 이상에는 "insight.zbin" 파일이 보고서 서버 루트 폴더에 복사되어야 합니다.
solution: Analytics
title: 언어 파일(.zbin 파일)을 사용하여 보고서 서버 업데이트
topic: Data workbench
uuid: 2ecf2afc-bb5f-4fc7-8fb8-a904fb7ed407
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 언어 파일(.zbin 파일)을 사용하여 보고서 서버 업데이트{#update-report-server-with-a-language-file-zbin-file}

모든 언어의 경우 보고서 서버 6.0 이상에는 &quot;insight.zbin&quot; 파일이 보고서 서버 루트 폴더에 복사되어야 합니다.

보고서 서버 언어 파일을 업데이트합니다.

1. 이름이 변경된 &quot;insight.zbin&quot; 파일을 루트 ReportServer 디렉토리에 추가합니다.
1. 보고서 서버 구성 파일(reportserver.cfg)에는 더블바이트 언어에 대한 글꼴 설정이 필요합니다. 예를 들어 중국어 번체에 SimSun을 사용하는 글꼴이 추가되어야 합니다.

   ```
   <b>Report Server.cfg - Add Fonts</b> 
   
   Fonts = vector: 2 items 
     0 = string: SimSun 
     1 = string: Arial
   ```

1. 보고서 서버 6.0의 매개 변수는 현지화를 위해 명령줄에 전달해야 합니다. 예:

   ```
   ReportServer.exe -Locale -zh-cn 
   ReportServer.exe -Locale -en-us
   ```

   >[!NOTE]
   >
   >로케일이 지정되지 않은 경우 보고서 서버는 기본적으로 영어로 설정됩니다.

   다음 단계에 따라 Locale 매개 변수를 사용하여 서비스로 ReportServer를 실행합니다.

   1. 관리자로 명령 프롬프트를 실행합니다.
   1. ReportServer 설치 폴더로 이동합니다.
   1. 다음 명령을 입력하여 서비스를 시작합니다.

      * 영어: [!DNL ReportServer.exe -RegServer -Locale -en-us]
      * 중국어: [!DNL ReportServer.exe -RegServer -Locale -zh-cn]

1. ReportServer가 올바른 매개 변수와 함께 실행 중인지 확인하려면:

   1. Windows 서비스 관리자를 엽니다.
   1. 마우스 오른쪽 버튼을 클릭합니다 [!DNL Adobe Insight Report Server - Properties].
   실행 파일 경로에 매개 변수가 포함됩니다.

   ```
   ReportServer.exe -Service ReportServer -Locale -en-us
   ```

