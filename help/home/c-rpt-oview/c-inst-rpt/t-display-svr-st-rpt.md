---
description: 데이터 워크벤치의 세부 상태 인터페이스는 데이터 워크벤치 서버의 고객인 데이터 워크벤치 서버 및 보고서 서버 시스템의 오류나 기타 문제를 해결하는 데 유용합니다.
solution: Analytics
title: 보고서 서버 상태 표시
topic: Data workbench
uuid: 5260266d-5bd1-4905-9619-f67f6e1bc54c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 보고서 서버 상태 표시{#displaying-report-server-status}

데이터 워크벤치의 세부 상태 인터페이스는 데이터 워크벤치 서버의 고객인 데이터 워크벤치 서버 및 보고서 서버 시스템의 오류나 기타 문제를 해결하는 데 유용합니다.

인터페이스에서 보고서 상태를 보려면 데이터 워크벤치 서버 [!DNL Master Server Detailed Status] [!DNL Servers] [!DNL Communications.cfg] 파일의 벡터에 보고서 상태 서버를 추가해야 합니다. 다음 절차에서는 보고서 상태 서버를 [!DNL Communications.cfg] 파일에 추가하는 방법에 대해 설명합니다.

인터페이스에 대한 자세한 [!DNL Detailed Status] 내용은 데이터 워크벤치 사용자 안내서의 관리 *인터페이스 장을 참조하십시오*.

**To add a[!DNL Report Status Server]**

1. 데이터 워크벤치 서버를 설치한 디렉토리(InsightServer64.exe)의 구성 요소 폴더로 이동합니다.

   예: [!DNL C:\Adobe\Server\Components]
1. 메모장과 같은 텍스트 편집기에서 [!DNL Communications.cfg] 엽니다.
1. 다음 파일 조각에서 강조 표시된 대로 [!DNL Servers] 벡터를 찾아 보고서 상태 서버를 이 벡터에 추가합니다.

   ```
    . . .
   Servers = vector: 17 items
       0 = FileServer: 
         Local Path = string: Audit\\
         URI = string: /Audit
       1 = FileServer: 
         Local Path = string: Bin\\
         URI = string: /Bin
       2 = FileServer: 
         Local Path = string: Components\\
         URI = string: /Components
     . . .
       16 = ReportStatusServer: 
         URI = string: /ReportStatus.vsp
   ```

1. 이전 단계의 파일 조각에서 강조 표시된 대로 [!DNL Servers] 벡터의 항목 카운트를 업데이트합니다(즉, 항목 값을 1씩 증가).
1. 파일을 저장합니다.
