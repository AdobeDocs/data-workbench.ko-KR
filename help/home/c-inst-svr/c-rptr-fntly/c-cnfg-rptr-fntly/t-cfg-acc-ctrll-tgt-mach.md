---
description: Insight Server 복제 서비스를 실행하는 Insight Server Target 시스템은 이 반복 서버에서 로그 파일을 읽을 수 있어야 합니다.
title: Target 컴퓨터에 대한 액세스 제어 구성
uuid: 35e032cf-6c1d-4348-88ce-4f4a6a30b16f
exl-id: 2d0b554a-30e9-4344-9aec-a68fd5f57304
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 6%

---

# Target 컴퓨터에 대한 액세스 제어 구성{#configuring-access-control-for-target-machines}

Insight Server 복제 서비스를 실행하는 Insight Server Target 시스템은 이 반복 서버에서 로그 파일을 읽을 수 있어야 합니다.

대상 컴퓨터에 대한 액세스 권한은 [!DNL Access Control.cfg] 파일을 사용하여 부여됩니다.

**대상 컴퓨터에 의한 액세스를 위한 액세스 제어를  [!DNL Insight Server] 구성하려면**

1. 반복 기능을 설치한 디렉토리의 [!DNL Access Control] 폴더로 이동합니다.

   예: [!DNL D:\Adobe\Repeater\Access Control]

1. 메모장과 같은 텍스트 편집기에서 [!DNL Access Control.cfg] 을 엽니다.
1. 이 반복 서버의 로그 파일에 액세스해야 하는 [!DNL Insight Server] 컴퓨터에 대한 액세스 그룹을 만듭니다. 이 액세스 그룹에 &quot;복제 Target&quot;과 같은 이름을 지정합니다.

   다음 파일 조각은 액세스 그룹이 어떻게 표시되어야 하는지를 보여줍니다.

   ```
   . . . 
     6 = AccessGroup: 
       Members = vector: N items 
         0 = string: IP:Machine0IPAddress 
         1 = string: IP:Machine1IPAddress 
   . . . 
         N = string: IP:MachineNIPAddress 
       Name = string: Replication Targets 
       Read-Only Access = vector: 1 items 
         0 = string: EventDataLocation 
       Read-Write Access = vector: 0 items 
   . . .
   ```

   1. 멤버 섹션에서 각 시스템의 IP 주소를 지정합니다.
   1. 삽입한 컴퓨터 IP 주소 수를 반영하도록 멤버 벡터에 대한 항목 수를 업데이트합니다.
   1. 읽기 전용 액세스 섹션에서 복제 대상이 액세스할 이벤트 데이터의 위치를 지정합니다. 경로 사양(/)에 슬래시를 사용합니다. 기본 위치는 반복 시스템(/Logs/)의 [!DNL Logs] 폴더입니다.
   1. 삽입한 위치 수를 반영하도록 읽기 전용 액세스 벡터의 항목 수를 업데이트합니다.

1. 새 액세스 그룹의 추가를 반영하도록 파일의 상단에 있는 액세스 제어 그룹 벡터의 액세스 그룹 수를 업데이트합니다.

   ```
   Access Control Groups = vector: n items
   ```

1. 파일을 저장합니다.
