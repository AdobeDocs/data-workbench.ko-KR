---
description: 요소 점 레이어 열에 대한 정보입니다.
title: 요소 점 조회 파일 형식
uuid: 3480b9f3-35cd-40b7-aac9-15a3e2f19c1c
exl-id: da81da9e-0567-4f3a-bc0d-ab6c5e4a23b7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 6%

---

# 요소 점 조회 파일 형식{#element-point-lookup-file-format}

{{eol}}

요소 점 레이어 열에 대한 정보입니다.

요소 점 레이어 조회 파일은 다음 세 개 이상의 열을 포함해야 합니다.

* **[!DNL Key]열:** 이 열에는 일반 키 데이터가 포함되어야 합니다. 이 경우 Data Workbench 서버가 조회 파일의 데이터를 데이터 집합에 있는 데이터에 연결할 수 있습니다. 다음 [!DNL Key] 열은 조회 파일의 첫 번째 열이어야 합니다. 이 열의 각 행은 차원의 요소를 식별합니다.

* **[!DNL Longitude]열:** 이 열에는 [!DNL Key] 열.

* **[!DNL Latitude]열:** 이 열에는 [!DNL Key] 열.

* **[!DNL Name]열:** (선택 사항). 각 데이터 포인트에 대해 맵에 표시할 이름을 지정하려면 [!DNL Name] 조회 파일의 열.

의 각 행 [!DNL Zip Points.txt] 조회 파일에는 첫 번째 열에 ZIP 코드가 들어 있고 그 뒤에는 경도, 위도 및 연관된 도시 이름이 옵니다.

```
tude, and associated city name.
ZIP_CODE LATITUDE LONGITUDE NAME
00210 +43.005895 -071.013202 PORTSMOUTH, NH
00211 +43.005895 -071.013202 PORTSMOUTH, NH
...
```
