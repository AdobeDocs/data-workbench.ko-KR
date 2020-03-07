---
description: 데이터 워크벤치 제거 단계지리적 위치를 참조하십시오.
solution: Analytics
title: 데이터 워크벤치 지역 제거
topic: Data workbench
uuid: 038b2dfb-4db2-42c6-85c3-bc5d776e7736
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 워크벤치 지역 제거{#uninstalling-data-workbench-geography}

데이터 워크벤치 제거 단계지리적 위치를 참조하십시오.

>[!NOTE]
>
>데이터 워크벤치를 사용하는 프로파일이 데이터 워크벤치 서버 클러스터에서 실행 [!DNL Geography] 중인 경우 클러스터의 마스터 데이터 워크벤치 서버에서 [!DNL Geography] 프로파일을 제거합니다.

1. 데이터 워크벤치를 사용하고 있는 각 프로필에 대한 [!DNL profile.cfg] 파일을 업데이트하려면 다음 단계를 [!DNL Geography]사용합니다.

   1.  [!DNL Profile Manager].
   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 [!DNL profile.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. 창이 [!DNL profile.cfg] 나타납니다.

   1. 창의 [!DNL profile.cfg] 벡터에서 [!DNL Geography] 프로필 항목을 삭제합니다 [!DNL Directories] .

   1. 데이터 서비스를 사용하고 있는 경우 [!DNL IP Geo-intelligence] 벡터에서 또는 [!DNL IP Geo-location] [!DNL Directories] 프로필 항목을 삭제합니다.

   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 [!DNL Profile Manager]열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL profile.cfg] > [!DNL User] &lt; **[!UICONTROL Save to]** > *을 클릭합니다&#x200B;**[!UICONTROL profile name]***.

1. 데이터 워크벤치 서버 설치 디렉토리의 Profiles 폴더에서 Geography 폴더를 삭제합니다.
1. 데이터 서비스를 사용하고 있는 경우 데이터 워크벤치 서버 설치 디렉토리의 프로필 폴더에서 IP 지리 정보 또는 IP 지역 폴더를 삭제합니다.
1. 데이터 워크벤치 서버 설치 디렉토리의 조회 폴더에서 지역 폴더를 삭제합니다.
1. 데이터 서비스를 사용하고 있는 경우 데이터 워크벤치 서버 설치 디렉토리의 룩업 폴더에서 IP 지역 인텔리전스 또는 IP 지역 폴더를 삭제합니다.
1. 새 지형 이미지를 만든 경우 데이터 워크벤치 서버 설치 디렉토리의 구성 요소 폴더에서 [!DNL Terrain Images.cfg] 파일을 삭제합니다.
