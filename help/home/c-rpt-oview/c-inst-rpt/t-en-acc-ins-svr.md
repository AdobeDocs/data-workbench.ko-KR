---
description: Data Workbench 서버에 연결하려면 보고서 서버에 해당 서버에 액세스할 수 있는 권한이 있어야 합니다.
title: Data Workbench 서버에 대한 액세스 활성화
uuid: e112ac2a-34fe-40a2-9324-262f5cb1f681
exl-id: bf409413-470e-4e05-9bd2-b5b511bbe4a5
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 6%

---

# Data Workbench 서버에 대한 액세스 활성화{#enabling-access-to-the-data-workbench-server}

Data Workbench 서버에 연결하려면 보고서 서버에 해당 서버에 액세스할 수 있는 권한이 있어야 합니다.

보고서 서버의 액세스 제어 파일에 보고서 서버의 일반 이름(보고서 서버의 디지털 인증서에 지정된 이름)을 추가하여 Data Workbench 서버에 대한 액세스 권한을 부여합니다.

>[!NOTE]
>
>클러스터형 환경에서 작업할 경우 동기화 문제를 방지하기 위해 마스터 Data Workbench 서버에 액세스하도록 보고서 서버를 구성해야 합니다. Data Workbench에서는 [!DNL Servers Manager]의 [!DNL Related Servers] 메뉴 항목을 사용하여 클러스터의 처리 서버에 대한 정보를 볼 수 있습니다. [!DNL Servers Manager]에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;의 관리 인터페이스 장을 참조하십시오.

다음 절차에서는 Data Workbench 서버의 액세스 제어 파일에 보고서 서버를 수동으로 추가하는 방법을 설명합니다. 이러한 방식으로 액세스 제어 파일을 업데이트하려면 Data Workbench 서버가 설치된 시스템에서 파일 시스템 액세스 권한이 있어야 합니다.

Data Workbench에서 [!DNL Server Files Manager] 을 사용하여 서버의 액세스 제어 파일을 업데이트할 수도 있습니다. 이렇게 하려면 Data Workbench 클라이언트에 서버에 대한 관리 권한이 있어야 합니다.

[!DNL Server Files Manager]에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;의 관리 인터페이스 장을 참조하십시오.

**Data Workbench 서버에 대한 액세스를 구성하려면**

1. Data Workbench 서버를 설치한 디렉토리의 액세스 제어 폴더로 이동합니다(InsightServer64.exe).

   예: [!DNL C:\Adobe\Server\Access Control]

1. 메모장과 같은 텍스트 편집기에서 [!DNL Access Control.cfg] 을 엽니다.
1. 다음 파일 조각에서 강조 표시된 대로 [!DNL Report Server AccessGroup] 을 찾아 [!DNL Report Server’s] 공통 이름을 이 그룹에 추가합니다. ([!DNL Report Server’s] 디지털 인증서에 표시되는 것과 동일한 일반 이름을 입력합니다.)

   ```
   . . .
     5 = AccessGroup: 
       Members = vector: 1 items
         0 = string: CN: ReportCommonName
       Name = string: Report Server
       Read-Only Access = vector: 5 items
         0 = string: /Profiles/$
         1 = string: /Status/
         3 = string: /Software/
         4 = string: /Addresses/
         5 = string: /Users/$
       Read-Write Access = vector: 3 items
         0 = string: /Profiles/
         1 = string: /Users/%CN%/
         2 = string: /ReportStatus.vsp
      . . .
   ```

1. 파일을 저장합니다.
