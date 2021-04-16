---
description: 데이터 집합 스키마 인터페이스는 변형 데이터 집합 구성 파일에 정의된 확장 차원(계산 가능, 단순, 다대다, 숫자, 비정상 및 시간 차원)과 이러한 차원 간의 관계를 표시합니다.
title: 데이터 세트 스키마
uuid: 4ef5f14b-dc19-4118-a2f2-d680ded8092c
exl-id: b80e6e8e-9147-46ec-8602-2d7e5d33f077
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 3%

---

# 데이터 세트 스키마{#dataset-schema}

데이터 집합 스키마 인터페이스는 변형 데이터 집합 구성 파일에 정의된 확장 차원(계산 가능, 단순, 다대다, 숫자, 비정상 및 시간 차원)과 이러한 차원 간의 관계를 표시합니다.

또한 [!DNL Dataset Schema] 인터페이스에서는 사용자가 정의한 파생된 차원 및 숨김으로 구성된 확장 차원을 표시합니다.

![](assets/vis_DatasetSchema_Example.png)

이 섹션에서는 다음 주제를 다룹니다.

* [데이터 집합 스키마 인터페이스를 사용하여 차원 유형을 해석하려면](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-schema.md#section-16a0a12b11334c07bec558c0b7d260b1)
* [차원에 대한 기본 시각화를 표시하려면](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-schema.md#section-1bbb73a5cbb34ffb844eb1932db85318)
* [차원에 대한 특정 시각화를 표시하려면](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-dataset-config-int/c-dataset-schema.md#section-d46626df90bc4c44ae60c4b71eaeac7f)

## 데이터 집합 스키마 인터페이스를 사용하여 Dimension 유형을 해석하려면 {#section-16a0a12b11334c07bec558c0b7d260b1}

다음 표에는 차원 유형과 이름이 [!DNL Dataset Schema] 인터페이스에 나타나는 색상이 나열됩니다. 위의 예에서 샘플 치수의 부모도 표시됩니다.

<table id="table_20D1A9EAAED247338476C475C63255F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Dimension 유형 </th> 
   <th colname="col2" class="entry"> 색상 </th> 
   <th colname="col3" class="entry"> 샘플 Dimension 및 상위 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 계산 가능 </td> 
   <td colname="col2"> 분홍색 </td> 
   <td colname="col3"> <p>방문자 - 이 스키마에서 방문자는 루트 계산 가능한 차원입니다. </p> <p> 세션 - 상위는 방문자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Denormal </td> 
   <td colname="col2"> 노란색 </td> 
   <td colname="col3"> 비정상 페이지 - 상위는 페이지 보기입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 파생됨 </td> 
   <td colname="col2"> 파란색 </td> 
   <td colname="col3"> 다음 페이지 - 상위 페이지가 페이지 보기입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 다대다 </td> 
   <td colname="col2"> 분홍색과 녹색(상위의 줄기는 분홍색이고 차원 이름은 녹색입니다.) </td> 
   <td colname="col3"> 검색어 - 상위는 세션입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숫자 </td> 
   <td colname="col2"> 녹색 </td> 
   <td colname="col3"> 정확한 페이지 지속 시간 - 상위는 페이지 보기입니다. 이 예에서는, 정확한 페이지 지속 시간이 숨겨진 숫자 차원입니다. 이 표에서 숨겨진 차원 유형을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 단순 </td> 
   <td colname="col2"> 녹색 </td> 
   <td colname="col3"> 페이지 - 상위는 페이지 보기입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간 </td> 
   <td colname="col2"> 녹색 </td> 
   <td colname="col3"> 시간 - 상위는 세션입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숨김 </td> 
   <td colname="col2"> 숨겨진 치수는 해당 치수 유형 색상의 어두운 버전입니다. 예를 들어, 숨겨진 숫자 치수는 어둡고 덜 밝은 녹색입니다. </td> 
   <td colname="col3"> 정확한 페이지 지속 시간 - 상위는 페이지 보기입니다. </td> 
  </tr> 
 </tbody> 
</table>

## Dimension {#section-1bbb73a5cbb34ffb844eb1932db85318}에 대한 기본 시각화를 표시하려면

* [!DNL Dataset Schema] 인터페이스에서 원하는 차원을 클릭합니다. 기본 시각화가 표시됩니다. 예를 들어 기본 시각화가 세션 및 선택한 차원을 표시하는 테이블이고 URI 차원을 클릭하면 데이터 워크벤치가 세션별 URI가 있는 테이블을 표시합니다.

>[!NOTE]
>
>표시되는 기본 시각화를 변경하려면 *Data Workbench 사용자 안내서*&#x200B;의 인터페이스 및 분석 기능 구성 장을 참조하십시오.

## Dimension {#section-d46626df90bc4c44ae60c4b71eaeac7f}에 대한 특정 시각화를 표시하려면

* [!DNL Dataset Schema] 인터페이스에서 원하는 차원을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add Visualization]** > *&lt;**[!UICONTROL visualization type]***&#x200B;를 클릭합니다.
