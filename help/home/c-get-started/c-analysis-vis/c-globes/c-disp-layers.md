---
description: 지리적 위치 프로필에는 이미지 레이어 및 파일 컬렉션이 저장됩니다.
title: 레이어 표시
uuid: ebc7025d-e619-43dd-88da-7452ada3226b
exl-id: 12ec913f-c7e5-49b5-8792-db0881cb5cfe
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# 레이어 표시{#display-layers}

지리적 위치 프로필에는 이미지 레이어 및 파일 컬렉션이 저장됩니다.

글로브를 표시할 때 특정 분석 작업에 표시할 사용 가능한 레이어 중 하나를 선택할 수 있습니다.

* **블루 마블 2km:** 이 레이어는 지구를 표시합니다. 이 레이어를 선택하지 않으면 글로브가 표시되지 않습니다.
* **IP 좌표:** 이 요소 포인트 레이어는 방문자 IP 주소를 기반으로 데이터 세트에 있는 위치의 위도와 경도를 표시합니다.
* **우편 번호:** 이 레이어는 Adobe에서 제공하는 미국 우편 번호 목록을 기반으로 데이터 세트에 있는 위치의 위도와 경도를 표시합니다. [!DNL Zip Points.txt] 조회 파일에는 표시할 ZIP 코드, 위도 및 경도 데이터가 들어 있고, [!DNL Zip Points.layer] 파일에는 이 데이터를 지구에 표시하는 데 필요한 구성 매개 변수가 포함되어 있습니다. 이 두 파일은 모두 Profiles\Geography\Maps folder within the Data Workbench server installation directory폴더에 저장됩니다.

* ***다른 사용 가능한 레이어 이름:*** 각 레이어 이름은 Insight Server 설치 디렉토리 내의 Profiles\Geography\Maps folder, Profiles\IP Geo-location\Maps 폴더 또는 Profiles\IP Geo-intelligence\Maps 폴더에 저장된  [!DNL .layer] 파일을 나타냅니다.

>[!NOTE]
>
>IP 지리적 위치 또는 IP 지리 정보 프로필을 사용하려면 각각 IP 지리적 위치 또는 IP 지리 정보 데이터 서비스에 가입해야 합니다.

레이어의 표시 순서를 제어하려면 [!DNL order.txt] 파일을 사용할 수 있습니다. [Order.txt 파일을 사용하여 메뉴 사용자 지정](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999)을 참조하십시오.

**지구에서의 레이어 전환**

* 시각화 내에서 마우스 오른쪽 단추를 클릭하고 원하는 레이어 이름을 클릭합니다. 레이어 왼쪽에 X를 입력하면 레이어가 표시됩니다.
