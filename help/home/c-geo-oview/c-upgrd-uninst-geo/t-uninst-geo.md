---
description: Data workbenchGeography 제거 절차.
title: Data Workbench Geography 제거
uuid: 038b2dfb-4db2-42c6-85c3-bc5d776e7736
exl-id: e3898423-3b28-4786-834a-1d1ff9deb7c6
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 4%

---

# Data Workbench Geography 제거{#uninstalling-data-workbench-geography}

{{eol}}

Data workbenchGeography 제거 절차.

>[!NOTE]
>
>Data Workbench를 사용하는 프로필인 경우 [!DNL Geography] data workbench 서버 클러스터에서 실행 중인 경우 제거 [!DNL Geography] 클러스터의 마스터 data workbench 서버에서 프로필을 생성합니다.

1. 다음 단계를 사용하여 를 업데이트합니다 [!DNL profile.cfg] data workbench를 사용하고 있는 각 프로필에 대한 파일 [!DNL Geography].

   1.  [!DNL Profile Manager].
   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL profile.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. 다음 [!DNL profile.cfg] 창이 나타납니다.

   1. 에서 [!DNL profile.cfg] 창, 삭제 [!DNL Geography] 프로필 항목 [!DNL Directories] 벡터입니다.

   1. 데이터 서비스를 사용 중이라면 [!DNL IP Geo-intelligence] 또는 [!DNL IP Geo-location] 프로필 항목 [!DNL Directories] 벡터입니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Profile Manager]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL profile.cfg] 에서 [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

1. Data Workbench 서버 설치 디렉토리의 Profiles 폴더에서 Geography 폴더를 삭제합니다.
1. 데이터 서비스를 사용하는 경우 Data Workbench 서버 설치 디렉토리의 Profiles 폴더에서 IP 지리 인텔리전스 또는 IP 위치 폴더를 삭제합니다.
1. Data Workbench 서버 설치 디렉토리의 조회 폴더에서 Geography 폴더를 삭제합니다.
1. 데이터 서비스를 사용하는 경우 Data Workbench 서버 설치 디렉토리의 조회 폴더에서 IP Geo-intelligence 또는 IP Geo-location 폴더를 삭제합니다.
1. 새 지형 이미지를 만든 경우 [!DNL Terrain Images.cfg] data workbench 서버 설치 디렉토리의 구성 요소 폴더에서 을 클릭합니다.
