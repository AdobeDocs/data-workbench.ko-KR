---
description: 데이터 서비스 프로필(IP 지역 인텔리전스 및 IP 지역)은 Adobe 애플리케이션에 추가 기능을 제공하는 내부 프로필입니다.
title: 데이터 서비스 프로필 설치
uuid: 1c03d0cd-7eaa-4e48-bbff-8bfad8fed9e9
exl-id: 51d080bb-f874-426c-91ea-3912ffd38419
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 1%

---

# 데이터 서비스 프로필 설치{#installing-the-data-service-profile}

데이터 서비스 프로필(IP 지역 인텔리전스 및 IP 지역)은 Adobe 애플리케이션에 추가 기능을 제공하는 내부 프로필입니다.

Adobe이 제공하는 다른 모든 내부 프로필과 마찬가지로 이러한 프로필은 변경하지 않아야 합니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 수행해야 합니다.

데이터 서비스 프로필에는 Data Workbench 서버에 설치할 파일이 포함되어 있습니다.

* **프로필\*프로필 이름&#x200B;*\Dataset\Log Processing\Traffic\IP.cfg:** 로그 처리에서 변형으로 전달할 c-ip 필드를 나열합니다.
* **프로필\*프로필 이름&#x200B;*\Dataset\Transformation\Geography\IPLookup.cfg:** 제공된 IP 지역 인텔리전스 또는 IP 지역 위치 조회 파일을 사용하여 여러 지리적 데이터 필드를 생성하는 IP 조회 변환을 정의합니다.

변형 데이터 집합에 파일이 포함된 것에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.

또한 각 데이터 서비스 프로필은 [!DNL IP Coordinates.layer] 이라는 요소 점 계층 파일을 제공합니다. 이 레이어 파일을 사용하면 IP 주소를 사용하여 전 세계 데이터 세트에 있는 위치를 동적으로 매핑할 수 있습니다. 설치 후 계층은 Data Workbench 서버 설치 디렉토리 내의 Profiles\*data service name*\Map 폴더에 저장됩니다.

[!DNL IP Coordinates.layer] 파일은 [!DNL Geography] 프로필과 함께 제공되는 [!DNL Coordinates.cfg] 파일에 정의되어 Dataset\Transformation\Geography folder에 있는 좌표 차원을 참조합니다. 데이터 세트에 정의된 좌표 차원의 각 요소는 해당 요소에 포함된 위도와 경도 정보를 사용하여 전방에 매핑됩니다. 동적 점을 사용하는 요소 점 레이어에 대한 자세한 내용은 [동적 점을 사용하여 요소 점 레이어 정의](../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3)를 참조하십시오.

>[!NOTE]
>
>버전 5.1 이전의 IP 지리 특성 및 IP 지리적 위치 데이터 서비스를 설치한 경우 요소 점 계층 파일은 동적 점을 사용하지 않고 조회 파일을 참조합니다. 각 레이어 파일은 IP Geocodes 조회 파일과 IP Geocode 차원을 참조합니다. IP 지리 코드 조회 파일에는 IP 주소 기반 지리적 위치 및 각 지역의 위도와 경도 목록이 포함되어 있습니다. 데이터 세트에 정의된 IP 지리 코드 차원의 각 요소는 IP 지리 코드 조회 파일에서 해당 IP 지리 코드에 대해 나열된 위도와 경도를 사용하여 전방에 매핑됩니다.

레이어 파일의 이름과 참조하는 파일이 데이터 서비스마다 다릅니다.

* [!DNL IP Geocodes D.layer] 파일은 IP Geo-intelligence(Digital Envoy) 프로필과 함께 설치됩니다. 이 요소 점 계층은 [!DNL IP Geocodes D yyyymmdd.txt] 조회 파일(정기적으로 업데이트해야 함)과 IP Geocode D 차원을 참조합니다.

* [!DNL IP Geocodes Q.layer] 파일은 IP 지역(Quova) 프로필과 함께 설치됩니다. 이 요소 점 계층은 [!DNL IP Geocodes Q yyyymmdd.txt] 조회 파일(정기적으로 업데이트해야 함)과 IP Geocode Q 차원을 참조합니다.

조회 파일을 사용하는 요소 점 레이어에 대한 자세한 내용은 [조회 파일을 참조하는 요소 점 레이어 정의](../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyrs-ref-lkp-files.md#concept-c40bd0890a984112bce831b596827f0f)를 참조하십시오.

## IP Geo-intelligence 또는 IP 지리적 위치 프로필을 설치하려면 {#section-6dff402ffdcb4b31b9bcd0c40a5f7625}

>[!NOTE]
>
>다음 설치 지침은 Data Workbench를 설치하고 Data Workbench [!DNL Geography] 를 설치하는 Data Workbench 서버와 Data Workbench 서버 간의 연결을 설정했다고 가정합니다. 아직 완료하지 않았다면 *Data Workbench 사용 안내서*&#x200B;를 참조하십시오.

1. Adobe에서 받은 [!DNL .zip] 파일에서 Profiles 폴더를 엽니다.
1. Data Workbench 서버 설치 디렉토리의 Profiles 폴더에 IP Geo-intelligence 또는 IP Geo-location 폴더를 복사합니다. 당신은 결국 ...로 끝나길 원합니다.\Profiles\IP Geo-intelligence folder or a ..\Profiles\IP Geo-location on your data workbench server as shown in the following example [!DNL Profiles] 폴더 내의 다른 폴더의 이름이 표시된 폴더 이름과 다를 수 있습니다.

   ![](assets/Geo_installProfiles_dirIP.png)

1. 다음 단계를 사용하여 [!DNL IP Geo-intelligence] 또는 [!DNL IP Geo-location] 프로필을 사용할 각 프로필에 대한 [!DNL profile.cfg] 파일을 업데이트합니다.

   1.  **[!UICONTROL Profile Manager]**.
   1. [!DNL profile.cfg] 옆의 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]** 를 클릭합니다. [!DNL profile.cfg] 창이 나타납니다.

   1. [!DNL profile.cfg]창에서 **[!UICONTROL Directories]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

      새 디렉터리를 디렉터리 목록 끝에 추가하려면 목록에서 마지막 디렉터리의 번호나 이름을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]** 를 클릭합니다.

   1. 새 디렉토리의 이름을 입력합니다.[!DNL IP Geo-intelligence] 또는 [!DNL P Geo-location] 입니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. [!DNL Profile Manager]에서 [!DNL User] 열의 [!DNL profile.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]***&#x200B;를 클릭합니다.

>[!NOTE]
>
>이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe이 제공하는 내부 프로필( [!DNL IP Geo-location] 또는 [!DNL IP Geo-intelligence] 프로필 포함)에 저장하지 마십시오.
