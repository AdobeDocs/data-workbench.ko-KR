---
description: Data Workbench는 모든 지형 이미지 레이어 소스에 대한 위도-경도 예측 및 UTM(범용 교차 지표) 예측을 모두 지원합니다.
title: 지형 이미지에 대한 투영 정보 지정
uuid: cc1e1e35-6b23-4121-a9f5-489001cb2ef8
exl-id: 2638c5d4-164d-411b-8464-0a3af81b6537
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 3%

---

# 지형 이미지에 대한 투영 정보 지정{#specify-projection-information-for-terrain-images}

Data Workbench는 모든 지형 이미지 레이어 소스에 대한 위도-경도 예측 및 UTM(범용 교차 지표) 예측을 모두 지원합니다.

투영 정보는 투영되지 않은 원시 비트맵과 투영되지 않은 일반 이미지에 필요합니다. 투영 정보가 포함된 이미지에 대한 투영 정보를 지정할 수 있지만, 투영 매개변수는 이미지 자체에 포함된 지리 데이터에서 자동으로 결정되므로 필요하지 않습니다. 다음 섹션에서는 [!DNL Terrain Images.cfg] 파일에서 이러한 투영 형식을 지정하는 방법에 대한 세부 정보를 제공합니다.

## 위도-경도 예측 {#section-6e335357ec28462ba39c565e0a5986c7}

[!DNL Terrain Images.cfg] 파일의 위도-경도 투영 형식(LatLonProjection)은 위도와 경도의 네 개의 매개 변수로 정의됩니다.

투영되지 않은 이미지(투영되지 않은 원시 비트맵 및 일반 이미지, 투영되지 않은 이미지)에 대한 LatLonProjection을 지정하려면 Data Workbench의 [!DNL Terrain Images.cfg] 창 내에 LatLonProjection에 대한 설정을 입력할 수 있습니다.

포함된 투영 정보가 있는 이미지에 대한 LatLonProjection을 지정하려면 메모장과 같은 텍스트 편집기에서 [!DNL Terrain Images.cfg] 파일을 열고 투영 정보 매개 변수를 LatLonProjection으로 설정하고 [!DNL LatLonProjection]에 대한 설정을 추가해야 합니다.

**투영되지 않은 이미지에 대한 LatLonProjection을 지정하려면**

1. Data Workbench에서 [!DNL Terrain Images.cfg] 파일을 열고 [지형 이미지 레이어를 정의하려면 ](../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-ter-img-layers.md#concept-f4b3a20969354ca38955e3fd5beb0f4f)에 설명된 대로 지형 이미지 레이어 소스를 추가합니다.
1. 다음 매개변수 테이블을 안내서로 사용하여 투영 정보 매개변수를 편집합니다.

<table id="table_32F6EADB2DA34592ABD6FFAC9E00BB27"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Lat0 </p> </td> 
   <td colname="col2"> <p>영상의 위쪽 가장자리의 위도인 도(도)로 90은 북극이고 -90은 남극이다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lat1 </p> </td> 
   <td colname="col2"> <p>이미지 하단 가장자리의 위도입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lon0 </p> </td> 
   <td colname="col2"> <p>영상의 왼쪽 가장자리 경도로서, 양수가 동이고 음수가 서쪽입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lon1 </p> </td> 
   <td colname="col2"> <p>이미지의 오른쪽 가장자리 경도입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭하여 파일을 저장합니다.
1. 로컬로 수행된 변경 내용을 Data Workbench 서버 컴퓨터에 저장하려면 [!DNL Server Files Manager] 열에서 [!DNL Terrain Images.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]***&#x200B;를 클릭합니다.[!DNL Temp]

**포함된 투영 정보 내의 이미지에 대한 LatLonProjection을 지정하기**

[!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 해당 콘텐츠를 봅니다. [!DNL Terrain Images.cfg] 파일이 이 디렉터리 내에 있습니다.

서버 이름 열의 [!DNL Terrain Images.cfg] 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Make Local]** 을 클릭합니다. [!DNL Terrain Images.cfg]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다.

[!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]** 를 클릭합니다. [!DNL Terrain Images.cfg] 파일이 메모장 창에 나타납니다.

다음 샘플 파일 조각을 안내서로 사용하여 투영 정보 매개변수를 편집합니다. 투영 유형을 아래에 강조 표시된 대로 지정해야 합니다. 매개 변수에 대한 설명은 이전 절차의 LatLonProjection 매개 변수 테이블을 참조하십시오.

```
Projection Info = LatLonProjection:
  Lat0 = double: 90
  Lat1 = double: -90
  Lon0 = double: -180
  Lon1 = double: 180
```

## 범용 교차 지표 예측 {#section-606df0ed1c2d4a6bac3ff0fa2cfb3e82}

UTM(Universal Transverse Mercator) 프로젝션은 8개의 매개 변수로 정의됩니다. 지형 이미지 레이어에 대해 범용 교차 지표 투영을 지정할 때 지형 이미지 파일은 이미지의 맨 위 방향으로 false(투영됨) 북쪽으로 정렬되고 이미지의 오른쪽 방향으로 false로 정렬되어야 합니다.

지형 이미지 소스에 대한 UTM 투영을 지정하려면 메모장과 같은 텍스트 편집기에서 [!DNL Terrain Images.cfg] 파일을 열고 투영 정보 매개 변수를 &quot;TransverseMercatorProjection&quot;으로 설정하고 UTM 투영에 대한 설정을 추가해야 합니다.

**범용 교차 지표 투영 지정하기**

1. [!DNL Server Files Manager]에서 **[!UICONTROL Components]**&#x200B;을 클릭하여 해당 콘텐츠를 봅니다. [!DNL Terrain Images.cfg] 파일이 이 디렉터리 내에 있습니다.
1. 서버 이름 열의 [!DNL Terrain Images.cfg] 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Make Local]** 을 클릭합니다. [!DNL Terrain Images.cfg.]에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다
1. [!DNL Temp] 열에서 새로 만든 확인 표시를 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]** 를 클릭합니다. [!DNL Terrain Images.cfg] 파일이 메모장 창에 나타납니다.
1. 다음 샘플 파일 조각 및 매개변수 테이블을 안내선으로 사용하여 투영 정보 매개변수를 편집합니다. 투영 유형을 아래에 강조 표시된 대로 지정해야 합니다.

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
   <td colname="col1"> <p>타원 역 평탄화, 타원 반조축 </p> </td> 
   <td colname="col2"> <p>투영에 사용되는 줄임표의 매개 변수입니다. 반축축은 미터 단위로 지정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>거짓 이스팅 </p> </td> 
   <td colname="col2"> <p>투영법 중앙 경락의 잘못된 동쪽을 미터 단위로. UTM의 경우 항상 50만 개입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>잘못된 노링 </p> </td> 
   <td colname="col2"> <p>적도의 잘못된 북구, 즉 수 미터 단위. UTM의 경우, 이것은 북반구 지역은 0이고, 남반구 지역은 1만입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>북서쪽 모서리 좌표, 남동 코너 좌표 </p> </td> 
   <td colname="col2"> <p>이미지의 왼쪽 상단 및 오른쪽 하단 모서리의 좌표(투영된 미터)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>경락 </p> </td> 
   <td colname="col2"> <p>그리니치의 동쪽에 지정된 투영 중앙 경도의 경도입니다. 음수는 서쪽으로 도 지정을 위해 사용될 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>배율 계수 </p> </td> 
   <td colname="col2"> <p>투영 실린더의 반경과 타원의 반조축에 대한 비율입니다. UTM(범용 교차 지표) 예측의 경우 항상 0.9996입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
