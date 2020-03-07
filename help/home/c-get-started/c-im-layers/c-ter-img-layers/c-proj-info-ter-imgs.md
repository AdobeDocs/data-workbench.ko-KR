---
description: 데이터 워크벤치에서는 모든 지형 이미지 레이어 소스에 대한 위도 경도 예상치와 UTM(Universal Transverse Mercator) 예상치를 모두 지원합니다.
solution: Analytics
title: 지형 이미지에 대한 투영 정보 지정
topic: Data workbench
uuid: cc1e1e35-6b23-4121-a9f5-489001cb2ef8
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 지형 이미지에 대한 투영 정보 지정{#specify-projection-information-for-terrain-images}

데이터 워크벤치에서는 모든 지형 이미지 레이어 소스에 대한 위도 경도 예상치와 UTM(Universal Transverse Mercator) 예상치를 모두 지원합니다.

투영 정보는 투영되지 않은 원시 비트맵과 투영되지 않은 일반 이미지에 필요합니다. 프로젝션 매개 변수가 이미지 자체에 포함된 지리 데이터에서 자동으로 결정되므로 일반적으로 필요하지 않지만 임베드된 투영 정보가 있는 이미지에 대한 투영 정보를 지정할 수 있습니다. 다음 섹션에서는 [!DNL Terrain Images.cfg] 파일에서 이러한 투영 형식을 지정하는 방법에 대한 세부 정보를 제공합니다.

## 위도-경도 예측 {#section-6e335357ec28462ba39c565e0a5986c7}

파일의 위도 경도 투영 형식(LatLonProjection)은 위도 및 경도의 네 가지 매개 변수로 정의됩니다. [!DNL Terrain Images.cfg]

투영되지 않은 이미지(투영되지 않은 원시 비트맵 및 일반 이미지, 투영되지 않은 이미지)에 대한 LatLonProjection을 지정하려면 데이터 워크벤치의 창 내에 LatLonProjection에 대한 설정을 입력할 수 [!DNL Terrain Images.cfg] 있습니다.

임베드된 투영 정보가 있는 이미지에 LatLonProjection을 지정하려면 메모장과 같은 텍스트 편집기에서 [!DNL Terrain Images.cfg] 파일을 열고 투영 정보 매개 변수를 LatLonProjection으로 설정한 다음 [!DNL LatLonProjection]에 대한 설정을 추가해야 합니다.

**투영되지 않은 이미지에 대해 LatLonProjection을 지정하려면**

1. 데이터 워크벤치에서 [!DNL Terrain Images.cfg] 파일을 열고 지형 이미지 레이어를 [정의하려면 에 설명된 대로 지형 이미지 레이어 소스를](../../../../home/c-get-started/c-im-layers/c-ter-img-layers/c-ter-img-layers.md#concept-f4b3a20969354ca38955e3fd5beb0f4f)추가합니다.
1. 다음 매개변수 테이블을 가이드로 사용하여 투영 정보 매개변수를 편집합니다.

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
   <td colname="col2"> <p>이미지의 맨 위 가장자리 위도는 도 단위로, 90은 북극이고 -90은 남극입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lat1 </p> </td> 
   <td colname="col2"> <p>이미지의 아래쪽 가장자리 위도입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lon0 </p> </td> 
   <td colname="col2"> <p>이미지의 왼쪽 가장자리의 위도(도)로, 양수가 동쪽이고 음수가 서쪽인 경우 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lon1 </p> </td> 
   <td colname="col2"> <p>이미지의 오른쪽 가장자리의 경도입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭하여 파일을 저장합니다 **[!UICONTROL Save]**.
1. 로컬에서 변경한 데이터 워크벤치 서버 컴퓨터를 저장하려면 [!DNL Server Files Manager]열에서 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL Terrain Images.cfg] > [!DNL Temp] &lt; **[!UICONTROL Save to]** > *을 클릭합니다&#x200B;**[!UICONTROL server name]***.

**포함된 투영 정보 내에서 이미지에 대한 LatLonProjection을 지정하려면**

에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Components]** 봅니다. 이 [!DNL Terrain Images.cfg] 파일은 이 디렉토리 내에 있습니다.

에 대한 서버 이름 열에서 확인 표시를 마우스 오른쪽 단추로 [!DNL Terrain Images.cfg]클릭한 다음 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 에 대한 [!DNL Temp] 열에 확인 표시가 나타납니다 [!DNL Terrain Images.cfg].

열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Notepad]**&#x200B;을 클릭합니다. 파일이 메모장 창에 나타납니다 [!DNL Terrain Images.cfg] .

다음 샘플 파일 조각을 가이드로 사용하여 투영 정보 매개변수를 편집합니다. 아래 강조표시된 투영 유형을 지정해야 합니다. 매개 변수에 대한 설명은 이전 절차의 LatLonProjection 매개 변수 표를 참조하십시오.

```
Projection Info = LatLonProjection:
  Lat0 = double: 90
  Lat1 = double: -90
  Lon0 = double: -180
  Lon1 = double: 180
```

## 범용 가로 지표 예측 {#section-606df0ed1c2d4a6bac3ff0fa2cfb3e82}

UTM(Universal Transverse Mercator) 투영은 8개의 매개 변수로 정의됩니다. 지형 이미지 레이어에 대해 Universal Transverse Mercator 투영을 지정할 때 지형 이미지 파일은 이미지 위쪽으로 false(투영됨) 북쪽을 맞추고 이미지 오른쪽에 거짓 동쪽을 사용하여 정렬해야 합니다.

모든 지형 이미지 소스에 대한 UTM 투영을 지정하려면 메모장과 같은 텍스트 편집기에서 [!DNL Terrain Images.cfg] 파일을 열고 투영 정보 매개 변수를 &quot;TransverseMercatorProjection&quot;으로 설정하고 UTM 투영에 대한 설정을 추가해야 합니다.

**범용 가로 변환기 투영 지정하기**

1. 에서 [!DNL Server Files Manager]을 클릭하여 컨텐츠를 **[!UICONTROL Components]** 봅니다. 이 [!DNL Terrain Images.cfg] 파일은 이 디렉토리 내에 있습니다.
1. 에 대한 서버 이름 열에서 확인 표시를 마우스 오른쪽 단추로 [!DNL Terrain Images.cfg]클릭한 다음 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 열에 확인 표시가 나타납니다. [!DNL Temp][!DNL Terrain Images.cfg.]
1. 열에서 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Temp] > **[!UICONTROL Open]** **[!UICONTROL in Notepad]**&#x200B;을 클릭합니다. 파일이 메모장 창에 나타납니다 [!DNL Terrain Images.cfg] .
1. 다음 샘플 파일 조각 및 매개변수 테이블을 안내선으로 사용하여 투영 정보 매개변수를 편집합니다. 아래 강조표시된 투영 유형을 지정해야 합니다.

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
   <td colname="col1"> <p>줄임표 역 병합, 줄임표 세마조 축 </p> </td> 
   <td colname="col2"> <p>투영에 사용되는 줄임표의 매개 변수입니다. 세미나 축은 미터 단위로 지정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>False Easting </p> </td> 
   <td colname="col2"> <p>투영된 중앙 경선의 오동방향(미터 단위). UTM의 경우 항상 500,000입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>False Northing </p> </td> 
   <td colname="col2"> <p>적도의 잘못된 북쪽, 즉 미터로. UTM의 경우, 이것은 북반구 지역의 경우 0이고 남반구 지역의 경우 10,000입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>북서쪽 모서리 좌표, 남동 모서리 좌표 </p> </td> 
   <td colname="col2"> <p>이미지의 왼쪽 상단 및 오른쪽 하단 모서리의 좌표(투영된 미터)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Prime Meridian </p> </td> 
   <td colname="col2"> <p>그리니치의 동쪽에 지정된 투영 중경도의 경도입니다. 음수는 서쪽으로 도 지정에 사용될 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비율 계수 </p> </td> 
   <td colname="col2"> <p>투영 원통의 반지름과 타원형의 반지름의 비율입니다. UTM(Universal Transverse Mercator) 예측의 경우 항상 0.9996입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

