---
description: 지형의 이미지 층은 지구의 지형을 표시합니다.
solution: Analytics
title: 지형 이미지 레이어
topic: Data workbench
uuid: 17968293-1ad2-4040-a174-d33f418af9b7
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 지형 이미지 레이어{#terrain-image-layers}

지형의 이미지 층은 지구의 지형을 표시합니다.

[!DNL Terrain image layers] 는 사용자 정의 형식으로 프로필에 저장됩니다 [!DNL Geography] . 이러한 이미지 레이어는 Adobe에서 생성할 수 있고 Data Workbench 서버는 사용자가 제공한 지형 이미지를 지구 시각화에 사용할 수 있는 지형 레이어로 변환할 수 있습니다.

>[!NOTE]
>
>함께 작업하려면 [!DNL terrain image layers]Adobe에서 제공하는 [!DNL Terrain Images.cfg] 파일을 설치해야 합니다.

지형 이미지 레이어를 정의하려면 다음 항목이 있어야 합니다.

* **세계에 표시할 이미지가 포함된 하나 이상의 지형 이미지 파일** .
* **레이어에 사용할 지형 이미지 파일을 지정하는[!DNL Terrain Images.cfg]파일입니다** . 이 [!DNL Terrain Images.cfg] 파일을 사용하면 하나 이상의 소스를 추가하여 소스를 만들 수 [!DNL terrain image layer]있습니다. 지형 이미지 파일의 형식은 추가할 소스의 유형을 결정합니다. 다음 표에서는 지원되는 지형 이미지 파일 형식을 포함하여 사용 가능한 지형 이미지 레이어 소스에 대한 설명을 제공합니다.

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
   <td colname="col2"> <p>24비트 헤드리스 없는 RGB 파일에서 <span class="wintitle"> 지형 이미지 레이어를</span> 만듭니다. 이 RGB 파일은 위도와 경도 정렬(투영되지 않음)되며, 여기서 북쪽은 이미지의 상단이고, 동쪽은 오른쪽에 있습니다. </p> <p>지원되는 이미지 형식:RAW </p> <p> <p>참고:이 소스에는 프로젝션 정보가 필요합니다. 투영 형식에 대한 자세한 내용은 지형 이미지에 <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> 대한 투영 정보 지정을 참조하십시오</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>일반 이미지, 투영되지 않음 </p> </td> 
   <td colname="col2"> <p>24비트 위도로 정렬된(투영되지 않음) 이미지 포맷에서 <span class="wintitle"> 지형 이미지 레이어를</span> 만듭니다. 여기서 북은 이미지의 맨 위에, 동쪽은 오른쪽에 있습니다. </p> <p>지원되는 이미지 형식:BMP, JPG, PNG, TIFF </p> <p> <p>참고:이 소스에는 프로젝션 정보가 필요합니다. 투영 형식에 대한 자세한 내용은 지형 이미지에 <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> 대한 투영 정보 지정을 참조하십시오</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>포함된 프로젝션이 있는 이미지 </p> </td> 
   <td colname="col2"> <p>이미지 파일에 지리 데이터를 임베드하는 이미지 포맷에서 <span class="wintitle"> 지형 이미지 레이어를</span> 만듭니다. 프로젝션 정보는 이미지에서 추출됩니다. </p> <p>지원되는 이미지 형식:Erdas(IMG), GeoTIFF </p> <p> <p>참고:이 소스는 대개 프로젝션 정보가 필요하지 않지만 필요한 경우 이러한 정보를 추가할 수 있습니다. 투영 형식에 대한 자세한 내용은 지형 이미지에 <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> 대한 투영 정보 지정을 참조하십시오</a>. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**지형 이미지 레이어를 정의하려면**

1. 데이터 워크벤치의 **[!UICONTROL Admin]** > **[!UICONTROL Dataset and Profile]** 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 [!DNL Servers Manager] 작업 영역을 엽니다.
1. 창 내에서 [!DNL Servers Manager] 원하는 데이터 워크벤치 서버 아이콘을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Server Files]**&#x200B;클릭합니다.
1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Components]** 봅니다. 이 [!DNL Terrain Images.cfg] 파일은 이 디렉토리 내에 있습니다.
1. 에 대한 서버 이름 열에서 확인 표시를 마우스 오른쪽 단추로 [!DNL Terrain Images.cfg]클릭한 다음 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다 [!DNL Terrain Images.cfg].
1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Temp]** > **[!UICONTROL Open]** **[!UICONTROL from the workbench]**&#x200B;을 클릭합니다. 창이 [!DNL Terrain Images.cfg] 나타납니다.
1. 창에서 [!DNL Terrain Images] 을 클릭하여 내용을 **[!UICONTROL component]** 봅니다.
1. 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Sources]** > **[!UICONTROL Add new]** 다음 소스 유형 중 하나를 선택합니다.

   * **[!UICONTROL Raw unprojected bitmap]** 구문을 사용하는 키-값 쌍으로 전달됩니다. (이 소스 유형이 추가되면 [!DNL Terrain Images] 창에 RawTerrainSource 레이블이 표시됩니다.)

   * **[!UICONTROL General image, unprojected]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 소스 유형이 추가되면 [!DNL GDALTerrainSource] 창에 레이블이 표시됩니다 [!DNL Terrain Images] .

   * **[!UICONTROL Image with embedded projection]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 소스 유형이 추가되면 [!DNL GDALTerrainSource] 창에 레이블이 표시됩니다 [!DNL Terrain Images] .

1. 다음 샘플 파일과 매개 변수 표를 안내선으로 사용하여 필요에 따라 소스의 매개 변수를 편집합니다.

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
   <td colname="col2"> <p>모든 소스에 대한 선택 사항입니다. 소스 이미지에 적용할 감마 교정을 지정합니다. 데이터 워크벤치가 일반적으로 높은 감마 설정으로 실행되기 때문에 이 작업이 바람직할 수 있습니다. 기본값은 1입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>높이 </p> </td> 
   <td colname="col2"> <p>투영되지 않은 원시 비트맵 이미지에 필요합니다. 소스 이미지의 높이(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>투영 정보 </p> </td> 
   <td colname="col2"> <p>투영되지 않은 Raw 비트맵 이미지 및 일반 이미지(투영되지 않음)에는 필요하지만 임베드된 투영된 이미지에 대해서는 지원됩니다. Data Workbench는 지형 이미지 레이어에 대한 위도 경도 예측 및 TM(Transverse Mercator) 예측을 지원합니다. 기본 투영 형식은 위도 경도 투영(LatLonProjection)입니다. </p> <p>투영 형식에 대한 자세한 내용은 지형 이미지에 <a href="../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-proj-info-ter-imgs.md#concept-eec35baa01744895b847a02e69dad04e"> 대한 투영 정보 지정을 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>소스 이미지 </p> </td> 
   <td colname="col2"> <p>모든 소스에 필요합니다. 소스 이미지 파일의 이름입니다. 파일 이름 또는 와일드카드 패턴일 수 있습니다. 예를 들어, 연결된 메타데이터가 변경되지 않고 다른 날짜에 있는 동일한 영역에 대한 이미지가 업로드되는 경우 패턴을 사용하는 것이 유용합니다. 따라서 Tysons <span class="filepath"> Corner *.raw와</span> 같은 패턴은 Tysons Corner 050211.raw <span class="filepath"> , Tysons Corner 050218.raw</span>등과 <span class="filepath"></span>같은 새 이미지가 추가되면 파일에 대한 매개 변수가 다른 방식으로 동일한 경우 추가 구성이 필요하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>타일 압축 품질 </p> </td> 
   <td colname="col2"> <p>모든 소스에 대한 선택 사항입니다. JPEG 압축의 경우 이미지 크기 및 품질 균형을 조정하는 방법을 지정하는 0에서 100까지의 정수입니다. 기본값은 0입니다. 숫자가 높을수록 이미지 품질은 향상되지만 Data Workbench 사용자는 더 많은 이미지와 다운로드 시간이 길어집니다. </p> <p> <p>참고: 70 미만의 이미지를 압축하면 이미지 저하가 발생할 수 있습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>타일 압축기 </p> </td> 
   <td colname="col2"> <p>모든 소스에 대한 선택 사항입니다. 출력 파일을 쓰는 데 사용할 압축 방법을 지정합니다. 현재 지원되는 유일한 방법은 RAWRGB(기본값, 압축 안 함)와 JPEG입니다. JPEG 압축을 사용하면 프로필 동기화 동안 전송되는 레이어 크기를 줄일 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>너비 </p> </td> 
   <td colname="col2"> <p>투영되지 않은 원시 비트맵 이미지에 필요합니다. 소스 이미지의 너비(픽셀 단위)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 다음 표를 가이드로 사용하여 소스 이미지 위치, 임시 이미지 저장소 및 레이어 쓰기를 매개 변수에 편집합니다. 이러한 매개 변수는 이 파일의 [!DNL Sources] 섹션에서 정의하는 모든 지형 이미지 소스에 적용됩니다.

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
   <td colname="col2"> <p>필수 여부. 이미지를 스캔하여 지형 레이어로 변환할 수 있는 디렉토리입니다. 절대 경로가 아닌 경우 Data Workbench 서버 설치 디렉토리에 상대적인 방식으로 해석됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>임시 이미지 저장소 </p> </td> 
   <td colname="col2"> <p>선택 사항입니다. 소스 이미지를 지형 레이어로 변환하는 데 사용되는 임시 파일을 저장하는 데 사용되는 디렉토리의 이름입니다. 절대 경로가 아닌 경우 Data Workbench 서버 설치 디렉토리에 상대적인 방식으로 해석됩니다. 기본 위치는 Temp <span class="wintitle"> 디렉토리입니다</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>레이어 쓰기 대상 </p> </td> 
   <td colname="col2"> <p>필수 여부. 지형 레이어가 출력되는 디렉토리입니다. 보통 프로필 디렉토리의 Maps 하위 디렉토리이므로 지구 시각화가 레이어를 찾을 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭하여 파일을 저장합니다 **[!UICONTROL Save]**.
1. 업데이트된 파일을 데이터 워크벤치 서버 컴퓨터에 저장하려면 [!DNL Server Files Manager]열에서 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Terrain Images.cfg] > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *을 클릭합니다&#x200B;**[!UICONTROL server name]***.

