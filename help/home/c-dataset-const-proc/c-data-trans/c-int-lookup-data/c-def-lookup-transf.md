---
description: 조회 데이터를 데이터 집합에 통합하는 데 사용할 수 있는 변형에 대한 정보입니다.
title: 조회 변환 정의
uuid: 4f7358b1-9e6a-4d03-b0c6-411e454fc11e
exl-id: 7b1504be-8669-4340-8400-e33f9663b602
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '2288'
ht-degree: 2%

---

# 조회 변환 정의{#defining-lookup-transformations}

{{eol}}

조회 데이터를 데이터 집합에 통합하는 데 사용할 수 있는 변형에 대한 정보입니다.

데이터 집합 구성 프로세스의 두 단계에서 모든 유형을 사용할 수는 없습니다.

* [분류](../../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-def-lookup-transf.md#section-8474376c14e54d14ae73749696ada468)
* [플랫 파일 조회](../../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-def-lookup-transf.md#section-e09b2eeb96444a859b14f03cdaab31f2)
* [ODBCLookup](../../../../home/c-dataset-const-proc/c-data-trans/c-int-lookup-data/c-def-lookup-transf.md#section-4dcc3747e42e45c0a057e85f308a83cc)

## 분류 {#section-8474376c14e54d14ae73749696ada468}

다음 [!DNL Categorize] 변환에서는 패턴-문자열/값 쌍으로 구성된 두 열 조회 테이블을 사용합니다. 이 변형 중에 Data Workbench 서버는 각 이벤트 데이터 레코드를 차례로 읽고 레코드의 지정된 필드의 내용을 조회 테이블의 첫 번째 열에 나열된 각 패턴 문자열과 비교합니다. 지정된 필드가 패턴 문자열 중 하나와 일치하는 경우 Data Workbench 서버는 해당 패턴 문자열과 연결된 값(두 번째 열에 있음)을 레코드의 지정된 출력 필드에 기록합니다.

조회 테이블의 첫 번째 열에 있는 문자열은 선택적으로 $ 문자에서 ^문자 및/또는 끝을 사용하여 시작 및/또는 끝에서 일치를 강제 적용할 수 있습니다. 이 변환에서는 첫 번째 열에서 일치 조건을 정의하기 위한 정규 표현식을 허용하지 않습니다. 입력 값이 문자열의 벡터인 경우 각 문자열은 변환을 통해 실행되며 결과는 출력 문자열 벡터에 추가됩니다.

A [!DNL Categorize] 일반적으로 변형을 사용하는 것보다 쉽고 빠르게 [!DNL Regular Expression] 같은 것을 성취하기 위한 변화.

>[!NOTE]
>
>에서 사용되는 하위 문자열 테스트입니다 [!DNL Categorize] 는 대/소문자를 구분하지 않습니다. [!DNL Case Sensitive] 매개 변수.

<table id="table_1773344FAAE34BD4919CC4414249FDEE"> 
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
   <td colname="col1"> 대/소문자 구분 </td> 
   <td colname="col2"> True 또는 False입니다. 하위 문자열 테스트가 대/소문자를 구분하는지 여부를 지정합니다. </td> 
   <td colname="col3"> true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 댓글 </td> 
   <td colname="col2"> 선택 사항. 변환에 대한 참고 사항. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 이 변환이 적용되는 조건입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기본값 </td> 
   <td colname="col2"> 조건 테스트가 전달되고 분류 파일의 항목이 입력과 일치하지 않거나 입력 필드가 주어진 로그 항목에 정의되지 않은 경우 사용할 기본값입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 구분 기호 </td> 
   <td colname="col2"> <p>조회 파일에서 열을 구분하는 데 사용되는 문자열입니다. 길이는 단일 문자여야 합니다. </p> <p> Ctrl 키를 누른 채 구분 기호 매개 변수 내에서 마우스 오른쪽 단추를 클릭하면 <span class="wintitle"> 삽입</span> 메뉴가 나타납니다. 이 메뉴에는 구분 기호로 자주 사용되는 특수 문자 목록이 포함되어 있습니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 여러 값 </td> 
   <td colname="col2"> True 또는 False입니다. true인 경우 파일의 여러 행이 입력과 일치하면 각 일치하는 값이 문자열의 출력 벡터에 추가됩니다. false인 경우 파일의 첫 번째 일치 행만 출력에 사용됩니다. 후자의 경우, 입력이 벡터인 경우, 출력은 동등한 길이의 벡터이기도 합니다. 입력이 간단한 문자열이면 출력은 간단한 문자열이기도 합니다. </td> 
   <td colname="col3"> false </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 파일 </td> 
   <td colname="col2"> 분류 파일의 경로 및 파일 이름입니다. 상대 경로는 Data Workbench 서버의 설치 디렉토리에 대한 것입니다. 이 파일은 일반적으로 Data Workbench 서버 설치 디렉토리 내의 조회 디렉토리에 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> 분류 파일은 이 필드의 값과 해당 하위 문자열을 일치시켜 파일에서 일치하는 행을 식별합니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> 결과와 연결된 필드의 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

**분류 고려 사항**

* 의 조회 파일 변경 [!DNL Categorize] 에 정의된 변형 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일을 다시 변환해야 데이터 세트가 있습니다. 조회 파일 [!DNL Categorize] 에 정의된 변형 [!DNL Log Processing.cfg] 파일 또는 [!DNL Log Processing Dataset Include] 파일에는 이 제한이 적용되지 않습니다. 데이터 재처리에 대한 자세한 내용은 [재처리 및 재변형](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

* [!DNL Categorize] 에 정의된 변형 [!DNL Log Processing.cfg] 파일 또는 [!DNL Log Processing Dataset Include] 조회 파일이 변경될 때마다 파일이 조회 파일을 다시 로드합니다. 변경 사항은 소급적용되지 않지만 변경 사항이 발생한 후 읽은 모든 로그 데이터에 적용됩니다.

이 예에서는 [!DNL Categorize] 변환: 조회 데이터를 웹 사이트 트래픽에서 수집된 이벤트 데이터와 통합합니다. 특정 웹 사이트에 비즈니스 섹션이 있고 다른 섹션에서 생성한 트래픽 흐름과 값에 따라 확인하고 비교할 수 있어야 한다고 가정합니다. 이러한 서로 다른 섹션을 식별하는 데 사용되는 하위 문자열을 나열하는 조회 파일을 만들 수 있습니다.

조회 파일 [!DNL Lookups\custommap.txt] 에는 다음 테이블이 포함되어 있습니다.

| /products/ | 제품 |
|---|---|
| ^/sports/ | 스포츠 |
| ^/뉴스/ | 뉴스 |
| ... | ... |

이 분류 파일은 문자열 &quot;/products/&quot;를 포함하는 모든 항목을 &quot;Products&quot; 값에, &quot;/sports/&quot;로 시작하는 모든 항목을 &quot;Sports&quot; 값에, &quot;/news/&quot;로 시작하는 모든 항목을 &quot;News&quot; 값에 매핑합니다. 다음 분류 변환에서는 cs-uri-stem 필드의 값을 일치하는 하위 문자열을 찾는 문자열로 사용합니다. 변형 결과는 x-custommap 필드에 배치됩니다.

![](assets/cfg_TransformationType_Categorize.png)

복수 값(Multiple Values) 매개 변수가 false로 설정된다고 가정할 경우, 이 예는 cs-uri-stem에 대해 나열된 값을 기준으로 x-custommap에 대해 다음 값을 생성합니다.

| [!DNL cs-uri-stem] | [!DNL x-custommap] |
|---|---|
| [!DNL /sports/news/today.php] | 스포츠 |
| [!DNL /sports/products/buy.php] | 제품 |
| [!DNL /news/headlines.php] | 뉴스 |
| [!DNL /news/products/subscribe.php] | 제품 |

출력은 조회 파일의 하위 문자열 순서를 기반으로 합니다. 예를 들어, cs-uri-stem [!DNL /sports/products/buy.php] 는 &quot;products&quot;를 반환합니다. URI 줄기가 &quot;/sports/&quot;로 시작하지만, 문자열 &quot;/products/&quot;가 조회 파일의 &quot;/sports/&quot; 앞에 나열됩니다. Multiple Values 매개 변수가 true로 설정된 경우 마지막 예제가 조회 테이블의 두 행과 일치하므로 x-custommap에 대한 추가 값이 있습니다. 제품 및 뉴스.

## 플랫 파일 조회 {#section-e09b2eeb96444a859b14f03cdaab31f2}

다음 [!DNL FlatFileLookup] 변환에서는 여러 열과 행으로 구성된 조회 테이블을 사용합니다(하지만 이 테이블이 메모리에 있으면 기억함). 이 유형의 변형 중에 Data Workbench 서버는 각 이벤트 데이터 레코드를 차례로 읽고 레코드의 지정된 필드의 내용을 조회 테이블의 지정된 열에 있는 각 값과 비교합니다. 일치하는 항목이 있으면 Data Workbench 서버는 조회 테이블의 대응 행에서 이벤트 데이터 레코드에 있는 하나 이상의 지정된 출력 필드에 하나 이상의 값을 기록합니다.

이 변형 중에 사용된 조회 테이블은 변형을 정의할 때 지정하는 위치의 플랫 파일에서 채워집니다.

<table id="table_772B8ABF3B44493F99069010DDB5F77A"> 
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
   <td colname="col2"> 선택 사항. 변환에 대한 참고 사항. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 이 변환이 적용되는 조건입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기본값 </td> 
   <td colname="col2"> 조건이 충족되고 조회 파일의 항목이 입력과 일치하지 않는 경우 사용할 기본값입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 구분 기호 </td> 
   <td colname="col2"> <p>조회 파일에서 열을 구분하는 데 사용되는 문자열입니다. 길이는 단일 문자여야 합니다. </p> <p> Ctrl 키를 누른 채 구분 기호 매개 변수 내에서 마우스 오른쪽 단추를 클릭하면 <span class="wintitle"> 삽입</span> 메뉴가 나타납니다. 이 메뉴에는 구분 기호로 자주 사용되는 특수 문자 목록이 포함되어 있습니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 파일 </td> 
   <td colname="col2"> 조회 파일의 경로 및 파일 이름입니다. 상대 경로는 Data Workbench 서버의 설치 디렉토리에 대한 것입니다. 이 파일은 일반적으로 Data Workbench 서버 설치 디렉토리 내의 조회 디렉토리에 있습니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 머리글 행 </td> 
   <td colname="col2"> True 또는 False입니다. 표의 첫 번째 행이 처리 시 무시할 머리글 행임을 나타냅니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 </td> 
   <td colname="col2"> <span class="wintitle"> 열 이름</span> 은 파일의 행에 입력을 일치시키는 데 사용되는 열의 이름입니다. 헤더 행이 true인 경우 조회 파일에서 열의 이름이 될 수 있습니다. 그렇지 않으면 0부터 시작하는 열 번호여야 합니다. <span class="wintitle"> 필드 이름</span> 는 조회 파일에서 행을 찾는 데 사용되는 필드의 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 여러 값 </td> 
   <td colname="col2"> <p>True 또는 False입니다. 단일 값(일치하는 행) 또는 여러 값을 반환할지(일치하는 각 행에 대해 하나씩) 결정합니다. </p> <p> <p>참고: If <span class="wintitle"> 여러 값</span> 가 false로 설정되어 있으면 일치하는 항목이 여러 개 없는지 확인해야 합니다. 여러 일치 항목이 발생하면 어떤 일치 항목이 반환되는지 확인되지 않습니다. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 </td> 
   <td colname="col2"> <p>각 객체가 열 및 필드 이름으로 정의된 열 객체(결과)의 벡터입니다. </p> <p> <span class="wintitle"> 열 이름</span> 은 출력 값을 가져오는 열입니다. If <span class="wintitle"> 머리글 행</span> true인 경우 조회 파일에서 열의 이름이 될 수 있습니다. 그렇지 않으면 0부터 시작하는 열 번호여야 합니다. </p> <p> <span class="wintitle"> 필드 이름</span> 은 출력을 캡처하는 데 사용되는 필드의 이름입니다. 복수 값 매개 변수가 true인 경우 식별된 각 행에 대해 하나씩, 결과 벡터일 수 있습니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

**고려 사항[!DNL FlatFileLookup]**

* 입력 필드를 조회 파일에 일치시키는 것은 항상 대/소문자를 구분합니다.
* 의 조회 파일 변경 [!DNL FlatFileLookup] 에 정의된 변형 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일은 데이터 집합을 다시 변환해야 합니다. 조회 파일 [!DNL FlatFileLookup] 에 정의된 변형 [!DNL Log Processing.cfg] 파일 또는 [!DNL Log Processing Dataset Include] 파일은 이 제한을 받지 않습니다. 데이터 재처리에 대한 자세한 내용은 [재처리 및 재변형](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

* [!DNL FlatFileLookup] 변형 [!DNL Log Processing.cfg] 파일 또는 [!DNL Log Processing Dataset Include] 조회 파일이 변경될 때마다 파일이 조회 파일을 다시 로드합니다. 변경 사항은 소급적용되지 않지만 변경 사항이 발생한 후 읽은 모든 로그 데이터에 적용됩니다.

이 예에서는 [!DNL FlatFileLookup] 변환: 조회 데이터를 웹 사이트 트래픽에서 수집된 이벤트 데이터와 통합합니다. 웹 사이트로 트래픽을 라우팅하는 웹 사이트 파트너를 분리하고 해당 파트너 ID를 보다 친숙한 이름으로 변환한다고 가정합니다. 그런 다음 사용자에게 친숙한 이름을 사용하여 라우팅 트래픽에 사용되는 사이트 간 관계보다 비즈니스 관계에 더 명확하게 매핑되는 확장 차원 및 시각화를 만들 수 있습니다.

예제 변환은 cs(referrer-query) 필드에서 PartnerID 이름-값 쌍을 검색하고, 찾은 경우 조회 파일을 검색합니다 [!DNL Lookups\partners.txt] 는 PartnerID 값을 [!DNL Partner] 표의 열 행이 있으면 출력 필드 x-partner-name에 [!DNL PrintName] 식별된 행의 열.

![](assets/cfg_TransformationType_FlatFileLookup.png)

조회 테이블에 다음 정보가 포함된 경우:

| ID | 파트너 | 시작됨 | PrintName |
|---|---|---|---|
| 1 | P154 | 1999년 8월 21일 | Yahoo |
| 2 | P232 | 2000년 7월 10일 | Microsoft |
| 3 | P945 | 2001년 1월 12일 | Amazon |

다음 예제는 다음과 같이 변형됩니다.

* cs(referrer)(PartnerID)가 P232를 반환하면 x-partner-name 필드에 &quot;Microsoft&quot; 값이 지정됩니다.
* cs(referrer)(PartnerID)가 P100을 반환하면 x-partner-name 필드에 &quot;No Partner&quot; 값이 지정됩니다.
* cs(referrer)(PartnerID)에서 아무 것도 반환하지 않은 경우 x-partner-name 필드에 Default 매개 변수에 지정된 대로 &quot;No Partner&quot; 값이 지정됩니다.

## ODBCLookup {#section-4dcc3747e42e45c0a057e85f308a83cc}

다음 [!DNL ODBCLookup] 변형은 마치 [!DNL FlatFileLookup] 변환. 유일한 차이는 이 변형 중에 사용된 조회 테이블이 플랫 파일이 아닌 ODBC 데이터베이스에서 채워진다는 것입니다.

>[!NOTE]
>
>[!DNL ODBCLookup] 변형은 데이터 집합 구성 프로세스의 변형 단계 동안에만 실행할 수 있습니다. 가능하면 Adobe은 [!DNL FlatFileLookup] 변환 대신 [!DNL ODBCLookup] 변환. [!DNL FlatFileLookup] 변형은 본질적으로 더 신뢰적입니다. 왜냐하면 외부 시스템의 가용성에 의존하지 않기 때문입니다. 또한 조회 테이블이 로컬에서 제어하는 플랫 파일에 있는 경우 조회 테이블이 수정될 위험이 줄어듭니다.

<table id="table_B903DB291BCC4F44B09D54300216D288"> 
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
   <td colname="col2"> 선택 사항. 변환에 대한 참고 사항. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 조건 </td> 
   <td colname="col2"> 이 변환이 적용되는 조건입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 데이터 소스 이름 </td> 
   <td colname="col2"> 데이터 집합이 처리되는 Data Workbench 서버 시스템의 관리자가 제공하는 DSN으로서 데이터가 로드될 데이터베이스를 참조합니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 데이터베이스 암호 </td> 
   <td colname="col2">데이터베이스에 연결할 때 사용할 암호입니다. DSN에 대해 암호를 구성한 경우 <span class="wintitle"> 데이터 소스 관리자</span>: 비워 둘 수 있습니다. 여기에서 제공된 모든 암호는 <span class="wintitle"> 데이터 소스 관리자</span>. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 데이터베이스 사용자 ID </td> 
   <td colname="col2">데이터베이스에 연결할 때 사용할 사용자 ID입니다. 사용자 ID가 <span class="wintitle"> 데이터 소스 관리자</span>: 비워 둘 수 있습니다. 여기에서 제공된 모든 사용자 ID는 DSN에 대해 구성된 사용자 ID를 <span class="wintitle"> 데이터 소스 관리자</span>. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 기본값 </td> 
   <td colname="col2"> 조건이 충족되고 조회 파일의 항목이 입력과 일치하지 않는 경우 사용할 기본값입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 입력 열 </td> 
   <td colname="col2"> <span class="wintitle"> 열 이름</span> 입력과 일치하는 데이터의 열 이름 또는 SQL 표현식입니다. <span class="wintitle"> 필드 이름</span> 는 조회할 데이터가 포함된 필드의 이름입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 여러 값 </td> 
   <td colname="col2"> <p>True 또는 False입니다. 단일 값(일치하는 행) 또는 여러 값을 반환할지(일치하는 각 행에 대해 하나씩) 결정합니다. </p> <p> <p>참고: If <span class="wintitle"> 여러 값</span> 가 false로 설정되어 있으면 일치하는 항목이 여러 개 없는지 확인해야 합니다. 여러 일치 항목이 발생하면 어떤 일치 항목이 반환되는지 확인되지 않습니다. </p> </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 출력 열 </td> 
   <td colname="col2"> <p>각 객체가 열 및 필드 이름으로 정의된 열 객체(결과)의 벡터입니다. </p> <p> <span class="wintitle"> 열 이름</span> 은 출력 값을 가져오는 열의 또는 SQL 표현식의 이름입니다. <span class="wintitle"> 필드 이름</span> 은 출력을 캡처하는 데 사용되는 필드의 이름입니다. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> 테이블 식별자</span> </td> 
   <td colname="col2"> 데이터를 로드할 테이블 또는 뷰의 이름을 지정하는 SQL 식입니다. 일반적인 테이블 식별자는 SCHEMA.TABLE 형식입니다. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

* 데이터 소스 이름, [!DNL Database User ID], [!DNL Database Password]및 테이블 식별자 매개 변수는 ODBC 데이터 소스에 대해 설명된 것과 동일한 이름의 매개 변수와 동일합니다. 자세한 내용은 [ODBC 데이터 소스](../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3).

* ODBC 데이터 소스와 달리, [!DNL ODBCLookup] 변형에는 ID 열을 늘릴 필요가 없습니다. 자세한 내용은 [ODBC 데이터 소스](../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-odbc-data-sources.md#concept-5f2cf635081d44beab826ef5ec8cf4e3). 데이터 세트가 활성화된 동안에는 조회 테이블의 내용을 변경해서는 안 되기 때문입니다. 다시 변환이 발생하기 전까지 조회 테이블 또는 뷰의 변경 내용을 검색할 수 없습니다. 데이터 재처리에 대한 자세한 내용은 [재처리 및 재변형](../../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

오래된 DNS 레코드를 업데이트된 레코드로 변환한다고 가정합니다. 두 레코드 집합은 모두 SQL 데이터베이스에 저장됩니다. 이 작업을 수행하려면 데이터베이스에서 생성된 조회 테이블을 참조하고 오래된 DNS 레코드를 바꿉니다.

예제 변환은 로그 항목에서 s-dns 필드를 검색하고, 찾을 경우 조회 테이블 VISUAL.LOOKUP을 사용하여 s-dns 항목을 의 항목과 비교합니다 [!DNL OLDDNS] 표의 열 행이 테이블에 있으면 출력 필드 s-dns에 [!DNL NEWDNS] 식별된 행의 열.

![](assets/cfg_TransformationType_ODBCLookup.png)
