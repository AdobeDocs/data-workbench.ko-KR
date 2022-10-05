---
description: 데이터 서비스를 구독하는 경우 Adobe에서 제공한 데이터 서비스 파일을 정기적으로 업데이트해야 합니다.
title: 데이터 서비스 파일 업데이트
uuid: 8c14be34-fde3-4c4c-9c22-739863317d6e
exl-id: bb92d40c-cc8d-4ecf-bd48-ed962fd5d73b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 1%

---

# 데이터 서비스 파일 업데이트{#updating-data-service-files}

{{eol}}

데이터 서비스를 구독하는 경우 Adobe에서 제공한 데이터 서비스 파일을 정기적으로 업데이트해야 합니다.

이렇게 하려면 Data Workbench 서버의 파일에 액세스할 수 있어야 합니다.

로드하려면 [!DNL IP Geo-location] 또는 [!DNL IP Geo-intelligence] 데이터 파일에서 다음 절차를 완료해야 합니다.

## 데이터 파일 바꾸기 {#section-2b53c2951ae04c6fa8b3bdf080469ff6}

1. Data Workbench에서 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판 그림을 클릭하여 열기 [!DNL Servers Manager] 작업 공간.

1. 내 [!DNL Servers Manager] 창에서 파일을 로드할 data workbench 서버의 아이콘을 마우스 오른쪽 단추로 클릭하고 를 클릭합니다. **[!UICONTROL Server Files]**.

1. 에서 [!DNL Server Files Manager]를 마우스 오른쪽 단추로 클릭합니다. **[!UICONTROL Temp]** 열 **[!UICONTROL Lookups\IP Geo-location]** 또는 **[!UICONTROL Lookups\IP Geo-intelligence]** 을(를) 클릭합니다. **[!UICONTROL Open]** > *&lt;**[!UICONTROL folder]**>*.

1. 를 복사합니다. [!DNL .bin] 조회\IP 지리적 위치 또는 조회\IP Geo-intelligence 폴더 창에 Adobe이 제공한 데이터 파일입니다.
1. 파일을 마우스 오른쪽 단추로 클릭하여 Data Workbench 서버 시스템에 저장합니다 [!DNL Temp] 데이터 파일에 대한 열 및 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

   클러스터를 실행 중인 경우 클러스터의 마스터 Data Workbench 서버에 파일을 업로드합니다.

## IP 조회 변환 업데이트 {#section-a8b99afe3eb04afabe88e15bd465f935}

1. 에서 [!DNL Profile Manager]를 클릭합니다. **[!UICONTROL Dataset]**, **[!UICONTROL Transformation]**, 및 **[!UICONTROL Geography]**.

1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL IP Lookup.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.

1. 새 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. 변환 구성 창이 나타납니다.

1. 창에서 **[!UICONTROL Transformation]**&#x200B;를 클릭한 다음 **[!UICONTROL Transformations]**.

1. 다음 중 하나를 찾아 클릭합니다 **[!UICONTROL IPLookup Quova]** 또는 **[!UICONTROL IPLookup Digital Envoy]**.

1. File 매개 변수의 경우 새 데이터( [!DNL .bin]) Adobe이 제공한 파일입니다.
1. 마우스 오른쪽 단추를 클릭하여 변형 구성 파일을 저장합니다 **[!UICONTROL (modified)]** 구성 창 상단에서 을 클릭하고 **[!UICONTROL Save]**.

1. 다음 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하여 데이터 서비스를 사용하는 각 프로필에 수정된 구성 파일을 저장합니다 [!DNL IP Lookup.cfg] 에서 [!DNL User] 열 및 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*. 데이터 세트 프로필을 동기화한 후 데이터 재변환이 시작됩니다.

   데이터 집합 재변형에 대한 자세한 내용은 *데이터 집합 구성 안내서*.

   >[!NOTE]
   >
   >수정된 구성 파일을 Adobe이 제공한 내부 프로필(다음을 포함)에 저장하지 마십시오 [!DNL IP Geo-location] 또는 [!DNL IP Geo-intelligence] 프로필)로 업데이트되는 경우 이러한 프로필에 업데이트를 설치하면 변경 사항을 덮어씁니다.

를 설치한 경우 [!DNL IP Geo-intelligence] 및 [!DNL IP Geo-location] 버전 5.1 이상의 데이터 서비스에서는 데이터 서비스 업데이트를 완료했습니다. 그러나 를 설치한 경우 [!DNL IP Geo-intelligence] 및 [!DNL IP Geo-location] 데이터 서비스 버전 5.1 이전의 경우 다음 추가 절차를 완료해야 합니다.

## 조회 파일 바꾸기 {#section-ced1efa38a76419d812edd35423dbff7}

다음 단계는 [!DNL IP Geo-intelligence] 및 [!DNL IP Geo-location] 버전 5.1 이전의 데이터 서비스.

1. 에서 [!DNL Server Files Manager]다음 중 하나를 클릭합니다. **[!UICONTROL Profiles]** > **[!UICONTROL IP Geo-intelligence]** 또는 **[!UICONTROL Profiles]** > **[!UICONTROL IP Geo-location]**&#x200B;를 클릭한 다음 **[!UICONTROL Maps]** 콘텐츠를 보려면 클릭하십시오.

1. 에서 마우스 오른쪽 단추를 클릭합니다. **[!UICONTROL Temp]** 열 **[!UICONTROL Maps]** 을(를) 클릭합니다. **[!UICONTROL Open]** > *&lt;**[!UICONTROL folder]**>*.

1. 새 복사본 [!DNL .txt] 맵 폴더 창에 Adobe이 제공하는 파일입니다.
1. Data Workbench 서버 시스템에 파일을 저장하려면 [!DNL Temp] 열 [!DNL .txt] 파일 및 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

>[!NOTE]
>
>클러스터를 실행 중인 경우 클러스터의 마스터 Data Workbench 서버에 파일을 업로드합니다.

## 레이어 파일 업데이트 {#section-8b84e7099bad40c9a69665a4890fe66e}

>[!NOTE]
>
>다음 단계는 [!DNL IP Geo-intelligence] 및 [!DNL IP Geo-location] 버전 5.1 이전의 데이터 서비스.

모든 레이어에 대해 다음 단계를 완료합니다( [!DNL .layer]) 를 참조하는 파일입니다. [!DNL IP Geo-intelligence] 또는 [!DNL IP Geo-location] 조회 ( [!DNL .txt]) 파일로 내보낼 때 시간별 세부기간이 작동하지 않는 문제를 해결했습니다.

1. Data Workbench 서버 설치 디렉토리 내의 Profiles\*data service name*\Map 폴더에서 [!DNL .layer] 메모장과 같은 텍스트 편집기에 있는 파일입니다.

1. 에서 [!DNL Data Paths] vector에서 [!DNL .txt] 새 파일의 이름과 일치하는 조회 파일 [!DNL .txt] 다음 파일 샘플에 강조 표시된 대로 Adobe이 제공한 파일:

   ```
   Layer = ElementPointLayer:
     Data Paths = vector: 1 items
       0 = Path: Maps\\LookupFileName.txt
     Longitude Column = string: LongitudeColumnName
     Latitude Column = string: LatitudeColumnName
     Name Column = string: LocationColumnName
     Key Column = string: KeyColumnName
     Dimension = ref: wdata/model/dim/DimensionName
     Metric = ref: wdata/model/metric/MetricName
   ```

1. 업데이트된 레이어 파일을 저장합니다.
1. 에 대해 2단계와 3단계를 반복합니다 [!DNL .layer] 를 참조하는 파일 [!DNL IP Geo-intelligence] 또는 [!DNL IP Geo-location] [!DNL .txt] 파일.
