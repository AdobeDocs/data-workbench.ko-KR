---
description: 데이터 세트 스키마 인터페이스는 변형 데이터 세트 구성 파일에 정의된 확장 차원(계산 가능한, 단순, 다대다, 숫자, 비정상 및 시간 차원)을 표시하고 이러한 차원 간의 관계를 볼 수 있도록 제공합니다.
title: 데이터 세트 스키마 인터페이스
uuid: 3726e568-d3ea-47f8-8ac4-582c97fbbe0a
exl-id: a8d4cf02-4ff7-4fcc-9062-425c1fe1fb28
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 3%

---

# 데이터 세트 스키마 인터페이스{#dataset-schema-interface}

데이터 세트 스키마 인터페이스는 변형 데이터 세트 구성 파일에 정의된 확장 차원(계산 가능한, 단순, 다대다, 숫자, 비정상 및 시간 차원)을 표시하고 이러한 차원 간의 관계를 볼 수 있도록 제공합니다.

또한 [!DNL Dataset Schema] 인터페이스에서는 사용자가 정의한 파생된 차원 및 숨김으로 구성된 확장 차원을 표시합니다.

![](assets/vis_DatasetSchema_Example2.png)

>[!NOTE]
>
>스키마 다이어그램 내에서 차원을 검색할 수 있습니다. 검색 문자열에 있는 차원의 이름이 강조 표시되고 상위 클래스의 선은 하위 하위 하위 차원에 있는 모든 히트에 대한 색상을 변경합니다. 가산 가능한 차원은 스크롤할 때 계속 표시되어 볼 수 있는 계층 구조 및 컨텍스트를 제공합니다.

**인터페이스를 사용하여 차원 유형을  [!DNL Dataset Schema] 해석하려면**

다음 표에는 차원 유형과 이름이 [!DNL Dataset Schema] 인터페이스에 나타나는 색상이 나열됩니다. 위의 예에서 샘플 치수의 부모도 표시됩니다.

<table id="table_CF888522626E49A4A10D87085CAB5CC1"> 
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
   <td colname="col3"> <p>방문자 - 이 스키마에서 방문자는 루트 계산 가능한 차원입니다. </p> <p>세션 - 상위가 방문자임 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Denormal </td> 
   <td colname="col2"> 노란색 </td> 
   <td colname="col3"> 비정상 페이지 - 상위 페이지가 페이지 보기임 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 파생됨 </td> 
   <td colname="col2"> 파란색 </td> 
   <td colname="col3"> 다음 페이지 - 상위 페이지가 페이지 보기임 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 다대다 </td> 
   <td colname="col2"> 분홍색과 녹색(상위의 줄기는 분홍색이고 차원 이름은 녹색입니다.) </td> 
   <td colname="col3"> 검색어 - 상위가 세션임 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숫자 </td> 
   <td colname="col2"> 녹색 </td> 
   <td colname="col3"> 정확한 페이지 지속 시간 - 상위는 페이지 보기입니다. 이 예에서, 정확한 페이지 기간은 숨겨진 숫자 차원입니다. 이 표에서 숨겨진 차원 유형을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 단순 </td> 
   <td colname="col2"> 녹색 </td> 
   <td colname="col3"> 페이지 - 상위 페이지가 페이지 보기임 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간 </td> 
   <td colname="col2"> 녹색 </td> 
   <td colname="col3"> 시간 - 상위가 세션임 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숨김 </td> 
   <td colname="col2"> 숨겨진 치수는 해당 치수 유형 색상의 어두운 버전입니다. 예를 들어, 숨겨진 숫자 치수는 어둡고 덜 밝은 녹색입니다. </td> 
   <td colname="col3"> 정확한 페이지 기간 - 상위 페이지가 페이지 보기임 </td> 
  </tr> 
 </tbody> 
</table>

이러한 차원 유형에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.

**차원에 대한 기본 시각화를 표시하려면**

* [!DNL Dataset Schema] 인터페이스에서 원하는 차원을 클릭합니다. 기본 시각화가 표시됩니다. 예를 들어 기본 시각화가 세션 및 선택한 차원을 표시하는 테이블이고 URI 차원을 클릭하면 Data Workbench에 세션별 URI가 있는 테이블이 표시됩니다.

   >[!NOTE]
   >
   >표시되는 기본 시각화를 변경하려면 [데이터 세트 스키마 인터페이스](../../../home/c-get-started/c-admin-intrf/c-dtst-sch-intrf.md#concept-e147b3a5b542453ca2b121e1c85bb175)를 참조하십시오.

**차원에 대한 특정 시각화를 표시하려면**

* [!DNL Dataset Schema] 인터페이스에서 원하는 차원을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add Visualization]** > *&lt;**[!UICONTROL visualization type]***&#x200B;를 클릭합니다.
