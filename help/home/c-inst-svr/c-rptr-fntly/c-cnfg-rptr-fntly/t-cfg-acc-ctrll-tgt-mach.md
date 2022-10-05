---
description: Insight Server 복제 서비스를 실행하는 Insight Server Target 시스템은 이 반복 서버에서 로그 파일을 읽을 수 있어야 합니다.
title: Target 컴퓨터에 대한 액세스 제어 구성
uuid: 35e032cf-6c1d-4348-88ce-4f4a6a30b16f
exl-id: 2d0b554a-30e9-4344-9aec-a68fd5f57304
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 6%

---

# Target 컴퓨터에 대한 액세스 제어 구성{#configuring-access-control-for-target-machines}

{{eol}}

Insight Server 복제 서비스를 실행하는 Insight Server Target 시스템은 이 반복 서버에서 로그 파일을 읽을 수 있어야 합니다.

대상 컴퓨터에 대한 액세스 권한은 [!DNL Access Control.cfg] 파일.

**Target별 액세스를 위한 액세스 제어를 구성하려면 [!DNL Insight Server] 머신**

1. 로 이동합니다 [!DNL Access Control] 반복 기능을 설치한 디렉토리의 폴더

   예: [!DNL D:\Adobe\Repeater\Access Control]

1. 열기 [!DNL Access Control.cfg] ( 메모장과 같은 텍스트 편집기)
1. 에 대한 액세스 그룹 만들기 [!DNL Insight Server] 이 반복 서버의 로그 파일에 액세스해야 하는 컴퓨터 이 액세스 그룹에 &quot;복제 Target&quot;과 같은 이름을 지정합니다.

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
   1. 읽기 전용 액세스 섹션에서 복제 대상이 액세스할 이벤트 데이터의 위치를 지정합니다. 경로 사양(/)에 슬래시를 사용합니다. 기본 위치는 입니다. [!DNL Logs] Repeater 컴퓨터의 폴더(/Logs/)를 참조하십시오.
   1. 삽입한 위치 수를 반영하도록 읽기 전용 액세스 벡터의 항목 수를 업데이트합니다.

1. 새 액세스 그룹의 추가를 반영하도록 파일의 상단에 있는 액세스 제어 그룹 벡터의 액세스 그룹 수를 업데이트합니다.

   ```
   Access Control Groups = vector: n items
   ```

1. 파일을 저장합니다.
