---
description: Data Workbench의 상세 상태 인터페이스는 Data Workbench 서버의 클라이언트인 Data Workbench 서버 및 보고서 서버 시스템의 오류 또는 기타 문제를 해결하는 데 유용합니다.
title: 보고서 서버 상태 표시
uuid: 5260266d-5bd1-4905-9619-f67f6e1bc54c
exl-id: 3a717a81-7c5d-432d-b214-4ae0455b19b5
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 6%

---

# 보고서 서버 상태 표시{#displaying-report-server-status}

Data Workbench의 상세 상태 인터페이스는 Data Workbench 서버의 클라이언트인 Data Workbench 서버 및 보고서 서버 시스템의 오류 또는 기타 문제를 해결하는 데 유용합니다.

[!DNL Master Server Detailed Status] 인터페이스에서 보고서 상태를 보려면 Data Workbench 서버의 [!DNL Communications.cfg] 파일에서 [!DNL Servers] 벡터에 보고서 상태 서버를 추가해야 합니다. 다음 절차에서는 보고서 상태 서버를 [!DNL Communications.cfg] 파일에 추가하는 방법을 설명합니다.

[!DNL Detailed Status] 인터페이스에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;의 관리 인터페이스 장을 참조하십시오.

**을(를) 추가하려면[!DNL Report Status Server]**

1. Data Workbench 서버를 설치한 디렉토리의 구성 요소 폴더로 이동합니다(InsightServer64.exe).

   예: [!DNL C:\Adobe\Server\Components]
1. 메모장과 같은 텍스트 편집기에서 [!DNL Communications.cfg] 을 엽니다.
1. [!DNL Servers] 벡터를 찾아 다음 파일 조각에서 강조 표시된 대로 보고서 상태 서버를 이 벡터에 추가합니다.

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

1. 이전 단계의 파일 조각에서 강조 표시된 대로 [!DNL Servers] 벡터에 대한 항목 수(즉, 항목 값을 하나씩 증가)를 업데이트합니다.
1. 파일을 저장합니다.
