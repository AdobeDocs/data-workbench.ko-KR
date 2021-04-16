---
description: 동적 점을 사용하여 요소 포인트 레이어를 만들 때 위도 및 경도 데이터는 차원의 각 요소에 포함됩니다.
title: 동적 점을 사용하여 요소 점 레이어 정의
uuid: f4b41969-329a-4c33-a8db-8d85597fa577
exl-id: 5f6e264c-5804-47fa-a3ca-8608a3f7e9d3
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 5%

---

# 동적 점을 사용하여 요소 점 레이어 정의{#define-element-point-layers-using-dynamic-points}

동적 점을 사용하여 요소 포인트 레이어를 만들 때 위도 및 경도 데이터는 차원의 각 요소에 포함됩니다.

동적 점을 사용하여 요소 점 레이어를 정의하려면 다음을 만들거나 이미 사용 가능하게 해야 합니다.

* [!DNL Transformation.cfg] 파일 또는 [!DNL transformation dataset include] 파일에 정의된 차원으로서 각 요소에 &quot;latitude, 위도&quot; 또는 &quot;latitude,경도,이름&quot; 문자열이 포함되어 있습니다.

   차원을 만드는 단계는 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.

* 관련 치수를 지정하는 레이어 파일입니다.

레이어 파일의 필수 형식에 대한 자세한 내용은 [요소 점 레이어 파일 형식](../../../../home/c-get-started/c-im-layers/c-elmt-pt-layers/c-elmt-pt-dyn-pts.md#section-0645fbc761c14bb986f3d6f02df407a0)을 참조하십시오.

>[!NOTE]
>
>[!DNL Dynamic Points]을 사용할 때는 레이어 파일에 지정된 치수의 기수가 적절한지 확인해야 합니다. 데이터 세트의 모든 행에 다른 위도와 경도가 있는 경우 치수가 빠르게 채워지고 대부분의 행이 작은 요소 요소에 포함됩니다. 작은 요소 요소에는 위도와 경도가 없으므로 지구에는 나타나지 않습니다.

## 요소 포인트 레이어 파일 형식 {#section-0645fbc761c14bb986f3d6f02df407a0}

동적 점을 사용하는 각 요소 포인트 레이어 파일은 다음 템플릿을 사용하여 서식을 지정해야 합니다.

```
Layer = ElementPointLayer:
  Dimension = ref: wdata/model/dim/Dimension Name
  Metric = ref: wdata/model/metric/Metric Name
  Dynamic Points = bool: true
  Scale = double: Scale
  Color = v3d: RGB Color Vector
  Rendering Mode = int: Mode Number
```

<table id="table_8756BDCC49F447C0855BA64BC0078A0C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 차원 </td> 
   <td colname="col2"> <p>다음 예에서 보듯이 "latitude,경도" 또는 "latitude,경도,이름" 문자열을 가진 요소를 포함해야 하는 차원(변형 구성 파일에 정의됨)의 이름입니다. 
     <ul id="ul_CC12F05459C640F5AB3C295932B04F83"> 
      <li id="li_9023CFA04A0F407E9DF0E1A4D71BB18C">37.5181,-77.1903 </li> 
      <li id="li_F002AB3AB98049A4AF1588B51167C7FA">35.3317,-77.8126,어딘가 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 지표 </td> 
   <td colname="col2"> Dimension 매개 변수에 지정된 차원 위에 평가되는 지표의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 동적 포인트 </td> 
   <td colname="col2"> 동적 점을 활성화합니다. true로 설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 비율 조정 </td> 
   <td colname="col2"> 선택 사항입니다. 레이어의 포인트 크기를 지정하는 데 사용되는 값입니다. 기본값은 100입니다. 값이 클수록 점이 커지고 값이 작을수록 점이 작아집니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 색상 </td> 
   <td colname="col2"> 선택 사항입니다. RGB 색상 벡터로서 (빨강,녹색,파랑)으로 표현됩니다. 벡터의 각 색상에 대해 0.0부터 1.0까지의 값을 입력할 수 있습니다. 예를 들어 (1.0, 0.0, 0.0)은 밝은 빨간색이고 (0.5, 0.5, 0.5)는 회색입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 렌더링 모드 </td> 
   <td colname="col2"> <p>선택 사항입니다. 레이어에 사용할 렌더링 모드를 나타내는 정수 값입니다. 사용 가능한 세 가지 모드는 다음과 같습니다. 
     <ul id="ul_C7A74B9B085741C8B7116E4F110DF830"> 
      <li id="li_75CC2BE35C594B6895F743A1967A2E07">렌더링 모드 1. 포인트 크기는 화면 공간에 정의됩니다(포인트는 컴퓨터 화면에 따라 일정한 크기로 유지됨). 포인트는 다각형을 사용하여 렌더링되므로 포인트 크기에 대한 상한값이 없습니다. 기본 렌더링 모드입니다. </li> 
      <li id="li_5B19C5B0F59548E28DCE7F7CD319E210">렌더링 모드 2. 포인트 크기는 월드 공간에 정의됩니다(포인트는 지구 크기를 기준으로 일정하게 유지). 포인트는 다각형을 사용하여 렌더링되므로 포인트 크기에 대한 상한값이 없습니다. </li> 
      <li id="li_DF0C9AEFE82642C9BD5AEA79770D2896">렌더링 모드 3. 포인트 크기는 화면 공간에 정의됩니다. 점은 OpenGL 매끄러운 점을 사용하여 렌더링됩니다. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

[!DNL IP Coordinates.layer] 파일의 형식은 다음과 같습니다.

```
Layer = ElementPointLayer:
  Dimension = ref: wdata/model/dim/Coordinates
  Metric = ref: wdata/model/metric/Visitors
  Dynamic Points = bool: true
```
