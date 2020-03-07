---
description: 동적 점을 사용하여 요소 포인트 레이어를 만들 때 위도 및 경도 데이터는 차원의 각 요소에 포함됩니다.
solution: Analytics
title: 동적 점을 사용하여 요소 점 레이어 정의
topic: Data workbench
uuid: 5f1b4638-fe45-40be-b963-18dcd5d09afa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 동적 점을 사용하여 요소 점 레이어 정의{#defining-element-point-layers-using-dynamic-points}

동적 점을 사용하여 요소 포인트 레이어를 만들 때 위도 및 경도 데이터는 차원의 각 요소에 포함됩니다.

동적 점을 사용하여 요소 점 레이어를 정의하려면 다음을 만들거나 이미 사용할 수 있어야 합니다.

* **파일 또는 변형 데이터 세트에**[!DNL Transformation.cfg] 정의된 치수에는 각 요소에 &quot;latitude, 경도&quot; 또는 &quot;latitude,경도,이름&quot; 문자열이 포함되어 있는 파일이 포함되어 있습니다.

   차원을 만드는 단계는 데이터 세트 구성 *안내서를 참조하십시오*.

* **관련 차원을 지정하는 레이어 파일입니다** .

   레이어 파일의 필수 형식에 대한 자세한 내용은 요소 점 레이어 [파일 형식을 참조하십시오](../../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-elmt-pt-lyr-file-frmt.md#concept-678a95cb69644105a7af1b86ad5a5981).

>[!NOTE]
>
>사용할 [!DNL Dynamic Points]때는 레이어 파일에 지정된 치수의 카디널리티가 적합한지 확인해야 합니다. 데이터 세트의 모든 행에 다른 위도와 경도가 있는 경우, 차원은 빠르게 채워지고 대부분의 행은 작은 요소 요소에 속하게 됩니다. 작은 요소 요소에는 위도와 경도가 없으므로 지구에는 나타나지 않습니다.

## 요소 점 레이어 파일 형식 {#section-bbcc2baa2f754dba81eba93339a97cbd}

동적 포인트를 사용하는 각 요소 포인트 레이어 파일의 형식은 다음 템플릿을 사용하여 지정해야 합니다.

```
Layer = ElementPointLayer:
  Dimension = ref: wdata/model/dim/Dimension Name
  Metric = ref: wdata/model/metric/Metric Name
  Dynamic Points = bool: true
  Scale = double: Scale
  Color = v3d: RGB Color Vector
  Rendering Mode = int: Mode Number
```

<table id="table_71AD13D7A9234782A4495DFBBD959F76"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 차원 </td> 
   <td colname="col2"> <p>다음 예에서 보듯이 "latitude, 경도" 또는 "latitude, 경도, 이름" 문자열이 포함된 요소를 포함해야 하는 차원(변형 구성 파일에 정의됨)의 이름입니다. 
     <ul id="ul_49069B74AF5A4CE28E20BB3B98BB2D89"> 
      <li id="li_296010E3A513424A86AFA09E4DA2DFA4">37.5181,-77.1903 </li> 
      <li id="li_352D380B55044DD5AAB9B6FF8335AAC6">35.3317,-77.8126,어딘가 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지표 </td> 
   <td colname="col2"> 차원 매개 변수에 지정된 차원 위에 평가되는 지표의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 동적 포인트 </td> 
   <td colname="col2"> 동적 포인트를 활성화합니다. true로 설정합니다. </td> 
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
     <ul id="ul_771F0E43E3CD45259918520F092BCCE4"> 
      <li id="li_2B4CF2EC50174143AAD589A08C7457F8">렌더링 모드 1. 포인트 크기는 화면 공간에 정의됩니다(포인트는 컴퓨터 화면에 따라 일정한 크기로 유지됨). 점은 다각형을 사용하여 렌더링되므로 포인트 크기에 대한 상한을 두지 않습니다. 기본 렌더링 모드입니다. </li> 
      <li id="li_5F0737A941474EF5898735ECD0563D8D">렌더링 모드 2. 포인트 크기는 월드 공간에서 정의됩니다(포인트는 지구 크기를 기준으로 일정하게 유지). 점은 다각형을 사용하여 렌더링되므로 포인트 크기에 대한 상한을 두지 않습니다. </li> 
      <li id="li_4B9EDE5FFA8348B9A50E5232CEB98F17">렌더링 모드 3. 포인트 크기는 화면 공간에 정의됩니다. 점은 OpenGL 부드러운 점을 사용하여 렌더링됩니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

파일의 [!DNL IP Coordinates.layer] 형식은 다음과 같습니다.

```
Layer = ElementPointLayer:
  Dimension = ref: wdata/model/dim/Coordinates
  Metric = ref: wdata/model/metric/Visitors
  Dynamic Points = bool: true
```
