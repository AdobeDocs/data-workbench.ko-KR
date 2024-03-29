---
description: 비어 있지 않은 비교, 범위, 정규 표현식 및 문자열 일치를 포함한 테스트 작업 조건에 대한 정보입니다.
title: 테스트 작업 조건
uuid: 6a117569-1372-4095-972b-76289a45f19e
exl-id: 6c1f521b-a6b9-4bb7-bdfa-56c615b0c916
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1114'
ht-degree: 5%

---

# 테스트 작업 조건{#test-operation-conditions}

{{eol}}

비어 있지 않은 비교, 범위, 정규 표현식 및 문자열 일치를 포함한 테스트 작업 조건에 대한 정보입니다.

* [비교](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-fb2bdb3838504099b324b9838cdeeaac)
* [비어 있지 않음](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-1decb9d887894073a1b6b3d985729ac8)
* [Range](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-1db31583bb09418b8f49481a897b08a6)
* [정규 표현식](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-ae9c016502cb44128760c58f2d2d5297)
* [문자열 일치](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-f8d132085c6b4500bfbe4515b848142f)

## 비교 {#section-fb2bdb3838504099b324b9838cdeeaac}

다음 [!DNL Compare] 조건은 문자열 또는 숫자 값을 비교합니다. 문자열 값 비교를 위해 대/소문자를 고려할지 여부를 지정할 수 있습니다.

의 매개 변수 [!DNL Compare] 조건은 다음 표에 설명되어 있습니다.

<table id="table_05B1FBB2AED242D99081E62BE2FBEC60"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 대/소문자 구분 </td> 
   <td colname="col2">True 또는 False입니다. Type이 <span class="wintitle"> 어휘</span>. false로 설정하면 대문자나 소문자는 동일하게 간주됩니다. </td> 
   <td colname="col3"> true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항. 조건에 대한 참고 사항. </td> 
   <td colname="col3"> 댓글 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 A </td> 
   <td colname="col2"> 비교할 두 값 중 첫 번째 값입니다. 이 값은 조건에 있는 왼쪽 피연산자를 나타냅니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 B </td> 
   <td colname="col2"> 비교할 두 값 중 두 번째 값입니다. 이 값은 조건에 있는 올바른 피연산자를 나타냅니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 작업 </td> 
   <td colname="col2"> <p>비교 작업입니다. 사용 가능한 작업(및 그 의미)은 다음과 같습니다. 
     <ul id="ul_74F3C298E9CC4FE89897BA0052A9EB9F"> 
      <li id="li_1605FA73474E404A84056D40E7082623"> = 또는 ==(입력 A가 입력 B와 같음) </li> 
      <li id="li_F694A262ED7A4787B2A68B877339620C"> &lt;&gt; 또는 != (입력 A가 입력 B와 같지 않음) </li> 
      <li id="li_1A75437E23B64BEB92297E1C771092B0"> &lt; 입력 A가 입력 B보다 작음) </li> 
      <li id="li_B80ED6BE9DEA41FE84BC6BA3B7759276"> &lt;=(입력 A가 입력 B보다 작거나 같음) </li> 
      <li id="li_93148F34065F489E8E198DFB9F9F0E70"> &gt; (입력 A가 입력 B보다 큼) </li> 
      <li id="li_8A98EE9AED2445429805169040BB253D"> &gt;=(입력 A가 입력 B보다 크거나 같음) </li> 
     </ul> </p> </td> 
   <td colname="col3"> = </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 유형 </td> 
   <td colname="col2">작성할 비교 유형입니다. 사용 가능한 유형은 다음과 같습니다 <span class="wintitle"> 어휘</span>, <span class="wintitle"> 숫자</span>, 및 <span class="wintitle"> DATETIME</span>. 유형에 대한 설명은 다음을 참조하십시오 <a href="../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-types.md#concept-a9fca97a2f03464cb0cbab8b5f809d0a"> 테스트 작업 유형</a>. </td> 
   <td colname="col3"> <span class="wintitle"> 어휘</span> </td> 
  </tr> 
 </tbody> 
</table>

이 예제에서는 [!DNL Compare] 정의할 조건 [!DNL Log Entry Condition]. Data Workbench 서버가 각 이벤트 데이터 레코드를 읽으면 숫자 값 x-age 및 55를 비교합니다. 주어진 로그 항목의 경우 x-age 가 55보다 작거나 같은 경우 로그 항목이 데이터 집합 구성 프로세스에 포함됩니다.

![](assets/cfg_Condition_CompareCondition.png)

## 비어 있지 않음 {#section-1decb9d887894073a1b6b3d985729ac8}

다음 [!DNL Not Empty] 조건이 값을 포함하는지 또는 비어 있는지 확인하기 위해 필드를 검사합니다. 값이 [!DNL Input] 필드가 비어 있지 않습니다.

의 매개 변수 [!DNL Not Empty] 조건은 다음 표에 설명되어 있습니다.

| 매개 변수 | 설명 | 기본값 |
|---|---|---|
| 댓글 | 선택 사항. 조건에 대한 참고 사항. | 댓글 |
| 입력 | 내용을 확인할 로그 항목의 필드 이름입니다. |  |

이 예제에서는 입력 x-some-field로 를 가져와 필드가 비어 있지 않은지 테스트합니다. 필드가 채워지면 조건이 충족됩니다.

![](assets/cfg_Condition_NotEmpty.png)

## Range {#section-1db31583bb09418b8f49481a897b08a6}

다음 [!DNL Range] 조건은 입력 필드를 사용하여 해당 필드의 값이 지정된 최소(최소) 및 최대(최대) 매개 변수 값 내에 포함, 포함되는지 여부를 결정합니다.

의 매개 변수 [!DNL Range] 조건은 다음 표에 설명되어 있습니다.

<table id="table_1587D8D333804FC28024C0DFC2F2D4D3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 대/소문자 구분 </td> 
   <td colname="col2">True 또는 False입니다. 다음 경우에만 사용됩니다 <span class="wintitle"> 유형</span> is <span class="wintitle"> 어휘</span>. false로 설정하면 대문자나 소문자는 동일하게 간주됩니다. </td> 
   <td colname="col3"> true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항. 조건에 대한 참고 사항. </td> 
   <td colname="col3"> 댓글 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> 입력으로 사용할 로그 항목의 필드 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최소 </td> 
   <td colname="col2"> <p>범위의 하한. </p> <p> 이 매개 변수의 값은 리터럴 값 또는 문자열이어야 하며 필드 이름이 아니어야 합니다. 이 필드에 날짜를 사용하는 경우 시간대를 지정해야 합니다. 지원되는 표준 시간대 약자 목록은 <a href="../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 시간대 코드</a>. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 최대 </td> 
   <td colname="col2"> <p>범위의 상단입니다. </p> <p> <p>참고: 이 매개 변수의 값은 리터럴 값 또는 문자열이어야 하며 필드 이름이 아니어야 합니다. 이 필드에 날짜를 사용하는 경우 시간대를 지정해야 합니다. 지원되는 표준 시간대 약자 목록은 <a href="../../../../home/c-dataset-const-proc/c-time-zone.md#concept-9b540ec3e770490d94e9d5a985765477"> 시간대 코드</a>. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 유형 </td> 
   <td colname="col2">작성할 비교 유형입니다. 사용 가능한 유형은 다음과 같습니다 <span class="wintitle"> 어휘</span>, <span class="wintitle"> 숫자</span>, 및 <span class="wintitle"> DATETIME</span>. 유형에 대한 설명은 다음을 참조하십시오 <a href="../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-types.md#concept-a9fca97a2f03464cb0cbab8b5f809d0a"> 테스트 작업 유형</a>. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예제에서는 [!DNL Range] 정의할 조건 [!DNL Log Entry Condition]. Data Workbench 서버가 각 [!DNL event data] 레코드 는 x-age 및 55의 숫자 값을 비교합니다. 주어진 로그 항목의 경우 x-age 가 55 이상인 경우 로그 항목이 데이터 집합 구성 프로세스에 포함됩니다. 이 예에서는 와 동일한 함수를 수행합니다. [!DNL Compare] 조건 예. 자세한 내용은 [비교](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-op-con.md#section-fb2bdb3838504099b324b9838cdeeaac).

>[!NOTE]
>
>최소 또는 최대 매개 변수를 비워 두면 Data Workbench 서버는 사용 가능한 최소 또는 최대 정수 값으로 대체됩니다. 최소값은 0이고 최대값은 무한대입니다.

![](assets/cfg_Condition_RangeCondition.png)

## 정규 표현식 {#section-ae9c016502cb44128760c58f2d2d5297}

다음 [!DNL Regular Expression] 조건 테스트는 정규 표현식 패턴 일치를 사용합니다(참조). [정규 표현식](../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c))를 클릭하여 지정된 입력 필드의 값에 Matches 매개 변수에 지정된 패턴 중 하나와 일치하는 문자열이 포함되어 있는지 확인합니다.

입력이 문자열 벡터인 경우, 벡터의 첫 번째 값만 테스트에 사용됩니다. 다음 [!DNL Regular Expression] 조건은 전체 문자열 비교를 수행합니다. 부분 문자열을 식별하려면 &quot; 앞에 를 추가하고 추가해야 합니다.&#42;&quot; 값을 로 설정합니다.

의 매개 변수 [!DNL Regular Expression] 조건은 다음 표에 설명되어 있습니다.

<table id="table_0BF5F89F87C9493B8DABA97620074FAD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 대/소문자 구분 </td> 
   <td colname="col2"> True 또는 False입니다. false로 설정하면 대문자나 소문자는 동일하게 간주됩니다. </td> 
   <td colname="col3"> true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항. 조건에 대한 참고 사항. </td> 
   <td colname="col3"> 댓글 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> 입력으로 사용할 로그 항목의 필드 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 일치 </td> 
   <td colname="col2"> <p>입력 필드의 값에 대해 일치하는 정규 표현식 패턴입니다. </p> <p> <b> 정규 표현식 패턴을 추가하려면</b> 
     <ol id="ol_6D6467FF74334DEA8E8625C3B155D11D"> 
      <li id="li_9E13A63558FF44749C2E49BD50B7F770">마우스 오른쪽 단추 클릭 <span class="uicontrol"> 일치</span>. </li> 
      <li id="li_195A2F3B6B9442F5B1DACDE0FC96CE5C">클릭 <span class="uicontrol"> 새로 추가</span> &gt; <span class="uicontrol"> 정규 표현식</span>. </li> 
      <li id="li_225E98F8EF39426A9483B86EA2CFE6DF">텍스트 상자에 원하는 정규 표현식을 입력합니다. </li> 
     </ol> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예에서는 [!DNL Regular Expression] 조건을 사용하여 웹 사이트 트래픽에서 수집된 데이터의 필드를 일치시킵니다. cs(referrer-query) 필드에 정규 표현식과 일치하는 문자열이 들어 있는 경우에만 조건이 true를 반환합니다 `campaign=C[1-9][0-9]{4}`. 이 정규 표현식은 `campaign=C12345`. 하지만 패턴은 문자열과 일치하지 않습니다 `campaign=C0123&` 첫 번째 문자 다음에 `C` 이 범위 내에 없습니다. `1-9`.

![](assets/cfg_Condition_RegularExpression.png)

## 문자열 일치 {#section-f8d132085c6b4500bfbe4515b848142f}

다음 [!DNL String Match] 조건이 문자열 같음을 테스트합니다. 지정된 필드를 입력으로 사용하고 작업의 Matches 매개 변수에 지정된 문자열에 대해 각 로그 항목의 해당 필드 값을 테스트합니다. 대/소문자를 구분하는 일치 문자열 중 하나가 제공된 입력 필드의 값과 동일한 경우 작업이 true를 반환합니다. 다음의 경우에 [!DNL StringCondition] 에 일치 문자열이 없으면 조건이 false를 반환합니다. 입력이 문자열 벡터인 경우, 벡터의 첫 번째 값(문자열)만 테스트에 사용됩니다.

<table id="table_BD599BAA5DD54B278813B6C38AC8DE6B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매개 변수 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
   <th colname="col3" class="entry"> 기본값 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 대/소문자 구분 </td> 
   <td colname="col2"> True 또는 False입니다. false로 설정하면 대문자나 소문자는 동일하게 간주됩니다. </td> 
   <td colname="col3"> true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항. 조건에 대한 참고 사항. </td> 
   <td colname="col3"> 댓글 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> 입력으로 사용할 로그 항목의 필드 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 일치 </td> 
   <td colname="col2"> <p>입력 필드의 값과 일치하는 문자열입니다. </p> <p> <b>문자열을 추가하려면</b> 
     <ol id="ol_9E32218C771445D88357960475FAD6EB"> 
      <li id="li_A700747858D0470491783E9B3933DAFE">마우스 오른쪽 단추 클릭 <span class="uicontrol"> 일치</span>. </li> 
      <li id="li_9D1A2462EA404B0F84426176737CAFED">클릭 <span class="uicontrol"> 새로 추가</span> &gt; <span class="uicontrol"> 문자열</span>. </li> 
      <li id="li_E84D2439B59548E5B1803C64A295A18E">텍스트 상자에 원하는 문자열을 입력합니다. </li> 
     </ol> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

이 예에서는 웹 사이트 트래픽에서 수집된 데이터를 사용하여 [!DNL String Match] 조건. 조건은 입력 필드(cs-uri-stem)가 Matches 매개 변수에 지정된 두 문자열 중 하나와 일치하는지 여부를 테스트하고, cs-uri-stem 필드가 완전 일치 문자열인 경우 성공합니다 [!DNL /navigation/footer.asp] 또는 정확한 문자열 [!DNL /navigation/header.asp].

![](assets/cfg_Condition_StringMatch.png)
