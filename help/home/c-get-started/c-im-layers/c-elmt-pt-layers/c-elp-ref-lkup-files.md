---
description: 위도 및 경도 데이터를 얻기 위해 조회 파일을 참조하는 요소 포인트 레이어를 만들 때 조회 파일에서 각 요소 및 관련 위도와 경도를 검색하여 해당 위치의 위치를 얻습니다.
solution: Analytics
title: 조회 파일을 참조하는 요소 포인트 레이어 정의
topic: Data workbench
uuid: 32c8de7a-4316-4f91-9810-7f584bc7fb0b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 조회 파일을 참조하는 요소 포인트 레이어 정의{#define-element-point-layers-referencing-lookup-files}

위도 및 경도 데이터를 얻기 위해 조회 파일을 참조하는 요소 포인트 레이어를 만들 때 조회 파일에서 각 요소 및 관련 위도와 경도를 검색하여 해당 위치의 위치를 얻습니다.

>[!NOTE]
>
>조회 파일을 사용하는 대신 위치의 위도와 경도를 차원의 각 요소 이름에 포함하는 동적 포인트 기능을 사용할 수 있습니다. 동적 [포인트를 사용하여 요소 점 레이어 정의를 참조하십시오](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-dyn-pts.md#concept-51adc5e1df8a48e7bd7a582967e4c512).

조회 파일을 참조하는 요소 포인트 레이어를 정의하려면 다음을 만들거나 이미 사용할 수 있어야 합니다.

* **또는** [!DNL Transformation.cfg file] [!DNL transformation dataset include] 파일에 정의된 차원입니다. 변형 구성 파일에 대한 자세한 내용은 데이터 세트 구성 *안내서를 참조하십시오*.

* **각 데이터 포인트를 플롯하는 데 사용되는 데이터가 들어 있는 조회 파일** . 이 파일에는 각 데이터 포인트에 대해 최소 3개의 데이터 열이 있어야 합니다.키, 경도 및 위도 조회 파일의 필수 형식에 대한 자세한 내용은 요소 점 레이어 [파일 형식을 참조하십시오](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elp-ref-lkup-files.md#section-52d7e92be8354d979af9e7a2210b76f2).

* **조회 파일의 위치를 지정하고 조회 파일의 키, 경도 및 위도 열 이름뿐만 아니라 관련 차원과 지표를 식별하는 레이어 파일입니다** . 레이어 파일의 필수 형식에 대한 자세한 내용은 요소 점 레이어 [파일 형식을 참조하십시오](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elp-ref-lkup-files.md#section-52d7e92be8354d979af9e7a2210b76f2).

   >[!NOTE]
   >
   >프로파일과 함께 제공되는 [!DNL Zip Points.layer] 파일은 [!DNL Geography] [!DNL Zipcode.dim] [!DNL Sessions.metric] [!DNL Zip Points.txt] 파일, 파일, 조회 파일, 조회 파일, 조회 파일의 키, 경도, 위도 및 이름 열의 이름을 식별하는 요소 포인트 레이어입니다.

## 요소 포인트 조회 파일 형식 {#section-0bc8c652c1bd40eb84078f2af71a5c06}

요소 포인트 레이어 조회 파일은 다음 세 개 이상의 열을 포함해야 합니다.

* **[!DNL Key]열:**이 열에는 데이터 워크벤치 서버가 조회 파일의 데이터를 데이터 세트에 있는 데이터에 연결할 수 있는 공통 키 데이터가 포함되어야 합니다. 이[!DNL key]열은 조회 파일의 첫 번째 열이어야 합니다. 이 열의 각 행은 차원의 요소를 식별합니다.

* **[!DNL Longitude]열:**이 열에는[!DNL Key]열의 각 데이터 포인트에 대한 경도가 포함되어야 합니다.

* **[!DNL Latitude]열:**이 열에는[!DNL Key]열의 각 데이터 포인트에 대한 위도가 포함되어야 합니다.

* **[!DNL Name]열(선택 사항):**각 데이터 포인트에 대해 맵에 표시할 이름을 지정하려면 조회 파일에[!DNL Name]열을 포함할 수 있습니다.

조회 파일의 각 행은 첫 번째 열에 ZIP 코드가 들어 있고 그 뒤에 경도, 위도 및 연관된 도시 이름이 있습니다. [!DNL Zip Points.txt]

```
tude, and associated city name.
ZIP_CODE LATITUDE LONGITUDE NAME
00210 +43.005895 -071.013202 PORTSMOUTH, NH
00211 +43.005895 -071.013202 PORTSMOUTH, NH
...
```

## 요소 포인트 레이어 파일 포맷 {#section-52d7e92be8354d979af9e7a2210b76f2}

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
   <td colname="col2"> 위도 데이터를 포함하는 조회 파일의 열 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 이름 열 </td> 
   <td colname="col2"> 선택 사항입니다. 위도 및 경도 데이터로 표시되는 위치의 이름이 들어 있는 조회 파일의 열 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 키 열 </td> 
   <td colname="col2"> <p>Data Workbench 서버가 조회 파일의 데이터를 데이터 세트에 통합할 수 있도록 하는 일반적인 키 데이터를 포함하는 조회 파일의 열 이름입니다. 조회 파일의 첫 번째 열이어야 합니다. </p> <p>이 열의 각 행은 차원의 요소입니다. 이 차원은 Transformation.cfg <span class="filepath"> 파일에</span> 정의되어야 하거나 변환 데이터 세트에 <span class="wintitle"></span> 파일이 포함되며 이 파일의 Dimension 매개 변수에 지정해야 합니다. 변형 구성 파일에 대한 자세한 내용은 데이터 세트 구성 <i>안내서를 참조하십시오</i>. </p> </td> 
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
     <ul id="ul_F15E43B3BFE54CDD8026837027E25819"> 
      <li id="li_5405D939540E4D0FA7828D2623D72C44">렌더링 모드 1. 포인트 크기는 화면 공간에 정의됩니다(포인트는 컴퓨터 화면에 따라 일정한 크기로 유지됨). 점은 다각형을 사용하여 렌더링되므로 포인트 크기에 대한 상한을 두지 않습니다. 기본 렌더링 모드입니다. </li> 
      <li id="li_61C5AA926777449E8804C7BCE9E46F9B">렌더링 모드 2. 포인트 크기는 월드 공간에서 정의됩니다(포인트는 지구 크기를 기준으로 일정하게 유지). 점은 다각형을 사용하여 렌더링되므로 포인트 크기에 대한 상한을 두지 않습니다. </li> 
      <li id="li_C00527F959354D3BB7422EFFE1FB5135">렌더링 모드 3. 포인트 크기는 화면 공간에 정의됩니다. 점은 OpenGL 부드러운 점을 사용하여 렌더링됩니다. </li> 
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

