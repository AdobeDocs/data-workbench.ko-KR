---
description: 지형 이미지 층은 지구의 지형 이미지를 표시합니다.
title: 지형 이미지 레이어
uuid: 17968293-1ad2-4040-a174-d33f418af9b7
exl-id: 754211a7-0b1f-4353-86f8-9c634d70cd83
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 2%

---

# 지형 이미지 레이어{#terrain-image-layers}

지형 이미지 층은 지구의 지형 이미지를 표시합니다.

[!DNL Terrain image layers] 은 프로필에  [!DNL Geography] 사용자 정의 형식으로 저장됩니다. 이러한 이미지 레이어는 Adobe에 의해 생성할 수 있거나 Data Workbench 서버가 사용자가 제공하는 지형 이미지를 지구 시각화에서 사용할 수 있는 지형 레이어로 변환할 수 있습니다.

>[!NOTE]
>
>[!DNL terrain image layers] 을 사용하여 작업하려면 Adobe에서 제공한 [!DNL Terrain Images.cfg] 파일을 설치해야 합니다.

지형 이미지 레이어를 정의하려면 다음을 수행해야 합니다.

* **전 세계에** 표시할 이미지가 포함된 하나 이상의 지형 이미지 파일입니다.
* **레이어 [!DNL Terrain Images.cfg]** 에 사용할 지형 이미지 파일을 지정하는 파일입니다. [!DNL Terrain Images.cfg] 파일을 사용하면 하나 이상의 소스를 추가하여 [!DNL terrain image layer]을 만들 수 있습니다. 지형 이미지 파일의 형식은 추가해야 하는 소스 유형을 결정합니다. 다음 표에서는 지원되는 지형 이미지 파일 형식을 포함하여 사용 가능한 지형 이미지 레이어 소스에 대한 설명을 제공합니다.

<table id="table_CFDF5E61FCCD40B29A9D35FFA42F68D1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 유형 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>투영되지 않은 원시 비트맵 </p> </td> 
   <td colname="col2"> <p>24비트 헤드리스 없는 RGB 파일에서 <span class="wintitle"> 지형 이미지 레이어</span>를 만듭니다. 이 RGB 파일은 위도-경도 정렬(투영되지 않음)이며, 여기서 북쪽은 이미지의 상단이고, 동쪽은 오른쪽에 있습니다. </p> <p>지원되는 이미지 형식:RAW </p> <p> <p>참고:이 소스에는 투영 정보가 필요합니다. 투영 형식에 대한 자세한 내용은 <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> 지형 이미지에 대한 투영 정보 지정</a>을 참조하십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>일반 이미지, 투영되지 않음 </p> </td> 
   <td colname="col2"> <p>24비트, 위도-경도 정렬(투영되지 않은) 이미지 포맷에서 <span class="wintitle"> 지형 이미지 레이어</span>를 만듭니다. 여기서 북은 이미지의 상단이고, 동쪽은 오른쪽에 있습니다. </p> <p>지원되는 이미지 형식:BMP, JPG, PNG, TIFF </p> <p> <p>참고:이 소스에는 투영 정보가 필요합니다. 투영 형식에 대한 자세한 내용은 <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> 지형 이미지에 대한 투영 정보 지정</a>을 참조하십시오. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>포함된 투사가 있는 이미지 </p> </td> 
   <td colname="col2"> <p>이미지 파일에 지리 데이터를 포함하는 이미지 형식에서 <span class="wintitle"> 지형 이미지 레이어</span>를 만듭니다. 이미지에서 투영 정보가 추출됩니다. </p> <p>지원되는 이미지 형식:Erdas(IMG), GeoTIFF </p> <p> <p>참고:이 소스는 일반적으로 프로젝션 정보가 필요하지 않지만 필요한 경우 이러한 정보의 추가를 지원합니다. 투영 형식에 대한 자세한 내용은 <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> 지형 이미지에 대한 투영 정보 지정</a>을 참조하십시오. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**지형 이미지 레이어를 정의하려면**

1. Data Workbench의 **[!UICONTROL Admin]** > **[!UICONTROL Dataset and Profile]** 탭에서 **[!UICONTROL Servers Manager]** 섬네일을 클릭하여 [!DNL Servers Manager] 작업 영역을 엽니다.
1. [!DNL Servers Manager] 창 내에서 원하는 Data Workbench 서버의 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]** 를 클릭합니다.
1. [!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 해당 콘텐츠를 봅니다. [!DNL Terrain Images.cfg] 파일이 이 디렉터리 내에 있습니다.
1. 서버 이름 열의 [!DNL Terrain Images.cfg] 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Make Local]** 을 클릭합니다. [!DNL Terrain Images.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.
1. **[!UICONTROL Temp]** 열에서 새로 만든 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]** 를 클릭합니다. [!DNL Terrain Images.cfg] 창이 나타납니다.
1. [!DNL Terrain Images] 창에서 **[!UICONTROL component]** 을 클릭하여 해당 콘텐츠를 봅니다.
1. **[!UICONTROL Sources]** > **[!UICONTROL Add new]** 을 마우스 오른쪽 단추로 클릭하고 다음 소스 유형 중 하나를 선택합니다.

   * **[!UICONTROL Raw unprojected bitmap]** 구문을 사용하는 키-값 쌍으로 전달됩니다. (이 소스 유형이 추가되면 [!DNL Terrain Images] 창에서 RawTerrainSource 레이블이 지정됩니다.)

   * **[!UICONTROL General image, unprojected]** 구문을 사용하는 키-값 쌍으로 전달됩니다. (이 소스 유형이 추가되면 [!DNL Terrain Images] 창에서 [!DNL GDALTerrainSource] 레이블이 지정됩니다.)

   * **[!UICONTROL Image with embedded projection]** 구문을 사용하는 키-값 쌍으로 전달됩니다. (이 소스 유형이 추가되면 [!DNL Terrain Images] 창에서 [!DNL GDALTerrainSource] 레이블이 지정됩니다.)

1. 다음 샘플 파일 및 매개변수 테이블을 안내서로 사용하여 필요에 따라 소스의 매개변수를 편집합니다.

   ![](assets/cfg_TerrainImages_ALL.png)

<table id="table_345ACB4C48524516AADB731D87FC6792"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>감마 </p> </td> 
   <td colname="col2"> <p>모든 소스에 대해 선택 사항입니다. 소스 이미지에 적용할 감마 수정을 지정합니다. 이는 Data Workbench이 일반적으로 높은 감마 설정으로 실행되기 때문에 바람직할 수 있습니다. 기본값은 1입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>높이 </p> </td> 
   <td colname="col2"> <p>투영되지 않은 원시 비트맵 이미지에 필요합니다. 소스 이미지의 높이(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>투영 정보 </p> </td> 
   <td colname="col2"> <p>투영되지 않은 원시 비트맵 이미지 및 일반 이미지에 필요하나 투영되지 않지만 포함된 영상의 경우 지원됩니다. Data Workbench은 지형 이미지 레이어에 대한 위도-경도 예측 및 TM(Transverse Mercator) 예측을 지원합니다. 기본 투영 형식은 위도-경도 투영(LatLonProjection)입니다. </p> <p>투영 형식에 대한 자세한 내용은 <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> 지형 이미지에 대한 투영 정보 지정</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>소스 이미지 </p> </td> 
   <td colname="col2"> <p>모든 소스에 필요합니다. 소스 이미지 파일의 이름입니다. 파일 이름이나 와일드카드 패턴일 수 있습니다. 패턴을 사용하면 연관된 메타데이터가 변경되지 않고 다른 날짜에 있는 동일한 영역에 대한 이미지를 업로드하는 경우 유용할 수 있습니다. 따라서 <span class="filepath"> Tysons Corner *.raw</span> 같은 패턴은 <span class="filepath"> Tysons Corner 050211.raw</span>, <span class="filepath"> Tysons Corner 050218.raw</span> 등과 같은 새 이미지를 추가하고 파일의 매개 변수가 동일하면 추가 구성이 필요하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>타일 압축 품질 </p> </td> 
   <td colname="col2"> <p>모든 소스에 대해 선택 사항입니다. JPEG 압축의 경우 이미지 크기와 품질의 균형을 조정하는 방법을 지정하는 0에서 100까지의 정수입니다. 기본값은 0입니다. 숫자가 높을수록 이미지 품질이 향상되지만 Data Workbench 사용자의 경우 더 큰 이미지가 생성되고 다운로드 시간이 길어집니다. </p> <p> <p>참고: 70보다 작은 이미지를 압축하면 이미지가 저하될 수 있습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>타일 압축기 </p> </td> 
   <td colname="col2"> <p>모든 소스에 대해 선택 사항입니다. 출력 파일을 작성하는 데 사용되는 압축 방법을 지정합니다. 현재 지원되는 유일한 방법은 RAWRAWGB(기본값, 압축 안 함) 및 JPEG입니다. JPEG 압축을 사용하면 프로필 동기화 중에 전송되는 레이어의 크기를 줄일 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>너비 </p> </td> 
   <td colname="col2"> <p>투영되지 않은 원시 비트맵 이미지에 필요합니다. 소스 이미지의 너비(픽셀 단위)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 다음 표를 안내서로 사용하여 소스 이미지 위치, 임시 이미지 저장소 및 레이어 쓰기 매개 변수를 편집합니다. 이러한 매개 변수는 이 파일의 [!DNL Sources] 섹션에서 정의한 모든 지형 이미지 소스에 적용됩니다.

<table id="table_103F02C54ED94C6C922450F5B2781CAE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>소스 이미지 위치 </p> </td> 
   <td colname="col2"> <p>필수 여부. 이미지가 지형 레이어로 변환되도록 스캔되는 디렉토리입니다. 절대 경로가 아닌 경우 Data Workbench 서버 설치 디렉토리에 대해 해석됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>임시 이미지 저장소 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 소스 이미지를 지형 레이어로 변환하는 데 사용되는 임시 파일을 저장하는 데 사용되는 디렉토리 이름입니다. 절대 경로가 아닌 경우 Data Workbench 서버 설치 디렉토리에 대해 해석됩니다. 기본 위치는 <span class="wintitle"> Temp</span> 디렉토리입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>레이어 쓰기 대상 </p> </td> 
   <td colname="col2"> <p>필수 여부. 지형 레이어가 출력되는 디렉토리입니다. 일반적으로 Globe 시각화가 레이어를 찾을 수 있도록 프로필 디렉토리의 Map 하위 디렉토리입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭하여 파일을 저장합니다.
1. 업데이트된 파일을 Data Workbench 서버 컴퓨터에 저장하려면 [!DNL Server Files Manager] 열에서 [!DNL Terrain Images.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]*** 를 클릭합니다.[!DNL Temp]
