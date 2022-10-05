---
description: REMatch 변형은 정규 표현식을 사용하여 입력에서 찾고 캡처할 하나 이상의 패턴을 지정하는 패턴 일치 변형입니다.
title: 재일치
uuid: 8ef80bfa-aea2-45a1-a7d9-38ad33043886
exl-id: 571e6f1c-f557-49c3-9e7c-c31f06132ec7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 3%

---

# 재일치{#rematch}

{{eol}}

REMatch 변형은 정규 표현식을 사용하여 입력에서 찾고 캡처할 하나 이상의 패턴을 지정하는 패턴 일치 변형입니다.

변환은 정규 표현식에서 각 캡처 하위 패턴에 대한 출력 필드를 구성합니다. 정규 표현식이 입력 필드와 일치하지 않으면 출력이 비어 있고 출력 필드가 이미 있으면 값이 빈 값으로 바뀝니다. 정규 표현식 사용에 대한 간단한 지침은 [정규 표현식](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).

>[!NOTE]
>
>다음 [!DNL REMatch] 변환 기능은 [!DNL RETransform] 변환( [RETransform](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-retransform.md#concept-23f80aa0bc204565b337e5c4931f6a74)). 정규 표현식을 사용하여 문자열을 캡처하고 단일 출력 필드에 해당 문자열을 저장합니다.

[!DNL REMatch] 문자열을 여러 개보다 효율적으로 구문 분석합니다. [!DNL RETransform] 변형 또는 단일 [!DNL RETransform] 변환 후 [!DNL Flatten] 변환. 자세한 내용은 [평면화](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-flatten.md#concept-7acd351a6d2444bd960ca412ae3333ce).

<table id="table_7077578512B249E986BC79AE770CBD9A"> 
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
   <td colname="col2"> 변환의 설명 이름입니다. 여기에 이름을 입력할 수 있습니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 대/소문자 구분 </td> 
   <td colname="col2"> True 또는 False입니다. 대/소문자를 구분하는지 여부를 지정합니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항. 변환에 대한 참고 사항. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 이 변환이 적용되는 조건입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 표현식 </td> 
   <td colname="col2"> 일치에 사용되는 정규 표현식입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> 정규 표현식이 평가되는 필드입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> <p>출력 문자열 또는 벡터의 이름입니다. 문자열 벡터를 입력으로 하는 경우 출력도 문자열 벡터입니다. </p> <p> 표현식에서 각 캡처 하위 패턴에 대해 출력 필드가 있어야 합니다. </p> </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!DNL REMatch] 변형은 매우 느릴 수 있으며 데이터 처리 시간의 대부분을 고려할 수 있습니다.

이 예제에서는 [!DNL REMatch] 변환은 YYYY-MM-DD 형식의 날짜를 x-년, x-월 및 x-일 필드로 구문 분석합니다. 날짜 2007-01-02의 경우 x-year, x-month 및 x-day 값은 각각 2007, 01 및 02입니다.

![](assets/cfg_TransformationType_REMatch.png)
