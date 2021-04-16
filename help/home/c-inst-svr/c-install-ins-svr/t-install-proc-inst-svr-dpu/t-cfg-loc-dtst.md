---
description: 기본적으로 Insight Server는 데이터 세트(temp.db)를 Insight Server 프로그램 파일과 동일한 드라이브에 기록합니다.
title: 데이터 세트 위치 구성(temp.db)
uuid: a6884cad-70ed-4bc6-853c-700d301fb178
exl-id: 6812883f-ad51-4314-8c80-e95c3fe84664
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 5%

---

# 데이터 세트 위치 구성(temp.db){#configuring-the-location-of-the-dataset-temp-db}

기본적으로 Insight Server는 데이터 세트(temp.db)를 Insight Server 프로그램 파일과 동일한 드라이브에 기록합니다.

예를 들어 드라이브 C에 [!DNL Insight Server]을 설치한 경우 데이터 세트를 작성하여 C 드라이브에 기록합니다.

[!DNL Insight Server]이(가) 다른 드라이브에 있는 데이터 세트를 유지하려는 경우 또는 수집할 데이터의 양이 여러 드라이브를 사용해야 하는 경우 [!DNL Disk Files.cfg] 파일을 업데이트하여 [!DNL Insight Server] 파일이 [!DNL temp.db] 파일을 쓸 위치를 지정해야 합니다.

**temp.db의 위치를 구성하려면**

1. [!DNL Insight Server]을(를) 설치한 디렉토리의 [!DNL Components] 폴더로 이동합니다.

   예: [!DNL C:\Adobe\Server\Components]

1. 메모장과 같은 텍스트 편집기에서 [!DNL Disk Files.cfg] 파일을 엽니다.

   기본적으로 이 파일은 아래와 같이 디스크 파일 구조의 단일 항목을 포함합니다.

   ```
   component = DiskSpaceManagerComponent:
     Disk Files = vector: 1 items
      0 = string: Temp\\temp.db
     Detect Disk Corruption = bool: true
   ```

1. [!DNL temp.db]의 위치를 변경하려면 디스크 파일 정의를 수정합니다. 다음 예제에서는 구성을 편집하여 드라이브 C, D 및 E에 [!DNL temp.db] 파일을 확장하는 방법을 보여 줍니다.

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
   >위의 파일 이름에 이중 백슬래시를 사용합니다. [!DNL Insight Server] 구성 파일에서 백슬래시 문자는 이스케이프 문자입니다. 텍스트의 특수 컨트롤 시퀀스(예: 탭 문자의 경우 \t)를 표현하는 데 사용됩니다. 실제 백슬래시 문자를 나타내려면 이스케이프 함수를 재정의하려면 백슬래시를 두 번 입력해야 합니다(예: \\). 이는 메모장과 같은 텍스트 편집기에서 구성 파일을 편집할 때만 적용됩니다.
