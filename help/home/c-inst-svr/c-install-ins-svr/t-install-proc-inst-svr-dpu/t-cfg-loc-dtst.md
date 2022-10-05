---
description: 기본적으로 Insight Server는 데이터 세트(temp.db)를 Insight Server 프로그램 파일과 동일한 드라이브에 기록합니다.
title: 데이터 세트 위치 구성(temp.db)
uuid: a6884cad-70ed-4bc6-853c-700d301fb178
exl-id: 6812883f-ad51-4314-8c80-e95c3fe84664
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 5%

---

# 데이터 세트 위치 구성(temp.db){#configuring-the-location-of-the-dataset-temp-db}

{{eol}}

기본적으로 Insight Server는 데이터 세트(temp.db)를 Insight Server 프로그램 파일과 동일한 드라이브에 기록합니다.

예를 들어 [!DNL Insight Server] 드라이브 C에서는 데이터 세트를 C 드라이브에 씁니다.

원한다면 [!DNL Insight Server] 데이터 세트를 다른 드라이브에서 유지 관리하거나 수집할 데이터의 양이 여러 드라이브를 사용해야 하는 경우 [!DNL Disk Files.cfg] 파일을 사용하여 원하는 위치를 지정할 수 있습니다. [!DNL Insight Server] 쓰기 [!DNL temp.db] 파일.

**temp.db의 위치를 구성하려면**

1. 로 이동합니다 [!DNL Components] 설치한 디렉토리의 폴더 [!DNL Insight Server].

   예: [!DNL C:\Adobe\Server\Components]

1. 를 엽니다. [!DNL Disk Files.cfg] 메모장과 같은 텍스트 편집기에 있는 파일입니다.

   기본적으로 이 파일에는 다음과 같이 디스크 파일 구조의 단일 항목이 포함되어 있습니다.

   ```
   component = DiskSpaceManagerComponent:
     Disk Files = vector: 1 items
      0 = string: Temp\\temp.db
     Detect Disk Corruption = bool: true
   ```

1. 위치를 변경하려면 [!DNL temp.db]디스크 파일 정의를 수정합니다. 다음 예에서는 구성을 편집하여 [!DNL temp.db] C, D 및 E 드라이브에 있는 파일:

   ```
   component = DiskSpaceManagerComponent:
     Disk Files = vector: 3 items
       0 = string: C:\\Temp\\temp.db
       1 = string: D:\\Temp\\temp.db
       2 = string: E:\\Temp\\temp.db
     Detect Disk Corruption = bool: true
   ```

   >[!NOTE]
   >
   >위의 파일 이름에 이중 백슬래시를 사용하십시오. in [!DNL Insight Server] 구성 파일에서 백슬래시 문자는 이스케이프 문자입니다. 텍스트에 특수 제어 시퀀스(예: 탭 문자의 경우 \t)를 표시하는 데 사용됩니다. 실제 백슬래시 문자를 나타내려면 백슬래시를 두 번 입력해야 합니다(예: \\). 이는 메모장과 같은 텍스트 편집기에서 구성 파일을 편집할 때만 적용됩니다.
