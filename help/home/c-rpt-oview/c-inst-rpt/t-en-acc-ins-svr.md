---
description: 데이터 워크벤치 서버에 연결하려면 보고서 서버에 해당 서버에 액세스할 수 있는 권한이 있어야 합니다.
solution: Analytics
title: 데이터 워크벤치 서버에 대한 액세스 활성화
topic: Data workbench
uuid: e112ac2a-34fe-40a2-9324-262f5cb1f681
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 워크벤치 서버에 대한 액세스 활성화{#enabling-access-to-the-data-workbench-server}

데이터 워크벤치 서버에 연결하려면 보고서 서버에 해당 서버에 액세스할 수 있는 권한이 있어야 합니다.

보고서 서버의 액세스 제어 파일에 보고서 서버의 일반 이름(보고서 서버의 디지털 인증서에 할당됨)을 추가하여 데이터 워크벤치 서버에 대한 액세스 권한을 부여합니다.

>[!NOTE]
>
>클러스터된 환경에서 작업할 때 동기화 문제를 방지하려면 마스터 데이터 워크벤치 서버에 액세스하도록 보고서 서버를 구성해야 합니다. 데이터 워크벤치에서는 의 [!DNL Related Servers] 메뉴 항목을 사용하여 클러스터의 서버 처리 정보를 볼 수 [!DNL Servers Manager]있습니다. 자세한 내용은 [!DNL Servers Manager]데이터 워크벤치 사용자 안내서의 관리 *인터페이스 장을 참조하십시오*.

다음 절차에서는 데이터 워크벤치 서버의 액세스 제어 파일에 보고서 서버를 수동으로 추가하는 방법에 대해 설명합니다. 이렇게 액세스 제어 파일을 업데이트하려면 데이터 워크벤치 서버가 설치된 시스템에서 파일 시스템 액세스 권한이 있어야 합니다.

데이터 워크벤치의 액세스 제어 파일을 사용하여 서버의 액세스 제어 파일을 업데이트할 수도 [!DNL Server Files Manager] 있습니다. 이렇게 하려면 데이터 워크벤치 클라이언트에 서버에 대한 관리 권한이 있어야 합니다.

자세한 내용은 [!DNL Server Files Manager]데이터 워크벤치 사용자 안내서의 관리 *인터페이스 장을 참조하십시오*.

**데이터 워크벤치 서버에 대한 액세스를 구성하려면**

1. 데이터 워크벤치 서버를 설치한 디렉토리(InsightServer64.exe)의 액세스 제어 폴더로 이동합니다.

   예: [!DNL C:\Adobe\Server\Access Control]

1. 메모장과 같은 텍스트 편집기에서 [!DNL Access Control.cfg] 엽니다.
1. 다음 파일 조각에서 강조 표시된 대로 [!DNL Report Server AccessGroup] [!DNL Report Server’s] 이 그룹에 공통 이름을 추가하고 이 이름을 추가합니다. (일반적인 이름을 [!DNL Report Server’s] 디지털 인증서에 나타나는 대로 입력합니다.)

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
