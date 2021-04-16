---
description: 비정상 차원은 상위 계산 가능한 차원과 일대일 관계를 가집니다.
title: 비정상 차원
uuid: f172fbce-e967-41ce-9958-9062561ecbcc
exl-id: 0c4fad38-bc7c-4b63-98ec-c9121e576a36
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 2%

---

# 비정상 차원{#denormal-dimensions}

비정상 차원은 상위 계산 가능한 차원과 일대일 관계를 가집니다.

원하는 차원에 상위의 각 요소에 대한 고유 요소가 포함될 때마다 비정상 차원을 정의합니다. 예를 들어 [!DNL EMail Address]은 방문자 상위의 비정상 차원입니다. 각 방문자에게는 이메일 주소가 있고 이메일 주소 차원의 각 요소는 단일 방문자의 이메일 주소입니다. 두 명의 방문자가 동일한 이메일 주소를 사용하더라도 주소는 이메일 주소 차원의 별개의 요소입니다.

테이블 시각화, 세부 사항 테이블에서 비정상 차원을 사용하거나 필터를 만들 수 있습니다. 또한 데이터 워크벤치 서버의 세그먼트 내보내기 기능에 비정상 차원을 사용하여 값이 많은 필드(예: [!DNL Tracking ID] 또는 [!DNL EMail Address]) 값을 내보낼 수 있습니다. 내보내려는 세그먼트 데이터는 프로필 내의 차원으로 정의해야 하므로 필드 데이터의 원시 문자열을 저장하는 비정상 차원을 만들어야 합니다.

>[!NOTE]
>
>일반 차원을 기대하는 테이블 또는 기타 시각화에서 비정상 차원을 사용할 경우 파생된 비정상 차원이 자동으로 생성됩니다. 파생된 비정상 차원은 상위 차원과 일대다 관계를 가집니다.

세부 사항 테이블 시각화 및 필터에 대한 자세한 내용은 *Data Workbench 사용자 안내서*&#x200B;의 분석 시각화 장을 참조하십시오. 세그먼트 내보내기에 대한 자세한 내용은 *Data Workbench 사용자 안내서*&#x200B;의 인터페이스 및 분석 기능 구성 장을 참조하십시오.

>[!NOTE]
>
>비정상 크기는 쿼리 시간 및 디스크 공간에서 매우 비쌀 수 있습니다. 상위 [!DNL Page View]과 50바이트 평균 입력 문자열이 있는 비정상 차원은 일반 큰 일반적인 데이터 세트에서 25GB의 데이터를 버퍼에 추가할 수 있으며, 이것은 약 13개의 단순 또는 숫자 페이지 보기 차원 또는 약 125개의 세션 수준 차원에 해당합니다. 성능 영향을 주의 깊게 평가하지 않고도 데이터 세트에 비정상 차원을 추가하지 마십시오.

비정상 차원은 다음 매개 변수로 정의됩니다.

<table id="table_532AD791E39B4CF296FFA1C33FB8302E"> 
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
   <td colname="col2"> 데이터 워크벤치에 나타나는 차원의 설명형 이름. 차원 이름에는 하이픈(-)을 포함할 수 없습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항입니다. 확장 차원에 대한 참고 사항. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 상위와 입력 필드 값 간의 관계를 만들어야 하는 조건. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 숨김 </td> 
   <td colname="col2"> 데이터 워크벤치 인터페이스에 차원이 나타나는지 여부를 결정합니다. 기본적으로 이 매개 변수는 false로 설정됩니다. 예를 들어 차원이 지표의 기준으로만 사용되도록 설정된 경우 이 매개 변수를 true로 설정하여 데이터 워크벤치 디스플레이에서 차원을 숨길 수 있습니다. </td> 
   <td colname="col3"> true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> 상위 차원(상위)과 관련된 값입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 정규화된 요소 </td> 
   <td colname="col2"> 이름이 시스템 메모리에 저장될 차원 요소의 수를 지정하는 성능 조정 매개 변수입니다. 이 매개 변수를 더 높은 값으로 설정하면 비정상 치수가 더 많은 RAM을 사용하지만 더 빠른 쿼리를 생성합니다. 기본값은 16383입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작업 </td> 
   <td colname="col2"> <p>사용 가능한 작업은 다음과 같습니다. </p> <p> 
     <ul id="ul_CCDC45838A3941BD949B6D21EA0492B3"> 
      <li id="li_F33898192A82437692B5C15684EFCF64"> 비어 있지 않은 첫 번째:첫 번째 로그 항목에서 오는지 여부에 관계없이 비어 있지 않은 첫 번째 입력 값이 사용됩니다. <span class="wintitle"> 입력</span>이 벡터 필드이면 관련 로그 항목의 벡터의 첫 번째 행이 사용됩니다. </li> 
      <li id="li_4ADD0A368BB74B64AD29126C8E7B333F"> 첫 번째 행:입력이 비어 있더라도 상위 차원 요소와 관련된 첫 번째 로그 항목의 값이 사용됩니다. <span class="wintitle"> 입력</span>이 벡터 필드이면 관련 로그 항목의 벡터의 첫 번째 행이 사용됩니다. 이 값이 비어 있거나 숫자가 아닌 경우 또는 관련 로그 항목이 차원의 조건에 맞지 않는 경우 값이 사용되지 않습니다. </li> 
      <li id="li_C93CA22ADA634F21A6488BB3BEE7CB23"> 마지막 비어 있지 않음:마지막 로그 항목에서 오는지 여부에 관계없이 비어 있지 않은 마지막 입력 값이 사용됩니다. <span class="wintitle"> 입력</span>이 벡터 필드이면 관련 로그 항목의 벡터의 첫 번째 행이 사용됩니다. </li> 
      <li id="li_2FFE585521B14FE5ABBF66AAC47F22C4"> 마지막 행:입력이 비어 있더라도 상위 차원 요소와 관련된 마지막 로그 항목의 값이 사용됩니다. <span class="wintitle"> 입력</span>이 벡터 필드이면 관련 로그 항목의 벡터의 첫 번째 행이 사용됩니다. 이 값이 비어 있거나 숫자가 아닌 경우 또는 관련 로그 항목이 차원의 조건에 맞지 않는 경우 값이 사용되지 않습니다. </li> 
     </ul> </p> <p> <p>참고: 작업에 값이 없으면 빈 값("")이 사용됩니다. </p> </p> <p> 차원이 의도대로 정의되도록 작업을 지정해야 합니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 상위 </td> 
   <td colname="col2"> 상위 차원의 이름입니다. 모든 계산 가능한 차원은 상위 차원일 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예제에서 표시된 비정상 차원은 x-trackingid 필드의 모든 데이터를 입력으로 가져와서 방문자 ID라는 차원에 포함합니다. 만든 방문자 세그먼트의 경우 방문자 ID 차원(및 기타 정의된 차원)의 데이터를 내보낼 수 있습니다.

![](assets/cfg_Transformation_Dim_Denormal.png)
