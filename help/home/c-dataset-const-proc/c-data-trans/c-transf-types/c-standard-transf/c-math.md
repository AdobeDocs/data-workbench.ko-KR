---
description: 수학 변형을 사용하면 로그 항목 내의 필드에 대해 산술 연산을 사용할 수 있습니다.
solution: Analytics
title: 수학
topic: Data workbench
uuid: 9e1a5950-8fb2-48e9-b9a1-82c5165fba10
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 수학{#math}

수학 변형을 사용하면 로그 항목 내의 필드에 대해 산술 연산을 사용할 수 있습니다.

연산에는 소수점 정수와 부동 소수점 상수가 포함될 수 있습니다.

<table id="table_FDF3DDF1960E43E391A67C9DC2A0E302"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1">  이름  </td> 
   <td colname="col2"> 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 설명 </td> 
   <td colname="col2"> 선택 사항입니다. 변환에 대한 참고 사항. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 이 변환이 적용되는 조건입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 표현식 </td> 
   <td colname="col2"> <p>수행할 계산을 설명하는 산술 표현식입니다. </p> <p> 아래 나열된 작업 및 함수를 사용할 수 있으며 표현식에 필드 이름을 통합할 수 있습니다. </p> <p> 작업 
     <ul id="ul_DB5915FADA0A41A3B11F1F48615F40A9">
      <li id="li_CA9EA97243F04760A81313C17EE057B3"> 추가 (+) </li>
      <li id="li_908A272EBA2340098C20F22AA8D9ED26"> 빼기 (-) </li>
      <li id="li_C62257FF3AAB436D9148BBEA441621D7"> 곱하기 (*) </li>
      <li id="li_B5A9EAB3E49D4CB9A297172199F23542"> 나누기 (/) </li>
      <li id="li_D2D2B51DB2C8412A9B6F9D5F3CC03F8A"> 나머지 (%) </li>
      <li id="li_07E7E368FFD2437A852B785E159848E5"> 거듭제곱 (^) </li>
     </ul></p> <p>함수 
     <ul id="ul_E335AE8D684340AA998C4A2633FFDEE1">
      <li id="li_E036FF0B5DF244DDBFEDA9BFEDC62251"> sgn(x). x가 양수이면 1을, x가 0이면 0을, x가 음수이면 -1을 반환합니다. </li>
      <li id="li_90CD8899DDC14778A95930C2768C82BC"> abs(x). x의 절대값을 반환합니다. </li>
      <li id="li_F4AF23F343F74BD88B7166B1C2BB065E"> floor(x). x보다 작거나 같은 최대 정수를 반환합니다. </li>
      <li id="li_A31379A3659240C3A629BFAF19A6DDF1"> round(x). 가장 가까운 정수를 x에 반환합니다. </li>
      <li id="li_9C0A0F3A4A304026B543F2A64B98B922"> log(b,x). x base b의 로그를 반환합니다. </li>
      <li id="li_124D62C2CA5A42CBBCC5DB18FAA8920E"> min(x,y,..). 모든 인수의 최소 값을 반환합니다. </li>
      <li id="li_3B7B9FC1C0BF4E7688F9F49130B97B7F"> max(x,y,..). 모든 인수 중 가장 큰 인수를 반환합니다. </li>
     </ul></p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> 산술 연산의 결과를 포함하는 필드의 이름입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

이 예에서는 웹 사이트 트래픽에서 수집된 데이터의 필드를 사용하며 x-page-duration이라는 새 필드는 x-timestamp에서 x-last-pv-timestamp를 빼고 1을 추가하여 계산됩니다. 출력은 방문자의 마지막 페이지 보기의 타임스탬프를 나타내는 사용자 정의 필드 x-last-pv-timestamp가 채워지거나 &quot;비어 있지 않음&quot;인 경우에만 계산됩니다.

![](assets/cfg_TransformationType_Math.png)

조건에 대한 자세한 내용은 [!DNL Not Empty] 조건을 [참조하십시오](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md).
