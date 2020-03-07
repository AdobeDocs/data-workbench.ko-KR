---
description: 데이터 워크벤치에서 지형 이미지 레이어는 지구의 지형 이미지를 표시합니다.
solution: Analytics
title: 지형 이미지 레이어 작업
topic: Data workbench
uuid: 2f23a2c8-f551-4b84-bd87-5d7053910ab3
translation-type: tm+mt
source-git-commit: 948c6dd04819e939b45745db573a53c8be51ce37

---


# 지형 이미지 레이어 작업{#working-with-terrain-image-layers}

데이터 워크벤치에서 지형 이미지 레이어는 지구의 지형 이미지를 표시합니다.

지형 이미지 레이어는 [!DNL Geography] 프로필에 사용자 정의 형식으로 저장됩니다. 이러한 이미지 레이어는 Adobe에서 생성할 수 있고 데이터 워크벤치 서버는 사용자가 제공한 지형 이미지를 지구 시각화에 사용할 수 있는 지형 레이어로 변환할 수 있습니다.

>[!NOTE]
>
>지형 이미지 레이어를 사용하여 작업하려면 Adobe에서 제공하는 [!DNL Terrain Images.cfg] 파일을 설치해야 합니다. 설치 지침은 데이터 워크벤치 [지역 설치를 참조하십시오](../../../../home/c-geo-oview/c-inst-geo/c-inst-geo.md).

지형 이미지 레이어를 정의하려면 다음 항목이 있어야 합니다.

* **세계에 표시할 이미지가 포함된 하나 이상의 지형 이미지 파일** .
* **레이어에 사용할 지형 이미지** 파일을 지정하는 Terrain Images.cfg 파일 이 [!DNL Terrain Images.cfg] 파일을 사용하면 하나 이상의 소스를 추가하여 지형 이미지 레이어를 만들 수 있습니다. 지형 이미지 파일의 형식은 추가할 소스의 유형을 결정합니다. 다음 표에서는 지원되는 지형 이미지 파일 형식을 포함하여 사용 가능한 지형 이미지 레이어 소스에 대한 설명을 제공합니다.

<table id="table_BF8D5933BFBE45039BD164C258D3B450"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 유형 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 투영되지 않은 원시 비트맵 </td> 
   <td colname="col2"> <p>24비트 헤드리스 RGB 파일에서 투영되지 않은 위도로 정렬된 지형 이미지 레이어를 만듭니다. 이 RGB 파일은 북쪽이 이미지의 상단이고 동쪽은 오른쪽에 있습니다. </p> <p>지원되는 이미지 형식:RAW </p> <p> <p>참고:이 소스에는 프로젝션 정보가 필요합니다. 투영 형식에 대한 자세한 내용은 지형 이미지에 <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> 대한 투영 정보 지정을 참조하십시오</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 일반 이미지, 투영되지 않음 </td> 
   <td colname="col2"> <p>24비트 위도와 투영되지 않은 이미지 포맷으로 지형 이미지 레이어를 만듭니다. 여기서 북쪽은 이미지의 상단이고, 동쪽은 오른쪽에 있습니다. </p> <p>지원되는 이미지 형식:BMP, JPG, PNG, TIFF </p> <p> <p>참고:이 소스에는 프로젝션 정보가 필요합니다. 투영 형식에 대한 자세한 내용은 지형 이미지에 <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> 대한 투영 정보 지정을 참조하십시오</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 포함된 프로젝션이 있는 이미지 </td> 
   <td colname="col2"> <p>이미지 파일에 지리 데이터를 임베드하는 이미지 포맷에서 지형 이미지 레이어를 만듭니다. 프로젝션 정보는 이미지에서 추출됩니다. </p> <p>지원되는 이미지 형식:Erdas(IMG), GeoTIFF </p> <p> <p>참고:이 소스는 대개 프로젝션 정보가 필요하지 않지만 필요한 경우 이러한 정보를 추가할 수 있습니다. 투영 형식에 대한 자세한 내용은 지형 이미지에 <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> 대한 투영 정보 지정을 참조하십시오</a>. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**지형 이미지 레이어를 정의하려면**

1. 데이터 워크벤치의 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판을 클릭하여 [!DNL Servers Manager] 작업 영역을 엽니다.

1. 창 내에서 원하는 데이터 워크벤치 서버의 아이콘을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다. [!DNL Servers Manager] **[!UICONTROL Server Files]**

1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Components]** 봅니다. 이 [!DNL Terrain Images.cfg] 파일은 이 디렉토리 내에 있습니다.

1. 에 대한 서버 이름 열에서 확인 표시를 마우스 오른쪽 단추로 [!DNL Terrain Images.cfg]클릭한 다음 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 열에 확인 표시가 나타납니다. [!DNL Temp][!DNL Terrain Images.cfg.]

1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL from the workbench]**&#x200B;을 클릭합니다. 창이 [!DNL Terrain Images.cfg]나타납니다.

1. 창에서 [!DNL Terrain Images] 을 클릭하여 내용을 **[!UICONTROL component]** 봅니다.

1. 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Sources]** > **[!UICONTROL Add new]** 다음 소스 유형 중 하나를 선택합니다.

   * **[!UICONTROL Raw unprojected bitmap]** 구문을 사용하는 키-값 쌍으로 전달됩니다. (이 소스 유형이 추가되면 [!DNL Terrain Images] 창에 RawTerrainSource 레이블이 표시됩니다.)

   * **[!UICONTROL General image, unprojected]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 소스 유형이 추가되면 [!DNL Terrain Images] 창에서 GDALTerrainSource로 레이블이 지정됩니다.

   * **[!UICONTROL Image with embedded projection]** 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 소스 유형이 추가되면 [!DNL Terrain Images] 창에서 GDALTerrainSource로 레이블이 지정됩니다.

1. 다음 샘플 파일과 매개 변수 표를 안내선으로 사용하여 필요에 따라 소스의 매개 변수를 편집합니다.

   ![](assets/cfg_TerrainImages_ALL.png)

<table id="table_83171CB58F8B4816BCCA9BFFD5ECD92A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 감마 </td> 
   <td colname="col2"> 모든 소스에 대한 선택 사항입니다. 소스 이미지에 적용할 감마 교정을 지정합니다. 데이터 워크벤치가 일반적으로 높은 감마 설정으로 실행되기 때문에 이 작업이 바람직할 수 있습니다. 기본값은 1입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 높이 </td> 
   <td colname="col2"> 투영되지 않은 원시 비트맵 이미지에 필요합니다. 소스 이미지의 높이(픽셀 단위)입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 투영 정보 </td> 
   <td colname="col2"> <p>투영되지 않은 Raw 비트맵 이미지 및 일반 이미지(투영되지 않음)에는 필요하지만 임베드된 투영된 이미지에 대해서는 지원됩니다. 데이터 워크벤치<span class="wintitle"> 지리는</span> 지형 이미지 레이어에 대한 위도 경도 투영과 TM(Transverse Mercator) 투영을 지원합니다. 기본 투영 형식은 위도 경도 투영(LatLonProjection)입니다. </p> <p>투영 형식에 대한 자세한 내용은 지형 이미지에 <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> 대한 투영 정보 지정을 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 소스 이미지 </td> 
   <td colname="col2">모든 소스에 필요합니다. 소스 이미지 파일의 이름입니다. 파일 이름 또는 와일드카드 패턴일 수 있습니다. 예를 들어, 연결된 메타데이터가 변경되지 않고 다른 날짜에 있는 동일한 영역에 대한 이미지가 업로드되는 경우 패턴을 사용하는 것이 유용합니다. 따라서 "Tysons<span class="filepath"> Corner *.raw</span>"와 같은 패턴은 Tysons Corner 050211.raw <span class="filepath"> , Tysons Corner 050218.raw</span>등과 <span class="filepath"></span>같은 새로운 이미지가 추가되면 파일에 대한 매개 변수가 동일할 경우 추가 구성이 필요하지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 타일 압축 품질 </td> 
   <td colname="col2"> <p>모든 소스에 대한 선택 사항입니다. JPEG 압축의 경우 이미지 크기 및 품질 균형을 조정하는 방법을 지정하는 0에서 100까지의 정수입니다. 기본값은 0입니다. 숫자가 높을수록 이미지 품질은 향상되지만 데이터 워크벤치 사용자는 더 큰 이미지와 더 긴 다운로드 시간을 생성합니다. </p> <p>70 미만의 이미지를 압축하면 이미지 저하가 발생할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 타일 압축기 </td> 
   <td colname="col2"> 모든 소스에 대한 선택 사항입니다. 출력 파일을 쓰는 데 사용할 압축 방법을 지정합니다. 현재 지원되는 유일한 방법은 RAWRGB(기본값, 압축 안 함)와 JPEG입니다. JPEG 압축을 사용하면 프로필 동기화 동안 전송되는 레이어 크기를 줄일 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 너비 </td> 
   <td colname="col2"> 투영되지 않은 원시 비트맵 이미지에 필요합니다. 소스 이미지의 너비(픽셀 단위)입니다. </td> 
  </tr> 
 </tbody> 
</table>

1. 다음 표를 가이드로 사용하여 소스 이미지 위치, 임시 이미지 저장소 및 레이어 쓰기를 매개 변수에 편집합니다. 이러한 매개 변수는 이 파일의 소스 섹션에서 정의하는 모든 지형 이미지 소스에 적용됩니다.

   | 매개 변수 | 설명 |
   |---|---|
   | 소스 이미지 위치 | 필수 여부. 이미지를 스캔하여 지형 레이어로 변환할 수 있는 디렉토리입니다. 절대 경로가 아닌 경우 데이터 워크벤치 서버 설치 디렉토리에 대해 상대 경로로 해석됩니다. |
   | 임시 이미지 저장소 | 선택 사항입니다. 소스 이미지를 지형 레이어로 변환하는 데 사용되는 임시 파일을 저장하는 데 사용되는 디렉토리의 이름입니다. 절대 경로가 아닌 경우 데이터 워크벤치 서버 설치 디렉토리에 대해 상대 경로로 해석됩니다. 기본 위치는 임시 디렉토리입니다. |
   | 레이어 쓰기 대상 | 필수 여부. 지형 레이어가 출력되는 디렉토리입니다. 일반적으로 프로필 디렉토리의 Maps 하위 디렉토리이므로 시각화가 레이어를 찾을 수 있습니다. [!DNL Globe] |

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭하여 파일을 저장합니다 **[!UICONTROL Save]**.

1. 업데이트된 파일을 데이터 워크벤치 서버 시스템에 저장하려면 [!DNL Server Files Manager]열에서 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Terrain Images.cfg] > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *을 클릭합니다&#x200B;**[!UICONTROL server name]***.

