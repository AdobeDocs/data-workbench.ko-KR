---
description: Insight Server Replication Service를 실행하는 Target Insight Server 시스템은 이 반복 서버에서 로그 파일을 읽을 수 있어야 합니다.
solution: Insight
title: 대상 컴퓨터에 대한 액세스 제어 구성
uuid: 35e032cf-6c1d-4348-88ce-4f4a6a30b16f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 대상 컴퓨터에 대한 액세스 제어 구성{#configuring-access-control-for-target-machines}

Insight Server Replication Service를 실행하는 Target Insight Server 시스템은 이 반복 서버에서 로그 파일을 읽을 수 있어야 합니다.

대상 컴퓨터에 대한 액세스 권한은 [!DNL Access Control.cfg] 파일을 사용하여 부여됩니다.

**대상[!DNL Insight Server]시스템별 액세스에 대한 액세스 제어를 구성하려면**

1. 반복 기능을 설치한 디렉토리의 [!DNL Access Control] 폴더로 이동합니다.

   예: [!DNL D:\Adobe\Repeater\Access Control]

1. 메모장과 같은 텍스트 편집기에서 [!DNL Access Control.cfg] 엽니다.
1. 이 반복 서버의 로그 파일에 액세스해야 하는 [!DNL Insight Server] 컴퓨터의 액세스 그룹을 만듭니다. 이 액세스 그룹에 &quot;복제 대상&quot;과 같은 이름을 지정합니다.

       다음 파일 조각은 액세스 그룹이 표시되는 방식을 보여줍니다.
       
       ```
       . . .
       6 = AccessGroup:
  멤버 =     벡터:N 항목
 0     = 문자열:IP:Machine0IPAddress
     1 = 문자열:IP:Machine1IPAddress
     ...
   N     = 문자열:IP:MachineNIPAddress
 Name     = 문자열:복제 타겟
 읽기     전용 액세스 = 벡터:1개 항목
     0 = 문자열:EventDataLocation
 읽기     쓰기 액세스 = 벡터:0개 항목
     ...
      &quot;
   
   1. 멤버 섹션에서 각 시스템의 IP 주소를 지정합니다.
   1. 삽입한 컴퓨터 IP 주소 수를 반영하도록 멤버 벡터의 항목 수를 업데이트합니다.
   1. 읽기 전용 액세스 섹션에서 복제가 액세스를 대상으로 하는 이벤트 데이터의 위치를 지정합니다. 경로 사양(/)에 슬래시를 사용합니다. 기본 위치는 Repeater 컴퓨터의 [!DNL Logs] 폴더(/Logs/)입니다.
   1. 삽입한 위치의 수를 반영하도록 읽기 전용 액세스 벡터의 항목 수를 업데이트합니다.

1. 새 액세스 그룹 추가를 반영하도록 파일 맨 위에 있는 액세스 제어 그룹 벡터의 액세스 그룹 수를 업데이트합니다.

   ```
   Access Control Groups = vector: n items
   ```

1. 파일을 저장합니다.
