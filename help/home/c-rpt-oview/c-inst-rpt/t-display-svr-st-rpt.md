---
description: Data Workbench의 상세 상태 인터페이스는 Data Workbench 서버의 클라이언트인 Data Workbench 서버 및 보고서 서버 시스템의 오류 또는 기타 문제를 해결하는 데 유용합니다.
title: 보고서 서버 상태 표시
uuid: 5260266d-5bd1-4905-9619-f67f6e1bc54c
exl-id: 3a717a81-7c5d-432d-b214-4ae0455b19b5
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 6%

---

# 보고서 서버 상태 표시{#displaying-report-server-status}

{{eol}}

Data Workbench의 상세 상태 인터페이스는 Data Workbench 서버의 클라이언트인 Data Workbench 서버 및 보고서 서버 시스템의 오류 또는 기타 문제를 해결하는 데 유용합니다.

에서 보고서 상태를 보려면 [!DNL Master Server Detailed Status] 인터페이스를 사용하려면 보고서 상태 서버를 [!DNL Servers] data workbench 서버의 벡터 [!DNL Communications.cfg] 파일. 다음 절차에서는 보고서 상태 서버를 [!DNL Communications.cfg] 파일:

에 대한 자세한 정보 [!DNL Detailed Status] 인터페이스, *Data Workbench 사용 안내서*.

**을(를) 추가하려면[!DNL Report Status Server]**

1. Data Workbench 서버를 설치한 디렉토리의 구성 요소 폴더로 이동합니다(InsightServer64.exe).

   예: [!DNL C:\Adobe\Server\Components]
1. 열기 [!DNL Communications.cfg] ( 메모장과 같은 텍스트 편집기)
1. 을(를) 찾습니다 [!DNL Servers] 벡터를 사용하여 보고서 상태 서버를 다음 파일 조각에서 강조 표시된 대로 이 벡터에 추가합니다.

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

1. 의 항목 수 업데이트 [!DNL Servers] 벡터(즉, 항목 값을 1씩 증가시킵니다)를 이전 단계의 파일 조각에서 강조 표시합니다.
1. 파일을 저장합니다.
