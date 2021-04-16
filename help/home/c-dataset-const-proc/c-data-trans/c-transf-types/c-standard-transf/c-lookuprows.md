---
description: LookupRows 변환은 동일한 추적 ID를 가진 다른 로그 항목을 보고 출력 필드의 값을 입력 행의 지정된 필드 값으로 설정합니다.
title: 조회 행
uuid: 4cff7cf1-00c8-4ab1-8adc-3805518226d3
exl-id: caa9a311-b056-4fe8-bb11-1605cc690375
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# 조회 행{#lookuprows}

LookupRows 변환은 동일한 추적 ID를 가진 다른 로그 항목을 보고 출력 필드의 값을 입력 행의 지정된 필드 값으로 설정합니다.

[!DNL LookupRows] 변환은 조회 파일이 아닌 로그 항목을 조회하므로 [!DNL CrossRows] 변환과 매우 유사합니다. [CrossRows](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-crossrows.md#concept-fcace08804f54db397ed631cc13ff4f2)를 참조하십시오.

이 작업을 수행하려면 [!DNL LookupRows] 변형이 소스 데이터의 추적 ID로 지정된 시간에 데이터를 정렬하고 그룹화해야 합니다. 따라서 [!DNL LookupRows]은 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일에 정의된 경우에만 작동합니다.

다음 표에서 매개 변수에 대한 설명을 검토할 때는 다음 사항을 기억하십시오.

* 출력 행은 특정 시점의 변형이 작업 중인 데이터의 행입니다.
* 입력 행은 입력 필드의 값이 변환에 입력되는 다른 데이터 행(출력 행 이전, 이후 또는 포함)입니다.

<table id="table_AB68A89ECD5C45F39B8433F994BBD7D8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 이름 </td> 
   <td colname="col2"> 변환의 설명형 이름입니다. 여기에 이름을 입력할 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항입니다. 변형에 대한 참고 사항 </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 변환 출력을 특정 로그 항목으로 제한합니다. 특정 로그 항목에 대한 조건이 충족되지 않으면 출력 행 값 출력 매개 변수의 필드는 변경되지 않습니다. 다른 로그 항목에 영향을 주는 경우에도 입력을 사용할 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 조건 </td> 
   <td colname="col2">특정 입력 행에서만 변환에 대한 입력을 허용합니다. 특정 입력 행에 대해 <span class="wintitle"> 입력</span> 조건이 충족되지 않으면 해당 행의 입력 필드가 무시되고 다른 출력 행에 영향을 주지 않습니다. 그러나 해당 행의 출력 필드는 지정된 조건에 따라 여전히 수정됩니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 행 키 입력 </td> 
   <td colname="col2"> 입력 행의 키로 사용할 필드의 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 행 값 입력 </td> 
   <td colname="col2"> 모든 조건이 충족되는 경우 출력 행 값 출력 매개 변수의 필드에 값이 복사되는 입력 행의 필드 이름. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작업 </td> 
   <td colname="col2"> <p>각 출력 행에 대해 <span class="wintitle"> 입력</span> 조건 및 입력 행 키 입력 매개 변수에 의해 정의된 모든 조건을 충족하는 모든 입력 행에 적용되는 작업을 통해 출력을 생성하는 작업: 
     <ul id="ul_16FB152CB558497794DDED72A2F05CDD"> 
      <li id="li_22DA9F814E4E42D0B21E90B63A2A7A0E"> FIRST는 데이터의 첫 번째 일치 입력 행에서 입력 행 입력 매개 변수의 필드 값을 출력합니다(출력 행 뒤에 첫 번째 일치 행이 아님). </li> 
      <li id="li_45E00C3DE0494A1CB5C09B942088F161"> LAST는 데이터의 마지막 입력 행에서 입력 행 값 입력 매개 변수의 필드 값을 출력합니다(출력 행 앞의 마지막 일치 행 아님). </li> 
     </ul> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 행 키 입력 </td> 
   <td colname="col2"> 출력 행의 키로 사용할 필드의 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 행 값 출력 </td> 
   <td colname="col2">모든 조건이 충족되는 경우 입력 행 값 입력 매개 변수의 필드에서 값이 복사되는 출력 행의 필드 이름. x-trackingid 및 <span class="wintitle"> 출력 행 키 입력 </span>값이 동일한 <span class="wintitle"> 출력 행 값 출력</span> 값을 가진 모든 출력 행입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

입력 행 키 입력, 입력 행 값 입력 및 입력 조건 매개 변수는 각 추적 ID에 대한 조회 파일을 함께 정의하며 출력 행 키 입력, 출력 행 값 입력 및 조건 매개 변수는 파일에서 조회되는 내용과 출력 행 값 출력으로 지정된 필드에 저장되는 값을 제어합니다.

변환 작업을 더 잘 이해하려면 다음 개요를 고려하십시오.

* 조건을 만족시키고 비어 있지 않은 출력 행 키 입력이 있는 각 출력 행에 대해:

   * FIRST 또는 LAST 입력 행을 찾아

      * 입력 행이 입력 조건을 충족하고
      * 입력 행의 x-trackingid는 출력 행의 x-trackingid와 같습니다.
      * 입력 행의 입력 행 키 입력은 출력 행의 출력 행 키 입력과 같습니다.

* 출력 행의 출력 행 값 출력을 입력 행의 입력 행 값 입력으로 설정합니다.

[!DNL LookupRows]에 대한 고려 사항

* 빈 키 값은 절대 일치하지 않습니다. [!DNL Input Condition]과 일치하는 빈 키와 비어 있지 않은 값이 있는 입력 행이 있는 경우에도 &quot;&quot;의 [!DNL Output Row Key Input]은 항상 &quot;&quot;의 [!DNL Output Row Value Output]를 생성합니다.

* [!DNL Input Condition]에서 금지하지 않는 경우 [!DNL Input Row Key Input] 및 [!DNL Output Row Key Input] 값이 동일하면 행이 자체적으로 검색될 수 있습니다.

키 값이 여러 개인 경우 [!DNL LookupRows] 변형을 적용하기 전에 [!DNL Format] 변환([Format](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-format.md#concept-3de04869181e4694ab072b092186684b) 참조)을 사용하여 결합할 수 있습니다.

애완 동물 등록 페이지, 이름 및 종을 입력하고 이후 &quot;장난감 구매&quot; 페이지에서 애완 동물의 이름만 사용될 수 있다고 가정합니다. 등록 페이지에 입력한 애완 동물 이름과 애완 동물 이름을 연결할 수 있어야 합니다. 이렇게 하려면 다음 [!DNL LookupRows] 변형을 만들 수 있습니다.

![](assets/cfg_TransformationType_LookupRows.png)

이전 개요를 사용하여 이 예제를 분석하겠습니다.

* 비어 있지 않은 cs-uri-query(petname) 값을 갖는 각 출력 행에 대해:

   * LAST 입력 행을 찾아

      * 입력 행에는 cs-uri-query(petbreed)의 비어 있지 않은 값이 들어 있으며,
      * 입력 행의 x-trackingid는 출력 행의 x-trackingid와 같습니다.
      * 입력 행의 cs-uri-query(petname) 값은 출력 행의 cs-uri-query(petname) 값과 같습니다.

* 출력 행의 x-pet-breed 값을 입력 행의 cs-uri-query(petbreed) 값으로 설정합니다.

[!DNL LookupRows] 변형은 애완 동물 종들이 애완 동물 등록과 장난감 페이지 둘 다에 연결되어 있는지 확인하기 위해(키)를 사용하여 여러 애완 동물을 방문하는 방문자에게도 각 애완 동물 품종에 대해 구입한 장난감을 분석할 수 있도록 합니다.
