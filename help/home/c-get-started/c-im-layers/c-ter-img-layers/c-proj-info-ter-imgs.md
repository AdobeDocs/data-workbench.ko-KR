---
description: 데이터 워크벤치에서는 모든 지형 이미지 레이어 소스에 대한 위도 경도 예상치와 UTM(Universal Transverse Mercator) 예상치를 모두 지원합니다.
title: 지형 이미지에 대한 투영 정보 지정
uuid: cc1e1e35-6b23-4121-a9f5-489001cb2ef8
exl-id: 2638c5d4-164d-411b-8464-0a3af81b6537
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 3%

---

# 지형 이미지에 대한 투영 정보 지정{#specify-projection-information-for-terrain-images}

데이터 워크벤치에서는 모든 지형 이미지 레이어 소스에 대한 위도 경도 예상치와 UTM(Universal Transverse Mercator) 예상치를 모두 지원합니다.

투영 정보는 투영되지 않은 원시 비트맵과 투영되지 않은 일반 이미지에 필요합니다. 투영 매개 변수가 이미지 자체에 포함된 지리 데이터(geometric data)에서 자동으로 결정되므로 일반적으로 필요하지 않지만 포함된 투영 정보가 있는 이미지에 대한 투영 정보를 지정할 수 있습니다. 다음 섹션에서는 [!DNL Terrain Images.cfg] 파일에서 이러한 투영 형식을 지정하는 방법에 대한 세부 정보를 제공합니다.

## 위도-경도 예측 {#section-6e335357ec28462ba39c565e0a5986c7}

[!DNL Terrain Images.cfg] 파일의 위도 경도 투영 형식(LatLonProjection)은 위도 및 경도의 4개의 매개 변수로 정의됩니다.

투영되지 않은 이미지(투영되지 않은 원시 비트맵 및 일반 이미지, 투영되지 않은 이미지)에 LatLonProjection을 지정하려면 Data Workbench의 [!DNL Terrain Images.cfg] 창 내에 LatLonProjection에 대한 설정을 입력할 수 있습니다.

포함된 투영 정보가 있는 이미지에 LatLonProjection을 지정하려면 메모장과 같은 텍스트 편집기에서 [!DNL Terrain Images.cfg] 파일을 열고 투영 정보 매개 변수를 LatLonProjection으로 설정하고 [!DNL LatLonProjection]에 대한 설정을 추가해야 합니다.

**투영되지 않은 이미지에 대해 LatLonProjection을 지정하려면**

1. [!DNL Terrain Images.cfg] 파일을 Data Workbench에서 열고 [지형 이미지 레이어를 정의하려면 ](../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-ter-img-layers.md#concept-f4b3a20969354ca38955e3fd5beb0f4f)에 설명된 대로 지형 이미지 레이어 소스를 추가합니다.
1. 다음 매개변수 테이블을 안내선으로 사용하여 투영 정보 매개변수를 편집합니다.

<table id="table_32F6EADB2DA34592ABD6FFAC9E00BB27"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>마지막0 </p> </td> 
   <td colname="col2"> <p>이미지의 맨 위 가장자리 위도가 90은 북극이고 -90은 남극입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>최근1 </p> </td> 
   <td colname="col2"> <p>이미지의 아래쪽 가장자리 위도입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lon0 </p> </td> 
   <td colname="col2"> <p>이미지의 왼쪽 가장자리의 경도(도)로, 양수가 동이고 음수가 서쪽인 경우 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lon1 </p> </td> 
   <td colname="col2"> <p>이미지의 오른쪽 가장자리 경도입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭하여 파일을 저장합니다.
1. Data Workbench 서버 컴퓨터에 로컬로 변경한 내용을 저장하려면 [!DNL Server Files Manager]에서 [!DNL Temp] 열에서 [!DNL Terrain Images.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;을 클릭합니다.

**포함된 투영 정보 내의 이미지에 대한 LatLonProjection을 지정하려면**

[!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 콘텐트를 봅니다. [!DNL Terrain Images.cfg] 파일이 이 디렉터리 내에 있습니다.

[!DNL Terrain Images.cfg]에 대한 서버 이름 열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Make Local]** 을 클릭합니다. [!DNL Terrain Images.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.

[!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**&#x200B;를 클릭합니다. [!DNL Terrain Images.cfg] 파일이 메모장 창에 나타납니다.

다음 샘플 파일 조각을 안내선으로 사용하여 투영 정보 매개변수를 편집합니다. 투영 유형을 아래에 강조 표시된 것으로 지정해야 합니다. 매개 변수에 대한 설명은 이전 절차의 LatLonProjection 매개 변수 표를 참조하십시오.

```
Projection Info = LatLonProjection:
  Lat0 = double: 90
  Lat1 = double: -90
  Lon0 = double: -180
  Lon1 = double: 180
```

## 범용 교차 지표 예측 {#section-606df0ed1c2d4a6bac3ff0fa2cfb3e82}

UTM(Universal Transverse Mercator) 투영은 8개의 매개 변수로 정의됩니다. 지형 이미지 레이어에 대해 Universal Transverse Mercator 투영을 지정할 때 지형 이미지 파일은 이미지 위쪽을 향해 false(투영된) 북쪽으로 정렬하고 이미지 오른쪽에 거짓 동쪽을 기준으로 정렬해야 합니다.

모든 지형 이미지 소스에 대한 UTM 투영을 지정하려면 메모장과 같은 텍스트 편집기에서 [!DNL Terrain Images.cfg] 파일을 열고 [투영 정보] 매개 변수를 &quot;TransverseMercatorProjection&quot;으로 설정하고 UTM 투영에 대한 설정을 추가해야 합니다.

**범용 가로 병합 투영 지정하기**

1. [!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 콘텐트를 봅니다. [!DNL Terrain Images.cfg] 파일이 이 디렉터리 내에 있습니다.
1. [!DNL Terrain Images.cfg]에 대한 서버 이름 열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Make Local]** 을 클릭합니다. [!DNL Terrain Images.cfg.]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.
1. [!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**&#x200B;를 클릭합니다. [!DNL Terrain Images.cfg] 파일이 메모장 창에 나타납니다.
1. 다음 샘플 파일 조각 및 매개변수 테이블을 안내선으로 사용하여 투영 정보 매개변수를 편집합니다. 투영 유형을 아래에 강조 표시된 것으로 지정해야 합니다.

   ```
   Projection Info = TransverseMercatorProjection:
     Ellipsoid Inverse Flattening = double: 294.9786982139006
     Ellipsoid Semimajor Axis = double: 6378206.4000000004
     False Easting = double: 500000
     False Northing = double: 0
     Northwest Corner Coordinates = v3d: (550339, 5.42059e+006, 0)
     Prime Meridian = double: -123
     Scale Factor = double: 0.9996
     Southeast Corner Coordinates = v3d: (555099, 5.41356e+006, 0)
   ```

<table id="table_71AEEAE808B9436B9846987A54D5D1D2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>타원 반전 병합, 타원 반축 </p> </td> 
   <td colname="col2"> <p>투영에 사용되는 타원 매개 변수입니다. 반축 은 미터 단위로 지정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>False Easting </p> </td> 
   <td colname="col2"> <p>투영 중경에서 오직하는 길이 미터 단위. UTM의 경우 항상 500,000입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>False Northing </p> </td> 
   <td colname="col2"> <p>적도의 잘못된 북쪽, 즉 미터로. UTM의 경우 북반구 지역은 0이고 남반구 지역은 10,000입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>북서쪽 모퉁이 좌표, 남동쪽 모퉁이 좌표 </p> </td> 
   <td colname="col2"> <p>이미지의 왼쪽 위 및 오른쪽 아래 모서리의 좌표(투영된 미터)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Primerid </p> </td> 
   <td colname="col2"> <p>그리니치의 동쪽에 지정된 투영 중앙 경도의 경도입니다. 음수가 서쪽을 지정하는 데 사용될 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비율 인수 </p> </td> 
   <td colname="col2"> <p>투영 원통의 반지름을 타원형의 반지축에 대한 비율입니다. UTM(Universal Transverse Mercator) 예상치에 대해서는 항상 0.9996입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
