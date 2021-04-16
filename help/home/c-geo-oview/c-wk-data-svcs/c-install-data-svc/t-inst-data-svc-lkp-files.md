---
description: IP 지리 정보 또는 IP 지역 조회 파일을 설치하는 절차.
title: 데이터 서비스 조회 파일 설치
uuid: a3fe8a14-2c74-4105-bc5b-2298f0f4b61e
exl-id: b19904f4-ead0-4bed-a79f-864c78bc0e1d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 6%

---

# 데이터 서비스 조회 파일 설치{#installing-the-data-service-lookup-files}

IP 지리 정보 또는 IP 지역 조회 파일을 설치하는 절차.

데이터 서비스 프로필과 함께 제공되는 조회 파일(Lookups\*profile name*\*data file name*)은 IP 주소를 기반으로 지리적으로 관련된 데이터를 포함하는 이진 파일( [!DNL .bin])입니다. 이 파일을 정기적으로 교체하여 가장 최근의 지리적 데이터가 있는지 확인해야 합니다. [데이터 서비스 파일 업데이트](../../../../home/c-geo-oview/c-wk-data-svcs/c-updt-data-svc-files.md#concept-2b3d11e4cb814fc09add5de58a87045c)를 참조하십시오.

**IP 지리 정보 또는 IP 지역 조회 파일을 설치하려면**

>[!NOTE]
>
>모든 [!DNL IP Geo-location] 또는 [!DNL IP Geo-intelligence] 데이터 파일은 데이터 워크벤치 서버의 사용 가능한 실제 메모리에 들어가야 합니다.

1. Adobe에서 받은 [!DNL .zip] 파일에서 조회 폴더를 엽니다.
1. IP 지리 정보 또는 IP 지리적 위치 폴더를 데이터 워크벤치 서버 설치 디렉토리의 룩업 폴더에 복사합니다. (을(를) ...로 끝내려는 경우..\Lookups\IP Geo-intelligence or a ..\Lookups\IP Geo-location folder on your data workbench server as shown in the following example을 참조하십시오. 조회 폴더 내의 다른 폴더 이름은 표시된 폴더 이름과 다를 수 있습니다.

   ![단계 정보](assets/Geo_installLookups_dirIP.png)

   >[!NOTE]
   >
   >Adobe은 업데이트된 [!DNL IP Geo-intelligence] 또는 [!DNL IP Geo-location] 조회 파일을 포함하는 파일을 정기적으로 전송합니다. 이러한 파일을 받으면 Adobe의 지시에 따라 데이터 워크벤치 서버에 파일을 로드해야 합니다. 자세한 내용은 다음 섹션을 참조하십시오.
