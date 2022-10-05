---
description: Data Workbench에서 지형 이미지 레이어는 지구의 지형 이미지를 표시합니다.
title: 지형 이미지 레이어 작업
uuid: 2f23a2c8-f551-4b84-bd87-5d7053910ab3
exl-id: 22026b41-4e12-4247-b019-461ae223bd07
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 2%

---

# 지형 이미지 레이어 작업{#working-with-terrain-image-layers}

{{eol}}

Data Workbench에서 지형 이미지 레이어는 지구의 지형 이미지를 표시합니다.

지형 이미지 레이어는 [!DNL Geography] profile(사용자 지정 형식) 이러한 이미지 레이어는 Adobe에서 생성할 수 있습니다. 또는 Data Workbench 서버가 사용자가 제공하는 지형 이미지를 지구 시각화에서 사용할 수 있는 지형 레이어로 변환할 수 있습니다.

>[!NOTE]
>
>지형 이미지 레이어로 작업하려면 [!DNL Terrain Images.cfg] Adobe이 제공한 파일입니다. 설치 지침은 [Data Workbench Geography 설치](../../../../home/c-geo-oview/c-inst-geo/c-inst-geo.md).

지형 이미지 레이어를 정의하려면 다음을 수행해야 합니다.

* **하나 이상의 지형 이미지 파일** 전방에 표시할 이미지를 포함합니다.
* **Terrain Images.cfg** 레이어에 사용할 지형 이미지 파일을 지정하는 파일입니다. 다음 [!DNL Terrain Images.cfg] 파일을 사용하면 하나 이상의 소스를 추가하여 지형 이미지 레이어를 만들 수 있습니다. 지형 이미지 파일의 형식은 추가해야 하는 소스 유형을 결정합니다. 다음 표에서는 지원되는 지형 이미지 파일 형식을 포함하여 사용 가능한 지형 이미지 레이어 소스에 대한 설명을 제공합니다.

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
   <td colname="col2"> <p>24비트 헤드리스 RGB 파일에서 위도-경도 정렬(투영되지 않음)된 지형 이미지 레이어를 생성합니다. 여기서 북은 이미지 상단이고 동쪽은 오른쪽에 있습니다. </p> <p>지원되는 이미지 형식: RAW </p> <p> <p>참고: 이 소스에는 투영 정보가 필요합니다. 투영 형식에 대한 자세한 내용은 <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> 지형 이미지에 대한 투영 정보 지정</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 일반 이미지, 투영되지 않음 </td> 
   <td colname="col2"> <p>24비트, 위도-경도 정렬(투영되지 않은) 이미지 형식으로 지형 이미지 레이어를 만듭니다. 여기서 북은 이미지의 상단이고 동쪽은 오른쪽에 있습니다. </p> <p>지원되는 이미지 형식: BMP, JPG, PNG, TIFF </p> <p> <p>참고: 이 소스에는 투영 정보가 필요합니다. 투영 형식에 대한 자세한 내용은 <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> 지형 이미지에 대한 투영 정보 지정</a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 포함된 투사가 있는 이미지 </td> 
   <td colname="col2"> <p>이미지 파일에 지리 데이터를 포함하는 이미지 형식에서 지형 이미지 레이어를 만듭니다. 이미지에서 투영 정보가 추출됩니다. </p> <p>지원되는 이미지 형식: Erdas(IMG), GeoTIFF </p> <p> <p>참고: 이 소스는 일반적으로 프로젝션 정보가 필요하지 않지만 필요한 경우 이러한 정보의 추가를 지원합니다. 투영 형식에 대한 자세한 내용은 <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> 지형 이미지에 대한 투영 정보 지정</a>. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**지형 이미지 레이어를 정의하려면**

1. Data Workbench에서 [!DNL Admin] > [!DNL Dataset and Profile] 탭에서 **[!UICONTROL Servers Manager]** 축소판 그림을 클릭하여 열기 [!DNL Servers Manager] 작업 공간.

1. 내 [!DNL Servers Manager] 창에서 원하는 data workbench 서버 아이콘을 마우스 오른쪽 단추로 클릭하고 를 클릭합니다. **[!UICONTROL Server Files]**.

1. 에서 [!DNL Server Files Manager]를 클릭합니다. **[!UICONTROL Components]** 콘텐츠를 보려면 클릭하십시오. 다음 [!DNL Terrain Images.cfg] 파일이 이 디렉터리 내에 있습니다.

1. 서버 이름 열의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Terrain Images.cfg]를 클릭한 다음 **[!UICONTROL Make Local]**. 에 확인 표시가 나타납니다 [!DNL Temp] 열 [!DNL Terrain Images.cfg.]

1. 에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Temp] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. 다음 [!DNL Terrain Images.cfg]창이 나타납니다.

1. 에서 [!DNL Terrain Images] 창 **[!UICONTROL component]** 콘텐츠를 보려면 클릭하십시오.

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Sources]** > **[!UICONTROL Add new]** 다음 소스 유형 중 하나를 선택합니다.

   * **[!UICONTROL Raw unprojected bitmap]** 구문을 사용하는 키-값 쌍으로 전달됩니다. (이 소스 유형이 추가되면 [!DNL Terrain Images] 창을 엽니다.)

   * **[!UICONTROL General image, unprojected]** 구문을 사용하는 키-값 쌍으로 전달됩니다. (이 소스 유형이 추가되면, [!DNL Terrain Images] 창을 엽니다.)

   * **[!UICONTROL Image with embedded projection]** 구문을 사용하는 키-값 쌍으로 전달됩니다. (이 소스 유형이 추가되면, [!DNL Terrain Images] 창을 엽니다.)

1. 다음 샘플 파일 및 매개변수 테이블을 안내서로 사용하여 필요에 따라 소스의 매개변수를 편집합니다.

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
   <td colname="col2"> 모든 소스에 대해 선택 사항입니다. 소스 이미지에 적용할 감마 수정을 지정합니다. 이는 Data Workbench가 일반적으로 높은 감마 설정을 사용하여 실행되기 때문에 바람직할 수 있습니다. 기본값은 1입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 높이 </td> 
   <td colname="col2"> 투영되지 않은 원시 비트맵 이미지에 필요합니다. 소스 이미지의 높이(픽셀 단위)입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 투영 정보 </td> 
   <td colname="col2"> <p>투영되지 않은 원시 비트맵 이미지 및 일반 이미지에 필요하나 투영되지 않지만 포함된 영상의 경우 지원됩니다. Data Workbench<span class="wintitle"> Geography</span> 은 지형 이미지 레이어에 대한 위도-경도 예측 및 TM(Transverse Mercator) 예측을 지원합니다. 기본 투영 형식은 위도-경도 투영(LatLonProjection)입니다. </p> <p>투영 형식에 대한 자세한 내용은 <a href="../../../../home/c-geo-oview/c-wk-img-lyrs/c-trn-img-lyrs/c-proj-info-trn-imgs/c-proj-info-trn-imgs.md#concept-69b0c668038f4de9bf430a3a468a2abd"> 지형 이미지에 대한 투영 정보 지정</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 소스 이미지 </td> 
   <td colname="col2">모든 소스에 필요합니다. 소스 이미지 파일의 이름입니다. 파일 이름이나 와일드카드 패턴일 수 있습니다. 패턴을 사용하면 연관된 메타데이터가 변경되지 않고 다른 날짜에 있는 동일한 영역에 대한 이미지를 업로드하는 경우 유용할 수 있습니다. 따라서 "<span class="filepath"> Tysons Corner *.raw</span>" <span class="filepath"> Tysons Corner 050211.raw</span>, <span class="filepath"> Tysons Corner 050218.raw</span>및 를 추가할 때 파일의 매개 변수가 동일하면 추가 구성이 필요 없이 새 이미지가 추가됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 타일 압축 품질 </td> 
   <td colname="col2"> <p>모든 소스에 대해 선택 사항입니다. JPEG 압축의 경우 0에서 100까지의 정수로 이미지 크기와 품질의 균형을 조정하는 방법을 지정합니다. 기본값은 0입니다. 숫자가 높을수록 이미지 품질이 향상되지만 Data Workbench 사용자에 대해 더 큰 이미지와 더 긴 다운로드 시간이 생성됩니다. </p> <p>70보다 작은 이미지를 압축하면 이미지가 저하될 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 타일 압축기 </td> 
   <td colname="col2"> 모든 소스에 대해 선택 사항입니다. 출력 파일을 작성하는 데 사용되는 압축 방법을 지정합니다. 현재 지원되는 유일한 방법은 RAWRGB(기본값, 압축 안 함) 및 JPEG입니다. JPEG 압축을 사용하면 프로필 동기화 중에 전송되는 레이어의 크기를 줄일 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 너비 </td> 
   <td colname="col2"> 투영되지 않은 원시 비트맵 이미지에 필요합니다. 소스 이미지의 너비(픽셀 단위)입니다. </td> 
  </tr> 
 </tbody> 
</table>

1. 다음 표를 안내서로 사용하여 소스 이미지 위치, 임시 이미지 저장소 및 레이어 쓰기 매개 변수를 편집합니다. 이러한 매개 변수는 이 파일의 소스 섹션에서 정의한 모든 지형 이미지 소스에 적용됩니다.

   | 매개 변수 | 설명 |
   |---|---|
   | 소스 이미지 위치 | 필수 여부. 이미지가 지형 레이어로 변환되도록 스캔되는 디렉토리입니다. 절대 경로가 아닌 경우 Data Workbench 서버 설치 디렉토리에 대해 해석됩니다. |
   | 임시 이미지 저장소 | 선택 사항. 소스 이미지를 지형 레이어로 변환하는 데 사용되는 임시 파일을 저장하는 데 사용되는 디렉토리 이름입니다. 절대 경로가 아닌 경우 Data Workbench 서버 설치 디렉토리에 대해 해석됩니다. 기본 위치는 Temp 디렉터리입니다. |
   | 레이어 쓰기 대상 | 필수 여부. 지형 레이어가 출력되는 디렉토리입니다. 일반적으로 프로필 디렉토리의 Map 하위 디렉토리이므로 [!DNL Globe] 시각화가 레이어를 찾을 수 있습니다. |

1. 마우스 오른쪽 단추를 클릭하여 파일을 저장합니다 **[!UICONTROL (modified)]** 창 상단에서 **[!UICONTROL Save]**.

1. 업데이트된 파일을 Data Workbench 서버 시스템에 저장하려면 [!DNL Server Files Manager]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL Terrain Images.cfg] 에서 [!DNL Temp] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.
