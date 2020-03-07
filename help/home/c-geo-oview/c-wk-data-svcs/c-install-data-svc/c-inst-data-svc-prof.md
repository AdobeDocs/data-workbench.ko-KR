---
description: 데이터 서비스 프로필(IP 지리 정보 및 IP 지역)은 Adobe 애플리케이션에 추가 기능을 제공하는 내부 프로필입니다.
solution: Analytics
title: 데이터 서비스 프로필 설치
topic: Data workbench
uuid: 1c03d0cd-7eaa-4e48-bbff-8bfad8fed9e9
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 서비스 프로필 설치{#installing-the-data-service-profile}

데이터 서비스 프로필(IP 지리 정보 및 IP 지역)은 Adobe 애플리케이션에 추가 기능을 제공하는 내부 프로필입니다.

Adobe에서 제공하는 기타 모든 내부 프로필과 마찬가지로 이러한 프로필도 변경하면 안 됩니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 수행해야 합니다.

데이터 서비스 프로필에는 데이터 워크벤치 서버에 설치할 파일이 포함되어 있습니다.

* **프로필\*프로필 이름&#x200B;*\Dataset\Log Processing\Traffic\IP.cfg:** 로그 처리에서 변환으로 전달할 c-ip 필드를 나열합니다.
* **Profiles\*프로필 이름&#x200B;*\Dataset\Transformation\Geography\IPLookup.cfg:** 제공된 IP 지역 인텔리전스 또는 IP 지역 조회 파일을 사용하여 여러 지역 데이터 필드를 생성하는 IPLookup 변환을 정의합니다.

변형 데이터 세트에 대한 자세한 내용은 데이터 세트 구성 *안내서를 참조하십시오*.

또한 각 데이터 서비스 프로필은 이름이 [!DNL IP Coordinates.layer]지정된 요소 포인트 레이어 파일을 제공합니다. 이 레이어 파일을 사용하면 IP 주소를 사용하여 지구 상의 데이터 세트에 있는 위치를 동적으로 매핑할 수 있습니다. 설치 후 레이어는 데이터 워크벤치 서버 설치 디렉토리 내의 Profiles\*data service name*\Maps 폴더에 저장됩니다.

이 [!DNL IP Coordinates.layer] 파일은 프로파일과 함께 제공되어 Dataset\Transformation\Geography folder폴더에 있는 [!DNL Coordinates.cfg] [!DNL Geography] 파일에 정의된 좌표 차원을 참조합니다. 데이터 세트에 정의된 좌표 차원의 각 요소는 해당 요소에 포함된 위도 및 경도 정보를 사용하여 지구 전체에 매핑됩니다. 다이내믹한 점을 사용하는 요소 포인트 레이어에 대한 자세한 내용은 다이내믹한 점을 [사용하여 요소 점 레이어 정의를 참조하십시오](../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3).

>[!NOTE]
>
>버전 5.1 이전에 IP 지역 인텔리전스 및 IP 지역 데이터 서비스를 설치한 경우, 요소 포인트 레이어 파일은 다이내믹 포인트를 사용하는 대신 조회 파일을 참조합니다. 각 레이어 파일은 IP 지리 코드 조회 파일과 IP 지리 코드 차원을 참조합니다. IP 지리 코드 조회 파일에는 IP 지리 코드 목록(IP 주소를 기반으로 한 지리적 위치)과 각 지역의 위도 및 경도 목록이 포함되어 있습니다. 데이터 세트에 정의된 IP 지리 코드 차원의 각 요소는 IP 지리 코드 조회 파일에서 해당 IP 지리 코드에 대해 나열된 위도 및 경도를 사용하여 지구 전체에 매핑됩니다.

레이어 파일의 이름과 참조하는 파일은 각 데이터 서비스에 대해 다릅니다.

* 이 [!DNL IP Geocodes D.layer] 파일은 IP 지리 정보(Digital Envoy) 프로필과 함께 설치됩니다. 이 요소 포인트 레이어는 주기적으로 업데이트해야 하는 [!DNL IP Geocodes D yyyymmdd.txt] 조회 파일과 IP 지리 코드 D 차원을 참조합니다.

* 이 [!DNL IP Geocodes Q.layer] 파일은 IP 지역(Quova) 프로필과 함께 설치됩니다. 이 요소 포인트 레이어는 주기적으로 업데이트해야 하는 [!DNL IP Geocodes Q yyyymmdd.txt] 조회 파일과 IP 지리 코드 Q 차원을 참조합니다.

조회 파일을 사용하는 요소 포인트 레이어에 대한 자세한 내용은 조회 [파일을 참조하는 요소 포인트 레이어 정의를 참조하십시오](../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyrs-ref-lkp-files.md#concept-c40bd0890a984112bce831b596827f0f).

## IP 지리 정보 또는 IP 지리 위치 프로필을 설치하려면 {#section-6dff402ffdcb4b31b9bcd0c40a5f7625}

>[!NOTE]
>
>다음 설치 지침은 데이터 워크벤치를 설치하고 데이터 워크벤치를 설치하는 데이터 워크벤치와 데이터 워크벤치 서버 사이에 연결을 설정했다고 가정합니다 [!DNL Geography]. 이렇게 하지 않은 경우 데이터 워크벤치 *사용 안내서를 참조하십시오*.

1. Adobe로부터 받은 [!DNL .zip] 파일에서 Profiles 폴더를 엽니다.
1. IP 지리 정보 또는 IP 지리 위치 폴더를 데이터 워크벤치 서버 설치 디렉토리의 프로필 폴더에 복사합니다. 결국..\Profiles\IP Geo-intelligence folder or a ...\Profiles\IP Geo-location on your data workbench server as shown in the following example. 폴더 내의 다른 폴더 이름은 [!DNL Profiles] 표시된 폴더 이름과 다를 수 있습니다.

   ![](assets/Geo_installProfiles_dirIP.png)

1. 다음 단계에 따라 [!DNL profile.cfg] 또는 [!DNL IP Geo-intelligence] [!DNL IP Geo-location] 프로파일을 사용할 각 프로필에 대한 파일을 업데이트합니다.

   1.  **[!UICONTROL Profile Manager]**.
   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 [!DNL profile.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. 창이 [!DNL profile.cfg] 나타납니다.

   1. 창에서 [!DNL profile.cfg]마우스 오른쪽 단추를 **[!UICONTROL Directories]** 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

      디렉토리 목록 끝에 새 디렉토리를 추가하려면 목록에서 마지막 디렉토리의 번호나 이름을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

   1. 새 디렉토리의 이름을 입력합니다. [!DNL IP Geo-intelligence] 또는 [!DNL P Geo-location]I.

   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 [!DNL Profile Manager]열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL profile.cfg] > [!DNL User] &lt; **[!UICONTROL Save to]** > *을 클릭합니다&#x200B;**[!UICONTROL profile name]***.

>[!NOTE]
>
>이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필( [!DNL IP Geo-location] 또는 [!DNL IP Geo-intelligence] 프로필 포함)에 저장하지 마십시오.

