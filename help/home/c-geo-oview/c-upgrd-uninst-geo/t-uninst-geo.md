---
description: 데이터 워크벤치를 제거하는 절차. 지리적 위치.
title: Data Workbench Geography 제거
uuid: 038b2dfb-4db2-42c6-85c3-bc5d776e7736
exl-id: e3898423-3b28-4786-834a-1d1ff9deb7c6
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 4%

---

# Data Workbench Geography 제거{#uninstalling-data-workbench-geography}

데이터 워크벤치를 제거하는 절차. 지리적 위치.

>[!NOTE]
>
>데이터 워크벤치 [!DNL Geography]을(를) 사용하는 프로필이 데이터 워크벤치 서버 클러스터에서 실행 중인 경우 클러스터의 마스터 데이터 워크벤치 서버에서 [!DNL Geography] 프로필을 제거합니다.

1. 데이터 워크벤치 [!DNL Geography]을(를) 사용하고 있는 각 프로필에 대해 [!DNL profile.cfg] 파일을 업데이트하려면 다음 단계를 따르십시오.

   1.  [!DNL Profile Manager].
   1. [!DNL profile.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 을 클릭합니다. 이 파일의 확인 표시는 [!DNL User] 열에 표시됩니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. [!DNL profile.cfg] 창이 나타납니다.

   1. [!DNL profile.cfg] 창의 [!DNL Directories] 벡터에서 [!DNL Geography] 프로필 항목을 삭제합니다.

   1. 데이터 서비스를 사용하고 있는 경우 [!DNL Directories] 벡터에서 [!DNL IP Geo-intelligence] 또는 [!DNL IP Geo-location] 프로필 항목을 삭제합니다.

   1. 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   1. [!DNL Profile Manager]에서 [!DNL User] 열의 [!DNL profile.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]***&#x200B;을 클릭합니다.

1. 데이터 워크벤치 서버 설치 디렉토리의 Profiles 폴더에서 Geography 폴더를 삭제합니다.
1. 데이터 서비스를 사용하고 있는 경우 데이터 워크벤치 서버 설치 디렉토리의 Profiles 폴더에서 IP 지역 인텔리전스 또는 IP 지역 폴더를 삭제합니다.
1. 데이터 워크벤치 서버 설치 디렉토리의 Lookups 폴더에서 Geography 폴더를 삭제합니다.
1. 데이터 서비스를 사용하고 있는 경우 데이터 워크벤치 서버 설치 디렉토리의 룩업 폴더에서 IP 지역 인텔리전스 또는 IP 지역 폴더를 삭제합니다.
1. 새 지형 이미지를 만든 경우 데이터 워크벤치 서버 설치 디렉토리의 Components 폴더에서 [!DNL Terrain Images.cfg] 파일을 삭제합니다.
