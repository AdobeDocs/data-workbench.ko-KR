---
description: 요소 점 레이어 파일에 대한 서식 정보.
solution: Analytics
title: 요소 점 레이어 파일 형식
topic: Data workbench
uuid: a8b3d2f4-0ed2-480d-a2a6-75d43025a579
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 요소 점 레이어 파일 형식{#element-point-layer-file-format}

요소 점 레이어 파일에 대한 서식 정보.

조회 파일을 참조하는 각 요소 포인트 레이어 [!DNL .layer] 파일의 형식은 다음 템플릿을 사용하여 지정해야 합니다.

```
Layer = ElementPointLayer:
  Data Paths = vector: 1 items
    0 = Path: Maps\\Lookup File Name.txt
  Longitude Column = string: Longitude Column Name
  Latitude Column = string: Latitude Column Name
  Name Column = string: Location Column Name
  Key Column = string: Key Column Name
  Dimension = ref: wdata/model/dim/Dimension Name
  Metric = ref: wdata/model/metric/Metric Name
  Scale = double: Scale
  Color = v3d: RGB Color Vector
  Rendering Mode = int: Mode Number
```

<table id="table_B2BC5FE8C80E4680B9A565878192D75B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 데이터 경로 </td> 
   <td colname="col2"> 위도 및 경도 데이터를 포함하는 조회 파일의 경로입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 경도 열 </td> 
   <td colname="col2"> 경도 데이터를 포함하는 조회 파일의 열 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 위도 열 </td> 
   <td colname="col2"> 위도 데이터를 포함하는 조회 파일의 열 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이름 열 </td> 
   <td colname="col2"> 선택 사항입니다. 위도 및 경도 데이터로 표시되는 위치의 이름이 들어 있는 조회 파일의 열 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 키 열 </td> 
   <td colname="col2"> <p>데이터 워크벤치 서버가 조회 파일의 데이터를 데이터 세트에 통합할 수 있도록 하는 공통 키 데이터를 포함하는 조회 파일의 열 이름입니다. 조회 파일의 첫 번째 열이어야 합니다. </p> <p>이 열의 각 행은 차원의 요소입니다. 이 차원은 Transformation.cfg <span class="filepath"> 파일에서</span> 정의되어야 하거나 변형 데이터 세트에 파일이 포함되고 이 파일의 Dimension 매개 변수에 지정되어야 합니다. 변형 구성 파일에 대한 자세한 내용은 데이터 세트 구성 <i>안내서를 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 차원 </td> 
   <td colname="col2">키 열의 데이터 행에 해당하는 요소를 포함하는 차원(변환 구성 파일에 정의)의 <span class="wintitle"> 이름입니다</span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지표 </td> 
   <td colname="col2"> 차원 매개 변수에 지정된 차원 위에 평가되는 지표의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 비율 조정 </td> 
   <td colname="col2"> 선택 사항입니다. 레이어의 포인트 크기를 지정하는 데 사용되는 값입니다. 기본값은 100입니다. 값이 클수록 점이 커지고 값이 작을수록 점이 커집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 색상 </td> 
   <td colname="col2"> 선택 사항입니다. RGB 색상 벡터로 표현됩니다(빨강,녹색,파랑). 벡터의 각 색상에 대해 0.0부터 1.0까지의 값을 입력할 수 있습니다.예를 들어 (1.0, 0.0, 0.0)은 밝은 빨강이고 (0.5, 0.5, 0.5)는 회색입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 렌더링 모드 </td> 
   <td colname="col2"> <p>선택 사항입니다. 레이어에 사용할 렌더링 모드를 나타내는 정수 값입니다. 사용 가능한 세 가지 모드는 다음과 같습니다. 
     <ul id="ul_CBB26B32505846A39FEB85E831E1C7AB"> 
      <li id="li_B31528A8858C4418ABCDFF0B4EFB25D7">렌더링 모드 1. 포인트 크기는 화면 공간에 정의됩니다(포인트는 컴퓨터 화면에 따라 일정한 크기로 유지됨). 점은 다각형을 사용하여 렌더링되므로 포인트 크기에 대한 상한을 두지 않습니다. 기본 렌더링 모드입니다. </li> 
      <li id="li_CA0C3E0DBF004ADBB4D7819C0BF192FC">렌더링 모드 2. 포인트 크기는 월드 공간에서 정의됩니다(포인트는 지구 크기를 기준으로 일정하게 유지). 점은 다각형을 사용하여 렌더링되므로 포인트 크기에 대한 상한을 두지 않습니다. </li> 
      <li id="li_8F8729976DDB434D869E81D4381E2688">렌더링 모드 3. 포인트 크기는 화면 공간에 정의됩니다. 점은 OpenGL 부드러운 점을 사용하여 렌더링됩니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

파일의 [!DNL Zip Points.layer] 형식은 다음과 같습니다.

```
Layer = ElementPointLayer:
  Data Paths = vector: 1 items
    0 = Path: Maps\\Zip Points.txt
  Longitude Column = string: LONGITUDE
  Latitude Column = string: LATITUDE
  Name Column = string: NAME
  Key Column = string: ZIP_CODE
  Dimension = ref: wdata/model/dim/Zipcode
  Metric = ref: wdata/model/metric/Sessions
```

