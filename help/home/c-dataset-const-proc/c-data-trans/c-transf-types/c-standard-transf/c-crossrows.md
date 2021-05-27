---
description: 다른 변형처럼 교차 행 변환이 로그 소스의 데이터 행(로그 항목)에 적용됩니다.
title: 교차 행
uuid: 5910c150-6bec-4d98-b116-9b382fd54d3c
exl-id: 321f986e-44a9-454c-9311-0ae37a11a088
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 1%

---

# 교차 행{#crossrows}

다른 변형처럼 교차 행 변환이 로그 소스의 데이터 행(로그 항목)에 적용됩니다.

각 데이터 행에 대해 변환은 지정된 입력 필드의 값을 가져오고, 처리 단계 집합을 수행하고, 지정한 출력 필드에 결과를 기록합니다. 그러나 [!DNL CrossRows] 변형이 하나의 데이터 행에서 작동하는 경우(이 행을 출력 행이라고 함) 해당 행과 동일한 추적 ID와 연결된 하나 이상의 다른 데이터 행(이러한 행을 입력 행이라고 함)을 고려합니다. 따라서, 주어진 추적 ID의 경우, 각 출력 행에 대한 출력 필드의 값은 하나 이상의 입력 행에 대한 입력 필드의 값을 기반으로 한다.

변환에서는 변환에 대한 입력 행을 제한할 수 있는 여러 조건과 제약 조건을 제공합니다. Data Workbench 서버의 조건( [조건](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md) 참조), 출력 행에 대한 입력 행 범위 또는 출력 행의 시간에 대한 상대적 시간의 범위에서 이러한 제한을 표시할 수 있습니다. 변환의 조건 및 제약 조건을 만족하는 입력 행의 경우 출력 필드의 값을 결정하는 작업(예: SUM)을 적용할 수 있습니다.

>[!NOTE]
>
>작동하려면 [!DNL CrossRows] 변형을 사용하려면 데이터가 제시간에 정렬되어 소스 데이터의 추적 ID별로 그룹화되어야 합니다. 따라서 [!DNL CrossRows]은 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일에 정의된 경우에만 작동합니다.

다음 테이블에서 매개변수 설명을 검토할 때 다음 사항을 기억하십시오.

* 출력 행은 특정 시점에 변환에서 작동하는 데이터의 행입니다.
* 입력 행은 입력 필드의 값이 변환에 대한 입력으로 사용되는 다른 데이터 행(출력 행 전, 후 또는 포함)입니다. 입력 행에는 입력 조건, 키, 행 시작, 행 종료, 시간 시작 및 시간 종료 매개 변수가 적용됩니다.

<table id="table_152851484AFF4C50AF736DC62FAA43E3"> 
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
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항입니다. 변환에 대한 참고 사항. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 변환 출력을 특정 로그 항목으로 제한합니다. 특정 로그 항목에 대해 조건이 충족되지 않으면 출력 매개 변수의 필드는 변경되지 않은 상태로 유지됩니다. 입력은 다른 로그 항목에 영향을 주는 데 사용할 수 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> 입력으로 사용할 입력 행의 필드 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 조건 </td> 
   <td colname="col2"> 특정 입력 행에서만 변형을 위한 입력을 허용합니다. 특정 입력 행에 대해 입력 조건이 충족되지 않으면 해당 행의 입력 필드가 무시되며 다른 출력 행에 영향을 주지 않습니다. 그러나 해당 행의 출력 필드는 지정된 조건에 따라 계속 수정됩니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 키 </td> 
   <td colname="col2"> <p>선택 사항입니다. 키로 사용할 필드의 이름입니다. </p> <p> 키를 지정하면, 지정된 출력 행의 입력 행은 출력 행과 동일한 키 값을 갖는 행의 연속 블록으로 제한됩니다. 이 제한 사항은 <span class="wintitle"> CrossRows</span> 변환의 다른 매개 변수로 입력 행에 배치된 다른 모든 제한 사항 외에 있습니다. </p> <p> 예를 들어, 웹 데이터를 사용하여 작업하는 경우 필드 x-session-key(각 세션에 대한 고유한 값이 있음)를 키에 지정하는 경우 변환의 입력 행은 출력 행과 동일한 x-session-key 값을 갖는 행으로 제한됩니다. 따라서 출력 행과 동일한 세션 중에 발생하는 페이지 보기를 나타내는 입력 행만 고려합니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작업 </td> 
   <td colname="col2"> <p>각 출력 행에 대해 입력 조건, 키, 행 시작, 행 끝, 시간 시작 및 시간 종료 매개변수에 정의된 모든 조건을 충족하는 모든 입력 행에 적용된 작업을 통해 출력을 생성합니다. 
     <ul id="ul_C01CCF73A9544BCFB7B1105042FEF2DD"> 
      <li id="li_2D1A192970904499AB9F4431D51106D7"> ALL은 입력 행에서 입력 필드의 모든 값을 가져와 벡터로 출력합니다. </li> 
      <li id="li_B8863724AD924DE5BDBC987143548257"> SUM은 입력 행으로부터 입력 필드의 값을 숫자로 해석하여 합합니다. </li> 
      <li id="li_BF930069DCEA4E0B80893C3C06CAE100"> 첫 번째 행은 첫 번째 입력 행에서 입력 필드의 값을 출력합니다. </li> 
      <li id="li_04B9E2D88C0847E28101FC830C18D8E2"> 마지막 행 은 마지막 입력 행에서 입력 필드의 값을 출력합니다. </li> 
     </ul> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> 출력 필드의 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 행 시작/행 끝 </td> 
   <td colname="col2"> <p>선택 사항입니다. 출력 행에 상대적인 입력 행 범위를 지정합니다. 예를 들어, 행 시작 값 "0"은 출력 행 앞에 있는 모든 행을 제외합니다. 행 시작 값 "1"은 출력 행도 제외합니다. 일반적인 범위는 다음과 같습니다. 
     <ul id="ul_B030F32A5146430BA50DD4FAB4A527B0"> 
      <li id="li_30DFB8C0265349C295943A1CB8077B86"> 시작 0:이 행 및 그 이후의 모든 행. </li> 
      <li id="li_9090C2E94E394351867BC5B78F27B41C"> 시작 1:모든 후속 행. </li> 
      <li id="li_F870DC913E3F45BA94EE2EC04D344DE0"> 종료 0:이 행 및 모든 이전 행. </li> 
      <li id="li_B8A576E419744D84AB1298E5155B583E"> 종료 -1:모든 이전 행. </li> 
      <li id="li_CD2307A262D34542A2860FF07005CAD7"> 시작 -1, 끝 -1:이전 행입니다. </li> 
      <li id="li_6BF30B7BB7CC40A68B2332A3C11DD3B5"> 1, 1 종료:다음 행. </li> 
     </ul> </p> </td> 
   <td colname="col3"> 모든 행 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간 시작/시간 종료 </td> 
   <td colname="col2"> <p>선택 사항입니다. 출력 행의 시간을 기준으로 하는 시간 범위를 지정합니다. 예를 들어 30분의 시간 종료에는 출력 행 후 30분 이내에 발생하는 모든 행이 포함됩니다. -30분의 시간 시작에는 출력 행 30분 이내에 발생하는 모든 행이 포함됩니다. </p> <p> 사용 가능한 시간 단위는 일, 주, 시간, 분, 밀리초, 틱(100나노초) 및 ns(나노초)입니다. </p> </td> 
   <td colname="col3"> 항상 </td> 
  </tr> 
 </tbody> 
</table>

이 예제의 [!DNL CrossRows] 변환은 다음 페이지 보기 시간을 기준으로 각 페이지 보기에 대해 찾기 위해 웹 데이터 행에 적용됩니다. [!DNL CrossRows]은 데이터 집합 구성 프로세스의 변형 단계 동안에만 적용된다는 것을 알고 있으므로 데이터 행의 순서가 방문자(각 방문자는 고유한 추적 ID를 가지고 있음)와 시간으로 지정됩니다.

x-timestamp 입력 필드는 x-is-page-view 필드가 채워지는 입력 행에만 고려됩니다(데이터 행이 페이지 보기를 나타내는지 표시). Key 매개 변수에 대해 x-session-key 필드(각 세션에 대한 고유한 값)가 지정됩니다. 따라서, 변환을 위한 입력 행(로그 항목)은 출력 행과 동일한 값을 갖는 행의 연속 블록으로 제한됩니다. 즉, 변환에 대해 고려하려면 입력 행이 출력 행의 페이지 보기와 동일한 세션 중에 발생하는 페이지 보기를 나타내야 합니다. 첫 번째 행 작업은 [!DNL Input] 조건을 만족하고 출력 행과 동일한 x-session-key 값을 갖는 첫 번째 입력 행에서 출력 필드의 값을 가져옵니다.

![](assets/cfg_TransformationType_CrossRows.png)

[!DNL CrossRows] 은 입력 크기와 출력 크기에 비례하는 시간을 실행합니다. 즉, SUM, FIRST ROW 및 LAST ROW 작업의 경우 다른 변형보다 효율적이지 않습니다. ALL의 경우 지정된 추적 ID에 대한 총 행(로그 항목)에 비례하는 각 데이터 행(로그 항목)에 대한 데이터 양을 출력하도록 [!DNL CrossRows]을 구성할 수 있으므로 상황이 더 복잡합니다.
