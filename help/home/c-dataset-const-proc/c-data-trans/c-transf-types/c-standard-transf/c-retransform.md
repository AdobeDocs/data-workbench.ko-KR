---
description: RETransform(정규 표현식) 변환은 정규 표현식을 사용하여 입력에서 찾고 캡처할 패턴을 지정하고 지정된 출력 필드에 캡처된 문자열을 저장하는 패턴 일치 변형입니다.
title: 재변환
uuid: 60b5b60e-678a-416d-b5c3-57b1bbefce7d
exl-id: 2595f782-0efb-4a2a-84bd-fdb04baf0852
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---

# 재변환{#retransform}

{{eol}}

RETransform(정규 표현식) 변환은 정규 표현식을 사용하여 입력에서 찾고 캡처할 패턴을 지정하고 지정된 출력 필드에 캡처된 문자열을 저장하는 패턴 일치 변형입니다.

정규 표현식은 전체 입력 문자열에 대해 평가됩니다. 입력이 정규 표현식에 지정된 패턴과 일치하지 않으면 데이터가 캡처되지 않습니다. 정규 표현식 사용에 대한 간단한 지침은 [정규 표현식](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).

>[!NOTE]
>
>다음 [!DNL RETransform] 변환 기능은 [!DNL REMatch] 변환( [REMatch](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-rematch.md#concept-7f0b1caad1df46aabef4448f88261a8e)참조)입니다. 생각해보면 [!DNL RETransform] 의 조합으로 [!DNL REMatch] 및 [!DNL Format] 변형 작업 매개 변수(다음 테이블의 작업 참조)가 &quot;RESULTS&quot;로 설정된 경우 [!DNL RETransform] 는 [!DNL REMatch] 및 [!DNL Union] 변형

<table id="table_51B7342E6A5E4E31913BD0F6A6ACC424"> 
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
   <td colname="col1"> 기본값 </td> 
   <td colname="col2"> 조건이 충족되고 입력 값을 사용할 수 없거나 정규 표현식이 입력 값과 일치하지 않는 경우 사용할 기본값입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작업 </td> 
   <td colname="col2"> <p>결과가 처리되는 방식을 지정합니다. RESULTS의 기본 설정은 일치하는 패턴을 가져오고 추출되는 패턴에서 문자열 벡터를 만듭니다. </p> <p> 또는 특정 형식의 간단한 문자열 출력을 만드는 서식 문자열일 수 있습니다. 이 기술을 사용하여 % 기호 사이에 일치하는 각 패턴의 위치에 해당하는 번호를 지정합니다. 예를 들어 일치하는 첫 번째 패턴은 %1%이고 세 번째 패턴은 %3%입니다. 형식 문자열에 문자 그대로 다른 문자를 지정합니다. </p> </td> 
   <td colname="col3"> 결과 </td> 
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
   <td colname="col2"> 출력 문자열의 이름입니다. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!DNL RETransform] 변형은 매우 느릴 수 있으며 데이터 처리 시간의 대부분을 고려할 수 있습니다.

이 예에서는 웹 사이트 방문자가 사용하는 Windows 운영 체제의 버전을 격리하고 해당 값으로부터 필드 x-windows 버전을 만듭니다. 이 경우 출력 값은 단순히 버전 번호가 됩니다.

![](assets/cfg_TransformationType_RegularExpression.png)

가독성을 위해 버전 번호 앞에 문자열 &quot;버전&quot;을 포함하려면 작업 매개 변수를 &quot;RESULTS&quot;에서 &quot;버전 %1%&quot;로 변경하십시오. 출력에 리터럴 퍼센트 기호(%)를 포함하려면 &quot;%&quot;에서와 같이 두 번째 퍼센트 기호로 이스케이프 처리합니다.
