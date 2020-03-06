---
description: 정규 표현식은 쿼리 엔티티 패널을 포함한 모든 데이터 워크벤치 검색 필드에서 사용됩니다.
solution: Analytics
title: 정규 표현식
topic: Data workbench
uuid: f3a0119d-6fac-4f63-8dca-4db32d2a737a
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Regular Expressions{#regular-expressions}

정규 표현식은 쿼리 엔티티 패널을 포함한 모든 데이터 워크벤치 검색 필드에서 사용됩니다.

* [정규 표현식 정보](../../home/c-dataset-const-proc/c-reg-exp.md#section-cc9dc7293bb04fc0b41fe8acdee708f0)
* [정규 표현식 용어](../../home/c-dataset-const-proc/c-reg-exp.md#section-80b0d54f731e448391532ab3eb3c525c)
* [문자 일치 정보](../../home/c-dataset-const-proc/c-reg-exp.md#section-ec4497e3160c47ba9b828d939761b3e0)
* [메타 문자 사용](../../home/c-dataset-const-proc/c-reg-exp.md#section-e29a804336304ea1ba33d40d60139aa2)
* [패턴 추출](../../home/c-dataset-const-proc/c-reg-exp.md#section-4389779653b64f6cb7c47615b25c1a79)

## 정규 표현식 정보 {#section-cc9dc7293bb04fc0b41fe8acdee708f0}

정규 표현식은 패턴을 찾고 텍스트에서 하위 문자열을 추출하는 영숫자 문자와 메타 문자로 구성된 텍스트 패턴입니다. 정규 표현식은 컴퓨터 프로그래밍에 널리 사용되고 펄 같은 언어의 일부분입니다.

복잡한 문자열 패턴을 식별하고 추출하기 위해 데이터 워크벤치 서버는 일부 변형 및 조건에서 정규 표현식을 사용합니다. 다음은 정규 표현식에 대한 간단한 안내서입니다.

이 부록은 일반적인 표현식에 대한 포괄적인 소개가 아닙니다. 특히 참고로 O&#39;Reilly의 Mastering Regular *Expressions, Jeffrey E의 제2Edition* .F.친구

## 정규 표현식 용어 {#section-80b0d54f731e448391532ab3eb3c525c}

| 용어 | 정의 |
|---|---|
| 리터럴 | 리터럴은 정규 표현식에서 특정 문자 시퀀스를 찾기 위해 사용하는 문자입니다. 예를 들어, 에서 제품을 찾으려면 문자열 [!DNL shop/products.html]제품이 문자 그대로 또는 문자열에서 실제로 찾고 있는 것입니다. |
| 메타 문자 | 메타문자는 정규 표현식 컨텍스트에서 고유한 해석을 갖는 특수 문자입니다. 예: 마침표(.) 는 모든 문자와 일치하는 메타문자입니다. |
| 시퀀스 이스케이프 | 이스케이프 시퀀스는 단순히 정규 표현식 엔진에서 메타문자 중 하나를 리터럴로 사용하려는 것임을 알리는 방법입니다. 이스케이프 시퀀스는 항상 백슬래시 문자(`\`)로 시작됩니다. 정규 표현식 엔진은 메타문자 앞에 백슬래시(메타문자라고도 함)를 배치하여 이스케이프된 메타 문자를 리터럴로 해석합니다. 예를 들어 메타 문자 기간(`.`)을 일치시키려면 이스케이프 시퀀스를 사용해야 합니다. 그러나 168.196.0.11 문자열의 마침표 중 하나를 일치시키려면 백슬래시와 마침표(`\.`)로 구성된 정규 표현식을 사용할 수 있습니다. |
| 패턴 | 정규 표현식의 축약입니다. 본질적으로 정규 표현식은 대상 문자열과 일치시키려는 패턴입니다. |
| 대상 문자열 | 이 용어는 원하는 패턴을 찾기 위해 검색하는 문자열을 나타냅니다. |

## 문자 일치 정보 {#section-ec4497e3160c47ba9b828d939761b3e0}

리터럴 일치는 이스케이프 문자가 없는 리터럴 문자열을 사용하며 대상 문자열에서 해당 문자열이 대상 문자열의 하위 문자열인지 확인합니다.

이 예제에서는 문자 일치를 사용하는 방법을 확인합니다. 웹 사이트 트래픽에서 데이터가 수집되고 cs(레퍼러) 필드에 다음 값이 포함되어 있는 상황을 고려하십시오.

`http://www.abc.com/adventurenews/today.html?ad=123AZ45`

레퍼러가 광고 중 하나를 클릭한 사람을 나타내는지 여부를 결정하려면 레퍼러에 문자열 광고가 포함되어 있는지 확인해야 합니다. 간단히 리터럴 문자열 광고를 사용하여 대상 문자열을 검색하고 트래픽을 사이트로 라우팅하는 데 광고가 사용되었는지 확인할 수 있습니다. 이 문자열이 대상 문자열과 일치하지만 두 위치에서 일치하므로 모호하며 잘못된 양수로 이어질 수 있습니다.

다음 URL에는 문자열 광고가 서로 다른 두 위치에 포함됩니다.

`http://www.abc.com/ad vertnews/today.html?ad =123AZ45`

따라서 특정 광고 캠페인의 결과로 시작된 세션을 결정하려고 하는 경우 일반 표현식으로 문자 광고를 사용하기만 해도 충분하지 않습니다. 리터럴을 &quot;ad=&quot;로 변경하면 이러한 모호성이 제거되고 표현식이 한 번만 일치하게 됩니다. 하지만 레퍼러가 광고 캠페인의 일부인지 확인하는 데 충분하지 않을 수 있습니다. 다음 레퍼러를 고려해 보십시오.

`http://www.xyz.com/hello.html?pad=something`

다른 사람이 사이트에 대한 링크를 만드는 데 사용할 수 있는 URL을 제어할 수 없습니다. 리터럴 검색은 광고 캠페인의 결과로 시작된 세션을 찾을 수 없는 단순한 메커니즘입니다. 다음 섹션에서는 보다 유연하고 강력한 일치를 위해 메타 문자를 사용하는 방법에 대해 설명합니다.

## 메타 문자 사용 {#section-e29a804336304ea1ba33d40d60139aa2}

메타문자는 다른 문자에 대한 정보를 제공하는 프로그램 또는 데이터 필드의 특수 문자입니다.

| 메타문자 | description |
|---|---|
| . (점) | 예를 들어 단일 문자와 일치합니다.&quot;xyz&quot; 또는 &quot;xxz&quot;와 `re:x.z` 일치합니다. |
| * (별) | 하나 이상의 문자와 일치합니다(예:&quot;ZZZ&quot;와 `re:Z*` 일치합니다. |
| ? (와일드카드) | 이전 식의 0 또는 1과 일치하여 최소값 일치를 적용합니다(예:&quot;xy&quot; 및 &quot;xyz&quot;와 `xy?z` 일치합니다. |

추가적인 일반 표현식을 사용하여 보다 복잡한 검색 문자열을 만들 수도 있습니다.

**목록, 범위 및 OR**

리터럴 일치를 사용하면 단일 문자열을 찾을 수 있지만 대괄호, 대시 및 파이프를 사용하면 대상 문자열에서 찾을 항목 목록을 정의할 수 있습니다.

<table id="table_18B86955EC3748079E7C176273ADE92B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 메타 문자... </th> 
   <th colname="col2" class="entry"> 정규 표현식 프로세서는... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 대괄호([ ]) </td> 
   <td colname="col2"> 대괄호 안의 모든 문자를 단일 문자 위치로 일치시킵니다. 예를 들어 [AB]는 문자 A나 문자 B와 일치하는 명령이며 [0123456789]는 0에서 9 사이의 모든 문자와 일치한다고 말합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 대시(-) </td> 
   <td colname="col2"> <p>문자 범위를 일치시킵니다. 따라서 [0123456789]를 쓰는 대신 [0-9]만 쓸 수 있습니다. </p> <p> 이 범위는 하나의 대괄호 안에 있는 문자 범위와 여러 범위로 확장할 수 있습니다. 예를 들어 [0-9A-C]는 0에서 9까지의 문자와 A에서 C까지의 문자를 찾습니다. </p> <p> <p>참고: 대괄호 안에 있는 문자(-)로 대시(-)를 테스트하려면, 첫 번째 또는 마지막에 와야 합니다. 예를 들어 - 및 0~9에 대해 [-0-9] 테스트를 수행합니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 파이프 (|) </td> 
   <td colname="col2"> 두 선택 항목 중 하나를 지정된 대상 문자열에 일치시킵니다. 예를 들어 b|nat는 bat 또는 nat와 일치합니다. </td> 
  </tr> 
 </tbody> 
</table>

다음 예를 생각해 보십시오.

| 패턴 | 문자열 | 일치 |
|---|---|---|
| Win9`[58]` | OS=Win95 | Win95 |
| Win95 | 8 | OS=Win98 | Win98 |
| `[0-9]` | Mozilla/3.0 | 3 |
| 레슨`[A-Z]` | 제1과 | 소문자 a가 대문자 A에서 Z까지의 범위에 있지 않으므로 일치하지 않습니다. |

**부정**

부정 행위는 주어진 문자를 제외한 모든 항목을 일치시키고자 한다고 말하는 방법입니다. 꺾은 메타문자, 곡절 또는 삽입 기호(`^`)는 대괄호 안의 첫 번째 문자로 사용하여 대괄호 안의 나머지 문자를 제외한 모든 문자로 일치하게 합니다. 예를 들어, 세미콜론(`;`)을 제외한 모든 문자와 일치시키려면

[`^;`]

세미콜론을 제외한 모든 문자와 일치합니다.

**포지셔닝**

대상 문자열의 시작 또는 끝에 일치를 적용하려면 두 메타 문자 중 하나가 사용됩니다.

| 이 메타 문자... | 정규 표현식 프로세서는... |
|---|---|
| 곡절 또는 삽입 기호(`^`) | 문자열의 시작 부분과 일치합니다. 예를 들어 ^`[Tt]`He would match the target string &quot;The Beginning&quot; but would not match &quot;This is the beginning.&quot; |
| 달러 기호 (`$`) | 문자열 끝과 일치합니다. 예를 들어 `[Ee]`nd$는 &quot;This is the end&quot;와 일치하지만 &quot;The end is a special time&quot;과 일치하지 않습니다. |

>[!NOTE]
>
>정규 표현식의 시작 부분과 끝 부분에 ^이 포함된 경우 전체 대상 문자열이 정규 표현식과 일치해야 합니다.

**일치하는 항목**

마침표(.) 는 대상 문자열의 모든 문자와 일치하는 특수 메타 문자입니다. 예를 들어 정규 표현식은 정확히 세 자 길이의 모든 대상 문자열과 `^…$` 일치합니다. 정규 표현식 &quot;...&quot;은 3자 이상을 포함하는 모든 대상 문자열과 일치합니다.

**반복 패턴**

반복 메타 문자를 사용하면 패턴을 두 번 이상 일치시킬 수 있습니다.

<table id="table_6A14333D6C264A48ADF1EBBAF687CADD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 메타 문자... </th> 
   <th colname="col2" class="entry"> 정규 표현식 프로세서는... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 물음표(?) </td> 
   <td colname="col2"> 메타 문자(?) 바로 앞에 있는 문자나 인스턴스의 인스턴스와 일치하지 않습니다. 예를 들어 패턴 rea?d는 빨간색과 읽기와 일치합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 별표 (*) </td> 
   <td colname="col2"> 메타 문자(*) 바로 앞에 있는 0개 이상의 문자를 일치시킵니다. 예를 들어 패턴 [0-9]*은 0부터 9까지의 모든 문자(임의 정수)와 일치합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 플러스 (+) </td> 
   <td colname="col2"> 이전 문자 또는 범위의 하나 이상의 항목을 일치시킵니다. 예를 들어 3+의 패턴은 3과 일치하지만 통과하지는 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> {n} </td> 
   <td colname="col2"> <p>진행 문자 또는 범위를 정확하게 n번 일치시킵니다. 다음 패턴은 미국 전화 번호와 일치합니다.[0-9]{3}-[0-9]{3}-[0-9]{4}. </p> <p> 최적의 패턴은 아니지만 대상 문자열이 올바른 형식인지 여부를 결정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> {n,m} </td> 
   <td colname="col2"> 이전 문자와 최소 n번 이상 m번 일치시킵니다. 예를 들어, {1,2}d는 음식과 음식은 일치하지만 음식은 일치하지 않습니다. </td> 
  </tr> 
 </tbody> 
</table>

## 패턴 추출 {#section-4389779653b64f6cb7c47615b25c1a79}

패턴 일치는 정규 표현식의 힘 중 일부에 불과합니다. 정규 표현식은 대상 문자열의 키 부분을 추출하는 메커니즘을 제공합니다. 이것은 왼쪽 및 오른쪽 괄호를 사용하여 수행됩니다. 이러한 추출은 일반적으로 다른 프로세스에 대한 입력으로 사용되며 *%position%*(위치)을 사용하여 액세스합니다. 여기서 position은 괄호 집합이 일치하는 수를 참조하는 정수입니다.

패턴 추출의 다음 예를 고려하십시오.

<table id="table_BC8D471B966844049FFFCDEC0F183941"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 패턴 </th> 
   <th colname="col2" class="entry"> 문자열 </th> 
   <th colname="col3" class="entry"> 일치 </th> 
   <th colname="col4" class="entry"> 추출 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Win(9[58]) </td> 
   <td colname="col2"> OS=Win95 </td> 
   <td colname="col3"> Win95 </td> 
   <td colname="col4"> %1% = 95 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> (Win)(95|8) </td> 
   <td colname="col2"> OS=Win98 </td> 
   <td colname="col3"> Win98 </td> 
   <td colname="col4"> <p>%1% = Win </p> <p> %2% = 98 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mozilla/([0-9]).([0-9]) </td> 
   <td colname="col2"> Mozilla/3.0 </td> 
   <td colname="col3"> Mozilla/3.03 </td> 
   <td colname="col4"> <p>%1% = 3 </p> <p> %2% = 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 수업([A-Z]) </td> 
   <td colname="col2"> 제1과 </td> 
   <td colname="col3"> 소문자 a가 대문자 A에서 Z까지의 범위에 있지 않으므로 일치하지 않습니다. </td> 
   <td colname="col4"> </td> 
  </tr> 
 </tbody> 
</table>

