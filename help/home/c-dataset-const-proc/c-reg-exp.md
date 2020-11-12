---
description: 정규 표현식은 쿼리 엔티티 패널을 포함한 모든 데이터 워크벤치 검색 필드에서 사용됩니다.
solution: Analytics
title: 정규 표현식
topic: Data workbench
uuid: f3a0119d-6fac-4f63-8dca-4db32d2a737a
translation-type: tm+mt
source-git-commit: 0727e5b18c89a22b6ee775b1293d3b68e5cee81c
workflow-type: tm+mt
source-wordcount: '1418'
ht-degree: 2%

---


# 정규 표현식{#regular-expressions}

정규 표현식은 쿼리 엔티티 패널을 포함한 모든 데이터 워크벤치 검색 필드에서 사용됩니다.

* [정규 표현식 정보](../../home/c-dataset-const-proc/c-reg-exp.md#section-cc9dc7293bb04fc0b41fe8acdee708f0)
* [정규 표현식 용어](../../home/c-dataset-const-proc/c-reg-exp.md#section-80b0d54f731e448391532ab3eb3c525c)
* [문자 일치 정보](../../home/c-dataset-const-proc/c-reg-exp.md#section-ec4497e3160c47ba9b828d939761b3e0)
* [메타 문자 사용](../../home/c-dataset-const-proc/c-reg-exp.md#section-e29a804336304ea1ba33d40d60139aa2)
* [패턴 추출](../../home/c-dataset-const-proc/c-reg-exp.md#section-4389779653b64f6cb7c47615b25c1a79)

## 정규 표현식 정보 {#section-cc9dc7293bb04fc0b41fe8acdee708f0}

정규 표현식은 패턴을 찾아 텍스트에서 하위 문자열을 추출하는 영숫자 문자와 메타 문자로 구성된 텍스트 패턴입니다. 정규 표현식은 컴퓨터 프로그래밍에 널리 사용되고 펄과 같은 언어의 필수 요소입니다.

복잡한 문자열 패턴을 식별하고 추출하기 위해 데이터 워크벤치 서버는 일부 변환 및 조건에서 정규 표현식을 사용합니다. 다음은 정규 표현식에 대한 간단한 안내서입니다.

이 부록은 일반적인 표현식에 대한 포괄적인 소개가 아닙니다. 특히 좋은 표현은 O&#39;Reilly 출판사가 *Mastering Regular Expressions, 2번째 Edition* , Jeffrey E. F. Fridl.

## 정규 표현식 용어 {#section-80b0d54f731e448391532ab3eb3c525c}

| 용어 | 정의 |
|---|---|
| 리터럴 | 리터럴은 특정 문자 시퀀스를 찾기 위해 일반 표현식에서 사용하는 문자입니다. 예를 들어 문자열 제품에서 제품을 찾으려면 문자열 제품 [!DNL shop/products.html]이 문자 그대로 또는 문자열에서 문자 그대로 검색하는 것입니다. |
| 메타 문자 | 메타 문자는 정규 표현식 컨텍스트에서 고유한 해석을 가진 특수 문자입니다. 예: 마침표(.) 는 모든 문자와 일치하는 메타 문자입니다. |
| 이스케이프 시퀀스 | 이스케이프 시퀀스는 단순히 정규 표현식 엔진에 문자 중 하나를 리터럴로 사용하고자 한다고 알려 주는 방법입니다. 이스케이프 시퀀스는 항상 백슬래시 문자(`\`)로 시작됩니다. 일반 표현식 엔진은 메타 문자 앞에 백슬래시(메타 문자라고도 함)를 배치하여 이스케이프 처리된 메타 문자를 문자 그대로 해석합니다. 예를 들어 메타 문자 기간(`.`)을 일치시키려면 이스케이프 시퀀스를 사용해야 합니다. 그러나 168.196.0.11 문자열의 점 중 하나를 일치시키려면 백슬래시와 마침표(`\.`)로 구성된 정규 표현식을 사용할 수 있습니다. |
| 패턴 | 일반 표현식의 축약입니다. 본질적으로 정규 표현식은 대상 문자열과 일치시키려는 패턴입니다. |
| Target 문자열 | 이 용어는 원하는 패턴을 찾기 위해 검색하는 문자열을 나타냅니다. |

## 문자 일치 정보 {#section-ec4497e3160c47ba9b828d939761b3e0}

리터럴 일치는 이스케이프 문자가 없는 리터럴 문자열을 가져와서 대상 문자열의 하위 문자열인지 확인합니다.

이 예에서는 문자 일치를 적용하는 방법을 확인할 수 있습니다. 웹 사이트 트래픽에서 데이터가 수집되고 cs(referrer) 필드에 다음 값이 포함되어 있는 경우를 생각해 보십시오.

`http://www.abc.com/adventurenews/today.html?ad=123AZ45`

레퍼러가 광고 중 하나를 클릭한 사람을 나타내는지 여부를 결정하려면 레퍼러에 문자열 광고가 포함되어 있는지 확인해야 합니다. 간단히 리터럴 문자열 광고를 사용하여 대상 문자열을 검색하고 트래픽을 사이트로 라우팅하는 데 광고가 사용되었는지 확인할 수 있습니다. 이 문자열이 대상 문자열과 일치하지만 두 위치에서 일치하므로 모호하므로 잘못된 양성으로 이어질 수 있습니다.

다음 URL에는 두 개의 다른 위치에 있는 문자열 광고가 포함됩니다.

`http://www.abc.com/ad vertnews/today.html?ad =123AZ45`

따라서 특정 광고 캠페인의 결과로 시작된 세션을 결정하려는 경우, 문자 광고를 정규식으로 사용하기만 하면 충분하지 않습니다. 리터럴을 &quot;ad=&quot;로 변경하면 이러한 모호성이 제거되고 식이 하나만 일치하게 됩니다. 하지만 레퍼러가 광고 캠페인의 일부인지 확인하기에는 충분하지 않을 수 있습니다. 다음 레퍼러를 고려해 보십시오.

`http://www.xyz.com/hello.html?pad=something`

다른 사용자가 사이트에 대한 링크를 만드는 데 사용할 수 있는 URL에 대한 제어 권한은 없습니다. 문자 일치 기능은 광고 캠페인의 결과로 시작된 세션을 찾는 메커니즘이 너무 간단합니다. 다음 섹션에서는 보다 유연하고 강력한 일치를 위해 메타 문자를 사용하는 방법에 대해 설명합니다.

## 메타 문자 사용 {#section-e29a804336304ea1ba33d40d60139aa2}

메타 문자는 다른 문자에 대한 정보를 제공하는 프로그램 또는 데이터 필드의 특수 문자입니다.

| 메타 문자 | description |
|---|---|
| . (점) | 단일 문자와 일치합니다. 예: `re:x.z` &quot;xyz&quot; 또는 &quot;xxz&quot;와 일치합니다. |
| * (별) | 하나 이상의 문자와 일치합니다. 예: `re:Z*` &quot;ZZZ&quot;와 일치합니다. |
| ? (와일드카드) | 이전 식의 0 또는 1과 일치하여 최소값 일치를 적용합니다. 예: `xy?z` &quot;xy&quot; 및 &quot;xyz&quot;와 일치합니다. |

추가적인 일반 표현식을 사용하여 더 복잡한 검색 문자열을 만들 수도 있습니다.

**목록, 범위 및 OR**

리터럴 일치를 사용하면 단일 문자열을 찾을 수 있지만 대괄호, 대시 및 파이프를 사용하면 대상 문자열에서 찾을 개체 목록을 정의할 수 있습니다.

<table id="table_18B86955EC3748079E7C176273ADE92B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 메타 문자.. </th> 
   <th colname="col2" class="entry"> 정규 표현식 프로세서는 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 대괄호([ ]) </td> 
   <td colname="col2"> 대괄호 안의 모든 문자와 단일 문자 위치를 일치시킵니다. 예를 들어, [AB]는 문자 A나 문자 B와 일치하는 명령이며 [0123456789]는 0에서 9 사이의 모든 문자와 일치하는 명령입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 대시(-) </td> 
   <td colname="col2"> <p>문자 범위를 일치시킵니다. 따라서 [0123456789]를 쓰는 대신 [0-9]만 입력하면 됩니다. </p> <p> 이 범위는 하나의 대괄호 안에 있는 문자 범위 및 여러 범위로 확장할 수 있습니다. 예를 들어 [0-9A-C]는 0에서 9까지의 문자와 A에서 C 사이의 문자와 일치합니다. </p> <p> <p>참고: 대괄호 안에 있는 문자(-)로 대시(-)를 테스트하려면 첫 번째 또는 마지막에 와야 합니다. 예: [-0-9]은 - 및 0-9에 대해 테스트합니다. </p> </p> </td> 
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
| 수업`[A-Z]` | 레슨 a | 소문자 a가 대문자 A에서 Z까지의 범위에 있지 않기 때문에 일치하지 않습니다. |

**부정**

부정은 주어진 문자를 제외한 모든 문자와 일치한다고 말하는 방법입니다. 대괄호 안의 첫 번째 문자인 곡절 메타문자(곡절 또는 삽입 기호`^`)는 대괄호 안의 나머지 문자를 제외한 모든 문자를 일치로 사용합니다. 예를 들어, 세미콜론(`;`)을 제외한 모든 문자와 일치시키려면

[`^;`]

세미콜론을 제외한 모든 문자와 일치합니다.

**포지셔닝**

대상 문자열의 시작 또는 끝에 일치를 적용하려면 두 메타 문자 중 하나가 사용됩니다.

| 이 메타 문자.. | 정규 표현식 프로세서는 |
|---|---|
| 곡절 또는 삽입 기호(`^`) | 문자열의 시작 부분과 일치합니다. 예를 들어 ^`[Tt]`그는 대상 문자열 &quot;The Beginning&quot;과 일치하지만 &quot;This is the beginning&quot;과 일치하지 않습니다. |
| 달러 기호 (`$`) | 문자열 끝과 일치합니다. 예를 들어 `[Ee]`nd$는 &quot;This is the end&quot;와 일치하지만 &quot;The end is a special time&quot;과 일치하지 않습니다. |

>[!NOTE]
>
>정규 표현식의 시작 부분에 ^이 있고 끝에 $ 가 있으면 전체 대상 문자열이 정규 표현식과 일치해야 합니다.

**일치하는 항목**

마침표(.) 는 대상 문자열의 모든 문자와 일치하는 특수 메타 문자입니다. 예를 들어, 정규 표현식은 정확히 세 문자 길이의 모든 대상 문자열과 `^…$` 일치합니다. 정규 표현식 &quot;..&quot;은 3자 이상이 포함된 모든 대상 문자열과 일치합니다.

**반복 패턴**

반복 메타 문자를 사용하면 패턴을 두 번 이상 일치시킬 수 있습니다.

<table id="table_6A14333D6C264A48ADF1EBBAF687CADD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 메타 문자.. </th> 
   <th colname="col2" class="entry"> 정규 표현식 프로세서는 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 물음표(?) </td> 
   <td colname="col2"> 메타 문자(?) 바로 앞의 문자에서 인스턴스나 한 인스턴스에 일치시키지 않습니다. 예를 들어 패턴 rea?d는 빨간색과 읽기와 일치합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 별표 (*) </td> 
   <td colname="col2"> 메타 문자(*) 바로 앞의 문자 발생을 0개 이상 일치시킵니다. 예를 들어 패턴 [0-9]*은 0부터 9까지의 모든 문자(정수)와 일치합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Plus (+) </td> 
   <td colname="col2"> 이전 문자 또는 범위의 항목을 하나 이상 일치시킵니다. 예를 들어 3+의 패턴은 3과 일치하지만 통과는 일치하지 않습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> {n} </td> 
   <td colname="col2"> <p>진행 문자 또는 범위를 정확하게 n번 일치시킬 수 있습니다. 다음 패턴은 미국 전화 번호와 일치합니다. <code>[0-9]{3}-[0-9]{3}-[0-9]{4}</code>. </p> <p> 최적의 패턴이 아닌 경우 대상 문자열이 올바른 형식인지 확인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> {n,m} </td> 
   <td colname="col2"> 이전 문자와 최소 n회 이상 일치하는 항목을 찾습니다. 예를 들어, {1,2}d는 음식과 음식은 일치하지만 음식은 일치하지 않습니다. </td> 
  </tr> 
 </tbody> 
</table>

## 패턴 추출 {#section-4389779653b64f6cb7c47615b25c1a79}

패턴 일치는 일반 표현식의 힘 중 일부에 불과합니다. 정규 표현식은 대상 문자열의 키 부분을 추출하는 메커니즘을 제공합니다. 이것은 왼쪽 및 오른쪽 괄호를 사용하여 수행됩니다. 이러한 추출은 일반적으로 다른 프로세스에 대한 입력으로 사용되며 *%position%*(위치)을 사용하여 액세스합니다. 여기서 position은 괄호 집합이 일치하는 수를 참조하는 정수입니다.

다음 패턴 추출 예를 생각해 보십시오.

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
   <td colname="col2"> 레슨 a </td> 
   <td colname="col3"> 소문자 a가 대문자 A에서 Z까지의 범위에 있지 않기 때문에 일치 안 함 </td> 
   <td colname="col4"> </td> 
  </tr> 
 </tbody> 
</table>

