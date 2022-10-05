---
description: 모든 언어의 경우 보고서 서버 6.0 이상에서는 보고서 서버 루트 폴더에 복사된 "insight.zbin" 파일이 필요합니다.
title: 언어 파일(.zbin 파일)로 보고서 서버 업데이트
uuid: 2ecf2afc-bb5f-4fc7-8fb8-a904fb7ed407
exl-id: a76b7c01-83f0-4cf2-97a9-07d51cc75b3c
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 9%

---

# 언어 파일(.zbin 파일)로 보고서 서버 업데이트{#update-report-server-with-a-language-file-zbin-file}

{{eol}}

모든 언어의 경우 보고서 서버 6.0 이상에서는 보고서 서버 루트 폴더에 복사된 &quot;insight.zbin&quot; 파일이 필요합니다.

보고서 서버 언어 파일을 업데이트합니다.

1. 이름이 변경된 &quot;insight.zbin&quot; 파일을 루트 ReportServer 디렉토리에 추가합니다.
1. 보고서 서버 구성 파일(reportserver.cfg)에는 더블바이트 언어에 대한 글꼴 설정이 필요합니다. 예를 들어, 중국어 번체는 SimSun을 사용하여 글꼴을 추가해야 합니다.

   ```
   <b>Report Server.cfg - Add Fonts</b> 
   
   Fonts = vector: 2 items 
     0 = string: SimSun 
     1 = string: Arial
   ```

1. 지역화를 위해 명령줄에서 보고서 서버 6.0에 대한 매개 변수를 전달해야 합니다. 예를 들면 다음과 같습니다.

   ```
   ReportServer.exe -Locale -zh-cn 
   ReportServer.exe -Locale -en-us
   ```

   >[!NOTE]
   >
   >로케일을 지정하지 않으면 보고서 서버의 기본값이 영어로 지정됩니다.

   다음 단계에 따라 Locale 매개 변수를 사용하여 ReportServer as a service를 시작합니다.

   1. 관리자로 명령 프롬프트를 실행합니다.
   1. ReportServer 설치 폴더로 이동합니다.
   1. 서비스를 시작하려면 다음 명령을 입력합니다.

      * 영어: [!DNL ReportServer.exe -RegServer -Locale -en-us]
      * 중국어: [!DNL ReportServer.exe -RegServer -Locale -zh-cn]

1. ReportServer가 올바른 매개 변수로 실행되고 있는지 확인하려면:

   1. Windows 서비스 관리자를 엽니다.
   1. 마우스 오른쪽 단추 클릭 [!DNL Adobe Insight Report Server - Properties].

   실행 파일 경로에는 다음과 같은 매개 변수가 포함됩니다.

   ```
   ReportServer.exe -Service ReportServer -Locale -en-us
   ```
