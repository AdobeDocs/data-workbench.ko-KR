---
description: 조회 파일을 참조하여 위도 및 경도 데이터를 얻는 요소 점 레이어를 만들면 조회 파일에서 각 요소 및 연관된 위도와 경도를 검색하여 점의 위치를 얻습니다.
title: 조회 파일을 참조하는 요소 점 레이어 정의
uuid: 32c8de7a-4316-4f91-9810-7f584bc7fb0b
exl-id: 2275fa8e-82fe-49e4-ab3e-91ec6ecb6233
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 3%

---

# 조회 파일을 참조하는 요소 점 레이어 정의{#define-element-point-layers-referencing-lookup-files}

조회 파일을 참조하여 위도 및 경도 데이터를 얻는 요소 점 레이어를 만들면 조회 파일에서 각 요소 및 연관된 위도와 경도를 검색하여 점의 위치를 얻습니다.

>[!NOTE]
>
>조회 파일을 사용하는 대신 동적 점 기능을 사용하여 차원의 각 요소 이름에 위치의 위도와 경도를 포함할 수 있습니다. [동적 점을 사용하여 요소 점 레이어 정의](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-dyn-pts.md#concept-51adc5e1df8a48e7bd7a582967e4c512)를 참조하십시오.

조회 파일을 참조하는 요소 점 레이어를 정의하려면 다음을 생성하거나 이미 사용 가능해야 합니다.

* **또는** 파일에 정의된  [!DNL Transformation.cfg file]  [!DNL transformation dataset include] 차원입니다. 변형 구성 파일에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.

* **각** 데이터 포인트를 플롯하는 데 사용되는 데이터가 포함된 조회 필터입니다. 이 파일은 각 데이터 포인트에 대해 최소 3개의 데이터 열을 포함해야 합니다.키, 경도 및 위도입니다. 조회 파일의 필수 형식에 대한 자세한 내용은 [요소 점 레이어 파일 형식](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elp-ref-lkup-files.md#section-52d7e92be8354d979af9e7a2210b76f2)을 참조하십시오.

* **조회 파일** 의 위치를 지정하고 조회 파일의 키, 경도 및 위도 열 이름과 관련 차원 및 지표를 식별하는 레이어 파일입니다. 레이어 파일의 필수 형식에 대한 자세한 내용은 [요소 점 레이어 파일 형식](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elp-ref-lkup-files.md#section-52d7e92be8354d979af9e7a2210b76f2)을 참조하십시오.

   >[!NOTE]
   >
   >[!DNL Geography] 프로필과 함께 제공되는 [!DNL Zip Points.layer] 파일은 [!DNL Zipcode.dim] 파일, [!DNL Sessions.metric] 파일, [!DNL Zip Points.txt] 조회 파일 및 조회 파일의 키, 경도, 위도 및 이름 열의 이름을 식별하는 요소 포인트 레이어입니다.

## 요소 점 조회 파일 형식 {#section-0bc8c652c1bd40eb84078f2af71a5c06}

요소 점 레이어 조회 파일은 다음 세 개 이상의 열을 포함해야 합니다.

* **[!DNL Key]열:** 이 열에는 일반 키 데이터가 포함되어야 합니다. 이렇게 하면 Data Workbench 서버가 조회 파일의 데이터를 데이터 세트에 연결할 수 있습니다. [!DNL key] 열은 조회 파일의 첫 번째 열이어야 합니다. 이 열의 각 행은 차원의 요소를 식별합니다.

* **[!DNL Longitude]열:** 이 열에는 열의 각 데이터 포인트에 대한 경도가 포함되어야  [!DNL Key] 합니다.

* **[!DNL Latitude]열:** 이 열에는 열의 각 데이터 포인트에 대한 위도가 포함되어야  [!DNL Key] 합니다.

* **[!DNL Name]열(선택 사항):** 각 데이터 포인트에 대한 맵에 표시할 이름을 지정하려면 조회  [!DNL Name] 파일에 열을 포함할 수 있습니다.

[!DNL Zip Points.txt] 조회 파일의 각 행에는 첫 번째 열의 ZIP 코드가 포함되며 그 뒤에는 경도, 위도 및 연관된 도시 이름이 옵니다.

```
tude, and associated city name.
ZIP_CODE LATITUDE LONGITUDE NAME
00210 +43.005895 -071.013202 PORTSMOUTH, NH
00211 +43.005895 -071.013202 PORTSMOUTH, NH
...
```

## 요소 점 레이어 파일 형식 {#section-52d7e92be8354d979af9e7a2210b76f2}

조회 파일을 참조하는 각 요소 점 레이어 [!DNL .layer] 파일은 다음 템플릿을 사용하여 형식을 지정해야 합니다.

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

<table id="table_7287F8869DD04886BE1477CBB11EB796"> 
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
   <td colname="col2"> 선택 사항입니다. 위도 및 경도 데이터로 표현되는 위치의 이름이 들어 있는 조회 파일의 열 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 키 열 </td> 
   <td colname="col2"> <p>Data Workbench 서버가 조회 파일의 데이터를 데이터 세트에 통합할 수 있는 공통 키 데이터가 포함된 조회 파일의 열 이름입니다. 조회 파일의 첫 번째 열이어야 합니다. </p> <p>이 열의 각 행은 차원의 요소입니다. 이 차원은 <span class="filepath"> Transformation.cfg</span> 파일 또는 <span class="wintitle"> 변형 데이터 세트에</span> 파일을 포함하며 이 파일의 Dimension 매개 변수에 지정되어야 합니다. 변형 구성 파일에 대한 자세한 내용은 <i>데이터 집합 구성 안내서</i>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 차원 </td> 
   <td colname="col2"><span class="wintitle"> 키</span> 열의 데이터 행에 해당하는 요소를 포함하는 차원(변형 구성 파일에 정의됨)의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지표 </td> 
   <td colname="col2"> Dimension 매개 변수에 지정된 차원을 통해 평가되는 지표의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 크기 조정 </td> 
   <td colname="col2"> 선택 사항입니다. 레이어의 점 크기를 지정하는 데 사용되는 값입니다. 기본값은 100입니다. 값이 클수록 점이 커지고 값이 작을수록 점이 작아집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 색상 </td> 
   <td colname="col2"> 선택 사항입니다. (빨간색,녹색,파란색)으로 표시되는 RGB 색상 벡터입니다. 벡터의 각 색상에 대해 0.0부터 1.0까지의 값을 입력할 수 있습니다. 예를 들어, (1.0, 0.0, 0.0)은 밝은 빨간색이고 (0.5, 0.5, 0.5)은 회색으로 표시됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 렌더링 모드 </td> 
   <td colname="col2"> <p>선택 사항입니다. 레이어에 사용할 렌더링 모드를 나타내는 정수 값입니다. 사용 가능한 세 가지 모드는 다음과 같습니다. 
     <ul id="ul_F15E43B3BFE54CDD8026837027E25819"> 
      <li id="li_5405D939540E4D0FA7828D2623D72C44">렌더링 모드 1. 포인트 크기는 화면 공간에 정의됩니다. 점은 컴퓨터 화면에 대해 일정한 크기를 유지합니다. 점은 다각형을 사용하여 렌더링되므로 포인트 크기에는 제한이 없습니다. 기본 렌더링 모드입니다. </li> 
      <li id="li_61C5AA926777449E8804C7BCE9E46F9B">렌더링 모드 2. 포인트 크기는 세계 공간에서 정의됩니다. 점은 지구보다 일정한 크기를 유지합니다. 점은 다각형을 사용하여 렌더링되므로 포인트 크기에는 제한이 없습니다. </li> 
      <li id="li_C00527F959354D3BB7422EFFE1FB5135">렌더링 모드 3. 포인트 크기는 화면 공간에 정의됩니다. 점은 OpenGL 평활점을 사용하여 렌더링됩니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

[!DNL Zip Points.layer] 파일의 형식은 다음과 같습니다.

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
