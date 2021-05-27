---
description: 상속된 프로파일에 대한 변환 데이터 세트 포함 파일에는 데이터 집합 구성의 변환 단계와 연관된 매개 변수가 포함되어 있습니다.
title: 변형 데이터 세트에 파일 포함
uuid: 46756f68-843c-4b0d-a79e-f107ef85db6c
exl-id: 58793f82-162a-4d43-aea9-163716c82db6
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 3%

---

# 변형 데이터 세트에 파일 포함{#transformation-dataset-include-files}

상속된 프로파일에 대한 변환 데이터 세트 포함 파일에는 데이터 집합 구성의 변환 단계와 연관된 매개 변수가 포함되어 있습니다.

파일의 첫 번째 줄은 확장 Dimension, 매개 변수, 재처리, 스테이지 및 변환 매개 변수를 지원하는 [!DNL TransformationInclude] 유형을 정의합니다. 다른 모든 매개 변수는 데이터 집합 프로필의 데이터 집합 디렉터리의 [!DNL Transformation.cfg] 파일에 정의해야 합니다.

[!DNL Transformation Dataset Include] 파일에 확장 Dimension, 매개 변수, 재처리, 스테이지 및 변환 이외의 매개 변수를 포함하면 오류가 발생합니다.

[!DNL Transformation Dataset Include] 파일의 이름을 원하는 대로 지정할 수 있지만 파일 확장명은 [!DNL .cfg]이어야 합니다. 파일은 *상속된 프로필 이름*\Dataset\Transformation directory 내에 저장해야 합니다. 파일은 데이터 집합 구성의 변환 단계 동안 재귀적으로 로드되므로 디렉터리 내의 임의의 수준(예: *상속된 프로필 이름*\Dataset\Transformation\*폴더 이름*\*include file name*.cfg 포함)에 [!DNL Transformation Dataset Include] 파일을 저장할 수 있습니다.

>[!NOTE]
>
>사이트에 대한 많은 웹 특정 구성 매개 변수가 [!DNL Transformation Dataset Include] 파일에 정의되어 있습니다. 이러한 매개 변수에 대한 자세한 내용은 [웹 데이터에 대한 구성 설정](../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519)을 참조하십시오.

다음 표에서는 [!DNL Transformation Dataset Include] 파일에서 사용할 수 있는 매개 변수에 대해 설명합니다.

<table id="table_7BD343888D9145BCBA889B531A4D18F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 확장된 차원 </td> 
   <td colname="col2"> 선택 사항입니다. 확장 차원을 정의합니다. <a href="../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md"> 확장 Dimension</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 매개 변수 </td> 
   <td colname="col2"> 선택 사항입니다. 다른 구성 매개 변수에서 참조할 수 있는 변수입니다. 자세한 내용은 데이터 집합에 있는 매개 변수 정의 <a href="../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-def-param-dataset-inc-files/c-def-param-dataset-inc-files.md#concept-5ad06acc8dc44bf2a99643fafdd56b50"> 포함 파일</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 재처리 </td> 
   <td colname="col2"> <p>선택 사항입니다. 여기에 문자 또는 문자 조합을 입력할 수 있습니다. 이 매개 변수를 변경하고 파일을 저장하면 데이터 재변환이 시작됩니다. </p> <p> 데이터 재처리에 대한 자세한 내용은 <a href="../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md"> 재처리 및 재변형</a>을 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 단계 </td> 
   <td colname="col2"> <p>선택 사항입니다. 이 <span class="wintitle"> 변형 데이터 집합에 적용되는 처리 단계 이름</span> 파일 처리 단계는 <span class="filepath"> Transformation.cfg</span> 파일의 Stage 매개 변수에 정의됩니다. </p> <p> <p>참고:Stage를 지정하는 경우 Stage의 이름은 데이터 세트 프로필의 <span class="filepath"> Transformation.cfg</span> 파일의 Stage 매개 변수에 나열된 이름과 정확히 일치해야 합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 변형 </td> 
   <td colname="col2"> 선택 사항입니다. 변형 중에 적용해야 하는 데이터 변형을 정의합니다. 사용 가능한 변형 유형에 대한 자세한 내용은 <a href="../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md"> 데이터 변환</a>을 참조하십시오. </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!DNL Transformation.cfg] 파일의 매개 변수에 대한 설명은 [변형 구성 파일](../../../../home/c-dataset-const-proc/c-trans-config-file/c-abt-trans-config-file.md)을 참조하십시오.

[!DNL Transformation Dataset Include] 파일을 사용할 때는 항상 다음 사항을 염두에 두어야 합니다.

* 이 파일의 매개 변수를 변경하려면 데이터를 다시 변환해야 합니다.
* [!DNL CrossRows],  [!DNL ODBCLookup],  [!DNL Sessionize]및  [!DNL AppendURI] 변형은 파일에 정의된 경우에만  [!DNL Transformation Dataset Configuration] 작동합니다. 이러한 변형에 대한 자세한 내용은 [데이터 변환](../../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md)을 참조하십시오.

* 메모장에서 파일을 열고 편집하여 위에 설명된 매개 변수를 [!DNL Transformation Dataset Include] 파일에 추가할 수 있습니다. 사용자가 만들고 저장하는 모든 변경 사항은 Data Workbench에서 파일을 다시 열면 나타납니다. 새 매개 변수를 추가할 때 Space 키(Tab 키 아님)를 사용하여 이전 제목 수준 오른쪽에 있는 두 개의(2) 공백을 들여씁니다.

Adobe의 [!DNL IP Geo-location] 또는 [!DNL IP Geo-intelligence] 데이터 서비스를 구독하는 경우, Adobe은 데이터 서비스를 위해 특별히 만들어진 데이터 변환 세트와 확장 차원으로 구성된 내부 프로필을 제공합니다. 변형 및 차원은 내부 프로필의 데이터 세트 디렉터리에 포함된 [!DNL Transformation Dataset Include] 파일에 정의됩니다. [!DNL IP Geo-location] 또는 [!DNL IP Geo-intelligence] 데이터 서비스의 내부 프로필을 설치하는 방법은 *Data Workbench 사용 안내서*&#x200B;를 참조하십시오.
