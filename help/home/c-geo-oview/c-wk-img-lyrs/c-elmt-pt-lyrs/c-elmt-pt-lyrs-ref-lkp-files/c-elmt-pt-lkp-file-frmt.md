---
description: 요소 포인트 레이어 열에 대한 정보입니다.
solution: Analytics
title: 요소 포인트 조회 파일 형식
topic: Data workbench
uuid: 3480b9f3-35cd-40b7-aac9-15a3e2f19c1c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 요소 포인트 조회 파일 형식{#element-point-lookup-file-format}

요소 포인트 레이어 열에 대한 정보입니다.

요소 포인트 레이어 조회 파일은 다음 세 개 이상의 열을 포함해야 합니다.

* **[!DNL Key]열:**이 열에는 데이터 워크벤치 서버가 조회 파일의 데이터를 데이터 세트에 있는 데이터에 연결할 수 있는 공통 키 데이터가 포함되어야 합니다. 이[!DNL Key]열은 조회 파일의 첫 번째 열이어야 합니다. 이 열의 각 행은 차원의 요소를 식별합니다.

* **[!DNL Longitude]열:**이 열에는[!DNL Key]열의 각 데이터 포인트에 대한 경도가 포함되어야 합니다.

* **[!DNL Latitude]열:**이 열에는[!DNL Key]열의 각 데이터 포인트에 대한 위도가 포함되어야 합니다.

* **[!DNL Name]열:**(선택 사항). 각 데이터 포인트에 대해 맵에 표시할 이름을 지정하려면 조회 파일에[!DNL Name]열을 포함할 수 있습니다.

조회 파일의 각 행은 첫 번째 열에 ZIP 코드가 들어 있고 그 뒤에 경도, 위도 및 연관된 도시 이름이 있습니다. [!DNL Zip Points.txt]

```
tude, and associated city name.
ZIP_CODE LATITUDE LONGITUDE NAME
00210 +43.005895 -071.013202 PORTSMOUTH, NH
00211 +43.005895 -071.013202 PORTSMOUTH, NH
...
```
