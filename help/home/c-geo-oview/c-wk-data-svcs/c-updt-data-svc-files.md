---
description: 데이터 서비스를 구독하는 경우 Adobe에서 제공하는 데이터 서비스 파일을 정기적으로 업데이트해야 합니다.
title: 데이터 서비스 파일 업데이트
uuid: 8c14be34-fde3-4c4c-9c22-739863317d6e
exl-id: bb92d40c-cc8d-4ecf-bd48-ed962fd5d73b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 1%

---

# 데이터 서비스 파일 업데이트{#updating-data-service-files}

데이터 서비스를 구독하는 경우 Adobe에서 제공하는 데이터 서비스 파일을 정기적으로 업데이트해야 합니다.

이렇게 하려면 데이터 워크벤치 서버의 파일에 액세스할 수 있어야 합니다.

[!DNL IP Geo-location] 또는 [!DNL IP Geo-intelligence] 데이터 파일을 로드하려면 다음 절차를 완료해야 합니다.

## 데이터 파일 {#section-2b53c2951ae04c6fa8b3bdf080469ff6} 바꾸기

1. 데이터 워크벤치의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 [!DNL Servers Manager] 작업 영역을 엽니다.

1. [!DNL Servers Manager] 창 내에서 파일을 로드할 데이터 워크벤치 서버의 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]** 을 클릭합니다.

1. [!DNL Server Files Manager]에서 **[!UICONTROL Lookups\IP Geo-location]** 또는 **[!UICONTROL Lookups\IP Geo-intelligence]**&#x200B;의 **[!UICONTROL Temp]** 열을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > *&lt;**[!UICONTROL folder]***&#x200B;을 클릭합니다.

1. Adobe에서 제공한 [!DNL .bin] 데이터 파일을 Lookups\IP Geo-location 또는 Lookups\IP Geo-intelligence 폴더 창에 복사합니다.
1. 데이터 파일의 [!DNL Temp] 열을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 클릭하여 데이터 워크벤치 서버 시스템에 파일을 저장합니다.

   클러스터를 실행 중인 경우 클러스터의 마스터 데이터 워크벤치 서버에 파일을 업로드합니다.

## IPLookup 변환 업데이트 {#section-a8b99afe3eb04afabe88e15bd465f935}

1. [!DNL Profile Manager]에서 **[!UICONTROL Dataset]**, **[!UICONTROL Transformation]** 및 **[!UICONTROL Geography]**&#x200B;을 클릭합니다.

1. [!DNL IP Lookup.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 을 클릭합니다. 이 파일의 확인 표시는 [!DNL User] 열에 표시됩니다.

1. 새 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다. 변형 구성 창이 나타납니다.

1. 창에서 **[!UICONTROL Transformation]**&#x200B;을 클릭한 다음 **[!UICONTROL Transformations]**&#x200B;을 클릭합니다.

1. **[!UICONTROL IPLookup Quova]** 또는 **[!UICONTROL IPLookup Digital Envoy]** 중 하나를 찾아 클릭합니다.

1. File 매개 변수의 경우 Adobe에서 제공하는 새 데이터( [!DNL .bin]) 파일의 이름과 일치하도록 파일 이름을 업데이트합니다.
1. 구성 창의 맨 위에서 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭하여 변형 구성 파일을 저장합니다.

1. [!DNL User] 열에서 [!DNL IP Lookup.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]***&#x200B;를 클릭하여 데이터 서비스를 사용하는 각 프로필에 수정된 구성 파일을 저장합니다. 데이터 세트 프로필의 동기화 후 데이터 재변환이 시작됩니다.

   데이터 집합 재변환에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;의 다시 처리 및 변형 장을 참조하십시오.

   >[!NOTE]
   >
   >이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓸 경우 수정된 구성 파일을 Adobe에서 제공하는 내부 프로필([!DNL IP Geo-location] 또는 [!DNL IP Geo-intelligence] 프로필 포함)에 저장하지 마십시오.

버전 5.1 이상용 [!DNL IP Geo-intelligence] 및 [!DNL IP Geo-location] 데이터 서비스를 설치한 경우 데이터 서비스 업데이트를 완료했습니다. 그러나 버전 5.1 이전에 [!DNL IP Geo-intelligence] 및 [!DNL IP Geo-location] 데이터 서비스를 설치한 경우에는 다음 추가 절차를 완료해야 합니다.

## 조회 파일 {#section-ced1efa38a76419d812edd35423dbff7} 바꾸기

버전 5.1 이전에 [!DNL IP Geo-intelligence] 및 [!DNL IP Geo-location] 데이터 서비스를 설치한 경우에만 다음 단계를 완료해야 합니다.

1. [!DNL Server Files Manager]에서 **[!UICONTROL Profiles]** > **[!UICONTROL IP Geo-intelligence]** 또는 **[!UICONTROL Profiles]** > **[!UICONTROL IP Geo-location]**&#x200B;를 클릭한 다음 **[!UICONTROL Maps]**&#x200B;를 클릭하여 내용을 봅니다.

1. **[!UICONTROL Maps]**&#x200B;에 대한 **[!UICONTROL Temp]** 열을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > *&lt;**[!UICONTROL folder]***&#x200B;를 클릭합니다.

1. Adobe에서 제공한 새 [!DNL .txt] 파일을 맵 폴더 창에 복사합니다.
1. [!DNL .txt] 파일의 [!DNL Temp] 열에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 클릭하여 데이터 워크벤치 서버 시스템에 파일을 저장합니다.

>[!NOTE]
>
>클러스터를 실행 중인 경우 클러스터의 마스터 데이터 워크벤치 서버에 파일을 업로드합니다.

## 레이어 파일 업데이트 중 {#section-8b84e7099bad40c9a69665a4890fe66e}

>[!NOTE]
>
>버전 5.1 이전에 [!DNL IP Geo-intelligence] 및 [!DNL IP Geo-location] 데이터 서비스를 설치한 경우에만 다음 단계를 완료해야 합니다.

[!DNL IP Geo-intelligence] 또는 [!DNL IP Geo-location] 조회( [!DNL .txt]) 파일을 참조하는 모든 레이어( [!DNL .layer]) 파일에 대해 다음 단계를 완료합니다.

1. 데이터 워크벤치 서버 설치 디렉토리 내의 Profiles\*data service name*\Maps 폴더에서 메모장과 같은 텍스트 편집기에서 [!DNL .layer] 파일을 엽니다.

1. [!DNL Data Paths] 벡터에서 다음 파일 샘플에 표시된 것처럼 Adobe에서 제공하는 새 [!DNL .txt] 파일의 이름과 일치하도록 [!DNL .txt] 조회 파일의 이름을 업데이트합니다.

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
1. [!DNL IP Geo-intelligence] 또는 [!DNL IP Geo-location] [!DNL .txt] 파일을 참조하는 모든 [!DNL .layer] 파일에 대해 2단계와 3단계를 반복합니다.
