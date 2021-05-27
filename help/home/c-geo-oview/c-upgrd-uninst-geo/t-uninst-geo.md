---
description: Data workbenchGeography 제거 절차.
title: Data Workbench Geography 제거
uuid: 038b2dfb-4db2-42c6-85c3-bc5d776e7736
exl-id: e3898423-3b28-4786-834a-1d1ff9deb7c6
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 4%

---

# Data Workbench Geography 제거{#uninstalling-data-workbench-geography}

Data workbenchGeography 제거 절차.

>[!NOTE]
>
>Data Workbench [!DNL Geography] 을 사용하는 프로필이 Data Workbench 서버 클러스터에서 실행 중인 경우 클러스터의 마스터 Data Workbench 서버에서 [!DNL Geography] 프로필을 제거합니다.

1. 다음 단계를 사용하여 Data Workbench [!DNL Geography] 를 사용하는 각 프로필에 대해 [!DNL profile.cfg] 파일을 업데이트합니다.

   1.  [!DNL Profile Manager].
   1. [!DNL profile.cfg] 옆의 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]** 를 클릭합니다. [!DNL profile.cfg] 창이 나타납니다.

   1. [!DNL profile.cfg] 창의 [!DNL Directories] 벡터에서 [!DNL Geography] 프로필 항목을 삭제합니다.

   1. 데이터 서비스를 사용하는 경우 [!DNL Directories] 벡터에서 [!DNL IP Geo-intelligence] 또는 [!DNL IP Geo-location] 프로필 항목을 삭제합니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. [!DNL Profile Manager]에서 [!DNL User] 열의 [!DNL profile.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]***&#x200B;를 클릭합니다.

1. Data Workbench 서버 설치 디렉토리의 Profiles 폴더에서 Geography 폴더를 삭제합니다.
1. 데이터 서비스를 사용하는 경우 Data Workbench 서버 설치 디렉토리의 Profiles 폴더에서 IP 지리 인텔리전스 또는 IP 위치 폴더를 삭제합니다.
1. Data Workbench 서버 설치 디렉토리의 조회 폴더에서 Geography 폴더를 삭제합니다.
1. 데이터 서비스를 사용하는 경우 Data Workbench 서버 설치 디렉토리의 조회 폴더에서 IP Geo-intelligence 또는 IP Geo-location 폴더를 삭제합니다.
1. 새 지형 이미지를 만든 경우 Data Workbench 서버 설치 디렉토리의 구성 요소 폴더에서 [!DNL Terrain Images.cfg] 파일을 삭제합니다.
