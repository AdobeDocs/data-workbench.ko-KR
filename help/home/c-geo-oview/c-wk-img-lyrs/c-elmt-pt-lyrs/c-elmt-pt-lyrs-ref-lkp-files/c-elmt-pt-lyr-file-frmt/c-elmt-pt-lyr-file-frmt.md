---
description: 요소 점 레이어 파일에 대한 서식 정보.
title: 요소 점 레이어 파일 형식
uuid: a8b3d2f4-0ed2-480d-a2a6-75d43025a579
exl-id: 125796f6-a447-4f12-bcf2-3e669783cf1e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 5%

---

# 요소 점 레이어 파일 형식{#element-point-layer-file-format}

{{eol}}

요소 점 레이어 파일에 대한 서식 정보.

각 요소 점 레이어 [!DNL .layer] 조회 파일을 참조하는 파일은 다음 템플릿을 사용하여 포맷해야 합니다.

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
   <td colname="col2"> 위도 데이터가 포함된 조회 파일의 열 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이름 열 </td> 
   <td colname="col2"> 선택 사항. 위도 및 경도 데이터로 표현되는 위치의 이름이 들어 있는 조회 파일의 열 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 키 열 </td> 
   <td colname="col2"> <p>Data Workbench 서버가 조회 파일의 데이터를 데이터 집합에 통합할 수 있도록 하는 공통 키 데이터가 포함된 조회 파일의 열 이름입니다. 조회 파일의 첫 번째 열이어야 합니다. </p> <p>이 열의 각 행은 차원의 요소입니다. 이 차원은 <span class="filepath"> Transformation.cfg</span> 파일 또는 변형 데이터 집합에는 파일을 포함하고 이 파일의 Dimension 매개 변수에 지정됩니다. 변환 구성 파일에 대한 자세한 내용은 <i>데이터 집합 구성 안내서</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 차원 </td> 
   <td colname="col2">의 데이터 행에 해당하는 요소가 들어 있는 차원(변형 구성 파일에 정의됨)의 이름입니다 <span class="wintitle"> 키</span> 열. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지표 </td> 
   <td colname="col2"> Dimension 매개 변수에 지정된 차원을 통해 평가되는 지표의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 크기 조정 </td> 
   <td colname="col2"> 선택 사항. 레이어의 점 크기를 지정하는 데 사용되는 값입니다. 기본값은 100입니다. 값이 클수록 점이 커지고 값이 작을수록 점이 작아집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 색상 </td> 
   <td colname="col2"> 선택 사항. (빨간색,녹색,파란색)으로 표시되는 RGB 색상 벡터입니다. 벡터의 각 색상에 대해 0.0부터 1.0까지의 값을 입력할 수 있습니다. 예를 들어, (1.0, 0.0, 0.0)은 밝은 빨간색이고 (0.5, 0.5, 0.5)은 회색으로 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 렌더링 모드 </td> 
   <td colname="col2"> <p>선택 사항. 레이어에 사용할 렌더링 모드를 나타내는 정수 값입니다. 사용 가능한 세 가지 모드는 다음과 같습니다. 
     <ul id="ul_CBB26B32505846A39FEB85E831E1C7AB"> 
      <li id="li_B31528A8858C4418ABCDFF0B4EFB25D7">렌더링 모드 1. 포인트 크기는 화면 공간에 정의됩니다. 점은 컴퓨터 화면에 대해 일정한 크기를 유지합니다. 점은 다각형을 사용하여 렌더링되므로 포인트 크기에는 제한이 없습니다. 기본 렌더링 모드입니다. </li> 
      <li id="li_CA0C3E0DBF004ADBB4D7819C0BF192FC">렌더링 모드 2. 포인트 크기는 세계 공간에서 정의됩니다. 점은 지구보다 일정한 크기를 유지합니다. 점은 다각형을 사용하여 렌더링되므로 포인트 크기에는 제한이 없습니다. </li> 
      <li id="li_8F8729976DDB434D869E81D4381E2688">렌더링 모드 3. 포인트 크기는 화면 공간에 정의됩니다. 점은 OpenGL 평활점을 사용하여 렌더링됩니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 [!DNL Zip Points.layer] 파일의 형식은 다음과 같습니다.

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
