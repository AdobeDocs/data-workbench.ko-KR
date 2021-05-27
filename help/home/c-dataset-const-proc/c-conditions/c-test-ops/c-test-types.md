---
description: 비교 조건 및 범위 조건에서는 조건에 대해 수행할 비교 유형을 지정해야 합니다.
title: 테스트 작업 유형
uuid: dc0433dd-a35e-472e-8975-f58347512c11
exl-id: 8abed46e-e76d-47c0-bbe9-cf98cf2d61e8
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 2%

---

# 테스트 작업 유형{#test-types-for-test-operations}

비교 조건 및 범위 조건에서는 조건에 대해 수행할 비교 유형을 지정해야 합니다.

다음 표에서는 사용 가능한 유형( [!DNL LEXICAL], [!DNL NUMERIC] 및 [!DNL DATETIME])에 대해 설명합니다.

<table id="table_1B3AD8BDF0414D0AB8EE0E6D1B53E2CE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 테스트 유형 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 참고 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> 정수</span> </p> </td> 
   <td colname="col2"> <p>먼저 입력 필드를 정수로 바꿉니다. 불가능한 경우 값이 0입니다. 결과 정수 입력 값이 지정된 최소값보다 크거나 같고 지정된 최대값보다 작거나 같은 경우에만 테스트가 true를 반환합니다. </p> </td> 
   <td colname="col3"> <p>최소 또는 최대 필드 중 하나를 비워 두면 시스템은 64비트 부호 있는 정수에 사용할 수 있는 적절한 최소 또는 최대 값을 사용합니다. </p> <p> 조건에 지정된 최소 또는 최대 값이 정수 값으로 구문 분석되지 않으면 시스템은 0을 대체하며 데이터 집합 처리를 중지하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> DATETIME</span> </p> </td> 
   <td colname="col2"> <p>먼저 입력 필드를 날짜로 바꿉니다. 입력 필드를 유효한 날짜로 변환할 수 없으면 조건 테스트는 false를 반환합니다. 필드를 날짜로 설정할 수 있는 경우, 입력 날짜가 지정된 최소 날짜 이후와 지정된 최대 날짜 이후에만 true를 반환합니다. </p> </td> 
   <td colname="col3"> <p>최소 및 최대 날짜가 올바르지 않으면 데이터 세트가 생성되지 않습니다. </p> <p> 최소 또는 최대 날짜가 제공되지 않으면 시스템은 최소 날짜(1600년 1월 1일) 또는 최대 날짜(24세기 어느 한 시기)를 적절하게 대체합니다. </p> <p> Adobe은 <span class="wintitle"> DATETIME</span>에 다음 형식 중 하나를 사용하는 것이 좋습니다. </p> 
    <ul id="ul_44F469CC5D974382AF70D7B1975CF077"> 
     <li id="li_DB5FD4AFD6B34436ACD7C13282F64956"> 2013년 1월 1일 HH:MM:SS EDT </li> 
     <li id="li_307580C3F97D495BB16F1212DB38CE37"> 2013년 1월 1일 HH:MM:SS GMT </li> 
    </ul> <p> 지정하지 않은 경우 시간대의 기본값은 GMT입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="wintitle"> 어휘</span> </p> </td> 
   <td colname="col2"> <p>입력 필드가 최소값으로 지정된 문자열보다 사전적으로 크거나 같고 최대값에 지정된 문자열보다 작거나 같은 경우에만 true를 반환합니다. </p> </td> 
   <td colname="col3"> <p>사전적 비교에서는 문자를 왼쪽에서 오른쪽으로 이동하는 문자열에 있는 문자의 ASCII 값을 사용합니다. 일치하지 않는 첫 번째 문자의 경우 ASCII 값이 큰 문자는 둘 중 큰 것으로 간주됩니다. 한 문자열이 다른 문자열보다 짧지만, 그 지점까지 모든 문자가 동일하면 더 긴 문자열이 두 문자열 중 큰 문자열로 간주됩니다. 문자열이 문자값과 정확히 동일한 길이에 대한 문자이면 사전적으로 동일한 것으로 간주됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
